---
title: Атрибут Алтернатесаурцеурл
description: Атрибут Алтернатесаурцеурл — это универсальный указатель ресурсов для элемента мультимедиа, который служит альтернативой атрибутам Длнасаурцеури и Саурцеурл.
ms.assetid: 2be88d9b-4fd8-4e70-9a4d-114a2bf8b23c
keywords:
- проигрыватель Windows Media атрибута алтернатесаурцеурл
topic_type:
- apiref
api_name:
- AlternateSourceURL Attribute
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 765c7a3945224e82a0112c0f4dd7249e4340ec13e0d78adbd59039d25f234aaf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055242"
---
# <a name="alternatesourceurl-attribute"></a>Атрибут Алтернатесаурцеурл

Атрибут **алтернатесаурцеурл** — это универсальный указатель ресурсов для элемента мультимедиа, который служит альтернативой атрибутам [**длнасаурцеури**](dlnasourceuri-attribute.md) и [**саурцеурл**](sourceurl-attribute.md) .

## <a name="applies-to"></a>Применяется к

-   [**Звуковые элементы**](audio-item-attributes.md)
-   [**Элементы фото**](photo-item-attributes.md)
-   [**Элементы списка воспроизведения**](playlist-attributes-ref.md)
-   [**Элементы видео**](video-item-attributes.md)

## <a name="remarks"></a>Remarks

Этот атрибут недоступен для элементов мультимедиа в локальной библиотеке текущего пользователя. Он доступен только для элементов мультимедиа, принадлежащих удаленной библиотеке. то есть библиотека, доступная другим пользователям в домашней сети. Чтобы определить, является ли библиотека мультимедиа удаленной, вызовите метод [**ивмплибрари:: Get \_ Type**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_type).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|------------------------------------|
| Версия<br/> | проигрыватель Windows Media 12<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Ссылка на атрибут**](attribute-reference.md)
</dt> </dl>

 

 





