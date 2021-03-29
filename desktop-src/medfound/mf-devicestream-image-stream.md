---
description: Указывает, является ли поток в источнике видеозаписи по-прежнему потоком изображения.
ms.assetid: 52251A45-3603-41C7-A869-7F6319BD337F
title: Атрибут MF_DEVICESTREAM_IMAGE_STREAM (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 382ce587574d6ec46509a460dfb964e23dd416d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810486"
---
# <a name="mf_devicestream_image_stream-attribute"></a>\_ \_ Атрибут потока изображений MF девицестреам \_

Указывает, является ли поток в источнике видеозаписи по-прежнему потоком изображения.

## <a name="data-type"></a>Тип данных

**Bool** , сохраненный как **UINT32**

## <a name="remarks"></a>Комментарии

Некоторые видеокамеры предоставляют поток с изображением по-прежнему, который создает изображения с высоким разрешением. Поток изображений может создавать несжатые изображения или изображения в формате JPEG. Если камера имеет поток изображений, источник носителя для устройства записи устанавливает для этого атрибута **значение true** в потоке изображений.

Чтобы получить этот атрибут, выполните следующие действия.

1.  Запросите источник мультимедиа для интерфейса [**имфмедиасаурцеекс**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex) .
2.  Вызовите метод [**имфмедиасаурцеекс:: жетстреаматтрибутес**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) , чтобы получить указатель [**имфаттрибутес**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) для потока.
3.  Вызовите [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) , чтобы получить атрибут.

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

 

 




