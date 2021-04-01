---
description: '\_ \_ \_ \_ Управляющий код ключа возобновления фсктл SRV-запроса используется для получения ссылки на непрозрачный файл для использования с \_ управляющим кодом ioctl COPYCHUNK.'
ms.assetid: a6e0d253-5beb-4de8-8c40-d004f5794d47
title: Код элемента управления FSCTL_SRV_REQUEST_RESUME_KEY
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FSCTL_SRV_REQUEST_RESUME_KEY
api_type:
- NA
api_location: ''
ms.openlocfilehash: 8f11b70f7b4bfd05cbd5f7c29323f1dca00083a4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895429"
---
# <a name="fsctl_srv_request_resume_key-control-code"></a>\_ \_ \_ \_ Код управления ключами возобновления ключа для запроса SRV фсктл

Управляющий код **\_ \_ \_ \_ ключа возобновления фсктл SRV-запроса** используется для получения ссылки на непрозрачный файл для использования с управляющим кодом [**ioctl \_ COPYCHUNK**](ioctl-copychunk.md) .

Чтобы выполнить эту операцию, вызовите функцию [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) со следующими параметрами.


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,             // handle to device
  FSCTL_SRV_REQUEST_RESUME_KEY, // dwIoControlCode
  NULL,                         // lpInBuffer
  0,                            // nInBufferSize
  (LPVOID) lpOutBuffer,         // output buffer
  (DWORD) nOutBufferSize,       // size of output buffer
  (LPDWORD) lpBytesReturned,    // number of bytes returned
  (LPOVERLAPPED) lpOverlapped   // OVERLAPPED structure
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хдевице* \[ окне\]
</dt> <dd>

Описатель файла, для которого запрашивается ключ исходного файла. Чтобы получить этот маркер, вызовите функцию [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) .

</dd> <dt>

*двиоконтролкоде* \[ окне\]
</dt> <dd>

Управляющий код для операции. Используйте **\_ \_ \_ \_ ключ возобновления запроса SRV фсктл** для этой операции.

</dd> <dt>

*лпинбуффер* 
</dt> <dd>

Не используется в этой операции; Задайте **значение NULL**.

</dd> <dt>

*нинбуфферсизе* \[ окне\]
</dt> <dd>

Не используется в этой операции; присвойте ему значение 0.

</dd> <dt>

*лпаутбуффер* \[ заполняет\]
</dt> <dd>

Указатель на выходной буфер, структура **\_ \_ \_ ключа возобновления SRV-запроса** . Дополнительные сведения см. в разделе "Замечания".

</dd> <dt>

*наутбуфферсизе* \[ окне\]
</dt> <dd>

Размер выходного буфера в байтах.

</dd> <dt>

*лпбитесретурнед* \[ заполняет\]
</dt> <dd>

Указатель на переменную, которая получает размер данных, хранящихся в буфере вывода, в байтах.

Если выходной буфер слишком мал, вызов завершается ошибкой, функция [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) возвращает **ошибку \_ недостаточно \_ буфера**, а *лпбитесретурнед* равно нулю.

Если параметр *лповерлаппед* имеет **значение NULL**, *Лпбитесретурнед* не может иметь **значение NULL**. Даже если операция не возвращает выходные данные и параметр *лпаутбуффер* имеет **значение NULL**, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) использует *лпбитесретурнед*. После такой операции значение *лпбитесретурнед* не имеет смысла.

Если *лповерлаппед* не **равно NULL**, *лпбитесретурнед* может иметь **значение NULL**. Если *лповерлаппед* не равно **null** и операция возвращает данные, *лпбитесретурнед* не имеет смысла до тех пор, пока не завершится операция перекрытия. Чтобы получить число возвращаемых байтов, вызовите функцию [**GetOverlappedResult**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult) . Если параметр *хдевице* связан с портом завершения ввода-вывода, можно получить число байтов, возвращенных путем вызова функции [**жеткуеуедкомплетионстатус**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) .

</dd> <dt>

*лповерлаппед* \[ окне\]
</dt> <dd>

Указатель на структуру [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) .

Если параметр *хдевице* был открыт без указания **\_ флага файла \_ OVERLAPPED**, *лповерлаппед* игнорируется.

Если *хдевице* был открыт с флагом **File \_ Flag \_ OVERLAPPED** , операция выполняется как Перекрываемая (асинхронная) операция. В этом случае *лповерлаппед* должен указывать на допустимую структуру [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) , которая содержит указатель на объект события. В противном случае функция завершается ошибкой непредсказуемым образом.

Для операций с перекрытием [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) возвращает значение немедленно, а объект события получает сигнал о завершении операции. В противном случае функция не возвращает значение до завершения операции или до возникновения ошибки.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если операция завершается успешно, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) возвращает ненулевое значение.

Если операция завершается неудачно или ожидает выполнения, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) возвращает ноль. Дополнительные сведения об ошибке можно получить, вызвав [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Комментарии

Этот управляющий код не имеет связанного файла заголовка. Необходимо определить управляющий код и структуры данных следующим образом.

``` syntax
#define FSCTL_SRV_REQUEST_RESUME_KEY CTL_CODE(FILE_DEVICE_NETWORK_FILE_SYSTEM, 30, METHOD_BUFFERED, FILE_ANY_ACCESS)

typedef struct _SRV_RESUME_KEY {
    UINT64 ResumeKey;
    UINT64 Timestamp;
    UINT64 Pid;
} SRV_RESUME_KEY, *PSRV_RESUME_KEY;

typedef struct _SRV_REQUEST_RESUME_KEY {
    SRV_RESUME_KEY Key;
    ULONG  ContextLength;
    BYTE   Context[1];
} SRV_REQUEST_RESUME_KEY, *PSRV_REQUEST_RESUME_KEY;
```

Эти члены можно описать следующим образом.



| Член                                                                                                                       | Описание                                                                                                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ResumeKey"></span><span id="resumekey"></span><span id="RESUMEKEY"></span>**ресумекэй**<br/>                 | Непрозрачное значение, идентифицирующее исходный файл на сервере.<br/>                                                                                                   |
| <span id="Timestamp"></span><span id="timestamp"></span><span id="TIMESTAMP"></span>**Timestamp**<br/>                 | Непрозрачное значение, определяющее время открытия файла.<br/>                                                                                               |
| <span id="Pid"></span><span id="pid"></span><span id="PID"></span>**PID**<br/>                                         | Непрозрачное значение, идентифицирующее процесс, открывший файл.<br/>                                                                                                |
| <span id="Key"></span><span id="key"></span><span id="KEY"></span>**Раздел**<br/>                                         | Структура **\_ \_ ключа возобновления SRV** . Для выполнения операции копирования на стороне сервера используйте эту структуру с управляющим кодом [**ioctl \_ COPYCHUNK**](ioctl-copychunk.md) .<br/> |
| <span id="ContextLength"></span><span id="contextlength"></span><span id="CONTEXTLENGTH"></span>**контекстленгс**<br/> | Этот член зарезервирован для системного использования; не используйте.<br/>                                                                                                              |
| <span id="Context"></span><span id="context"></span><span id="CONTEXT"></span>**Локального**<br/>                         | Этот член зарезервирован для системного использования; не используйте.<br/>                                                                                                              |



 

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[**\_COPYCHUNK ioctl**](ioctl-copychunk.md)
</dt> </dl>

 

 
