---
description: Содержит методы, управляющие яркостью монитора.
ms.assetid: e7e4139e-b985-4163-9c95-03008a2cc8cb
title: Класс Вмимониторбригхтнессмесодс
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorBrightnessMethods
- WmiMonitorBrightnessMethods.Active
- WmiMonitorBrightnessMethods.InstanceName
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 36fe823703d5d5e4f1f6008d02c600828fe2b53f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674018"
---
# <a name="wmimonitorbrightnessmethods-class"></a>Класс Вмимониторбригхтнессмесодс

Класс WMI **вмимониторбригхтнессмесодс** содержит методы, управляющие яркостью монитора.

## <a name="syntax"></a>Синтаксис

``` syntax
class WmiMonitorBrightnessMethods
{
  boolean Active;
  string  InstanceName;
};
```

## <a name="members"></a>Члены

Класс **вмимониторбригхтнессмесодс** имеет следующие типы членов:

-   [Методы](#wmimonitorbrightnessmethods-class)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Класс **вмимониторбригхтнессмесодс** содержит следующие методы.



| Метод                                                                                                         | Описание                                                    |
|:---------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------|
| [**вмиреверттополицибригхтнесс**](wmireverttopolicybrightness-method-in-class-wmimonitorbrightnessmethods.md) | Задает значение яркости для параметра политики.<br/>     |
| [**вмисеталсбригхтнесс**](wmisetalsbrightness-method-in-class-wmimonitorbrightnessmethods.md)                 | Задает значение яркости датчика окружающего освещения.<br/>     |
| [**вмисеталсбригхтнессстате**](wmisetalsbrightnessstate-method-in-class-wmimonitorbrightnessmethods.md)       | Управляет состоянием яркости датчика внешнего освещения.<br/> |
| [**вмисетбригхтнесс**](wmisetbrightness-method-in-class-wmimonitorbrightnessmethods.md)                       | Задает яркость монитора.<br/>                        |



 

### <a name="properties"></a>Свойства

Класс **вмимониторбригхтнессмесодс** имеет следующие свойства.

<dl> <dt>

**Активен**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает активный монитор.

</dd> <dt>

**InstanceName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **ключ**
</dt> </dl>

Имя конкретного экземпляра монитора.

</dd> </dl>

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

 

 




