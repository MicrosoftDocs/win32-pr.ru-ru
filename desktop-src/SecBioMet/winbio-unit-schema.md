---
title: Структура WINBIO_UNIT_SCHEMA (Винбио \_ types. h)
description: Описывает возможности биометрического блока.
ms.assetid: b20adf18-2948-481f-9d12-8da17aa152f7
keywords:
- API структуры WINBIO_UNIT_SCHEMA биометрическая платформа Windows
- PWINBIO_UNIT_SCHEMA API биометрическая платформа Windows указателя структуры
topic_type:
- apiref
api_name:
- WINBIO_UNIT_SCHEMA
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c217be1e0c6bde740c815f5a990509a6a87ef0f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989342"
---
# <a name="winbio_unit_schema-structure"></a><span data-ttu-id="1d4af-105">\_ \_ Структура схемы единицы винбио</span><span class="sxs-lookup"><span data-stu-id="1d4af-105">WINBIO\_UNIT\_SCHEMA structure</span></span>

<span data-ttu-id="1d4af-106">Структура **\_ \_ схемы единицы винбио** описывает возможности биометрического блока.</span><span class="sxs-lookup"><span data-stu-id="1d4af-106">The **WINBIO\_UNIT\_SCHEMA** structure describes the capabilities of a biometric unit.</span></span> <span data-ttu-id="1d4af-107">Он используется функцией [**винбиоенумбиометрикунитс**](/windows/desktop/api/Winbio/nf-winbio-winbioenumbiometricunits) .</span><span class="sxs-lookup"><span data-stu-id="1d4af-107">It is used by the [**WinBioEnumBiometricUnits**](/windows/desktop/api/Winbio/nf-winbio-winbioenumbiometricunits) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d4af-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1d4af-108">Syntax</span></span>


```C++
typedef struct _WINBIO_UNIT_SCHEMA {
  WINBIO_UNIT_ID                  UnitId;
  WINBIO_POOL_TYPE                PoolType;
  WINBIO_BIOMETRIC_TYPE           BiometricFactor;
  WINBIO_BIOMETRIC_SENSOR_SUBTYPE SensorSubType;
  WINBIO_CAPABILITIES             Capabilities;
  WINBIO_STRING                   DeviceInstanceId;
  WINBIO_STRING                   Description;
  WINBIO_STRING                   Manufacturer;
  WINBIO_STRING                   Model;
  WINBIO_STRING                   SerialNumber;
  WINBIO_VERSION                  FirmwareVersion;
} WINBIO_UNIT_SCHEMA, *PWINBIO_UNIT_SCHEMA;
```



## <a name="members"></a><span data-ttu-id="1d4af-109">Члены</span><span class="sxs-lookup"><span data-stu-id="1d4af-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="1d4af-110">**унитид**</span><span class="sxs-lookup"><span data-stu-id="1d4af-110">**UnitId**</span></span>
</dt> <dd>

<span data-ttu-id="1d4af-111">Значение, идентифицирующее биометрическую единицу.</span><span class="sxs-lookup"><span data-stu-id="1d4af-111">A value that identifies the biometric unit.</span></span>

</dd> <dt>

<span data-ttu-id="1d4af-112">**пултипе**</span><span class="sxs-lookup"><span data-stu-id="1d4af-112">**PoolType**</span></span>
</dt> <dd>

<span data-ttu-id="1d4af-113">Значение типа **ulong** , указывающее тип биометрического блока.</span><span class="sxs-lookup"><span data-stu-id="1d4af-113">A **ULONG** value that specifies the type of the biometric unit.</span></span> <span data-ttu-id="1d4af-114">Может иметь одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="1d4af-114">This can be one of the following values:</span></span>



