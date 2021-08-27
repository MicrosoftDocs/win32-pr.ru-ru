---
description: Удаляет все задания, включая текущую печать из очереди.
ms.assetid: d7466513-b123-43af-ab17-b3213ba80284
ms.tgt_platform: multiple
title: Метод Канцелаллжобс класса Win32_Printer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Printer.CancelAllJobs
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 06aae96cec4e38c7ff9c213cd19dc35e9843a077c262aafcaf0aed43160505a9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120085844"
---
# <a name="cancelalljobs-method-of-the-win32_printer-class"></a>Метод Канцелаллжобс \_ класса принтера Win32

Метод  [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) канцелаллжобс удаляет все задания, включая текущую печать из очереди.

В этом разделе используется синтаксис MOF-файл (MOF). Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Синтаксис


```mof
uint32 CancelAllJobs();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

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

</dd> </dl>

## <a name="examples"></a>Примеры

[Уведомление пользователей об очистке очереди печати](https://Gallery.TechNet.Microsoft.Com/9f8ad84e-239d-45bf-a14f-ad8f3fc4988a) использует Msg.exe для отправки сетевого оповещения всем пользователям, имеющим документы в очереди печати, для очистки. После отправки предупреждений сценарий удаляет очередь печати.

Пример кода VBScript " [удалить все задания печати](https://Gallery.TechNet.Microsoft.Com/0e89fa7c-a837-4607-b421-c870142e7323) " удаляет все задания печати на локальном компьютере.

Следующий пример сценария VBScript удаляет все задания печати для принтера с именем HP Куиетжет.


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colInstalledPrinters =  objWMIService.ExecQuery _ 
    ("Select * from Win32_Printer Where Name = 'HP QuietJet'") 
 
For Each objPrinter in colInstalledPrinters 
    objPrinter.CancelAllJobs() 
Next 
```



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                      |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                                |
| Пространство имен<br/>                | Корневой \\ CIMV2<br/>                                                                        |
| MOF<br/>                      | <dl> <dt>Win32 \_ Printer. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl>       |



## <a name="see-also"></a>См. также

<dl> <dt>

[Аппаратные классы системы компьютера](computer-system-hardware-classes.md)
</dt> <dt>

[**\_Принтер Win32**](win32-printer.md)
</dt> </dl>

 

