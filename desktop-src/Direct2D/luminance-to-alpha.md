---
title: Воздействие светимости на альфа
description: Используйте воздействие «светимость на альфа», чтобы установить альфа-канал на светимость изображения и задать для цветовых каналов значение 0.
ms.assetid: B380DE5A-C097-47E0-8E0F-E3C9D2BA44B0
keywords:
- воздействие светимости на альфа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fb4c6fb78a1d49498b2adab6716d41e93d30deb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104556321"
---
# <a name="luminance-to-alpha-effect"></a>Воздействие светимости на альфа

Используйте воздействие «светимость на альфа», чтобы установить альфа-канал на светимость изображения и задать для цветовых каналов значение 0. Вывод этого результата можно использовать для создания полупрозрачного наложения на основе яркости входного изображения. Его также можно использовать для создания маски изображения.

> [!Note]  
> У этого действия нет свойств.

 

Идентификатором CLSID для этого действия является CLSID \_ D2D1LuminanceToAlpha.

## <a name="example-image"></a>Пример изображения

В этом примере показаны выходные данные светимости в альфа-эффекты, совмещенные на белой поверхности для отображения прозрачности.



| До                                                            |
|-------------------------------------------------------------------|
| ![изображение перед результатом.](images/default-before.jpg)        |
| После                                                             |
| ![изображение после преобразования.](images/18-luminancetoalpha.png) |



 


```C++
ComPtr<ID2D1Effect> luminanceToAlphaEffect;
m_d2dContext->CreateEffect(CLSID_D2D1LuminanceToAlpha, &luminanceToAlphaEffect);

luminanceToAlphaEffect->SetInput(0, bitmap);

// LuminanceToAlpha result is composited on top of a white surface to show opacity.
ComPtr<ID2D1Effect> floodEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Flood, &floodEffect);
floodEffect->SetValue(D2D1_FLOOD_PROP_COLOR, D2D1::Vector4F(1.0f, 1.0f, 1.0f, 1.0f));

ComPtr<ID2D1Effect> compositeEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Composite, &compositeEffect);

compositeEffect->SetInputEffect(0, floodEffect.Get());
compositeEffect->SetInputEffect(1, luminanceToAlphaEffect.Get());

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(compositeEffect.Get());
m_d2dContext->EndDraw();
```



Этот результат устанавливает в качестве альфа-канала выходных данных светимость входного изображения, используя эту матрицу цветов.

![Цветовая матрица, используемая для установки альфа-канала.](images/luminance-to-alpha-math1.png)

Этот результат использует и выводит предварительно умноженные альфа-изображения. Этот результат не будет работать с прямыми альфа-изображениями, если они не полностью непрозрачны.

> [!Note]
>
> Поскольку изображения хранятся в формате с гамма-компенсацией, перед вычислением светимости для изображения необходимо сначала выполнить инверсную гамму-коррекцию, чтобы получить значения True Color для изображения. Так как изображения обычно хранятся в 2,2 гаммы, можно использовать гамма-пересылку с экспонентой (1/2.2), а затем использовать выходные данные этого результата.

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента | Windows 8 и обновление платформы для \[ классических приложений Windows 7 \| приложения для Магазина Windows\] |
| Минимальная версия сервера | Windows 8 и обновление платформы для \[ классических приложений Windows 7 \| приложения для Магазина Windows\] |
| Header                   | d2d1effects. h                                                                      |
| Библиотека                  | D2D1. lib, дксгуид. lib                                                               |



 

## <a name="output-bitmap"></a>Битовая карта вывода

Выходные данные имеют тот же размер, что и входной образ.

## <a name="related-topics"></a>См. также

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

 
