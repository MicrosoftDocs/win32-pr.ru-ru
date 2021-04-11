---
description: Для многих методов отрисовки и создания содержимого требуется уникальная, непересекающаяся схема 2D-сигнала (например, текстура) на сетке.
ms.assetid: 0ec19e8c-2a14-4392-93de-7ab832784085
title: Использование Уватлас (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b335dd6ea94a3db0c0760b0d07a0b8df3fe4c7c
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/04/2021
ms.locfileid: "104273167"
---
# <a name="using-uvatlas-direct3d-9"></a><span data-ttu-id="6ccfc-103">Использование Уватлас (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="6ccfc-103">Using UVAtlas (Direct3D 9)</span></span>

<span data-ttu-id="6ccfc-104">Для многих методов отрисовки и создания содержимого требуется уникальная, непересекающаяся схема 2D-сигнала (например, текстура) на сетке.</span><span class="sxs-lookup"><span data-stu-id="6ccfc-104">Many rendering and content generation techniques require a unique, non-overlapping map of a 2D signal (such as a texture) onto a mesh.</span></span> <span data-ttu-id="6ccfc-105">К таким методам относятся:</span><span class="sxs-lookup"><span data-stu-id="6ccfc-105">Such techniques include:</span></span>

-   <span data-ttu-id="6ccfc-106">Сопоставление обычного и среднего смещения</span><span class="sxs-lookup"><span data-stu-id="6ccfc-106">Normal/displacement mapping</span></span>
-   <span data-ttu-id="6ccfc-107">Имитация PRTа текстуры и схемы освещения</span><span class="sxs-lookup"><span data-stu-id="6ccfc-107">Texture-space PRT simulations and light maps</span></span>
-   <span data-ttu-id="6ccfc-108">Рисование поверхности</span><span class="sxs-lookup"><span data-stu-id="6ccfc-108">Surface painting</span></span>
-   <span data-ttu-id="6ccfc-109">Освещение-пространство текстуры</span><span class="sxs-lookup"><span data-stu-id="6ccfc-109">Texture-space lighting</span></span>

<span data-ttu-id="6ccfc-110">Создание уникального UV-сопоставления вручную часто занимает много времени и утомительно; Это особенно важно, когда входная геометрическая фигура является сложной и эффективной или низкой интенсивностью использования пространства текстуры.</span><span class="sxs-lookup"><span data-stu-id="6ccfc-110">Generating a unique UV mapping manually is often time-consuming and tedious; this is especially true when the input geometry is complex and efficient/low-distortion texture-space utilization is desired.</span></span> <span data-ttu-id="6ccfc-111">На следующем рисунке показан пример сетки и соответствующая текстура Atlas.</span><span class="sxs-lookup"><span data-stu-id="6ccfc-111">The following illustration shows an example mesh and its corresponding texture atlas.</span></span>

![Показывает пример сетки и соответствующую текстуру Atlas.](images/uvatlas1.jpg)

<span data-ttu-id="6ccfc-113">В этом примере показана сетка слева и соответствующая нормальная схема UV-Space (справа).</span><span class="sxs-lookup"><span data-stu-id="6ccfc-113">This example shows a mesh (on the left) and the corresponding UV-space normal map (on the right).</span></span> <span data-ttu-id="6ccfc-114">Обратите внимание, что текстура Atlas содержит несколько групп или кластеров данных. Каждый кластер называется диаграммой и в приведенном выше примере отображает обычные данные для части сетки.</span><span class="sxs-lookup"><span data-stu-id="6ccfc-114">Notice that the texture atlas contains several groups or clusters of data; each cluster is called a chart and in the example above, displays contains the normal data for a portion of the mesh.</span></span>

<span data-ttu-id="6ccfc-115">API-интерфейсы D3DX Уватлас автоматически создают оптимальную, не пересекающую текстуру Atlas.</span><span class="sxs-lookup"><span data-stu-id="6ccfc-115">The D3DX UVAtlas APIs automatically generate an optimal, non-overlapping texture atlas.</span></span> <span data-ttu-id="6ccfc-116">Интерфейсы API предоставляют входные параметры, позволяющие:</span><span class="sxs-lookup"><span data-stu-id="6ccfc-116">The APIs provide input parameters that allow you to:</span></span>

-   <span data-ttu-id="6ccfc-117">Уменьшение растяжения, искажения и недовыборки текстур.</span><span class="sxs-lookup"><span data-stu-id="6ccfc-117">Minimize texture stretch, distortion, and undersampling.</span></span>
-   <span data-ttu-id="6ccfc-118">Максимальная плотность упаковки пространства текстуры для эффективного использования памяти.</span><span class="sxs-lookup"><span data-stu-id="6ccfc-118">Maximize texture-space packing density for efficient use of memory.</span></span>
-   <span data-ttu-id="6ccfc-119">Предоставьте одинаковую выборку по сети, уменьшая непрерывность при частоте выборки.</span><span class="sxs-lookup"><span data-stu-id="6ccfc-119">Provide an even sampling across the mesh, minimizing discontinuities in sampling frequency.</span></span>

## <a name="how-uvatlas-works"></a><span data-ttu-id="6ccfc-120">Как работает Уватлас</span><span class="sxs-lookup"><span data-stu-id="6ccfc-120">How UVAtlas Works</span></span>

<span data-ttu-id="6ccfc-121">API-интерфейсы Уватлас (см. раздел [функции уватлас](dx9-graphics-reference-d3dx-functions-uvatlas.md)) создают текстуру Atlas, выключая поверхность на диаграммах и упаковку диаграмм в текстуру Atlas.</span><span class="sxs-lookup"><span data-stu-id="6ccfc-121">The UVAtlas APIs (see [UVAtlas Functions](dx9-graphics-reference-d3dx-functions-uvatlas.md)) generate a texture atlas by partitioning a surface into charts and packing the charts into a texture atlas.</span></span> <span data-ttu-id="6ccfc-122">Используйте [**D3DXUVAtlasPartition**](d3dxuvatlaspartition.md) и [**D3DXUVAtlasPack**](d3dxuvatlaspack.md) для выполнения этих действий отдельно. или используйте [**D3DXUVAtlasCreate**](d3dxuvatlascreate.md) для секционирования, параметризации и упаковки в одном вызове.</span><span class="sxs-lookup"><span data-stu-id="6ccfc-122">Use [**D3DXUVAtlasPartition**](d3dxuvatlaspartition.md) and [**D3DXUVAtlasPack**](d3dxuvatlaspack.md) to perform these steps separately; or use [**D3DXUVAtlasCreate**](d3dxuvatlascreate.md) to partition, parameterize and pack in a single call.</span></span>

-   [<span data-ttu-id="6ccfc-123">Секционирование и параметризация сетки</span><span class="sxs-lookup"><span data-stu-id="6ccfc-123">Partitioning and Parameterizing a Mesh</span></span>](#partitioning-and-parameterizing-a-mesh)
-   [<span data-ttu-id="6ccfc-124">Использование встроенных десятков метрик для управления параметризации</span><span class="sxs-lookup"><span data-stu-id="6ccfc-124">Using Integrated Metric Tensors to Control Parameterization</span></span>](#using-integrated-metric-tensors-to-control-parameterization)
-   [<span data-ttu-id="6ccfc-125">Использование Соседовых данных для указанного пользователем Креасес</span><span class="sxs-lookup"><span data-stu-id="6ccfc-125">Using Adjacency Data for User Specified Creases</span></span>](#using-adjacency-data-for-user-specified-creases)
-   [<span data-ttu-id="6ccfc-126">Упаковка диаграмм в Atlas</span><span class="sxs-lookup"><span data-stu-id="6ccfc-126">Packing Charts Into an Atlas</span></span>](#packing-charts-into-an-atlas)

### <a name="partitioning-and-parameterizing-a-mesh"></a><span data-ttu-id="6ccfc-127">Секционирование и параметризация сетки</span><span class="sxs-lookup"><span data-stu-id="6ccfc-127">Partitioning and Parameterizing a Mesh</span></span>

<span data-ttu-id="6ccfc-128">Во-первых, сетка разделяется на диаграммы, а затем каждая из них преобразуется в собственный \[ 0-и 1 \] UV.</span><span class="sxs-lookup"><span data-stu-id="6ccfc-128">First, the mesh is partitioned into charts, then each chart is parameterized into its own \[0,1\] UV-space.</span></span> <span data-ttu-id="6ccfc-129">Цилиндр может быть параметризован одной диаграммой; для сферы с другой стороны потребуется две диаграммы, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="6ccfc-129">A cylinder can be parameterized by one chart; a sphere on the other hand will require two charts, as shown in the following illustration.</span></span>

![Иллюстрация сферы, секционированная на две диаграммы](images/uvatlas3.jpg)

<span data-ttu-id="6ccfc-131">Сетка, которая может быть параметризована с одной диаграммой, классифицируется как «хомеоморфик на диск», что означает, что можно распределить бесконечно гибкое, бесконечное растяжение диска на диаграмме и полностью охватить геометрию.</span><span class="sxs-lookup"><span data-stu-id="6ccfc-131">A mesh which can be parameterized with a single chart is classified as "homeomorphic to a disk", meaning you could spread out an infinitely flexible, infinitely stretchable disk over the chart and cover the geometry perfectly.</span></span> <span data-ttu-id="6ccfc-132">Это растяжение, называемое хомеоморфисм, является двунаправленной функцией. Это означает, что можно переходить от одной параметризации к другой без потери информации.</span><span class="sxs-lookup"><span data-stu-id="6ccfc-132">This stretching, called a homeomorphism, is a bidirectional function; which means you can go from one parameterization to the other without losing information.</span></span>

<span data-ttu-id="6ccfc-133">Очень мало реальных сеток можно разделить на два измерения, не разделив сетку на кластеры или диаграммы.</span><span class="sxs-lookup"><span data-stu-id="6ccfc-133">Very few real-world meshes can be parameterized into two dimensions without separating the mesh into clusters, or charts.</span></span> <span data-ttu-id="6ccfc-134">На следующем рисунке показан другой пример сетки и соответствующая текстура Atlas.</span><span class="sxs-lookup"><span data-stu-id="6ccfc-134">The following illustration shows another example mesh and its corresponding texture atlas.</span></span>

![Показывает пример сетки с различными фигурами и соответствующей текстурой Atlas.](images/uvatlas2.jpg)

<span data-ttu-id="6ccfc-136">Число создаваемых диаграмм определяется двумя параметрами:</span><span class="sxs-lookup"><span data-stu-id="6ccfc-136">There are two parameters that determine the number of charts created:</span></span>

-   <span data-ttu-id="6ccfc-137">Максимальное число диаграмм, разрешенное для Atlas</span><span class="sxs-lookup"><span data-stu-id="6ccfc-137">The maximum number of charts allowed for the atlas</span></span>
-   <span data-ttu-id="6ccfc-138">Максимальный размер растяжения, разрешенный для каждой диаграммы</span><span class="sxs-lookup"><span data-stu-id="6ccfc-138">The maximum amount of stretch allowed for each chart</span></span>

<span data-ttu-id="6ccfc-139">Степень растяжения определит количество создаваемых диаграмм и общее качество выборки.</span><span class="sxs-lookup"><span data-stu-id="6ccfc-139">The amount of stretch will determine the number of charts that are generated, and the overall quality of the sampling.</span></span> <span data-ttu-id="6ccfc-140">Растяжение диапазонов от 0,0 (без растяжения) до 1,0 (любой размер растяжения).</span><span class="sxs-lookup"><span data-stu-id="6ccfc-140">Stretch ranges from 0.0 (no stretch) to 1.0 (any amount of stretch).</span></span> <span data-ttu-id="6ccfc-141">D3DXUVAtlasCreate и D3DXUVAtlasPartition возвращают максимальное растяжение, созданное алгоритмом.</span><span class="sxs-lookup"><span data-stu-id="6ccfc-141">D3DXUVAtlasCreate and D3DXUVAtlasPartition return the maximum stretch generated by the algorithm.</span></span> <span data-ttu-id="6ccfc-142">На следующем рисунке показан другой пример сетки и соответствующая текстура Atlas.</span><span class="sxs-lookup"><span data-stu-id="6ccfc-142">The following illustration shows another example mesh and its corresponding texture atlas.</span></span>

![Иллюстрация сетки примера и соответствующей текстуры Atlas](images/uvatlas4.jpg)

### <a name="using-integrated-metric-tensors-to-control-parameterization"></a><span data-ttu-id="6ccfc-144">Использование встроенных десятков метрик для управления параметризации</span><span class="sxs-lookup"><span data-stu-id="6ccfc-144">Using Integrated Metric Tensors to Control Parameterization</span></span>

<span data-ttu-id="6ccfc-145">Приоритет пространства текстуры можно задать для каждого треугольника.</span><span class="sxs-lookup"><span data-stu-id="6ccfc-145">Texture-space prioritization can be specified on a per-triangle basis.</span></span> <span data-ttu-id="6ccfc-146">Для управления растяжением треугольников в результирующем пространстве на основе текстур можно предоставить интегрированные десятки.</span><span class="sxs-lookup"><span data-stu-id="6ccfc-146">Integrated Metric Tensors can be provided to control how triangles are stretched in the resulting texture-space atlas.</span></span> <span data-ttu-id="6ccfc-147">ИМТ можно указать напрямую или вычислить на основе входного сигнала, используя вычислительные функции D3DX ИМТ.</span><span class="sxs-lookup"><span data-stu-id="6ccfc-147">IMT's can be specified directly or computed based on an input signal using the D3DX IMT computation functions.</span></span> <span data-ttu-id="6ccfc-148">Интегрированная метрика тензорные (или ИМТ) — это симметричная матрица 2x2, которая описывает растяжение треугольника в Atlas.</span><span class="sxs-lookup"><span data-stu-id="6ccfc-148">An integrated metric tensor (or IMT) is a symmetrical 2x2 matrix that describes how a triangle is stretched in the atlas.</span></span> <span data-ttu-id="6ccfc-149">Каждый ИМТ определяется 3 плавающей точкой, вызывайте их (a, b, c).</span><span class="sxs-lookup"><span data-stu-id="6ccfc-149">Each IMT is defined by 3 floats, call them (a,b,c).</span></span> <span data-ttu-id="6ccfc-150">Их можно разместить в симметричной матрице 2x2 следующим образом:</span><span class="sxs-lookup"><span data-stu-id="6ccfc-150">They can be arranged in a symmetric 2x2 matrix like this:</span></span>


```
a b
b c
```



<span data-ttu-id="6ccfc-151">Затем ИМТ можно использовать для поиска расстояния между двумя векторами.</span><span class="sxs-lookup"><span data-stu-id="6ccfc-151">Then the IMT can be used to find the distance between two vectors.</span></span> <span data-ttu-id="6ccfc-152">С учетом двух векторов V1 и v2, где:</span><span class="sxs-lookup"><span data-stu-id="6ccfc-152">Given two vectors v1 and v2, where :</span></span>


```
vector v1
vector v2 = v1 + (s,t)
```



<span data-ttu-id="6ccfc-153">Расстояние между v1 и v2 можно вычислить следующим образом:</span><span class="sxs-lookup"><span data-stu-id="6ccfc-153">The distance between v1 and v2 can be calculated as:</span></span>


```
sqrt((s, t) * M * (s, t)^T)
```



<span data-ttu-id="6ccfc-154">Иными словами, векторы (s, t) могут быть величиной растяжения в произвольном направлении в пространстве u-v.</span><span class="sxs-lookup"><span data-stu-id="6ccfc-154">In other words, the vector (s,t) could be the magnitude of the stretch in an arbitrary direction in u-v space.</span></span> <span data-ttu-id="6ccfc-155">В этом случае вектором s является направление от первой к второй вершиной, а t — перекрестное произведение обычных и s.</span><span class="sxs-lookup"><span data-stu-id="6ccfc-155">In this case, the s vector is a direction from the first to the second vertex, and t is the cross product of the normal and s.</span></span> <span data-ttu-id="6ccfc-156">Например:</span><span class="sxs-lookup"><span data-stu-id="6ccfc-156">For instance:</span></span>


```
(1,1) * (1,1) = (2,2)
        (1,1)
IMT(1,1,1) scales by 2
```




```
(1,-1) * (1,1) = (0,0)
         (1,1)
IMT(2,0,2) scales by 2 with no shearing
```



<span data-ttu-id="6ccfc-157">ИМТ можно указать напрямую или вычислить на основе сигнала ввода с помощью вычислительных функций D3DX ИМТ: D3DXComputeIMTFromPerVertexSignal, D3DXComputeIMTFromPerTexelSignal, D3DXComputeIMTFromSignal и D3DXComputeIMTFromTexture \_ Graphics.</span><span class="sxs-lookup"><span data-stu-id="6ccfc-157">IMT's can be specified directly or computed based on an input signal using the D3DX IMT computation functions: D3DXComputeIMTFromPerVertexSignal, D3DXComputeIMTFromPerTexelSignal, D3DXComputeIMTFromSignal, and D3DXComputeIMTFromTexture\_graphics.</span></span>

<span data-ttu-id="6ccfc-158">Укажите данные ИМТ напрямую, если требуется управлять выделением пространства текстуры для отдельных треугольников.</span><span class="sxs-lookup"><span data-stu-id="6ccfc-158">Specify IMT data directly if you want to control how texture-space is allocated to individual triangles.</span></span> <span data-ttu-id="6ccfc-159">Таким образом, выделяйте больше областей в Atlas к важным областям сетки (например, к лицевой части символа или сундука логотипу или областям сцены рядом с прохождением по пути к игроку).</span><span class="sxs-lookup"><span data-stu-id="6ccfc-159">By doing so, allocate more area in the atlas to important areas of a mesh (such as a character's face or chest logo, or regions of a scene near a player's walking-path).</span></span> <span data-ttu-id="6ccfc-160">При указании ИМТ, которые являются кратными матрицы идентификаторов, итоговые треугольники будут равномерно масштабироваться в пространстве текстуры.</span><span class="sxs-lookup"><span data-stu-id="6ccfc-160">By specifying IMT's that are multiples of the identity matrix, the resulting triangles will be scaled uniformly in texture space.</span></span>

<span data-ttu-id="6ccfc-161">Например, при наличии нормального сопоставления с высоким разрешением вы можете вычислить ИМТ, чтобы предоставить больше пространства текстуры для областей с более высокой частотой в обычной карте.</span><span class="sxs-lookup"><span data-stu-id="6ccfc-161">For example, given a high-resolution normal map, you can compute IMT to provide more texture-space to areas of higher frequency signal in the normal map.</span></span> <span data-ttu-id="6ccfc-162">Треугольники «Flat» (которые сопоставлены с областями констант исходной стандартной схемы) будут иметь меньше пространства текстуры.</span><span class="sxs-lookup"><span data-stu-id="6ccfc-162">Triangles that are "flat" (that mapped to constant regions of the original normal map) will receive less texture space.</span></span> <span data-ttu-id="6ccfc-163">Треугольники, которые содержат большую часть сведений о нормальном сопоставлении, получат больше текстурной области в окончательном результате.</span><span class="sxs-lookup"><span data-stu-id="6ccfc-163">Triangles that contain a great deal of normal-map detail will receive more texture area in the final result.</span></span> <span data-ttu-id="6ccfc-164">Затем можно переделать нормальную карту на меньшую текстуру, но сохранить сведения или повторно вычислить нормальную карту с более оптимальным отображением UV.</span><span class="sxs-lookup"><span data-stu-id="6ccfc-164">You can then resample the normal map into a smaller texture but maintain detail, or you can recompute the normal map with the more optimal UV mapping.</span></span>

### <a name="using-adjacency-data-for-user-specified-creases"></a><span data-ttu-id="6ccfc-165">Использование Соседовых данных для указанного пользователем Креасес</span><span class="sxs-lookup"><span data-stu-id="6ccfc-165">Using Adjacency Data for User Specified Creases</span></span>

<span data-ttu-id="6ccfc-166">Определяемые пользователем сведения о соотношении соседей могут быть предоставлены функции секционирования для описания предварительно определенных креасес в сетке и, таким же, определяют границы диаграммы между смежными лицами.</span><span class="sxs-lookup"><span data-stu-id="6ccfc-166">User-defined adjacency information can be provided to the partitioning function to describe pre-defined creases in the mesh, and thus define a chart boundary between adjacent faces.</span></span> <span data-ttu-id="6ccfc-167">Это простой способ, с помощью которого вызывающий объект может указать собственное секционирование диаграммы в качестве входных данных для алгоритма, который будет дополнительно уточнять диаграммы для переноса максимально допустимого значения.</span><span class="sxs-lookup"><span data-stu-id="6ccfc-167">This is a simple way for the caller to specify their own chart partitioning as input into the algorithm, which will further refine charts to bring the stretch under the maximum allowed.</span></span>

### <a name="example"></a><span data-ttu-id="6ccfc-168">Пример</span><span class="sxs-lookup"><span data-stu-id="6ccfc-168">Example</span></span>

<span data-ttu-id="6ccfc-169">В этом примере показано, как можно использовать API Уватлас и средство просмотра DirectX (Dxviewer.exe) для поиска и исправления небесперебойной работы модели, которые могут значительно повлиять на размер текстуры Atlas.</span><span class="sxs-lookup"><span data-stu-id="6ccfc-169">This example illustrates how you might use the UVAtlas APIs and the DirectX Viewer (Dxviewer.exe) to find and fix discontinuities in your model that can dramatically affect the size of your texture atlas.</span></span> <span data-ttu-id="6ccfc-170">Вы можете получить Dxviewer.exe и узнать о нем из пакета SDK DirectX.</span><span class="sxs-lookup"><span data-stu-id="6ccfc-170">You can get Dxviewer.exe and learn about it from the DirectX SDK.</span></span> <span data-ttu-id="6ccfc-171">Dxviewer.exe был удален из пакета SDK DirectX после версии 2009 августа, поэтому для ее получения необходим по крайней мере пакет SDK DirectX за Август 2009.</span><span class="sxs-lookup"><span data-stu-id="6ccfc-171">Dxviewer.exe was removed from the DirectX SDK after the August 2009 version so to get it you'll need at least the August 2009 DirectX SDK.</span></span> <span data-ttu-id="6ccfc-172">Сведения о пакете SDK для DirectX см. в разделе [где находится пакет DirectX SDK?](../directx-sdk--august-2009-.md).</span><span class="sxs-lookup"><span data-stu-id="6ccfc-172">For info about the DirectX SDK, see [Where is the DirectX SDK?](../directx-sdk--august-2009-.md).</span></span>

<span data-ttu-id="6ccfc-173">Предположим, вы начали работу с какой-либо моделью в любимом программном обеспечении для создания содержимого (в этом примере используется Главная модель Dwarf, созданная в Maya).</span><span class="sxs-lookup"><span data-stu-id="6ccfc-173">Assume you started with some model in your favorite content generation software (this example uses a dwarf head model that was created in Maya).</span></span> <span data-ttu-id="6ccfc-174">Экспортируйте текстурированную модель в файл x и создайте текстуру Atlas с помощью D3DXUVAtlasCreate.</span><span class="sxs-lookup"><span data-stu-id="6ccfc-174">Export the textured model to an .x file and create a texture atlas with D3DXUVAtlasCreate.</span></span> <span data-ttu-id="6ccfc-175">Полученная текстура Atlas будет выглядеть примерно так, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="6ccfc-175">The resulting texture atlas would look something like the following illustration.</span></span>

![Иллюстрация Atlas для модели dwarf](images/uvatlas5.jpg)

<span data-ttu-id="6ccfc-177">Atlas имеет 22 диаграммы и максимальный растяжение 0,994.</span><span class="sxs-lookup"><span data-stu-id="6ccfc-177">The atlas has 22 charts and a maximum stretch of 0.994.</span></span>

<span data-ttu-id="6ccfc-178">Теперь взгляните на текстурную модель, чтобы увидеть, насколько хорошо текстура Atlas сопоставляется с геометрическим объектом.</span><span class="sxs-lookup"><span data-stu-id="6ccfc-178">Now look at the textured model to see how well the texture atlas maps to the geometry.</span></span> <span data-ttu-id="6ccfc-179">Для этого загрузите модель в средство просмотра:</span><span class="sxs-lookup"><span data-stu-id="6ccfc-179">To do this, load the model into the viewer tool:</span></span>

-   <span data-ttu-id="6ccfc-180">Откройте средство просмотра из служебных программ DirectX.</span><span class="sxs-lookup"><span data-stu-id="6ccfc-180">Open the viewer tool from the DirectX Utilities.</span></span>
-   <span data-ttu-id="6ccfc-181">Загрузите файл. x, нажав кнопку Открыть.</span><span class="sxs-lookup"><span data-stu-id="6ccfc-181">Load the .x file by clicking the Open button.</span></span>
-   <span data-ttu-id="6ccfc-182">Чтобы включить параметр просмотра величить, нажмите кнопку вид и выберите Креасес из всплывающего окна.</span><span class="sxs-lookup"><span data-stu-id="6ccfc-182">Enabling the crease viewing option by clicking the view button and selecting Creases from popup.</span></span>

<span data-ttu-id="6ccfc-183">На следующем рисунке показано, что должно отображаться в средстве просмотра.</span><span class="sxs-lookup"><span data-stu-id="6ccfc-183">The following illustration shows what you should see in the viewer tool.</span></span>

![Иллюстрация текстурированной сетки в средстве просмотра](images/uvatlas6c.jpg)

<span data-ttu-id="6ccfc-185">Каждая строка представляет собой величить, который является смежным ребром между двумя диаграммами в текстуре Atlas.</span><span class="sxs-lookup"><span data-stu-id="6ccfc-185">Each line is a crease which is an adjacent edge between two charts in the texture atlas.</span></span> <span data-ttu-id="6ccfc-186">Число диаграмм, созданных алгоритмом, вызвано незначительными различиями, возможно, из-за ненепрерывности нормальной работы.</span><span class="sxs-lookup"><span data-stu-id="6ccfc-186">The number of charts generated by the algorithm is caused by slight differences perhaps due to discontinuities in the normals.</span></span> <span data-ttu-id="6ccfc-187">Эти небольшие различия можно сократить, Велдинг данные, то есть заставляя данные, которые почти равны.</span><span class="sxs-lookup"><span data-stu-id="6ccfc-187">These small differences can be reduced by welding data, that is, forcing data that is nearly equal to be equal.</span></span> <span data-ttu-id="6ccfc-188">Чтобы расшва нормали и скинвеигхтс, сделайте следующее:</span><span class="sxs-lookup"><span data-stu-id="6ccfc-188">To weld the normals and the skinweights:</span></span>

-   <span data-ttu-id="6ccfc-189">Запустите средство DirectX Ops (dxops.exe) со следующей командной строкой в сетке (замените "modelName. x" на имя модели):</span><span class="sxs-lookup"><span data-stu-id="6ccfc-189">Run the DirectX Ops (dxops.exe) tool with the following command line on the mesh (replacing 'modelName.x' with the name of your model):</span></span>
    ```
    Dxops.exe -s "load 'modelName.x'; Optimize n:2.01 w:2.01 uv0:0.01;  save 'newModelName.x';"
    ```

    

<span data-ttu-id="6ccfc-190">Это сравнение обычных и скинвеигхтс и того, где они отличаются в значении меньшим, чем 2,01, данные становятся равными.</span><span class="sxs-lookup"><span data-stu-id="6ccfc-190">This compares the normals and skinweights, and where they differ in value by less than 2.01, the data is made equal.</span></span> <span data-ttu-id="6ccfc-191">На следующих иллюстрациях показано, как можно увидеть креасес перед Велдинг (слева) и креасес после Велдинг (справа):</span><span class="sxs-lookup"><span data-stu-id="6ccfc-191">The following illustrations shows a close up of the eye to see the creases before welding (on the left) and the creases after welding (on the right):</span></span>

![Иллюстрация креасес перед Велдинг](images/uvatlas6a.jpg)![Иллюстрация креасес после Велдинг](images/uvatlas6b.jpg)

<span data-ttu-id="6ccfc-194">Рис. 7. Удаление креасес by Велдинг</span><span class="sxs-lookup"><span data-stu-id="6ccfc-194">Figure 7: Removing creases by welding</span></span>

<span data-ttu-id="6ccfc-195">В этом примере Велдинг удалили 86 вершин из входной сетки.</span><span class="sxs-lookup"><span data-stu-id="6ccfc-195">In this example, welding removed 86 vertices from the input mesh.</span></span> <span data-ttu-id="6ccfc-196">Если в сетке меньше креасес, можно повторно создать Atlas, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="6ccfc-196">With fewer creases in the mesh, you can regenerate the atlas, as the following illustration shows.</span></span>

![Иллюстрация новой Atlas с удаленным креасес](images/uvatlas8.jpg)

<span data-ttu-id="6ccfc-198">Atlas содержит только 7 диаграмм и максимальный растяжение приблизительно 0,0776.</span><span class="sxs-lookup"><span data-stu-id="6ccfc-198">The atlas only has 7 charts and a maximum stretch of approximately 0.0776.</span></span> <span data-ttu-id="6ccfc-199">Новая Atlas теперь занимает меньшую текстуру (в этом примере приблизительно 30% меньше).</span><span class="sxs-lookup"><span data-stu-id="6ccfc-199">The new atlas now fits into a smaller texture (approximately 30% smaller in this example).</span></span>

### <a name="packing-charts-into-an-atlas"></a><span data-ttu-id="6ccfc-200">Упаковка диаграмм в Atlas</span><span class="sxs-lookup"><span data-stu-id="6ccfc-200">Packing Charts Into an Atlas</span></span>

<span data-ttu-id="6ccfc-201">После разделения сетки на отдельные параметризованные диаграммы необходимо эффективно упаковывать диаграммы в одну текстурную карту.</span><span class="sxs-lookup"><span data-stu-id="6ccfc-201">Once a mesh has been partitioned into individually-parameterized charts, the charts need to be packed efficiently into a single texture map.</span></span> <span data-ttu-id="6ccfc-202">Это выполняется в качестве второго шага D3DXUVAtlasCreate или может быть вызвано явным образом путем вызова D3DXUVAtlasPack.</span><span class="sxs-lookup"><span data-stu-id="6ccfc-202">This is performed as the second step of D3DXUVAtlasCreate or can be invoked explicitly by calling D3DXUVAtlasPack.</span></span>

<span data-ttu-id="6ccfc-203">Упакованные диаграммы разделяются заданной пользователем шириной переплета.</span><span class="sxs-lookup"><span data-stu-id="6ccfc-203">Packed charts are separated by a user-specified gutter width.</span></span> <span data-ttu-id="6ccfc-204">Ширина переплета — это величина разделения между диаграммами, позволяющая билинейной интерполяцию и MIP-сопоставление, чтобы избежать артефактов отрисовки на границах диаграммы.</span><span class="sxs-lookup"><span data-stu-id="6ccfc-204">The gutter width is the amount of separation between charts, and allows for bilinear interpolation and mip-mapping to avoid rendering artifacts at chart boundaries.</span></span> <span data-ttu-id="6ccfc-205">D3DX предоставляет интерфейс для автоматического заполнения этих переплетов. Дополнительные сведения см. в разделе [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) .</span><span class="sxs-lookup"><span data-stu-id="6ccfc-205">D3DX provides an interface for automatically filling in these gutters - see [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) for more information.</span></span>

## <a name="integrating-uvatlas-into-your-pipeline"></a><span data-ttu-id="6ccfc-206">Интеграция Уватлас в конвейер</span><span class="sxs-lookup"><span data-stu-id="6ccfc-206">Integrating UVAtlas Into Your Pipeline</span></span>

<span data-ttu-id="6ccfc-207">Помимо прорисовки текстур, эти функции можно интегрировать в автоматизированный конвейер.</span><span class="sxs-lookup"><span data-stu-id="6ccfc-207">In addition to being artist-invoked prior to texture painting, these functions can be integrated into an automated art pipeline.</span></span> <span data-ttu-id="6ccfc-208">Например, вызов Уватлас может быть выдан автоматически после обновления ресурса до выполнения PRT моделирования или нормального сопоставления.</span><span class="sxs-lookup"><span data-stu-id="6ccfc-208">For example, a UVAtlas call can be issued automatically after an asset is updated, prior to performing a PRT simulation or normal mapping pass.</span></span> <span data-ttu-id="6ccfc-209">Это позволяет избежать необходимости вручную ручного восстановления UV, если топология сетки была изменена.</span><span class="sxs-lookup"><span data-stu-id="6ccfc-209">This avoids any need to manually manual repair of an object's UV mapping if the mesh's topology has been modified.</span></span>

<span data-ttu-id="6ccfc-210">Пример использования функций Уватлас см. в разделе [инструмент UV Atlas Command-Line (uvatlas.exe)](https://msdn.microsoft.com/library/Ee419017(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="6ccfc-210">See the [UV Atlas Command-Line Tool (uvatlas.exe)](https://msdn.microsoft.com/library/Ee419017(v=VS.85).aspx) for example usage of the UVAtlas functions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6ccfc-211">См. также</span><span class="sxs-lookup"><span data-stu-id="6ccfc-211">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6ccfc-212">Дополнительные разделы</span><span class="sxs-lookup"><span data-stu-id="6ccfc-212">Advanced Topics</span></span>](advanced-topics.md)
</dt> </dl>

 

 
