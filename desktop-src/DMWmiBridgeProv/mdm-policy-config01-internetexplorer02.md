---
title: Класс MDM_Policy_Config01_InternetExplorer02
description: '\_Класс политики MDM \_ Config01 \_ InternetExplorer02 настраивает политики Internet Explorer.'
ms.assetid: 32cc6a64-3008-4add-96e8-33b31beb207f
keywords:
- Класс MDM_Policy_Config01_InternetExplorer02
- MDM_Policy_Config01_InternetExplorer02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_InternetExplorer02
- MDM_Policy_Config01_InternetExplorer02.InstanceID
- MDM_Policy_Config01_InternetExplorer02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48a448b0034e3f4658f1c13b238abf455bf413a3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490509"
---
# <a name="mdm_policy_config01_internetexplorer02-class"></a><span data-ttu-id="f768e-105">\_Класс политики MDM \_ Config01 \_ InternetExplorer02</span><span class="sxs-lookup"><span data-stu-id="f768e-105">MDM\_Policy\_Config01\_InternetExplorer02 class</span></span>

<span data-ttu-id="f768e-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="f768e-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="f768e-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="f768e-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="f768e-108">\_Класс политики MDM \_ Config01 \_ InternetExplorer02 настраивает политики Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="f768e-108">The MDM\_Policy\_Config01\_InternetExplorer02 class configures the Internet Explorer policies.</span></span>

<span data-ttu-id="f768e-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="f768e-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f768e-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f768e-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_InternetExplorer02
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

## <a name="members"></a><span data-ttu-id="f768e-111">Члены</span><span class="sxs-lookup"><span data-stu-id="f768e-111">Members</span></span>

<span data-ttu-id="f768e-112">Класс **\_ политики MDM \_ Config01 \_ InternetExplorer02** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="f768e-112">The **MDM\_Policy\_Config01\_InternetExplorer02** class has these types of members:</span></span>

