---
description: Задает визуальный элемент Microsoft DirectComposition в качестве региона воспроизведения для механизма мультимедиа.
ms.assetid: C381D28E-B7A1-4A1A-9F8D-42A4ABB1C633
title: Атрибут MF_MEDIA_ENGINE_PLAYBACK_VISUAL (Мфмедиаенгине. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25e9c7366bd0fbf4bf36523cf7a68f2d6da70bc3
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105647757"
---
# <a name="mf_media_engine_playback_visual-attribute"></a>\_ \_ \_ Визуальный атрибут воспроизведения МУЛЬТИМЕДИЙного модуля MF \_

Задает визуальный элемент Microsoft DirectComposition в качестве региона воспроизведения для механизма мультимедиа.

## <a name="data-type"></a>Тип данных

**Идкомпоситионвисуал \* *_ хранится как _* IUnknown\***

## <a name="getset"></a>Get/Set

Чтобы получить этот атрибут, вызовите [**имфаттрибутес:: ununknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).

Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: сетункновн**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).

## <a name="remarks"></a>Комментарии

Дополнительные сведения о DirectComposition см. в разделе [DirectComposition](../directcomp/directcomposition-portal.md) и [**идкомпоситионвисуал**](/windows/win32/api/dcomp/nn-dcomp-idcompositionvisual).

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

 

 
