---
title: Эффекты RGB-оттенков
description: Преобразует изображение RGB в цветовые пространства HSL (оттенок, насыщенность, освещение) или HSV (оттенок, насыщенность, значение).
ms.assetid: 1def972d-8172-9217-8ce7-abce4a93f6e1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c474705d050c2ef2eff9050a759c60c5d8f1098440e06601ec1e3981e349aaff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118160390"
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
-   [Связанные темы](#related-topics)

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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------------|---------------------------------------------------|
| Минимальная версия клиента | Windows 10 \[ классические приложения \| Windows приложения магазина\] |
| Минимальная версия сервера | Windows 10 \[ классические приложения \| Windows приложения магазина\] |
| Заголовок                   | d2d1effects \_ 2. h                                  |
| Библиотека                  | D2D1. lib, дксгуид. lib                              |


## <a name="related-topics"></a>Связанные темы

* [Интерфейс ID2D1Effect](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
