---
title: Массивы MIDL
description: Массивы MIDL.
ms.assetid: dee30788-0575-4b49-a6b8-5208ad295183
keywords:
- типы данных MIDL, массивы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78c5ca08740084783f615d2cd34b46f0de4a4020
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104069949"
---
# <a name="midl-arrays"></a><span data-ttu-id="12237-104">Массивы MIDL</span><span class="sxs-lookup"><span data-stu-id="12237-104">MIDL Arrays</span></span>

<span data-ttu-id="12237-105">Деклараторы массивов отображаются в теле интерфейса IDL в виде одного из следующих элементов:</span><span class="sxs-lookup"><span data-stu-id="12237-105">Array declarators appear in the interface body of the IDL file as one of the following:</span></span>

-   <span data-ttu-id="12237-106">Часть общего объявления</span><span class="sxs-lookup"><span data-stu-id="12237-106">Part of a general declaration</span></span>
-   <span data-ttu-id="12237-107">Член структуры или декларатора объединения</span><span class="sxs-lookup"><span data-stu-id="12237-107">A member of a structure or union declarator</span></span>
-   <span data-ttu-id="12237-108">Параметр для удаленного вызова процедуры</span><span class="sxs-lookup"><span data-stu-id="12237-108">A parameter to a remote procedure call</span></span>

<span data-ttu-id="12237-109">Границы каждого измерения массива выражаются внутри отдельной пары квадратных скобок.</span><span class="sxs-lookup"><span data-stu-id="12237-109">The bounds of each dimension of the array are expressed inside a separate pair of square brackets.</span></span> <span data-ttu-id="12237-110">Выражение, результатом которого является *n* , означает нижнюю границу, равную нулю, и верхнюю границу *n-1*.</span><span class="sxs-lookup"><span data-stu-id="12237-110">An expression that evaluates to *n* signifies a lower bound of zero and an upper bound of *n - 1*.</span></span> <span data-ttu-id="12237-111">Если квадратные скобки пусты или содержат одну звездочку ( \* ), Нижняя граница равна нулю, а верхняя граница определяется во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="12237-111">If the square brackets are empty or contain a single asterisk (\*), the lower bound is zero and the upper bound is determined at runtime.</span></span>

<span data-ttu-id="12237-112">Массив также может содержать два значения, разделенные многоточием, которые представляют нижнюю и верхнюю границы массива, как показано \[ *ниже*... *верхний* \] .</span><span class="sxs-lookup"><span data-stu-id="12237-112">The array can also contain two values separated by an ellipsis that represent the lower and upper bounds of the array, as in \[*lower*...*upper*\].</span></span> <span data-ttu-id="12237-113">Для Microsoft RPC требуется нижняя граница, равная нулю.</span><span class="sxs-lookup"><span data-stu-id="12237-113">Microsoft RPC requires a lower bound of zero.</span></span> <span data-ttu-id="12237-114">Компилятор MIDL не распознает конструкции, указывающие ненулевые нижние границы.</span><span class="sxs-lookup"><span data-stu-id="12237-114">The MIDL compiler does not recognize constructs that specify nonzero lower bounds.</span></span>

<span data-ttu-id="12237-115">Массивы могут быть связаны с атрибутами [**поля size \_ —**](size-is.md), [**Max \_ —**](max-is.md), [**length \_ —**](length-is.md), [**First \_ —**](first-is.md), а [**Last \_ —**](last-is.md) указать размер массива или часть массива, которая содержит допустимые данные.</span><span class="sxs-lookup"><span data-stu-id="12237-115">Arrays can be associated with the field attributes [**size\_is**](size-is.md), [**max\_is**](max-is.md), [**length\_is**](length-is.md), [**first\_is**](first-is.md), and [**last\_is**](last-is.md) to specify the size of the array or the part of the array that contains valid data.</span></span> <span data-ttu-id="12237-116">Эти атрибуты полей определяют параметр, поле структуры или константу, указывающую измерение или индекс массива.</span><span class="sxs-lookup"><span data-stu-id="12237-116">These field attributes identify the parameter, structure field, or constant that specifies the array dimension or index.</span></span>

