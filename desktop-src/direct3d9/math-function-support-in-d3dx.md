---
description: Сведения о поддержке математических функций в D3DX. D3DX — это служебная Библиотека, которая предоставляет вспомогательные службы. Это уровень выше компонента Direct3D.
ms.assetid: a44d25de-f79d-4132-a75a-0c22ccd84341
title: Поддержка математических функций в D3DX (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a28c32b13d185694e4ffa41c314cf9f77cbb18b7
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407527"
---
# <a name="math-function-support-in-d3dx-direct3d-9"></a><span data-ttu-id="a62bd-105">Поддержка математических функций в D3DX (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="a62bd-105">Math Function Support in D3DX (Direct3D 9)</span></span>

<span data-ttu-id="a62bd-106">D3DX — это служебная Библиотека, которая предоставляет вспомогательные службы.</span><span class="sxs-lookup"><span data-stu-id="a62bd-106">D3DX is a utility library that provides helper services.</span></span> <span data-ttu-id="a62bd-107">Это уровень выше компонента Direct3D.</span><span class="sxs-lookup"><span data-stu-id="a62bd-107">It is a layer above the Direct3D component.</span></span>

## <a name="math"></a><span data-ttu-id="a62bd-108">Математический</span><span class="sxs-lookup"><span data-stu-id="a62bd-108">Math</span></span>

<span data-ttu-id="a62bd-109">Математические функции, содержащиеся в наборе функций, предоставляются для:</span><span class="sxs-lookup"><span data-stu-id="a62bd-109">Math support, contained in a set of functions, is provided for:</span></span>

-   <span data-ttu-id="a62bd-110">Вычисления цветов</span><span class="sxs-lookup"><span data-stu-id="a62bd-110">Color calculations</span></span>
-   <span data-ttu-id="a62bd-111">Плоскост</span><span class="sxs-lookup"><span data-stu-id="a62bd-111">Planes</span></span>
-   <span data-ttu-id="a62bd-112">Обработка матриц</span><span class="sxs-lookup"><span data-stu-id="a62bd-112">Matrix manipulation</span></span>
-   <span data-ttu-id="a62bd-113">Кватернионы</span><span class="sxs-lookup"><span data-stu-id="a62bd-113">Quaternions</span></span>
-   <span data-ttu-id="a62bd-114">Двумерные векторы</span><span class="sxs-lookup"><span data-stu-id="a62bd-114">2D vectors</span></span>
-   <span data-ttu-id="a62bd-115">Трехмерные векторы</span><span class="sxs-lookup"><span data-stu-id="a62bd-115">3D vectors</span></span>
-   <span data-ttu-id="a62bd-116">векторы 4D</span><span class="sxs-lookup"><span data-stu-id="a62bd-116">4D vectors</span></span>

<span data-ttu-id="a62bd-117">Обратите внимание, что при сочетании с перегрузками C++ поддержка базовых трехмерных математических типов является обширной.</span><span class="sxs-lookup"><span data-stu-id="a62bd-117">Please note that when coupled with the C++ overloads, the support for basic 3D math types is extensive.</span></span>

<span data-ttu-id="a62bd-118">Дополнительные сведения об этих функциях см. в разделе [функции D3DX](dx9-graphics-reference-d3dx-functions.md).</span><span class="sxs-lookup"><span data-stu-id="a62bd-118">For more information about these functions, see [D3DX Functions](dx9-graphics-reference-d3dx-functions.md).</span></span> <span data-ttu-id="a62bd-119">Чтобы найти необходимую функцию, они разбиваются на несколько папок.</span><span class="sxs-lookup"><span data-stu-id="a62bd-119">To help find the function you need, they are broken up in several folders.</span></span>

## <a name="float16"></a><span data-ttu-id="a62bd-120">FLOAT16</span><span class="sxs-lookup"><span data-stu-id="a62bd-120">FLOAT16</span></span>

<span data-ttu-id="a62bd-121">При использовании типа данных FLOAT16 не забудьте ограничить значения максимальным значением D3DX \_ 16F \_ Max.</span><span class="sxs-lookup"><span data-stu-id="a62bd-121">When using the FLOAT16 data type, be sure to limit values to a maximum of D3DX\_16F\_MAX.</span></span> <span data-ttu-id="a62bd-122">Любое значение FLOAT16, превышающее это, приведет к неопределенному поведению в конвейере.</span><span class="sxs-lookup"><span data-stu-id="a62bd-122">Any FLOAT16 value that exceeds this will result in undefined behavior in the pipeline.</span></span> <span data-ttu-id="a62bd-123">См. [другие константы D3DX](other-d3dx-constants.md).</span><span class="sxs-lookup"><span data-stu-id="a62bd-123">See [Other D3DX Constants](other-d3dx-constants.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a62bd-124">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="a62bd-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a62bd-125">D3DX</span><span class="sxs-lookup"><span data-stu-id="a62bd-125">D3DX</span></span>](d3dx.md)
</dt> </dl>

 

 



