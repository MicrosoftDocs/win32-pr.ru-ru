---
title: Эффект выделения и теней
description: Регулирует выделение и тени изображения.
ms.assetid: ebbb7d99-9144-ffff-af73-d89e7d269924
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d595a5b82a2df0b0b0bab14c03e6a807511ed61
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104568642"
---
# <a name="highlights-and-shadows-effect"></a>Эффект выделения и теней

Регулирует выделение и тени изображения.

Идентификатором CLSID для этого действия является CLSID \_ D2D1HighlightsShadows.

-   [Пример изображения](#example-image)
-   [Образец кода](#sample-code)
-   [Свойства эффектов](#effect-properties)
-   [Требования](#requirements)
-   [См. также](#related-topics)

## <a name="example-image"></a>Пример изображения

![Пример выходных данных эффектов](images/highlights-and-shadows-effect.png)

## <a name="sample-code"></a>Пример кода

```cpp
ComPtr<ID2D1Effect> highlightsAndShadowsEffect;
m_d2dContext->CreateEffect(CLSID_D2D1HighlightsShadows, &highlightsAndShadowsEffect);
 
highlightsAndShadowsEffect->SetInput(0, bitmap);
highlightsAndShadowsEffect->SetValue(D2D1_HIGHLIGHTSANDSHADOWS_PROP_HIGHLIGHTS, 0.0f);
highlightsAndShadowsEffect->SetValue(D2D1_HIGHLIGHTSANDSHADOWS_PROP_SHADOWS, 0.5f);
highlightsAndShadowsEffect->SetValue(D2D1_HIGHLIGHTSANDSHADOWS_PROP_CLARITY, 0.2f);
highlightsAndShadowsEffect->SetValue(D2D1_HIGHLIGHTSANDSHADOWS_PROP_INPUT_GAMMA, D2D1_HIGHLIGHTSANDSHADOWS_INPUT_GAMMA_LINEAR);
highlightsAndShadowsEffect->SetValue(D2D1_HIGHLIGHTSANDSHADOWS_PROP_MASK_BLUR_RADIUS, 1.0f);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(hueToRgbEffect.Get());
m_d2dContext->EndDraw();
```

## <a name="effect-properties"></a>Свойства эффектов

Свойства для эффектов светлых и темных значений определяются перечислением [**D2D1 \_ хигхлигхтсандшадовс \_ prop**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_highlightsandshadows_prop) .

## <a name="requirements"></a>Требования

| Требование | Значение |
|--------------------------|---------------------------------------------------|
| Минимальная версия клиента | Приложения для \[ магазина Windows для классических приложений Windows 10 \|\] |
| Минимальная версия сервера | Приложения для \[ магазина Windows для классических приложений Windows 10 \|\] |
| Header                   | d2d1effects \_ 2. h                                  |
| Библиотека                  | D2D1. lib, дксгуид. lib                              |

## <a name="related-topics"></a>См. также

* [Интерфейс ID2D1Effect](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
