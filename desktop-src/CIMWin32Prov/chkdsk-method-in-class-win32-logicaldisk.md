---
description: Вызывает операцию chkdsk на диске.
ms.assetid: 65942702-b660-46cd-b614-e3e1ec3df7b9
ms.tgt_platform: multiple
title: Метод chkdsk класса Win32_LogicalDisk
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogicalDisk.Chkdsk
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 662fc8739f90eea15295b762edc446ac16677aef
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104142112"
---
# <a name="chkdsk-method-of-the-win32_logicaldisk-class"></a>Метод chkdsk \_ класса LogicalDisk Win32

Метод экземпляра **chkdsk** вызывает операцию **chkdsk** на диске.

В этом разделе используется синтаксис MOF-файл (MOF). Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Синтаксис


```mof
uint32 Chkdsk(
  [in] boolean FixErrors = ,
  [in] boolean VigorousIndexCheck = ,
  [in] boolean SkipFolderCycle = ,
  [in] boolean ForceDismount = ,
  [in] boolean RecoverBadSectors = ,
  [in] boolean OKToRunAtBootUp = 
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Фиксеррорс* \[ окне\]
</dt> <dd>

Указывает, что следует сделать с ошибками, обнаруженными на диске. Если **значение равно true**, ошибки исправлены. Значение по умолчанию — **false**.

</dd> <dt>

*Вигораусиндексчекк* \[ окне\]
</dt> <dd>

Если **значение — true**, необходимо выполнить менее тщательные проверку записей индекса. Значение по умолчанию — **false**.

</dd> <dt>

*Скипфолдерцикле* \[ окне\]
</dt> <dd>

Если **значение равно true**, проверка цикла папок должна быть пропущена. Значение по умолчанию — **true**.

</dd> <dt>

*Форцедисмаунт* \[ окне\]
</dt> <dd>

Если **значение — true**, перед проверкой диск должен быть принудительно отключен. Значение по умолчанию — **false**.

</dd> <dt>

*Рековербадсекторс* \[ окне\]
</dt> <dd>

Если **значение равно true**, то должны быть найдены поврежденные секторы и данные для чтения должны быть восстановлены из этих секторов. Значение по умолчанию — **false**.

</dd> <dt>

*Окторунатбутуп* \[ окне\]
</dt> <dd>

Если **значение — true**, операция **chkdsk** должна выполняться при следующей загрузке, если операция не может быть выполнена, так как диск заблокирован во время вызова этого метода. Значение по умолчанию — **false**.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

При успешном выполнении возвращает значение 0 (нуль). Другие значения перечислены в следующем списке. Дополнительные коды ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Успешно — Chkdsk завершена**
</dt> <dd>

0

Успешно — [**chkdsk**](chkdsk-method-in-class-win32-logicaldisk.md) завершена

</dd> <dt>

**Успешно — заблокировано и chkdsk запланировано при перезагрузке**
</dt> <dd>

1

</dd> <dt>

**Сбой — неизвестная файловая система**
</dt> <dd>

2

</dd> <dt>

**Сбой-неизвестная ошибка**
</dt> <dd>

3

</dd> <dt>

**Сбой-неподдерживаемая файловая система**
</dt> <dd>

4

</dd> </dl>

## <a name="remarks"></a>Комментарии

Этот метод применим только к тем экземплярам логического диска, которые представляют физический диск на компьютере. Он неприменим к сопоставленным логическим дискам.

## <a name="examples"></a>Примеры

В образце кода PowerShell[для сервера выполняется](https://Gallery.TechNet.Microsoft.Com/57076851-97fb-4af6-8c5c-1e34156ceab4) проверка удаленной системы и возвращается значение true или false, если установлен флаг chkdsk/f.

Пример кода PowerShell для [удаленной проверки](https://Gallery.TechNet.Microsoft.Com/Remotely-scan-disk-dd4fc267) запускается удаленно или планирует проверку диска.

Следующий пример кода VBScript выполняется ChkDsk.exe на диске D на компьютере.


```VB
Const FIX_ERRORS = True 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set objDisk = objWMIService.Get("Win32_LogicalDisk.DeviceID='D:'") 
 
errReturn = objDisk.ChkDsk(FIX_ERRORS) 
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

[**Win32 \_ LogicalDisk**](win32-logicaldisk.md)
</dt> <dt>

[Аппаратные классы системы компьютера](computer-system-hardware-classes.md)
</dt> </dl>

 

