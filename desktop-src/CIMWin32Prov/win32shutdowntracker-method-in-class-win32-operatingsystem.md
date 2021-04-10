---
description: Метод Win32ShutdownTracker предоставляет тот же набор параметров завершения работы, что и метод Win32Shutdown в Win32 \_ операционной системы, но он также позволяет указать комментарии, причину завершения работы или время ожидания.
ms.assetid: 2c5502c9-9ec0-4f9e-b661-1f8015556008
ms.tgt_platform: multiple
title: Метод Win32ShutdownTracker класса Win32_OperatingSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_OperatingSystem.Win32ShutdownTracker
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 44c86972d014da906b98ad8d3bd8e98d01f1cfcb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141034"
---
# <a name="win32shutdowntracker-method-of-the-win32_operatingsystem-class"></a>Метод Win32ShutdownTracker \_ класса операционной системы Win32

Метод **Win32ShutdownTracker** предоставляет тот же набор параметров завершения работы, что и метод [**Win32Shutdown**](win32shutdown-method-in-class-win32-operatingsystem.md) в [**Win32 \_ операционной**](win32-operatingsystem.md)системы, но он также позволяет указать комментарии, причину завершения работы или время ожидания.

## <a name="syntax"></a>Синтаксис


```mof
uint32 Win32ShutdownTracker(
  [in] uint32 Timeout,
  [in] string Comment,
  [in] uint32 ReasonCode,
  [in] sint32 Flags
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Время ожидания* \[ окне\]
</dt> <dd>

Время в секундах до завершения работы. Значение по умолчанию — 0 (нуль).

</dd> <dt>

*Комментарий* \[ окне\]
</dt> <dd>

Сообщение, отображаемое в диалоговом окне завершения работы, которое также хранится в виде комментария в записи журнала событий.

</dd> <dt>

*Реасонкоде* \[ окне\]
</dt> <dd>

Причина начала завершения работы.

</dd> <dt>

*Флаги* \[ окне\]
</dt> <dd>

Набор флагов битовой панели для выключения компьютера. Чтобы принудительно выполнить команду, добавьте к значению команды флаг force (4). Использование Force в сочетании с завершением работы или перезагрузкой на удаленном компьютере немедленно завершает все (включая WMI, COM и т. д.) или перезагружает удаленный компьютер. Это приводит к неопределенному возвращаемому значению.

<dt>

0 (0x0)
</dt> <dd>

Выход из системы

</dd> <dt>

4 (0x4)
</dt> <dd>

Принудительный выход из системы (0 + 4)

</dd> <dt>

1 (0x1)
</dt> <dd>

Завершить работу

</dd> <dt>

5 (0x5)
</dt> <dd>

Принудительное завершение работы (1 + 4)

</dd> <dt>

2 (0x2)
</dt> <dd>

Перезагрузка

</dd> <dt>

6 (0x6)
</dt> <dd>

Принудительная перезагрузка (2 + 4)

</dd> <dt>

8 (0x8)
</dt> <dd>

Выключение питания

</dd> <dt>

12 (0xC)
</dt> <dd>

Принудительное выключение питания (8 + 4)

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает ноль (0), чтобы указать на успешное выполнение. Любое другое значение указывает на ошибку. Коды ошибок см. в разделе [**константы WMI Error**](../wmisdk/wmi-error-constants.md) или [**вбемерроренум**](/windows/win32/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Общие значения **HRESULT** см. в разделе [коды системных ошибок](../debug/system-error-codes.md).

<dl> <dt>

**Успешно** (0)
</dt> <dt>

**Другое** (1 – 4294967295)
</dt> </dl>

## <a name="remarks"></a>Комментарии

Вызывающий процесс должен иметь привилегию **SE \_ Shutdown \_ Name** .

## <a name="examples"></a>Примеры

В следующем примере кода VBScript описано, как вызвать **Win32ShutdownTracker**.


```VB
Set objArgs = Wscript.Arguments 

intTimeOut = objArgs(0) 'Countdown time (in seconds) before action
strComment = objArgs(1) 'Message to display
intFlags = objArgs(2) 'Set of flags to shutdown the computer:
'0 = Logoff, 4 = Forced Logoff (0+4), 1 = Shutdown, 2 = Reboot, 6 = Forced Reboot (2+4), 8 = Power Off, 12 = Forced Power Off (8+4) - 2 (Reboot) 

strComputer = "." 

Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate,(Shutdown)}!\\" & strComputer & "\root\cimv2")

Set colOperatingSystems = objWMIService.ExecQuery ("Select * from Win32_OperatingSystem") 

For Each objOperatingSystem in colOperatingSystems 
objOperatingSystem.Win32ShutdownTracker intTimeOut,strComment,0,intFlags 
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

[Классы операционной системы](./operating-system-classes.md)
</dt> <dt>

[**Win32, \_ Операционная система**](win32-operatingsystem.md)
</dt> <dt>

[**Win32Shutdown**](win32shutdown-method-in-class-win32-operatingsystem.md)
</dt> </dl>

 

 
