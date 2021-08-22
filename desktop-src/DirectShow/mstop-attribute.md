---
description: Атрибут МСТОП задает время окончания клипа относительно исходного файла мультимедиа.
ms.assetid: 01559d29-9c7b-4842-a1f7-16552adbda43
title: Атрибут МСТОП
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9d432c3ed9ff80a9252def74fb553ed307668b36e660d96963baae0f4d0db04
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072945"
---
# <a name="mstop-attribute"></a>Атрибут МСТОП

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`mstop`Атрибут задает время окончания клипа относительно исходного файла мультимедиа.

## <a name="applies-to"></a>Применяется к

[**clip**](clip-element.md)

## <a name="possible-values"></a>Возможные значения

Должен быть строкой формата *чч: мм: СС. FF* , где *чч* = ч, *мм* = минуты, *SS* = секунды и *FF* = доли секунды. Пример: 1:04:30.512. Начальные единицы можно опустить. Например, допустимыми являются 3:00 (три минуты) и 45 (45 секунд).

## <a name="see-also"></a>См. также

<dl> <dt>

[Атрибуты КСТЛ](xtl-attributes.md)
</dt> <dt>

[**Иамтимелинесрк:: Сетмедиатимес**](iamtimelinesrc-setmediatimes.md)
</dt> </dl>

 

 



