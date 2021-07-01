---
title: Per-Component математических операций
description: С помощью HLSL можно программировать шейдеры на уровне алгоритма.
ms.assetid: a919df50-2d13-489d-9011-1137c997e121
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2c8c9eeea1072c53915588ac0099998e76c0452a
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119599"
---
# <a name="per-component-math-operations"></a><span data-ttu-id="8043c-103">Per-Component математических операций</span><span class="sxs-lookup"><span data-stu-id="8043c-103">Per-Component Math Operations</span></span>

<span data-ttu-id="8043c-104">С помощью HLSL можно программировать шейдеры на уровне алгоритма.</span><span class="sxs-lookup"><span data-stu-id="8043c-104">With HLSL, you can program shaders at an algorithm level.</span></span> <span data-ttu-id="8043c-105">Чтобы понять язык, необходимо знать, как объявлять переменные и функции, использовать встроенные функции, определять пользовательские типы данных и использовать семантику для подключения аргументов шейдера к другим шейдерам и к конвейеру.</span><span class="sxs-lookup"><span data-stu-id="8043c-105">To understand the language, you will need to know how to declare variables and functions, use intrinsic functions, define custom data types and use semantics to connect shader arguments to other shaders and to the pipeline.</span></span>

<span data-ttu-id="8043c-106">Когда вы научитесь создавать шейдеры в HLSL, вам потребуется изучить вызовы API, чтобы вы могли: компилировать шейдер для определенного оборудования, инициализировать константы шейдеров и при необходимости инициализировать другое состояние конвейера.</span><span class="sxs-lookup"><span data-stu-id="8043c-106">Once you learn how to author shaders in HLSL, you will need to learn about API calls so that you can: compile a shader for particular hardware, initialize shader constants, and initialize other pipeline state if necessary.</span></span>

