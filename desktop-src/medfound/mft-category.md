---
description: Следующие идентификаторы GUID определяют категории для Media Foundation преобразований (МФТС). Эти категории используются для регистрации и перечисления МФТС.
ms.assetid: eca3ae3b-e40a-407d-986c-d0a85b891f52
title: MFT_CATEGORY (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb7bc74054ad9f201b1f2ca53b526826d34c510d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898733"
---
# <a name="mft_category"></a>\_Категория MFT

Следующие идентификаторы GUID определяют категории для Media Foundation преобразований (МФТС). Эти категории используются для регистрации и перечисления МФТС.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Константа</th>
<th style="text-align: left;">Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="MFT_CATEGORY_AUDIO_DECODER"></span><span id="mft_category_audio_decoder"></span><dl> <dt><strong>MFT_CATEGORY_AUDIO_DECODER</strong></dt> </dl></td>
<td style="text-align: left;">Звуковые декодеры.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="MFT_CATEGORY_AUDIO_EFFECT"></span><span id="mft_category_audio_effect"></span><dl> <dt><strong>MFT_CATEGORY_AUDIO_EFFECT</strong></dt> </dl></td>
<td style="text-align: left;">Звуковые эффекты.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="MFT_CATEGORY_AUDIO_ENCODER"></span><span id="mft_category_audio_encoder"></span><dl> <dt><strong>MFT_CATEGORY_AUDIO_ENCODER</strong></dt> </dl></td>
<td style="text-align: left;">Звуковые кодировщики.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="MFT_CATEGORY_DEMULTIPLEXER"></span><span id="mft_category_demultiplexer"></span><dl> <dt><strong>MFT_CATEGORY_DEMULTIPLEXER</strong></dt> </dl></td>
<td style="text-align: left;">Демультиплексоры.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="MFT_CATEGORY_MULTIPLEXER"></span><span id="mft_category_multiplexer"></span><dl> <dt><strong>MFT_CATEGORY_MULTIPLEXER</strong></dt> </dl></td>
<td style="text-align: left;">Мультиплексоры.<br/>
<blockquote>
[!Note]<br />
В Windows Vista конвейер Media Foundation не поддерживает МФТС с более чем одним входом. В Windows 7 поддерживаются множественные входные МФТС.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="MFT_CATEGORY_OTHER"></span><span id="mft_category_other"></span><dl> <dt><strong>MFT_CATEGORY_OTHER</strong></dt> </dl></td>
<td style="text-align: left;">Прочие МФТС.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="MFT_CATEGORY_VIDEO_DECODER"></span><span id="mft_category_video_decoder"></span><dl> <dt><strong>MFT_CATEGORY_VIDEO_DECODER</strong></dt> </dl></td>
<td style="text-align: left;">Видеодекодеры.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="MFT_CATEGORY_VIDEO_EFFECT"></span><span id="mft_category_video_effect"></span><dl> <dt><strong>MFT_CATEGORY_VIDEO_EFFECT</strong></dt> </dl></td>
<td style="text-align: left;">Видеоэффекты.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="MFT_CATEGORY_VIDEO_RENDERER_EFFECT"></span><span id="mft_category_video_renderer_effect"></span><dl> <dt><strong>MFT_CATEGORY_VIDEO_RENDERER_EFFECT</strong></dt> </dl></td>
<td style="text-align: left;">Эффекты модуля подготовки видео.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="MFT_CATEGORY_VIDEO_ENCODER"></span><span id="mft_category_video_encoder"></span><dl> <dt><strong>MFT_CATEGORY_VIDEO_ENCODER</strong></dt> </dl></td>
<td style="text-align: left;">Видеокодировщики.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="MFT_CATEGORY_VIDEO_PROCESSOR"></span><span id="mft_category_video_processor"></span><dl> <dt><strong>MFT_CATEGORY_VIDEO_PROCESSOR</strong></dt> </dl></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
Впервые появился в Windows 7.
</blockquote>
<br/> Обработчики видео. <br/> Эта категория ограничена МФТС, которая выполняет преобразования формата в несжатом видео, включая преобразования цветового пространства. Для видеоэффектов, изменяющих внешний вид изображения (например, эффект размытия или преобразование цветов в оттенки серого), используйте категорию <strong>MFT_CATEGORY_VIDEO_EFFECT</strong> .<br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                     |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                               |
| Header<br/>                   | <dl> <dt>Мфапи. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Константы Media Foundation](media-foundation-constants.md)
</dt> <dt>

[Преобразования Media Foundation](media-foundation-transforms.md)
</dt> <dt>

[**мфтенум**](/windows/desktop/api/mfapi/nf-mfapi-mftenum)
</dt> <dt>

[**мфтенумекс**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex)
</dt> <dt>

[**мфтрегистер**](/windows/desktop/api/mfapi/nf-mfapi-mftregister)
</dt> </dl>

 

 




