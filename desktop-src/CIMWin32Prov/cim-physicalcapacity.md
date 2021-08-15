---
description: Класс CIM \_ фисикалкапаЦити является абстрактным классом, который представляет минимальные и максимальные требования физического элемента и его способность поддерживать различные типы оборудования.
ms.assetid: e422aec0-1830-464e-ac52-2911652165a2
ms.tgt_platform: multiple
title: Класс CIM_PhysicalCapacity
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PhysicalCapacity
- CIM_PhysicalCapacity.Caption
- CIM_PhysicalCapacity.Description
- CIM_PhysicalCapacity.Name
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 78574fc7acc8e4b96be745d5eb2d00d2715d1ba3a570dd514be1ba0a3a706581
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118678366"
---
# <a name="cim_physicalcapacity-class"></a>\_Класс CIM фисикалкапаЦити

Класс **CIM \_ фисикалкапаЦити** является абстрактным классом, который представляет минимальные и максимальные требования физического элемента и его способность поддерживать различные типы оборудования. Например, минимальные и максимальные требования к памяти можно моделировать как подкласс **CIM \_ фисикалкапаЦити**.

> [!IMPORTANT]
> Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI. В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства. Свойства перечислены в алфавитном порядке, а не в MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
[Abstract, UUID("{FAF76B69-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PhysicalCapacity
{
  string Caption;
  string Description;
  string Name;
};
```

## <a name="members"></a>Члены

Класс **CIM \_ фисикалкапаЦити** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **CIM \_ фисикалкапаЦити** имеет следующие свойства.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Краткое текстовое описание объекта.

</dd> <dt>

**Описание**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Текстовое описание объекта.

</dd> <dt>

**Имя**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Метка, по которой известен объект. При создании подклассов это свойство может быть переопределено как свойство ключа.

</dd> </dl>

## <a name="remarks"></a>Remarks

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



 

