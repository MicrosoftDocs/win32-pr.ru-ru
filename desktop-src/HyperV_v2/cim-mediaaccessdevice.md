---
description: Представляет устройство, которое может использовать носители для хранения и извлечения данных.
ms.assetid: c63b1731-dbc0-4e5e-acb8-cd91b5569dd2
title: Класс CIM_MediaAccessDevice (Управление Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MediaAccessDevice
- CIM_MediaAccessDevice.Capabilities
- CIM_MediaAccessDevice.CapabilityDescriptions
- CIM_MediaAccessDevice.ErrorMethodology
- CIM_MediaAccessDevice.CompressionMethod
- CIM_MediaAccessDevice.NumberOfMediaSupported
- CIM_MediaAccessDevice.MaxMediaSize
- CIM_MediaAccessDevice.DefaultBlockSize
- CIM_MediaAccessDevice.MaxBlockSize
- CIM_MediaAccessDevice.MinBlockSize
- CIM_MediaAccessDevice.NeedsCleaning
- CIM_MediaAccessDevice.MediaIsLocked
- CIM_MediaAccessDevice.Security
- CIM_MediaAccessDevice.LastCleaned
- CIM_MediaAccessDevice.MaxAccessTime
- CIM_MediaAccessDevice.UncompressedDataRate
- CIM_MediaAccessDevice.LoadTime
- CIM_MediaAccessDevice.UnloadTime
- CIM_MediaAccessDevice.MountCount
- CIM_MediaAccessDevice.TimeOfLastMount
- CIM_MediaAccessDevice.TotalMountTime
- CIM_MediaAccessDevice.UnitsDescription
- CIM_MediaAccessDevice.MaxUnitsBeforeCleaning
- CIM_MediaAccessDevice.UnitsUsed
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: bb97ded03cfc853fc0dde6ede26083be01cf218f210c31f947f315634599e179
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119900264"
---
# <a name="cim_mediaaccessdevice-class-hyper-v-management"></a>Класс CIM_MediaAccessDevice (Управление Hyper-V)

Представляет устройство, которое может использовать носители для хранения и извлечения данных.

## <a name="syntax"></a>Синтаксис

``` syntax
[Abstract, Version("2.6.0"), UMLPackagePath("CIM::Device::StorageDevices"), AMENDMENT]
class CIM_MediaAccessDevice : CIM_LogicalDevice
{
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
  string   ErrorMethodology;
  string   CompressionMethod;
  uint32   NumberOfMediaSupported;
  uint64   MaxMediaSize;
  uint64   DefaultBlockSize;
  uint64   MaxBlockSize;
  uint64   MinBlockSize;
  boolean  NeedsCleaning;
  boolean  MediaIsLocked;
  uint16   Security;
  datetime LastCleaned;
  uint64   MaxAccessTime;
  uint32   UncompressedDataRate;
  uint64   LoadTime;
  uint64   UnloadTime;
  uint64   MountCount;
  datetime TimeOfLastMount;
  uint64   TotalMountTime;
  string   UnitsDescription;
  uint64   MaxUnitsBeforeCleaning;
  uint64   UnitsUsed;
};
```

## <a name="members"></a>Члены

Класс **CIM \_ медиаакцессдевице** имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Класс **CIM \_ медиаакцессдевице** содержит следующие методы.



| Метод                                               | Описание                                                            |
|:-----------------------------------------------------|:-----------------------------------------------------------------------|
| [**локкмедиа**](cim-mediaaccessdevice-lockmedia.md) | Блокирует и разблокирует съемные носители на устройстве доступа к носителю.<br/> |



 

### <a name="properties"></a>Свойства

Класс **CIM \_ медиаакцессдевице** имеет следующие свойства.

<dl> <dt>

**Capabilities**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16** , массив
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| служба хранилища устройства \| 001,9 "," MIF. DMTF \| служба хранилища устройства \| 001,11 "," MIF. DMTF \| служба хранилища устройства \| 001,12 "," MIF. \|Диски DMTF \| 003,7 "," MIF. DMTF- \| диск \| 001,2 "," MIF. \|Жесткий диск DMTF \| 001,4 "), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ медиаакцессдевице**.**Капабилитидескриптионс**")
</dt> </dl>

