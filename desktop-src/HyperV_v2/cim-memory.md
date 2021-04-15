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
# <a name="cim_memory-class-hyper-v-management"></a>Класс CIM_Memory (Управление Hyper-V)

Представляет возможности и управление логическими устройствами, связанными с памятью.

## <a name="syntax"></a>Синтаксис

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

## <a name="members"></a>Члены

Класс **\_ памяти CIM** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **\_ памяти CIM** имеет следующие свойства.

<dl> <dt>

**аддитионалеррордата**
</dt> <dd> <dl> <dt>

Тип данных: массив **Uint8**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: не [**рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ мемореррор. аддитионалеррордата"), **октетстринг**, [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Memory Device \| 005,18 "," MIF. \|Массив физической памяти DMTF \| 001,13 ")
</dt> </dl>

Массив октетов, который содержит дополнительные сведения об ошибке. Например, синдром ECC или возврат битовой проверки, если используется методология ошибок на основе CRC. В последнем случае, если распознана одна разрядная ошибка и известен алгоритм CRC, можно определить точный бит, который завершился сбоем.

Если свойство **errorInfo** содержит значение 3 (ОК), это свойство не используется.

</dd> <dt>

**корректаблиррор**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: не [**рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ мемореррор. корректаблиррор"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Массив физической памяти DMTF \| 001,8 ")
</dt> </dl>

**значение true** , если последняя ошибка является правильной. в противном случае — **значение false**. Если свойство **errorInfo** содержит значение 3 (ОК), это свойство не используется.

</dd> <dt>

