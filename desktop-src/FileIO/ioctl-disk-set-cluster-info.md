---
description: Задает сведения о кластере на диске.
ms.assetid: AB2243D9-4913-4412-87E0-2C8DB8AB10B8
title: Код элемента управления IOCTL_DISK_SET_CLUSTER_INFO (Нтдддиск. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_DISK_SET_CLUSTER_INFO
api_type:
- HeaderDef
api_location:
- Ntdddisk.h
ms.openlocfilehash: 4ba0994dd1c9030e84c22e24b1eb4583eba7e3d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664426"
---
# <a name="ioctl_disk_set_cluster_info-control-code"></a>\_ \_ \_ \_ Управляющий код для сведений о кластере для набора дисков ioctl

Задает сведения о кластере на диске.

Чтобы выполнить эту операцию, вызовите функцию [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) со следующими параметрами.


```C++
BOOL 
WINAPI 
DeviceIoControl( (HANDLE)       hDevice,         // handle to device 
                 IOCTL_DISK_SET_CLUSTER_INFO,    // dwIoControlCode
                 (LPVOID)       NULL,            // lpInBuffer 
                 (DWORD)        0,               // nInBufferSize 
                 (LPVOID)       lpOutBuffer,     // output buffer:GET_DISK_ATTRIBUTES
                 (DWORD)        nOutBufferSize,  // size of output buffer
                 (LPDWORD)      lpBytesReturned, // number of bytes returned
                 (LPOVERLAPPED) lpOverlapped );  // OVERLAPPED structure
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хдевице* 
</dt> <dd>

Маркер диска.

Чтобы получить маркер устройства, вызовите функцию [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) .

</dd> <dt>

*двиоконтролкоде* 
</dt> <dd>

Управляющий код для операции.

Используйте **ioctl \_ дискового \_ задания \_ \_ сведения о кластере** для этой операции.

</dd> <dt>

*лпинбуффер* 
</dt> <dd>

Указатель на структуру данных [**\_ \_ о кластере дисков**](disk-cluster-info.md) , содержащую сведения о кластере для диска.

</dd> <dt>

*нинбуфферсизе* 
</dt> <dd>

Размер входного буфера в байтах.

</dd> <dt>

*лпаутбуффер* 
</dt> <dd>

Не используется с этой операцией. Задайте **значение NULL**.

</dd> <dt>

*наутбуфферсизе* 
</dt> <dd>

Размер выходного буфера в байтах. Задайте значение 0 (ноль).

</dd> <dt>

*лпбитесретурнед* 
</dt> <dd>

Не используется с этой операцией. Задайте **значение NULL**.

</dd> <dt>

*лповерлаппед* 
</dt> <dd>

Указатель на структуру [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) .

Если *хдевице* был открыт без указания **\_ флага файла \_ OVERLAPPED**, *лповерлаппед* игнорируется.

Если *хдевице* был открыт с флагом **File \_ Flag \_ OVERLAPPED** , операция выполняется как Перекрываемая (асинхронная) операция. В этом случае *лповерлаппед* должен указывать на допустимую структуру [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) , которая содержит указатель на объект события. В противном случае функция завершается ошибкой непредсказуемым образом.

Для операций с перекрытием [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) возвращает значение немедленно, а объект события получает сигнал о завершении операции. В противном случае функция не возвращает значение до тех пор, пока операция не будет завершена или произойдет ошибка.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если операция завершается успешно, указывая на то, что все тома на диске готовы к использованию, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) возвращает ненулевое значение.

Если операция завершается неудачно или ожидает выполнения, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) возвращает ноль. Дополнительные сведения об ошибке можно получить, вызвав [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                             |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Нтдддиск. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[Управляющие коды управления дисками](disk-management-control-codes.md)
</dt> <dt>

[**\_сведения о кластере диска \_**](disk-cluster-info.md)
</dt> <dt>

[**IOCTL \_ Disk \_ Получение \_ \_ сведений о кластере**](ioctl-disk-get-cluster-info.md)
</dt> </dl>

 

