---
description: '\_Класс замены CIM объединяет физические элементы, которые должны быть заменены вместе.'
ms.assetid: db55ae2d-49b3-4cc9-95ee-1e757f58a427
ms.tgt_platform: multiple
title: Класс CIM_ReplacementSet
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ReplacementSet
- CIM_ReplacementSet.Description
- CIM_ReplacementSet.Name
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: defc63628e494465d7a31d8adcea758e538c4c9e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141071"
---
# <a name="cim_replacementset-class"></a>\_Класс замены CIM

Класс **\_ замены CIM** объединяет физические элементы, которые должны быть заменены вместе. Например, при замене платы памяти микросхемы памяти компонента также могут быть удалены и заменены. Или можно использовать эту связь для замены или обновления набора микросхем памяти.

> [!IMPORTANT]
> Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI. В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства. Свойства перечислены в алфавитном порядке, а не в MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
[Abstract, UUID("{FAF76B6C-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_ReplacementSet
{
  string Description;
  string Name;
};
```

## <a name="members"></a>Члены

Класс **\_ замены CIM** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **\_ замены CIM** имеет эти свойства.

<dl> <dt>

**Описание**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Произвольная строка, указывающая сведения, связанные с этим классом. Назначение набора или сведения, связанные с заменой элементов компонента, можно добавить в это свойство.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Произвольная строка, которая определяет метку для этого свойства. Это свойство является ключом объекта.

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



 

