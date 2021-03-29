---
description: Представляет связь между контроллером и логическим устройством, которое управляется контроллером.
ms.assetid: 5a938fa4-3b91-42ad-beee-12ed0ce6df9a
title: Класс CIM_ControlledBy (Управление Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ControlledBy
- CIM_ControlledBy.Antecedent
- CIM_ControlledBy.Dependent
- CIM_ControlledBy.AccessState
- CIM_ControlledBy.TimeOfDeviceReset
- CIM_ControlledBy.NumberOfHardResets
- CIM_ControlledBy.NumberOfSoftResets
- CIM_ControlledBy.DeviceNumber
- CIM_ControlledBy.AccessMode
- CIM_ControlledBy.AccessPriority
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7b035a93c47f9c33d981614ba6fc46b35f916e7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897894"
---
# <a name="cim_controlledby-class-hyper-v-management"></a>Класс CIM_ControlledBy (Управление Hyper-V)

Представляет связь между контроллером и логическим устройством, которое управляется контроллером.

## <a name="syntax"></a>Синтаксис

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Device::Controller"), AMENDMENT]
class CIM_ControlledBy : CIM_DeviceConnection
{
  CIM_Controller    REF Antecedent;
  CIM_LogicalDevice REF Dependent;
  uint16                AccessState;
  datetime              TimeOfDeviceReset;
  uint32                NumberOfHardResets;
  uint32                NumberOfSoftResets;
  string                DeviceNumber;
  uint16                AccessMode;
  uint16                AccessPriority;
};
```

## <a name="members"></a>Члены

Класс **CIM \_ контролледби** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **CIM \_ контролледби** имеет следующие свойства.

<dl> <dt>

**AccessMode**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Это свойство описывает доступность устройства через контроллер.

<dt>

<span id="ReadWrite"></span><span id="readwrite"></span><span id="READWRITE"></span>

**ReadWrite** (2)


</dt> <dd></dd> <dt>

<span id="ReadOnly"></span><span id="readonly"></span><span id="READONLY"></span>

**ReadOnly** (3)


</dt> <dd></dd> <dt>

<span id="NoAccess"></span><span id="noaccess"></span><span id="NOACCESS"></span>

**Недоступно** (4)


</dt> <dd></dd> </dl>

</dd> <dt>

**акцессприорити**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Приоритет доступа устройства через контроллер. Более низкое значение указывает более высокий приоритет.

</dd> <dt>

**акцессстате**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, активно ли устройство управляет устройством.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Неизвестно** (0)


</dt> <dd></dd> <dt>

<span id="Active"></span><span id="active"></span><span id="ACTIVE"></span>

**Активно** (1)


</dt> <dd></dd> <dt>

<span id="Inactive"></span><span id="inactive"></span><span id="INACTIVE"></span>

**Неактивно** (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**Завершил**
</dt> <dd> <dl> <dt>

Тип данных: **CIM \_ Controller**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")
</dt> </dl>

Контроллер.

</dd> <dt>

**Него**
</dt> <dd> <dl> <dt>

Тип данных: **CIM \_** с типом "модель"
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")
</dt> </dl>

Логические устройства.

</dd> <dt>

**девиценумбер**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Адрес связанного устройства в контексте контроллера.

</dd> <dt>

**нумберофхардресетс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **Счетчик**
</dt> </dl>

Число жестких сбросов, выданных контроллером. Жесткий сброс возвращает устройство в состояние инициализации или загрузки, после чего теряются все внутренние сведения о состоянии устройства и данные.

</dd> <dt>

**нумберофсофтресетс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **Счетчик**
</dt> </dl>

Число мягких сбросов, выданных контроллером. При мягком сбросе состояние устройства или данные не удаляются.

</dd> <dt>

**тимеофдевицересет**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Время последнего сброса подчиненного устройства контроллером.

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

[**\_ДЕВИЦЕКОННЕКТИОН CIM**](cim-deviceconnection.md)
</dt> </dl>

 

