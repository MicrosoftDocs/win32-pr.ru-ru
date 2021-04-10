---
title: D2D1_SIZE_U (D2DBaseTypes. h)
description: Сохраняет упорядоченную пару целых чисел — обычно ширину и высоту прямоугольника.
ms.assetid: e28da5ee-7d68-4ec5-b477-c6ead0c725e6
keywords:
- D2D1_SIZE_U
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c78b5c317a98169957402dd125c054b8f6e0bc69
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135439"
---
# <a name="d2d1_size_u"></a>D2D1 \_ размер \_ U

Сохраняет упорядоченную пару целых чисел — обычно ширину и высоту прямоугольника.


```C++
typedef D2D_SIZE_U D2D1_SIZE_U;
```



## <a name="remarks"></a>Комментарии

Как и точки, размеры являются еще одной важной концепцией графики. В Direct2D размеры представлены структурами D2D1 размера **\_ \_ U** или D2D1, [**\_ равными \_ F**](d2d1-size-f.md) . Они содержат упорядоченную пару чисел. Структура **D2D1 \_ size \_ U** содержит упорядоченную пару значений **UINT32** , а структура **D2D1 \_ size \_ F** содержит упорядоченную пару значений **float** .

Структура **D2D1 \_ size \_ U** предоставляет удобный способ хранения упорядоченной пары чисел, например ширины и высоты прямоугольника.

**D2D1 \_ РАЗМЕР \_ u** — это новое имя для уже определенного типа **D2D с \_ размером \_ U**. Для создания структуры **D2D1 \_ size \_ U** можно использовать функцию **D2D1:: сизеу** . Как правило, эта структура используется для указания размера пикселя [**D2D1 \_ HWND \_ визуализации \_ целевой структуры \_ свойств**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_hwnd_render_target_properties) . Ниже приведен пример использования этой структуры.


```C++
    if (!m_pRenderTarget)
    {
        RECT rc;
        GetClientRect(m_hwnd, &rc);

        D2D1_SIZE_U size = D2D1::SizeU(
            rc.right - rc.left,
            rc.bottom - rc.top
            );

        // Create a Direct2D render target.
        hr = m_pD2DFactory->CreateHwndRenderTarget(
            D2D1::RenderTargetProperties(),
            D2D1::HwndRenderTargetProperties(m_hwnd, size),
            &m_pRenderTarget
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

[**\_Размер D2D \_ U**](/windows/desktop/api/dcommon/ns-dcommon-d2d_size_u)
</dt> <dt>

[**D2D1 \_ размер \_ F**](d2d1-size-f.md)
</dt> <dt>

[**D2D1:: Хвндрендертаржетпропертиес**](/windows/desktop/api/d2d1helper/nf-d2d1helper-hwndrendertargetproperties)
</dt> </dl>

 