| <span data-ttu-id="1d4af-115">Значение</span><span class="sxs-lookup"><span data-stu-id="1d4af-115">Value</span></span>                                                                                                                                                                            | <span data-ttu-id="1d4af-116">Значение</span><span class="sxs-lookup"><span data-stu-id="1d4af-116">Meaning</span></span>                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_POOL_UNKNOWN"></span><span id="winbio_pool_unknown"></span><dl> <span data-ttu-id="1d4af-117"><dt>**\_неизвестный пул винбио \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1d4af-117"><dt>**WINBIO\_POOL\_UNKNOWN**</dt></span></span> </dl> | <span data-ttu-id="1d4af-118">Тип неизвестен.</span><span class="sxs-lookup"><span data-stu-id="1d4af-118">The type is unknown.</span></span><br/>                                                                            |
| <span id="WINBIO_POOL_SYSTEM"></span><span id="winbio_pool_system"></span><dl> <span data-ttu-id="1d4af-119"><dt>**\_система пула \_ винбио**</dt></span><span class="sxs-lookup"><span data-stu-id="1d4af-119"><dt>**WINBIO\_POOL\_SYSTEM**</dt></span></span> </dl>    | <span data-ttu-id="1d4af-120">Сеанс подключается к общей коллекции биометрических модулей, управляемых поставщиком услуг.</span><span class="sxs-lookup"><span data-stu-id="1d4af-120">The session connects to a shared collection of biometric units managed by the service provider.</span></span><br/> |
| <span id="WINBIO_POOL_PRIVATE"></span><span id="winbio_pool_private"></span><dl> <span data-ttu-id="1d4af-121"><dt>**\_частный пул \_ винбио**</dt></span><span class="sxs-lookup"><span data-stu-id="1d4af-121"><dt>**WINBIO\_POOL\_PRIVATE**</dt></span></span> </dl> | <span data-ttu-id="1d4af-122">Сеанс подключается к коллекции биометрических единиц, управляемых вызывающим объектом.</span><span class="sxs-lookup"><span data-stu-id="1d4af-122">The session connects to a collection of biometric units that are managed by the caller.</span></span><br/>         |



 

</dd> <dt>

<span data-ttu-id="1d4af-123">**биометрикфактор**</span><span class="sxs-lookup"><span data-stu-id="1d4af-123">**BiometricFactor**</span></span>
</dt> <dd>

<span data-ttu-id="1d4af-124">Значение типа, указывающее тип биометрического блока.</span><span class="sxs-lookup"><span data-stu-id="1d4af-124">A value that specifies the type of the biometric unit.</span></span> <span data-ttu-id="1d4af-125">В настоящее время поддерживается только **\_ \_ отпечаток типа винбио** .</span><span class="sxs-lookup"><span data-stu-id="1d4af-125">Only **WINBIO\_TYPE\_FINGERPRINT** is currently supported.</span></span>

</dd> <dt>

<span data-ttu-id="1d4af-126">**сенсорсубтипе**</span><span class="sxs-lookup"><span data-stu-id="1d4af-126">**SensorSubType**</span></span>
</dt> <dd>

<span data-ttu-id="1d4af-127">Подтип датчика, определенный для биометрического типа, заданного членом **биометрикфактор** .</span><span class="sxs-lookup"><span data-stu-id="1d4af-127">A sensor subtype defined for the biometric type specified by the **BiometricFactor** member.</span></span> <span data-ttu-id="1d4af-128">В настоящее время поддерживаются только типы отпечатков пальцев (**\_ тип \_ винбио**).</span><span class="sxs-lookup"><span data-stu-id="1d4af-128">Only fingerprint types (**WINBIO\_TYPE\_FINGERPRINT**) are currently supported.</span></span> <span data-ttu-id="1d4af-129">В настоящее время для отпечатков пальцев определены следующие подтипы:</span><span class="sxs-lookup"><span data-stu-id="1d4af-129">The following subtypes are currently defined for fingerprints:</span></span>

-   <span data-ttu-id="1d4af-130">\_неизвестный \_ ПОДТИП датчика \_ винбио</span><span class="sxs-lookup"><span data-stu-id="1d4af-130">WINBIO\_SENSOR\_SUBTYPE\_UNKNOWN</span></span>
-   <span data-ttu-id="1d4af-131">\_ \_ \_ считывание подтипа датчика винбио FP \_</span><span class="sxs-lookup"><span data-stu-id="1d4af-131">WINBIO\_FP\_SENSOR\_SUBTYPE\_SWIPE</span></span>
-   <span data-ttu-id="1d4af-132">\_ \_ \_ касание подтипа датчика FP винбио \_</span><span class="sxs-lookup"><span data-stu-id="1d4af-132">WINBIO\_FP\_SENSOR\_SUBTYPE\_TOUCH</span></span>

</dd> <dt>

