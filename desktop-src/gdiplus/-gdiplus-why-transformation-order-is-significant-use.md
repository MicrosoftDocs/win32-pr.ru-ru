---
description: Один объект Matrix может хранить одно преобразование или последовательность преобразований.
ms.assetid: 1dc68ff8-6b17-4934-82da-ab2fc612aafa
title: Значение порядка преобразований
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a7350d63456902ff47183faa08170b3b2fef481
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984424"
---
# <a name="why-transformation-order-is-significant"></a><span data-ttu-id="81d15-103">Значение порядка преобразований</span><span class="sxs-lookup"><span data-stu-id="81d15-103">Why Transformation Order Is Significant</span></span>

<span data-ttu-id="81d15-104">Один объект [**Matrix**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) может хранить одно преобразование или последовательность преобразований.</span><span class="sxs-lookup"><span data-stu-id="81d15-104">A single [**Matrix**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) object can store a single transformation or a sequence of transformations.</span></span> <span data-ttu-id="81d15-105">Последнее называется *составным*  *преобразованием*.</span><span class="sxs-lookup"><span data-stu-id="81d15-105">The latter is called a *composite*  *transformation*.</span></span> <span data-ttu-id="81d15-106">Матрица составного преобразования получается путем умножения матриц отдельных преобразований.</span><span class="sxs-lookup"><span data-stu-id="81d15-106">The matrix of a composite transformation is obtained by multiplying the matrices of the individual transformations.</span></span>

<span data-ttu-id="81d15-107">В составном преобразовании важен порядок отдельных преобразований.</span><span class="sxs-lookup"><span data-stu-id="81d15-107">In a composite transformation, the order of the individual transformations is important.</span></span> <span data-ttu-id="81d15-108">Например, если сначала повернуть, затем масштабировать, а затем преобразовать, вы получите другой результат, чем при первом переводе, при повороте, а затем при масштабировании.</span><span class="sxs-lookup"><span data-stu-id="81d15-108">For example, if you first rotate, then scale, then translate, you get a different result than if you first translate, then rotate, then scale.</span></span> <span data-ttu-id="81d15-109">В Windows GDI+ составные преобразования строятся слева направо.</span><span class="sxs-lookup"><span data-stu-id="81d15-109">In Windows GDI+, composite transformations are built from left to right.</span></span> <span data-ttu-id="81d15-110">Если S, R и T являются матрицами масштабирования, вращения и перевода соответственно, то продукт SRT (в таком порядке) является матрицей составного преобразования, которое сначала масштабируется, затем поворачивается, а затем преобразуется.</span><span class="sxs-lookup"><span data-stu-id="81d15-110">If S, R, and T are scale, rotation, and translation matrices respectively, then the product SRT (in that order) is the matrix of the composite transformation that first scales, then rotates, then translates.</span></span> <span data-ttu-id="81d15-111">Матрица, формируемая продуктом SRT, отличается от матрицы, созданной ТРСом продукта.</span><span class="sxs-lookup"><span data-stu-id="81d15-111">The matrix produced by the product SRT is different from the matrix produced by the product TRS.</span></span>

<span data-ttu-id="81d15-112">Один из причин важен в том, что преобразования, такие как вращение и масштабирование, выполняются по отношению к источнику системы координат.</span><span class="sxs-lookup"><span data-stu-id="81d15-112">One reason order is significant is that transformations like rotation and scaling are done with respect to the origin of the coordinate system.</span></span> <span data-ttu-id="81d15-113">Масштабирование объекта, центрированного по отношению к источнику, приводит к другому результату, чем масштабирование объекта, перемещенного из источника.</span><span class="sxs-lookup"><span data-stu-id="81d15-113">Scaling an object that is centered at the origin produces a different result than scaling an object that has been moved away from the origin.</span></span> <span data-ttu-id="81d15-114">Аналогично, поворот объекта, центрированного по отношению к источнику, приводит к результату, отличному от поворота объекта, который был перемещен от источника.</span><span class="sxs-lookup"><span data-stu-id="81d15-114">Similarly, rotating an object that is centered at the origin produces a different result than rotating an object that has been moved away from the origin.</span></span>

<span data-ttu-id="81d15-115">Следующий пример сочетает масштабирование, поворот и преобразование (в этом порядке) для формирования составного преобразования.</span><span class="sxs-lookup"><span data-stu-id="81d15-115">The following example combines scaling, rotation and translation (in that order) to form a composite transformation.</span></span> <span data-ttu-id="81d15-116">Аргумент [\* \* \* \* матриксордераппенд \*](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-matrixorder) \* \* \*, передаваемый методу [**Graphics:: RotateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-rotatetransform) , указывает, что поворот будет следовать за масштабированием.</span><span class="sxs-lookup"><span data-stu-id="81d15-116">The argument [\*\*\*\*MatrixOrderAppend\*\*\*\*](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-matrixorder) passed to the [**Graphics::RotateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-rotatetransform) method specifies that the rotation will follow the scaling.</span></span> <span data-ttu-id="81d15-117">Аналогичным образом, аргумент [\* \* \* \* матриксордераппенд \*](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-matrixorder) \* \* \*, передаваемый методу [**Graphics:: TranslateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-translatetransform) , указывает, что перевод будет следовать за поворотом.</span><span class="sxs-lookup"><span data-stu-id="81d15-117">Likewise, the argument [\*\*\*\*MatrixOrderAppend\*\*\*\*](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-matrixorder) passed to the [**Graphics::TranslateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-translatetransform) method specifies that the translation will follow the rotation.</span></span>


