---
description: '\_ \_ \_ Код управления атрибутами Da Get NFS запрашивает дополнительные сведения о ресурсе NFS.'
ms.assetid: BC9E0E19-7D78-4AE7-A3E6-9FD9212B2B83
title: Код элемента управления DA_GET_NFS_ATTRIBUTES
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DA_GET_NFS_ATTRIBUTES
api_type:
- NA
api_location: ''
ms.openlocfilehash: 4427dd48190bd12f7837c4841a98e15f7ddaff5f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538681"
---
# <a name="da_get_nfs_attributes-control-code"></a>\_ \_ \_ Код элемента управления для получения атрибутов NFS

Код **управления \_ \_ \_ атрибутами Da Get NFS** запрашивает дополнительные сведения о ресурсе NFS.

Чтобы выполнить эту операцию, вызовите функцию [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) со следующими параметрами.


```C++
BOOL 
   WINAPI 
   DeviceIoControl( (HANDLE)       hDevice,               // handle to device
                    (DWORD)        DA_GET_NFS_ATTRIBUTES, // dwIoControlCode
                                   NULL,                  // lpInBuffer
                                   0,                     // nInBufferSize
                    (LPDWORD)      lpOutBuffer,           // output buffer
                    (DWORD)        nOutBufferSize,        // size of output buffer
                    (LPDWORD)      lpBytesReturned,       // number of bytes returned
                    (LPOVERLAPPED) lpOverlapped );        // OVERLAPPED structure
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хдевице* \[ окне\]
</dt> <dd>

Маркер файла в общей папке NFS. Чтобы получить этот маркер, вызовите функцию [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) .

</dd> <dt>

*двиоконтролкоде* \[ окне\]
</dt> <dd>

Управляющий код для операции. Для этой операции используйте **\_ \_ \_ атрибут Da Get NFS** .

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

Указатель на выходной буфер, который содержит структуру **\_ \_ атрибутов файла NFS** . Дополнительные сведения см. в разделе "Замечания".

</dd> <dt>

*наутбуфферсизе* \[ окне\]
</dt> <dd>

Размер выходного буфера в байтах.

</dd> <dt>

*лпбитесретурнед* \[ заполняет\]
</dt> <dd>

Указатель на переменную, которая получает размер данных, хранящихся в буфере вывода, в байтах.

Если выходной буфер слишком мал, вызов завершается ошибкой, [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) возвращает **ошибку \_ недостаточно \_ буфера**, а *лпбитесретурнед* — ноль.

Если *лповерлаппед* имеет **значение NULL**, *Лпбитесретурнед* не может иметь **значение NULL**. Даже если операция не возвращает выходные данные, а *лпаутбуффер* имеет **значение NULL**, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) использует *лпбитесретурнед*. После такой операции значение *лпбитесретурнед* не имеет смысла.

Если *лповерлаппед* не **равно NULL**, *лпбитесретурнед* может иметь **значение NULL**. Если этот параметр не равен **null** и операция возвращает данные, *лпбитесретурнед* не имеет смысла до тех пор, пока не завершится операция перекрытия. Чтобы получить число возвращаемых байтов, вызовите [**GetOverlappedResult**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult). Если параметр *хдевице* связан с портом завершения ввода-вывода, можно получить число байтов, возвращенных вызовом [**жеткуеуедкомплетионстатус**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus).

</dd> <dt>

*лповерлаппед* \[ окне\]
</dt> <dd>

Указатель на структуру [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) .

Если *хдевице* был открыт без указания **\_ флага файла \_ OVERLAPPED**, *лповерлаппед* игнорируется.

Если *хдевице* был открыт с флагом **File \_ Flag \_ OVERLAPPED** , операция выполняется как Перекрываемая (асинхронная) операция. В этом случае *лповерлаппед* должен указывать на допустимую структуру [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) , которая содержит указатель на объект события. В противном случае функция завершается ошибкой непредсказуемым образом.

Для операций с перекрытием [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) возвращает значение немедленно, а объект события получает сигнал о завершении операции. В противном случае функция не возвращает значение до тех пор, пока операция не будет завершена или произойдет ошибка.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если операция завершается успешно, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) возвращает ненулевое значение.

Если операция завершается неудачно или ожидает выполнения, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) возвращает ноль. Дополнительные сведения об ошибке можно получить, вызвав [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Комментарии

Этот управляющий код не имеет связанного файла заголовка. Необходимо определить управляющий код и структуры данных следующим образом.

``` syntax
#define DEVICE_DA_RDR 0x80000  
 
