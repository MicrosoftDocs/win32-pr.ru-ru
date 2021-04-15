---
description: Представляет возможности и управление логическими устройствами, связанными с памятью.
ms.assetid: 802c1c0e-7eab-4a17-9a29-6502ece6cb24
title: Класс CIM_Memory (Управление Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Memory
- CIM_Memory.Volatile
- CIM_Memory.ErrorMethodology
- CIM_Memory.StartingAddress
- CIM_Memory.EndingAddress
- CIM_Memory.ErrorInfo
- CIM_Memory.OtherErrorDescription
- CIM_Memory.CorrectableError
- CIM_Memory.ErrorTime
- CIM_Memory.ErrorAccess
- CIM_Memory.ErrorTransferSize
- CIM_Memory.ErrorData
- CIM_Memory.ErrorDataOrder
- CIM_Memory.ErrorAddress
- CIM_Memory.SystemLevelAddress
- CIM_Memory.ErrorResolution
- CIM_Memory.AdditionalErrorData
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 410d580542421aee153b610726bed1f438efbcde
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546031"
---
# <a name="cim_memory-class-hyper-v-management"></a><span data-ttu-id="f9bca-103">Класс CIM_Memory (Управление Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="f9bca-103">CIM_Memory class (Hyper-V management)</span></span>

<span data-ttu-id="f9bca-104">Представляет возможности и управление логическими устройствами, связанными с памятью.</span><span class="sxs-lookup"><span data-stu-id="f9bca-104">Represents the capabilities and management of memory-related logical devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9bca-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f9bca-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.8.0"), UMLPackagePath("CIM::Device::Memory"), AMENDMENT]
class CIM_Memory : CIM_StorageExtent
{
  boolean  Volatile;
  string   ErrorMethodology;
  uint64   StartingAddress;
  uint64   EndingAddress;
  uint16   ErrorInfo;
  string   OtherErrorDescription;
  boolean  CorrectableError;
  datetime ErrorTime;
  uint16   ErrorAccess;
  uint32   ErrorTransferSize;
  uint8    ErrorData[];
  uint16   ErrorDataOrder;
  uint64   ErrorAddress;
  boolean  SystemLevelAddress;
  uint64   ErrorResolution;
  uint8    AdditionalErrorData[];
};
```

## <a name="members"></a><span data-ttu-id="f9bca-106">Члены</span><span class="sxs-lookup"><span data-stu-id="f9bca-106">Members</span></span>

<span data-ttu-id="f9bca-107">Класс **\_ памяти CIM** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="f9bca-107">The **CIM\_Memory** class has these types of members:</span></span>

-   [<span data-ttu-id="f9bca-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="f9bca-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f9bca-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="f9bca-109">Properties</span></span>

<span data-ttu-id="f9bca-110">Класс **\_ памяти CIM** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="f9bca-110">The **CIM\_Memory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f9bca-111">**аддитионалеррордата**</span><span class="sxs-lookup"><span data-stu-id="f9bca-111">**AdditionalErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9bca-112">Тип данных: массив **Uint8**</span><span class="sxs-lookup"><span data-stu-id="f9bca-112">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="f9bca-113">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f9bca-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9bca-114">Квалификаторы: не [**рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ мемореррор. аддитионалеррордата"), **октетстринг**, [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Memory Device \| 005,18 "," MIF. \|Массив физической памяти DMTF \| 001,13 ")</span><span class="sxs-lookup"><span data-stu-id="f9bca-114">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_MemoryError.AdditionalErrorData"), **OctetString**, [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|005.18", "MIF.DMTF\|Physical Memory Array\|001.13")</span></span>
</dt> </dl>

<span data-ttu-id="f9bca-115">Массив октетов, который содержит дополнительные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="f9bca-115">An array of octets that contains additional error information.</span></span> <span data-ttu-id="f9bca-116">Например, синдром ECC или возврат битовой проверки, если используется методология ошибок на основе CRC.</span><span class="sxs-lookup"><span data-stu-id="f9bca-116">An example is ECC syndrome or the return of the check bits if a CRC-based error methodology is used.</span></span> <span data-ttu-id="f9bca-117">В последнем случае, если распознана одна разрядная ошибка и известен алгоритм CRC, можно определить точный бит, который завершился сбоем.</span><span class="sxs-lookup"><span data-stu-id="f9bca-117">In the latter case, if a single bit error is recognized and the CRC algorithm is known, it is possible to determine the exact bit that failed.</span></span>

<span data-ttu-id="f9bca-118">Если свойство **errorInfo** содержит значение 3 (ОК), это свойство не используется.</span><span class="sxs-lookup"><span data-stu-id="f9bca-118">If the **ErrorInfo** property contains "3" (OK), this property is not used.</span></span>

</dd> <dt>

<span data-ttu-id="f9bca-119">**корректаблиррор**</span><span class="sxs-lookup"><span data-stu-id="f9bca-119">**CorrectableError**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9bca-120">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="f9bca-120">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f9bca-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f9bca-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9bca-122">Квалификаторы: не [**рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ мемореррор. корректаблиррор"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Массив физической памяти DMTF \| 001,8 ")</span><span class="sxs-lookup"><span data-stu-id="f9bca-122">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_MemoryError.CorrectableError"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Memory Array\|001.8")</span></span>
</dt> </dl>

<span data-ttu-id="f9bca-123">**значение true** , если последняя ошибка является правильной. в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="f9bca-123">**true** if the most recent error is correctable; otherwise, **false**.</span></span> <span data-ttu-id="f9bca-124">Если свойство **errorInfo** содержит значение 3 (ОК), это свойство не используется.</span><span class="sxs-lookup"><span data-stu-id="f9bca-124">If the **ErrorInfo** property contains "3" (OK), this property is not used.</span></span>

</dd> <dt>

<span data-ttu-id="f9bca-125">**ендингаддресс**</span><span class="sxs-lookup"><span data-stu-id="f9bca-125">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9bca-126">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f9bca-126">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f9bca-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f9bca-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9bca-128">Квалификаторы: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("килобайты"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Массив памяти DMTF, сопоставленный адресам \| 001,4 "," MIF. \|Сопоставленные адреса памяти \| в формате DMTF 001,5 "), **Пунит** (" Byte \* 10 ^ 3 ")</span><span class="sxs-lookup"><span data-stu-id="f9bca-128">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("KiloBytes"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Array Mapped Addresses\|001.4", "MIF.DMTF\|Memory Device Mapped Addresses\|001.5"), **PUnit** ("byte \* 10^3")</span></span>
</dt> </dl>

<span data-ttu-id="f9bca-129">Конечный адрес, на который ссылается приложение или операционная система, сопоставленный контроллером памяти для объекта памяти.</span><span class="sxs-lookup"><span data-stu-id="f9bca-129">The ending address that is referenced by an application or operating system, and mapped by a memory controller for the memory object.</span></span> <span data-ttu-id="f9bca-130">Конечный адрес указывается в килобайтах.</span><span class="sxs-lookup"><span data-stu-id="f9bca-130">The ending address is specified in kilobytes.</span></span>

</dd> <dt>

<span data-ttu-id="f9bca-131">**ерроракцесс**</span><span class="sxs-lookup"><span data-stu-id="f9bca-131">**ErrorAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9bca-132">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f9bca-132">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f9bca-133">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f9bca-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9bca-134">Квалификаторы: не [**рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ мемореррор. ерроракцесс"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Массив физической памяти DMTF \| 001,10 ")</span><span class="sxs-lookup"><span data-stu-id="f9bca-134">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_MemoryError.ErrorAccess"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Memory Array\|001.10")</span></span>
</dt> </dl>

<span data-ttu-id="f9bca-135">Операция доступа к памяти, вызвавшая последнюю ошибку.</span><span class="sxs-lookup"><span data-stu-id="f9bca-135">The memory access operation that caused the last error.</span></span> <span data-ttu-id="f9bca-136">Если свойство **errorInfo** содержит значение 3 (ОК), это свойство не используется.</span><span class="sxs-lookup"><span data-stu-id="f9bca-136">If the **ErrorInfo** property contains "3" (OK), this property is not used.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="f9bca-137">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="f9bca-137">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f9bca-138">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="f9bca-138">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>

<span data-ttu-id="f9bca-139">**Чтение** (3)</span><span class="sxs-lookup"><span data-stu-id="f9bca-139">**Read** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write"></span><span id="write"></span><span id="WRITE"></span>

<span data-ttu-id="f9bca-140">**Запись** (4)</span><span class="sxs-lookup"><span data-stu-id="f9bca-140">**Write** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Partial_Write"></span><span id="partial_write"></span><span id="PARTIAL_WRITE"></span>

<span data-ttu-id="f9bca-141">**Частичная запись** (5)</span><span class="sxs-lookup"><span data-stu-id="f9bca-141">**Partial Write** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f9bca-142">**еррораддресс**</span><span class="sxs-lookup"><span data-stu-id="f9bca-142">**ErrorAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9bca-143">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f9bca-143">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f9bca-144">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f9bca-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9bca-145">Квалификаторы: не [**рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ мемореррор. стартингаддресс"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Memory Device \| 005,19 "," MIF. \|Массив физической памяти DMTF \| 001,14 ")</span><span class="sxs-lookup"><span data-stu-id="f9bca-145">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_MemoryError.StartingAddress"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|005.19", "MIF.DMTF\|Physical Memory Array\|001.14")</span></span>
</dt> </dl>

<span data-ttu-id="f9bca-146">Адрес последней ошибки памяти.</span><span class="sxs-lookup"><span data-stu-id="f9bca-146">The address of the last memory error.</span></span> <span data-ttu-id="f9bca-147">Тип ошибки описан в свойстве **errorInfo** .</span><span class="sxs-lookup"><span data-stu-id="f9bca-147">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="f9bca-148">Если свойство **errorInfo** содержит значение 3 (ОК), это свойство не используется.</span><span class="sxs-lookup"><span data-stu-id="f9bca-148">If the **ErrorInfo** property contains "3" (OK), this property is not used.</span></span>

</dd> <dt>

<span data-ttu-id="f9bca-149">**ErrorData**</span><span class="sxs-lookup"><span data-stu-id="f9bca-149">**ErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9bca-150">Тип данных: массив **Uint8**</span><span class="sxs-lookup"><span data-stu-id="f9bca-150">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="f9bca-151">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f9bca-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9bca-152">Квалификаторы: не [**рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ мемореррор. ErrorData"), **октетстринг**, [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Массив физической памяти DMTF \| 001,12 ")</span><span class="sxs-lookup"><span data-stu-id="f9bca-152">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_MemoryError.ErrorData"), **OctetString**, [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Memory Array\|001.12")</span></span>
</dt> </dl>

<span data-ttu-id="f9bca-153">Массив, содержащий данные, захваченные во время последнего ошибочного доступа к памяти.</span><span class="sxs-lookup"><span data-stu-id="f9bca-153">An array that contains data captured during the last erroneous memory access.</span></span> <span data-ttu-id="f9bca-154">Данные занимают первые n октетов массива, необходимых для хранения числа битов, заданных свойством **еррортрансферсизе** .</span><span class="sxs-lookup"><span data-stu-id="f9bca-154">The data occupies the first n octets of the array necessary to hold the number of bits specified by the **ErrorTransferSize** property.</span></span>

<span data-ttu-id="f9bca-155">Если свойство **еррортрансферсизе** содержит "0" (ОК), это свойство не используется.</span><span class="sxs-lookup"><span data-stu-id="f9bca-155">If the **ErrorTransferSize** property contains "0" (OK), this property is not used.</span></span>

</dd> <dt>

<span data-ttu-id="f9bca-156">**еррордатаордер**</span><span class="sxs-lookup"><span data-stu-id="f9bca-156">**ErrorDataOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9bca-157">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f9bca-157">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f9bca-158">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f9bca-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9bca-159">Квалификаторы: не [**рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ мемореррор. еррордатаордер")</span><span class="sxs-lookup"><span data-stu-id="f9bca-159">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_MemoryError.ErrorDataOrder")</span></span>
</dt> </dl>

<span data-ttu-id="f9bca-160">Упорядочивание данных, хранящихся в свойстве **ErrorData** .</span><span class="sxs-lookup"><span data-stu-id="f9bca-160">The ordering for data stored in the **ErrorData** property.</span></span> <span data-ttu-id="f9bca-161">Может быть указан "наименьший байт сначала" (значение = 1) или "наиболее значимый байт первым" (2).</span><span class="sxs-lookup"><span data-stu-id="f9bca-161">"Least Significant Byte First" (value=1) or "Most Significant Byte First" (2) can be specified.</span></span> <span data-ttu-id="f9bca-162">Если свойство **еррортрансферсизе** содержит "0" (ОК), это свойство не используется.</span><span class="sxs-lookup"><span data-stu-id="f9bca-162">If the **ErrorTransferSize** property contains "0" (OK), this property is not used.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f9bca-163">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="f9bca-163">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Least_Significant_Byte_First"></span><span id="least_significant_byte_first"></span><span id="LEAST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="f9bca-164">**Наименьший значащий байт первым** (1)</span><span class="sxs-lookup"><span data-stu-id="f9bca-164">**Least Significant Byte First** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Most_Significant_Byte_First"></span><span id="most_significant_byte_first"></span><span id="MOST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="f9bca-165">**Первый старший байт** (2)</span><span class="sxs-lookup"><span data-stu-id="f9bca-165">**Most Significant Byte First** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f9bca-166">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="f9bca-166">**ErrorInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9bca-167">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f9bca-167">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f9bca-168">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f9bca-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9bca-169">Квалификаторы: не [**рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ мемореррор. errorInfo"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Memory Device \| 005,12 "," MIF. \|Массив физической памяти DMTF \| 001,8 "), [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ память CIM**".**Осереррордескриптион**")</span><span class="sxs-lookup"><span data-stu-id="f9bca-169">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_MemoryError.ErrorInfo"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|005.12", "MIF.DMTF\|Physical Memory Array\|001.8"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Memory**.**OtherErrorDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="f9bca-170">Тип последней возникшей ошибки.</span><span class="sxs-lookup"><span data-stu-id="f9bca-170">The type of the last error to occur.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="f9bca-171">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="f9bca-171">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f9bca-172">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="f9bca-172">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="f9bca-173">**ОК** (3)</span><span class="sxs-lookup"><span data-stu-id="f9bca-173">**OK** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Bad_Read"></span><span id="bad_read"></span><span id="BAD_READ"></span>

<span data-ttu-id="f9bca-174">**Неправильное чтение** (4)</span><span class="sxs-lookup"><span data-stu-id="f9bca-174">**Bad Read** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Parity_Error"></span><span id="parity_error"></span><span id="PARITY_ERROR"></span>

<span data-ttu-id="f9bca-175">**Ошибка четности** (5)</span><span class="sxs-lookup"><span data-stu-id="f9bca-175">**Parity Error** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Single-Bit_Error"></span><span id="single-bit_error"></span><span id="SINGLE-BIT_ERROR"></span>

<span data-ttu-id="f9bca-176">**Одноразрядная ошибка** (6)</span><span class="sxs-lookup"><span data-stu-id="f9bca-176">**Single-Bit Error** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Double-Bit_Error"></span><span id="double-bit_error"></span><span id="DOUBLE-BIT_ERROR"></span>

<span data-ttu-id="f9bca-177">**Ошибка в двух битах** (7)</span><span class="sxs-lookup"><span data-stu-id="f9bca-177">**Double-Bit Error** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Multi-Bit_Error"></span><span id="multi-bit_error"></span><span id="MULTI-BIT_ERROR"></span>

<span data-ttu-id="f9bca-178">**Многоразрядная ошибка** (8)</span><span class="sxs-lookup"><span data-stu-id="f9bca-178">**Multi-Bit Error** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Nibble_Error"></span><span id="nibble_error"></span><span id="NIBBLE_ERROR"></span>

<span data-ttu-id="f9bca-179">**Ошибка в погрешностях** (9)</span><span class="sxs-lookup"><span data-stu-id="f9bca-179">**Nibble Error** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Checksum_Error"></span><span id="checksum_error"></span><span id="CHECKSUM_ERROR"></span>

<span data-ttu-id="f9bca-180">**Ошибка контрольной суммы** (10)</span><span class="sxs-lookup"><span data-stu-id="f9bca-180">**Checksum Error** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="CRC_Error"></span><span id="crc_error"></span><span id="CRC_ERROR"></span>

<span data-ttu-id="f9bca-181">**Ошибка CRC** (11)</span><span class="sxs-lookup"><span data-stu-id="f9bca-181">**CRC Error** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="f9bca-182">Не **определено** (12)</span><span class="sxs-lookup"><span data-stu-id="f9bca-182">**Undefined** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="f9bca-183">Не **определено** (13)</span><span class="sxs-lookup"><span data-stu-id="f9bca-183">**Undefined** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="f9bca-184">Не **определено** (14)</span><span class="sxs-lookup"><span data-stu-id="f9bca-184">**Undefined** (14)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f9bca-185">**еррормесодологи**</span><span class="sxs-lookup"><span data-stu-id="f9bca-185">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9bca-186">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f9bca-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f9bca-187">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f9bca-187">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9bca-188">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("еррормесодологи"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Массив физической памяти DMTF \| 001,7 ")</span><span class="sxs-lookup"><span data-stu-id="f9bca-188">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ErrorMethodology"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Memory Array\|001.7")</span></span>
</dt> </dl>

<span data-ttu-id="f9bca-189">Указывает, используются ли объектом памяти алгоритмы четности, алгоритмы CRC, ECC или другие механизмы.</span><span class="sxs-lookup"><span data-stu-id="f9bca-189">Indicates whether parity algorithms, CRC algorithms, ECC, or other mechanisms are used by the memory object.</span></span> <span data-ttu-id="f9bca-190">Также можно указать сведения об алгоритме.</span><span class="sxs-lookup"><span data-stu-id="f9bca-190">Details on the algorithm can also be supplied.</span></span>

</dd> <dt>

<span data-ttu-id="f9bca-191">**еррорресолутион**</span><span class="sxs-lookup"><span data-stu-id="f9bca-191">**ErrorResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9bca-192">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f9bca-192">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f9bca-193">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f9bca-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9bca-194">Квалификаторы: не [**рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ мемореррор. еррорресолутион"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Memory Device \| 005,21 "," MIF. \|Массив физической памяти DMTF \| 001,15 "), **Пунит** (" Byte ")</span><span class="sxs-lookup"><span data-stu-id="f9bca-194">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_MemoryError.ErrorResolution"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|005.21", "MIF.DMTF\|Physical Memory Array\|001.15"), **PUnit** ("byte")</span></span>
</dt> </dl>

<span data-ttu-id="f9bca-195">Диапазон в байтах, в котором может быть разрешена Последняя ошибка.</span><span class="sxs-lookup"><span data-stu-id="f9bca-195">The range, in bytes, in which the last error can be resolved.</span></span> <span data-ttu-id="f9bca-196">Например, если адреса ошибок разрешаются в бит 11, например на основе обычной страницы; затем ошибки могут быть разрешены на границы 4 КБ, а для этого свойства задано значение "4000".</span><span class="sxs-lookup"><span data-stu-id="f9bca-196">For example, if error addresses are resolved to bit 11, such as on a typical page basis; then the errors can be resolved to 4K boundaries, and this property is set to "4000".</span></span> <span data-ttu-id="f9bca-197">Если свойство **errorInfo** содержит значение 3 (ОК), это свойство не используется.</span><span class="sxs-lookup"><span data-stu-id="f9bca-197">If the **ErrorInfo** property contains "3" (OK), this property is not used.</span></span>

</dd> <dt>

<span data-ttu-id="f9bca-198">**ErrorTime**</span><span class="sxs-lookup"><span data-stu-id="f9bca-198">**ErrorTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9bca-199">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="f9bca-199">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f9bca-200">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f9bca-200">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9bca-201">Квалификаторы: не [**рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ мемореррор. еррортиме")</span><span class="sxs-lookup"><span data-stu-id="f9bca-201">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_MemoryError.ErrorTime")</span></span>
</dt> </dl>

<span data-ttu-id="f9bca-202">Время, когда произошла последняя ошибка памяти.</span><span class="sxs-lookup"><span data-stu-id="f9bca-202">The time when the last memory error occurred.</span></span> <span data-ttu-id="f9bca-203">Если свойство **errorInfo** содержит значение 3 (ОК), это свойство не используется.</span><span class="sxs-lookup"><span data-stu-id="f9bca-203">If the **ErrorInfo** property contains "3" (OK), this property is not used.</span></span>

</dd> <dt>

<span data-ttu-id="f9bca-204">**еррортрансферсизе**</span><span class="sxs-lookup"><span data-stu-id="f9bca-204">**ErrorTransferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9bca-205">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f9bca-205">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f9bca-206">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f9bca-206">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9bca-207">Квалификаторы: не [**рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ мемореррор. еррортрансферсизе"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("BITS"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Массив физической памяти DMTF \| 001,11 "), **Пунит** (" bit ")</span><span class="sxs-lookup"><span data-stu-id="f9bca-207">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_MemoryError.ErrorTransferSize"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Memory Array\|001.11"), **PUnit** ("bit")</span></span>
</dt> </dl>

<span data-ttu-id="f9bca-208">Размер передачи данных в битах, который привел к последней ошибке.</span><span class="sxs-lookup"><span data-stu-id="f9bca-208">The size of the data transfer, in bits, that caused the last error.</span></span> <span data-ttu-id="f9bca-209">"0" означает отсутствие ошибки.</span><span class="sxs-lookup"><span data-stu-id="f9bca-209">"0" indicates no error.</span></span> <span data-ttu-id="f9bca-210">Если свойство **errorInfo** содержит значение 3 (ОК), это свойство не используется.</span><span class="sxs-lookup"><span data-stu-id="f9bca-210">If the **ErrorInfo** property contains "3" (OK), this property is not used.</span></span>

</dd> <dt>

<span data-ttu-id="f9bca-211">**осереррордескриптион**</span><span class="sxs-lookup"><span data-stu-id="f9bca-211">**OtherErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9bca-212">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f9bca-212">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f9bca-213">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f9bca-213">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9bca-214">Квалификаторы: не [**рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ мемореррор. осереррордескриптион"), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ память CIM**".**ErrorInfo**")</span><span class="sxs-lookup"><span data-stu-id="f9bca-214">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_MemoryError.OtherErrorDescription"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Memory**.**ErrorInfo**")</span></span>
</dt> </dl>

<span data-ttu-id="f9bca-215">Описание типа ошибки, если свойство **ErrorType** имеет значение 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="f9bca-215">A description of the error type, when the **ErrorType** property is set to "1" (other).</span></span>

</dd> <dt>

<span data-ttu-id="f9bca-216">**стартингаддресс**</span><span class="sxs-lookup"><span data-stu-id="f9bca-216">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9bca-217">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f9bca-217">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f9bca-218">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f9bca-218">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9bca-219">Квалификаторы: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("килобайты"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Массив памяти DMTF, сопоставленный адресам \| 001,3 "," MIF. \|Сопоставленные адреса памяти \| в формате DMTF 001,4 "), **Пунит** (" Byte \* 10 ^ 3 ")</span><span class="sxs-lookup"><span data-stu-id="f9bca-219">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("KiloBytes"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Array Mapped Addresses\|001.3", "MIF.DMTF\|Memory Device Mapped Addresses\|001.4"), **PUnit** ("byte \* 10^3")</span></span>
</dt> </dl>

<span data-ttu-id="f9bca-220">Начальный адрес, на который ссылается приложение или операционная система, сопоставленный контроллером памяти для объекта памяти.</span><span class="sxs-lookup"><span data-stu-id="f9bca-220">The starting address that is referenced by an application or operating system, and mapped by a memory controller for the memory object.</span></span> <span data-ttu-id="f9bca-221">Начальный адрес указывается в килобайтах.</span><span class="sxs-lookup"><span data-stu-id="f9bca-221">The starting address is specified in kilobytes.</span></span>

</dd> <dt>

<span data-ttu-id="f9bca-222">**системлевеладдресс**</span><span class="sxs-lookup"><span data-stu-id="f9bca-222">**SystemLevelAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9bca-223">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="f9bca-223">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f9bca-224">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f9bca-224">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9bca-225">Квалификаторы: не [**рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_MemoryError.Sysтемлевеладдресс")</span><span class="sxs-lookup"><span data-stu-id="f9bca-225">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_MemoryError.SystemLevelAddress")</span></span>
</dt> </dl>

<span data-ttu-id="f9bca-226">**значение true** , если сведения об адресе в свойстве **еррораддресс** являются адресом системного уровня, и **значение false** , если это физический адрес.</span><span class="sxs-lookup"><span data-stu-id="f9bca-226">**true** if the address information in the **ErrorAddress** property is a system-level address, **false** if it is a physical address.</span></span>

</dd> <dt>

<span data-ttu-id="f9bca-227">**Независимо**</span><span class="sxs-lookup"><span data-stu-id="f9bca-227">**Volatile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9bca-228">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="f9bca-228">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f9bca-229">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f9bca-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f9bca-230">**значение true** , если память является временной; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="f9bca-230">**true** if the memory is volatile; otherwise, **false**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f9bca-231">Требования</span><span class="sxs-lookup"><span data-stu-id="f9bca-231">Requirements</span></span>



| <span data-ttu-id="f9bca-232">Требование</span><span class="sxs-lookup"><span data-stu-id="f9bca-232">Requirement</span></span> | <span data-ttu-id="f9bca-233">Значение</span><span class="sxs-lookup"><span data-stu-id="f9bca-233">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9bca-234">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f9bca-234">Minimum supported client</span></span><br/> | <span data-ttu-id="f9bca-235">Windows 8</span><span class="sxs-lookup"><span data-stu-id="f9bca-235">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="f9bca-236">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f9bca-236">Minimum supported server</span></span><br/> | <span data-ttu-id="f9bca-237">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f9bca-237">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="f9bca-238">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f9bca-238">Namespace</span></span><br/>                | <span data-ttu-id="f9bca-239">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="f9bca-239">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="f9bca-240">MOF</span><span class="sxs-lookup"><span data-stu-id="f9bca-240">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f9bca-241"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f9bca-241"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f9bca-242">DLL</span><span class="sxs-lookup"><span data-stu-id="f9bca-242">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f9bca-243"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f9bca-243"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f9bca-244">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f9bca-244">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9bca-245">**\_СТОРАЖЕЕКСТЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="f9bca-245">**CIM\_StorageExtent**</span></span>](cim-storageextent.md)
</dt> </dl>

 

