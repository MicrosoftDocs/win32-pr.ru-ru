---
description: Указывает, находится ли кадр видео с чередованием или с последовательной разверткой.
ms.assetid: 3cb80e75-e803-493b-a22d-e485e77b5177
title: Атрибут MFSampleExtension_Interlaced (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36d928d42fc2399536d5beee4f4af87cbacaa82171048ad191a4e9fc7ef3e939
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118240651"
---
# <a name="mfsampleextension_interlaced-attribute"></a>Мфсампликстенсион \_ чередующийся атрибут

Указывает, находится ли кадр видео с чередованием или с последовательной разверткой. **Значение true** показывает, что кадр является чередованием. Если **значение равно false**, кадр является прогрессивным. Если не задано, тип носителя описывает чересстрочную развертку. Этот атрибут применяется к примерам мультимедиа.

## <a name="data-type"></a>Тип данных

**Bool** , сохраненный как **UINT32**

## <a name="getset"></a>Get/Set

Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Применяется к

[**имфсампле**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a>Remarks

Для видеосодержимого, содержащего смешанные прогрессивные и чередующиеся кадры, задайте тип мультимедиа с чередованием и используйте этот атрибут в каждом кадре, чтобы указать, является ли кадр прогрессивным или чередованием.

Для содержимого видео, которое полностью перемещается в чередование, задайте тип мультимедиа с чередованием и опустите этот атрибут или задайте для него **значение true** при каждом выборке.

Для содержимого видео, которое полностью прогрессивно, установите для типа мультимедиа значение прогрессивный и пропустите этот атрибут или задайте для него **значение false** в каждом образце.

Константа GUID для этого атрибута экспортируется из мфууид. lib.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Приложения UWP для классических приложений Vista \|\]<br/>                              |
| Минимальная версия сервера<br/> | Windows \[Приложения UWP для классических приложений сервера 2008 \|\]<br/>                        |
| Header<br/>                   | <dl> <dt>Мфапи. h</dt> </dl> |



## <a name="see-also"></a>См. также статью

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**Имфаттрибутес:: UINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**Имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**имфсампле**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)
</dt> <dt>

[Примеры атрибутов](sample-attributes.md)
</dt> <dt>

[Примеры носителей](media-samples.md)
</dt> <dt>

[Чередование видео](video-interlacing.md)
</dt> </dl>

 

 




