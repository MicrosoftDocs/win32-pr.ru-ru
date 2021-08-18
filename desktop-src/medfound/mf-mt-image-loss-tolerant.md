---
description: Указывает, является ли поток изображений ASF типом деградабле JPEG.
ms.assetid: e29d0893-8561-4a8c-99e2-168186becd82
title: Атрибут MF_MT_IMAGE_LOSS_TOLERANT (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fdf5b2633586cf4b73279a636119ac4770a5321d6bc22b5b961fa85881019b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035172"
---
# <a name="mf_mt_image_loss_tolerant-attribute"></a>\_ \_ \_ \_ Атрибут нечувствительного к утере образа MF

Указывает, является ли поток изображений ASF типом деградабле JPEG.

## <a name="data-type"></a>Тип данных

**UINT32**

## <a name="getset"></a>Get/Set

Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Применяется к

[**имфмедиатипе**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a>Remarks

Этот атрибут применяется к типу мультимедиа для потоков изображений в формате ASF. Если значение равно **true**, то поток является типом изображения деградабле JPEG. В противном случае поток является типом изображения JFIF. Дополнительные сведения об этих типах потоков см. в спецификации ASF.

Помимо \_ \_ \_ \_ нечувствительного к сбоям образа, тип носителя для потока изображений ASF содержит следующие атрибуты:



| attribute                                                 | Описание                                |
|-----------------------------------------------------------|--------------------------------------------|
| [**\_ \_ основной тип MF \_ MT**](mf-mt-major-type-attribute.md) | Содержит изображение value **мфмедиатипе \_**. |
| [**\_ \_ Размер пакета MF \_ MT**](mf-mt-frame-size-attribute.md) | Задает размер изображения в пикселях.            |



 

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

[Атрибуты типа мультимедиа](media-type-attributes.md)
</dt> </dl>

 

 




