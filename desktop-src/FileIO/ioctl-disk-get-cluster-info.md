---
description: Извлекает атрибуты указанного дискового устройства.
ms.assetid: 2FF81F67-9E70-43C6-A504-0D60382E0945
title: Код элемента управления IOCTL_DISK_GET_CLUSTER_INFO (Нтдддиск. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_DISK_GET_CLUSTER_INFO
api_type:
- HeaderDef
api_location:
- Ntdddisk.h
ms.openlocfilehash: 3acf923a9f0288bd3fe3a0b12d4c61b71437f61c1c4f96a3a3bef1af5f05fd95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068684"
---
# <a name="ioctl_disk_get_cluster_info-control-code"></a>IOCTL \_ Disk \_ Получение \_ \_ кода управления сведениями о кластере

Извлекает атрибуты указанного дискового устройства.

Чтобы выполнить эту операцию, вызовите функцию [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) со следующими параметрами.


```C++
BOOL 
WINAPI 
DeviceIoControl( (HANDLE)       hDevice,         // handle to device 
                 IOCTL_DISK_GET_CLUSTER_INFO,    // dwIoControlCode
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

Использование **ioctl \_ Disk \_ Получение \_ \_ сведений о кластере** для этой операции.

</dd> <dt>

*лпинбуффер* 
</dt> <dd>

Не используется с этой операцией. Задайте **значение NULL**.

</dd> <dt>

*нинбуфферсизе* 
</dt> <dd>

Размер входного буфера в байтах. Задайте значение 0 (ноль).

</dd> <dt>

*лпаутбуффер* 
</dt> <dd>

Указатель на буфер, который получает структуру данных [**\_ \_ о дисковых кластерах**](disk-cluster-info.md) .

</dd> <dt>

*наутбуфферсизе* 
</dt> <dd>

Размер выходного буфера в байтах.

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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                             |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Нтдддиск. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[Управляющие коды управления дисками](disk-management-control-codes.md)
</dt> <dt>

[**\_сведения о кластере диска \_**](disk-cluster-info.md)
</dt> <dt>

[**\_ \_ сведения о наборе дисков для \_ кластера ioctl \_**](ioctl-disk-set-cluster-info.md)
</dt> </dl>

 

