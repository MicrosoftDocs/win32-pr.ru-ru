---
description: Класс CIM \_ ассоЦиатедпроцессормемори связывает процессор и системную память или кэш процессора.
ms.assetid: a4c28a0a-e4cc-4db2-bd77-b7b5023eace6
ms.tgt_platform: multiple
title: Класс CIM_AssociatedProcessorMemory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AssociatedProcessorMemory
- CIM_AssociatedProcessorMemory.Antecedent
- CIM_AssociatedProcessorMemory.Dependent
- CIM_AssociatedProcessorMemory.BusSpeed
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: f35cdca92cb15e1c6fff215ff1363844e0d47012
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990670"
---
# <a name="cim_associatedprocessormemory-class"></a>\_Класс CIM ассоЦиатедпроцессормемори

Класс **CIM \_ ассоЦиатедпроцессормемори** связывает процессор и системную память или кэш процессора.

> [!IMPORTANT]
> Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI. В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства. Свойства перечислены в алфавитном порядке, а не в MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
[abstract, UUID("{464FFAB1-946F-11d2-AAE2-006008C78BC7}"), AMENDMENT]
class CIM_AssociatedProcessorMemory : CIM_AssociatedMemory
{
  CIM_Memory    REF Antecedent;
  CIM_Processor REF Dependent;
  uint32            BusSpeed;
};
```

## <a name="members"></a>Члены

Класс **CIM \_ ассоЦиатедпроцессормемори** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **CIM \_ ассоЦиатедпроцессормемори** имеет следующие свойства.

<dl> <dt>

**Завершил**
</dt> <dd> <dl> <dt>

Тип данных: **\_ память CIM**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

[**\_ Память CIM**](cim-memory.md) , описывающая память, установленную на устройстве или связанной с ней.

Это свойство наследуется от [**CIM \_ ассоЦиатедмемори**](cim-associatedmemory.md).

</dd> <dt>

**бусспид**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**единицы измерения**](/windows/desktop/WmiSdk/standard-qualifiers) ("мегагерц")
</dt> </dl>

Скорость шины в мегагерцах (МГц) между процессором и памятью.

</dd> <dt>

**Него**
</dt> <dd> <dl> <dt>

Тип данных: **\_ процессор CIM**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")
</dt> </dl>

[**\_ Процессор CIM**](cim-processor.md) , описывающий процессор, обращающийся к памяти или использующий кэш.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Класс **CIM \_ ассоЦиатедпроцессормемори** является производным от [**CIM \_ ассоЦиатедмемори**](cim-associatedmemory.md).

Инструментарий WMI не реализует этот класс. Дополнительные сведения о классах, производных от **CIM \_ ассоЦиатедпроцессормемори**, см. в разделе [Классы Win32](win32-provider.md).

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

[**\_АССОЦИАТЕДМЕМОРИ CIM**](cim-associatedmemory.md)
</dt> </dl>

 

