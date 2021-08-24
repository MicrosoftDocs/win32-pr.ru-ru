---
description: Класс CIM \_ меморйонкард связывает физическую память, размещенную на досках размещения, платах адаптеров и т. д. Эта ассоциация явно определяет связь памяти с картами.
ms.assetid: 0d094cad-c542-4794-b6e1-87cdc8067668
ms.tgt_platform: multiple
title: Класс CIM_MemoryOnCard
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MemoryOnCard
- CIM_MemoryOnCard.LocationWithinContainer
- CIM_MemoryOnCard.PartComponent
- CIM_MemoryOnCard.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a07a8894e237be24a4c7b49e8491278ffb9e9ea82109fee00c27fc4eb9d5fcb5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119506794"
---
# <a name="cim_memoryoncard-class"></a>\_Класс CIM меморйонкард

Класс **CIM \_ меморйонкард** связывает физическую память, размещенную на досках размещения, платах адаптеров и т. д. Эта ассоциация явно определяет связь памяти с картами.

> [!IMPORTANT]
> Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI. В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства. Свойства перечислены в алфавитном порядке, а не в MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
[Abstract, UUID("{FAF76B7C-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_MemoryOnCard : CIM_PackagedComponent
{
  string                 LocationWithinContainer;
  CIM_PhysicalMemory REF PartComponent;
  CIM_Card           REF GroupComponent;
};
```

## <a name="members"></a>Члены

Класс **CIM \_ меморйонкард** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **CIM \_ меморйонкард** имеет следующие свойства.

<dl> <dt>

**Ссылка**
</dt> <dd> <dl> <dt>

Тип данных: **\_ карта CIM**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

[**\_ Карта CIM**](cim-card.md) , описывающая карточку, которая включает в себя или "содержит" память.

</dd> <dt>

**локатионвисинконтаинер**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Произвольная строка, представляющая расположение физического элемента в физическом пакете. Сведения относительно стационарных элементов в контейнере (например, "второй отсек для дисков сверху"), углы, высота и другие данные могут быть записаны в это свойство. Эта строка может дополнять или использоваться вместо создания экземпляра объекта [**\_ расположения CIM**](cim-location.md) .

Это свойство наследуется от [**CIM- \_ контейнера**](cim-container.md).

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Тип данных: **CIM \_ фисикалмемори**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")
</dt> </dl>

[**\_ Фисикалмемори CIM**](cim-physicalmemory.md) , описывающий физическую память, расположенную на карте.

</dd> </dl>

## <a name="remarks"></a>Remarks

Класс **CIM \_ меморйонкард** является производным от [**CIM \_ паккажедкомпонент**](cim-packagedcomponent.md).

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



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_ПАККАЖЕДКОМПОНЕНТ CIM**](cim-packagedcomponent.md)
</dt> </dl>

 

