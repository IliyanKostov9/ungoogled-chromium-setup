# Instructions for enabling DRM content

**Note**: This readme is for users, who still experience issues, when trying to play DRM content (example: Spotify), even after enabling the `protected content` in the security options blade. More specifically, this type of issue is  only targeting Linux users, due to Widewine not being installed (possibly due to the security nature of the ungoogled chromium project, that blocks all google domains and inadvertently also blocking Widewine).
This topic has already been discussed: <https://github.com/ungoogled-software/ungoogled-chromium/issues/1831#issuecomment-1076960806>, therefore this instruction manual is a step-by-step guide  of following that referenced comment and mainly targeting the stubborn audience, that don't want to give up on using this awesome browser, without the tracking BS.

## Requirements

1. Install Chrome or Chromium of your choice (you would only need it for a copying a directory, don't worry you don't need to use it)
2. Go to the installation directory (usually in `~/.config/google-chrome`)
3. Inside it, try to find a directory, named `WidevineCdm` (same as my archived example, but most definitely with different version number than mine. You can actually skip step 1 and 2 and just directly use `WidevineCdm.zip`, but I don't recommend you doing that, just because at the moment of you reading this, there should have already been released a new Widevine version, and it's always better to have the latest updates of any type of software)
4. After you locate the directory in question, open a new file explorer or terminal session and navigate to the ungoogled chromium folder (usually in `~/.config/google-chrome`) and please try to verify that in there the `WidevineCdm` directory is empty - if it is, then the DRM issue you're having is most definitely related to this directory being empty
5. Now do an entire copy on the `WidevineCdm` directory from the `google-chrome` config, right in to the `chromium` config - make sure you copy the directory at the same level as the one, that already exists on the `chromium` side (e.g you can freely replace that empty `WidevineCdm` with the other one coming from `google-chrome`)
6. Now you can restart your browser and try if there is any DRM issue. Hope it helps!
