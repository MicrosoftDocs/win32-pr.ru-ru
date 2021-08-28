---
title: Воздействие на обнаружение границ
description: Отфильтровывает содержимое изображения, открывая линии на краях контрастных разделов изображения.
ms.assetid: d22868cf-95fe-690e-66ac-268d7e116aee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7067243c19ed65bcdc23f1654999ff10ad3b80bafa641d0d3da940719db7bcd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119967073"
---
# <a name="edge-detection-effect"></a>Воздействие на обнаружение границ

Отфильтровывает содержимое изображения, открывая линии на краях контрастных разделов изображения.

Идентификатором CLSID для этого действия является CLSID \_ D2D1EdgeDetection.

-   [Пример изображения](#example-image)
-   [Образец кода](#sample-code)
-   [Свойства эффектов](#effect-properties)
-   [Требования](#requirements)
-   [Связанные темы](#related-topics)

## <a name="example-image"></a>Пример изображения

![Пример выходных данных эффектов](images/edge-detection-effect.png)

## <a name="sample-code"></a>Пример кода

```cpp
ComPtr<ID2D1Effect> edgeDetectionEffect;
m_d2dContext->CreateEffect(CLSID_D2D1EdgeDetection, &edgeDetectionEffect);
 
edgeDetectionEffect->SetInput(0, bitmap);
edgeDetectionEffect->SetValue(D2D1_EDGEDETECTION_PROP_STRENGTH, 0.5f);
edgeDetectionEffect->SetValue(D2D1_EDGEDETECTION_PROP_BLUR_RADIUS, 0.0f);
edgeDetectionEffect->SetValue(D2D1_EDGEDETECTION_PROP_MODE, D2D1_EDGEDETECTION_MODE_SOBEL);
edgeDetectionEffect->SetValue(D2D1_EDGEDETECTION_PROP_OVERLAY_EDGES, false);
edgeDetectionEffect->SetValue(D2D1_EDGEDETECTION_PROP_ALPHA_MODE, D2D1_ALPHA_MODE_PREMULTIPLIED);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(edgeDetectionEffect.Get());
m_d2dContext->EndDraw();
```

## <a name="effect-properties"></a>Свойства эффектов

Свойства для воздействия на обнаружение границ определяются перечислением [**D2D1 \_ еджедетектион \_ prop**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_edgedetection_prop) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------------|---------------------------------------------------|
| Минимальная версия клиента | Windows 10 \[ классические приложения \| Windows приложения магазина\] |
| Минимальная версия сервера | Windows 10 \[ классические приложения \| Windows приложения магазина\] |
| Заголовок                   | d2d1effects \_ 2. h                                  |
| Библиотека                  | D2D1. lib, дксгуид. lib                              |

## <a name="related-topics"></a>Связанные темы

* [Интерфейс ID2D1Effect](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
