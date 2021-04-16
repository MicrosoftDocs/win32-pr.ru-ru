---
description: Класс CIM \_ елементсеттинг представляет ассоциацию между управляемыми системными элементами и определенным для них классом параметров.
ms.assetid: e9b7c43f-7539-48c3-8679-568fb4b036bb
ms.tgt_platform: multiple
title: Класс CIM_ElementSetting (поставщики WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ElementSetting
- CIM_ElementSetting.Element
- CIM_ElementSetting.Setting
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2c1ea52648728397e811cfae35e7a83e272ab8d3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655919"
---
# <a name="cim_elementsetting-class-cimwin32-wmi-providers"></a>Класс CIM_ElementSetting (поставщики WMI CIMWin32)

Класс **CIM \_ елементсеттинг** представляет ассоциацию между управляемыми системными элементами и определенным для них классом параметров.

> [!IMPORTANT]
> Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI. В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства. Свойства перечислены в алфавитном порядке, а не в MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
[Abstract, Association, UUID("{8502C577-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_ElementSetting
{
  CIM_ManagedSystemElement REF Element;
  CIM_Setting              REF Setting;
};
```

## <a name="members"></a>Члены

Класс **CIM \_ елементсеттинг** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **CIM \_ елементсеттинг** имеет следующие свойства.

<dl> <dt>

**Элемент**
</dt> <dd> <dl> <dt>

Тип данных: **CIM \_ манажедсистемелемент**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Ссылка на роль объекта [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md) ассоциации **\_ елементсеттинг CIM** . Связанный управляемый системный элемент предоставляет элемент, реализующий параметр элемента.

</dd> <dt>

**Параметр**
</dt> <dd> <dl> <dt>

Тип данных: **\_ параметр CIM**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Ссылка на роль объекта [**\_ параметров CIM**](cim-setting.md) ассоциации **\_ елементсеттинг CIM** . Связанный параметр предоставляет параметр, реализующий параметр элемента.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Инструментарий WMI не реализует этот класс. Классы, производные от **CIM \_ елементсеттинг**, см. в разделе [Классы Win32](win32-provider.md).

Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF. Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Пространство имен<br/>                | Корневой \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



 

 




