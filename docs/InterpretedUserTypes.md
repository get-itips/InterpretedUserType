
| InterpretedUserType | Possible Description |
|------- | -------------------- |
|AADConnectDisabledOnlineActiveDirectoryDisabledUser||
|AADConnectDisabledOnlineActiveDirectoryDisabledUserPendingDeletionFromAD||
|AADConnectDisabledOnlineSfBUserWithTeamsLicensePendingDeletionFromAD||
|AADConnectDisabledOnlineTeamsUserPendingDeletionFromAD||
|AADConnectDisabledOnlineTeamsUser||
|AADConnectDisabledOnlineUserNotLicensedForServicePendingDeletionFromAD||
|AADConnectDisabledOnlineUserNotLicensedForService||
|AADConnectEnabledOnlineActiveDirectoryDisabledUserPendingAttributeRemovalFromAD||
|AADConnectEnabledOnlineActiveDirectoryDisabledUser||
|AADConnectEnabledOnlineSfBUserWithTeamsLicense||
|AADConnectEnabledOnlineSfBUserWithTeamsLicenseWithMCOValidationError||
|AADConnectEnabledOnlineTeamsOnlyUserNotLicensedForServiceInPDLPendingAttributeRemovalFromAD||
|AADConnectEnabledOnlineSfBUser||
|AADConnectEnabledOnlineTeamsUserNeedsProvisioningToAD||
|AADConnectEnabledOnlineTeamsUserWithMCOValidationError||
|AADConnectEnabledOnlineTeamsUser||
|AADConnectEnabledOnlineUserNotLicensedForServiceNeedsProvisioningToAD||
|AADConnectEnabledOnlineUserNotLicensedForServiceNotInPDL||
|AADConnectEnabledOnlineUserNotLicensedForServicePendingAttributeRemovalFromAD||
|AADConnectEnabledOnlineUserNotLicensedForService||
|AADConnectEnabledSfBUserWithTeamsLicenseNeedsProvisioningToAD||
|DirSyncDisabledDisabledUser| User account disabled in SfB online and disabled in local AD, has a sipAddress attribute online, RegistrarPool has a value.|
|DirSyncDisabledNoService| User account disabled in SfB online and does not have a sipAddress attribute online, RegistrarPool empty, OnPremHostingProvider shows sipfed.online.lync.com.|
|DirSyncDisabledSfBUser| User account disabled in SfB online and has a sipAddress attribute online, also, has a RegistrarPool value and OnPremHostingProvider is empty.|
|DirSyncDisabledUser| User account disabled in SfB online and disabled in local AD, does not have a RegistrarPool value.|
|DirSyncNoService| To this day, I still do not know exactly what that means.|
|DirSyncSfBUserNeedsProvisioning| This appears to be a temporal state before DirSyncSfBUser|
|DirSyncSfBUser| Enabled in SfB Online, has a SipAddress and has a RegistrarPool, this is the best value we can get.|
|EnabledUserWithNoService|Active users without any license|
|EnabledUserWithTeamsLicense|Active users with Teams license|
|HybridOnlineDisabledUserNeedsProvisioning| User account disabled in SfB online, hasn't a SipAddress attribute online and OnPremHostingProvider is not empty.|
|HybridOnlineDisabledUserWithDeletedLicenses| It's like HybridOnlineDisabledUser but, it seems that license is not assigned.|
|HybridOnlineDisabledUser| User account disabled in SfB online, has a SipAddress attribute online and OnPremHostingProvider is not empty.|
|HybridOnlineSfBUserWithDeletedLicenses| Same as HybridOnlineSfBUser but judging by the name, it seems that license is not present.|
|HybridOnlineSfBUserWithTeamsLicense||
|HybridOnlineTeamsOnlyUserNeedsProvisioningToAD||
|HybridOnlineSfBUser| User account enabled and DirSynched, has a SipAddress and a OnPremHostingProvider and RegistrarPool.|
|HybridOnpremActiveDirectoryDisabledUser||
|HybridOnpremActiveDirectoryDisabledUserWithMCOValidationError||
|HybridOnpremDisabledUser| User account disabled in SfB OnPrem, OnPremHostingProvider has "SRV:" value and RegistrarPool is empty.|
|HybridOnpremSfBUserWithMCOValidationError||
|HybridOnpremSfBUserWithTeamsLicense||
|HybridOnpremSfBUserWithTeamsLicenseWithMCOValidationError||
|HybridOnpremSfBUser| According to Johan Delimon's Blog, the account is created at Customer AD, DirSynched and uses SfB OnPrem, we can judge this by the presence of OnPremHostingProvider.|
|HybridOnpremUserNotLicensedForService||
|PureOnlineActiveDirectoryDisabledUserPendingAttributeRemovalFromAD||
|PureOnlineActiveDirectoryDisabledUser||
|PureOnlineApplicationInstance||
|PureOnlineEnabledUserWithNoService||
|PureOnlineEnabledUserWithSfBAndTeamsLicense||
|PureOnlineEnabledUserWithTeamsLicense||
|PureOnlineNoServiceWithDeletedLicenses| User account created in Office 365, has no local AD account, so is not DirSynched, has no SfB license.|
|PureOnlineNoService| I still do not know exactly what that means.|
|PureOnlineSfBUserWithTeamsLicense||
|PureOnlineSfBUser| User account created in Office 365, has no local AD account, so is not DirSynched, and uses SfB Online.|
|PureOnlineTeamsOnlyUserFailedProvisioningToBVD|Enterprise Voice is enabled, and a number is added to the user. The number needs to synchronise into Microsoft's Business Voice Directory (BVD). When calls are received to Microsoft SBC's, the BVD is checked to determine which user the call should be routed to.|
|PureOnlineTeamsOnlyUserNeedsProvisioningToAD||
|PureOnlineTeamsOnlyUser||
|PureOnlineTeamsUser||
|PureOnlineUserNotLicensedForServiceFailedPublishingToAAD||
|PureOnlineUserNotLicensedForServicePendingAttributeRemovalFromAD||
|PureOnlineUserNotLicensedForService||