Массив, содержащий возможности устройства доступа к носителю.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Неизвестно** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Другое** (1)


</dt> <dd></dd> <dt>

<span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>

**Последовательный доступ** (2)


</dt> <dd></dd> <dt>

<span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>

**Произвольный доступ** (3)


</dt> <dd></dd> <dt>

<span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>

**Поддерживает запись** (4)


</dt> <dd></dd> <dt>

<span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>

**Шифрование** (5)


</dt> <dd></dd> <dt>

<span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>

**Сжатие** (6)


</dt> <dd></dd> <dt>

<span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>

**Поддерживает** съемные носители (7)


</dt> <dd></dd> <dt>

<span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>

**Очистка вручную** (8)


</dt> <dd></dd> <dt>

<span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>

**Автоматическая очистка** (9)


</dt> <dd></dd> <dt>

<span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>

**Интеллектуальное уведомление** (10)


</dt> <dd></dd> <dt>

<span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>

**Поддержка двусторонних носителей** (11)


</dt> <dd></dd> <dt>

<span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>

**Извлечение с отключением не требуется** (12)


</dt> <dd></dd> </dl>

</dd> <dt>

**капабилитидескриптионс**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный"), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ медиаакцессдевице**.**Возможности**")
</dt> </dl>

Массив описаний характеристик для элементов в массиве **capabilities** .

</dd> <dt>

**компрессионмесод**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Имя алгоритма или средства, используемого устройством для поддержки сжатия.

Если тип сжатия не указан, можно использовать одно из следующих значений:

-   Неизвестная поддержка сжатия неизвестна или не указана.
-   "Сжатое" Сжатие поддерживается, но тип неизвестен или не указан.
-   "Не сжато" устройство не поддерживает возможности сжатия.

</dd> <dt>

**дефаултблокксизе**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes"), **Пунит** ("Byte")
</dt> </dl>

Размер блока по умолчанию для устройства (в байтах).

</dd> <dt>

**еррормесодологи**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Тип обнаружения и исправления ошибок, поддерживаемых устройством.

</dd> <dt>

**ластклеанед**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Дата и время последней очистки устройства.

</dd> <dt>

**лоадтиме**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("миллисекунды"), **Пунит** ("Second \* 10 ^-3")
</dt> </dl>

Время, затрачиваемое устройством на чтение или запись носителя после загрузки устройства (в миллисекундах). Например, для дисков это интервал между диском, который не передается на диск, сообщает о том, что он готов к операциям чтения и записи. Для ленточных накопителей это начинается при вставке носителя и заканчивается, когда устройство сообщает о готовности к работе для приложения. Обычно это находится в области ленты ленты (BOT).

</dd> <dt>

**максакцесстиме**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("миллисекунды"), **Пунит** ("Second \* 10 ^-3")
</dt> </dl>

Максимальное время доступа к носителю в миллисекундах. Для диска это означает полный поиск и полную задержку вращения. Для ленточных накопителей этот элемент представляет собой поиск с начала ленты до наиболее физической отдаленной точки.

</dd> <dt>

**максблокксизе**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes"), **Пунит** ("Byte")
</dt> </dl>

Максимальный размер блока в байтах для носителя, доступного устройству.

</dd> <dt>

**максмедиасизе**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Устройства с последовательным доступом DMTF \| 001,2 "," MIF. \|Жесткий диск DMTF \| 001,5 ")
</dt> </dl>

Максимальный размер носителя, поддерживаемого этим устройством (в килобайтах).

</dd> <dt>

**максунитсбефореклеанинг**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ медиаакцессдевице**.**Унитсдескриптион**")
</dt> </dl>

Максимальное число единиц, которое можно использовать до очистки устройства. **Унитсдескриптион** определяет, как тип единицы измерения.

</dd> <dt>

**медиаислоккед**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

**значение true** , если носитель заблокирован на устройстве и не может быть извлечен. в противном случае — **значение false**. Для несъемных устройств это значение должно быть **равно true**.

