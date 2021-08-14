---
description: Задает первичные цвета для типа видеоклипа.
ms.assetid: 56f31c1a-b610-4da0-9df4-76e15add672c
title: Атрибут MF_MT_VIDEO_PRIMARIES (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44b4e1c99dc9a4f288ebab36d413f7eed7c74881e7c10d3c7e9a8a4fe3f0bcf6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117876714"
---
# <a name="mf_mt_video_primaries-attribute"></a>\_ \_ \_ Атрибут первичного видео MF MT

Задает первичные цвета для типа видеоклипа.

## <a name="data-type"></a>Тип данных

**UINT32**

## <a name="remarks"></a>Remarks

Значение этого атрибута является членом перечисления [**мфвидеопримариес**](/windows/desktop/api/mfobjects/ne-mfobjects-mfvideoprimaries) .

Перечисление [**мфвидеопримариес**](/windows/desktop/api/mfobjects/ne-mfobjects-mfvideoprimaries) определяет первичные цвета, связанные с определенными распространенными стандартами видео. Если тип мультимедиа использует первичные цвета, которые не определены в перечислении **мфвидеопримариес** , задайте вместо этого атрибута атрибут " [**\_ \_ пользовательские \_ \_ первичные цвета" MF MT**](mf-mt-custom-video-primaries-attribute.md) .

Константа GUID для этого атрибута экспортируется из мфууид. lib.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Приложения UWP для классических приложений Vista \|\]<br/>                              |
| Минимальная версия сервера<br/> | Windows \[Приложения UWP для классических приложений сервера 2008 \|\]<br/>                        |
| Header<br/>                   | <dl> <dt>Мфапи. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**Имфаттрибутес:: UINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**Имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**имфмедиатипе**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Атрибуты типа мультимедиа](media-type-attributes.md)
</dt> <dt>

[Расширенные сведения о цвете](extended-color-information.md)
</dt> </dl>

 

 




