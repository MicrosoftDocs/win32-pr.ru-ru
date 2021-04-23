---
title: Класс MDM_Policy_Result01_Privacy02
description: '\_Класс политики MDM \_ Result01 \_ Privacy02 представляет доступные политики поиска.'
ms.assetid: 40aa1b74-bdec-471d-a7d4-89e59bf8637c
keywords:
- Класс MDM_Policy_Result01_Privacy02
- MDM_Policy_Result01_Privacy02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Privacy02
- MDM_Policy_Result01_Privacy02.InstanceID
- MDM_Policy_Result01_Privacy02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80bbe28d1c0bc1258ec3c9fb57fd592a97c96026
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489216"
---
# <a name="mdm_policy_result01_privacy02-class"></a><span data-ttu-id="67dbb-105">\_Класс политики MDM \_ Result01 \_ Privacy02</span><span class="sxs-lookup"><span data-stu-id="67dbb-105">MDM\_Policy\_Result01\_Privacy02 class</span></span>

<span data-ttu-id="67dbb-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="67dbb-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="67dbb-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="67dbb-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="67dbb-108">Класс **\_ политики MDM \_ Result01 \_ Privacy02** представляет доступные политики поиска.</span><span class="sxs-lookup"><span data-stu-id="67dbb-108">The **MDM\_Policy\_Result01\_Privacy02** class represents the search policies available.</span></span>

