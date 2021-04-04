---
description: Определяет параметры миграции виртуальной системы, управляемой экземпляром \_ класса CIM виртуалсистеммигратионсервице.
ms.assetid: c28ed48b-bacc-49c8-9131-2543c0edb3fd
title: Класс CIM_VirtualSystemMigrationSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemMigrationSettingData
- CIM_VirtualSystemMigrationSettingData.MigrationType
- CIM_VirtualSystemMigrationSettingData.Priority
- CIM_VirtualSystemMigrationSettingData.Bandwidth
- CIM_VirtualSystemMigrationSettingData.BandwidthUnit
- CIM_VirtualSystemMigrationSettingData.OtherTransportType
- CIM_VirtualSystemMigrationSettingData.TransportType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0d33479d0148bc4004fbbbda216e508c276c7ee9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813385"
---
# <a name="cim_virtualsystemmigrationsettingdata-class"></a>\_Класс CIM виртуалсистеммигратионсеттингдата

Определяет параметры миграции виртуальной системы, управляемой экземпляром класса [**CIM \_ виртуалсистеммигратионсервице**](cim-virtualsystemmigrationservice.md) .

## <a name="syntax"></a>Синтаксис

``` syntax
[Experimental, Abstract, Version("2.20.0"), UMLPackagePath("CIM::System::Virtualization"), AMENDMENT]
class CIM_VirtualSystemMigrationSettingData : CIM_SettingData
{
  uint16 MigrationType;
  uint16 Priority;
  uint16 Bandwidth;
  string BandwidthUnit;
  string OtherTransportType;
  uint16 TransportType;
};
```

## <a name="members"></a>Члены

Класс **CIM \_ виртуалсистеммигратионсеттингдата** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **CIM \_ виртуалсистеммигратионсеттингдата** имеет следующие свойства.

<dl> <dt>

**Пропускная способность**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**датчик**](/windows/desktop/WmiSdk/standard-qualifiers), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ виртуалсистеммигратионсеттингдата**.**Бандвидсунит**")
</dt> </dl>

Пропускная способность, назначенная или запрошенная для операции миграции виртуальной системы. "0" — пропускная способность по умолчанию для запросов на миграцию.

Свойства **пропускной способности** и **приоритета** можно использовать в сочетании. Процессы миграции, имеющие наивысшие значения **приоритета** , совместно используют доступную пропускную способность в зависимости от запрошенной пропускной способности. Если этот набор процессов потребляет не всю пропускную способность, процессы миграции со следующими более низкими значениями **приоритета** совместно используют оставшуюся пропускную способность. Если пропускная способность осталась, рассматриваются процессы миграции со следующими более низкими значениями **приоритета** .

Единица, используемая в свойстве **пропускной способности** , задается значением свойства **бандвидсунит** .

Если свойство **бандвидсунит** имеет значение «Percent», применяются следующие правила.

-   Значение свойства **пропускной способности** должно находиться в диапазоне от "0" до "100" с более высоким значением, указывающим на более высокую пропускную способность.
-   Значение "100" указывает всю доступную пропускную способность для выполнения операций миграции виртуальной системы.
-   Значения между "1" и "100" линейно сопоставляются с доступным диапазоном пропускной способности. Например, значение 50 запрашивает половину доступной пропускной способности.

</dd> <dt>

**бандвидсунит**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ виртуалсистеммигратионсеттингдата**.**Пропускная способность**"), **испунит**
</dt> </dl>

Единица, используемая свойством **пропускной способности** . Значением этого свойства должно быть допустимое значение квалификатора программных единиц, определенное в приложении C. 1 DSP0004 V 2.4 или более поздней версии.

> [!Note]  
> Такие профили, как DMTF DSP1081, определяют, как клиенты могут обнаруживать набор единиц, поддерживаемых реализацией, а также диапазоны и приращения значений свойства **пропускной способности** .

 

</dd> <dt>

**MigrationType**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Тип выполняемой операции миграции.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Неизвестно** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Другое** (1)


</dt> <dd></dd> <dt>

<span id="Live"></span><span id="live"></span><span id="LIVE"></span>

**Live** (2)


</dt> <dd></dd> <dt>

<span id="Resume"></span><span id="resume"></span><span id="RESUME"></span>

**Возобновление** (3)


</dt> <dd></dd> <dt>

<span id="Restart"></span><span id="restart"></span><span id="RESTART"></span>

**Перезапустить** (4)


</dt> <dd></dd> </dl>

</dd> <dt>

**осертранспорттипе**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ виртуалсистеммигратионсеттингдата**.**TransportType**")
</dt> </dl>

Тип транспорта, который необходимо применить, если значение **TransportType** равно "1" (другое).

</dd> <dt>

**Приоритет**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Важность относительной миграции, которую реализация миграции виртуальной системы может использовать для упорядочивания или назначения предпочтений между несколькими ожидающими запросами на миграцию. Чем ниже значение, тем выше приоритет. "0" — пропускная способность по умолчанию для запросов на миграцию.

</dd> <dt>

**TransportType**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ виртуалсистеммигратионсеттингдата**.**Осертранспорттипе**")
</dt> </dl>

Тип транспорта, применяемый к операции миграции виртуальной системы.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Неизвестно** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Другое** (1)


</dt> <dd></dd> <dt>

<span id="SSH"></span><span id="ssh"></span>

**SSH** (2)


</dt> <dd></dd> <dt>

<span id="TLS"></span><span id="tls"></span>

**TLS** (3)


</dt> <dd></dd> <dt>

<span id="TLS_Strict"></span><span id="tls_strict"></span><span id="TLS_STRICT"></span>

**TLS-точность** (4)


</dt> <dd></dd> <dt>

<span id="TCP"></span><span id="tcp"></span>

**TCP** (5)


</dt> <dd></dd> <dt>

<span id="IPC"></span><span id="ipc"></span>

**IPC** (6)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**Зарезервировано DMTF** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**Поставщик зарезервирован** (32768...)


</dt> <dd></dd> </dl>

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

[**\_SETTINGDATA CIM**](cim-settingdata.md)
</dt> </dl>

 

