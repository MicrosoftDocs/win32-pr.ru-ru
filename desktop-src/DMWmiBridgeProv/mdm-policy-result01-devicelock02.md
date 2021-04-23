---
title: Класс MDM_Policy_Result01_DeviceLock02
description: '\_Класс политики MDM \_ Result01 \_ DeviceLock02 представляет доступные политики блокировки устройств.'
ms.assetid: 9aac25a8-8502-468f-9478-1ac4ccccaf0b
keywords:
- Класс MDM_Policy_Result01_DeviceLock02
- MDM_Policy_Result01_DeviceLock02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_DeviceLock02
- MDM_Policy_Result01_DeviceLock02.InstanceID
- MDM_Policy_Result01_DeviceLock02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa93236b99add5cb49e0b54aa10eab9e959ab01a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891986"
---
# <a name="mdm_policy_result01_devicelock02-class"></a><span data-ttu-id="c0ae6-105">\_Класс политики MDM \_ Result01 \_ DeviceLock02</span><span class="sxs-lookup"><span data-stu-id="c0ae6-105">MDM\_Policy\_Result01\_DeviceLock02 class</span></span>

<span data-ttu-id="c0ae6-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="c0ae6-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="c0ae6-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="c0ae6-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="c0ae6-108">Класс **\_ политики MDM \_ Result01 \_ DeviceLock02** представляет доступные политики блокировки устройств.</span><span class="sxs-lookup"><span data-stu-id="c0ae6-108">The **MDM\_Policy\_Result01\_DeviceLock02** class represents the device lock policies available.</span></span>

<span data-ttu-id="c0ae6-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="c0ae6-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0ae6-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c0ae6-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_DeviceLock02
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

## <a name="members"></a><span data-ttu-id="c0ae6-111">Члены</span><span class="sxs-lookup"><span data-stu-id="c0ae6-111">Members</span></span>

<span data-ttu-id="c0ae6-112">Класс **\_ политики MDM \_ Result01 \_ DeviceLock02** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="c0ae6-112">The **MDM\_Policy\_Result01\_DeviceLock02** class has these types of members:</span></span>

-   [<span data-ttu-id="c0ae6-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="c0ae6-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c0ae6-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="c0ae6-114">Properties</span></span>

<span data-ttu-id="c0ae6-115">Класс **\_ политики MDM \_ Result01 \_ DeviceLock02** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="c0ae6-115">The **MDM\_Policy\_Result01\_DeviceLock02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c0ae6-116">AllowScreenTimeoutWhileLockedUserConfig</span><span class="sxs-lookup"><span data-stu-id="c0ae6-116">AllowScreenTimeoutWhileLockedUserConfig</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0ae6-117">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="c0ae6-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c0ae6-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="c0ae6-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c0ae6-119">AllowSimpleDevicePassword</span><span class="sxs-lookup"><span data-stu-id="c0ae6-119">AllowSimpleDevicePassword</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-allowsimpledevicepassword)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0ae6-120">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="c0ae6-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c0ae6-121">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="c0ae6-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c0ae6-122">AlphanumericDevicePasswordRequired</span><span class="sxs-lookup"><span data-stu-id="c0ae6-122">AlphanumericDevicePasswordRequired</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-alphanumericdevicepasswordrequired)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0ae6-123">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="c0ae6-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c0ae6-124">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="c0ae6-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c0ae6-125">DevicePasswordEnabled</span><span class="sxs-lookup"><span data-stu-id="c0ae6-125">DevicePasswordEnabled</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-devicepasswordenabled)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0ae6-126">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="c0ae6-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c0ae6-127">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="c0ae6-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c0ae6-128">DevicePasswordExpiration</span><span class="sxs-lookup"><span data-stu-id="c0ae6-128">DevicePasswordExpiration</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-devicepasswordexpiration)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0ae6-129">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="c0ae6-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c0ae6-130">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="c0ae6-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c0ae6-131">DevicePasswordHistory</span><span class="sxs-lookup"><span data-stu-id="c0ae6-131">DevicePasswordHistory</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-devicepasswordhistory)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0ae6-132">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="c0ae6-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c0ae6-133">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="c0ae6-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c0ae6-134">енфорцелоккскринандлогонимаже</span><span class="sxs-lookup"><span data-stu-id="c0ae6-134">EnforceLockScreenAndLogonImage</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-enforcelockscreenandlogonimage)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0ae6-135">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c0ae6-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c0ae6-136">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="c0ae6-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c0ae6-137">енфорцелоккскринпровидер</span><span class="sxs-lookup"><span data-stu-id="c0ae6-137">EnforceLockScreenProvider</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0ae6-138">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c0ae6-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c0ae6-139">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="c0ae6-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c0ae6-140">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="c0ae6-140">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0ae6-141">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c0ae6-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c0ae6-142">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c0ae6-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0ae6-143">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c0ae6-143">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c0ae6-144">Определяет имя родительского узла.</span><span class="sxs-lookup"><span data-stu-id="c0ae6-144">Identifies the name of the parent node.</span></span> <span data-ttu-id="c0ae6-145">Для этого класса строка имеет значение "Девицелокк".</span><span class="sxs-lookup"><span data-stu-id="c0ae6-145">For this class, the string is "DeviceLock".</span></span>

