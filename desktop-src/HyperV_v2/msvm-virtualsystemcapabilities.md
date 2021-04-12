---
description: Описывает возможности связанной Мсвм \_ ComputerSystem.
ms.assetid: 7e3b51ba-f85d-4b83-abc6-a094d412eca1
title: Класс Msvm_VirtualSystemCapabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemCapabilities
- Msvm_VirtualSystemCapabilities.InstanceID
- Msvm_VirtualSystemCapabilities.Caption
- Msvm_VirtualSystemCapabilities.Description
- Msvm_VirtualSystemCapabilities.ElementName
- Msvm_VirtualSystemCapabilities.ElementNameEditSupported
- Msvm_VirtualSystemCapabilities.MaxElementNameLen
- Msvm_VirtualSystemCapabilities.RequestedStatesSupported
- Msvm_VirtualSystemCapabilities.ElementNameMask
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9fbd9b747e85ec1c9a1b7754f99282a7d913994e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262895"
---
# <a name="msvm_virtualsystemcapabilities-class"></a>\_Класс мсвм виртуалсистемкапабилитиес

Описывает возможности связанной [**мсвм \_ ComputerSystem**](msvm-computersystem.md).

Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemCapabilities : CIM_EnabledLogicalElementCapabilities
{
  string  InstanceID;
  string  Caption = "Hyper-V Virtual System Capabilities";
  string  Description = "Defines Virtual System Capabilities";
  string  ElementName = "Hyper-V Virtual System Capabilities";
  boolean ElementNameEditSupported = True;
  unit16  MaxElementNameLen = 100;
  unit16  RequestedStatesSupported[];
  string  ElementNameMask;
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ виртуалсистемкапабилитиес** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **мсвм \_ виртуалсистемкапабилитиес** имеет следующие свойства.

<dl> <dt>

**Заголовок**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Краткое описание объекта. Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**Описание**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Описание объекта. Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Отображаемое имя объекта. Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**елементнамидитсуппортед**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, можно ли изменить свойство **ElementName** . Это свойство наследуется от **CIM \_ енабледлогикалелементкапабилитиес**.

</dd> <dt>

**елементнамемаск**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Задает ограничения для **ElementName**, выраженные в виде регулярного выражения. Это свойство наследуется от **CIM \_ енабледлогикалелементкапабилитиес**.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **ключ**
</dt> </dl>

Уникально идентифицирует экземпляр этого класса. Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**макселементнамелен**
</dt> <dd> <dl> <dt>

Тип данных: **unit16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **MaxValue** (256)
</dt> </dl>

Задает максимальную поддерживаемую длину свойства **ElementName** . Это свойство наследуется от **CIM \_ енабледлогикалелементкапабилитиес**.

</dd> <dt>

**рекуестедстатессуппортед**
</dt> <dd> <dl> <dt>

Тип данных: массив **unit16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает возможные состояния, которые могут быть запрошены при использовании метода **RequestStateChange** для включенного логического элемента. Это свойство наследуется от **CIM \_ енабледлогикалелементкапабилитиес**.



| Значение                                                                         | Значение              |
|-------------------------------------------------------------------------------|----------------------|
| <dl> <dt>2</dt> </dl>  | Активировано<br/>   |
| <dl> <dt>3</dt> </dl>  | Отключит<br/>  |
| <dl> <dt>4</dt> </dl>  | Завершение работы<br/> |
| <dl> <dt>6</dt> </dl>  | Автономная миграция<br/>   |
| <dl> <dt>7</dt> </dl>  | Тест<br/>      |
| <dl> <dt>8</dt> </dl>  | Которого<br/>     |
| <dl> <dt>9</dt> </dl>  | Замораживани<br/>   |
| <dl> <dt>10</dt> </dl> | Перезагрузка<br/>    |
| <dl> <dt>11</dt> </dl> | Reset<br/>     |



 

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                                              |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                                                    |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

