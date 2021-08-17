---
title: Атрибут WM/Албумковерурл
description: Атрибут WM/Албумковерурл представляет собой универсальный указатель ресурсов (URL-адрес) для обложки альбома или эскиза изображения.
ms.assetid: 0134867a-7c11-4d50-9ab5-b48c1ca6c473
keywords:
- проигрыватель Windows Media атрибута WM/албумковерурл
topic_type:
- apiref
api_name:
- WM/AlbumCoverURL Attribute
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce3e3d2948419761a139139493e737df1a9a709147613eadd3e077f0f5101f3a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118332630"
---
# <a name="wmalbumcoverurl-attribute"></a>Атрибут WM/Албумковерурл

Атрибут **WM/албумковерурл** представляет собой универсальный указатель ресурсов (URL-адрес) для обложки альбома или эскиза изображения.

## <a name="applies-to"></a>Применяется к

-   [**Звуковые элементы**](audio-item-attributes.md)
-   [**Элементы фото**](photo-item-attributes.md)
-   [**Элементы видео**](video-item-attributes.md)

## <a name="remarks"></a>Remarks

Для звукового элемента этот атрибут является URL-адресом обложки альбома. Для фотографии или видеозаписи этот атрибут является URL-адресом эскиза изображения.

Этот атрибут недоступен для элементов мультимедиа в локальной библиотеке текущего пользователя. Он доступен только для элементов мультимедиа, принадлежащих удаленной библиотеке. то есть библиотека, доступная другим пользователям в домашней сети. Чтобы определить, является ли библиотека мультимедиа удаленной, вызовите метод [**ивмплибрари:: Get \_ Type**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_type).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------|
| Версия<br/> | проигрыватель Windows Media 12 или более поздней версии.<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Ссылка на атрибут**](attribute-reference.md)
</dt> </dl>

 

 





