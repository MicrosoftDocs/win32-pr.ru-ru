---
description: Удаление&\# 8194; Метод класса WMI удаляет запланированное задание.
ms.assetid: 064ff3f8-6d41-4f8d-a511-6c051bb48a5b
ms.tgt_platform: multiple
title: Метод Delete класса Win32_ScheduledJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ScheduledJob.Delete
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: dd375c3da85bd72bddfc97ed3f57e52103578441
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104142916"
---
# <a name="delete-method-of-the-win32_scheduledjob-class"></a>Метод DELETE \_ класса ScheduledJob Win32

Метод **удаления** [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) удаляет запланированное задание.

В этом разделе используется синтаксис MOF-файл (MOF). Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Синтаксис


```mof
uint32 Delete();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение 0 (нуль) при успешном выполнении и любое другое число для указания ошибки. Дополнительные коды ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Успешное завершение**
</dt> <dd>

0

Запрос принят.

</dd> <dt>

**Не поддерживается**
</dt> <dd>

1

Запрос не поддерживается.

</dd> <dt>

**Доступ запрещен**
</dt> <dd>

2

У пользователя нет необходимых прав доступа.

</dd> <dt>

**Неизвестный сбой**
</dt> <dd>

8

Интерактивный процесс.

</dd> <dt>

**Путь не найден**
</dt> <dd>

9

Не найден путь к каталогу исполняемого файла службы.

</dd> <dt>

**недопустимый параметр.**
</dt> <dd>

21

Службе переданы недопустимые параметры.

</dd> <dt>

**Служба не запущена**
</dt> <dd>

22

Учетная запись, под которой будет запускаться эта служба, недопустима или не имеет разрешений на запуск службы.

</dd> <dt>

**Другое**
</dt> <dd>

23 4294967295

</dd> </dl>

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

[**\_ScheduledJob Win32**](win32-scheduledjob.md)
</dt> </dl>

 

