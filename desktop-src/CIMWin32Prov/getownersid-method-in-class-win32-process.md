---
description: Жетовнерсид&\# 8194; Метод класса WMI получает идентификатор безопасности (SID) для владельца этого процесса.
ms.assetid: f856b06c-8080-4145-a775-51361f741873
ms.tgt_platform: multiple
title: Метод Жетовнерсид класса Win32_Process
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Process.GetOwnerSid
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: c3ed34d132d363c0ce9f83511459ec40f340a06c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655790"
---
# <a name="getownersid-method-of-the-win32_process-class"></a>Метод Жетовнерсид \_ класса процесса Win32

Метод  [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) жетовнерсид ИЗВЛЕКАЕТ идентификатор безопасности (SID) для владельца этого процесса.

В этом разделе используется синтаксис MOF-файл (MOF). Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Синтаксис


```mof
uint32 GetOwnerSid(
  [out] string Sid
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Идентификатор безопасности* \[ заполняет\]
</dt> <dd>

Возвращает дескриптор идентификатора безопасности для этого процесса.

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

Пример кода PowerShell для [поиска пользователей, вошедших в систему на удаленном компьютере с версией 2](https://Gallery.TechNet.Microsoft.Com/Find-the-logged-on-users-1161bd92) , запрашивает удаленные компьютеры, чтобы узнать, кто вошел в систему.

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

 

