---
description: Вычисление значений параметров
ms.assetid: cc3c26ed-a007-4350-99be-0ebd94953689
title: Вычисление значений параметров
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89dac0767d7d19bc4331e1a9ee032ec5b3eaae2e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105655589"
---
# <a name="calculating-parameter-values"></a><span data-ttu-id="531d1-103">Вычисление значений параметров</span><span class="sxs-lookup"><span data-stu-id="531d1-103">Calculating Parameter Values</span></span>

<span data-ttu-id="531d1-104">Возможно, входной буфер может быть очень большим.</span><span class="sxs-lookup"><span data-stu-id="531d1-104">Potentially, an input buffer could be very large.</span></span> <span data-ttu-id="531d1-105">В идеале, когда объект DMO обрабатывает буфер, параметры будут точно соответствовать их кривым по всему пакету данных.</span><span class="sxs-lookup"><span data-stu-id="531d1-105">Ideally, when the DMO processes the buffer, the parameters will exactly follow their curves throughout the entire batch of data.</span></span> <span data-ttu-id="531d1-106">Однако у DMO есть некоторые отклонения в том, как он вычисляет эти значения.</span><span class="sxs-lookup"><span data-stu-id="531d1-106">However, a DMO has some leeway in how it calculates those values.</span></span>

-   <span data-ttu-id="531d1-107">Наиболее точный подход заключается в вычислении точного значения для каждой атомарной единицы данных. Например, каждый звуковой образец.</span><span class="sxs-lookup"><span data-stu-id="531d1-107">The most accurate approach is to calculate the exact value for every atomic unit of data; for example, each audio sample.</span></span> <span data-ttu-id="531d1-108">Этот подход является наиболее ресурсоемким.</span><span class="sxs-lookup"><span data-stu-id="531d1-108">This approach is the most computationally expensive.</span></span>
-   <span data-ttu-id="531d1-109">Другой подход состоит в том, чтобы разделить данные на более мелкие единицы фиксированного размера, например 100.</span><span class="sxs-lookup"><span data-stu-id="531d1-109">Another approach is to slice the data into smaller units of some fixed size, such as 100 samples.</span></span> <span data-ttu-id="531d1-110">При таком подходе создается «лестничное пошаговое выполнение».</span><span class="sxs-lookup"><span data-stu-id="531d1-110">This approach creates a "stair-stepping" effect.</span></span> <span data-ttu-id="531d1-111">Для некоторых параметров это может быть приемлемым.</span><span class="sxs-lookup"><span data-stu-id="531d1-111">For some parameters, that might be acceptable.</span></span> <span data-ttu-id="531d1-112">В звуковых эффектах он может создавать звуковые артефакты.</span><span class="sxs-lookup"><span data-stu-id="531d1-112">In audio effects, it might create audible artifacts.</span></span>
-   <span data-ttu-id="531d1-113">Компромисс заключается в использовании предыдущей методики, но в каждом пакете выполняет линейную интерполяцию значения параметра для каждого образца.</span><span class="sxs-lookup"><span data-stu-id="531d1-113">A compromise is to use the previous technique, but within each batch, perform a linear interpolation of the parameter value for each sample.</span></span>

<span data-ttu-id="531d1-114">Эти проблемы особенно важны для обработки звука.</span><span class="sxs-lookup"><span data-stu-id="531d1-114">These issues are especially important for audio processing.</span></span> <span data-ttu-id="531d1-115">Одна секунда звука может содержать 48 000 звуковых выборок на канал, что является большим количеством вычислений, но с учетом таких артефактов, как присвоение псевдонимов.</span><span class="sxs-lookup"><span data-stu-id="531d1-115">One second of audio might contain 48,000 audio samples per channel, which is a lot of calculations to perform, yet the ear is sensitive to artifacts such as aliasing.</span></span>

## <a name="related-topics"></a><span data-ttu-id="531d1-116">См. также</span><span class="sxs-lookup"><span data-stu-id="531d1-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="531d1-117">Параметры носителя</span><span class="sxs-lookup"><span data-stu-id="531d1-117">Media Parameters</span></span>](media-parameters.md)
</dt> </dl>

 

 



