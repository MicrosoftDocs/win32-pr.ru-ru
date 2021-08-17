---
description: Указывает формат выходных данных устройства.
ms.assetid: 33a1b546-ece2-44ef-a1c0-5579c32be0bc
title: Атрибут MF_DEVSOURCE_ATTRIBUTE_MEDIA_TYPE (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb4685f419658ecf77782a4cef770fd205119bb6cfd95523edb7fbbe001fd700
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105040"
---
# <a name="mf_devsource_attribute_media_type-attribute"></a>\_ \_ \_ Атрибут типа носителя для атрибута MF девсаурце \_

Указывает формат выходных данных устройства.

## <a name="data-type"></a>Тип данных

**[**MFT \_ \_ \_ Сведения о типе регистрации**](/windows/win32/api/mfobjects/ns-mfobjects-mft_register_type_info)** хранятся в виде **байта \[ \]**

## <a name="getset"></a>Get/Set

Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес::-BLOB**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).

Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).

## <a name="remarks"></a>Remarks

Этот атрибут содержит пару идентификаторов GUID: основной тип и подтип. Эти GUID описывают формат вывода по умолчанию для устройства. Устройство может поддерживать дополнительные выходные форматы.

Например, если устройство видеозаписи видео выводит RGB-32 видео, значение этого атрибута равно `{ MFMediaType_Video, MFVideoFormat_RGB32 }` .

Этот атрибут является указанием для приложения. Чтобы получить точный формат вывода, создайте источник мультимедиа для устройства и получите дескриптор представления источника мультимедиа.

Этот атрибут задается для объектов активации, возвращаемых следующими функциями:

-   [**мфкреатедевицесаурцеактивате**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate)
-   [**мфенумдевицесаурцес**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources)

Константа GUID для этого атрибута экспортируется из мфууид. lib.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>                                         |
| Минимальная версия сервера<br/> | Windows \[Только для настольных приложений сервера 2008 R2\]<br/>                            |
| Header<br/>                   | <dl> <dt>Мфидл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Захват аудио- и видеоданных](audio-video-capture.md)
</dt> <dt>

[Запись атрибутов устройства](capture-device-attributes.md)
</dt> </dl>

 

 




