---
description: '\#Матрица m&215; n представляет собой набор чисел, упорядоченных по m строкам и n столбцам. На следующем рисунке показаны несколько матриц.'
ms.assetid: 62215ae0-b095-42b2-911c-aa7607a8b61a
title: Матричное представление преобразований
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0577cae38c401e842cff2ff14179594f9118dfd2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809652"
---
# <a name="matrix-representation-of-transformations"></a><span data-ttu-id="66e76-104">Матричное представление преобразований</span><span class="sxs-lookup"><span data-stu-id="66e76-104">Matrix Representation of Transformations</span></span>

<span data-ttu-id="66e76-105">Матрица размером *m × n* представляет собой набор чисел, упорядоченных по *m* строкам и *n* столбцам.</span><span class="sxs-lookup"><span data-stu-id="66e76-105">An *m×n* matrix is a set of numbers arranged in *m* rows and *n* columns.</span></span> <span data-ttu-id="66e76-106">На следующем рисунке показаны несколько матриц.</span><span class="sxs-lookup"><span data-stu-id="66e76-106">The following illustration shows several matrices.</span></span>

![Иллюстрация, демонстрирующая шесть матриц различных измерений](images/aboutgdip05-art04.png)

<span data-ttu-id="66e76-108">Можно добавить две матрицы одного размера, добавив отдельные элементы.</span><span class="sxs-lookup"><span data-stu-id="66e76-108">You can add two matrices of the same size by adding individual elements.</span></span> <span data-ttu-id="66e76-109">На следующем рисунке показаны два примера добавления матрицы.</span><span class="sxs-lookup"><span data-stu-id="66e76-109">The following illustration shows two examples of matrix addition.</span></span>

![Иллюстрация, показывающий, как выполнить добавление матрицы](images/aboutgdip05-art05.png)

<span data-ttu-id="66e76-111">Матрицу размером *m × n* можно умножить на матрицу *n × p* , а результатом будет матрица *m × p* .</span><span class="sxs-lookup"><span data-stu-id="66e76-111">An *m×n* matrix can be multiplied by an *n×p* matrix, and the result is an *m×p* matrix.</span></span> <span data-ttu-id="66e76-112">Число столбцов в первой матрице должно совпадать с количеством строк во второй матрице.</span><span class="sxs-lookup"><span data-stu-id="66e76-112">The number of columns in the first matrix must be the same as the number of rows in the second matrix.</span></span> <span data-ttu-id="66e76-113">Например, матрицу размером 4 × 2 можно умножить на матрицу размером 2 × 3, чтобы создать матрицу размером 4 × 3.</span><span class="sxs-lookup"><span data-stu-id="66e76-113">For example, a 4 ×2 matrix can be multiplied by a 2 ×3 matrix to produce a 4 ×3 matrix.</span></span>

<span data-ttu-id="66e76-114">Точки в плоскости, а также строки и столбцы матрицы можно рассматривать как векторы.</span><span class="sxs-lookup"><span data-stu-id="66e76-114">Points in the plane and rows and columns of a matrix can be thought of as vectors.</span></span> <span data-ttu-id="66e76-115">Например, (2, 5) — это вектор с двумя компонентами, а (3, 7, 1) — вектор с тремя компонентами.</span><span class="sxs-lookup"><span data-stu-id="66e76-115">For example, (2, 5) is a vector with two components, and (3, 7, 1) is a vector with three components.</span></span> <span data-ttu-id="66e76-116">Скалярное произведение двух векторов определяется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="66e76-116">The dot product of two vectors is defined as follows:</span></span>

<span data-ttu-id="66e76-117">(a, б) • (c, d) = AC + BD</span><span class="sxs-lookup"><span data-stu-id="66e76-117">(a, b) • (c, d) = ac + bd</span></span>

<span data-ttu-id="66e76-118">(a, b, c) • (d, e, f) = AD + быть + CF</span><span class="sxs-lookup"><span data-stu-id="66e76-118">(a, b, c) • (d, e, f) = ad + be + cf</span></span>

