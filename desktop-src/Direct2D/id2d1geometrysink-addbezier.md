---
title: Методы Аддбезиер ID2D1GeometrySink (D2d1. h)
description: Создает кривую Безье третьего порядка между текущей точкой и заданной конечной точкой и добавляет ее в приемник геометрии.
ms.assetid: d1e228eb-dac6-485d-b3c9-69b2bd45e531
keywords:
- Методы Аддбезиер Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: b470129350463920583c34bec5f886f60b16485e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657638"
---
# <a name="id2d1geometrysinkaddbezier-methods"></a><span data-ttu-id="8072e-104">Методы ID2D1GeometrySink:: Аддбезиер</span><span class="sxs-lookup"><span data-stu-id="8072e-104">ID2D1GeometrySink::AddBezier methods</span></span>

<span data-ttu-id="8072e-105">Создает кривую Безье третьего порядка между текущей точкой и заданной конечной точкой и добавляет ее в приемник геометрии.</span><span class="sxs-lookup"><span data-stu-id="8072e-105">Creates a cubic Bezier curve between the current point and the specified end point and adds it to the geometry sink.</span></span>

### <a name="overload-list"></a><span data-ttu-id="8072e-106">Список перегрузок</span><span class="sxs-lookup"><span data-stu-id="8072e-106">Overload list</span></span>



| <span data-ttu-id="8072e-107">Метод</span><span class="sxs-lookup"><span data-stu-id="8072e-107">Method</span></span>                                                                                            | <span data-ttu-id="8072e-108">Описание</span><span class="sxs-lookup"><span data-stu-id="8072e-108">Description</span></span>                                                                                    |
|:--------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="8072e-109">[**Аддбезиер ( \_ сегмент Безье D2D1 \_&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometrysink-addbezier(constd2d1_bezier_segment_))</span><span class="sxs-lookup"><span data-stu-id="8072e-109">[**AddBezier(D2D1\_BEZIER\_SEGMENT&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometrysink-addbezier(constd2d1_bezier_segment_))</span></span>  | <span data-ttu-id="8072e-110">Создает кривую Безье третьего порядка между текущей и заданной конечной точками.</span><span class="sxs-lookup"><span data-stu-id="8072e-110">Creates a cubic Bezier curve between the current point and the specified end point.</span></span><br/> |
| <span data-ttu-id="8072e-111">[**Аддбезиер ( \_ сегмент Безье \_ D2D1 \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometrysink-addbezier(constd2d1_bezier_segment))</span><span class="sxs-lookup"><span data-stu-id="8072e-111">[**AddBezier(D2D1\_BEZIER\_SEGMENT\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometrysink-addbezier(constd2d1_bezier_segment))</span></span> | <span data-ttu-id="8072e-112">Создает кривую Безье третьего порядка между текущей точкой и указанной конечной точкой.</span><span class="sxs-lookup"><span data-stu-id="8072e-112">Creates a cubic Bezier curve between the current point and the specified endpoint.</span></span><br/>  |



## <a name="examples"></a><span data-ttu-id="8072e-113">Примеры</span><span class="sxs-lookup"><span data-stu-id="8072e-113">Examples</span></span>

<span data-ttu-id="8072e-114">В следующем примере создается [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry), извлекается приемник и используется для определения формы песочных часов.</span><span class="sxs-lookup"><span data-stu-id="8072e-114">The following example creates an [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry), retrieves a sink, and uses it to define an hourglass shape.</span></span> <span data-ttu-id="8072e-115">Полный пример см. в разделе [Рисование и заполнение сложной фигуры](how-to-draw-and-fill-a-complex-shape.md).</span><span class="sxs-lookup"><span data-stu-id="8072e-115">For the complete example, see [How to Draw and Fill a Complex Shape](how-to-draw-and-fill-a-complex-shape.md).</span></span>


```C++
ID2D1GeometrySink *pSink = NULL;



// Create a path geometry.
if (SUCCEEDED(hr))
{
    hr = m_pD2DFactory->CreatePathGeometry(&m_pPathGeometry);

    if (SUCCEEDED(hr))
    {
        // Write to the path geometry using the geometry sink.
        hr = m_pPathGeometry->Open(&pSink);

        if (SUCCEEDED(hr))
        {
            pSink->BeginFigure(
                D2D1::Point2F(0, 0),
                D2D1_FIGURE_BEGIN_FILLED
                );

            pSink->AddLine(D2D1::Point2F(200, 0));

            pSink->AddBezier(
                D2D1::BezierSegment(
                    D2D1::Point2F(150, 50),
                    D2D1::Point2F(150, 150),
                    D2D1::Point2F(200, 200))
                );

            pSink->AddLine(D2D1::Point2F(0, 200));

            pSink->AddBezier(
                D2D1::BezierSegment(
                    D2D1::Point2F(50, 150),
                    D2D1::Point2F(50, 50),
                    D2D1::Point2F(0, 0))
                );

            pSink->EndFigure(D2D1_FIGURE_END_CLOSED);

            hr = pSink->Close();
        }
        SafeRelease(&pSink);
    }
}
```





## <a name="requirements"></a><span data-ttu-id="8072e-116">Требования</span><span class="sxs-lookup"><span data-stu-id="8072e-116">Requirements</span></span>



| <span data-ttu-id="8072e-117">Требование</span><span class="sxs-lookup"><span data-stu-id="8072e-117">Requirement</span></span> | <span data-ttu-id="8072e-118">Значение</span><span class="sxs-lookup"><span data-stu-id="8072e-118">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="8072e-119">Header</span><span class="sxs-lookup"><span data-stu-id="8072e-119">Header</span></span><br/>  | <dl> <span data-ttu-id="8072e-120"><dt>D2d1. h</dt></span><span class="sxs-lookup"><span data-stu-id="8072e-120"><dt>D2d1.h</dt></span></span> </dl>   |
| <span data-ttu-id="8072e-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="8072e-121">Library</span></span><br/> | <dl> <span data-ttu-id="8072e-122"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8072e-122"><dt>D2d1.lib</dt></span></span> </dl> |
| <span data-ttu-id="8072e-123">DLL</span><span class="sxs-lookup"><span data-stu-id="8072e-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="8072e-124"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8072e-124"><dt>D2d1.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8072e-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8072e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8072e-126">**ID2D1GeometrySink**</span><span class="sxs-lookup"><span data-stu-id="8072e-126">**ID2D1GeometrySink**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink)
</dt> </dl>

<span data-ttu-id="8072e-127">�</span><span class="sxs-lookup"><span data-stu-id="8072e-127">�</span></span>

<span data-ttu-id="8072e-128">�</span><span class="sxs-lookup"><span data-stu-id="8072e-128">�</span></span>
