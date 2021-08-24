---
description: Указывает параметр дискретизация (QP), который использовался для кодирования примера видео.
ms.assetid: F7C4FEFC-FEE7-4614-BC90-4F9D5D878F49
title: Атрибут MFSampleExtension_VideoEncodeQP (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f86253b29dfa93b3699d5175b5c5ef198b4ab24e862901572caafcc55fd62d1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119777024"
---
# <a name="mfsampleextension_videoencodeqp-attribute"></a>Мфсампликстенсион \_ видеоенкодекп, атрибут

Указывает параметр дискретизация (QP), который использовался для кодирования примера видео.

## <a name="data-type"></a>Тип данных

**UINT64**

## <a name="getset"></a>Get/Set

Чтобы получить этот атрибут, вызовите [**имфаттрибутес:: UInt64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).

Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).

## <a name="applies-to"></a>Применяется к

[**имфсампле**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a>Remarks

[**Кодировщик видео H. 264**](h-264-video-encoder.md) устанавливает этот атрибут для создаваемых результирующих примеров.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ приложения UWP для классических приложений \|\]<br/>                                  |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                          |
| Заголовок<br/>                   | <dl> <dt>Мфапи. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**Кодировщик видео H. 264**](h-264-video-encoder.md)
</dt> <dt>

[Примеры атрибутов](sample-attributes.md)
</dt> <dt>

[Примеры носителей](media-samples.md)
</dt> </dl>

 

 