<span data-ttu-id="1d4af-133">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="1d4af-133">**Capabilities**</span></span>
</dt> <dd>

<span data-ttu-id="1d4af-134">Битовая маска возможностей биометрического датчика.</span><span class="sxs-lookup"><span data-stu-id="1d4af-134">A bitmask of the biometric sensor capabilities.</span></span> <span data-ttu-id="1d4af-135">Это может быть побитовое **или** из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="1d4af-135">This can be a bitwise **OR** of the following values:</span></span>

-   <span data-ttu-id="1d4af-136">\_датчик возможностей \_ винбио</span><span class="sxs-lookup"><span data-stu-id="1d4af-136">WINBIO\_CAPABILITY\_SENSOR</span></span>
-   <span data-ttu-id="1d4af-137">\_Сопоставление возможностей \_ винбио</span><span class="sxs-lookup"><span data-stu-id="1d4af-137">WINBIO\_CAPABILITY\_MATCHING</span></span>
-   <span data-ttu-id="1d4af-138">\_ \_ база данных возможностей винбио</span><span class="sxs-lookup"><span data-stu-id="1d4af-138">WINBIO\_CAPABILITY\_DATABASE</span></span>
-   <span data-ttu-id="1d4af-139">\_Обработка возможностей \_ винбио</span><span class="sxs-lookup"><span data-stu-id="1d4af-139">WINBIO\_CAPABILITY\_PROCESSING</span></span>
-   <span data-ttu-id="1d4af-140">\_Шифрование возможностей \_ винбио</span><span class="sxs-lookup"><span data-stu-id="1d4af-140">WINBIO\_CAPABILITY\_ENCRYPTION</span></span>
-   <span data-ttu-id="1d4af-141">\_Навигация по ВОЗМОЖНОСТЯМ винбио \_</span><span class="sxs-lookup"><span data-stu-id="1d4af-141">WINBIO\_CAPABILITY\_NAVIGATION</span></span>
-   <span data-ttu-id="1d4af-142">\_индикатор возможности \_ винбио</span><span class="sxs-lookup"><span data-stu-id="1d4af-142">WINBIO\_CAPABILITY\_INDICATOR</span></span>
-   <span data-ttu-id="1d4af-143">\_ \_ виртуальный датчик возможностей \_ винбио</span><span class="sxs-lookup"><span data-stu-id="1d4af-143">WINBIO\_CAPABILITY\_VIRTUAL\_SENSOR</span></span>
    > [!Note]  
    > <span data-ttu-id="1d4af-144">Константа **\_ \_ виртуального \_ датчика возможностей Винбио** применяется только для Windows 10 и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="1d4af-144">The **WINBIO\_CAPABILITY\_VIRTUAL\_SENSOR** constant applies only for Windows 10 and later.</span></span>

     

</dd> <dt>

<span data-ttu-id="1d4af-145">**девицеинстанцеид**</span><span class="sxs-lookup"><span data-stu-id="1d4af-145">**DeviceInstanceId**</span></span>
</dt> <dd>

<span data-ttu-id="1d4af-146">Строковое значение, содержащее идентификатор устройства.</span><span class="sxs-lookup"><span data-stu-id="1d4af-146">A string value that contains the device ID.</span></span> <span data-ttu-id="1d4af-147">Строка может содержать до 256 символов Юникода, включая завершающий **нуль** -символ.</span><span class="sxs-lookup"><span data-stu-id="1d4af-147">The string can contain up to 256 Unicode characters including a terminating **NULL** character.</span></span>

</dd> <dt>

<span data-ttu-id="1d4af-148">**Описание**</span><span class="sxs-lookup"><span data-stu-id="1d4af-148">**Description**</span></span>
</dt> <dd>

<span data-ttu-id="1d4af-149">Строковое значение, содержащее описание биометрического блока.</span><span class="sxs-lookup"><span data-stu-id="1d4af-149">A string value that contains a description of the biometric unit.</span></span> <span data-ttu-id="1d4af-150">Строка может содержать до 256 символов Юникода, включая завершающий **нуль** -символ.</span><span class="sxs-lookup"><span data-stu-id="1d4af-150">The string can contain up to 256 Unicode characters including a terminating **NULL** character.</span></span>

</dd> <dt>

