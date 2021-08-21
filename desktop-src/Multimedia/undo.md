---
title: Команда "отменить"
description: Команда Undo отменяет действие, выполняемое последней успешной командой копирования, вырезания, удаления, отмены или вставки. Устройство Digital-Video распознает эту команду.
ms.assetid: 81d696a9-5288-4efd-bc76-8416dd63e694
keywords:
- команда "отменить" Windows мультимедиа
topic_type:
- apiref
api_name:
- undo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec088f893b221a80cb3fe84c191a52874a8c29f5163ad3bcdaa8e68a9a4d4d2e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119804734"
---
# <a name="undo-command"></a>Команда "отменить"

Команда Undo отменяет действие, выполняемое последней успешной командой [копирования](copy.md), [вырезания](cut.md), [удаления](delete.md), отмены или [вставки](paste.md) . Устройство Digital-Video распознает эту команду.

Чтобы отправить эту команду, вызовите функцию [**mciSendString**](/previous-versions//dd757161(v=vs.85)) с заданным параметром *лпсзкомманд* , как показано ниже.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("undo %s %s"), 
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

Может принимать значение "Wait", "notify", "Test" или их сочетание. Дополнительные сведения об этих флагах см. [в разделе Флаги ожидания, уведомления и проверки](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает нуль в случае успеха или ошибку в противном случае.

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
</dt> <dt>

[copy](copy.md)
</dt> <dt>

[бавьте](cut.md)
</dt> <dt>

[delete](delete.md)
</dt> <dt>

[вставка](paste.md)
</dt> </dl>

 

