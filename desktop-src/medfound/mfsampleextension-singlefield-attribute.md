---
description: Указывает, содержит ли образец видео одно поле или два поля с чередованием. Этот атрибут применяется к примерам мультимедиа.
ms.assetid: 550619be-2042-4a2c-9ad2-728474835255
title: Атрибут MFSampleExtension_SingleField (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 747dbeebb9bcc8e773b59467f460b12645ed50ebfbddf5bbf6845119c2bba81d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119462904"
---
# <a name="mfsampleextension_singlefield-attribute"></a>Мфсампликстенсион \_ синглефиелд, атрибут

Указывает, содержит ли образец видео одно поле или два поля с чередованием. Этот атрибут применяется к примерам мультимедиа.

## <a name="data-type"></a>Тип данных

**Bool** , сохраненный как **UINT32**

## <a name="getset"></a>Get/Set

Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Применяется к

[**имфсампле**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a>Remarks

Если значение равно **true**, пример содержит одно поле. Если значение равно **false** или атрибут не задан, пример содержит полный кадр. (Два поля при чередовании или прогрессивный фрейм.)

Если тип носителя — прогрессивные кадры или поля с чередованием, этот атрибут должен иметь **значение false** или не заполняться.

Если тип мультимедиа является одним полем, этот атрибут должен иметь **значение true**. Задайте атрибут [**мфсампликстенсион \_ боттомфиелдфирст**](mfsampleextension-bottomfieldfirst-attribute.md) в образце, чтобы указать, является ли это верхнее поле или нижнее поле.

В настоящее время расширенный обработчик видео (Евр) не поддерживает содержимое, переключаясь между чередованием кадров и отдельными полями.

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

[Примеры атрибутов](sample-attributes.md)
</dt> <dt>

[Примеры носителей](media-samples.md)
</dt> <dt>

[Чередование видео](video-interlacing.md)
</dt> </dl>

 

 