<span data-ttu-id="66e76-119">Например, точка произведения (2, 3) и (5, 4) имеет значение (2) (5) + (3) (4) = 22.</span><span class="sxs-lookup"><span data-stu-id="66e76-119">For example, the dot product of (2, 3) and (5, 4) is (2)(5) + (3)(4) = 22.</span></span> <span data-ttu-id="66e76-120">Скалярное произведение (2, 5, 1) и (4, 3, 1) равно (2) (4) + (5) (3) + (1) (1) = 24.</span><span class="sxs-lookup"><span data-stu-id="66e76-120">The dot product of (2, 5, 1) and (4, 3, 1) is (2)(4) + (5)(3) + (1)(1) = 24.</span></span> <span data-ttu-id="66e76-121">Обратите внимание, что скалярное произведение двух векторов является числом, а не другим вектором.</span><span class="sxs-lookup"><span data-stu-id="66e76-121">Note that the dot product of two vectors is a number, not another vector.</span></span> <span data-ttu-id="66e76-122">Также обратите внимание, что можно вычислить значение с точкой, только если два вектора имеют одинаковое число компонентов.</span><span class="sxs-lookup"><span data-stu-id="66e76-122">Also note that you can calculate the dot product only if the two vectors have the same number of components.</span></span>

<span data-ttu-id="66e76-123">Позвольте A (i, j) быть записью в матрице A **в строке i** и j **th** .</span><span class="sxs-lookup"><span data-stu-id="66e76-123">Let A(i, j) be the entry in matrix A in the i **th** row and the j **th** column.</span></span> <span data-ttu-id="66e76-124">Например, A (3, 2) — это запись в матрице A в строке 3 на рабочем **столе** и в столбце 2 **ND** .</span><span class="sxs-lookup"><span data-stu-id="66e76-124">For example A(3, 2) is the entry in matrix A in the 3 **rd** row and the 2 **nd** column.</span></span> <span data-ttu-id="66e76-125">Предположим, что A, B и C являются матрицами, а AB = C. Записи в языке C рассчитываются следующим образом:</span><span class="sxs-lookup"><span data-stu-id="66e76-125">Suppose A, B, and C are matrices, and AB = C. The entries of C are calculated as follows:</span></span>

<span data-ttu-id="66e76-126">C (i, j) = (строка i из A) • (столбец j из B)</span><span class="sxs-lookup"><span data-stu-id="66e76-126">C(i, j) = (row i of A) • (column j of B)</span></span>

<span data-ttu-id="66e76-127">На следующем рисунке показано несколько примеров перемножения матриц.</span><span class="sxs-lookup"><span data-stu-id="66e76-127">The following illustration shows several examples of matrix multiplication.</span></span>

![Иллюстрация, показывающая, как выполнить умножение матрицы](images/aboutgdip05-art06.png)

<span data-ttu-id="66e76-129">Если вы считаете, что точка в плоскости является матрицей размером 1 × 2, можно преобразовать эту точку, умножив ее на матрицу размером 2 × 2.</span><span class="sxs-lookup"><span data-stu-id="66e76-129">If you think of a point in the plane as a 1 × 2 matrix, you can transform that point by multiplying it by a 2 × 2 matrix.</span></span> <span data-ttu-id="66e76-130">На следующем рисунке показано несколько преобразований, примененных к точке (2, 1).</span><span class="sxs-lookup"><span data-stu-id="66e76-130">The following illustration shows several transformations applied to the point (2, 1).</span></span>

![Иллюстрация, в которой показано, как использовать умножение матрицы для масштабирования, вращения или отражения точки в плоскости](images/aboutgdip05-art07.png)

<span data-ttu-id="66e76-132">Все преобразования, показанные на предыдущем рисунке, являются линейными преобразованиями.</span><span class="sxs-lookup"><span data-stu-id="66e76-132">All the transformations shown in the previous figure are linear transformations.</span></span> <span data-ttu-id="66e76-133">Некоторые другие преобразования, такие как перевод, не являются линейными и не могут быть выражены умножением матрицы 2 × 2.</span><span class="sxs-lookup"><span data-stu-id="66e76-133">Certain other transformations, such as translation, are not linear, and cannot be expressed as multiplication by a 2 × 2 matrix.</span></span> <span data-ttu-id="66e76-134">Предположим, что вы хотите начать с точки (2, 1), повернуть ее 90 градусов, перевести 3 единицы в направлении x и перевести 4 единицы в направлении по оси y.</span><span class="sxs-lookup"><span data-stu-id="66e76-134">Suppose you want to start with the point (2, 1), rotate it 90 degrees, translate it 3 units in the x direction, and translate it 4 units in the y direction.</span></span> <span data-ttu-id="66e76-135">Это можно сделать, выполнив умножение матрицы, за которым следует Добавление матрицы.</span><span class="sxs-lookup"><span data-stu-id="66e76-135">You can accomplish this by performing a matrix multiplication followed by a matrix addition.</span></span>

