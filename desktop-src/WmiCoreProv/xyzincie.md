---
description: Содержит координаты изображения в цветовом пространстве "Международная комиссия по освещения (ЦИЕ) XYZ".
ms.assetid: e44e8a5f-005d-4d58-84e3-135d4e396086
title: Класс КсизинЦие
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- XYZinCIE
- XYZinCIE.X
- XYZinCIE.Y
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: ba7f781a83f3e6ba5aa4683003386a0478d65088
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712676"
---
# <a name="xyzincie-class"></a>Класс КсизинЦие

Класс WMI **ксизинЦие** содержит координаты дисплея в цветовом пространстве «Международная комиссия по освещения (ЦИЕ) XYZ».

## <a name="syntax"></a>Синтаксис

``` syntax
class XYZinCIE : WmiMonitorColorCharacteristics
{
  uint16 X;
  uint16 Y;
};
```

## <a name="members"></a>Члены

Класс **ксизинЦие** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **ксизинЦие** имеет следующие свойства.

<dl> <dt>

**X**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Координата по оси X.

</dd> <dt>

**да**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Координата по оси Y.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Класс [**вмимониторколорчарактеристикс**](wmimonitorcolorcharacteristics.md) содержит внедренные экземпляры класса **ксизинЦие** для описания цветовых характеристик монитора.

Чтобы вычислить координату z на основе значений x и y, используйте отношение \| \| (x, y, z) \| \| = 1.

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

 

 




