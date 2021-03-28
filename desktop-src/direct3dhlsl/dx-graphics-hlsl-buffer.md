---
title: Тип буфера
description: Чтобы объявить переменную буфера, используйте следующий синтаксис.
ms.assetid: f21f0de5-58e3-466b-97bb-e4e7efa9cc1c
keywords:
- Тип буфера HLSL
topic_type:
- apiref
api_name:
- Buffer Type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e36030f3dd31f1bdada238e89c1048e4971cd45c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070204"
---
# <a name="buffer-type"></a><span data-ttu-id="d1d81-104">Тип буфера</span><span class="sxs-lookup"><span data-stu-id="d1d81-104">Buffer Type</span></span>

<span data-ttu-id="d1d81-105">Чтобы объявить переменную буфера, используйте следующий синтаксис.</span><span class="sxs-lookup"><span data-stu-id="d1d81-105">Use the following syntax to declare a buffer variable.</span></span>



| <span data-ttu-id="d1d81-106">Buffer< >  *имя* типа;</span><span class="sxs-lookup"><span data-stu-id="d1d81-106">Buffer<*Type*> *Name*;</span></span> |
|------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="d1d81-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="d1d81-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1d81-108"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>**Двойной**</span><span class="sxs-lookup"><span data-stu-id="d1d81-108"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>**Buffer**</span></span>
</dt> <dd>

<span data-ttu-id="d1d81-109">Обязательное ключевое слово.</span><span class="sxs-lookup"><span data-stu-id="d1d81-109">Required keyword.</span></span>

</dd> <dt>

<span data-ttu-id="d1d81-110"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>*Тип*</span><span class="sxs-lookup"><span data-stu-id="d1d81-110"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>*Type*</span></span>
</dt> <dd>

<span data-ttu-id="d1d81-111">Один из типов [скалярных](dx-graphics-hlsl-scalar.md), [векторных](dx-graphics-hlsl-vector.md)и некоторых [матричных](dx-graphics-hlsl-matrix.md) HLSL.</span><span class="sxs-lookup"><span data-stu-id="d1d81-111">One of the [scalar](dx-graphics-hlsl-scalar.md), [vector](dx-graphics-hlsl-vector.md), and some [matrix](dx-graphics-hlsl-matrix.md) HLSL types.</span></span> <span data-ttu-id="d1d81-112">Можно объявить переменную буфера с матрицей, если она умещается в 4 32-разрядном количестве.</span><span class="sxs-lookup"><span data-stu-id="d1d81-112">You can declare a buffer variable with a matrix as long as it fits in 4 32-bit quantities.</span></span> <span data-ttu-id="d1d81-113">Итак, можно написать `Buffer<float2x2>` .</span><span class="sxs-lookup"><span data-stu-id="d1d81-113">So, you can write `Buffer<float2x2>`.</span></span> <span data-ttu-id="d1d81-114">Но `Buffer<float4x4>` слишком большой, и компилятор выдаст ошибку.</span><span class="sxs-lookup"><span data-stu-id="d1d81-114">But `Buffer<float4x4>` is too large, and the compiler will generate an error.</span></span>

</dd> <dt>

<span data-ttu-id="d1d81-115"><span id="Name"></span><span id="name"></span><span id="NAME"></span>*Безымян*</span><span class="sxs-lookup"><span data-stu-id="d1d81-115"><span id="Name"></span><span id="name"></span><span id="NAME"></span>*Name*</span></span>
</dt> <dd>

<span data-ttu-id="d1d81-116">Строка ASCII, однозначно определяющая имя переменной.</span><span class="sxs-lookup"><span data-stu-id="d1d81-116">An ASCII string that uniquely identifies the variable name.</span></span>

</dd> </dl>

## <a name="example"></a><span data-ttu-id="d1d81-117">Например, .</span><span class="sxs-lookup"><span data-stu-id="d1d81-117">Example</span></span>

<span data-ttu-id="d1d81-118">Ниже приведен пример объявления буфера из файла Пипесгс. FX в [примере пипесгс](https://msdn.microsoft.com/library/Ee416423(v=VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="d1d81-118">Here is an example of a buffer declaration from the PipesGS.fx file in [PipesGS Sample](https://msdn.microsoft.com/library/Ee416423(v=VS.85).aspx).</span></span>


```
Buffer<float4> g_Buffer;
```



<span data-ttu-id="d1d81-119">Данные считываются из буфера с помощью перегруженной версии встроенной функции [**Load**](dx-graphics-hlsl-to-load.md) HLSL, которая принимает один входной параметр (целочисленный индекс).</span><span class="sxs-lookup"><span data-stu-id="d1d81-119">Data is read from a buffer using an overloaded version of the [**Load**](dx-graphics-hlsl-to-load.md) HLSL intrinsic function that takes one input parameter (an integer index).</span></span> <span data-ttu-id="d1d81-120">Доступ к буферу осуществляется как к массиву элементов. Поэтому в этом примере считывается второй элемент.</span><span class="sxs-lookup"><span data-stu-id="d1d81-120">A buffer is accessed like an array of elements; therefore, this example reads the second element.</span></span>


```
float4 bufferData = g_Buffer.Load( 1 );
```



<span data-ttu-id="d1d81-121">Используйте [этап потокового вывода](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-output-stream-stage) для вывода данных в буфер.</span><span class="sxs-lookup"><span data-stu-id="d1d81-121">Use the [stream-output stage](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-output-stream-stage) to output data to a buffer.</span></span>

## <a name="see-also"></a><span data-ttu-id="d1d81-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d1d81-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1d81-123">Типы данных (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d1d81-123">Data Types (DirectX HLSL)</span></span>](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 

 