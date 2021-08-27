---
description: Содержит предпочитаемый язык RFC 1766 для источника мультимедиа.
ms.assetid: 30f99804-6aea-473b-9bbf-e8c715501391
title: Атрибут MF_PD_PREFERRED_LANGUAGE (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6cd01a47002bf3cd9419579786ff37df1fc03af940f54b2d2a2bb859d5b97007
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118740715"
---
# <a name="mf_pd_preferred_language-attribute"></a>\_ \_ Атрибут предпочтительного \_ языка MF PD

Содержит предпочитаемый язык RFC 1766 для источника мультимедиа.

## <a name="data-type"></a>Тип данных

**WCHAR**

## <a name="getset"></a>Get/Set

Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).

Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: сеттринг**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).

## <a name="applies-to"></a>Применяется к

[**имфпресентатиондескриптор**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)

## <a name="remarks"></a>Remarks

\_ \_ Атрибут предпочтительного языка MF PD \_ является необязательным. Приложение может установить этот атрибут в источнике мультимедиа (например, в сетевом источнике), чтобы указать предпочтительный язык.

Константа GUID для этого атрибута экспортируется из мфууид. lib.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[приложения UWP для классических приложений Windows 7 \|\]<br/>                                  |
| Минимальная версия сервера<br/> | Windows \[Приложения UWP для настольных приложений Server 2008 R2 \|\]<br/>                     |
| Header<br/>                   | <dl> <dt>Мфидл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Атрибуты дескриптора представления](presentation-descriptor-attributes.md)
</dt> </dl>

 

 




