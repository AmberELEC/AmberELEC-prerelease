Upgrading from a previous beta
Though it is probably easiest to just put a new beta tar in the updates folder and update from an old beta manually, it is possible, with some manual steps, to update from the RG351 device running one of the previous betas to the new beta. This is not possible from the latest stable release. The steps involve setting developer options, so use at your own risk.

Process:

In emulation station, press start -> EmulationStation Settings -> Developer -> Updates -> Github Repo and set it to 351ELEC-beta. This must match case, exactly, etc.
Back on the main menu, go to Updates & Downloads and select Start Update. This should update your as normal.
After updating, make sure to release the Github Repo back to "" (blank) under developer settings otherwise it will break your releases channel (it will attempt to look for releases in 351ELEC-beta which won't have any releases).
Technical Details
Needed to switch to the ncipollo/release-action@v1 release action as the existing github action didn't seem to work to publish to a different repo.
Not included - but in the future we should probably switch the 'draft-release' functionality to that action as well for consistency. Since draft releases publish to the 351ELEC org (in preparation for a real release), it's not required to switch.
Included 'merge' commits in the release notes for the beta releases as there's no real reason to shorten them and it actually makes it easier to find all the PRs.
Also needed to prepend the 351ELEC/351ELEC@ to any git SHA's (release notes) as they are not in the current repository.
Examples
https://github.com/pkegg/351ELEC-beta/releases