<span data-ttu-id="67dbb-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="67dbb-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="67dbb-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="67dbb-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Privacy02
{
  string InstanceID;
  string ParentID;
  sint32 AllowAutoAcceptPairingAndPrivacyConsentPrompts;
  sint32 AllowInputPersonalization;
  string LetAppsSyncWithDevices_UserInControlOfTheseApps;
  sint32 PublishUserActivities;
  string LetAppsSyncWithDevices_ForceDenyTheseApps;
  string LetAppsSyncWithDevices_ForceAllowTheseApps;
  sint32 LetAppsSyncWithDevices;
  string LetAppsAccessTrustedDevices_UserInControlOfTheseApps;
  string LetAppsRunInBackground_UserInControlOfTheseApps;
  string LetAppsRunInBackground_ForceDenyTheseApps;
  string LetAppsRunInBackground_ForceAllowTheseApps;
  sint32 LetAppsRunInBackground;
  string LetAppsGetDiagnosticInfo_UserInControlOfTheseApps;
  string LetAppsGetDiagnosticInfo_ForceDenyTheseApps;
  string LetAppsGetDiagnosticInfo_ForceAllowTheseApps;
  sint32 LetAppsGetDiagnosticInfo;
  string LetAppsAccessTrustedDevices_ForceDenyTheseApps;
  string LetAppsAccessTrustedDevices_ForceAllowTheseApps;
  sint32 LetAppsAccessTrustedDevices;
  string LetAppsAccessRadios_UserInControlOfTheseApps;
  string LetAppsAccessTasks_UserInControlOfTheseApps;
  string LetAppsAccessTasks_ForceDenyTheseApps;
  string LetAppsAccessTasks_ForceAllowTheseApps;
  sint32 LetAppsAccessTasks;
  string LetAppsAccessRadios_ForceDenyTheseApps;
  string LetAppsAccessRadios_ForceAllowTheseApps;
  sint32 LetAppsAccessRadios;
  string LetAppsAccessPhone_UserInControlOfTheseApps;
  string LetAppsAccessPhone_ForceDenyTheseApps;
  string LetAppsAccessPhone_ForceAllowTheseApps;
  sint32 LetAppsAccessPhone;
  string LetAppsAccessMotion_UserInControlOfTheseApps;
  string LetAppsAccessNotifications_UserInControlOfTheseApps;
  string LetAppsAccessNotifications_ForceDenyTheseApps;
  string LetAppsAccessNotifications_ForceAllowTheseApps;
  sint32 LetAppsAccessNotifications;
  string LetAppsAccessMotion_ForceDenyTheseApps;
  string LetAppsAccessMotion_ForceAllowTheseApps;
  sint32 LetAppsAccessMotion;
  string LetAppsAccessMicrophone_UserInControlOfTheseApps;
  string LetAppsAccessMicrophone_ForceDenyTheseApps;
  string LetAppsAccessMicrophone_ForceAllowTheseApps;
  sint32 LetAppsAccessMicrophone;
  string LetAppsAccessMessaging_UserInControlOfTheseApps;
  string LetAppsAccessMessaging_ForceDenyTheseApps;
  string LetAppsAccessMessaging_ForceAllowTheseApps;
  sint32 LetAppsAccessMessaging;
  string LetAppsAccessLocation_UserInControlOfTheseApps;
  string LetAppsAccessLocation_ForceDenyTheseApps;
  string LetAppsAccessLocation_ForceAllowTheseApps;
  sint32 LetAppsAccessLocation;
  string LetAppsAccessEmail_UserInControlOfTheseApps;
  string LetAppsAccessEmail_ForceDenyTheseApps;
  string LetAppsAccessEmail_ForceAllowTheseApps;
  sint32 LetAppsAccessEmail;
  string LetAppsAccessContacts_UserInControlOfTheseApps;
  string LetAppsAccessContacts_ForceDenyTheseApps;
  string LetAppsAccessContacts_ForceAllowTheseApps;
  sint32 LetAppsAccessContacts;
  string LetAppsAccessCamera_UserInControlOfTheseApps;
  string LetAppsAccessCamera_ForceDenyTheseApps;
  string LetAppsAccessCamera_ForceAllowTheseApps;
  sint32 LetAppsAccessCamera;
  string LetAppsAccessCallHistory_UserInControlOfTheseApps;
  string LetAppsAccessCallHistory_ForceDenyTheseApps;
  string LetAppsAccessCallHistory_ForceAllowTheseApps;
  sint32 LetAppsAccessCallHistory;
  string LetAppsAccessCalendar_UserInControlOfTheseApps;
  string LetAppsAccessCalendar_ForceDenyTheseApps;
  string LetAppsAccessCalendar_ForceAllowTheseApps;
  sint32 LetAppsAccessCalendar;
  string LetAppsAccessAccountInfo_UserInControlOfTheseApps;
  string LetAppsAccessAccountInfo_ForceDenyTheseApps;
  string LetAppsAccessAccountInfo_ForceAllowTheseApps;
  sint32 LetAppsAccessAccountInfo;
  sint32 DisableAdvertisingId;
  sint32 EnableActivityFeed;
};
```

## <a name="members"></a><span data-ttu-id="67dbb-111">Члены</span><span class="sxs-lookup"><span data-stu-id="67dbb-111">Members</span></span>

<span data-ttu-id="67dbb-112">Класс **\_ политики MDM \_ Result01 \_ Privacy02** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="67dbb-112">The **MDM\_Policy\_Result01\_Privacy02** class has these types of members:</span></span>

-   [<span data-ttu-id="67dbb-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="67dbb-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="67dbb-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="67dbb-114">Properties</span></span>

<span data-ttu-id="67dbb-115">Класс **\_ политики MDM \_ Result01 \_ Privacy02** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="67dbb-115">The **MDM\_Policy\_Result01\_Privacy02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="67dbb-116">AllowAutoAcceptPairingAndPrivacyConsentPrompts</span><span class="sxs-lookup"><span data-stu-id="67dbb-116">AllowAutoAcceptPairingAndPrivacyConsentPrompts</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-allowautoacceptpairingandprivacyconsentprompts)
</dt> <dd> <dl> <dt>

<span data-ttu-id="67dbb-117">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="67dbb-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="67dbb-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="67dbb-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="67dbb-119">AllowInputPersonalization</span><span class="sxs-lookup"><span data-stu-id="67dbb-119">AllowInputPersonalization</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-allowinputpersonalization)
</dt> <dd> <dl> <dt>

<span data-ttu-id="67dbb-120">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="67dbb-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="67dbb-121">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="67dbb-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="67dbb-122">DisableAdvertisingId</span><span class="sxs-lookup"><span data-stu-id="67dbb-122">DisableAdvertisingId</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-disableadvertisingid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="67dbb-123">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="67dbb-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="67dbb-124">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="67dbb-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="67dbb-125">енаблеактивитифид</span><span class="sxs-lookup"><span data-stu-id="67dbb-125">EnableActivityFeed</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-enableactivityfeed)
</dt> <dd> <dl> <dt>

<span data-ttu-id="67dbb-126">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="67dbb-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="67dbb-127">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="67dbb-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="67dbb-128">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="67dbb-128">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67dbb-129">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="67dbb-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67dbb-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="67dbb-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67dbb-131">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="67dbb-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="67dbb-132">Определяет имя родительского узла.</span><span class="sxs-lookup"><span data-stu-id="67dbb-132">Identifies the name of the parent node.</span></span> <span data-ttu-id="67dbb-133">Для этого класса строка имеет значение "Privacy".</span><span class="sxs-lookup"><span data-stu-id="67dbb-133">For this class, the string is "Privacy".</span></span>

</dd> <dt>

[<span data-ttu-id="67dbb-134">летаппсакцессаккаунтинфо</span><span class="sxs-lookup"><span data-stu-id="67dbb-134">LetAppsAccessAccountInfo</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessaccountinfo)
</dt> <dd> <dl> <dt>

<span data-ttu-id="67dbb-135">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="67dbb-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="67dbb-136">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="67dbb-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="67dbb-137">Летаппсакцессаккаунтинфо \_ форцеалловсесеаппс</span><span class="sxs-lookup"><span data-stu-id="67dbb-137">LetAppsAccessAccountInfo\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessaccountinfo-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="67dbb-138">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="67dbb-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67dbb-139">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="67dbb-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="67dbb-140">Летаппсакцессаккаунтинфо \_ форцеденисесеаппс</span><span class="sxs-lookup"><span data-stu-id="67dbb-140">LetAppsAccessAccountInfo\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessaccountinfo-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="67dbb-141">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="67dbb-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67dbb-142">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="67dbb-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="67dbb-143">Летаппсакцессаккаунтинфо \_ усеринконтролофсесеаппс</span><span class="sxs-lookup"><span data-stu-id="67dbb-143">LetAppsAccessAccountInfo\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessaccountinfo-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="67dbb-144">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="67dbb-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67dbb-145">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="67dbb-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="67dbb-146">летаппсакцесскалендар</span><span class="sxs-lookup"><span data-stu-id="67dbb-146">LetAppsAccessCalendar</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscalendar)
</dt> <dd> <dl> <dt>

<span data-ttu-id="67dbb-147">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="67dbb-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="67dbb-148">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="67dbb-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="67dbb-149">Летаппсакцесскалендар \_ форцеалловсесеаппс</span><span class="sxs-lookup"><span data-stu-id="67dbb-149">LetAppsAccessCalendar\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscalendar-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="67dbb-150">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="67dbb-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67dbb-151">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="67dbb-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="67dbb-152">Летаппсакцесскалендар \_ форцеденисесеаппс</span><span class="sxs-lookup"><span data-stu-id="67dbb-152">LetAppsAccessCalendar\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscalendar-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="67dbb-153">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="67dbb-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67dbb-154">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="67dbb-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="67dbb-155">Летаппсакцесскалендар \_ усеринконтролофсесеаппс</span><span class="sxs-lookup"><span data-stu-id="67dbb-155">LetAppsAccessCalendar\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscalendar-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="67dbb-156">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="67dbb-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67dbb-157">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="67dbb-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="67dbb-158">летаппсакцесскаллхистори</span><span class="sxs-lookup"><span data-stu-id="67dbb-158">LetAppsAccessCallHistory</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscallhistory)
</dt> <dd> <dl> <dt>

<span data-ttu-id="67dbb-159">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="67dbb-159">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="67dbb-160">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="67dbb-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="67dbb-161">Летаппсакцесскаллхистори \_ форцеалловсесеаппс</span><span class="sxs-lookup"><span data-stu-id="67dbb-161">LetAppsAccessCallHistory\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscallhistory-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="67dbb-162">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="67dbb-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67dbb-163">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="67dbb-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="67dbb-164">Летаппсакцесскаллхистори \_ форцеденисесеаппс</span><span class="sxs-lookup"><span data-stu-id="67dbb-164">LetAppsAccessCallHistory\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscallhistory-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="67dbb-165">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="67dbb-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67dbb-166">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="67dbb-166">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="67dbb-167">Летаппсакцесскаллхистори \_ усеринконтролофсесеаппс</span><span class="sxs-lookup"><span data-stu-id="67dbb-167">LetAppsAccessCallHistory\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscallhistory-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="67dbb-168">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="67dbb-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67dbb-169">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="67dbb-169">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="67dbb-170">летаппсакцесскамера</span><span class="sxs-lookup"><span data-stu-id="67dbb-170">LetAppsAccessCamera</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscamera)
</dt> <dd> <dl> <dt>

<span data-ttu-id="67dbb-171">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="67dbb-171">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="67dbb-172">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="67dbb-172">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="67dbb-173">Летаппсакцесскамера \_ форцеалловсесеаппс</span><span class="sxs-lookup"><span data-stu-id="67dbb-173">LetAppsAccessCamera\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscamera-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="67dbb-174">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="67dbb-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67dbb-175">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="67dbb-175">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="67dbb-176">Летаппсакцесскамера \_ форцеденисесеаппс</span><span class="sxs-lookup"><span data-stu-id="67dbb-176">LetAppsAccessCamera\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscamera-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="67dbb-177">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="67dbb-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67dbb-178">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="67dbb-178">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="67dbb-179">Летаппсакцесскамера \_ усеринконтролофсесеаппс</span><span class="sxs-lookup"><span data-stu-id="67dbb-179">LetAppsAccessCamera\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscamera-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="67dbb-180">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="67dbb-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67dbb-181">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="67dbb-181">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="67dbb-182">летаппсакцессконтактс</span><span class="sxs-lookup"><span data-stu-id="67dbb-182">LetAppsAccessContacts</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscontacts)
</dt> <dd> <dl> <dt>

<span data-ttu-id="67dbb-183">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="67dbb-183">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="67dbb-184">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="67dbb-184">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="67dbb-185">Летаппсакцессконтактс \_ форцеалловсесеаппс</span><span class="sxs-lookup"><span data-stu-id="67dbb-185">LetAppsAccessContacts\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscontacts-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="67dbb-186">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="67dbb-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67dbb-187">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="67dbb-187">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="67dbb-188">Летаппсакцессконтактс \_ форцеденисесеаппс</span><span class="sxs-lookup"><span data-stu-id="67dbb-188">LetAppsAccessContacts\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscontacts-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="67dbb-189">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="67dbb-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67dbb-190">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="67dbb-190">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="67dbb-191">Летаппсакцессконтактс \_ усеринконтролофсесеаппс</span><span class="sxs-lookup"><span data-stu-id="67dbb-191">LetAppsAccessContacts\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscontacts-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="67dbb-192">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="67dbb-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67dbb-193">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="67dbb-193">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="67dbb-194">летаппсакцессемаил</span><span class="sxs-lookup"><span data-stu-id="67dbb-194">LetAppsAccessEmail</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessemail)
</dt> <dd> <dl> <dt>

<span data-ttu-id="67dbb-195">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="67dbb-195">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="67dbb-196">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="67dbb-196">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="67dbb-197">Летаппсакцессемаил \_ форцеалловсесеаппс</span><span class="sxs-lookup"><span data-stu-id="67dbb-197">LetAppsAccessEmail\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessemail-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="67dbb-198">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="67dbb-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67dbb-199">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="67dbb-199">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="67dbb-200">Летаппсакцессемаил \_ форцеденисесеаппс</span><span class="sxs-lookup"><span data-stu-id="67dbb-200">LetAppsAccessEmail\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessemail-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="67dbb-201">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="67dbb-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67dbb-202">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="67dbb-202">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="67dbb-203">Летаппсакцессемаил \_ усеринконтролофсесеаппс</span><span class="sxs-lookup"><span data-stu-id="67dbb-203">LetAppsAccessEmail\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessemail-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="67dbb-204">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="67dbb-204">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67dbb-205">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="67dbb-205">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="67dbb-206">летаппсакцесслокатион</span><span class="sxs-lookup"><span data-stu-id="67dbb-206">LetAppsAccessLocation</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesslocation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="67dbb-207">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="67dbb-207">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="67dbb-208">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="67dbb-208">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="67dbb-209">Летаппсакцесслокатион \_ форцеалловсесеаппс</span><span class="sxs-lookup"><span data-stu-id="67dbb-209">LetAppsAccessLocation\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesslocation-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="67dbb-210">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="67dbb-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67dbb-211">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="67dbb-211">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="67dbb-212">Летаппсакцесслокатион \_ форцеденисесеаппс</span><span class="sxs-lookup"><span data-stu-id="67dbb-212">LetAppsAccessLocation\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesslocation-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="67dbb-213">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="67dbb-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67dbb-214">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="67dbb-214">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="67dbb-215">Летаппсакцесслокатион \_ усеринконтролофсесеаппс</span><span class="sxs-lookup"><span data-stu-id="67dbb-215">LetAppsAccessLocation\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesslocation-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="67dbb-216">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="67dbb-216">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67dbb-217">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="67dbb-217">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="67dbb-218">летаппсакцессмессагинг</span><span class="sxs-lookup"><span data-stu-id="67dbb-218">LetAppsAccessMessaging</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmessaging)
</dt> <dd> <dl> <dt>

<span data-ttu-id="67dbb-219">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="67dbb-219">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="67dbb-220">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="67dbb-220">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="67dbb-221">Летаппсакцессмессагинг \_ форцеалловсесеаппс</span><span class="sxs-lookup"><span data-stu-id="67dbb-221">LetAppsAccessMessaging\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmessaging-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="67dbb-222">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="67dbb-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67dbb-223">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="67dbb-223">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="67dbb-224">Летаппсакцессмессагинг \_ форцеденисесеаппс</span><span class="sxs-lookup"><span data-stu-id="67dbb-224">LetAppsAccessMessaging\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmessaging-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="67dbb-225">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="67dbb-225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67dbb-226">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="67dbb-226">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="67dbb-227">Летаппсакцессмессагинг \_ усеринконтролофсесеаппс</span><span class="sxs-lookup"><span data-stu-id="67dbb-227">LetAppsAccessMessaging\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmessaging-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="67dbb-228">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="67dbb-228">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67dbb-229">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="67dbb-229">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="67dbb-230">летаппсакцессмикрофоне</span><span class="sxs-lookup"><span data-stu-id="67dbb-230">LetAppsAccessMicrophone</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmicrophone)
</dt> <dd> <dl> <dt>

<span data-ttu-id="67dbb-231">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="67dbb-231">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="67dbb-232">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="67dbb-232">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="67dbb-233">Летаппсакцессмикрофоне \_ форцеалловсесеаппс</span><span class="sxs-lookup"><span data-stu-id="67dbb-233">LetAppsAccessMicrophone\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmicrophone-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="67dbb-234">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="67dbb-234">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67dbb-235">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="67dbb-235">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="67dbb-236">Летаппсакцессмикрофоне \_ форцеденисесеаппс</span><span class="sxs-lookup"><span data-stu-id="67dbb-236">LetAppsAccessMicrophone\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmicrophone-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="67dbb-237">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="67dbb-237">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67dbb-238">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="67dbb-238">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="67dbb-239">Летаппсакцессмикрофоне \_ усеринконтролофсесеаппс</span><span class="sxs-lookup"><span data-stu-id="67dbb-239">LetAppsAccessMicrophone\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmicrophone-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="67dbb-240">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="67dbb-240">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67dbb-241">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="67dbb-241">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="67dbb-242">летаппсакцессмотион</span><span class="sxs-lookup"><span data-stu-id="67dbb-242">LetAppsAccessMotion</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmotion)
</dt> <dd> <dl> <dt>

<span data-ttu-id="67dbb-243">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="67dbb-243">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="67dbb-244">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="67dbb-244">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="67dbb-245">Летаппсакцессмотион \_ форцеалловсесеаппс</span><span class="sxs-lookup"><span data-stu-id="67dbb-245">LetAppsAccessMotion\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmotion-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="67dbb-246">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="67dbb-246">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67dbb-247">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="67dbb-247">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="67dbb-248">Летаппсакцессмотион \_ форцеденисесеаппс</span><span class="sxs-lookup"><span data-stu-id="67dbb-248">LetAppsAccessMotion\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmotion-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="67dbb-249">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="67dbb-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67dbb-250">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="67dbb-250">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="67dbb-251">Летаппсакцессмотион \_ усеринконтролофсесеаппс</span><span class="sxs-lookup"><span data-stu-id="67dbb-251">LetAppsAccessMotion\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmotion-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="67dbb-252">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="67dbb-252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67dbb-253">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="67dbb-253">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="67dbb-254">летаппсакцесснотификатионс</span><span class="sxs-lookup"><span data-stu-id="67dbb-254">LetAppsAccessNotifications</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessnotifications)
</dt> <dd> <dl> <dt>

<span data-ttu-id="67dbb-255">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="67dbb-255">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="67dbb-256">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="67dbb-256">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="67dbb-257">Летаппсакцесснотификатионс \_ форцеалловсесеаппс</span><span class="sxs-lookup"><span data-stu-id="67dbb-257">LetAppsAccessNotifications\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessnotifications-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="67dbb-258">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="67dbb-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67dbb-259">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="67dbb-259">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="67dbb-260">Летаппсакцесснотификатионс \_ форцеденисесеаппс</span><span class="sxs-lookup"><span data-stu-id="67dbb-260">LetAppsAccessNotifications\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessnotifications-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="67dbb-261">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="67dbb-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67dbb-262">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="67dbb-262">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="67dbb-263">Летаппсакцесснотификатионс \_ усеринконтролофсесеаппс</span><span class="sxs-lookup"><span data-stu-id="67dbb-263">LetAppsAccessNotifications\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessnotifications-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="67dbb-264">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="67dbb-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67dbb-265">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="67dbb-265">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="67dbb-266">летаппсакцессфоне</span><span class="sxs-lookup"><span data-stu-id="67dbb-266">LetAppsAccessPhone</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessphone)
</dt> <dd> <dl> <dt>

<span data-ttu-id="67dbb-267">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="67dbb-267">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="67dbb-268">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="67dbb-268">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="67dbb-269">Летаппсакцессфоне \_ форцеалловсесеаппс</span><span class="sxs-lookup"><span data-stu-id="67dbb-269">LetAppsAccessPhone\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessphone-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="67dbb-270">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="67dbb-270">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67dbb-271">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="67dbb-271">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="67dbb-272">Летаппсакцессфоне \_ форцеденисесеаппс</span><span class="sxs-lookup"><span data-stu-id="67dbb-272">LetAppsAccessPhone\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessphone-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="67dbb-273">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="67dbb-273">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67dbb-274">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="67dbb-274">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="67dbb-275">Летаппсакцессфоне \_ усеринконтролофсесеаппс</span><span class="sxs-lookup"><span data-stu-id="67dbb-275">LetAppsAccessPhone\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessphone-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="67dbb-276">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="67dbb-276">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67dbb-277">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="67dbb-277">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="67dbb-278">летаппсакцессрадиос</span><span class="sxs-lookup"><span data-stu-id="67dbb-278">LetAppsAccessRadios</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessradios)
</dt> <dd> <dl> <dt>

<span data-ttu-id="67dbb-279">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="67dbb-279">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="67dbb-280">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="67dbb-280">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="67dbb-281">Летаппсакцессрадиос \_ форцеалловсесеаппс</span><span class="sxs-lookup"><span data-stu-id="67dbb-281">LetAppsAccessRadios\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessradios-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="67dbb-282">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="67dbb-282">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67dbb-283">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="67dbb-283">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="67dbb-284">Летаппсакцессрадиос \_ форцеденисесеаппс</span><span class="sxs-lookup"><span data-stu-id="67dbb-284">LetAppsAccessRadios\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessradios-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="67dbb-285">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="67dbb-285">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67dbb-286">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="67dbb-286">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="67dbb-287">Летаппсакцессрадиос \_ усеринконтролофсесеаппс</span><span class="sxs-lookup"><span data-stu-id="67dbb-287">LetAppsAccessRadios\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessradios-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="67dbb-288">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="67dbb-288">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67dbb-289">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="67dbb-289">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="67dbb-290">летаппсакцесстаскс</span><span class="sxs-lookup"><span data-stu-id="67dbb-290">LetAppsAccessTasks</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesstasks)
</dt> <dd> <dl> <dt>

<span data-ttu-id="67dbb-291">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="67dbb-291">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="67dbb-292">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="67dbb-292">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="67dbb-293">Летаппсакцесстаскс \_ форцеалловсесеаппс</span><span class="sxs-lookup"><span data-stu-id="67dbb-293">LetAppsAccessTasks\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesstasks-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="67dbb-294">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="67dbb-294">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67dbb-295">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="67dbb-295">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="67dbb-296">Летаппсакцесстаскс \_ форцеденисесеаппс</span><span class="sxs-lookup"><span data-stu-id="67dbb-296">LetAppsAccessTasks\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesstasks-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="67dbb-297">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="67dbb-297">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67dbb-298">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="67dbb-298">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="67dbb-299">Летаппсакцесстаскс \_ усеринконтролофсесеаппс</span><span class="sxs-lookup"><span data-stu-id="67dbb-299">LetAppsAccessTasks\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesstasks-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="67dbb-300">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="67dbb-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67dbb-301">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="67dbb-301">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="67dbb-302">летаппсакцесструстеддевицес</span><span class="sxs-lookup"><span data-stu-id="67dbb-302">LetAppsAccessTrustedDevices</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesstrusteddevices)
</dt> <dd> <dl> <dt>

<span data-ttu-id="67dbb-303">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="67dbb-303">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="67dbb-304">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="67dbb-304">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="67dbb-305">Летаппсакцесструстеддевицес \_ форцеалловсесеаппс</span><span class="sxs-lookup"><span data-stu-id="67dbb-305">LetAppsAccessTrustedDevices\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesstrusteddevices-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="67dbb-306">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="67dbb-306">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67dbb-307">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="67dbb-307">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="67dbb-308">Летаппсакцесструстеддевицес \_ форцеденисесеаппс</span><span class="sxs-lookup"><span data-stu-id="67dbb-308">LetAppsAccessTrustedDevices\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesstrusteddevices-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="67dbb-309">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="67dbb-309">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67dbb-310">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="67dbb-310">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="67dbb-311">Летаппсакцесструстеддевицес \_ усеринконтролофсесеаппс</span><span class="sxs-lookup"><span data-stu-id="67dbb-311">LetAppsAccessTrustedDevices\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesstrusteddevices-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="67dbb-312">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="67dbb-312">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67dbb-313">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="67dbb-313">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="67dbb-314">летаппсжетдиагностиЦинфо</span><span class="sxs-lookup"><span data-stu-id="67dbb-314">LetAppsGetDiagnosticInfo</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsgetdiagnosticinfo)
</dt> <dd> <dl> <dt>

<span data-ttu-id="67dbb-315">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="67dbb-315">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="67dbb-316">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="67dbb-316">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="67dbb-317">ЛетаппсжетдиагностиЦинфо \_ форцеалловсесеаппс</span><span class="sxs-lookup"><span data-stu-id="67dbb-317">LetAppsGetDiagnosticInfo\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsgetdiagnosticinfo-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="67dbb-318">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="67dbb-318">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67dbb-319">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="67dbb-319">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="67dbb-320">ЛетаппсжетдиагностиЦинфо \_ форцеденисесеаппс</span><span class="sxs-lookup"><span data-stu-id="67dbb-320">LetAppsGetDiagnosticInfo\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsgetdiagnosticinfo-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="67dbb-321">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="67dbb-321">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67dbb-322">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="67dbb-322">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="67dbb-323">ЛетаппсжетдиагностиЦинфо \_ усеринконтролофсесеаппс</span><span class="sxs-lookup"><span data-stu-id="67dbb-323">LetAppsGetDiagnosticInfo\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsgetdiagnosticinfo-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="67dbb-324">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="67dbb-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67dbb-325">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="67dbb-325">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="67dbb-326">летаппсрунинбаккграунд</span><span class="sxs-lookup"><span data-stu-id="67dbb-326">LetAppsRunInBackground</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsruninbackground)
</dt> <dd> <dl> <dt>

<span data-ttu-id="67dbb-327">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="67dbb-327">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="67dbb-328">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="67dbb-328">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="67dbb-329">Летаппсрунинбаккграунд \_ форцеалловсесеаппс</span><span class="sxs-lookup"><span data-stu-id="67dbb-329">LetAppsRunInBackground\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsruninbackground-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="67dbb-330">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="67dbb-330">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67dbb-331">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="67dbb-331">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="67dbb-332">Летаппсрунинбаккграунд \_ форцеденисесеаппс</span><span class="sxs-lookup"><span data-stu-id="67dbb-332">LetAppsRunInBackground\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsruninbackground-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="67dbb-333">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="67dbb-333">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67dbb-334">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="67dbb-334">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="67dbb-335">Летаппсрунинбаккграунд \_ усеринконтролофсесеаппс</span><span class="sxs-lookup"><span data-stu-id="67dbb-335">LetAppsRunInBackground\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsruninbackground-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="67dbb-336">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="67dbb-336">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67dbb-337">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="67dbb-337">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="67dbb-338">летаппссинквисдевицес</span><span class="sxs-lookup"><span data-stu-id="67dbb-338">LetAppsSyncWithDevices</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappssyncwithdevices)
</dt> <dd> <dl> <dt>

<span data-ttu-id="67dbb-339">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="67dbb-339">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="67dbb-340">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="67dbb-340">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="67dbb-341">Летаппссинквисдевицес \_ форцеалловсесеаппс</span><span class="sxs-lookup"><span data-stu-id="67dbb-341">LetAppsSyncWithDevices\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappssyncwithdevices-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="67dbb-342">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="67dbb-342">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67dbb-343">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="67dbb-343">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="67dbb-344">Летаппссинквисдевицес \_ форцеденисесеаппс</span><span class="sxs-lookup"><span data-stu-id="67dbb-344">LetAppsSyncWithDevices\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappssyncwithdevices-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="67dbb-345">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="67dbb-345">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67dbb-346">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="67dbb-346">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="67dbb-347">Летаппссинквисдевицес \_ усеринконтролофсесеаппс</span><span class="sxs-lookup"><span data-stu-id="67dbb-347">LetAppsSyncWithDevices\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappssyncwithdevices-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="67dbb-348">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="67dbb-348">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67dbb-349">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="67dbb-349">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="67dbb-350">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="67dbb-350">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67dbb-351">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="67dbb-351">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67dbb-352">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="67dbb-352">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67dbb-353">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="67dbb-353">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="67dbb-354">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="67dbb-354">Describes the full path to the parent node.</span></span> <span data-ttu-id="67dbb-355">Для этого класса строка имеет значение "./вендор/мсфт/Полици/ресулт"</span><span class="sxs-lookup"><span data-stu-id="67dbb-355">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> <dt>

[<span data-ttu-id="67dbb-356">публишусерактивитиес</span><span class="sxs-lookup"><span data-stu-id="67dbb-356">PublishUserActivities</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-publishuseractivities)
</dt> <dd> <dl> <dt>

<span data-ttu-id="67dbb-357">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="67dbb-357">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="67dbb-358">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="67dbb-358">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="67dbb-359">Требования</span><span class="sxs-lookup"><span data-stu-id="67dbb-359">Requirements</span></span>



| <span data-ttu-id="67dbb-360">Требование</span><span class="sxs-lookup"><span data-stu-id="67dbb-360">Requirement</span></span> | <span data-ttu-id="67dbb-361">Значение</span><span class="sxs-lookup"><span data-stu-id="67dbb-361">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67dbb-362">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="67dbb-362">Minimum supported client</span></span><br/> | <span data-ttu-id="67dbb-363">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="67dbb-363">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="67dbb-364">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="67dbb-364">Minimum supported server</span></span><br/> | <span data-ttu-id="67dbb-365">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="67dbb-365">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="67dbb-366">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="67dbb-366">Namespace</span></span><br/>                | <span data-ttu-id="67dbb-367">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="67dbb-367">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="67dbb-368">MOF</span><span class="sxs-lookup"><span data-stu-id="67dbb-368">MOF</span></span><br/>                      | <dl> <span data-ttu-id="67dbb-369"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="67dbb-369"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="67dbb-370">DLL</span><span class="sxs-lookup"><span data-stu-id="67dbb-370">DLL</span></span><br/>                      | <dl> <span data-ttu-id="67dbb-371"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="67dbb-371"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67dbb-372">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="67dbb-372">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67dbb-373">Использование сценариев PowerShell с WMI Bridge Provider</span><span class="sxs-lookup"><span data-stu-id="67dbb-373">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

