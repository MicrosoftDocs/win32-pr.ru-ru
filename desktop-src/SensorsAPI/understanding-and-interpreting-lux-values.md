---
description: Основной тип данных датчика для внешних датчиков окружающей среды — иллуминанце в Lux (люменов за квадратный метр). Принципы, описанные в этом разделе, основаны на получении значений Lux в качестве входных данных и реагировании на эти данные в программе.
ms.assetid: 29855779-7c27-4cfe-b8af-b33bc86a1f62
title: Основные сведения и интерпретация значений Lux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8012f983eeac29cc07b18ac2d27918d2df6ed52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081126"
---
# <a name="understanding-and-interpreting-lux-values"></a><span data-ttu-id="58fae-104">Основные сведения и интерпретация значений Lux</span><span class="sxs-lookup"><span data-stu-id="58fae-104">Understanding and Interpreting Lux Values</span></span>

<span data-ttu-id="58fae-105">Основной тип данных датчика для внешних датчиков окружающей среды — иллуминанце в Lux (люменов за квадратный метр).</span><span class="sxs-lookup"><span data-stu-id="58fae-105">The primary sensor data type for ambient light sensors is illuminance in lux (lumens per square meter).</span></span> <span data-ttu-id="58fae-106">Принципы, описанные в этом разделе, основаны на получении значений Lux в качестве входных данных и реагировании на эти данные в программе.</span><span class="sxs-lookup"><span data-stu-id="58fae-106">The principles outlined in this topic are based on taking lux values as input and reacting to that data in a program.</span></span>

<span data-ttu-id="58fae-107">Чтение Lux прямо пропорционально энергии на квадратный метр, который будет израсходован в секунду.</span><span class="sxs-lookup"><span data-stu-id="58fae-107">Lux readings are directly proportional to the energy per square meter that is absorbed per second.</span></span> <span data-ttu-id="58fae-108">Человеческие восприятие легких уровней не настолько просто.</span><span class="sxs-lookup"><span data-stu-id="58fae-108">Human perception of light levels is not so straightforward.</span></span> <span data-ttu-id="58fae-109">Человеческий глаз довольно сложен, так как наши глаза постоянно настраиваются и другие биологических процессы влияют на наше восприятие.</span><span class="sxs-lookup"><span data-stu-id="58fae-109">Human perception of light is complicated because our eyes are constantly adjusting and other biological processes are affecting our perception.</span></span> <span data-ttu-id="58fae-110">Однако мы можем подумать об этом восприятии с упрощенной точки зрения, создавая несколько интересующих диапазонов с известными верхними и нижними пороговыми значениями.</span><span class="sxs-lookup"><span data-stu-id="58fae-110">However, we can think of this perception from a simplified perspective by creating several ranges of interest with known upper and lower thresholds.</span></span>

<span data-ttu-id="58fae-111">В следующем примере набор данных представляет приблизительные пороговые значения для распространенных условий освещения и соответствующий шаг освещения.</span><span class="sxs-lookup"><span data-stu-id="58fae-111">The following example data set represents rough thresholds for common lighting conditions, and the corresponding lighting step.</span></span> <span data-ttu-id="58fae-112">Здесь каждый этап освещения представляет изменение в среде освещения.</span><span class="sxs-lookup"><span data-stu-id="58fae-112">Here, each lighting step represents a change in lighting environment.</span></span>

> [!Note]  
> <span data-ttu-id="58fae-113">Этот набор данных предназначен для иллюстрации и может быть неполным точным для всех пользователей или ситуаций.</span><span class="sxs-lookup"><span data-stu-id="58fae-113">This data set is for illustration and may not be completely accurate for all users or situations.</span></span>

 



