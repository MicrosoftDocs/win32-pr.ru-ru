---
description: Задает различные сведения о батарее.
ms.assetid: b827983d-5fb8-43f2-b732-541d16b3eb7b
title: Код элемента управления IOCTL_BATTERY_SET_INFORMATION (Покласс. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_BATTERY_SET_INFORMATION
api_type:
- HeaderDef
api_location:
- Poclass.h
- Batclass.h
ms.openlocfilehash: be6fca1042c4ba381996ccca1740d1662f9795269aaaa8b3e429576d96011dbc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143497"
---
# <a name="ioctl_battery_set_information-control-code"></a>\_ \_ Контрольный код для настройки аккумулятора с ПАРАМЕТРом ioctl \_

Задает различные сведения о батарее. Структура входных параметров, [**\_ \_ информация о заряде аккумулятора**](battery-set-information-str.md), указывает, какие сведения о состоянии аккумулятора должны быть установлены.

Чтобы выполнить эту операцию, вызовите функцию [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) со следующими параметрами.


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,              // handle to battery
  IOCTL_BATTERY_SET_INFORMATION, // dwIoControlCode
  (LPVOID) lpInBuffer,           // input buffer
  (DWORD) nInBufferSize,         // size of input buffer
  NULL,                          // lpOutBuffer
  0,                             // nOutBufferSize
  (LPDWORD) lpBytesReturned,     // number of bytes returned
  (LPOVERLAPPED) lpOverlapped    // OVERLAPPED structure
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хдевице* 
</dt> <dd>

Маркер батареи, для которого задаются сведения. Чтобы получить маркер устройства, вызовите функцию [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) .

</dd> <dt>

*двиоконтролкоде* 
</dt> <dd>

Управляющий код для операции. Это значение определяет конкретную выполняемую операцию и тип устройства, на котором она выполняется. Использовать **\_ \_ \_ сведения о настройке аккумулятора** с помощью ioctl для этой операции.

</dd> <dt>

*лпинбуффер* 
</dt> <dd>

Указатель на структуру [**\_ \_ сведений о наборе аккумулятора**](battery-set-information-str.md) .

</dd> <dt>

*нинбуфферсизе* 
</dt> <dd>

Размер входного буфера в байтах.

</dd> <dt>

*лпаутбуффер* 
</dt> <dd>

Не используется в этой операции; Задайте **значение NULL**.

</dd> <dt>

*наутбуфферсизе* 
</dt> <dd>

Не используется в этой операции; присвойте ему значение 0.

</dd> <dt>

*лпбитесретурнед* 
</dt> <dd>

Указатель на переменную, которая получает размер данных, возвращаемых в буфере *лпаутбуффер* , в байтах.

Если выходной буфер слишком мал для возвращения каких-либо данных, вызов завершается ошибкой, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) возвращает код ошибки \_ недостаточный \_ Размер буфера, а возвращенное число байтов равно нулю.

Если *лповерлаппед* имеет **значение NULL** (ноноверлаппед I/O), *Лпбитесретурнед* не может иметь **значение NULL**, даже если *лпаутбуффер* имеет **значение NULL**.

Если *лповерлаппед* не **равно NULL** (перекрывающиеся операции ввода-вывода), *лпбитесретурнед* может иметь **значение NULL**. Если это операция с перекрытием, можно получить число байтов, возвращенных путем вызова функции [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) . Если *хдевице* связан с портом завершения ввода-вывода, можно получить число возвращаемых байтов, вызвав функцию [**жеткуеуедкомплетионстатус**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) .

</dd> <dt>

*лповерлаппед* 
</dt> <dd>

Указатель на структуру [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) .

Если *хдевице* был открыт с \_ \_ флагом File Flag OVERLAPPED, *лповерлаппед* должен указывать на допустимую структуру [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) . В этом случае [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) выполняется как Перекрываемая (асинхронная) операция. Если устройство было открыто с \_ флагом File Flag \_ OVERLAPPED и *Лповерлаппед* имеет **значение NULL**, функция завершается ошибкой непредсказуемым образом.

Если *хдевице* был открыт без указания \_ \_ флага File Flag OVERLAPPED, *Лповерлаппед* игнорируется и функция [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) не возвращает значение до тех пор, пока операция не будет завершена или пока не произойдет ошибка.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если операция завершается успешно, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) возвращает ненулевое значение.

Если операция завершается неудачно или ожидает выполнения, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) возвращает ноль. Дополнительные сведения об ошибке можно получить, вызвав [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Комментарии

Все запросы на установку сведений о батарее будут завершаться с состоянием " \_ файл ошибки \_ не \_ найдено", если заданный в запросе тег батареи не соответствует значению текущего тега батареи.

Влияние перекрывающегося ввода-вывода на эту операцию см. в разделе "Примечания" раздела [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения XP\]<br/>                                                                                                                                                                                                                         |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                                                                                                                                                                                                |
| Header<br/>                   | <dl> <dt>Покласс. h;</dt> <dt>баткласс. h на Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows Server 2003 и Windows XP</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Сведения о батарее](battery-information.md)
</dt> <dt>

[Управляющие коды управления питанием](power-management-control-codes.md)
</dt> <dt>

[**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[**\_ \_ сведения о настройке аккумулятора**](battery-set-information-str.md)
</dt> <dt>

[**\_ \_ сведения о запросе от аккумулятора ioctl \_**](ioctl-battery-query-information.md)
</dt> <dt>

[**\_ \_ состояние запроса аккумулятора \_ ioctl**](ioctl-battery-query-status.md)
</dt> <dt>

[**\_тег запроса на батарею ioctl \_ \_**](ioctl-battery-query-tag.md)
</dt> </dl>

 

