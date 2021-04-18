---
description: Декодер Windows Media Audio Voice декодирует потоки, закодированные кодировщиком Windows Media Audio Voice.
ms.assetid: 8bb5c8bd-949f-4faa-b679-8854f78076a4
title: Декодер Windows Media Audio Voice (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4565a511f2816d2914ec96f3ae89f3af5dd19016
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694890"
---
# <a name="windows-media-audio-voice-decoder"></a>Декодер Windows Media Audio Voice

Декодер Windows Media Audio Voice декодирует потоки, закодированные [**кодировщиком Windows Media Audio Voice**](windowsmediaaudiovoiceencoder.md).

## <a name="class-identifier"></a>Идентификатор класса

Идентификатор класса (CLSID) для декодера Windows Media Audio Voice представлен константой **CLSID \_ квмспдекмедиаобжект**. Вы можете создать экземпляр декодера голоса, вызвав **CoCreateInstance**.

## <a name="input-formats"></a>Форматы входных данных

Содержимое в кодировке Windows Media Audio Voice определяется тегом формата 0x00.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|-----------------------------------------------------------------------------------------|
| Клиент<br/> | Windows XP, Windows Vista или Windows 7<br/>                                       |
| Header<br/> | <dl> <dt>Вмкодекдсп. h</dt> </dl> |
| DLL<br/>    | <dl> <dt>Wmspdmod.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Объекты кодека](codecobjects.md)
</dt> <dt>

[Использование кодека Windows Media Audio Voice](usingthewindowsmediaaudio9voicecodec.md)
</dt> <dt>

[Кодировщик Windows Media Audio Voice](windowsmediaaudiovoiceencoder.md)
</dt> </dl>

 

 




