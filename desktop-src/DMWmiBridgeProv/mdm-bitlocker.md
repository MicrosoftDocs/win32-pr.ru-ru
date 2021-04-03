---
title: Класс MDM_BitLocker
description: Класс MDM \_ BitLocker используется предприятием для управления шифрованием компьютеров и устройств.
ms.assetid: e8bea6dc-8d3d-46d2-b2e3-9a4c547a639f
keywords:
- Класс MDM_BitLocker
- MDM_BitLocker класс, описание
topic_type:
- apiref
api_name:
- MDM_BitLocker
- MDM_BitLocker.InstanceID
- MDM_BitLocker.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b94db491333cada64b6287dc87ec233b420bf0f6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137538"
---
# <a name="mdm_bitlocker-class"></a><span data-ttu-id="f7071-105">\_Класс MDM BitLocker</span><span class="sxs-lookup"><span data-stu-id="f7071-105">MDM\_BitLocker class</span></span>

<span data-ttu-id="f7071-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="f7071-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="f7071-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="f7071-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="f7071-108">Класс MDM \_ BitLocker используется предприятием для управления шифрованием компьютеров и устройств.</span><span class="sxs-lookup"><span data-stu-id="f7071-108">The MDM\_BitLocker class is used by the enterprise to manage encryption of PCs and devices.</span></span>

<span data-ttu-id="f7071-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="f7071-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7071-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f7071-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_BitLocker
{
  string InstanceID;
  string ParentID;
  sint32 RequireStorageCardEncryption;
  sint32 RequireDeviceEncryption;
  string EncryptionMethodByDriveType;
  string SystemDrivesRequireStartupAuthentication;
  string SystemDrivesMinimumPINLength;
  string SystemDrivesRecoveryMessage;
  string SystemDrivesRecoveryOptions;
  string FixedDrivesRecoveryOptions;
  string FixedDrivesRequireEncryption;
  string RemovableDrivesRequireEncryption;
  sint32 AllowWarningForOtherDiskEncryption;
};
```

## <a name="members"></a><span data-ttu-id="f7071-111">Члены</span><span class="sxs-lookup"><span data-stu-id="f7071-111">Members</span></span>

<span data-ttu-id="f7071-112">Класс **MDM \_ BitLocker** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="f7071-112">The **MDM\_BitLocker** class has these types of members:</span></span>

-   [<span data-ttu-id="f7071-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="f7071-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f7071-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="f7071-114">Properties</span></span>

<span data-ttu-id="f7071-115">Класс **MDM \_ BitLocker** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="f7071-115">The **MDM\_BitLocker** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="f7071-116">алловварнингфоросердискенкриптион</span><span class="sxs-lookup"><span data-stu-id="f7071-116">AllowWarningForOtherDiskEncryption</span></span>](/windows/client-management/mdm/bitlocker-csp#allowwarningforotherdiskencryption)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7071-117">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="f7071-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f7071-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f7071-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f7071-119">енкриптионмесодбидриветипе</span><span class="sxs-lookup"><span data-stu-id="f7071-119">EncryptionMethodByDriveType</span></span>](/windows/client-management/mdm/bitlocker-csp#encryptionmethodbydrivetype)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7071-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f7071-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f7071-121">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f7071-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f7071-122">фикседдривесрековерйоптионс</span><span class="sxs-lookup"><span data-stu-id="f7071-122">FixedDrivesRecoveryOptions</span></span>](/windows/client-management/mdm/bitlocker-csp#fixeddrivesrecoveryoptions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7071-123">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f7071-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f7071-124">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f7071-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f7071-125">FixedDrivesRequireEncryption</span><span class="sxs-lookup"><span data-stu-id="f7071-125">FixedDrivesRequireEncryption</span></span>](/windows/client-management/mdm/bitlocker-csp#fixeddrivesrequireencryption)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7071-126">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f7071-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f7071-127">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f7071-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f7071-128">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="f7071-128">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7071-129">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f7071-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f7071-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f7071-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f7071-131">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f7071-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f7071-132">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="f7071-132">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7071-133">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f7071-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f7071-134">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f7071-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f7071-135">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f7071-135">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f7071-136">RemovableDrivesRequireEncryption</span><span class="sxs-lookup"><span data-stu-id="f7071-136">RemovableDrivesRequireEncryption</span></span>](/windows/client-management/mdm/bitlocker-csp#removabledrivesrequireencryption)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7071-137">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f7071-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f7071-138">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f7071-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f7071-139">RequireDeviceEncryption</span><span class="sxs-lookup"><span data-stu-id="f7071-139">RequireDeviceEncryption</span></span>](/windows/client-management/mdm/bitlocker-csp#requiredeviceencryption)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7071-140">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="f7071-140">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f7071-141">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f7071-141">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f7071-142">рекуиресторажекарденкриптион</span><span class="sxs-lookup"><span data-stu-id="f7071-142">RequireStorageCardEncryption</span></span>](/windows/client-management/mdm/bitlocker-csp#requirestoragecardencryption)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7071-143">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="f7071-143">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f7071-144">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f7071-144">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f7071-145">системдривесминимумпинленгс</span><span class="sxs-lookup"><span data-stu-id="f7071-145">SystemDrivesMinimumPINLength</span></span>](/windows/client-management/mdm/bitlocker-csp#systemdrivesminimumpinlength)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7071-146">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f7071-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f7071-147">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f7071-147">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f7071-148">системдривесрековеримессаже</span><span class="sxs-lookup"><span data-stu-id="f7071-148">SystemDrivesRecoveryMessage</span></span>](/windows/client-management/mdm/bitlocker-csp#systemdrivesrecoverymessage)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7071-149">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f7071-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f7071-150">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f7071-150">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f7071-151">системдривесрековерйоптионс</span><span class="sxs-lookup"><span data-stu-id="f7071-151">SystemDrivesRecoveryOptions</span></span>](/windows/client-management/mdm/bitlocker-csp#systemdrivesrecoveryoptions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7071-152">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f7071-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f7071-153">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f7071-153">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f7071-154">системдривесрекуирестартупаусентикатион</span><span class="sxs-lookup"><span data-stu-id="f7071-154">SystemDrivesRequireStartupAuthentication</span></span>](/windows/client-management/mdm/bitlocker-csp#systemdrivesrequirestartupauthentication)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7071-155">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f7071-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f7071-156">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f7071-156">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f7071-157">Требования</span><span class="sxs-lookup"><span data-stu-id="f7071-157">Requirements</span></span>



| <span data-ttu-id="f7071-158">Требование</span><span class="sxs-lookup"><span data-stu-id="f7071-158">Requirement</span></span> | <span data-ttu-id="f7071-159">Значение</span><span class="sxs-lookup"><span data-stu-id="f7071-159">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7071-160">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f7071-160">Minimum supported client</span></span><br/> | <span data-ttu-id="f7071-161">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="f7071-161">Windows 10 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f7071-162">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f7071-162">Minimum supported server</span></span><br/> | <span data-ttu-id="f7071-163">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="f7071-163">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="f7071-164">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f7071-164">Namespace</span></span><br/>                | <span data-ttu-id="f7071-165">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="f7071-165">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                              |
| <span data-ttu-id="f7071-166">MOF</span><span class="sxs-lookup"><span data-stu-id="f7071-166">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f7071-167"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f7071-167"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl> |
| <span data-ttu-id="f7071-168">DLL</span><span class="sxs-lookup"><span data-stu-id="f7071-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f7071-169"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f7071-169"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl>  |



 

