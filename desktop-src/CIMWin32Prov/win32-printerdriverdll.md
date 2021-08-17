---
description: '\_Класс WMI взаимосвязей Win32 принтердривердлл связывает локальный принтер и его файл драйвера.'
ms.assetid: decbd1de-8091-47f7-94a1-42862070b920
ms.tgt_platform: multiple
title: Класс Win32_PrinterDriverDll
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrinterDriverDll
- Win32_PrinterDriverDll.Antecedent
- Win32_PrinterDriverDll.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 884c52e388da62529a2aceb49c68ca888f18e0fd7701e05d951880774c3ed035
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119971864"
---
# <a name="win32_printerdriverdll-class"></a>\_Класс Win32 принтердривердлл

[Класс WMI](../wmisdk/retrieving-a-class.md) взаимосвязей **Win32 \_ принтердривердлл** связывает локальный принтер и его файл драйвера.

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства. Свойства перечислены в алфавитном порядке, а не в MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
class Win32_PrinterDriverDll : CIM_Dependency
{
  CIM_DataFile  REF Antecedent;
  Win32_Printer REF Dependent;
};
```

## <a name="members"></a>Члены

Класс **Win32 \_ принтердривердлл** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **Win32 \_ принтердривердлл** имеет следующие свойства.

<dl> <dt>

**Завершил**
</dt> <dd> <dl> <dt>

Тип данных: **CIM \_ File**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **ключ**](../wmisdk/standard-qualifiers.md)
</dt> </dl>

ссылка на экземпляр [**\_ файла данных CIM**](cim-datafile.md) , представляющий файл драйвера для данного принтера на основе Windows.

Это свойство наследуется [**от \_ зависимости CIM**](cim-dependency.md).

</dd> <dt>

**Него**
</dt> <dd> <dl> <dt>

Тип данных: **\_ принтер Win32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **ключ**](../wmisdk/standard-qualifiers.md)
</dt> </dl>

Ссылка на экземпляр [**\_ принтера Win32**](win32-printer.md) .

Это свойство наследуется [**от \_ зависимости CIM**](cim-dependency.md).

</dd> </dl>

## <a name="remarks"></a>Remarks

Класс **Win32 \_ принтердривердлл** является производным от [**\_ зависимости CIM**](cim-dependency.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                      |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                                |
| Пространство имен<br/>                | Корневой \\ CIMV2<br/>                                                                        |
| MOF<br/>                      | <dl> <dt>Win32 \_ Printer. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl>       |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Зависимость CIM**](cim-dependency.md)
</dt> <dt>

[Аппаратные классы системы компьютера](computer-system-hardware-classes.md)
</dt> </dl>

 

 
