---
title: Класс MDM_Policy_Config01_LocalPoliciesSecurityOptions02
description: Политика MDM \_ \_ Config01 \_ LocalPoliciesSecurityOptions02 настраивает параметры безопасности локальных политик.
ms.assetid: 07688109-f14a-4a04-91b2-ee928d8911b4
keywords:
- Класс MDM_Policy_Config01_LocalPoliciesSecurityOptions02
- MDM_Policy_Config01_LocalPoliciesSecurityOptions02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_LocalPoliciesSecurityOptions02
- MDM_Policy_Config01_LocalPoliciesSecurityOptions02.InstanceID
- MDM_Policy_Config01_LocalPoliciesSecurityOptions02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf39e1db2f5d6f823667865054a8c72b18dc916f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071602"
---
# <a name="mdm_policy_config01_localpoliciessecurityoptions02-class"></a><span data-ttu-id="2c34f-105">\_Класс политики MDM \_ Config01 \_ LocalPoliciesSecurityOptions02</span><span class="sxs-lookup"><span data-stu-id="2c34f-105">MDM\_Policy\_Config01\_LocalPoliciesSecurityOptions02 class</span></span>

<span data-ttu-id="2c34f-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="2c34f-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="2c34f-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="2c34f-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="2c34f-108">Политика MDM \_ \_ Config01 \_ LocalPoliciesSecurityOptions02 настраивает параметры безопасности локальных политик.</span><span class="sxs-lookup"><span data-stu-id="2c34f-108">The MDM\_Policy\_Config01\_LocalPoliciesSecurityOptions02 configures the local policies security options.</span></span>

<span data-ttu-id="2c34f-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="2c34f-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c34f-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2c34f-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_LocalPoliciesSecurityOptions02
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

## <a name="members"></a><span data-ttu-id="2c34f-111">Члены</span><span class="sxs-lookup"><span data-stu-id="2c34f-111">Members</span></span>

<span data-ttu-id="2c34f-112">Класс **\_ политики MDM \_ Config01 \_ LocalPoliciesSecurityOptions02** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="2c34f-112">The **MDM\_Policy\_Config01\_LocalPoliciesSecurityOptions02** class has these types of members:</span></span>

