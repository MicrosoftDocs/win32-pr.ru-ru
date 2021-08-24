---
title: Команда MCI_SIGNAL (Ммсистем. h)
description: Команда MCI \_ Signal задает указанную точку в рабочей области. Устройство Digital-Video распознает эту команду. МЦИАВИ поддерживает только один активный сигнал за раз.
ms.assetid: 32ca21a0-e2df-47f1-8e13-67c9d8f149db
keywords:
- команда MCI_SIGNAL Windows мультимедиа
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
ms.openlocfilehash: fda7585ad63415f888f5971397df2b27c23710864ea21a8ed5e6ebce1a7c66f3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119689844"
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

## <a name="remarks"></a>Remarks

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

устройство будет отправит значение расположения с Windows сообщением вместо указанного пользователем значения.

</dd> <dt>

<span id="MCI_DGV_SIGNAL_USERVAL"></span><span id="mci_dgv_signal_userval"></span>\_ \_ УСЕРВАЛ сигнала MCI \_ ДГВ
</dt> <dd>

Значение типа данных включается в элемент **двусерпарм** структуры, идентифицируемой *лпсигнал*. значение данных, связанное с этим запросом, возвращается в виде Windows сообщения.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                                |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                      |
| Заголовок<br/>                   | <dl> <dt>ммсистем. h (включает Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[Команды MCI](mci-commands.md)
</dt> </dl>

 

