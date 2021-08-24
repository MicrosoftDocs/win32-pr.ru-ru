---
description: Класс CIM \_ ассоЦиатедсенсор связывает установленный датчик с логическим устройством. Датчик измеряет критические свойства ввода и вывода и может быть добавлен вместе с устройством или установлен поблизости.
ms.assetid: 8ccaa37f-b95f-4582-a694-23bdc15b8c8b
ms.tgt_platform: multiple
title: Класс CIM_AssociatedSensor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AssociatedSensor
- CIM_AssociatedSensor.Dependent
- CIM_AssociatedSensor.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4e70ac657cd1bacff2d396cad08253d50bca422dde2044f562dfda179396e18c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119701134"
---
# <a name="cim_associatedsensor-class"></a>\_Класс CIM ассоЦиатедсенсор

Класс **CIM \_ ассоЦиатедсенсор** связывает установленный датчик с логическим устройством. Датчик измеряет критические свойства ввода и вывода и может быть добавлен вместе с устройством или установлен поблизости.

> [!IMPORTANT]
> Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI. В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства. Свойства перечислены в алфавитном порядке, а не в MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
[Abstract, UUID("{956597A0-7D80-11D2-AAD3-006008C78BC7}"), AMENDMENT]
class CIM_AssociatedSensor : CIM_Dependency
{
  CIM_LogicalDevice REF Dependent;
  CIM_Sensor        REF Antecedent;
};
```

## <a name="members"></a>Члены

Класс **CIM \_ ассоЦиатедсенсор** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **CIM \_ ассоЦиатедсенсор** имеет следующие свойства.

<dl> <dt>

**Завершил**
</dt> <dd> <dl> <dt>

Тип данных: **\_ датчик CIM**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")
</dt> </dl>

[**\_ Датчик CIM**](cim-sensor.md) , описывающий датчик.

</dd> <dt>

**Него**
</dt> <dd> <dl> <dt>

Тип данных: **CIM \_** с типом "модель"
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")
</dt> </dl>

Логическая [**модель \_ CIM**](cim-logicaldevice.md) , описывающая логическое устройство, для которого данные измеряются датчиком.

</dd> </dl>

## <a name="remarks"></a>Remarks

Класс **CIM \_ ассоЦиатедсенсор** является производным от [**\_ зависимости CIM**](cim-dependency.md).

Инструментарий WMI не реализует этот класс. Дополнительные сведения о классах, производных от **CIM \_ ассоЦиатедсенсор**, см. в разделе [Классы Win32](win32-provider.md).

Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF. Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Пространство имен<br/>                | Корневой \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_Зависимость CIM**](cim-dependency.md)
</dt> </dl>

 

