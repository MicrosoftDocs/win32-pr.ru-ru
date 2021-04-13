---
description: Указывает, является ли поток изображений в источнике видеозаписи независимым от видеопотока.
ms.assetid: DC4ED612-593B-40BF-BB42-946149042D1F
title: Атрибут MF_DEVICESTREAM_INDEPENDENT_IMAGE_STREAM (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 174e62a1bdd178ad2d8dce7fab5bf9ce3104d834
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105647239"
---
# <a name="mf_devicestream_independent_image_stream-attribute"></a>\_ \_ Атрибут потока с независимым \_ изображением MF девицестреам \_

Указывает, является ли поток изображений в источнике видеозаписи независимым от видеопотока.

## <a name="data-type"></a>Тип данных

**Bool** , сохраненный как **UINT32**

## <a name="remarks"></a>Комментарии

Некоторые USB-камеры видео предоставляют поток, который создает изображения. В некоторых камерах поток изображений просто возвращает следующий кадр из видеопотока. В других камерах поток изображений работает независимо от видеопотока. Если камера имеет независимый поток изображений, источник носителя для устройства записи устанавливает для этого атрибута **значение true** в потоке изображений.

Чтобы получить этот атрибут, выполните следующие действия.

1.  Запросите источник мультимедиа для интерфейса [**имфмедиасаурцеекс**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex) .
2.  Вызовите метод [**имфмедиасаурцеекс:: жетстреаматтрибутес**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) , чтобы получить указатель [**имфаттрибутес**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) для потока.
3.  Вызовите [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) , чтобы получить атрибут.

Этот атрибут применяется только в том случае, если атрибут [ \_ \_ \_ потока изображений MF девицестреам](mf-devicestream-image-stream.md) имеет **значение true**.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                         |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                               |
| Header<br/>                   | <dl> <dt>Мфидл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




