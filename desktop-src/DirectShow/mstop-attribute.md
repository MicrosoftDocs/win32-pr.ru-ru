---
description: Атрибут МСТОП задает время окончания клипа относительно исходного файла мультимедиа.
ms.assetid: 01559d29-9c7b-4842-a1f7-16552adbda43
title: Атрибут МСТОП
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a63f52a1b912392165293e008074cf64a03b9751
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104139298"
---
# <a name="mstop-attribute"></a>Атрибут МСТОП

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`mstop`Атрибут задает время окончания клипа относительно исходного файла мультимедиа.

## <a name="applies-to"></a>Применение

[**clip**](clip-element.md)

## <a name="possible-values"></a>Возможные значения

Должен быть строкой формата *чч: мм: СС. FF* , где *чч* = ч, *мм* = минуты, *SS* = секунды и *FF* = доли секунды. Пример: 1:04:30.512. Начальные единицы можно опустить. Например, допустимыми являются 3:00 (три минуты) и 45 (45 секунд).

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Атрибуты КСТЛ](xtl-attributes.md)
</dt> <dt>

[**Иамтимелинесрк:: Сетмедиатимес**](iamtimelinesrc-setmediatimes.md)
</dt> </dl>

 

 



