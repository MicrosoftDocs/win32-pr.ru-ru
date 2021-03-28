---
title: Оптимизация шейдеров HLSL
description: В этом разделе описываются стратегии общего назначения, которые можно использовать для оптимизации шейдеров. Эти стратегии можно применять к шейдерам, написанным на любом языке, на любой платформе.
ms.assetid: 014b9cb3-a489-48d7-8174-b97de168bf3a
keywords:
- язык шейдера высокого уровня
- HLSL, производительность
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 06d3bb806e98e489020aa1755ef2a6c952459d86
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068362"
---
# <a name="optimizing-hlsl-shaders"></a><span data-ttu-id="a2f49-106">Оптимизация шейдеров HLSL</span><span class="sxs-lookup"><span data-stu-id="a2f49-106">Optimizing HLSL Shaders</span></span>

<span data-ttu-id="a2f49-107">В этом разделе описываются стратегии общего назначения, которые можно использовать для оптимизации шейдеров.</span><span class="sxs-lookup"><span data-stu-id="a2f49-107">This section describes general-purpose strategies that you can use to optimize your shaders.</span></span> <span data-ttu-id="a2f49-108">Эти стратегии можно применять к шейдерам, написанным на любом языке, на любой платформе.</span><span class="sxs-lookup"><span data-stu-id="a2f49-108">You can apply these strategies to shaders that are written in any language, on any platform.</span></span>

