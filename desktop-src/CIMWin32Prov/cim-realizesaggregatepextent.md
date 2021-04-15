---
description: '\_Ассоциация РЕАЛИЗЕСАГГРЕГАТЕПЕКСТЕНТ CIM представляет связь, в которой \_ класс CIM аггрегатепекстент реализован на физическом носителе.'
ms.assetid: 420dde1d-daa8-4cd3-b3fd-c2aefdc1e217
ms.tgt_platform: multiple
title: Класс CIM_RealizesAggregatePExtent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_RealizesAggregatePExtent
- CIM_RealizesAggregatePExtent.Dependent
- CIM_RealizesAggregatePExtent.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: eb80414134534d09a4030e2e87003a660e69fd9f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655833"
---
# <a name="cim_realizesaggregatepextent-class"></a>\_Класс CIM реализесаггрегатепекстент

Ассоциация **\_ реализесаггрегатепекстент CIM** представляет связь, в которой класс [**CIM \_ аггрегатепекстент**](cim-aggregatepextent.md) реализован на физическом носителе.

> [!IMPORTANT]
> Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI. В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства. Свойства перечислены в алфавитном порядке, а не в MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
[Abstract, UUID("{FAF76B81-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_RealizesAggregatePExtent : CIM_Realizes
{
  CIM_AggregatePExtent REF Dependent;
  CIM_PhysicalMedia    REF Antecedent;
};
```

## <a name="members"></a>Члены

Класс **CIM \_ реализесаггрегатепекстент** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **CIM \_ реализесаггрегатепекстент** имеет следующие свойства.

<dl> <dt>

**Завершил**
</dt> <dd> <dl> <dt>

Тип данных: **CIM \_ фисикалмедиа**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

[**\_ Фисикалмедиа CIM**](cim-physicalmedia.md) , описывающий физический носитель, на котором реализован экстент.

</dd> <dt>

**Него**
</dt> <dd> <dl> <dt>

Тип данных: **CIM \_ аггрегатепекстент**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")
</dt> </dl>

[**\_ Аггрегатепекстент CIM**](cim-aggregatepextent.md) , расположенный на носителе.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Класс **CIM \_ реализесаггрегатепекстент** является производным от [**CIM \_**](cim-realizes.md).

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

[**\_Реализации CIM**](cim-realizes.md)
</dt> </dl>

 

