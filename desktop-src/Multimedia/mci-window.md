---
title: Команда MCI_WINDOW (Ммсистем. h)
description: '\_Команда окна MCI задает окно и характеристики для графических устройств. Эта команда распознает цифровые видеоролики и устройства наложения видео.'
ms.assetid: 8b6c4d9a-ee72-4c64-aebe-6c8153167496
keywords:
- MCI_WINDOW команды мультимедиа Windows
topic_type:
- apiref
api_name:
- MCI_WINDOW
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41b4d630dbc9dbc7403e93cd0bda3de2eef1e5cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988801"
---
# <a name="mci_window-command"></a>\_Команда окна MCI

\_Команда окна MCI задает окно и характеристики для графических устройств. Эта команда распознает цифровые видеоролики и устройства наложения видео.

Чтобы отправить эту команду, вызовите функцию [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) со следующими параметрами.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_WINDOW, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpWindow
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

\_Уведомление MCI, \_ Ожидание MCI или, для устройств с цифровыми видео, \_ тест MCI. Дополнительные сведения об этих флагах см. [в разделе Флаги ожидания, уведомления и проверки](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpWindow"></span><span id="lpwindow"></span><span id="LPWINDOW"></span>*лпвиндов*
</dt> <dd>

Указатель на [**общую структуру \_ \_ пармс MCI**](mci-generic-parms.md) . (Устройства с расширенными наборами команд могут заменить эту структуру структурой, зависящей от устройства.)

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает нуль в случае успеха или ошибку в противном случае.

## <a name="remarks"></a>Комментарии

Графические устройства должны создавать окно по умолчанию, когда устройство открыто, но не должно отображать его, пока не получит команду [MCI \_ Play](mci-play.md) . \_Команда окна MCI используется для передачи на устройство окна, созданного приложением, и для изменения характеристик экрана, определенных приложением или окном просмотра по умолчанию. Если приложение предоставляет окно просмотра, оно должно быть подготовлено к обновлению недопустимого прямоугольника в окне.

С типом устройства **дигиталвидео** используются следующие дополнительные флаги:

<dl> <dt>

<span id="MCI_DGV_WINDOW_HWND"></span><span id="mci_dgv_window_hwnd"></span>\_ \_ HWND окна MCI \_ ДГВ
</dt> <dd>

Дескриптор окна, необходимый для использования в качестве назначения, включается в элемент **HWND** структуры, идентифицируемой *лпвиндов*.

</dd> <dt>

<span id="MCI_DGV_WINDOW_STATE"></span><span id="mci_dgv_window_state"></span>\_ \_ состояние окна MCI \_ ДГВ
</dt> <dd>

Элемент **нкмдшов** структуры, идентифицируемой *лпвиндов* , содержит параметры для установки состояния окна.

</dd> <dt>

<span id="MCI_DGV_WINDOW_TEXT"></span><span id="mci_dgv_window_text"></span>\_ \_ текст окна MCI \_ ДГВ
</dt> <dd>

Элемент **лпстртекст** структуры, идентифицируемой *лпвиндов* , содержит адрес буфера, содержащего заголовок, используемый в заголовке окна.

</dd> </dl>

Для устройств с цифровыми видео параметр *лпвиндов* указывает на структуру [**\_ ДГВ \_ окна MCI \_ пармс**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_window_parmsa) .

Для типа устройства **наложения** используются следующие дополнительные флаги:

<dl> <dt>

<span id="MCI_OVLY_WINDOW_DISABLE_STRETCH"></span><span id="mci_ovly_window_disable_stretch"></span>\_окно MCI \_ овли \_ Отключить \_ растяжение
</dt> <dd>

Отключает растяжение изображения.

</dd> <dt>

<span id="MCI_OVLY_WINDOW_ENABLE_STRETCH"></span><span id="mci_ovly_window_enable_stretch"></span>\_окно MCI \_ овли \_ включить \_ растяжение
</dt> <dd>

Включает растяжение изображения.

</dd> <dt>

<span id="MCI_OVLY_WINDOW_HWND"></span><span id="mci_ovly_window_hwnd"></span>\_ \_ HWND окна MCI \_ овли
</dt> <dd>

Дескриптор окна, используемого для назначения, включается в элемент **HWND** структуры, идентифицируемой *лпвиндов*. Установите этот флаг в \_ окне MCI овли \_ Window Default, \_ чтобы вернуться в окно по умолчанию.

</dd> <dt>

<span id="MCI_OVLY_WINDOW_STATE"></span><span id="mci_ovly_window_state"></span>\_ \_ состояние окна MCI \_ овли
</dt> <dd>

Элемент **нкмдшов** структуры *лпвиндов* содержит параметры для установки состояния окна. Этот флаг эквивалентен вызову [ShowWindow](/windows/win32/api/winuser/nf-winuser-showwindow) с параметром *State* . Константы аналогичны тем, которые определены в WINDOWS. H (например, скрытие программного отображения, программное \_ \_ СВЕРНУТЬ или SW \_ шовнормал).

</dd> <dt>

<span id="MCI_OVLY_WINDOW_TEXT"></span><span id="mci_ovly_window_text"></span>\_ \_ текст окна MCI \_ овли
</dt> <dd>

Элемент **лпстртекст** структуры, идентифицируемой *лпвиндов* , содержит адрес буфера, содержащего заголовок, используемый для окна.

</dd> </dl>

Для устройств с наложением параметр *лпвиндов* указывает на структуру [**\_ овли окна MCI \_ \_ пармс**](mci-ovly-window-parms.md) .

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

 

