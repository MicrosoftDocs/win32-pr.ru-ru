---
title: 'Приложение: операции с матрицами'
description: В этом разделе представлен математический Обзор преобразований матрицы для двухмерной графики.
ms.assetid: 8cc01f45-dd84-4f3e-a5f2-26edc5cbdfa1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a5a9b09f75b17e4baf8afe5e7fde8643c06982f
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/28/2021
ms.locfileid: "104557514"
---
# <a name="appendix-matrix-transforms"></a><span data-ttu-id="ea90a-103">Приложение. преобразования матрицы</span><span class="sxs-lookup"><span data-stu-id="ea90a-103">Appendix: Matrix Transforms</span></span>

<span data-ttu-id="ea90a-104">В этом разделе представлен математический Обзор преобразований матрицы для двухмерной графики.</span><span class="sxs-lookup"><span data-stu-id="ea90a-104">This topic provides a mathematical overview of matrix transforms for 2-D graphics.</span></span> <span data-ttu-id="ea90a-105">Однако для использования преобразований в Direct2D вам не нужно знать математические вычисления.</span><span class="sxs-lookup"><span data-stu-id="ea90a-105">However, you don't need to know matrix math in order to use transforms in Direct2D.</span></span> <span data-ttu-id="ea90a-106">Прочтите этот раздел, если вы заинтересованы в математических вычислениях. в противном случае вы можете пропустить этот раздел.</span><span class="sxs-lookup"><span data-stu-id="ea90a-106">Read this topic if you are interested in the math; otherwise, feel free to skip this topic.</span></span>