| <span data-ttu-id="58fae-114">Условие освещения</span><span class="sxs-lookup"><span data-stu-id="58fae-114">Lighting condition</span></span> | <span data-ttu-id="58fae-115">Из (LUX)</span><span class="sxs-lookup"><span data-stu-id="58fae-115">From (lux)</span></span> | <span data-ttu-id="58fae-116">To (LUX)</span><span class="sxs-lookup"><span data-stu-id="58fae-116">To (lux)</span></span> | <span data-ttu-id="58fae-117">Среднее значение (LUX)</span><span class="sxs-lookup"><span data-stu-id="58fae-117">Mean value (lux)</span></span> | <span data-ttu-id="58fae-118">Шаг освещения</span><span class="sxs-lookup"><span data-stu-id="58fae-118">Lighting step</span></span> |
|--------------------|------------|----------|------------------|---------------|
| <span data-ttu-id="58fae-119">Черный тон</span><span class="sxs-lookup"><span data-stu-id="58fae-119">Pitch Black</span></span>        | <span data-ttu-id="58fae-120">0</span><span class="sxs-lookup"><span data-stu-id="58fae-120">0</span></span>          | <span data-ttu-id="58fae-121">10</span><span class="sxs-lookup"><span data-stu-id="58fae-121">10</span></span>       | <span data-ttu-id="58fae-122">5</span><span class="sxs-lookup"><span data-stu-id="58fae-122">5</span></span>                | <span data-ttu-id="58fae-123">1</span><span class="sxs-lookup"><span data-stu-id="58fae-123">1</span></span>             |
| <span data-ttu-id="58fae-124">Очень темный</span><span class="sxs-lookup"><span data-stu-id="58fae-124">Very Dark</span></span>          | <span data-ttu-id="58fae-125">11</span><span class="sxs-lookup"><span data-stu-id="58fae-125">11</span></span>         | <span data-ttu-id="58fae-126">50</span><span class="sxs-lookup"><span data-stu-id="58fae-126">50</span></span>       | <span data-ttu-id="58fae-127">30</span><span class="sxs-lookup"><span data-stu-id="58fae-127">30</span></span>               | <span data-ttu-id="58fae-128">2</span><span class="sxs-lookup"><span data-stu-id="58fae-128">2</span></span>             |
| <span data-ttu-id="58fae-129">Темные двери</span><span class="sxs-lookup"><span data-stu-id="58fae-129">Dark Indoors</span></span>       | <span data-ttu-id="58fae-130">51</span><span class="sxs-lookup"><span data-stu-id="58fae-130">51</span></span>         | <span data-ttu-id="58fae-131">200</span><span class="sxs-lookup"><span data-stu-id="58fae-131">200</span></span>      | <span data-ttu-id="58fae-132">125</span><span class="sxs-lookup"><span data-stu-id="58fae-132">125</span></span>              | <span data-ttu-id="58fae-133">3</span><span class="sxs-lookup"><span data-stu-id="58fae-133">3</span></span>             |
| <span data-ttu-id="58fae-134">Затениить крышки</span><span class="sxs-lookup"><span data-stu-id="58fae-134">Dim Indoors</span></span>        | <span data-ttu-id="58fae-135">201</span><span class="sxs-lookup"><span data-stu-id="58fae-135">201</span></span>        | <span data-ttu-id="58fae-136">400</span><span class="sxs-lookup"><span data-stu-id="58fae-136">400</span></span>      | <span data-ttu-id="58fae-137">300</span><span class="sxs-lookup"><span data-stu-id="58fae-137">300</span></span>              | <span data-ttu-id="58fae-138">4</span><span class="sxs-lookup"><span data-stu-id="58fae-138">4</span></span>             |
| <span data-ttu-id="58fae-139">Нормальные выдвижки</span><span class="sxs-lookup"><span data-stu-id="58fae-139">Normal Indoors</span></span>     | <span data-ttu-id="58fae-140">401</span><span class="sxs-lookup"><span data-stu-id="58fae-140">401</span></span>        | <span data-ttu-id="58fae-141">1000</span><span class="sxs-lookup"><span data-stu-id="58fae-141">1000</span></span>     | <span data-ttu-id="58fae-142">700</span><span class="sxs-lookup"><span data-stu-id="58fae-142">700</span></span>              | <span data-ttu-id="58fae-143">5</span><span class="sxs-lookup"><span data-stu-id="58fae-143">5</span></span>             |
| <span data-ttu-id="58fae-144">Яркие крышки</span><span class="sxs-lookup"><span data-stu-id="58fae-144">Bright Indoors</span></span>     | <span data-ttu-id="58fae-145">1001</span><span class="sxs-lookup"><span data-stu-id="58fae-145">1001</span></span>       | <span data-ttu-id="58fae-146">5000</span><span class="sxs-lookup"><span data-stu-id="58fae-146">5000</span></span>     | <span data-ttu-id="58fae-147">3000</span><span class="sxs-lookup"><span data-stu-id="58fae-147">3000</span></span>             | <span data-ttu-id="58fae-148">6</span><span class="sxs-lookup"><span data-stu-id="58fae-148">6</span></span>             |
| <span data-ttu-id="58fae-149">Dim туризм</span><span class="sxs-lookup"><span data-stu-id="58fae-149">Dim Outdoors</span></span>       | <span data-ttu-id="58fae-150">5001</span><span class="sxs-lookup"><span data-stu-id="58fae-150">5001</span></span>       | <span data-ttu-id="58fae-151">10 000</span><span class="sxs-lookup"><span data-stu-id="58fae-151">10,000</span></span>   | <span data-ttu-id="58fae-152">7500</span><span class="sxs-lookup"><span data-stu-id="58fae-152">7500</span></span>             | <span data-ttu-id="58fae-153">7</span><span class="sxs-lookup"><span data-stu-id="58fae-153">7</span></span>             |
| <span data-ttu-id="58fae-154">Cloud туризм</span><span class="sxs-lookup"><span data-stu-id="58fae-154">Cloudy Outdoors</span></span>    | <span data-ttu-id="58fae-155">10 001</span><span class="sxs-lookup"><span data-stu-id="58fae-155">10,001</span></span>     | <span data-ttu-id="58fae-156">30 000</span><span class="sxs-lookup"><span data-stu-id="58fae-156">30,000</span></span>   | <span data-ttu-id="58fae-157">20 000</span><span class="sxs-lookup"><span data-stu-id="58fae-157">20,000</span></span>           | <span data-ttu-id="58fae-158">8</span><span class="sxs-lookup"><span data-stu-id="58fae-158">8</span></span>             |
| <span data-ttu-id="58fae-159">Прямые солнечные света</span><span class="sxs-lookup"><span data-stu-id="58fae-159">Direct Sunlight</span></span>    | <span data-ttu-id="58fae-160">30 001</span><span class="sxs-lookup"><span data-stu-id="58fae-160">30,001</span></span>     | <span data-ttu-id="58fae-161">100 000</span><span class="sxs-lookup"><span data-stu-id="58fae-161">100,000</span></span>  | <span data-ttu-id="58fae-162">65 000</span><span class="sxs-lookup"><span data-stu-id="58fae-162">65,000</span></span>           | <span data-ttu-id="58fae-163">9</span><span class="sxs-lookup"><span data-stu-id="58fae-163">9</span></span>             |



 

