---
description: Предоставляет дополнительные сведения для использования с методом CreateSnapshot \_ класса Виртуалсистемснапшотсервице мсвм.
ms.assetid: d4a025c4-6a3c-4ae0-8f2c-421c1aa1eb23
title: Класс Msvm_VirtualSystemSnapshotSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemSnapshotSettingData
- Msvm_VirtualSystemSnapshotSettingData.ConsistencyLevel
- Msvm_VirtualSystemSnapshotSettingData.IgnoreNonSnapshottableDisks
- Msvm_VirtualSystemSnapshotSettingData.GuestBackupType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 32ab52da97e9fcc943c3a70548bb6b1a6d7994a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423686"
---
# <a name="msvm_virtualsystemsnapshotsettingdata-class"></a>\_Класс мсвм виртуалсистемснапшотсеттингдата

Предоставляет дополнительные сведения для использования с методом [**CreateSnapshot**](cim-virtualsystemsnapshotservice-createsnapshot.md) класса [**\_ виртуалсистемснапшотсервице мсвм**](msvm-virtualsystemsnapshotservice.md) .

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[AMENDMENT]
class Msvm_VirtualSystemSnapshotSettingData : CIM_SettingData
{
  uint8   ConsistencyLevel;
  boolean IgnoreNonSnapshottableDisks;
  uint8   GuestBackupType;
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ виртуалсистемснапшотсеттингдата** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **мсвм \_ виртуалсистемснапшотсеттингдата** имеет следующие свойства.

<dl> <dt>

**ConsistencyLevel**
</dt> <dd> <dl> <dt>

Тип данных: **Uint8**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Уровень согласованности моментального снимка.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Неизвестно** (0)


</dt> <dd></dd> <dt>

<span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>

С **совместимостью приложений** (1)


</dt> <dd></dd> <dt>

<span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>

**Отказоустойчивость (2** )


</dt> <dd></dd> </dl>

</dd> <dt>

**гуестбаккуптипе**
</dt> <dd> <dl> <dt>

Тип данных: **Uint8**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Тип резервной копии, который будет использоваться в гостевой системе.

> [!Note]  
> Свойство добавлено в Windows 10, версия 1703

 

<dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

**Undefined** (0)


</dt> <dd></dd> <dt>

<span id="Full"></span><span id="full"></span><span id="FULL"></span>

**Full** (1)


</dt> <dd></dd> <dt>

<span id="Copy"></span><span id="copy"></span><span id="COPY"></span>

**Копирование** (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**игноренонснапшоттабледискс**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, пропускаются ли не снапшоттабле диски, такие как транзитные диски и диски Fibre Channel, во время создания моментального снимка.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ настольных приложений Windows 10\]<br/>                                                             |
| Минимальная версия сервера<br/> | Windows Server 2016<br/>                                                                          |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_SETTINGDATA CIM**](cim-settingdata.md)
</dt> </dl>

 

 




