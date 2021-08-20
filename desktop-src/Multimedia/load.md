---
title: Команда Load
description: Команда Load загружает файл в формате, характерном для устройства. Эта команда распознает цифровые видеоролики и устройства наложения видео.
ms.assetid: ae7bfe92-7957-4756-a408-e3ab60dd9aa4
keywords:
- загрузка команды Windows мультимедиа
topic_type:
- apiref
api_name:
- load
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c66822de727ea45e93839c710dae19739cba8adaac8b571846c1fa23ef0083c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118139359"
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

## <a name="remarks"></a>Remarks

Устройство "видбоард" отправляет сообщение с уведомлением о завершении загрузки.

## <a name="examples"></a>Примеры

Следующая команда загружает файл на устройство "видбоард".

``` syntax
load vidboard c:\vid\fish.vid notify
```

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/> |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>       |



## <a name="see-also"></a>См. также

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[Строки команд MCI](mci-command-strings.md)
</dt> </dl>

 

