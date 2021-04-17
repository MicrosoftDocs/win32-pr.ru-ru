---
description: Представляет параметры яркости монитора компьютера.
ms.assetid: 01fa3efc-2a1d-4405-989f-2c180842c6b9
title: Класс Вмимониторбригхтнесс
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorBrightness
- WmiMonitorBrightness.Active
- WmiMonitorBrightness.CurrentBrightness
- WmiMonitorBrightness.InstanceName
- WmiMonitorBrightness.Level
- WmiMonitorBrightness.Levels
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: b8d16c8dc20291a03fb205441c8826c85125970c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703021"
---
# <a name="wmimonitorbrightness-class"></a>Класс Вмимониторбригхтнесс

Класс WMI **вмимониторбригхтнесс** представляет параметры яркости монитора компьютера.

## <a name="syntax"></a>Синтаксис

``` syntax
class WmiMonitorBrightness : MSMonitorClass
{
  boolean Active;
  uint8   CurrentBrightness;
          InstanceName;
  uint8   Level[];
  uint32  Levels;
};
```

## <a name="members"></a>Члены

Класс **вмимониторбригхтнесс** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **вмимониторбригхтнесс** имеет следующие свойства.

<dl> <dt>

**Активен**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, активен ли целевой монитор.

</dd> <dt>

**куррентбригхтнесс**
</dt> <dd> <dl> <dt>

Тип данных: **Uint8**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Текущая яркость. Это значение должно быть значением, взятым из *уровней*.

Пример: 100

</dd> <dt>

InstanceName
</dt> <dd> <dl> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: ключ
</dt> </dl>

Имя конкретного экземпляра монитора.

</dd> <dt>

**Уровень**
</dt> <dd> <dl> <dt>

Тип данных: массив **Uint8**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Массив, содержащий возможные уровни яркости.

Пример: \[ 0, 1, 2,..., 100 \] .

</dd> <dt>

**Уровни**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Общее число уровней яркости, поддерживаемых монитором, как описано в разделе *уровень*.

Пример: 101

</dd> </dl>

## <a name="examples"></a>Примеры

Дополнительные сведения и примеры кода по использованию этого класса в PowerShell см. в разделе [Использование PowerShell для сообщения и Установка яркости монитора](https://blogs.technet.com/b/heyscriptingguy/archive/2013/07/25/use-powershell-to-report-and-set-monitor-brightness.aspx).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                               |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                         |
| Пространство имен<br/>                | Корневой \\ инструментарий WMI<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>Вмикоре. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WmiProv.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**мсмониторкласс**](msmonitorclass.md)
</dt> </dl>

 

 