#define DA_GET_NFS_ATTRIBUTES CTL_CODE(DEVICE_DA_RDR, 0x804, METHOD_BUFFERED, FILE_ANY_ACCESS)

typedef struct _NFS_SPEC_DATA {  
    ULONG               SpecData1;
    ULONG               SpecData2;
} NFS_SPEC_DATA, *PNFS_SPEC_DATA;

typedef struct _NFS_TIME {
    ULONG        Seconds;
    ULONG        nSeconds;
} NFS_TIME, *PNFS_TIME;

#define NFS_TYPE_REG         1
#define NFS_TYPE_DIR         2
#define NFS_TYPE_BLK         3
#define NFS_TYPE_CHR         4
#define NFS_TYPE_LNK         5
#define NFS_TYPE_SOCK        6
#define NFS_TYPE_FIFO        7

typedef struct _NFS_FILE_ATTRIBUTES {  
    ULONG               FileType;  
    ULONG               Mode;  
    ULONG               NLink;  
    ULONG               Uid;  
    ULONG               Gid;  
    ULONGLONG           Size;  
    ULONGLONG           Used;
    NFS_SPEC_DATA       Rdev;
    ULONGLONG           Fsid;  
    ULONGLONG           FileId;  
    NFS_TIME            AccessTime;  
    NFS_TIME            ModifyTime;  
    NFS_TIME            ChangeTime;  
} NFS_FILE_ATTRIBUTES, *PNFS_FILE_ATTRIBUTES;