-   [<span data-ttu-id="8043c-107">Тип вектора</span><span class="sxs-lookup"><span data-stu-id="8043c-107">The Vector Type</span></span>](#the-vector-type)
-   [<span data-ttu-id="8043c-108">Тип матрицы</span><span class="sxs-lookup"><span data-stu-id="8043c-108">The Matrix Type</span></span>](#the-matrix-type)
    -   [<span data-ttu-id="8043c-109">Упорядочение матрицы</span><span class="sxs-lookup"><span data-stu-id="8043c-109">Matrix Ordering</span></span>](#matrix-ordering)
-   [<span data-ttu-id="8043c-110">Примеры</span><span class="sxs-lookup"><span data-stu-id="8043c-110">Examples</span></span>](#examples)
-   [<span data-ttu-id="8043c-111">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="8043c-111">Related topics</span></span>](#related-topics)

## <a name="the-vector-type"></a><span data-ttu-id="8043c-112">Тип вектора</span><span class="sxs-lookup"><span data-stu-id="8043c-112">The Vector Type</span></span>

<span data-ttu-id="8043c-113">Vector — это структура данных, которая содержит от одного до четырех компонентов.</span><span class="sxs-lookup"><span data-stu-id="8043c-113">A vector is a data structure that contains between one and four components.</span></span>


```
bool    bVector;   // scalar containing 1 Boolean
bool1   bVector;   // vector containing 1 Boolean
int1    iVector;   // vector containing 1 int
float3  fVector;   // vector containing 3 floats
double4 dVector;   // vector containing 4 doubles
```



<span data-ttu-id="8043c-114">Целое число непосредственно после типа данных — число компонентов в векторе.</span><span class="sxs-lookup"><span data-stu-id="8043c-114">The integer immediately following the data type is the number of components on the vector.</span></span>

<span data-ttu-id="8043c-115">Инициализаторы также можно включать в объявления.</span><span class="sxs-lookup"><span data-stu-id="8043c-115">Initializers can also be included in the declarations.</span></span>


```
bool    bVector = false;
int1    iVector = 1;
float3  fVector = { 0.2f, 0.3f, 0.4f };
double4 dVector = { 0.2, 0.3, 0.4, 0.5 };
```



<span data-ttu-id="8043c-116">Кроме того, тип Vector можно использовать для создания одних и тех же объявлений:</span><span class="sxs-lookup"><span data-stu-id="8043c-116">Alternatively, the vector type can be used to make the same declarations:</span></span>


```
vector <bool,   1> bVector = false;
vector <int,    1> iVector = 1;
vector <float,  3> fVector = { 0.2f, 0.3f, 0.4f };
vector <double, 4> dVector = { 0.2, 0.3, 0.4, 0.5 };
```



<span data-ttu-id="8043c-117">Тип Vector использует угловые скобки для указания типа и количества компонентов.</span><span class="sxs-lookup"><span data-stu-id="8043c-117">The vector type uses angle brackets to specify the type and number of components.</span></span>

<span data-ttu-id="8043c-118">Векторы содержат до четырех компонентов, к которым можно получить доступ с помощью одного из двух наборов имен:</span><span class="sxs-lookup"><span data-stu-id="8043c-118">Vectors contain up to four components, each of which can be accessed using one of two naming sets:</span></span>

-   <span data-ttu-id="8043c-119">Набор позиций: x, y, z, w</span><span class="sxs-lookup"><span data-stu-id="8043c-119">The position set: x,y,z,w</span></span>
-   <span data-ttu-id="8043c-120">Набор цветов: r, g, b, a</span><span class="sxs-lookup"><span data-stu-id="8043c-120">The color set: r,g,b,a</span></span>

<span data-ttu-id="8043c-121">Эти инструкции возвращают значение в третьем компоненте.</span><span class="sxs-lookup"><span data-stu-id="8043c-121">These statements both return the value in the third component.</span></span>


```
// Given
float4 pos = float4(0,0,2,1);

pos.z    // value is 2
pos.b    // value is 2
```



<span data-ttu-id="8043c-122">Наборы имен могут использовать один или несколько компонентов, но они не могут быть смешанными.</span><span class="sxs-lookup"><span data-stu-id="8043c-122">Naming sets can use one or more components, but they cannot be mixed.</span></span>


```
// Given
float4 pos = float4(0,0,2,1);
float2 temp;

temp = pos.xy  // valid
temp = pos.rg  // valid

temp = pos.xg  // NOT VALID because the position and color sets were used.
```



<span data-ttu-id="8043c-123">Указание одного или нескольких компонентов вектора при чтении компонентов называется группирующие.</span><span class="sxs-lookup"><span data-stu-id="8043c-123">Specifying one or more vector components when reading components is called swizzling.</span></span> <span data-ttu-id="8043c-124">Пример.</span><span class="sxs-lookup"><span data-stu-id="8043c-124">For example:</span></span>


```
float4 pos = float4(0,0,2,1);
float2 f_2D;
f_2D = pos.xy;   // read two components 
f_2D = pos.xz;   // read components in any order       
f_2D = pos.zx;

f_2D = pos.xx;   // components can be read more than once
f_2D = pos.yy;
```



<span data-ttu-id="8043c-125">Маскирование управляет количеством записываемых компонентов.</span><span class="sxs-lookup"><span data-stu-id="8043c-125">Masking controls how many components are written.</span></span>


```
float4 pos = float4(0,0,2,1);
float4 f_4D;
f_4D    = pos;     // write four components          

f_4D.xz = pos.xz;  // write two components        
f_4D.zx = pos.xz;  // change the write order

f_4D.xzyw = pos.w; // write one component to more than one component
f_4D.wzyx = pos;
```



<span data-ttu-id="8043c-126">Назначения не могут быть записаны в один и тот же компонент несколько раз.</span><span class="sxs-lookup"><span data-stu-id="8043c-126">Assignments cannot be written to the same component more than once.</span></span> <span data-ttu-id="8043c-127">Поэтому левая часть оператора является недопустимой:</span><span class="sxs-lookup"><span data-stu-id="8043c-127">So the left side of this statement is invalid:</span></span>


```
f_4D.xx = pos.xy;   // cannot write to the same destination components 
```



<span data-ttu-id="8043c-128">Кроме того, пространства имен компонентов не могут быть смешанными.</span><span class="sxs-lookup"><span data-stu-id="8043c-128">Also, the component name spaces cannot be mixed.</span></span> <span data-ttu-id="8043c-129">Это недопустимый компонент записи:</span><span class="sxs-lookup"><span data-stu-id="8043c-129">This is an invalid component write:</span></span>


```
f_4D.xg = pos.rgrg;    // invalid write: cannot mix component name spaces 
```



<span data-ttu-id="8043c-130">Доступ к вектору в качестве скаляра будет осуществлять доступ к первому компоненту вектора.</span><span class="sxs-lookup"><span data-stu-id="8043c-130">Accessing a vector as a scalar will access the first component of the vector.</span></span> <span data-ttu-id="8043c-131">Следующие две инструкции эквивалентны.</span><span class="sxs-lookup"><span data-stu-id="8043c-131">The following two statements are equivalent.</span></span>


```
f_4D.a = pos * 5.0f;
f_4D.a = pos.r * 5.0f;
```



## <a name="the-matrix-type"></a><span data-ttu-id="8043c-132">Тип матрицы</span><span class="sxs-lookup"><span data-stu-id="8043c-132">The Matrix Type</span></span>

<span data-ttu-id="8043c-133">Матрица — это структура данных, содержащая строки и столбцы данных.</span><span class="sxs-lookup"><span data-stu-id="8043c-133">A matrix is a data structure that contains rows and columns of data.</span></span> <span data-ttu-id="8043c-134">Данные могут быть любыми скалярными типами данных, однако каждый элемент матрицы имеет один и тот же тип данных.</span><span class="sxs-lookup"><span data-stu-id="8043c-134">The data can be any of the scalar data types, however, every element of a matrix is the same data type.</span></span> <span data-ttu-id="8043c-135">Число строк и столбцов указывается строкой по столбцам, добавляемым к типу данных.</span><span class="sxs-lookup"><span data-stu-id="8043c-135">The number of rows and columns is specified with the row-by-column string that is appended to the data type.</span></span>


```
int1x1    iMatrix;   // integer matrix with 1 row,  1 column
int2x1    iMatrix;   // integer matrix with 2 rows, 1 column
...
int4x1    iMatrix;   // integer matrix with 4 rows, 1 column
...
int1x4    iMatrix;   // integer matrix with 1 row, 4 columns
double1x1 dMatrix;   // double matrix with 1 row,  1 column
double2x2 dMatrix;   // double matrix with 2 rows, 2 columns
double3x3 dMatrix;   // double matrix with 3 rows, 3 columns
double4x4 dMatrix;   // double matrix with 4 rows, 4 columns
```



<span data-ttu-id="8043c-136">Максимальное число строк или столбцов равно 4; Минимальное значение равно 1.</span><span class="sxs-lookup"><span data-stu-id="8043c-136">The maximum number of rows or columns is 4; the minimum number is 1.</span></span>

<span data-ttu-id="8043c-137">Матрицу можно инициализировать при ее объявлении:</span><span class="sxs-lookup"><span data-stu-id="8043c-137">A matrix can be initialized when it is declared:</span></span>


```
float2x2 fMatrix = { 0.0f, 0.1, // row 1
                     2.1f, 2.2f // row 2
                   };   
```



<span data-ttu-id="8043c-138">Или тип матрицы можно использовать для создания одних и тех же объявлений:</span><span class="sxs-lookup"><span data-stu-id="8043c-138">Or, the matrix type can be used to make the same declarations:</span></span>


```
matrix <float, 2, 2> fMatrix = { 0.0f, 0.1, // row 1
                                 2.1f, 2.2f // row 2
                               };
```



<span data-ttu-id="8043c-139">Тип матрицы использует угловые скобки для указания типа, числа строк и числа столбцов.</span><span class="sxs-lookup"><span data-stu-id="8043c-139">The matrix type uses the angle brackets to specify the type, the number of rows, and the number of columns.</span></span> <span data-ttu-id="8043c-140">В этом примере создается матрица с плавающей точкой с двумя строками и двумя столбцами.</span><span class="sxs-lookup"><span data-stu-id="8043c-140">This example creates a floating-point matrix, with two rows and two columns.</span></span> <span data-ttu-id="8043c-141">Можно использовать любой скалярный тип данных.</span><span class="sxs-lookup"><span data-stu-id="8043c-141">Any of the scalar data types can be used.</span></span>

<span data-ttu-id="8043c-142">Это объявление определяет матрицу значений float (32-разрядных чисел с плавающей запятой) с двумя строками и тремя столбцами:</span><span class="sxs-lookup"><span data-stu-id="8043c-142">This declaration defines a matrix of float values (32-bit floating-point numbers) with two rows and three columns:</span></span>


```
matrix <float, 2, 3> fFloatMatrix;
```



<span data-ttu-id="8043c-143">Матрица содержит значения, упорядоченные в строках и столбцах, к которым можно получить доступ с помощью оператора структуры ".", за которым следует один из двух наборов именования:</span><span class="sxs-lookup"><span data-stu-id="8043c-143">A matrix contains values organized in rows and columns, which can be accessed using the structure operator "." followed by one of two naming sets:</span></span>

-   <span data-ttu-id="8043c-144">Отсчитываемая от нуля расположение столбца строки:</span><span class="sxs-lookup"><span data-stu-id="8043c-144">The zero-based row-column position:</span></span>
    -   <span data-ttu-id="8043c-145">\_M00, \_ M01, \_ M02, \_ M03</span><span class="sxs-lookup"><span data-stu-id="8043c-145">\_m00, \_m01, \_m02, \_m03</span></span>
    -   <span data-ttu-id="8043c-146">\_M10, \_ M11, \_ M12, \_ M13</span><span class="sxs-lookup"><span data-stu-id="8043c-146">\_m10, \_m11, \_m12, \_m13</span></span>
    -   <span data-ttu-id="8043c-147">\_M20, \_ M21, \_ M22, \_ M23</span><span class="sxs-lookup"><span data-stu-id="8043c-147">\_m20, \_m21, \_m22, \_m23</span></span>
    -   <span data-ttu-id="8043c-148">\_M30, \_ M31, \_ M32, \_ M33</span><span class="sxs-lookup"><span data-stu-id="8043c-148">\_m30, \_m31, \_m32, \_m33</span></span>
-   <span data-ttu-id="8043c-149">Расположение строкового столбца, основанного на одной строке:</span><span class="sxs-lookup"><span data-stu-id="8043c-149">The one-based row-column position:</span></span>
    -   <span data-ttu-id="8043c-150">\_11, \_ 12, \_ 13, \_ 14</span><span class="sxs-lookup"><span data-stu-id="8043c-150">\_11, \_12, \_13, \_14</span></span>
    -   <span data-ttu-id="8043c-151">\_21, \_ 22, \_ 23, \_ 24</span><span class="sxs-lookup"><span data-stu-id="8043c-151">\_21, \_22, \_23, \_24</span></span>
    -   <span data-ttu-id="8043c-152">\_31, \_ 32, \_ 33, \_ 34</span><span class="sxs-lookup"><span data-stu-id="8043c-152">\_31, \_32, \_33, \_34</span></span>
    -   <span data-ttu-id="8043c-153">\_41, \_ 42, \_ 43, \_ 44</span><span class="sxs-lookup"><span data-stu-id="8043c-153">\_41, \_42, \_43, \_44</span></span>

<span data-ttu-id="8043c-154">Каждый набор именования начинается с символа подчеркивания, за которым следует номер строки и номер столбца.</span><span class="sxs-lookup"><span data-stu-id="8043c-154">Each naming set starts with an underscore followed by the row number and the column number.</span></span> <span data-ttu-id="8043c-155">Соглашение об отсчете от нуля также включает букву «m» перед номером строки и столбца.</span><span class="sxs-lookup"><span data-stu-id="8043c-155">The zero-based convention also includes the letter "m" before the row and column number.</span></span> <span data-ttu-id="8043c-156">Ниже приведен пример, в котором для доступа к матрице используются два набора именования:</span><span class="sxs-lookup"><span data-stu-id="8043c-156">Here's an example that uses the two naming sets to access a matrix:</span></span>


```
// given
float2x2 fMatrix = { 1.0f, 1.1f, // row 1
                     2.0f, 2.1f  // row 2
                   }; 

float f_1D;
f_1D = matrix._m00; // read the value in row 1, column 1: 1.0
f_1D = matrix._m11; // read the value in row 2, column 2: 2.1

f_1D = matrix._11;  // read the value in row 1, column 1: 1.0
f_1D = matrix._22;  // read the value in row 2, column 2: 2.1
```



<span data-ttu-id="8043c-157">Как и векторы, наборы имен могут использовать один или несколько компонентов из любого набора именований.</span><span class="sxs-lookup"><span data-stu-id="8043c-157">Just like vectors, naming sets can use one or more components from either naming set.</span></span>


```
// Given
float2x2 fMatrix = { 1.0f, 1.1f, // row 1
                     2.0f, 2.1f  // row 2
                   };
float2 temp;

temp = fMatrix._m00_m11 // valid
temp = fMatrix._m11_m00 // valid
temp = fMatrix._11_22   // valid
temp = fMatrix._22_11   // valid
```



<span data-ttu-id="8043c-158">Доступ к матрице также можно получить с помощью нотации доступа к массиву, которая представляет собой набор индексов, начинающийся с нуля.</span><span class="sxs-lookup"><span data-stu-id="8043c-158">A matrix can also be accessed using array access notation, which is a zero-based set of indices.</span></span> <span data-ttu-id="8043c-159">Каждый индекс находится внутри квадратных скобок.</span><span class="sxs-lookup"><span data-stu-id="8043c-159">Each index is inside of square brackets.</span></span> <span data-ttu-id="8043c-160">Доступ к матрице 4x4 осуществляется со следующими индексами:</span><span class="sxs-lookup"><span data-stu-id="8043c-160">A 4x4 matrix is accessed with the following indices:</span></span>

-   <span data-ttu-id="8043c-161">\[0 \] \[ 0 \] , \[ 0 \] \[ 1 \] , \[ 0 \] \[ 2 \] , \[ 0 \] \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="8043c-161">\[0\]\[0\], \[0\]\[1\], \[0\]\[2\], \[0\]\[3\]</span></span>
-   <span data-ttu-id="8043c-162">\[1 \] \[ 0 \] , \[ 1 \] \[ 1 \] , \[ 1 \] \[ 2 \] , \[ 1 \] \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="8043c-162">\[1\]\[0\], \[1\]\[1\], \[1\]\[2\], \[1\]\[3\]</span></span>
-   <span data-ttu-id="8043c-163">\[2 \] \[ 0 \] , \[ 2 \] \[ 1 \] , \[ 2 \] \[ 2 \] , \[ 2 \] \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="8043c-163">\[2\]\[0\], \[2\]\[1\], \[2\]\[2\], \[2\]\[3\]</span></span>
-   <span data-ttu-id="8043c-164">\[3 \] \[ 0 \] , \[ 3 \] \[ 1 \] , \[ 3 \] \[ 2 \] , \[ 3 \] \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="8043c-164">\[3\]\[0\], \[3\]\[1\], \[3\]\[2\], \[3\]\[3\]</span></span>

<span data-ttu-id="8043c-165">Ниже приведен пример доступа к матрице.</span><span class="sxs-lookup"><span data-stu-id="8043c-165">Here is an example of accessing a matrix:</span></span>


```
float2x2 fMatrix = { 1.0f, 1.1f, // row 1
                     2.0f, 2.1f  // row 2
                   };
float temp;

temp = fMatrix[0][0] // single component read
temp = fMatrix[0][1] // single component read
```



<span data-ttu-id="8043c-166">Обратите внимание, что оператор Structure "." не используется для доступа к массиву.</span><span class="sxs-lookup"><span data-stu-id="8043c-166">Notice that the structure operator "." is not used to access an array.</span></span> <span data-ttu-id="8043c-167">Нотация доступа к массиву не может использовать группирующие для чтения более чем одного компонента.</span><span class="sxs-lookup"><span data-stu-id="8043c-167">Array access notation cannot use swizzling to read more than one component.</span></span>


```
float2 temp;
temp = fMatrix[0][0]_[0][1] // invalid, cannot read two components
```



<span data-ttu-id="8043c-168">Однако доступ к массиву может считывать вектор с несколькими компонентами.</span><span class="sxs-lookup"><span data-stu-id="8043c-168">However, array accessing can read a multi-component vector.</span></span>


```
float2 temp;
float2x2 fMatrix;
temp = fMatrix[0] // read the first row
```



<span data-ttu-id="8043c-169">Как и в случае с векторами, чтение более одного компонента матрицы называется группирующие.</span><span class="sxs-lookup"><span data-stu-id="8043c-169">As with vectors, reading more than one matrix component is called swizzling.</span></span> <span data-ttu-id="8043c-170">Можно назначить более одного компонента, предполагая, что используется только одно пространство имен.</span><span class="sxs-lookup"><span data-stu-id="8043c-170">More than one component can be assigned, assuming only one name space is used.</span></span> <span data-ttu-id="8043c-171">Все это допустимые назначения:</span><span class="sxs-lookup"><span data-stu-id="8043c-171">These are all valid assignments:</span></span>


```
// Given these variables
float4x4 worldMatrix = float4( {0,0,0,0}, {1,1,1,1}, {2,2,2,2}, {3,3,3,3} );
float4x4 tempMatrix;

tempMatrix._m00_m11 = worldMatrix._m00_m11; // multiple components
tempMatrix._m00_m11 = worldMatrix.m13_m23;

tempMatrix._11_22_33 = worldMatrix._11_22_33; // any order on swizzles
tempMatrix._11_22_33 = worldMatrix._24_23_22;
```



<span data-ttu-id="8043c-172">Маскирование управляет количеством записываемых компонентов.</span><span class="sxs-lookup"><span data-stu-id="8043c-172">Masking controls how many components are written.</span></span>


```
// Given
float4x4 worldMatrix = float4( {0,0,0,0}, {1,1,1,1}, {2,2,2,2}, {3,3,3,3} );
float4x4 tempMatrix;

tempMatrix._m00_m11 = worldMatrix._m00_m11; // write two components
tempMatrix._m23_m00 = worldMatrix._m00_m11;
```



<span data-ttu-id="8043c-173">Назначения не могут быть записаны в один и тот же компонент несколько раз.</span><span class="sxs-lookup"><span data-stu-id="8043c-173">Assignments cannot be written to the same component more than once.</span></span> <span data-ttu-id="8043c-174">Поэтому левая часть оператора является недопустимой:</span><span class="sxs-lookup"><span data-stu-id="8043c-174">So the left side of this statement is invalid:</span></span>


```
// cannot write to the same component more than once
tempMatrix._m00_m00 = worldMatrix._m00_m11;
```



<span data-ttu-id="8043c-175">Кроме того, пространства имен компонентов не могут быть смешанными.</span><span class="sxs-lookup"><span data-stu-id="8043c-175">Also, the component name spaces cannot be mixed.</span></span> <span data-ttu-id="8043c-176">Это недопустимый компонент записи:</span><span class="sxs-lookup"><span data-stu-id="8043c-176">This is an invalid component write:</span></span>


```
// Invalid use of same component on left side
tempMatrix._11_m23 = worldMatrix._11_22; 
```



### <a name="matrix-ordering"></a><span data-ttu-id="8043c-177">Упорядочение матрицы</span><span class="sxs-lookup"><span data-stu-id="8043c-177">Matrix Ordering</span></span>

<span data-ttu-id="8043c-178">Порядок упаковки матрицы для однородных параметров по умолчанию имеет значение столбец-основной.</span><span class="sxs-lookup"><span data-stu-id="8043c-178">Matrix packing order for uniform parameters is set to column-major by default.</span></span> <span data-ttu-id="8043c-179">Это означает, что каждый столбец матрицы хранится в одном регистре констант.</span><span class="sxs-lookup"><span data-stu-id="8043c-179">This means each column of the matrix is stored in a single constant register.</span></span> <span data-ttu-id="8043c-180">С другой стороны, матрица, посвященная строке, построчно упаковывает каждую строку матрицы в один регистр констант.</span><span class="sxs-lookup"><span data-stu-id="8043c-180">On the other hand, a row-major matrix packs each row of the matrix in a single constant register.</span></span> <span data-ttu-id="8043c-181">Упаковку матрицы можно изменить с помощью директивы **\# \_ матрицы прагмапакк** , либо со **строкой \_** ключевого слова Major или **Column \_** .</span><span class="sxs-lookup"><span data-stu-id="8043c-181">Matrix packing can be changed with the **\#pragmapack\_matrix** directive, or with the **row\_major** or the **column\_major** keyword.</span></span>

<span data-ttu-id="8043c-182">Данные в матрице загружаются в постоянные регистры шейдера перед запуском шейдера.</span><span class="sxs-lookup"><span data-stu-id="8043c-182">The data in a matrix is loaded into shader constant registers before a shader runs.</span></span> <span data-ttu-id="8043c-183">Существует два способа считывания данных матрицы: в строке или в основном порядке столбцов.</span><span class="sxs-lookup"><span data-stu-id="8043c-183">There are two choices for how the matrix data is read: in row-major order or in column-major order.</span></span> <span data-ttu-id="8043c-184">«Столбец — основной» означает, что каждый столбец матрицы будет храниться в одном регистре констант, а «строковый порядок» означает, что каждая строка матрицы будет храниться в одном регистре констант.</span><span class="sxs-lookup"><span data-stu-id="8043c-184">Column-major order means that each matrix column will be stored in a single constant register, and row-major order means that each row of the matrix will be stored in a single constant register.</span></span> <span data-ttu-id="8043c-185">Это важно учитывать, сколько регистров констант используется для матрицы.</span><span class="sxs-lookup"><span data-stu-id="8043c-185">This is an important consideration for how many constant registers are used for a matrix.</span></span>

<span data-ttu-id="8043c-186">Основная матрица, представленная в виде строки, выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="8043c-186">A row-major matrix is laid out like the following:</span></span>

:::row:::
    :::column:::
        <span data-ttu-id="8043c-187">11</span><span class="sxs-lookup"><span data-stu-id="8043c-187">11</span></span><br/>
        <span data-ttu-id="8043c-188">21</span><span class="sxs-lookup"><span data-stu-id="8043c-188">21</span></span><br/>
        <span data-ttu-id="8043c-189">31</span><span class="sxs-lookup"><span data-stu-id="8043c-189">31</span></span><br/>
        <span data-ttu-id="8043c-190">41</span><span class="sxs-lookup"><span data-stu-id="8043c-190">41</span></span><br/>
    :::column-end:::
    :::column:::
        <span data-ttu-id="8043c-191">12</span><span class="sxs-lookup"><span data-stu-id="8043c-191">12</span></span><br/>
        <span data-ttu-id="8043c-192">22</span><span class="sxs-lookup"><span data-stu-id="8043c-192">22</span></span><br/>
        <span data-ttu-id="8043c-193">32</span><span class="sxs-lookup"><span data-stu-id="8043c-193">32</span></span><br/>
        <span data-ttu-id="8043c-194">42</span><span class="sxs-lookup"><span data-stu-id="8043c-194">42</span></span><br/>
    :::column-end:::
    :::column:::
        <span data-ttu-id="8043c-195">13</span><span class="sxs-lookup"><span data-stu-id="8043c-195">13</span></span><br/>
        <span data-ttu-id="8043c-196">23</span><span class="sxs-lookup"><span data-stu-id="8043c-196">23</span></span><br/>
        <span data-ttu-id="8043c-197">33</span><span class="sxs-lookup"><span data-stu-id="8043c-197">33</span></span><br/>
        <span data-ttu-id="8043c-198">43</span><span class="sxs-lookup"><span data-stu-id="8043c-198">43</span></span><br/>
    :::column-end:::
    :::column:::
        <span data-ttu-id="8043c-199">14</span><span class="sxs-lookup"><span data-stu-id="8043c-199">14</span></span><br/>
        <span data-ttu-id="8043c-200">24</span><span class="sxs-lookup"><span data-stu-id="8043c-200">24</span></span><br/>
        <span data-ttu-id="8043c-201">34</span><span class="sxs-lookup"><span data-stu-id="8043c-201">34</span></span><br/>
        <span data-ttu-id="8043c-202">44</span><span class="sxs-lookup"><span data-stu-id="8043c-202">44</span></span><br/>
    :::column-end:::
:::row-end:::




 

<span data-ttu-id="8043c-203">Основная матрица столбца выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="8043c-203">A column-major matrix is laid out like the following:</span></span>


:::row:::
    :::column:::
        <span data-ttu-id="8043c-204">11</span><span class="sxs-lookup"><span data-stu-id="8043c-204">11</span></span><br/>
        <span data-ttu-id="8043c-205">12</span><span class="sxs-lookup"><span data-stu-id="8043c-205">12</span></span><br/>
        <span data-ttu-id="8043c-206">13</span><span class="sxs-lookup"><span data-stu-id="8043c-206">13</span></span><br/>
        <span data-ttu-id="8043c-207">14</span><span class="sxs-lookup"><span data-stu-id="8043c-207">14</span></span><br/>
    :::column-end:::
    :::column:::
        <span data-ttu-id="8043c-208">21</span><span class="sxs-lookup"><span data-stu-id="8043c-208">21</span></span><br/>
        <span data-ttu-id="8043c-209">22</span><span class="sxs-lookup"><span data-stu-id="8043c-209">22</span></span><br/>
        <span data-ttu-id="8043c-210">23</span><span class="sxs-lookup"><span data-stu-id="8043c-210">23</span></span><br/>
        <span data-ttu-id="8043c-211">24</span><span class="sxs-lookup"><span data-stu-id="8043c-211">24</span></span><br/>
    :::column-end:::
    :::column:::
        <span data-ttu-id="8043c-212">31</span><span class="sxs-lookup"><span data-stu-id="8043c-212">31</span></span><br/>
        <span data-ttu-id="8043c-213">32</span><span class="sxs-lookup"><span data-stu-id="8043c-213">32</span></span><br/>
        <span data-ttu-id="8043c-214">33</span><span class="sxs-lookup"><span data-stu-id="8043c-214">33</span></span><br/>
        <span data-ttu-id="8043c-215">34</span><span class="sxs-lookup"><span data-stu-id="8043c-215">34</span></span><br/>
    :::column-end:::
    :::column:::
        <span data-ttu-id="8043c-216">14</span><span class="sxs-lookup"><span data-stu-id="8043c-216">14</span></span><br/>
        <span data-ttu-id="8043c-217">24</span><span class="sxs-lookup"><span data-stu-id="8043c-217">24</span></span><br/>
        <span data-ttu-id="8043c-218">34</span><span class="sxs-lookup"><span data-stu-id="8043c-218">34</span></span><br/>
        <span data-ttu-id="8043c-219">44</span><span class="sxs-lookup"><span data-stu-id="8043c-219">44</span></span><br/>
    :::column-end:::
:::row-end:::




 

<span data-ttu-id="8043c-220">Упорядочение по строкам и основным столбцам определяет порядок, в котором компоненты матрицы считываются из входных шейдеров.</span><span class="sxs-lookup"><span data-stu-id="8043c-220">Row-major and column-major matrix ordering determine the order the matrix components are read from shader inputs.</span></span> <span data-ttu-id="8043c-221">После того как данные записываются в постоянные регистры, порядок матриц не влияет на использование данных или доступ из него в коде шейдера.</span><span class="sxs-lookup"><span data-stu-id="8043c-221">Once the data is written into constant registers, matrix order has no effect on how the data is used or accessed from within shader code.</span></span> <span data-ttu-id="8043c-222">Кроме того, матрицы, объявленные в теле шейдера, не упаковываются в постоянные регистры.</span><span class="sxs-lookup"><span data-stu-id="8043c-222">Also, matrices declared in a shader body do not get packed into constant registers.</span></span> <span data-ttu-id="8043c-223">Порядок упаковки строк и столбцов в основном и крупном порядке не влияет на порядок упаковки конструкторов (который всегда соответствует строкам в основном порядке).</span><span class="sxs-lookup"><span data-stu-id="8043c-223">Row-major and column-major packing order has no influence on the packing order of constructors (which always follows row-major ordering).</span></span>

<span data-ttu-id="8043c-224">Порядок данных в матрице может быть объявлен во время компиляции, или компилятор будет упорядочивать данные в среде выполнения для наиболее эффективного использования.</span><span class="sxs-lookup"><span data-stu-id="8043c-224">The order of the data in a matrix can be declared at compile time or the compiler will order the data at runtime for the most efficient use.</span></span>

## <a name="examples"></a><span data-ttu-id="8043c-225">Примеры</span><span class="sxs-lookup"><span data-stu-id="8043c-225">Examples</span></span>

<span data-ttu-id="8043c-226">HLSL использует два специальных типа: Векторный тип и тип матрицы, чтобы упростить программирование двухмерной и трехмерной графики.</span><span class="sxs-lookup"><span data-stu-id="8043c-226">HLSL uses two special types, a vector type and a matrix type to make programming 2D and 3D graphics easier.</span></span> <span data-ttu-id="8043c-227">Каждый из этих типов содержит более одного компонента; Вектор содержит до четырех компонентов, а матрица содержит до 16 компонентов.</span><span class="sxs-lookup"><span data-stu-id="8043c-227">Each of these types contain more than one component; a vector contains up to four components, and a matrix contains up to 16 components.</span></span> <span data-ttu-id="8043c-228">Если векторы и матрицы используются в стандартных уравнениях HLSL, математические операции предназначены для работы с каждым компонентом.</span><span class="sxs-lookup"><span data-stu-id="8043c-228">When vectors and matrices are used in standard HLSL equations, the math performed is designed to work per-component.</span></span> <span data-ttu-id="8043c-229">Например, HLSL реализует это умножение:</span><span class="sxs-lookup"><span data-stu-id="8043c-229">For instance, HLSL implements this multiply:</span></span>


```
float4 v = a*b;
```



<span data-ttu-id="8043c-230">при умножении четырех компонентов.</span><span class="sxs-lookup"><span data-stu-id="8043c-230">as a four-component multiply.</span></span> <span data-ttu-id="8043c-231">Результат имеет четыре скалярных оператора:</span><span class="sxs-lookup"><span data-stu-id="8043c-231">The result is four scalars:</span></span>


```
float4 v = a*b;

v.x = a.x*b.x;
v.y = a.y*b.y;
v.z = a.z*b.z;
v.w = a.w*b.w;
```



<span data-ttu-id="8043c-232">Это четыре умножения, где каждый результат хранится в отдельном компоненте v.</span><span class="sxs-lookup"><span data-stu-id="8043c-232">This is four multiplications where each result is stored in a separate component of v.</span></span> <span data-ttu-id="8043c-233">Это называется умножением четырех компонентов.</span><span class="sxs-lookup"><span data-stu-id="8043c-233">This is called a four-component multiply.</span></span> <span data-ttu-id="8043c-234">HLSL использует математические компоненты, что делает создание шейдеров очень эффективным.</span><span class="sxs-lookup"><span data-stu-id="8043c-234">HLSL uses component math which makes writing shaders very efficient.</span></span>

<span data-ttu-id="8043c-235">Это сильно отличается от умножения, которое обычно реализуется в виде точки, которая создает один скаляр:</span><span class="sxs-lookup"><span data-stu-id="8043c-235">This is very different from a multiply which is typically implemented as a dot product which generates a single scalar:</span></span>


```
v = a.x*b.x + a.y*b.y + a.z*b.z + a.w*b.w;
```



<span data-ttu-id="8043c-236">Матрица также использует операции для каждого компонента в HLSL:</span><span class="sxs-lookup"><span data-stu-id="8043c-236">A matrix also uses per-component operations in HLSL:</span></span>


```
float3x3 mat1,mat2;
...
float3x3 mat3 = mat1*mat2;
```



<span data-ttu-id="8043c-237">Результат является отдельным компонентом, умноженным на две матрицы (в отличие от стандартной матрицы 3x3).</span><span class="sxs-lookup"><span data-stu-id="8043c-237">The result is a per-component multiply of the two matrices (as opposed to a standard 3x3 matrix multiply).</span></span> <span data-ttu-id="8043c-238">Матрица для каждого компонента возвращает этот первый термин:</span><span class="sxs-lookup"><span data-stu-id="8043c-238">A per component matrix multiply yields this first term:</span></span>


```
mat3.m00 = mat1.m00 * mat2._m00;
```



<span data-ttu-id="8043c-239">Это отличается от умножения матрицы 3x3, что приведет к первому условию:</span><span class="sxs-lookup"><span data-stu-id="8043c-239">This is different from a 3x3 matrix multiply which would yield this first term:</span></span>


```
// First component of a four-component matrix multiply
mat.m00 = mat1._m00 * mat2._m00 + 
          mat1._m01 * mat2._m10 + 
          mat1._m02 * mat2._m20 + 
          mat1._m03 * mat2._m30;
```



<span data-ttu-id="8043c-240">Перегруженные версии метода умножения встроенных функций, где один операнд является вектором, а другой — матрицей.</span><span class="sxs-lookup"><span data-stu-id="8043c-240">Overloaded versions of the multiply intrinsic function handle cases where one operand is a vector and the other operand is a matrix.</span></span> <span data-ttu-id="8043c-241">Например: вектор вектора \* , \* Матрица вектора, вектор матрицы и матрица \* матрицы \* .</span><span class="sxs-lookup"><span data-stu-id="8043c-241">Such as: vector \* vector, vector \* matrix, matrix \* vector, and matrix \* matrix.</span></span> <span data-ttu-id="8043c-242">Например:</span><span class="sxs-lookup"><span data-stu-id="8043c-242">For instance:</span></span>


```
float4x3 World;

float4 main(float4 pos : SV_POSITION) : SV_POSITION
{
    float4 val;
    val.xyz = mul(pos,World);
    val.w = 0;

    return val;
}   
```



<span data-ttu-id="8043c-243">выдает тот же результат, что и:</span><span class="sxs-lookup"><span data-stu-id="8043c-243">produces the same result as:</span></span>


```
float4x3 World;

float4 main(float4 pos : SV_POSITION) : SV_POSITION
{
    float4 val;
    val.xyz = (float3) mul((float1x4)pos,World);
    val.w = 0;

    return val;
}   
```



<span data-ttu-id="8043c-244">В этом примере демонстрируется преобразование вектора POS в вектор столбца с помощью приведения (float1x4).</span><span class="sxs-lookup"><span data-stu-id="8043c-244">This example casts the pos vector to a column vector using the (float1x4) cast.</span></span> <span data-ttu-id="8043c-245">Изменение вектора путем приведения или переключение порядка аргументов, передаваемых для перемножения, эквивалентно преобразованию матрицы.</span><span class="sxs-lookup"><span data-stu-id="8043c-245">Changing a vector by casting, or swapping the order of the arguments supplied to multiply is equivalent to transposing the matrix.</span></span>

<span data-ttu-id="8043c-246">Автоматическое преобразование приведения приводит к тому, что встроенные функции умножения и точки возвращают те же результаты, что и здесь:</span><span class="sxs-lookup"><span data-stu-id="8043c-246">Automatic cast conversion causes the multiply and dot intrinsic functions to return the same results as used here:</span></span>


```
{
  float4 val;
  return mul(val,val);
}
```



<span data-ttu-id="8043c-247">Результатом умножения является \* 4 экземпляра 1ный вектор «1x4» = 1x1.</span><span class="sxs-lookup"><span data-stu-id="8043c-247">This result of the multiply is a 1x4 \* 4x1 = 1x1 vector.</span></span> <span data-ttu-id="8043c-248">Это эквивалентно продукту с точкой:</span><span class="sxs-lookup"><span data-stu-id="8043c-248">This is equivalent to a dot product:</span></span>


```
{
  float4 val;
  return dot(val,val);
}
```



<span data-ttu-id="8043c-249">, возвращающее одиночное скалярное значение.</span><span class="sxs-lookup"><span data-stu-id="8043c-249">which returns a single scalar value.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8043c-250">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="8043c-250">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8043c-251">Типы данных (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8043c-251">Data Types (DirectX HLSL)</span></span>](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 

 




