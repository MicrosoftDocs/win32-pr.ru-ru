---
description: Определяет набор клавиш анимации. Ключ матрицы полезен для наборов данных анимации, которые должны быть представлены как матрицы преобразования.
ms.assetid: bf007541-7fea-423e-910b-fa5f45271608
title: аниматионкэй
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bad23a6cc519b0b0525cd0dac1b488184b3bf91e99359e252f44dca435ace529
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118806409"
---
# <a name="animationkey"></a>аниматионкэй

Определяет набор клавиш анимации. Ключ матрицы полезен для наборов данных анимации, которые должны быть представлены как матрицы преобразования.

``` syntax
template AnimationKey
{
    < 10DD46A8-775B-11CF-8F52-0040333594A3 >
    DWORD keyType;
    DWORD nKeys;
    array TimedFloatKeys keys[nKeys];
} 
```

Где:

-   keyType — указывает, являются ли ключи ключами вращения, масштабирования, расположения или матрицы (с использованием целых чисел 0, 1, 2 или 3 соответственно).
-   Нкэйс — число ключей.
-   ключи — массив ключей. См. [**тимедфлоаткэйс**](timedfloatkeys.md).

## <a name="see-also"></a>См. также

<dl> <dt>

[Шаблоны](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



