---
description: Задает входной поток на Media Foundation преобразовании (MFT).
ms.assetid: 2922af62-3fcc-4153-a26a-aba3c4121a0b
title: Атрибут MF_EVENT_MFT_INPUT_STREAM_ID (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3d211eb30280e6b7390df8509795d49567c7f8a8c9016b2825786858fe888b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973813"
---
# <a name="mf_event_mft_input_stream_id-attribute"></a>\_ \_ \_ Атрибут ID входного \_ потока MFT события MF \_

Задает входной поток на Media Foundation преобразовании (MFT).

## <a name="data-type"></a>Тип данных

**UINT32**

Значение является идентификатором входного потока.

## <a name="getset"></a>Get/Set

Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Применяется к

[**имфмедиаевент**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent)

## <a name="remarks"></a>Remarks

Этот атрибут используется со следующими событиями:

-   [метрансформдраинкомплете](metransformdraincomplete.md)
-   [метрансформнидинпут](metransformneedinput.md)

Константа GUID для этого атрибута экспортируется из мфууид. lib.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[приложения UWP для классических приложений Windows 7 \|\]<br/>                                  |
| Минимальная версия сервера<br/> | Windows \[Приложения UWP для настольных приложений Server 2008 R2 \|\]<br/>                     |
| Заголовок<br/>                   | <dl> <dt>Мфапи. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Асинхронный МФТС](asynchronous-mfts.md)
</dt> <dt>

[Атрибуты событий](event-attributes.md)
</dt> </dl>

 

 




