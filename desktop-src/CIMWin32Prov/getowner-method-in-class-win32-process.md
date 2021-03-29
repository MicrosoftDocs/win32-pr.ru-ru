---
description: '&\# 8194; Метод класса WMI извлекает имя пользователя и доменное имя, под которым выполняется процесс.'
ms.assetid: bbd6d22b-ca54-42f3-8098-d3034048ec4d
ms.tgt_platform: multiple
title: Метод, являющийся владельцем класса Win32_Process
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Process.GetOwner
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 007acbe997f555e9a439ed27740a447d3bf7fe4d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141307"
---
# <a name="getowner-method-of-the-win32_process-class"></a>Метод, являющийся владельцем \_ класса процесса Win32

Метод  [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) -владельца получает имя пользователя и доменное имя, под которым выполняется процесс.

В этом разделе используется синтаксис MOF-файл (MOF). Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Синтаксис


```mof
uint32 GetOwner(
  [out] string User,
  [out] string Domain
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Пользователь* \[ заполняет\]
</dt> <dd>

Возвращает имя пользователя, владеющего этим процессом.

</dd> <dt>

*Домен* \[ заполняет\]
</dt> <dd>

Возвращает имя домена, в котором выполняется этот процесс.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает ноль (0), чтобы указать на успешное выполнение. Любое другое значение указывает на ошибку. Дополнительные коды ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Успешное завершение** (0)
</dt> <dt>

**Отказано в доступе** (2)
</dt> <dt>

**Недостаточно прав доступа** (3)
</dt> <dt>

**Неизвестный сбой** (8)
</dt> <dt>

**Путь не найден** (9)
</dt> <dt>

**Недопустимый параметр** (21)
</dt> <dt>

**Другие** (22 4294967295)
</dt> </dl>

## <a name="examples"></a>Примеры

[Процесс мониторинга PCT по имени с владельцем](https://Gallery.TechNet.Microsoft.Com/Monitor-Process-CPU-Pct-by-0f3a5a1c) Пример на языке VBScript собирает данные об использовании ЦП или процессора и выполняет поиск владельца процесса.

На странице [Получение всех серверов, в которые входит список пользователей,](https://Gallery.TechNet.Microsoft.Com/Get-all-servers-that-a-aecc07ef) в пример запросов PowerShell для владельца всех explorer.exe процессов.

Следующий пример кода VBScript получает сведения о владельце для каждого выполняющегося процесса.


```VB
strComputer = "."
Set colProcesses = GetObject("winmgmts:" & _
   "{impersonationLevel=impersonate}!\\" & strComputer & _
   "\root\cimv2").ExecQuery("Select * from Win32_Process")

For Each objProcess in colProcesses

    Return = objProcess.GetOwner(strNameOfUser)
    If Return <> 0 Then
        Wscript.Echo "Could not get owner info for process " & _  
            objProcess.Name & VBNewLine _
            & "Error = " & Return
    Else 
        Wscript.Echo "Process " _
            & objProcess.Name & " is owned by " _ 
            & "\" & strNameOfUser & "."
    End If
Next
```



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

[Классы операционной системы](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**\_Процесс Win32**](win32-process.md)
</dt> </dl>

 