typedef struct _DA_FILE_ATTRIBUTES {  
    NFS_FILE_ATTRIBUTES FileAttributes;  
    ULONG               Version;  
} DA_FILE_ATTRIBUTES, *PDA_FILE_ATTRIBUTES;
```

Члены структуры можно описать следующим образом.

<dl> <dt>

<span id="SpecData1"></span><span id="specdata1"></span><span id="SPECDATA1"></span>**SpecData1**
</dt> <dd>

Непрозрачное значение, используемое для специальных типов файлов, таких как файлы специального блока, специального символьного типа и FIFO.

</dd> <dt>

<span id="SpecData2"></span><span id="specdata2"></span><span id="SPECDATA2"></span>**SpecData2**
</dt> <dd>

Непрозрачное значение, используемое для специальных типов файлов, таких как файлы специального блока, специального символьного типа и FIFO.

</dd> <dt>

<span id="Seconds"></span><span id="seconds"></span><span id="SECONDS"></span>**Несколько**
</dt> <dd>

64-разрядное значение, представляющее секунды с 1 января 1970 (UTC).

</dd> <dt>

<span id="nSeconds"></span><span id="nseconds"></span><span id="NSECONDS"></span>**нсекондс**
</dt> <dd>

Число наносекунд, добавляемых к элементу **секунд** .

</dd> <dt>

<span id="FileType"></span><span id="filetype"></span><span id="FILETYPE"></span>**FileType**
</dt> <dd>

Тип файла NFS для общей папки.



| Тип файла NFS                                                                              | Описание                          |
|--------------------------------------------------------------------------------------------|--------------------------------------|
| <span id="NFS_TYPE_REG"></span><span id="nfs_type_reg"></span>\_тип NFS \_ reg<br/>    | Обычный файл.<br/>           |
| <span id="NFS_TYPE_DIR"></span><span id="nfs_type_dir"></span>\_dir тип \_ NFS<br/>    | Каталог.<br/>              |
| <span id="NFS_TYPE_BLK"></span><span id="nfs_type_blk"></span>\_тип NFS \_ BLK<br/>    | Специальный блочный файл.<br/>     |
| <span id="NFS_TYPE_CHR"></span><span id="nfs_type_chr"></span>\_тип NFS типа \_ Chr<br/>    | Специальный символьный файл.<br/> |
| <span id="NFS_TYPE_LNK"></span><span id="nfs_type_lnk"></span>\_тип NFS \_ LNK<br/>    | Символьная ссылка.<br/>          |
| <span id="NFS_TYPE_SOCK"></span><span id="nfs_type_sock"></span>\_тип NFS \_ Сокк<br/> | Сокет Windows.<br/>         |
| <span id="NFS_TYPE_FIFO"></span><span id="nfs_type_fifo"></span>\_тип NFS \_ FIFO<br/> | Файл FIFO.<br/>              |



 

</dd> <dt>

<span id="Mode"></span><span id="mode"></span><span id="MODE"></span>**Режима**
</dt> <dd>

Режим файла.

</dd> <dt>

<span id="NLink"></span><span id="nlink"></span><span id="NLINK"></span>**нлинк**
</dt> <dd>

Число ссылок на общую папку.

</dd> <dt>

<span id="Uid"></span><span id="uid"></span><span id="UID"></span>**Такой**
</dt> <dd>

Идентификатор пользователя UNIX (UID).

</dd> <dt>

<span id="Gid"></span><span id="gid"></span><span id="GID"></span>**Операционной**
</dt> <dd>

Идентификатор группы UNIX (GID).

</dd> <dt>

<span id="Size"></span><span id="size"></span><span id="SIZE"></span>**Изменять**
</dt> <dd>

Размер файла в байтах.

</dd> <dt>

<span id="Used"></span><span id="used"></span><span id="USED"></span>**Используется**
</dt> <dd>

Используемый размер файла в байтах. Это то же самое, что и размер файла.

</dd> <dt>

<span id="Rdev"></span><span id="rdev"></span><span id="RDEV"></span>**рдев**
</dt> <dd>

Идентификатор устройства.

</dd> <dt>

<span id="Fsid"></span><span id="fsid"></span><span id="FSID"></span>**фсид**
</dt> <dd>

Идентификатор файловой системы.

</dd> <dt>

<span id="FileId"></span><span id="fileid"></span><span id="FILEID"></span>**ИД**
</dt> <dd>

Идентификатор файла.

</dd> <dt>

<span id="AccessTime"></span><span id="accesstime"></span><span id="ACCESSTIME"></span>**акцесстиме**
</dt> <dd>

Время последнего доступа.

</dd> <dt>

<span id="ModifyTime"></span><span id="modifytime"></span><span id="MODIFYTIME"></span>**модифитиме**
</dt> <dd>

Время последнего изменения.

</dd> <dt>

<span id="ChangeTime"></span><span id="changetime"></span><span id="CHANGETIME"></span>**чанжетиме**
</dt> <dd>

Время последнего изменения.

</dd> <dt>

<span id="FileAttributes"></span><span id="fileattributes"></span><span id="FILEATTRIBUTES"></span>**FileAttributes**
</dt> <dd>

Структура **\_ \_ атрибутов файла NFS** .

> [!Note]  
> Более подробное описание членов этой структуры см. в описании структуры **fattr3** в спецификации протокола NFS версии 3 (как определено в [RFC 1813](https://www.ietf.org/rfc/rfc1813.txt)).

 

</dd> <dt>

<span id="Version"></span><span id="version"></span><span id="VERSION"></span>**Версия**
</dt> <dd>

Указывает, является ли подключение, для которого был создан маркер, для общего ресурса NFS по протоколу NFS версии 2 или NFS версии 3.



| Значение                            | Описание              |
|----------------------------------|--------------------------|
| <span id="2"></span>2<br/> | NFS версии 2<br/> |
| <span id="3"></span>3-5<br/> | NFS версии 3<br/> |



 

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>         |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>    |
| Окончание поддержки клиента<br/>    | Ни одна версия не поддерживается<br/>         |
| Поддержка конца сервера<br/>    | Windows Server 2008 R2<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> </dl>

 

 
