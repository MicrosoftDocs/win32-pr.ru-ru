---
description: Определяет набор клавиш анимации. Ключ матрицы полезен для наборов данных анимации, которые должны быть представлены как матрицы преобразования.
ms.assetid: bf007541-7fea-423e-910b-fa5f45271608
title: аниматионкэй
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05728f124ae01962a1291547f8fe8b7fcebd175a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701243"
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

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Шаблоны](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



