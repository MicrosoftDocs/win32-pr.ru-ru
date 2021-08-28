---
description: Класс CIM \_ кардинслот связывает адаптер адаптера с контейнером, в который он вставлен.
ms.assetid: 253fb444-2a9e-4099-a4d5-352b643d8e32
ms.tgt_platform: multiple
title: Класс CIM_CardInSlot
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CardInSlot
- CIM_CardInSlot.Dependent
- CIM_CardInSlot.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2653160c536d9fd11668e5038ae632b09414cae42ed5ae76d998f3abda85eeec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119322554"
---
# <a name="cim_cardinslot-class"></a>\_Класс CIM кардинслот

Класс **CIM \_ кардинслот** связывает адаптер адаптера с контейнером, в который он вставлен.

> [!IMPORTANT]
> Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI. В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства. Свойства перечислены в алфавитном порядке, а не в MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
[Abstract, MappingStrings("MIF.DMTF|System Slot|004.4"), UUID("{FAF76B8A-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_CardInSlot : CIM_PackageInSlot
{
  CIM_Card REF Dependent;
  CIM_Slot REF Antecedent;
};
```

## <a name="members"></a>Члены

Класс **CIM \_ кардинслот** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **CIM \_ кардинслот** имеет следующие свойства.

<dl> <dt>

**Завершил**
</dt> <dd> <dl> <dt>

Тип данных: **\_ слот CIM**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")
</dt> </dl>

[**\_ Слот CIM**](cim-slot.md) , описывающий слот, в который вставлена карта.

</dd> <dt>

**Него**
</dt> <dd> <dl> <dt>

Тип данных: **\_ карта CIM**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

[**\_ Карта CIM**](cim-card.md) , которая описывает карточку в слоте.

</dd> </dl>

## <a name="remarks"></a>Remarks

Класс **CIM \_ кардинслот** является производным от [**CIM \_ паккажеинслот**](cim-packageinslot.md).

Инструментарий WMI не реализует этот класс.

Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF. Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Пространство имен<br/>                | Корневой \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_ПАККАЖЕИНСЛОТ CIM**](cim-packageinslot.md)
</dt> </dl>

 

