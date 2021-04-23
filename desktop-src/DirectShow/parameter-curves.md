---
description: Кривые параметров
ms.assetid: c073e7d0-c119-4c36-a5b2-b31dd6326ac8
title: Кривые параметров
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc3c482112c8bd76217f5cbdabdf3cda13b09c3e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104140330"
---
# <a name="parameter-curves"></a><span data-ttu-id="5913f-103">Кривые параметров</span><span class="sxs-lookup"><span data-stu-id="5913f-103">Parameter Curves</span></span>

<span data-ttu-id="5913f-104">Параметры мультимедиа могут следовать кривой с течением времени.</span><span class="sxs-lookup"><span data-stu-id="5913f-104">Media parameters are able to follow a curve over time.</span></span> <span data-ttu-id="5913f-105">Каждая кривая описывается математической формулой и двумя конечными точками.</span><span class="sxs-lookup"><span data-stu-id="5913f-105">Each curve is described by a mathematical formula and two end-points.</span></span> <span data-ttu-id="5913f-106">Каждая конечная точка определяется временем ссылки и значением кривой в это время.</span><span class="sxs-lookup"><span data-stu-id="5913f-106">Each end-point is defined by a reference time and the value of the curve at that time.</span></span> <span data-ttu-id="5913f-107">Формула используется для вычисления промежуточных значений между точками и определяет форму кривой.</span><span class="sxs-lookup"><span data-stu-id="5913f-107">The formula is used to calculate intermediate values between the points, and determines the shape of the curve.</span></span> <span data-ttu-id="5913f-108">Возможные кривые:</span><span class="sxs-lookup"><span data-stu-id="5913f-108">The possible curves are:</span></span>

-   <span data-ttu-id="5913f-109">Перехода</span><span class="sxs-lookup"><span data-stu-id="5913f-109">Jump</span></span>
-   <span data-ttu-id="5913f-110">Линейная</span><span class="sxs-lookup"><span data-stu-id="5913f-110">Linear</span></span>
-   <span data-ttu-id="5913f-111">Square</span><span class="sxs-lookup"><span data-stu-id="5913f-111">Square</span></span>
-   <span data-ttu-id="5913f-112">Обратный квадрат</span><span class="sxs-lookup"><span data-stu-id="5913f-112">Inverse square</span></span>
-   <span data-ttu-id="5913f-113">Равен</span><span class="sxs-lookup"><span data-stu-id="5913f-113">Sine</span></span>

<span data-ttu-id="5913f-114">"Переход" означает переход непосредственно к конечному значению.</span><span class="sxs-lookup"><span data-stu-id="5913f-114">"Jump" means jump directly to the end value.</span></span> <span data-ttu-id="5913f-115">Другие кривые показаны на следующей схеме.</span><span class="sxs-lookup"><span data-stu-id="5913f-115">The other curves are shown in the following diagram.</span></span>

![кривые параметров](images/param-curves01.png)

<span data-ttu-id="5913f-117">Математические кривые работают следующим образом.</span><span class="sxs-lookup"><span data-stu-id="5913f-117">Mathematically, the curves work as follows.</span></span> <span data-ttu-id="5913f-118">Предположим, что кривая начинается со времени *t*₀ со значением *v*₀ и заканчивается в момент времени *t*₁ со значением *v*₁.</span><span class="sxs-lookup"><span data-stu-id="5913f-118">Suppose that a curve begins at time *t*₀ with a value of *v*₀, and ends at time *t*₁ with a value of *v*₁.</span></span> <span data-ttu-id="5913f-119">Две точки, определяющие кривую, — (*t*₀, *v*₀) и (*t*₁, *v*₁).</span><span class="sxs-lookup"><span data-stu-id="5913f-119">The two points that define the curve are (*t*₀, *v*₀) and (*t*₁, *v*₁).</span></span>

-   <span data-ttu-id="5913f-120">Пусть Δ *t* является общей длительностью кривой, *t*₁ –*t*₀.</span><span class="sxs-lookup"><span data-stu-id="5913f-120">Let Δ *t* be the total duration of the curve, *t*₁–*t*₀.</span></span>
-   <span data-ttu-id="5913f-121">Пусть Δ *v* является интервалом между начальным и конечным значениями, *v*₁ –*v*₀.</span><span class="sxs-lookup"><span data-stu-id="5913f-121">Let Δ *v* be the interval between the starting and ending values, *v*₁–*v*₀.</span></span>
-   <span data-ttu-id="5913f-122">В любой момент *t* таким, что *t*₀ <= *t*  <=  *t*₁, Let δ *t*"= *t*–*t*₀.</span><span class="sxs-lookup"><span data-stu-id="5913f-122">At any time *t* such that *t*₀ <= *t* <= *t*₁, let Δ *t*' = *t*–*t*₀.</span></span>

