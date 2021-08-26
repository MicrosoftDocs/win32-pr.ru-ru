---
description: '\_Управляющий код COPYCHUNK ioctl инициирует копию диапазона данных на стороне сервера, называемую также фрагментом.'
ms.assetid: 36f68840-bd5c-4cfc-a8ad-0cfbbdc5a2a9
title: Код элемента управления IOCTL_COPYCHUNK
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COPY_CHUNK
api_type:
- NA
api_location: ''
ms.openlocfilehash: 415e94d8ed19d3248beb31d8a5e6327e1adc11078483d4f60fcd42699e4dab89
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120001734"
---
# <a name="ioctl_copychunk-control-code"></a>\_Управляющий код COPYCHUNK ioctl

Управляющий код **\_ COPYCHUNK ioctl** инициирует копию диапазона данных на стороне сервера, называемую также фрагментом.

Чтобы выполнить эту операцию, вызовите функцию [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) со следующими параметрами.


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,             // handle to device
  IOCTL_COPYCHUNK,              // dwIoControlCode
  (LPVOID) lpInBuffer,          // input buffer
  (DWORD) nInBufferSize,        // size of input buffer
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

Описатель файла, который является целевым объектом операции копирования на стороне сервера. Чтобы получить этот маркер, вызовите функцию [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) .

</dd> <dt>

*двиоконтролкоде* \[ окне\]
</dt> <dd>

Управляющий код для операции. Для этой операции используйте **ioctl \_ COPYCHUNK** .

</dd> <dt>

*лпинбуффер* 
</dt> <dd>

Указатель на входной буфер — структуру **копирования SRV- \_ COPYCHUNK \_** . Дополнительные сведения см. в разделе "Замечания".

</dd> <dt>

*нинбуфферсизе* \[ окне\]
</dt> <dd>

Размер входного буфера в байтах.

</dd> <dt>

*лпаутбуффер* \[ заполняет\]
</dt> <dd>

Указатель на выходной буфер, структура **\_ \_ ответа SRV COPYCHUNK** . Дополнительные сведения см. в разделе "Замечания".

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
#define IOCTL_COPYCHUNK CTL_CODE(FILE_DEVICE_NETWORK_FILE_SYSTEM, 262, METHOD_BUFFERED,  FILE_READ_ACCESS)

typedef struct _SRV_COPYCHUNK {
    LARGE_INTEGER SourceOffset;
    LARGE_INTEGER DestinationOffset;
    ULONG  Length;
} SRV_COPYCHUNK, *PSRV_COPYCHUNK;

typedef struct _SRV_COPYCHUNK_COPY {
    SRV_RESUME_KEY SourceFile;
    ULONG          ChunkCount;
    ULONG          Reserved;
    SRV_COPYCHUNK  Chunk[1];    // Array
} SRV_COPYCHUNK_COPY, *PSRV_COPYCHUNK_COPY;

typedef struct _SRV_COPYCHUNK_RESPONSE {
    ULONG          ChunksWritten;
    ULONG          ChunkBytesWritten;
    ULONG          TotalBytesWritten;
} SRV_COPYCHUNK_RESPONSE, *PSRV_COPYCHUNK_RESPONSE;
```

Эти члены можно описать следующим образом.



| Член                                                                                                                                       | Описание                                                                                                                                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SourceOffset"></span><span id="sourceoffset"></span><span id="SOURCEOFFSET"></span>**саурцеоффсет**<br/>                     | Смещение в байтах от начала исходного файла до копируемого фрагмента.<br/>                                                                                                                                                                                                                                                                     |
| <span id="DestinationOffset"></span><span id="destinationoffset"></span><span id="DESTINATIONOFFSET"></span>**дестинатионоффсет**<br/> | Смещение (в байтах) от начала целевого файла до места копирования фрагмента.<br/>                                                                                                                                                                                                                                               |
| <span id="Length"></span><span id="length"></span><span id="LENGTH"></span>**Недопустим**<br/>                                             | Число байтов данных в копируемом фрагменте. Должно быть больше нуля и меньше или равно 1 МБ. **Длина** \* **Чунккаунт** должно быть меньше или равно 16 МБ.<br/>                                                                                                                                                                         |
| <span id="SourceFile"></span><span id="sourcefile"></span><span id="SOURCEFILE"></span>**SourceFile**<br/>                             | Ключ, представляющий исходный файл с копируемыми данными. Этот ключ получен с помощью [**\_ \_ \_ \_ ключа возобновления запроса фсктл SRV**](fsctl-srv-request-resume-key.md).<br/>                                                                                                                                                                                   |
| <span id="ChunkCount"></span><span id="chunkcount"></span><span id="CHUNKCOUNT"></span>**чунккаунт**<br/>                             | Число копируемых фрагментов. Должно быть больше нуля и меньше или равно 256.<br/>                                                                                                                                                                                                                                                                |
| <span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Процессу**<br/>                                     | Этот член зарезервирован для системного использования; не используйте.<br/>                                                                                                                                                                                                                                                                                                        |
| <span id="Chunk"></span><span id="chunk"></span><span id="CHUNK"></span>**Фрагмент**<br/>                                                 | Массив структур COPYCHUNK **чунккаунт** **SRV \_** , по одному для каждого копируемого фрагмента. Длина этого массива в байтах должна быть **чунккаунт** \* sizeof (**SRV \_ COPYCHUNK**).<br/>                                                                                                                                                                       |
| <span id="ChunksWritten"></span><span id="chunkswritten"></span><span id="CHUNKSWRITTEN"></span>**чунксвриттен**<br/>                 | Если операция завершилась ошибкой **с \_ недопустимым \_ параметром**, это значение указывает максимальное количество фрагментов, которые сервер будет принимать в одном запросе, то есть 256. В противном случае это значение указывает количество успешно записанных блоков.<br/>                                                                                               |
| <span id="ChunkBytesWritten"></span><span id="chunkbyteswritten"></span><span id="CHUNKBYTESWRITTEN"></span>**чункбитесвриттен**<br/> | Если операция завершилась ошибкой **с \_ недопустимым \_ параметром**, это значение указывает максимальное число байтов, которое сервер будет разрешать записывать в один блок, который равен 1 МБ. В противном случае это значение указывает число байтов, успешно записанных в последний фрагмент, который не был успешно обработан (если произошла частичная запись).<br/> |
| <span id="TotalBytesWritten"></span><span id="totalbyteswritten"></span><span id="TOTALBYTESWRITTEN"></span>**тоталбитесвриттен**<br/> | Если операция завершилась ошибкой **с \_ недопустимым \_ параметром**, это значение указывает максимальное число байтов, которое будет скопировано сервером в одном запросе, что составляет 16 МБ. В противном случае это значение указывает число успешно записанных байтов.<br/>                                                                                                 |



 

## <a name="see-also"></a>См. также

<dl> <dt>

[**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[**\_ \_ \_ ключ возобновления запроса SRV фсктл \_**](fsctl-srv-request-resume-key.md)
</dt> </dl>

 

 
