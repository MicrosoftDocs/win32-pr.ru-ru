---
title: Команда MCI_CAPTURE (Ммсистем. h)
description: '\_Команда захвата MCI захватывает содержимое буфера кадров и сохраняет его в указанном файле. Устройство Digital-Video распознает эту команду.'
ms.assetid: bdebddc5-a0a0-449e-889e-37c7d6612c60
keywords:
- MCI_CAPTURE команды мультимедиа Windows
topic_type:
- apiref
api_name:
- MCI_CAPTURE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 041954d786b007023226fb5d3febf4747c0121e2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988966"
---
# <a name="mci_capture-command"></a>\_Команда захвата MCI

\_Команда захвата MCI захватывает содержимое буфера кадров и сохраняет его в указанном файле. Устройство Digital-Video распознает эту команду.

Чтобы отправить эту команду, вызовите функцию [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) со следующими параметрами.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_CAPTURE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_CAPTURE_PARMS) lpCapture
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*вдевицеид*
</dt> <dd>

Идентификатор устройства MCI, который должен получить командное сообщение.

</dd> <dt>

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*
</dt> <dd>

\_Уведомление MCI, \_ Ожидание MCI или \_ тест MCI. Дополнительные сведения об этих флагах см. [в разделе Флаги ожидания, уведомления и проверки](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpCapture"></span><span id="lpcapture"></span><span id="LPCAPTURE"></span>*лпкаптуре*
</dt> <dd>

Указатель на структуру [**\_ \_ \_ пармс захвата ДГВ MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_capture_parmsa) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает нуль в случае успеха или ошибку в противном случае.

## <a name="remarks"></a>Комментарии

Следующие дополнительные флаги применяются к устройствам цифрового видео:

<dl> <dt>

<span id="MCI_DGV_CAPTURE_AS"></span><span id="mci_dgv_capture_as"></span>\_захват ДГВ \_ MCI \_
</dt> <dd>

Элемент **лпстрфиленаме** структуры, идентифицируемой *лпкаптуре* , содержит адрес буфера, указывающего путь назначения и имя файла. (Этот флаг является обязательным.)

</dd> <dt>

<span id="MCI_DGV_CAPTURE_AT"></span><span id="mci_dgv_capture_at"></span>\_захват ДГВ \_ MCI \_ в
</dt> <dd>

Элемент **RC** структуры, идентифицируемой *лпкаптуре* , содержит допустимый прямоугольник. Прямоугольник указывает прямоугольную область внутри буфера фрейма, которая обрезается и сохраняется на диске. Если этот параметр опущен, то в обрезанной области по умолчанию используется прямоугольник, указанный или установленный по умолчанию в предыдущей команде [MCI \_ ](mci-put.md) , которая указывает исходную область для данного экземпляра драйвера устройства.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                                |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                      |
| Заголовок<br/>                   | <dl> <dt>Ммсистем. h (включение Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[Команды MCI](mci-commands.md)
</dt> </dl>

 

