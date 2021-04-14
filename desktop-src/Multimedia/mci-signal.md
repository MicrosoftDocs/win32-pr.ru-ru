---
title: Команда MCI_SIGNAL (Ммсистем. h)
description: Команда MCI \_ Signal задает указанную точку в рабочей области. Устройство Digital-Video распознает эту команду. МЦИАВИ поддерживает только один активный сигнал за раз.
ms.assetid: 32ca21a0-e2df-47f1-8e13-67c9d8f149db
keywords:
- MCI_SIGNAL команды мультимедиа Windows
topic_type:
- apiref
api_name:
- MCI_SIGNAL
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 711238d73ee40f5809f15a2d6df93183fb17bf67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415352"
---
# <a name="mci_signal-command"></a>Сигнал MCI, \_ команда

Команда MCI \_ Signal задает указанную точку в рабочей области. Устройство Digital-Video распознает эту команду. МЦИАВИ поддерживает только один активный сигнал за раз.

Чтобы отправить эту команду, вызовите функцию [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) со следующими параметрами.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SIGNAL, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_SIGNAL_PARMS) lpSignal
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

<span id="lpSignal"></span><span id="lpsignal"></span><span id="LPSIGNAL"></span>*лпсигнал*
</dt> <dd>

Указатель на структуру [**\_ \_ \_ пармс сигнала MCI ДГВ**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_signal_parms) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает нуль в случае успеха или ошибку в противном случае.

## <a name="remarks"></a>Комментарии

Окно, дескриптор которого вы указали в элементе **двкаллбакк** структуры [**\_ \_ \_ пармс сигнала MCI ДГВ**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_signal_parms) , получает сообщение mm \_ мЦисигнал.

Следующие флаги применяются к устройствам цифрового видео:

<dl> <dt>

<span id="MCI_DGV_SIGNAL_AT"></span><span id="mci_dgv_signal_at"></span>\_сигнал ДГВ \_ MCI \_ в
</dt> <dd>

В элемент **двпоситион** структуры, идентифицируемой *лпсигнал*, включается сигнальное состояние.

</dd> <dt>

<span id="MCI_DGV_SIGNAL_CANCEL"></span><span id="mci_dgv_signal_cancel"></span>\_ \_ Отмена сигнала ДГВ \_ MCI
</dt> <dd>

Удаляет значение сигнала, указанное в значении, связанном с \_ ДГВ \_ сигнала MCI \_ усервал.

</dd> <dt>

<span id="MCI_DGV_SIGNAL_EVERY"></span><span id="mci_dgv_signal_every"></span>\_сигнал ДГВ \_ MCI \_ каждые
</dt> <dd>

Значение сигнального периода включено в элемент **двпериод** структуры, идентифицируемой *лпсигнал*.

</dd> <dt>

<span id="MCI_DGV_SIGNAL_POSITION"></span><span id="mci_dgv_signal_position"></span>\_ \_ Расположение сигнала ДГВ \_ MCI
</dt> <dd>

Устройство будет отправит значение расположения с сообщением Windows вместо указанного пользователем значения.

</dd> <dt>

<span id="MCI_DGV_SIGNAL_USERVAL"></span><span id="mci_dgv_signal_userval"></span>\_ \_ УСЕРВАЛ сигнала MCI \_ ДГВ
</dt> <dd>

Значение типа данных включается в элемент **двусерпарм** структуры, идентифицируемой *лпсигнал*. Значение данных, связанное с этим запросом, возвращается в виде сообщения Windows.

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

 

