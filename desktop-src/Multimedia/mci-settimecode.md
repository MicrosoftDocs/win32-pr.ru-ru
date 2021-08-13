---
title: Команда MCI_SETTIMECODE (Ммсистем. h)
description: Команда MCI \_ сеттимекоде включает или отключает запись времени для видеомагнитофона. Устройства ВИДЕОМАГНИТОФОНА распознают эту команду.
ms.assetid: b014fbe0-de97-4540-a5fe-b22d157361f7
keywords:
- команда MCI_SETTIMECODE Windows мультимедиа
topic_type:
- apiref
api_name:
- MCI_SETTIMECODE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f75a1722b1e1e26ece0bc7f3eac705bdd290f770a659cfebe46b603859a3918
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119430464"
---
# <a name="mci_settimecode-command"></a>\_Команда MCI сеттимекоде

Команда MCI \_ сеттимекоде включает или отключает запись времени для видеомагнитофона. Устройства ВИДЕОМАГНИТОФОНА распознают эту команду.

Чтобы отправить эту команду, вызовите функцию [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) со следующими параметрами.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SETTIMECODE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpSetTimeCode
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

<span id="lpSetTimeCode"></span><span id="lpsettimecode"></span><span id="LPSETTIMECODE"></span>*лпсеттимекоде*
</dt> <dd>

Указатель на [**общую структуру \_ \_ пармс MCI**](mci-generic-parms.md) . (Устройства с расширенными наборами команд могут заменить эту структуру структурой, зависящей от устройства.)

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает нуль в случае успеха или ошибку в противном случае.

## <a name="remarks"></a>Remarks

К устройствам ВИДЕОМАГНИТОФОНА применяется следующий дополнительный флаг:

<dl> <dt>

<span id="MCI_VCR_SETTIMECODE_RECORD"></span><span id="mci_vcr_settimecode_record"></span>\_ \_ запись СЕТТИМЕКОДЕ видеомагнитофона \_ MCI
</dt> <dd>

Задает значение ON или OFF для записи времени. Этот флаг используется в сочетании с одним из следующих дополнительных флагов:

</dd> <dt>

<span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI \_ задан \_ на
</dt> <dd>

Запись времени по времени в.

</dd> <dt>

<span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>MCI \_ установлен \_
</dt> <dd>

Запись времени начала.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



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

 

