---
description: '\_Класс WMI взаимосвязей Win32 дриверфордевице связывает экземпляр принтера с экземпляром драйвера принтера.'
ms.assetid: 56ff74b2-31ba-4d8e-b389-9f962932aa03
ms.tgt_platform: multiple
title: Класс Win32_DriverForDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DriverForDevice
- Win32_DriverForDevice.Antecedent
- Win32_DriverForDevice.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: f55025c84b8ab7e7114f5a1746d84f8fbdb6b0a7dfe952abfe84efb980430881
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119546324"
---
# <a name="win32_driverfordevice-class"></a>\_Класс Win32 дриверфордевице

[Класс WMI](/windows/desktop/WmiSdk/retrieving-a-class) взаимосвязей **Win32 \_ дриверфордевице** связывает экземпляр принтера с экземпляром драйвера принтера.

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства. Свойства перечислены в алфавитном порядке, а не в MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
class Win32_DriverForDevice : CIM_Dependency
{
  Win32_Printer       REF Antecedent;
  Win32_PrinterDriver REF Dependent;
};
```

## <a name="members"></a>Члены

Класс **Win32 \_ дриверфордевице** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **Win32 \_ дриверфордевице** имеет следующие свойства.

<dl> <dt>

**Завершил**
</dt> <dd> <dl> <dt>

Тип данных: **\_ принтер Win32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Ссылка на экземпляр [**\_ принтера Win32**](win32-printer.md) , представляющий принтер.

Это свойство наследуется [**от \_ зависимости CIM**](cim-dependency.md).

</dd> <dt>

**Него**
</dt> <dd> <dl> <dt>

Тип данных: **Win32 \_ принтердривер**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Ссылка на экземпляр [**Win32 \_ принтердривер**](win32-printerdriver.md) , представляющий драйвер принтера для принтера.

Это свойство наследуется [**от \_ зависимости CIM**](cim-dependency.md).

</dd> </dl>

## <a name="remarks"></a>Remarks

Класс **Win32 \_ дриверфордевице** является производным от [**\_ зависимости CIM**](cim-dependency.md).

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

[Аппаратные классы системы компьютера](computer-system-hardware-classes.md)
</dt> </dl>

 

