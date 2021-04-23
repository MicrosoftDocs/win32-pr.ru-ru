---
title: Многомерные массивы
description: Атрибуты массива также можно использовать с многомерными массивами.
ms.assetid: a01b904c-fbe8-4af4-8393-6864f7ef7364
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6eb7bcf94d97e1f35fdd6ab432ea5869e47f79ed
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103987728"
---
# <a name="multidimensional-arrays"></a><span data-ttu-id="250ad-103">Многомерные массивы</span><span class="sxs-lookup"><span data-stu-id="250ad-103">Multidimensional Arrays</span></span>

<span data-ttu-id="250ad-104">Атрибуты массива также можно использовать с многомерными массивами.</span><span class="sxs-lookup"><span data-stu-id="250ad-104">Array attributes can also be used with multidimensional arrays.</span></span> <span data-ttu-id="250ad-105">Однако будьте внимательны, чтобы гарантировать, что каждое измерение массива имеет соответствующий атрибут.</span><span class="sxs-lookup"><span data-stu-id="250ad-105">However, be careful to ensure that every dimension of the array has a corresponding attribute.</span></span> <span data-ttu-id="250ad-106">Пример:</span><span class="sxs-lookup"><span data-stu-id="250ad-106">For example:</span></span>

``` syntax
/* IDL file */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(2.0)
]
interface multiarray
{
  void arr2d( [in] short        d1size,
              [in] short        d2len,
              [in, size_is( d1size, ), length_is ( , d2len) ] long array2d[*][30] ) ;
}
```

<span data-ttu-id="250ad-107">Предыдущий массив является согласованным массивом (размером d1size) из 30 массивов элементов (с элементами d2len, поставляющимися для каждого).</span><span class="sxs-lookup"><span data-stu-id="250ad-107">The preceding array is a conformant array (of size d1size ) of 30 element arrays (with d2len elements shipped for each).</span></span> <span data-ttu-id="250ad-108">Запятая в круглых скобках \[ [**размера \_**](/windows/desktop/Midl/size-is) \] Attribute указывает, что значение в d1size применяется к первому измерению массива.</span><span class="sxs-lookup"><span data-stu-id="250ad-108">The comma in the parentheses of the \[[**size\_is**](/windows/desktop/Midl/size-is)\] attribute specifies that value in d1size is applied to the first dimension of the array.</span></span> <span data-ttu-id="250ad-109">Аналогичным образом, команда в круглых скобках \[ [**атрибута \_ length**](/windows/desktop/Midl/length-is) \] указывает, что значение в d2len применяется ко второму измерению массива.</span><span class="sxs-lookup"><span data-stu-id="250ad-109">Likewise, the command in the parentheses of the \[[**length\_is**](/windows/desktop/Midl/length-is)\] attribute indicates that the value in d2len is applied to the second dimension of the array.</span></span>

<span data-ttu-id="250ad-110">Компилятор MIDL 2,0 предоставляет два метода для маршалирования параметров: смешанный режим (/**ОС**) и полностью интерпретируемый (/**ОИФ** или/**оикф**).</span><span class="sxs-lookup"><span data-stu-id="250ad-110">The MIDL 2.0 compiler provides two methods for marshaling parameters: mixed-mode (/**Os**) and fully-interpreted (/**Oif** or /**Oicf**).</span></span> <span data-ttu-id="250ad-111">По умолчанию компилятор MIDL компилирует интерфейсы в смешанном режиме.</span><span class="sxs-lookup"><span data-stu-id="250ad-111">By default, the MIDL compiler compiles interfaces in mixed mode.</span></span> <span data-ttu-id="250ad-112">Не нужно явно указывать параметр [**/OS**](/windows/desktop/Midl/-os) для получения упакованного смешанного режима.</span><span class="sxs-lookup"><span data-stu-id="250ad-112">You do not need to explicitly specify the [**/Os**](/windows/desktop/Midl/-os) switch to get mixed-mode marshaling.</span></span>

<span data-ttu-id="250ad-113">Полностью интерпретируемый метод маршалирует данные полностью в автономном режиме.</span><span class="sxs-lookup"><span data-stu-id="250ad-113">The fully-interpreted method marshals data completely offline.</span></span> <span data-ttu-id="250ad-114">Это значительно сокращает размер кода заглушки, но также приводит к снижению производительности.</span><span class="sxs-lookup"><span data-stu-id="250ad-114">This reduces the size of the stub code considerably, but it also results in decreased performance.</span></span> <span data-ttu-id="250ad-115">В смешанном режиме упаковки заглушки маршалируются некоторые параметры в режиме в сети.</span><span class="sxs-lookup"><span data-stu-id="250ad-115">In mixed-mode marshaling, the stubs marshals some parameters online.</span></span> <span data-ttu-id="250ad-116">Хотя это приводит к увеличению размера заглушки, оно также обеспечивает повышенную производительность.</span><span class="sxs-lookup"><span data-stu-id="250ad-116">While this results in a larger stub size, it also offers increased performance.</span></span>

