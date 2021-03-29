---
title: Методы Креатехвндрендертаржет ID2D1Factory (D2d1. h)
description: Создает ID2D1HwndRenderTarget, целевой объект отрисовки, который готовится к просмотру в окне.
ms.assetid: 3b55b1b0-a423-40dc-9581-c1fbe8134ca5
keywords:
- Методы Креатехвндрендертаржет Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 984de8aea923c5b90d05fb79bc0c9edc319fb4bb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657603"
---
# <a name="id2d1factorycreatehwndrendertarget-methods"></a>Методы ID2D1Factory:: Креатехвндрендертаржет

Создает [**ID2D1HwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)), целевой объект отрисовки, который готовится к просмотру в окне.

### <a name="overload-list"></a>Список перегрузок



| Метод                                                                                                                                                                                                                                                                              | Описание                                                                                                             |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| [**Креатехвндрендертаржет ( \_ \_ свойства целевого объекта прорисовки D2D1 \_ \* , \_ \_ свойства целевого объекта прорисовки D2D1 HWND \_ \_ \* , ID2D1HwndRenderTarget \* \* )**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)) | Создает [**ID2D1HwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)), целевой объект отрисовки, который готовится к просмотру в окне.<br/> |
| [**Креатехвндрендертаржет ( \_ \_ свойства целевого объекта прорисовки D2D1 \_& \_ , \_ свойства целевого объекта прорисовки D2D1 HWND \_ \_&, ID2D1HwndRenderTarget \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createhwndrendertarget(constd2d1_render_target_properties__constd2d1_hwnd_render_target_properties__id2d1hwndrendertarget))   | Создает [**ID2D1HwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)), целевой объект отрисовки, который готовится к просмотру в окне.<br/> |



## <a name="remarks"></a>Комментарии

При создании целевого объекта рендеринга и возможности аппаратного ускорения выделяются ресурсы на GPU компьютера. Создавая целевой объект рендеринга один раз и постоянно сохраняющий его, вы получаете выигрыш в производительности. Приложение должно создавать целевые объекты рендеринга один раз и удерживать их на протяжении всего жизненного цикла приложения или до тех пор, пока не будет получено сообщение об ошибке [**\_ повторного создания \_ D2DERR**](direct2d-error-codes.md) . При возникновении этой ошибки необходимо повторно создать целевой объект рендеринга (и все созданные им ресурсы).

## <a name="examples"></a>Примеры

В следующем примере создается [**ID2D1HwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)).


```C++
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
|--------------------|-------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D2d1. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>D2d1. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)
</dt> </dl>
