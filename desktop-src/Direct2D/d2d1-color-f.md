---
title: D2D1_COLOR_F (D2DBaseTypes. h)
description: Описывает красный, зеленый, синий и альфа-компоненты цвета. | D2D1_COLOR_F (D2DBaseTypes. h)
ms.assetid: 564d4f41-2da7-49ed-b85a-d1070d662b40
keywords:
- D2D1_COLOR_F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78f12c4c833d7f73946b2309673dff8f3dd11395
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105674607"
---
# <a name="d2d1_color_f"></a>D2D1 \_ Color \_ F

Описывает красный, зеленый, синий и альфа-компоненты цвета.


```C++
typedef D2D_COLOR_F D2D1_COLOR_F;
```



## <a name="remarks"></a>Комментарии

**D2D1 \_ ЦВЕТ \_ f** — это определение типа [**D2D для \_ цвета \_ f**](d2d-color-f.md), который сам по себе является typedef для [D3DCOLORVALUE](../direct3d9/d3dcolorvalue.md). Дополнительные сведения о членах, предоставляемых **D2D1 \_ Color \_ F**, см. в разделе [D3DCOLORVALUE](../direct3d9/d3dcolorvalue.md).

Класс [**колорф**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) предоставляет набор предопределенных цветов и вспомогательных функций для определения цветов. Дополнительные сведения см. в справочнике по [**колорф**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) .

## <a name="examples"></a>Примеры

В следующем примере класс [**колорф**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) используется для указания стандартного цвета (черного) при создании [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush).


```C++
hr = m_pRenderTarget->CreateSolidColorBrush(
    D2D1::ColorF(D2D1::ColorF::Black, 1.0f),
    &m_pBlackBrush
    );
```



В следующем примере класс [**колорф**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) используется для указания цвета с помощью красного, зеленого, синего и альфа-значения.


```C++
ID2D1SolidColorBrush *pGridBrush = NULL;
hr = pCompatibleRenderTarget->CreateSolidColorBrush(
    D2D1::ColorF(D2D1::ColorF(0.93f, 0.94f, 0.96f, 1.0f)),
    &pGridBrush
    );
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 7, Windows Vista с пакетом обновления 2 (SP2) и обновлением платформы для \[ классических приложений Windows Vista \| приложения UWP\]<br/>                          |
| Минимальная версия сервера<br/> | Windows Server 2008 R2, Windows Server 2008 с пакетом обновления 2 (SP2) и обновление платформы для Windows Server 2008 классические \[ приложения \| UWP\]<br/> |
| Минимальный поддерживаемый телефон<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 и среда выполнения Windows приложения\]<br/>                                                  |
| Header<br/>                   | <dl> <dt>D2DBaseTypes. h (включение D2d1. h)</dt> </dl>                               |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[D3DCOLORVALUE](../direct3d9/d3dcolorvalue.md)
</dt> <dt>

[**колорф**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf)
</dt> </dl>

 

