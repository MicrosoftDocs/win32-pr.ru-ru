---
description: Для многих методов отрисовки и создания содержимого требуется уникальная, непересекающаяся схема 2D-сигнала (например, текстура) на сетке.
ms.assetid: 0ec19e8c-2a14-4392-93de-7ab832784085
title: Использование Уватлас (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8faeaa0a416f6f062c81c4101ff47d5222ca75d
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/09/2021
ms.locfileid: "111826332"
---
# <a name="using-uvatlas-direct3d-9"></a><span data-ttu-id="9ff18-103">Использование Уватлас (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="9ff18-103">Using UVAtlas (Direct3D 9)</span></span>

> [!NOTE]
> <span data-ttu-id="9ff18-104">Изначально Уватлас была поставлена в библиотеку утилти D3DX9.</span><span class="sxs-lookup"><span data-stu-id="9ff18-104">UVAtlas was originally shipped in the now-deprecated D3DX9 utilty library.</span></span> <span data-ttu-id="9ff18-105">Последняя версия доступна на странице [UV Atlas Command-Line Tool (uvatlas.exe)](https://github.com/Microsoft/UVAtlas).</span><span class="sxs-lookup"><span data-stu-id="9ff18-105">The latest version is available at [UV Atlas Command-Line Tool (uvatlas.exe)](https://github.com/Microsoft/UVAtlas).</span></span>

<span data-ttu-id="9ff18-106">Для многих методов отрисовки и создания содержимого требуется уникальная, непересекающаяся схема 2D-сигнала (например, текстура) на сетке.</span><span class="sxs-lookup"><span data-stu-id="9ff18-106">Many rendering and content generation techniques require a unique, non-overlapping map of a 2D signal (such as a texture) onto a mesh.</span></span> <span data-ttu-id="9ff18-107">К таким методам относятся:</span><span class="sxs-lookup"><span data-stu-id="9ff18-107">Such techniques include:</span></span>

-   <span data-ttu-id="9ff18-108">Сопоставление обычного и среднего смещения</span><span class="sxs-lookup"><span data-stu-id="9ff18-108">Normal/displacement mapping</span></span>
-   <span data-ttu-id="9ff18-109">Имитация PRTа текстуры и схемы освещения</span><span class="sxs-lookup"><span data-stu-id="9ff18-109">Texture-space PRT simulations and light maps</span></span>
-   <span data-ttu-id="9ff18-110">Рисование поверхности</span><span class="sxs-lookup"><span data-stu-id="9ff18-110">Surface painting</span></span>
-   <span data-ttu-id="9ff18-111">Освещение-пространство текстуры</span><span class="sxs-lookup"><span data-stu-id="9ff18-111">Texture-space lighting</span></span>

<span data-ttu-id="9ff18-112">Создание уникального UV-сопоставления вручную часто занимает много времени и утомительно; Это особенно важно, когда входная геометрическая фигура является сложной и эффективной или низкой интенсивностью использования пространства текстуры.</span><span class="sxs-lookup"><span data-stu-id="9ff18-112">Generating a unique UV mapping manually is often time-consuming and tedious; this is especially true when the input geometry is complex and efficient/low-distortion texture-space utilization is desired.</span></span> <span data-ttu-id="9ff18-113">На следующем рисунке показан пример сетки и соответствующая текстура Atlas.</span><span class="sxs-lookup"><span data-stu-id="9ff18-113">The following illustration shows an example mesh and its corresponding texture atlas.</span></span>

![Показывает пример сетки и соответствующую текстуру Atlas.](images/uvatlas1.jpg)

<span data-ttu-id="9ff18-115">В этом примере показана сетка слева и соответствующая нормальная схема UV-Space (справа).</span><span class="sxs-lookup"><span data-stu-id="9ff18-115">This example shows a mesh (on the left) and the corresponding UV-space normal map (on the right).</span></span> <span data-ttu-id="9ff18-116">Обратите внимание, что текстура Atlas содержит несколько групп или кластеров данных. Каждый кластер называется диаграммой и в приведенном выше примере отображает обычные данные для части сетки.</span><span class="sxs-lookup"><span data-stu-id="9ff18-116">Notice that the texture atlas contains several groups or clusters of data; each cluster is called a chart and in the example above, displays contains the normal data for a portion of the mesh.</span></span>

<span data-ttu-id="9ff18-117">API-интерфейсы D3DX Уватлас автоматически создают оптимальную, не пересекающую текстуру Atlas.</span><span class="sxs-lookup"><span data-stu-id="9ff18-117">The D3DX UVAtlas APIs automatically generate an optimal, non-overlapping texture atlas.</span></span> <span data-ttu-id="9ff18-118">Интерфейсы API предоставляют входные параметры, позволяющие:</span><span class="sxs-lookup"><span data-stu-id="9ff18-118">The APIs provide input parameters that allow you to:</span></span>

-   <span data-ttu-id="9ff18-119">Уменьшение растяжения, искажения и недовыборки текстур.</span><span class="sxs-lookup"><span data-stu-id="9ff18-119">Minimize texture stretch, distortion, and undersampling.</span></span>
-   <span data-ttu-id="9ff18-120">Максимальная плотность упаковки пространства текстуры для эффективного использования памяти.</span><span class="sxs-lookup"><span data-stu-id="9ff18-120">Maximize texture-space packing density for efficient use of memory.</span></span>
-   <span data-ttu-id="9ff18-121">Предоставьте одинаковую выборку по сети, уменьшая непрерывность при частоте выборки.</span><span class="sxs-lookup"><span data-stu-id="9ff18-121">Provide an even sampling across the mesh, minimizing discontinuities in sampling frequency.</span></span>

## <a name="how-uvatlas-works"></a><span data-ttu-id="9ff18-122">Как работает Уватлас</span><span class="sxs-lookup"><span data-stu-id="9ff18-122">How UVAtlas Works</span></span>

<span data-ttu-id="9ff18-123">API-интерфейсы Уватлас (см. раздел [функции уватлас](dx9-graphics-reference-d3dx-functions-uvatlas.md)) создают текстуру Atlas, выключая поверхность на диаграммах и упаковку диаграмм в текстуру Atlas.</span><span class="sxs-lookup"><span data-stu-id="9ff18-123">The UVAtlas APIs (see [UVAtlas Functions](dx9-graphics-reference-d3dx-functions-uvatlas.md)) generate a texture atlas by partitioning a surface into charts and packing the charts into a texture atlas.</span></span> <span data-ttu-id="9ff18-124">Используйте [**D3DXUVAtlasPartition**](d3dxuvatlaspartition.md) и [**D3DXUVAtlasPack**](d3dxuvatlaspack.md) для выполнения этих действий отдельно. или используйте [**D3DXUVAtlasCreate**](d3dxuvatlascreate.md) для секционирования, параметризации и упаковки в одном вызове.</span><span class="sxs-lookup"><span data-stu-id="9ff18-124">Use [**D3DXUVAtlasPartition**](d3dxuvatlaspartition.md) and [**D3DXUVAtlasPack**](d3dxuvatlaspack.md) to perform these steps separately; or use [**D3DXUVAtlasCreate**](d3dxuvatlascreate.md) to partition, parameterize and pack in a single call.</span></span>

-   [<span data-ttu-id="9ff18-125">Секционирование и параметризация сетки</span><span class="sxs-lookup"><span data-stu-id="9ff18-125">Partitioning and Parameterizing a Mesh</span></span>](#partitioning-and-parameterizing-a-mesh)
-   [<span data-ttu-id="9ff18-126">Использование встроенных десятков метрик для управления параметризации</span><span class="sxs-lookup"><span data-stu-id="9ff18-126">Using Integrated Metric Tensors to Control Parameterization</span></span>](#using-integrated-metric-tensors-to-control-parameterization)
-   [<span data-ttu-id="9ff18-127">Использование Соседовых данных для указанного пользователем Креасес</span><span class="sxs-lookup"><span data-stu-id="9ff18-127">Using Adjacency Data for User Specified Creases</span></span>](#using-adjacency-data-for-user-specified-creases)
-   [<span data-ttu-id="9ff18-128">Упаковка диаграмм в Atlas</span><span class="sxs-lookup"><span data-stu-id="9ff18-128">Packing Charts Into an Atlas</span></span>](#packing-charts-into-an-atlas)

### <a name="partitioning-and-parameterizing-a-mesh"></a><span data-ttu-id="9ff18-129">Секционирование и параметризация сетки</span><span class="sxs-lookup"><span data-stu-id="9ff18-129">Partitioning and Parameterizing a Mesh</span></span>

<span data-ttu-id="9ff18-130">Во-первых, сетка разделяется на диаграммы, а затем каждая из них преобразуется в собственный \[ 0-и 1 \] UV.</span><span class="sxs-lookup"><span data-stu-id="9ff18-130">First, the mesh is partitioned into charts, then each chart is parameterized into its own \[0,1\] UV-space.</span></span> <span data-ttu-id="9ff18-131">Цилиндр может быть параметризован одной диаграммой; для сферы с другой стороны потребуется две диаграммы, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="9ff18-131">A cylinder can be parameterized by one chart; a sphere on the other hand will require two charts, as shown in the following illustration.</span></span>

![Иллюстрация сферы, секционированная на две диаграммы](images/uvatlas3.jpg)

<span data-ttu-id="9ff18-133">Сетка, которая может быть параметризована с одной диаграммой, классифицируется как «хомеоморфик на диск», что означает, что можно распределить бесконечно гибкое, бесконечное растяжение диска на диаграмме и полностью охватить геометрию.</span><span class="sxs-lookup"><span data-stu-id="9ff18-133">A mesh which can be parameterized with a single chart is classified as "homeomorphic to a disk", meaning you could spread out an infinitely flexible, infinitely stretchable disk over the chart and cover the geometry perfectly.</span></span> <span data-ttu-id="9ff18-134">Это растяжение, называемое хомеоморфисм, является двунаправленной функцией. Это означает, что можно переходить от одной параметризации к другой без потери информации.</span><span class="sxs-lookup"><span data-stu-id="9ff18-134">This stretching, called a homeomorphism, is a bidirectional function; which means you can go from one parameterization to the other without losing information.</span></span>

<span data-ttu-id="9ff18-135">Очень мало реальных сеток можно разделить на два измерения, не разделив сетку на кластеры или диаграммы.</span><span class="sxs-lookup"><span data-stu-id="9ff18-135">Very few real-world meshes can be parameterized into two dimensions without separating the mesh into clusters, or charts.</span></span> <span data-ttu-id="9ff18-136">На следующем рисунке показан другой пример сетки и соответствующая текстура Atlas.</span><span class="sxs-lookup"><span data-stu-id="9ff18-136">The following illustration shows another example mesh and its corresponding texture atlas.</span></span>

![Показывает пример сетки с различными фигурами и соответствующей текстурой Atlas.](images/uvatlas2.jpg)

<span data-ttu-id="9ff18-138">Число создаваемых диаграмм определяется двумя параметрами:</span><span class="sxs-lookup"><span data-stu-id="9ff18-138">There are two parameters that determine the number of charts created:</span></span>

-   <span data-ttu-id="9ff18-139">Максимальное число диаграмм, разрешенное для Atlas</span><span class="sxs-lookup"><span data-stu-id="9ff18-139">The maximum number of charts allowed for the atlas</span></span>
-   <span data-ttu-id="9ff18-140">Максимальный размер растяжения, разрешенный для каждой диаграммы</span><span class="sxs-lookup"><span data-stu-id="9ff18-140">The maximum amount of stretch allowed for each chart</span></span>

<span data-ttu-id="9ff18-141">Степень растяжения определит количество создаваемых диаграмм и общее качество выборки.</span><span class="sxs-lookup"><span data-stu-id="9ff18-141">The amount of stretch will determine the number of charts that are generated, and the overall quality of the sampling.</span></span> <span data-ttu-id="9ff18-142">Растяжение диапазонов от 0,0 (без растяжения) до 1,0 (любой размер растяжения).</span><span class="sxs-lookup"><span data-stu-id="9ff18-142">Stretch ranges from 0.0 (no stretch) to 1.0 (any amount of stretch).</span></span> <span data-ttu-id="9ff18-143">D3DXUVAtlasCreate и D3DXUVAtlasPartition возвращают максимальное растяжение, созданное алгоритмом.</span><span class="sxs-lookup"><span data-stu-id="9ff18-143">D3DXUVAtlasCreate and D3DXUVAtlasPartition return the maximum stretch generated by the algorithm.</span></span> <span data-ttu-id="9ff18-144">На следующем рисунке показан другой пример сетки и соответствующая текстура Atlas.</span><span class="sxs-lookup"><span data-stu-id="9ff18-144">The following illustration shows another example mesh and its corresponding texture atlas.</span></span>

![Иллюстрация сетки примера и соответствующей текстуры Atlas](images/uvatlas4.jpg)

### <a name="using-integrated-metric-tensors-to-control-parameterization"></a><span data-ttu-id="9ff18-146">Использование встроенных десятков метрик для управления параметризации</span><span class="sxs-lookup"><span data-stu-id="9ff18-146">Using Integrated Metric Tensors to Control Parameterization</span></span>

<span data-ttu-id="9ff18-147">Приоритет пространства текстуры можно задать для каждого треугольника.</span><span class="sxs-lookup"><span data-stu-id="9ff18-147">Texture-space prioritization can be specified on a per-triangle basis.</span></span> <span data-ttu-id="9ff18-148">Для управления растяжением треугольников в результирующем пространстве на основе текстур можно предоставить интегрированные десятки.</span><span class="sxs-lookup"><span data-stu-id="9ff18-148">Integrated Metric Tensors can be provided to control how triangles are stretched in the resulting texture-space atlas.</span></span> <span data-ttu-id="9ff18-149">ИМТ можно указать напрямую или вычислить на основе входного сигнала, используя вычислительные функции D3DX ИМТ.</span><span class="sxs-lookup"><span data-stu-id="9ff18-149">IMT's can be specified directly or computed based on an input signal using the D3DX IMT computation functions.</span></span> <span data-ttu-id="9ff18-150">Интегрированная метрика тензорные (или ИМТ) — это симметричная матрица 2x2, которая описывает растяжение треугольника в Atlas.</span><span class="sxs-lookup"><span data-stu-id="9ff18-150">An integrated metric tensor (or IMT) is a symmetrical 2x2 matrix that describes how a triangle is stretched in the atlas.</span></span> <span data-ttu-id="9ff18-151">Каждый ИМТ определяется 3 плавающей точкой, вызывайте их (a, b, c).</span><span class="sxs-lookup"><span data-stu-id="9ff18-151">Each IMT is defined by 3 floats, call them (a,b,c).</span></span> <span data-ttu-id="9ff18-152">Их можно разместить в симметричной матрице 2x2 следующим образом:</span><span class="sxs-lookup"><span data-stu-id="9ff18-152">They can be arranged in a symmetric 2x2 matrix like this:</span></span>


```
a b
b c
```



<span data-ttu-id="9ff18-153">Затем ИМТ можно использовать для поиска расстояния между двумя векторами.</span><span class="sxs-lookup"><span data-stu-id="9ff18-153">Then the IMT can be used to find the distance between two vectors.</span></span> <span data-ttu-id="9ff18-154">С учетом двух векторов V1 и v2, где:</span><span class="sxs-lookup"><span data-stu-id="9ff18-154">Given two vectors v1 and v2, where :</span></span>


```
vector v1
vector v2 = v1 + (s,t)
```



<span data-ttu-id="9ff18-155">Расстояние между v1 и v2 можно вычислить следующим образом:</span><span class="sxs-lookup"><span data-stu-id="9ff18-155">The distance between v1 and v2 can be calculated as:</span></span>


```
sqrt((s, t) * M * (s, t)^T)
```



<span data-ttu-id="9ff18-156">Иными словами, векторы (s, t) могут быть величиной растяжения в произвольном направлении в пространстве u-v.</span><span class="sxs-lookup"><span data-stu-id="9ff18-156">In other words, the vector (s,t) could be the magnitude of the stretch in an arbitrary direction in u-v space.</span></span> <span data-ttu-id="9ff18-157">В этом случае вектором s является направление от первой к второй вершиной, а t — перекрестное произведение обычных и s.</span><span class="sxs-lookup"><span data-stu-id="9ff18-157">In this case, the s vector is a direction from the first to the second vertex, and t is the cross product of the normal and s.</span></span> <span data-ttu-id="9ff18-158">Например:</span><span class="sxs-lookup"><span data-stu-id="9ff18-158">For instance:</span></span>


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



<span data-ttu-id="9ff18-159">ИМТ можно указать напрямую или вычислить на основе сигнала ввода с помощью вычислительных функций D3DX ИМТ: D3DXComputeIMTFromPerVertexSignal, D3DXComputeIMTFromPerTexelSignal, D3DXComputeIMTFromSignal и D3DXComputeIMTFromTexture \_ Graphics.</span><span class="sxs-lookup"><span data-stu-id="9ff18-159">IMT's can be specified directly or computed based on an input signal using the D3DX IMT computation functions: D3DXComputeIMTFromPerVertexSignal, D3DXComputeIMTFromPerTexelSignal, D3DXComputeIMTFromSignal, and D3DXComputeIMTFromTexture\_graphics.</span></span>

<span data-ttu-id="9ff18-160">Укажите данные ИМТ напрямую, если требуется управлять выделением пространства текстуры для отдельных треугольников.</span><span class="sxs-lookup"><span data-stu-id="9ff18-160">Specify IMT data directly if you want to control how texture-space is allocated to individual triangles.</span></span> <span data-ttu-id="9ff18-161">Таким образом, выделяйте больше областей в Atlas к важным областям сетки (например, к лицевой части символа или сундука логотипу или областям сцены рядом с прохождением по пути к игроку).</span><span class="sxs-lookup"><span data-stu-id="9ff18-161">By doing so, allocate more area in the atlas to important areas of a mesh (such as a character's face or chest logo, or regions of a scene near a player's walking-path).</span></span> <span data-ttu-id="9ff18-162">При указании ИМТ, которые являются кратными матрицы идентификаторов, итоговые треугольники будут равномерно масштабироваться в пространстве текстуры.</span><span class="sxs-lookup"><span data-stu-id="9ff18-162">By specifying IMT's that are multiples of the identity matrix, the resulting triangles will be scaled uniformly in texture space.</span></span>

<span data-ttu-id="9ff18-163">Например, при наличии нормального сопоставления с высоким разрешением вы можете вычислить ИМТ, чтобы предоставить больше пространства текстуры для областей с более высокой частотой в обычной карте.</span><span class="sxs-lookup"><span data-stu-id="9ff18-163">For example, given a high-resolution normal map, you can compute IMT to provide more texture-space to areas of higher frequency signal in the normal map.</span></span> <span data-ttu-id="9ff18-164">Треугольники «Flat» (которые сопоставлены с областями констант исходной стандартной схемы) будут иметь меньше пространства текстуры.</span><span class="sxs-lookup"><span data-stu-id="9ff18-164">Triangles that are "flat" (that mapped to constant regions of the original normal map) will receive less texture space.</span></span> <span data-ttu-id="9ff18-165">Треугольники, которые содержат большую часть сведений о нормальном сопоставлении, получат больше текстурной области в окончательном результате.</span><span class="sxs-lookup"><span data-stu-id="9ff18-165">Triangles that contain a great deal of normal-map detail will receive more texture area in the final result.</span></span> <span data-ttu-id="9ff18-166">Затем можно переделать нормальную карту на меньшую текстуру, но сохранить сведения или повторно вычислить нормальную карту с более оптимальным отображением UV.</span><span class="sxs-lookup"><span data-stu-id="9ff18-166">You can then resample the normal map into a smaller texture but maintain detail, or you can recompute the normal map with the more optimal UV mapping.</span></span>

### <a name="using-adjacency-data-for-user-specified-creases"></a><span data-ttu-id="9ff18-167">Использование Соседовых данных для указанного пользователем Креасес</span><span class="sxs-lookup"><span data-stu-id="9ff18-167">Using Adjacency Data for User Specified Creases</span></span>

<span data-ttu-id="9ff18-168">Определяемые пользователем сведения о соотношении соседей могут быть предоставлены функции секционирования для описания предварительно определенных креасес в сетке и, таким же, определяют границы диаграммы между смежными лицами.</span><span class="sxs-lookup"><span data-stu-id="9ff18-168">User-defined adjacency information can be provided to the partitioning function to describe pre-defined creases in the mesh, and thus define a chart boundary between adjacent faces.</span></span> <span data-ttu-id="9ff18-169">Это простой способ, с помощью которого вызывающий объект может указать собственное секционирование диаграммы в качестве входных данных для алгоритма, который будет дополнительно уточнять диаграммы для переноса максимально допустимого значения.</span><span class="sxs-lookup"><span data-stu-id="9ff18-169">This is a simple way for the caller to specify their own chart partitioning as input into the algorithm, which will further refine charts to bring the stretch under the maximum allowed.</span></span>

### <a name="example"></a><span data-ttu-id="9ff18-170">Пример</span><span class="sxs-lookup"><span data-stu-id="9ff18-170">Example</span></span>

<span data-ttu-id="9ff18-171">В этом примере показано, как можно использовать API Уватлас и средство просмотра DirectX (Dxviewer.exe) для поиска и исправления небесперебойной работы модели, которые могут значительно повлиять на размер текстуры Atlas.</span><span class="sxs-lookup"><span data-stu-id="9ff18-171">This example illustrates how you might use the UVAtlas APIs and the DirectX Viewer (Dxviewer.exe) to find and fix discontinuities in your model that can dramatically affect the size of your texture atlas.</span></span> <span data-ttu-id="9ff18-172">Вы можете получить Dxviewer.exe и узнать о нем из пакета SDK DirectX.</span><span class="sxs-lookup"><span data-stu-id="9ff18-172">You can get Dxviewer.exe and learn about it from the DirectX SDK.</span></span> <span data-ttu-id="9ff18-173">Dxviewer.exe был удален из пакета SDK DirectX после версии 2009 августа, поэтому для ее получения необходим по крайней мере пакет SDK DirectX за Август 2009.</span><span class="sxs-lookup"><span data-stu-id="9ff18-173">Dxviewer.exe was removed from the DirectX SDK after the August 2009 version so to get it you'll need at least the August 2009 DirectX SDK.</span></span> <span data-ttu-id="9ff18-174">Сведения о пакете SDK для DirectX см. в разделе [где находится пакет DirectX SDK?](../directx-sdk--august-2009-.md).</span><span class="sxs-lookup"><span data-stu-id="9ff18-174">For info about the DirectX SDK, see [Where is the DirectX SDK?](../directx-sdk--august-2009-.md).</span></span>

<span data-ttu-id="9ff18-175">Предположим, вы начали работу с какой-либо моделью в любимом программном обеспечении для создания содержимого (в этом примере используется Главная модель Dwarf, созданная в Maya).</span><span class="sxs-lookup"><span data-stu-id="9ff18-175">Assume you started with some model in your favorite content generation software (this example uses a dwarf head model that was created in Maya).</span></span> <span data-ttu-id="9ff18-176">Экспортируйте текстурированную модель в файл x и создайте текстуру Atlas с помощью D3DXUVAtlasCreate.</span><span class="sxs-lookup"><span data-stu-id="9ff18-176">Export the textured model to an .x file and create a texture atlas with D3DXUVAtlasCreate.</span></span> <span data-ttu-id="9ff18-177">Полученная текстура Atlas будет выглядеть примерно так, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="9ff18-177">The resulting texture atlas would look something like the following illustration.</span></span>

![Иллюстрация Atlas для модели dwarf](images/uvatlas5.jpg)

<span data-ttu-id="9ff18-179">Atlas имеет 22 диаграммы и максимальный растяжение 0,994.</span><span class="sxs-lookup"><span data-stu-id="9ff18-179">The atlas has 22 charts and a maximum stretch of 0.994.</span></span>

<span data-ttu-id="9ff18-180">Теперь взгляните на текстурную модель, чтобы увидеть, насколько хорошо текстура Atlas сопоставляется с геометрическим объектом.</span><span class="sxs-lookup"><span data-stu-id="9ff18-180">Now look at the textured model to see how well the texture atlas maps to the geometry.</span></span> <span data-ttu-id="9ff18-181">Для этого загрузите модель в средство просмотра:</span><span class="sxs-lookup"><span data-stu-id="9ff18-181">To do this, load the model into the viewer tool:</span></span>

-   <span data-ttu-id="9ff18-182">Откройте средство просмотра из служебных программ DirectX.</span><span class="sxs-lookup"><span data-stu-id="9ff18-182">Open the viewer tool from the DirectX Utilities.</span></span>
-   <span data-ttu-id="9ff18-183">Загрузите файл. x, нажав кнопку Открыть.</span><span class="sxs-lookup"><span data-stu-id="9ff18-183">Load the .x file by clicking the Open button.</span></span>
-   <span data-ttu-id="9ff18-184">Чтобы включить параметр просмотра величить, нажмите кнопку вид и выберите Креасес из всплывающего окна.</span><span class="sxs-lookup"><span data-stu-id="9ff18-184">Enabling the crease viewing option by clicking the view button and selecting Creases from popup.</span></span>

<span data-ttu-id="9ff18-185">На следующем рисунке показано, что должно отображаться в средстве просмотра.</span><span class="sxs-lookup"><span data-stu-id="9ff18-185">The following illustration shows what you should see in the viewer tool.</span></span>

![Иллюстрация текстурированной сетки в средстве просмотра](images/uvatlas6c.jpg)

<span data-ttu-id="9ff18-187">Каждая строка представляет собой величить, который является смежным ребром между двумя диаграммами в текстуре Atlas.</span><span class="sxs-lookup"><span data-stu-id="9ff18-187">Each line is a crease which is an adjacent edge between two charts in the texture atlas.</span></span> <span data-ttu-id="9ff18-188">Число диаграмм, созданных алгоритмом, вызвано незначительными различиями, возможно, из-за ненепрерывности нормальной работы.</span><span class="sxs-lookup"><span data-stu-id="9ff18-188">The number of charts generated by the algorithm is caused by slight differences perhaps due to discontinuities in the normals.</span></span> <span data-ttu-id="9ff18-189">Эти небольшие различия можно сократить, Велдинг данные, то есть заставляя данные, которые почти равны.</span><span class="sxs-lookup"><span data-stu-id="9ff18-189">These small differences can be reduced by welding data, that is, forcing data that is nearly equal to be equal.</span></span> <span data-ttu-id="9ff18-190">Чтобы расшва нормали и скинвеигхтс, сделайте следующее:</span><span class="sxs-lookup"><span data-stu-id="9ff18-190">To weld the normals and the skinweights:</span></span>

-   <span data-ttu-id="9ff18-191">Запустите средство DirectX Ops (dxops.exe) со следующей командной строкой в сетке (замените "modelName. x" на имя модели):</span><span class="sxs-lookup"><span data-stu-id="9ff18-191">Run the DirectX Ops (dxops.exe) tool with the following command line on the mesh (replacing 'modelName.x' with the name of your model):</span></span>
    ```
    Dxops.exe -s "load 'modelName.x'; Optimize n:2.01 w:2.01 uv0:0.01;  save 'newModelName.x';"
    ```

    

<span data-ttu-id="9ff18-192">Это сравнение обычных и скинвеигхтс и того, где они отличаются в значении меньшим, чем 2,01, данные становятся равными.</span><span class="sxs-lookup"><span data-stu-id="9ff18-192">This compares the normals and skinweights, and where they differ in value by less than 2.01, the data is made equal.</span></span> <span data-ttu-id="9ff18-193">На следующих иллюстрациях показано, как можно увидеть креасес перед Велдинг (слева) и креасес после Велдинг (справа):</span><span class="sxs-lookup"><span data-stu-id="9ff18-193">The following illustrations shows a close up of the eye to see the creases before welding (on the left) and the creases after welding (on the right):</span></span>

![Иллюстрация креасес перед Велдинг](images/uvatlas6a.jpg)![Иллюстрация креасес после Велдинг](images/uvatlas6b.jpg)

<span data-ttu-id="9ff18-196">Рис. 7. Удаление креасес by Велдинг</span><span class="sxs-lookup"><span data-stu-id="9ff18-196">Figure 7: Removing creases by welding</span></span>

<span data-ttu-id="9ff18-197">В этом примере Велдинг удалили 86 вершин из входной сетки.</span><span class="sxs-lookup"><span data-stu-id="9ff18-197">In this example, welding removed 86 vertices from the input mesh.</span></span> <span data-ttu-id="9ff18-198">Если в сетке меньше креасес, можно повторно создать Atlas, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="9ff18-198">With fewer creases in the mesh, you can regenerate the atlas, as the following illustration shows.</span></span>

![Иллюстрация новой Atlas с удаленным креасес](images/uvatlas8.jpg)

<span data-ttu-id="9ff18-200">Atlas содержит только 7 диаграмм и максимальный растяжение приблизительно 0,0776.</span><span class="sxs-lookup"><span data-stu-id="9ff18-200">The atlas only has 7 charts and a maximum stretch of approximately 0.0776.</span></span> <span data-ttu-id="9ff18-201">Новая Atlas теперь занимает меньшую текстуру (в этом примере приблизительно 30% меньше).</span><span class="sxs-lookup"><span data-stu-id="9ff18-201">The new atlas now fits into a smaller texture (approximately 30% smaller in this example).</span></span>

### <a name="packing-charts-into-an-atlas"></a><span data-ttu-id="9ff18-202">Упаковка диаграмм в Atlas</span><span class="sxs-lookup"><span data-stu-id="9ff18-202">Packing Charts Into an Atlas</span></span>

<span data-ttu-id="9ff18-203">После разделения сетки на отдельные параметризованные диаграммы необходимо эффективно упаковывать диаграммы в одну текстурную карту.</span><span class="sxs-lookup"><span data-stu-id="9ff18-203">Once a mesh has been partitioned into individually-parameterized charts, the charts need to be packed efficiently into a single texture map.</span></span> <span data-ttu-id="9ff18-204">Это выполняется в качестве второго шага D3DXUVAtlasCreate или может быть вызвано явным образом путем вызова D3DXUVAtlasPack.</span><span class="sxs-lookup"><span data-stu-id="9ff18-204">This is performed as the second step of D3DXUVAtlasCreate or can be invoked explicitly by calling D3DXUVAtlasPack.</span></span>

<span data-ttu-id="9ff18-205">Упакованные диаграммы разделяются заданной пользователем шириной переплета.</span><span class="sxs-lookup"><span data-stu-id="9ff18-205">Packed charts are separated by a user-specified gutter width.</span></span> <span data-ttu-id="9ff18-206">Ширина переплета — это величина разделения между диаграммами, позволяющая билинейной интерполяцию и MIP-сопоставление, чтобы избежать артефактов отрисовки на границах диаграммы.</span><span class="sxs-lookup"><span data-stu-id="9ff18-206">The gutter width is the amount of separation between charts, and allows for bilinear interpolation and mip-mapping to avoid rendering artifacts at chart boundaries.</span></span> <span data-ttu-id="9ff18-207">D3DX предоставляет интерфейс для автоматического заполнения этих переплетов. Дополнительные сведения см. в разделе [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) .</span><span class="sxs-lookup"><span data-stu-id="9ff18-207">D3DX provides an interface for automatically filling in these gutters - see [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) for more information.</span></span>

## <a name="integrating-uvatlas-into-your-pipeline"></a><span data-ttu-id="9ff18-208">Интеграция Уватлас в конвейер</span><span class="sxs-lookup"><span data-stu-id="9ff18-208">Integrating UVAtlas Into Your Pipeline</span></span>

<span data-ttu-id="9ff18-209">Помимо прорисовки текстур, эти функции можно интегрировать в автоматизированный конвейер.</span><span class="sxs-lookup"><span data-stu-id="9ff18-209">In addition to being artist-invoked prior to texture painting, these functions can be integrated into an automated art pipeline.</span></span> <span data-ttu-id="9ff18-210">Например, вызов Уватлас может быть выдан автоматически после обновления ресурса до выполнения PRT моделирования или нормального сопоставления.</span><span class="sxs-lookup"><span data-stu-id="9ff18-210">For example, a UVAtlas call can be issued automatically after an asset is updated, prior to performing a PRT simulation or normal mapping pass.</span></span> <span data-ttu-id="9ff18-211">Это позволяет избежать необходимости вручную ручного восстановления UV, если топология сетки была изменена.</span><span class="sxs-lookup"><span data-stu-id="9ff18-211">This avoids any need to manually manual repair of an object's UV mapping if the mesh's topology has been modified.</span></span>

<span data-ttu-id="9ff18-212">Пример использования функций Уватлас см. в разделе [инструмент UV Atlas Command-Line (uvatlas.exe)](https://github.com/Microsoft/UVAtlas) .</span><span class="sxs-lookup"><span data-stu-id="9ff18-212">See the [UV Atlas Command-Line Tool (uvatlas.exe)](https://github.com/Microsoft/UVAtlas) for example usage of the UVAtlas functions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9ff18-213">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="9ff18-213">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9ff18-214">Дополнительные разделы</span><span class="sxs-lookup"><span data-stu-id="9ff18-214">Advanced Topics</span></span>](advanced-topics.md)
</dt> </dl>

 

 
