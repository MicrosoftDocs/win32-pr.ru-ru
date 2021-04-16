---
description: Указывает максимальное число кадров, которые будут помещены в буфер источника видеозаписи видео.
ms.assetid: af30606b-f1a0-4fbf-a831-05ed891f5d53
title: Атрибут MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_MAX_BUFFERS (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfa927d28b49da0eb0a0be40c3137f1cd9acf79b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682876"
---
# <a name="mf_devsource_attribute_source_type_vidcap_max_buffers-attribute"></a>MF \_ девсаурце \_ \_ тип источника \_ атрибута \_ видкап \_ максимальный \_ Размер буфера в атрибуте

Указывает максимальное число кадров, которые будут помещены в буфер источника видеозаписи видео.

## <a name="data-type"></a>Тип данных

**UINT32**

## <a name="getset"></a>Get/Set

Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Комментарии

По умолчанию источник видеозаписи видео помещает в буфер не более одного кадра за раз. Можно увеличить предельный размер буфера, задав этот атрибут.

Правильный способ установки этого атрибута зависит от функции, используемой для создания источника мультимедиа:

-   [**Мфкреатедевицесаурце**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource): Задайте атрибут с помощью параметра *паттрибутес* функции.
-   [**Мфкреатедевицесаурцеактивате**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate): Задайте атрибут с помощью параметра *паттрибутес* функции.
-   [**Мфенумдевицесаурцес**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources): Задайте атрибут для указателя [**имфактивате**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) , возвращаемого функцией. Задайте атрибут перед вызовом [**имфактивате:: активатеобжект**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).

Атрибут применяется только к устройствам записи видео.

Константа GUID для этого атрибута экспортируется из мфууид. lib.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/>                                         |
| Минимальная версия сервера<br/> | Только классические приложения Windows Server 2008 R2 \[\]<br/>                            |
| Header<br/>                   | <dl> <dt>Мфидл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Захват аудио- и видеоданных](audio-video-capture.md)
</dt> <dt>

[Запись атрибутов устройства](capture-device-attributes.md)
</dt> </dl>

 

 




