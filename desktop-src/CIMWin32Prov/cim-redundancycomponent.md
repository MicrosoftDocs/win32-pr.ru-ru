---
description: Класс CIM \_ редунданцикомпонент связывает группу избыточности, состоящую из управляемых системных элементов, и указывает, что вместе элементы обеспечивают избыточность.
ms.assetid: 2511ae26-011a-4e0d-ad34-d5fe9c78f0ff
ms.tgt_platform: multiple
title: Класс CIM_RedundancyComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_RedundancyComponent
- CIM_RedundancyComponent.GroupComponent
- CIM_RedundancyComponent.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5bcd1c16417ba0c02e13579f9e471076d4c61818
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895414"
---
# <a name="cim_redundancycomponent-class"></a>\_Класс CIM редунданцикомпонент

Класс **CIM \_ редунданцикомпонент** связывает группу избыточности, состоящую из управляемых системных элементов, и указывает, что вместе элементы обеспечивают избыточность. Все элементы, Объединенные в группу избыточности, должны быть экземплярами одного и того же класса объектов.

> [!IMPORTANT]
> Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI. В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства. Свойства перечислены в алфавитном порядке, а не в MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
[Abstract, UUID("{FB9D6E62-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_RedundancyComponent : CIM_Component
{
  CIM_RedundancyGroup      REF GroupComponent;
  CIM_ManagedSystemElement REF PartComponent;
};
```

## <a name="members"></a>Члены

Класс **CIM \_ редунданцикомпонент** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **CIM \_ редунданцикомпонент** имеет следующие свойства.

<dl> <dt>

**Ссылка**
</dt> <dd> <dl> <dt>

Тип данных: **CIM \_ редунданциграуп**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")
</dt> </dl>

Ассоциация **\_ редунданцикомпонент CIM** указывает, что "Этот набор вентиляторов" или "эти физические экстенты" участвуют в одной группе избыточности.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Тип данных: **CIM \_ манажедсистемелемент**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

[**\_ Манажедсистемелемент CIM**](cim-managedsystemelement.md) , описывающий дочерний элемент в ассоциации.

Это свойство наследуется [**от \_ компонента CIM**](cim-component.md).

</dd> </dl>

## <a name="remarks"></a>Комментарии

**Модель CIM \_ Редунданцикомпонент** является производным [**от \_ компонента CIM**](cim-component.md).

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

[**\_Компонент CIM**](cim-component.md)
</dt> </dl>

 

