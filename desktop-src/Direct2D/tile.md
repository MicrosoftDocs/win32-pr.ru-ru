---
title: Действие плитки
description: Используйте действие плитки для повторения указанной области изображения.
ms.assetid: C7505DBF-5F79-4407-84C4-634EA7EC06B7
keywords:
- действие плитки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0df10143a727fb8ce6585264b65b6db46d75c731070f2ea46ff8e7dffd59dd2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119430502"
---
# <a name="tile-effect"></a>Действие плитки

Используйте действие плитки для повторения указанной области изображения.

Идентификатором CLSID для этого действия является CLSID \_ D2D1Tile.

## <a name="example-image"></a>Пример изображения



| До                                                     |
|------------------------------------------------------------|
| ![изображение перед результатом.](images/default-before.jpg) |
| После                                                      |
| ![изображение после преобразования.](images/9-tile.png)       |



 


```C++
ComPtr<ID2D1Effect> tileEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Tile, &tileEffect);

tileEffect->SetInput(0, bitmap);

tileEffect->SetValue(D2D1_TILE_PROP_RECT, D2D1::RectF(0.0f, 0.0f, 256.0f, 192.0f));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(tileEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a>Свойства эффектов



| Отображаемое имя и перечисление индекса                | Тип и значение по умолчанию                                              | Описание                                                                                                                                        |
|---------------------------------------------------|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Rect<br/> D2D1 \_ элемента \_ prop \_ плитки<br/> | D2D1 \_ vector \_ 4F<br/> {0,0 f, 0,0 f, 100,0 f, 100,0 f}<br/> | Область изображения для мозаичного заполнения. Это свойство является D2D1 \_ вектором \_ 4F, определенным как: (слева, сверху, справа, снизу). Единицы измерения — DIP.<br/> |



 

## <a name="output-bitmap"></a>Битовая карта вывода

Этот результат приводит к созданию точечного рисунка с логически бесконечным размером.

Можно мозаично разместить изображение и вывести определенный размер без дополнительных эффектов, задав размер при вызове [**ID2D1DeviceContext::D равимаже**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1image_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode)).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента | Windows 8 и обновление платформы для Windows 7 \[ классических приложений \| Windows приложения магазина\] |
| Минимальная версия сервера | Windows 8 и обновление платформы для Windows 7 \[ классических приложений \| Windows приложения магазина\] |
| Header                   | d2d1effects. h                                                                      |
| Библиотека                  | D2D1. lib, дксгуид. lib                                                               |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

