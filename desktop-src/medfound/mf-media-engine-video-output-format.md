---
description: Задает формат целевого объекта подготовки к просмотру для механизма мультимедиа.
ms.assetid: 70FFDD44-9FDE-4D86-AD65-60019AC4A2BC
title: Атрибут MF_MEDIA_ENGINE_VIDEO_OUTPUT_FORMAT (Мфмедиаенгине. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 004025da1ad5258e5b04a3afba4a359f50f7444c
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "103820204"
---
# <a name="mf_media_engine_video_output_format-attribute"></a>\_ \_ \_ \_ Атрибут формата вывода видео для ОБРАБОТЧИКа передачи мультимедиа MF \_

Задает формат целевого объекта подготовки к просмотру для механизма мультимедиа.

## <a name="data-type"></a>Тип данных

**DXGI \_ ФОРМАТ** хранится как **UINT32**

## <a name="remarks"></a>Комментарии

Установите этот атрибут при создании подсистемы мультимедиа в режиме "Frame-Server". Дополнительные сведения см. в разделе [**имфмедиаенгинеклассфактори:: CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance). Значением атрибута является значение [ \_ формата DXGI](../direct3d9/d3dformat.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Приложения UWP для классических приложений Windows 8 \|\]<br/>                                          |
| Минимальная версия сервера<br/> | \[Приложения UWP для классических приложений Windows Server 2012 \|\]<br/>                                |
| Header<br/>                   | <dl> <dt>Мфмедиаенгине. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