<span data-ttu-id="12237-117">Массив должен быть связан с идентификатором, указанным в атрибуте Field следующим образом: Если массив является параметром, идентификатор также должен быть параметром той же функции. Если массив является полем структуры, идентификатор должен быть другим полем структуры этой же структуры.</span><span class="sxs-lookup"><span data-stu-id="12237-117">The array must be associated with the identifier specified by the field attribute in the following way: When the array is a parameter, the identifier must also be a parameter to the same function; when the array is a structure field, the identifier must be another structure field of that same structure.</span></span>

<span data-ttu-id="12237-118">Массив называется "согласованным", если верхняя граница любого измерения определяется во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="12237-118">An array is called "conformant" if the upper bound of any dimension is determined at runtime.</span></span> <span data-ttu-id="12237-119">(Во время выполнения можно определить только верхние границы.) Для определения верхней границы в объявлении массива должен быть указан атрибут [**size \_**](size-is.md) или [**Max. \_**](max-is.md)</span><span class="sxs-lookup"><span data-stu-id="12237-119">(Only upper bounds can be determined at runtime.) To determine the upper bound, the array declaration must include a [**size\_is**](size-is.md) or [**max\_is**](max-is.md) attribute.</span></span>

<span data-ttu-id="12237-120">Массив называется "разной", если его границы определяются во время компиляции, но диапазон переданных элементов определяется в среде выполнения.</span><span class="sxs-lookup"><span data-stu-id="12237-120">An array is called "varying" when its bounds are determined at compile time, but the range of transmitted elements is determined at runtime.</span></span> <span data-ttu-id="12237-121">Чтобы определить диапазон переданных элементов, в объявлении массива должна быть указана [**длина \_**](length-is.md), [**первый \_ —**](first-is.md), или [**Last \_ —**](last-is.md) атрибут.</span><span class="sxs-lookup"><span data-stu-id="12237-121">To determine the range of transmitted elements, the array declaration must include a [**length\_is**](length-is.md), [**first\_is**](first-is.md), or [**last\_is**](last-is.md) attribute.</span></span>

<span data-ttu-id="12237-122">Согласованный переменный массив (также называемый "Open") — это массив, верхняя граница которого и диапазон передаваемых элементов определяются во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="12237-122">A conformant varying array (also called "open") is an array whose upper bound and range of transmitted elements are determined at runtime.</span></span> <span data-ttu-id="12237-123">Не более одного согласованного или согласованного переменного массива может быть вложен в структуру C и должен быть последним элементом структуры.</span><span class="sxs-lookup"><span data-stu-id="12237-123">At most, one conformant or conformant varying array can be nested in a C structure and must be the last element of the structure.</span></span> <span data-ttu-id="12237-124">В отличие от этого, несоответствующие различные массивы могут находиться в любом месте структуры.</span><span class="sxs-lookup"><span data-stu-id="12237-124">In contrast, nonconformant varying arrays can occur anywhere in a structure.</span></span>

## <a name="examples"></a><span data-ttu-id="12237-125">Примеры</span><span class="sxs-lookup"><span data-stu-id="12237-125">Examples</span></span>

``` syntax
/* IDL file interface body */ 
#define MAX_INDEX 10 
 
typedef char  ATYPE[MAX_INDEX]; 
typedef short BTYPE[];        // Equivalent to [*]; 
typedef long  CTYPE[*][10];   // [][10] 
typedef float DTYPE[0..10];   // Equivalent to [11] 
typedef float ETYPE[0..(MAX_INDEX)];  
 
typedef struct 
{ 
    unsigned short size; 
    unsigned short length; 
    [size_is(size), length_is(length)] char string[*]; 
} counted_string; 
 
HRESULT MyFunction( 
     [in, out] short * pSize,  
     [in, out, string, size_is(*pSize)] char a[0..*] 
);
```

