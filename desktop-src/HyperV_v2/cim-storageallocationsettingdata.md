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
# <a name="cim_storageallocationsettingdata-class"></a>\_Класс CIM сторажеаллокатионсеттингдата

Представляет параметры для размещения виртуального хранилища.

## <a name="syntax"></a>Синтаксис

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

## <a name="members"></a>Члены

Класс **CIM \_ сторажеаллокатионсеттингдата** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **CIM \_ сторажеаллокатионсеттингдата** имеет следующие свойства.

<dl> <dt>

**Доступ**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**моделкорреспонденце**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ сторажеекстент**](cim-storageextent.md).**Доступ**")
</dt> </dl>

Поддержка выделения памяти для чтения и записи.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Неизвестно** (0)


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

**Для чтения** (1)


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

**Доступный для записи** (2)


</dt> <dd></dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

**Поддерживается чтение и запись** (3)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**Зарезервировано DMTF** (..)


</dt> <dd></dd> </dl>

</dd> <dt>

**хостекстентнаме**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**моделкорреспонденце**](../wmisdk/standard-qualifiers.md) ("**CIM \_ сторажеаллокатионсеттингдата**.**Хостекстентнамеформат**","**CIM \_ сторажеаллокатионсеттингдата**.**Хостекстентнаменамеспаце**","[**CIM \_ сторажеекстент**](cim-storageextent.md).**Name**")
</dt> </dl>

Уникальный идентификатор области хранения узла.

</dd> <dt>

**хостекстентнамеформат**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**моделкорреспонденце**](../wmisdk/standard-qualifiers.md) ("**CIM \_ сторажеаллокатионсеттингдата**.**Хостекстентнаме**","**CIM \_ сторажеаллокатионсеттингдата**.**Осерхостекстентнамеформат**","[**CIM \_ сторажеекстент**](cim-storageextent.md).**Намеформат**")
</dt> </dl>

Формат значения свойства **хостекстентнаме** .

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)


</dt> <dd></dd> <dt>

<span id="SNVM"></span><span id="snvm"></span>

<span id="SNVM"></span><span id="snvm"></span>**Снвм** (7)


</dt> <dd>

Серийный номер, поставщик/модель (СНВМ) СНВМ — 3 строки, представляющие имя поставщика, название продукта в пространстве имен поставщика и серийный номер в пространстве имен модели. Строки разделяются символом "+". Могут быть включены пробелы и быть значимыми. Серийный номер — это текстовое представление серийного номера в шестнадцатеричном верхнем регистре. Представляет идентификатор поставщика и модели из данных запроса SCSI. поле "поставщик" должно иметь ширину 8 символов, а поле "продукт" должно иметь ширину 16 символов. Например,

"Acme \_ \_ \_ \_ + Super Disk \_ \_ \_ \_ \_ \_ + 124437458" ( \_ является символом пробела)

</dd> <dt>

<span id="NAA"></span><span id="naa"></span>

<span id="NAA"></span><span id="naa"></span>**Удаляем** (9)


</dt> <dd>

9 = УДАЛЯЕМ в виде универсального формата. См.

https://standards.ieee.org/regauth/oui/tutorials/fibrecomp\_id.html. В формате 16 или 32 неразделенных шестнадцатеричных символов в верхнем регистре (2 за двоичный байт).

Например, "21000020372D3C73"

</dd> <dt>

<span id="EUI64"></span><span id="eui64"></span>

<span id="EUI64"></span><span id="eui64"></span>**EUI64** (10)


</dt> <dd>

EUI в качестве универсального формата (EUI64) см. в разделе

https://standards.ieee.org/content/dam/ieee-standards/standards/web/documents/tutorials/eui.pdf.

</dd> <dt>

<span id="T10VID"></span><span id="t10vid"></span>

<span id="T10VID"></span><span id="t10vid"></span>**T10VID** (11)


</dt> <dd>

Формат идентификатора поставщика T10, возвращенный SCSI-запросом VPD стр 83, тип идентификатора 1. См. спецификацию T10 SPC-3. Это 8-байтовый идентификатор поставщика ASCII из реестра T10, за которым следует идентификатор ASCII, определяемый поставщиком. разрешены пробелы. Для томов, отличных от SCSI, может быть наиболее подходящий вариант "СНВМ".

</dd> <dt>

<span id="OS_Device_Name"></span><span id="os_device_name"></span><span id="OS_DEVICE_NAME"></span>

<span id="OS_Device_Name"></span><span id="os_device_name"></span><span id="OS_DEVICE_NAME"></span>**Имя устройства ОС** (12)


</dt> <dd>

Имя устройства ОС (для Логикалдискс). Дополнительные сведения см. в описании имени диска LogicalDisk.

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)


</dt> <dd></dd> </dl>

</dd> <dt>

**хостекстентнаменамеспаце**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**моделкорреспонденце**](../wmisdk/standard-qualifiers.md) ("**CIM \_ сторажеаллокатионсеттингдата**.**Хостекстентнаме**","**CIM \_ сторажеаллокатионсеттингдата**.**Осерхостекстентнаменамеспаце**","**CIM \_ сторажеаллокатионсеттингдата**.**Хостекстентнамеформат**","[**CIM \_ сторажеекстент**](cim-storageextent.md).**Пространство имен**")
</dt> </dl>

Формат имени для свойства **Name** .

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Неизвестно** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Другое** (1)


</dt> <dd></dd> <dt>

<span id="VPD83Type3"></span><span id="vpd83type3"></span><span id="VPD83TYPE3"></span>

**VPD83Type3** (2)


</dt> <dd></dd> <dt>

