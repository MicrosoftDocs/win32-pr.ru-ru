---
description: Класс CIM \_ директориконтаинсфиле представляет связь между каталогом и файлами, содержащимися в этом каталоге.
ms.assetid: e05ec86e-c3cf-4589-9815-83850e0c84ed
ms.tgt_platform: multiple
title: Класс CIM_DirectoryContainsFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DirectoryContainsFile
- CIM_DirectoryContainsFile.PartComponent
- CIM_DirectoryContainsFile.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 01707dfe4c0257803b864ce50ac05e792eabf8f30b7d944f5c2232526c8c65b3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119924264"
---
# <a name="cim_directorycontainsfile-class"></a>\_Класс CIM директориконтаинсфиле

Класс **CIM \_ директориконтаинсфиле** представляет связь между каталогом и файлами, содержащимися в этом каталоге.

> [!IMPORTANT]
> Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI. В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства. Свойства перечислены в алфавитном порядке, а не в MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{6F9D4740-8324-11d2-AAD9-006008C78BC7}"), AMENDMENT]
class CIM_DirectoryContainsFile : CIM_Component
{
  CIM_DataFile  REF PartComponent;
  CIM_Directory REF GroupComponent;
};
```

## <a name="members"></a>Члены

Класс **CIM \_ директориконтаинсфиле** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **CIM \_ директориконтаинсфиле** имеет следующие свойства.

<dl> <dt>

**Ссылка**
</dt> <dd> <dl> <dt>

Тип данных: **\_ Каталог CIM**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

[**\_ Каталог CIM**](cim-directory.md) , описывающий каталог.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Тип данных: **CIM \_ File**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")
</dt> </dl>

[**\_ Файл CIM**](cim-datafile.md) , описывающий LogicalFile, содержащийся в каталоге.

</dd> </dl>

## <a name="remarks"></a>Remarks

WMI реализует класс **CIM \_ директориконтаинсфиле** , который является динамическим классом.

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

[**\_Компонент CIM**](cim-component.md)
</dt> </dl>

 

