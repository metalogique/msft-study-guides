# Exam MS-302 - Microsoft 365 Teamwork Administrator Certification Transition

If you are preparing for the MS-302 Certification, you can use this study guide. It can probably also be used for MS-300 or MS-301 as much of those exams cover the same topics.

This is provided with no warranty, only as a mean to share and save time to others...

Thanks to https://maruthigadde.com/2019/02/23/ms-300-deploying-microsoft-365-teamwork-learning-guide/ for his guide as it was used in compiling this.

## Configure and Manage SP Online (20-25%)

- Plan and configure site collections and hub sites
    - Identify procedures for creating, deleting, and restoring site collections
        - Admin console: 
          - https://docs.microsoft.com/en-us/sharepoint/create-site-collection
        - Powershell: 
          - https://docs.microsoft.com/en-us/powershell/module/sharepoint-online/?view=sharepoint-ps
    - Assign users or groups as site collection administrators
        - Add-PnpSiteCollectionAdmin -Owners
          - https://docs.microsoft.com/en-us/powershell/module/sharepoint-pnp/add-pnpsitecollectionadmin?view=sharepoint-ps
        - Set-SPOUser -IsSiteCollectionAdmin
          - https://docs.microsoft.com/en-us/powershell/module/sharepoint-online/set-spouser?view=sharepoint-ps
        - Admin console / Site collection parameters
    - Plan and configure navigation
        - https://docs.microsoft.com/en-us/office365/enterprise/navigation-options-for-sharepoint-online
        - https://docs.microsoft.com/en-us/sharepoint/plan-navigation-modern-experience
    - Design site collection and subsites structure
        - https://www.paitgroup.com/blog/modernizing-your-approach-to-site-architecture-in-sharepoint-and-office-365
        - https://docs.microsoft.com/en-us/sharepoint/dev/solution-guidance/portal-information-architecture
        - https://sharepointmaven.com/structure-sites-sharepoint-intranet/
    - Configure site collection settings and features
        - https://support.office.com/en-gb/article/enable-or-disable-site-collection-features-a2f2a5c2-093d-4897-8b7f-37f86d83df04
        - PNP Powershell
          - https://docs.microsoft.com/en-us/powershell/module/sharepoint-pnp/enable-pnpfeature?view=sharepoint-ps
- Plan and configure customizations and apps
    - Plan and configure App Catalog
        - Classic admin center
          - https://docs.microsoft.com/en-us/sharepoint/use-app-catalog
        - Add-SPOSiteCollectionAppCatalog -Site $site
          - https://docs.microsoft.com/en-us/sharepoint/dev/general-development/site-collection-app-catalog
    - Plan and deploy apps with proper permissions and licenses
        - https://docs.microsoft.com/en-us/sharepoint/manage-app-licenses
        - https://docs.microsoft.com/en-us/sharepoint/request-app-installation-permissions
- Plan and configure guest access
    - Assign guest licenses
        - https://answers.microsoft.com/en-us/msoffice/forum/all/assign-a-pro-license-to-a-guest-user-in-o365-admin/f70b2a84-269d-43f4-8890-1d0e65c307a2
    - Configure restricted domains
        - https://docs.microsoft.com/en-us/sharepoint/restricted-domains-sharing
    - Plan and configure guest sharing and site access
        - https://docs.microsoft.com/en-us/office365/admin/create-groups/manage-guest-access-in-groups?view=o365-worldwide
        - Set-SPOTenant -SharingAllowedDomainList
          - https://docs.microsoft.com/en-us/powershell/module/sharepoint-online/Set-SPOTenant?view=sharepoint-ps#parameters
- Manage SharePoint Online
Configure user profile properties
    - Classic admin center
        - https://docs.microsoft.com/en-us/sharepoint/add-and-edit-user-profile-properties
        - Set-AzureADUser
          - https://docs.microsoft.com/en-us/powershell/module/azuread/set-azureaduser?view=azureadps-2.0
    - Archive or delete unused artifacts
    - Site policy and retention
    - Plan for Information Rights Management
        - https://docs.microsoft.com/en-us/azure/information-protection/configure-office365#sharepointonline-and-onedrive-for-business-irm-configuration
    - Modify storage limits for SharePoint Online
        - https://docs.microsoft.com/en-us/powershell/module/sharepoint-online/set-sposite?view=sharepoint-ps
- Monitor and maintain the SharePoint Online service
    - Research, troubleshoot, and resolve reported issues
    - Admin center
    - Monitor service health issues
    - Monitor SharePoint usage and usage patterns
        - https://docs.microsoft.com/en-us/office365/admin/activity-reports/sharepoint-site-usage?view=o365-worldwide

## Configure and Manage OneDrive for Business (20-25%)

