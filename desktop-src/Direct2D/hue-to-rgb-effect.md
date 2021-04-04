---
title: Эффекты оттенка по RGB
description: Преобразует изображение HSL (оттенок, насыщенность, освещение) или HSV (оттенок, насыщенность, значение) в цветовое пространство RGB.
ms.assetid: 18e92535-9e89-bf8d-b8c3-a49b645fc417
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82064d01281ab0edf2327f00cf6e852a0bebae53
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988585"
---
# <a name="hue-to-rgb-effect"></a>Эффекты оттенка по RGB

Преобразует изображение HSL (оттенок, насыщенность, освещение) или HSV (оттенок, насыщенность, значение) в цветовое пространство RGB.

HSL и HSV — это две различные модели для представления цвета RGB в виде цилиндров цветового пространства. Они полезны, так как они позволяют понять цвет с помощью более интуитивно понятных концепций, таких как оттенок и интенсивность, а также сочетания красного, зеленого и синего значений.

Этот результат проходит через любые входные альфа-значения.

Идентификатором CLSID для этого действия является CLSID \_ D2D1HueToRgb.

Чтобы изменить поведение этого действия, используйте [эффекты оттенка RGB](rgb-to-hue-effect.md).

-   [Образец кода](#sample-code)
-   [Свойства эффектов](#effect-properties)
-   [Требования](#requirements)
-   [См. также](#related-topics)

## <a name="sample-code"></a>Пример кода

```cpp
ComPtr<ID2D1Effect> hueToRgbEffect;
m_d2dContext->CreateEffect(CLSID_D2D1HueToRgb, &hueToRgbEffect);
 
hueToRgbEffect->SetInput(0, bitmap);
hueToRgbEffect->SetValue(D2D1_HUETORGB_INPUT_COLOR_SPACE, D2D1_HUETORGB_INPUT_COLOR_SPACE_HUE_SATURATION_LIGHTNESS);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(hueToRgbEffect.Get());
m_d2dContext->EndDraw();
```

## <a name="effect-properties"></a>Свойства эффектов

Свойства для эффектов контрастности определяются перечислением [**D2D1 \_ хуеторгб \_ prop**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_huetorgb_prop) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------------|---------------------------------------------------|
| Минимальная версия клиента | Приложения для \[ магазина Windows для классических приложений Windows 10 \|\] |
| Минимальная версия сервера | Приложения для \[ магазина Windows для классических приложений Windows 10 \|\] |
| Header                   | d2d1effects \_ 2. h                                  |
| Библиотека                  | D2D1. lib, дксгуид. lib                              |



## <a name="related-topics"></a>См. также

* [Интерфейс ID2D1Effect](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
