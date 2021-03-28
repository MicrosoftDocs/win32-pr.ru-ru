---
title: Negate
description: Переворачивает знак значения исходного операнда, используемого в арифметической операции.
ms.assetid: 83ef3f61-7b0b-4033-8f7b-5345b205c441
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: cc2637a76b52b28eefcfb3637cc8b2d406c02c06
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104069332"
---
# <a name="negate"></a>Negate

Переворачивает знак значения исходного операнда, используемого в арифметической операции.



| \-  |
|-----|



 

Для одиночной и двойной точности с плавающей запятой модификатор отрицания отражает знак числа в исходном операнде, включая значения INF. Применение функции **отрицания** для NaN сохраняет NaN, хотя определенный битовый шаблон NaN, который не определен, не определяется.

Для целочисленных инструкций модификатор **отрицания** принимает значение 2 для чисел в исходном операнде.

## <a name="minimum-shader-model"></a>Минимальная модель шейдера

Этот модификатор поддерживается в следующих моделях шейдеров.



| Модель шейдера                                              | Поддерживается |
|-----------------------------------------------------------|-----------|
| [Модель шейдера 5](d3d11-graphics-reference-sm5.md)        | да       |
| [Модель шейдера 4,1](dx-graphics-hlsl-sm4.md)              | да       |
| [Модель шейдера 4](dx-graphics-hlsl-sm4.md)                | да       |
| [Модель шейдера 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | Нет        |
| [Модель шейдера 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | Нет        |
| [Модель шейдера 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | Нет        |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Модификаторы инструкций](instruction-modifiers.md)
</dt> </dl>

 

 




