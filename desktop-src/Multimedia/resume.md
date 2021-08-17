---
title: Команда возобновления
description: Команда Resume продолжает воспроизведение или запись на устройстве, которое было приостановлено с помощью команды Pause.
ms.assetid: 0a2cdd23-8c1d-4d9e-9b63-3fdcbb13e3a2
keywords:
- команда возобновления Windows мультимедиа
topic_type:
- apiref
api_name:
- resume
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7e4a728e3ca89e2b4ddc21809830d5af3be9a2b04e004f99d5a792a9be5da01
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117801896"
---
# <a name="resume-command"></a>Команда возобновления

Команда Resume продолжает воспроизведение или запись на устройстве, которое было приостановлено с помощью команды [Pause](pause.md) . Эта команда распознает цифровые видеоролики, видеомагнитофоны и звуковые устройства аудио-видео. Хотя аудио компакт-диск, программа MIDI Sequencer и устройства видеодиск также распознают эту команду, драйверы устройств МЦИКДА, МЦИСЕК и МЦИПИОНР не поддерживают эти команды.

Чтобы отправить эту команду, вызовите функцию [**mciSendString**](/previous-versions//dd757161(v=vs.85)) с заданным параметром *лпсзкомманд* , как показано ниже.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("resume %s %s"), 
  lpszDeviceID, 
  lpszFlags
); 
```

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*лпсздевицеид*
</dt> <dd>

Идентификатор устройства MCI. Этот идентификатор или псевдоним назначается при открытии устройства.

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*лпсзфлагс*
</dt> <dd>

Может иметь значение "Wait", "notify" или и то, и другое. Для устройств с цифровыми видео и ВИДЕОМАГНИТОФОНА можно также указать "Test". Дополнительные сведения об этих флагах см. [в разделе Флаги ожидания, уведомления и проверки](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает нуль в случае успеха или ошибку в противном случае.

## <a name="examples"></a>Примеры

Следующая команда продолжит воспроизведение или запись устройства "невсаунд".

``` syntax
resume newsound
```

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/> |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>       |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[Строки команд MCI](mci-command-strings.md)
</dt> <dt>

[pause](pause.md)
</dt> </dl>

 

