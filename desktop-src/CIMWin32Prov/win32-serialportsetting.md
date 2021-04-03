---
description: '\_Класс WMI взаимосвязей Win32 сериалпортсеттинг связывает последовательный порт и его параметры конфигурации.'
ms.assetid: 57856207-abe5-4d93-9a34-acfe30ccd80c
ms.tgt_platform: multiple
title: Класс Win32_SerialPortSetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SerialPortSetting
- Win32_SerialPortSetting.Setting
- Win32_SerialPortSetting.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 713cdb57b5ed7135529959d3c17f7453924ce1dc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990386"
---
# <a name="win32_serialportsetting-class"></a>\_Класс Win32 сериалпортсеттинг

[Класс WMI](../wmisdk/retrieving-a-class.md) взаимосвязей **Win32 \_ сериалпортсеттинг** связывает последовательный порт и его параметры конфигурации.

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства. Свойства перечислены в алфавитном порядке, а не в MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4FE-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SerialPortSetting : Win32_DeviceSettings
{
  Win32_SerialPortConfiguration REF Setting;
  Win32_SerialPort              REF Element;
};
```

## <a name="members"></a>Члены

Класс **Win32 \_ сериалпортсеттинг** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **Win32 \_ сериалпортсеттинг** имеет следующие свойства.

<dl> <dt>

**Элемент**
</dt> <dd> <dl> <dt>

Тип данных: **Win32 \_ SerialPort**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](../wmisdk/standard-qualifiers.md) ("элемент"), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ SerialPort")
</dt> </dl>

[**Win32 \_ SerialPort**](win32-serialport.md) , содержащий свойства последовательного порта в компьютерной системе.

</dd> <dt>

**Параметр**
</dt> <dd> <dl> <dt>

Тип данных: **Win32 \_ сериалпортконфигуратион**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](../wmisdk/standard-qualifiers.md) ("параметр"), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ сериалпортконфигуратион")
</dt> </dl>

[**\_ Сериалпортконфигуратион Win32**](win32-serialportconfiguration.md) , который содержит параметр конфигурации для последовательного порта.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Класс **Win32 \_ сериалпортсеттинг** является производным от [**Win32 \_ девицесеттингс**](win32-devicesettings.md).

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

[**\_Девицесеттингс Win32**](win32-devicesettings.md)
</dt> <dt>

[Аппаратные классы системы компьютера](computer-system-hardware-classes.md)
</dt> </dl>

 

 
