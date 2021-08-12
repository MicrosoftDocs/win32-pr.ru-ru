---
description: Класс CIM \_ пекстентредунданцикомпонент представляет физические экстенты, участвующие в группе избыточности хранилища.
ms.assetid: 5a4bb1e8-7b99-410a-bba5-2c63beabd00e
ms.tgt_platform: multiple
title: Класс CIM_PExtentRedundancyComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PExtentRedundancyComponent
- CIM_PExtentRedundancyComponent.PartComponent
- CIM_PExtentRedundancyComponent.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d19d1c9fa504b30f7a87dcd1402f47376a0f4613095e9f2ee25d196cd60ae581
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118678658"
---
# <a name="cim_pextentredundancycomponent-class"></a>\_Класс CIM пекстентредунданцикомпонент

Класс **CIM \_ пекстентредунданцикомпонент** представляет физические экстенты, участвующие в группе избыточности хранилища.

> [!IMPORTANT]
> Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI. В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства. Свойства перечислены в алфавитном порядке, а не в MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
[Abstract, UUID("{AD3C1FA2-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_PExtentRedundancyComponent : CIM_RedundancyComponent
{
  CIM_PhysicalExtent         REF PartComponent;
  CIM_StorageRedundancyGroup REF GroupComponent;
};
```

## <a name="members"></a>Члены

Класс **CIM \_ пекстентредунданцикомпонент** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **CIM \_ пекстентредунданцикомпонент** имеет следующие свойства.

<dl> <dt>

**Ссылка**
</dt> <dd> <dl> <dt>

Тип данных: **CIM \_ сторажередунданциграуп**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")
</dt> </dl>

[**\_ Сторажередунданциграуп CIM**](cim-storageredundancygroup.md) , описывающий группу избыточности хранилища.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Тип данных: **CIM \_ фисикалекстент**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")
</dt> </dl>

[**\_ Фисикалекстент CIM**](cim-physicalextent.md) , описывающий физическое пространство, участвующее в группе избыточности.

</dd> </dl>

## <a name="remarks"></a>Remarks

Класс **CIM \_ пекстентредунданцикомпонент** является производным от [**CIM \_ редунданцикомпонент**](cim-redundancycomponent.md).

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

[**\_РЕДУНДАНЦИКОМПОНЕНТ CIM**](cim-redundancycomponent.md)
</dt> </dl>

 

