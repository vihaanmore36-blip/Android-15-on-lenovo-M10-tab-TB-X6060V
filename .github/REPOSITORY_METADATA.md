Repository metadata and instructions

This file contains a suggested one-line repository description and a set of topics you can add to the repository to improve discoverability. It also includes copy-paste commands you can use to set the description/topics from the command line.

Suggested short description (copy to repo Description field):
Unofficial notes for flashing an Android 15 GSI on the Lenovo M10 TB-X6060V (DO NOT FLASH — this repo contains no images).

Suggested topics (list)
- android-gsi
- lenovo-m10
- tb-x6060v
- android-15
- device-port

Set description using gh (GitHub CLI)
- gh repo edit vihaanmore2011-sudo/Android-15-on-lenovo-M10-tab-TB-X6060V --description "Unofficial notes for flashing an Android 15 GSI on the Lenovo M10 TB-X6060V (DO NOT FLASH — this repo contains no images)."

Set topics using the GitHub Topics API (curl)
- Replace $GITHUB_TOKEN with a token that has repo scope.

curl -X PUT \
  -H "Accept: application/vnd.github+json" \
  -H "Authorization: Bearer $GITHUB_TOKEN" \
  https://api.github.com/repos/vihaanmore2011-sudo/Android-15-on-lenovo-M10-tab-TB-X6060V/topics \
  -d '{"names":["android-gsi","lenovo-m10","tb-x6060v","android-15","device-port"]}'

Notes
- The gh CLI must be installed and authenticated for the gh command to work.
- Topics set through the API replace the full topic list; include any existing topics you want to keep.
