---
title: Класс MDM_Policy_Result01_InternetExplorer02
description: Политика MDM \_ \_ Result01 \_ InternetExplorer02 представляет политики Internet Explorer.
ms.assetid: 4b14c9ea-2f4d-4e5a-8aab-3741f15b0b1e
keywords:
- Класс MDM_Policy_Result01_InternetExplorer02
- MDM_Policy_Result01_InternetExplorer02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_InternetExplorer02
- MDM_Policy_Result01_InternetExplorer02.InstanceID
- MDM_Policy_Result01_InternetExplorer02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63308b6100d6bd4ec924307a9dcd3892096fc0fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988542"
---
# <a name="mdm_policy_result01_internetexplorer02-class"></a><span data-ttu-id="78943-105">\_Класс политики MDM \_ Result01 \_ InternetExplorer02</span><span class="sxs-lookup"><span data-stu-id="78943-105">MDM\_Policy\_Result01\_InternetExplorer02 class</span></span>

<span data-ttu-id="78943-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="78943-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="78943-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="78943-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="78943-108">Политика MDM \_ \_ Result01 \_ InternetExplorer02 представляет политики Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="78943-108">The MDM\_Policy\_Result01\_InternetExplorer02 represents the Internet Explorer policies.</span></span>

<span data-ttu-id="78943-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="78943-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="78943-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="78943-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_InternetExplorer02
{
  string InstanceID;
  string ParentID;
  string AddSearchProvider;
  string AllowActiveXFiltering;
  string AllowAddOnList;
  string AllowDeletingBrowsingHistoryOnExit;
  string AllowCertificateAddressMismatchWarning;
  string AllowEnhancedProtectedMode;
  string AllowEnterpriseModeFromToolsMenu;
  string AllowEnterpriseModeSiteList;
  string AllowFallbackToSSL3;
  string AllowInternetExplorer7PolicyList;
  string AllowInternetExplorerStandardsMode;
  string AllowInternetZoneTemplate;
  string AllowIntranetZoneTemplate;
  string AllowLocalMachineZoneTemplate;
  string AllowLockedDownInternetZoneTemplate;
  string AllowLockedDownIntranetZoneTemplate;
  string AllowLockedDownLocalMachineZoneTemplate;
  string AllowLockedDownRestrictedSitesZoneTemplate;
  string AllowOneWordEntry;
  string AllowSiteToZoneAssignmentList;
  string AllowsLockedDownTrustedSitesZoneTemplate;
  string AllowSoftwareWhenSignatureIsInvalid;
  string AllowsRestrictedSitesZoneTemplate;
  string AllowSuggestedSites;
  string AllowTrustedSitesZoneTemplate;
  string ConsistentMimeHandlingInternetExplorerProcesses;
  string CheckSignaturesOnDownloadedPrograms;
  string CheckServerCertificateRevocation;
  string DisableAdobeFlash;
  string DisableBlockingOfOutdatedActiveXControls;
  string DisableBypassOfSmartScreenWarnings;
  string DisableBypassOfSmartScreenWarningsAboutUncommonFiles;
  string DisableCrashDetection;
  string DisableConfiguringHistory;
  string DisableCustomerExperienceImprovementProgramParticipation;
  string DisableDeletingUserVisitedWebsites;
  string DisableEnclosureDownloading;
  string DisableEncryptionSupport;
  string DisableFirstRunWizard;
  string DisableFlipAheadFeature;
  string DisableProcessesInEnhancedProtectedMode;
  string DisableInPrivateBrowsing;
  string DisableIgnoringCertificateErrors;
  string DisableProxyChange;
  string DisableSearchProviderChange;
  string DisableSecondaryHomePageChange;
  string DisableSecuritySettingsCheck;
  string DisableUpdateCheck;
  string DoNotAllowActiveXControlsInProtectedMode;
  string DoNotAllowUsersToAddSites;
  string DoNotAllowUsersToChangePolicies;
  string DoNotBlockOutdatedActiveXControls;
  string DoNotBlockOutdatedActiveXControlsOnSpecificDomains;
  string IncludeAllLocalSites;
  string IncludeAllNetworkPaths;
  string InternetZoneAllowAccessToDataSources;
  string InternetZoneAllowAutomaticPromptingForActiveXControls;
  string InternetZoneAllowAutomaticPromptingForFileDownloads;
  string InternetZoneAllowDragAndDropCopyAndPasteFiles;
  string InternetZoneAllowCopyPasteViaScript;
  string InternetZoneAllowFontDownloads;
  string InternetZoneAllowLessPrivilegedSites;
  string InternetZoneAllowLoadingOfXAMLFiles;
  string InternetZoneAllowNETFrameworkReliantComponents;
  string InternetZoneAllowScriptInitiatedWindows;
  string InternetZoneAllowScriptingOfInternetExplorerWebBrowserControls;
  string InternetZoneAllowOnlyApprovedDomainsToUseTDCActiveXControl;
  string InternetZoneAllowOnlyApprovedDomainsToUseActiveXControls;
  string InternetZoneAllowScriptlets;
  string InternetZoneAllowSmartScreenIE;
  string InternetZoneAllowUpdatesToStatusBarViaScript;
  string InternetZoneAllowUserDataPersistence;
  string InternetZoneDoNotRunAntimalwareAgainstActiveXControls;
  string InternetZoneIncludeLocalPathWhenUploadingFilesToServer;
  string InternetZoneEnableProtectedMode;
  string InternetZoneEnableMIMESniffing;
  string InternetZoneEnableDraggingOfContentFromDifferentDomainsWithinWindows;
  string InternetZoneEnableDraggingOfContentFromDifferentDomainsAcrossWindows;
  string InternetZoneEnableCrossSiteScriptingFilter;
  string InternetZoneDownloadUnsignedActiveXControls;
  string InternetZoneDownloadSignedActiveXControls;
  string InternetZoneInitializeAndScriptActiveXControls;
  string InternetZoneJavaPermissions;
  string InternetZoneLogonOptions;
  string InternetZoneLaunchingApplicationsAndFilesInIFRAME;
  string InternetZoneNavigateWindowsAndFrames;
  string InternetZoneWebsitesInLessPrivilegedZonesCanNavigateIntoThisZone;
  string InternetZoneUsePopupBlocker;
  string InternetZoneShowSecurityWarningForPotentiallyUnsafeFiles;
  string InternetZoneRunNETFrameworkReliantComponentsSignedWithAuthenticode;
  string InternetZoneRunNETFrameworkReliantComponentsNotSignedWithAuthenticode;
  string IntranetZoneAllowAccessToDataSources;
  string IntranetZoneAllowAutomaticPromptingForActiveXControls;
  string IntranetZoneAllowAutomaticPromptingForFileDownloads;
  string IntranetZoneAllowFontDownloads;
  string IntranetZoneAllowLessPrivilegedSites;
  string IntranetZoneAllowNETFrameworkReliantComponents;
  string IntranetZoneAllowScriptlets;
  string IntranetZoneAllowSmartScreenIE;
  string IntranetZoneAllowUserDataPersistence;
  string IntranetZoneDoNotRunAntimalwareAgainstActiveXControls;
  string IntranetZoneInitializeAndScriptActiveXControls;
  string IntranetZoneJavaPermissions;
  string IntranetZoneInitializeAndScriptActiveXControlsNotMarkedSafe;
  string IntranetZoneNavigateWindowsAndFrames;
  string LocalMachineZoneAllowAccessToDataSources;
  string LocalMachineZoneAllowAutomaticPromptingForActiveXControls;
  string LocalMachineZoneAllowAutomaticPromptingForFileDownloads;
  string LocalMachineZoneAllowFontDownloads;
  string LocalMachineZoneAllowLessPrivilegedSites;
  string LocalMachineZoneAllowNETFrameworkReliantComponents;
  string LocalMachineZoneAllowScriptlets;
  string LocalMachineZoneAllowSmartScreenIE;
  string LocalMachineZoneAllowUserDataPersistence;
  string LocalMachineZoneDoNotRunAntimalwareAgainstActiveXControls;
  string LocalMachineZoneInitializeAndScriptActiveXControls;
  string LocalMachineZoneJavaPermissions;
  string LocalMachineZoneNavigateWindowsAndFrames;
  string LockedDownInternetZoneAllowAccessToDataSources;
  string LockedDownInternetZoneAllowAutomaticPromptingForActiveXControls;
  string LockedDownInternetZoneAllowAutomaticPromptingForFileDownloads;
  string LockedDownInternetZoneAllowFontDownloads;
  string LockedDownInternetZoneAllowLessPrivilegedSites;
  string LockedDownInternetZoneAllowNETFrameworkReliantComponents;
  string LockedDownInternetZoneAllowScriptlets;
  string LockedDownInternetZoneAllowSmartScreenIE;
  string LockedDownInternetZoneAllowUserDataPersistence;
  string LockedDownInternetZoneInitializeAndScriptActiveXControls;
  string LockedDownInternetZoneJavaPermissions;
  string LockedDownInternetZoneNavigateWindowsAndFrames;
  string LockedDownIntranetZoneAllowAccessToDataSources;
  string LockedDownIntranetZoneAllowAutomaticPromptingForActiveXControls;
  string LockedDownIntranetZoneAllowAutomaticPromptingForFileDownloads;
  string LockedDownIntranetZoneAllowFontDownloads;
  string LockedDownIntranetZoneAllowLessPrivilegedSites;
  string LockedDownIntranetZoneAllowNETFrameworkReliantComponents;
  string LockedDownIntranetZoneAllowScriptlets;
  string LockedDownIntranetZoneAllowSmartScreenIE;
  string LockedDownIntranetZoneAllowUserDataPersistence;
  string LockedDownIntranetZoneInitializeAndScriptActiveXControls;
  string LockedDownIntranetZoneNavigateWindowsAndFrames;
  string LockedDownLocalMachineZoneAllowAccessToDataSources;
  string LockedDownLocalMachineZoneAllowAutomaticPromptingForActiveXControls;
  string LockedDownLocalMachineZoneAllowAutomaticPromptingForFileDownloads;
  string LockedDownLocalMachineZoneAllowFontDownloads;
  string LockedDownLocalMachineZoneAllowLessPrivilegedSites;
  string LockedDownLocalMachineZoneAllowNETFrameworkReliantComponents;
  string LockedDownLocalMachineZoneAllowScriptlets;
  string LockedDownLocalMachineZoneAllowSmartScreenIE;
  string LockedDownLocalMachineZoneAllowUserDataPersistence;
  string LockedDownLocalMachineZoneInitializeAndScriptActiveXControls;
  string LockedDownLocalMachineZoneJavaPermissions;
  string LockedDownLocalMachineZoneNavigateWindowsAndFrames;
  string LockedDownRestrictedSitesZoneAllowAccessToDataSources;
  string LockedDownRestrictedSitesZoneAllowAutomaticPromptingForActiveXControls;
  string LockedDownRestrictedSitesZoneAllowAutomaticPromptingForFileDownloads;
  string LockedDownRestrictedSitesZoneAllowFontDownloads;
  string LockedDownRestrictedSitesZoneAllowLessPrivilegedSites;
  string LockedDownRestrictedSitesZoneAllowNETFrameworkReliantComponents;
  string LockedDownRestrictedSitesZoneAllowScriptlets;
  string LockedDownRestrictedSitesZoneAllowSmartScreenIE;
  string LockedDownRestrictedSitesZoneAllowUserDataPersistence;
  string LockedDownRestrictedSitesZoneInitializeAndScriptActiveXControls;
  string LockedDownRestrictedSitesZoneJavaPermissions;
  string LockedDownRestrictedSitesZoneNavigateWindowsAndFrames;
  string LockedDownTrustedSitesZoneAllowAccessToDataSources;
  string LockedDownTrustedSitesZoneAllowAutomaticPromptingForActiveXControls;
  string LockedDownTrustedSitesZoneAllowAutomaticPromptingForFileDownloads;
  string LockedDownTrustedSitesZoneAllowFontDownloads;
  string LockedDownTrustedSitesZoneAllowLessPrivilegedSites;
  string LockedDownTrustedSitesZoneAllowNETFrameworkReliantComponents;
  string LockedDownTrustedSitesZoneAllowScriptlets;
  string LockedDownTrustedSitesZoneAllowSmartScreenIE;
  string LockedDownTrustedSitesZoneAllowUserDataPersistence;
  string LockedDownTrustedSitesZoneInitializeAndScriptActiveXControls;
  string LockedDownTrustedSitesZoneJavaPermissions;
  string LockedDownTrustedSitesZoneNavigateWindowsAndFrames;
  string RestrictActiveXInstallInternetExplorerProcesses;
  string RemoveRunThisTimeButtonForOutdatedActiveXControls;
  string ProtectionFromZoneElevationInternetExplorerProcesses;
  string PreventPerUserInstallationOfActiveXControls;
  string PreventManagingSmartScreenFilter;
  string NotificationBarInternetExplorerProcesses;
  string MKProtocolSecurityRestrictionInternetExplorerProcesses;
  string MimeSniffingSafetyFeatureInternetExplorerProcesses;
  string RestrictedSitesZoneAllowAccessToDataSources;
  string RestrictedSitesZoneAllowActiveScripting;
  string RestrictedSitesZoneAllowAutomaticPromptingForActiveXControls;
  string RestrictedSitesZoneAllowAutomaticPromptingForFileDownloads;
  string RestrictedSitesZoneAllowFileDownloads;
  string RestrictedSitesZoneAllowDragAndDropCopyAndPasteFiles;
  string RestrictedSitesZoneAllowCopyPasteViaScript;
  string RestrictedSitesZoneAllowBinaryAndScriptBehaviors;
  string RestrictedSitesZoneAllowFontDownloads;
  string RestrictedSitesZoneAllowLessPrivilegedSites;
  string RestrictedSitesZoneAllowMETAREFRESH;
  string RestrictedSitesZoneAllowLoadingOfXAMLFiles;
  string RestrictedSitesZoneAllowNETFrameworkReliantComponents;
  string RestrictedSitesZoneAllowScriptInitiatedWindows;
  string RestrictedSitesZoneAllowScriptingOfInternetExplorerWebBrowserControls;
  string RestrictedSitesZoneAllowOnlyApprovedDomainsToUseTDCActiveXControl;
  string RestrictedSitesZoneAllowOnlyApprovedDomainsToUseActiveXControls;
  string RestrictedSitesZoneAllowScriptlets;
  string RestrictedSitesZoneAllowSmartScreenIE;
  string RestrictedSitesZoneAllowUpdatesToStatusBarViaScript;
  string RestrictedSitesZoneAllowUserDataPersistence;
  string RestrictedSitesZoneIncludeLocalPathWhenUploadingFilesToServer;
  string RestrictedSitesZoneEnableMIMESniffing;
  string RestrictedSitesZoneEnableDraggingOfContentFromDifferentDomainsWithinWindows;
  string RestrictedSitesZoneEnableDraggingOfContentFromDifferentDomainsAcrossWindows;
  string RestrictedSitesZoneDownloadUnsignedActiveXControls;
  string RestrictedSitesZoneEnableCrossSiteScriptingFilter;
  string RestrictedSitesZoneDownloadSignedActiveXControls;
  string RestrictedSitesZoneDoNotRunAntimalwareAgainstActiveXControls;
  string RestrictedSitesZoneInitializeAndScriptActiveXControls;
  string RestrictedSitesZoneLogonOptions;
  string RestrictedSitesZoneLaunchingApplicationsAndFilesInIFRAME;
  string RestrictedSitesZoneJavaPermissions;
  string RestrictedSitesZoneNavigateWindowsAndFrames;
  string ScriptedWindowSecurityRestrictionsInternetExplorerProcesses;
  string RestrictFileDownloadInternetExplorerProcesses;
  string RestrictedSitesZoneScriptActiveXControlsMarkedSafeForScripting;
  string RestrictedSitesZoneUsePopupBlocker;
  string RestrictedSitesZoneTurnOnProtectedMode;
  string RestrictedSitesZoneTurnOnCrossSiteScriptingFilter;
  string RestrictedSitesZoneShowSecurityWarningForPotentiallyUnsafeFiles;
  string RestrictedSitesZoneScriptingOfJavaApplets;
  string RestrictedSitesZoneRunNETFrameworkReliantComponentsSignedWithAuthenticode;
  string RestrictedSitesZoneRunActiveXControlsAndPlugins;
  string RestrictedSitesZoneNavigateWindowsAndFramesAcrossDomains;
  string SearchProviderList;
  string SpecifyUseOfActiveXInstallerService;
  string SecurityZonesUseOnlyMachineSettings;
  string TrustedSitesZoneAllowAccessToDataSources;
  string TrustedSitesZoneAllowAutomaticPromptingForActiveXControls;
  string TrustedSitesZoneAllowAutomaticPromptingForFileDownloads;
  string TrustedSitesZoneAllowFontDownloads;
  string TrustedSitesZoneAllowLessPrivilegedSites;
  string TrustedSitesZoneAllowNETFrameworkReliantComponents;
  string TrustedSitesZoneAllowScriptlets;
  string TrustedSitesZoneAllowSmartScreenIE;
  string TrustedSitesZoneAllowUserDataPersistence;
  string TrustedSitesZoneDontRunAntimalwareProgramsAgainstActiveXControls;
  string TrustedSitesZoneDoNotRunAntimalwareAgainstActiveXControls;
  string TrustedSitesZoneInitializeAndScriptActiveXControls;
  string TrustedSitesZoneInitializeAndScriptActiveXControlsNotMarkedSafe;
  string TrustedSitesZoneInitializeAndScriptActiveXControlsNotMarkedAsSafe;
  string TrustedSitesZoneJavaPermissions;
  string TrustedSitesZoneNavigateWindowsAndFrames;
};
```

## <a name="members"></a><span data-ttu-id="78943-111">Члены</span><span class="sxs-lookup"><span data-stu-id="78943-111">Members</span></span>

<span data-ttu-id="78943-112">Класс **\_ политики MDM \_ Result01 \_ InternetExplorer02** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="78943-112">The **MDM\_Policy\_Result01\_InternetExplorer02** class has these types of members:</span></span>

-   [<span data-ttu-id="78943-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="78943-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="78943-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="78943-114">Properties</span></span>

<span data-ttu-id="78943-115">Класс **\_ политики MDM \_ Result01 \_ InternetExplorer02** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="78943-115">The **MDM\_Policy\_Result01\_InternetExplorer02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="78943-116">AddSearchProvider</span><span class="sxs-lookup"><span data-stu-id="78943-116">AddSearchProvider</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-addsearchprovider)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-117">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-119">алловактивексфилтеринг</span><span class="sxs-lookup"><span data-stu-id="78943-119">AllowActiveXFiltering</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowactivexfiltering)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-121">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-122">алловаддонлист</span><span class="sxs-lookup"><span data-stu-id="78943-122">AllowAddOnList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowaddonlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-123">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-124">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-125">алловцертификатеаддрессмисматчварнинг</span><span class="sxs-lookup"><span data-stu-id="78943-125">AllowCertificateAddressMismatchWarning</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowcertificateaddressmismatchwarning)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-126">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-127">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-128">алловделетингбровсингхисторйонексит</span><span class="sxs-lookup"><span data-stu-id="78943-128">AllowDeletingBrowsingHistoryOnExit</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowdeletingbrowsinghistoryonexit)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-129">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-130">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-131">алловенханцедпротектедмоде</span><span class="sxs-lookup"><span data-stu-id="78943-131">AllowEnhancedProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowenhancedprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-132">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-133">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-134">алловентерприсемодефромтулсмену</span><span class="sxs-lookup"><span data-stu-id="78943-134">AllowEnterpriseModeFromToolsMenu</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowenterprisemodefromtoolsmenu)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-135">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-136">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-137">алловентерприсемодесителист</span><span class="sxs-lookup"><span data-stu-id="78943-137">AllowEnterpriseModeSiteList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowenterprisemodesitelist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-138">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-139">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-140">AllowFallbackToSSL3</span><span class="sxs-lookup"><span data-stu-id="78943-140">AllowFallbackToSSL3</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowfallbacktossl3)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-141">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-142">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-143">AllowInternetExplorer7PolicyList</span><span class="sxs-lookup"><span data-stu-id="78943-143">AllowInternetExplorer7PolicyList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowinternetexplorer7policylist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-144">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-145">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-146">алловинтернетексплорерстандардсмоде</span><span class="sxs-lookup"><span data-stu-id="78943-146">AllowInternetExplorerStandardsMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowinternetexplorerstandardsmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-147">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-148">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-149">алловинтернетзонетемплате</span><span class="sxs-lookup"><span data-stu-id="78943-149">AllowInternetZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowinternetzonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-150">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-151">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-152">алловинтранетзонетемплате</span><span class="sxs-lookup"><span data-stu-id="78943-152">AllowIntranetZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowintranetzonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-153">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-154">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-155">алловлокалмачинезонетемплате</span><span class="sxs-lookup"><span data-stu-id="78943-155">AllowLocalMachineZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlocalmachinezonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-156">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-157">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-158">алловлоккеддовнинтернетзонетемплате</span><span class="sxs-lookup"><span data-stu-id="78943-158">AllowLockedDownInternetZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlockeddowninternetzonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-159">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-160">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-161">алловлоккеддовнинтранетзонетемплате</span><span class="sxs-lookup"><span data-stu-id="78943-161">AllowLockedDownIntranetZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlockeddownintranetzonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-162">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-163">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-164">алловлоккеддовнлокалмачинезонетемплате</span><span class="sxs-lookup"><span data-stu-id="78943-164">AllowLockedDownLocalMachineZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlockeddownlocalmachinezonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-165">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-166">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-166">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-167">алловлоккеддовнрестриктедситесзонетемплате</span><span class="sxs-lookup"><span data-stu-id="78943-167">AllowLockedDownRestrictedSitesZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlockeddownrestrictedsiteszonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-168">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-169">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-169">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-170">алловоневордентри</span><span class="sxs-lookup"><span data-stu-id="78943-170">AllowOneWordEntry</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowonewordentry)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-171">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-172">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-172">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-173">алловситетозонеассигнментлист</span><span class="sxs-lookup"><span data-stu-id="78943-173">AllowSiteToZoneAssignmentList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowsitetozoneassignmentlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-174">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-175">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-175">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-176">алловслоккеддовнтрустедситесзонетемплате</span><span class="sxs-lookup"><span data-stu-id="78943-176">AllowsLockedDownTrustedSitesZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowslockeddowntrustedsiteszonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-177">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-178">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-178">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-179">алловсофтваревхенсигнатуреисинвалид</span><span class="sxs-lookup"><span data-stu-id="78943-179">AllowSoftwareWhenSignatureIsInvalid</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowsoftwarewhensignatureisinvalid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-180">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-181">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-181">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-182">алловсрестриктедситесзонетемплате</span><span class="sxs-lookup"><span data-stu-id="78943-182">AllowsRestrictedSitesZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowsrestrictedsiteszonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-183">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-184">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-184">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-185">алловсугжестедситес</span><span class="sxs-lookup"><span data-stu-id="78943-185">AllowSuggestedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowsuggestedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-186">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-187">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-187">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-188">алловтрустедситесзонетемплате</span><span class="sxs-lookup"><span data-stu-id="78943-188">AllowTrustedSitesZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowtrustedsiteszonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-189">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-190">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-190">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-191">чекксерверцертификатеревокатион</span><span class="sxs-lookup"><span data-stu-id="78943-191">CheckServerCertificateRevocation</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-checkservercertificaterevocation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-192">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-193">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-193">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-194">чекксигнатуресондовнлоадедпрограмс</span><span class="sxs-lookup"><span data-stu-id="78943-194">CheckSignaturesOnDownloadedPrograms</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-checksignaturesondownloadedprograms)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-195">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-196">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-196">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-197">консистентмимехандлингинтернетексплорерпроцессес</span><span class="sxs-lookup"><span data-stu-id="78943-197">ConsistentMimeHandlingInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-consistentmimehandlinginternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-198">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-199">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-199">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-200">дисаблеадобефлаш</span><span class="sxs-lookup"><span data-stu-id="78943-200">DisableAdobeFlash</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableadobeflash)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-201">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-202">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-202">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="78943-203">дисаблеблоккингофаутдатедактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="78943-203">DisableBlockingOfOutdatedActiveXControls</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-204">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-204">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-205">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-205">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-206">дисаблебипассофсмартскринварнингс</span><span class="sxs-lookup"><span data-stu-id="78943-206">DisableBypassOfSmartScreenWarnings</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablebypassofsmartscreenwarnings)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-207">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-208">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-208">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-209">дисаблебипассофсмартскринварнингсабаутункоммонфилес</span><span class="sxs-lookup"><span data-stu-id="78943-209">DisableBypassOfSmartScreenWarningsAboutUncommonFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablebypassofsmartscreenwarningsaboutuncommonfiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-210">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-211">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-211">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-212">дисаблеконфигурингхистори</span><span class="sxs-lookup"><span data-stu-id="78943-212">DisableConfiguringHistory</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableconfiguringhistory)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-213">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-214">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-214">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-215">дисаблекрашдетектион</span><span class="sxs-lookup"><span data-stu-id="78943-215">DisableCrashDetection</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablecrashdetection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-216">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-216">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-217">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-217">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-218">дисаблекустомерекспериенцеимпровементпрогрампартиЦипатион</span><span class="sxs-lookup"><span data-stu-id="78943-218">DisableCustomerExperienceImprovementProgramParticipation</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablecustomerexperienceimprovementprogramparticipation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-219">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-220">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-220">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-221">дисабледелетингусервиситедвебситес</span><span class="sxs-lookup"><span data-stu-id="78943-221">DisableDeletingUserVisitedWebsites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disabledeletinguservisitedwebsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-222">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-223">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-223">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-224">дисаблинклосуредовнлоадинг</span><span class="sxs-lookup"><span data-stu-id="78943-224">DisableEnclosureDownloading</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableenclosuredownloading)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-225">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-226">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-226">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-227">дисаблинкриптионсуппорт</span><span class="sxs-lookup"><span data-stu-id="78943-227">DisableEncryptionSupport</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableencryptionsupport)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-228">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-228">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-229">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-229">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-230">дисаблефирструнвизард</span><span class="sxs-lookup"><span data-stu-id="78943-230">DisableFirstRunWizard</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablefirstrunwizard)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-231">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-231">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-232">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-232">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-233">дисаблефлипахеадфеатуре</span><span class="sxs-lookup"><span data-stu-id="78943-233">DisableFlipAheadFeature</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableflipaheadfeature)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-234">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-234">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-235">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-235">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-236">дисаблеигнорингцертификатиррорс</span><span class="sxs-lookup"><span data-stu-id="78943-236">DisableIgnoringCertificateErrors</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableignoringcertificateerrors)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-237">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-237">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-238">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-238">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-239">дисаблеинприватебровсинг</span><span class="sxs-lookup"><span data-stu-id="78943-239">DisableInPrivateBrowsing</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableinprivatebrowsing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-240">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-240">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-241">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-241">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-242">дисаблепроцессесиненханцедпротектедмоде</span><span class="sxs-lookup"><span data-stu-id="78943-242">DisableProcessesInEnhancedProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableprocessesinenhancedprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-243">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-243">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-244">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-244">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-245">дисаблепроксичанже</span><span class="sxs-lookup"><span data-stu-id="78943-245">DisableProxyChange</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableproxychange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-246">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-246">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-247">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-247">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-248">дисаблесеарчпровидерчанже</span><span class="sxs-lookup"><span data-stu-id="78943-248">DisableSearchProviderChange</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablesearchproviderchange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-249">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-250">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-250">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-251">дисаблесекондарихомепажечанже</span><span class="sxs-lookup"><span data-stu-id="78943-251">DisableSecondaryHomePageChange</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablesecondaryhomepagechange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-252">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-253">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-253">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-254">дисаблесекуритисеттингсчекк</span><span class="sxs-lookup"><span data-stu-id="78943-254">DisableSecuritySettingsCheck</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablesecuritysettingscheck)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-255">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-255">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-256">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-256">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-257">дисаблеупдатечекк</span><span class="sxs-lookup"><span data-stu-id="78943-257">DisableUpdateCheck</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableupdatecheck)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-258">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-259">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-259">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-260">доноталловактивексконтролсинпротектедмоде</span><span class="sxs-lookup"><span data-stu-id="78943-260">DoNotAllowActiveXControlsInProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-donotallowactivexcontrolsinprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-261">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-262">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-262">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-263">доноталловусерстоаддситес</span><span class="sxs-lookup"><span data-stu-id="78943-263">DoNotAllowUsersToAddSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-donotallowuserstoaddsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-264">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-265">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-265">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-266">доноталловусерсточанжеполиЦиес</span><span class="sxs-lookup"><span data-stu-id="78943-266">DoNotAllowUsersToChangePolicies</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-donotallowuserstochangepolicies)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-267">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-267">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-268">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-268">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-269">донотблоккаутдатедактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="78943-269">DoNotBlockOutdatedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-donotblockoutdatedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-270">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-270">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-271">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-271">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-272">донотблоккаутдатедактивексконтролсонспеЦификдомаинс</span><span class="sxs-lookup"><span data-stu-id="78943-272">DoNotBlockOutdatedActiveXControlsOnSpecificDomains</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-donotblockoutdatedactivexcontrolsonspecificdomains)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-273">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-273">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-274">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-274">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-275">инклудеалллокалситес</span><span class="sxs-lookup"><span data-stu-id="78943-275">IncludeAllLocalSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-includealllocalsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-276">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-276">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-277">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-277">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-278">инклудеаллнетворкпасс</span><span class="sxs-lookup"><span data-stu-id="78943-278">IncludeAllNetworkPaths</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-includeallnetworkpaths)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-279">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-279">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-280">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-280">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="78943-281">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="78943-281">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-282">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-282">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-283">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="78943-283">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="78943-284">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="78943-284">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-285">интернетзонеалловакцесстодатасаурцес</span><span class="sxs-lookup"><span data-stu-id="78943-285">InternetZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-286">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-286">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-287">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-287">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-288">интернетзонеалловаутоматикпромптингфорактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="78943-288">InternetZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-289">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-289">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-290">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-290">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-291">интернетзонеалловаутоматикпромптингфорфиледовнлоадс</span><span class="sxs-lookup"><span data-stu-id="78943-291">InternetZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-292">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-292">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-293">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-293">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-294">интернетзонеалловкопипастевиаскрипт</span><span class="sxs-lookup"><span data-stu-id="78943-294">InternetZoneAllowCopyPasteViaScript</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowcopypasteviascript)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-295">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-295">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-296">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-296">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-297">интернетзонеалловдраганддропкопяндпастефилес</span><span class="sxs-lookup"><span data-stu-id="78943-297">InternetZoneAllowDragAndDropCopyAndPasteFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowdraganddropcopyandpastefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-298">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-298">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-299">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-299">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-300">интернетзонеалловфонтдовнлоадс</span><span class="sxs-lookup"><span data-stu-id="78943-300">InternetZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-301">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-301">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-302">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-302">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-303">интернетзонеалловлесспривилежедситес</span><span class="sxs-lookup"><span data-stu-id="78943-303">InternetZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-304">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-304">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-305">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-305">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-306">интернетзонеалловлоадингофксамлфилес</span><span class="sxs-lookup"><span data-stu-id="78943-306">InternetZoneAllowLoadingOfXAMLFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowloadingofxamlfiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-307">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-308">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-308">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-309">интернетзонеалловнетфрамеворкрелианткомпонентс</span><span class="sxs-lookup"><span data-stu-id="78943-309">InternetZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-310">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-310">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-311">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-311">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-312">интернетзонеалловонляппроведдомаинстаусеактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="78943-312">InternetZoneAllowOnlyApprovedDomainsToUseActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowonlyapproveddomainstouseactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-313">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-313">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-314">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-314">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-315">интернетзонеалловонляппроведдомаинстаусетдкактивексконтрол</span><span class="sxs-lookup"><span data-stu-id="78943-315">InternetZoneAllowOnlyApprovedDomainsToUseTDCActiveXControl</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowonlyapproveddomainstousetdcactivexcontrol)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-316">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-316">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-317">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-317">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-318">интернетзонеалловскриптингофинтернетексплорервеббровсерконтролс</span><span class="sxs-lookup"><span data-stu-id="78943-318">InternetZoneAllowScriptingOfInternetExplorerWebBrowserControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowscriptingofinternetexplorerwebbrowsercontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-319">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-319">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-320">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-320">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-321">интернетзонеалловскриптинитиатедвиндовс</span><span class="sxs-lookup"><span data-stu-id="78943-321">InternetZoneAllowScriptInitiatedWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowscriptinitiatedwindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-322">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-322">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-323">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-323">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-324">интернетзонеалловскриптлетс</span><span class="sxs-lookup"><span data-stu-id="78943-324">InternetZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-325">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-325">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-326">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-326">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-327">интернетзонеалловсмартскриние</span><span class="sxs-lookup"><span data-stu-id="78943-327">InternetZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-328">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-328">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-329">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-329">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-330">интернетзонеалловупдатестостатусбарвиаскрипт</span><span class="sxs-lookup"><span data-stu-id="78943-330">InternetZoneAllowUpdatesToStatusBarViaScript</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowupdatestostatusbarviascript)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-331">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-331">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-332">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-332">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-333">интернетзонеалловусердатаперсистенце</span><span class="sxs-lookup"><span data-stu-id="78943-333">InternetZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-334">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-334">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-335">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-335">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-336">интернетзонедонотрунантималвареагаинстактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="78943-336">InternetZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-337">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-337">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-338">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-338">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-339">интернетзонедовнлоадсигнедактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="78943-339">InternetZoneDownloadSignedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonedownloadsignedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-340">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-340">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-341">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-341">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-342">интернетзонедовнлоадунсигнедактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="78943-342">InternetZoneDownloadUnsignedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonedownloadunsignedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-343">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-343">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-344">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-344">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-345">интернетзонинаблекроссситескриптингфилтер</span><span class="sxs-lookup"><span data-stu-id="78943-345">InternetZoneEnableCrossSiteScriptingFilter</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenablecrosssitescriptingfilter)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-346">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-346">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-347">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-347">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-348">интернетзонинабледраггингофконтентфромдифферентдомаинсакроссвиндовс</span><span class="sxs-lookup"><span data-stu-id="78943-348">InternetZoneEnableDraggingOfContentFromDifferentDomainsAcrossWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenabledraggingofcontentfromdifferentdomainsacrosswindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-349">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-349">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-350">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-350">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-351">интернетзонинабледраггингофконтентфромдифферентдомаинсвисинвиндовс</span><span class="sxs-lookup"><span data-stu-id="78943-351">InternetZoneEnableDraggingOfContentFromDifferentDomainsWithinWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenabledraggingofcontentfromdifferentdomainswithinwindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-352">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-352">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-353">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-353">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-354">интернетзонинаблемимесниффинг</span><span class="sxs-lookup"><span data-stu-id="78943-354">InternetZoneEnableMIMESniffing</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenablemimesniffing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-355">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-355">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-356">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-356">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-357">интернетзонинаблепротектедмоде</span><span class="sxs-lookup"><span data-stu-id="78943-357">InternetZoneEnableProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenableprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-358">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-358">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-359">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-359">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-360">интернетзонеинклуделокалпасвхенуплоадингфилестосервер</span><span class="sxs-lookup"><span data-stu-id="78943-360">InternetZoneIncludeLocalPathWhenUploadingFilesToServer</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneincludelocalpathwhenuploadingfilestoserver)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-361">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-361">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-362">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-362">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-363">интернетзонеинитиализеандскриптактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="78943-363">InternetZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-364">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-364">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-365">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-365">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-366">интернетзонежавапермиссионс</span><span class="sxs-lookup"><span data-stu-id="78943-366">InternetZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-367">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-367">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-368">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-368">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-369">интернетзонелаунчингаппликатионсандфилесинифраме</span><span class="sxs-lookup"><span data-stu-id="78943-369">InternetZoneLaunchingApplicationsAndFilesInIFRAME</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonelaunchingapplicationsandfilesiniframe)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-370">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-370">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-371">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-371">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-372">интернетзонелогоноптионс</span><span class="sxs-lookup"><span data-stu-id="78943-372">InternetZoneLogonOptions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonelogonoptions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-373">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-373">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-374">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-374">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-375">интернетзоненавигатевиндовсандфрамес</span><span class="sxs-lookup"><span data-stu-id="78943-375">InternetZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-376">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-376">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-377">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-377">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="78943-378">интернетзонеруннетфрамеворкрелианткомпонентснотсигнедвисаусентикоде</span><span class="sxs-lookup"><span data-stu-id="78943-378">InternetZoneRunNETFrameworkReliantComponentsNotSignedWithAuthenticode</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-379">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-379">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-380">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-380">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-381">интернетзонеруннетфрамеворкрелианткомпонентссигнедвисаусентикоде</span><span class="sxs-lookup"><span data-stu-id="78943-381">InternetZoneRunNETFrameworkReliantComponentsSignedWithAuthenticode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonerunnetframeworkreliantcomponentssignedwithauthenticode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-382">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-382">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-383">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-383">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-384">интернетзонешовсекуритиварнингфорпотентиаллюнсафефилес</span><span class="sxs-lookup"><span data-stu-id="78943-384">InternetZoneShowSecurityWarningForPotentiallyUnsafeFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneshowsecuritywarningforpotentiallyunsafefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-385">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-385">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-386">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-386">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-387">интернетзонеусепопупблоккер</span><span class="sxs-lookup"><span data-stu-id="78943-387">InternetZoneUsePopupBlocker</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneusepopupblocker)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-388">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-388">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-389">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-389">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="78943-390">интернетзоневебситесинлесспривилежедзонесканнавигатеинтосисзоне</span><span class="sxs-lookup"><span data-stu-id="78943-390">InternetZoneWebsitesInLessPrivilegedZonesCanNavigateIntoThisZone</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-391">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-391">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-392">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-392">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-393">интранетзонеалловакцесстодатасаурцес</span><span class="sxs-lookup"><span data-stu-id="78943-393">IntranetZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-394">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-394">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-395">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-395">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-396">интранетзонеалловаутоматикпромптингфорактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="78943-396">IntranetZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-397">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-397">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-398">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-398">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-399">интранетзонеалловаутоматикпромптингфорфиледовнлоадс</span><span class="sxs-lookup"><span data-stu-id="78943-399">IntranetZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-400">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-400">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-401">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-401">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-402">интранетзонеалловфонтдовнлоадс</span><span class="sxs-lookup"><span data-stu-id="78943-402">IntranetZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-403">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-403">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-404">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-404">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-405">интранетзонеалловлесспривилежедситес</span><span class="sxs-lookup"><span data-stu-id="78943-405">IntranetZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-406">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-406">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-407">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-407">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-408">интранетзонеалловнетфрамеворкрелианткомпонентс</span><span class="sxs-lookup"><span data-stu-id="78943-408">IntranetZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-409">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-409">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-410">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-410">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-411">интранетзонеалловскриптлетс</span><span class="sxs-lookup"><span data-stu-id="78943-411">IntranetZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-412">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-412">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-413">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-413">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-414">интранетзонеалловсмартскриние</span><span class="sxs-lookup"><span data-stu-id="78943-414">IntranetZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-415">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-415">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-416">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-416">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-417">интранетзонеалловусердатаперсистенце</span><span class="sxs-lookup"><span data-stu-id="78943-417">IntranetZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-418">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-418">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-419">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-419">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-420">интранетзонедонотрунантималвареагаинстактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="78943-420">IntranetZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-421">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-421">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-422">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-422">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-423">интранетзонеинитиализеандскриптактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="78943-423">IntranetZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-424">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-424">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-425">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-425">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="78943-426">интранетзонеинитиализеандскриптактивексконтролснотмаркедсафе</span><span class="sxs-lookup"><span data-stu-id="78943-426">IntranetZoneInitializeAndScriptActiveXControlsNotMarkedSafe</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-427">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-427">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-428">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-428">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-429">интранетзонежавапермиссионс</span><span class="sxs-lookup"><span data-stu-id="78943-429">IntranetZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-430">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-430">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-431">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-431">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-432">интранетзоненавигатевиндовсандфрамес</span><span class="sxs-lookup"><span data-stu-id="78943-432">IntranetZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-433">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-433">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-434">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-434">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-435">локалмачинезонеалловакцесстодатасаурцес</span><span class="sxs-lookup"><span data-stu-id="78943-435">LocalMachineZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-436">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-436">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-437">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-437">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-438">локалмачинезонеалловаутоматикпромптингфорактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="78943-438">LocalMachineZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-439">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-439">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-440">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-440">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-441">локалмачинезонеалловаутоматикпромптингфорфиледовнлоадс</span><span class="sxs-lookup"><span data-stu-id="78943-441">LocalMachineZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-442">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-442">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-443">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-443">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-444">локалмачинезонеалловфонтдовнлоадс</span><span class="sxs-lookup"><span data-stu-id="78943-444">LocalMachineZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-445">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-445">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-446">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-446">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-447">локалмачинезонеалловлесспривилежедситес</span><span class="sxs-lookup"><span data-stu-id="78943-447">LocalMachineZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-448">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-448">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-449">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-449">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-450">локалмачинезонеалловнетфрамеворкрелианткомпонентс</span><span class="sxs-lookup"><span data-stu-id="78943-450">LocalMachineZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-451">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-451">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-452">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-452">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-453">локалмачинезонеалловскриптлетс</span><span class="sxs-lookup"><span data-stu-id="78943-453">LocalMachineZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-454">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-454">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-455">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-455">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-456">локалмачинезонеалловсмартскриние</span><span class="sxs-lookup"><span data-stu-id="78943-456">LocalMachineZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-457">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-457">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-458">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-458">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-459">локалмачинезонеалловусердатаперсистенце</span><span class="sxs-lookup"><span data-stu-id="78943-459">LocalMachineZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-460">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-460">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-461">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-461">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-462">локалмачинезонедонотрунантималвареагаинстактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="78943-462">LocalMachineZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-463">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-463">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-464">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-464">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-465">локалмачинезонеинитиализеандскриптактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="78943-465">LocalMachineZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-466">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-466">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-467">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-467">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-468">локалмачинезонежавапермиссионс</span><span class="sxs-lookup"><span data-stu-id="78943-468">LocalMachineZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-469">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-469">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-470">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-470">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-471">локалмачинезоненавигатевиндовсандфрамес</span><span class="sxs-lookup"><span data-stu-id="78943-471">LocalMachineZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-472">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-472">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-473">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-473">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-474">локкеддовнинтернетзонеалловакцесстодатасаурцес</span><span class="sxs-lookup"><span data-stu-id="78943-474">LockedDownInternetZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-475">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-475">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-476">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-476">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-477">локкеддовнинтернетзонеалловаутоматикпромптингфорактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="78943-477">LockedDownInternetZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-478">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-478">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-479">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-479">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-480">локкеддовнинтернетзонеалловаутоматикпромптингфорфиледовнлоадс</span><span class="sxs-lookup"><span data-stu-id="78943-480">LockedDownInternetZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-481">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-481">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-482">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-482">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-483">локкеддовнинтернетзонеалловфонтдовнлоадс</span><span class="sxs-lookup"><span data-stu-id="78943-483">LockedDownInternetZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-484">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-484">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-485">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-485">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-486">локкеддовнинтернетзонеалловлесспривилежедситес</span><span class="sxs-lookup"><span data-stu-id="78943-486">LockedDownInternetZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-487">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-487">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-488">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-488">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-489">локкеддовнинтернетзонеалловнетфрамеворкрелианткомпонентс</span><span class="sxs-lookup"><span data-stu-id="78943-489">LockedDownInternetZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-490">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-490">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-491">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-491">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-492">локкеддовнинтернетзонеалловскриптлетс</span><span class="sxs-lookup"><span data-stu-id="78943-492">LockedDownInternetZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-493">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-493">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-494">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-494">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-495">локкеддовнинтернетзонеалловсмартскриние</span><span class="sxs-lookup"><span data-stu-id="78943-495">LockedDownInternetZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-496">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-496">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-497">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-497">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-498">локкеддовнинтернетзонеалловусердатаперсистенце</span><span class="sxs-lookup"><span data-stu-id="78943-498">LockedDownInternetZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-499">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-499">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-500">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-500">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-501">локкеддовнинтернетзонеинитиализеандскриптактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="78943-501">LockedDownInternetZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-502">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-502">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-503">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-503">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-504">локкеддовнинтернетзонежавапермиссионс</span><span class="sxs-lookup"><span data-stu-id="78943-504">LockedDownInternetZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-505">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-505">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-506">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-506">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-507">локкеддовнинтернетзоненавигатевиндовсандфрамес</span><span class="sxs-lookup"><span data-stu-id="78943-507">LockedDownInternetZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-508">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-508">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-509">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-509">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-510">локкеддовнинтранетзонеалловакцесстодатасаурцес</span><span class="sxs-lookup"><span data-stu-id="78943-510">LockedDownIntranetZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-511">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-511">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-512">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-512">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-513">локкеддовнинтранетзонеалловаутоматикпромптингфорактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="78943-513">LockedDownIntranetZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-514">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-514">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-515">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-515">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-516">локкеддовнинтранетзонеалловаутоматикпромптингфорфиледовнлоадс</span><span class="sxs-lookup"><span data-stu-id="78943-516">LockedDownIntranetZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-517">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-517">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-518">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-518">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-519">локкеддовнинтранетзонеалловфонтдовнлоадс</span><span class="sxs-lookup"><span data-stu-id="78943-519">LockedDownIntranetZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-520">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-520">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-521">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-521">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-522">локкеддовнинтранетзонеалловлесспривилежедситес</span><span class="sxs-lookup"><span data-stu-id="78943-522">LockedDownIntranetZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-523">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-523">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-524">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-524">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-525">локкеддовнинтранетзонеалловнетфрамеворкрелианткомпонентс</span><span class="sxs-lookup"><span data-stu-id="78943-525">LockedDownIntranetZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-526">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-526">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-527">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-527">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-528">локкеддовнинтранетзонеалловскриптлетс</span><span class="sxs-lookup"><span data-stu-id="78943-528">LockedDownIntranetZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-529">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-529">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-530">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-530">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-531">локкеддовнинтранетзонеалловсмартскриние</span><span class="sxs-lookup"><span data-stu-id="78943-531">LockedDownIntranetZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-532">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-532">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-533">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-533">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-534">локкеддовнинтранетзонеалловусердатаперсистенце</span><span class="sxs-lookup"><span data-stu-id="78943-534">LockedDownIntranetZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-535">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-535">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-536">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-536">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-537">локкеддовнинтранетзонеинитиализеандскриптактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="78943-537">LockedDownIntranetZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-538">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-538">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-539">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-539">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-540">локкеддовнинтранетзоненавигатевиндовсандфрамес</span><span class="sxs-lookup"><span data-stu-id="78943-540">LockedDownIntranetZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-541">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-541">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-542">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-542">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-543">локкеддовнлокалмачинезонеалловакцесстодатасаурцес</span><span class="sxs-lookup"><span data-stu-id="78943-543">LockedDownLocalMachineZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-544">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-544">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-545">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-545">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-546">локкеддовнлокалмачинезонеалловаутоматикпромптингфорактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="78943-546">LockedDownLocalMachineZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-547">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-547">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-548">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-548">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-549">локкеддовнлокалмачинезонеалловаутоматикпромптингфорфиледовнлоадс</span><span class="sxs-lookup"><span data-stu-id="78943-549">LockedDownLocalMachineZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-550">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-550">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-551">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-551">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-552">локкеддовнлокалмачинезонеалловфонтдовнлоадс</span><span class="sxs-lookup"><span data-stu-id="78943-552">LockedDownLocalMachineZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-553">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-553">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-554">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-554">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-555">локкеддовнлокалмачинезонеалловлесспривилежедситес</span><span class="sxs-lookup"><span data-stu-id="78943-555">LockedDownLocalMachineZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-556">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-556">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-557">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-557">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-558">локкеддовнлокалмачинезонеалловнетфрамеворкрелианткомпонентс</span><span class="sxs-lookup"><span data-stu-id="78943-558">LockedDownLocalMachineZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-559">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-559">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-560">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-560">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-561">локкеддовнлокалмачинезонеалловскриптлетс</span><span class="sxs-lookup"><span data-stu-id="78943-561">LockedDownLocalMachineZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-562">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-562">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-563">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-563">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-564">локкеддовнлокалмачинезонеалловсмартскриние</span><span class="sxs-lookup"><span data-stu-id="78943-564">LockedDownLocalMachineZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-565">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-565">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-566">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-566">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-567">локкеддовнлокалмачинезонеалловусердатаперсистенце</span><span class="sxs-lookup"><span data-stu-id="78943-567">LockedDownLocalMachineZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-568">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-568">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-569">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-569">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-570">локкеддовнлокалмачинезонеинитиализеандскриптактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="78943-570">LockedDownLocalMachineZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-571">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-571">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-572">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-572">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-573">локкеддовнлокалмачинезонежавапермиссионс</span><span class="sxs-lookup"><span data-stu-id="78943-573">LockedDownLocalMachineZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-574">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-574">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-575">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-575">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-576">локкеддовнлокалмачинезоненавигатевиндовсандфрамес</span><span class="sxs-lookup"><span data-stu-id="78943-576">LockedDownLocalMachineZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-577">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-577">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-578">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-578">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-579">локкеддовнрестриктедситесзонеалловакцесстодатасаурцес</span><span class="sxs-lookup"><span data-stu-id="78943-579">LockedDownRestrictedSitesZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-580">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-580">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-581">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-581">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-582">локкеддовнрестриктедситесзонеалловаутоматикпромптингфорактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="78943-582">LockedDownRestrictedSitesZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-583">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-583">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-584">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-584">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-585">локкеддовнрестриктедситесзонеалловаутоматикпромптингфорфиледовнлоадс</span><span class="sxs-lookup"><span data-stu-id="78943-585">LockedDownRestrictedSitesZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-586">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-586">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-587">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-587">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-588">локкеддовнрестриктедситесзонеалловфонтдовнлоадс</span><span class="sxs-lookup"><span data-stu-id="78943-588">LockedDownRestrictedSitesZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-589">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-589">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-590">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-590">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-591">локкеддовнрестриктедситесзонеалловлесспривилежедситес</span><span class="sxs-lookup"><span data-stu-id="78943-591">LockedDownRestrictedSitesZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-592">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-592">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-593">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-593">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-594">локкеддовнрестриктедситесзонеалловнетфрамеворкрелианткомпонентс</span><span class="sxs-lookup"><span data-stu-id="78943-594">LockedDownRestrictedSitesZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-595">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-595">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-596">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-596">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-597">локкеддовнрестриктедситесзонеалловскриптлетс</span><span class="sxs-lookup"><span data-stu-id="78943-597">LockedDownRestrictedSitesZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-598">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-598">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-599">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-599">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-600">локкеддовнрестриктедситесзонеалловсмартскриние</span><span class="sxs-lookup"><span data-stu-id="78943-600">LockedDownRestrictedSitesZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-601">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-601">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-602">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-602">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-603">локкеддовнрестриктедситесзонеалловусердатаперсистенце</span><span class="sxs-lookup"><span data-stu-id="78943-603">LockedDownRestrictedSitesZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-604">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-604">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-605">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-605">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-606">локкеддовнрестриктедситесзонеинитиализеандскриптактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="78943-606">LockedDownRestrictedSitesZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-607">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-607">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-608">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-608">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-609">локкеддовнрестриктедситесзонежавапермиссионс</span><span class="sxs-lookup"><span data-stu-id="78943-609">LockedDownRestrictedSitesZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-610">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-610">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-611">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-611">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-612">локкеддовнрестриктедситесзоненавигатевиндовсандфрамес</span><span class="sxs-lookup"><span data-stu-id="78943-612">LockedDownRestrictedSitesZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-613">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-613">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-614">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-614">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-615">локкеддовнтрустедситесзонеалловакцесстодатасаурцес</span><span class="sxs-lookup"><span data-stu-id="78943-615">LockedDownTrustedSitesZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-616">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-616">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-617">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-617">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-618">локкеддовнтрустедситесзонеалловаутоматикпромптингфорактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="78943-618">LockedDownTrustedSitesZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-619">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-619">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-620">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-620">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-621">локкеддовнтрустедситесзонеалловаутоматикпромптингфорфиледовнлоадс</span><span class="sxs-lookup"><span data-stu-id="78943-621">LockedDownTrustedSitesZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-622">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-622">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-623">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-623">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-624">локкеддовнтрустедситесзонеалловфонтдовнлоадс</span><span class="sxs-lookup"><span data-stu-id="78943-624">LockedDownTrustedSitesZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-625">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-625">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-626">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-626">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-627">локкеддовнтрустедситесзонеалловлесспривилежедситес</span><span class="sxs-lookup"><span data-stu-id="78943-627">LockedDownTrustedSitesZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-628">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-628">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-629">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-629">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-630">локкеддовнтрустедситесзонеалловнетфрамеворкрелианткомпонентс</span><span class="sxs-lookup"><span data-stu-id="78943-630">LockedDownTrustedSitesZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-631">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-631">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-632">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-632">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-633">локкеддовнтрустедситесзонеалловскриптлетс</span><span class="sxs-lookup"><span data-stu-id="78943-633">LockedDownTrustedSitesZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-634">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-634">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-635">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-635">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-636">локкеддовнтрустедситесзонеалловсмартскриние</span><span class="sxs-lookup"><span data-stu-id="78943-636">LockedDownTrustedSitesZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-637">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-637">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-638">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-638">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-639">локкеддовнтрустедситесзонеалловусердатаперсистенце</span><span class="sxs-lookup"><span data-stu-id="78943-639">LockedDownTrustedSitesZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-640">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-640">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-641">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-641">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-642">локкеддовнтрустедситесзонеинитиализеандскриптактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="78943-642">LockedDownTrustedSitesZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-643">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-643">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-644">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-644">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-645">локкеддовнтрустедситесзонежавапермиссионс</span><span class="sxs-lookup"><span data-stu-id="78943-645">LockedDownTrustedSitesZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-646">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-646">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-647">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-647">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-648">локкеддовнтрустедситесзоненавигатевиндовсандфрамес</span><span class="sxs-lookup"><span data-stu-id="78943-648">LockedDownTrustedSitesZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-649">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-649">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-650">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-650">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-651">мимесниффингсафетифеатуреинтернетексплорерпроцессес</span><span class="sxs-lookup"><span data-stu-id="78943-651">MimeSniffingSafetyFeatureInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-mimesniffingsafetyfeatureinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-652">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-652">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-653">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-653">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-654">мкпротоколсекуритирестриктионинтернетексплорерпроцессес</span><span class="sxs-lookup"><span data-stu-id="78943-654">MKProtocolSecurityRestrictionInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-mkprotocolsecurityrestrictioninternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-655">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-655">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-656">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-656">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-657">нотификатионбаринтернетексплорерпроцессес</span><span class="sxs-lookup"><span data-stu-id="78943-657">NotificationBarInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-notificationbarinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-658">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-658">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-659">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-659">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="78943-660">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="78943-660">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-661">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-661">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-662">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="78943-662">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="78943-663">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="78943-663">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-664">превентманагингсмартскринфилтер</span><span class="sxs-lookup"><span data-stu-id="78943-664">PreventManagingSmartScreenFilter</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-preventmanagingsmartscreenfilter)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-665">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-665">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-666">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-666">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-667">превентперусеринсталлатионофактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="78943-667">PreventPerUserInstallationOfActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-preventperuserinstallationofactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-668">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-668">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-669">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-669">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-670">протектионфромзонилеватионинтернетексплорерпроцессес</span><span class="sxs-lookup"><span data-stu-id="78943-670">ProtectionFromZoneElevationInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-protectionfromzoneelevationinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-671">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-671">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-672">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-672">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-673">ремоверунсистимебуттонфораутдатедактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="78943-673">RemoveRunThisTimeButtonForOutdatedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-removerunthistimebuttonforoutdatedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-674">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-674">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-675">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-675">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-676">рестриктактивексинсталлинтернетексплорерпроцессес</span><span class="sxs-lookup"><span data-stu-id="78943-676">RestrictActiveXInstallInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictactivexinstallinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-677">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-677">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-678">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-678">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-679">рестриктедситесзонеалловакцесстодатасаурцес</span><span class="sxs-lookup"><span data-stu-id="78943-679">RestrictedSitesZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-680">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-680">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-681">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-681">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-682">рестриктедситесзонеалловактивескриптинг</span><span class="sxs-lookup"><span data-stu-id="78943-682">RestrictedSitesZoneAllowActiveScripting</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowactivescripting)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-683">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-683">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-684">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-684">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-685">рестриктедситесзонеалловаутоматикпромптингфорактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="78943-685">RestrictedSitesZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-686">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-686">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-687">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-687">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-688">рестриктедситесзонеалловаутоматикпромптингфорфиледовнлоадс</span><span class="sxs-lookup"><span data-stu-id="78943-688">RestrictedSitesZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-689">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-689">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-690">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-690">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-691">рестриктедситесзонеалловбинаряндскриптбехавиорс</span><span class="sxs-lookup"><span data-stu-id="78943-691">RestrictedSitesZoneAllowBinaryAndScriptBehaviors</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowbinaryandscriptbehaviors)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-692">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-692">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-693">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-693">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-694">рестриктедситесзонеалловкопипастевиаскрипт</span><span class="sxs-lookup"><span data-stu-id="78943-694">RestrictedSitesZoneAllowCopyPasteViaScript</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowcopypasteviascript)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-695">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-695">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-696">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-696">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-697">рестриктедситесзонеалловдраганддропкопяндпастефилес</span><span class="sxs-lookup"><span data-stu-id="78943-697">RestrictedSitesZoneAllowDragAndDropCopyAndPasteFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowdraganddropcopyandpastefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-698">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-698">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-699">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-699">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-700">рестриктедситесзонеалловфиледовнлоадс</span><span class="sxs-lookup"><span data-stu-id="78943-700">RestrictedSitesZoneAllowFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-701">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-701">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-702">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-702">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-703">рестриктедситесзонеалловфонтдовнлоадс</span><span class="sxs-lookup"><span data-stu-id="78943-703">RestrictedSitesZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-704">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-704">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-705">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-705">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-706">рестриктедситесзонеалловлесспривилежедситес</span><span class="sxs-lookup"><span data-stu-id="78943-706">RestrictedSitesZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-707">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-707">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-708">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-708">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-709">рестриктедситесзонеалловлоадингофксамлфилес</span><span class="sxs-lookup"><span data-stu-id="78943-709">RestrictedSitesZoneAllowLoadingOfXAMLFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowloadingofxamlfiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-710">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-710">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-711">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-711">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-712">рестриктедситесзонеалловметарефреш</span><span class="sxs-lookup"><span data-stu-id="78943-712">RestrictedSitesZoneAllowMETAREFRESH</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowmetarefresh)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-713">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-713">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-714">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-714">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-715">рестриктедситесзонеалловнетфрамеворкрелианткомпонентс</span><span class="sxs-lookup"><span data-stu-id="78943-715">RestrictedSitesZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-716">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-716">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-717">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-717">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-718">рестриктедситесзонеалловонляппроведдомаинстаусеактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="78943-718">RestrictedSitesZoneAllowOnlyApprovedDomainsToUseActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowonlyapproveddomainstouseactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-719">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-719">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-720">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-720">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-721">рестриктедситесзонеалловонляппроведдомаинстаусетдкактивексконтрол</span><span class="sxs-lookup"><span data-stu-id="78943-721">RestrictedSitesZoneAllowOnlyApprovedDomainsToUseTDCActiveXControl</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowonlyapproveddomainstousetdcactivexcontrol)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-722">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-722">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-723">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-723">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-724">рестриктедситесзонеалловскриптингофинтернетексплорервеббровсерконтролс</span><span class="sxs-lookup"><span data-stu-id="78943-724">RestrictedSitesZoneAllowScriptingOfInternetExplorerWebBrowserControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowscriptingofinternetexplorerwebbrowsercontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-725">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-725">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-726">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-726">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-727">рестриктедситесзонеалловскриптинитиатедвиндовс</span><span class="sxs-lookup"><span data-stu-id="78943-727">RestrictedSitesZoneAllowScriptInitiatedWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowscriptinitiatedwindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-728">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-728">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-729">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-729">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-730">рестриктедситесзонеалловскриптлетс</span><span class="sxs-lookup"><span data-stu-id="78943-730">RestrictedSitesZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-731">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-731">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-732">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-732">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-733">рестриктедситесзонеалловсмартскриние</span><span class="sxs-lookup"><span data-stu-id="78943-733">RestrictedSitesZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-734">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-734">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-735">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-735">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-736">рестриктедситесзонеалловупдатестостатусбарвиаскрипт</span><span class="sxs-lookup"><span data-stu-id="78943-736">RestrictedSitesZoneAllowUpdatesToStatusBarViaScript</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowupdatestostatusbarviascript)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-737">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-737">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-738">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-738">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-739">рестриктедситесзонеалловусердатаперсистенце</span><span class="sxs-lookup"><span data-stu-id="78943-739">RestrictedSitesZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-740">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-740">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-741">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-741">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-742">рестриктедситесзонедонотрунантималвареагаинстактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="78943-742">RestrictedSitesZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-743">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-743">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-744">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-744">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-745">рестриктедситесзонедовнлоадсигнедактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="78943-745">RestrictedSitesZoneDownloadSignedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonedownloadsignedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-746">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-746">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-747">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-747">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-748">рестриктедситесзонедовнлоадунсигнедактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="78943-748">RestrictedSitesZoneDownloadUnsignedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonedownloadunsignedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-749">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-749">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-750">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-750">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-751">рестриктедситесзонинаблекроссситескриптингфилтер</span><span class="sxs-lookup"><span data-stu-id="78943-751">RestrictedSitesZoneEnableCrossSiteScriptingFilter</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneenablecrosssitescriptingfilter)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-752">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-752">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-753">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-753">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-754">рестриктедситесзонинабледраггингофконтентфромдифферентдомаинсакроссвиндовс</span><span class="sxs-lookup"><span data-stu-id="78943-754">RestrictedSitesZoneEnableDraggingOfContentFromDifferentDomainsAcrossWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneenabledraggingofcontentfromdifferentdomainsacrosswindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-755">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-755">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-756">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-756">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-757">рестриктедситесзонинабледраггингофконтентфромдифферентдомаинсвисинвиндовс</span><span class="sxs-lookup"><span data-stu-id="78943-757">RestrictedSitesZoneEnableDraggingOfContentFromDifferentDomainsWithinWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneenabledraggingofcontentfromdifferentdomainswithinwindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-758">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-758">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-759">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-759">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-760">рестриктедситесзонинаблемимесниффинг</span><span class="sxs-lookup"><span data-stu-id="78943-760">RestrictedSitesZoneEnableMIMESniffing</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneenablemimesniffing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-761">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-761">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-762">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-762">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-763">рестриктедситесзонеинклуделокалпасвхенуплоадингфилестосервер</span><span class="sxs-lookup"><span data-stu-id="78943-763">RestrictedSitesZoneIncludeLocalPathWhenUploadingFilesToServer</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneincludelocalpathwhenuploadingfilestoserver)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-764">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-764">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-765">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-765">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-766">рестриктедситесзонеинитиализеандскриптактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="78943-766">RestrictedSitesZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-767">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-767">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-768">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-768">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-769">рестриктедситесзонежавапермиссионс</span><span class="sxs-lookup"><span data-stu-id="78943-769">RestrictedSitesZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-770">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-770">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-771">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-771">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-772">рестриктедситесзонелаунчингаппликатионсандфилесинифраме</span><span class="sxs-lookup"><span data-stu-id="78943-772">RestrictedSitesZoneLaunchingApplicationsAndFilesInIFRAME</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonelaunchingapplicationsandfilesiniframe)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-773">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-773">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-774">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-774">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-775">рестриктедситесзонелогоноптионс</span><span class="sxs-lookup"><span data-stu-id="78943-775">RestrictedSitesZoneLogonOptions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonelogonoptions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-776">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-776">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-777">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-777">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-778">рестриктедситесзоненавигатевиндовсандфрамес</span><span class="sxs-lookup"><span data-stu-id="78943-778">RestrictedSitesZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-779">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-779">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-780">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-780">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="78943-781">рестриктедситесзоненавигатевиндовсандфрамесакроссдомаинс</span><span class="sxs-lookup"><span data-stu-id="78943-781">RestrictedSitesZoneNavigateWindowsAndFramesAcrossDomains</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-782">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-782">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-783">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-783">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-784">рестриктедситесзонерунактивексконтролсандплугинс</span><span class="sxs-lookup"><span data-stu-id="78943-784">RestrictedSitesZoneRunActiveXControlsAndPlugins</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonerunactivexcontrolsandplugins)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-785">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-785">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-786">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-786">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-787">рестриктедситесзонеруннетфрамеворкрелианткомпонентссигнедвисаусентикоде</span><span class="sxs-lookup"><span data-stu-id="78943-787">RestrictedSitesZoneRunNETFrameworkReliantComponentsSignedWithAuthenticode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonerunnetframeworkreliantcomponentssignedwithauthenticode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-788">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-788">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-789">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-789">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-790">рестриктедситесзонескриптактивексконтролсмаркедсафефорскриптинг</span><span class="sxs-lookup"><span data-stu-id="78943-790">RestrictedSitesZoneScriptActiveXControlsMarkedSafeForScripting</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonescriptactivexcontrolsmarkedsafeforscripting)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-791">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-791">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-792">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-792">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-793">рестриктедситесзонескриптингофжаваапплетс</span><span class="sxs-lookup"><span data-stu-id="78943-793">RestrictedSitesZoneScriptingOfJavaApplets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonescriptingofjavaapplets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-794">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-794">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-795">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-795">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-796">рестриктедситесзонешовсекуритиварнингфорпотентиаллюнсафефилес</span><span class="sxs-lookup"><span data-stu-id="78943-796">RestrictedSitesZoneShowSecurityWarningForPotentiallyUnsafeFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneshowsecuritywarningforpotentiallyunsafefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-797">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-797">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-798">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-798">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="78943-799">рестриктедситесзонетурнонкроссситескриптингфилтер</span><span class="sxs-lookup"><span data-stu-id="78943-799">RestrictedSitesZoneTurnOnCrossSiteScriptingFilter</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-800">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-800">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-801">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-801">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-802">рестриктедситесзонетурнонпротектедмоде</span><span class="sxs-lookup"><span data-stu-id="78943-802">RestrictedSitesZoneTurnOnProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneturnonprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-803">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-803">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-804">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-804">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-805">рестриктедситесзонеусепопупблоккер</span><span class="sxs-lookup"><span data-stu-id="78943-805">RestrictedSitesZoneUsePopupBlocker</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneusepopupblocker)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-806">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-806">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-807">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-807">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-808">рестриктфиледовнлоадинтернетексплорерпроцессес</span><span class="sxs-lookup"><span data-stu-id="78943-808">RestrictFileDownloadInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictfiledownloadinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-809">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-809">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-810">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-810">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-811">скриптедвиндовсекуритирестриктионсинтернетексплорерпроцессес</span><span class="sxs-lookup"><span data-stu-id="78943-811">ScriptedWindowSecurityRestrictionsInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-scriptedwindowsecurityrestrictionsinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-812">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-812">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-813">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-813">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-814">SearchProviderList</span><span class="sxs-lookup"><span data-stu-id="78943-814">SearchProviderList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-searchproviderlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-815">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-815">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-816">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-816">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-817">секуритизонесусеонлимачинесеттингс</span><span class="sxs-lookup"><span data-stu-id="78943-817">SecurityZonesUseOnlyMachineSettings</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-securityzonesuseonlymachinesettings)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-818">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-818">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-819">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-819">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-820">спеЦифюсеофактивексинсталлерсервице</span><span class="sxs-lookup"><span data-stu-id="78943-820">SpecifyUseOfActiveXInstallerService</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-specifyuseofactivexinstallerservice)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-821">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-821">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-822">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-822">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-823">трустедситесзонеалловакцесстодатасаурцес</span><span class="sxs-lookup"><span data-stu-id="78943-823">TrustedSitesZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-824">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-824">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-825">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-825">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-826">трустедситесзонеалловаутоматикпромптингфорактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="78943-826">TrustedSitesZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-827">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-827">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-828">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-828">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-829">трустедситесзонеалловаутоматикпромптингфорфиледовнлоадс</span><span class="sxs-lookup"><span data-stu-id="78943-829">TrustedSitesZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-830">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-830">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-831">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-831">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-832">трустедситесзонеалловфонтдовнлоадс</span><span class="sxs-lookup"><span data-stu-id="78943-832">TrustedSitesZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-833">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-833">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-834">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-834">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-835">трустедситесзонеалловлесспривилежедситес</span><span class="sxs-lookup"><span data-stu-id="78943-835">TrustedSitesZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-836">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-836">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-837">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-837">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-838">трустедситесзонеалловнетфрамеворкрелианткомпонентс</span><span class="sxs-lookup"><span data-stu-id="78943-838">TrustedSitesZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-839">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-839">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-840">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-840">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-841">трустедситесзонеалловскриптлетс</span><span class="sxs-lookup"><span data-stu-id="78943-841">TrustedSitesZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-842">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-842">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-843">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-843">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-844">трустедситесзонеалловсмартскриние</span><span class="sxs-lookup"><span data-stu-id="78943-844">TrustedSitesZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-845">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-845">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-846">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-846">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-847">трустедситесзонеалловусердатаперсистенце</span><span class="sxs-lookup"><span data-stu-id="78943-847">TrustedSitesZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-848">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-848">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-849">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-849">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-850">трустедситесзонедонотрунантималвареагаинстактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="78943-850">TrustedSitesZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-851">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-851">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-852">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-852">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="78943-853">трустедситесзонедонтрунантималварепрограмсагаинстактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="78943-853">TrustedSitesZoneDontRunAntimalwareProgramsAgainstActiveXControls</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-854">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-854">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-855">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-855">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-856">трустедситесзонеинитиализеандскриптактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="78943-856">TrustedSitesZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-857">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-857">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-858">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-858">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="78943-859">трустедситесзонеинитиализеандскриптактивексконтролснотмаркедассафе</span><span class="sxs-lookup"><span data-stu-id="78943-859">TrustedSitesZoneInitializeAndScriptActiveXControlsNotMarkedAsSafe</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-860">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-860">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-861">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-861">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="78943-862">трустедситесзонеинитиализеандскриптактивексконтролснотмаркедсафе</span><span class="sxs-lookup"><span data-stu-id="78943-862">TrustedSitesZoneInitializeAndScriptActiveXControlsNotMarkedSafe</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-863">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-863">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-864">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-864">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-865">трустедситесзонежавапермиссионс</span><span class="sxs-lookup"><span data-stu-id="78943-865">TrustedSitesZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-866">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-866">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-867">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-867">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="78943-868">трустедситесзоненавигатевиндовсандфрамес</span><span class="sxs-lookup"><span data-stu-id="78943-868">TrustedSitesZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78943-869">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78943-869">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78943-870">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78943-870">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="78943-871">Требования</span><span class="sxs-lookup"><span data-stu-id="78943-871">Requirements</span></span>



| <span data-ttu-id="78943-872">Требование</span><span class="sxs-lookup"><span data-stu-id="78943-872">Requirement</span></span> | <span data-ttu-id="78943-873">Значение</span><span class="sxs-lookup"><span data-stu-id="78943-873">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78943-874">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="78943-874">Minimum supported client</span></span><br/> | <span data-ttu-id="78943-875">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="78943-875">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="78943-876">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="78943-876">Minimum supported server</span></span><br/> | <span data-ttu-id="78943-877">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="78943-877">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="78943-878">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="78943-878">Namespace</span></span><br/>                | <span data-ttu-id="78943-879">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="78943-879">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="78943-880">MOF</span><span class="sxs-lookup"><span data-stu-id="78943-880">MOF</span></span><br/>                      | <dl> <span data-ttu-id="78943-881"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="78943-881"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="78943-882">DLL</span><span class="sxs-lookup"><span data-stu-id="78943-882">DLL</span></span><br/>                      | <dl> <span data-ttu-id="78943-883"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="78943-883"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