![Иллюстрация, показывающая, как умножение и сложение матрицы могут поворачивать точку и преобразовывать ее дважды](images/aboutgdip05-art08.png)

<span data-ttu-id="66e76-137">Линейное преобразование (умножение матрицы 2 × 2), за которым следует перевод (сложение матрицы размером 1 × 2), называется аффинное преобразованием.</span><span class="sxs-lookup"><span data-stu-id="66e76-137">A linear transformation (multiplication by a 2 × 2 matrix) followed by a translation (addition of a 1 × 2 matrix) is called an affine transformation.</span></span> <span data-ttu-id="66e76-138">Альтернатива хранению аффинных преобразований в паре матриц (одна для линейной части и другая для перевода) заключается в хранении всего преобразования в матрице размером 3 × 3.</span><span class="sxs-lookup"><span data-stu-id="66e76-138">An alternative to storing an affine transformation in a pair of matrices (one for the linear part and one for the translation) is to store the entire transformation in a 3 × 3 matrix.</span></span> <span data-ttu-id="66e76-139">Чтобы сделать эту работу, точка на плоскости должна храниться в матрице размером 1 × 3 с фиктивной третьей координатой.</span><span class="sxs-lookup"><span data-stu-id="66e76-139">To make this work, a point in the plane must be stored in a 1 × 3 matrix with a dummy 3rd coordinate.</span></span> <span data-ttu-id="66e76-140">Обычная методика — сделать все 3 Координаты равными 1.</span><span class="sxs-lookup"><span data-stu-id="66e76-140">The usual technique is to make all 3rd coordinates equal to 1.</span></span> <span data-ttu-id="66e76-141">Например, точка (2, 1) представлена матрицей \[ 2 1 1 \] .</span><span class="sxs-lookup"><span data-stu-id="66e76-141">For example, the point (2, 1) is represented by the matrix \[2 1 1\].</span></span> <span data-ttu-id="66e76-142">На следующем рисунке показано аффинное преобразование (поворот 90 градусов; сдвиг на три единицы в направлении по оси x, 4 единицы в направлении оси y), выраженный в виде умножения на одну матрицу размером 3 × 3.</span><span class="sxs-lookup"><span data-stu-id="66e76-142">The following illustration shows an affine transformation (rotate 90 degrees; translate 3 units in the x direction, 4 units in the y direction) expressed as multiplication by a single 3 × 3 matrix.</span></span>

![Иллюстрация, показывающая, как перемножение матрицы может выполнить аффинное преобразование](images/aboutgdip05-art09.png)

<span data-ttu-id="66e76-144">В предыдущем примере точка (2, 1) сопоставляется с точкой (2, 6).</span><span class="sxs-lookup"><span data-stu-id="66e76-144">In the previous example, the point (2, 1) is mapped to the point (2, 6).</span></span> <span data-ttu-id="66e76-145">Обратите внимание, что третий столбец матрицы размером 3 × 3 содержит числа 0, 0, 1.</span><span class="sxs-lookup"><span data-stu-id="66e76-145">Note that the third column of the 3 × 3 matrix contains the numbers 0, 0, 1.</span></span> <span data-ttu-id="66e76-146">Это всегда будет иметь место для матрицы аффинного преобразования, 3 × 3.</span><span class="sxs-lookup"><span data-stu-id="66e76-146">This will always be the case for the 3 × 3 matrix of an affine transformation.</span></span> <span data-ttu-id="66e76-147">Важные числа — это шесть чисел в столбцах 1 и 2.</span><span class="sxs-lookup"><span data-stu-id="66e76-147">The important numbers are the six numbers in columns 1 and 2.</span></span> <span data-ttu-id="66e76-148">Верхняя левая часть матрицы 2 × 2 представляет линейную часть преобразования, а первые две записи в третьей строке представляют перевод.</span><span class="sxs-lookup"><span data-stu-id="66e76-148">The upper-left 2 × 2 portion of the matrix represents the linear part of the transformation, and the first two entries in the 3rd row represent the translation.</span></span>