</dd> <dt>

**минблокксизе**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes"), **Пунит** ("Byte")
</dt> </dl>

Минимальный размер блока (в байтах) для носителя, доступного устройству.

</dd> <dt>

**маунткаунт**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **Счетчик**
</dt> </dl>

Количество случаев, когда носитель был подключен для передачи данных или для очистки устройства. Если устройство не поддерживает съемные носители, это свойство должно иметь значение 0.

</dd> <dt>

**нидсклеанинг**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

**значение true** , если устройству требуется очистка; в противном случае — **значение false**.

> [!Note]  
> Свойство **capabilities** указывает, возможна ли ручная или автоматическая очистка.

 

</dd> <dt>

**нумберофмедиасуппортед**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Если устройство поддерживает несколько отдельных носителей, это свойство определяет максимальное число, которое может поддерживаться или вставляться.

</dd> <dt>

**Безопасность**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Диски DMTF \| 003,22 ")
</dt> </dl>

Операционная безопасность для устройства.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Другое** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Неизвестно** (2)


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

**Нет** (3)


</dt> <dd></dd> <dt>

<span id="Read_Only"></span><span id="read_only"></span><span id="READ_ONLY"></span>

**Только для чтения** (4)


</dt> <dd></dd> <dt>

<span id="Locked_Out"></span><span id="locked_out"></span><span id="LOCKED_OUT"></span>

**Заблокировано** (5)


</dt> <dd></dd> <dt>

<span id="Boot_Bypass"></span><span id="boot_bypass"></span><span id="BOOT_BYPASS"></span>

**Обход загрузки** (6)


</dt> <dd></dd> <dt>

<span id="Boot_Bypass_and_Read_Only"></span><span id="boot_bypass_and_read_only"></span><span id="BOOT_BYPASS_AND_READ_ONLY"></span>

**Только для чтения и обхода загрузки** (7)


</dt> <dd></dd> </dl>

</dd> <dt>

**тимеофластмаунт**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Последняя дата и время подключения носителя к устройству. Это свойство используется только устройствами, поддерживающими съемные носители.

</dd> <dt>

**тоталмаунттиме**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Время в секундах, в течение которого носитель был подключен для передачи данных или для очистки устройства. Если устройство не поддерживает съемные носители, это свойство должно иметь значение 0.

</dd> <dt>

**ункомпресседдатарате**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("килобайт в секунду"), **Пунит** ("байт/сек \* 10 ^ 3")
</dt> </dl>

Постоянная скорость передачи данных в килобайтах, с которой устройство может выполнять чтение и запись на носитель. Это постоянная скорость необработанных данных. В этом свойстве не следует сообщать о максимальной скорости или тарифах с сжатием.

</dd> <dt>

**унитсдескриптион**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ медиаакцессдевице**.**Максунитсбефореклеанинг**","**CIM \_ медиаакцессдевице**.**Унитсусед**")
</dt> </dl>

Описывает тип единицы для свойств **максунитсбефореклеанинг** и **унитсусед** .

</dd> <dt>

**унитсусед**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**датчик**](/windows/desktop/WmiSdk/standard-qualifiers), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ медиаакцессдевице**.**Унитсдескриптион**","**CIM \_ медиаакцессдевице**.**Максунитсбефореклеанинг**")
</dt> </dl>

Число единиц, используемых устройством. Это свойство используется, чтобы определить, когда устройство должно быть очищено. **Унитсдескриптион** определяет, как тип единицы измерения.

</dd> <dt>

**унлоадтиме**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("миллисекунды"), **Пунит** ("Second \* 10 ^-3")
</dt> </dl>

Время в миллисекундах, необходимое для перехода устройства из чтения или записи носителя в выгружаемый поток. Например, для дисков это интервал между диском, который вращается с номинальной скоростью, и диск не вращается. Для накопителей на магнитной ленте это время, когда носитель будет полностью извлечен и доступен элементу выбора или оператору-человеку.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8<br/>                                                                                    |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                                          |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Модель \_ CIM**](cim-logicaldevice.md)
</dt> </dl>

 

