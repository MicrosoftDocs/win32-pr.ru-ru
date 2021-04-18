---
description: Задает первичные цвета для типа видеоклипа.
ms.assetid: 56f31c1a-b610-4da0-9df4-76e15add672c
title: Атрибут MF_MT_VIDEO_PRIMARIES (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6cdf26a3f49c7e2bb3aa0f48c52c9b283edd8cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712864"
---
# <a name="mf_mt_video_primaries-attribute"></a>\_ \_ \_ Атрибут первичного видео MF MT

Задает первичные цвета для типа видеоклипа.

## <a name="data-type"></a>Тип данных

**UINT32**

## <a name="remarks"></a>Комментарии

Значение этого атрибута является членом перечисления [**мфвидеопримариес**](/windows/desktop/api/mfobjects/ne-mfobjects-mfvideoprimaries) .

Перечисление [**мфвидеопримариес**](/windows/desktop/api/mfobjects/ne-mfobjects-mfvideoprimaries) определяет первичные цвета, связанные с определенными распространенными стандартами видео. Если тип мультимедиа использует первичные цвета, которые не определены в перечислении **мфвидеопримариес** , задайте вместо этого атрибута атрибут " [**\_ \_ пользовательские \_ \_ первичные цвета" MF MT**](mf-mt-custom-video-primaries-attribute.md) .

Константа GUID для этого атрибута экспортируется из мфууид. lib.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Приложения UWP для классических приложений Windows Vista \|\]<br/>                              |
| Минимальная версия сервера<br/> | \[Приложения UWP для классических приложений Windows Server 2008 \|\]<br/>                        |
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

 

 