<span data-ttu-id="12237-126">Дополнительные сведения см. в разделе [массивы и указатели](/windows/desktop/Rpc/arrays-and-pointers).</span><span class="sxs-lookup"><span data-stu-id="12237-126">For more information, see [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span>

## <a name="multidimensional-arrays"></a><span data-ttu-id="12237-127">Многомерные массивы</span><span class="sxs-lookup"><span data-stu-id="12237-127">Multidimensional Arrays</span></span>

<span data-ttu-id="12237-128">Пользователь может объявлять типы, которые являются массивами, а затем объявлять массивы объектов таких типов.</span><span class="sxs-lookup"><span data-stu-id="12237-128">The user can declare types that are arrays and then declare arrays of objects of such types.</span></span> <span data-ttu-id="12237-129">Семантика *объемных* массивов *n*-мерных массивов аналогична семантике  + *n многоуровневых* массивов.</span><span class="sxs-lookup"><span data-stu-id="12237-129">The semantics of *m*-dimensional arrays of *n*-dimensional array types are the same as the semantics of *m*+*n*-dimensional arrays.</span></span>

<span data-ttu-id="12237-130">Например, \_ тип Rect может быть определен как двухмерный массив, а переменная *Rect* может быть определена как массив \_ типа Rect.</span><span class="sxs-lookup"><span data-stu-id="12237-130">For example, the type RECT\_TYPE can be defined as a two-dimensional array and the variable *rect* can be defined as an array of RECT\_TYPE.</span></span> <span data-ttu-id="12237-131">Это эквивалентно трехмерному массиву, *эквивалентному \_ Rect*:</span><span class="sxs-lookup"><span data-stu-id="12237-131">This is equivalent to the three-dimensional array *equivalent\_rect*:</span></span>

``` syntax
typedef short int RECT_TYPE[10][20]; 
RECT_TYPE rect[15]; 
short int equivalent_rect[15][10][20];  // ~RECT_TYPE rect[15]
```

<span data-ttu-id="12237-132">Microsoft RPC ориентирован на C.</span><span class="sxs-lookup"><span data-stu-id="12237-132">Microsoft RPC is C oriented.</span></span> <span data-ttu-id="12237-133">В соответствии с соглашениями языка C, в среде выполнения можно определить только первое измерение многомерного массива.</span><span class="sxs-lookup"><span data-stu-id="12237-133">Following C-language conventions, only the first dimension of a multidimensional array can be determined at runtime.</span></span> <span data-ttu-id="12237-134">Взаимодействие с массивами IDL устройства DCE, которые поддерживают другие языки, ограничено:</span><span class="sxs-lookup"><span data-stu-id="12237-134">Interoperation with DCE IDL arrays that support other languages is limited to:</span></span>

-   <span data-ttu-id="12237-135">Многомерные массивы с константами (с определением времени компиляции).</span><span class="sxs-lookup"><span data-stu-id="12237-135">Multidimensional arrays with constant (compile-time-determined) bounds.</span></span>
-   <span data-ttu-id="12237-136">Многомерные массивы со всеми постоянными границами, за исключением первого измерения.</span><span class="sxs-lookup"><span data-stu-id="12237-136">Multidimensional arrays with all constant bounds except the first dimension.</span></span> <span data-ttu-id="12237-137">Верхняя граница и диапазон переданных элементов первого измерения зависят от среды выполнения.</span><span class="sxs-lookup"><span data-stu-id="12237-137">The upper bound and range of transmitted elements of the first dimension are dependent on runtime.</span></span>
-   <span data-ttu-id="12237-138">Любые одномерные массивы с нижней границей, равной нулю.</span><span class="sxs-lookup"><span data-stu-id="12237-138">Any one-dimensional arrays with a lower bound of zero.</span></span>

<span data-ttu-id="12237-139">Если **\[** [**строковый**](string.md) **\]** атрибут используется в многомерных массивах, атрибут применяется к крайнему правому массиву.</span><span class="sxs-lookup"><span data-stu-id="12237-139">When the **\[**[**string**](string.md)**\]** attribute is used on multidimensional arrays, the attribute applies to the rightmost array.</span></span>

## <a name="arrays-of-pointers"></a><span data-ttu-id="12237-140">Массивы указателей</span><span class="sxs-lookup"><span data-stu-id="12237-140">Arrays of Pointers</span></span>

<span data-ttu-id="12237-141">Ссылочные указатели должны указывать на допустимые данные.</span><span class="sxs-lookup"><span data-stu-id="12237-141">Reference pointers must point to valid data.</span></span> <span data-ttu-id="12237-142">Клиентское приложение должно выделить всю память для **\[** [**входного**](in.md) **\]** или **\[** [**выходного**](out-idl.md) **\]** массива ссылочных указателей, особенно если массив связан с **\[ в \]**, а также в значениях в, а **\[** **\]** также в, **\[** [**length \_**](length-is.md) **\]** или **\[** [**Last \_**](last-is.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="12237-142">The client application must allocate all memory for an **\[**[**in**](in.md)**\]** or **\[** **in,**[**out**](out-idl.md)**\]** array of reference pointers, especially when the array is associated with **\[in\]**, or **\[** **in,out\]**, **\[**[**length\_is**](length-is.md)**\]**, or **\[**[**last\_is**](last-is.md)**\]** values.</span></span> <span data-ttu-id="12237-143">Клиентское приложение также должно инициализировать все элементы массива перед вызовом.</span><span class="sxs-lookup"><span data-stu-id="12237-143">The client application must also initialize all array elements before the call.</span></span> <span data-ttu-id="12237-144">Перед возвратом клиенту серверное приложение должно убедиться, что все элементы массива в переданной точке диапазона находятся в допустимом хранилище.</span><span class="sxs-lookup"><span data-stu-id="12237-144">Before returning to the client, the server application must verify that all array elements in the transmitted range point to valid storage.</span></span>

<span data-ttu-id="12237-145">На стороне сервера заглушка выделяет хранилище для всех элементов массива независимо от **\[** [**длины \_ —**](length-is.md) **\]** или **\[** [**последнего \_**](last-is.md) **\]** значения во время вызова.</span><span class="sxs-lookup"><span data-stu-id="12237-145">On the server side, the stub allocates storage for all array elements, regardless of the **\[**[**length\_is**](length-is.md)**\]** or **\[**[**last\_is**](last-is.md)**\]** value at the time of the call.</span></span> <span data-ttu-id="12237-146">Эта функция может повлиять на производительность приложения.</span><span class="sxs-lookup"><span data-stu-id="12237-146">This feature can affect the performance of your application.</span></span>

<span data-ttu-id="12237-147">На массивы уникальных указателей не накладываются никакие ограничения.</span><span class="sxs-lookup"><span data-stu-id="12237-147">No restrictions are placed on arrays of unique pointers.</span></span> <span data-ttu-id="12237-148">Как на клиенте, так и на сервере хранилище выделяется для пустых указателей.</span><span class="sxs-lookup"><span data-stu-id="12237-148">On both the client and the server, storage is allocated for null pointers.</span></span> <span data-ttu-id="12237-149">Если указатели не равны NULL, данные помещаются в предварительно выделенное хранилище.</span><span class="sxs-lookup"><span data-stu-id="12237-149">When pointers are non-null, data is placed in preallocated storage.</span></span>

<span data-ttu-id="12237-150">Необязательный декларатор указателя может предшествовать декларатору массива.</span><span class="sxs-lookup"><span data-stu-id="12237-150">An optional pointer declarator can precede the array declarator.</span></span>

<span data-ttu-id="12237-151">Если внедренные ссылочные указатели являются **\[** [](out-idl.md) **\]** параметрами только для использования, код Server Manager должен присвоить допустимые значения массиву ссылочных указателей.</span><span class="sxs-lookup"><span data-stu-id="12237-151">When embedded reference pointers are **\[**[**out**](out-idl.md)**\]**-only parameters, the server-manager code must assign valid values to the array of reference pointers.</span></span> <span data-ttu-id="12237-152">Пример:</span><span class="sxs-lookup"><span data-stu-id="12237-152">For example:</span></span>

``` syntax
typedef [ref] short * ARefPointer;
typedef ARefPointer ArrayOfRef[10];
HRESULT proc1( [out] ArrayOfRef Parameter );
```

<span data-ttu-id="12237-153">Созданные заглушки распределяют массив и присваивают значения NULL всем указателям, внедренным в массив.</span><span class="sxs-lookup"><span data-stu-id="12237-153">The generated stubs allocate the array and assign null values to all pointers embedded in the array.</span></span>

 

 