</dd> <dt>

[<span data-ttu-id="c0ae6-146">MaxDevicePasswordFailedAttempts</span><span class="sxs-lookup"><span data-stu-id="c0ae6-146">MaxDevicePasswordFailedAttempts</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-maxdevicepasswordfailedattempts)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0ae6-147">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="c0ae6-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c0ae6-148">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="c0ae6-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c0ae6-149">MaxInactivityTimeDeviceLock</span><span class="sxs-lookup"><span data-stu-id="c0ae6-149">MaxInactivityTimeDeviceLock</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-maxinactivitytimedevicelock)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0ae6-150">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="c0ae6-150">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c0ae6-151">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="c0ae6-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c0ae6-152">MinDevicePasswordComplexCharacters</span><span class="sxs-lookup"><span data-stu-id="c0ae6-152">MinDevicePasswordComplexCharacters</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-mindevicepasswordcomplexcharacters)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0ae6-153">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="c0ae6-153">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c0ae6-154">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="c0ae6-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c0ae6-155">MinDevicePasswordLength</span><span class="sxs-lookup"><span data-stu-id="c0ae6-155">MinDevicePasswordLength</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-mindevicepasswordlength)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0ae6-156">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="c0ae6-156">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c0ae6-157">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="c0ae6-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c0ae6-158">минимумпассвордаже</span><span class="sxs-lookup"><span data-stu-id="c0ae6-158">MinimumPasswordAge</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-minimumpasswordage)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0ae6-159">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="c0ae6-159">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c0ae6-160">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="c0ae6-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c0ae6-161">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="c0ae6-161">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0ae6-162">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c0ae6-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c0ae6-163">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c0ae6-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0ae6-164">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c0ae6-164">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c0ae6-165">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="c0ae6-165">Describes the full path to the parent node.</span></span> <span data-ttu-id="c0ae6-166">Для этого класса строка имеет значение "./вендор/мсфт/Полици/ресулт"</span><span class="sxs-lookup"><span data-stu-id="c0ae6-166">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> <dt>

[<span data-ttu-id="c0ae6-167">превентлоккскринслидешов</span><span class="sxs-lookup"><span data-stu-id="c0ae6-167">PreventLockScreenSlideShow</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-preventlockscreenslideshow)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0ae6-168">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c0ae6-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c0ae6-169">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="c0ae6-169">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c0ae6-170">ScreenTimeoutWhileLocked</span><span class="sxs-lookup"><span data-stu-id="c0ae6-170">ScreenTimeoutWhileLocked</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0ae6-171">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="c0ae6-171">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c0ae6-172">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="c0ae6-172">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c0ae6-173">Требования</span><span class="sxs-lookup"><span data-stu-id="c0ae6-173">Requirements</span></span>



| <span data-ttu-id="c0ae6-174">Требование</span><span class="sxs-lookup"><span data-stu-id="c0ae6-174">Requirement</span></span> | <span data-ttu-id="c0ae6-175">Значение</span><span class="sxs-lookup"><span data-stu-id="c0ae6-175">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0ae6-176">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c0ae6-176">Minimum supported client</span></span><br/> | <span data-ttu-id="c0ae6-177">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="c0ae6-177">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c0ae6-178">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c0ae6-178">Minimum supported server</span></span><br/> | <span data-ttu-id="c0ae6-179">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="c0ae6-179">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="c0ae6-180">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="c0ae6-180">Namespace</span></span><br/>                | <span data-ttu-id="c0ae6-181">Корневой \\ CIMv2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="c0ae6-181">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="c0ae6-182">MOF</span><span class="sxs-lookup"><span data-stu-id="c0ae6-182">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c0ae6-183"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c0ae6-183"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="c0ae6-184">DLL</span><span class="sxs-lookup"><span data-stu-id="c0ae6-184">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c0ae6-185"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c0ae6-185"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0ae6-186">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c0ae6-186">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0ae6-187">Использование сценариев PowerShell с WMI Bridge Provider</span><span class="sxs-lookup"><span data-stu-id="c0ae6-187">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

