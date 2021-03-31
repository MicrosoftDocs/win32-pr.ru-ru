---
title: Класс MDM_Policy_User_Config01_InternetExplorer02
description: '\_ \_ \_ Класс User CONFIG01 InternetExplorer02 политики MDM \_ представляет доступные политики Internet Explorer.'
ms.assetid: 2b155e65-5a81-4916-815f-23763759bb9a
keywords:
- Класс MDM_Policy_User_Config01_InternetExplorer02
- MDM_Policy_User_Config01_InternetExplorer02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Policy_User_Config01_InternetExplorer02
- MDM_Policy_User_Config01_InternetExplorer02.InstanceID
- MDM_Policy_User_Config01_InternetExplorer02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2f79c00505037508307e93120f9e2545b135678
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071672"
---
# <a name="mdm_policy_user_config01_internetexplorer02-class"></a><span data-ttu-id="07939-105">\_Класс политики MDM \_ user \_ Config01 \_ InternetExplorer02</span><span class="sxs-lookup"><span data-stu-id="07939-105">MDM\_Policy\_User\_Config01\_InternetExplorer02 class</span></span>

<span data-ttu-id="07939-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="07939-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="07939-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="07939-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="07939-108">\_ \_ \_ Класс User CONFIG01 InternetExplorer02 политики MDM \_ представляет доступные политики Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="07939-108">The MDM\_Policy\_User\_Config01\_InternetExplorer02 class represents the available Internet Explorer policies.</span></span>

