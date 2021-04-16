---
title: Эффекты RGB-оттенков
description: Преобразует изображение RGB в цветовые пространства HSL (оттенок, насыщенность, освещение) или HSV (оттенок, насыщенность, значение).
ms.assetid: 1def972d-8172-9217-8ce7-abce4a93f6e1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53ccb4d3f67d116426d7a3497c04c4e8fb115b74
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415365"
---
# <a name="rgb-to-hue-effect"></a>Эффекты RGB-оттенков

Преобразует изображение RGB в цветовые пространства HSL (оттенок, насыщенность, освещение) или HSV (оттенок, насыщенность, значение).

HSL и HSV — это две различные модели для представления цвета RGB в виде цилиндров цветового пространства. Они полезны, так как они позволяют понять цвет с помощью более интуитивно понятных концепций, таких как оттенок и интенсивность, а также сочетания красного, зеленого и синего значений.

Этот результат нормализует выходные данные (оттенок, значение насыщенности для HSV или оттенка, насыщенность, освещение для HSL) до диапазона \[ 0, 1 \] .

Идентификатором CLSID для этого действия является CLSID \_ D2D1RgbToHue.

Чтобы изменить поведение этого действия, используйте [эффекты оттенок для RGB](hue-to-rgb-effect.md).

-   [Образец кода](#sample-code)
-   [Свойства эффектов](#effect-properties)
-   [Требования](#requirements)
-   [См. также](#related-topics)

## <a name="sample-code"></a>Пример кода


```C++
ComPtr<ID2D1Effect> rgbToHueEffect;
m_d2dContext->CreateEffect(CLSID_D2D1RgbToHue, &rgbToHueEffect);
 
rgbToHueEffect->SetInput(0, bitmap);
rgbToHueEffect->SetValue(D2D1_RGBTOHUE_PROP_OUTPUT_COLOR_SPACE, D2D1_RGBTOHUE_OUTPUT_COLOR_SPACE_HUE_SATURATION_VALUE);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(rgbToHueEffect.Get());
m_d2dContext->EndDraw();

```



## <a name="effect-properties"></a>Свойства эффектов

Свойства для эффектов контрастности определяются перечислением [**D2D1 \_ ргбтохуе \_ prop**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_rgbtohue_prop) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------------|---------------------------------------------------|
| Минимальная версия клиента | Приложения для \[ магазина Windows для классических приложений Windows 10 \|\] |
| Минимальная версия сервера | Приложения для \[ магазина Windows для классических приложений Windows 10 \|\] |
| Header                   | d2d1effects \_ 2. h                                  |
| Библиотека                  | D2D1. lib, дксгуид. lib                              |


## <a name="related-topics"></a>См. также

* [Интерфейс ID2D1Effect](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
