---
title: Команда Step
description: Команда Step выполняет шаги по воспроизведению одного или нескольких кадров вперед или назад. Действие по умолчанию — шаг вперед одного кадра. Это команда распознает устройства Digital-Video, ВИДЕОМАГНИТОФОН и Кав-Format видеодиск.
ms.assetid: 6017ace5-cde9-42a0-bb2f-f85d7847adc5
keywords:
- Пошаговая команда мультимедиа Windows
topic_type:
- apiref
api_name:
- step
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6203d0b2d5dea401e8197e1261946955cd28618a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490476"
---
# <a name="step-command"></a>Команда Step

Команда Step выполняет шаги по воспроизведению одного или нескольких кадров вперед или назад. Действие по умолчанию — шаг вперед одного кадра. Это команда распознает устройства Digital-Video, ВИДЕОМАГНИТОФОН и Кав-Format видеодиск.

Чтобы отправить эту команду, вызовите функцию [**mciSendString**](/previous-versions//dd757161(v=vs.85)) с заданным параметром *лпсзкомманд* , как показано ниже.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("step %s %s %s"), 
  lpszDeviceID, 
  lpszStepFlags, 
  lpszFlags
); 
```

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*лпсздевицеид*
</dt> <dd>

Идентификатор устройства MCI. Этот идентификатор или псевдоним назначается при открытии устройства.

</dd> <dt>

<span id="lpszStepFlags"></span><span id="lpszstepflags"></span><span id="LPSZSTEPFLAGS"></span>*лпсзстепфлагс*
</dt> <dd>

Один или оба следующих флага.



| Значение       | Значение                                                                                                                  |
|-------------|--------------------------------------------------------------------------------------------------------------------------|
| по *кадрам* | Указывает число кадров для шага. Если указано отрицательное значение *frames* , нельзя указать флаг "Reverse". |
| reverse     | Шаг между кадрами в обратную.                                                                                              |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*лпсзфлагс*
</dt> <dd>

Может иметь значение "Wait", "notify" или и то, и другое. Для устройств с цифровыми видео и ВИДЕОМАГНИТОФОНА можно также указать "Test". Дополнительные сведения об этих флагах см. [в разделе Флаги ожидания, уведомления и проверки](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает нуль в случае успеха или ошибку в противном случае.

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

 

