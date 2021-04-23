---
title: Класс MDM_Policy_User_Result01_InternetExplorer02
description: '\_ \_ \_ Класс User RESULT01 InternetExplorer02 политики MDM \_ представляет доступные политики Internet Explorer.'
ms.assetid: efd999aa-4aa8-486d-82d4-20af7e2005fe
keywords:
- Класс MDM_Policy_User_Result01_InternetExplorer02
- MDM_Policy_User_Result01_InternetExplorer02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Policy_User_Result01_InternetExplorer02
- MDM_Policy_User_Result01_InternetExplorer02.InstanceID
- MDM_Policy_User_Result01_InternetExplorer02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8693720c7a973cc6bc689abbf76a4674f185e23
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489201"
---
# <a name="mdm_policy_user_result01_internetexplorer02-class"></a><span data-ttu-id="a72b1-105">\_Класс политики MDM \_ user \_ Result01 \_ InternetExplorer02</span><span class="sxs-lookup"><span data-stu-id="a72b1-105">MDM\_Policy\_User\_Result01\_InternetExplorer02 class</span></span>

<span data-ttu-id="a72b1-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="a72b1-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="a72b1-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="a72b1-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="a72b1-108">\_ \_ \_ Класс User RESULT01 InternetExplorer02 политики MDM \_ представляет доступные политики Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="a72b1-108">The MDM\_Policy\_User\_Result01\_InternetExplorer02 class represents the available Internet Explorer policies.</span></span>

<span data-ttu-id="a72b1-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="a72b1-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a72b1-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a72b1-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Result01_InternetExplorer02
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

## <a name="members"></a><span data-ttu-id="a72b1-111">Члены</span><span class="sxs-lookup"><span data-stu-id="a72b1-111">Members</span></span>

<span data-ttu-id="a72b1-112">Класс **\_ \_ user \_ Result01 \_ InternetExplorer02 политики MDM** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="a72b1-112">The **MDM\_Policy\_User\_Result01\_InternetExplorer02** class has these types of members:</span></span>

