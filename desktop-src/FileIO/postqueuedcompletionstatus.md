---
description: Отправляет пакет завершения ввода-вывода в порт завершения ввода-вывода.
ms.assetid: 69a9b1e5-2d40-42de-a14a-f7b6f29bf571
title: Функция PostQueuedCompletionStatus (Иоапи. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PostQueuedCompletionStatus
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-io-l1-1-0.dll
- KernelBase.dll
- MinKernelBase.dll
- API-MS-Win-Core-io-l1-1-1.dll
- api-ms-win-downlevel-kernel32-l1-1-0.dll
ms.openlocfilehash: f12de10032df7fec32dd9a577353dd20c0f4eaa5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664179"
---
# <a name="postqueuedcompletionstatus-function"></a>Функция PostQueuedCompletionStatus

Отправляет пакет завершения ввода-вывода в порт завершения ввода-вывода.

## <a name="syntax"></a>Синтаксис


```C++
BOOL WINAPI PostQueuedCompletionStatus(
  _In_     HANDLE       CompletionPort,
  _In_     DWORD        dwNumberOfBytesTransferred,
  _In_     ULONG_PTR    dwCompletionKey,
  _In_opt_ LPOVERLAPPED lpOverlapped
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Комплетионпорт* \[ окне\]
</dt> <dd>

Маркер порта завершения ввода-вывода, в который должен быть отправлен пакет завершения ввода-вывода.

</dd> <dt>

*двнумберофбитестрансферред* \[ окне\]
</dt> <dd>

Значение, возвращаемое с помощью параметра *лпнумберофбитестрансферред* функции [**жеткуеуедкомплетионстатус**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) .

</dd> <dt>

*двкомплетионкэй* \[ окне\]
</dt> <dd>

Значение, возвращаемое с помощью параметра *лпкомплетионкэй* функции [**жеткуеуедкомплетионстатус**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) .

</dd> <dt>

*лповерлаппед* \[ в необязательное\]
</dt> <dd>

Значение, возвращаемое с помощью параметра *лповерлаппед* функции [**жеткуеуедкомплетионстатус**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если функция выполняется успешно, возвращается ненулевое значение.

Если функция выполняется неудачно, возвращается нулевое значение. Чтобы получить расширенные сведения об ошибке, вызовите [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) .

## <a name="remarks"></a>Комментарии

Пакет завершения ввода-вывода будет отвечать за необработанный вызов функции [**жеткуеуедкомплетионстатус**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) . Эта функция возвращает с тремя значениями, передаваемыми в качестве второго, третьего и четвертого параметров вызова **PostQueuedCompletionStatus**. Система не использует или не проверяет эти значения. В частности, параметр *лповерлаппед* не должен указывать на структуру [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) .

В Windows 8 и Windows Server 2012 эта функция поддерживается следующими технологиями.



| Технология                                           | Поддерживается      |
|------------------------------------------------------|----------------|
| Протокол SMB 3,0<br/>   | Да<br/> |
| Прозрачная отработка отказа SMB 3,0 (ОТРАБОТКА отказа)<br/>        | Да<br/> |
| SMB 3,0 с масштабируемыми файловыми ресурсами (SO)<br/>   | Да<br/> |
| Общий том кластераная файловая система (CsvFS)<br/> | Да<br/> |
| Восстанавливаемая файловая система (ReFS)<br/>              | Да<br/> |



 

CsvFs выполнит перенаправление операций ввода-вывода для сжатых файлов.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Приложения UWP для классических приложений Windows XP \|\]<br/>                                                                                                                                                                                                                                                       |
| Минимальная версия сервера<br/> | \[Приложения UWP для классических приложений Windows Server 2003 \|\]<br/>                                                                                                                                                                                                                                              |
| Header<br/>                   | <dl> <dt>Иоапи. h (включение Windows. h); </dt> <dt>Винбасе. h в Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows server 2003 и Windows XP (включая Windows. h)</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>Kernel32.lib</dt> </dl>                                                                                                                                                                                                                  |
| DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl>                                                                                                                                                                                                                  |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**CreateIoCompletionPort**](createiocompletionport.md)
</dt> <dt>

[Функции управления файлами](file-management-functions.md)
</dt> <dt>

[**жеткуеуедкомплетионстатус**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus)
</dt> <dt>

[**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped)
</dt> </dl>

 