![Иллюстрация, показывающая, что первые два столбца наиболее важны для матрицы 3x3 с аффинное преобразованием](images/aboutgdip05-art10.png)

<span data-ttu-id="66e76-150">В Windows GDI+ можно сохранить аффинное преобразование в объекте [**Matrix**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) .</span><span class="sxs-lookup"><span data-stu-id="66e76-150">In Windows GDI+ you can store an affine transformation in a [**Matrix**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) object.</span></span> <span data-ttu-id="66e76-151">Поскольку третий столбец матрицы, представляющий аффинное преобразование, всегда имеет значение (0, 0, 1), при построении объекта **Matrix** в первых двух столбцах указывается только шесть чисел.</span><span class="sxs-lookup"><span data-stu-id="66e76-151">Because the third column of a matrix that represents an affine transformation is always (0, 0, 1), you specify only the six numbers in the first two columns when you construct a **Matrix** object.</span></span> <span data-ttu-id="66e76-152">Оператор `Matrix myMatrix(0.0f, 1.0f, -1.0f, 0.0f, 3.0f, 4.0f);` конструирует матрицу, показанную на предыдущем рисунке.</span><span class="sxs-lookup"><span data-stu-id="66e76-152">The statement `Matrix myMatrix(0.0f, 1.0f, -1.0f, 0.0f, 3.0f, 4.0f);` constructs the matrix shown in the previous figure.</span></span>

## <a name="composite-transformations"></a><span data-ttu-id="66e76-153">Составные преобразования</span><span class="sxs-lookup"><span data-stu-id="66e76-153">Composite Transformations</span></span>

<span data-ttu-id="66e76-154">Составное преобразование — это последовательность преобразований, в одну за которой следуют другие.</span><span class="sxs-lookup"><span data-stu-id="66e76-154">A composite transformation is a sequence of transformations, one followed by the other.</span></span> <span data-ttu-id="66e76-155">Рассмотрим матрицы и преобразования в следующем списке:</span><span class="sxs-lookup"><span data-stu-id="66e76-155">Consider the matrices and transformations in the following list:</span></span>

-   <span data-ttu-id="66e76-156">Матрица A-вращение на повороте на 90 градусов</span><span class="sxs-lookup"><span data-stu-id="66e76-156">Matrix A    Rotate 90 degrees</span></span>
-   <span data-ttu-id="66e76-157">Матрица B. масштабирование по коэффициенту 2 в направлении x</span><span class="sxs-lookup"><span data-stu-id="66e76-157">Matrix B    Scale by a factor of 2 in the x direction</span></span>
-   <span data-ttu-id="66e76-158">Матрица C переводом 3 единицы по оси y</span><span class="sxs-lookup"><span data-stu-id="66e76-158">Matrix C    Translate 3 units in the y direction</span></span>

<span data-ttu-id="66e76-159">Если начать с точки (2, 1), представленной матрицей \[ 2 1 1 \] , и умножить ее на, то B, затем на C, точка (2, 1) пройдет три преобразования в указанном порядке.</span><span class="sxs-lookup"><span data-stu-id="66e76-159">If you start with the point (2, 1) — represented by the matrix \[2 1 1\] — and multiply by A, then B, then C, the point (2,1) will undergo the three transformations in the order listed.</span></span>

<span data-ttu-id="66e76-160">\[2 1 1 \] ABC = \[ – 2 5 1\]</span><span class="sxs-lookup"><span data-stu-id="66e76-160">\[2 1 1\]ABC = \[ –2 5 1\]</span></span>

<span data-ttu-id="66e76-161">Вместо того чтобы хранить три части составного преобразования в трех отдельных матрицах, можно умножить, B и C, чтобы получить одну матрицу размером 3 × 3, которая хранит все составное преобразование.</span><span class="sxs-lookup"><span data-stu-id="66e76-161">Rather than store the three parts of the composite transformation in three separate matrices, you can multiply A, B, and C together to get a single 3 × 3 matrix that stores the entire composite transformation.</span></span> <span data-ttu-id="66e76-162">Предположим, ABC = D. Затем точка, умноженная на D, дает тот же результат, что и точка, умноженная на, а затем на B, а затем на C.</span><span class="sxs-lookup"><span data-stu-id="66e76-162">Suppose ABC = D. Then a point multiplied by D gives the same result as a point multiplied by A, then B, then C.</span></span>

