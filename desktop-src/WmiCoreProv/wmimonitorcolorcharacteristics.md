---
description: Представляет характеристики цвета "Международная комиссия по освещения (ЦИЕ)" монитора компьютера.
ms.assetid: 476aefae-11c0-46be-a2bb-83fbafd70421
title: Класс Вмимониторколорчарактеристикс
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorColorCharacteristics
- WmiMonitorColorCharacteristics.Active
- WmiMonitorColorCharacteristics.Blue
- WmiMonitorColorCharacteristics.DefaultWhite
- WmiMonitorColorCharacteristics.Green
- WmiMonitorColorCharacteristics.InstanceName
- WmiMonitorColorCharacteristics.Red
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 9fbb7d56e56519576d257b077311a144e923d6bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346505"
---
# <a name="wmimonitorcolorcharacteristics-class"></a>Класс Вмимониторколорчарактеристикс

Класс **вмимониторколорчарактеристикс** представляет характеристики цвета международной комиссии по освещения (Цие) монитора компьютера. Данные соответствуют данным в блоке цветовых характеристик для расширенной структуры расширенных отображаемых идентификационных данных (E-EDID).

## <a name="syntax"></a>Синтаксис

``` syntax
class WmiMonitorColorCharacteristics : MSMonitorClass
{
  boolean  Active;
  XYZinCIE Blue;
  XYZinCIE DefaultWhite;
  XYZinCIE Green;
  string   InstanceName;
  XYZinCIE Red;
};
```

## <a name="members"></a>Члены

Класс **вмимониторколорчарактеристикс** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **вмимониторколорчарактеристикс** имеет следующие свойства.

<dl> <dt>

**Активен**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает активный монитор.

</dd> <dt>

**Синий**
</dt> <dd> <dl> <dt>

Тип данных: **[ **ксизинЦие**](xyzincie.md)**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

ЦИЕ координаты синего, представленные экземпляром класса [**ксизинЦие**](xyzincie.md) .

</dd> <dt>

**дефаултвхите**
</dt> <dd> <dl> <dt>

Тип данных: **[ **ксизинЦие**](xyzincie.md)**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Белые координаты ЦИЕ по умолчанию.

</dd> <dt>

**Зеленый**
</dt> <dd> <dl> <dt>

Тип данных: **[ **ксизинЦие**](xyzincie.md)**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

ЦИЕ координаты зеленого цвета, представленные экземпляром класса [**ксизинЦие**](xyzincie.md) .

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

</dd> <dt>

**Красный**
</dt> <dd> <dl> <dt>

Тип данных: **[ **ксизинЦие**](xyzincie.md)**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

ЦИЕ координаты красного, представленные экземпляром класса [**ксизинЦие**](xyzincie.md) .

</dd> </dl>

## <a name="remarks"></a>Комментарии

Значения «Цветность» и «белая точка» выражаются в виде дробных чисел в формате кодировки. Этот формат является точным для тысячового расположения, длина которого равна 10 битам. Самый значащий бит (старший) представляет 2 ^-1, а наименьший значащий бит (ЛСБ) представляет 2 ^-10 коэффициенты соответственно. Точность сохраненных значений в структуре E-EDID v1. x должна быть точной до +/-0,005 фактического значения.

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

 

 




