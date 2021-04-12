---
description: Создает новый драйвер принтера.
ms.assetid: 23d9ec50-235a-4bf8-ab6b-be3509c3869f
ms.tgt_platform: multiple
title: Метод Аддпринтердривер класса Win32_PrinterDriver
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrinterDriver.AddPrinterDriver
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 03c029d7689743150235d20b0658cd154ef64a4c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423234"
---
# <a name="addprinterdriver-method-of-the-win32_printerdriver-class"></a>Метод Аддпринтердривер \_ класса Win32 принтердривер

Метод класса **аддпринтердривер** создает новый драйвер принтера.

В этом разделе используется синтаксис MOF-файл (MOF). Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Синтаксис


```mof
uint32 AddPrinterDriver(
  [in] Win32_PrinterDriver DriverInfo
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Дриверинфо* \[ окне\]
</dt> <dd>

Экземпляр класса [**Win32 \_ принтердривер**](win32-printerdriver.md) , представляющий драйвер принтера.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает одно из значений, перечисленных в следующем списке, или любое другое значение, указывающее на ошибку. Для значений, отличающихся от перечисленных в следующем списке, см. раздел [**константы ошибки WMI**](/windows/desktop/WmiSdk/wmi-error-constants).

<dl> <dt>

**0**
</dt> <dd>

Успешно.

</dd> <dt>

**5**
</dt> <dd>

Доступ запрещен.

</dd> <dt>

**87**
</dt> <dd>

Неправильный параметр". Может возникнуть, когда объект неверно заполнен или не удается найти драйвер в системе. Кроме того, атрибут Name может отличаться от модели, указанной в INF-файле. Или в атрибуте Пасфиле может отсутствовать обратная косая черта (" \\ ").

</dd> <dt>

**1797**
</dt> <dd>

Неизвестный драйвер принтера.

</dd> </dl>

## <a name="remarks"></a>Комментарии

> [!Note]  
> При использовании метода **аддпринтердривер** необходимо использовать **селоаддриверпривилеже** для загрузки или выгрузки драйвера устройства.

 

## <a name="examples"></a>Примеры

[Установка драйвера принтера, не найденного в файле Drivers CAB](https://Gallery.TechNet.Microsoft.Com/1aac6333-a794-48d3-b7da-46d87df56ee1) , пример кода VBScript устанавливает гипотетический принтер с помощью драйвера печати, не найденного в Drivers.cab.

Следующий пример сценария VBScript устанавливает драйвер принтера для принтера Apple LaserWriter 8500.


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
objWMIService.Security_.Privileges.AddAsString "SeLoadDriverPrivilege", True 
 
Set objDriver = objWMIService.Get("Win32_PrinterDriver") 
 
objDriver.Name = "NewPrinter Model 2900" 
objDriver.SupportedPlatform = "Windows NT x86" 
objDriver.Version = "3" 
objDriver.DriverPath = "C:\Scripts\NewPrinter.dll" 
objDriver.Infname = "C:\Scripts\NewPrinter.inf" 
intResult = objDriver.AddPrinterDriver(objDriver) 
```



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
</dt> <dt>

[**\_Принтердривер Win32**](win32-printerdriver.md)
</dt> </dl>

 