<span id="VPD83Type2"></span><span id="vpd83type2"></span><span id="VPD83TYPE2"></span>

**VPD83Type2** (3)


</dt> <dd></dd> <dt>

<span id="VPD83Type1"></span><span id="vpd83type1"></span><span id="VPD83TYPE1"></span>

**VPD83Type1** (4)


</dt> <dd></dd> <dt>

<span id="VPD80"></span><span id="vpd80"></span>

**VPD80** (5)


</dt> <dd></dd> <dt>

<span id="NodeWWN"></span><span id="nodewwn"></span><span id="NODEWWN"></span>

**Нодеввн** (6)


</dt> <dd></dd> <dt>

<span id="SNVM"></span><span id="snvm"></span>

**Снвм** (7)


</dt> <dd></dd> <dt>

<span id="OS_Device_Namespace"></span><span id="os_device_namespace"></span><span id="OS_DEVICE_NAMESPACE"></span>

**Пространство имен устройств ОС** (8)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**Зарезервировано DMTF** (..)


</dt> <dd></dd> </dl>

</dd> <dt>

**хостекстентстартингаддресс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**моделкорреспонденце**](../wmisdk/standard-qualifiers.md) ("**CIM \_ сторажеаллокатионсеттингдата**.**Хостресаурцеблокксизе**","[**CIM \_ BasedOn**](cim-basedon.md).**Стартингаддресс**")
</dt> </dl>

Начальный адрес в области хранения узла. Значение NULL; UE означает, что нет прямого сопоставления между областью виртуального хранилища и областью хранения узла.

</dd> <dt>

**хостресаурцеблокксизе**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**моделкорреспонденце**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ сторажеекстент**](cim-storageextent.md).**Размерность ")**, **Пунит** (" Byte ")
</dt> </dl>

Размер (в байтах) блоков, выделенных на узле для выделения памяти. Если размер блока является переменным, то должен быть указан максимальный размер блока в байтах. Если размер блока неизвестен или если не применяется концепция блока, следует использовать значение "1" (неизвестно).

</dd> <dt>

**Ограничение**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](../wmisdk/standard-qualifiers.md) ("Limit"), [**Моделкорреспонденце**](../wmisdk/standard-qualifiers.md) ("**CIM \_ сторажеаллокатионсеттингдата**.**Хостресаурцеблокксизе**")
</dt> </dl>

Максимальный объем блоков, которые будут предоставлены для выделения ресурсов хранилища на узле. Размер блока задается свойством **хостресаурцеблокксизе** .

</dd> <dt>

**осерхостекстентнамеформат**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**моделкорреспонденце**](../wmisdk/standard-qualifiers.md) ("**CIM \_ сторажеаллокатионсеттингдата**.**Хостекстентнамеформат**")
</dt> </dl>

Формат свойства **хостекстентнаме** , если свойство имеет значение "1" (другое).

</dd> <dt>

**осерхостекстентнаменамеспаце**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**моделкорреспонденце**](../wmisdk/standard-qualifiers.md) ("**CIM \_ сторажеаллокатионсеттингдата**.**Хостекстентнаменамеспаце**")
</dt> </dl>

Строка, описывающая пространство имен свойства **хостекстентнаме** , если значение свойства **хостекстентнаменамеспаце** равно "1" (другое).

</dd> <dt>

**Резервирование**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](../wmisdk/standard-qualifiers.md) ("резервирование"), [**Моделкорреспонденце**](../wmisdk/standard-qualifiers.md) ("**CIM \_ сторажеаллокатионсеттингдата**.**Хостресаурцеблокксизе**")
</dt> </dl>

Количество блоков, которые гарантированно будут доступны для выделения ресурсов хранилища на узле. Размер блока задается свойством **хостресаурцеблокксизе** .

</dd> <dt>

**VirtualQuantity**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](../wmisdk/standard-qualifiers.md) ("виртуалкуантити"), [**Моделкорреспонденце**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ сторажеекстент**](cim-storageextent.md).**Нумберофблоккс**","**CIM \_ сторажеаллокатионсеттингдата**.**Виртуалкуантитюнитс**")
</dt> </dl>

Число блоков, которые предоставляет потребитель для выделения хранилища.

> [!Note]  
> Свойство **виртуалкуантити** может задавать размер блока "1", даже если **виртуалресаурцеблокксизе** неизвестен.

 

</dd> <dt>

**виртуалкуантитюнитс**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](../wmisdk/standard-qualifiers.md) ("виртуалкуантитюнитс"), [**Моделкорреспонденце**](../wmisdk/standard-qualifiers.md) ("**CIM \_ сторажеаллокатионсеттингдата**.**Виртуалкуантити**"), **испунит**
</dt> </dl>

Единицы, используемые свойством **виртуалкуантити** . Это значение должно быть равно "Count (блок фиксированного размера)" или "Byte". Значение по умолчанию, "Count (блок фиксированного размера)", должно использоваться для фиксированного размера блока, а "Byte" следует использовать для неизвестного или переменного размера блока.

</dd> <dt>

**виртуалресаурцеблокксизе**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**моделкорреспонденце**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ сторажеекстент**](cim-storageextent.md).**Размерность ")**, **Пунит** (" Byte ")
</dt> </dl>

Размер блоков в байтах, образующих запрос на выделение хранилища. Если размер блока является переменным, то должен быть указан максимальный размер блока. Если размер блока неизвестен или если не применяется концепция блока, то размер блока должен быть равен 1 (неизвестно).

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8<br/>                                                                                    |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                                          |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_РЕСАУРЦЕАЛЛОКАТИОНСЕТТИНГДАТА CIM**](cim-resourceallocationsettingdata.md)
</dt> </dl>

 

