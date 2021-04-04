---
description: Метод класса Pause WMI приостанавливает задание печати.
ms.assetid: f1e3906f-1ca2-45c0-9863-5762e4e2119a
ms.tgt_platform: multiple
title: Метод Pause класса Win32_PrintJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrintJob.Pause
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 785ba54b56c65fd298b6ef763ec2d7eca0d8f61a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896517"
---
# <a name="pause-method-of-the-win32_printjob-class"></a>Приостановка метода класса Win32 \_ PrintJob

Метод класса **Pause** [WMI](/windows/desktop/WmiSdk/retrieving-a-class) приостанавливает задание печати.

В этом разделе используется синтаксис MOF-файл (MOF). Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Синтаксис


```mof
uint32 Pause();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает одно из значений, перечисленных в следующем списке, или любое другое значение, указывающее на ошибку.

<dl> <dt>

**0**
</dt> <dd>

Успешно

</dd> <dt>

**5**
</dt> <dd>

доступ запрещен

</dd> </dl>

## <a name="examples"></a>Примеры

Пример кода " [приостановить все принтеры с пустыми очередями печати](https://Gallery.TechNet.Microsoft.Com/cf2b6b61-8ffe-444b-857b-e3a205bc693c) " приостанавливает работу всех принтеров, для которых нет ожидающих заданий печати.

Следующий пример кода VBScript приостанавливает все задания печати на сервере печати.


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colPrintJobs =  objWMIService.ExecQuery _ 
    ("Select * from Win32_PrintJob") 
 
For Each objPrintJob in colPrintJobs  
    objPrintJob.Pause 
Next 
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

[**Win32 \_ PrintJob**](win32-printjob.md)
</dt> </dl>

 

