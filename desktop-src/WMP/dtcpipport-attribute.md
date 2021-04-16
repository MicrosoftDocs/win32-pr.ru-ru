---
title: Атрибут Дткпиппорт
description: Атрибут Дткпиппорт — это номер порта TCP компьютера или устройства, к которому необходимо обратиться для цифровой передачи Защита содержимого по протоколу Internet Protocol (ДТКП-IP) обмен ключами с проверкой подлинности (Аке) для элемента мультимедиа.
ms.assetid: 63767ec1-dd01-40c2-bf9a-6e9b8a7db7f8
keywords:
- Дткпиппорт атрибут Windows Media Player
topic_type:
- apiref
api_name:
- DTCPIPPort Attribute
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16c1c6117425211c0015d218412c8a9ac0971d7b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699290"
---
# <a name="dtcpipport-attribute"></a>Атрибут Дткпиппорт

Атрибут **дткпиппорт** — это номер порта TCP компьютера или устройства, к которому необходимо обратиться для цифровой передачи защита содержимого по протоколу Internet Protocol (ДТКП-IP) обмен ключами с проверкой подлинности (Аке) для элемента мультимедиа.

## <a name="applies-to"></a>Применение

-   [**Звуковые элементы**](audio-item-attributes.md)
-   [**Элементы фото**](photo-item-attributes.md)
-   [**Элементы списка воспроизведения**](playlist-attributes-ref.md)
-   [**Элементы видео**](video-item-attributes.md)

## <a name="remarks"></a>Комментарии

Если этот атрибут доступен, элемент мультимедиа защищен с помощью ДТКП-IP.

Этот атрибут недоступен для элементов мультимедиа в локальной библиотеке текущего пользователя. Он доступен только для элементов мультимедиа, принадлежащих удаленной библиотеке. то есть библиотека, доступная другим пользователям в домашней сети. Чтобы определить, является ли библиотека мультимедиа удаленной, вызовите метод [**ивмплибрари:: Get \_ Type**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_type).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------|
| Версия<br/> | Проигрыватель Windows Media 12<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Ссылка на атрибут**](attribute-reference.md)
</dt> </dl>

 

 





