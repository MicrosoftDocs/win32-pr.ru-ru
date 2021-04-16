---
title: ID2D1Geometry Компутеареа методы
description: Выполняет вычисление области геометрии.
ms.assetid: 655f11bc-7435-4d23-b4b1-3d7c2110aa48
keywords:
- Методы Компутеареа Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: f6b79e8434a2174bcb05659f6656a46cc2d43cbb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680023"
---
# <a name="id2d1geometrycomputearea-methods"></a><span data-ttu-id="f63bc-104">Методы ID2D1Geometry:: Компутеареа</span><span class="sxs-lookup"><span data-stu-id="f63bc-104">ID2D1Geometry::ComputeArea methods</span></span>

<span data-ttu-id="f63bc-105">Выполняет вычисление области геометрии.</span><span class="sxs-lookup"><span data-stu-id="f63bc-105">Computes the area of the geometry.</span></span>

### <a name="overload-list"></a><span data-ttu-id="f63bc-106">Список перегрузок</span><span class="sxs-lookup"><span data-stu-id="f63bc-106">Overload list</span></span>



| <span data-ttu-id="f63bc-107">Метод</span><span class="sxs-lookup"><span data-stu-id="f63bc-107">Method</span></span>                                                                                                                      | <span data-ttu-id="f63bc-108">Описание</span><span class="sxs-lookup"><span data-stu-id="f63bc-108">Description</span></span>                                                                                                                                      |
|:----------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f63bc-109">[**Компутеареа (D2D1 \_ Matrix \_ 3X2 \_ F&, float \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computearea(constd2d1_matrix_3x2_f__float))</span><span class="sxs-lookup"><span data-stu-id="f63bc-109">[**ComputeArea(D2D1\_MATRIX\_3X2\_F&,FLOAT\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computearea(constd2d1_matrix_3x2_f__float))</span></span>              | <span data-ttu-id="f63bc-110">Выполняет вычисление области геометрии после преобразования указанной матрицы и плоской с использованием отклонения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f63bc-110">Computes the area of the geometry after it has been transformed by the specified matrix and flattened using the default tolerance.</span></span><br/>    |
| <span data-ttu-id="f63bc-111">[**Компутеареа (D2D1 \_ Matrix \_ 3X2 \_ F \* , float \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computearea(constd2d1_matrix_3x2_f_float))</span><span class="sxs-lookup"><span data-stu-id="f63bc-111">[**ComputeArea(D2D1\_MATRIX\_3X2\_F\*,FLOAT\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computearea(constd2d1_matrix_3x2_f_float))</span></span>             | <span data-ttu-id="f63bc-112">Выполняет вычисление области геометрии после ее преобразования в указанную матрицу и плоской с использованием отклонения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f63bc-112">Computes the area of the geometry after it has been transformed by the specified matrix and flattened by using the default tolerance.</span></span><br/> |
| <span data-ttu-id="f63bc-113">[**Компутеареа (D2D1 \_ Matrix \_ 3X2 \_ F&, float, float \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computearea(constd2d1_matrix_3x2_f__float_float))</span><span class="sxs-lookup"><span data-stu-id="f63bc-113">[**ComputeArea(D2D1\_MATRIX\_3X2\_F&,FLOAT,FLOAT\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computearea(constd2d1_matrix_3x2_f__float_float))</span></span>  | <span data-ttu-id="f63bc-114">Выполняет вычисление области геометрии после преобразования указанной матрицы и плоской с использованием указанного допуска.</span><span class="sxs-lookup"><span data-stu-id="f63bc-114">Computes the area of the geometry after it has been transformed by the specified matrix and flattened using the specified tolerance.</span></span><br/>  |
| <span data-ttu-id="f63bc-115">[**Компутеареа (D2D1 \_ Matrix \_ 3X2 \_ F \* , float, float \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computearea(constd2d1_matrix_3x2_f_float))</span><span class="sxs-lookup"><span data-stu-id="f63bc-115">[**ComputeArea(D2D1\_MATRIX\_3X2\_F\*,FLOAT,FLOAT\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computearea(constd2d1_matrix_3x2_f_float))</span></span> | <span data-ttu-id="f63bc-116">Выполняет вычисление области геометрии после преобразования указанной матрицы и плоской с использованием указанного допуска.</span><span class="sxs-lookup"><span data-stu-id="f63bc-116">Computes the area of the geometry after it has been transformed by the specified matrix and flattened using the specified tolerance.</span></span><br/>  |



## <a name="examples"></a><span data-ttu-id="f63bc-117">Примеры</span><span class="sxs-lookup"><span data-stu-id="f63bc-117">Examples</span></span>

<span data-ttu-id="f63bc-118">В следующем примере кода используется **компутеареа** для вычислить площадь указанного круга (**m \_ pCircleGeometry1**).</span><span class="sxs-lookup"><span data-stu-id="f63bc-118">The following code example uses **ComputeArea** to compute the area of a specified circle (**m\_pCircleGeometry1**).</span></span>


```C++
float area;

// Compute the area of circle1
hr = m_pCircleGeometry1->ComputeArea(
    D2D1::IdentityMatrix(),
    &area
    );
```



## <a name="requirements"></a><span data-ttu-id="f63bc-119">Требования</span><span class="sxs-lookup"><span data-stu-id="f63bc-119">Requirements</span></span>



| <span data-ttu-id="f63bc-120">Требование</span><span class="sxs-lookup"><span data-stu-id="f63bc-120">Requirement</span></span> | <span data-ttu-id="f63bc-121">Значение</span><span class="sxs-lookup"><span data-stu-id="f63bc-121">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="f63bc-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f63bc-122">Library</span></span><br/> | <dl> <span data-ttu-id="f63bc-123"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f63bc-123"><dt>D2d1.lib</dt></span></span> </dl> |
| <span data-ttu-id="f63bc-124">DLL</span><span class="sxs-lookup"><span data-stu-id="f63bc-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="f63bc-125"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f63bc-125"><dt>D2d1.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f63bc-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f63bc-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f63bc-127">**ID2D1Geometry**</span><span class="sxs-lookup"><span data-stu-id="f63bc-127">**ID2D1Geometry**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry)
</dt> </dl>

 

