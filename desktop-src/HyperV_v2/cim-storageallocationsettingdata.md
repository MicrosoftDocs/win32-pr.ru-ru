---
description: Представляет параметры для размещения виртуального хранилища.
ms.assetid: 128fd3e9-8759-4b2f-a881-d34e89c539ac
title: Класс CIM_StorageAllocationSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_StorageAllocationSettingData
- CIM_StorageAllocationSettingData.VirtualResourceBlockSize
- CIM_StorageAllocationSettingData.VirtualQuantity
- CIM_StorageAllocationSettingData.VirtualQuantityUnits
- CIM_StorageAllocationSettingData.Access
- CIM_StorageAllocationSettingData.HostResourceBlockSize
- CIM_StorageAllocationSettingData.Reservation
- CIM_StorageAllocationSettingData.Limit
- CIM_StorageAllocationSettingData.HostExtentStartingAddress
- CIM_StorageAllocationSettingData.HostExtentName
- CIM_StorageAllocationSettingData.HostExtentNameFormat
- CIM_StorageAllocationSettingData.OtherHostExtentNameFormat
- CIM_StorageAllocationSettingData.HostExtentNameNamespace
- CIM_StorageAllocationSettingData.OtherHostExtentNameNamespace
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e66322f20987e2d1f99042430f0f57cdc2e399d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813849"
---
# <a name="cim_storageallocationsettingdata-class"></a><span data-ttu-id="5d6e0-103">\_Класс CIM сторажеаллокатионсеттингдата</span><span class="sxs-lookup"><span data-stu-id="5d6e0-103">CIM\_StorageAllocationSettingData class</span></span>

