---
title: Класс MDM_Policy_Result01_LocalPoliciesSecurityOptions02
description: '\_Класс политики MDM \_ Result01 \_ LocalPoliciesSecurityOptions02 представляет параметры безопасности локальных политик.'
ms.assetid: 75ac4789-781f-4722-8b0a-33e53b307296
keywords:
- Класс MDM_Policy_Result01_LocalPoliciesSecurityOptions02
- MDM_Policy_Result01_LocalPoliciesSecurityOptions02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_LocalPoliciesSecurityOptions02
- MDM_Policy_Result01_LocalPoliciesSecurityOptions02.InstanceID
- MDM_Policy_Result01_LocalPoliciesSecurityOptions02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f1ece3790bf5a6a6ac51310d04661366bbe9e2a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071508"
---
# <a name="mdm_policy_result01_localpoliciessecurityoptions02-class"></a><span data-ttu-id="15950-105">\_Класс политики MDM \_ Result01 \_ LocalPoliciesSecurityOptions02</span><span class="sxs-lookup"><span data-stu-id="15950-105">MDM\_Policy\_Result01\_LocalPoliciesSecurityOptions02 class</span></span>

<span data-ttu-id="15950-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="15950-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="15950-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="15950-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="15950-108">\_Класс политики MDM \_ Result01 \_ LocalPoliciesSecurityOptions02 представляет параметры безопасности локальных политик.</span><span class="sxs-lookup"><span data-stu-id="15950-108">The MDM\_Policy\_Result01\_LocalPoliciesSecurityOptions02 class represents the local policies security options.</span></span>

