---
description: Указывает тип изображения, выводимого кодировщиком видео.
ms.assetid: 18A47033-3EAC-46C3-94AB-6ED20732F63C
title: Атрибут MFSampleExtension_VideoEncodePictureType (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3be87284be3b605e3af70d64df98e5d762aa7cc353bb83b5f61a110d1242ae1d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973173"
---
# <a name="mfsampleextension_videoencodepicturetype-attribute"></a>Мфсампликстенсион \_ видеоенкодепиктуретипе, атрибут

Указывает тип изображения, выводимого кодировщиком видео.

## <a name="data-type"></a>Тип данных

**eAVEncH264PictureType \_ Б** хранится как **UINT32**

## <a name="getset"></a>Get/Set

Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Применяется к

[**имфсампле**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a>Remarks

[**Кодировщик видео H. 264**](h-264-video-encoder.md) устанавливает этот атрибут для создаваемых результирующих примеров. Значение атрибута является членом перечисления [**eAVEncH264PictureType**](/windows/desktop/api/codecapi/ne-codecapi-eavench264picturetype) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ приложения UWP для классических приложений \|\]<br/>                                  |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                          |
| Заголовок<br/>                   | <dl> <dt>Мфапи. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**Кодировщик видео H. 264**](h-264-video-encoder.md)
</dt> <dt>

[Примеры атрибутов](sample-attributes.md)
</dt> <dt>

[Примеры носителей](media-samples.md)
</dt> </dl>

 

 