<span data-ttu-id="5d6e0-104">Представляет параметры для размещения виртуального хранилища.</span><span class="sxs-lookup"><span data-stu-id="5d6e0-104">Represents settings for the allocation of virtual storage.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d6e0-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5d6e0-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::Resource"), AMENDMENT]
class CIM_StorageAllocationSettingData : CIM_ResourceAllocationSettingData
{
  uint64 VirtualResourceBlockSize;
  uint64 VirtualQuantity;
  string VirtualQuantityUnits = "count(fixed size block)";
  uint16 Access;
  uint64 HostResourceBlockSize;
  uint64 Reservation;
  uint64 Limit;
  uint64 HostExtentStartingAddress;
  string HostExtentName;
  uint16 HostExtentNameFormat;
  string OtherHostExtentNameFormat;
  uint16 HostExtentNameNamespace;
  string OtherHostExtentNameNamespace;
};
```

## <a name="members"></a><span data-ttu-id="5d6e0-106">Члены</span><span class="sxs-lookup"><span data-stu-id="5d6e0-106">Members</span></span>

<span data-ttu-id="5d6e0-107">Класс **CIM \_ сторажеаллокатионсеттингдата** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="5d6e0-107">The **CIM\_StorageAllocationSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="5d6e0-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="5d6e0-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5d6e0-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="5d6e0-109">Properties</span></span>

<span data-ttu-id="5d6e0-110">Класс **CIM \_ сторажеаллокатионсеттингдата** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="5d6e0-110">The **CIM\_StorageAllocationSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5d6e0-111">**Доступ**</span><span class="sxs-lookup"><span data-stu-id="5d6e0-111">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d6e0-112">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5d6e0-112">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5d6e0-113">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5d6e0-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d6e0-114">Квалификаторы: [**моделкорреспонденце**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ сторажеекстент**](cim-storageextent.md).**Доступ**")</span><span class="sxs-lookup"><span data-stu-id="5d6e0-114">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_StorageExtent**](cim-storageextent.md).**Access**")</span></span>
</dt> </dl>

<span data-ttu-id="5d6e0-115">Поддержка выделения памяти для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="5d6e0-115">The read/write support of the storage allocation.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5d6e0-116">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="5d6e0-116">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="5d6e0-117">**Для чтения** (1)</span><span class="sxs-lookup"><span data-stu-id="5d6e0-117">**Readable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="5d6e0-118">**Доступный для записи** (2)</span><span class="sxs-lookup"><span data-stu-id="5d6e0-118">**Writeable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="5d6e0-119">**Поддерживается чтение и запись** (3)</span><span class="sxs-lookup"><span data-stu-id="5d6e0-119">**Read/Write Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="5d6e0-120">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="5d6e0-120">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5d6e0-121">**хостекстентнаме**</span><span class="sxs-lookup"><span data-stu-id="5d6e0-121">**HostExtentName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d6e0-122">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="5d6e0-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5d6e0-123">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5d6e0-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d6e0-124">Квалификаторы: [**моделкорреспонденце**](../wmisdk/standard-qualifiers.md) ("**CIM \_ сторажеаллокатионсеттингдата**.**Хостекстентнамеформат**","**CIM \_ сторажеаллокатионсеттингдата**.**Хостекстентнаменамеспаце**","[**CIM \_ сторажеекстент**](cim-storageextent.md).**Name**")</span><span class="sxs-lookup"><span data-stu-id="5d6e0-124">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM\_StorageAllocationSettingData**.**HostExtentNameFormat**", "**CIM\_StorageAllocationSettingData**.**HostExtentNameNamespace**", "[**CIM\_StorageExtent**](cim-storageextent.md).**Name**")</span></span>
</dt> </dl>

<span data-ttu-id="5d6e0-125">Уникальный идентификатор области хранения узла.</span><span class="sxs-lookup"><span data-stu-id="5d6e0-125">A unique identifier of the host storage extent.</span></span>

</dd> <dt>

<span data-ttu-id="5d6e0-126">**хостекстентнамеформат**</span><span class="sxs-lookup"><span data-stu-id="5d6e0-126">**HostExtentNameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d6e0-127">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5d6e0-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5d6e0-128">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5d6e0-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d6e0-129">Квалификаторы: [**моделкорреспонденце**](../wmisdk/standard-qualifiers.md) ("**CIM \_ сторажеаллокатионсеттингдата**.**Хостекстентнаме**","**CIM \_ сторажеаллокатионсеттингдата**.**Осерхостекстентнамеформат**","[**CIM \_ сторажеекстент**](cim-storageextent.md).**Намеформат**")</span><span class="sxs-lookup"><span data-stu-id="5d6e0-129">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM\_StorageAllocationSettingData**.**HostExtentName**", "**CIM\_StorageAllocationSettingData**.**OtherHostExtentNameFormat**", "[**CIM\_StorageExtent**](cim-storageextent.md).**NameFormat**")</span></span>
</dt> </dl>

<span data-ttu-id="5d6e0-130">Формат значения свойства **хостекстентнаме** .</span><span class="sxs-lookup"><span data-stu-id="5d6e0-130">The format that of the **HostExtentName** property value.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5d6e0-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="5d6e0-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="5d6e0-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="5d6e0-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="SNVM"></span><span id="snvm"></span>

<span data-ttu-id="5d6e0-133"><span id="SNVM"></span><span id="snvm"></span>**Снвм** (7)</span><span class="sxs-lookup"><span data-stu-id="5d6e0-133"><span id="SNVM"></span><span id="snvm"></span>**SNVM** (7)</span></span>


</dt> <dd>

<span data-ttu-id="5d6e0-134">Серийный номер, поставщик/модель (СНВМ) СНВМ — 3 строки, представляющие имя поставщика, название продукта в пространстве имен поставщика и серийный номер в пространстве имен модели.</span><span class="sxs-lookup"><span data-stu-id="5d6e0-134">Serial Number/Vendor/Model (SNVM) SNVM is 3 strings representing the vendor name, product name within the vendor namespace, and the serial number within the model namespace.</span></span> <span data-ttu-id="5d6e0-135">Строки разделяются символом "+".</span><span class="sxs-lookup"><span data-stu-id="5d6e0-135">Strings are delimited with a '+'.</span></span> <span data-ttu-id="5d6e0-136">Могут быть включены пробелы и быть значимыми.</span><span class="sxs-lookup"><span data-stu-id="5d6e0-136">Spaces may be included and are significant.</span></span> <span data-ttu-id="5d6e0-137">Серийный номер — это текстовое представление серийного номера в шестнадцатеричном верхнем регистре.</span><span class="sxs-lookup"><span data-stu-id="5d6e0-137">The serial number is the text representation of the serial number in hexadecimal upper case.</span></span> <span data-ttu-id="5d6e0-138">Представляет идентификатор поставщика и модели из данных запроса SCSI. поле "поставщик" должно иметь ширину 8 символов, а поле "продукт" должно иметь ширину 16 символов.</span><span class="sxs-lookup"><span data-stu-id="5d6e0-138">This represents the vendor and model ID from SCSI Inquiry data; the vendor field MUST be 8 characters wide and the product field MUST be 16 characters wide.</span></span> <span data-ttu-id="5d6e0-139">Например,</span><span class="sxs-lookup"><span data-stu-id="5d6e0-139">For example,</span></span>

<span data-ttu-id="5d6e0-140">"Acme \_ \_ \_ \_ + Super Disk \_ \_ \_ \_ \_ \_ + 124437458" ( \_ является символом пробела)</span><span class="sxs-lookup"><span data-stu-id="5d6e0-140">'ACME\_\_\_\_+SUPER DISK\_\_\_\_\_\_+124437458' (\_ is a space character)</span></span>

</dd> <dt>

<span id="NAA"></span><span id="naa"></span>

<span data-ttu-id="5d6e0-141"><span id="NAA"></span><span id="naa"></span>**Удаляем** (9)</span><span class="sxs-lookup"><span data-stu-id="5d6e0-141"><span id="NAA"></span><span id="naa"></span>**NAA** (9)</span></span>


</dt> <dd>

<span data-ttu-id="5d6e0-142">9 = УДАЛЯЕМ в виде универсального формата.</span><span class="sxs-lookup"><span data-stu-id="5d6e0-142">9 = NAA as a generic format.</span></span> <span data-ttu-id="5d6e0-143">См.</span><span class="sxs-lookup"><span data-stu-id="5d6e0-143">See</span></span>

<span data-ttu-id="5d6e0-144"> https://standards.ieee.org/regauth/oui/tutorials/fibrecomp\_id.html.</span><span class="sxs-lookup"><span data-stu-id="5d6e0-144">https://standards.ieee.org/regauth/oui/tutorials/fibrecomp\_id.html.</span></span> <span data-ttu-id="5d6e0-145">В формате 16 или 32 неразделенных шестнадцатеричных символов в верхнем регистре (2 за двоичный байт).</span><span class="sxs-lookup"><span data-stu-id="5d6e0-145">Formatted as 16 or 32 unseparated uppercase hex characters (2 per binary byte).</span></span>

<span data-ttu-id="5d6e0-146">Например, "21000020372D3C73"</span><span class="sxs-lookup"><span data-stu-id="5d6e0-146">For example '21000020372D3C73'</span></span>

</dd> <dt>

<span id="EUI64"></span><span id="eui64"></span>

<span data-ttu-id="5d6e0-147"><span id="EUI64"></span><span id="eui64"></span>**EUI64** (10)</span><span class="sxs-lookup"><span data-stu-id="5d6e0-147"><span id="EUI64"></span><span id="eui64"></span>**EUI64** (10)</span></span>


</dt> <dd>

<span data-ttu-id="5d6e0-148">EUI в качестве универсального формата (EUI64) см. в разделе</span><span class="sxs-lookup"><span data-stu-id="5d6e0-148">EUI as a generic format (EUI64) See</span></span>

<span data-ttu-id="5d6e0-149"> https://standards.ieee.org/content/dam/ieee-standards/standards/web/documents/tutorials/eui.pdf.</span><span class="sxs-lookup"><span data-stu-id="5d6e0-149">https://standards.ieee.org/content/dam/ieee-standards/standards/web/documents/tutorials/eui.pdf.</span></span>

</dd> <dt>

<span id="T10VID"></span><span id="t10vid"></span>

<span data-ttu-id="5d6e0-150"><span id="T10VID"></span><span id="t10vid"></span>**T10VID** (11)</span><span class="sxs-lookup"><span data-stu-id="5d6e0-150"><span id="T10VID"></span><span id="t10vid"></span>**T10VID** (11)</span></span>


</dt> <dd>

<span data-ttu-id="5d6e0-151">Формат идентификатора поставщика T10, возвращенный SCSI-запросом VPD стр 83, тип идентификатора 1.</span><span class="sxs-lookup"><span data-stu-id="5d6e0-151">T10 vendor identifier format as returned by SCSI Inquiry VPD page 83, identifier type 1.</span></span> <span data-ttu-id="5d6e0-152">См. спецификацию T10 SPC-3.</span><span class="sxs-lookup"><span data-stu-id="5d6e0-152">See T10 SPC-3 specification.</span></span> <span data-ttu-id="5d6e0-153">Это 8-байтовый идентификатор поставщика ASCII из реестра T10, за которым следует идентификатор ASCII, определяемый поставщиком. разрешены пробелы.</span><span class="sxs-lookup"><span data-stu-id="5d6e0-153">This is the 8-byte ASCII vendor ID from the T10 registry followed by a vendor specific ASCII identifier; spaces are permitted.</span></span> <span data-ttu-id="5d6e0-154">Для томов, отличных от SCSI, может быть наиболее подходящий вариант "СНВМ".</span><span class="sxs-lookup"><span data-stu-id="5d6e0-154">For non SCSI volumes, 'SNVM' may be the most appropriate choice.</span></span>

</dd> <dt>

<span id="OS_Device_Name"></span><span id="os_device_name"></span><span id="OS_DEVICE_NAME"></span>

<span data-ttu-id="5d6e0-155"><span id="OS_Device_Name"></span><span id="os_device_name"></span><span id="OS_DEVICE_NAME"></span>**Имя устройства ОС** (12)</span><span class="sxs-lookup"><span data-stu-id="5d6e0-155"><span id="OS_Device_Name"></span><span id="os_device_name"></span><span id="OS_DEVICE_NAME"></span>**OS Device Name** (12)</span></span>


</dt> <dd>

<span data-ttu-id="5d6e0-156">Имя устройства ОС (для Логикалдискс).</span><span class="sxs-lookup"><span data-stu-id="5d6e0-156">OS Device Name (for LogicalDisks).</span></span> <span data-ttu-id="5d6e0-157">Дополнительные сведения см. в описании имени диска LogicalDisk.</span><span class="sxs-lookup"><span data-stu-id="5d6e0-157">See LogicalDisk Name description for details.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="5d6e0-158"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="5d6e0-158"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5d6e0-159">**хостекстентнаменамеспаце**</span><span class="sxs-lookup"><span data-stu-id="5d6e0-159">**HostExtentNameNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d6e0-160">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5d6e0-160">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5d6e0-161">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5d6e0-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d6e0-162">Квалификаторы: [**моделкорреспонденце**](../wmisdk/standard-qualifiers.md) ("**CIM \_ сторажеаллокатионсеттингдата**.**Хостекстентнаме**","**CIM \_ сторажеаллокатионсеттингдата**.**Осерхостекстентнаменамеспаце**","**CIM \_ сторажеаллокатионсеттингдата**.**Хостекстентнамеформат**","[**CIM \_ сторажеекстент**](cim-storageextent.md).**Пространство имен**")</span><span class="sxs-lookup"><span data-stu-id="5d6e0-162">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM\_StorageAllocationSettingData**.**HostExtentName**", "**CIM\_StorageAllocationSettingData**.**OtherHostExtentNameNamespace**", "**CIM\_StorageAllocationSettingData**.**HostExtentNameFormat**", "[**CIM\_StorageExtent**](cim-storageextent.md).**Namespace**")</span></span>
</dt> </dl>

<span data-ttu-id="5d6e0-163">Формат имени для свойства **Name** .</span><span class="sxs-lookup"><span data-stu-id="5d6e0-163">The naming format for the **Name** property.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5d6e0-164">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="5d6e0-164">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="5d6e0-165">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="5d6e0-165">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="VPD83Type3"></span><span id="vpd83type3"></span><span id="VPD83TYPE3"></span>

<span data-ttu-id="5d6e0-166">**VPD83Type3** (2)</span><span class="sxs-lookup"><span data-stu-id="5d6e0-166">**VPD83Type3** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="VPD83Type2"></span><span id="vpd83type2"></span><span id="VPD83TYPE2"></span>

<span data-ttu-id="5d6e0-167">**VPD83Type2** (3)</span><span class="sxs-lookup"><span data-stu-id="5d6e0-167">**VPD83Type2** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="VPD83Type1"></span><span id="vpd83type1"></span><span id="VPD83TYPE1"></span>

<span data-ttu-id="5d6e0-168">**VPD83Type1** (4)</span><span class="sxs-lookup"><span data-stu-id="5d6e0-168">**VPD83Type1** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="VPD80"></span><span id="vpd80"></span>

<span data-ttu-id="5d6e0-169">**VPD80** (5)</span><span class="sxs-lookup"><span data-stu-id="5d6e0-169">**VPD80** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="NodeWWN"></span><span id="nodewwn"></span><span id="NODEWWN"></span>

<span data-ttu-id="5d6e0-170">**Нодеввн** (6)</span><span class="sxs-lookup"><span data-stu-id="5d6e0-170">**NodeWWN** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="SNVM"></span><span id="snvm"></span>

<span data-ttu-id="5d6e0-171">**Снвм** (7)</span><span class="sxs-lookup"><span data-stu-id="5d6e0-171">**SNVM** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_Device_Namespace"></span><span id="os_device_namespace"></span><span id="OS_DEVICE_NAMESPACE"></span>

<span data-ttu-id="5d6e0-172">**Пространство имен устройств ОС** (8)</span><span class="sxs-lookup"><span data-stu-id="5d6e0-172">**OS Device Namespace** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="5d6e0-173">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="5d6e0-173">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5d6e0-174">**хостекстентстартингаддресс**</span><span class="sxs-lookup"><span data-stu-id="5d6e0-174">**HostExtentStartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d6e0-175">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5d6e0-175">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5d6e0-176">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5d6e0-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d6e0-177">Квалификаторы: [**моделкорреспонденце**](../wmisdk/standard-qualifiers.md) ("**CIM \_ сторажеаллокатионсеттингдата**.**Хостресаурцеблокксизе**","[**CIM \_ BasedOn**](cim-basedon.md).**Стартингаддресс**")</span><span class="sxs-lookup"><span data-stu-id="5d6e0-177">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM\_StorageAllocationSettingData**.**HostResourceBlockSize**", "[**CIM\_BasedOn**](cim-basedon.md).**StartingAddress**")</span></span>
</dt> </dl>

<span data-ttu-id="5d6e0-178">Начальный адрес в области хранения узла.</span><span class="sxs-lookup"><span data-stu-id="5d6e0-178">The starting address on the host storage extent.</span></span> <span data-ttu-id="5d6e0-179">Значение NULL; UE означает, что нет прямого сопоставления между областью виртуального хранилища и областью хранения узла.</span><span class="sxs-lookup"><span data-stu-id="5d6e0-179">A NULL val;ue indicates that there is no direct mapping between the virtual storage extent and the host storage extent.</span></span>

</dd> <dt>

<span data-ttu-id="5d6e0-180">**хостресаурцеблокксизе**</span><span class="sxs-lookup"><span data-stu-id="5d6e0-180">**HostResourceBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d6e0-181">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5d6e0-181">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5d6e0-182">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5d6e0-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d6e0-183">Квалификаторы: [**моделкорреспонденце**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ сторажеекстент**](cim-storageextent.md).**Размерность ")**, **Пунит** (" Byte ")</span><span class="sxs-lookup"><span data-stu-id="5d6e0-183">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_StorageExtent**](cim-storageextent.md).**BlockSize**"), **PUnit** ("byte")</span></span>
</dt> </dl>

<span data-ttu-id="5d6e0-184">Размер (в байтах) блоков, выделенных на узле для выделения памяти.</span><span class="sxs-lookup"><span data-stu-id="5d6e0-184">The size, in bytes, of the blocks that are allocated on the host for the storage allocation.</span></span> <span data-ttu-id="5d6e0-185">Если размер блока является переменным, то должен быть указан максимальный размер блока в байтах.</span><span class="sxs-lookup"><span data-stu-id="5d6e0-185">If the block size is variable, then the maximum block size in bytes should be specified.</span></span> <span data-ttu-id="5d6e0-186">Если размер блока неизвестен или если не применяется концепция блока, следует использовать значение "1" (неизвестно).</span><span class="sxs-lookup"><span data-stu-id="5d6e0-186">If the block size is unknown or if a block concept does not apply, then the value "1" (unknown) should be used.</span></span>

</dd> <dt>

<span data-ttu-id="5d6e0-187">**Ограничение**</span><span class="sxs-lookup"><span data-stu-id="5d6e0-187">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d6e0-188">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5d6e0-188">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5d6e0-189">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5d6e0-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d6e0-190">Квалификаторы: [**override**](../wmisdk/standard-qualifiers.md) ("Limit"), [**Моделкорреспонденце**](../wmisdk/standard-qualifiers.md) ("**CIM \_ сторажеаллокатионсеттингдата**.**Хостресаурцеблокксизе**")</span><span class="sxs-lookup"><span data-stu-id="5d6e0-190">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Limit"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM\_StorageAllocationSettingData**.**HostResourceBlockSize**")</span></span>
</dt> </dl>

<span data-ttu-id="5d6e0-191">Максимальный объем блоков, которые будут предоставлены для выделения ресурсов хранилища на узле.</span><span class="sxs-lookup"><span data-stu-id="5d6e0-191">The maximum amount of blocks that will be granted for the storage resource allocation on the host.</span></span> <span data-ttu-id="5d6e0-192">Размер блока задается свойством **хостресаурцеблокксизе** .</span><span class="sxs-lookup"><span data-stu-id="5d6e0-192">The block size is specified by the **HostResourceBlockSize** property.</span></span>

</dd> <dt>

<span data-ttu-id="5d6e0-193">**осерхостекстентнамеформат**</span><span class="sxs-lookup"><span data-stu-id="5d6e0-193">**OtherHostExtentNameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d6e0-194">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="5d6e0-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5d6e0-195">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5d6e0-195">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d6e0-196">Квалификаторы: [**моделкорреспонденце**](../wmisdk/standard-qualifiers.md) ("**CIM \_ сторажеаллокатионсеттингдата**.**Хостекстентнамеформат**")</span><span class="sxs-lookup"><span data-stu-id="5d6e0-196">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM\_StorageAllocationSettingData**.**HostExtentNameFormat**")</span></span>
</dt> </dl>

<span data-ttu-id="5d6e0-197">Формат свойства **хостекстентнаме** , если свойство имеет значение "1" (другое).</span><span class="sxs-lookup"><span data-stu-id="5d6e0-197">The format of the **HostExtentName** property if the property is set to "1" (other).</span></span>

</dd> <dt>

<span data-ttu-id="5d6e0-198">**осерхостекстентнаменамеспаце**</span><span class="sxs-lookup"><span data-stu-id="5d6e0-198">**OtherHostExtentNameNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d6e0-199">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="5d6e0-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5d6e0-200">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5d6e0-200">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d6e0-201">Квалификаторы: [**моделкорреспонденце**](../wmisdk/standard-qualifiers.md) ("**CIM \_ сторажеаллокатионсеттингдата**.**Хостекстентнаменамеспаце**")</span><span class="sxs-lookup"><span data-stu-id="5d6e0-201">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM\_StorageAllocationSettingData**.**HostExtentNameNamespace**")</span></span>
</dt> </dl>

<span data-ttu-id="5d6e0-202">Строка, описывающая пространство имен свойства **хостекстентнаме** , если значение свойства **хостекстентнаменамеспаце** равно "1" (другое).</span><span class="sxs-lookup"><span data-stu-id="5d6e0-202">A string that describes the namespace of the **HostExtentName** property if the value of the **HostExtentNameNamespace** property is "1" (other).</span></span>

</dd> <dt>

<span data-ttu-id="5d6e0-203">**Резервирование**</span><span class="sxs-lookup"><span data-stu-id="5d6e0-203">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d6e0-204">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5d6e0-204">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5d6e0-205">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5d6e0-205">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d6e0-206">Квалификаторы: [**override**](../wmisdk/standard-qualifiers.md) ("резервирование"), [**Моделкорреспонденце**](../wmisdk/standard-qualifiers.md) ("**CIM \_ сторажеаллокатионсеттингдата**.**Хостресаурцеблокксизе**")</span><span class="sxs-lookup"><span data-stu-id="5d6e0-206">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Reservation"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM\_StorageAllocationSettingData**.**HostResourceBlockSize**")</span></span>
</dt> </dl>

<span data-ttu-id="5d6e0-207">Количество блоков, которые гарантированно будут доступны для выделения ресурсов хранилища на узле.</span><span class="sxs-lookup"><span data-stu-id="5d6e0-207">The amount of blocks that are guaranteed to be available for the storage resource allocation on the host.</span></span> <span data-ttu-id="5d6e0-208">Размер блока задается свойством **хостресаурцеблокксизе** .</span><span class="sxs-lookup"><span data-stu-id="5d6e0-208">The block size is specified by the **HostResourceBlockSize** property.</span></span>

</dd> <dt>

<span data-ttu-id="5d6e0-209">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="5d6e0-209">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d6e0-210">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5d6e0-210">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5d6e0-211">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5d6e0-211">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d6e0-212">Квалификаторы: [**override**](../wmisdk/standard-qualifiers.md) ("виртуалкуантити"), [**Моделкорреспонденце**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ сторажеекстент**](cim-storageextent.md).**Нумберофблоккс**","**CIM \_ сторажеаллокатионсеттингдата**.**Виртуалкуантитюнитс**")</span><span class="sxs-lookup"><span data-stu-id="5d6e0-212">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("VirtualQuantity"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_StorageExtent**](cim-storageextent.md).**NumberOfBlocks**", "**CIM\_StorageAllocationSettingData**.**VirtualQuantityUnits**")</span></span>
</dt> </dl>

<span data-ttu-id="5d6e0-213">Число блоков, которые предоставляет потребитель для выделения хранилища.</span><span class="sxs-lookup"><span data-stu-id="5d6e0-213">The number of blocks that the storage allocation presents to the consumer.</span></span>

> [!Note]  
> <span data-ttu-id="5d6e0-214">Свойство **виртуалкуантити** может задавать размер блока "1", даже если **виртуалресаурцеблокксизе** неизвестен.</span><span class="sxs-lookup"><span data-stu-id="5d6e0-214">The **VirtualQuantity** property can specify a block size of "1", even if **VirtualResourceBlockSize** is unknown.</span></span>

 

</dd> <dt>

<span data-ttu-id="5d6e0-215">**виртуалкуантитюнитс**</span><span class="sxs-lookup"><span data-stu-id="5d6e0-215">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d6e0-216">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="5d6e0-216">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5d6e0-217">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5d6e0-217">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d6e0-218">Квалификаторы: [**override**](../wmisdk/standard-qualifiers.md) ("виртуалкуантитюнитс"), [**Моделкорреспонденце**](../wmisdk/standard-qualifiers.md) ("**CIM \_ сторажеаллокатионсеттингдата**.**Виртуалкуантити**"), **испунит**</span><span class="sxs-lookup"><span data-stu-id="5d6e0-218">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("VirtualQuantityUnits"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM\_StorageAllocationSettingData**.**VirtualQuantity**"), **IsPUnit**</span></span>
</dt> </dl>

<span data-ttu-id="5d6e0-219">Единицы, используемые свойством **виртуалкуантити** .</span><span class="sxs-lookup"><span data-stu-id="5d6e0-219">The units used by the **VirtualQuantity** property.</span></span> <span data-ttu-id="5d6e0-220">Это значение должно быть равно "Count (блок фиксированного размера)" или "Byte".</span><span class="sxs-lookup"><span data-stu-id="5d6e0-220">This value shall should be set to "count(fixed size block)" or "byte".</span></span> <span data-ttu-id="5d6e0-221">Значение по умолчанию, "Count (блок фиксированного размера)", должно использоваться для фиксированного размера блока, а "Byte" следует использовать для неизвестного или переменного размера блока.</span><span class="sxs-lookup"><span data-stu-id="5d6e0-221">The default value, "count(fixed size block)" should be used for a fixed block size, and "byte" should be used for an unknown or variable block size.</span></span>

</dd> <dt>

<span data-ttu-id="5d6e0-222">**виртуалресаурцеблокксизе**</span><span class="sxs-lookup"><span data-stu-id="5d6e0-222">**VirtualResourceBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d6e0-223">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5d6e0-223">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5d6e0-224">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5d6e0-224">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d6e0-225">Квалификаторы: [**моделкорреспонденце**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ сторажеекстент**](cim-storageextent.md).**Размерность ")**, **Пунит** (" Byte ")</span><span class="sxs-lookup"><span data-stu-id="5d6e0-225">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_StorageExtent**](cim-storageextent.md).**BlockSize**"), **PUnit** ("byte")</span></span>
</dt> </dl>

<span data-ttu-id="5d6e0-226">Размер блоков в байтах, образующих запрос на выделение хранилища.</span><span class="sxs-lookup"><span data-stu-id="5d6e0-226">The size, in bytes, of the blocks that form the storage allocation request.</span></span> <span data-ttu-id="5d6e0-227">Если размер блока является переменным, то должен быть указан максимальный размер блока.</span><span class="sxs-lookup"><span data-stu-id="5d6e0-227">If the block size is variable, then the maximum block size should be specified.</span></span> <span data-ttu-id="5d6e0-228">Если размер блока неизвестен или если не применяется концепция блока, то размер блока должен быть равен 1 (неизвестно).</span><span class="sxs-lookup"><span data-stu-id="5d6e0-228">If the block size is unknown or if a block concept does not apply, then the block size should be "1" (unknown).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5d6e0-229">Требования</span><span class="sxs-lookup"><span data-stu-id="5d6e0-229">Requirements</span></span>



| <span data-ttu-id="5d6e0-230">Требование</span><span class="sxs-lookup"><span data-stu-id="5d6e0-230">Requirement</span></span> | <span data-ttu-id="5d6e0-231">Значение</span><span class="sxs-lookup"><span data-stu-id="5d6e0-231">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d6e0-232">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5d6e0-232">Minimum supported client</span></span><br/> | <span data-ttu-id="5d6e0-233">Windows 8</span><span class="sxs-lookup"><span data-stu-id="5d6e0-233">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="5d6e0-234">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5d6e0-234">Minimum supported server</span></span><br/> | <span data-ttu-id="5d6e0-235">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5d6e0-235">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="5d6e0-236">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="5d6e0-236">Namespace</span></span><br/>                | <span data-ttu-id="5d6e0-237">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="5d6e0-237">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="5d6e0-238">MOF</span><span class="sxs-lookup"><span data-stu-id="5d6e0-238">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5d6e0-239"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5d6e0-239"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5d6e0-240">DLL</span><span class="sxs-lookup"><span data-stu-id="5d6e0-240">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5d6e0-241"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5d6e0-241"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="5d6e0-242">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5d6e0-242">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d6e0-243">**\_РЕСАУРЦЕАЛЛОКАТИОНСЕТТИНГДАТА CIM**</span><span class="sxs-lookup"><span data-stu-id="5d6e0-243">**CIM\_ResourceAllocationSettingData**</span></span>](cim-resourceallocationsettingdata.md)
</dt> </dl>

 

