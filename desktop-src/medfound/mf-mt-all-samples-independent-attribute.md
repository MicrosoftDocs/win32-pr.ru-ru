---
description: Указывает тип носителя, независимо от других выборок в потоке.
ms.assetid: 40434f63-e191-45e1-b788-5f80fe7f49ae
title: Атрибут MF_MT_ALL_SAMPLES_INDEPENDENT (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ada34232ccbc7eb30fc9a5bcb64e96542b0375140de426fae951f5e0317c9e1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060754"
---
# <a name="mf_mt_all_samples_independent-attribute"></a>MF \_ \_ все \_ примеры \_ независимых атрибутов

Указывает тип носителя, независимо от других выборок в потоке.

## <a name="data-type"></a>Тип данных

**UINT32**

Рассматривать как логическое значение.

## <a name="remarks"></a>Remarks

Если этот атрибут имеет **значение false**, некоторые примеры нельзя использовать без ссылки на другие примеры в потоке. Например, если видеоформат содержит разностные кадры, этот атрибут должен иметь **значение false**.

этот атрибут соответствует полю **бтемпоралкомпрессион** в структуре [**\_ \_ типа мультимедиа**](/windows/win32/api/strmif/ns-strmif-am_media_type) DirectShow.

Задайте для этого атрибута **значение true** для всех несжатых типов мультимедиа.

Константа GUID для этого атрибута экспортируется из мфууид. lib.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Приложения UWP для классических приложений Vista \|\]<br/>                              |
| Минимальная версия сервера<br/> | Windows \[Приложения UWP для классических приложений сервера 2008 \|\]<br/>                        |
| Заголовок<br/>                   | <dl> <dt>Мфапи. h</dt> </dl> |



## <a name="see-also"></a>См. также

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
</dt> </dl>

 

 
