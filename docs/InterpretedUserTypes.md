
| InterpretedUserType | Possible Description |
|------- | -------------------- |
|DirSyncDisabledDisabledUser| User account disabled in SfB online and disabled in local AD, has a sipAddress attribute online, RegistrarPool has a value
|DirSyncDisabledNoService| User account disabled in SfB online and does not have a sipAddress attribute online, RegistrarPool empty, OnPremHostingProvider shows sipfed.online.lync.com
|DirSyncDisabledSfBUser| User account disabled in SfB online and has a sipAddress attribute online, also, has a RegistrarPool value and OnPremHostingProvider is empty
|DirSyncDisabledUser| User account disabled in SfB online and disabled in local AD, does not have a RegistrarPool value.
|DirSyncNoService| To this day, I still do not know exactly what that means.
|DirSyncSfBUser| Enabled in SfB Online, has a SipAddress and has a RegistrarPool, this is the best value we can get.
|DirSyncSfBUserNeedsProvisioning| This appears to be a temporal state before DirSyncSfBUser
|HybridOnlineDisabledUser| User account disabled in SfB online, has a SipAddress attribute online and OnPremHostingProvider is not empty.
|HybridOnlineDisabledUserNeedsProvisioning| User account disabled in SfB online, hasn't a SipAddress attribute online and OnPremHostingProvider is not empty.
|HybridOnlineDisabledUserWithDeletedLicenses| It's like HybridOnlineDisabledUser but, it seems that license is not assigned.
|HybridOnlineSfBUser| User account enabled and DirSynched, has a SipAddress and a OnPremHostingProvider and RegistrarPool.
|HybridOnlineSfBUserWithDeletedLicenses| Same as HybridOnlineSfBUser but judging by the name, it seems that license is not present.
|HybridOnpremDisabledUser| User account disabled in SfB OnPrem, OnPremHostingProvider has "SRV:" value and RegistrarPool is empty.
|HybridOnpremSfBUser| According to Johan Delimon's Blog, the account is created at Customer AD, DirSynched and uses SfB OnPrem, we can judge this by the presence of OnPremHostingProvider
|PureOnlineNoService| I still do not know exactly what that means.
|PureOnlineNoServiceWithDeletedLicenses| User account created in Office 365, has no local AD account, so is not DirSynched, has no SfB license.
|PureOnlineSfBUser| User account created in Office 365, has no local AD account, so is not DirSynched, and uses SfB Online.
