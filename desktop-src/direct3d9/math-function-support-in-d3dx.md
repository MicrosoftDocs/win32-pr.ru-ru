---
description: D3DX — это служебная Библиотека, которая предоставляет вспомогательные службы. Это уровень выше компонента Direct3D.
ms.assetid: a44d25de-f79d-4132-a75a-0c22ccd84341
title: Поддержка математических функций в D3DX (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac69e0385919b015d1f8d3e7d47e221c06a04fbb
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104139970"
---
# <a name="math-function-support-in-d3dx-direct3d-9"></a><span data-ttu-id="806ec-104">Поддержка математических функций в D3DX (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="806ec-104">Math Function Support in D3DX (Direct3D 9)</span></span>

<span data-ttu-id="806ec-105">D3DX — это служебная Библиотека, которая предоставляет вспомогательные службы.</span><span class="sxs-lookup"><span data-stu-id="806ec-105">D3DX is a utility library that provides helper services.</span></span> <span data-ttu-id="806ec-106">Это уровень выше компонента Direct3D.</span><span class="sxs-lookup"><span data-stu-id="806ec-106">It is a layer above the Direct3D component.</span></span>

## <a name="math"></a><span data-ttu-id="806ec-107">Математический</span><span class="sxs-lookup"><span data-stu-id="806ec-107">Math</span></span>

<span data-ttu-id="806ec-108">Математические функции, содержащиеся в наборе функций, предоставляются для:</span><span class="sxs-lookup"><span data-stu-id="806ec-108">Math support, contained in a set of functions, is provided for:</span></span>

-   <span data-ttu-id="806ec-109">Вычисления цветов</span><span class="sxs-lookup"><span data-stu-id="806ec-109">Color calculations</span></span>
-   <span data-ttu-id="806ec-110">Плоскост</span><span class="sxs-lookup"><span data-stu-id="806ec-110">Planes</span></span>
-   <span data-ttu-id="806ec-111">Обработка матриц</span><span class="sxs-lookup"><span data-stu-id="806ec-111">Matrix manipulation</span></span>
-   <span data-ttu-id="806ec-112">Кватернионы</span><span class="sxs-lookup"><span data-stu-id="806ec-112">Quaternions</span></span>
-   <span data-ttu-id="806ec-113">Двумерные векторы</span><span class="sxs-lookup"><span data-stu-id="806ec-113">2D vectors</span></span>
-   <span data-ttu-id="806ec-114">Трехмерные векторы</span><span class="sxs-lookup"><span data-stu-id="806ec-114">3D vectors</span></span>
-   <span data-ttu-id="806ec-115">векторы 4D</span><span class="sxs-lookup"><span data-stu-id="806ec-115">4D vectors</span></span>

<span data-ttu-id="806ec-116">Обратите внимание, что при сочетании с перегрузками C++ поддержка базовых трехмерных математических типов является обширной.</span><span class="sxs-lookup"><span data-stu-id="806ec-116">Please note that when coupled with the C++ overloads, the support for basic 3D math types is extensive.</span></span>

<span data-ttu-id="806ec-117">Дополнительные сведения об этих функциях см. в разделе [функции D3DX](dx9-graphics-reference-d3dx-functions.md).</span><span class="sxs-lookup"><span data-stu-id="806ec-117">For more information about these functions, see [D3DX Functions](dx9-graphics-reference-d3dx-functions.md).</span></span> <span data-ttu-id="806ec-118">Чтобы найти необходимую функцию, они разбиваются на несколько папок.</span><span class="sxs-lookup"><span data-stu-id="806ec-118">To help find the function you need, they are broken up in several folders.</span></span>

## <a name="float16"></a><span data-ttu-id="806ec-119">FLOAT16</span><span class="sxs-lookup"><span data-stu-id="806ec-119">FLOAT16</span></span>

<span data-ttu-id="806ec-120">При использовании типа данных FLOAT16 не забудьте ограничить значения максимальным значением D3DX \_ 16F \_ Max.</span><span class="sxs-lookup"><span data-stu-id="806ec-120">When using the FLOAT16 data type, be sure to limit values to a maximum of D3DX\_16F\_MAX.</span></span> <span data-ttu-id="806ec-121">Любое значение FLOAT16, превышающее это, приведет к неопределенному поведению в конвейере.</span><span class="sxs-lookup"><span data-stu-id="806ec-121">Any FLOAT16 value that exceeds this will result in undefined behavior in the pipeline.</span></span> <span data-ttu-id="806ec-122">См. [другие константы D3DX](other-d3dx-constants.md).</span><span class="sxs-lookup"><span data-stu-id="806ec-122">See [Other D3DX Constants](other-d3dx-constants.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="806ec-123">См. также</span><span class="sxs-lookup"><span data-stu-id="806ec-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="806ec-124">D3DX</span><span class="sxs-lookup"><span data-stu-id="806ec-124">D3DX</span></span>](d3dx.md)
</dt> </dl>

 

 



