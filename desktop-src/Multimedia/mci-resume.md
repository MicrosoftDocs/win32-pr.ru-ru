---
title: Команда MCI_RESUME (Ммсистем. h)
description: Команда MCI \_ Resume запускает приостановленное устройство для возобновления приостановленной операции.
ms.assetid: 2df712c1-5005-4e89-a439-a651076bbb73
keywords:
- команда MCI_RESUME Windows мультимедиа
topic_type:
- apiref
api_name:
- MCI_RESUME
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4872162e4f4913d7165d9ec69e6cc1164b3be40919facacbfd1a94d569a46c89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120038344"
---
# <a name="mci_resume-command"></a>\_Команда возобновления работы с MCI

Команда MCI \_ Resume запускает приостановленное устройство для возобновления приостановленной операции. Эта команда распознает цифровые видеоролики, видеомагнитофоны и звуковые устройства аудио-видео. Хотя аудио компакт-диск, программа MIDI Sequencer и устройства видеодиск также распознают эту команду, драйверы устройств МЦИКДА, МЦИСЕК и МЦИПИОНР не поддерживают эти команды.

Чтобы отправить эту команду, вызовите функцию [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) со следующими параметрами.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_RESUME, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpResume
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

\_Уведомление MCI, \_ Ожидание MCI или, для устройств цифрового видео и видеомагнитофона, тест MCI \_ . Дополнительные сведения об этих флагах см. [в разделе Флаги ожидания, уведомления и проверки](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpResume"></span><span id="lpresume"></span><span id="LPRESUME"></span>*лпресуме*
</dt> <dd>

Указатель на [**общую структуру \_ \_ пармс MCI**](mci-generic-parms.md) . (Устройства с расширенными наборами команд могут заменить эту структуру структурой, зависящей от устройства.)

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает нуль в случае успеха или ошибку в противном случае.

## <a name="remarks"></a>Remarks

Эта команда возобновляет воспроизведение и запись, не изменяя текущий набор [ \_ записей](mci-record.md)с помощью [MCI \_ Play](mci-play.md) или MCI.

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

 