- Configure and manage OneDrive for Business
  - Configure settings in the OneDrive for Business admin center
    - https://admin.onedrive.com/
  - Configure external sharing, sync, and storage settings
    - https://docs.microsoft.com/en-us/powershell/module/sharepoint-online/set-spotenantsyncclientrestriction?view=sharepoint-ps
  - Configure device access, notification, and compliance settings
    - https://docs.microsoft.com/en-us/onedrive/use-group-policy
    - https://docs.microsoft.com/en-us/onedrive/control-access-to-mobile-app-features
  - Research, troubleshoot, and resolve reported issues
  - Plan OneDrive for Business silent account configuration
    - https://docs.microsoft.com/en-us/onedrive/use-silent-account-configuration
- Manage users and groups
  - Add and remove admins for a OneDrive account
    - https://docs.microsoft.com/en-us/onedrive/restore-deleted-onedrive
  - Assign a default storage quota
    - https://docs.microsoft.com/en-us/onedrive/set-default-storage-space
  - Configure a retention policy for deleted OneDrive for Business users.
    - https://docs.microsoft.com/en-us/onedrive/retention-and-deletion
- Manage sharing and security
  - Configure data encryption in OneDrive for Business
  - Control access to OneDrive for Business from unmanaged devices
  - Audit sharing activities and view files shared with people outside an organization
- Manage sync security
  - Recommend group policy settings to control OneDrive sync client settings
    - https://docs.microsoft.com/en-us/onedrive/use-group-policy
  - Limit syncing to devices joined to specific domains
    - https://docs.microsoft.com/en-us/onedrive/allow-syncing-only-on-specific-domains
    - https://docs.microsoft.com/en-us/onedrive/control-access-based-on-network-location-or-app
  - Limit syncing to domain-joined or compliant devices
  - Block syncing of specific file types
    - https://docs.microsoft.com/en-us/onedrive/block-file-types
- Monitor and maintain the OneDrive service
  - Research, troubleshoot, and resolve reported issues
    - https://docs.microsoft.com/en-us/onedrive/transition-from-previous-sync-client
    - https://docs.microsoft.com/en-us/office365/securitycompliance/search-the-mailbox-and-onedrive-for-business-for-a-list-of-users
  - Monitor service health issues
  - Monitor OneDrive usage and usage patterns

## Configure and Manage Teams (20-25%)

- Plan and Configure Team settings
  - Configure settings in the Teams admin center,
    - https://docs.microsoft.com/en-us/microsoftteams/enable-features-office-365
    - https://docs.microsoft.com/en-us/powershell/module/teams/?view=teams-ps
  - Configure email integration options,
    - https://docs.microsoft.com/en-us/microsoftteams/messaging-policies-in-teams
    - https://docs.microsoft.com/en-us/powershell/module/skype/grant-csteamsmessagingpolicy?view=skype-ps
  - Configure and manage Apps settings,
    - https://docs.microsoft.com/en-us/powershell/module/skype/grant-csteamsappsetuppolicy?view=skype-ps
  - Configure custom cloud storage
    - https://techcommunity.microsoft.com/t5/Microsoft-Teams/Disable-additional-cloud-storage-DropBox-Box-and-Google-Drive/td-p/253335
  - Configure a Teams meeting policy
    - https://docs.microsoft.com/en-us/microsoftteams/meeting-policies-in-teams
    - https://docs.microsoft.com/en-us/powershell/module/skype/grant-csteamsmeetingpolicy?view=skype-ps
  - Configure Content Search,
  - Plan and configure the provisioning process,
  - Plan and configure Teams templates
    - https://docs.microsoft.com/en-us/microsoftteams/get-started-with-teams-templates
- Plan identity and authentication for Teams
  - Implement identity models and authentication,
    - https://docs.microsoft.com/en-us/microsoftteams/identify-models-authentication
  - Configure guest access
    - https://docs.microsoft.com/en-us/microsoftteams/guest-access-powershell
    - https://docs.microsoft.com/en-us/microsoftteams/manage-external-access
- Manage the Teams environment
  - Deploy Teams client apps,
    - https://docs.microsoft.com/en-us/microsoftteams/get-clients
  - Manage visible Apps,
    - https://docs.microsoft.com/en-us/microsoftteams/admin-settings
    - https://docs.microsoft.com/en-us/microsoftteams/office-365-custom-connectors
    - https://docs.microsoft.com/en-us/microsoftteams/tenant-apps-catalog-teams
  - Monitor the audit log for events
    - https://docs.microsoft.com/en-us/microsoftteams/audit-log-events
    - https://blogs.technet.microsoft.com/skypehybridguy/2017/09/05/microsoft-teams-audit-log-of-activity/
- Monitor and maintain the Teams service
  - Research, troubleshoot, and resolve reported issues,
    - https://docs.microsoft.com/en-us/microsoftteams/teams-analytics-and-reports/teams-reporting-reference
    - https://docs.microsoft.com/en-us/microsoftteams/log-files
  - Monitor service health issues,
  - Monitor Teams usage and usage patterns


## Configure and Manage Workload Integrations (15-20%)

