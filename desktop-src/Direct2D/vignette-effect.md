---
title: Вигнетте, результат
description: Постепенно уменьшает входной рисунок на краях до заданного пользователем цвета.
ms.assetid: 34da221f-44a2-1d01-d88d-d7846b9770b9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3fe9302a86a49b060aa05ecb856ce43122d946d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136735"
---
# <a name="vignette-effect"></a>Вигнетте, результат

Постепенно уменьшает входной рисунок на краях до заданного пользователем цвета.

Идентификатором CLSID для этого действия является CLSID \_ D2D1Vignette.

-   [Пример изображения](#example-image)
-   [Образец кода](#sample-code)
-   [Свойства эффектов](#effect-properties)
-   [Требования](#requirements)
-   [См. также](#related-topics)

## <a name="example-image"></a>Пример изображения

![Пример выходных данных эффектов](images/vignette-effect.png)

## <a name="sample-code"></a>Пример кода

```cpp
ComPtr<ID2D1Effect> vignetteEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Vignette, &vignetteEffect);
 
vignetteEffect->SetInput(0, bitmap);
vignetteEffect->SetValue(D2D1_VIGNETTE_PROP_COLOR, );
vignetteEffect->SetValue(D2D1_VIGNETTE_PROP_TRANSITION_SIZE, 0.1f);
vignetteEffect->SetValue(D2D1_VIGNETTE_PROP_STRENGTH, 0.5f);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(vignetteEffect.Get());
m_d2dContext->EndDraw();
```

## <a name="effect-properties"></a>Свойства эффектов

Свойства для вигнеттеного действия определяются перечислением [**D2D1 \_ вигнетте \_ prop**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_vignette_prop) .

## <a name="requirements"></a>Требования

| Требование | Значение |
|--------------------------|---------------------------------------------------|
| Минимальная версия клиента | Приложения для \[ магазина Windows для классических приложений Windows 10 \|\] |
| Минимальная версия сервера | Приложения для \[ магазина Windows для классических приложений Windows 10 \|\] |
| Header                   | d2d1effects \_ 2. h                                  |
| Библиотека                  | D2D1. lib, дксгуид. lib                              |

## <a name="related-topics"></a>См. также

* [Интерфейс ID2D1Effect](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
