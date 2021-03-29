---
description: '\_Прикрепленная Ассоциация CIM представляет связь между двумя корпусами. Например, портативный компьютер (тип корпуса) можно закрепить на стыковочный станции (другой тип корпуса). Эта типичная связь описана явно.'
ms.assetid: 72cb36bb-f79e-4d1a-a859-4024031e4ebc
ms.tgt_platform: multiple
title: Класс CIM_Docked
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Docked
- CIM_Docked.Dependent
- CIM_Docked.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 899b85d63293861f0a36df3d3c30610f8cff05ac
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807517"
---
# <a name="cim_docked-class"></a>\_Закрепленный класс CIM

**\_ Прикрепленная Ассоциация CIM** представляет связь между двумя корпусами. Например, портативный компьютер (тип корпуса) можно закрепить на стыковочный станции (другой тип корпуса). Эта типичная связь описана явно.

> [!IMPORTANT]
> Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI. В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Abstract, MappingStrings("MIF.DMTF|Dynamic States|001.2"), UUID("{FAF76B75-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_Docked : CIM_Dependency
{
  CIM_Chassis REF Dependent;
  CIM_Chassis REF Antecedent;
};
```

## <a name="members"></a>Члены

**\_ Закрепленный класс CIM** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

**\_ Прикрепленный класс CIM** имеет эти свойства.

<dl> <dt>

**Завершил**
</dt> <dd> <dl> <dt>

Тип данных: **CIM \_ Chassis**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

[**\_ Корпус CIM**](cim-chassis.md) , описывающий станцию стыковки.

</dd> <dt>

**Него**
</dt> <dd> <dl> <dt>

Тип данных: **CIM \_ Chassis**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

[**\_ Корпус CIM**](cim-chassis.md) , описывающий закрепленный портативный компьютер.

</dd> </dl>

## <a name="remarks"></a>Комментарии

**\_ Закрепленный класс CIM** является производным от [**\_ зависимости CIM**](cim-dependency.md).

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



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Зависимость CIM**](cim-dependency.md)
</dt> </dl>

 

