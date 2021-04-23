---
title: Класс MDM_Policy_Config01_DeviceLock02
description: '\_Класс политики MDM \_ Config01 \_ DeviceLock02 представляет доступные политики блокировки устройств.'
ms.assetid: 222081ec-c38f-481d-ae38-941fd1317197
keywords:
- Класс MDM_Policy_Config01_DeviceLock02
- MDM_Policy_Config01_DeviceLock02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_DeviceLock02
- MDM_Policy_Config01_DeviceLock02.InstanceID
- MDM_Policy_Config01_DeviceLock02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c5926912d276fbe04f75c161196c47d0f0dd384
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137263"
---
# <a name="mdm_policy_config01_devicelock02-class"></a><span data-ttu-id="e7c54-105">\_Класс политики MDM \_ Config01 \_ DeviceLock02</span><span class="sxs-lookup"><span data-stu-id="e7c54-105">MDM\_Policy\_Config01\_DeviceLock02 class</span></span>

<span data-ttu-id="e7c54-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="e7c54-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="e7c54-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="e7c54-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="e7c54-108">Класс **\_ политики MDM \_ Config01 \_ DeviceLock02** представляет доступные политики блокировки устройств.</span><span class="sxs-lookup"><span data-stu-id="e7c54-108">The **MDM\_Policy\_Config01\_DeviceLock02** class represents the device lock policies available.</span></span>

