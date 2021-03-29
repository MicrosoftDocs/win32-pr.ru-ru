---
description: '\_Ассоциация АДЖАЦЕНТСЛОТС CIM описывает расположение слотов на плате размещения или адаптере карты.'
ms.assetid: d604647f-7b2f-4f99-8d98-adf115ae9dfb
ms.tgt_platform: multiple
title: Класс CIM_AdjacentSlots
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AdjacentSlots
- CIM_AdjacentSlots.DistanceBetweenSlots
- CIM_AdjacentSlots.SharedSlots
- CIM_AdjacentSlots.SlotA
- CIM_AdjacentSlots.SlotB
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 695f9c668d6f75864e46026deac9a969993596ff
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104142109"
---
# <a name="cim_adjacentslots-class"></a>\_Класс CIM аджацентслотс

Ассоциация **\_ аджацентслотс CIM** описывает расположение слотов на плате размещения или адаптере карты. Такие сведения, как расстояние между слотами и то, являются ли они общими (если один из них заполнен, другие слоты не могут использоваться), передаются как свойства связи.

> [!IMPORTANT]
> Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI. В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства. Свойства перечислены в алфавитном порядке, а не в MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
[Abstract, Association, UUID("{FAF76B88-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_AdjacentSlots
{
  real32       DistanceBetweenSlots;
  boolean      SharedSlots;
  CIM_Slot REF SlotA;
  CIM_Slot REF SlotB;
};
```

## <a name="members"></a>Члены

Класс **CIM \_ аджацентслотс** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **CIM \_ аджацентслотс** имеет следующие свойства.

<dl> <dt>

**дистанцебетвинслотс**
</dt> <dd> <dl> <dt>

Тип данных: **real32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("дюймы")
</dt> </dl>

Расстояние в дюймах между соседними слотами.

</dd> <dt>

**шаредслотс**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Если **значение равно true**, один из слотов заполняется платой адаптера; другой слот необходимо оставить пустым.

</dd> <dt>

**Разъем a**
</dt> <dd> <dl> <dt>

Тип данных: **\_ слот CIM**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Ссылка на один из соседних слотов.

</dd> <dt>

**слотб**
</dt> <dd> <dl> <dt>

Тип данных: **\_ слот CIM**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Ссылка на смежный слот.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Инструментарий WMI не реализует этот класс.

Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF. Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Пространство имен<br/>                | Корневой \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Классы CIM](/windows/desktop/WmiSdk/cimclas)
</dt> </dl>

 