<span data-ttu-id="58fae-164">Если мы будем визуализировать эти данные, используя средние значения из этой таблицы, мы видим, что отношение "Lux к освещению" не линейное, как показано на следующем графике.</span><span class="sxs-lookup"><span data-stu-id="58fae-164">If we visualize this data by using the mean values from this table, we see that the lux-to-lighting-step relationship is not linear, as show in the following graph.</span></span>

![Линейный иллуминанце граф](images/luxtostep.png)

<span data-ttu-id="58fae-166">Однако при просмотре этих данных с помощью логарифмической шкалы на оси x видно, что появляется приблизительное линейное отношение.</span><span class="sxs-lookup"><span data-stu-id="58fae-166">However, if we view this data by using a logarithmic scale on the x-axis, we can see that a roughly linear relationship emerges.</span></span>

![Логарифмическая иллуминанце диаграмма](images/luxlogtostep.png)

### <a name="an-example-transform"></a><span data-ttu-id="58fae-168">Пример преобразования</span><span class="sxs-lookup"><span data-stu-id="58fae-168">An Example Transform</span></span>

<span data-ttu-id="58fae-169">На основе образца набора данных для датчиков внешнего освещения, приведенного ранее, можно приступить к приведенному ниже уравнению, чтобы сопоставлять значения Lux с человеческим восприятием.</span><span class="sxs-lookup"><span data-stu-id="58fae-169">Based on the sample data set for ambient light sensors previously provided, you could arrive at the following equation to map lux values to human perception.</span></span> <span data-ttu-id="58fae-170">В этом примере ожидаемые значения находятся в диапазоне от 0 Lux до 1 000 000 LUX.</span><span class="sxs-lookup"><span data-stu-id="58fae-170">In this example, the expected values range from 0 lux to 1,000,000 lux.</span></span>

![уравнение значения Lux](images/sensor-lux-equation.jpg)

<span data-ttu-id="58fae-172">Это уравнение приводит к получению значений, которые варьируются примерно линейно в диапазоне от 0,0 до 1,0.</span><span class="sxs-lookup"><span data-stu-id="58fae-172">This equation results in values that vary in a roughly linear fashion between 0.0 and 1.0.</span></span> <span data-ttu-id="58fae-173">Этот результат показывает, как воспринимаемое пользователем освещение изменилось на основе показанного выше примера набора данных.</span><span class="sxs-lookup"><span data-stu-id="58fae-173">This result indicates how human-perceived lighting changed based on the example data set that was shown previously.</span></span>

 

 



