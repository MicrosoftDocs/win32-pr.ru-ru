---
description: Чтобы полностью понять шейдер, который реализует PRT, полезно получить формулу, используемую шейдером для вычисления выходного радианце.
ms.assetid: 66876e9e-cde1-4d04-9b31-30be1c115e6b
title: Уравнения PRT (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a65559fada82fda7f7eed1c7d05543883a06a19e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104140198"
---
# <a name="prt-equations-direct3d-9"></a><span data-ttu-id="837a5-103">Уравнения PRT (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="837a5-103">PRT Equations (Direct3D 9)</span></span>

<span data-ttu-id="837a5-104">Чтобы полностью понять шейдер, который реализует PRT, полезно получить формулу, используемую шейдером для вычисления выходного радианце.</span><span class="sxs-lookup"><span data-stu-id="837a5-104">To fully understand a shader that implements PRT, it is useful to derive the formula the shader uses to calculate exit radiance.</span></span>

<span data-ttu-id="837a5-105">Чтобы начать работу, следующее уравнение является общим уравнением для вычисления выходного радианце, полученного в результате прямого освещения на рассеянном объекте с произвольным удаленным освещением.</span><span class="sxs-lookup"><span data-stu-id="837a5-105">To start off, the following equation is the general equation to calculate exit radiance resulting from direct lighting on a diffuse object with arbitrary distant lighting.</span></span>

![уравнение радианце выхода, полученное в результате прямого освещения на рассеянном объекте с произвольным удаленным освещением](images/prt-theory-eq1.png)

<span data-ttu-id="837a5-107">где:</span><span class="sxs-lookup"><span data-stu-id="837a5-107">where:</span></span>



| <span data-ttu-id="837a5-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="837a5-108">Parameter</span></span>     | <span data-ttu-id="837a5-109">Описание</span><span class="sxs-lookup"><span data-stu-id="837a5-109">Description</span></span>                                                                                             |
|---------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="837a5-110">RP</span><span class="sxs-lookup"><span data-stu-id="837a5-110">Rₚ</span></span>            | <span data-ttu-id="837a5-111">Радианце выхода в вершине p.</span><span class="sxs-lookup"><span data-stu-id="837a5-111">The exit radiance at vertex p.</span></span> <span data-ttu-id="837a5-112">Вычисляется на каждой вершине сетки.</span><span class="sxs-lookup"><span data-stu-id="837a5-112">Evaluated at every vertex on the mesh.</span></span>                                   |
| <span data-ttu-id="837a5-113">p<sub>d</sub></span><span class="sxs-lookup"><span data-stu-id="837a5-113">p<sub>d</sub></span></span> | <span data-ttu-id="837a5-114">Албедо поверхности.</span><span class="sxs-lookup"><span data-stu-id="837a5-114">The albedo of the surface.</span></span>                                                                              |
| <span data-ttu-id="837a5-115">pi</span><span class="sxs-lookup"><span data-stu-id="837a5-115">pi</span></span>            | <span data-ttu-id="837a5-116">Константа, используемая в качестве коэффициента нормализации энергии.</span><span class="sxs-lookup"><span data-stu-id="837a5-116">A constant, used as an energy conservation normalization factor.</span></span>                                        |
| <span data-ttu-id="837a5-117">L (s)</span><span class="sxs-lookup"><span data-stu-id="837a5-117">L(s)</span></span>          | <span data-ttu-id="837a5-118">Среда освещения (источник радианце).</span><span class="sxs-lookup"><span data-stu-id="837a5-118">The lighting environment (source radiance).</span></span>                                                             |
| <span data-ttu-id="837a5-119">Вице — президент ₍ s ₎</span><span class="sxs-lookup"><span data-stu-id="837a5-119">Vₚ₍ₛ₎</span></span>         | <span data-ttu-id="837a5-120">Двоичная функция видимости для точки p.</span><span class="sxs-lookup"><span data-stu-id="837a5-120">A binary visibility function for point p.</span></span> <span data-ttu-id="837a5-121">Значение равно 1, если точка может видеть освещение, 0 в противном случае.</span><span class="sxs-lookup"><span data-stu-id="837a5-121">It is 1 if the point can see the light, 0 if not.</span></span>             |
| <span data-ttu-id="837a5-122">₎ ХНП ₍ s</span><span class="sxs-lookup"><span data-stu-id="837a5-122">Hₙₚ₍ₛ₎</span></span>        | <span data-ttu-id="837a5-123">Косинус из закона Ламберта.</span><span class="sxs-lookup"><span data-stu-id="837a5-123">The cosine term from Lambert's law.</span></span> <span data-ttu-id="837a5-124">Равно Max ((NP · s), 0), где NP — это нормальная поверхность в точке p.</span><span class="sxs-lookup"><span data-stu-id="837a5-124">Equal to max((Nₚ· s), 0) where Nₚ is the surface normal at point p.</span></span> |
| <span data-ttu-id="837a5-125">s</span><span class="sxs-lookup"><span data-stu-id="837a5-125">s</span></span>             | <span data-ttu-id="837a5-126">Переменная, которая интегрируется над сферой.</span><span class="sxs-lookup"><span data-stu-id="837a5-126">The variable that integrates over the sphere.</span></span>                                                           |



 

<span data-ttu-id="837a5-127">Использование сферовых функций, таких как сферические гармонические колебания, в следующем уравнении приблизительно соответствует среде освещения.</span><span class="sxs-lookup"><span data-stu-id="837a5-127">Using spherical basis functions, such as spherical harmonics, the following equation approximates the lighting environment.</span></span>

![уравнение среды освещения](images/prt-theory-eq2.png)

<span data-ttu-id="837a5-129">где:</span><span class="sxs-lookup"><span data-stu-id="837a5-129">where:</span></span>



| <span data-ttu-id="837a5-130">Параметр</span><span class="sxs-lookup"><span data-stu-id="837a5-130">Parameter</span></span>        | <span data-ttu-id="837a5-131">Описание</span><span class="sxs-lookup"><span data-stu-id="837a5-131">Description</span></span>                                              |
|------------------|----------------------------------------------------------|
| <span data-ttu-id="837a5-132">L (s)</span><span class="sxs-lookup"><span data-stu-id="837a5-132">L(s)</span></span>             | <span data-ttu-id="837a5-133">Среда освещения (источник радианце).</span><span class="sxs-lookup"><span data-stu-id="837a5-133">The lighting environment (source radiance).</span></span>              |
| <span data-ttu-id="837a5-134">i</span><span class="sxs-lookup"><span data-stu-id="837a5-134">i</span></span>                | <span data-ttu-id="837a5-135">Целое число, которое суммирует за число базисных функций.</span><span class="sxs-lookup"><span data-stu-id="837a5-135">An integer that sums over the number of basis functions.</span></span> |
| <span data-ttu-id="837a5-136">O</span><span class="sxs-lookup"><span data-stu-id="837a5-136">O</span></span>                | <span data-ttu-id="837a5-137">Порядок сферических гармоний.</span><span class="sxs-lookup"><span data-stu-id="837a5-137">The order of spherical harmonics.</span></span>                        |
| <span data-ttu-id="837a5-138">l<sub>i</sub></span><span class="sxs-lookup"><span data-stu-id="837a5-138">l<sub>i</sub></span></span>    | <span data-ttu-id="837a5-139">Коэффициент.</span><span class="sxs-lookup"><span data-stu-id="837a5-139">A coefficient.</span></span>                                           |
| <span data-ttu-id="837a5-140">Y<sub>i (s)</sub></span><span class="sxs-lookup"><span data-stu-id="837a5-140">Y<sub>i(s)</sub></span></span> | <span data-ttu-id="837a5-141">Некоторой базовой функции над сферой.</span><span class="sxs-lookup"><span data-stu-id="837a5-141">Some basis function over the sphere.</span></span>                     |



 

<span data-ttu-id="837a5-142">Коллекция этих коэффициентов, L, обеспечивает оптимальное приближение для функции L с использованием базисных функций Y (s).</span><span class="sxs-lookup"><span data-stu-id="837a5-142">The collection of these coefficients, L', provides the optimal approximation for function L(s) with the basis functions Y(s).</span></span> <span data-ttu-id="837a5-143">Подстановка и распространение дает следующее уравнение.</span><span class="sxs-lookup"><span data-stu-id="837a5-143">Substituting and distributing yields the following equation.</span></span>

![Формула выхода радианце после подстановки l (s) и распространение](images/prt-theory-eq3.png)

<span data-ttu-id="837a5-145">Неотъемлемой частью<sub>i (s)</sub>вице-президента ₍ s ₎ ХНП ₍ s ₎ является коэффициент пересылки t<sub>Pi</sub> , который в симуляторе выполняет предварительное вычисление для каждой вершины в сети.</span><span class="sxs-lookup"><span data-stu-id="837a5-145">The integral of Y<sub>i(s)</sub>Vₚ₍ₛ₎Hₙₚ₍ₛ₎ is a transfer coefficient t<sub>pi</sub> that the simulator precomputes for every vertex on the mesh.</span></span> <span data-ttu-id="837a5-146">При замене это дает следующее уравнение.</span><span class="sxs-lookup"><span data-stu-id="837a5-146">Substituting this yields the following equation.</span></span>

![уравнение радианце выхода после подстановки коэффициента пересылки](images/prt-theory-eq4.png)

<span data-ttu-id="837a5-148">При изменении этого значения на векторную нотацию выводится следующее несжатое уравнение для вычисления выходного радианце для каждого канала.</span><span class="sxs-lookup"><span data-stu-id="837a5-148">Changing this to vector notation yields the following uncompressed equation to calculate exit radiance for each channel.</span></span>

![уравнение радианце выхода после перехода на векторную нотацию](images/prt-theory-eq5.png)

<span data-ttu-id="837a5-150">где:</span><span class="sxs-lookup"><span data-stu-id="837a5-150">where:</span></span>



| <span data-ttu-id="837a5-151">Параметр</span><span class="sxs-lookup"><span data-stu-id="837a5-151">Parameter</span></span>     | <span data-ttu-id="837a5-152">Описание</span><span class="sxs-lookup"><span data-stu-id="837a5-152">Description</span></span>                                                                                                                                                                         |
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="837a5-153">RP</span><span class="sxs-lookup"><span data-stu-id="837a5-153">Rₚ</span></span>            | <span data-ttu-id="837a5-154">Радианце выхода в вершине p.</span><span class="sxs-lookup"><span data-stu-id="837a5-154">The exit radiance at vertex p.</span></span>                                                                                                                                                      |
| <span data-ttu-id="837a5-155">p<sub>d</sub></span><span class="sxs-lookup"><span data-stu-id="837a5-155">p<sub>d</sub></span></span> | <span data-ttu-id="837a5-156">Албедо поверхности.</span><span class="sxs-lookup"><span data-stu-id="837a5-156">The albedo of the surface.</span></span>                                                                                                                                                          |
| <span data-ttu-id="837a5-157">Н</span><span class="sxs-lookup"><span data-stu-id="837a5-157">L'</span></span>            | <span data-ttu-id="837a5-158">Вектор l<sub>i</sub>и является проекцией исходного радианце в сферические функции-основания.</span><span class="sxs-lookup"><span data-stu-id="837a5-158">The vector of l<sub>i</sub>, and is the projection of the source radiance into the spherical harmonic basis functions.</span></span> <span data-ttu-id="837a5-159">Это порядок следования в виде вектора сферического гармонического коэффициента.</span><span class="sxs-lookup"><span data-stu-id="837a5-159">This is an order² vector of spherical harmonic coefficients.</span></span> |
| <span data-ttu-id="837a5-160">Пи</span><span class="sxs-lookup"><span data-stu-id="837a5-160">Tₚ</span></span>            | <span data-ttu-id="837a5-161">Вектор перемещения Order ² для вершины p.</span><span class="sxs-lookup"><span data-stu-id="837a5-161">An order² transfer vector for vertex p.</span></span> <span data-ttu-id="837a5-162">Симулятор делит коэффициенты перемещения на p.</span><span class="sxs-lookup"><span data-stu-id="837a5-162">The simulator divides the transfer coefficients by p.</span></span>                                                                                       |



 

<span data-ttu-id="837a5-163">Оба этих вектора являются вектором порядка следования для сферических гармонических коэффициентов, поэтому обратите внимание, что это просто элементный продукт.</span><span class="sxs-lookup"><span data-stu-id="837a5-163">Both of these vectors are an order² vector of spherical harmonic coefficients, so notice that this is simply a dot product.</span></span> <span data-ttu-id="837a5-164">В зависимости от порядка, точка может быть дорогостоящей, поэтому можно использовать сжатие.</span><span class="sxs-lookup"><span data-stu-id="837a5-164">Depending on the order, the dot can be expensive so compression can be used.</span></span> <span data-ttu-id="837a5-165">Алгоритм, именуемый анализом кластеризованных основных компонентов (КПКА), эффективно сжимает данные.</span><span class="sxs-lookup"><span data-stu-id="837a5-165">An algorithm called Clustered Principal Component Analysis (CPCA) efficiently compresses the data.</span></span> <span data-ttu-id="837a5-166">Это позволяет использовать грубые гармонические колебания более высокого порядка, что приводит к темным теням.</span><span class="sxs-lookup"><span data-stu-id="837a5-166">This enables the use of a higher-order spherical harmonic approximation which results in sharper shadows.</span></span>

<span data-ttu-id="837a5-167">КПКА предоставляет следующее уравнение для приближения к вектору перемещения.</span><span class="sxs-lookup"><span data-stu-id="837a5-167">CPCA provides the following equation to approximate the transfer vector.</span></span>

![уравнение приближенного вектора перемещения](images/prt-theory-eq6.png)

<span data-ttu-id="837a5-169">где:</span><span class="sxs-lookup"><span data-stu-id="837a5-169">where:</span></span>



| <span data-ttu-id="837a5-170">Параметр</span><span class="sxs-lookup"><span data-stu-id="837a5-170">Parameter</span></span>      | <span data-ttu-id="837a5-171">Описание</span><span class="sxs-lookup"><span data-stu-id="837a5-171">Description</span></span>                                          |
|----------------|------------------------------------------------------|
| <span data-ttu-id="837a5-172">Пи</span><span class="sxs-lookup"><span data-stu-id="837a5-172">Tₚ</span></span>             | <span data-ttu-id="837a5-173">Вектор перемещения для вершины p.</span><span class="sxs-lookup"><span data-stu-id="837a5-173">The transfer vector for vertex p.</span></span>                    |
| <span data-ttu-id="837a5-174">MK</span><span class="sxs-lookup"><span data-stu-id="837a5-174">Mₖ</span></span>             | <span data-ttu-id="837a5-175">Среднее для Cluster k.</span><span class="sxs-lookup"><span data-stu-id="837a5-175">The mean for cluster k.</span></span>                              |
| <span data-ttu-id="837a5-176">j</span><span class="sxs-lookup"><span data-stu-id="837a5-176">j</span></span>              | <span data-ttu-id="837a5-177">Целое число, которое суммирует по количеству векторов PCA.</span><span class="sxs-lookup"><span data-stu-id="837a5-177">An integer that sums over the number of PCA vectors.</span></span> |
| <span data-ttu-id="837a5-178">Нет</span><span class="sxs-lookup"><span data-stu-id="837a5-178">N</span></span>              | <span data-ttu-id="837a5-179">Число векторов PCA.</span><span class="sxs-lookup"><span data-stu-id="837a5-179">The number of PCA vectors.</span></span>                           |
| <span data-ttu-id="837a5-180">w<sub>PJ</sub></span><span class="sxs-lookup"><span data-stu-id="837a5-180">w<sub>pj</sub></span></span> | <span data-ttu-id="837a5-181">Вес ЖС PCA для точки p.</span><span class="sxs-lookup"><span data-stu-id="837a5-181">The jth PCA weight for point p.</span></span>                      |
| <span data-ttu-id="837a5-182">Б<sub>KJ</sub></span><span class="sxs-lookup"><span data-stu-id="837a5-182">B<sub>kj</sub></span></span> | <span data-ttu-id="837a5-183">Вектор ЖС PCA для кластера k.</span><span class="sxs-lookup"><span data-stu-id="837a5-183">The jth PCA basis vector for cluster k.</span></span>              |



 

<span data-ttu-id="837a5-184">Кластер — это просто некоторое количество вершин, имеющих одинаковый вектор.</span><span class="sxs-lookup"><span data-stu-id="837a5-184">A cluster is simply some number of vertices that share the same mean vector.</span></span> <span data-ttu-id="837a5-185">О том, как получить среднее значение кластера, весовые коэффициенты PCA, векторы PCA и идентификаторы кластеров для вершин обсуждаются ниже.</span><span class="sxs-lookup"><span data-stu-id="837a5-185">How to get the cluster mean, the PCA weights, the PCA basis vectors, and the cluster ids for the vertices is discussed below.</span></span>

<span data-ttu-id="837a5-186">При замене этих двух формул выдается следующее:</span><span class="sxs-lookup"><span data-stu-id="837a5-186">Substituting these two equations yields:</span></span>

![уравнение радианцеа выхода после подстановки вектора перемещения](images/prt-theory-eq7.png)

<span data-ttu-id="837a5-188">Затем при распространении произведения точки выдается следующее уравнение.</span><span class="sxs-lookup"><span data-stu-id="837a5-188">Then distributing the dot product yields the following equation.</span></span>

![Формула выхода радианце после распространения произведения точки](images/prt-theory-eq8.png)

<span data-ttu-id="837a5-190">Так как оба (MK · L ') и (B<sub>KJ</sub>· L ') — константа на вершину, пример вычисляет эти значения с помощью ЦП и передает их в виде констант в шейдер вершин. так как w<sub>PJ</sub> изменяется для каждой вершины, в этом примере данные для каждой вершины сохраняются в буфере вершин.</span><span class="sxs-lookup"><span data-stu-id="837a5-190">Because both (Mₖ· L') and (B<sub>kj</sub>· L') are constant per vertex, the sample calculates these values with the CPU and passes them as constants into the vertex shader; because w<sub>pj</sub> changes for each vertex, the sample stores this per-vertex data in the vertex buffer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="837a5-191">См. также</span><span class="sxs-lookup"><span data-stu-id="837a5-191">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="837a5-192">Предварительно вычисленный перенос Радианце</span><span class="sxs-lookup"><span data-stu-id="837a5-192">Precomputed Radiance Transfer</span></span>](precomputed-radiance-transfer.md)
</dt> </dl>

 

 