> [!Caution]  
> <span data-ttu-id="250ad-117">Соблюдайте осторожность при компиляции IDL-файлов в этом режиме.</span><span class="sxs-lookup"><span data-stu-id="250ad-117">Exercise caution when compiling IDL files in this mode.</span></span> <span data-ttu-id="250ad-118">Использование многомерных массивов в смешанном режиме может привести к неправильному маршалировании параметров.</span><span class="sxs-lookup"><span data-stu-id="250ad-118">Using multidimensional arrays in mixed mode can result in parameters that are not marshaled correctly.</span></span> <span data-ttu-id="250ad-119">Параметр командной строки [**/Oicf**](/windows/desktop/Midl/-oi) рекомендуется использовать, если интерфейс определяет параметры многомерных массивов.</span><span class="sxs-lookup"><span data-stu-id="250ad-119">The [**/Oicf**](/windows/desktop/Midl/-oi) command line switch is recommended when your interface defines parameters that are multidimensional arrays.</span></span>

 

<span data-ttu-id="250ad-120">Атрибут \[ [**String**](/windows/desktop/Midl/string) \] можно также использовать с многомерными массивами.</span><span class="sxs-lookup"><span data-stu-id="250ad-120">The \[[**string**](/windows/desktop/Midl/string)\] attribute can also be used with multidimensional arrays.</span></span> <span data-ttu-id="250ad-121">Атрибут применяется к наименее значимому измерению, такому как согласованный массив строк.</span><span class="sxs-lookup"><span data-stu-id="250ad-121">The attribute applies to the least significant dimension, such as a conformant array of strings.</span></span> <span data-ttu-id="250ad-122">Можно также использовать атрибуты многомерных указателей.</span><span class="sxs-lookup"><span data-stu-id="250ad-122">You can also use multidimensional pointer attributes.</span></span> <span data-ttu-id="250ad-123">Пример:</span><span class="sxs-lookup"><span data-stu-id="250ad-123">For example:</span></span>

``` syntax
/* IDL file */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(2.0)
]
interface multiarray
{
  void arr2d([in] short  d1len,
             [in] short  d2len,
             [in] size_is(d1len, d2len) ] long  ** ptr2d) ;
}
```

<span data-ttu-id="250ad-124">В предыдущем примере переменная ptr2d является указателем на блок указателей d1len, каждый из которых указывает на значение **Long** в указателе на d2len.</span><span class="sxs-lookup"><span data-stu-id="250ad-124">In the preceding example, the variable ptr2d is a pointer to a d1len-sized block of pointers, each of which points to d2len pointers to **long**.</span></span>

<span data-ttu-id="250ad-125">Многомерные массивы не эквивалентны массивам указателей.</span><span class="sxs-lookup"><span data-stu-id="250ad-125">Multidimensional arrays are not equivalent to arrays of pointers.</span></span> <span data-ttu-id="250ad-126">Многомерный массив — это один большой блок данных в памяти.</span><span class="sxs-lookup"><span data-stu-id="250ad-126">A multidimensional array is a single, large block of data in memory.</span></span> <span data-ttu-id="250ad-127">Массив указателей содержит только блок указателей в массиве.</span><span class="sxs-lookup"><span data-stu-id="250ad-127">An array of pointers only contains a block of pointers in the array.</span></span> <span data-ttu-id="250ad-128">Данные, на которые указывают указатели, могут находиться в любом месте памяти.</span><span class="sxs-lookup"><span data-stu-id="250ad-128">The data that the pointers point to can be anywhere in memory.</span></span> <span data-ttu-id="250ad-129">Кроме того, синтаксис ANSI C позволяет не указывать наиболее значимое (крайнее самое левое) измерение массива в многомерном массиве.</span><span class="sxs-lookup"><span data-stu-id="250ad-129">Also, ANSI C syntax allows only the most significant (leftmost) array dimension to be unspecified in a multidimensional array.</span></span> <span data-ttu-id="250ad-130">Поэтому ниже приведена допустимая инструкция:</span><span class="sxs-lookup"><span data-stu-id="250ad-130">Therefore, the following is a valid statement:</span></span>

`long a1[] [20]`

<span data-ttu-id="250ad-131">Сравните это с следующей недопустимой инструкцией:</span><span class="sxs-lookup"><span data-stu-id="250ad-131">Compare this to the following invalid statement:</span></span>

`long a1[20] []`

 

 