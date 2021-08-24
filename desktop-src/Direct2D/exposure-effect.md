---
title: Воздействие на выдержки
description: Увеличение или уменьшение экспозиции изображения.
ms.assetid: d384f539-5c19-53c7-e52b-bf833e221449
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcdcd99e125251c3144d96ffd6054897e6801eb3299c1d1ae90e37494620faea
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119652932"
---
# <a name="exposure-effect"></a>Воздействие на выдержки

Увеличение или уменьшение экспозиции изображения.

Идентификатором CLSID для этого действия является CLSID \_ D2D1Exposure.

-   [Пример изображения](#example-image)
-   [Образец кода](#sample-code)
-   [Свойства эффектов](#effect-properties)
-   [Требования](#requirements)
-   [Связанные темы](#related-topics)

## <a name="example-image"></a>Пример изображения

![Пример выходных данных эффектов](images/exposure-effect.png)

## <a name="sample-code"></a>Пример кода


```C++
ComPtr<ID2D1Effect> exposureEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Exposure, &exposureEffect);
 
exposureEffect->SetInput(0, bitmap);
exposureEffect->SetValue(D2D1_EXPOSURE_PROP_EXPOSURE_VALUE, 1.0f);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(exposureEffect.Get());
m_d2dContext->EndDraw();


```



## <a name="effect-properties"></a>Свойства эффектов

Свойства для влияния на выдержки определяются перечислением [**D2D1 \_ экспозиции \_**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_exposure_prop) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------------|---------------------------------------------------|
| Минимальная версия клиента | Windows 10 \[ классические приложения \| Windows приложения магазина\] |
| Минимальная версия сервера | Windows 10 \[ классические приложения \| Windows приложения магазина\] |
| Заголовок                   | d2d1effects \_ 2. h                                  |
| Библиотека                  | D2D1. lib, дксгуид. lib                              |


## <a name="related-topics"></a>Связанные темы

* [Интерфейс ID2D1Effect](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)