<span data-ttu-id="15950-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="15950-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="15950-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="15950-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_LocalPoliciesSecurityOptions02
{
  string InstanceID;
  string ParentID;
  sint32 Accounts_BlockMicrosoftAccounts;
  sint32 Accounts_EnableGuestAccountStatus;
  sint32 Accounts_EnableAdministratorAccountStatus;
  sint32 Accounts_LimitLocalAccountUseOfBlankPasswordsToConsoleLogonOnly;
  string Accounts_RenameAdministratorAccount;
  string Accounts_RenameGuestAccount;
  string Devices_RestrictCDROMAccessToLocallyLoggedOnUserOnly;
  sint32 Devices_PreventUsersFromInstallingPrinterDriversWhenConnectingToSharedPrinters;
  sint32 Devices_AllowUndockWithoutHavingToLogon;
  string Devices_AllowedToFormatAndEjectRemovableMedia;
  sint32 InteractiveLogon_DisplayUserInformationWhenTheSessionIsLocked;
  sint32 Interactivelogon_DoNotDisplayLastSignedIn;
  sint32 Interactivelogon_DoNotDisplayUsernameAtSignIn;
  sint32 Interactivelogon_DoNotRequireCTRLALTDEL;
  sint32 InteractiveLogon_MachineInactivityLimit;
  string InteractiveLogon_MessageTextForUsersAttemptingToLogOn;
  string InteractiveLogon_MessageTitleForUsersAttemptingToLogOn;
  sint32 NetworkAccess_DoNotAllowAnonymousEnumerationOfSAMAccountsAndShares;
  sint32 NetworkAccess_RestrictAnonymousAccessToNamedPipesAndShares;
  string NetworkAccess_RestrictClientsAllowedToMakeRemoteCallsToSAM;
  sint32 NetworkSecurity_AllowPKU2UAuthenticationRequests;
  sint32 RecoveryConsole_AllowAutomaticAdministrativeLogon;
  sint32 Shutdown_AllowSystemToBeShutDownWithoutHavingToLogOn;
  sint32 Shutdown_ClearVirtualMemoryPageFile;
  sint32 UserAccountControl_AllowUIAccessApplicationsToPromptForElevation;
  sint32 UserAccountControl_BehaviorOfTheElevationPromptForAdministrators;
  sint32 UserAccountControl_BehaviorOfTheElevationPromptForStandardUsers;
  sint32 UserAccountControl_DetectApplicationInstallationsAndPromptForElevation;
  sint32 UserAccountControl_OnlyElevateExecutableFilesThatAreSignedAndValidated;
  sint32 UserAccountControl_OnlyElevateUIAccessApplicationsThatAreInstalledInSecureLocations;
  sint32 UserAccountControl_RunAllAdministratorsInAdminApprovalMode;
  sint32 UserAccountControl_SwitchToTheSecureDesktopWhenPromptingForElevation;
  sint32 UserAccountControl_UseAdminApprovalMode;
  sint32 UserAccountControl_VirtualizeFileAndRegistryWriteFailuresToPerUserLocations;
};
```

## <a name="members"></a><span data-ttu-id="15950-111">Члены</span><span class="sxs-lookup"><span data-stu-id="15950-111">Members</span></span>

<span data-ttu-id="15950-112">Класс **\_ политики MDM \_ Result01 \_ LocalPoliciesSecurityOptions02** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="15950-112">The **MDM\_Policy\_Result01\_LocalPoliciesSecurityOptions02** class has these types of members:</span></span>

-   [<span data-ttu-id="15950-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="15950-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="15950-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="15950-114">Properties</span></span>

<span data-ttu-id="15950-115">Класс **\_ политики MDM \_ Result01 \_ LocalPoliciesSecurityOptions02** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="15950-115">The **MDM\_Policy\_Result01\_LocalPoliciesSecurityOptions02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="15950-116">Блоккмикрософтаккаунтс учетных записей \_</span><span class="sxs-lookup"><span data-stu-id="15950-116">Accounts\_BlockMicrosoftAccounts</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-accounts-blockmicrosoftaccounts)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15950-117">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="15950-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="15950-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="15950-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="15950-119">Accounts_EnableAdministratorAccountStatus</span><span class="sxs-lookup"><span data-stu-id="15950-119">Accounts_EnableAdministratorAccountStatus</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15950-120">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="15950-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="15950-121">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="15950-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="15950-122">Accounts_EnableGuestAccountStatus</span><span class="sxs-lookup"><span data-stu-id="15950-122">Accounts_EnableGuestAccountStatus</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15950-123">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="15950-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="15950-124">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="15950-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15950-125">Лимитлокалаккаунтусеофбланкпассвордстоконсолелогононли учетных записей \_</span><span class="sxs-lookup"><span data-stu-id="15950-125">Accounts\_LimitLocalAccountUseOfBlankPasswordsToConsoleLogonOnly</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-accounts-limitlocalaccountuseofblankpasswordstoconsolelogononly)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15950-126">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="15950-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="15950-127">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="15950-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15950-128">Ренамеадминистратораккаунт учетных записей \_</span><span class="sxs-lookup"><span data-stu-id="15950-128">Accounts\_RenameAdministratorAccount</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-accounts-renameadministratoraccount)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15950-129">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="15950-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15950-130">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="15950-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15950-131">Ренамегуестаккаунт учетных записей \_</span><span class="sxs-lookup"><span data-stu-id="15950-131">Accounts\_RenameGuestAccount</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-accounts-renameguestaccount)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15950-132">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="15950-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15950-133">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="15950-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15950-134">Устройства \_ алловедтоформатандежектремоваблемедиа</span><span class="sxs-lookup"><span data-stu-id="15950-134">Devices\_AllowedToFormatAndEjectRemovableMedia</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-devices-allowedtoformatandejectremovablemedia)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15950-135">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="15950-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15950-136">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="15950-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15950-137">Устройства \_ алловундокквисаусавингтологон</span><span class="sxs-lookup"><span data-stu-id="15950-137">Devices\_AllowUndockWithoutHavingToLogon</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-devices-allowundockwithouthavingtologon)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15950-138">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="15950-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="15950-139">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="15950-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15950-140">Устройства \_ превентусерсфроминсталлингпринтердриверсвхенконнектингтошаредпринтерс</span><span class="sxs-lookup"><span data-stu-id="15950-140">Devices\_PreventUsersFromInstallingPrinterDriversWhenConnectingToSharedPrinters</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-devices-preventusersfrominstallingprinterdriverswhenconnectingtosharedprinters)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15950-141">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="15950-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="15950-142">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="15950-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15950-143">Устройства \_ рестрикткдромакцесстолокаллилогжедонусеронли</span><span class="sxs-lookup"><span data-stu-id="15950-143">Devices\_RestrictCDROMAccessToLocallyLoggedOnUserOnly</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-devices-restrictcdromaccesstolocallyloggedonuseronly)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15950-144">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="15950-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15950-145">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="15950-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="15950-146">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="15950-146">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15950-147">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="15950-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15950-148">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="15950-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="15950-149">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="15950-149">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15950-150">Интерактивелогон \_ дисплайусеринформатионвхенсесессионислоккед</span><span class="sxs-lookup"><span data-stu-id="15950-150">InteractiveLogon\_DisplayUserInformationWhenTheSessionIsLocked</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-interactivelogon-displayuserinformationwhenthesessionislocked)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15950-151">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="15950-151">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="15950-152">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="15950-152">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15950-153">Интерактивелогон \_ донотдисплайластсигнедин</span><span class="sxs-lookup"><span data-stu-id="15950-153">Interactivelogon\_DoNotDisplayLastSignedIn</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-interactivelogon-donotdisplaylastsignedin)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15950-154">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="15950-154">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="15950-155">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="15950-155">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15950-156">Интерактивелогон \_ донотдисплайусернамеатсигнин</span><span class="sxs-lookup"><span data-stu-id="15950-156">Interactivelogon\_DoNotDisplayUsernameAtSignIn</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-interactivelogon-donotdisplayusernameatsignin)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15950-157">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="15950-157">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="15950-158">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="15950-158">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15950-159">Интерактивелогон \_ донотрекуиректрлалтдел</span><span class="sxs-lookup"><span data-stu-id="15950-159">Interactivelogon\_DoNotRequireCTRLALTDEL</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-interactivelogon-donotrequirectrlaltdel)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15950-160">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="15950-160">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="15950-161">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="15950-161">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15950-162">Интерактивелогон \_ мачинеинактивитилимит</span><span class="sxs-lookup"><span data-stu-id="15950-162">InteractiveLogon\_MachineInactivityLimit</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-interactivelogon-machineinactivitylimit)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15950-163">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="15950-163">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="15950-164">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="15950-164">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15950-165">Интерактивелогон \_ мессажетекстфорусерсаттемптингтологон</span><span class="sxs-lookup"><span data-stu-id="15950-165">InteractiveLogon\_MessageTextForUsersAttemptingToLogOn</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-interactivelogon-messagetextforusersattemptingtologon)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15950-166">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="15950-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15950-167">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="15950-167">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15950-168">Интерактивелогон \_ мессажетитлефорусерсаттемптингтологон</span><span class="sxs-lookup"><span data-stu-id="15950-168">InteractiveLogon\_MessageTitleForUsersAttemptingToLogOn</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-interactivelogon-messagetitleforusersattemptingtologon)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15950-169">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="15950-169">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15950-170">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="15950-170">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15950-171">Нетворкакцесс \_ доноталлованонимаусенумератионофсамаккаунтсандшарес</span><span class="sxs-lookup"><span data-stu-id="15950-171">NetworkAccess\_DoNotAllowAnonymousEnumerationOfSAMAccountsAndShares</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-networkaccess-donotallowanonymousenumerationofsamaccountsandshares)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15950-172">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="15950-172">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="15950-173">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="15950-173">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15950-174">Нетворкакцесс \_ рестриктанонимаусакцесстонамедпипесандшарес</span><span class="sxs-lookup"><span data-stu-id="15950-174">NetworkAccess\_RestrictAnonymousAccessToNamedPipesAndShares</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-networkaccess-restrictanonymousaccesstonamedpipesandshares)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15950-175">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="15950-175">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="15950-176">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="15950-176">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15950-177">Нетворкакцесс \_ рестриктклиентсалловедтомакеремотекаллстосам</span><span class="sxs-lookup"><span data-stu-id="15950-177">NetworkAccess\_RestrictClientsAllowedToMakeRemoteCallsToSAM</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-networkaccess-restrictclientsallowedtomakeremotecallstosam)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15950-178">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="15950-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15950-179">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="15950-179">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15950-180">Нетворксекурити \_ AllowPKU2UAuthenticationRequests</span><span class="sxs-lookup"><span data-stu-id="15950-180">NetworkSecurity\_AllowPKU2UAuthenticationRequests</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-networksecurity-allowpku2uauthenticationrequests)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15950-181">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="15950-181">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="15950-182">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="15950-182">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="15950-183">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="15950-183">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15950-184">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="15950-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15950-185">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="15950-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="15950-186">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="15950-186">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15950-187">Рековериконсоле \_ алловаутоматикадминистративелогон</span><span class="sxs-lookup"><span data-stu-id="15950-187">RecoveryConsole\_AllowAutomaticAdministrativeLogon</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-recoveryconsole-allowautomaticadministrativelogon)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15950-188">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="15950-188">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="15950-189">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="15950-189">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15950-190">Завершение работы \_ алловсистемтобешутдовнвисаусавингтологон</span><span class="sxs-lookup"><span data-stu-id="15950-190">Shutdown\_AllowSystemToBeShutDownWithoutHavingToLogOn</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-shutdown-allowsystemtobeshutdownwithouthavingtologon)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15950-191">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="15950-191">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="15950-192">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="15950-192">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15950-193">Завершение работы \_ клеарвиртуалмеморипажефиле</span><span class="sxs-lookup"><span data-stu-id="15950-193">Shutdown\_ClearVirtualMemoryPageFile</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-shutdown-clearvirtualmemorypagefile)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15950-194">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="15950-194">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="15950-195">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="15950-195">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15950-196">\_Алловуиакцессаппликатионстопромптфорелеватион userAccountControl</span><span class="sxs-lookup"><span data-stu-id="15950-196">UserAccountControl\_AllowUIAccessApplicationsToPromptForElevation</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-useraccountcontrol-allowuiaccessapplicationstopromptforelevation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15950-197">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="15950-197">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="15950-198">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="15950-198">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15950-199">\_Бехавиорофсилеватионпромптфорадминистраторс userAccountControl</span><span class="sxs-lookup"><span data-stu-id="15950-199">UserAccountControl\_BehaviorOfTheElevationPromptForAdministrators</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-useraccountcontrol-behavioroftheelevationpromptforadministrators)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15950-200">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="15950-200">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="15950-201">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="15950-201">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15950-202">\_Бехавиорофсилеватионпромптфорстандардусерс userAccountControl</span><span class="sxs-lookup"><span data-stu-id="15950-202">UserAccountControl\_BehaviorOfTheElevationPromptForStandardUsers</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-useraccountcontrol-behavioroftheelevationpromptforstandardusers)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15950-203">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="15950-203">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="15950-204">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="15950-204">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15950-205">\_Детектаппликатионинсталлатионсандпромптфорелеватион userAccountControl</span><span class="sxs-lookup"><span data-stu-id="15950-205">UserAccountControl\_DetectApplicationInstallationsAndPromptForElevation</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-useraccountcontrol-detectapplicationinstallationsandpromptforelevation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15950-206">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="15950-206">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="15950-207">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="15950-207">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15950-208">\_Онлелеватиксекутаблефилессатаресигнедандвалидатед userAccountControl</span><span class="sxs-lookup"><span data-stu-id="15950-208">UserAccountControl\_OnlyElevateExecutableFilesThatAreSignedAndValidated</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-useraccountcontrol-onlyelevateexecutablefilesthataresignedandvalidated)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15950-209">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="15950-209">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="15950-210">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="15950-210">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15950-211">\_Онлелеватеуиакцессаппликатионссатареинсталлединсекурелокатионс userAccountControl</span><span class="sxs-lookup"><span data-stu-id="15950-211">UserAccountControl\_OnlyElevateUIAccessApplicationsThatAreInstalledInSecureLocations</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-useraccountcontrol-onlyelevateuiaccessapplicationsthatareinstalledinsecurelocations)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15950-212">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="15950-212">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="15950-213">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="15950-213">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15950-214">\_Руналладминистраторсинадминаппровалмоде userAccountControl</span><span class="sxs-lookup"><span data-stu-id="15950-214">UserAccountControl\_RunAllAdministratorsInAdminApprovalMode</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-useraccountcontrol-runalladministratorsinadminapprovalmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15950-215">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="15950-215">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="15950-216">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="15950-216">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15950-217">\_Свитчтосесекуредесктопвхенпромптингфорелеватион userAccountControl</span><span class="sxs-lookup"><span data-stu-id="15950-217">UserAccountControl\_SwitchToTheSecureDesktopWhenPromptingForElevation</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-useraccountcontrol-switchtothesecuredesktopwhenpromptingforelevation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15950-218">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="15950-218">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="15950-219">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="15950-219">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15950-220">\_Усеадминаппровалмоде userAccountControl</span><span class="sxs-lookup"><span data-stu-id="15950-220">UserAccountControl\_UseAdminApprovalMode</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-useraccountcontrol-useadminapprovalmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15950-221">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="15950-221">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="15950-222">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="15950-222">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15950-223">\_Виртуализефилеандрегистривритефаилурестоперусерлокатионс userAccountControl</span><span class="sxs-lookup"><span data-stu-id="15950-223">UserAccountControl\_VirtualizeFileAndRegistryWriteFailuresToPerUserLocations</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-useraccountcontrol-virtualizefileandregistrywritefailurestoperuserlocations)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15950-224">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="15950-224">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="15950-225">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="15950-225">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="15950-226">Требования</span><span class="sxs-lookup"><span data-stu-id="15950-226">Requirements</span></span>



| <span data-ttu-id="15950-227">Требование</span><span class="sxs-lookup"><span data-stu-id="15950-227">Requirement</span></span> | <span data-ttu-id="15950-228">Значение</span><span class="sxs-lookup"><span data-stu-id="15950-228">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15950-229">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="15950-229">Minimum supported client</span></span><br/> | <span data-ttu-id="15950-230">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="15950-230">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="15950-231">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="15950-231">Minimum supported server</span></span><br/> | <span data-ttu-id="15950-232">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="15950-232">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="15950-233">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="15950-233">Namespace</span></span><br/>                | <span data-ttu-id="15950-234">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="15950-234">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="15950-235">MOF</span><span class="sxs-lookup"><span data-stu-id="15950-235">MOF</span></span><br/>                      | <dl> <span data-ttu-id="15950-236"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="15950-236"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="15950-237">DLL</span><span class="sxs-lookup"><span data-stu-id="15950-237">DLL</span></span><br/>                      | <dl> <span data-ttu-id="15950-238"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="15950-238"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

