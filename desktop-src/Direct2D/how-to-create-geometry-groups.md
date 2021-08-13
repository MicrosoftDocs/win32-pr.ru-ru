---
title: Создание геометрических групп
description: В этом разделе описывается создание групп Geometry.
ms.assetid: be364440-75ab-4d8f-a359-39da275272fd
keywords:
- Direct2D, пример режима Fill
- группы Geometry
- Direct2D, геометрические группы
- геометрические контуры
- Direct2D, геометрические объекты
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5540d96b9befddaa8eb6eef7fcc61e3e6c7665a7319de1ea123c9ce94281f101
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119259254"
---
# <a name="how-to-create-geometry-groups"></a>Создание геометрических групп

В этом разделе описывается создание групп Geometry.

Чтобы создать группу Geometry, вызовите метод [**ID2D1Factory:: креатежеометриграуп**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-creategeometrygroup) и укажите массив геометрических объектов и режим заполнения.

При объединении геометрических объектов в группу Geometry убедитесь, что геометрические объекты аналогичны. Если вы не знаете ориентацию геометрических объектов, вызовите [**ID2D1Geometry:: структурировать**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-outline(constd2d1_matrix_3x2_f__float_id2d1simplifiedgeometrysink)) для каждого из них по отдельности, а затем вставьте полученные объекты Geometry в группу Geometry.

В следующем примере кода показано создание четырех концентрических кругов: первый круг имеет радиус 25, второй 50, третий 75 и четвертый 100. Код также показывает создание экземпляра массива геометрических объектов, а также два вызова [**креатежеометриграуп**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-creategeometrygroup).


```C++
HRESULT DemoApp::CreateGeometryResources()
{
    HRESULT hr;

    const D2D1_ELLIPSE ellipse1 = D2D1::Ellipse(
        D2D1::Point2F(105.0f, 105.0f),
        25.0f,
        25.0f
        );

    hr = m_pD2DFactory->CreateEllipseGeometry(
        ellipse1,
        &m_pEllipseGeometry1
        );

    if (SUCCEEDED(hr))
    {
        const D2D1_ELLIPSE ellipse2 = D2D1::Ellipse(
            D2D1::Point2F(105.0f, 105.0f),
            50.0f,
            50.0f
            );

        hr = m_pD2DFactory->CreateEllipseGeometry(
            ellipse2,
            &m_pEllipseGeometry2
            );
    }

    if (SUCCEEDED(hr))
    {

        const D2D1_ELLIPSE ellipse3 = D2D1::Ellipse(
            D2D1::Point2F(105.0f, 105.0f),
            75.0f,
            75.0f
            );

        hr = m_pD2DFactory->CreateEllipseGeometry(
            ellipse3,
            &m_pEllipseGeometry3
            );
    }

    if (SUCCEEDED(hr))
    {
        const D2D1_ELLIPSE ellipse4 = D2D1::Ellipse(
            D2D1::Point2F(105.0f, 105.0f),
            100.0f,
            100.0f
            );

        hr = m_pD2DFactory->CreateEllipseGeometry(
            ellipse4,
            &m_pEllipseGeometry4
            );
    }

    if (SUCCEEDED(hr))
    {
        ID2D1Geometry *ppGeometries[] =
        {
            m_pEllipseGeometry1,
            m_pEllipseGeometry2,
            m_pEllipseGeometry3,
            m_pEllipseGeometry4
        };

        hr = m_pD2DFactory->CreateGeometryGroup(
            D2D1_FILL_MODE_ALTERNATE,
            ppGeometries,
            ARRAYSIZE(ppGeometries),
            &m_pGeoGroup_AlternateFill
            );

        if (SUCCEEDED(hr))
        {
            hr = m_pD2DFactory->CreateGeometryGroup(
                D2D1_FILL_MODE_WINDING,
                ppGeometries,
                ARRAYSIZE(ppGeometries),
                &m_pGeoGroup_WindingFill
                );
        }

    }
    return hr;
}
```



## <a name="drawing-and-filling-of-geometry-groups"></a>Рисование и заполнение геометрических групп

Чтобы нарисовать и заполнить геометрическую группу, используйте методы [**ID2D1RenderTarget:: филлжеометри**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) и [**ID2D1RenderTarget::D равжеометри**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) . В следующем примере кода показано рисование и заливка геометрической группы.


```C++
HRESULT DemoApp::OnRender()
{
    HRESULT hr = CreateDeviceResources();

    if (SUCCEEDED(hr))
    {
        static const WCHAR sc_fillModeAlternateText[] = L"D2D1_FILL_MODE_ALTERNATE";
        static const WCHAR sc_fillModeWindingText[] = L"D2D1_FILL_MODE_WINDING";

        m_pRenderTarget->BeginDraw();

        m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Identity());

        m_pRenderTarget->Clear(D2D1::ColorF(D2D1::ColorF::White));

        D2D1_SIZE_F rtSize = m_pRenderTarget->GetSize();
        m_pRenderTarget->FillRectangle(
            D2D1::RectF(0.0f, 0.0f, rtSize.width, rtSize.height),
            m_pGridPatternBitmapBrush
            );

        // Centers the text in a layout rectangle.
        hr = m_pTextFormat->SetTextAlignment(DWRITE_TEXT_ALIGNMENT_CENTER);

        if (SUCCEEDED(hr))
        {
            // Fill the geometry group with D2D1_FILL_MODE_ALTERNATE and
            // then draw the geometries in the group.
            m_pRenderTarget->FillGeometry(m_pGeoGroup_AlternateFill, m_pFillBrush);
            m_pRenderTarget->DrawGeometry(m_pGeoGroup_AlternateFill, m_pStrokeBrush, 1.0f);

            m_pRenderTarget->DrawText(
                sc_fillModeAlternateText,
                ARRAYSIZE(sc_fillModeAlternateText) - 1,
                m_pTextFormat,
                D2D1::RectF(5, 215, 205, 240),
                m_pStrokeBrush,
                D2D1_DRAW_TEXT_OPTIONS_NONE,
                DWRITE_MEASURING_MODE_NATURAL
                );

            m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Translation(300, 0));

            // Fill the geometry group with D2D1_FILL_MODE_WINDING and
            // then draw the geometries in the group.
            m_pRenderTarget->FillGeometry(m_pGeoGroup_WindingFill, m_pFillBrush);
            m_pRenderTarget->DrawGeometry(m_pGeoGroup_WindingFill, m_pStrokeBrush, 1.0f);

            m_pRenderTarget->DrawText(
                sc_fillModeWindingText,
                ARRAYSIZE(sc_fillModeWindingText) - 1,
                m_pTextFormat,
                D2D1::RectF(5, 215, 205, 240),
                m_pStrokeBrush,
                D2D1_DRAW_TEXT_OPTIONS_NONE,
                DWRITE_MEASURING_MODE_NATURAL
                );

            hr = m_pRenderTarget->EndDraw();

            if (hr == D2DERR_RECREATE_TARGET)
            {
                hr = S_OK;
                DiscardDeviceResources();
            }
        }
    }
    return hr;
}
```



Код создает выходные данные, показанные на следующем рисунке.

![Иллюстрация двух наборов из четырех концентрических кругов: один с заполненным вторым и четвертым кольцами, а другой — со всеми заполненными кольцами](images/create-geometry-group.png)

 

 