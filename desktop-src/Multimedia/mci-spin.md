---
title: Команда MCI_SPIN (Ммсистем. h)
description: Команда MCI \_ Spin запускает устройство. Устройства видеодиск распознают эту команду.
ms.assetid: 9e491455-d06d-44c6-8aca-6360384ec266
keywords:
- команда MCI_SPIN Windows мультимедиа
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
ms.openlocfilehash: 41457cbd04de7ffc85248912224819f9c7549c8aebd34d60c4a7efcd70bbcada
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118374596"
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

## <a name="remarks"></a>Remarks

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
| Заголовок<br/>                   | <dl> <dt>ммсистем. h (включает Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[Команды MCI](mci-commands.md)
</dt> </dl>

 

