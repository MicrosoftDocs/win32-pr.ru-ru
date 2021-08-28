---
description: Следующие идентификаторы GUID определяют категории для Media Foundation преобразований (МФТС). Эти категории используются для регистрации и перечисления МФТС.
ms.assetid: eca3ae3b-e40a-407d-986c-d0a85b891f52
title: MFT_CATEGORY (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12a65386561f18c105fde47d885ca97858131ecb
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475560"
---
# <a name="mft_category"></a>\_Категория MFT

Следующие идентификаторы GUID определяют категории для Media Foundation преобразований (МФТС). Эти категории используются для регистрации и перечисления МФТС.




| Константа | Описание | 
|----------|-------------|
| <span id="MFT_CATEGORY_AUDIO_DECODER"></span><span id="mft_category_audio_decoder"></span><dl><dt><strong>MFT_CATEGORY_AUDIO_DECODER</strong></dt></dl> | Звуковые декодеры.<br /> | 
| <span id="MFT_CATEGORY_AUDIO_EFFECT"></span><span id="mft_category_audio_effect"></span><dl><dt><strong>MFT_CATEGORY_AUDIO_EFFECT</strong></dt></dl> | Звуковые эффекты.<br /> | 
| <span id="MFT_CATEGORY_AUDIO_ENCODER"></span><span id="mft_category_audio_encoder"></span><dl><dt><strong>MFT_CATEGORY_AUDIO_ENCODER</strong></dt></dl> | Звуковые кодировщики.<br /> | 
| <span id="MFT_CATEGORY_DEMULTIPLEXER"></span><span id="mft_category_demultiplexer"></span><dl><dt><strong>MFT_CATEGORY_DEMULTIPLEXER</strong></dt></dl> | Демультиплексоры.<br /> | 
| <span id="MFT_CATEGORY_MULTIPLEXER"></span><span id="mft_category_multiplexer"></span><dl><dt><strong>MFT_CATEGORY_MULTIPLEXER</strong></dt></dl> | Мультиплексоры.<br /><blockquote>[!Note]<br />в Windows Vista конвейер Media Foundation не поддерживает мфтс с более чем одним входом. в Windows 7 поддерживаются множественные входные мфтс.</blockquote><br /><br /> | 
| <span id="MFT_CATEGORY_OTHER"></span><span id="mft_category_other"></span><dl><dt><strong>MFT_CATEGORY_OTHER</strong></dt></dl> | Прочие МФТС.<br /> | 
| <span id="MFT_CATEGORY_VIDEO_DECODER"></span><span id="mft_category_video_decoder"></span><dl><dt><strong>MFT_CATEGORY_VIDEO_DECODER</strong></dt></dl> | Видеодекодеры.<br /> | 
| <span id="MFT_CATEGORY_VIDEO_EFFECT"></span><span id="mft_category_video_effect"></span><dl><dt><strong>MFT_CATEGORY_VIDEO_EFFECT</strong></dt></dl> | Видеоэффекты.<br /> | 
| <span id="MFT_CATEGORY_VIDEO_RENDERER_EFFECT"></span><span id="mft_category_video_renderer_effect"></span><dl><dt><strong>MFT_CATEGORY_VIDEO_RENDERER_EFFECT</strong></dt></dl> | Эффекты модуля подготовки видео.<br /> | 
| <span id="MFT_CATEGORY_VIDEO_ENCODER"></span><span id="mft_category_video_encoder"></span><dl><dt><strong>MFT_CATEGORY_VIDEO_ENCODER</strong></dt></dl> | Видеокодировщики.<br /> | 
| <span id="MFT_CATEGORY_VIDEO_PROCESSOR"></span><span id="mft_category_video_processor"></span><dl><dt><strong>MFT_CATEGORY_VIDEO_PROCESSOR</strong></dt></dl> | <blockquote>[!Note]<br />появилось в Windows 7.</blockquote><br /> Обработчики видео. <br /> Эта категория ограничена МФТС, которая выполняет преобразования формата в несжатом видео, включая преобразования цветового пространства. Для видеоэффектов, изменяющих внешний вид изображения (например, эффект размытия или преобразование цветов в оттенки серого), используйте категорию <strong>MFT_CATEGORY_VIDEO_EFFECT</strong> .<br /> | 




## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                     |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                               |
| Заголовок<br/>                   | <dl> <dt>Мфапи. h</dt> </dl> |



## <a name="see-also"></a>См. также

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

 

 




