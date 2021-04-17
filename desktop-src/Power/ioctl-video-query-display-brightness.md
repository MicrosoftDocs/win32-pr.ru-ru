---
description: Извлекает текущие уровни подсветки AC и DC и текущее состояние электропитания.
ms.assetid: c7b7c302-6e92-46a7-b9a6-e3f2a3e44d1b
title: Код элемента управления IOCTL_VIDEO_QUERY_DISPLAY_BRIGHTNESS (Нтддвдео. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_VIDEO_QUERY_DISPLAY_BRIGHTNESS
api_type:
- HeaderDef
api_location:
- Ntddvdeo.h
ms.openlocfilehash: 547501a28492aecfe06f63f95b0e007fc80d3d02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673806"
---
# <a name="ioctl_video_query_display_brightness-control-code"></a>\_ \_ \_ \_ Код управления яркостью экрана запроса видео ioctl

\[Этот управляющий код доступен для использования в операционных системах, указанных в разделе требования. Поддержка этого кода элемента управления была удалена в Windows Server 2008 и Windows Vista. Вместо этого используйте класс [**вмимониторбригхтнесс**](/windows/desktop/WmiCoreProv/wmimonitorbrightness) .\]

Извлекает текущие уровни подсветки AC и DC и текущее состояние электропитания.

Чтобы выполнить эту операцию, вызовите функцию [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) со следующими параметрами.


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,                // handle to device
  IOCTL_VIDEO_QUERY_DISPLAY_BRIGHTNESS,  // dwIoControlCode
  NULL,                            // lpInBuffer
  0,                               // nInBufferSize
  (LPVOID) lpOutBuffer,            // output buffer
  (DWORD) nOutBufferSize,          // size of output buffer
  (LPDWORD) lpBytesReturned,       // number of bytes returned
  (LPOVERLAPPED) lpOverlapped      // OVERLAPPED structure
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хдевице* 
</dt> <dd>

Маркер для \\ \\ . \\ ЖК-устройство. Чтобы получить маркер устройства, вызовите функцию [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) .

</dd> <dt>

*двиоконтролкоде* 
</dt> <dd>

Управляющий код для операции. Это значение определяет конкретную выполняемую операцию и тип устройства, на котором она выполняется. Используйте для этой операции **\_ \_ \_ \_ яркость экрана запроса видео ioctl** .

</dd> <dt>

*лпинбуффер* 
</dt> <dd>

Не используется в этой операции; Задайте **значение NULL**.

</dd> <dt>

*нинбуфферсизе* 
</dt> <dd>

Не используется в этой операции; присвойте ему значение 0.

</dd> <dt>

*лпаутбуффер* 
</dt> <dd>

Указатель на буфер, который получит структуру [**\_ яркости экрана**](/previous-versions/windows/desktop/legacy/aa372686(v=vs.85)) .

</dd> <dt>

*наутбуфферсизе* 
</dt> <dd>

Размер выходного буфера в байтах.

</dd> <dt>

*лпбитесретурнед* 
</dt> <dd>

Указатель на переменную, которая получает размер возвращаемых выходных данных в байтах.

Если выходной буфер слишком мал для возвращения каких-либо данных, вызов завершается ошибкой, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) возвращает код ошибки \_ недостаточный \_ Размер буфера, а возвращенное число байтов равно нулю.

Если выходной буфер слишком мал для хранения всех данных, но может содержать некоторые записи, то операционная система возвращает столько, сколько подходит, вызов завершается неудачно, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) возвращает код ошибки \_ Дополнительные \_ данные, а *лпбитесретурнед* указывает объем возвращаемых данных. Приложение должно повторно вызвать [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) с той же операцией, указав новую отправную точку.

Если *лповерлаппед* имеет **значение NULL** (ноноверлаппед I/O), *Лпбитесретурнед* не может иметь **значение NULL**.

Если *лповерлаппед* не **равно NULL** (перекрывающиеся операции ввода-вывода), *лпбитесретурнед* может иметь **значение NULL**. Если это операция с перекрытием, можно получить число байтов, возвращенных путем вызова функции [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) . Если *хдевице* связан с портом завершения ввода-вывода, можно получить число возвращаемых байтов, вызвав функцию [**жеткуеуедкомплетионстатус**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) .

</dd> <dt>

*лповерлаппед* 
</dt> <dd>

Указатель на структуру [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) .

Если *хдевице* был открыт с \_ \_ флагом File Flag OVERLAPPED, *лповерлаппед* должен указывать на допустимую структуру [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) . В этом случае операция выполняется как Перекрываемая (асинхронная) операция. Если устройство было открыто с \_ флагом File Flag \_ OVERLAPPED и *Лповерлаппед* имеет **значение NULL**, функция завершается ошибкой непредсказуемым образом.

Если *хдевице* был открыт без указания \_ \_ флага File Flag OVERLAPPED, *Лповерлаппед* игнорируется, а [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) не возвращает значение до тех пор, пока операция не будет завершена или пока не произойдет ошибка.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если операция завершается успешно, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) возвращает ненулевое значение.

Если операция завершается неудачно или ожидает выполнения, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) возвращает ноль. Дополнительные сведения об ошибке можно получить, вызвав [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Комментарии

Файл заголовка, используемый для создания приложений, включающих эту функцию, Нтддвдео. h, входит в состав пакета средств разработки драйверов Microsoft Windows (DDK). Сведения о получении DDK см. в разделе [https://www.microsoft.com/whdc/devtools/ddk/default.mspx](https://msdn.microsoft.com/windows/hardware/gg454513) .

Кроме того, этот код элемента управления можно определить следующим образом:

``` syntax
#define IOCTL_VIDEO_QUERY_DISPLAY_BRIGHTNESS \
  CTL_CODE(FILE_DEVICE_VIDEO, 0x126, METHOD_BUFFERED, FILE_ANY_ACCESS)
```

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для настольных приложений Windows XP с пакетом обновления 1 \[\]<br/>                                  |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Окончание поддержки клиента<br/>    | Windows XP с пакетом обновления 2 (SP2)<br/>                                                        |
| Поддержка конца сервера<br/>    | Windows Server 2003 R2<br/>                                                     |
| Header<br/>                   | <dl> <dt>Нтддвдео. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Интерфейс управления подсветкой](backlight-control-interface.md)
</dt> <dt>

[**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[**\_яркость экрана**](/previous-versions/windows/desktop/legacy/aa372686(v=vs.85))
</dt> <dt>

[**\_ \_ Настройка \_ яркости экрана для видео ioctl \_**](ioctl-video-set-display-brightness.md)
</dt> </dl>

 

