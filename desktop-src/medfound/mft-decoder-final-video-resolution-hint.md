---
description: Задает окончательное разрешение вывода декодированного изображения после обработки видео.
ms.assetid: 067867D8-155C-4406-BE07-720016B2AEBC
title: Атрибут MFT_DECODER_FINAL_VIDEO_RESOLUTION_HINT (Мфтрансформ. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 847a2925f2249c741e9a45a1dcc4826a1cbe3d6bb12cda4d8017ee0fb5de0069
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973143"
---
# <a name="mft_decoder_final_video_resolution_hint-attribute"></a>\_Атрибут указания \_ конечного \_ \_ разрешения \_ экрана декодера MFT

Задает окончательное разрешение вывода декодированного изображения после обработки видео.

## <a name="data-type"></a>Тип данных

**UINT64**

## <a name="remarks"></a>Remarks

Этот атрибут поддерживается некоторыми декодерами видео. Приложение может установить этот атрибут, чтобы указать ширину и высоту изображения после обработки видео. Декодер может использовать эти сведения для оптимизации процесса декодирования, особенно в том случае, если окончательный размер изображения намного меньше, чем размер образа в машинном коде. Например, декодер может пропустить фильтр по внешнему циклу.

Верхние 32 разрядов содержат ширину, а более низкие биты 32 содержат высоту.

Чтобы задать этот атрибут, сделайте следующее:

1.  Вызовите метод [**имфтрансформ:: OutAttribute**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) в декодере, чтобы получить указатель [**имфаттрибутес**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .
2.  Вызовите [**мфсетаттрибутесизе**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributesize) , чтобы добавить атрибут.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ приложения UWP для классических приложений \|\]<br/>                                        |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                |
| Header<br/>                   | <dl> <dt>Мфтрансформ. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Атрибуты преобразования](transform-attributes.md)
</dt> </dl>

 

 




