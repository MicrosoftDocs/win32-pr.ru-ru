---
description: кодировщик Windows Media Audio voice оптимизирован для кодирования человеческого голоса при высоком коэффициенте сжатия. Это предпочтительный кодировщик для потоков, состоящих в основном на произнесенных словах.
ms.assetid: b3cfa845-4fe1-405f-88e5-4555398639ef
title: Windows Кодировщик Media Audio Voice (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c107e4e09309ff0ed56e899d3ec2cd0c9d372261b48231b4530ed3222ee3a68
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119462433"
---
# <a name="windows-media-audio-voice-encoder"></a>Windows Кодировщик Media Audio Voice

кодировщик Windows Media Audio voice оптимизирован для кодирования человеческого голоса при высоком коэффициенте сжатия. Это предпочтительный кодировщик для потоков, состоящих в основном на произнесенных словах.

## <a name="class-identifier"></a>Идентификатор класса

идентификатор класса (CLSID) для кодировщика Windows Media Audio Voice представлен константой **CLSID \_ CWMSPEncMediaObject2**. Экземпляр речевого кодировщика можно создать, вызвав **CoCreateInstance**.

## <a name="output-formats"></a>Форматы выходных данных

Windows Содержимое, закодированное в Media Audio Voice, определяется тегом формата 0x00.

## <a name="encoder-properties"></a>Свойства кодировщика

кодировщик Windows Media Audio Voice поддерживает следующие свойства.



<table>
<thead>
<tr class="header">
<th>Свойство</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="mfpkey-wmavoice-enc-bufferwindowproperty.md">MFPKEY_WMAVOICE_ENC_BufferWindow</a></td>
<td>Указывает окно буфера (в миллисекундах), используемое для речевого кодека.<br/> <dl> Windows XP и более поздних версий.<br />
Доступный только на запись.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-wmavoice-enc-decoderdelayproperty.md">MFPKEY_WMAVOICE_ENC_DecoderDelay</a></td>
<td>Указывает задержку кодировщика в единицах пакетов.<br/> <dl> Windows XP и более поздних версий.<br />
Доступный только на запись.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-wmavoice-enc-edlproperty.md">MFPKEY_WMAVOICE_ENC_EDL</a></td>
<td>Указывает фрагменты содержимого, которые должны быть закодированы голосовым кодеком в качестве музыки.<br/> <dl> Windows XP и более поздних версий.<br />
Read/write.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-wmavoice-enc-musicspeechclassmodeproperty.md">MFPKEY_WMAVOICE_ENC_MusicSpeechClassMode</a></td>
<td>Задает режим работы с голосовым кодеком.<br/> <dl> Windows XP и более поздних версий.<br />
Read/write.<br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|-----------------------------------------------------------------------------------------|
| Клиент<br/> | Windows XP, Windows Vista или Windows 7<br/>                                       |
| Заголовок<br/> | <dl> <dt>Вмкодекдсп. h</dt> </dl> |
| DLL<br/>    | <dl> <dt>Wmspdmoe.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Объекты кодека](codecobjects.md)
</dt> <dt>

[использование видеокодека Windows Media Audio](usingthewindowsmediaaudio9voicecodec.md)
</dt> </dl>

 

 




