---
description: Атрибут мленгс задает длительность исходного файла. Это значение должно быть фактической длительностью, или могут возникать ошибки отрисовки.
ms.assetid: f33ce85c-df61-4248-8dea-677162fa1a07
title: Атрибут мленгс
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35eadc288e29d99df0e6af7f06e1404d86f6a938
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103989883"
---
# <a name="mlength-attribute"></a>Атрибут мленгс

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`mlength`Атрибут задает длительность исходного файла. Это значение должно быть фактической длительностью, или могут возникать ошибки отрисовки.

## <a name="applies-to"></a>Применение

[**clip**](clip-element.md)

## <a name="possible-values"></a>Возможные значения

Должен быть строкой формата *чч: мм: СС. FF* , где *чч* = ч, *мм* = минуты, *SS* = секунды и *FF* = доли секунды. Пример: 1:04:30.512. Начальные единицы можно опустить. Например, допустимыми являются 3:00 (три минуты) и 45 (45 секунд).

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Атрибуты КСТЛ](xtl-attributes.md)
</dt> <dt>

[**Иамтимелинесрк:: Сетмедиаленгс**](iamtimelinesrc-setmedialength.md)
</dt> </dl>

 

 