<span data-ttu-id="1d4af-151">**Производителя**</span><span class="sxs-lookup"><span data-stu-id="1d4af-151">**Manufacturer**</span></span>
</dt> <dd>

<span data-ttu-id="1d4af-152">Строковое значение, содержащее имя производителя.</span><span class="sxs-lookup"><span data-stu-id="1d4af-152">A string value that contains the name of the manufacturer.</span></span> <span data-ttu-id="1d4af-153">Строка может содержать до 256 символов Юникода, включая завершающий **нуль** -символ.</span><span class="sxs-lookup"><span data-stu-id="1d4af-153">The string can contain up to 256 Unicode characters including a terminating **NULL** character.</span></span>

</dd> <dt>

<span data-ttu-id="1d4af-154">**Модель**</span><span class="sxs-lookup"><span data-stu-id="1d4af-154">**Model**</span></span>
</dt> <dd>

<span data-ttu-id="1d4af-155">Строковое значение, содержащее номер модели биометрического блока.</span><span class="sxs-lookup"><span data-stu-id="1d4af-155">A string value that contains the model number of the biometric unit.</span></span> <span data-ttu-id="1d4af-156">Строка может содержать до 256 символов Юникода, включая завершающий **нуль** -символ.</span><span class="sxs-lookup"><span data-stu-id="1d4af-156">The string can contain up to 256 Unicode characters including a terminating **NULL** character.</span></span>

</dd> <dt>

<span data-ttu-id="1d4af-157">**Номер**</span><span class="sxs-lookup"><span data-stu-id="1d4af-157">**SerialNumber**</span></span>
</dt> <dd>

<span data-ttu-id="1d4af-158">Строка **в Юникоде**, заканчивающаяся нулем, которая содержит серийный номер биометрического блока.</span><span class="sxs-lookup"><span data-stu-id="1d4af-158">A **NULL**-terminated Unicode string that contains the serial number of the biometric unit.</span></span> <span data-ttu-id="1d4af-159">Строка может содержать до 256 символов Юникода, включая завершающий **нуль** -символ.</span><span class="sxs-lookup"><span data-stu-id="1d4af-159">The string can contain up to 256 Unicode characters including a terminating **NULL** character.</span></span>

</dd> <dt>

<span data-ttu-id="1d4af-160">**фирмвареверсион**</span><span class="sxs-lookup"><span data-stu-id="1d4af-160">**FirmwareVersion**</span></span>
</dt> <dd>

<span data-ttu-id="1d4af-161">Структура [**\_ версии винбио**](winbio-version.md) , которая содержит основной и дополнительный номера версий для биометрического блока.</span><span class="sxs-lookup"><span data-stu-id="1d4af-161">A [**WINBIO\_VERSION**](winbio-version.md) structure that contains the major and minor version numbers for the biometric unit.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1d4af-162">Требования</span><span class="sxs-lookup"><span data-stu-id="1d4af-162">Requirements</span></span>



| <span data-ttu-id="1d4af-163">Требование</span><span class="sxs-lookup"><span data-stu-id="1d4af-163">Requirement</span></span> | <span data-ttu-id="1d4af-164">Значение</span><span class="sxs-lookup"><span data-stu-id="1d4af-164">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d4af-165">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1d4af-165">Minimum supported client</span></span><br/> | <span data-ttu-id="1d4af-166">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="1d4af-166">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="1d4af-167">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1d4af-167">Minimum supported server</span></span><br/> | <span data-ttu-id="1d4af-168">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="1d4af-168">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="1d4af-169">Header</span><span class="sxs-lookup"><span data-stu-id="1d4af-169">Header</span></span><br/>                   | <dl> <span data-ttu-id="1d4af-170"><dt>Винбио \_ types. h (include винбио. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1d4af-170"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d4af-171">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1d4af-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d4af-172">Структуры клиентских приложений</span><span class="sxs-lookup"><span data-stu-id="1d4af-172">Client Application Structures</span></span>](client-application-structures.md)
</dt> <dt>

[<span data-ttu-id="1d4af-173">**винбиоенумбиометрикунитс**</span><span class="sxs-lookup"><span data-stu-id="1d4af-173">**WinBioEnumBiometricUnits**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbioenumbiometricunits)
</dt> </dl>

 

 





