---
title: THEME. playSound
description: Метод playSound воспроизводит указанный звуковой файл.
ms.assetid: 42675a66-0139-4e74-9abe-1b42017fc6fe
keywords:
- Проигрыватель Windows Media THEME. playSound
topic_type:
- apiref
api_name:
- THEME.playSound
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8ceb30e5c47632a1358262019124fceae056294d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105688873"
---
# <a name="themeplaysound"></a>THEME. playSound

Метод **PlaySound** воспроизводит указанный звуковой файл.

``` syntax
        theme.playSound(soundFile)
```

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="soundFile"></span><span id="soundfile"></span><span id="SOUNDFILE"></span>*soundFile*
</dt> <dd>

**Строка** , указывающая имя звукового файла для воспроизведения.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Комментарии

Этот метод позволяет добавлять звуковые эффекты к обложке, например при нажатии кнопок. Звук воспроизводится операционной системой напрямую, а не проигрывателем Windows Media Player. Это означает, что звук нельзя контролировать с помощью параметров и методов проигрывателя Windows Media, но его можно воспроизводить, пока проигрыватель Windows Media воспроизводит другой файл цифрового мультимедиа.

Этот метод поддерживает только файлы WAV.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media 9 Series или более поздней версии<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Элемент THEME**](theme-element.md)
</dt> </dl>

 

 





