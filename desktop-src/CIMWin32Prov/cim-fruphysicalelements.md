---
description: Класс CIM \_ фруфисикалелементс представляет физические элементы, составляющие заменяемый элемент поля (FRU).
ms.assetid: ecdb19a8-5169-4370-8d2d-a21a0021ea5b
ms.tgt_platform: multiple
title: Класс CIM_FRUPhysicalElements
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_FRUPhysicalElements
- CIM_FRUPhysicalElements.Component
- CIM_FRUPhysicalElements.FRU
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 15a1f94771e7ccdcaaf132f4366b7b06824b14010d9cf8abf5914ea446f9ac8c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119080598"
---
# <a name="cim_fruphysicalelements-class"></a>\_Класс CIM фруфисикалелементс

Класс **CIM \_ фруфисикалелементс** представляет физические элементы, составляющие заменяемый элемент поля (FRU).

> [!IMPORTANT]
> Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI. В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства. Свойства перечислены в алфавитном порядке, а не в MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
[Abstract, UUID("{977E36CA-DB2A-11d2-85FC-0000F8102E5F}"), Aggregation, Association, AMENDMENT]
class CIM_FRUPhysicalElements
{
  CIM_PhysicalElement REF Component;
  CIM_FRU             REF FRU;
};
```

## <a name="members"></a>Члены

Класс **CIM \_ фруфисикалелементс** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **CIM \_ фруфисикалелементс** имеет следующие свойства.

<dl> <dt>

**Компонент**
</dt> <dd> <dl> <dt>

Тип данных: **CIM \_ фисикалелемент**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Ссылка на физический элемент, который является частью FRU.

</dd> <dt>

**ЭКСПЛУАТАЦИИ**
</dt> <dd> <dl> <dt>

Тип данных: **CIM \_ FRU**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Ссылка на FRU.

</dd> </dl>

## <a name="remarks"></a>Remarks

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



 

