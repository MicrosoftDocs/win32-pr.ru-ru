---
description: Связывает устройство хранения с контроллером хранилища, которому принадлежит устройство.
ms.assetid: 3DE05EDC-C54A-4C3C-9057-4418246037D5
title: Класс Msvm_ControlledBy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ControlledBy
- Msvm_ControlledBy.NegotiatedSpeed
- Msvm_ControlledBy.NegotiatedDataWidth
- Msvm_ControlledBy.Antecedent
- Msvm_ControlledBy.Dependent
- Msvm_ControlledBy.AccessState
- Msvm_ControlledBy.TimeOfDeviceReset
- Msvm_ControlledBy.NumberOfHardResets
- Msvm_ControlledBy.NumberOfSoftResets
- Msvm_ControlledBy.DeviceNumber
- Msvm_ControlledBy.AccessMode
- Msvm_ControlledBy.AccessPriority
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7986ffb842f7a1a104a0a8d846c1b6ee47a21523
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684269"
---
# <a name="msvm_controlledby-class"></a>\_Класс мсвм контролледби

Связывает устройство хранения с контроллером хранилища, которому принадлежит устройство. Эта ассоциация используется как с IDE, так и с контроллерами флоппи-дисковода.

Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ControlledBy : CIM_ControlledBy
{
  uint64                NegotiatedSpeed = 0;
  uint32                NegotiatedDataWidth = 0;
  CIM_Controller    REF Antecedent;
  CIM_LogicalDevice REF Dependent;
  uint16                AccessState = 1;
  datetime              TimeOfDeviceReset;
  uint32                NumberOfHardResets;
  uint32                NumberOfSoftResets;
  string                DeviceNumber;
  uint16                AccessMode = 2;
  uint16                AccessPriority = 0;
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ контролледби** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **мсвм \_ контролледби** имеет следующие свойства.

<dl> <dt>

**AccessMode**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Доступность устройства через предшествующий контроллер. Это свойство наследуется от [**CIM \_ контролледби**](/windows/desktop/CIMWin32Prov/cim-controlledby)и всегда имеет значение 2 (чтение и запись).

</dd> <dt>

**акцессприорити**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Приоритет, предоставляемый для доступа к устройству через этот контроллер. Путь с наивысшим приоритетом будет иметь наименьшее значение. Это свойство наследуется от [**CIM \_ контролледби**](/windows/desktop/CIMWin32Prov/cim-controlledby)и всегда имеет значение 0.

</dd> <dt>

**акцессстате**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, является ли контроллер активной командой или доступом к устройству. Это свойство наследуется от [**CIM \_ контролледби**](/windows/desktop/CIMWin32Prov/cim-controlledby)и всегда имеет значение 1 (активно).

</dd> <dt>

**Завершил**
</dt> <dd> <dl> <dt>

Тип данных: **[ **CIM \_ Controller**](/windows/desktop/CIMWin32Prov/cim-controller)**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Ссылка на контроллер. Это свойство наследуется от [**CIM \_ контролледби**](/windows/desktop/CIMWin32Prov/cim-controlledby).

</dd> <dt>

**Него**
</dt> <dd> <dl> <dt>

Тип данных: CIM с типом " **[ **модель \_** "](/windows/desktop/CIMWin32Prov/cim-logicaldevice)**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Ссылка на управляемое устройство. Это свойство наследуется от [**CIM \_ контролледби**](/windows/desktop/CIMWin32Prov/cim-controlledby).

</dd> <dt>

**девиценумбер**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Адрес связанного устройства в контексте предшествующего контроллера. Это свойство наследуется от [**CIM \_ контролледби**](/windows/desktop/CIMWin32Prov/cim-controlledby).

</dd> <dt>

**неготиатеддатавидс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Это свойство наследуется от [**CIM \_ девицеконнектион**](/windows/desktop/CIMWin32Prov/cim-deviceconnection)и всегда имеет значение 0.

</dd> <dt>

**неготиатедспид**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Это свойство наследуется от [**CIM \_ девицеконнектион**](/windows/desktop/CIMWin32Prov/cim-deviceconnection)и всегда имеет значение 0.

</dd> <dt>

**нумберофхардресетс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Это свойство наследуется от [**CIM \_ контролледби**](/windows/desktop/CIMWin32Prov/cim-controlledby), но не используется.

</dd> <dt>

**нумберофсофтресетс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Это свойство наследуется от [**CIM \_ контролледби**](/windows/desktop/CIMWin32Prov/cim-controlledby), но не используется.

</dd> <dt>

**тимеофдевицересет**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Это свойство наследуется от [**CIM \_ контролледби**](/windows/desktop/CIMWin32Prov/cim-controlledby), но не используется.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Доступ к классу **\_ контролледби мсвм** может быть ограничен фильтром контроля учетных записей. Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                                              |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                                                    |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_КОНТРОЛЛЕДБИ CIM**](cim-controlledby.md)
</dt> <dt>

[**\_КОНТРОЛЛЕДБИ CIM**](/windows/desktop/CIMWin32Prov/cim-controlledby)
</dt> <dt>

[Классы хранения](storage-classes.md)
</dt> </dl>

 

