---
title: Команда приостановки
description: Команда Pause приостанавливает воспроизведение или запись.
ms.assetid: 8fa1a40d-fdb1-4c9f-a8db-9dd6a0d83b87
keywords:
- Приостановка команды мультимедиа Windows
topic_type:
- apiref
api_name:
- pause
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25957defa4db514ce84f2e013dcc3751e21779b8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892746"
---
# <a name="pause-command"></a>Команда приостановки

Команда Pause приостанавливает воспроизведение или запись. Большинство драйверов сохранены в текущей позиции и в конечном итоге возобновляют воспроизведение или запись в этой позиции. Эта команда распознает аудио компакт-диск, цифровое видео, устройство MIDI Sequencer, ВИДЕОМАГНИТОФОН, видеодиск и волна-аудиоустройства.

Чтобы отправить эту команду, вызовите функцию [**mciSendString**](/previous-versions//dd757161(v=vs.85)) с заданным параметром *лпсзкомманд* , как показано ниже.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("pause %s %s"), 
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

## <a name="remarks"></a>Комментарии

При использовании драйверов МЦИКДА, МЦИСЕК и МЦИПИОНР команда Pause работает так же, как команда [остановки](stop.md) .

## <a name="examples"></a>Примеры

Следующая команда приостанавливает работу устройства "мисаунд".

``` syntax
pause mysound
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

[stop](stop.md)
</dt> </dl>

 

