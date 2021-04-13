---
title: Управляющий код FSCTL_DFS_GET_PKT_ENTRY_STATE (LmDfs.h)
description: Код элемента управления FSCTL_DFS_GET_PKT_ENTRY_STATE может получить те же сведения, что и функция Нетдфсжетклиентинфо, но может обеспечить лучшую производительность в некоторых конфигурациях с высокой задержкой для серверов DFS.
ms.assetid: d4eec104-128b-43b5-9fae-08ab0b977dec
topic_type:
- apiref
api_name:
- FSCTL_DFS_GET_PKT_ENTRY_STATE
api_location:
- LmDfs.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a57fb448934908ebc1530e95a298715324aaee6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539176"
---
# <a name="fsctl_dfs_get_pkt_entry_state-control-code"></a>Код элемента управления FSCTL_DFS_GET_PKT_ENTRY_STATE

Код элемента управления **FSCTL_DFS_GET_PKT_ENTRY_STATE** может получить те же сведения, что и функция [**нетдфсжетклиентинфо**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetclientinfo) , но может обеспечить лучшую производительность в некоторых конфигурациях с высокой задержкой для серверов DFS. Не рекомендуется использовать управляющий код **FSCTL_DFS_GET_PKT_ENTRY_STATE** , если нет проблем с производительностью.

Чтобы выполнить эту операцию, вызовите функцию [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) со следующими параметрами.

```C++
BOOL 
   WINAPI 
   DeviceIoControl( (HANDLE)       hDevice,            // handle to device
                    (DWORD)        FSCTL_DFS_GET_PKT_ENTRY_STATE, // dwIoControlCode(LPDWORD)      lpInBuffer,         // input buffer
                    (DWORD)        nInBufferSize,      // size of input buffer
                    (LPDWORD)      lpOutBuffer,        // output buffer
                    (DWORD)        nOutBufferSize,     // size of output buffer
                    (LPDWORD)      lpBytesReturned,    // number of bytes returned
                    (LPOVERLAPPED) lpOverlapped );     // OVERLAPPED structure
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*хдевице* [in]
</dt> <dd>

Маркер устройства. Чтобы получить маркер устройства, вызовите функцию [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) .

</dd> <dt>

*двиоконтролкоде* [in]
</dt> <dd>

Управляющий код для операции. Для этой операции используйте **FSCTL_DFS_GET_PKT_ENTRY_STATE** .

</dd> <dt>

*лпинбуффер* 
</dt> <dd>

Адрес структуры [**DFS_GET_PKT_ENTRY_STATE_ARG**](/windows/win32/api/lmdfs/ns-lmdfs-dfs_get_pkt_entry_state_arg) и следующих 1-3 строк Юникода.

</dd> <dt>

*нинбуфферсизе* [in]
</dt> <dd>

Размер (в байтах) буфера, на который указывает параметр *лпинбуффер* .

</dd> <dt>

*лпаутбуффер* [out]
</dt> <dd>

Адрес структуры **DFS_INFO_ \#** и любых строк и структур, на которые указывает структура **DFS_INFO_ \#** . Возвращаемая структура зависит от элемента **уровня** в структуре [**DFS_GET_PKT_ENTRY_STATE_ARG**](/windows/win32/api/lmdfs/ns-lmdfs-dfs_get_pkt_entry_state_arg) , передаваемой во входном буфере.

</dd> <dt>

*наутбуфферсизе* [in]
</dt> <dd>

Размер (в байтах) буфера, на который указывает параметр *лпаутбуффер* . Из-за строк и структур, на которые ссылается возвращенная **DFS_INFO_ная \#** структура, которые также находятся в выходном буфере, этот буфер должен быть больше, чем указанная структура **DFS_INFO_ \#** .

</dd> <dt>

*лпбитесретурнед* [out]
</dt> <dd>

Указатель на переменную, которая получает размер данных, хранящихся в буфере вывода, в байтах.

Если выходной буфер слишком мал, но, по крайней мере, достаточно большой для хранения **DWORD**, происходит сбой вызова, [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) возвращает **ERROR_MORE_DATA**, а первый **DWORD** выходного буфера содержит необходимый размер. Если выходной буфер не может содержать **DWORD** , вызов завершается с **ERROR_INSUFFICIENT_BUFFER**, а *лпбитесретурнед* — нулем.

Если *лповерлаппед* имеет **значение NULL**, *Лпбитесретурнед* не может иметь **значение NULL**. Даже если операция не возвращает выходные данные, а *лпаутбуффер* имеет **значение NULL**, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) использует *лпбитесретурнед*. После такой операции значение *лпбитесретурнед* не имеет смысла.

Если *лповерлаппед* не **равно NULL**, *лпбитесретурнед* может иметь **значение NULL**. Если этот параметр не равен **null** и операция возвращает данные, *лпбитесретурнед* не имеет смысла до тех пор, пока не завершится операция перекрытия. Чтобы получить число возвращаемых байтов, вызовите [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult). Если параметр *хдевице* связан с портом завершения ввода-вывода, можно получить число байтов, возвращенных вызовом [**жеткуеуедкомплетионстатус**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus).

</dd> <dt>

*лповерлаппед* [in]
</dt> <dd>

Указатель на структуру [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) .

Если *хдевице* был открыт без указания **FILE_FLAG_OVERLAPPED**, *лповерлаппед* игнорируется.

Если *хдевице* был открыт с флагом **FILE_FLAG_OVERLAPPED** , операция выполняется как Перекрываемая (асинхронная) операция. В этом случае *лповерлаппед* должен указывать на допустимую структуру [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) , которая содержит указатель на объект события. В противном случае функция завершается ошибкой непредсказуемым образом.

Для операций с перекрытием [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) возвращает значение немедленно, а объект события получает сигнал о завершении операции. В противном случае функция не возвращает значение до тех пор, пока операция не будет завершена или произойдет ошибка.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если операция завершается успешно, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) возвращает ненулевое значение.

Если операция завершается неудачно или ожидает выполнения, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) возвращает ноль. Дополнительные сведения об ошибке можно получить, вызвав [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="requirements"></a>Требования

| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                             |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                                       |
| Header<br/>                   | <dl> <dt>Лмдфс. h (включение Лмдфс. h)</dt> </dl> |

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[**нетдфсжетклиентинфо**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetclientinfo)
</dt> </dl>
