---
description: '\_Класс WMI взаимосвязей Win32 принтершаре связывает локальный принтер и общую папку, которая представляет его по мере просмотра по сети.'
ms.assetid: 9ac99e52-5e8f-4329-960f-7bd1fd229e37
ms.tgt_platform: multiple
title: Класс Win32_PrinterShare
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrinterShare
- Win32_PrinterShare.Antecedent
- Win32_PrinterShare.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 57bc15fc5d3db78179335b039851d7d3b7cbf8a4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896265"
---
# <a name="win32_printershare-class"></a>\_Класс Win32 принтершаре

[Класс WMI](../wmisdk/retrieving-a-class.md) взаимосвязей **Win32 \_ принтершаре** связывает локальный принтер и общую папку, которая представляет его по мере просмотра по сети.

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства. Свойства и методы имеют алфавитный порядок, а не порядок MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
class Win32_PrinterShare : CIM_Dependency
{
  Win32_Printer REF Antecedent;
  Win32_Share   REF Dependent;
};
```

## <a name="members"></a>Члены

Класс **Win32 \_ принтершаре** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **Win32 \_ принтершаре** имеет следующие свойства.

<dl> <dt>

**Завершил**
</dt> <dd> <dl> <dt>

Тип данных: **\_ принтер Win32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **ключ**](../wmisdk/standard-qualifiers.md)
</dt> </dl>

Ссылка на экземпляр, представляющий локальный принтер, совместно используемый в этой ассоциации.

</dd> <dt>

**Него**
</dt> <dd> <dl> <dt>

Тип данных: **\_ общий ресурс Win32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **ключ**](../wmisdk/standard-qualifiers.md)
</dt> </dl>

Ссылка на экземпляр, представляющий общую папку принтера в этой ассоциации.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Класс **Win32 \_ принтершаре** является производным от [**\_ зависимости CIM**](cim-dependency.md).

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

[Классы операционной системы](./operating-system-classes.md)
</dt> </dl>

 

 
