---
description: В этом разделе перечислены методы Трансформвекторс класса Matrix. Полный список методов для класса Matrix см. в разделе методы матрицы.
ms.assetid: 6a2ed6a7-825a-422b-b035-b88746f3ab5d
title: Методы Matrix. Трансформвекторс (Гдиплусматрикс. h)
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 3bdb67d839163ffe2d26623a01fc186f8e885ca2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "104987464"
---
# <a name="matrixtransformvectors-methods"></a><span data-ttu-id="efa29-104">Методы Matrix. Трансформвекторс</span><span class="sxs-lookup"><span data-stu-id="efa29-104">Matrix.TransformVectors methods</span></span>

<span data-ttu-id="efa29-105">В этом разделе перечислены методы Трансформвекторс класса [**Matrix**](/windows/win32/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) .</span><span class="sxs-lookup"><span data-stu-id="efa29-105">This topic lists the TransformVectors methods of the [**Matrix**](/windows/win32/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) class.</span></span> <span data-ttu-id="efa29-106">Полный список методов для класса **Matrix** см. в разделе [методы матрицы](-gdiplus-class-matrix-methods.md).</span><span class="sxs-lookup"><span data-stu-id="efa29-106">For a complete list of methods for the **Matrix** class, see [Matrix Methods](-gdiplus-class-matrix-methods.md).</span></span>

### <a name="overload-list"></a><span data-ttu-id="efa29-107">Список перегрузок</span><span class="sxs-lookup"><span data-stu-id="efa29-107">Overload list</span></span>



| <span data-ttu-id="efa29-108">Метод</span><span class="sxs-lookup"><span data-stu-id="efa29-108">Method</span></span>                                                                                                 | <span data-ttu-id="efa29-109">Описание</span><span class="sxs-lookup"><span data-stu-id="efa29-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                      |
|:-------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="efa29-110">[**Трансформвекторс (Point \* , int)**](/windows/win32/api/gdiplusmatrix/nf-gdiplusmatrix-matrix-transformvectors(inoutpoint_inint))</span><span class="sxs-lookup"><span data-stu-id="efa29-110">[**TransformVectors(Point\*,INT)**](/windows/win32/api/gdiplusmatrix/nf-gdiplusmatrix-matrix-transformvectors(inoutpoint_inint))</span></span>   | <span data-ttu-id="efa29-111">Метод [**Matrix:: трансформвекторс**](/windows/win32/api/gdiplusmatrix/nf-gdiplusmatrix-matrix-transformvectors(inoutpoint_inint)) умножает каждый вектор в массиве на эту матрицу.</span><span class="sxs-lookup"><span data-stu-id="efa29-111">The [**Matrix::TransformVectors**](/windows/win32/api/gdiplusmatrix/nf-gdiplusmatrix-matrix-transformvectors(inoutpoint_inint)) method multiplies each vector in an array by this matrix.</span></span> <span data-ttu-id="efa29-112">Элементы смещения данной матрицы (третья строка) игнорируются.</span><span class="sxs-lookup"><span data-stu-id="efa29-112">The translation elements of this matrix (third row) are ignored.</span></span> <span data-ttu-id="efa29-113">Каждый вектор рассматривается как матрица строк.</span><span class="sxs-lookup"><span data-stu-id="efa29-113">Each vector is treated as a row matrix.</span></span> <span data-ttu-id="efa29-114">Умножение выполняется с помощью матрицы строк слева и этой матрицы справа.</span><span class="sxs-lookup"><span data-stu-id="efa29-114">The multiplication is performed with the row matrix on the left and this matrix on the right.</span></span><br/>  |
| <span data-ttu-id="efa29-115">[**Трансформвекторс (PointF \* , int)**](/previous-versions//ms535319(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="efa29-115">[**TransformVectors(PointF\*,INT)**](/previous-versions//ms535319(v=vs.85))</span></span> | <span data-ttu-id="efa29-116">Метод [**Matrix:: трансформвекторс**](/previous-versions//ms535319(v=vs.85)) умножает каждый вектор в массиве на эту матрицу.</span><span class="sxs-lookup"><span data-stu-id="efa29-116">The [**Matrix::TransformVectors**](/previous-versions//ms535319(v=vs.85)) method multiplies each vector in an array by this matrix.</span></span> <span data-ttu-id="efa29-117">Элементы смещения данной матрицы (третья строка) игнорируются.</span><span class="sxs-lookup"><span data-stu-id="efa29-117">The translation elements of this matrix (third row) are ignored.</span></span> <span data-ttu-id="efa29-118">Каждый вектор рассматривается как матрица строк.</span><span class="sxs-lookup"><span data-stu-id="efa29-118">Each vector is treated as a row matrix.</span></span> <span data-ttu-id="efa29-119">Умножение выполняется с помощью матрицы строк слева и этой матрицы справа.</span><span class="sxs-lookup"><span data-stu-id="efa29-119">The multiplication is performed with the row matrix on the left and this matrix on the right.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="efa29-120">Требования</span><span class="sxs-lookup"><span data-stu-id="efa29-120">Requirements</span></span>



| <span data-ttu-id="efa29-121">Требование</span><span class="sxs-lookup"><span data-stu-id="efa29-121">Requirement</span></span> | <span data-ttu-id="efa29-122">Значение</span><span class="sxs-lookup"><span data-stu-id="efa29-122">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="efa29-123">Header</span><span class="sxs-lookup"><span data-stu-id="efa29-123">Header</span></span><br/> | <dl> <span data-ttu-id="efa29-124"><dt>Гдиплусматрикс. h</dt></span><span class="sxs-lookup"><span data-stu-id="efa29-124"><dt>Gdiplusmatrix.h</dt></span></span> </dl> |



 

 
