---
description: Отношение CIM \_ депенденциконтекст связывает \_ класс зависимостей CIM с одним или несколькими \_ объектами конфигурации CIM. Например, зависимости компьютера могут изменяться в зависимости от сети, к которой подключена система.
ms.assetid: 9f35fc41-1bfa-4018-a54c-64c875c710d4
ms.tgt_platform: multiple
title: Класс CIM_DependencyContext
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DependencyContext
- CIM_DependencyContext.Context
- CIM_DependencyContext.Dependency
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 845086b7d41eb03227d6b5b47240ef4bf9e1a2c35f8049c96d5c665800b327e6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119924644"
---
# <a name="cim_dependencycontext-class"></a>\_Класс CIM депенденциконтекст

Отношение **CIM \_ депенденциконтекст** связывает класс [**\_ зависимостей CIM**](cim-dependency.md) с одним или несколькими объектами [**\_ конфигурации CIM**](cim-configuration.md) . Например, зависимости компьютера могут изменяться в зависимости от сети, к которой подключена система.

> [!IMPORTANT]
> Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI. В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства. Свойства перечислены в алфавитном порядке, а не в MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
[Abstract, Aggregation, Association, UUID("{A228E208-DB22-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_DependencyContext
{
  CIM_Configuration REF Context;
  CIM_Dependency    REF Dependency;
};
```

## <a name="members"></a>Члены

Класс **CIM \_ депенденциконтекст** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **CIM \_ депенденциконтекст** имеет следующие свойства.

<dl> <dt>

**Контекст**
</dt> <dd> <dl> <dt>

Тип данных: **\_ Конфигурация CIM**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Ссылка на объект конфигурации, который выполняет статистическую обработку зависимости.

</dd> <dt>

**Зависимость**
</dt> <dd> <dl> <dt>

Тип данных: **\_ зависимость CIM**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Ссылка на агрегированную зависимость.

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



 

