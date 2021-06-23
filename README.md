# Sample Playlist Includes Skillet

This is used in the training material as part of the Playlist Includes tutorial.

The solution utilizes three playlists:

1. A full IronSkillet PAN-OS 10.0 configuration
2. An Alert-Only Security Profiles IronSkillet PAN-OS 10.0 configuration
    * only includes Alert-Only Security Profiles
    * the IronSkillet version tag is included for documentation purposes
3. A IronSkillet Not-Shared Panorama 10.0 Security Profiles configuration
    * only includes Security Profiles for a Not-Shared Panorama configuration
    * the IronSkillet version tag is included for documentation purposes

These playlists were based off of some of the playlists in the
[IronSkillet 10.1 branch](https://github.com/PaloAltoNetworks/iron-skillet/tree/panos_v10.1/playlists).
Check out the [README](https://github.com/PaloAltoNetworks/iron-skillet/blob/panos_v10.1/playlists/README.md)
for more information on the playlists and content they contain.

Configuration elements in the playlists pull from the
[ironskillet-components](https://github.com/PaloAltoNetworks/ironskillet-components) submodule, which has several
sub-skillets. All skillet-player tools (PanHandler, SLI, etc.) will be able to read in the snippets from the
sub-skillets in the submodule using the `include_snippets` attribute in the playlists. However, the submodule
has a few steps for upkeep when using content locally.

When cloning this repository, the submodule will need to be initiated and updated before being able to use it.
To do this, run the following commands:
* Clone the repository: `git clone <clone_link>`
* Initiate the submodule: `git submodule init`
* Update the submodule to the latest commit: `git submodule update`

It is also recommended to update the submodule as needed (not done automatically as new commits are released). It
is necessary to commit and push changes in order to see the latest commit pulled into a skillet player. This
can be done using the following steps:
* Open the repository
* Update the submodule: `git submodule update --remote --merge`
* Commit and Push any changes