- Integrate M365 workloads
  - Manage Office 365 connectors for Teams, Yammer, and SharePoint
    - https://docs.microsoft.com/en-us/microsoftteams/platform/concepts/connectors/connectors-using
    - https://docs.microsoft.com/en-us/MicrosoftTeams/office-365-custom-connectors
  - Manage integration with Office apps
  - Manage user licenses for Flow and PowerApps
    - https://docs.microsoft.com/en-us/flow/organization-q-and-a
    - https://powerapps.microsoft.com/en-us/pricing/
  - Manage quotas for Flow and PowerApps
    - https://powerusers.microsoft.com/t5/General-Discussion/Restricting-users-from-creating-powerapps/td-p/81349
    - http://www.lifeonplanetgroove.com/microsoft-flow-quotas-explained/
  - Utilize Delve for collaboration
    - https://regarding365.com/hiding-from-delve-in-office-365-2d5427c3490c
  - Plan for and manage Office 365 groups
    - https://docs.microsoft.com/en-us/office365/admin/create-groups/plan-for-groups-governance
    - https://docs.microsoft.com/en-us/microsoftteams/plan-office-365-groups
  - Manage data and environment policies for M365 workloads
    - https://docs.microsoft.com/en-us/flow/prevent-data-loss
  - Manage workload Apps with proper permissions and licenses
- Manage Yammer capabilities
  - Enable document support for Yammer
    - https://docs.microsoft.com/en-us/yammer/configure-your-yammer-network/configure-yammer
  - Integrate Yammer with SharePoint,
  - Enable the Yammer webpart for SharePoint sites,
    - https://docs.microsoft.com/en-us/yammer/integrate-yammer-with-other-apps/embed-a-feed-into-a-sharepoint-site
  - Enable and manage Yammer and Office 365 connected groups,
    - https://docs.microsoft.com/en-us/yammer/manage-yammer-groups/yammer-and-office-365-groups
  - Migrate users to Azure AD to enable authentication with Yammer,
    - https://docs.microsoft.com/en-us/yammer/manage-yammer-users/aad-account-required
  - Enable Yammer integration with on-premises SharePoint deployments
    - https://docs.microsoft.com/en-us/SharePoint/administration/integrate-yammer-with-on-premises-sharepoint-server-environments
- Manage Stream capabilities
  - Configure Stream channels to allow integration with Teams,
    - https://docs.microsoft.com/en-us/stream/admin-overview
  - Enable viewing, sharing, and embedding of Microsoft Stream video content in Teams, SharePoint Online, and Yammer,
  - Deploy, configure and manage Live Events to publish with Yammer, Stream, and Teams,
    - https://docs.microsoft.com/en-us/stream/live-event-administration
  - Configure company-wide channel creation
    - https://docs.microsoft.com/en-us/stream/restrict-companywide-channels
- Integrate M365 workloads with external data and systems
  - Identify data access requirements to integrate with line-of-business solutions,
    - https://docs.microsoft.com/en-us/power-bi/service-gateway-getting-started
  - Manage tenant settings for Power BI,
    - https://docs.microsoft.com/en-us/power-bi/service-admin-portal
  - Monitor workload usage and usage patterns,
  - Monitor license usage for workloads
    - https://docs.microsoft.com/en-us/power-bi/service-admin-licensing-organization

## Configure and Manage Hybrid Scenarios (5-10%)

- Implement hybrid teamwork artifacts
  - Plan, configure, and monitor hybrid SharePoint taxonomies and hybrid content types,
    - https://docs.microsoft.com/en-us/sharepoint/hybrid/plan-hybrid-sharepoint-taxonomy-and-hybrid-content-types
  - Plan and configure hybrid OneDrive for Business,
    - https://docs.microsoft.com/en-us/sharepoint/hybrid/plan-hybrid-onedrive-for-business
  - Plan for and add custom tiles to the hybrid app launcher,
    - https://docs.microsoft.com/en-us/sharepoint/hybrid/the-extensible-hybrid-app-launcher
  - Configure document rendering for Web Apps
- Implement a data gateway
  - Plan the implementation of on-premises data gateway
    - https://biinsight.com/definitive-guide-to-implement-on-premises-data-gateway-enterprise-mode-in-organisations/
  - Install and configure an on-premises data gateway
    - https://www.enjoysharepoint.com/on-premises-data-gateway/
  - Manage an on-premises data gateway

## Migrate to SharePoint Online (5-10%)

- Migrate data and content
  - Identify and resolve blocking issues that prevent migration,
    - https://sharepoint.fpweb.net/sharepoint-blog/avoid-getting-throttled-sharepoint-online-office-365/
    - https://www.c-sharpcorner.com/blogs/challenges-and-issues-in-microsoft-sharepoint-online
    - http://www.digdes.com/blog/sharepoint-migration-common-issues/
- Determine course of action for data and content that cannot be migrated,
- Prepare data for migration
  - https://docs.microsoft.com/en-us/sharepointmigration/fileshare-to-odsp-migration-guide
  - https://docs.microsoft.com/en-us/sharepointmigration/overview-of-the-sharepoint-migration-assessment-tool
- Recommend tools and strategies to migrate data
  - https://docs.microsoft.com/en-us/sharepointmigration/introducing-the-sharepoint-migration-tool
  - https://docs.microsoft.com/en-us/sharepointmigration/sharepoint-migration-identity-mapping-tool
