---
title: Эффекты резкости
description: Повышает резкость изображения.
ms.assetid: 1eb12d1e-83c1-ba13-33be-df2078f3ccb8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b74d95f7305dd6d44eb4dfbe2707f9e636e2ce704af2dc02fcf55477dbf2222d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119873772"
---
# <a name="sharpen-effect"></a>Эффекты резкости

Повышает резкость изображения.

Идентификатором CLSID для этого действия является CLSID \_ D2D1Sharpen.

-   [Пример изображения](#example-image)
-   [Образец кода](#sample-code)
-   [Свойства эффектов](#effect-properties)
-   [Требования](#requirements)
-   [Связанные темы](#related-topics)

## <a name="example-image"></a>Пример изображения

![Пример выходных данных эффектов](images/sharpen-effect.png)

## <a name="sample-code"></a>Пример кода


```C++
ComPtr<ID2D1Effect> sharpenEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Sharpen, &sharpenEffect);
 
sharpenEffect->SetInput(0, bitmap);
sharpenEffect->SetValue(D2D1_SHARPEN_PROP_SHARPNESS, 1.0f);
sharpenEffect->SetValue(D2D1_SHARPEN_PROP_THRESHOLD, 0.5f);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(hueToRgbEffect.Get());
m_d2dContext->EndDraw();


```



## <a name="effect-properties"></a>Свойства эффектов

Свойства для эффектов резкости определяются перечислением [**D2D1 \_ резкость \_**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_sharpen_prop) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------------|---------------------------------------------------|
| Минимальная версия клиента | Windows 10 \[ классические приложения \| Windows приложения магазина\] |
| Минимальная версия сервера | Windows 10 \[ классические приложения \| Windows приложения магазина\] |
| Заголовок                   | d2d1effects \_ 2. h                                  |
| Библиотека                  | D2D1. lib, дксгуид. lib                              |


## <a name="related-topics"></a>Связанные темы

* [Интерфейс ID2D1Effect](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)



