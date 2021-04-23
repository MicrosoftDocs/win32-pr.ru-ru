---
title: Тип матрицы
description: Матрица — это специальный тип данных, содержащий от одного до шестнадцати компонентов. Каждый компонент матрицы должен быть одного типа.
ms.assetid: 728eb472-103d-4c7f-b6f6-e515fc024801
keywords:
- Тип матрицы HLSL
topic_type:
- apiref
api_name:
- Matrix Type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c580706a2ddae3e4a94c138a1ca0f6932457732a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104068784"
---
# <a name="matrix-type"></a><span data-ttu-id="3c0dc-105">Тип матрицы</span><span class="sxs-lookup"><span data-stu-id="3c0dc-105">Matrix Type</span></span>

<span data-ttu-id="3c0dc-106">Матрица — это специальный тип данных, содержащий от одного до шестнадцати компонентов.</span><span class="sxs-lookup"><span data-stu-id="3c0dc-106">A matrix is a special data type that contains between one and sixteen components.</span></span> <span data-ttu-id="3c0dc-107">Каждый компонент матрицы должен быть одного типа.</span><span class="sxs-lookup"><span data-stu-id="3c0dc-107">Every component of a matrix must be of the same type.</span></span>



|                         |
|-------------------------|
| <span data-ttu-id="3c0dc-108">**Имя Типекомпонентс**</span><span class="sxs-lookup"><span data-stu-id="3c0dc-108">**TypeComponents Name**</span></span> |



 

## <a name="components"></a><span data-ttu-id="3c0dc-109">Компоненты</span><span class="sxs-lookup"><span data-stu-id="3c0dc-109">Components</span></span>



| <span data-ttu-id="3c0dc-110">Элемент</span><span class="sxs-lookup"><span data-stu-id="3c0dc-110">Item</span></span>                                                                                                                             | <span data-ttu-id="3c0dc-111">Описание</span><span class="sxs-lookup"><span data-stu-id="3c0dc-111">Description</span></span>                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c0dc-112"><span id="TypeComponents"></span><span id="typecomponents"></span><span id="TYPECOMPONENTS"></span>**типекомпонентс**</span><span class="sxs-lookup"><span data-stu-id="3c0dc-112"><span id="TypeComponents"></span><span id="typecomponents"></span><span id="TYPECOMPONENTS"></span>**TypeComponents**</span></span><br/> | <span data-ttu-id="3c0dc-113">Одно имя, содержащее три части.</span><span class="sxs-lookup"><span data-stu-id="3c0dc-113">A single name that contains three parts.</span></span> <span data-ttu-id="3c0dc-114">Первая часть является одним из [скалярных](dx-graphics-hlsl-data-types.md) типов.</span><span class="sxs-lookup"><span data-stu-id="3c0dc-114">The first part is one of the [scalar](dx-graphics-hlsl-data-types.md) types.</span></span> <span data-ttu-id="3c0dc-115">Вторая часть — число строк.</span><span class="sxs-lookup"><span data-stu-id="3c0dc-115">The second part is the number of rows.</span></span> <span data-ttu-id="3c0dc-116">Третья часть — число столбцов.</span><span class="sxs-lookup"><span data-stu-id="3c0dc-116">The third part is the number of columns.</span></span> <span data-ttu-id="3c0dc-117">Число строк и столбцов является положительным целым числом от 1 до 4 включительно.</span><span class="sxs-lookup"><span data-stu-id="3c0dc-117">The number of rows and columns is a positive integer between 1 and 4 inclusive.</span></span><br/> |
| <span data-ttu-id="3c0dc-118"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Безымян**</span><span class="sxs-lookup"><span data-stu-id="3c0dc-118"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Name**</span></span><br/>                                         | <span data-ttu-id="3c0dc-119">Строка ASCII, однозначно определяющая имя переменной.</span><span class="sxs-lookup"><span data-stu-id="3c0dc-119">An ASCII string that uniquely identifies the variable name.</span></span><br/>                                                                                                                                                                                                                            |



 

## <a name="examples"></a><span data-ttu-id="3c0dc-120">Примеры</span><span class="sxs-lookup"><span data-stu-id="3c0dc-120">Examples</span></span>

<span data-ttu-id="3c0dc-121">Ниже приводится несколько примеров.</span><span class="sxs-lookup"><span data-stu-id="3c0dc-121">Here are some examples:</span></span>


```
int1x1    iMatrix;   // integer matrix with 1 row,  1 column
int4x1    iMatrix;   // integer matrix with 4 rows, 1 column
int1x4    iMatrix;   // integer matrix with 1 row, 4 columns
double3x3 dMatrix;   // double matrix with 3 rows, 3 columns

float2x2 fMatrix = { 0.0f, 0.1, // row 1
                     2.1f, 2.2f // row 2
                   };   
```



<span data-ttu-id="3c0dc-122">Матрицу можно объявить с помощью этого синтаксиса:</span><span class="sxs-lookup"><span data-stu-id="3c0dc-122">A matrix can be declared using this syntax also:</span></span>


```
matrix <Type, Number> VariableName
```



<span data-ttu-id="3c0dc-123">Тип матрицы использует угловые скобки для указания типа, числа строк и числа столбцов.</span><span class="sxs-lookup"><span data-stu-id="3c0dc-123">The matrix type uses the angle brackets to specify the type, the number of rows, and the number of columns.</span></span> <span data-ttu-id="3c0dc-124">В этом примере создается матрица с плавающей точкой с двумя строками и двумя столбцами.</span><span class="sxs-lookup"><span data-stu-id="3c0dc-124">This example creates a floating-point matrix, with two rows and two columns.</span></span> <span data-ttu-id="3c0dc-125">Можно использовать любой скалярный тип данных.</span><span class="sxs-lookup"><span data-stu-id="3c0dc-125">Any of the scalar data types can be used.</span></span>

<span data-ttu-id="3c0dc-126">Пример:</span><span class="sxs-lookup"><span data-stu-id="3c0dc-126">Here is an example:</span></span>


```
matrix <float, 2, 2> fMatrix = { 0.0f, 0.1, // row 1
                                 2.1f, 2.2f // row 2
                               };
```



## <a name="see-also"></a><span data-ttu-id="3c0dc-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3c0dc-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c0dc-128">Типы данных (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3c0dc-128">Data Types (DirectX HLSL)</span></span>](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 

 





