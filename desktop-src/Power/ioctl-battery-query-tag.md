---
description: Извлекает текущий тег аккумулятора.
ms.assetid: 0bbe59ba-e037-47ce-a54a-6500ea7c9bc5
title: Код элемента управления IOCTL_BATTERY_QUERY_TAG (Покласс. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_BATTERY_QUERY_TAG
api_type:
- HeaderDef
api_location:
- Poclass.h
- BatClass.h
ms.openlocfilehash: 1d8435e62c4f061ac13b3e18e5bcd64afcb399c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673808"
---
# <a name="ioctl_battery_query_tag-control-code"></a>\_ \_ \_ Код элемента управления тега запроса на батарею ioctl

Извлекает текущий тег батареи.

Чтобы выполнить эту операцию, вызовите функцию [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) со следующими параметрами.


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,            // handle to battery
  IOCTL_BATTERY_QUERY_TAG,     // dwIoControlCode
  (LPVOID) lpInBuffer,         // input buffer
  (DWORD) nInBufferSize,       // size of input buffer
  (LPVOID) lpOutBuffer,        // output buffer
  (DWORD) nOutBufferSize,      // size of output buffer
  (LPDWORD) lpBytesReturned,   // number of bytes returned
  (LPOVERLAPPED) lpOverlapped);// OVERLAPPED structure
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хдевице* 
</dt> <dd>

Маркер батареи, из которого извлекается тег. Чтобы получить маркер устройства, вызовите функцию [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) .

</dd> <dt>

*двиоконтролкоде* 
</dt> <dd>

Управляющий код для операции. Это значение определяет конкретную выполняемую операцию и тип устройства, на котором она выполняется. Для этой операции используйте **\_ \_ \_ тег запроса на батарею от аккумулятора** .

</dd> <dt>

*лпинбуффер* 
</dt> <dd>

Указатель на входной буфер типа **ulong** . Значение указывает время ожидания в миллисекундах при отсутствии аккумулятора. Значение-1 указывает на то, что запрос будет ждать бесконечно (или пока не отменяется другим событием).

</dd> <dt>

*нинбуфферсизе* 
</dt> <dd>

Размер входного буфера в байтах.

</dd> <dt>

*лпаутбуффер* 
</dt> <dd>

Указатель на выходной буфер **ulong** . При успешном выполнении этот буфер содержит тег текущего аккумулятора, который может быть любым значением, кроме тега батареи, является \_ \_ недопустимым. В случае сбоя, если [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) возвращает файл с кодом ошибки **\_ \_ не \_ найден**, этот буфер содержит **\_ \_ Недопустимый тег** значения для батареи.

</dd> <dt>

*наутбуфферсизе* 
</dt> <dd>

Размер выходного буфера в байтах.

</dd> <dt>

*лпбитесретурнед* 
</dt> <dd>

Указатель на переменную, которая получает размер данных, хранящихся в буфере *лпаутбуффер* , в байтах.

Если выходной буфер слишком мал для возвращения каких-либо данных, то вызов завершается неудачно, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) возвращает код ошибки **\_ недостаточный \_ Размер буфера**, а возвращенное число байтов равно нулю.

Если *лповерлаппед* имеет **значение NULL** (ноноверлаппед I/O), *Лпбитесретурнед* не может иметь **значение NULL**.

Если *лповерлаппед* не **равно NULL** (перекрывающиеся операции ввода-вывода), *лпбитесретурнед* может иметь **значение NULL**. Если это операция с перекрытием, можно получить число байтов, возвращенных путем вызова функции [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) . Если *хдевице* связан с портом завершения ввода-вывода, можно получить число возвращаемых байтов, вызвав функцию [**жеткуеуедкомплетионстатус**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) .

</dd> <dt>

*лповерлаппед* 
</dt> <dd>

Указатель на структуру [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) .

Если *хдевице* был открыт с флагом **File \_ Flag \_ OVERLAPPED** , *ЛПОВЕРЛАППЕД* должен указывать на допустимую структуру [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) . В этом случае [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) выполняется как Перекрываемая (асинхронная) операция. Если устройство было открыто с флагом **File \_ Flag \_ OVERLAPPED** и *лповерлаппед* имеет **значение NULL**, функция завершается ошибкой непредсказуемым образом.

Если *хдевице* был открыт без указания флага **File \_ Flag \_ OVERLAPPED** , *лповерлаппед* игнорируется и функция [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) не возвращает значение до тех пор, пока операция не будет завершена или пока не произойдет ошибка.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если операция завершается успешно, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) возвращает ненулевое значение.

Если операция завершается неудачно или ожидает выполнения, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) возвращает ноль. Дополнительные сведения об ошибке можно получить, вызвав [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Комментарии

Этот параметр аккумулятора IOCTL получает текущий тег батареи. Тег батареи — это уникальное ненулевое значение, которое изменяется при повторной вставке, замене или изменении характеристик физической батареи. Дополнительные сведения об изменении тега аккумулятора, обнаружении изменений и возможностях работы приложения после изменения тега батареи см. в разделе "Теги батареи" в разделе "Общие [сведения о батарее](battery-information.md) ". Если батарея отсутствует, этот запрос будет ждать указанного времени, и если батарея по-прежнему отсутствует, то будет возвращен **файл ошибки, который \_ \_ не \_ найден** , и установлен тег аккумулятора на **\_ \_ Недопустимый тег** аккумулятора. (Дополнительные сведения см. в разделе сведения о батарее.)

Для всех запросов других сведений о батарее требуется, чтобы вызывающий объект предоставил соответствующий тег батареи. Это гарантирует, что вызывающий объект получает информацию для одного и того же аккумулятора для каждого запроса и гарантирует, что вызывающий объект знает об изменениях аккумулятора без постоянного опроса.

Влияние перекрывающегося ввода-вывода на эту операцию см. в разделе "Примечания" раздела [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) .

## <a name="examples"></a>Примеры

Пример см. в разделе [Перечисление устройств аккумулятора](enumerating-battery-devices.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows XP\]<br/>                                                                                                                                                                                                                         |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                                                                                                                                                                                                |
| Header<br/>                   | <dl> <dt>Покласс. h; </dt> <dt>Баткласс. h в Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows server 2003 и Windows XP</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Сведения о батарее](battery-information.md)
</dt> <dt>

[Управляющие коды управления питанием](power-management-control-codes.md)
</dt> <dt>

[**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[**\_ \_ сведения о запросе от аккумулятора ioctl \_**](ioctl-battery-query-information.md)
</dt> <dt>

[**\_ \_ состояние запроса аккумулятора \_ ioctl**](ioctl-battery-query-status.md)
</dt> <dt>

[**\_ \_ сведения о настройке аккумулятора ioctl \_**](ioctl-battery-set-information.md)
</dt> </dl>

 

