---
description: Кодировщик Windows Media Audio Voice оптимизирован для кодирования человеческого голоса при высоком коэффициенте сжатия. Это предпочтительный кодировщик для потоков, состоящих в основном на произнесенных словах.
ms.assetid: b3cfa845-4fe1-405f-88e5-4555398639ef
title: Кодировщик Windows Media Audio Voice (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bef79f2c3d0c48fee8ec33e08bfb9fdf21c3656b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699070"
---
# <a name="windows-media-audio-voice-encoder"></a>Кодировщик Windows Media Audio Voice

Кодировщик Windows Media Audio Voice оптимизирован для кодирования человеческого голоса при высоком коэффициенте сжатия. Это предпочтительный кодировщик для потоков, состоящих в основном на произнесенных словах.

## <a name="class-identifier"></a>Идентификатор класса

Идентификатор класса (CLSID) для кодировщика Windows Media Audio Voice представлен константой **CLSID \_ CWMSPEncMediaObject2**. Экземпляр речевого кодировщика можно создать, вызвав **CoCreateInstance**.

## <a name="output-formats"></a>Форматы выходных данных

Содержимое в кодировке Windows Media Audio Voice определяется тегом формата 0x00.

## <a name="encoder-properties"></a>Свойства кодировщика

Кодировщик Windows Media Audio Voice поддерживает следующие свойства.



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
<td>Указывает окно буфера (в миллисекундах), используемое для речевого кодека.<br/> <dl> Windows XP и более поздние версии.<br />
Доступный только на запись.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-wmavoice-enc-decoderdelayproperty.md">MFPKEY_WMAVOICE_ENC_DecoderDelay</a></td>
<td>Указывает задержку кодировщика в единицах пакетов.<br/> <dl> Windows XP и более поздние версии.<br />
Доступный только на запись.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-wmavoice-enc-edlproperty.md">MFPKEY_WMAVOICE_ENC_EDL</a></td>
<td>Указывает фрагменты содержимого, которые должны быть закодированы голосовым кодеком в качестве музыки.<br/> <dl> Windows XP и более поздние версии.<br />
Read/write.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-wmavoice-enc-musicspeechclassmodeproperty.md">MFPKEY_WMAVOICE_ENC_MusicSpeechClassMode</a></td>
<td>Задает режим работы с голосовым кодеком.<br/> <dl> Windows XP и более поздние версии.<br />
Read/write.<br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|-----------------------------------------------------------------------------------------|
| Клиент<br/> | Windows XP, Windows Vista или Windows 7<br/>                                       |
| Header<br/> | <dl> <dt>Вмкодекдсп. h</dt> </dl> |
| DLL<br/>    | <dl> <dt>Wmspdmoe.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Объекты кодека](codecobjects.md)
</dt> <dt>

[Использование кодека Windows Media Audio Voice](usingthewindowsmediaaudio9voicecodec.md)
</dt> </dl>

 

 




