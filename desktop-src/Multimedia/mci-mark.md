---
title: Команда MCI_MARK (Ммсистем. h)
description: Команда MCI \_ Mark записывает или стирает метки, которые можно использовать с \_ командой MCI Seek для высокоскоростных поисков. Устройства ВИДЕОМАГНИТОФОНА распознают эту команду.
ms.assetid: 69b17e5b-99a1-4fb9-bc0e-30e772c1f11f
keywords:
- MCI_MARK команды мультимедиа Windows
topic_type:
- apiref
api_name:
- MCI_MARK
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ddc80decb4559659efb29132f17f18459c334fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071315"
---
# <a name="mci_mark-command"></a>\_Команда ДЕЛЕНИЯ MCI

Команда MCI \_ Mark записывает или стирает метки, которые можно использовать с командой [MCI \_ Seek](mci-seek.md) для высокоскоростных поисков. Устройства ВИДЕОМАГНИТОФОНА распознают эту команду.

Чтобы отправить эту команду, вызовите функцию [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) со следующими параметрами.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_MARK, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpMark
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

<span id="lpMark"></span><span id="lpmark"></span><span id="LPMARK"></span>*лпмарк*
</dt> <dd>

Указатель на [**общую структуру \_ \_ пармс MCI**](mci-generic-parms.md) . (Устройства с расширенными наборами команд могут заменить эту структуру структурой, зависящей от устройства.)

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает нуль в случае успеха или ошибку в противном случае.

## <a name="remarks"></a>Комментарии

Следующие дополнительные флаги применяются к устройствам ВИДЕОМАГНИТОФОНА:

<dl> <dt>

<span id="MCI_VCR_MARK_ERASE"></span><span id="mci_vcr_mark_erase"></span>\_ \_ стирание метки видеомагнитофона \_ видеомагнитофон
</dt> <dd>

Удаляет метку в текущей позиции, если она существует.

</dd> <dt>

<span id="MCI_VCR_MARK_WRITE"></span><span id="mci_vcr_mark_write"></span>\_ \_ запись маркера видеомагнитофона MCI \_
</dt> <dd>

Записывает метку в текущей позиции.

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

 

