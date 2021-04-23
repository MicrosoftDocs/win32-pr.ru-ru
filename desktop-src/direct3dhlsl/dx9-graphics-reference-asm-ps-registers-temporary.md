---
title: Временный регистр (Справочник по HLSL PS)
description: Временные регистры входных построителей текстуры используются для хранения промежуточных результатов.
ms.assetid: e61daaa1-0a9b-4b1c-b91c-56573be59ed9
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7aebee99a693ac629d9cc8a372fba7589a9e29ef
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/23/2019
ms.locfileid: "103890064"
---
# <a name="temporary-register-hlsl-ps-reference"></a><span data-ttu-id="c6eba-103">Временный регистр (Справочник по HLSL PS)</span><span class="sxs-lookup"><span data-stu-id="c6eba-103">Temporary register (HLSL PS reference)</span></span>

<span data-ttu-id="c6eba-104">Временные регистры входных построителей текстуры используются для хранения промежуточных результатов.</span><span class="sxs-lookup"><span data-stu-id="c6eba-104">Pixel shader input temporary registers are used to hold intermediate results.</span></span>

<span data-ttu-id="c6eba-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c6eba-105">Syntax</span></span>


```
no declaration is required
```





| <span data-ttu-id="c6eba-106">Версии шейдеров пикселей</span><span class="sxs-lookup"><span data-stu-id="c6eba-106">Pixel shader versions</span></span> | <span data-ttu-id="c6eba-107">1\_1</span><span class="sxs-lookup"><span data-stu-id="c6eba-107">1\_1</span></span> | <span data-ttu-id="c6eba-108">1\_2</span><span class="sxs-lookup"><span data-stu-id="c6eba-108">1\_2</span></span> | <span data-ttu-id="c6eba-109">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="c6eba-109">1\_3</span></span> | <span data-ttu-id="c6eba-110">1\_4</span><span class="sxs-lookup"><span data-stu-id="c6eba-110">1\_4</span></span> | <span data-ttu-id="c6eba-111">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c6eba-111">2\_0</span></span> | <span data-ttu-id="c6eba-112">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="c6eba-112">2\_sw</span></span> | <span data-ttu-id="c6eba-113">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="c6eba-113">2\_x</span></span> | <span data-ttu-id="c6eba-114">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c6eba-114">3\_0</span></span> | <span data-ttu-id="c6eba-115">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="c6eba-115">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|-------|------|------|-------|
| <span data-ttu-id="c6eba-116">Временный регистр</span><span class="sxs-lookup"><span data-stu-id="c6eba-116">Temporary Register</span></span>    |      |      |      |      | <span data-ttu-id="c6eba-117">x</span><span class="sxs-lookup"><span data-stu-id="c6eba-117">x</span></span>    | <span data-ttu-id="c6eba-118">x</span><span class="sxs-lookup"><span data-stu-id="c6eba-118">x</span></span>     | <span data-ttu-id="c6eba-119">x</span><span class="sxs-lookup"><span data-stu-id="c6eba-119">x</span></span>    | <span data-ttu-id="c6eba-120">x</span><span class="sxs-lookup"><span data-stu-id="c6eba-120">x</span></span>    | <span data-ttu-id="c6eba-121">x</span><span class="sxs-lookup"><span data-stu-id="c6eba-121">x</span></span>     |



 

-   <span data-ttu-id="c6eba-122">Существует 12 временных регистров построителя текстуры: r0 в R11.</span><span class="sxs-lookup"><span data-stu-id="c6eba-122">There are 12 pixel-shader temporary registers: r0 to r11.</span></span>
-   <span data-ttu-id="c6eba-123">Эти регистры используются для хранения промежуточных результатов во время вычислений.</span><span class="sxs-lookup"><span data-stu-id="c6eba-123">These registers are used for storing intermediate results during computations.</span></span>
-   <span data-ttu-id="c6eba-124">Если временный регистр использует компоненты, которые не определены в предыдущем коде, проверка шейдера завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="c6eba-124">If a temporary register uses components that are not defined in previous code, shader validation will fail.</span></span>
-   <span data-ttu-id="c6eba-125">По меньшей мере точность с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="c6eba-125">These are at least floating-point precision.</span></span>
-   <span data-ttu-id="c6eba-126">В одной инструкции можно использовать не более трех.</span><span class="sxs-lookup"><span data-stu-id="c6eba-126">A maximum of three can be used in a single instruction.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c6eba-127">См. также</span><span class="sxs-lookup"><span data-stu-id="c6eba-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c6eba-128">Регистры</span><span class="sxs-lookup"><span data-stu-id="c6eba-128">Registers</span></span>](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 




