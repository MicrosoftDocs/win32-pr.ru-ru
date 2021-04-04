---
description: Задает маркер для окна воспроизведения видео для механизма мультимедиа.
ms.assetid: 63889D81-12C5-47C1-B52A-6358E68830C3
title: Атрибут MF_MEDIA_ENGINE_PLAYBACK_HWND (Мфмедиаенгине. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c6a9d38d40b04b32244f48289d3334199a7e035
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "103999886"
---
# <a name="mf_media_engine_playback_hwnd-attribute"></a>\_ \_ \_ Атрибут HWND воспроизведения ОБРАБОТЧИКа мультимедиа MF \_

Задает маркер для окна воспроизведения видео для механизма мультимедиа.

## <a name="data-type"></a>Тип данных

**HWND** хранится как **UINT64**

## <a name="getset"></a>Get/Set

Чтобы получить этот атрибут, вызовите [**имфаттрибутес:: UInt64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).

Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).

## <a name="remarks"></a>Комментарии

Этот атрибут используется с методом [**имфмедиаенгинеклассфактори:: CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) для инициализации механизма мультимедиа.

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

 

 




