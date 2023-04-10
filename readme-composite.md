## Error permissions:

That most likely means that your ./.github/scripts/backend_decrypt.sh script doesn’t have the “execute” filesystem permission set. I assume you’re developing on Windows locally, which doesn’t have that kind of permission system.

You can tell git to add the permission anyway with this command:

git update-index --chmod=+x .\.github\actions\composite-action\goodbye.sh
update-index is similar to add in that it adds the change to the index, so you’ll have to commit and push as usual.