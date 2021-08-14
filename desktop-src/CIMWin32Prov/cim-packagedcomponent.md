---
description: Ассоциация CIM \_ паккажедкомпонент представляет собой явную связь, в которой компонент обычно содержится в физическом пакете, таком как шасси или плата.
ms.assetid: ef0cdbc4-41ee-4517-92ca-61cfcbe64c36
ms.tgt_platform: multiple
title: Класс CIM_PackagedComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PackagedComponent
- CIM_PackagedComponent.LocationWithinContainer
- CIM_PackagedComponent.PartComponent
- CIM_PackagedComponent.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: deda43cc153baf320f5c927438314114edf3ec2d92d9e96af95707d1b7805e56
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118422034"
---
# <a name="cim_packagedcomponent-class"></a>\_Класс CIM паккажедкомпонент

Ассоциация **CIM \_ паккажедкомпонент** представляет собой явную связь, в которой компонент обычно содержится в физическом пакете, таком как шасси или плата.

**Примечание**  .  Компонент может быть удален из или еще не вставлен в, содержащий его пакет (то есть **съемное** логическое свойство имеет **значение true**). Таким образом, компонент не всегда связан с контейнером.

> [!IMPORTANT]
> Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI. В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства. Свойства перечислены в алфавитном порядке, а не в MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
[Abstract, UUID("{FAF76B79-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PackagedComponent : CIM_Container
{
  string                    LocationWithinContainer;
  CIM_PhysicalComponent REF PartComponent;
  CIM_PhysicalPackage   REF GroupComponent;
};
```

## <a name="members"></a>Члены

Класс **CIM \_ паккажедкомпонент** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **CIM \_ паккажедкомпонент** имеет следующие свойства.

<dl> <dt>

**Ссылка**
</dt> <dd> <dl> <dt>

Тип данных: **CIM \_ фисикалпаккаже**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

[**\_ Фисикалпаккаже CIM**](cim-physicalpackage.md) , описывающий физический пакет, содержащий компоненты.

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

Тип данных: **CIM \_ фисикалкомпонент**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")
</dt> </dl>

[**\_ Фисикалкомпонент CIM**](cim-physicalcomponent.md) , описывающий физический компонент, содержащийся в пакете.

</dd> </dl>

## <a name="remarks"></a>Remarks

Класс **CIM \_ паккажедкомпонент** является производным от [**\_ контейнера CIM**](cim-container.md).

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

[**\_Контейнер CIM**](cim-container.md)
</dt> </dl>

 