<span data-ttu-id="66e76-163">\[2 1 1 \] D = \[ – 2 5 1\]</span><span class="sxs-lookup"><span data-stu-id="66e76-163">\[2 1 1\]D = \[ –2 5 1\]</span></span>

<span data-ttu-id="66e76-164">На следующем рисунке показаны матрицы A, B, C и D.</span><span class="sxs-lookup"><span data-stu-id="66e76-164">The following illustration shows the matrices A, B, C, and D.</span></span>

![Иллюстрация, демонстрирующая выполнение нескольких преобразований путем умножения составляющих матриц](images/aboutgdip05-art12.png)

<span data-ttu-id="66e76-166">Тот факт, что матрица составного преобразования может быть сформирована путем умножения отдельных матриц преобразования, означает, что любая последовательность аффинных преобразований может храниться в одном объекте [**матрицы**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) .</span><span class="sxs-lookup"><span data-stu-id="66e76-166">The fact that the matrix of a composite transformation can be formed by multiplying the individual transformation matrices means that any sequence of affine transformations can be stored in a single [**Matrix**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) object.</span></span>

> [!Note]  
> <span data-ttu-id="66e76-167">Порядок составного преобразования важен.</span><span class="sxs-lookup"><span data-stu-id="66e76-167">The order of a composite transformation is important.</span></span> <span data-ttu-id="66e76-168">Как правило, поворот, масштабирование, преобразование не не отличается от масштабирования, затем поворота и преобразования.</span><span class="sxs-lookup"><span data-stu-id="66e76-168">In general, rotate, then scale, then translate is not the same as scale, then rotate, then translate.</span></span> <span data-ttu-id="66e76-169">Аналогично, важен порядок умножения матриц.</span><span class="sxs-lookup"><span data-stu-id="66e76-169">Similarly, the order of matrix multiplication is important.</span></span> <span data-ttu-id="66e76-170">Как правило, ABC не совпадает с БПЗ.</span><span class="sxs-lookup"><span data-stu-id="66e76-170">In general, ABC is not the same as BAC.</span></span>

 

<span data-ttu-id="66e76-171">Класс [**Matrix**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) предоставляет несколько методов для создания составного преобразования: [**Matrix:: перемножения**](/windows/desktop/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-multiply), [**Matrix:: вращение**](/windows/desktop/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-rotate), [**Матрица:: ротатеат**](/windows/desktop/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-rotateat), [**Матрица:: масштаб**](/windows/desktop/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-scale), [**Матрица:. сдвиг**](/windows/desktop/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-shear)и [**Матрица:: сдвиг**](/windows/desktop/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-translate).</span><span class="sxs-lookup"><span data-stu-id="66e76-171">The [**Matrix**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) class provides several methods for building a composite transformation: [**Matrix::Multiply**](/windows/desktop/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-multiply), [**Matrix::Rotate**](/windows/desktop/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-rotate), [**Matrix::RotateAt**](/windows/desktop/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-rotateat), [**Matrix::Scale**](/windows/desktop/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-scale), [**Matrix::Shear**](/windows/desktop/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-shear), and [**Matrix::Translate**](/windows/desktop/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-translate).</span></span> <span data-ttu-id="66e76-172">В следующем примере создается матрица составного преобразования, которая сначала поворачивает 30 градусов, затем масштабируется по коэффициенту 2 в направлении y, а затем преобразует 5 единиц в направлении x.</span><span class="sxs-lookup"><span data-stu-id="66e76-172">The following example creates the matrix of a composite transformation that first rotates 30 degrees, then scales by a factor of 2 in the y direction, and then translates 5 units in the x direction.</span></span>


```
Matrix myMatrix;
myMatrix.Rotate(30.0f);
myMatrix.Scale(1.0f, 2.0f, MatrixOrderAppend);
myMatrix.Translate(5.0f, 0.0f, MatrixOrderAppend);
```



<span data-ttu-id="66e76-173">На следующем рисунке показана матрица.</span><span class="sxs-lookup"><span data-stu-id="66e76-173">The following illustration shows the matrix.</span></span>

![Иллюстрация, на которой показана матрица со значениями, выраженными в виде тригонометрических функций, и матрица с приблизительными значениями этих функций](images/aboutgdip05-art13.png)

 

 



