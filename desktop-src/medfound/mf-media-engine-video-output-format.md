---
description: Задает формат целевого объекта подготовки к просмотру для механизма мультимедиа.
ms.assetid: 70FFDD44-9FDE-4D86-AD65-60019AC4A2BC
title: Атрибут MF_MEDIA_ENGINE_VIDEO_OUTPUT_FORMAT (Мфмедиаенгине. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eaa0dab3c3ea1c9ce23d767458df0b68a9b3c787f80ca1af786061536343a356
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973733"
---
# <a name="mf_media_engine_video_output_format-attribute"></a>\_ \_ \_ \_ Атрибут формата вывода видео для ОБРАБОТЧИКа передачи мультимедиа MF \_

Задает формат целевого объекта подготовки к просмотру для механизма мультимедиа.

## <a name="data-type"></a>Тип данных

**DXGI \_ ФОРМАТ** хранится как **UINT32**

## <a name="remarks"></a>Remarks

Установите этот атрибут при создании подсистемы мультимедиа в режиме "Frame-Server". Дополнительные сведения см. в разделе [**имфмедиаенгинеклассфактори:: CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance). Значением атрибута является значение [ \_ формата DXGI](../direct3d9/d3dformat.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ приложения UWP для классических приложений \|\]<br/>                                          |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ приложения UWP для классических приложений \|\]<br/>                                |
| Заголовок<br/>                   | <dl> <dt>Мфмедиаенгине. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