```
Rect rect(0, 0, 50, 50);
Pen pen(Color(255, 255, 0, 0), 0);
graphics.ScaleTransform(1.75f, 0.5f);
graphics.RotateTransform(28.0f, MatrixOrderAppend);
graphics.TranslateTransform(150.0f, 150.0f, MatrixOrderAppend);
graphics.DrawRectangle(&pen, rect);
```



<span data-ttu-id="81d15-118">В следующем примере выполняется вызов тех же методов, что и в предыдущем примере, но порядок вызовов обращен.</span><span class="sxs-lookup"><span data-stu-id="81d15-118">The following example makes the same method calls as the previous example, but the order of the calls is reversed.</span></span> <span data-ttu-id="81d15-119">Полученный порядок операций сначала преобразуется, затем поворачивается, затем масштабируется, что приводит к значительному результату, чем при первом масштабировании, затем поворачивается, а затем преобразуется:</span><span class="sxs-lookup"><span data-stu-id="81d15-119">The resulting order of operations is first translate, then rotate, then scale, which produces a very different result than first scale, then rotate, then translate:</span></span>


```
Rect rect(0, 0, 50, 50);
Pen pen(Color(255, 255, 0, 0), 0);
graphics.TranslateTransform(150.0f, 150.0f);
graphics.RotateTransform(28.0f, MatrixOrderAppend);
graphics.ScaleTransform(1.75f, 0.5f, MatrixOrderAppend);
graphics.DrawRectangle(&pen, rect);
```



<span data-ttu-id="81d15-120">Один из способов изменения порядка отдельных преобразований в составных преобразованиях заключается в том, чтобы обратить порядок последовательности вызовов методов.</span><span class="sxs-lookup"><span data-stu-id="81d15-120">One way to reverse the order of the individual transformations in a composite transformation is to reverse the order of a sequence of method calls.</span></span> <span data-ttu-id="81d15-121">Вторым способом управления порядком операций является изменение аргумента порядка матриц.</span><span class="sxs-lookup"><span data-stu-id="81d15-121">A second way to control the order of operations is to change the matrix order argument.</span></span> <span data-ttu-id="81d15-122">Следующий пример аналогичен предыдущему, за исключением того, что [\* \* \* \* матриксордераппенд \* \*](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-matrixorder) \* \* был изменен на \* \* \* \* [матриксордерпрепенд \* \*](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-matrixorder)\* \*.</span><span class="sxs-lookup"><span data-stu-id="81d15-122">The following example is the same as the previous example, except that [\*\*\*\*MatrixOrderAppend\*\*\*\*](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-matrixorder) has been changed to [\*\*\*\*MatrixOrderPrepend\*\*\*\*](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-matrixorder).</span></span> <span data-ttu-id="81d15-123">Умножение матрицы выполняется в порядке SRT, где S, R и T являются матрицами для масштабирования, вращения и преобразования соответственно.</span><span class="sxs-lookup"><span data-stu-id="81d15-123">The matrix multiplication is done in the order SRT, where S, R, and T are the matrices for scale, rotate, and translate, respectively.</span></span> <span data-ttu-id="81d15-124">Порядок составного преобразования сначала масштабируется, затем поворачивается, а затем преобразуется.</span><span class="sxs-lookup"><span data-stu-id="81d15-124">The order of the composite transformation is first scale, then rotate, then translate.</span></span>


```
Rect rect(0, 0, 50, 50);
Pen pen(Color(255, 255, 0, 0), 0);
graphics.TranslateTransform(150.0f, 150.0f,MatrixOrderPrepend);
graphics.RotateTransform(28.0f, MatrixOrderPrepend);
graphics.ScaleTransform(1.75f, 0.5f, MatrixOrderPrepend);
graphics.DrawRectangle(&pen, rect);
```



<span data-ttu-id="81d15-125">Результатом предыдущего примера является тот же результат, что и в первом примере этого раздела.</span><span class="sxs-lookup"><span data-stu-id="81d15-125">The result of the preceding example is the same result that we achieved in the first example of this section.</span></span> <span data-ttu-id="81d15-126">Это обусловлено тем, что мы отменяем порядок вызовов методов и порядок умножения матриц.</span><span class="sxs-lookup"><span data-stu-id="81d15-126">This is because we reversed both the order of the method calls and the order of the matrix multiplication.</span></span>

 

 



