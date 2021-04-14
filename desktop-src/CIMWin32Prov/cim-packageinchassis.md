---
description: Ассоциация CIM \_ паккажеинчассис представляет собой связь, в которой шасси может содержать другие пакеты, такие как другие шасси и платы.
ms.assetid: 3243bc0f-ce20-4108-b6e3-838bcb8f2fec
ms.tgt_platform: multiple
title: Класс CIM_PackageInChassis
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PackageInChassis
- CIM_PackageInChassis.LocationWithinContainer
- CIM_PackageInChassis.PartComponent
- CIM_PackageInChassis.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 26b65f983970c91d36e8d0a301277c67a2cc5639
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496272"
---
# <a name="cim_packageinchassis-class"></a>\_Класс CIM паккажеинчассис

Ассоциация **CIM \_ паккажеинчассис** представляет собой связь, в которой шасси может содержать другие пакеты, такие как другие шасси и платы.

> [!IMPORTANT]
> Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI. В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства. Свойства перечислены в алфавитном порядке, а не в MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
[Abstract, UUID("{FAF76B74-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PackageInChassis : CIM_Container
{
  string                  LocationWithinContainer;
  CIM_PhysicalPackage REF PartComponent;
  CIM_Chassis         REF GroupComponent;
};
```

## <a name="members"></a>Члены

Класс **CIM \_ паккажеинчассис** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **CIM \_ паккажеинчассис** имеет следующие свойства.

<dl> <dt>

**Ссылка**
</dt> <dd> <dl> <dt>

Тип данных: **CIM \_ Chassis**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

[**\_ Корпус CIM**](cim-chassis.md) , описывающий корпус, который содержит другие физические пакеты.

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

Тип данных: **CIM \_ фисикалпаккаже**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")
</dt> </dl>

[**\_ Фисикалпаккаже CIM**](cim-physicalpackage.md) , описывающий физический пакет, содержащийся в корпусе.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Класс **CIM \_ паккажеинчассис** является производным от [**\_ контейнера CIM**](cim-container.md).

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

[**\_Контейнер CIM**](cim-container.md)
</dt> </dl>

 

