---
title: Атрибут Алтернатесаурцеурл
description: Атрибут Алтернатесаурцеурл — это универсальный указатель ресурсов для элемента мультимедиа, который служит альтернативой атрибутам Длнасаурцеури и Саурцеурл.
ms.assetid: 2be88d9b-4fd8-4e70-9a4d-114a2bf8b23c
keywords:
- Алтернатесаурцеурл атрибут Windows Media Player
topic_type:
- apiref
api_name:
- AlternateSourceURL Attribute
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 574a355dfa862c4db004fa2df942e464934a38ec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105695027"
---
# <a name="alternatesourceurl-attribute"></a>Атрибут Алтернатесаурцеурл

Атрибут **алтернатесаурцеурл** — это универсальный указатель ресурсов для элемента мультимедиа, который служит альтернативой атрибутам [**длнасаурцеури**](dlnasourceuri-attribute.md) и [**саурцеурл**](sourceurl-attribute.md) .

## <a name="applies-to"></a>Применение

-   [**Звуковые элементы**](audio-item-attributes.md)
-   [**Элементы фото**](photo-item-attributes.md)
-   [**Элементы списка воспроизведения**](playlist-attributes-ref.md)
-   [**Элементы видео**](video-item-attributes.md)

## <a name="remarks"></a>Комментарии

Этот атрибут недоступен для элементов мультимедиа в локальной библиотеке текущего пользователя. Он доступен только для элементов мультимедиа, принадлежащих удаленной библиотеке. то есть библиотека, доступная другим пользователям в домашней сети. Чтобы определить, является ли библиотека мультимедиа удаленной, вызовите метод [**ивмплибрари:: Get \_ Type**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_type).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------|
| Версия<br/> | Проигрыватель Windows Media 12<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Ссылка на атрибут**](attribute-reference.md)
</dt> </dl>

 

 