-   [<span data-ttu-id="ea90a-107">Общие сведения о матрицах</span><span class="sxs-lookup"><span data-stu-id="ea90a-107">Introduction to Matrices</span></span>](#introduction-to-matrices)
    -   [<span data-ttu-id="ea90a-108">Операции с матрицей</span><span class="sxs-lookup"><span data-stu-id="ea90a-108">Matrix Operations</span></span>](#matrix-operations)
-   [<span data-ttu-id="ea90a-109">Аффинных преобразований</span><span class="sxs-lookup"><span data-stu-id="ea90a-109">Affine Transforms</span></span>](#affine-transforms)
    -   [<span data-ttu-id="ea90a-110">Преобразование перевода</span><span class="sxs-lookup"><span data-stu-id="ea90a-110">Translation Transform</span></span>](#translation-transform)
    -   [<span data-ttu-id="ea90a-111">Преобразование масштабирования</span><span class="sxs-lookup"><span data-stu-id="ea90a-111">Scaling Transform</span></span>](#scaling-transform)
    -   [<span data-ttu-id="ea90a-112">Поворот вокруг источника</span><span class="sxs-lookup"><span data-stu-id="ea90a-112">Rotation Around the Origin</span></span>](#rotation-around-the-origin)
    -   [<span data-ttu-id="ea90a-113">Поворот вокруг произвольной точки</span><span class="sxs-lookup"><span data-stu-id="ea90a-113">Rotation Around an Arbitrary Point</span></span>](#rotation-around-an-arbitrary-point)
    -   [<span data-ttu-id="ea90a-114">Преобразование отклонений</span><span class="sxs-lookup"><span data-stu-id="ea90a-114">Skew Transform</span></span>](#skew-transform)
-   [<span data-ttu-id="ea90a-115">Представление преобразований в Direct2D</span><span class="sxs-lookup"><span data-stu-id="ea90a-115">Representing Transforms in Direct2D</span></span>](#representing-transforms-in-direct2d)
-   [<span data-ttu-id="ea90a-116">Вперед</span><span class="sxs-lookup"><span data-stu-id="ea90a-116">Next</span></span>](#next)

## <a name="introduction-to-matrices"></a><span data-ttu-id="ea90a-117">Общие сведения о матрицах</span><span class="sxs-lookup"><span data-stu-id="ea90a-117">Introduction to Matrices</span></span>

<span data-ttu-id="ea90a-118">Матрица представляет собой прямоугольный массив вещественных чисел.</span><span class="sxs-lookup"><span data-stu-id="ea90a-118">A matrix is a rectangular array of real numbers.</span></span> <span data-ttu-id="ea90a-119">*Порядок* матрицы — это количество строк и столбцов.</span><span class="sxs-lookup"><span data-stu-id="ea90a-119">The *order* of the matrix is the number of rows and columns.</span></span> <span data-ttu-id="ea90a-120">Например, если матрица содержит 3 строки и 2 столбца, то порядком будет 3 × 2.</span><span class="sxs-lookup"><span data-stu-id="ea90a-120">For example, if the matrix has 3 rows and 2 columns, the order is 3 × 2.</span></span> <span data-ttu-id="ea90a-121">Матрицы обычно отображаются с элементами матрицы, заключенными в квадратные скобки:</span><span class="sxs-lookup"><span data-stu-id="ea90a-121">Matrices are usually shown with the matrix elements enclosed in square brackets:</span></span>

![3 x 2 матрица.](images/matrix01.png)

<span data-ttu-id="ea90a-123">Нотация: матрица обозначена заглавной буквой.</span><span class="sxs-lookup"><span data-stu-id="ea90a-123">Notation: A matrix is designated by a capital letter.</span></span> <span data-ttu-id="ea90a-124">Элементы обозначены строчными буквами.</span><span class="sxs-lookup"><span data-stu-id="ea90a-124">Elements are designated by lowercase letters.</span></span> <span data-ttu-id="ea90a-125">Индексы указывают номер строки и столбца элемента.</span><span class="sxs-lookup"><span data-stu-id="ea90a-125">Subscripts indicate the row and column number of an element.</span></span> <span data-ttu-id="ea90a-126">Например,*ИЖ* — это элемент в столбце и'с Row и ж'с матрицы a.</span><span class="sxs-lookup"><span data-stu-id="ea90a-126">For example, a *ij* is the element at the i'th row and j'th column of the matrix A.</span></span>

<span data-ttu-id="ea90a-127">На следующей диаграмме показана матрица i × j с отдельными элементами в каждой ячейке матрицы.</span><span class="sxs-lookup"><span data-stu-id="ea90a-127">The following diagram shows an i × j matrix, with the individual elements in each cell of the matrix.</span></span>

![Матрица с столбцами i строками и j.](images/matrix15.png)

### <a name="matrix-operations"></a><span data-ttu-id="ea90a-129">Операции с матрицей</span><span class="sxs-lookup"><span data-stu-id="ea90a-129">Matrix Operations</span></span>

<span data-ttu-id="ea90a-130">В этом разделе описываются основные операции, определенные для матриц.</span><span class="sxs-lookup"><span data-stu-id="ea90a-130">This section describes the basic operations defined on matrices.</span></span>

<span data-ttu-id="ea90a-131">*Добавление*.</span><span class="sxs-lookup"><span data-stu-id="ea90a-131">*Addition*.</span></span> <span data-ttu-id="ea90a-132">Сумма A + B двух матриц получена путем добавления соответствующих элементов A и B:</span><span class="sxs-lookup"><span data-stu-id="ea90a-132">The sum A + B of two matrices is obtained by adding the corresponding elements of A and B:</span></span>

<dl> <span data-ttu-id="ea90a-133">А + b = \[ a *ИЖ* \]  +  \[ B *ИЖ* \]  =  \[ *ИЖ* + b *ИЖ*\]</span><span class="sxs-lookup"><span data-stu-id="ea90a-133">A + B = \[ a *ij* \] + \[ b *ij* \] = \[ a *ij* + b *ij* \]</span></span>
</dl>

<span data-ttu-id="ea90a-134">*Скалярное умножение*.</span><span class="sxs-lookup"><span data-stu-id="ea90a-134">*Scalar multiplication*.</span></span> <span data-ttu-id="ea90a-135">Эта операция умножает матрицу на вещественное число.</span><span class="sxs-lookup"><span data-stu-id="ea90a-135">This operation multiplies a matrix by a real number.</span></span> <span data-ttu-id="ea90a-136">Учитывая вещественное число *,* скалярный продукт «ка» получается путем умножения каждого элемента a на *k*.</span><span class="sxs-lookup"><span data-stu-id="ea90a-136">Given a real number *k*, the scalar product kA is obtained by multiplying every element of A by *k*.</span></span>

<dl> <span data-ttu-id="ea90a-137">ка = k \[ *ИЖ* \]  =  \[ k × a *ИЖ*\]</span><span class="sxs-lookup"><span data-stu-id="ea90a-137">kA = k\[ a *ij* \] = \[ k × a *ij* \]</span></span>
</dl>

<span data-ttu-id="ea90a-138">*Умножение матрицы*.</span><span class="sxs-lookup"><span data-stu-id="ea90a-138">*Matrix multiplication*.</span></span> <span data-ttu-id="ea90a-139">Учитывая две матрицы A и B с Order (m × n) и (n × p), продукт C = A × B является матрицей с заказом (m × p), который определяется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="ea90a-139">Given two matrices A and B with order (m × n) and (n × p), the product C = A × B is a matrix with order (m × p), defined as follows:</span></span>

![Показывает формулу для умножения матрицы.](images/matrix02.png)

<span data-ttu-id="ea90a-141">или эквивалентно:</span><span class="sxs-lookup"><span data-stu-id="ea90a-141">or, equivalently:</span></span>

<dl> <span data-ttu-id="ea90a-142">c *ИЖ* = a *1 x* B1 *j* + a *i* 2 x B2 *j* +... + a *в* + b *NJ*  
</span><span class="sxs-lookup"><span data-stu-id="ea90a-142">c *ij* = a *i* 1 x b1 *j* + a *i* 2 x b2 *j* + ... + a *in* + b *nj*  
</span></span></dl>

<span data-ttu-id="ea90a-143">То есть, чтобы вычислить каждый элемент c *ИЖ*, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="ea90a-143">That is, to compute each element c *ij*, do the following:</span></span>

1.  <span data-ttu-id="ea90a-144">Возьмите строку и'с столбца A и ж'с в B.</span><span class="sxs-lookup"><span data-stu-id="ea90a-144">Take the i'th row of A and the j'th column of B.</span></span>
2.  <span data-ttu-id="ea90a-145">Перемножьте каждую пару элементов в строке и столбце: первая запись строки по первому столбцу, вторая запись строки со второй записью столбца и т. д.</span><span class="sxs-lookup"><span data-stu-id="ea90a-145">Multiply each pair of elements in the row and column: the first row entry by the first column entry, the second row entry by the second column entry, and so forth.</span></span>
3.  <span data-ttu-id="ea90a-146">Суммировать результат.</span><span class="sxs-lookup"><span data-stu-id="ea90a-146">Sum the result.</span></span>

<span data-ttu-id="ea90a-147">Ниже приведен пример умножения матрицы (2 × 2) на матрицу (2 × 3).</span><span class="sxs-lookup"><span data-stu-id="ea90a-147">Here is an example of multiplying a (2 × 2) matrix by a (2 × 3) matrix.</span></span>

![умножение матрицы.](images/matrix03.png)

<span data-ttu-id="ea90a-149">Умножение матриц не коммутативной.</span><span class="sxs-lookup"><span data-stu-id="ea90a-149">Matrix multiplication is not commutative.</span></span> <span data-ttu-id="ea90a-150">То есть × B ≠ B × A. Кроме того, из определения следует, что не все пары матриц можно умножить.</span><span class="sxs-lookup"><span data-stu-id="ea90a-150">That is, A × B ≠ B × A. Also, from the definition it follows that not every pair of matrices can be multiplied.</span></span> <span data-ttu-id="ea90a-151">Число столбцов в левой матрице должно равняться числу строк в правой матрице.</span><span class="sxs-lookup"><span data-stu-id="ea90a-151">The number of columns in the left-hand matrix must equal the number of rows in the right-hand matrix.</span></span> <span data-ttu-id="ea90a-152">В противном случае оператор × не определен.</span><span class="sxs-lookup"><span data-stu-id="ea90a-152">Otherwise, the × operator is not defined.</span></span>

<span data-ttu-id="ea90a-153">*Обозначить матрицу*.</span><span class="sxs-lookup"><span data-stu-id="ea90a-153">*Identify matrix*.</span></span> <span data-ttu-id="ea90a-154">Матрица идентификации, обозначенная I, представляет собой квадратную матрицу, определенную следующим образом:</span><span class="sxs-lookup"><span data-stu-id="ea90a-154">An identity matrix, designated I, is a square matrix defined as follows:</span></span>

<dl> <span data-ttu-id="ea90a-155">I *ИЖ* = 1, если *i*  =  *j*, или 0 в противном случае.</span><span class="sxs-lookup"><span data-stu-id="ea90a-155">I *ij* = 1 if *i* = *j*, or 0 otherwise.</span></span>  
</dl>

<span data-ttu-id="ea90a-156">Иными словами, матрица идентификаторов содержит 1 для каждого элемента, где номер строки равен номеру столбца, и ноль для всех остальных элементов.</span><span class="sxs-lookup"><span data-stu-id="ea90a-156">In other words, an identity matrix contains 1 for each element where the row number equals the column number, and zero for all other elements.</span></span> <span data-ttu-id="ea90a-157">Например, ниже показана матрица идентификации 3 × 3.</span><span class="sxs-lookup"><span data-stu-id="ea90a-157">For example, here is the 3 × 3 identity matrix.</span></span>

![матрица идентификаторов.](images/matrix04.png)

<span data-ttu-id="ea90a-159">Следующий екуалитиес удерживается для любой матрицы M.</span><span class="sxs-lookup"><span data-stu-id="ea90a-159">The following equalities hold for any matrix M.</span></span>

<dl> <span data-ttu-id="ea90a-160">M x I = M</span><span class="sxs-lookup"><span data-stu-id="ea90a-160">M x I = M</span></span>  
<span data-ttu-id="ea90a-161">I x M = M</span><span class="sxs-lookup"><span data-stu-id="ea90a-161">I x M = M</span></span>  
</dl>

## <a name="affine-transforms"></a><span data-ttu-id="ea90a-162">Аффинных преобразований</span><span class="sxs-lookup"><span data-stu-id="ea90a-162">Affine Transforms</span></span>

<span data-ttu-id="ea90a-163">*Аффинное преобразование* — это математическая операция, которая сопоставляет одно пространство координат с другим.</span><span class="sxs-lookup"><span data-stu-id="ea90a-163">An *affine transform* is a mathematical operation that maps one coordinate space to another.</span></span> <span data-ttu-id="ea90a-164">Иными словами, он сопоставляет один набор точек с другим набором точек.</span><span class="sxs-lookup"><span data-stu-id="ea90a-164">In other words, it maps one set of points to another set of points.</span></span> <span data-ttu-id="ea90a-165">Аффинное преобразование имеет некоторые функции, которые делают их полезными в компьютерных графиках.</span><span class="sxs-lookup"><span data-stu-id="ea90a-165">Affine transforms have some features that make them useful in computer graphics.</span></span>

-   <span data-ttu-id="ea90a-166">Аффинное преобразование сохраняет *коллинеарность*.</span><span class="sxs-lookup"><span data-stu-id="ea90a-166">Affine transforms preserve *collinearity*.</span></span> <span data-ttu-id="ea90a-167">Если три или более точек попадают в строку, они по-прежнему формируют строку после преобразования.</span><span class="sxs-lookup"><span data-stu-id="ea90a-167">If three or more points fall on a line, they still form a line after the transformation.</span></span> <span data-ttu-id="ea90a-168">Прямые линии остаются прямыми.</span><span class="sxs-lookup"><span data-stu-id="ea90a-168">Straight lines remain straight.</span></span>
-   <span data-ttu-id="ea90a-169">Композиция двух аффинных преобразований является аффинное преобразованием.</span><span class="sxs-lookup"><span data-stu-id="ea90a-169">The composition of two affine transforms is an affine transform.</span></span>

<span data-ttu-id="ea90a-170">Аффинное преобразование для 2-мерная пространства имеет следующую форму.</span><span class="sxs-lookup"><span data-stu-id="ea90a-170">Affine transforms for 2-D space have the following form.</span></span>

![Показывает аффинное преобразование для 2-мерная пространства.](images/matrix05.png)

<span data-ttu-id="ea90a-172">Если применить определение умножения матрицы, заданное ранее, можно увидеть, что произведение двух аффинных преобразований является еще одним аффинное преобразованием.</span><span class="sxs-lookup"><span data-stu-id="ea90a-172">If you apply the definition of matrix multiplication given earlier, you can show that the product of two affine transforms is another affine transform.</span></span> <span data-ttu-id="ea90a-173">Для преобразования двухмерной точки с помощью аффинных преобразований точка представляется как матрица размером 1 × 3.</span><span class="sxs-lookup"><span data-stu-id="ea90a-173">To transform a 2D point using an affine transform, the point is represented as a 1 × 3 matrix.</span></span>

<dl> <span data-ttu-id="ea90a-174">P = \| x y 1 \|</span><span class="sxs-lookup"><span data-stu-id="ea90a-174">P = \| x y 1 \|</span></span>  
</dl>

<span data-ttu-id="ea90a-175">Первые два элемента содержат координаты x и y точки.</span><span class="sxs-lookup"><span data-stu-id="ea90a-175">The first two elements contain the x and y coordinates of the point.</span></span> <span data-ttu-id="ea90a-176">1 помещается в третий элемент, чтобы сделать математическим работу правильно.</span><span class="sxs-lookup"><span data-stu-id="ea90a-176">The 1 is placed in the third element to make the math work out correctly.</span></span> <span data-ttu-id="ea90a-177">Чтобы применить преобразование, умножьте эти матрицы следующим образом.</span><span class="sxs-lookup"><span data-stu-id="ea90a-177">To apply the transform, multiply the two matrices as follows.</span></span>

<dl> <span data-ttu-id="ea90a-178">P ' = P × M</span><span class="sxs-lookup"><span data-stu-id="ea90a-178">P' = P × M</span></span>  
</dl>

<span data-ttu-id="ea90a-179">Это расширяется до следующего.</span><span class="sxs-lookup"><span data-stu-id="ea90a-179">This expands to the following.</span></span>

![аффинное преобразование.](images/matrix06.png)

<span data-ttu-id="ea90a-181&quot;>where</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;ea90a-181&quot;>where</span></span>

<dl> <span data-ttu-id=&quot;ea90a-182&quot;>x &quot;= AX + CY + e</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;ea90a-182&quot;>x' = ax + cy + e</span></span>  
<span data-ttu-id=&quot;ea90a-183&quot;>y &quot;= BX + DY + f</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;ea90a-183&quot;>y' = bx + dy + f</span></span>  
</dl>

<span data-ttu-id=&quot;ea90a-184&quot;>Чтобы получить преобразованную точку, Возьмите первые два элемента матрицы P '.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;ea90a-184&quot;>To get the transformed point, take the first two elements of matrix P'.</span></span>

<dl> <span data-ttu-id=&quot;ea90a-185&quot;>p = (x &quot;, y") = (AX + CY + e, BX + DY + f)</span><span class="sxs-lookup"><span data-stu-id="ea90a-185">p = (x', y') = (ax + cy + e, bx + dy + f)</span></span>  
</dl>

> [!Note]  
> <span data-ttu-id="ea90a-186">Матрица размером 1 × *n* называется *вектором строк*.</span><span class="sxs-lookup"><span data-stu-id="ea90a-186">A 1 × *n* matrix is called a *row vector*.</span></span> <span data-ttu-id="ea90a-187">Direct2D и Direct3D используют векторы строк для представления точек в двухмерном или трехмерном пространстве.</span><span class="sxs-lookup"><span data-stu-id="ea90a-187">Direct2D and Direct3D both use row vectors to represent points in 2D or 3D space.</span></span> <span data-ttu-id="ea90a-188">Эквивалентный результат можно получить, используя вектор столбца (*n* × 1) и переполнив матрицу преобразования.</span><span class="sxs-lookup"><span data-stu-id="ea90a-188">You can get an equivalent result by using a column vector (*n* × 1) and transposing the transform matrix.</span></span> <span data-ttu-id="ea90a-189">В большинстве графических текстов используется форма «вектор столбцов».</span><span class="sxs-lookup"><span data-stu-id="ea90a-189">Most graphics texts use the column vector form.</span></span> <span data-ttu-id="ea90a-190">В этом разделе представлена форма вектора строк для обеспечения согласованности с Direct2D и Direct3D.</span><span class="sxs-lookup"><span data-stu-id="ea90a-190">This topic presents the row vector form for consistency with Direct2D and Direct3D.</span></span>

 

<span data-ttu-id="ea90a-191">Следующие несколько разделов являются производными от базовых преобразований.</span><span class="sxs-lookup"><span data-stu-id="ea90a-191">The next several sections derive the basic transforms.</span></span>

### <a name="translation-transform"></a><span data-ttu-id="ea90a-192">Преобразование перевода</span><span class="sxs-lookup"><span data-stu-id="ea90a-192">Translation Transform</span></span>

<span data-ttu-id="ea90a-193">Матрица преобразования перевода имеет следующую форму.</span><span class="sxs-lookup"><span data-stu-id="ea90a-193">The translation transform matrix has the following form.</span></span>

![Преобразование перевода.](images/matrix07.png)

<span data-ttu-id="ea90a-195">Подключение точки *P* к этому уравнению дает следующее:</span><span class="sxs-lookup"><span data-stu-id="ea90a-195">Plugging a point *P* into this equation yields:</span></span>

<dl> <span data-ttu-id="ea90a-196">P ' = (*x*  +  *DX*, *y*  +  *dy*)</span><span class="sxs-lookup"><span data-stu-id="ea90a-196">P' = (*x* + *dx*, *y* + *dy*)</span></span>
</dl>

<span data-ttu-id="ea90a-197">соответствует точке (x, y), переведенной в *DX* на оси x и *dy* на оси y.</span><span class="sxs-lookup"><span data-stu-id="ea90a-197">which corresponds to the point (x, y) translated by *dx* in the X-axis and *dy* in the Y-axis.</span></span>

![Диаграмма, на которой показан перевод двух точек.](images/graphics22.png)

### <a name="scaling-transform"></a><span data-ttu-id="ea90a-199">Преобразование масштабирования</span><span class="sxs-lookup"><span data-stu-id="ea90a-199">Scaling Transform</span></span>

<span data-ttu-id="ea90a-200">Матрица преобразования масштабирования имеет следующую форму.</span><span class="sxs-lookup"><span data-stu-id="ea90a-200">The scaling transform matrix has the following form.</span></span>

![преобразование масштабирования.](images/matrix09.png)

<span data-ttu-id="ea90a-202">Подключение точки *P* к этому уравнению дает следующее:</span><span class="sxs-lookup"><span data-stu-id="ea90a-202">Plugging a point *P* into this equation yields:</span></span>

<dl> <span data-ttu-id="ea90a-203">P ' = (*x* ∙ *DX*, *y* -∙ *dy*)</span><span class="sxs-lookup"><span data-stu-id="ea90a-203">P' = (*x* ∙ *dx*, *y* ∙ *dy*)</span></span>
</dl>

<span data-ttu-id="ea90a-204">соответствует точке (x, y), масштабированной по *DX* и *dy*.</span><span class="sxs-lookup"><span data-stu-id="ea90a-204">which corresponds to the point (x,y) scaled by *dx* and *dy*.</span></span>

![Диаграмма, показывающая масштабирование двух точек.](images/graphics23.png)

### <a name="rotation-around-the-origin"></a><span data-ttu-id="ea90a-206">Поворот вокруг источника</span><span class="sxs-lookup"><span data-stu-id="ea90a-206">Rotation Around the Origin</span></span>

<span data-ttu-id="ea90a-207">Матрица для поворота точки вокруг начала координат имеет следующую форму.</span><span class="sxs-lookup"><span data-stu-id="ea90a-207">The matrix to rotate a point around the origin has the following form.</span></span>

![Показывает формулу для преобразования поворота.](images/matrix11.png)

<span data-ttu-id="ea90a-209">Преобразованная точка:</span><span class="sxs-lookup"><span data-stu-id="ea90a-209">The transformed point is:</span></span>

<dl> <span data-ttu-id="ea90a-210">P ' = (*x* Косθ – исинθ, *x* синθ + *y* косθ)</span><span class="sxs-lookup"><span data-stu-id="ea90a-210">P' = (*x* cosΘ – ysinΘ, *x* sinΘ + *y* cosΘ)</span></span>
</dl>

<span data-ttu-id="ea90a-211">Средство.</span><span class="sxs-lookup"><span data-stu-id="ea90a-211">Proof.</span></span> <span data-ttu-id="ea90a-212">Чтобы отобразить, что P представляет поворот, рассмотрим следующую диаграмму.</span><span class="sxs-lookup"><span data-stu-id="ea90a-212">To show that P' represents a rotation, consider the following diagram.</span></span>

![Схема, показывающая поворот вокруг источника.](images/graphics24.png)

<span data-ttu-id="ea90a-214">Исходные данные:</span><span class="sxs-lookup"><span data-stu-id="ea90a-214">Given:</span></span>

<dl> <dt>

<span data-ttu-id="ea90a-215"><span id="P____x_y_"></span><span id="p____x_y_"></span><span id="P____X_Y_"></span>P = (x, y)</span><span class="sxs-lookup"><span data-stu-id="ea90a-215"><span id="P____x_y_"></span><span id="p____x_y_"></span><span id="P____X_Y_"></span>P = (x,y)</span></span>
</dt> <dd>

<span data-ttu-id="ea90a-216">Исходная точка для преобразования.</span><span class="sxs-lookup"><span data-stu-id="ea90a-216">The original point to transform.</span></span>

</dd> <dt>

<span data-ttu-id="ea90a-217">φ</span><span class="sxs-lookup"><span data-stu-id="ea90a-217">Φ</span></span>
</dt> <dd>

<span data-ttu-id="ea90a-218">Угол, сформированный строкой (0, 0), до P.</span><span class="sxs-lookup"><span data-stu-id="ea90a-218">The angle formed by the line (0,0) to P.</span></span>

</dd> <dt>

<span data-ttu-id="ea90a-219">Θ</span><span class="sxs-lookup"><span data-stu-id="ea90a-219">Θ</span></span>
</dt> <dd>

<span data-ttu-id="ea90a-220">Угол поворота (x, y) источника.</span><span class="sxs-lookup"><span data-stu-id="ea90a-220">The angle by which to rotate (x,y) about the origin.</span></span>

</dd> <dt>

<span data-ttu-id="ea90a-221"><span id="P_____x__y__"></span><span id="p_____x__y__"></span><span id="P_____X__Y__"></span>P ' = (x ', y ')</span><span class="sxs-lookup"><span data-stu-id="ea90a-221"><span id="P_____x__y__"></span><span id="p_____x__y__"></span><span id="P_____X__Y__"></span>P' = (x',y')</span></span>
</dt> <dd>

<span data-ttu-id="ea90a-222">Преобразованная точка.</span><span class="sxs-lookup"><span data-stu-id="ea90a-222">The transformed point.</span></span>

</dd> <dt>

<span data-ttu-id="ea90a-223"><span id="R"></span><span id="r"></span>Cерверный</span><span class="sxs-lookup"><span data-stu-id="ea90a-223"><span id="R"></span><span id="r"></span>R</span></span>
</dt> <dd>

<span data-ttu-id="ea90a-224">Длина строки (0, 0) в P. Также радиус круга поворота.</span><span class="sxs-lookup"><span data-stu-id="ea90a-224">The length of the line (0,0) to P. Also the radius of the circle of rotation.</span></span>

</dd> </dl>

> [!Note]  
> <span data-ttu-id="ea90a-225">Эта диаграмма использует стандартную систему координат, используемую в геометрии, где на оси y настраивается положительная ось.</span><span class="sxs-lookup"><span data-stu-id="ea90a-225">This diagram uses the standard coordinate system used in geometry, where the positive y-axis points up.</span></span> <span data-ttu-id="ea90a-226">Direct2D использует систему координат Windows, на которой отключается положительная ось y.</span><span class="sxs-lookup"><span data-stu-id="ea90a-226">Direct2D uses the Windows coordinate system, where the positive y-axis points down.</span></span>

 

<span data-ttu-id="ea90a-227">Угол между осью x и линией (0, 0) по P ' — Φ + Θ.</span><span class="sxs-lookup"><span data-stu-id="ea90a-227">The angle between the x-axis and the line (0,0) to P' is Φ + Θ.</span></span> <span data-ttu-id="ea90a-228">Следующие удостоверения содержат:</span><span class="sxs-lookup"><span data-stu-id="ea90a-228">The following identities hold:</span></span>

<dl> <span data-ttu-id="ea90a-229">x = R Косφ</span><span class="sxs-lookup"><span data-stu-id="ea90a-229">x = R cosΦ</span></span>  
<span data-ttu-id="ea90a-230">y = Синφ R</span><span class="sxs-lookup"><span data-stu-id="ea90a-230">y = R sinΦ</span></span>  
<span data-ttu-id="ea90a-231">x "= R cos (Φ + Θ)</span><span class="sxs-lookup"><span data-stu-id="ea90a-231">x' = R cos(Φ + Θ)</span></span>  
<span data-ttu-id="ea90a-232">y "= R Sin (Φ + Θ)</span><span class="sxs-lookup"><span data-stu-id="ea90a-232">y' = R sin(Φ+ Θ)</span></span>  
</dl>

<span data-ttu-id="ea90a-233">Теперь разрешите для x "и y" с точки зрения Θ.</span><span class="sxs-lookup"><span data-stu-id="ea90a-233">Now solve for x' and y' in terms of Θ.</span></span> <span data-ttu-id="ea90a-234">По формулам сложения:</span><span class="sxs-lookup"><span data-stu-id="ea90a-234">By the trigonometric addition formulas:</span></span>

<dl> <span data-ttu-id="ea90a-235">x "= R (Косφкосθ – Синφсинθ) = Ркосφкосθ — Рсинφсинθ</span><span class="sxs-lookup"><span data-stu-id="ea90a-235">x' = R(cosΦcosΘ – sinΦsinΘ) = RcosΦcosΘ – RsinΦsinΘ</span></span>  
<span data-ttu-id="ea90a-236">y "= R (Синφкосθ + Косφсинθ) = Рсинφкосθ + Ркосφсинθ</span><span class="sxs-lookup"><span data-stu-id="ea90a-236">y' = R(sinΦcosΘ + cosΦsinΘ) = RsinΦcosΘ + RcosΦsinΘ</span></span>  
</dl>

<span data-ttu-id="ea90a-237">Подставив, мы получаем:</span><span class="sxs-lookup"><span data-stu-id="ea90a-237">Substituting, we get:</span></span>

<dl> <span data-ttu-id="ea90a-238">x "= Кскосθ — Исинθ</span><span class="sxs-lookup"><span data-stu-id="ea90a-238">x' = xcosΘ – ysinΘ</span></span>  
<span data-ttu-id="ea90a-239">y "= Кссинθ + Икосθ</span><span class="sxs-lookup"><span data-stu-id="ea90a-239">y' = xsinΘ + ycosΘ</span></span>  
</dl>

<span data-ttu-id="ea90a-240">соответствует преобразованной точке P, показанной ранее.</span><span class="sxs-lookup"><span data-stu-id="ea90a-240">which corresponds to the transformed point P' shown earlier.</span></span>

### <a name="rotation-around-an-arbitrary-point"></a><span data-ttu-id="ea90a-241">Поворот вокруг произвольной точки</span><span class="sxs-lookup"><span data-stu-id="ea90a-241">Rotation Around an Arbitrary Point</span></span>

<span data-ttu-id="ea90a-242">Для поворота вокруг точки (x, y), отличной от исходной, используется следующая матрица.</span><span class="sxs-lookup"><span data-stu-id="ea90a-242">To rotate around a point (x,y) other than the origin, the following matrix is used.</span></span>

![преобразование поворота.](images/matrix13.png)

<span data-ttu-id="ea90a-244">Эту матрицу можно получить, отменив точку (x, y) на начало.</span><span class="sxs-lookup"><span data-stu-id="ea90a-244">You can derive this matrix by taking the point (x,y) to be the origin.</span></span>

![Диаграмма, показывающая поворот вокруг точки.](images/graphics25.png)

<span data-ttu-id="ea90a-246">Let (x1, y1) является точкой, полученной в результате поворота точки (x0, y0) вокруг точки (x, y).</span><span class="sxs-lookup"><span data-stu-id="ea90a-246">Let (x1, y1) be the point that results from rotating the point (x0, y0) around the point (x,y).</span></span> <span data-ttu-id="ea90a-247">Можно наследовать x1 следующим образом.</span><span class="sxs-lookup"><span data-stu-id="ea90a-247">We can derive x1 as follows.</span></span>

<dl> <span data-ttu-id="ea90a-248">x1 = (x0 – x) Косθ – (Y0 – y) Синθ + x</span><span class="sxs-lookup"><span data-stu-id="ea90a-248">x1 = (x0 – x)cosΘ– (y0 – y)sinΘ + x</span></span>  
<span data-ttu-id="ea90a-249">x1 = x0cosΘ – y0sinΘ + \[ (1 – косθ) + исинθ \]</span><span class="sxs-lookup"><span data-stu-id="ea90a-249">x1 = x0cosΘ – y0sinΘ + \[ (1 – cosΘ) + ysinΘ \]</span></span>  
</dl>

<span data-ttu-id="ea90a-250">Теперь подсоедините это уравнение к матрице преобразования, используя формулу x1 = ax0 + CY0 + e из предыдущих версий.</span><span class="sxs-lookup"><span data-stu-id="ea90a-250">Now plug this equation back into the transform matrix, using the formula x1 = ax0 + cy0 + e from earlier.</span></span> <span data-ttu-id="ea90a-251">Используйте ту же процедуру, чтобы получить значение Y1.</span><span class="sxs-lookup"><span data-stu-id="ea90a-251">Use the same procedure to derive y1.</span></span>

### <a name="skew-transform"></a><span data-ttu-id="ea90a-252">Преобразование отклонений</span><span class="sxs-lookup"><span data-stu-id="ea90a-252">Skew Transform</span></span>

<span data-ttu-id="ea90a-253">Преобразование «наклон» определяется четырьмя параметрами:</span><span class="sxs-lookup"><span data-stu-id="ea90a-253">The skew transform is defined by four parameters:</span></span>

-   <span data-ttu-id="ea90a-254">Θ: величина наклона вдоль оси x, измеряемая как угол от оси y.</span><span class="sxs-lookup"><span data-stu-id="ea90a-254">Θ: The amount to skew along the x-axis, measured as an angle from the y-axis.</span></span>
-   <span data-ttu-id="ea90a-255">Φ: величина наклона вдоль оси y, измеряемая как угол от оси x.</span><span class="sxs-lookup"><span data-stu-id="ea90a-255">Φ: The amount to skew along the y-axis, measured as an angle from the x-axis.</span></span>
-   <span data-ttu-id="ea90a-256">(*px*, *корректировка*): координаты x и y точки, относительно которой выполняется отклонение.</span><span class="sxs-lookup"><span data-stu-id="ea90a-256">(*px*, *py*): The x- and y-coordinates of the point about which the skew is performed.</span></span>

<span data-ttu-id="ea90a-257">Преобразование «наклон» использует следующую матрицу.</span><span class="sxs-lookup"><span data-stu-id="ea90a-257">The skew transform uses the following matrix.</span></span>

![Преобразование отклонений.](images/matrix14.png)

<span data-ttu-id="ea90a-259">Преобразованная точка:</span><span class="sxs-lookup"><span data-stu-id="ea90a-259">The transformed point is:</span></span>

<dl> <span data-ttu-id="ea90a-260">P ' = (*x*  +  *y* танθ – *Копировать* танθ, *y*  +  *x* танφ) — *Копировать* танφ</span><span class="sxs-lookup"><span data-stu-id="ea90a-260">P' = (*x* + *y* tanΘ – *py* tanΘ, *y* + *x* tanΦ) – *py* tanΦ</span></span>
</dl>

<span data-ttu-id="ea90a-261">или аналогичным образом:</span><span class="sxs-lookup"><span data-stu-id="ea90a-261">or equivalently:</span></span>

<dl> <span data-ttu-id="ea90a-262">P ' = (*x* + (*y* – *Копировать*) танθ, *y* + (*x* – *px*) танφ)</span><span class="sxs-lookup"><span data-stu-id="ea90a-262">P' = (*x* + (*y* – *py*)tanΘ, *y* + (*x* – *px*)tanΦ)</span></span>
</dl>

<span data-ttu-id="ea90a-263">Чтобы увидеть, как работает преобразование, рассмотрите каждый компонент по отдельности.</span><span class="sxs-lookup"><span data-stu-id="ea90a-263">To see how this transform works, consider each component individually.</span></span> <span data-ttu-id="ea90a-264">Параметр Θ перемещает каждую точку в направлении x на величину, равную Танθ.</span><span class="sxs-lookup"><span data-stu-id="ea90a-264">The Θ parameter moves every point in the x direction by an amount equal to tanΘ.</span></span> <span data-ttu-id="ea90a-265">На следующей диаграмме показана связь между Θ и наклоном по оси x.</span><span class="sxs-lookup"><span data-stu-id="ea90a-265">The following diagram shows the relation between Θ and the x-axis skew.</span></span>

![Схема, на которой показана асимметрия вдоль оси x.](images/graphics26.png)

<span data-ttu-id="ea90a-267">Вот та же разница, примененная к прямоугольнику:</span><span class="sxs-lookup"><span data-stu-id="ea90a-267">Here is the same skew applied to a rectangle:</span></span>

![Схема, показывающая асимметрию вдоль оси x при применении к прямоугольнику.](images/graphics27.png)

<span data-ttu-id="ea90a-269">Параметр Φ имеет тот же результат, но вдоль оси y:</span><span class="sxs-lookup"><span data-stu-id="ea90a-269">The Φ parameter has the same effect, but along the y-axis:</span></span>

![Схема, на которой показана асимметрия вдоль оси y.](images/graphics28.png)

<span data-ttu-id="ea90a-271">На следующей схеме показано отклонение по оси y, применяемое к прямоугольнику.</span><span class="sxs-lookup"><span data-stu-id="ea90a-271">The next diagram shows y-axis skew applied to a rectangle.</span></span>

![Схема, показывающая асимметрию вдоль оси y при применении к прямоугольнику.](images/graphics29.png)

<span data-ttu-id="ea90a-273">Наконец, параметры *px* и *корректировки* сдвигаются центральную точку наклона вдоль осей x и y.</span><span class="sxs-lookup"><span data-stu-id="ea90a-273">Finally, the parameters *px* and *py* shift the center point for the skew along the x- and y-axes.</span></span>

## <a name="representing-transforms-in-direct2d"></a><span data-ttu-id="ea90a-274">Представление преобразований в Direct2D</span><span class="sxs-lookup"><span data-stu-id="ea90a-274">Representing Transforms in Direct2D</span></span>

<span data-ttu-id="ea90a-275">Все преобразования Direct2D являются аффинноеи преобразованиями.</span><span class="sxs-lookup"><span data-stu-id="ea90a-275">All Direct2D transforms are affine transforms.</span></span> <span data-ttu-id="ea90a-276">Direct2D не поддерживает преобразования, не являющиеся аффинных.</span><span class="sxs-lookup"><span data-stu-id="ea90a-276">Direct2D does not support non-affine transforms.</span></span> <span data-ttu-id="ea90a-277">Преобразования представлены структурой [**\_ матрицы D2D1 Matrix \_ 3X2 \_ F**](/windows/desktop/Direct2D/d2d1-matrix-3x2-f) .</span><span class="sxs-lookup"><span data-stu-id="ea90a-277">Transforms are represented by the [**D2D1\_MATRIX\_3X2\_F**](/windows/desktop/Direct2D/d2d1-matrix-3x2-f) structure.</span></span> <span data-ttu-id="ea90a-278">Эта структура определяет матрицу размером 3 × 2.</span><span class="sxs-lookup"><span data-stu-id="ea90a-278">This structure defines a 3 × 2 matrix.</span></span> <span data-ttu-id="ea90a-279">Так как третий столбец аффинных преобразований всегда один и тот же ( \[ 0, 0, 1 \] ), а Direct2D не поддерживает преобразования, не являющиеся аффинных, нет необходимости указывать всю матрицу 3 × 3.</span><span class="sxs-lookup"><span data-stu-id="ea90a-279">Because the third column of an affine transform is always the same (\[0, 0, 1\]), and because Direct2D does not support non-affine transforms, there is no need to specify the entire 3 × 3 matrix.</span></span> <span data-ttu-id="ea90a-280">На внутреннем уровне Direct2D использует матрицы 3 × 3 для вычислений преобразований.</span><span class="sxs-lookup"><span data-stu-id="ea90a-280">Internally, Direct2D uses 3 × 3 matrices to compute the transforms.</span></span>

<span data-ttu-id="ea90a-281">Элементы [**\_ матрицы D2D1 \_ 3X2 \_ F**](/windows/desktop/Direct2D/d2d1-matrix-3x2-f) именуются в соответствии с их позицией индекса: **\_ 11** элемент — это Element (1, 1), **\_ 12** элементов — элемент (1, 2) и т. д.</span><span class="sxs-lookup"><span data-stu-id="ea90a-281">The members of the [**D2D1\_MATRIX\_3X2\_F**](/windows/desktop/Direct2D/d2d1-matrix-3x2-f) are named according to their index position: the **\_11** member is element (1,1), the **\_12** member is element (1,2), and so forth.</span></span> <span data-ttu-id="ea90a-282">Хотя члены структуры можно инициализировать напрямую, рекомендуется использовать класс [**D2D1:: Matrix3x2F**](/windows/desktop/api/d2d1helper/nl-d2d1helper-matrix3x2f) .</span><span class="sxs-lookup"><span data-stu-id="ea90a-282">Although you can initialize the structure members directly, it is recommended to use the [**D2D1::Matrix3x2F**](/windows/desktop/api/d2d1helper/nl-d2d1helper-matrix3x2f) class.</span></span> <span data-ttu-id="ea90a-283">Этот класс наследует **D2D1 \_ Matrix \_ 3X2 \_ F** и предоставляет вспомогательные методы для создания любых базовых аффинных преобразований.</span><span class="sxs-lookup"><span data-stu-id="ea90a-283">This class inherits **D2D1\_MATRIX\_3X2\_F** and provides helper methods for creating any of the basic affine transforms.</span></span> <span data-ttu-id="ea90a-284">Класс также определяет [**оператор \* ()**](/windows/desktop/api/d2d1helper/nf-d2d1helper-matrix3x2f-operator-mult) для составления двух или более преобразований, как описано в разделе [применение преобразований в Direct2D](applying-transforms-in-direct2d.md).</span><span class="sxs-lookup"><span data-stu-id="ea90a-284">The class also defines [**operator\*()**](/windows/desktop/api/d2d1helper/nf-d2d1helper-matrix3x2f-operator-mult) for composing two or more transforms, as described in [Applying Transforms in Direct2D](applying-transforms-in-direct2d.md).</span></span>

## <a name="next"></a><span data-ttu-id="ea90a-285">Следующая</span><span class="sxs-lookup"><span data-stu-id="ea90a-285">Next</span></span>

[<span data-ttu-id="ea90a-286">Модуль 4. Ввод данных пользователем</span><span class="sxs-lookup"><span data-stu-id="ea90a-286">Module 4. User Input</span></span>](module-4--user-input.md)

 

 