---
title: Контрастный результат
description: Увеличивает или уменьшает контрастность изображения.
ms.assetid: c0cc0f86-f6d4-e951-0cdd-dbad488e0793
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6f287b1309aceadc4709bae3b1c2101a06df32d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071732"
---
# <a name="contrast-effect"></a>Контрастный результат

Увеличивает или уменьшает контрастность изображения.

Идентификатором CLSID для этого действия является CLSID \_ D2D1Contrast.

Функция контрастности изменяет каждое значение цветового канала с помощью двух кусочно-ных полиномов, которые соответствуют наклону непрерывности в точке (0,5, 0,5).

![кусочно-ие одноквадратных коэффициентов, которые соответствуют наклону непрерывности в точке (0,5, 0,5)](images/contrast-effect-slope.png)

-   [Примеры изображений](#example-images)
-   [Образец кода](#sample-code)
-   [Свойства эффектов](#effect-properties)
-   [Требования](#requirements)
-   [См. также](#related-topics)

## <a name="example-images"></a>Примеры изображений

В этом примере показаны выходные данные результата с максимальной контрастностью (контраст = 1,0).

До

![изображение перед применением эффектов](images/contrast-effect-before.png)

После

![изображение после применения эффектов](images/contrast-effect-after.png)

## <a name="sample-code"></a>Пример кода

```cpp
ComPtr<ID2D1Effect> contrastEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Contrast, &contrastEffect);
 
contrastEffect->SetInput(0, bitmap);
contrastEffect->SetValue(D2D1_CONTRAST_PROP_CONTRAST, 0.5f);
contrastEffect->SetValue(D2D1_CONTRAST_PROP_CLAMP_INPUT, TRUE);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(contrastEffect.Get());
m_d2dContext->EndDraw();
```

## <a name="effect-properties"></a>Свойства эффектов

Свойства для эффектов контрастности определяются перечислением [**\_ \_ prop контрастности D2D1**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_contrast_prop) .

## <a name="requirements"></a>Требования

| Требование | Значение |
|--------------------------|---------------------------------------------------|
| Минимальная версия клиента | Приложения для \[ магазина Windows для классических приложений Windows 10 \|\] |
| Минимальная версия сервера | Приложения для \[ магазина Windows для классических приложений Windows 10 \|\] |
| Header                   | d2d1effects \_ 2. h                                  |
| Библиотека                  | D2D1. lib, дксгуид. lib                              |

## <a name="related-topics"></a>См. также

* [Интерфейс ID2D1Effect](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
