---
description: Атрибут самплинграте задает частоту выборки выходного звука в Гц.
ms.assetid: d053285c-bf94-465a-99d3-bed7c2d09b1a
title: Атрибут самплинграте
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2daa2751b0c41f5bf2eb030841dad638d8672a8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105673063"
---
# <a name="samplingrate-attribute"></a>Атрибут самплинграте

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`samplingrate`Атрибут задает частоту выборки выходного звука в Гц.

## <a name="possible-values"></a>Возможные значения

Значение должно быть 8000, 11025, 22050, 32000, 44100 или 48000. Значение по умолчанию — 44100.

## <a name="applies-to"></a>Применение

[**сгруппировать**](group-element.md)

## <a name="remarks"></a>Комментарии

Устанавливайте этот атрибут только в том случае, если атрибут **Type** имеет значение `audio` .

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Атрибуты КСТЛ](xtl-attributes.md)
</dt> </dl>

 

 