-   [<span data-ttu-id="a72b1-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="a72b1-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a72b1-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="a72b1-114">Properties</span></span>

<span data-ttu-id="a72b1-115">Класс **\_ \_ user \_ Result01 \_ InternetExplorer02 политики MDM** имеет эти свойства.</span><span class="sxs-lookup"><span data-stu-id="a72b1-115">The **MDM\_Policy\_User\_Result01\_InternetExplorer02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="a72b1-116">AddSearchProvider</span><span class="sxs-lookup"><span data-stu-id="a72b1-116">AddSearchProvider</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-addsearchprovider)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-117">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-119">алловактивексфилтеринг</span><span class="sxs-lookup"><span data-stu-id="a72b1-119">AllowActiveXFiltering</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowactivexfiltering)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-121">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-122">алловаддонлист</span><span class="sxs-lookup"><span data-stu-id="a72b1-122">AllowAddOnList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowaddonlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-123">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-124">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-125">алловаутокомплете</span><span class="sxs-lookup"><span data-stu-id="a72b1-125">AllowAutoComplete</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowautocomplete)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-126">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-127">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-128">алловцертификатеаддрессмисматчварнинг</span><span class="sxs-lookup"><span data-stu-id="a72b1-128">AllowCertificateAddressMismatchWarning</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowcertificateaddressmismatchwarning)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-129">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-130">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-131">алловделетингбровсингхисторйонексит</span><span class="sxs-lookup"><span data-stu-id="a72b1-131">AllowDeletingBrowsingHistoryOnExit</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowdeletingbrowsinghistoryonexit)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-132">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-133">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-134">алловенханцедпротектедмоде</span><span class="sxs-lookup"><span data-stu-id="a72b1-134">AllowEnhancedProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowenhancedprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-135">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-136">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-137">алловентерприсемодефромтулсмену</span><span class="sxs-lookup"><span data-stu-id="a72b1-137">AllowEnterpriseModeFromToolsMenu</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowenterprisemodefromtoolsmenu)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-138">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-139">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-140">алловентерприсемодесителист</span><span class="sxs-lookup"><span data-stu-id="a72b1-140">AllowEnterpriseModeSiteList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowenterprisemodesitelist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-141">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-142">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-143">AllowInternetExplorer7PolicyList</span><span class="sxs-lookup"><span data-stu-id="a72b1-143">AllowInternetExplorer7PolicyList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowinternetexplorer7policylist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-144">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-145">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-146">алловинтернетексплорерстандардсмоде</span><span class="sxs-lookup"><span data-stu-id="a72b1-146">AllowInternetExplorerStandardsMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowinternetexplorerstandardsmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-147">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-148">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-149">алловинтернетзонетемплате</span><span class="sxs-lookup"><span data-stu-id="a72b1-149">AllowInternetZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowinternetzonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-150">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-151">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-152">алловинтранетзонетемплате</span><span class="sxs-lookup"><span data-stu-id="a72b1-152">AllowIntranetZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowintranetzonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-153">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-154">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-155">алловлокалмачинезонетемплате</span><span class="sxs-lookup"><span data-stu-id="a72b1-155">AllowLocalMachineZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlocalmachinezonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-156">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-157">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-158">алловлоккеддовнинтернетзонетемплате</span><span class="sxs-lookup"><span data-stu-id="a72b1-158">AllowLockedDownInternetZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlockeddowninternetzonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-159">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-160">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-161">алловлоккеддовнинтранетзонетемплате</span><span class="sxs-lookup"><span data-stu-id="a72b1-161">AllowLockedDownIntranetZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlockeddownintranetzonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-162">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-163">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-164">алловлоккеддовнлокалмачинезонетемплате</span><span class="sxs-lookup"><span data-stu-id="a72b1-164">AllowLockedDownLocalMachineZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlockeddownlocalmachinezonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-165">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-166">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-166">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-167">алловлоккеддовнрестриктедситесзонетемплате</span><span class="sxs-lookup"><span data-stu-id="a72b1-167">AllowLockedDownRestrictedSitesZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlockeddownrestrictedsiteszonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-168">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-169">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-169">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-170">алловоневордентри</span><span class="sxs-lookup"><span data-stu-id="a72b1-170">AllowOneWordEntry</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowonewordentry)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-171">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-172">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-172">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-173">алловситетозонеассигнментлист</span><span class="sxs-lookup"><span data-stu-id="a72b1-173">AllowSiteToZoneAssignmentList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowsitetozoneassignmentlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-174">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-175">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-175">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-176">алловслоккеддовнтрустедситесзонетемплате</span><span class="sxs-lookup"><span data-stu-id="a72b1-176">AllowsLockedDownTrustedSitesZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowslockeddowntrustedsiteszonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-177">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-178">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-178">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-179">алловсофтваревхенсигнатуреисинвалид</span><span class="sxs-lookup"><span data-stu-id="a72b1-179">AllowSoftwareWhenSignatureIsInvalid</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowsoftwarewhensignatureisinvalid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-180">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-181">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-181">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-182">алловсрестриктедситесзонетемплате</span><span class="sxs-lookup"><span data-stu-id="a72b1-182">AllowsRestrictedSitesZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowsrestrictedsiteszonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-183">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-184">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-184">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-185">алловсугжестедситес</span><span class="sxs-lookup"><span data-stu-id="a72b1-185">AllowSuggestedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowsuggestedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-186">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-187">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-187">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-188">алловтрустедситесзонетемплате</span><span class="sxs-lookup"><span data-stu-id="a72b1-188">AllowTrustedSitesZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowtrustedsiteszonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-189">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-190">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-190">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-191">чекксерверцертификатеревокатион</span><span class="sxs-lookup"><span data-stu-id="a72b1-191">CheckServerCertificateRevocation</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-checkservercertificaterevocation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-192">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-193">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-193">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-194">чекксигнатуресондовнлоадедпрограмс</span><span class="sxs-lookup"><span data-stu-id="a72b1-194">CheckSignaturesOnDownloadedPrograms</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-checksignaturesondownloadedprograms)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-195">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-196">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-196">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-197">консистентмимехандлингинтернетексплорерпроцессес</span><span class="sxs-lookup"><span data-stu-id="a72b1-197">ConsistentMimeHandlingInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-consistentmimehandlinginternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-198">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-199">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-199">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-200">дисаблеадобефлаш</span><span class="sxs-lookup"><span data-stu-id="a72b1-200">DisableAdobeFlash</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableadobeflash)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-201">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-202">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-202">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a72b1-203">дисаблеблоккингофаутдатедактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="a72b1-203">DisableBlockingOfOutdatedActiveXControls</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-204">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-204">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-205">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-205">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-206">дисаблебипассофсмартскринварнингс</span><span class="sxs-lookup"><span data-stu-id="a72b1-206">DisableBypassOfSmartScreenWarnings</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablebypassofsmartscreenwarnings)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-207">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-208">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-208">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-209">дисаблебипассофсмартскринварнингсабаутункоммонфилес</span><span class="sxs-lookup"><span data-stu-id="a72b1-209">DisableBypassOfSmartScreenWarningsAboutUncommonFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablebypassofsmartscreenwarningsaboutuncommonfiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-210">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-211">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-211">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-212">дисаблеконфигурингхистори</span><span class="sxs-lookup"><span data-stu-id="a72b1-212">DisableConfiguringHistory</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableconfiguringhistory)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-213">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-214">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-214">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-215">дисаблекрашдетектион</span><span class="sxs-lookup"><span data-stu-id="a72b1-215">DisableCrashDetection</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablecrashdetection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-216">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-216">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-217">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-217">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-218">дисаблекустомерекспериенцеимпровементпрогрампартиЦипатион</span><span class="sxs-lookup"><span data-stu-id="a72b1-218">DisableCustomerExperienceImprovementProgramParticipation</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablecustomerexperienceimprovementprogramparticipation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-219">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-220">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-220">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-221">дисабледелетингусервиситедвебситес</span><span class="sxs-lookup"><span data-stu-id="a72b1-221">DisableDeletingUserVisitedWebsites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disabledeletinguservisitedwebsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-222">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-223">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-223">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-224">дисаблинклосуредовнлоадинг</span><span class="sxs-lookup"><span data-stu-id="a72b1-224">DisableEnclosureDownloading</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableenclosuredownloading)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-225">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-226">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-226">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-227">дисаблинкриптионсуппорт</span><span class="sxs-lookup"><span data-stu-id="a72b1-227">DisableEncryptionSupport</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableencryptionsupport)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-228">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-228">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-229">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-229">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-230">дисаблефирструнвизард</span><span class="sxs-lookup"><span data-stu-id="a72b1-230">DisableFirstRunWizard</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablefirstrunwizard)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-231">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-231">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-232">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-232">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-233">дисаблефлипахеадфеатуре</span><span class="sxs-lookup"><span data-stu-id="a72b1-233">DisableFlipAheadFeature</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableflipaheadfeature)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-234">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-234">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-235">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-235">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-236">дисаблехомепажечанже</span><span class="sxs-lookup"><span data-stu-id="a72b1-236">DisableHomePageChange</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablehomepagechange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-237">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-237">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-238">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-238">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-239">дисаблеигнорингцертификатиррорс</span><span class="sxs-lookup"><span data-stu-id="a72b1-239">DisableIgnoringCertificateErrors</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableignoringcertificateerrors)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-240">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-240">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-241">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-241">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-242">дисаблеинприватебровсинг</span><span class="sxs-lookup"><span data-stu-id="a72b1-242">DisableInPrivateBrowsing</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableinprivatebrowsing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-243">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-243">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-244">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-244">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-245">дисаблепроцессесиненханцедпротектедмоде</span><span class="sxs-lookup"><span data-stu-id="a72b1-245">DisableProcessesInEnhancedProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableprocessesinenhancedprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-246">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-246">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-247">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-247">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-248">дисаблепроксичанже</span><span class="sxs-lookup"><span data-stu-id="a72b1-248">DisableProxyChange</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableproxychange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-249">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-250">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-250">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-251">дисаблесеарчпровидерчанже</span><span class="sxs-lookup"><span data-stu-id="a72b1-251">DisableSearchProviderChange</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablesearchproviderchange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-252">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-253">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-253">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-254">дисаблесекондарихомепажечанже</span><span class="sxs-lookup"><span data-stu-id="a72b1-254">DisableSecondaryHomePageChange</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablesecondaryhomepagechange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-255">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-255">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-256">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-256">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-257">дисаблесекуритисеттингсчекк</span><span class="sxs-lookup"><span data-stu-id="a72b1-257">DisableSecuritySettingsCheck</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablesecuritysettingscheck)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-258">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-259">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-259">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-260">доноталловактивексконтролсинпротектедмоде</span><span class="sxs-lookup"><span data-stu-id="a72b1-260">DoNotAllowActiveXControlsInProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-donotallowactivexcontrolsinprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-261">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-262">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-262">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-263">донотблоккаутдатедактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="a72b1-263">DoNotBlockOutdatedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-donotblockoutdatedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-264">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-265">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-265">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-266">донотблоккаутдатедактивексконтролсонспеЦификдомаинс</span><span class="sxs-lookup"><span data-stu-id="a72b1-266">DoNotBlockOutdatedActiveXControlsOnSpecificDomains</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-donotblockoutdatedactivexcontrolsonspecificdomains)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-267">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-267">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-268">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-268">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-269">инклудеалллокалситес</span><span class="sxs-lookup"><span data-stu-id="a72b1-269">IncludeAllLocalSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-includealllocalsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-270">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-270">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-271">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-271">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-272">инклудеаллнетворкпасс</span><span class="sxs-lookup"><span data-stu-id="a72b1-272">IncludeAllNetworkPaths</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-includeallnetworkpaths)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-273">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-273">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-274">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-274">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a72b1-275">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="a72b1-275">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-276">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-276">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-277">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a72b1-277">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-278">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a72b1-278">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-279">интернетзонеалловакцесстодатасаурцес</span><span class="sxs-lookup"><span data-stu-id="a72b1-279">InternetZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-280">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-280">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-281">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-281">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-282">интернетзонеалловаутоматикпромптингфорактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="a72b1-282">InternetZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-283">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-283">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-284">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-284">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-285">интернетзонеалловаутоматикпромптингфорфиледовнлоадс</span><span class="sxs-lookup"><span data-stu-id="a72b1-285">InternetZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-286">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-286">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-287">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-287">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-288">интернетзонеалловкопипастевиаскрипт</span><span class="sxs-lookup"><span data-stu-id="a72b1-288">InternetZoneAllowCopyPasteViaScript</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowcopypasteviascript)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-289">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-289">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-290">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-290">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-291">интернетзонеалловдраганддропкопяндпастефилес</span><span class="sxs-lookup"><span data-stu-id="a72b1-291">InternetZoneAllowDragAndDropCopyAndPasteFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowdraganddropcopyandpastefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-292">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-292">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-293">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-293">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-294">интернетзонеалловфонтдовнлоадс</span><span class="sxs-lookup"><span data-stu-id="a72b1-294">InternetZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-295">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-295">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-296">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-296">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-297">интернетзонеалловлесспривилежедситес</span><span class="sxs-lookup"><span data-stu-id="a72b1-297">InternetZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-298">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-298">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-299">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-299">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-300">интернетзонеалловлоадингофксамлфилес</span><span class="sxs-lookup"><span data-stu-id="a72b1-300">InternetZoneAllowLoadingOfXAMLFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowloadingofxamlfiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-301">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-301">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-302">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-302">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-303">интернетзонеалловнетфрамеворкрелианткомпонентс</span><span class="sxs-lookup"><span data-stu-id="a72b1-303">InternetZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-304">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-304">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-305">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-305">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-306">интернетзонеалловонляппроведдомаинстаусеактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="a72b1-306">InternetZoneAllowOnlyApprovedDomainsToUseActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowonlyapproveddomainstouseactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-307">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-308">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-308">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-309">интернетзонеалловонляппроведдомаинстаусетдкактивексконтрол</span><span class="sxs-lookup"><span data-stu-id="a72b1-309">InternetZoneAllowOnlyApprovedDomainsToUseTDCActiveXControl</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowonlyapproveddomainstousetdcactivexcontrol)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-310">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-310">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-311">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-311">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-312">интернетзонеалловскриптингофинтернетексплорервеббровсерконтролс</span><span class="sxs-lookup"><span data-stu-id="a72b1-312">InternetZoneAllowScriptingOfInternetExplorerWebBrowserControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowscriptingofinternetexplorerwebbrowsercontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-313">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-313">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-314">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-314">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-315">интернетзонеалловскриптинитиатедвиндовс</span><span class="sxs-lookup"><span data-stu-id="a72b1-315">InternetZoneAllowScriptInitiatedWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowscriptinitiatedwindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-316">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-316">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-317">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-317">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-318">интернетзонеалловскриптлетс</span><span class="sxs-lookup"><span data-stu-id="a72b1-318">InternetZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-319">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-319">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-320">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-320">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-321">интернетзонеалловсмартскриние</span><span class="sxs-lookup"><span data-stu-id="a72b1-321">InternetZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-322">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-322">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-323">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-323">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-324">интернетзонеалловупдатестостатусбарвиаскрипт</span><span class="sxs-lookup"><span data-stu-id="a72b1-324">InternetZoneAllowUpdatesToStatusBarViaScript</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowupdatestostatusbarviascript)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-325">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-325">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-326">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-326">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-327">интернетзонеалловусердатаперсистенце</span><span class="sxs-lookup"><span data-stu-id="a72b1-327">InternetZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-328">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-328">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-329">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-329">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-330">интернетзонедонотрунантималвареагаинстактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="a72b1-330">InternetZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-331">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-331">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-332">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-332">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-333">интернетзонедовнлоадсигнедактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="a72b1-333">InternetZoneDownloadSignedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonedownloadsignedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-334">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-334">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-335">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-335">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-336">интернетзонедовнлоадунсигнедактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="a72b1-336">InternetZoneDownloadUnsignedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonedownloadunsignedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-337">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-337">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-338">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-338">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-339">интернетзонинаблекроссситескриптингфилтер</span><span class="sxs-lookup"><span data-stu-id="a72b1-339">InternetZoneEnableCrossSiteScriptingFilter</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenablecrosssitescriptingfilter)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-340">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-340">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-341">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-341">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-342">интернетзонинабледраггингофконтентфромдифферентдомаинсакроссвиндовс</span><span class="sxs-lookup"><span data-stu-id="a72b1-342">InternetZoneEnableDraggingOfContentFromDifferentDomainsAcrossWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenabledraggingofcontentfromdifferentdomainsacrosswindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-343">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-343">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-344">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-344">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-345">интернетзонинабледраггингофконтентфромдифферентдомаинсвисинвиндовс</span><span class="sxs-lookup"><span data-stu-id="a72b1-345">InternetZoneEnableDraggingOfContentFromDifferentDomainsWithinWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenabledraggingofcontentfromdifferentdomainswithinwindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-346">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-346">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-347">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-347">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-348">интернетзонинаблемимесниффинг</span><span class="sxs-lookup"><span data-stu-id="a72b1-348">InternetZoneEnableMIMESniffing</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenablemimesniffing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-349">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-349">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-350">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-350">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-351">интернетзонинаблепротектедмоде</span><span class="sxs-lookup"><span data-stu-id="a72b1-351">InternetZoneEnableProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenableprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-352">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-352">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-353">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-353">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-354">интернетзонеинклуделокалпасвхенуплоадингфилестосервер</span><span class="sxs-lookup"><span data-stu-id="a72b1-354">InternetZoneIncludeLocalPathWhenUploadingFilesToServer</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneincludelocalpathwhenuploadingfilestoserver)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-355">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-355">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-356">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-356">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-357">интернетзонеинитиализеандскриптактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="a72b1-357">InternetZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-358">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-358">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-359">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-359">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-360">интернетзонежавапермиссионс</span><span class="sxs-lookup"><span data-stu-id="a72b1-360">InternetZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-361">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-361">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-362">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-362">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-363">интернетзонелаунчингаппликатионсандфилесинифраме</span><span class="sxs-lookup"><span data-stu-id="a72b1-363">InternetZoneLaunchingApplicationsAndFilesInIFRAME</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonelaunchingapplicationsandfilesiniframe)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-364">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-364">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-365">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-365">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-366">интернетзонелогоноптионс</span><span class="sxs-lookup"><span data-stu-id="a72b1-366">InternetZoneLogonOptions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonelogonoptions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-367">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-367">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-368">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-368">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-369">интернетзоненавигатевиндовсандфрамес</span><span class="sxs-lookup"><span data-stu-id="a72b1-369">InternetZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-370">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-370">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-371">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-371">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a72b1-372">интернетзонеруннетфрамеворкрелианткомпонентснотсигнедвисаусентикоде</span><span class="sxs-lookup"><span data-stu-id="a72b1-372">InternetZoneRunNETFrameworkReliantComponentsNotSignedWithAuthenticode</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-373">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-373">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-374">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-374">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-375">интернетзонеруннетфрамеворкрелианткомпонентссигнедвисаусентикоде</span><span class="sxs-lookup"><span data-stu-id="a72b1-375">InternetZoneRunNETFrameworkReliantComponentsSignedWithAuthenticode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonerunnetframeworkreliantcomponentssignedwithauthenticode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-376">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-376">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-377">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-377">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-378">интернетзонешовсекуритиварнингфорпотентиаллюнсафефилес</span><span class="sxs-lookup"><span data-stu-id="a72b1-378">InternetZoneShowSecurityWarningForPotentiallyUnsafeFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneshowsecuritywarningforpotentiallyunsafefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-379">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-379">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-380">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-380">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-381">интернетзонеусепопупблоккер</span><span class="sxs-lookup"><span data-stu-id="a72b1-381">InternetZoneUsePopupBlocker</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneusepopupblocker)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-382">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-382">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-383">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-383">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a72b1-384">интернетзоневебситесинлесспривилежедзонесканнавигатеинтосисзоне</span><span class="sxs-lookup"><span data-stu-id="a72b1-384">InternetZoneWebsitesInLessPrivilegedZonesCanNavigateIntoThisZone</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-385">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-385">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-386">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-386">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-387">интранетзонеалловакцесстодатасаурцес</span><span class="sxs-lookup"><span data-stu-id="a72b1-387">IntranetZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-388">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-388">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-389">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-389">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-390">интранетзонеалловаутоматикпромптингфорактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="a72b1-390">IntranetZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-391">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-391">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-392">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-392">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-393">интранетзонеалловаутоматикпромптингфорфиледовнлоадс</span><span class="sxs-lookup"><span data-stu-id="a72b1-393">IntranetZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-394">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-394">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-395">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-395">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-396">интранетзонеалловфонтдовнлоадс</span><span class="sxs-lookup"><span data-stu-id="a72b1-396">IntranetZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-397">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-397">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-398">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-398">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-399">интранетзонеалловлесспривилежедситес</span><span class="sxs-lookup"><span data-stu-id="a72b1-399">IntranetZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-400">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-400">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-401">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-401">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-402">интранетзонеалловнетфрамеворкрелианткомпонентс</span><span class="sxs-lookup"><span data-stu-id="a72b1-402">IntranetZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-403">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-403">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-404">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-404">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-405">интранетзонеалловскриптлетс</span><span class="sxs-lookup"><span data-stu-id="a72b1-405">IntranetZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-406">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-406">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-407">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-407">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-408">интранетзонеалловсмартскриние</span><span class="sxs-lookup"><span data-stu-id="a72b1-408">IntranetZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-409">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-409">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-410">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-410">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-411">интранетзонеалловусердатаперсистенце</span><span class="sxs-lookup"><span data-stu-id="a72b1-411">IntranetZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-412">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-412">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-413">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-413">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-414">интранетзонедонотрунантималвареагаинстактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="a72b1-414">IntranetZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-415">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-415">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-416">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-416">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-417">интранетзонеинитиализеандскриптактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="a72b1-417">IntranetZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-418">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-418">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-419">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-419">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a72b1-420">интранетзонеинитиализеандскриптактивексконтролснотмаркедсафе</span><span class="sxs-lookup"><span data-stu-id="a72b1-420">IntranetZoneInitializeAndScriptActiveXControlsNotMarkedSafe</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-421">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-421">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-422">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-422">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-423">интранетзонежавапермиссионс</span><span class="sxs-lookup"><span data-stu-id="a72b1-423">IntranetZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-424">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-424">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-425">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-425">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-426">интранетзоненавигатевиндовсандфрамес</span><span class="sxs-lookup"><span data-stu-id="a72b1-426">IntranetZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-427">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-427">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-428">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-428">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-429">локалмачинезонеалловакцесстодатасаурцес</span><span class="sxs-lookup"><span data-stu-id="a72b1-429">LocalMachineZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-430">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-430">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-431">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-431">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-432">локалмачинезонеалловаутоматикпромптингфорактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="a72b1-432">LocalMachineZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-433">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-433">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-434">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-434">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-435">локалмачинезонеалловаутоматикпромптингфорфиледовнлоадс</span><span class="sxs-lookup"><span data-stu-id="a72b1-435">LocalMachineZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-436">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-436">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-437">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-437">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-438">локалмачинезонеалловфонтдовнлоадс</span><span class="sxs-lookup"><span data-stu-id="a72b1-438">LocalMachineZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-439">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-439">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-440">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-440">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-441">локалмачинезонеалловлесспривилежедситес</span><span class="sxs-lookup"><span data-stu-id="a72b1-441">LocalMachineZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-442">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-442">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-443">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-443">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-444">локалмачинезонеалловнетфрамеворкрелианткомпонентс</span><span class="sxs-lookup"><span data-stu-id="a72b1-444">LocalMachineZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-445">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-445">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-446">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-446">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-447">локалмачинезонеалловскриптлетс</span><span class="sxs-lookup"><span data-stu-id="a72b1-447">LocalMachineZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-448">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-448">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-449">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-449">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-450">локалмачинезонеалловсмартскриние</span><span class="sxs-lookup"><span data-stu-id="a72b1-450">LocalMachineZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-451">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-451">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-452">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-452">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-453">локалмачинезонеалловусердатаперсистенце</span><span class="sxs-lookup"><span data-stu-id="a72b1-453">LocalMachineZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-454">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-454">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-455">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-455">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-456">локалмачинезонедонотрунантималвареагаинстактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="a72b1-456">LocalMachineZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-457">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-457">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-458">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-458">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-459">локалмачинезонеинитиализеандскриптактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="a72b1-459">LocalMachineZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-460">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-460">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-461">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-461">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-462">локалмачинезонежавапермиссионс</span><span class="sxs-lookup"><span data-stu-id="a72b1-462">LocalMachineZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-463">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-463">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-464">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-464">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-465">локалмачинезоненавигатевиндовсандфрамес</span><span class="sxs-lookup"><span data-stu-id="a72b1-465">LocalMachineZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-466">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-466">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-467">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-467">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-468">локкеддовнинтернетзонеалловакцесстодатасаурцес</span><span class="sxs-lookup"><span data-stu-id="a72b1-468">LockedDownInternetZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-469">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-469">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-470">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-470">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-471">локкеддовнинтернетзонеалловаутоматикпромптингфорактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="a72b1-471">LockedDownInternetZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-472">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-472">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-473">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-473">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-474">локкеддовнинтернетзонеалловаутоматикпромптингфорфиледовнлоадс</span><span class="sxs-lookup"><span data-stu-id="a72b1-474">LockedDownInternetZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-475">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-475">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-476">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-476">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-477">локкеддовнинтернетзонеалловфонтдовнлоадс</span><span class="sxs-lookup"><span data-stu-id="a72b1-477">LockedDownInternetZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-478">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-478">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-479">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-479">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-480">локкеддовнинтернетзонеалловлесспривилежедситес</span><span class="sxs-lookup"><span data-stu-id="a72b1-480">LockedDownInternetZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-481">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-481">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-482">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-482">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-483">локкеддовнинтернетзонеалловнетфрамеворкрелианткомпонентс</span><span class="sxs-lookup"><span data-stu-id="a72b1-483">LockedDownInternetZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-484">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-484">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-485">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-485">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-486">локкеддовнинтернетзонеалловскриптлетс</span><span class="sxs-lookup"><span data-stu-id="a72b1-486">LockedDownInternetZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-487">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-487">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-488">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-488">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-489">локкеддовнинтернетзонеалловсмартскриние</span><span class="sxs-lookup"><span data-stu-id="a72b1-489">LockedDownInternetZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-490">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-490">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-491">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-491">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-492">локкеддовнинтернетзонеалловусердатаперсистенце</span><span class="sxs-lookup"><span data-stu-id="a72b1-492">LockedDownInternetZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-493">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-493">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-494">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-494">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-495">локкеддовнинтернетзонеинитиализеандскриптактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="a72b1-495">LockedDownInternetZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-496">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-496">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-497">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-497">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-498">локкеддовнинтернетзонежавапермиссионс</span><span class="sxs-lookup"><span data-stu-id="a72b1-498">LockedDownInternetZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-499">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-499">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-500">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-500">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-501">локкеддовнинтернетзоненавигатевиндовсандфрамес</span><span class="sxs-lookup"><span data-stu-id="a72b1-501">LockedDownInternetZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-502">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-502">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-503">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-503">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-504">локкеддовнинтранетзонеалловакцесстодатасаурцес</span><span class="sxs-lookup"><span data-stu-id="a72b1-504">LockedDownIntranetZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-505">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-505">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-506">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-506">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-507">локкеддовнинтранетзонеалловаутоматикпромптингфорактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="a72b1-507">LockedDownIntranetZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-508">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-508">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-509">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-509">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-510">локкеддовнинтранетзонеалловаутоматикпромптингфорфиледовнлоадс</span><span class="sxs-lookup"><span data-stu-id="a72b1-510">LockedDownIntranetZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-511">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-511">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-512">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-512">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-513">локкеддовнинтранетзонеалловфонтдовнлоадс</span><span class="sxs-lookup"><span data-stu-id="a72b1-513">LockedDownIntranetZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-514">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-514">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-515">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-515">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-516">локкеддовнинтранетзонеалловлесспривилежедситес</span><span class="sxs-lookup"><span data-stu-id="a72b1-516">LockedDownIntranetZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-517">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-517">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-518">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-518">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-519">локкеддовнинтранетзонеалловнетфрамеворкрелианткомпонентс</span><span class="sxs-lookup"><span data-stu-id="a72b1-519">LockedDownIntranetZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-520">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-520">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-521">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-521">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-522">локкеддовнинтранетзонеалловскриптлетс</span><span class="sxs-lookup"><span data-stu-id="a72b1-522">LockedDownIntranetZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-523">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-523">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-524">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-524">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-525">локкеддовнинтранетзонеалловсмартскриние</span><span class="sxs-lookup"><span data-stu-id="a72b1-525">LockedDownIntranetZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-526">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-526">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-527">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-527">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-528">локкеддовнинтранетзонеалловусердатаперсистенце</span><span class="sxs-lookup"><span data-stu-id="a72b1-528">LockedDownIntranetZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-529">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-529">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-530">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-530">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-531">локкеддовнинтранетзонеинитиализеандскриптактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="a72b1-531">LockedDownIntranetZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-532">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-532">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-533">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-533">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-534">локкеддовнинтранетзоненавигатевиндовсандфрамес</span><span class="sxs-lookup"><span data-stu-id="a72b1-534">LockedDownIntranetZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-535">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-535">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-536">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-536">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-537">локкеддовнлокалмачинезонеалловакцесстодатасаурцес</span><span class="sxs-lookup"><span data-stu-id="a72b1-537">LockedDownLocalMachineZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-538">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-538">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-539">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-539">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-540">локкеддовнлокалмачинезонеалловаутоматикпромптингфорактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="a72b1-540">LockedDownLocalMachineZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-541">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-541">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-542">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-542">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-543">локкеддовнлокалмачинезонеалловаутоматикпромптингфорфиледовнлоадс</span><span class="sxs-lookup"><span data-stu-id="a72b1-543">LockedDownLocalMachineZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-544">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-544">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-545">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-545">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-546">локкеддовнлокалмачинезонеалловфонтдовнлоадс</span><span class="sxs-lookup"><span data-stu-id="a72b1-546">LockedDownLocalMachineZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-547">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-547">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-548">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-548">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-549">локкеддовнлокалмачинезонеалловлесспривилежедситес</span><span class="sxs-lookup"><span data-stu-id="a72b1-549">LockedDownLocalMachineZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-550">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-550">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-551">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-551">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-552">локкеддовнлокалмачинезонеалловнетфрамеворкрелианткомпонентс</span><span class="sxs-lookup"><span data-stu-id="a72b1-552">LockedDownLocalMachineZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-553">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-553">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-554">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-554">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-555">локкеддовнлокалмачинезонеалловскриптлетс</span><span class="sxs-lookup"><span data-stu-id="a72b1-555">LockedDownLocalMachineZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-556">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-556">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-557">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-557">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-558">локкеддовнлокалмачинезонеалловсмартскриние</span><span class="sxs-lookup"><span data-stu-id="a72b1-558">LockedDownLocalMachineZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-559">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-559">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-560">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-560">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-561">локкеддовнлокалмачинезонеалловусердатаперсистенце</span><span class="sxs-lookup"><span data-stu-id="a72b1-561">LockedDownLocalMachineZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-562">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-562">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-563">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-563">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-564">локкеддовнлокалмачинезонеинитиализеандскриптактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="a72b1-564">LockedDownLocalMachineZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-565">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-565">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-566">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-566">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-567">локкеддовнлокалмачинезонежавапермиссионс</span><span class="sxs-lookup"><span data-stu-id="a72b1-567">LockedDownLocalMachineZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-568">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-568">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-569">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-569">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-570">локкеддовнлокалмачинезоненавигатевиндовсандфрамес</span><span class="sxs-lookup"><span data-stu-id="a72b1-570">LockedDownLocalMachineZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-571">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-571">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-572">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-572">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-573">локкеддовнрестриктедситесзонеалловакцесстодатасаурцес</span><span class="sxs-lookup"><span data-stu-id="a72b1-573">LockedDownRestrictedSitesZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-574">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-574">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-575">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-575">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-576">локкеддовнрестриктедситесзонеалловаутоматикпромптингфорактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="a72b1-576">LockedDownRestrictedSitesZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-577">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-577">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-578">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-578">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-579">локкеддовнрестриктедситесзонеалловаутоматикпромптингфорфиледовнлоадс</span><span class="sxs-lookup"><span data-stu-id="a72b1-579">LockedDownRestrictedSitesZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-580">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-580">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-581">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-581">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-582">локкеддовнрестриктедситесзонеалловфонтдовнлоадс</span><span class="sxs-lookup"><span data-stu-id="a72b1-582">LockedDownRestrictedSitesZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-583">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-583">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-584">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-584">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-585">локкеддовнрестриктедситесзонеалловлесспривилежедситес</span><span class="sxs-lookup"><span data-stu-id="a72b1-585">LockedDownRestrictedSitesZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-586">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-586">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-587">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-587">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-588">локкеддовнрестриктедситесзонеалловнетфрамеворкрелианткомпонентс</span><span class="sxs-lookup"><span data-stu-id="a72b1-588">LockedDownRestrictedSitesZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-589">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-589">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-590">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-590">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-591">локкеддовнрестриктедситесзонеалловскриптлетс</span><span class="sxs-lookup"><span data-stu-id="a72b1-591">LockedDownRestrictedSitesZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-592">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-592">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-593">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-593">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-594">локкеддовнрестриктедситесзонеалловсмартскриние</span><span class="sxs-lookup"><span data-stu-id="a72b1-594">LockedDownRestrictedSitesZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-595">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-595">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-596">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-596">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-597">локкеддовнрестриктедситесзонеалловусердатаперсистенце</span><span class="sxs-lookup"><span data-stu-id="a72b1-597">LockedDownRestrictedSitesZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-598">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-598">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-599">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-599">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-600">локкеддовнрестриктедситесзонеинитиализеандскриптактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="a72b1-600">LockedDownRestrictedSitesZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-601">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-601">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-602">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-602">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-603">локкеддовнрестриктедситесзонежавапермиссионс</span><span class="sxs-lookup"><span data-stu-id="a72b1-603">LockedDownRestrictedSitesZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-604">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-604">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-605">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-605">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-606">локкеддовнрестриктедситесзоненавигатевиндовсандфрамес</span><span class="sxs-lookup"><span data-stu-id="a72b1-606">LockedDownRestrictedSitesZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-607">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-607">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-608">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-608">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-609">локкеддовнтрустедситесзонеалловакцесстодатасаурцес</span><span class="sxs-lookup"><span data-stu-id="a72b1-609">LockedDownTrustedSitesZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-610">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-610">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-611">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-611">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-612">локкеддовнтрустедситесзонеалловаутоматикпромптингфорактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="a72b1-612">LockedDownTrustedSitesZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-613">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-613">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-614">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-614">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-615">локкеддовнтрустедситесзонеалловаутоматикпромптингфорфиледовнлоадс</span><span class="sxs-lookup"><span data-stu-id="a72b1-615">LockedDownTrustedSitesZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-616">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-616">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-617">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-617">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-618">локкеддовнтрустедситесзонеалловфонтдовнлоадс</span><span class="sxs-lookup"><span data-stu-id="a72b1-618">LockedDownTrustedSitesZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-619">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-619">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-620">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-620">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-621">локкеддовнтрустедситесзонеалловлесспривилежедситес</span><span class="sxs-lookup"><span data-stu-id="a72b1-621">LockedDownTrustedSitesZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-622">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-622">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-623">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-623">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-624">локкеддовнтрустедситесзонеалловнетфрамеворкрелианткомпонентс</span><span class="sxs-lookup"><span data-stu-id="a72b1-624">LockedDownTrustedSitesZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-625">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-625">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-626">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-626">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-627">локкеддовнтрустедситесзонеалловскриптлетс</span><span class="sxs-lookup"><span data-stu-id="a72b1-627">LockedDownTrustedSitesZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-628">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-628">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-629">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-629">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-630">локкеддовнтрустедситесзонеалловсмартскриние</span><span class="sxs-lookup"><span data-stu-id="a72b1-630">LockedDownTrustedSitesZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-631">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-631">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-632">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-632">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-633">локкеддовнтрустедситесзонеалловусердатаперсистенце</span><span class="sxs-lookup"><span data-stu-id="a72b1-633">LockedDownTrustedSitesZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-634">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-634">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-635">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-635">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-636">локкеддовнтрустедситесзонеинитиализеандскриптактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="a72b1-636">LockedDownTrustedSitesZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-637">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-637">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-638">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-638">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-639">локкеддовнтрустедситесзонежавапермиссионс</span><span class="sxs-lookup"><span data-stu-id="a72b1-639">LockedDownTrustedSitesZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-640">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-640">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-641">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-641">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-642">локкеддовнтрустедситесзоненавигатевиндовсандфрамес</span><span class="sxs-lookup"><span data-stu-id="a72b1-642">LockedDownTrustedSitesZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-643">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-643">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-644">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-644">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-645">мимесниффингсафетифеатуреинтернетексплорерпроцессес</span><span class="sxs-lookup"><span data-stu-id="a72b1-645">MimeSniffingSafetyFeatureInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-mimesniffingsafetyfeatureinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-646">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-646">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-647">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-647">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-648">мкпротоколсекуритирестриктионинтернетексплорерпроцессес</span><span class="sxs-lookup"><span data-stu-id="a72b1-648">MKProtocolSecurityRestrictionInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-mkprotocolsecurityrestrictioninternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-649">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-649">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-650">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-650">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-651">нотификатионбаринтернетексплорерпроцессес</span><span class="sxs-lookup"><span data-stu-id="a72b1-651">NotificationBarInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-notificationbarinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-652">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-652">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-653">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-653">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a72b1-654">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="a72b1-654">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-655">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-655">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-656">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a72b1-656">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-657">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a72b1-657">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-658">превентманагингсмартскринфилтер</span><span class="sxs-lookup"><span data-stu-id="a72b1-658">PreventManagingSmartScreenFilter</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-preventmanagingsmartscreenfilter)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-659">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-659">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-660">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-660">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-661">превентперусеринсталлатионофактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="a72b1-661">PreventPerUserInstallationOfActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-preventperuserinstallationofactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-662">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-662">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-663">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-663">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-664">протектионфромзонилеватионинтернетексплорерпроцессес</span><span class="sxs-lookup"><span data-stu-id="a72b1-664">ProtectionFromZoneElevationInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-protectionfromzoneelevationinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-665">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-665">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-666">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-666">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-667">ремоверунсистимебуттонфораутдатедактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="a72b1-667">RemoveRunThisTimeButtonForOutdatedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-removerunthistimebuttonforoutdatedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-668">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-668">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-669">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-669">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-670">рестриктактивексинсталлинтернетексплорерпроцессес</span><span class="sxs-lookup"><span data-stu-id="a72b1-670">RestrictActiveXInstallInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictactivexinstallinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-671">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-671">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-672">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-672">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-673">рестриктедситесзонеалловакцесстодатасаурцес</span><span class="sxs-lookup"><span data-stu-id="a72b1-673">RestrictedSitesZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-674">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-674">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-675">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-675">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-676">рестриктедситесзонеалловактивескриптинг</span><span class="sxs-lookup"><span data-stu-id="a72b1-676">RestrictedSitesZoneAllowActiveScripting</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowactivescripting)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-677">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-677">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-678">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-678">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-679">рестриктедситесзонеалловаутоматикпромптингфорактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="a72b1-679">RestrictedSitesZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-680">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-680">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-681">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-681">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-682">рестриктедситесзонеалловаутоматикпромптингфорфиледовнлоадс</span><span class="sxs-lookup"><span data-stu-id="a72b1-682">RestrictedSitesZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-683">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-683">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-684">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-684">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-685">рестриктедситесзонеалловбинаряндскриптбехавиорс</span><span class="sxs-lookup"><span data-stu-id="a72b1-685">RestrictedSitesZoneAllowBinaryAndScriptBehaviors</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowbinaryandscriptbehaviors)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-686">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-686">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-687">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-687">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-688">рестриктедситесзонеалловкопипастевиаскрипт</span><span class="sxs-lookup"><span data-stu-id="a72b1-688">RestrictedSitesZoneAllowCopyPasteViaScript</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowcopypasteviascript)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-689">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-689">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-690">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-690">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-691">рестриктедситесзонеалловдраганддропкопяндпастефилес</span><span class="sxs-lookup"><span data-stu-id="a72b1-691">RestrictedSitesZoneAllowDragAndDropCopyAndPasteFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowdraganddropcopyandpastefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-692">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-692">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-693">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-693">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-694">рестриктедситесзонеалловфиледовнлоадс</span><span class="sxs-lookup"><span data-stu-id="a72b1-694">RestrictedSitesZoneAllowFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-695">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-695">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-696">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-696">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-697">рестриктедситесзонеалловфонтдовнлоадс</span><span class="sxs-lookup"><span data-stu-id="a72b1-697">RestrictedSitesZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-698">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-698">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-699">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-699">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-700">рестриктедситесзонеалловлесспривилежедситес</span><span class="sxs-lookup"><span data-stu-id="a72b1-700">RestrictedSitesZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-701">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-701">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-702">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-702">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-703">рестриктедситесзонеалловлоадингофксамлфилес</span><span class="sxs-lookup"><span data-stu-id="a72b1-703">RestrictedSitesZoneAllowLoadingOfXAMLFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowloadingofxamlfiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-704">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-704">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-705">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-705">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-706">рестриктедситесзонеалловметарефреш</span><span class="sxs-lookup"><span data-stu-id="a72b1-706">RestrictedSitesZoneAllowMETAREFRESH</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowmetarefresh)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-707">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-707">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-708">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-708">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-709">рестриктедситесзонеалловнетфрамеворкрелианткомпонентс</span><span class="sxs-lookup"><span data-stu-id="a72b1-709">RestrictedSitesZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-710">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-710">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-711">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-711">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-712">рестриктедситесзонеалловонляппроведдомаинстаусеактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="a72b1-712">RestrictedSitesZoneAllowOnlyApprovedDomainsToUseActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowonlyapproveddomainstouseactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-713">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-713">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-714">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-714">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-715">рестриктедситесзонеалловонляппроведдомаинстаусетдкактивексконтрол</span><span class="sxs-lookup"><span data-stu-id="a72b1-715">RestrictedSitesZoneAllowOnlyApprovedDomainsToUseTDCActiveXControl</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowonlyapproveddomainstousetdcactivexcontrol)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-716">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-716">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-717">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-717">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-718">рестриктедситесзонеалловскриптингофинтернетексплорервеббровсерконтролс</span><span class="sxs-lookup"><span data-stu-id="a72b1-718">RestrictedSitesZoneAllowScriptingOfInternetExplorerWebBrowserControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowscriptingofinternetexplorerwebbrowsercontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-719">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-719">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-720">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-720">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-721">рестриктедситесзонеалловскриптинитиатедвиндовс</span><span class="sxs-lookup"><span data-stu-id="a72b1-721">RestrictedSitesZoneAllowScriptInitiatedWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowscriptinitiatedwindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-722">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-722">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-723">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-723">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-724">рестриктедситесзонеалловскриптлетс</span><span class="sxs-lookup"><span data-stu-id="a72b1-724">RestrictedSitesZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-725">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-725">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-726">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-726">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-727">рестриктедситесзонеалловсмартскриние</span><span class="sxs-lookup"><span data-stu-id="a72b1-727">RestrictedSitesZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-728">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-728">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-729">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-729">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-730">рестриктедситесзонеалловупдатестостатусбарвиаскрипт</span><span class="sxs-lookup"><span data-stu-id="a72b1-730">RestrictedSitesZoneAllowUpdatesToStatusBarViaScript</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowupdatestostatusbarviascript)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-731">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-731">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-732">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-732">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-733">рестриктедситесзонеалловусердатаперсистенце</span><span class="sxs-lookup"><span data-stu-id="a72b1-733">RestrictedSitesZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-734">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-734">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-735">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-735">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-736">рестриктедситесзонедонотрунантималвареагаинстактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="a72b1-736">RestrictedSitesZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-737">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-737">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-738">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-738">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-739">рестриктедситесзонедовнлоадсигнедактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="a72b1-739">RestrictedSitesZoneDownloadSignedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonedownloadsignedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-740">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-740">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-741">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-741">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-742">рестриктедситесзонедовнлоадунсигнедактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="a72b1-742">RestrictedSitesZoneDownloadUnsignedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonedownloadunsignedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-743">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-743">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-744">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-744">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-745">рестриктедситесзонинаблекроссситескриптингфилтер</span><span class="sxs-lookup"><span data-stu-id="a72b1-745">RestrictedSitesZoneEnableCrossSiteScriptingFilter</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneenablecrosssitescriptingfilter)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-746">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-746">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-747">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-747">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-748">рестриктедситесзонинабледраггингофконтентфромдифферентдомаинсакроссвиндовс</span><span class="sxs-lookup"><span data-stu-id="a72b1-748">RestrictedSitesZoneEnableDraggingOfContentFromDifferentDomainsAcrossWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneenabledraggingofcontentfromdifferentdomainsacrosswindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-749">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-749">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-750">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-750">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-751">рестриктедситесзонинабледраггингофконтентфромдифферентдомаинсвисинвиндовс</span><span class="sxs-lookup"><span data-stu-id="a72b1-751">RestrictedSitesZoneEnableDraggingOfContentFromDifferentDomainsWithinWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneenabledraggingofcontentfromdifferentdomainswithinwindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-752">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-752">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-753">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-753">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-754">рестриктедситесзонинаблемимесниффинг</span><span class="sxs-lookup"><span data-stu-id="a72b1-754">RestrictedSitesZoneEnableMIMESniffing</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneenablemimesniffing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-755">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-755">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-756">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-756">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-757">рестриктедситесзонеинклуделокалпасвхенуплоадингфилестосервер</span><span class="sxs-lookup"><span data-stu-id="a72b1-757">RestrictedSitesZoneIncludeLocalPathWhenUploadingFilesToServer</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneincludelocalpathwhenuploadingfilestoserver)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-758">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-758">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-759">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-759">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-760">рестриктедситесзонеинитиализеандскриптактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="a72b1-760">RestrictedSitesZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-761">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-761">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-762">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-762">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-763">рестриктедситесзонежавапермиссионс</span><span class="sxs-lookup"><span data-stu-id="a72b1-763">RestrictedSitesZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-764">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-764">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-765">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-765">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-766">рестриктедситесзонелаунчингаппликатионсандфилесинифраме</span><span class="sxs-lookup"><span data-stu-id="a72b1-766">RestrictedSitesZoneLaunchingApplicationsAndFilesInIFRAME</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonelaunchingapplicationsandfilesiniframe)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-767">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-767">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-768">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-768">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-769">рестриктедситесзонелогоноптионс</span><span class="sxs-lookup"><span data-stu-id="a72b1-769">RestrictedSitesZoneLogonOptions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonelogonoptions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-770">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-770">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-771">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-771">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-772">рестриктедситесзоненавигатевиндовсандфрамес</span><span class="sxs-lookup"><span data-stu-id="a72b1-772">RestrictedSitesZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-773">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-773">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-774">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-774">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a72b1-775">рестриктедситесзоненавигатевиндовсандфрамесакроссдомаинс</span><span class="sxs-lookup"><span data-stu-id="a72b1-775">RestrictedSitesZoneNavigateWindowsAndFramesAcrossDomains</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-776">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-776">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-777">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-777">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-778">рестриктедситесзонерунактивексконтролсандплугинс</span><span class="sxs-lookup"><span data-stu-id="a72b1-778">RestrictedSitesZoneRunActiveXControlsAndPlugins</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonerunactivexcontrolsandplugins)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-779">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-779">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-780">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-780">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-781">рестриктедситесзонеруннетфрамеворкрелианткомпонентссигнедвисаусентикоде</span><span class="sxs-lookup"><span data-stu-id="a72b1-781">RestrictedSitesZoneRunNETFrameworkReliantComponentsSignedWithAuthenticode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonerunnetframeworkreliantcomponentssignedwithauthenticode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-782">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-782">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-783">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-783">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-784">рестриктедситесзонескриптактивексконтролсмаркедсафефорскриптинг</span><span class="sxs-lookup"><span data-stu-id="a72b1-784">RestrictedSitesZoneScriptActiveXControlsMarkedSafeForScripting</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonescriptactivexcontrolsmarkedsafeforscripting)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-785">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-785">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-786">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-786">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-787">рестриктедситесзонескриптингофжаваапплетс</span><span class="sxs-lookup"><span data-stu-id="a72b1-787">RestrictedSitesZoneScriptingOfJavaApplets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonescriptingofjavaapplets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-788">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-788">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-789">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-789">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-790">рестриктедситесзонешовсекуритиварнингфорпотентиаллюнсафефилес</span><span class="sxs-lookup"><span data-stu-id="a72b1-790">RestrictedSitesZoneShowSecurityWarningForPotentiallyUnsafeFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneshowsecuritywarningforpotentiallyunsafefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-791">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-791">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-792">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-792">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a72b1-793">рестриктедситесзонетурнонкроссситескриптингфилтер</span><span class="sxs-lookup"><span data-stu-id="a72b1-793">RestrictedSitesZoneTurnOnCrossSiteScriptingFilter</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-794">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-794">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-795">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-795">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-796">рестриктедситесзонетурнонпротектедмоде</span><span class="sxs-lookup"><span data-stu-id="a72b1-796">RestrictedSitesZoneTurnOnProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneturnonprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-797">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-797">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-798">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-798">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-799">рестриктедситесзонеусепопупблоккер</span><span class="sxs-lookup"><span data-stu-id="a72b1-799">RestrictedSitesZoneUsePopupBlocker</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneusepopupblocker)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-800">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-800">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-801">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-801">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-802">рестриктфиледовнлоадинтернетексплорерпроцессес</span><span class="sxs-lookup"><span data-stu-id="a72b1-802">RestrictFileDownloadInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictfiledownloadinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-803">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-803">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-804">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-804">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-805">скриптедвиндовсекуритирестриктионсинтернетексплорерпроцессес</span><span class="sxs-lookup"><span data-stu-id="a72b1-805">ScriptedWindowSecurityRestrictionsInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-scriptedwindowsecurityrestrictionsinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-806">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-806">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-807">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-807">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-808">SearchProviderList</span><span class="sxs-lookup"><span data-stu-id="a72b1-808">SearchProviderList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-searchproviderlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-809">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-809">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-810">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-810">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-811">спеЦифюсеофактивексинсталлерсервице</span><span class="sxs-lookup"><span data-stu-id="a72b1-811">SpecifyUseOfActiveXInstallerService</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-specifyuseofactivexinstallerservice)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-812">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-812">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-813">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-813">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-814">трустедситесзонеалловакцесстодатасаурцес</span><span class="sxs-lookup"><span data-stu-id="a72b1-814">TrustedSitesZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-815">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-815">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-816">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-816">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-817">трустедситесзонеалловаутоматикпромптингфорактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="a72b1-817">TrustedSitesZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-818">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-818">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-819">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-819">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-820">трустедситесзонеалловаутоматикпромптингфорфиледовнлоадс</span><span class="sxs-lookup"><span data-stu-id="a72b1-820">TrustedSitesZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-821">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-821">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-822">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-822">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-823">трустедситесзонеалловфонтдовнлоадс</span><span class="sxs-lookup"><span data-stu-id="a72b1-823">TrustedSitesZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-824">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-824">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-825">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-825">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-826">трустедситесзонеалловлесспривилежедситес</span><span class="sxs-lookup"><span data-stu-id="a72b1-826">TrustedSitesZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-827">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-827">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-828">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-828">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-829">трустедситесзонеалловнетфрамеворкрелианткомпонентс</span><span class="sxs-lookup"><span data-stu-id="a72b1-829">TrustedSitesZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-830">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-830">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-831">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-831">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-832">трустедситесзонеалловскриптлетс</span><span class="sxs-lookup"><span data-stu-id="a72b1-832">TrustedSitesZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-833">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-833">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-834">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-834">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-835">трустедситесзонеалловсмартскриние</span><span class="sxs-lookup"><span data-stu-id="a72b1-835">TrustedSitesZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-836">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-836">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-837">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-837">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-838">трустедситесзонеалловусердатаперсистенце</span><span class="sxs-lookup"><span data-stu-id="a72b1-838">TrustedSitesZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-839">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-839">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-840">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-840">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-841">трустедситесзонедонотрунантималвареагаинстактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="a72b1-841">TrustedSitesZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-842">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-842">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-843">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-843">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a72b1-844">трустедситесзонедонтрунантималварепрограмсагаинстактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="a72b1-844">TrustedSitesZoneDontRunAntimalwareProgramsAgainstActiveXControls</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-845">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-845">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-846">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-846">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-847">трустедситесзонеинитиализеандскриптактивексконтролс</span><span class="sxs-lookup"><span data-stu-id="a72b1-847">TrustedSitesZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-848">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-848">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-849">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-849">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a72b1-850">трустедситесзонеинитиализеандскриптактивексконтролснотмаркедассафе</span><span class="sxs-lookup"><span data-stu-id="a72b1-850">TrustedSitesZoneInitializeAndScriptActiveXControlsNotMarkedAsSafe</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-851">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-851">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-852">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-852">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a72b1-853">трустедситесзонеинитиализеандскриптактивексконтролснотмаркедсафе</span><span class="sxs-lookup"><span data-stu-id="a72b1-853">TrustedSitesZoneInitializeAndScriptActiveXControlsNotMarkedSafe</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-854">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-854">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-855">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-855">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-856">трустедситесзонежавапермиссионс</span><span class="sxs-lookup"><span data-stu-id="a72b1-856">TrustedSitesZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-857">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-857">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-858">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-858">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a72b1-859">трустедситесзоненавигатевиндовсандфрамес</span><span class="sxs-lookup"><span data-stu-id="a72b1-859">TrustedSitesZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a72b1-860">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a72b1-860">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a72b1-861">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a72b1-861">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a72b1-862">Требования</span><span class="sxs-lookup"><span data-stu-id="a72b1-862">Requirements</span></span>



| <span data-ttu-id="a72b1-863">Требование</span><span class="sxs-lookup"><span data-stu-id="a72b1-863">Requirement</span></span> | <span data-ttu-id="a72b1-864">Значение</span><span class="sxs-lookup"><span data-stu-id="a72b1-864">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a72b1-865">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a72b1-865">Minimum supported client</span></span><br/> | <span data-ttu-id="a72b1-866">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="a72b1-866">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a72b1-867">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a72b1-867">Minimum supported server</span></span><br/> | <span data-ttu-id="a72b1-868">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="a72b1-868">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="a72b1-869">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="a72b1-869">Namespace</span></span><br/>                | <span data-ttu-id="a72b1-870">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="a72b1-870">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="a72b1-871">MOF</span><span class="sxs-lookup"><span data-stu-id="a72b1-871">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a72b1-872"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a72b1-872"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="a72b1-873">DLL</span><span class="sxs-lookup"><span data-stu-id="a72b1-873">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a72b1-874"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a72b1-874"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

