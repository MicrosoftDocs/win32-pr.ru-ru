---
description: Указывает, является ли поток в источнике видеозаписи по-прежнему потоком изображения.
ms.assetid: 52251A45-3603-41C7-A869-7F6319BD337F
title: Атрибут MF_DEVICESTREAM_IMAGE_STREAM (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a42ec0ea6ac8f89c7b35e5ae137c92aaf62006b9b06be689bb7203626f36b7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118244767"
---
# <a name="mf_devicestream_image_stream-attribute"></a>\_ \_ Атрибут потока изображений MF девицестреам \_

Указывает, является ли поток в источнике видеозаписи по-прежнему потоком изображения.

## <a name="data-type"></a>Тип данных

**Bool** , сохраненный как **UINT32**

## <a name="remarks"></a>Remarks

Некоторые видеокамеры предоставляют поток с изображением по-прежнему, который создает изображения с высоким разрешением. Поток изображений может создавать несжатые изображения или изображения в формате JPEG. Если камера имеет поток изображений, источник носителя для устройства записи устанавливает для этого атрибута **значение true** в потоке изображений.

Чтобы получить этот атрибут, выполните следующие действия.

1.  Запросите источник мультимедиа для интерфейса [**имфмедиасаурцеекс**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex) .
2.  Вызовите метод [**имфмедиасаурцеекс:: жетстреаматтрибутес**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) , чтобы получить указатель [**имфаттрибутес**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) для потока.
3.  Вызовите [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) , чтобы получить атрибут.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                         |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                               |
| Header<br/>                   | <dl> <dt>Мфидл. h</dt> </dl> |



## <a name="see-also"></a>См. также статью

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




