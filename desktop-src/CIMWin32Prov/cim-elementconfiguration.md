---
description: Ассоциация CIM \_ елементконфигуратион связывает \_ объект конфигурации CIM с одним или несколькими управляемыми системными элементами. \_Объект конфигурации CIM представляет определенное поведение или требуемое функциональное состояние для связанного \_ манажедсистемелемент CIM.
ms.assetid: 4d2af009-7466-4394-af42-72c8d96e0786
ms.tgt_platform: multiple
title: Класс CIM_ElementConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ElementConfiguration
- CIM_ElementConfiguration.Configuration
- CIM_ElementConfiguration.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7707338a3c2268cba51146aa8462b3b244b149ac
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072468"
---
# <a name="cim_elementconfiguration-class"></a>\_Класс CIM елементконфигуратион

Ассоциация **CIM \_ елементконфигуратион** связывает объект [**\_ конфигурации CIM**](cim-configuration.md) с одним или несколькими управляемыми системными элементами. Объект **\_ конфигурации CIM** представляет определенное поведение или требуемое функциональное состояние для связанного [**\_ манажедсистемелемент CIM**](cim-managedsystemelement.md).

> [!IMPORTANT]
> Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI. В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства. Свойства перечислены в алфавитном порядке, а не в MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
[Abstract, UUID("{FC049DCE-DB29-11d2-85FC-0000F8102E5F}"), Association, AMENDMENT]
class CIM_ElementConfiguration
{
  CIM_Configuration        REF Configuration;
  CIM_ManagedSystemElement REF Element;
};
```

## <a name="members"></a>Члены

Класс **CIM \_ елементконфигуратион** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **CIM \_ елементконфигуратион** имеет следующие свойства.

<dl> <dt>

**Конфигурация**
</dt> <dd> <dl> <dt>

Тип данных: **\_ Конфигурация CIM**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Ссылка на объект [**\_ конфигурации CIM**](cim-configuration.md) , который группирует параметры и зависимости, связанные с управляемым элементом System.

</dd> <dt>

**Элемент**
</dt> <dd> <dl> <dt>

Тип данных: **CIM \_ манажедсистемелемент**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Ссылка на управляемый системный элемент.

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



 

 




