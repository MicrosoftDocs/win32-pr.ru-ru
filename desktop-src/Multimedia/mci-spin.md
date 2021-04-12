---
title: Команда MCI_SPIN (Ммсистем. h)
description: Команда MCI \_ Spin запускает устройство. Устройства видеодиск распознают эту команду.
ms.assetid: 9e491455-d06d-44c6-8aca-6360384ec266
keywords:
- MCI_SPIN команды мультимедиа Windows
topic_type:
- apiref
api_name:
- MCI_SPIN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0b154d9a2f54248ac6174e71a24d4afe74918d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415349"
---
# <a name="mci_spin-command"></a>\_Команда MCI Spin

Команда MCI \_ Spin запускает устройство. Устройства видеодиск распознают эту команду.

Чтобы отправить эту команду, вызовите функцию [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) со следующими параметрами.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SPIN, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpSpin
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

\_Ожидание с уведомлением MCI или MCI \_ . Дополнительные сведения об этих флагах см. [в разделе Флаги ожидания, уведомления и проверки](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpSpin"></span><span id="lpspin"></span><span id="LPSPIN"></span>*лпспин*
</dt> <dd>

Указатель на [**общую структуру \_ \_ пармс MCI**](mci-generic-parms.md) . (Устройства с расширенными наборами команд могут заменить эту структуру структурой, зависящей от устройства.)

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает нуль в случае успеха или ошибку в противном случае.

## <a name="remarks"></a>Комментарии

Следующие дополнительные флаги применяются к устройствам видеодиск:

<dl> <dt>

<span id="MCI_VD_SPIN_DOWN"></span><span id="mci_vd_spin_down"></span>\_Счетчик VD \_ MCI \_
</dt> <dd>

Останавливает вращение диска.

</dd> <dt>

<span id="MCI_VD_SPIN_UP"></span><span id="mci_vd_spin_up"></span>\_регулятор MCI \_ VD \_
</dt> <dd>

Начинает вращение диска.

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

 

