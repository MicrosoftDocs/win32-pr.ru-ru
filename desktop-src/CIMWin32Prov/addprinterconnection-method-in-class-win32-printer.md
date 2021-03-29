---
description: Обеспечивает подключение к существующему принтеру в сети и добавляет его в список доступных принтеров.
ms.assetid: 44149051-4abf-4428-8999-355dd0b0ce69
ms.tgt_platform: multiple
title: Метод Аддпринтерконнектион класса Win32_Printer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Printer.AddPrinterConnection
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: e2ad9e225a60e33fdf51d5f677dd4342acd148b3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895541"
---
# <a name="addprinterconnection-method-of-the-win32_printer-class"></a>Метод Аддпринтерконнектион \_ класса принтера Win32

Метод  [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) аддпринтерконнектион обеспечивает подключение к существующему принтеру в сети и добавляет его в список доступных принтеров.

В этом разделе используется синтаксис MOF-файл (MOF). Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Синтаксис


```mof
uint32 AddPrinterConnection(
  [in] string Name
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Имя* \[ окне\]
</dt> <dd>

Понятное имя принтера.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает одно из значений, перечисленных в следующем списке, или любое другое значение, указывающее на ошибку. Дополнительные коды ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**0**
</dt> <dd>

Успешно

</dd> <dt>

**5**
</dt> <dd>

доступ запрещен

</dd> <dt>

**1801**
</dt> <dd>

Недопустимое имя принтера

</dd> <dt>

**1930**
</dt> <dd>

Несовместимый драйвер принтера

</dd> </dl>

## <a name="examples"></a>Примеры

Образец PowerShell [Add-принтердривер](https://Gallery.TechNet.Microsoft.Com/1c8f4c0d-9439-4af0-8840-59686d9b4bc1) устанавливает все драйверы принтеров с указанного сервера печати.

В [ListSharedPrintersAddPrintConnection.ps1](https://Gallery.TechNet.Microsoft.Com/b7f74333-e78b-49d8-b23a-f1307d5b1ee6) примере PowerShell перечисляются общие принтеры на удаленном компьютере и предоставляется возможность добавить подключение принтера с удаленного компьютера на компьютер.

В следующем примере кода VBScript добавляется локальный принтер.


```VB
Dim strPrinterName as String = "Isidoros Printer"
Dim strComputer AsString = My.Computer.Name
Dim objWMIService, objPrinter AsObject
objWMIService = GetObject(
"winmgmts:" _

& 
"{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")

objPrinter = objWMIService.Get(
"Win32_Printer").SpawnInstance_
objPrinter.Name = strPrinterName
objPrinter.DriverName = "Generic / Text Only"
objPrinter.PortName = 
"c:\temp\file.prn"
objPrinter.DeviceID = strPrinterName
'objPrinter.Location = "Athens, Greece"
objPrinter.Network = 
False
objPrinter.Shared = 
False'objPrinter.ShareName = "MyShareName"
objPrinter.Put_()
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

[Задачи WMI: принтеры и печать](/windows/desktop/WmiSdk/wmi-tasks--printers-and-printing)
</dt> <dt>

[**\_Принтер Win32**](win32-printer.md)
</dt> </dl>

 

