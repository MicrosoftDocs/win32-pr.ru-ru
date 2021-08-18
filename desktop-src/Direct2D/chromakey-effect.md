---
title: Чрома-клавиша
description: Преобразует заданный цвет плюс или минус значение допуска в альфа-канал. Например, чрома-Key может удалить фон изображения для зеленого цвета экрана.
ms.assetid: f7bb5c65-f406-f947-c05d-2756cff99d21
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 485cec7842c8460169b9c335eb74e9cc6d5a13e0541a49fc99835dfaa591efc2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119075596"
---
# <a name="chroma-key-effect"></a>Чрома-клавиша

Преобразует заданный цвет плюс или минус значение допуска в альфа-канал. Например, чрома-Key может удалить фон изображения для зеленого цвета экрана.

Идентификатором CLSID для этого действия является CLSID \_ D2D1ChromaKey.

-   [Пример изображения](#example-image)
-   [Образец кода](#sample-code)
-   [Свойства эффектов](#effect-properties)
-   [Требования](#requirements)
-   [Связанные темы](#related-topics)

## <a name="example-image"></a>Пример изображения

![Пример выходных данных эффектов](images/chromakey-effect.png)

> [!Note]  
> В этом примере результатом действия чрома-Key является второе изображение с прозрачным фоном шахматной доски. Третий образ сочетает это с фоновым изображением для окончательного наложения зеленого экрана.

## <a name="sample-code"></a>Пример кода

```cppcx
ComPtr<ID2D1Effect> chromakeyEffect;
m_d2dContext->CreateEffect(CLSID_D2D1ChromaKey, &chromakeyEffect);
 
chromakeyEffect->SetInput(0, bitmap);
chromaKeyEffect->SetValue(D2D1_CHROMAKEY_PROP_COLOR, {0.0f, 1.0f, 0.0f, 0.0f});
chromakeyEffect->SetValue(D2D1_CHROMAKEY_PROP_TOLERANCE, 0.2f);
chromakeyEffect->SetValue(D2D1_CHROMAKEY_PROP_INVERT_ALPHA, false);
chromakeyEffect->SetValue(D2D1_CHROMAKEY_PROP_FEATHER, false);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(chromakeyEffect.Get());
m_d2dContext->EndDraw();
```

## <a name="effect-properties"></a>Свойства эффектов

Свойства для влияния чрома-Key определяются перечислением [**D2D1 \_ чромакэй \_ prop**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_chromakey_prop) .

## <a name="requirements"></a>Требования

| Требование | Значение |
|--------------------------|---------------------------------------------------|
| Минимальная версия клиента | Windows 10 \[ классические приложения \| Windows приложения магазина\] |
| Минимальная версия сервера | Windows 10 \[ классические приложения \| Windows приложения магазина\] |
| Заголовок                   | d2d1effects \_ 2. h                                  |
| Библиотека                  | D2D1. lib, дксгуид. lib                              |

## <a name="related-topics"></a>Связанные темы

* [Интерфейс ID2D1Effect](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