-   [<span data-ttu-id="a2f49-109">Узнайте, где выполнять вычисления шейдера</span><span class="sxs-lookup"><span data-stu-id="a2f49-109">Know Where To Perform Shader Calculations</span></span>](#know-where-to-perform-shader-calculations)
-   [<span data-ttu-id="a2f49-110">Пропустить ненужные инструкции</span><span class="sxs-lookup"><span data-stu-id="a2f49-110">Skip Unnecessary Instructions</span></span>](#skip-unnecessary-instructions)
-   [<span data-ttu-id="a2f49-111">Переменные Pack и Интерполантс</span><span class="sxs-lookup"><span data-stu-id="a2f49-111">Pack Variables and Interpolants</span></span>](#pack-variables-and-interpolants)
-   [<span data-ttu-id="a2f49-112">Уменьшение сложности шейдера</span><span class="sxs-lookup"><span data-stu-id="a2f49-112">Reduce Shader Complexity</span></span>](#reduce-shader-complexity)
-   [<span data-ttu-id="a2f49-113">См. также</span><span class="sxs-lookup"><span data-stu-id="a2f49-113">Related Topics</span></span>](#related-topics)
-   [<span data-ttu-id="a2f49-114">См. также</span><span class="sxs-lookup"><span data-stu-id="a2f49-114">Related topics</span></span>](#related-topics)

## <a name="know-where-to-perform-shader-calculations"></a><span data-ttu-id="a2f49-115">Узнайте, где выполнять вычисления шейдера</span><span class="sxs-lookup"><span data-stu-id="a2f49-115">Know Where To Perform Shader Calculations</span></span>

<span data-ttu-id="a2f49-116">Шейдеры вершин выполняют операции, которые включают выборку вершин и выполнение преобразования матрицы в данные вершин.</span><span class="sxs-lookup"><span data-stu-id="a2f49-116">Vertex shaders perform operations that include fetching vertices and performing matrix transformation of vertex data.</span></span> <span data-ttu-id="a2f49-117">Как правило, шейдеры вершин выполняются один раз для каждой вершины.</span><span class="sxs-lookup"><span data-stu-id="a2f49-117">Typically, vertex shaders are executed once per vertex.</span></span>

<span data-ttu-id="a2f49-118">Шейдеры пикселей выполняют операции, которые включают выборку данных текстуры и выполнение вычислений освещения.</span><span class="sxs-lookup"><span data-stu-id="a2f49-118">Pixel Shaders perform operations that include fetching texture data and performing lighting calculations.</span></span> <span data-ttu-id="a2f49-119">Как правило, шейдеры пикселей выполняются один раз на пиксель для определенного фрагмента геометрии.</span><span class="sxs-lookup"><span data-stu-id="a2f49-119">Typically, pixel shaders are executed once per pixel for a given piece of geometry.</span></span>

<span data-ttu-id="a2f49-120">Обычно в пикселях нумеруются вершины в сцене, поэтому шейдеры пикселей выполняются чаще, чем шейдеры вершин.</span><span class="sxs-lookup"><span data-stu-id="a2f49-120">Typically, pixels outnumber vertices in a scene, so pixel shaders execute more often than vertex shaders.</span></span>

<span data-ttu-id="a2f49-121">При проектировании алгоритмов шейдера необходимо учитывать следующее.</span><span class="sxs-lookup"><span data-stu-id="a2f49-121">When you design shader algorithms, keep the following in mind:</span></span>

-   <span data-ttu-id="a2f49-122">По возможности выполняйте вычисления в шейдере вершин.</span><span class="sxs-lookup"><span data-stu-id="a2f49-122">Perform calculations on the vertex shader if possible.</span></span> <span data-ttu-id="a2f49-123">Вычисление, выполняемое на шейдере пикселей, гораздо дороже, чем вычисление, выполняемое на шейдере вершин.</span><span class="sxs-lookup"><span data-stu-id="a2f49-123">A calculation that is performed on a pixel shader is much more expensive than a calculation that is performed on a vertex shader.</span></span>
-   <span data-ttu-id="a2f49-124">Используйте вычисления для каждой вершины, чтобы повысить производительность в таких ситуациях, как сжатые сети.</span><span class="sxs-lookup"><span data-stu-id="a2f49-124">Consider using per-vertex calculations to improve performance in situations such as dense meshes.</span></span> <span data-ttu-id="a2f49-125">Для плотных сеток вычисления по вершинам могут формировать результаты, визуально не отличающиеся от результатов, полученных при вычислениях на основе точек.</span><span class="sxs-lookup"><span data-stu-id="a2f49-125">For dense meshes, per-vertex calculations may produce results that are visually indistinguishable from results produced with per-pixel calculations.</span></span>

## <a name="skip-unnecessary-instructions"></a><span data-ttu-id="a2f49-126">Пропустить ненужные инструкции</span><span class="sxs-lookup"><span data-stu-id="a2f49-126">Skip Unnecessary Instructions</span></span>

<span data-ttu-id="a2f49-127">В HLSL Динамическое ветвление позволяет ограничить количество выполняемых инструкций.</span><span class="sxs-lookup"><span data-stu-id="a2f49-127">In HLSL, dynamic branching provides the ability to limit the number of instructions that are executed.</span></span> <span data-ttu-id="a2f49-128">Таким образом, Динамическое ветвление помогает ускорить выполнение шейдера.</span><span class="sxs-lookup"><span data-stu-id="a2f49-128">Therefore, dynamic branching can help speed up shader execution time.</span></span> <span data-ttu-id="a2f49-129">Если геометрия или Пиксели не отображаются, используйте динамическое ветвление для выхода из шейдера или для ограничения инструкций.</span><span class="sxs-lookup"><span data-stu-id="a2f49-129">If geometry or pixels are not displayed, use dynamic branching to exit the shader or to limit instructions.</span></span> <span data-ttu-id="a2f49-130">Например, если пиксел не горит, то нет никакой точки в исполнении алгоритма освещения.</span><span class="sxs-lookup"><span data-stu-id="a2f49-130">For example, if a pixel is not lit, there is no point in executing the lighting algorithm.</span></span>

<span data-ttu-id="a2f49-131">В следующей таблице перечислены случаи, когда можно проверить условия в шейдере и использовать динамическое ветвление для пропуска ненужных инструкций.</span><span class="sxs-lookup"><span data-stu-id="a2f49-131">The following table lists some cases where you can test conditions in your shader and use dynamic branching to skip unnecessary instructions.</span></span> <span data-ttu-id="a2f49-132">Таблица не является исчерпывающей.</span><span class="sxs-lookup"><span data-stu-id="a2f49-132">The table not comprehensive.</span></span> <span data-ttu-id="a2f49-133">Вместо этого он предназначен для предоставления идей по оптимизации кода.</span><span class="sxs-lookup"><span data-stu-id="a2f49-133">Rather, it is intended to give you ideas for optimizing your code.</span></span>



| <span data-ttu-id="a2f49-134">Проверяемое условие</span><span class="sxs-lookup"><span data-stu-id="a2f49-134">Condition to Check</span></span>                                    | <span data-ttu-id="a2f49-135">Ответ в шейдере</span><span class="sxs-lookup"><span data-stu-id="a2f49-135">Response in the Shader</span></span>       |
|-------------------------------------------------------|------------------------------|
| <span data-ttu-id="a2f49-136">Проверка альфа-канала определяет, что пиксель не будет отображаться.</span><span class="sxs-lookup"><span data-stu-id="a2f49-136">Alpha check determines that a pixel will not be seen.</span></span> | <span data-ttu-id="a2f49-137">Пропустите оставшуюся часть шейдера.</span><span class="sxs-lookup"><span data-stu-id="a2f49-137">Skip the rest of the shader.</span></span> |
| <span data-ttu-id="a2f49-138">Пиксель или геометрия полностью фогжед.</span><span class="sxs-lookup"><span data-stu-id="a2f49-138">The pixel or geometry is fully fogged.</span></span>                | <span data-ttu-id="a2f49-139">Пропустите оставшуюся часть шейдера.</span><span class="sxs-lookup"><span data-stu-id="a2f49-139">Skip the rest of the shader.</span></span> |
| <span data-ttu-id="a2f49-140">Вес обложки равен нулю.</span><span class="sxs-lookup"><span data-stu-id="a2f49-140">Skin weights are zero.</span></span>                                | <span data-ttu-id="a2f49-141">Пропустите кости.</span><span class="sxs-lookup"><span data-stu-id="a2f49-141">Skip bones.</span></span>                  |
| <span data-ttu-id="a2f49-142">Ослабление яркости равно нулю.</span><span class="sxs-lookup"><span data-stu-id="a2f49-142">Light attenuation is zero.</span></span>                            | <span data-ttu-id="a2f49-143">Пропустить освещение.</span><span class="sxs-lookup"><span data-stu-id="a2f49-143">Skip lighting.</span></span>               |
| <span data-ttu-id="a2f49-144">Неположительный Ламбертиан термин.</span><span class="sxs-lookup"><span data-stu-id="a2f49-144">Non-positive Lambertian term.</span></span>                         | <span data-ttu-id="a2f49-145">Пропустить освещение.</span><span class="sxs-lookup"><span data-stu-id="a2f49-145">Skip lighting.</span></span>               |



 

## <a name="pack-variables-and-interpolants"></a><span data-ttu-id="a2f49-146">Переменные Pack и Интерполантс</span><span class="sxs-lookup"><span data-stu-id="a2f49-146">Pack Variables and Interpolants</span></span>

<span data-ttu-id="a2f49-147">Учитывать пространство, необходимое для данных шейдера.</span><span class="sxs-lookup"><span data-stu-id="a2f49-147">Be mindful of the space required for shader data.</span></span> <span data-ttu-id="a2f49-148">Упаковать как можно больше информации в переменную или интерполант.</span><span class="sxs-lookup"><span data-stu-id="a2f49-148">Pack as much information into a variable or interpolant as possible.</span></span> <span data-ttu-id="a2f49-149">Иногда сведения из двух переменных можно упаковывать в область памяти одной переменной.</span><span class="sxs-lookup"><span data-stu-id="a2f49-149">Sometimes, the information from two variables can be packed into the memory space of a single variable.</span></span>

## <a name="reduce-shader-complexity"></a><span data-ttu-id="a2f49-150">Уменьшение сложности шейдера</span><span class="sxs-lookup"><span data-stu-id="a2f49-150">Reduce Shader Complexity</span></span>

<span data-ttu-id="a2f49-151">Старайтесь не усложнять шейдеры.</span><span class="sxs-lookup"><span data-stu-id="a2f49-151">Keep your shaders small and simple.</span></span> <span data-ttu-id="a2f49-152">Как правило, шейдеры с меньшим количеством инструкций выполняются быстрее, чем шейдеры с дополнительными инструкциями.</span><span class="sxs-lookup"><span data-stu-id="a2f49-152">In general, shaders with fewer instructions execute more quickly than shaders with more instructions.</span></span> <span data-ttu-id="a2f49-153">Также проще выполнять отладку и оптимизацию небольших, менее сложных шейдеров.</span><span class="sxs-lookup"><span data-stu-id="a2f49-153">It is also easier to debug and optimize smaller, less complex shaders.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a2f49-154">См. также</span><span class="sxs-lookup"><span data-stu-id="a2f49-154">Related Topics</span></span>

[<span data-ttu-id="a2f49-155">Руководство по программированию для HLSL</span><span class="sxs-lookup"><span data-stu-id="a2f49-155">Programming Guide for HLSL</span></span>](dx-graphics-hlsl-pguide.md)


## <a name="related-topics"></a><span data-ttu-id="a2f49-156">См. также</span><span class="sxs-lookup"><span data-stu-id="a2f49-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a2f49-157">Руководство по программированию для HLSL</span><span class="sxs-lookup"><span data-stu-id="a2f49-157">Programming Guide for HLSL</span></span>](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

 