![Вычисление параметров](images/param-curves02.png)

<span data-ttu-id="5913f-124">Значение параметра в момент времени *t* равно:</span><span class="sxs-lookup"><span data-stu-id="5913f-124">The value of the parameter at time *t* is:</span></span>

<span data-ttu-id="5913f-125">*v* = f (δ *t*'/δ *t* ) \* δ *v*  +  *v*₀</span><span class="sxs-lookup"><span data-stu-id="5913f-125">*v* = f( Δ *t*' / Δ *t* ) \* Δ *v* + *v*₀</span></span>

<span data-ttu-id="5913f-126">где f (x) — функция, определяемая типом кривой:</span><span class="sxs-lookup"><span data-stu-id="5913f-126">where f(x) is a function determined by the curve type:</span></span>

-   <span data-ttu-id="5913f-127">Линейный: y = x</span><span class="sxs-lookup"><span data-stu-id="5913f-127">Linear: y = x</span></span>
-   <span data-ttu-id="5913f-128">Квадратный: y = x ^ 2</span><span class="sxs-lookup"><span data-stu-id="5913f-128">Square: y = x^2</span></span>
-   <span data-ttu-id="5913f-129">Обратный квадрат: y = Sqrt (x)</span><span class="sxs-lookup"><span data-stu-id="5913f-129">Inverse square: y = sqrt(x)</span></span>
-   <span data-ttu-id="5913f-130">Синус: y = \[ sin (πкс – π/2) + 1 \] /2</span><span class="sxs-lookup"><span data-stu-id="5913f-130">Sine: y = \[ sin(πx – π/2) + 1 \] / 2</span></span>

<span data-ttu-id="5913f-131">Обратите внимание, что Δ *t*' < δ *t*, поэтому термин δ *t*'/δ *t* находится в диапазоне от 0 до 1.</span><span class="sxs-lookup"><span data-stu-id="5913f-131">Observe that Δ *t*' < Δ *t*, so the term Δ *t*'/Δ *t* ranges from 0 to 1.</span></span> <span data-ttu-id="5913f-132">Таким образом, f (x) также находится в диапазоне от 0 до 1, а *v* всегда находится между *v*₀ и *v*₁.</span><span class="sxs-lookup"><span data-stu-id="5913f-132">Therefore, f(x) also ranges from 0 to 1, and *v* always falls between *v*₀ and *v*₁.</span></span> <span data-ttu-id="5913f-133">Это верно, когда *v*₀ < *v*₁ или наоборот.</span><span class="sxs-lookup"><span data-stu-id="5913f-133">This is true whether *v*₀ < *v*₁ or vice versa.</span></span> <span data-ttu-id="5913f-134">Иными словами, кривая ограничена прямоугольником (*t*₀, *v*₀, *t*₁, *v*₁).</span><span class="sxs-lookup"><span data-stu-id="5913f-134">In other words, the curve is bounded by the rectangle (*t*₀, *v*₀, *t*₁, *v*₁).</span></span>

<span data-ttu-id="5913f-135">Для синусной кривой значение (πкс – π/2) лежит в диапазоне от – π/2 до π/2, что означает, что Sin (πкс – π/2) находится в диапазоне от – 1 до 1.</span><span class="sxs-lookup"><span data-stu-id="5913f-135">For the sine curve, the value of (πx – π/2) ranges from –π/2 to π/2, which means that sin(πx – π/2) ranges from –1 to 1.</span></span> <span data-ttu-id="5913f-136">Затем результат нормализуется таким образом, что f (x) попадает в диапазон (0 – 1).</span><span class="sxs-lookup"><span data-stu-id="5913f-136">The result is then normalized so that f(x) falls into the range (0–1).</span></span>

## <a name="related-topics"></a><span data-ttu-id="5913f-137">См. также</span><span class="sxs-lookup"><span data-stu-id="5913f-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5913f-138">Параметры носителя</span><span class="sxs-lookup"><span data-stu-id="5913f-138">Media Parameters</span></span>](media-parameters.md)
</dt> </dl>

 

 



