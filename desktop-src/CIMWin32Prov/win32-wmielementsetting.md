---
description: '\_Класс WMI взаимосвязей Win32 вмиелементсеттинг связывает службу, работающую в системе Windows, и параметры WMI, которые она может использовать.'
ms.assetid: 00e9f882-5f54-4042-a916-2f90ed9a37c0
ms.tgt_platform: multiple
title: Класс Win32_WMIElementSetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_WMIElementSetting
- Win32_WMIElementSetting.Element
- Win32_WMIElementSetting.Setting
api_type:
- DllExport
api_location:
- Wbemcore.dll
ms.openlocfilehash: 41f79614fd0931759d502bbd61c7f4143e9e7dc9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895454"
---
# <a name="win32_wmielementsetting-class"></a>\_Класс Win32 вмиелементсеттинг

[Класс WMI](../wmisdk/retrieving-a-class.md) взаимосвязей **Win32 \_ вмиелементсеттинг** связывает службу, работающую в системе Windows, и параметры WMI, которые она может использовать.

Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства. Свойства и методы имеют алфавитный порядок, а не порядок MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
[Dynamic, Provider("WBEMCORE"), UUID("{A83EF167-CA8D-11d2-B33D-00104BCC4B4A}"), AMENDMENT]
class Win32_WMIElementSetting : CIM_ElementSetting
{
  Win32_Service    REF Element;
  Win32_WMISetting REF Setting;
};
```

## <a name="members"></a>Члены

Класс **Win32 \_ вмиелементсеттинг** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **Win32 \_ вмиелементсеттинг** имеет следующие свойства.

<dl> <dt>

**Элемент**
</dt> <dd> <dl> <dt>

Тип данных: **\_ служба Win32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**ключ**](../wmisdk/key-qualifier.md), [**Переопределение**](../wmisdk/standard-qualifiers.md) ("элемент"), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| Служба WMI Win32 \_ ")
</dt> </dl>

Ссылка на экземпляр, представляющий службу Windows, с помощью или свойств WMI отображая.

</dd> <dt>

**Параметр**
</dt> <dd> <dl> <dt>

Тип данных: **Win32 \_ вмисеттинг**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**ключ**](../wmisdk/key-qualifier.md), [**Переопределение**](../wmisdk/standard-qualifiers.md) ("параметр"), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ вмисеттинг")
</dt> </dl>

Ссылка на экземпляр, представляющий параметры WMI, доступные для службы Windows.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Класс **Win32 \_ вмиелементсеттинг** является производным от [**CIM \_ елементсеттинг**](cim-elementsetting.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Пространство имен<br/>                | Корневой \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemcore.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_ЕЛЕМЕНТСЕТТИНГ CIM**](cim-elementsetting.md)
</dt> <dt>

[Классы управления службами WMI](./wmi-service-management-classes.md)
</dt> </dl>

 

 
