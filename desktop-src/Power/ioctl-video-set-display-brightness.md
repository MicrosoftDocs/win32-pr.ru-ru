---
description: Задает текущие уровни подсветки AC и DC.
ms.assetid: baa77811-046d-4a07-b3df-2a31fba2d9a7
title: Код элемента управления IOCTL_VIDEO_SET_DISPLAY_BRIGHTNESS (Нтддвдео. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_VIDEO_SET_DISPLAY_BRIGHTNESS
api_type:
- HeaderDef
api_location:
- Ntddvdeo.h
ms.openlocfilehash: a0c679f352012eea66b80335bc3ad1547501dd92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998502"
---
# <a name="ioctl_video_set_display_brightness-control-code"></a>\_ \_ \_ \_ Код управления яркостью дисплея ioctl Video Set

Задает текущие уровни подсветки AC и DC.

Чтобы выполнить эту операцию, вызовите функцию [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) со следующими параметрами.


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,            // handle to device
  IOCTL_VIDEO_SET_DISPLAY_BRIGHTNESS, // dwIoControlCode
  (LPVOID) lpInBuffer,         // input buffer
  (DWORD) nInBufferSize,       // size of the input buffer
  NULL,                        // lpOutBuffer
  0,                           // nOutBufferSize 
  (LPDWORD) lpBytesReturned,   // number of bytes returned
  (LPOVERLAPPED) lpOverlapped  // OVERLAPPED structure
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

Управляющий код для операции. Это значение определяет конкретную выполняемую операцию и тип устройства, на котором она выполняется. Использовать для этой операции **\_ \_ \_ \_ яркость экрана с помощью ioctl Video Set** .

</dd> <dt>

*лпинбуффер* 
</dt> <dd>

Указатель на структуру [**\_ яркости экрана**](/previous-versions/windows/desktop/legacy/aa372686(v=vs.85)) .

</dd> <dt>

*нинбуфферсизе* 
</dt> <dd>

Размер буфера, на который указывает *лпаутбуффер*, в байтах.

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

Указатель на переменную, которая получает фактическое число байтов, возвращенных функцией в выходном буфере.

Если *лповерлаппед* имеет **значение NULL** (ноноверлаппед I/O), *лпбитесретурнед* используется внутренне и не может иметь **значение NULL**.

Если *лповерлаппед* не **равно NULL** (перекрывающиеся операции ввода-вывода), *лпбитесретурнед* может иметь **значение NULL**.

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

Значения, указанные в элементах **укакбригхтнесс** и **Укдкбригхтнесс** структуры [**\_ яркости экрана**](/previous-versions/windows/desktop/legacy/aa372686(v=vs.85)) , должны быть ранее возвращены с помощью [**\_ запроса видео \_ , \_ поддерживаемого \_ функцией ioctl**](ioctl-video-query-supported-brightness.md). Например, если поддерживаются значения 10, 20, 30, 40, 50, 60, 70, 80, 90 и 100, то при использовании значения 33 будет выдаваться ошибка.

Файл заголовка, используемый для создания приложений, включающих эту функцию, Нтддвдео. h, входит в состав пакета средств разработки драйверов Microsoft Windows (DDK). Сведения о получении DDK см. в разделе [https://www.microsoft.com/whdc/devtools/ddk/default.mspx](https://msdn.microsoft.com/windows/hardware/gg454513) .

Кроме того, этот код элемента управления можно определить следующим образом:

``` syntax
#define IOCTL_VIDEO_SET_DISPLAY_BRIGHTNESS \
  CTL_CODE(FILE_DEVICE_VIDEO, 0x127, METHOD_BUFFERED, FILE_ANY_ACCESS)
```

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista, Windows XP с пакетом обновления 1 (SP1), \[ только классические приложения\]<br/>                   |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Нтддвдео. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Интерфейс управления подсветкой](backlight-control-interface.md)
</dt> <dt>

[**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[**\_яркость экрана**](/previous-versions/windows/desktop/legacy/aa372686(v=vs.85))
</dt> <dt>

[**\_ \_ \_ яркость экрана запроса видео \_ ioctl**](ioctl-video-query-display-brightness.md)
</dt> <dt>

[**видеозапрос IOCTL — \_ \_ \_ поддерживаемая \_ яркость**](ioctl-video-query-supported-brightness.md)
</dt> </dl>

 