**ендингаддресс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("килобайты"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Массив памяти DMTF, сопоставленный адресам \| 001,4 "," MIF. \|Сопоставленные адреса памяти \| в формате DMTF 001,5 "), **Пунит** (" Byte \* 10 ^ 3 ")
</dt> </dl>

Конечный адрес, на который ссылается приложение или операционная система, сопоставленный контроллером памяти для объекта памяти. Конечный адрес указывается в килобайтах.

</dd> <dt>

**ерроракцесс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: не [**рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ мемореррор. ерроракцесс"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Массив физической памяти DMTF \| 001,10 ")
</dt> </dl>

Операция доступа к памяти, вызвавшая последнюю ошибку. Если свойство **errorInfo** содержит значение 3 (ОК), это свойство не используется.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Другое** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Неизвестно** (2)


</dt> <dd></dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>

**Чтение** (3)


</dt> <dd></dd> <dt>

<span id="Write"></span><span id="write"></span><span id="WRITE"></span>

**Запись** (4)


</dt> <dd></dd> <dt>

<span id="Partial_Write"></span><span id="partial_write"></span><span id="PARTIAL_WRITE"></span>

**Частичная запись** (5)


</dt> <dd></dd> </dl>

</dd> <dt>

**еррораддресс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: не [**рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ мемореррор. стартингаддресс"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Memory Device \| 005,19 "," MIF. \|Массив физической памяти DMTF \| 001,14 ")
</dt> </dl>

Адрес последней ошибки памяти. Тип ошибки описан в свойстве **errorInfo** . Если свойство **errorInfo** содержит значение 3 (ОК), это свойство не используется.

</dd> <dt>

**ErrorData**
</dt> <dd> <dl> <dt>

Тип данных: массив **Uint8**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: не [**рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ мемореррор. ErrorData"), **октетстринг**, [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Массив физической памяти DMTF \| 001,12 ")
</dt> </dl>

Массив, содержащий данные, захваченные во время последнего ошибочного доступа к памяти. Данные занимают первые n октетов массива, необходимых для хранения числа битов, заданных свойством **еррортрансферсизе** .

Если свойство **еррортрансферсизе** содержит "0" (ОК), это свойство не используется.

</dd> <dt>

**еррордатаордер**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: не [**рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ мемореррор. еррордатаордер")
</dt> </dl>

Упорядочивание данных, хранящихся в свойстве **ErrorData** . Может быть указан "наименьший байт сначала" (значение = 1) или "наиболее значимый байт первым" (2). Если свойство **еррортрансферсизе** содержит "0" (ОК), это свойство не используется.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Неизвестно** (0)


</dt> <dd></dd> <dt>

<span id="Least_Significant_Byte_First"></span><span id="least_significant_byte_first"></span><span id="LEAST_SIGNIFICANT_BYTE_FIRST"></span>

**Наименьший значащий байт первым** (1)


</dt> <dd></dd> <dt>

<span id="Most_Significant_Byte_First"></span><span id="most_significant_byte_first"></span><span id="MOST_SIGNIFICANT_BYTE_FIRST"></span>

**Первый старший байт** (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**ErrorInfo**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: не [**рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ мемореррор. errorInfo"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Memory Device \| 005,12 "," MIF. \|Массив физической памяти DMTF \| 001,8 "), [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ память CIM**".**Осереррордескриптион**")
</dt> </dl>

Тип последней возникшей ошибки.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Другое** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Неизвестно** (2)


</dt> <dd></dd> <dt>

<span id="OK"></span><span id="ok"></span>

**ОК** (3)


</dt> <dd></dd> <dt>

<span id="Bad_Read"></span><span id="bad_read"></span><span id="BAD_READ"></span>

**Неправильное чтение** (4)


</dt> <dd></dd> <dt>

<span id="Parity_Error"></span><span id="parity_error"></span><span id="PARITY_ERROR"></span>

**Ошибка четности** (5)


</dt> <dd></dd> <dt>

<span id="Single-Bit_Error"></span><span id="single-bit_error"></span><span id="SINGLE-BIT_ERROR"></span>

**Одноразрядная ошибка** (6)


</dt> <dd></dd> <dt>

<span id="Double-Bit_Error"></span><span id="double-bit_error"></span><span id="DOUBLE-BIT_ERROR"></span>

**Ошибка в двух битах** (7)


</dt> <dd></dd> <dt>

<span id="Multi-Bit_Error"></span><span id="multi-bit_error"></span><span id="MULTI-BIT_ERROR"></span>

**Многоразрядная ошибка** (8)


</dt> <dd></dd> <dt>

<span id="Nibble_Error"></span><span id="nibble_error"></span><span id="NIBBLE_ERROR"></span>

**Ошибка в погрешностях** (9)


</dt> <dd></dd> <dt>

<span id="Checksum_Error"></span><span id="checksum_error"></span><span id="CHECKSUM_ERROR"></span>

**Ошибка контрольной суммы** (10)


</dt> <dd></dd> <dt>

<span id="CRC_Error"></span><span id="crc_error"></span><span id="CRC_ERROR"></span>

**Ошибка CRC** (11)


</dt> <dd></dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

Не **определено** (12)


</dt> <dd></dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

Не **определено** (13)


</dt> <dd></dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

Не **определено** (14)


</dt> <dd></dd> </dl>

</dd> <dt>

**еррормесодологи**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("еррормесодологи"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Массив физической памяти DMTF \| 001,7 ")
</dt> </dl>

Указывает, используются ли объектом памяти алгоритмы четности, алгоритмы CRC, ECC или другие механизмы. Также можно указать сведения об алгоритме.

</dd> <dt>

**еррорресолутион**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: не [**рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ мемореррор. еррорресолутион"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Memory Device \| 005,21 "," MIF. \|Массив физической памяти DMTF \| 001,15 "), **Пунит** (" Byte ")
</dt> </dl>

Диапазон в байтах, в котором может быть разрешена Последняя ошибка. Например, если адреса ошибок разрешаются в бит 11, например на основе обычной страницы; затем ошибки могут быть разрешены на границы 4 КБ, а для этого свойства задано значение "4000". Если свойство **errorInfo** содержит значение 3 (ОК), это свойство не используется.

</dd> <dt>

**ErrorTime**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: не [**рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ мемореррор. еррортиме")
</dt> </dl>

Время, когда произошла последняя ошибка памяти. Если свойство **errorInfo** содержит значение 3 (ОК), это свойство не используется.

</dd> <dt>

**еррортрансферсизе**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: не [**рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ мемореррор. еррортрансферсизе"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("BITS"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Массив физической памяти DMTF \| 001,11 "), **Пунит** (" bit ")
</dt> </dl>

Размер передачи данных в битах, который привел к последней ошибке. "0" означает отсутствие ошибки. Если свойство **errorInfo** содержит значение 3 (ОК), это свойство не используется.

</dd> <dt>

**осереррордескриптион**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: не [**рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ мемореррор. осереррордескриптион"), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ память CIM**".**ErrorInfo**")
</dt> </dl>

Описание типа ошибки, если свойство **ErrorType** имеет значение 1 (другое).

</dd> <dt>

**стартингаддресс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("килобайты"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Массив памяти DMTF, сопоставленный адресам \| 001,3 "," MIF. \|Сопоставленные адреса памяти \| в формате DMTF 001,4 "), **Пунит** (" Byte \* 10 ^ 3 ")
</dt> </dl>

Начальный адрес, на который ссылается приложение или операционная система, сопоставленный контроллером памяти для объекта памяти. Начальный адрес указывается в килобайтах.

</dd> <dt>

**системлевеладдресс**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: не [**рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_MemoryError.Sysтемлевеладдресс")
</dt> </dl>

**значение true** , если сведения об адресе в свойстве **еррораддресс** являются адресом системного уровня, и **значение false** , если это физический адрес.

</dd> <dt>

**Независимо**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

**значение true** , если память является временной; в противном случае — **значение false**.

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

[**\_СТОРАЖЕЕКСТЕНТ CIM**](cim-storageextent.md)
</dt> </dl>

 