<span data-ttu-id="07939-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="07939-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="07939-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="07939-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Config01_InternetExplorer02
{
  string InstanceID;
  string ParentID;
  string AddSearchProvider;
  string AllowActiveXFiltering;
  string AllowAddOnList;
  string AllowDeletingBrowsingHistoryOnExit;
  string AllowCertificateAddressMismatchWarning;
  string AllowAutoComplete;
  string AllowEnhancedProtectedMode;
  string AllowEnterpriseModeFromToolsMenu;
  string AllowEnterpriseModeSiteList;
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
  string DisableHomePageChange;
  string DisableProcessesInEnhancedProtectedMode;
  string DisableInPrivateBrowsing;
  string DisableIgnoringCertificateErrors;
  string DisableProxyChange;
  string DisableSearchProviderChange;
  string DisableSecondaryHomePageChange;
  string DoNotAllowActiveXControlsInProtectedMode;
  string DisableSecuritySettingsCheck;
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

## <a name="members"></a><span data-ttu-id="07939-111">Члены</span><span class="sxs-lookup"><span data-stu-id="07939-111">Members</span></span>

<span data-ttu-id="07939-112">Класс **\_ \_ user \_ Config01 \_ InternetExplorer02 политики MDM** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="07939-112">The **MDM\_Policy\_User\_Config01\_InternetExplorer02** class has these types of members:</span></span>

-   [<span data-ttu-id="07939-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="07939-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="07939-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="07939-114">Properties</span></span>

<span data-ttu-id="07939-115">Класс **\_ \_ user \_ Config01 \_ InternetExplorer02 политики MDM** имеет эти свойства.</span><span class="sxs-lookup"><span data-stu-id="07939-115">The **MDM\_Policy\_User\_Config01\_InternetExplorer02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="07939-116">AddSearchProvider</span><span class="sxs-lookup"><span data-stu-id="07939-116">AddSearchProvider</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-addsearchprovider)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-117">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-119">алловактивексфилтеринг</span><span class="sxs-lookup"><span data-stu-id="07939-119">AllowActiveXFiltering</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowactivexfiltering)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-121">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-122">алловаддонлист</span><span class="sxs-lookup"><span data-stu-id="07939-122">AllowAddOnList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowaddonlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-123">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-124">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-125">алловаутокомплете</span><span class="sxs-lookup"><span data-stu-id="07939-125">AllowAutoComplete</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowautocomplete)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-126">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-127">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-128">алловцертификатеаддрессмисматчварнинг</span><span class="sxs-lookup"><span data-stu-id="07939-128">AllowCertificateAddressMismatchWarning</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowcertificateaddressmismatchwarning)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-129">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-130">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-131">алловделетингбровсингхисторйонексит</span><span class="sxs-lookup"><span data-stu-id="07939-131">AllowDeletingBrowsingHistoryOnExit</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowdeletingbrowsinghistoryonexit)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-132">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-133">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-134">алловенханцедпротектедмоде</span><span class="sxs-lookup"><span data-stu-id="07939-134">AllowEnhancedProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowenhancedprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-135">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-136">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-137">алловентерприсемодефромтулсмену</span><span class="sxs-lookup"><span data-stu-id="07939-137">AllowEnterpriseModeFromToolsMenu</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowenterprisemodefromtoolsmenu)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-138">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-139">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-140">алловентерприсемодесителист</span><span class="sxs-lookup"><span data-stu-id="07939-140">AllowEnterpriseModeSiteList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowenterprisemodesitelist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-141">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-142">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-143">AllowInternetExplorer7PolicyList</span><span class="sxs-lookup"><span data-stu-id="07939-143">AllowInternetExplorer7PolicyList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowinternetexplorer7policylist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-144">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-145">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-146">алловинтернетексплорерстандардсмоде</span><span class="sxs-lookup"><span data-stu-id="07939-146">AllowInternetExplorerStandardsMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowinternetexplorerstandardsmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-147">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-148">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-149">алловинтернетзонетемплате</span><span class="sxs-lookup"><span data-stu-id="07939-149">AllowInternetZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowinternetzonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-150">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-151">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-152">алловинтранетзонетемплате</span><span class="sxs-lookup"><span data-stu-id="07939-152">AllowIntranetZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowintranetzonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-153">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-154">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-155">алловлокалмачинезонетемплате</span><span class="sxs-lookup"><span data-stu-id="07939-155">AllowLocalMachineZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlocalmachinezonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-156">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-157">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-158">алловлоккеддовнинтернетзонетемплате</span><span class="sxs-lookup"><span data-stu-id="07939-158">AllowLockedDownInternetZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlockeddowninternetzonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-159">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-160">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-161">алловлоккеддовнинтранетзонетемплате</span><span class="sxs-lookup"><span data-stu-id="07939-161">AllowLockedDownIntranetZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlockeddownintranetzonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-162">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-163">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-164">алловлоккеддовнлокалмачинезонетемплате</span><span class="sxs-lookup"><span data-stu-id="07939-164">AllowLockedDownLocalMachineZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlockeddownlocalmachinezonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-165">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-166">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-166">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-167">алловлоккеддовнрестриктедситесзонетемплате</span><span class="sxs-lookup"><span data-stu-id="07939-167">AllowLockedDownRestrictedSitesZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlockeddownrestrictedsiteszonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-168">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-169">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-169">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-170">алловоневордентри</span><span class="sxs-lookup"><span data-stu-id="07939-170">AllowOneWordEntry</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowonewordentry)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-171">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-172">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-172">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-173">алловситетозонеассигнментлист</span><span class="sxs-lookup"><span data-stu-id="07939-173">AllowSiteToZoneAssignmentList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowsitetozoneassignmentlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-174">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-175">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-175">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-176">алловслоккеддовнтрустедситесзонетемплате</span><span class="sxs-lookup"><span data-stu-id="07939-176">AllowsLockedDownTrustedSitesZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowslockeddowntrustedsiteszonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-177">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-178">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-178">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-179">алловсофтваревхенсигнатуреисинвалид</span><span class="sxs-lookup"><span data-stu-id="07939-179">AllowSoftwareWhenSignatureIsInvalid</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowsoftwarewhensignatureisinvalid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-180">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-181">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-181">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-182">алловсрестриктедситесзонетемплате</span><span class="sxs-lookup"><span data-stu-id="07939-182">AllowsRestrictedSitesZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowsrestrictedsiteszonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-183">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-184">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-184">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-185">алловсугжестедситес</span><span class="sxs-lookup"><span data-stu-id="07939-185">AllowSuggestedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowsuggestedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-186">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-187">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-187">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-188">алловтрустедситесзонетемплате</span><span class="sxs-lookup"><span data-stu-id="07939-188">AllowTrustedSitesZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowtrustedsiteszonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-189">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-190">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-190">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-191">чекксерверцертификатеревокатион</span><span class="sxs-lookup"><span data-stu-id="07939-191">CheckServerCertificateRevocation</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-checkservercertificaterevocation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-192">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-193">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-193">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-194">чекксигнатуресондовнлоадедпрограмс</span><span class="sxs-lookup"><span data-stu-id="07939-194">CheckSignaturesOnDownloadedPrograms</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-checksignaturesondownloadedprograms)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-195">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-196">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-196">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-197">консистентмимехандлингинтернетексплорерпроцессес</span><span class="sxs-lookup"><span data-stu-id="07939-197">ConsistentMimeHandlingInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-consistentmimehandlinginternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-198">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-199">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-199">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-200">дисаблеадобефлаш</span><span class="sxs-lookup"><span data-stu-id="07939-200">DisableAdobeFlash</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableadobeflash)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-201">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-202">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-202">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="07939-203">дисаблеблоккингофаутдатедактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="07939-203">DisableBlockingOfOutdatedActiveXControls</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-204">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-204">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-205">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-205">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-206">дисаблебипассофсмартскринварнингс</span><span class="sxs-lookup"><span data-stu-id="07939-206">DisableBypassOfSmartScreenWarnings</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablebypassofsmartscreenwarnings)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-207">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-208">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-208">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-209">дисаблебипассофсмартскринварнингсабаутункоммонфилес</span><span class="sxs-lookup"><span data-stu-id="07939-209">DisableBypassOfSmartScreenWarningsAboutUncommonFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablebypassofsmartscreenwarningsaboutuncommonfiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-210">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-211">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-211">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-212">дисаблеконфигурингхистори</span><span class="sxs-lookup"><span data-stu-id="07939-212">DisableConfiguringHistory</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableconfiguringhistory)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-213">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-214">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-214">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-215">дисаблекрашдетектион</span><span class="sxs-lookup"><span data-stu-id="07939-215">DisableCrashDetection</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablecrashdetection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-216">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-216">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-217">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-217">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-218">дисаблекустомерекспериенцеимпровементпрогрампартиЦипатион</span><span class="sxs-lookup"><span data-stu-id="07939-218">DisableCustomerExperienceImprovementProgramParticipation</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablecustomerexperienceimprovementprogramparticipation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-219">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-220">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-220">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-221">дисабледелетингусервиситедвебситес</span><span class="sxs-lookup"><span data-stu-id="07939-221">DisableDeletingUserVisitedWebsites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disabledeletinguservisitedwebsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-222">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-223">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-223">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-224">дисаблинклосуредовнлоадинг</span><span class="sxs-lookup"><span data-stu-id="07939-224">DisableEnclosureDownloading</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableenclosuredownloading)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-225">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-226">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-226">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-227">дисаблинкриптионсуппорт</span><span class="sxs-lookup"><span data-stu-id="07939-227">DisableEncryptionSupport</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableencryptionsupport)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-228">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-228">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-229">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-229">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-230">дисаблефирструнвизард</span><span class="sxs-lookup"><span data-stu-id="07939-230">DisableFirstRunWizard</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablefirstrunwizard)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-231">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-231">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-232">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-232">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-233">дисаблефлипахеадфеатуре</span><span class="sxs-lookup"><span data-stu-id="07939-233">DisableFlipAheadFeature</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableflipaheadfeature)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-234">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-234">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-235">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-235">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-236">дисаблехомепажечанже</span><span class="sxs-lookup"><span data-stu-id="07939-236">DisableHomePageChange</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablehomepagechange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-237">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-237">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-238">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-238">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-239">дисаблеигнорингцертификатиррорс</span><span class="sxs-lookup"><span data-stu-id="07939-239">DisableIgnoringCertificateErrors</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableignoringcertificateerrors)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-240">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-240">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-241">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-241">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-242">дисаблеинприватебровсинг</span><span class="sxs-lookup"><span data-stu-id="07939-242">DisableInPrivateBrowsing</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableinprivatebrowsing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-243">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-243">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-244">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-244">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-245">дисаблепроцессесиненханцедпротектедмоде</span><span class="sxs-lookup"><span data-stu-id="07939-245">DisableProcessesInEnhancedProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableprocessesinenhancedprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-246">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-246">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-247">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-247">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-248">дисаблепроксичанже</span><span class="sxs-lookup"><span data-stu-id="07939-248">DisableProxyChange</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableproxychange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-249">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-250">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-250">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-251">дисаблесеарчпровидерчанже</span><span class="sxs-lookup"><span data-stu-id="07939-251">DisableSearchProviderChange</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablesearchproviderchange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-252">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-253">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-253">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-254">дисаблесекондарихомепажечанже</span><span class="sxs-lookup"><span data-stu-id="07939-254">DisableSecondaryHomePageChange</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablesecondaryhomepagechange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-255">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-255">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-256">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-256">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-257">дисаблесекуритисеттингсчекк</span><span class="sxs-lookup"><span data-stu-id="07939-257">DisableSecuritySettingsCheck</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablesecuritysettingscheck)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-258">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-259">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-259">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-260">доноталловактивексконтролсинпротектедмоде</span><span class="sxs-lookup"><span data-stu-id="07939-260">DoNotAllowActiveXControlsInProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-donotallowactivexcontrolsinprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-261">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-262">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-262">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-263">донотблоккаутдатедактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="07939-263">DoNotBlockOutdatedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-donotblockoutdatedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-264">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-265">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-265">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-266">донотблоккаутдатедактивексконтролсонспеЦификдомаинс</span><span class="sxs-lookup"><span data-stu-id="07939-266">DoNotBlockOutdatedActiveXControlsOnSpecificDomains</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-donotblockoutdatedactivexcontrolsonspecificdomains)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-267">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-267">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-268">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-268">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-269">инклудеалллокалситес</span><span class="sxs-lookup"><span data-stu-id="07939-269">IncludeAllLocalSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-includealllocalsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-270">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-270">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-271">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-271">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-272">инклудеаллнетворкпасс</span><span class="sxs-lookup"><span data-stu-id="07939-272">IncludeAllNetworkPaths</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-includeallnetworkpaths)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-273">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-273">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-274">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-274">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="07939-275">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="07939-275">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-276">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-276">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-277">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="07939-277">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="07939-278">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="07939-278">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-279">интернетзонеалловакцесстодатасаурцес</span><span class="sxs-lookup"><span data-stu-id="07939-279">InternetZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-280">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-280">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-281">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-281">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-282">интернетзонеалловаутоматикпромптингфорактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="07939-282">InternetZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-283">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-283">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-284">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-284">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-285">интернетзонеалловаутоматикпромптингфорфиледовнлоадс</span><span class="sxs-lookup"><span data-stu-id="07939-285">InternetZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-286">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-286">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-287">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-287">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-288">интернетзонеалловкопипастевиаскрипт</span><span class="sxs-lookup"><span data-stu-id="07939-288">InternetZoneAllowCopyPasteViaScript</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowcopypasteviascript)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-289">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-289">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-290">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-290">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-291">интернетзонеалловдраганддропкопяндпастефилес</span><span class="sxs-lookup"><span data-stu-id="07939-291">InternetZoneAllowDragAndDropCopyAndPasteFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowdraganddropcopyandpastefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-292">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-292">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-293">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-293">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-294">интернетзонеалловфонтдовнлоадс</span><span class="sxs-lookup"><span data-stu-id="07939-294">InternetZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-295">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-295">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-296">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-296">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-297">интернетзонеалловлесспривилежедситес</span><span class="sxs-lookup"><span data-stu-id="07939-297">InternetZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-298">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-298">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-299">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-299">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-300">интернетзонеалловлоадингофксамлфилес</span><span class="sxs-lookup"><span data-stu-id="07939-300">InternetZoneAllowLoadingOfXAMLFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowloadingofxamlfiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-301">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-301">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-302">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-302">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-303">интернетзонеалловнетфрамеворкрелианткомпонентс</span><span class="sxs-lookup"><span data-stu-id="07939-303">InternetZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-304">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-304">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-305">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-305">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-306">интернетзонеалловонляппроведдомаинстаусеактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="07939-306">InternetZoneAllowOnlyApprovedDomainsToUseActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowonlyapproveddomainstouseactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-307">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-308">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-308">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-309">интернетзонеалловонляппроведдомаинстаусетдкактивексконтрол</span><span class="sxs-lookup"><span data-stu-id="07939-309">InternetZoneAllowOnlyApprovedDomainsToUseTDCActiveXControl</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowonlyapproveddomainstousetdcactivexcontrol)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-310">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-310">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-311">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-311">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-312">интернетзонеалловскриптингофинтернетексплорервеббровсерконтролс</span><span class="sxs-lookup"><span data-stu-id="07939-312">InternetZoneAllowScriptingOfInternetExplorerWebBrowserControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowscriptingofinternetexplorerwebbrowsercontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-313">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-313">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-314">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-314">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-315">интернетзонеалловскриптинитиатедвиндовс</span><span class="sxs-lookup"><span data-stu-id="07939-315">InternetZoneAllowScriptInitiatedWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowscriptinitiatedwindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-316">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-316">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-317">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-317">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-318">интернетзонеалловскриптлетс</span><span class="sxs-lookup"><span data-stu-id="07939-318">InternetZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-319">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-319">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-320">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-320">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-321">интернетзонеалловсмартскриние</span><span class="sxs-lookup"><span data-stu-id="07939-321">InternetZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-322">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-322">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-323">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-323">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-324">интернетзонеалловупдатестостатусбарвиаскрипт</span><span class="sxs-lookup"><span data-stu-id="07939-324">InternetZoneAllowUpdatesToStatusBarViaScript</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowupdatestostatusbarviascript)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-325">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-325">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-326">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-326">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-327">интернетзонеалловусердатаперсистенце</span><span class="sxs-lookup"><span data-stu-id="07939-327">InternetZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-328">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-328">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-329">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-329">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-330">интернетзонедонотрунантималвареагаинстактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="07939-330">InternetZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-331">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-331">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-332">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-332">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-333">интернетзонедовнлоадсигнедактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="07939-333">InternetZoneDownloadSignedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonedownloadsignedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-334">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-334">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-335">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-335">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-336">интернетзонедовнлоадунсигнедактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="07939-336">InternetZoneDownloadUnsignedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonedownloadunsignedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-337">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-337">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-338">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-338">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-339">интернетзонинаблекроссситескриптингфилтер</span><span class="sxs-lookup"><span data-stu-id="07939-339">InternetZoneEnableCrossSiteScriptingFilter</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenablecrosssitescriptingfilter)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-340">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-340">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-341">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-341">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-342">интернетзонинабледраггингофконтентфромдифферентдомаинсакроссвиндовс</span><span class="sxs-lookup"><span data-stu-id="07939-342">InternetZoneEnableDraggingOfContentFromDifferentDomainsAcrossWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenabledraggingofcontentfromdifferentdomainsacrosswindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-343">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-343">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-344">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-344">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-345">интернетзонинабледраггингофконтентфромдифферентдомаинсвисинвиндовс</span><span class="sxs-lookup"><span data-stu-id="07939-345">InternetZoneEnableDraggingOfContentFromDifferentDomainsWithinWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenabledraggingofcontentfromdifferentdomainswithinwindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-346">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-346">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-347">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-347">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-348">интернетзонинаблемимесниффинг</span><span class="sxs-lookup"><span data-stu-id="07939-348">InternetZoneEnableMIMESniffing</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenablemimesniffing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-349">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-349">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-350">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-350">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-351">интернетзонинаблепротектедмоде</span><span class="sxs-lookup"><span data-stu-id="07939-351">InternetZoneEnableProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenableprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-352">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-352">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-353">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-353">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-354">интернетзонеинклуделокалпасвхенуплоадингфилестосервер</span><span class="sxs-lookup"><span data-stu-id="07939-354">InternetZoneIncludeLocalPathWhenUploadingFilesToServer</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneincludelocalpathwhenuploadingfilestoserver)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-355">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-355">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-356">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-356">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-357">интернетзонеинитиализеандскриптактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="07939-357">InternetZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-358">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-358">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-359">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-359">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-360">интернетзонежавапермиссионс</span><span class="sxs-lookup"><span data-stu-id="07939-360">InternetZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-361">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-361">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-362">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-362">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-363">интернетзонелаунчингаппликатионсандфилесинифраме</span><span class="sxs-lookup"><span data-stu-id="07939-363">InternetZoneLaunchingApplicationsAndFilesInIFRAME</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonelaunchingapplicationsandfilesiniframe)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-364">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-364">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-365">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-365">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-366">интернетзонелогоноптионс</span><span class="sxs-lookup"><span data-stu-id="07939-366">InternetZoneLogonOptions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonelogonoptions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-367">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-367">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-368">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-368">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-369">интернетзоненавигатевиндовсандфрамес</span><span class="sxs-lookup"><span data-stu-id="07939-369">InternetZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-370">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-370">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-371">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-371">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="07939-372">интернетзонеруннетфрамеворкрелианткомпонентснотсигнедвисаусентикоде</span><span class="sxs-lookup"><span data-stu-id="07939-372">InternetZoneRunNETFrameworkReliantComponentsNotSignedWithAuthenticode</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-373">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-373">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-374">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-374">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-375">интернетзонеруннетфрамеворкрелианткомпонентссигнедвисаусентикоде</span><span class="sxs-lookup"><span data-stu-id="07939-375">InternetZoneRunNETFrameworkReliantComponentsSignedWithAuthenticode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonerunnetframeworkreliantcomponentssignedwithauthenticode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-376">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-376">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-377">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-377">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-378">интернетзонешовсекуритиварнингфорпотентиаллюнсафефилес</span><span class="sxs-lookup"><span data-stu-id="07939-378">InternetZoneShowSecurityWarningForPotentiallyUnsafeFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneshowsecuritywarningforpotentiallyunsafefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-379">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-379">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-380">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-380">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-381">интернетзонеусепопупблоккер</span><span class="sxs-lookup"><span data-stu-id="07939-381">InternetZoneUsePopupBlocker</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneusepopupblocker)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-382">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-382">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-383">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-383">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="07939-384">интернетзоневебситесинлесспривилежедзонесканнавигатеинтосисзоне</span><span class="sxs-lookup"><span data-stu-id="07939-384">InternetZoneWebsitesInLessPrivilegedZonesCanNavigateIntoThisZone</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-385">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-385">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-386">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-386">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-387">интранетзонеалловакцесстодатасаурцес</span><span class="sxs-lookup"><span data-stu-id="07939-387">IntranetZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-388">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-388">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-389">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-389">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-390">интранетзонеалловаутоматикпромптингфорактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="07939-390">IntranetZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-391">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-391">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-392">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-392">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-393">интранетзонеалловаутоматикпромптингфорфиледовнлоадс</span><span class="sxs-lookup"><span data-stu-id="07939-393">IntranetZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-394">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-394">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-395">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-395">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-396">интранетзонеалловфонтдовнлоадс</span><span class="sxs-lookup"><span data-stu-id="07939-396">IntranetZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-397">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-397">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-398">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-398">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-399">интранетзонеалловлесспривилежедситес</span><span class="sxs-lookup"><span data-stu-id="07939-399">IntranetZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-400">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-400">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-401">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-401">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-402">интранетзонеалловнетфрамеворкрелианткомпонентс</span><span class="sxs-lookup"><span data-stu-id="07939-402">IntranetZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-403">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-403">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-404">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-404">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-405">интранетзонеалловскриптлетс</span><span class="sxs-lookup"><span data-stu-id="07939-405">IntranetZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-406">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-406">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-407">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-407">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-408">интранетзонеалловсмартскриние</span><span class="sxs-lookup"><span data-stu-id="07939-408">IntranetZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-409">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-409">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-410">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-410">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-411">интранетзонеалловусердатаперсистенце</span><span class="sxs-lookup"><span data-stu-id="07939-411">IntranetZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-412">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-412">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-413">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-413">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-414">интранетзонедонотрунантималвареагаинстактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="07939-414">IntranetZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-415">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-415">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-416">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-416">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-417">интранетзонеинитиализеандскриптактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="07939-417">IntranetZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-418">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-418">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-419">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-419">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="07939-420">интранетзонеинитиализеандскриптактивексконтролснотмаркедсафе</span><span class="sxs-lookup"><span data-stu-id="07939-420">IntranetZoneInitializeAndScriptActiveXControlsNotMarkedSafe</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-421">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-421">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-422">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-422">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-423">интранетзонежавапермиссионс</span><span class="sxs-lookup"><span data-stu-id="07939-423">IntranetZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-424">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-424">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-425">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-425">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-426">интранетзоненавигатевиндовсандфрамес</span><span class="sxs-lookup"><span data-stu-id="07939-426">IntranetZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-427">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-427">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-428">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-428">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-429">локалмачинезонеалловакцесстодатасаурцес</span><span class="sxs-lookup"><span data-stu-id="07939-429">LocalMachineZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-430">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-430">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-431">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-431">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-432">локалмачинезонеалловаутоматикпромптингфорактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="07939-432">LocalMachineZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-433">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-433">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-434">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-434">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-435">локалмачинезонеалловаутоматикпромптингфорфиледовнлоадс</span><span class="sxs-lookup"><span data-stu-id="07939-435">LocalMachineZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-436">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-436">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-437">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-437">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-438">локалмачинезонеалловфонтдовнлоадс</span><span class="sxs-lookup"><span data-stu-id="07939-438">LocalMachineZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-439">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-439">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-440">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-440">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-441">локалмачинезонеалловлесспривилежедситес</span><span class="sxs-lookup"><span data-stu-id="07939-441">LocalMachineZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-442">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-442">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-443">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-443">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-444">локалмачинезонеалловнетфрамеворкрелианткомпонентс</span><span class="sxs-lookup"><span data-stu-id="07939-444">LocalMachineZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-445">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-445">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-446">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-446">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-447">локалмачинезонеалловскриптлетс</span><span class="sxs-lookup"><span data-stu-id="07939-447">LocalMachineZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-448">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-448">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-449">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-449">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-450">локалмачинезонеалловсмартскриние</span><span class="sxs-lookup"><span data-stu-id="07939-450">LocalMachineZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-451">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-451">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-452">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-452">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-453">локалмачинезонеалловусердатаперсистенце</span><span class="sxs-lookup"><span data-stu-id="07939-453">LocalMachineZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-454">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-454">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-455">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-455">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-456">локалмачинезонедонотрунантималвареагаинстактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="07939-456">LocalMachineZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-457">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-457">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-458">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-458">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-459">локалмачинезонеинитиализеандскриптактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="07939-459">LocalMachineZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-460">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-460">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-461">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-461">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-462">локалмачинезонежавапермиссионс</span><span class="sxs-lookup"><span data-stu-id="07939-462">LocalMachineZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-463">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-463">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-464">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-464">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-465">локалмачинезоненавигатевиндовсандфрамес</span><span class="sxs-lookup"><span data-stu-id="07939-465">LocalMachineZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-466">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-466">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-467">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-467">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-468">локкеддовнинтернетзонеалловакцесстодатасаурцес</span><span class="sxs-lookup"><span data-stu-id="07939-468">LockedDownInternetZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-469">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-469">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-470">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-470">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-471">локкеддовнинтернетзонеалловаутоматикпромптингфорактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="07939-471">LockedDownInternetZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-472">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-472">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-473">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-473">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-474">локкеддовнинтернетзонеалловаутоматикпромптингфорфиледовнлоадс</span><span class="sxs-lookup"><span data-stu-id="07939-474">LockedDownInternetZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-475">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-475">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-476">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-476">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-477">локкеддовнинтернетзонеалловфонтдовнлоадс</span><span class="sxs-lookup"><span data-stu-id="07939-477">LockedDownInternetZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-478">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-478">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-479">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-479">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-480">локкеддовнинтернетзонеалловлесспривилежедситес</span><span class="sxs-lookup"><span data-stu-id="07939-480">LockedDownInternetZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-481">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-481">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-482">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-482">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-483">локкеддовнинтернетзонеалловнетфрамеворкрелианткомпонентс</span><span class="sxs-lookup"><span data-stu-id="07939-483">LockedDownInternetZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-484">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-484">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-485">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-485">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-486">локкеддовнинтернетзонеалловскриптлетс</span><span class="sxs-lookup"><span data-stu-id="07939-486">LockedDownInternetZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-487">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-487">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-488">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-488">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-489">локкеддовнинтернетзонеалловсмартскриние</span><span class="sxs-lookup"><span data-stu-id="07939-489">LockedDownInternetZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-490">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-490">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-491">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-491">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-492">локкеддовнинтернетзонеалловусердатаперсистенце</span><span class="sxs-lookup"><span data-stu-id="07939-492">LockedDownInternetZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-493">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-493">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-494">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-494">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-495">локкеддовнинтернетзонеинитиализеандскриптактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="07939-495">LockedDownInternetZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-496">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-496">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-497">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-497">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-498">локкеддовнинтернетзонежавапермиссионс</span><span class="sxs-lookup"><span data-stu-id="07939-498">LockedDownInternetZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-499">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-499">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-500">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-500">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-501">локкеддовнинтернетзоненавигатевиндовсандфрамес</span><span class="sxs-lookup"><span data-stu-id="07939-501">LockedDownInternetZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-502">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-502">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-503">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-503">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-504">локкеддовнинтранетзонеалловакцесстодатасаурцес</span><span class="sxs-lookup"><span data-stu-id="07939-504">LockedDownIntranetZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-505">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-505">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-506">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-506">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-507">локкеддовнинтранетзонеалловаутоматикпромптингфорактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="07939-507">LockedDownIntranetZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-508">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-508">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-509">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-509">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-510">локкеддовнинтранетзонеалловаутоматикпромптингфорфиледовнлоадс</span><span class="sxs-lookup"><span data-stu-id="07939-510">LockedDownIntranetZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-511">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-511">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-512">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-512">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-513">локкеддовнинтранетзонеалловфонтдовнлоадс</span><span class="sxs-lookup"><span data-stu-id="07939-513">LockedDownIntranetZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-514">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-514">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-515">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-515">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-516">локкеддовнинтранетзонеалловлесспривилежедситес</span><span class="sxs-lookup"><span data-stu-id="07939-516">LockedDownIntranetZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-517">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-517">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-518">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-518">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-519">локкеддовнинтранетзонеалловнетфрамеворкрелианткомпонентс</span><span class="sxs-lookup"><span data-stu-id="07939-519">LockedDownIntranetZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-520">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-520">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-521">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-521">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-522">локкеддовнинтранетзонеалловскриптлетс</span><span class="sxs-lookup"><span data-stu-id="07939-522">LockedDownIntranetZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-523">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-523">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-524">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-524">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-525">локкеддовнинтранетзонеалловсмартскриние</span><span class="sxs-lookup"><span data-stu-id="07939-525">LockedDownIntranetZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-526">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-526">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-527">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-527">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-528">локкеддовнинтранетзонеалловусердатаперсистенце</span><span class="sxs-lookup"><span data-stu-id="07939-528">LockedDownIntranetZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-529">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-529">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-530">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-530">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-531">локкеддовнинтранетзонеинитиализеандскриптактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="07939-531">LockedDownIntranetZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-532">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-532">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-533">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-533">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-534">локкеддовнинтранетзоненавигатевиндовсандфрамес</span><span class="sxs-lookup"><span data-stu-id="07939-534">LockedDownIntranetZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-535">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-535">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-536">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-536">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-537">локкеддовнлокалмачинезонеалловакцесстодатасаурцес</span><span class="sxs-lookup"><span data-stu-id="07939-537">LockedDownLocalMachineZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-538">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-538">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-539">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-539">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-540">локкеддовнлокалмачинезонеалловаутоматикпромптингфорактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="07939-540">LockedDownLocalMachineZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-541">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-541">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-542">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-542">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-543">локкеддовнлокалмачинезонеалловаутоматикпромптингфорфиледовнлоадс</span><span class="sxs-lookup"><span data-stu-id="07939-543">LockedDownLocalMachineZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-544">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-544">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-545">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-545">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-546">локкеддовнлокалмачинезонеалловфонтдовнлоадс</span><span class="sxs-lookup"><span data-stu-id="07939-546">LockedDownLocalMachineZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-547">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-547">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-548">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-548">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-549">локкеддовнлокалмачинезонеалловлесспривилежедситес</span><span class="sxs-lookup"><span data-stu-id="07939-549">LockedDownLocalMachineZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-550">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-550">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-551">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-551">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-552">локкеддовнлокалмачинезонеалловнетфрамеворкрелианткомпонентс</span><span class="sxs-lookup"><span data-stu-id="07939-552">LockedDownLocalMachineZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-553">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-553">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-554">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-554">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-555">локкеддовнлокалмачинезонеалловскриптлетс</span><span class="sxs-lookup"><span data-stu-id="07939-555">LockedDownLocalMachineZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-556">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-556">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-557">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-557">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-558">локкеддовнлокалмачинезонеалловсмартскриние</span><span class="sxs-lookup"><span data-stu-id="07939-558">LockedDownLocalMachineZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-559">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-559">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-560">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-560">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-561">локкеддовнлокалмачинезонеалловусердатаперсистенце</span><span class="sxs-lookup"><span data-stu-id="07939-561">LockedDownLocalMachineZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-562">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-562">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-563">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-563">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-564">локкеддовнлокалмачинезонеинитиализеандскриптактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="07939-564">LockedDownLocalMachineZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-565">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-565">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-566">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-566">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-567">локкеддовнлокалмачинезонежавапермиссионс</span><span class="sxs-lookup"><span data-stu-id="07939-567">LockedDownLocalMachineZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-568">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-568">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-569">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-569">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-570">локкеддовнлокалмачинезоненавигатевиндовсандфрамес</span><span class="sxs-lookup"><span data-stu-id="07939-570">LockedDownLocalMachineZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-571">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-571">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-572">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-572">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-573">локкеддовнрестриктедситесзонеалловакцесстодатасаурцес</span><span class="sxs-lookup"><span data-stu-id="07939-573">LockedDownRestrictedSitesZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-574">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-574">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-575">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-575">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-576">локкеддовнрестриктедситесзонеалловаутоматикпромптингфорактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="07939-576">LockedDownRestrictedSitesZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-577">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-577">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-578">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-578">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-579">локкеддовнрестриктедситесзонеалловаутоматикпромптингфорфиледовнлоадс</span><span class="sxs-lookup"><span data-stu-id="07939-579">LockedDownRestrictedSitesZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-580">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-580">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-581">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-581">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-582">локкеддовнрестриктедситесзонеалловфонтдовнлоадс</span><span class="sxs-lookup"><span data-stu-id="07939-582">LockedDownRestrictedSitesZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-583">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-583">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-584">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-584">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-585">локкеддовнрестриктедситесзонеалловлесспривилежедситес</span><span class="sxs-lookup"><span data-stu-id="07939-585">LockedDownRestrictedSitesZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-586">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-586">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-587">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-587">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-588">локкеддовнрестриктедситесзонеалловнетфрамеворкрелианткомпонентс</span><span class="sxs-lookup"><span data-stu-id="07939-588">LockedDownRestrictedSitesZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-589">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-589">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-590">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-590">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-591">локкеддовнрестриктедситесзонеалловскриптлетс</span><span class="sxs-lookup"><span data-stu-id="07939-591">LockedDownRestrictedSitesZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-592">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-592">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-593">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-593">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-594">локкеддовнрестриктедситесзонеалловсмартскриние</span><span class="sxs-lookup"><span data-stu-id="07939-594">LockedDownRestrictedSitesZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-595">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-595">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-596">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-596">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-597">локкеддовнрестриктедситесзонеалловусердатаперсистенце</span><span class="sxs-lookup"><span data-stu-id="07939-597">LockedDownRestrictedSitesZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-598">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-598">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-599">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-599">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-600">локкеддовнрестриктедситесзонеинитиализеандскриптактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="07939-600">LockedDownRestrictedSitesZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-601">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-601">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-602">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-602">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-603">локкеддовнрестриктедситесзонежавапермиссионс</span><span class="sxs-lookup"><span data-stu-id="07939-603">LockedDownRestrictedSitesZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-604">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-604">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-605">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-605">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-606">локкеддовнрестриктедситесзоненавигатевиндовсандфрамес</span><span class="sxs-lookup"><span data-stu-id="07939-606">LockedDownRestrictedSitesZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-607">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-607">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-608">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-608">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-609">локкеддовнтрустедситесзонеалловакцесстодатасаурцес</span><span class="sxs-lookup"><span data-stu-id="07939-609">LockedDownTrustedSitesZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-610">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-610">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-611">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-611">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-612">локкеддовнтрустедситесзонеалловаутоматикпромптингфорактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="07939-612">LockedDownTrustedSitesZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-613">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-613">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-614">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-614">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-615">локкеддовнтрустедситесзонеалловаутоматикпромптингфорфиледовнлоадс</span><span class="sxs-lookup"><span data-stu-id="07939-615">LockedDownTrustedSitesZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-616">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-616">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-617">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-617">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-618">локкеддовнтрустедситесзонеалловфонтдовнлоадс</span><span class="sxs-lookup"><span data-stu-id="07939-618">LockedDownTrustedSitesZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-619">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-619">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-620">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-620">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-621">локкеддовнтрустедситесзонеалловлесспривилежедситес</span><span class="sxs-lookup"><span data-stu-id="07939-621">LockedDownTrustedSitesZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-622">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-622">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-623">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-623">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-624">локкеддовнтрустедситесзонеалловнетфрамеворкрелианткомпонентс</span><span class="sxs-lookup"><span data-stu-id="07939-624">LockedDownTrustedSitesZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-625">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-625">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-626">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-626">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-627">локкеддовнтрустедситесзонеалловскриптлетс</span><span class="sxs-lookup"><span data-stu-id="07939-627">LockedDownTrustedSitesZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-628">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-628">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-629">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-629">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-630">локкеддовнтрустедситесзонеалловсмартскриние</span><span class="sxs-lookup"><span data-stu-id="07939-630">LockedDownTrustedSitesZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-631">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-631">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-632">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-632">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-633">локкеддовнтрустедситесзонеалловусердатаперсистенце</span><span class="sxs-lookup"><span data-stu-id="07939-633">LockedDownTrustedSitesZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-634">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-634">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-635">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-635">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-636">локкеддовнтрустедситесзонеинитиализеандскриптактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="07939-636">LockedDownTrustedSitesZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-637">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-637">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-638">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-638">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-639">локкеддовнтрустедситесзонежавапермиссионс</span><span class="sxs-lookup"><span data-stu-id="07939-639">LockedDownTrustedSitesZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-640">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-640">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-641">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-641">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-642">локкеддовнтрустедситесзоненавигатевиндовсандфрамес</span><span class="sxs-lookup"><span data-stu-id="07939-642">LockedDownTrustedSitesZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-643">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-643">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-644">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-644">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-645">мимесниффингсафетифеатуреинтернетексплорерпроцессес</span><span class="sxs-lookup"><span data-stu-id="07939-645">MimeSniffingSafetyFeatureInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-mimesniffingsafetyfeatureinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-646">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-646">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-647">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-647">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-648">мкпротоколсекуритирестриктионинтернетексплорерпроцессес</span><span class="sxs-lookup"><span data-stu-id="07939-648">MKProtocolSecurityRestrictionInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-mkprotocolsecurityrestrictioninternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-649">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-649">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-650">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-650">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-651">нотификатионбаринтернетексплорерпроцессес</span><span class="sxs-lookup"><span data-stu-id="07939-651">NotificationBarInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-notificationbarinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-652">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-652">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-653">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-653">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="07939-654">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="07939-654">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-655">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-655">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-656">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="07939-656">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="07939-657">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="07939-657">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-658">превентманагингсмартскринфилтер</span><span class="sxs-lookup"><span data-stu-id="07939-658">PreventManagingSmartScreenFilter</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-preventmanagingsmartscreenfilter)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-659">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-659">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-660">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-660">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-661">превентперусеринсталлатионофактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="07939-661">PreventPerUserInstallationOfActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-preventperuserinstallationofactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-662">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-662">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-663">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-663">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-664">протектионфромзонилеватионинтернетексплорерпроцессес</span><span class="sxs-lookup"><span data-stu-id="07939-664">ProtectionFromZoneElevationInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-protectionfromzoneelevationinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-665">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-665">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-666">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-666">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-667">ремоверунсистимебуттонфораутдатедактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="07939-667">RemoveRunThisTimeButtonForOutdatedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-removerunthistimebuttonforoutdatedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-668">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-668">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-669">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-669">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-670">рестриктактивексинсталлинтернетексплорерпроцессес</span><span class="sxs-lookup"><span data-stu-id="07939-670">RestrictActiveXInstallInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictactivexinstallinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-671">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-671">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-672">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-672">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-673">рестриктедситесзонеалловакцесстодатасаурцес</span><span class="sxs-lookup"><span data-stu-id="07939-673">RestrictedSitesZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-674">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-674">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-675">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-675">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-676">рестриктедситесзонеалловактивескриптинг</span><span class="sxs-lookup"><span data-stu-id="07939-676">RestrictedSitesZoneAllowActiveScripting</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowactivescripting)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-677">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-677">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-678">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-678">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-679">рестриктедситесзонеалловаутоматикпромптингфорактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="07939-679">RestrictedSitesZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-680">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-680">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-681">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-681">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-682">рестриктедситесзонеалловаутоматикпромптингфорфиледовнлоадс</span><span class="sxs-lookup"><span data-stu-id="07939-682">RestrictedSitesZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-683">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-683">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-684">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-684">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-685">рестриктедситесзонеалловбинаряндскриптбехавиорс</span><span class="sxs-lookup"><span data-stu-id="07939-685">RestrictedSitesZoneAllowBinaryAndScriptBehaviors</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowbinaryandscriptbehaviors)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-686">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-686">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-687">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-687">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-688">рестриктедситесзонеалловкопипастевиаскрипт</span><span class="sxs-lookup"><span data-stu-id="07939-688">RestrictedSitesZoneAllowCopyPasteViaScript</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowcopypasteviascript)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-689">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-689">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-690">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-690">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-691">рестриктедситесзонеалловдраганддропкопяндпастефилес</span><span class="sxs-lookup"><span data-stu-id="07939-691">RestrictedSitesZoneAllowDragAndDropCopyAndPasteFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowdraganddropcopyandpastefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-692">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-692">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-693">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-693">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-694">рестриктедситесзонеалловфиледовнлоадс</span><span class="sxs-lookup"><span data-stu-id="07939-694">RestrictedSitesZoneAllowFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-695">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-695">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-696">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-696">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-697">рестриктедситесзонеалловфонтдовнлоадс</span><span class="sxs-lookup"><span data-stu-id="07939-697">RestrictedSitesZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-698">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-698">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-699">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-699">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-700">рестриктедситесзонеалловлесспривилежедситес</span><span class="sxs-lookup"><span data-stu-id="07939-700">RestrictedSitesZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-701">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-701">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-702">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-702">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-703">рестриктедситесзонеалловлоадингофксамлфилес</span><span class="sxs-lookup"><span data-stu-id="07939-703">RestrictedSitesZoneAllowLoadingOfXAMLFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowloadingofxamlfiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-704">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-704">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-705">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-705">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-706">рестриктедситесзонеалловметарефреш</span><span class="sxs-lookup"><span data-stu-id="07939-706">RestrictedSitesZoneAllowMETAREFRESH</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowmetarefresh)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-707">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-707">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-708">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-708">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-709">рестриктедситесзонеалловнетфрамеворкрелианткомпонентс</span><span class="sxs-lookup"><span data-stu-id="07939-709">RestrictedSitesZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-710">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-710">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-711">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-711">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-712">рестриктедситесзонеалловонляппроведдомаинстаусеактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="07939-712">RestrictedSitesZoneAllowOnlyApprovedDomainsToUseActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowonlyapproveddomainstouseactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-713">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-713">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-714">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-714">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-715">рестриктедситесзонеалловонляппроведдомаинстаусетдкактивексконтрол</span><span class="sxs-lookup"><span data-stu-id="07939-715">RestrictedSitesZoneAllowOnlyApprovedDomainsToUseTDCActiveXControl</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowonlyapproveddomainstousetdcactivexcontrol)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-716">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-716">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-717">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-717">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-718">рестриктедситесзонеалловскриптингофинтернетексплорервеббровсерконтролс</span><span class="sxs-lookup"><span data-stu-id="07939-718">RestrictedSitesZoneAllowScriptingOfInternetExplorerWebBrowserControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowscriptingofinternetexplorerwebbrowsercontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-719">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-719">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-720">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-720">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-721">рестриктедситесзонеалловскриптинитиатедвиндовс</span><span class="sxs-lookup"><span data-stu-id="07939-721">RestrictedSitesZoneAllowScriptInitiatedWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowscriptinitiatedwindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-722">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-722">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-723">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-723">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-724">рестриктедситесзонеалловскриптлетс</span><span class="sxs-lookup"><span data-stu-id="07939-724">RestrictedSitesZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-725">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-725">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-726">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-726">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-727">рестриктедситесзонеалловсмартскриние</span><span class="sxs-lookup"><span data-stu-id="07939-727">RestrictedSitesZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-728">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-728">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-729">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-729">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-730">рестриктедситесзонеалловупдатестостатусбарвиаскрипт</span><span class="sxs-lookup"><span data-stu-id="07939-730">RestrictedSitesZoneAllowUpdatesToStatusBarViaScript</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowupdatestostatusbarviascript)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-731">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-731">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-732">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-732">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-733">рестриктедситесзонеалловусердатаперсистенце</span><span class="sxs-lookup"><span data-stu-id="07939-733">RestrictedSitesZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-734">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-734">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-735">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-735">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-736">рестриктедситесзонедонотрунантималвареагаинстактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="07939-736">RestrictedSitesZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-737">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-737">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-738">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-738">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-739">рестриктедситесзонедовнлоадсигнедактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="07939-739">RestrictedSitesZoneDownloadSignedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonedownloadsignedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-740">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-740">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-741">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-741">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-742">рестриктедситесзонедовнлоадунсигнедактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="07939-742">RestrictedSitesZoneDownloadUnsignedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonedownloadunsignedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-743">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-743">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-744">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-744">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-745">рестриктедситесзонинаблекроссситескриптингфилтер</span><span class="sxs-lookup"><span data-stu-id="07939-745">RestrictedSitesZoneEnableCrossSiteScriptingFilter</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneenablecrosssitescriptingfilter)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-746">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-746">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-747">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-747">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-748">рестриктедситесзонинабледраггингофконтентфромдифферентдомаинсакроссвиндовс</span><span class="sxs-lookup"><span data-stu-id="07939-748">RestrictedSitesZoneEnableDraggingOfContentFromDifferentDomainsAcrossWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneenabledraggingofcontentfromdifferentdomainsacrosswindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-749">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-749">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-750">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-750">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-751">рестриктедситесзонинабледраггингофконтентфромдифферентдомаинсвисинвиндовс</span><span class="sxs-lookup"><span data-stu-id="07939-751">RestrictedSitesZoneEnableDraggingOfContentFromDifferentDomainsWithinWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneenabledraggingofcontentfromdifferentdomainswithinwindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-752">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-752">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-753">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-753">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-754">рестриктедситесзонинаблемимесниффинг</span><span class="sxs-lookup"><span data-stu-id="07939-754">RestrictedSitesZoneEnableMIMESniffing</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneenablemimesniffing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-755">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-755">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-756">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-756">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-757">рестриктедситесзонеинклуделокалпасвхенуплоадингфилестосервер</span><span class="sxs-lookup"><span data-stu-id="07939-757">RestrictedSitesZoneIncludeLocalPathWhenUploadingFilesToServer</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneincludelocalpathwhenuploadingfilestoserver)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-758">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-758">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-759">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-759">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-760">рестриктедситесзонеинитиализеандскриптактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="07939-760">RestrictedSitesZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-761">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-761">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-762">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-762">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-763">рестриктедситесзонежавапермиссионс</span><span class="sxs-lookup"><span data-stu-id="07939-763">RestrictedSitesZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-764">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-764">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-765">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-765">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-766">рестриктедситесзонелаунчингаппликатионсандфилесинифраме</span><span class="sxs-lookup"><span data-stu-id="07939-766">RestrictedSitesZoneLaunchingApplicationsAndFilesInIFRAME</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonelaunchingapplicationsandfilesiniframe)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-767">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-767">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-768">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-768">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-769">рестриктедситесзонелогоноптионс</span><span class="sxs-lookup"><span data-stu-id="07939-769">RestrictedSitesZoneLogonOptions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonelogonoptions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-770">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-770">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-771">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-771">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-772">рестриктедситесзоненавигатевиндовсандфрамес</span><span class="sxs-lookup"><span data-stu-id="07939-772">RestrictedSitesZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-773">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-773">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-774">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-774">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="07939-775">рестриктедситесзоненавигатевиндовсандфрамесакроссдомаинс</span><span class="sxs-lookup"><span data-stu-id="07939-775">RestrictedSitesZoneNavigateWindowsAndFramesAcrossDomains</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-776">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-776">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-777">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-777">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-778">рестриктедситесзонерунактивексконтролсандплугинс</span><span class="sxs-lookup"><span data-stu-id="07939-778">RestrictedSitesZoneRunActiveXControlsAndPlugins</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonerunactivexcontrolsandplugins)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-779">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-779">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-780">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-780">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-781">рестриктедситесзонеруннетфрамеворкрелианткомпонентссигнедвисаусентикоде</span><span class="sxs-lookup"><span data-stu-id="07939-781">RestrictedSitesZoneRunNETFrameworkReliantComponentsSignedWithAuthenticode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonerunnetframeworkreliantcomponentssignedwithauthenticode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-782">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-782">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-783">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-783">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-784">рестриктедситесзонескриптактивексконтролсмаркедсафефорскриптинг</span><span class="sxs-lookup"><span data-stu-id="07939-784">RestrictedSitesZoneScriptActiveXControlsMarkedSafeForScripting</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonescriptactivexcontrolsmarkedsafeforscripting)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-785">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-785">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-786">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-786">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-787">рестриктедситесзонескриптингофжаваапплетс</span><span class="sxs-lookup"><span data-stu-id="07939-787">RestrictedSitesZoneScriptingOfJavaApplets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonescriptingofjavaapplets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-788">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-788">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-789">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-789">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-790">рестриктедситесзонешовсекуритиварнингфорпотентиаллюнсафефилес</span><span class="sxs-lookup"><span data-stu-id="07939-790">RestrictedSitesZoneShowSecurityWarningForPotentiallyUnsafeFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneshowsecuritywarningforpotentiallyunsafefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-791">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-791">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-792">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-792">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="07939-793">рестриктедситесзонетурнонкроссситескриптингфилтер</span><span class="sxs-lookup"><span data-stu-id="07939-793">RestrictedSitesZoneTurnOnCrossSiteScriptingFilter</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-794">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-794">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-795">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-795">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-796">рестриктедситесзонетурнонпротектедмоде</span><span class="sxs-lookup"><span data-stu-id="07939-796">RestrictedSitesZoneTurnOnProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneturnonprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-797">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-797">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-798">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-798">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-799">рестриктедситесзонеусепопупблоккер</span><span class="sxs-lookup"><span data-stu-id="07939-799">RestrictedSitesZoneUsePopupBlocker</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneusepopupblocker)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-800">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-800">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-801">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-801">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-802">рестриктфиледовнлоадинтернетексплорерпроцессес</span><span class="sxs-lookup"><span data-stu-id="07939-802">RestrictFileDownloadInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictfiledownloadinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-803">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-803">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-804">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-804">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-805">скриптедвиндовсекуритирестриктионсинтернетексплорерпроцессес</span><span class="sxs-lookup"><span data-stu-id="07939-805">ScriptedWindowSecurityRestrictionsInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-scriptedwindowsecurityrestrictionsinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-806">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-806">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-807">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-807">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-808">SearchProviderList</span><span class="sxs-lookup"><span data-stu-id="07939-808">SearchProviderList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-searchproviderlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-809">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-809">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-810">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-810">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-811">спеЦифюсеофактивексинсталлерсервице</span><span class="sxs-lookup"><span data-stu-id="07939-811">SpecifyUseOfActiveXInstallerService</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-specifyuseofactivexinstallerservice)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-812">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-812">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-813">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-813">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-814">трустедситесзонеалловакцесстодатасаурцес</span><span class="sxs-lookup"><span data-stu-id="07939-814">TrustedSitesZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-815">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-815">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-816">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-816">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-817">трустедситесзонеалловаутоматикпромптингфорактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="07939-817">TrustedSitesZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-818">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-818">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-819">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-819">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-820">трустедситесзонеалловаутоматикпромптингфорфиледовнлоадс</span><span class="sxs-lookup"><span data-stu-id="07939-820">TrustedSitesZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-821">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-821">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-822">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-822">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-823">трустедситесзонеалловфонтдовнлоадс</span><span class="sxs-lookup"><span data-stu-id="07939-823">TrustedSitesZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-824">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-824">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-825">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-825">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-826">трустедситесзонеалловлесспривилежедситес</span><span class="sxs-lookup"><span data-stu-id="07939-826">TrustedSitesZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-827">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-827">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-828">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-828">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-829">трустедситесзонеалловнетфрамеворкрелианткомпонентс</span><span class="sxs-lookup"><span data-stu-id="07939-829">TrustedSitesZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-830">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-830">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-831">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-831">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-832">трустедситесзонеалловскриптлетс</span><span class="sxs-lookup"><span data-stu-id="07939-832">TrustedSitesZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-833">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-833">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-834">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-834">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-835">трустедситесзонеалловсмартскриние</span><span class="sxs-lookup"><span data-stu-id="07939-835">TrustedSitesZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-836">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-836">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-837">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-837">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-838">трустедситесзонеалловусердатаперсистенце</span><span class="sxs-lookup"><span data-stu-id="07939-838">TrustedSitesZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-839">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-839">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-840">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-840">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-841">трустедситесзонедонотрунантималвареагаинстактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="07939-841">TrustedSitesZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-842">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-842">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-843">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-843">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="07939-844">трустедситесзонедонтрунантималварепрограмсагаинстактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="07939-844">TrustedSitesZoneDontRunAntimalwareProgramsAgainstActiveXControls</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-845">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-845">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-846">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-846">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-847">трустедситесзонеинитиализеандскриптактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="07939-847">TrustedSitesZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-848">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-848">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-849">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-849">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="07939-850">трустедситесзонеинитиализеандскриптактивексконтролснотмаркедассафе</span><span class="sxs-lookup"><span data-stu-id="07939-850">TrustedSitesZoneInitializeAndScriptActiveXControlsNotMarkedAsSafe</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-851">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-851">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-852">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-852">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="07939-853">трустедситесзонеинитиализеандскриптактивексконтролснотмаркедсафе</span><span class="sxs-lookup"><span data-stu-id="07939-853">TrustedSitesZoneInitializeAndScriptActiveXControlsNotMarkedSafe</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-854">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-854">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-855">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-855">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-856">трустедситесзонежавапермиссионс</span><span class="sxs-lookup"><span data-stu-id="07939-856">TrustedSitesZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-857">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-857">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-858">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-858">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="07939-859">трустедситесзоненавигатевиндовсандфрамес</span><span class="sxs-lookup"><span data-stu-id="07939-859">TrustedSitesZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="07939-860">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07939-860">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07939-861">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="07939-861">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="07939-862">Требования</span><span class="sxs-lookup"><span data-stu-id="07939-862">Requirements</span></span>



| <span data-ttu-id="07939-863">Требование</span><span class="sxs-lookup"><span data-stu-id="07939-863">Requirement</span></span> | <span data-ttu-id="07939-864">Значение</span><span class="sxs-lookup"><span data-stu-id="07939-864">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07939-865">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="07939-865">Minimum supported client</span></span><br/> | <span data-ttu-id="07939-866">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="07939-866">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="07939-867">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="07939-867">Minimum supported server</span></span><br/> | <span data-ttu-id="07939-868">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="07939-868">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="07939-869">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="07939-869">Namespace</span></span><br/>                | <span data-ttu-id="07939-870">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="07939-870">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="07939-871">MOF</span><span class="sxs-lookup"><span data-stu-id="07939-871">MOF</span></span><br/>                      | <dl> <span data-ttu-id="07939-872"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="07939-872"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="07939-873">DLL</span><span class="sxs-lookup"><span data-stu-id="07939-873">DLL</span></span><br/>                      | <dl> <span data-ttu-id="07939-874"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="07939-874"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