<span data-ttu-id="e7c54-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="e7c54-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7c54-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e7c54-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_DeviceLock02
{
  string InstanceID;
  string ParentID;
  sint32 AllowScreenTimeoutWhileLockedUserConfig;
  sint32 AllowSimpleDevicePassword;
  sint32 AlphanumericDevicePasswordRequired;
  sint32 DevicePasswordEnabled;
  sint32 DevicePasswordExpiration;
  sint32 DevicePasswordHistory;
  string EnforceLockScreenAndLogonImage;
  string EnforceLockScreenProvider;
  sint32 MinimumPasswordAge;
  sint32 MaxDevicePasswordFailedAttempts;
  sint32 MaxInactivityTimeDeviceLock;
  sint32 MinDevicePasswordComplexCharacters;
  sint32 MinDevicePasswordLength;
  sint32 ScreenTimeoutWhileLocked;
  string PreventLockScreenSlideShow;
};
```

## <a name="members"></a><span data-ttu-id="e7c54-111">Члены</span><span class="sxs-lookup"><span data-stu-id="e7c54-111">Members</span></span>

<span data-ttu-id="e7c54-112">Класс **\_ политики MDM \_ Config01 \_ DeviceLock02** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="e7c54-112">The **MDM\_Policy\_Config01\_DeviceLock02** class has these types of members:</span></span>

-   [<span data-ttu-id="e7c54-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="e7c54-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e7c54-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="e7c54-114">Properties</span></span>

<span data-ttu-id="e7c54-115">Класс **\_ политики MDM \_ Config01 \_ DeviceLock02** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="e7c54-115">The **MDM\_Policy\_Config01\_DeviceLock02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e7c54-116">AllowScreenTimeoutWhileLockedUserConfig</span><span class="sxs-lookup"><span data-stu-id="e7c54-116">AllowScreenTimeoutWhileLockedUserConfig</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7c54-117">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="e7c54-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e7c54-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="e7c54-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e7c54-119">AllowSimpleDevicePassword</span><span class="sxs-lookup"><span data-stu-id="e7c54-119">AllowSimpleDevicePassword</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-allowsimpledevicepassword)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7c54-120">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="e7c54-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e7c54-121">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="e7c54-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e7c54-122">AlphanumericDevicePasswordRequired</span><span class="sxs-lookup"><span data-stu-id="e7c54-122">AlphanumericDevicePasswordRequired</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-alphanumericdevicepasswordrequired)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7c54-123">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="e7c54-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e7c54-124">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="e7c54-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e7c54-125">DevicePasswordEnabled</span><span class="sxs-lookup"><span data-stu-id="e7c54-125">DevicePasswordEnabled</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-devicepasswordenabled)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7c54-126">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="e7c54-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e7c54-127">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="e7c54-127">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e7c54-128">Девицепассворденаблед не следует включать в значение Enabled (0), если Инструментарий WMI используется для установки политик Девицелокк EAS с заданными, что он включен по умолчанию в политике CSP для обратной совместимости с Windows 8. x.</span><span class="sxs-lookup"><span data-stu-id="e7c54-128">DevicePasswordEnabled should not be set to Enabled (0) when WMI is used to set the EAS DeviceLock policies given that it is Enabled by default in Policy CSP for back compat with Windows 8.x.</span></span> <span data-ttu-id="e7c54-129">Если для Девицепассворденаблед задано значение Enabled (0), CSP политики возвратит ошибку, сообщающую, что Девицепассворденаблед уже существует.</span><span class="sxs-lookup"><span data-stu-id="e7c54-129">If DevicePasswordEnabled is set to Enabled(0) then Policy CSP will return an error stating that DevicePasswordEnabled already exists.</span></span> <span data-ttu-id="e7c54-130">Windows 8. x не поддерживает политику Девицепассворд.</span><span class="sxs-lookup"><span data-stu-id="e7c54-130">Windows 8.x did not support DevicePassword policy.</span></span> <span data-ttu-id="e7c54-131">При отключении Девицепассворденаблед (1) это должен быть единственный набор политик из группы Девицелокк ниже.</span><span class="sxs-lookup"><span data-stu-id="e7c54-131">When disabling DevicePasswordEnabled  (1) then this should be the only policy set from the DeviceLock group of policies below.</span></span> <span data-ttu-id="e7c54-132">Политики перечислены ниже: >-Девицепассворденаблед является родительской политикой следующего:</span><span class="sxs-lookup"><span data-stu-id="e7c54-132">The policies are listed below: > - DevicePasswordEnabled is the parent policy of the following:</span></span>

-   <span data-ttu-id="e7c54-133">Девицепассворденаблед — это родительская политика для следующих элементов:</span><span class="sxs-lookup"><span data-stu-id="e7c54-133">DevicePasswordEnabled is the parent policy of the following:</span></span>
    -   <span data-ttu-id="e7c54-134">AllowSimpleDevicePassword</span><span class="sxs-lookup"><span data-stu-id="e7c54-134">AllowSimpleDevicePassword</span></span>
    -   <span data-ttu-id="e7c54-135">MinDevicePasswordLength</span><span class="sxs-lookup"><span data-stu-id="e7c54-135">MinDevicePasswordLength</span></span>
    -   <span data-ttu-id="e7c54-136">Алфанумерикдевицепассвордрекуиред — это родительская политика:</span><span class="sxs-lookup"><span data-stu-id="e7c54-136">AlphanumericDevicePasswordRequired is the parent policy of:</span></span>
        -   <span data-ttu-id="e7c54-137">MinDevicePasswordComplexCharacters</span><span class="sxs-lookup"><span data-stu-id="e7c54-137">MinDevicePasswordComplexCharacters</span></span> 
    -   <span data-ttu-id="e7c54-138">MaxDevicePasswordFailedAttempts</span><span class="sxs-lookup"><span data-stu-id="e7c54-138">MaxDevicePasswordFailedAttempts</span></span>
    -   <span data-ttu-id="e7c54-139">MaxInactivityTimeDeviceLock</span><span class="sxs-lookup"><span data-stu-id="e7c54-139">MaxInactivityTimeDeviceLock</span></span>

</dd> <dt>

[<span data-ttu-id="e7c54-140">DevicePasswordExpiration</span><span class="sxs-lookup"><span data-stu-id="e7c54-140">DevicePasswordExpiration</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-devicepasswordexpiration)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7c54-141">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="e7c54-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e7c54-142">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="e7c54-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e7c54-143">DevicePasswordHistory</span><span class="sxs-lookup"><span data-stu-id="e7c54-143">DevicePasswordHistory</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-devicepasswordhistory)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7c54-144">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="e7c54-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e7c54-145">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="e7c54-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e7c54-146">енфорцелоккскринандлогонимаже</span><span class="sxs-lookup"><span data-stu-id="e7c54-146">EnforceLockScreenAndLogonImage</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-enforcelockscreenandlogonimage)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7c54-147">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e7c54-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e7c54-148">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="e7c54-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e7c54-149">енфорцелоккскринпровидер</span><span class="sxs-lookup"><span data-stu-id="e7c54-149">EnforceLockScreenProvider</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7c54-150">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e7c54-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e7c54-151">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="e7c54-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e7c54-152">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="e7c54-152">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7c54-153">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e7c54-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e7c54-154">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e7c54-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e7c54-155">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e7c54-155">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="e7c54-156">Определяет имя родительского узла.</span><span class="sxs-lookup"><span data-stu-id="e7c54-156">Identifies the name of the parent node.</span></span> <span data-ttu-id="e7c54-157">Для этого класса строка имеет значение "Девицелокк".</span><span class="sxs-lookup"><span data-stu-id="e7c54-157">For this class, the string is "DeviceLock".</span></span>

</dd> <dt>

[<span data-ttu-id="e7c54-158">MaxDevicePasswordFailedAttempts</span><span class="sxs-lookup"><span data-stu-id="e7c54-158">MaxDevicePasswordFailedAttempts</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-maxdevicepasswordfailedattempts)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7c54-159">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="e7c54-159">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e7c54-160">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="e7c54-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e7c54-161">MaxInactivityTimeDeviceLock</span><span class="sxs-lookup"><span data-stu-id="e7c54-161">MaxInactivityTimeDeviceLock</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-maxinactivitytimedevicelock)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7c54-162">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="e7c54-162">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e7c54-163">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="e7c54-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e7c54-164">MinDevicePasswordComplexCharacters</span><span class="sxs-lookup"><span data-stu-id="e7c54-164">MinDevicePasswordComplexCharacters</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-mindevicepasswordcomplexcharacters)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7c54-165">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="e7c54-165">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e7c54-166">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="e7c54-166">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e7c54-167">MinDevicePasswordLength</span><span class="sxs-lookup"><span data-stu-id="e7c54-167">MinDevicePasswordLength</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-mindevicepasswordlength)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7c54-168">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="e7c54-168">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e7c54-169">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="e7c54-169">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e7c54-170">минимумпассвордаже</span><span class="sxs-lookup"><span data-stu-id="e7c54-170">MinimumPasswordAge</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-minimumpasswordage)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7c54-171">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="e7c54-171">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e7c54-172">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="e7c54-172">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e7c54-173">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="e7c54-173">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7c54-174">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e7c54-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e7c54-175">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e7c54-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e7c54-176">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e7c54-176">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="e7c54-177">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="e7c54-177">Describes the full path to the parent node.</span></span> <span data-ttu-id="e7c54-178">Для этого класса строка имеет значение "./вендор/мсфт/Полици/конфиг"</span><span class="sxs-lookup"><span data-stu-id="e7c54-178">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> <dt>

[<span data-ttu-id="e7c54-179">превентлоккскринслидешов</span><span class="sxs-lookup"><span data-stu-id="e7c54-179">PreventLockScreenSlideShow</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-preventlockscreenslideshow)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7c54-180">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e7c54-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e7c54-181">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="e7c54-181">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e7c54-182">ScreenTimeoutWhileLocked</span><span class="sxs-lookup"><span data-stu-id="e7c54-182">ScreenTimeoutWhileLocked</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7c54-183">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="e7c54-183">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e7c54-184">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="e7c54-184">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e7c54-185">Требования</span><span class="sxs-lookup"><span data-stu-id="e7c54-185">Requirements</span></span>



| <span data-ttu-id="e7c54-186">Требование</span><span class="sxs-lookup"><span data-stu-id="e7c54-186">Requirement</span></span> | <span data-ttu-id="e7c54-187">Значение</span><span class="sxs-lookup"><span data-stu-id="e7c54-187">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7c54-188">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e7c54-188">Minimum supported client</span></span><br/> | <span data-ttu-id="e7c54-189">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="e7c54-189">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e7c54-190">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e7c54-190">Minimum supported server</span></span><br/> | <span data-ttu-id="e7c54-191">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="e7c54-191">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="e7c54-192">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="e7c54-192">Namespace</span></span><br/>                | <span data-ttu-id="e7c54-193">Корневой \\ CIMv2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="e7c54-193">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="e7c54-194">MOF</span><span class="sxs-lookup"><span data-stu-id="e7c54-194">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e7c54-195"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e7c54-195"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="e7c54-196">DLL</span><span class="sxs-lookup"><span data-stu-id="e7c54-196">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e7c54-197"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e7c54-197"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7c54-198">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e7c54-198">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7c54-199">Использование сценариев PowerShell с WMI Bridge Provider</span><span class="sxs-lookup"><span data-stu-id="e7c54-199">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