-   [<span data-ttu-id="2c34f-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="2c34f-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2c34f-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="2c34f-114">Properties</span></span>

<span data-ttu-id="2c34f-115">Класс **\_ политики MDM \_ Config01 \_ LocalPoliciesSecurityOptions02** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="2c34f-115">The **MDM\_Policy\_Config01\_LocalPoliciesSecurityOptions02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="2c34f-116">Блоккмикрософтаккаунтс учетных записей \_</span><span class="sxs-lookup"><span data-stu-id="2c34f-116">Accounts\_BlockMicrosoftAccounts</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-accounts-blockmicrosoftaccounts)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c34f-117">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="2c34f-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2c34f-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="2c34f-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2c34f-119">Accounts_EnableAdministratorAccountStatus</span><span class="sxs-lookup"><span data-stu-id="2c34f-119">Accounts_EnableAdministratorAccountStatus</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c34f-120">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="2c34f-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2c34f-121">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="2c34f-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2c34f-122">Accounts_EnableGuestAccountStatus</span><span class="sxs-lookup"><span data-stu-id="2c34f-122">Accounts_EnableGuestAccountStatus</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c34f-123">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="2c34f-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2c34f-124">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="2c34f-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2c34f-125">Лимитлокалаккаунтусеофбланкпассвордстоконсолелогононли учетных записей \_</span><span class="sxs-lookup"><span data-stu-id="2c34f-125">Accounts\_LimitLocalAccountUseOfBlankPasswordsToConsoleLogonOnly</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-accounts-limitlocalaccountuseofblankpasswordstoconsolelogononly)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c34f-126">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="2c34f-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2c34f-127">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="2c34f-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2c34f-128">Ренамеадминистратораккаунт учетных записей \_</span><span class="sxs-lookup"><span data-stu-id="2c34f-128">Accounts\_RenameAdministratorAccount</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-accounts-renameadministratoraccount)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c34f-129">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2c34f-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c34f-130">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="2c34f-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2c34f-131">Ренамегуестаккаунт учетных записей \_</span><span class="sxs-lookup"><span data-stu-id="2c34f-131">Accounts\_RenameGuestAccount</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-accounts-renameguestaccount)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c34f-132">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2c34f-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c34f-133">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="2c34f-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2c34f-134">Устройства \_ алловедтоформатандежектремоваблемедиа</span><span class="sxs-lookup"><span data-stu-id="2c34f-134">Devices\_AllowedToFormatAndEjectRemovableMedia</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-devices-allowedtoformatandejectremovablemedia)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c34f-135">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2c34f-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c34f-136">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="2c34f-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2c34f-137">Устройства \_ алловундокквисаусавингтологон</span><span class="sxs-lookup"><span data-stu-id="2c34f-137">Devices\_AllowUndockWithoutHavingToLogon</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-devices-allowundockwithouthavingtologon)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c34f-138">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="2c34f-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2c34f-139">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="2c34f-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2c34f-140">Устройства \_ превентусерсфроминсталлингпринтердриверсвхенконнектингтошаредпринтерс</span><span class="sxs-lookup"><span data-stu-id="2c34f-140">Devices\_PreventUsersFromInstallingPrinterDriversWhenConnectingToSharedPrinters</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-devices-preventusersfrominstallingprinterdriverswhenconnectingtosharedprinters)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c34f-141">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="2c34f-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2c34f-142">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="2c34f-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2c34f-143">Устройства \_ рестрикткдромакцесстолокаллилогжедонусеронли</span><span class="sxs-lookup"><span data-stu-id="2c34f-143">Devices\_RestrictCDROMAccessToLocallyLoggedOnUserOnly</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-devices-restrictcdromaccesstolocallyloggedonuseronly)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c34f-144">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2c34f-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c34f-145">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="2c34f-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2c34f-146">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="2c34f-146">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c34f-147">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2c34f-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c34f-148">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2c34f-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c34f-149">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2c34f-149">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2c34f-150">Интерактивелогон \_ дисплайусеринформатионвхенсесессионислоккед</span><span class="sxs-lookup"><span data-stu-id="2c34f-150">InteractiveLogon\_DisplayUserInformationWhenTheSessionIsLocked</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-interactivelogon-displayuserinformationwhenthesessionislocked)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c34f-151">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="2c34f-151">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2c34f-152">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="2c34f-152">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2c34f-153">Интерактивелогон \_ донотдисплайластсигнедин</span><span class="sxs-lookup"><span data-stu-id="2c34f-153">Interactivelogon\_DoNotDisplayLastSignedIn</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-interactivelogon-donotdisplaylastsignedin)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c34f-154">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="2c34f-154">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2c34f-155">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="2c34f-155">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2c34f-156">Интерактивелогон \_ донотдисплайусернамеатсигнин</span><span class="sxs-lookup"><span data-stu-id="2c34f-156">Interactivelogon\_DoNotDisplayUsernameAtSignIn</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-interactivelogon-donotdisplayusernameatsignin)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c34f-157">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="2c34f-157">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2c34f-158">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="2c34f-158">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2c34f-159">Интерактивелогон \_ донотрекуиректрлалтдел</span><span class="sxs-lookup"><span data-stu-id="2c34f-159">Interactivelogon\_DoNotRequireCTRLALTDEL</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-interactivelogon-donotrequirectrlaltdel)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c34f-160">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="2c34f-160">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2c34f-161">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="2c34f-161">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2c34f-162">Интерактивелогон \_ мачинеинактивитилимит</span><span class="sxs-lookup"><span data-stu-id="2c34f-162">InteractiveLogon\_MachineInactivityLimit</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-interactivelogon-machineinactivitylimit)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c34f-163">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="2c34f-163">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2c34f-164">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="2c34f-164">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2c34f-165">Интерактивелогон \_ мессажетекстфорусерсаттемптингтологон</span><span class="sxs-lookup"><span data-stu-id="2c34f-165">InteractiveLogon\_MessageTextForUsersAttemptingToLogOn</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-interactivelogon-messagetextforusersattemptingtologon)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c34f-166">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2c34f-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c34f-167">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="2c34f-167">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2c34f-168">Интерактивелогон \_ мессажетитлефорусерсаттемптингтологон</span><span class="sxs-lookup"><span data-stu-id="2c34f-168">InteractiveLogon\_MessageTitleForUsersAttemptingToLogOn</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-interactivelogon-messagetitleforusersattemptingtologon)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c34f-169">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2c34f-169">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c34f-170">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="2c34f-170">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2c34f-171">Нетворкакцесс \_ доноталлованонимаусенумератионофсамаккаунтсандшарес</span><span class="sxs-lookup"><span data-stu-id="2c34f-171">NetworkAccess\_DoNotAllowAnonymousEnumerationOfSAMAccountsAndShares</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-networkaccess-donotallowanonymousenumerationofsamaccountsandshares)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c34f-172">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="2c34f-172">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2c34f-173">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="2c34f-173">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2c34f-174">Нетворкакцесс \_ рестриктанонимаусакцесстонамедпипесандшарес</span><span class="sxs-lookup"><span data-stu-id="2c34f-174">NetworkAccess\_RestrictAnonymousAccessToNamedPipesAndShares</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-networkaccess-restrictanonymousaccesstonamedpipesandshares)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c34f-175">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="2c34f-175">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2c34f-176">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="2c34f-176">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2c34f-177">Нетворкакцесс \_ рестриктклиентсалловедтомакеремотекаллстосам</span><span class="sxs-lookup"><span data-stu-id="2c34f-177">NetworkAccess\_RestrictClientsAllowedToMakeRemoteCallsToSAM</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-networkaccess-restrictclientsallowedtomakeremotecallstosam)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c34f-178">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2c34f-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c34f-179">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="2c34f-179">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2c34f-180">Нетворксекурити \_ AllowPKU2UAuthenticationRequests</span><span class="sxs-lookup"><span data-stu-id="2c34f-180">NetworkSecurity\_AllowPKU2UAuthenticationRequests</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-networksecurity-allowpku2uauthenticationrequests)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c34f-181">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="2c34f-181">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2c34f-182">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="2c34f-182">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2c34f-183">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="2c34f-183">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c34f-184">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2c34f-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c34f-185">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2c34f-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c34f-186">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2c34f-186">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2c34f-187">Рековериконсоле \_ алловаутоматикадминистративелогон</span><span class="sxs-lookup"><span data-stu-id="2c34f-187">RecoveryConsole\_AllowAutomaticAdministrativeLogon</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-recoveryconsole-allowautomaticadministrativelogon)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c34f-188">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="2c34f-188">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2c34f-189">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="2c34f-189">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2c34f-190">Завершение работы \_ алловсистемтобешутдовнвисаусавингтологон</span><span class="sxs-lookup"><span data-stu-id="2c34f-190">Shutdown\_AllowSystemToBeShutDownWithoutHavingToLogOn</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-shutdown-allowsystemtobeshutdownwithouthavingtologon)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c34f-191">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="2c34f-191">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2c34f-192">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="2c34f-192">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2c34f-193">Завершение работы \_ клеарвиртуалмеморипажефиле</span><span class="sxs-lookup"><span data-stu-id="2c34f-193">Shutdown\_ClearVirtualMemoryPageFile</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-shutdown-clearvirtualmemorypagefile)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c34f-194">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="2c34f-194">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2c34f-195">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="2c34f-195">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2c34f-196">\_Алловуиакцессаппликатионстопромптфорелеватион userAccountControl</span><span class="sxs-lookup"><span data-stu-id="2c34f-196">UserAccountControl\_AllowUIAccessApplicationsToPromptForElevation</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-useraccountcontrol-allowuiaccessapplicationstopromptforelevation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c34f-197">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="2c34f-197">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2c34f-198">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="2c34f-198">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2c34f-199">\_Бехавиорофсилеватионпромптфорадминистраторс userAccountControl</span><span class="sxs-lookup"><span data-stu-id="2c34f-199">UserAccountControl\_BehaviorOfTheElevationPromptForAdministrators</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-useraccountcontrol-behavioroftheelevationpromptforadministrators)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c34f-200">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="2c34f-200">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2c34f-201">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="2c34f-201">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2c34f-202">\_Бехавиорофсилеватионпромптфорстандардусерс userAccountControl</span><span class="sxs-lookup"><span data-stu-id="2c34f-202">UserAccountControl\_BehaviorOfTheElevationPromptForStandardUsers</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-useraccountcontrol-behavioroftheelevationpromptforstandardusers)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c34f-203">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="2c34f-203">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2c34f-204">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="2c34f-204">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2c34f-205">\_Детектаппликатионинсталлатионсандпромптфорелеватион userAccountControl</span><span class="sxs-lookup"><span data-stu-id="2c34f-205">UserAccountControl\_DetectApplicationInstallationsAndPromptForElevation</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-useraccountcontrol-detectapplicationinstallationsandpromptforelevation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c34f-206">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="2c34f-206">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2c34f-207">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="2c34f-207">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2c34f-208">\_Онлелеватиксекутаблефилессатаресигнедандвалидатед userAccountControl</span><span class="sxs-lookup"><span data-stu-id="2c34f-208">UserAccountControl\_OnlyElevateExecutableFilesThatAreSignedAndValidated</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-useraccountcontrol-onlyelevateexecutablefilesthataresignedandvalidated)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c34f-209">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="2c34f-209">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2c34f-210">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="2c34f-210">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2c34f-211">\_Онлелеватеуиакцессаппликатионссатареинсталлединсекурелокатионс userAccountControl</span><span class="sxs-lookup"><span data-stu-id="2c34f-211">UserAccountControl\_OnlyElevateUIAccessApplicationsThatAreInstalledInSecureLocations</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-useraccountcontrol-onlyelevateuiaccessapplicationsthatareinstalledinsecurelocations)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c34f-212">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="2c34f-212">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2c34f-213">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="2c34f-213">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2c34f-214">\_Руналладминистраторсинадминаппровалмоде userAccountControl</span><span class="sxs-lookup"><span data-stu-id="2c34f-214">UserAccountControl\_RunAllAdministratorsInAdminApprovalMode</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-useraccountcontrol-runalladministratorsinadminapprovalmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c34f-215">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="2c34f-215">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2c34f-216">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="2c34f-216">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2c34f-217">\_Свитчтосесекуредесктопвхенпромптингфорелеватион userAccountControl</span><span class="sxs-lookup"><span data-stu-id="2c34f-217">UserAccountControl\_SwitchToTheSecureDesktopWhenPromptingForElevation</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-useraccountcontrol-switchtothesecuredesktopwhenpromptingforelevation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c34f-218">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="2c34f-218">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2c34f-219">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="2c34f-219">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2c34f-220">\_Усеадминаппровалмоде userAccountControl</span><span class="sxs-lookup"><span data-stu-id="2c34f-220">UserAccountControl\_UseAdminApprovalMode</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-useraccountcontrol-useadminapprovalmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c34f-221">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="2c34f-221">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2c34f-222">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="2c34f-222">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2c34f-223">\_Виртуализефилеандрегистривритефаилурестоперусерлокатионс userAccountControl</span><span class="sxs-lookup"><span data-stu-id="2c34f-223">UserAccountControl\_VirtualizeFileAndRegistryWriteFailuresToPerUserLocations</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-useraccountcontrol-virtualizefileandregistrywritefailurestoperuserlocations)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c34f-224">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="2c34f-224">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2c34f-225">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="2c34f-225">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2c34f-226">Требования</span><span class="sxs-lookup"><span data-stu-id="2c34f-226">Requirements</span></span>



| <span data-ttu-id="2c34f-227">Требование</span><span class="sxs-lookup"><span data-stu-id="2c34f-227">Requirement</span></span> | <span data-ttu-id="2c34f-228">Значение</span><span class="sxs-lookup"><span data-stu-id="2c34f-228">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c34f-229">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2c34f-229">Minimum supported client</span></span><br/> | <span data-ttu-id="2c34f-230">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="2c34f-230">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2c34f-231">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2c34f-231">Minimum supported server</span></span><br/> | <span data-ttu-id="2c34f-232">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="2c34f-232">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="2c34f-233">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="2c34f-233">Namespace</span></span><br/>                | <span data-ttu-id="2c34f-234">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="2c34f-234">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="2c34f-235">MOF</span><span class="sxs-lookup"><span data-stu-id="2c34f-235">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2c34f-236"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2c34f-236"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="2c34f-237">DLL</span><span class="sxs-lookup"><span data-stu-id="2c34f-237">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2c34f-238"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2c34f-238"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