-   [<span data-ttu-id="f768e-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="f768e-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f768e-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="f768e-114">Properties</span></span>

<span data-ttu-id="f768e-115">Класс **\_ политики MDM \_ Config01 \_ InternetExplorer02** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="f768e-115">The **MDM\_Policy\_Config01\_InternetExplorer02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="f768e-116">AddSearchProvider</span><span class="sxs-lookup"><span data-stu-id="f768e-116">AddSearchProvider</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-addsearchprovider)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-117">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-119">алловактивексфилтеринг</span><span class="sxs-lookup"><span data-stu-id="f768e-119">AllowActiveXFiltering</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowactivexfiltering)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-121">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-122">алловаддонлист</span><span class="sxs-lookup"><span data-stu-id="f768e-122">AllowAddOnList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowaddonlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-123">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-124">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-125">алловцертификатеаддрессмисматчварнинг</span><span class="sxs-lookup"><span data-stu-id="f768e-125">AllowCertificateAddressMismatchWarning</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowcertificateaddressmismatchwarning)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-126">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-127">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-128">алловделетингбровсингхисторйонексит</span><span class="sxs-lookup"><span data-stu-id="f768e-128">AllowDeletingBrowsingHistoryOnExit</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowdeletingbrowsinghistoryonexit)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-129">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-130">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-131">алловенханцедпротектедмоде</span><span class="sxs-lookup"><span data-stu-id="f768e-131">AllowEnhancedProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowenhancedprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-132">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-133">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-134">алловентерприсемодефромтулсмену</span><span class="sxs-lookup"><span data-stu-id="f768e-134">AllowEnterpriseModeFromToolsMenu</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowenterprisemodefromtoolsmenu)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-135">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-136">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-137">алловентерприсемодесителист</span><span class="sxs-lookup"><span data-stu-id="f768e-137">AllowEnterpriseModeSiteList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowenterprisemodesitelist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-138">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-139">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-140">AllowFallbackToSSL3</span><span class="sxs-lookup"><span data-stu-id="f768e-140">AllowFallbackToSSL3</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowfallbacktossl3)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-141">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-142">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-143">AllowInternetExplorer7PolicyList</span><span class="sxs-lookup"><span data-stu-id="f768e-143">AllowInternetExplorer7PolicyList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowinternetexplorer7policylist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-144">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-145">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-146">алловинтернетексплорерстандардсмоде</span><span class="sxs-lookup"><span data-stu-id="f768e-146">AllowInternetExplorerStandardsMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowinternetexplorerstandardsmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-147">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-148">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-149">алловинтернетзонетемплате</span><span class="sxs-lookup"><span data-stu-id="f768e-149">AllowInternetZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowinternetzonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-150">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-151">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-152">алловинтранетзонетемплате</span><span class="sxs-lookup"><span data-stu-id="f768e-152">AllowIntranetZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowintranetzonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-153">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-154">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-155">алловлокалмачинезонетемплате</span><span class="sxs-lookup"><span data-stu-id="f768e-155">AllowLocalMachineZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlocalmachinezonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-156">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-157">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-158">алловлоккеддовнинтернетзонетемплате</span><span class="sxs-lookup"><span data-stu-id="f768e-158">AllowLockedDownInternetZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlockeddowninternetzonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-159">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-160">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-161">алловлоккеддовнинтранетзонетемплате</span><span class="sxs-lookup"><span data-stu-id="f768e-161">AllowLockedDownIntranetZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlockeddownintranetzonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-162">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-163">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-164">алловлоккеддовнлокалмачинезонетемплате</span><span class="sxs-lookup"><span data-stu-id="f768e-164">AllowLockedDownLocalMachineZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlockeddownlocalmachinezonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-165">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-166">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-166">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-167">алловлоккеддовнрестриктедситесзонетемплате</span><span class="sxs-lookup"><span data-stu-id="f768e-167">AllowLockedDownRestrictedSitesZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlockeddownrestrictedsiteszonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-168">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-169">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-169">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-170">алловоневордентри</span><span class="sxs-lookup"><span data-stu-id="f768e-170">AllowOneWordEntry</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowonewordentry)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-171">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-172">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-172">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-173">алловситетозонеассигнментлист</span><span class="sxs-lookup"><span data-stu-id="f768e-173">AllowSiteToZoneAssignmentList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowsitetozoneassignmentlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-174">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-175">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-175">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-176">алловслоккеддовнтрустедситесзонетемплате</span><span class="sxs-lookup"><span data-stu-id="f768e-176">AllowsLockedDownTrustedSitesZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowslockeddowntrustedsiteszonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-177">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-178">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-178">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-179">алловсофтваревхенсигнатуреисинвалид</span><span class="sxs-lookup"><span data-stu-id="f768e-179">AllowSoftwareWhenSignatureIsInvalid</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowsoftwarewhensignatureisinvalid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-180">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-181">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-181">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-182">алловсрестриктедситесзонетемплате</span><span class="sxs-lookup"><span data-stu-id="f768e-182">AllowsRestrictedSitesZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowsrestrictedsiteszonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-183">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-184">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-184">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-185">алловсугжестедситес</span><span class="sxs-lookup"><span data-stu-id="f768e-185">AllowSuggestedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowsuggestedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-186">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-187">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-187">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-188">алловтрустедситесзонетемплате</span><span class="sxs-lookup"><span data-stu-id="f768e-188">AllowTrustedSitesZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowtrustedsiteszonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-189">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-190">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-190">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-191">чекксерверцертификатеревокатион</span><span class="sxs-lookup"><span data-stu-id="f768e-191">CheckServerCertificateRevocation</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-checkservercertificaterevocation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-192">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-193">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-193">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-194">чекксигнатуресондовнлоадедпрограмс</span><span class="sxs-lookup"><span data-stu-id="f768e-194">CheckSignaturesOnDownloadedPrograms</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-checksignaturesondownloadedprograms)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-195">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-196">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-196">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-197">консистентмимехандлингинтернетексплорерпроцессес</span><span class="sxs-lookup"><span data-stu-id="f768e-197">ConsistentMimeHandlingInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-consistentmimehandlinginternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-198">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-199">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-199">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-200">дисаблеадобефлаш</span><span class="sxs-lookup"><span data-stu-id="f768e-200">DisableAdobeFlash</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableadobeflash)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-201">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-202">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-202">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f768e-203">дисаблеблоккингофаутдатедактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="f768e-203">DisableBlockingOfOutdatedActiveXControls</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-204">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-204">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-205">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-205">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-206">дисаблебипассофсмартскринварнингс</span><span class="sxs-lookup"><span data-stu-id="f768e-206">DisableBypassOfSmartScreenWarnings</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablebypassofsmartscreenwarnings)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-207">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-208">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-208">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-209">дисаблебипассофсмартскринварнингсабаутункоммонфилес</span><span class="sxs-lookup"><span data-stu-id="f768e-209">DisableBypassOfSmartScreenWarningsAboutUncommonFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablebypassofsmartscreenwarningsaboutuncommonfiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-210">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-211">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-211">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-212">дисаблеконфигурингхистори</span><span class="sxs-lookup"><span data-stu-id="f768e-212">DisableConfiguringHistory</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableconfiguringhistory)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-213">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-214">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-214">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-215">дисаблекрашдетектион</span><span class="sxs-lookup"><span data-stu-id="f768e-215">DisableCrashDetection</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablecrashdetection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-216">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-216">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-217">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-217">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-218">дисаблекустомерекспериенцеимпровементпрогрампартиЦипатион</span><span class="sxs-lookup"><span data-stu-id="f768e-218">DisableCustomerExperienceImprovementProgramParticipation</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablecustomerexperienceimprovementprogramparticipation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-219">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-220">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-220">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-221">дисабледелетингусервиситедвебситес</span><span class="sxs-lookup"><span data-stu-id="f768e-221">DisableDeletingUserVisitedWebsites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disabledeletinguservisitedwebsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-222">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-223">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-223">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-224">дисаблинклосуредовнлоадинг</span><span class="sxs-lookup"><span data-stu-id="f768e-224">DisableEnclosureDownloading</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableenclosuredownloading)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-225">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-226">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-226">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-227">дисаблинкриптионсуппорт</span><span class="sxs-lookup"><span data-stu-id="f768e-227">DisableEncryptionSupport</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableencryptionsupport)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-228">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-228">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-229">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-229">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-230">дисаблефирструнвизард</span><span class="sxs-lookup"><span data-stu-id="f768e-230">DisableFirstRunWizard</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablefirstrunwizard)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-231">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-231">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-232">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-232">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-233">дисаблефлипахеадфеатуре</span><span class="sxs-lookup"><span data-stu-id="f768e-233">DisableFlipAheadFeature</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableflipaheadfeature)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-234">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-234">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-235">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-235">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-236">дисаблеигнорингцертификатиррорс</span><span class="sxs-lookup"><span data-stu-id="f768e-236">DisableIgnoringCertificateErrors</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableignoringcertificateerrors)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-237">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-237">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-238">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-238">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-239">дисаблеинприватебровсинг</span><span class="sxs-lookup"><span data-stu-id="f768e-239">DisableInPrivateBrowsing</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableinprivatebrowsing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-240">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-240">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-241">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-241">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-242">дисаблепроцессесиненханцедпротектедмоде</span><span class="sxs-lookup"><span data-stu-id="f768e-242">DisableProcessesInEnhancedProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableprocessesinenhancedprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-243">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-243">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-244">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-244">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-245">дисаблепроксичанже</span><span class="sxs-lookup"><span data-stu-id="f768e-245">DisableProxyChange</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableproxychange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-246">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-246">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-247">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-247">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-248">дисаблесеарчпровидерчанже</span><span class="sxs-lookup"><span data-stu-id="f768e-248">DisableSearchProviderChange</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablesearchproviderchange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-249">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-250">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-250">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-251">дисаблесекондарихомепажечанже</span><span class="sxs-lookup"><span data-stu-id="f768e-251">DisableSecondaryHomePageChange</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablesecondaryhomepagechange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-252">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-253">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-253">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-254">дисаблесекуритисеттингсчекк</span><span class="sxs-lookup"><span data-stu-id="f768e-254">DisableSecuritySettingsCheck</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablesecuritysettingscheck)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-255">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-255">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-256">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-256">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-257">дисаблеупдатечекк</span><span class="sxs-lookup"><span data-stu-id="f768e-257">DisableUpdateCheck</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableupdatecheck)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-258">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-259">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-259">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-260">доноталловактивексконтролсинпротектедмоде</span><span class="sxs-lookup"><span data-stu-id="f768e-260">DoNotAllowActiveXControlsInProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-donotallowactivexcontrolsinprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-261">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-262">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-262">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-263">доноталловусерстоаддситес</span><span class="sxs-lookup"><span data-stu-id="f768e-263">DoNotAllowUsersToAddSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-donotallowuserstoaddsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-264">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-265">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-265">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-266">доноталловусерсточанжеполиЦиес</span><span class="sxs-lookup"><span data-stu-id="f768e-266">DoNotAllowUsersToChangePolicies</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-donotallowuserstochangepolicies)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-267">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-267">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-268">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-268">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-269">донотблоккаутдатедактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="f768e-269">DoNotBlockOutdatedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-donotblockoutdatedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-270">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-270">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-271">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-271">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-272">донотблоккаутдатедактивексконтролсонспеЦификдомаинс</span><span class="sxs-lookup"><span data-stu-id="f768e-272">DoNotBlockOutdatedActiveXControlsOnSpecificDomains</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-donotblockoutdatedactivexcontrolsonspecificdomains)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-273">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-273">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-274">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-274">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-275">инклудеалллокалситес</span><span class="sxs-lookup"><span data-stu-id="f768e-275">IncludeAllLocalSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-includealllocalsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-276">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-276">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-277">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-277">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-278">инклудеаллнетворкпасс</span><span class="sxs-lookup"><span data-stu-id="f768e-278">IncludeAllNetworkPaths</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-includeallnetworkpaths)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-279">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-279">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-280">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-280">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f768e-281">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="f768e-281">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-282">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-282">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-283">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f768e-283">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f768e-284">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f768e-284">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-285">интернетзонеалловакцесстодатасаурцес</span><span class="sxs-lookup"><span data-stu-id="f768e-285">InternetZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-286">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-286">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-287">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-287">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-288">интернетзонеалловаутоматикпромптингфорактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="f768e-288">InternetZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-289">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-289">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-290">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-290">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-291">интернетзонеалловаутоматикпромптингфорфиледовнлоадс</span><span class="sxs-lookup"><span data-stu-id="f768e-291">InternetZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-292">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-292">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-293">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-293">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-294">интернетзонеалловкопипастевиаскрипт</span><span class="sxs-lookup"><span data-stu-id="f768e-294">InternetZoneAllowCopyPasteViaScript</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowcopypasteviascript)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-295">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-295">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-296">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-296">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-297">интернетзонеалловдраганддропкопяндпастефилес</span><span class="sxs-lookup"><span data-stu-id="f768e-297">InternetZoneAllowDragAndDropCopyAndPasteFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowdraganddropcopyandpastefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-298">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-298">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-299">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-299">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-300">интернетзонеалловфонтдовнлоадс</span><span class="sxs-lookup"><span data-stu-id="f768e-300">InternetZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-301">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-301">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-302">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-302">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-303">интернетзонеалловлесспривилежедситес</span><span class="sxs-lookup"><span data-stu-id="f768e-303">InternetZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-304">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-304">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-305">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-305">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-306">интернетзонеалловлоадингофксамлфилес</span><span class="sxs-lookup"><span data-stu-id="f768e-306">InternetZoneAllowLoadingOfXAMLFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowloadingofxamlfiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-307">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-308">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-308">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-309">интернетзонеалловнетфрамеворкрелианткомпонентс</span><span class="sxs-lookup"><span data-stu-id="f768e-309">InternetZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-310">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-310">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-311">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-311">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-312">интернетзонеалловонляппроведдомаинстаусеактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="f768e-312">InternetZoneAllowOnlyApprovedDomainsToUseActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowonlyapproveddomainstouseactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-313">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-313">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-314">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-314">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-315">интернетзонеалловонляппроведдомаинстаусетдкактивексконтрол</span><span class="sxs-lookup"><span data-stu-id="f768e-315">InternetZoneAllowOnlyApprovedDomainsToUseTDCActiveXControl</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowonlyapproveddomainstousetdcactivexcontrol)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-316">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-316">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-317">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-317">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-318">интернетзонеалловскриптингофинтернетексплорервеббровсерконтролс</span><span class="sxs-lookup"><span data-stu-id="f768e-318">InternetZoneAllowScriptingOfInternetExplorerWebBrowserControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowscriptingofinternetexplorerwebbrowsercontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-319">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-319">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-320">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-320">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-321">интернетзонеалловскриптинитиатедвиндовс</span><span class="sxs-lookup"><span data-stu-id="f768e-321">InternetZoneAllowScriptInitiatedWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowscriptinitiatedwindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-322">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-322">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-323">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-323">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-324">интернетзонеалловскриптлетс</span><span class="sxs-lookup"><span data-stu-id="f768e-324">InternetZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-325">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-325">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-326">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-326">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-327">интернетзонеалловсмартскриние</span><span class="sxs-lookup"><span data-stu-id="f768e-327">InternetZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-328">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-328">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-329">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-329">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-330">интернетзонеалловупдатестостатусбарвиаскрипт</span><span class="sxs-lookup"><span data-stu-id="f768e-330">InternetZoneAllowUpdatesToStatusBarViaScript</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowupdatestostatusbarviascript)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-331">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-331">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-332">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-332">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-333">интернетзонеалловусердатаперсистенце</span><span class="sxs-lookup"><span data-stu-id="f768e-333">InternetZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-334">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-334">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-335">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-335">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-336">интернетзонедонотрунантималвареагаинстактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="f768e-336">InternetZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-337">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-337">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-338">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-338">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-339">интернетзонедовнлоадсигнедактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="f768e-339">InternetZoneDownloadSignedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonedownloadsignedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-340">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-340">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-341">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-341">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-342">интернетзонедовнлоадунсигнедактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="f768e-342">InternetZoneDownloadUnsignedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonedownloadunsignedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-343">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-343">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-344">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-344">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-345">интернетзонинаблекроссситескриптингфилтер</span><span class="sxs-lookup"><span data-stu-id="f768e-345">InternetZoneEnableCrossSiteScriptingFilter</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenablecrosssitescriptingfilter)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-346">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-346">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-347">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-347">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-348">интернетзонинабледраггингофконтентфромдифферентдомаинсакроссвиндовс</span><span class="sxs-lookup"><span data-stu-id="f768e-348">InternetZoneEnableDraggingOfContentFromDifferentDomainsAcrossWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenabledraggingofcontentfromdifferentdomainsacrosswindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-349">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-349">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-350">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-350">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-351">интернетзонинабледраггингофконтентфромдифферентдомаинсвисинвиндовс</span><span class="sxs-lookup"><span data-stu-id="f768e-351">InternetZoneEnableDraggingOfContentFromDifferentDomainsWithinWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenabledraggingofcontentfromdifferentdomainswithinwindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-352">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-352">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-353">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-353">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-354">интернетзонинаблемимесниффинг</span><span class="sxs-lookup"><span data-stu-id="f768e-354">InternetZoneEnableMIMESniffing</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenablemimesniffing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-355">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-355">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-356">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-356">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-357">интернетзонинаблепротектедмоде</span><span class="sxs-lookup"><span data-stu-id="f768e-357">InternetZoneEnableProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenableprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-358">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-358">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-359">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-359">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-360">интернетзонеинклуделокалпасвхенуплоадингфилестосервер</span><span class="sxs-lookup"><span data-stu-id="f768e-360">InternetZoneIncludeLocalPathWhenUploadingFilesToServer</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneincludelocalpathwhenuploadingfilestoserver)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-361">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-361">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-362">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-362">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-363">интернетзонеинитиализеандскриптактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="f768e-363">InternetZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-364">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-364">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-365">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-365">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-366">интернетзонежавапермиссионс</span><span class="sxs-lookup"><span data-stu-id="f768e-366">InternetZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-367">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-367">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-368">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-368">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-369">интернетзонелаунчингаппликатионсандфилесинифраме</span><span class="sxs-lookup"><span data-stu-id="f768e-369">InternetZoneLaunchingApplicationsAndFilesInIFRAME</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonelaunchingapplicationsandfilesiniframe)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-370">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-370">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-371">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-371">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-372">интернетзонелогоноптионс</span><span class="sxs-lookup"><span data-stu-id="f768e-372">InternetZoneLogonOptions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonelogonoptions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-373">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-373">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-374">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-374">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-375">интернетзоненавигатевиндовсандфрамес</span><span class="sxs-lookup"><span data-stu-id="f768e-375">InternetZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-376">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-376">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-377">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-377">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f768e-378">интернетзонеруннетфрамеворкрелианткомпонентснотсигнедвисаусентикоде</span><span class="sxs-lookup"><span data-stu-id="f768e-378">InternetZoneRunNETFrameworkReliantComponentsNotSignedWithAuthenticode</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-379">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-379">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-380">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-380">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-381">интернетзонеруннетфрамеворкрелианткомпонентссигнедвисаусентикоде</span><span class="sxs-lookup"><span data-stu-id="f768e-381">InternetZoneRunNETFrameworkReliantComponentsSignedWithAuthenticode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonerunnetframeworkreliantcomponentssignedwithauthenticode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-382">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-382">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-383">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-383">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-384">интернетзонешовсекуритиварнингфорпотентиаллюнсафефилес</span><span class="sxs-lookup"><span data-stu-id="f768e-384">InternetZoneShowSecurityWarningForPotentiallyUnsafeFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneshowsecuritywarningforpotentiallyunsafefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-385">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-385">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-386">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-386">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-387">интернетзонеусепопупблоккер</span><span class="sxs-lookup"><span data-stu-id="f768e-387">InternetZoneUsePopupBlocker</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneusepopupblocker)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-388">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-388">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-389">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-389">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f768e-390">интернетзоневебситесинлесспривилежедзонесканнавигатеинтосисзоне</span><span class="sxs-lookup"><span data-stu-id="f768e-390">InternetZoneWebsitesInLessPrivilegedZonesCanNavigateIntoThisZone</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-391">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-391">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-392">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-392">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-393">интранетзонеалловакцесстодатасаурцес</span><span class="sxs-lookup"><span data-stu-id="f768e-393">IntranetZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-394">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-394">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-395">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-395">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-396">интранетзонеалловаутоматикпромптингфорактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="f768e-396">IntranetZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-397">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-397">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-398">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-398">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-399">интранетзонеалловаутоматикпромптингфорфиледовнлоадс</span><span class="sxs-lookup"><span data-stu-id="f768e-399">IntranetZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-400">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-400">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-401">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-401">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-402">интранетзонеалловфонтдовнлоадс</span><span class="sxs-lookup"><span data-stu-id="f768e-402">IntranetZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-403">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-403">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-404">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-404">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-405">интранетзонеалловлесспривилежедситес</span><span class="sxs-lookup"><span data-stu-id="f768e-405">IntranetZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-406">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-406">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-407">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-407">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-408">интранетзонеалловнетфрамеворкрелианткомпонентс</span><span class="sxs-lookup"><span data-stu-id="f768e-408">IntranetZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-409">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-409">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-410">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-410">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-411">интранетзонеалловскриптлетс</span><span class="sxs-lookup"><span data-stu-id="f768e-411">IntranetZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-412">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-412">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-413">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-413">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-414">интранетзонеалловсмартскриние</span><span class="sxs-lookup"><span data-stu-id="f768e-414">IntranetZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-415">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-415">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-416">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-416">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-417">интранетзонеалловусердатаперсистенце</span><span class="sxs-lookup"><span data-stu-id="f768e-417">IntranetZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-418">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-418">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-419">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-419">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-420">интранетзонедонотрунантималвареагаинстактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="f768e-420">IntranetZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-421">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-421">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-422">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-422">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-423">интранетзонеинитиализеандскриптактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="f768e-423">IntranetZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-424">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-424">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-425">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-425">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f768e-426">интранетзонеинитиализеандскриптактивексконтролснотмаркедсафе</span><span class="sxs-lookup"><span data-stu-id="f768e-426">IntranetZoneInitializeAndScriptActiveXControlsNotMarkedSafe</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-427">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-427">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-428">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-428">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-429">интранетзонежавапермиссионс</span><span class="sxs-lookup"><span data-stu-id="f768e-429">IntranetZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-430">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-430">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-431">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-431">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-432">интранетзоненавигатевиндовсандфрамес</span><span class="sxs-lookup"><span data-stu-id="f768e-432">IntranetZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-433">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-433">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-434">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-434">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-435">локалмачинезонеалловакцесстодатасаурцес</span><span class="sxs-lookup"><span data-stu-id="f768e-435">LocalMachineZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-436">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-436">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-437">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-437">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-438">локалмачинезонеалловаутоматикпромптингфорактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="f768e-438">LocalMachineZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-439">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-439">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-440">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-440">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-441">локалмачинезонеалловаутоматикпромптингфорфиледовнлоадс</span><span class="sxs-lookup"><span data-stu-id="f768e-441">LocalMachineZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-442">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-442">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-443">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-443">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-444">локалмачинезонеалловфонтдовнлоадс</span><span class="sxs-lookup"><span data-stu-id="f768e-444">LocalMachineZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-445">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-445">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-446">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-446">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-447">локалмачинезонеалловлесспривилежедситес</span><span class="sxs-lookup"><span data-stu-id="f768e-447">LocalMachineZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-448">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-448">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-449">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-449">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-450">локалмачинезонеалловнетфрамеворкрелианткомпонентс</span><span class="sxs-lookup"><span data-stu-id="f768e-450">LocalMachineZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-451">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-451">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-452">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-452">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-453">локалмачинезонеалловскриптлетс</span><span class="sxs-lookup"><span data-stu-id="f768e-453">LocalMachineZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-454">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-454">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-455">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-455">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-456">локалмачинезонеалловсмартскриние</span><span class="sxs-lookup"><span data-stu-id="f768e-456">LocalMachineZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-457">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-457">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-458">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-458">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-459">локалмачинезонеалловусердатаперсистенце</span><span class="sxs-lookup"><span data-stu-id="f768e-459">LocalMachineZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-460">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-460">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-461">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-461">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-462">локалмачинезонедонотрунантималвареагаинстактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="f768e-462">LocalMachineZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-463">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-463">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-464">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-464">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-465">локалмачинезонеинитиализеандскриптактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="f768e-465">LocalMachineZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-466">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-466">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-467">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-467">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-468">локалмачинезонежавапермиссионс</span><span class="sxs-lookup"><span data-stu-id="f768e-468">LocalMachineZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-469">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-469">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-470">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-470">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-471">локалмачинезоненавигатевиндовсандфрамес</span><span class="sxs-lookup"><span data-stu-id="f768e-471">LocalMachineZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-472">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-472">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-473">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-473">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-474">локкеддовнинтернетзонеалловакцесстодатасаурцес</span><span class="sxs-lookup"><span data-stu-id="f768e-474">LockedDownInternetZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-475">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-475">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-476">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-476">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-477">локкеддовнинтернетзонеалловаутоматикпромптингфорактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="f768e-477">LockedDownInternetZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-478">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-478">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-479">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-479">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-480">локкеддовнинтернетзонеалловаутоматикпромптингфорфиледовнлоадс</span><span class="sxs-lookup"><span data-stu-id="f768e-480">LockedDownInternetZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-481">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-481">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-482">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-482">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-483">локкеддовнинтернетзонеалловфонтдовнлоадс</span><span class="sxs-lookup"><span data-stu-id="f768e-483">LockedDownInternetZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-484">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-484">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-485">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-485">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-486">локкеддовнинтернетзонеалловлесспривилежедситес</span><span class="sxs-lookup"><span data-stu-id="f768e-486">LockedDownInternetZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-487">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-487">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-488">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-488">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-489">локкеддовнинтернетзонеалловнетфрамеворкрелианткомпонентс</span><span class="sxs-lookup"><span data-stu-id="f768e-489">LockedDownInternetZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-490">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-490">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-491">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-491">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-492">локкеддовнинтернетзонеалловскриптлетс</span><span class="sxs-lookup"><span data-stu-id="f768e-492">LockedDownInternetZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-493">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-493">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-494">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-494">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-495">локкеддовнинтернетзонеалловсмартскриние</span><span class="sxs-lookup"><span data-stu-id="f768e-495">LockedDownInternetZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-496">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-496">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-497">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-497">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-498">локкеддовнинтернетзонеалловусердатаперсистенце</span><span class="sxs-lookup"><span data-stu-id="f768e-498">LockedDownInternetZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-499">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-499">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-500">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-500">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-501">локкеддовнинтернетзонеинитиализеандскриптактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="f768e-501">LockedDownInternetZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-502">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-502">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-503">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-503">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-504">локкеддовнинтернетзонежавапермиссионс</span><span class="sxs-lookup"><span data-stu-id="f768e-504">LockedDownInternetZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-505">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-505">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-506">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-506">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-507">локкеддовнинтернетзоненавигатевиндовсандфрамес</span><span class="sxs-lookup"><span data-stu-id="f768e-507">LockedDownInternetZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-508">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-508">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-509">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-509">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-510">локкеддовнинтранетзонеалловакцесстодатасаурцес</span><span class="sxs-lookup"><span data-stu-id="f768e-510">LockedDownIntranetZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-511">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-511">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-512">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-512">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-513">локкеддовнинтранетзонеалловаутоматикпромптингфорактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="f768e-513">LockedDownIntranetZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-514">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-514">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-515">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-515">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-516">локкеддовнинтранетзонеалловаутоматикпромптингфорфиледовнлоадс</span><span class="sxs-lookup"><span data-stu-id="f768e-516">LockedDownIntranetZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-517">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-517">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-518">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-518">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-519">локкеддовнинтранетзонеалловфонтдовнлоадс</span><span class="sxs-lookup"><span data-stu-id="f768e-519">LockedDownIntranetZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-520">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-520">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-521">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-521">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-522">локкеддовнинтранетзонеалловлесспривилежедситес</span><span class="sxs-lookup"><span data-stu-id="f768e-522">LockedDownIntranetZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-523">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-523">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-524">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-524">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-525">локкеддовнинтранетзонеалловнетфрамеворкрелианткомпонентс</span><span class="sxs-lookup"><span data-stu-id="f768e-525">LockedDownIntranetZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-526">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-526">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-527">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-527">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-528">локкеддовнинтранетзонеалловскриптлетс</span><span class="sxs-lookup"><span data-stu-id="f768e-528">LockedDownIntranetZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-529">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-529">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-530">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-530">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-531">локкеддовнинтранетзонеалловсмартскриние</span><span class="sxs-lookup"><span data-stu-id="f768e-531">LockedDownIntranetZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-532">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-532">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-533">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-533">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-534">локкеддовнинтранетзонеалловусердатаперсистенце</span><span class="sxs-lookup"><span data-stu-id="f768e-534">LockedDownIntranetZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-535">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-535">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-536">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-536">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-537">локкеддовнинтранетзонеинитиализеандскриптактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="f768e-537">LockedDownIntranetZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-538">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-538">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-539">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-539">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-540">локкеддовнинтранетзоненавигатевиндовсандфрамес</span><span class="sxs-lookup"><span data-stu-id="f768e-540">LockedDownIntranetZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-541">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-541">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-542">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-542">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-543">локкеддовнлокалмачинезонеалловакцесстодатасаурцес</span><span class="sxs-lookup"><span data-stu-id="f768e-543">LockedDownLocalMachineZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-544">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-544">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-545">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-545">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-546">локкеддовнлокалмачинезонеалловаутоматикпромптингфорактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="f768e-546">LockedDownLocalMachineZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-547">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-547">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-548">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-548">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-549">локкеддовнлокалмачинезонеалловаутоматикпромптингфорфиледовнлоадс</span><span class="sxs-lookup"><span data-stu-id="f768e-549">LockedDownLocalMachineZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-550">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-550">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-551">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-551">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-552">локкеддовнлокалмачинезонеалловфонтдовнлоадс</span><span class="sxs-lookup"><span data-stu-id="f768e-552">LockedDownLocalMachineZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-553">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-553">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-554">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-554">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-555">локкеддовнлокалмачинезонеалловлесспривилежедситес</span><span class="sxs-lookup"><span data-stu-id="f768e-555">LockedDownLocalMachineZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-556">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-556">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-557">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-557">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-558">локкеддовнлокалмачинезонеалловнетфрамеворкрелианткомпонентс</span><span class="sxs-lookup"><span data-stu-id="f768e-558">LockedDownLocalMachineZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-559">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-559">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-560">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-560">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-561">локкеддовнлокалмачинезонеалловскриптлетс</span><span class="sxs-lookup"><span data-stu-id="f768e-561">LockedDownLocalMachineZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-562">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-562">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-563">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-563">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-564">локкеддовнлокалмачинезонеалловсмартскриние</span><span class="sxs-lookup"><span data-stu-id="f768e-564">LockedDownLocalMachineZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-565">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-565">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-566">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-566">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-567">локкеддовнлокалмачинезонеалловусердатаперсистенце</span><span class="sxs-lookup"><span data-stu-id="f768e-567">LockedDownLocalMachineZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-568">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-568">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-569">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-569">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-570">локкеддовнлокалмачинезонеинитиализеандскриптактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="f768e-570">LockedDownLocalMachineZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-571">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-571">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-572">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-572">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-573">локкеддовнлокалмачинезонежавапермиссионс</span><span class="sxs-lookup"><span data-stu-id="f768e-573">LockedDownLocalMachineZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-574">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-574">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-575">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-575">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-576">локкеддовнлокалмачинезоненавигатевиндовсандфрамес</span><span class="sxs-lookup"><span data-stu-id="f768e-576">LockedDownLocalMachineZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-577">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-577">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-578">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-578">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-579">локкеддовнрестриктедситесзонеалловакцесстодатасаурцес</span><span class="sxs-lookup"><span data-stu-id="f768e-579">LockedDownRestrictedSitesZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-580">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-580">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-581">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-581">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-582">локкеддовнрестриктедситесзонеалловаутоматикпромптингфорактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="f768e-582">LockedDownRestrictedSitesZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-583">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-583">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-584">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-584">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-585">локкеддовнрестриктедситесзонеалловаутоматикпромптингфорфиледовнлоадс</span><span class="sxs-lookup"><span data-stu-id="f768e-585">LockedDownRestrictedSitesZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-586">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-586">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-587">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-587">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-588">локкеддовнрестриктедситесзонеалловфонтдовнлоадс</span><span class="sxs-lookup"><span data-stu-id="f768e-588">LockedDownRestrictedSitesZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-589">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-589">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-590">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-590">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-591">локкеддовнрестриктедситесзонеалловлесспривилежедситес</span><span class="sxs-lookup"><span data-stu-id="f768e-591">LockedDownRestrictedSitesZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-592">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-592">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-593">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-593">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-594">локкеддовнрестриктедситесзонеалловнетфрамеворкрелианткомпонентс</span><span class="sxs-lookup"><span data-stu-id="f768e-594">LockedDownRestrictedSitesZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-595">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-595">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-596">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-596">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-597">локкеддовнрестриктедситесзонеалловскриптлетс</span><span class="sxs-lookup"><span data-stu-id="f768e-597">LockedDownRestrictedSitesZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-598">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-598">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-599">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-599">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-600">локкеддовнрестриктедситесзонеалловсмартскриние</span><span class="sxs-lookup"><span data-stu-id="f768e-600">LockedDownRestrictedSitesZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-601">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-601">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-602">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-602">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-603">локкеддовнрестриктедситесзонеалловусердатаперсистенце</span><span class="sxs-lookup"><span data-stu-id="f768e-603">LockedDownRestrictedSitesZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-604">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-604">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-605">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-605">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-606">локкеддовнрестриктедситесзонеинитиализеандскриптактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="f768e-606">LockedDownRestrictedSitesZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-607">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-607">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-608">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-608">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-609">локкеддовнрестриктедситесзонежавапермиссионс</span><span class="sxs-lookup"><span data-stu-id="f768e-609">LockedDownRestrictedSitesZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-610">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-610">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-611">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-611">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-612">локкеддовнрестриктедситесзоненавигатевиндовсандфрамес</span><span class="sxs-lookup"><span data-stu-id="f768e-612">LockedDownRestrictedSitesZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-613">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-613">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-614">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-614">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-615">локкеддовнтрустедситесзонеалловакцесстодатасаурцес</span><span class="sxs-lookup"><span data-stu-id="f768e-615">LockedDownTrustedSitesZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-616">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-616">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-617">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-617">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-618">локкеддовнтрустедситесзонеалловаутоматикпромптингфорактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="f768e-618">LockedDownTrustedSitesZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-619">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-619">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-620">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-620">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-621">локкеддовнтрустедситесзонеалловаутоматикпромптингфорфиледовнлоадс</span><span class="sxs-lookup"><span data-stu-id="f768e-621">LockedDownTrustedSitesZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-622">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-622">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-623">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-623">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-624">локкеддовнтрустедситесзонеалловфонтдовнлоадс</span><span class="sxs-lookup"><span data-stu-id="f768e-624">LockedDownTrustedSitesZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-625">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-625">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-626">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-626">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-627">локкеддовнтрустедситесзонеалловлесспривилежедситес</span><span class="sxs-lookup"><span data-stu-id="f768e-627">LockedDownTrustedSitesZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-628">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-628">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-629">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-629">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-630">локкеддовнтрустедситесзонеалловнетфрамеворкрелианткомпонентс</span><span class="sxs-lookup"><span data-stu-id="f768e-630">LockedDownTrustedSitesZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-631">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-631">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-632">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-632">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-633">локкеддовнтрустедситесзонеалловскриптлетс</span><span class="sxs-lookup"><span data-stu-id="f768e-633">LockedDownTrustedSitesZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-634">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-634">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-635">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-635">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-636">локкеддовнтрустедситесзонеалловсмартскриние</span><span class="sxs-lookup"><span data-stu-id="f768e-636">LockedDownTrustedSitesZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-637">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-637">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-638">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-638">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-639">локкеддовнтрустедситесзонеалловусердатаперсистенце</span><span class="sxs-lookup"><span data-stu-id="f768e-639">LockedDownTrustedSitesZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-640">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-640">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-641">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-641">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-642">локкеддовнтрустедситесзонеинитиализеандскриптактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="f768e-642">LockedDownTrustedSitesZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-643">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-643">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-644">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-644">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-645">локкеддовнтрустедситесзонежавапермиссионс</span><span class="sxs-lookup"><span data-stu-id="f768e-645">LockedDownTrustedSitesZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-646">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-646">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-647">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-647">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-648">локкеддовнтрустедситесзоненавигатевиндовсандфрамес</span><span class="sxs-lookup"><span data-stu-id="f768e-648">LockedDownTrustedSitesZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-649">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-649">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-650">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-650">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-651">мимесниффингсафетифеатуреинтернетексплорерпроцессес</span><span class="sxs-lookup"><span data-stu-id="f768e-651">MimeSniffingSafetyFeatureInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-mimesniffingsafetyfeatureinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-652">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-652">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-653">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-653">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-654">мкпротоколсекуритирестриктионинтернетексплорерпроцессес</span><span class="sxs-lookup"><span data-stu-id="f768e-654">MKProtocolSecurityRestrictionInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-mkprotocolsecurityrestrictioninternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-655">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-655">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-656">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-656">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-657">нотификатионбаринтернетексплорерпроцессес</span><span class="sxs-lookup"><span data-stu-id="f768e-657">NotificationBarInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-notificationbarinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-658">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-658">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-659">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-659">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f768e-660">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="f768e-660">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-661">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-661">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-662">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f768e-662">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f768e-663">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f768e-663">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-664">превентманагингсмартскринфилтер</span><span class="sxs-lookup"><span data-stu-id="f768e-664">PreventManagingSmartScreenFilter</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-preventmanagingsmartscreenfilter)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-665">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-665">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-666">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-666">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-667">превентперусеринсталлатионофактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="f768e-667">PreventPerUserInstallationOfActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-preventperuserinstallationofactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-668">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-668">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-669">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-669">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-670">протектионфромзонилеватионинтернетексплорерпроцессес</span><span class="sxs-lookup"><span data-stu-id="f768e-670">ProtectionFromZoneElevationInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-protectionfromzoneelevationinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-671">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-671">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-672">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-672">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-673">ремоверунсистимебуттонфораутдатедактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="f768e-673">RemoveRunThisTimeButtonForOutdatedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-removerunthistimebuttonforoutdatedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-674">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-674">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-675">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-675">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-676">рестриктактивексинсталлинтернетексплорерпроцессес</span><span class="sxs-lookup"><span data-stu-id="f768e-676">RestrictActiveXInstallInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictactivexinstallinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-677">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-677">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-678">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-678">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-679">рестриктедситесзонеалловакцесстодатасаурцес</span><span class="sxs-lookup"><span data-stu-id="f768e-679">RestrictedSitesZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-680">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-680">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-681">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-681">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-682">рестриктедситесзонеалловактивескриптинг</span><span class="sxs-lookup"><span data-stu-id="f768e-682">RestrictedSitesZoneAllowActiveScripting</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowactivescripting)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-683">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-683">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-684">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-684">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-685">рестриктедситесзонеалловаутоматикпромптингфорактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="f768e-685">RestrictedSitesZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-686">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-686">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-687">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-687">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-688">рестриктедситесзонеалловаутоматикпромптингфорфиледовнлоадс</span><span class="sxs-lookup"><span data-stu-id="f768e-688">RestrictedSitesZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-689">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-689">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-690">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-690">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-691">рестриктедситесзонеалловбинаряндскриптбехавиорс</span><span class="sxs-lookup"><span data-stu-id="f768e-691">RestrictedSitesZoneAllowBinaryAndScriptBehaviors</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowbinaryandscriptbehaviors)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-692">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-692">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-693">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-693">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-694">рестриктедситесзонеалловкопипастевиаскрипт</span><span class="sxs-lookup"><span data-stu-id="f768e-694">RestrictedSitesZoneAllowCopyPasteViaScript</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowcopypasteviascript)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-695">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-695">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-696">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-696">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-697">рестриктедситесзонеалловдраганддропкопяндпастефилес</span><span class="sxs-lookup"><span data-stu-id="f768e-697">RestrictedSitesZoneAllowDragAndDropCopyAndPasteFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowdraganddropcopyandpastefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-698">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-698">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-699">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-699">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-700">рестриктедситесзонеалловфиледовнлоадс</span><span class="sxs-lookup"><span data-stu-id="f768e-700">RestrictedSitesZoneAllowFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-701">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-701">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-702">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-702">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-703">рестриктедситесзонеалловфонтдовнлоадс</span><span class="sxs-lookup"><span data-stu-id="f768e-703">RestrictedSitesZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-704">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-704">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-705">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-705">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-706">рестриктедситесзонеалловлесспривилежедситес</span><span class="sxs-lookup"><span data-stu-id="f768e-706">RestrictedSitesZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-707">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-707">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-708">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-708">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-709">рестриктедситесзонеалловлоадингофксамлфилес</span><span class="sxs-lookup"><span data-stu-id="f768e-709">RestrictedSitesZoneAllowLoadingOfXAMLFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowloadingofxamlfiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-710">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-710">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-711">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-711">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-712">рестриктедситесзонеалловметарефреш</span><span class="sxs-lookup"><span data-stu-id="f768e-712">RestrictedSitesZoneAllowMETAREFRESH</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowmetarefresh)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-713">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-713">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-714">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-714">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-715">рестриктедситесзонеалловнетфрамеворкрелианткомпонентс</span><span class="sxs-lookup"><span data-stu-id="f768e-715">RestrictedSitesZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-716">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-716">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-717">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-717">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-718">рестриктедситесзонеалловонляппроведдомаинстаусеактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="f768e-718">RestrictedSitesZoneAllowOnlyApprovedDomainsToUseActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowonlyapproveddomainstouseactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-719">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-719">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-720">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-720">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-721">рестриктедситесзонеалловонляппроведдомаинстаусетдкактивексконтрол</span><span class="sxs-lookup"><span data-stu-id="f768e-721">RestrictedSitesZoneAllowOnlyApprovedDomainsToUseTDCActiveXControl</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowonlyapproveddomainstousetdcactivexcontrol)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-722">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-722">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-723">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-723">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-724">рестриктедситесзонеалловскриптингофинтернетексплорервеббровсерконтролс</span><span class="sxs-lookup"><span data-stu-id="f768e-724">RestrictedSitesZoneAllowScriptingOfInternetExplorerWebBrowserControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowscriptingofinternetexplorerwebbrowsercontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-725">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-725">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-726">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-726">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-727">рестриктедситесзонеалловскриптинитиатедвиндовс</span><span class="sxs-lookup"><span data-stu-id="f768e-727">RestrictedSitesZoneAllowScriptInitiatedWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowscriptinitiatedwindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-728">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-728">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-729">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-729">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-730">рестриктедситесзонеалловскриптлетс</span><span class="sxs-lookup"><span data-stu-id="f768e-730">RestrictedSitesZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-731">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-731">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-732">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-732">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-733">рестриктедситесзонеалловсмартскриние</span><span class="sxs-lookup"><span data-stu-id="f768e-733">RestrictedSitesZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-734">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-734">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-735">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-735">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-736">рестриктедситесзонеалловупдатестостатусбарвиаскрипт</span><span class="sxs-lookup"><span data-stu-id="f768e-736">RestrictedSitesZoneAllowUpdatesToStatusBarViaScript</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowupdatestostatusbarviascript)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-737">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-737">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-738">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-738">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-739">рестриктедситесзонеалловусердатаперсистенце</span><span class="sxs-lookup"><span data-stu-id="f768e-739">RestrictedSitesZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-740">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-740">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-741">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-741">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-742">рестриктедситесзонедонотрунантималвареагаинстактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="f768e-742">RestrictedSitesZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-743">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-743">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-744">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-744">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-745">рестриктедситесзонедовнлоадсигнедактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="f768e-745">RestrictedSitesZoneDownloadSignedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonedownloadsignedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-746">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-746">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-747">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-747">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-748">рестриктедситесзонедовнлоадунсигнедактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="f768e-748">RestrictedSitesZoneDownloadUnsignedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonedownloadunsignedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-749">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-749">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-750">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-750">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-751">рестриктедситесзонинаблекроссситескриптингфилтер</span><span class="sxs-lookup"><span data-stu-id="f768e-751">RestrictedSitesZoneEnableCrossSiteScriptingFilter</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneenablecrosssitescriptingfilter)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-752">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-752">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-753">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-753">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-754">рестриктедситесзонинабледраггингофконтентфромдифферентдомаинсакроссвиндовс</span><span class="sxs-lookup"><span data-stu-id="f768e-754">RestrictedSitesZoneEnableDraggingOfContentFromDifferentDomainsAcrossWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneenabledraggingofcontentfromdifferentdomainsacrosswindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-755">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-755">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-756">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-756">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-757">рестриктедситесзонинабледраггингофконтентфромдифферентдомаинсвисинвиндовс</span><span class="sxs-lookup"><span data-stu-id="f768e-757">RestrictedSitesZoneEnableDraggingOfContentFromDifferentDomainsWithinWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneenabledraggingofcontentfromdifferentdomainswithinwindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-758">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-758">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-759">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-759">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-760">рестриктедситесзонинаблемимесниффинг</span><span class="sxs-lookup"><span data-stu-id="f768e-760">RestrictedSitesZoneEnableMIMESniffing</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneenablemimesniffing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-761">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-761">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-762">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-762">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-763">рестриктедситесзонеинклуделокалпасвхенуплоадингфилестосервер</span><span class="sxs-lookup"><span data-stu-id="f768e-763">RestrictedSitesZoneIncludeLocalPathWhenUploadingFilesToServer</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneincludelocalpathwhenuploadingfilestoserver)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-764">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-764">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-765">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-765">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-766">рестриктедситесзонеинитиализеандскриптактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="f768e-766">RestrictedSitesZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-767">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-767">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-768">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-768">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-769">рестриктедситесзонежавапермиссионс</span><span class="sxs-lookup"><span data-stu-id="f768e-769">RestrictedSitesZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-770">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-770">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-771">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-771">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-772">рестриктедситесзонелаунчингаппликатионсандфилесинифраме</span><span class="sxs-lookup"><span data-stu-id="f768e-772">RestrictedSitesZoneLaunchingApplicationsAndFilesInIFRAME</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonelaunchingapplicationsandfilesiniframe)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-773">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-773">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-774">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-774">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-775">рестриктедситесзонелогоноптионс</span><span class="sxs-lookup"><span data-stu-id="f768e-775">RestrictedSitesZoneLogonOptions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonelogonoptions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-776">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-776">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-777">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-777">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-778">рестриктедситесзоненавигатевиндовсандфрамес</span><span class="sxs-lookup"><span data-stu-id="f768e-778">RestrictedSitesZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-779">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-779">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-780">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-780">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f768e-781">рестриктедситесзоненавигатевиндовсандфрамесакроссдомаинс</span><span class="sxs-lookup"><span data-stu-id="f768e-781">RestrictedSitesZoneNavigateWindowsAndFramesAcrossDomains</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-782">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-782">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-783">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-783">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-784">рестриктедситесзонерунактивексконтролсандплугинс</span><span class="sxs-lookup"><span data-stu-id="f768e-784">RestrictedSitesZoneRunActiveXControlsAndPlugins</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonerunactivexcontrolsandplugins)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-785">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-785">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-786">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-786">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-787">рестриктедситесзонеруннетфрамеворкрелианткомпонентссигнедвисаусентикоде</span><span class="sxs-lookup"><span data-stu-id="f768e-787">RestrictedSitesZoneRunNETFrameworkReliantComponentsSignedWithAuthenticode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonerunnetframeworkreliantcomponentssignedwithauthenticode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-788">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-788">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-789">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-789">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-790">рестриктедситесзонескриптактивексконтролсмаркедсафефорскриптинг</span><span class="sxs-lookup"><span data-stu-id="f768e-790">RestrictedSitesZoneScriptActiveXControlsMarkedSafeForScripting</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonescriptactivexcontrolsmarkedsafeforscripting)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-791">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-791">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-792">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-792">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-793">рестриктедситесзонескриптингофжаваапплетс</span><span class="sxs-lookup"><span data-stu-id="f768e-793">RestrictedSitesZoneScriptingOfJavaApplets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonescriptingofjavaapplets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-794">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-794">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-795">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-795">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-796">рестриктедситесзонешовсекуритиварнингфорпотентиаллюнсафефилес</span><span class="sxs-lookup"><span data-stu-id="f768e-796">RestrictedSitesZoneShowSecurityWarningForPotentiallyUnsafeFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneshowsecuritywarningforpotentiallyunsafefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-797">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-797">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-798">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-798">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f768e-799">рестриктедситесзонетурнонкроссситескриптингфилтер</span><span class="sxs-lookup"><span data-stu-id="f768e-799">RestrictedSitesZoneTurnOnCrossSiteScriptingFilter</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-800">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-800">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-801">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-801">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-802">рестриктедситесзонетурнонпротектедмоде</span><span class="sxs-lookup"><span data-stu-id="f768e-802">RestrictedSitesZoneTurnOnProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneturnonprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-803">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-803">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-804">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-804">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-805">рестриктедситесзонеусепопупблоккер</span><span class="sxs-lookup"><span data-stu-id="f768e-805">RestrictedSitesZoneUsePopupBlocker</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneusepopupblocker)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-806">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-806">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-807">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-807">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-808">рестриктфиледовнлоадинтернетексплорерпроцессес</span><span class="sxs-lookup"><span data-stu-id="f768e-808">RestrictFileDownloadInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictfiledownloadinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-809">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-809">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-810">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-810">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-811">скриптедвиндовсекуритирестриктионсинтернетексплорерпроцессес</span><span class="sxs-lookup"><span data-stu-id="f768e-811">ScriptedWindowSecurityRestrictionsInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-scriptedwindowsecurityrestrictionsinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-812">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-812">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-813">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-813">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-814">SearchProviderList</span><span class="sxs-lookup"><span data-stu-id="f768e-814">SearchProviderList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-searchproviderlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-815">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-815">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-816">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-816">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-817">секуритизонесусеонлимачинесеттингс</span><span class="sxs-lookup"><span data-stu-id="f768e-817">SecurityZonesUseOnlyMachineSettings</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-securityzonesuseonlymachinesettings)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-818">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-818">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-819">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-819">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-820">спеЦифюсеофактивексинсталлерсервице</span><span class="sxs-lookup"><span data-stu-id="f768e-820">SpecifyUseOfActiveXInstallerService</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-specifyuseofactivexinstallerservice)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-821">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-821">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-822">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-822">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-823">трустедситесзонеалловакцесстодатасаурцес</span><span class="sxs-lookup"><span data-stu-id="f768e-823">TrustedSitesZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-824">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-824">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-825">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-825">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-826">трустедситесзонеалловаутоматикпромптингфорактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="f768e-826">TrustedSitesZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-827">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-827">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-828">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-828">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-829">трустедситесзонеалловаутоматикпромптингфорфиледовнлоадс</span><span class="sxs-lookup"><span data-stu-id="f768e-829">TrustedSitesZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-830">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-830">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-831">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-831">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-832">трустедситесзонеалловфонтдовнлоадс</span><span class="sxs-lookup"><span data-stu-id="f768e-832">TrustedSitesZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-833">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-833">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-834">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-834">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-835">трустедситесзонеалловлесспривилежедситес</span><span class="sxs-lookup"><span data-stu-id="f768e-835">TrustedSitesZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-836">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-836">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-837">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-837">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-838">трустедситесзонеалловнетфрамеворкрелианткомпонентс</span><span class="sxs-lookup"><span data-stu-id="f768e-838">TrustedSitesZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-839">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-839">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-840">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-840">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-841">трустедситесзонеалловскриптлетс</span><span class="sxs-lookup"><span data-stu-id="f768e-841">TrustedSitesZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-842">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-842">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-843">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-843">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-844">трустедситесзонеалловсмартскриние</span><span class="sxs-lookup"><span data-stu-id="f768e-844">TrustedSitesZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-845">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-845">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-846">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-846">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-847">трустедситесзонеалловусердатаперсистенце</span><span class="sxs-lookup"><span data-stu-id="f768e-847">TrustedSitesZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-848">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-848">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-849">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-849">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-850">трустедситесзонедонотрунантималвареагаинстактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="f768e-850">TrustedSitesZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-851">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-851">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-852">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-852">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f768e-853">трустедситесзонедонтрунантималварепрограмсагаинстактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="f768e-853">TrustedSitesZoneDontRunAntimalwareProgramsAgainstActiveXControls</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-854">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-854">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-855">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-855">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-856">трустедситесзонеинитиализеандскриптактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="f768e-856">TrustedSitesZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-857">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-857">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-858">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-858">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f768e-859">трустедситесзонеинитиализеандскриптактивексконтролснотмаркедассафе</span><span class="sxs-lookup"><span data-stu-id="f768e-859">TrustedSitesZoneInitializeAndScriptActiveXControlsNotMarkedAsSafe</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-860">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-860">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-861">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-861">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f768e-862">трустедситесзонеинитиализеандскриптактивексконтролснотмаркедсафе</span><span class="sxs-lookup"><span data-stu-id="f768e-862">TrustedSitesZoneInitializeAndScriptActiveXControlsNotMarkedSafe</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-863">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-863">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-864">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-864">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-865">трустедситесзонежавапермиссионс</span><span class="sxs-lookup"><span data-stu-id="f768e-865">TrustedSitesZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-866">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-866">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-867">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-867">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f768e-868">трустедситесзоненавигатевиндовсандфрамес</span><span class="sxs-lookup"><span data-stu-id="f768e-868">TrustedSitesZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f768e-869">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f768e-869">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f768e-870">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f768e-870">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f768e-871">Требования</span><span class="sxs-lookup"><span data-stu-id="f768e-871">Requirements</span></span>



| <span data-ttu-id="f768e-872">Требование</span><span class="sxs-lookup"><span data-stu-id="f768e-872">Requirement</span></span> | <span data-ttu-id="f768e-873">Значение</span><span class="sxs-lookup"><span data-stu-id="f768e-873">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f768e-874">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f768e-874">Minimum supported client</span></span><br/> | <span data-ttu-id="f768e-875">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="f768e-875">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f768e-876">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f768e-876">Minimum supported server</span></span><br/> | <span data-ttu-id="f768e-877">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="f768e-877">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="f768e-878">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f768e-878">Namespace</span></span><br/>                | <span data-ttu-id="f768e-879">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="f768e-879">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="f768e-880">MOF</span><span class="sxs-lookup"><span data-stu-id="f768e-880">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f768e-881"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f768e-881"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="f768e-882">DLL</span><span class="sxs-lookup"><span data-stu-id="f768e-882">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f768e-883"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f768e-883"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

