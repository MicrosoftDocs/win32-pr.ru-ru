---
description: Получает текущее состояние аккумулятора.
ms.assetid: 7a7bf429-9b2c-4faf-9f27-fb5fd8dd18df
title: Код элемента управления IOCTL_BATTERY_QUERY_STATUS (Покласс. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_BATTERY_QUERY_STATUS
api_type:
- HeaderDef
api_location:
- Poclass.h
- BatClass.h
ms.openlocfilehash: e2de9d3ab48aec13a9a5c1957a5f98aefbe6a09f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663119"
---
# <a name="ioctl_battery_query_status-control-code"></a>\_ \_ \_ Управляющий код состояния запроса аккумулятора ioctl

Получает текущее состояние аккумулятора.

Чтобы выполнить эту операцию, вызовите функцию [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) со следующими параметрами.


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,           // handle to battery
  IOCTL_BATTERY_QUERY_STATUS, // dwIoControlCode
  (LPVOID) lpInBuffer,        // input buffer
  (DWORD) nInBufferSize,      // size of input buffer
  (LPVOID) lpOutBuffer,       // output buffer
  (DWORD) nOutBufferSize,     // size of output buffer
  (LPDWORD) lpBytesReturned,  // number of bytes returned
  (LPOVERLAPPED) lpOverlapped // OVERLAPPED structure
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хдевице* 
</dt> <dd>

Маркер аккумулятора, из которого возвращаются сведения. Чтобы получить маркер устройства, вызовите функцию [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) .

</dd> <dt>

*двиоконтролкоде* 
</dt> <dd>

Управляющий код для операции. Это значение определяет конкретную выполняемую операцию и тип устройства, на котором она выполняется. Использовать **\_ \_ \_ состояние запроса аккумулятора** для этой операции.

</dd> <dt>

*лпинбуффер* 
</dt> <dd>

Указатель на структуру [**\_ \_ состояния ожидания аккумулятора**](battery-wait-status-str.md) .

</dd> <dt>

*нинбуфферсизе* 
</dt> <dd>

Размер входного буфера в байтах.

</dd> <dt>

*лпаутбуффер* 
</dt> <dd>

Указатель на структуру [**\_ состояния аккумулятора**](battery-status-str.md) .

</dd> <dt>

*наутбуфферсизе* 
</dt> <dd>

Размер выходного буфера в байтах.

</dd> <dt>

*лпбитесретурнед* 
</dt> <dd>

Указатель на переменную, которая получает размер данных, возвращаемых в буфере *лпаутбуффер* , в байтах.

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

Этот параметр аккумулятора IOCTL получает состояние аккумулятора на момент возвращения операции. Структура входных параметров, [**\_ \_ состояние ожидания аккумулятора**](battery-wait-status-str.md), указывает, когда состояние аккумулятора должно быть обработано и возвращено.

Запросы на состояние аккумулятора могут быть доступны для немедленного возврата или могут быть настроены на ожидание определенного условия перед завершением. Например, можно установить запрос сведений о батарее, который ожидает, пока заряд батареи не достигнет заданной точки или не изменится состояние аккумулятора.

Все запросы сведений о батарее будут завершены с состоянием " **\_ файл ошибки \_ не \_ найден** ", если элемент **баттеритаг** запроса не соответствует значению текущего тега батареи. (Дополнительные сведения см. в разделе " [теги батареи](battery-information.md) ".) Это используется, чтобы убедиться, что возвращенные сведения о батарее соответствуют запрошенному аккумулятору.

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

[**\_состояние аккумулятора**](battery-status-str.md)
</dt> <dt>

[**\_состояние ожидания \_ аккумулятора**](battery-wait-status-str.md)
</dt> <dt>

[**\_ \_ сведения о запросе от аккумулятора ioctl \_**](ioctl-battery-query-information.md)
</dt> <dt>

[**\_тег запроса на батарею ioctl \_ \_**](ioctl-battery-query-tag.md)
</dt> <dt>

[**\_ \_ сведения о настройке аккумулятора ioctl \_**](ioctl-battery-set-information.md)
</dt> </dl>

 

