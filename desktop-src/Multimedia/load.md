---
title: Команда Load
description: Команда Load загружает файл в формате, характерном для устройства. Эта команда распознает цифровые видеоролики и устройства наложения видео.
ms.assetid: ae7bfe92-7957-4756-a408-e3ab60dd9aa4
keywords:
- Загрузка команды Windows мультимедиа
topic_type:
- apiref
api_name:
- load
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b199a6d3aea8a2697217eb75176c24b2b0bc2e2a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803022"
---
# <a name="load-command"></a>Команда Load

Команда Load загружает файл в формате, характерном для устройства. Эта команда распознает цифровые видеоролики и устройства наложения видео.

Чтобы отправить эту команду, вызовите функцию [**mciSendString**](/previous-versions//dd757161(v=vs.85)) с заданным параметром *лпсзкомманд* , как показано ниже.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("load %s %s %s"), 
  lpszDeviceID, 
  lpszFilePos, 
  lpszFlags
); 
```

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*лпсздевицеид*
</dt> <dd>

Идентификатор устройства MCI. Этот идентификатор или псевдоним назначается при открытии устройства.

</dd> <dt>

<span id="lpszFilePos"></span><span id="lpszfilepos"></span><span id="LPSZFILEPOS"></span>*лпсзфилепос*
</dt> <dd>

Путь и имя файла для загрузки. Для устройств с наложением видео это также может включать целевой прямоугольник для данных. Чтобы указать целевой прямоугольник, укажите "at", за которым следует **x1 Y1 x2 Y2**, где **x1 Y1** укажите верхний левый угол прямоугольника, а **x2 Y2** — ширину и высоту. Прямоугольник задается относительно источника видеобуфера.

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*лпсзфлагс*
</dt> <dd>

Может иметь значение "Wait", "notify" или и то, и другое. Для устройств Digital-Video также можно указать "Test". Дополнительные сведения об этих флагах см. [в разделе Флаги ожидания, уведомления и проверки](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает нуль в случае успеха или ошибку в противном случае.

## <a name="remarks"></a>Комментарии

Устройство "видбоард" отправляет сообщение с уведомлением о завершении загрузки.

## <a name="examples"></a>Примеры

Следующая команда загружает файл на устройство "видбоард".

``` syntax
load vidboard c:\vid\fish.vid notify
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
</dt> </dl>

 

