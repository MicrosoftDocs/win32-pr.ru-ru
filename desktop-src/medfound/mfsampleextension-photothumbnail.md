---
description: Содержит эскиз фотографии Имфсампле.
ms.assetid: 510706A3-92FB-4188-97B9-6E8E0B4B175F
title: Атрибут MFSampleExtension_PhotoThumbnail (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5cbdb6f79b1b1ee187677a7f1a7a7792acb10fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155962"
---
# <a name="mfsampleextension_photothumbnail-attribute"></a>\_Атрибут Фотоэскизов мфсампликстенсион

Содержит эскиз фотографии [**имфсампле**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample).

## <a name="data-type"></a>Тип данных

**IUnknown** , хранимый как **имфмедиабуффер**

Эскиз настраивается с помощью **кспропертисетид \_ екстендедкамераконтрол**.

## <a name="remarks"></a>Комментарии

Этот атрибут задается для [**имфсампле**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) , ПРЕДОСТАВЛЯЕМого MFT0, и является интерфейсом [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) [**имфмедиабуффер**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) , связанным с эскизом фотографии.

Эскиз фотографии может иметь формат JPEG (изображение крупного типа), NV12 или ARGB32.

[Мфсампликстенсион \_ фотосумбнаилмедиатипе](mfsampleextension-photothumbnailmediatype.md) необходим для того, чтобы эскизы описывали тип носителя.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Приложения UWP для классических приложений Windows 8.1 \|\]<br/>                                |
| Минимальная версия сервера<br/> | \[Приложения UWP для классических приложений Windows Server 2012 R2 \|\]<br/>                     |
| Header<br/>                   | <dl> <dt>Мфапи. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**имфсампле**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)
</dt> </dl>

 

 
