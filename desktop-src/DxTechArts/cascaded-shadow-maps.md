---
title: Каскадные карты теней
description: Каскадные теневые карты (Ксмс) — это лучший способ противостоять одной из самых распространенных ошибок с помощью псевдонимов перспективы.
ms.assetid: d3570d0a-74e0-5b9c-6586-c933f630c4ee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae70433f97f33c3cc28af8e282b14ea1f513cf4d
ms.sourcegitcommit: 54db9e6a00a5c8f68e7c1a16b8c6d4943374498c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "106165524"
---
# <a name="cascaded-shadow-maps"></a><span data-ttu-id="4273d-103">Каскадные карты теней</span><span class="sxs-lookup"><span data-stu-id="4273d-103">Cascaded Shadow Maps</span></span>

<span data-ttu-id="4273d-104">Каскадные теневые карты (Ксмс) — это лучший способ противостоять одной из самых распространенных ошибок с тенью: «псевдонимы перспективы».</span><span class="sxs-lookup"><span data-stu-id="4273d-104">Cascaded shadow maps (CSMs) are the best way to combat one of the most prevalent errors with shadowing: perspective aliasing.</span></span> <span data-ttu-id="4273d-105">Эта Техническая статья, в которой предполагается, что читатель знаком с теневым отображением, рассматривается раздел Ксмс.</span><span class="sxs-lookup"><span data-stu-id="4273d-105">This technical article, which assumes the reader is familiar with shadow mapping, tackles the topic of CSMs.</span></span> <span data-ttu-id="4273d-106">В частности, код:</span><span class="sxs-lookup"><span data-stu-id="4273d-106">Specifically, it:</span></span>

-   <span data-ttu-id="4273d-107">объясняет сложность Ксмс;</span><span class="sxs-lookup"><span data-stu-id="4273d-107">explains the complexity of CSMs;</span></span>
-   <span data-ttu-id="4273d-108">содержит подробные сведения о возможных разновидностях алгоритмов CSM.</span><span class="sxs-lookup"><span data-stu-id="4273d-108">gives details on the possible variations of the CSM algorithms;</span></span>
-   <span data-ttu-id="4273d-109">Описание двух наиболее распространенных методов фильтрации: процент более детальной фильтрации (PCF) и фильтрация с помощью теневых карт дисперсии (ВСМС).</span><span class="sxs-lookup"><span data-stu-id="4273d-109">describes the two most common filtering techniques—percentage closer filtering (PCF) and filtering with variance shadow maps (VSMs);</span></span>
-   <span data-ttu-id="4273d-110">определяет и устраняет некоторые распространенные ошибки, связанные с добавлением фильтрации в Ксмс; перетаскивани</span><span class="sxs-lookup"><span data-stu-id="4273d-110">identifies and addresses some of the common pitfalls associated with adding filtering to CSMs; and</span></span>
-   <span data-ttu-id="4273d-111">показывает, как сопоставлять Ксмс с Direct3D 10 до Direct3D 11 Hardware.</span><span class="sxs-lookup"><span data-stu-id="4273d-111">shows how to map CSMs to Direct3D 10 through Direct3D 11 hardware.</span></span>

<span data-ttu-id="4273d-112">Код, используемый в этой статье, можно найти в разделе CascadedShadowMaps11 and VarianceShadows11 Samples SDK (пакет средств разработки программного обеспечения DirectX).</span><span class="sxs-lookup"><span data-stu-id="4273d-112">The code used in this article can be found in the DirectX Software Development Kit (SDK) in the CascadedShadowMaps11 and VarianceShadows11 samples.</span></span> <span data-ttu-id="4273d-113">Эта статья будет наиболее полезной после реализации методик, описанных в технической статье, и реализовать [Общие методы улучшения карт теневой глубины](/windows/desktop/DxTechArts/common-techniques-to-improve-shadow-depth-maps).</span><span class="sxs-lookup"><span data-stu-id="4273d-113">This article will prove most useful after implementing the techniques covered in the technical article, [Common Techniques to Improve Shadow Depth Maps](/windows/desktop/DxTechArts/common-techniques-to-improve-shadow-depth-maps), are implemented.</span></span>

## <a name="cascaded-shadow-maps-and-perspective-aliasing"></a><span data-ttu-id="4273d-114">Каскадные теневые карты и псевдонимы перспектив</span><span class="sxs-lookup"><span data-stu-id="4273d-114">Cascaded Shadow Maps and Perspective Aliasing</span></span>

<span data-ttu-id="4273d-115">Псевдоним перспективы в теневой карте — одна из самых сложных проблем, которую следует преодолеть.</span><span class="sxs-lookup"><span data-stu-id="4273d-115">Perspective aliasing in a shadow map is one of the most difficult problems to overcome.</span></span> <span data-ttu-id="4273d-116">В технической статье описываются распространенные методы улучшения карт глубины теневого копирования, описание псевдонимов перспективы и некоторые подходы к устранению проблемы.</span><span class="sxs-lookup"><span data-stu-id="4273d-116">In the technical article, Common Techniques to Improve Shadow Depth Maps, perspective aliasing is described and some approaches to mitigate the problem are identified.</span></span> <span data-ttu-id="4273d-117">На практике Ксмс, как правило, является лучшим решением и обычно используются в современных играх.</span><span class="sxs-lookup"><span data-stu-id="4273d-117">In practice, CSMs tend to be the best solution, and are commonly employed in modern games.</span></span>

<span data-ttu-id="4273d-118">Базовое понятие Ксмс легко понять.</span><span class="sxs-lookup"><span data-stu-id="4273d-118">The basic concept of CSMs is easy to understand.</span></span> <span data-ttu-id="4273d-119">Для разных областей камеры фрустум требуются теневые карты с разными разрешениями.</span><span class="sxs-lookup"><span data-stu-id="4273d-119">Different areas of the camera frustum require shadow maps with different resolutions.</span></span> <span data-ttu-id="4273d-120">Для объектов, ближайших к глазу, требуется более высокое разрешение, чем более отдаленные объекты.</span><span class="sxs-lookup"><span data-stu-id="4273d-120">Objects nearest the eye require a higher resolution than do more distant objects.</span></span> <span data-ttu-id="4273d-121">На самом деле, когда глаз очень близко к геометрической области, Пиксели, близкие к этому глазу, могут потребовать настолько большого разрешения, что даже на теневой карте 4096 × 4096 недостаточно.</span><span class="sxs-lookup"><span data-stu-id="4273d-121">In fact, when the eye moves very close to the geometry, the pixels nearest the eye can require so much resolution that even a 4096 × 4096 shadow map is insufficient.</span></span>

<span data-ttu-id="4273d-122">Основная идея Ксмс состоит в том, чтобы секционировать фрустум в несколько Фруста.</span><span class="sxs-lookup"><span data-stu-id="4273d-122">The basic idea of CSMs is to partition the frustum into multiple frusta.</span></span> <span data-ttu-id="4273d-123">Для каждого субфрустум отображается теневая схема; построитель текстуры затем выбирается из схемы, которая наиболее точно соответствует требуемому разрешению (рис. 2).</span><span class="sxs-lookup"><span data-stu-id="4273d-123">A shadow map is rendered for each subfrustum; the pixel shader then samples from the map that most closely matches the required resolution (Figure 2).</span></span>

<span data-ttu-id="4273d-124">**Рис. 1. Покрытие теневой схемы**</span><span class="sxs-lookup"><span data-stu-id="4273d-124">**Figure 1. Shadow map coverage**</span></span>

![покрытие теневой схемы](images/shadow-map-coverage.png)

<span data-ttu-id="4273d-126">На рис. 1 качество отображается (слева направо) от самого высокого до самого низкого.</span><span class="sxs-lookup"><span data-stu-id="4273d-126">In Figure 1, quality is shown (left to right) from highest to lowest.</span></span> <span data-ttu-id="4273d-127">Ряд сеток, представляющих теневые карты с представлением фрустум (инвертированный конус в красном фоне), показывает, как покрытие на уровне пикселей влияет на различные теневые карты разрешения.</span><span class="sxs-lookup"><span data-stu-id="4273d-127">The series of grids representing shadow maps with a view frustum (inverted cone in red) shows how pixel coverage is affected with different resolution shadow maps.</span></span> <span data-ttu-id="4273d-128">Тени имеют наивысшее качество (белые пиксели) при наличии пикселов сопоставления соотношения 1:1 в пространстве, пикселей текстуры на теневой карте.</span><span class="sxs-lookup"><span data-stu-id="4273d-128">Shadows are of the highest quality (white pixels) when there is a 1:1 ratio mapping pixels in light space to texels in the shadow map.</span></span> <span data-ttu-id="4273d-129">Псевдоним перспективы имеет форму больших, блочных текстурных карт (левое изображение), если слишком много пикселей сопоставлены с одним и тем же теневым шаг текселя.</span><span class="sxs-lookup"><span data-stu-id="4273d-129">Perspective aliasing occurs in the form of large, blocky texture maps (left image) when too many pixels map to the same shadow texel.</span></span> <span data-ttu-id="4273d-130">Если теневая схема слишком велика, она находится в разделе выборка.</span><span class="sxs-lookup"><span data-stu-id="4273d-130">When the shadow map is too large, it is under sampled.</span></span> <span data-ttu-id="4273d-131">В этом случае пикселей текстуры пропускаются, отображаются артефакты Шиммеринг, а производительность затронется.</span><span class="sxs-lookup"><span data-stu-id="4273d-131">In this case, texels are skipped, shimmering artifacts are introduced, and performance is affected.</span></span>

<span data-ttu-id="4273d-132">**Рис. 2. Качество тени CSM**</span><span class="sxs-lookup"><span data-stu-id="4273d-132">**Figure 2. CSM shadow quality**</span></span>

![качество тени CSM](images/csm-shadow-quality.png)

<span data-ttu-id="4273d-134">На рис. 2 показаны отрезки от раздела наивысшего качества на каждой теневой карте на рис. 1.</span><span class="sxs-lookup"><span data-stu-id="4273d-134">Figure 2 shows cutouts from the highest quality section in each shadow map in Figure 1.</span></span> <span data-ttu-id="4273d-135">Теневая схема с наиболее близко расположенными пикселами (в вершине) является ближайшей глазой.</span><span class="sxs-lookup"><span data-stu-id="4273d-135">The shadow map with the most closely placed pixels (at the apex) is nearest the eye.</span></span> <span data-ttu-id="4273d-136">Технически это карты одного и того же размера с белым и серым цветом, используемыми для проиллюстрировать успеха каскадной теневой карты.</span><span class="sxs-lookup"><span data-stu-id="4273d-136">Technically, these are maps of the same size, with white and grey used to exemplify the success of the cascaded shadow map.</span></span> <span data-ttu-id="4273d-137">Белый вариант идеален, так как он показывает хорошее покрытие — коэффициент 1:1 для пикселов глаза и пикселей текстуры теневой схемы.</span><span class="sxs-lookup"><span data-stu-id="4273d-137">White is ideal because it shows good coverage—a 1:1 ratio for eye-space pixels and shadow-map texels.</span></span>

<span data-ttu-id="4273d-138">Ксмс для каждого кадра необходимо выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="4273d-138">CSMs require the following steps per frame.</span></span>

1.  <span data-ttu-id="4273d-139">Разбейте фрустум на субфруста.</span><span class="sxs-lookup"><span data-stu-id="4273d-139">Partition the frustum into subfrusta.</span></span>
2.  <span data-ttu-id="4273d-140">Вычислите ортогональную проекцию для каждого субфрустум.</span><span class="sxs-lookup"><span data-stu-id="4273d-140">Compute an orthographic projection for each subfrustum.</span></span>
3.  <span data-ttu-id="4273d-141">Выводите теневую карту для каждого субфрустум.</span><span class="sxs-lookup"><span data-stu-id="4273d-141">Render a shadow map for each subfrustum.</span></span>
4.  <span data-ttu-id="4273d-142">Отрисовка сцены.</span><span class="sxs-lookup"><span data-stu-id="4273d-142">Render the scene.</span></span>

    1.  <span data-ttu-id="4273d-143">Привяжите теневые карты и визуализацию.</span><span class="sxs-lookup"><span data-stu-id="4273d-143">Bind the shadow maps and render.</span></span>
    2.  <span data-ttu-id="4273d-144">Шейдер вершин выполняет следующие действия:</span><span class="sxs-lookup"><span data-stu-id="4273d-144">The vertex shader does the following:</span></span>

        -   <span data-ttu-id="4273d-145">Вычисляет координаты текстуры для каждого светлого субфрустум (если в шейдере пикселей не вычисляется нужная Координата текстуры).</span><span class="sxs-lookup"><span data-stu-id="4273d-145">Computes texture coordinates for each light subfrustum (unless the needed texture coordinate is calculated in the pixel shader).</span></span>
        -   <span data-ttu-id="4273d-146">Преобразует и подсвечивает вершину и т. д.</span><span class="sxs-lookup"><span data-stu-id="4273d-146">Transforms and lights the vertex, and so on.</span></span>

    3.  <span data-ttu-id="4273d-147">Шейдер пикселей выполняет следующие действия:</span><span class="sxs-lookup"><span data-stu-id="4273d-147">The pixel shader does the following:</span></span>

        -   <span data-ttu-id="4273d-148">Определяет правильную теневую карту.</span><span class="sxs-lookup"><span data-stu-id="4273d-148">Determines the proper shadow map.</span></span>
        -   <span data-ttu-id="4273d-149">При необходимости преобразует координаты текстуры.</span><span class="sxs-lookup"><span data-stu-id="4273d-149">Transforms the texture coordinates if necessary.</span></span>
        -   <span data-ttu-id="4273d-150">Выборка каскадом.</span><span class="sxs-lookup"><span data-stu-id="4273d-150">Samples the cascade.</span></span>
        -   <span data-ttu-id="4273d-151">Освещение пикселя.</span><span class="sxs-lookup"><span data-stu-id="4273d-151">Lights the pixel.</span></span>

## <a name="partitioning-the-frustum"></a><span data-ttu-id="4273d-152">Секционирование Фрустум</span><span class="sxs-lookup"><span data-stu-id="4273d-152">Partitioning the Frustum</span></span>

<span data-ttu-id="4273d-153">Секционирование фрустум — это процесс создания субфруста.</span><span class="sxs-lookup"><span data-stu-id="4273d-153">Partitioning the frustum is the act of creating subfrusta.</span></span> <span data-ttu-id="4273d-154">Одним из способов разделения фрустум является вычисление интервалов от нуля до 100 процентов в направлении по оси Z.</span><span class="sxs-lookup"><span data-stu-id="4273d-154">One technique for splitting the frustum is to calculate intervals from zero percent to one hundred percent in the Z-direction.</span></span> <span data-ttu-id="4273d-155">Затем каждый интервал представляет близкую плоскость и дальнее плоскость в процентах от оси Z.</span><span class="sxs-lookup"><span data-stu-id="4273d-155">Each interval then represents a near plane and a far plane as a percentage of the Z-axis.</span></span>

<span data-ttu-id="4273d-156">**Рис. 3. Произвольное представление секционирования фрустумс**</span><span class="sxs-lookup"><span data-stu-id="4273d-156">**Figure 3. View frustums partitioned arbitrarily**</span></span>

![Произвольное представление секционирования фрустумс](images/view-frustums-partitioned-arbitrarily.png)

<span data-ttu-id="4273d-158">На практике повторное вычисление разбиений фрустум на кадр приводит к шиммерию теней.</span><span class="sxs-lookup"><span data-stu-id="4273d-158">In practice, recalculating the frustum splits per frame causes shadow edges to shimmer.</span></span> <span data-ttu-id="4273d-159">Обычно принято использовать статический набор каскадных интервалов для каждого сценария.</span><span class="sxs-lookup"><span data-stu-id="4273d-159">The generally accepted practice is to use a static set of cascade intervals per scenario.</span></span> <span data-ttu-id="4273d-160">В этом сценарии интервал по оси Z используется для описания субфрустум, возникающего при секционировании фрустум.</span><span class="sxs-lookup"><span data-stu-id="4273d-160">In this scenario, the interval along the Z-axis is used to describe a subfrustum that occurs when partitioning the frustum.</span></span> <span data-ttu-id="4273d-161">Определение правильных интервалов для заданной сцены зависит от нескольких факторов.</span><span class="sxs-lookup"><span data-stu-id="4273d-161">Determining the correct size intervals for a given scene depends upon several factors.</span></span>

### <a name="orientation-of-the-scene-geometry"></a><span data-ttu-id="4273d-162">Ориентация геометрии сцены</span><span class="sxs-lookup"><span data-stu-id="4273d-162">Orientation of the Scene Geometry</span></span>

<span data-ttu-id="4273d-163">По отношению к геометрии сцены ориентация на камеру влияет на выбор каскадного интервала.</span><span class="sxs-lookup"><span data-stu-id="4273d-163">With respect to scene geometry, camera orientation affects cascade interval selection.</span></span> <span data-ttu-id="4273d-164">Например, Камера, почти близкая к заземлению, например, Камера в футболе, имеет другой статический набор интервалов Cascade, чем камера в перевозки.</span><span class="sxs-lookup"><span data-stu-id="4273d-164">For example, a camera very near the ground, such as a ground camera in a football game, has a different static set of cascade intervals than a camera in the sky.</span></span>

<span data-ttu-id="4273d-165">На рис. 4 показаны некоторые различные камеры и их соответствующие секции.</span><span class="sxs-lookup"><span data-stu-id="4273d-165">Figure 4 shows some different cameras and their respective partitions.</span></span> <span data-ttu-id="4273d-166">Если Z-диапазон сцены очень большой, требуется больше разделенных плоскостей.</span><span class="sxs-lookup"><span data-stu-id="4273d-166">When the scene's Z-range is very large, more split planes are required.</span></span> <span data-ttu-id="4273d-167">Например, когда глаз почти находится рядом с плоскостью земли, но удаленные объекты по-прежнему видны, может потребоваться несколько каскадных переходов.</span><span class="sxs-lookup"><span data-stu-id="4273d-167">For example, when the eye is very near the ground plane, but distant objects are still visible, multiple cascades can be necessary.</span></span> <span data-ttu-id="4273d-168">Деление фрустум таким образом, чтобы более разбиваются рядом с глазом (где изменение псевдонимов перспективы меняется быстрее) также является ценным.</span><span class="sxs-lookup"><span data-stu-id="4273d-168">Dividing the frustum so that more splits are near the eye (where perspective aliasing is changing the fastest) is also valuable.</span></span> <span data-ttu-id="4273d-169">Если большая часть геометрического объекта клумпед в небольшой раздел (например, на представление "затраты на накладные расходы" или симулятор рейсов) представления фрустум, необходимо меньше каскадных элементов.</span><span class="sxs-lookup"><span data-stu-id="4273d-169">When most of the geometry is clumped into a small section (such as an overhead view or a flight simulator) of the view frustum, fewer cascades are necessary.</span></span>

<span data-ttu-id="4273d-170">**Рис. 4. Для различных конфигураций требуются разные фрустум разбиения**</span><span class="sxs-lookup"><span data-stu-id="4273d-170">**Figure 4. Different configurations require different frustum splits**</span></span>

![для различных конфигураций требуются разные фрустум разбиения](images/different-configurations-require-different-frustum-splits.png)

<span data-ttu-id="4273d-172">Слева Если геометрический объект имеет большой динамический диапазон в Z, требуется много каскадных.</span><span class="sxs-lookup"><span data-stu-id="4273d-172">(Left) When geometry has a high dynamic range in Z, lots of cascades are required.</span></span> <span data-ttu-id="4273d-173">Center Если геометрический объект имеет низкий динамический диапазон в Z, существует небольшое преимущество нескольких фрустумс.</span><span class="sxs-lookup"><span data-stu-id="4273d-173">(Center) When the geometry has low dynamic range in Z, there is little benefit from multiple frustums.</span></span> <span data-ttu-id="4273d-174">Справа Если динамический диапазон является средним, необходимы только три секции.</span><span class="sxs-lookup"><span data-stu-id="4273d-174">(Right) Only three partitions are needed when the dynamic range is medium.</span></span>

### <a name="orientation-of-the-light-and-the-camera"></a><span data-ttu-id="4273d-175">Ориентация освещения и камеры</span><span class="sxs-lookup"><span data-stu-id="4273d-175">Orientation of the Light and the Camera</span></span>

<span data-ttu-id="4273d-176">Каждая матрица проекции каскадом тесно связана с соответствующей субфрустум.</span><span class="sxs-lookup"><span data-stu-id="4273d-176">Each cascade's projection matrix is fit tightly around its corresponding subfrustum.</span></span> <span data-ttu-id="4273d-177">В конфигурациях, в которых Камера и лампочка представления являются ортогональными, каскадные расположения могут быть тесно связаны с небольшим перекрытием.</span><span class="sxs-lookup"><span data-stu-id="4273d-177">In configurations where the view camera and the light directions are orthogonal, the cascades can be fit tightly with little overlap.</span></span> <span data-ttu-id="4273d-178">Перекрытие увеличивается по мере того, как лампочка и вид камеры переходят в параллельное выравнивание (рис. 5).</span><span class="sxs-lookup"><span data-stu-id="4273d-178">The overlap becomes larger as the light and the view camera move into parallel alignment (Figure 5).</span></span> <span data-ttu-id="4273d-179">Если лампочка и вид камеры почти параллельны, она называется «дуелинг Фруста» и является очень сложной ситуацией для большинства алгоритмов теневого копирования.</span><span class="sxs-lookup"><span data-stu-id="4273d-179">When the light and the view camera are nearly parallel, it is called a "dueling frusta," and is a very hard scenario for most shadowing algorithms.</span></span> <span data-ttu-id="4273d-180">Нередко можно ограничить освещение и камеру, чтобы этот сценарий не наблюдались.</span><span class="sxs-lookup"><span data-stu-id="4273d-180">It is not uncommon to constrain the light and camera so that this scenario does not occur.</span></span> <span data-ttu-id="4273d-181">Однако в этом сценарии Ксмс работают гораздо лучше, чем многие другие алгоритмы.</span><span class="sxs-lookup"><span data-stu-id="4273d-181">CSMs, however, perform much better than many other algorithms in this scenario.</span></span>

<span data-ttu-id="4273d-182">**Рис. 5. Каскадное перекрытие увеличивается, так как направление освещения становится параллельным с направлением камеры**</span><span class="sxs-lookup"><span data-stu-id="4273d-182">**Figure 5. Cascade overlap increases as light direction becomes parallel with camera direction**</span></span>

![каскадное перекрытие увеличивается, так как направление освещения становится параллельным с направлением камеры](images/cascade-overlap-increases-as-light-direction-becomes.jpg)

<span data-ttu-id="4273d-184">Многие реализации CSM используют Фруста фиксированного размера.</span><span class="sxs-lookup"><span data-stu-id="4273d-184">Many CSM implementations use fixed-size frusta.</span></span> <span data-ttu-id="4273d-185">Шейдер пикселей может использовать Z-глубину для индексации массива каскадных значений, когда фрустум разбивается в интервалах фиксированного размера.</span><span class="sxs-lookup"><span data-stu-id="4273d-185">The pixel shader can use the Z-depth to index into the array of cascades when the frustum is split in fixed-size intervals.</span></span>

## <a name="calculating-a-view-frustum-bound"></a><span data-ttu-id="4273d-186">Вычисление привязанного к View-Frustumу</span><span class="sxs-lookup"><span data-stu-id="4273d-186">Calculating a View-Frustum Bound</span></span>

<span data-ttu-id="4273d-187">После выбора интервалов фрустум субфруста создаются с помощью одного из двух: по размеру сцены и по размеру каскада.</span><span class="sxs-lookup"><span data-stu-id="4273d-187">Once the frustum intervals are selected, the subfrusta are created using one of two: fit to scene and fit to cascade.</span></span>

### <a name="fit-to-scene"></a><span data-ttu-id="4273d-188">Вписать в сцену</span><span class="sxs-lookup"><span data-stu-id="4273d-188">Fit to Scene</span></span>

<span data-ttu-id="4273d-189">Все Фруста можно создать с одной и той же ближней плоскостью.</span><span class="sxs-lookup"><span data-stu-id="4273d-189">All of the frusta can be created with the same near plane.</span></span> <span data-ttu-id="4273d-190">Это приводит к перекрытию каскадных переходов.</span><span class="sxs-lookup"><span data-stu-id="4273d-190">This forces the cascades to overlap.</span></span> <span data-ttu-id="4273d-191">Пример CascadedShadowMaps11 вызывает этот метод по размеру сцены.</span><span class="sxs-lookup"><span data-stu-id="4273d-191">The CascadedShadowMaps11 sample calls this technique fit to scene.</span></span>

### <a name="fit-to-cascade"></a><span data-ttu-id="4273d-192">Вписать в каскадную</span><span class="sxs-lookup"><span data-stu-id="4273d-192">Fit to Cascade</span></span>

<span data-ttu-id="4273d-193">Кроме того, Фруста можно создать с фактическим интервалом секций, который используется в качестве ближайших и дальнех плоскостей.</span><span class="sxs-lookup"><span data-stu-id="4273d-193">Alternatively, frusta can be created with the actual partition interval being used as near and far planes.</span></span> <span data-ttu-id="4273d-194">Это приводит к более тесному подаче, но вырождению для использования сцены в случае дуелинг Фруста.</span><span class="sxs-lookup"><span data-stu-id="4273d-194">This causes a tighter fit, but degenerates to fit to scene in the case of dueling frusta.</span></span> <span data-ttu-id="4273d-195">Примеры CascadedShadowMaps11 вызывают этот метод для размещения каскадом.</span><span class="sxs-lookup"><span data-stu-id="4273d-195">The CascadedShadowMaps11 samples calls this technique fit to cascade.</span></span>

<span data-ttu-id="4273d-196">Эти два метода показаны на рис. 6.</span><span class="sxs-lookup"><span data-stu-id="4273d-196">These two methods are shown in Figure 6.</span></span> <span data-ttu-id="4273d-197">Подгонка к каскадным расходам с меньшим разрешением.</span><span class="sxs-lookup"><span data-stu-id="4273d-197">Fit to cascade wastes less resolution.</span></span> <span data-ttu-id="4273d-198">Проблема по размеру каскада заключается в том, что ортогональная проекция растет и сжимается в зависимости от ориентации представления фрустум.</span><span class="sxs-lookup"><span data-stu-id="4273d-198">The problem with fit to cascade is that the orthographic projection grows and shrinks based on the orientation of the view frustum.</span></span> <span data-ttu-id="4273d-199">Методика "вписать в сцену" размещает ортогональную проекцию на максимальный размер представления фрустум удаление артефактов, отображаемых при перемещении представления камерой.</span><span class="sxs-lookup"><span data-stu-id="4273d-199">The fit to scene technique pads the orthographic projection by the max size of the view frustum removing the artifacts that appear when the view-camera moves.</span></span> <span data-ttu-id="4273d-200">[Распространенные методы улучшения карт теневой глубины позволяют](/windows/desktop/DxTechArts/common-techniques-to-improve-shadow-depth-maps) устранить помехи, которые появляются, когда источник перемещается в разделе «Перемещение освещения с увеличением размера шаг текселя».</span><span class="sxs-lookup"><span data-stu-id="4273d-200">[Common Techniques to Improve Shadow Depth Maps](/windows/desktop/DxTechArts/common-techniques-to-improve-shadow-depth-maps) addresses the artifacts that appear when the light moves in the section "Moving the light in texel sized increments."</span></span>

<span data-ttu-id="4273d-201">**Рис. 6. По размеру сцены и по размеру каскадом**</span><span class="sxs-lookup"><span data-stu-id="4273d-201">**Figure 6. Fit to scene vs. fit to cascade**</span></span>

![вписать в сцену и разместить в каскаде](images/fit-to-scene-vs-fit-to-cascade.png)

## <a name="render-the-shadow-map"></a><span data-ttu-id="4273d-203">Визуализация теневой схемы</span><span class="sxs-lookup"><span data-stu-id="4273d-203">Render the Shadow Map</span></span>

<span data-ttu-id="4273d-204">Образец CascadedShadowMaps11 визуализирует теневые карты в один большой буфер.</span><span class="sxs-lookup"><span data-stu-id="4273d-204">The CascadedShadowMaps11 sample renders the shadow maps into one large buffer.</span></span> <span data-ttu-id="4273d-205">Это обусловлено тем, что PCF на массивах текстур — это функция Direct3D 10,1.</span><span class="sxs-lookup"><span data-stu-id="4273d-205">This is because PCF on texture arrays is a Direct3D 10.1 feature.</span></span> <span data-ttu-id="4273d-206">Для каждого каскадного представления создается окно просмотра, охватывающее раздел буфера глубины, соответствующий этому каскаду.</span><span class="sxs-lookup"><span data-stu-id="4273d-206">For every cascade, a viewport is created that covers the section of the depth buffer corresponding to that cascade.</span></span> <span data-ttu-id="4273d-207">Привязка шейдера пикселей NULL выполнена, так как требуется только глубина.</span><span class="sxs-lookup"><span data-stu-id="4273d-207">A null pixel shader is bound because only the depth is needed.</span></span> <span data-ttu-id="4273d-208">Наконец, правильная область просмотра и матрица Shadow задаются для каждого каскада, так как карты глубины подготавливаются к просмотру по одной за раз в основном буфере теневого копирования.</span><span class="sxs-lookup"><span data-stu-id="4273d-208">Finally, the correct viewport and shadow matrix are set for each cascade as the depth maps are rendered one at a time into the main shadow buffer.</span></span>

## <a name="render-the-scene"></a><span data-ttu-id="4273d-209">Отрисовка сцены</span><span class="sxs-lookup"><span data-stu-id="4273d-209">Render the Scene</span></span>

<span data-ttu-id="4273d-210">Буфер, содержащий тени, теперь привязан к шейдеру пикселей.</span><span class="sxs-lookup"><span data-stu-id="4273d-210">The buffer containing the shadows is now bound to the pixel shader.</span></span> <span data-ttu-id="4273d-211">Существует два метода выбора каскада, реализованного в образце CascadedShadowMaps11.</span><span class="sxs-lookup"><span data-stu-id="4273d-211">There are two methods for selecting the cascade implemented in the CascadedShadowMaps11 sample.</span></span> <span data-ttu-id="4273d-212">Эти два метода объясняются с помощью кода шейдера.</span><span class="sxs-lookup"><span data-stu-id="4273d-212">These two methods are explained with shader code.</span></span>

### <a name="interval-based-cascade-selection"></a><span data-ttu-id="4273d-213">Interval-Based каскадный выбор</span><span class="sxs-lookup"><span data-stu-id="4273d-213">Interval-Based Cascade Selection</span></span>

<span data-ttu-id="4273d-214">**Рис. 7. Каскадное выделение на основе интервалов**</span><span class="sxs-lookup"><span data-stu-id="4273d-214">**Figure 7. Interval-based cascade selection**</span></span>

![каскадное выделение на основе интервалов](images/interval-based-cascade-selection.jpg)

<span data-ttu-id="4273d-216">В выборе на основе интервалов (рис. 7) Вершинный шейдер вычислит расположение в мировом пространстве вершины.</span><span class="sxs-lookup"><span data-stu-id="4273d-216">In interval-based selection (Figure 7), the vertex shader computes the position in world-space of the vertex.</span></span>


```C++
Output.vDepth = mul( Input.vPosition, m_mWorldView ).z;
```



<span data-ttu-id="4273d-217">Построитель текстуры получает глубину интерполяции.</span><span class="sxs-lookup"><span data-stu-id="4273d-217">The pixel shader receives the interpolated depth.</span></span>


```C++
fCurrentPixelDepth = Input.vDepth;
```



<span data-ttu-id="4273d-218">При каскадном выборе на основе интервалов используется сравнение вектора и точки для определения правильного какаде.</span><span class="sxs-lookup"><span data-stu-id="4273d-218">Interval-based cascade selection uses a vector comparison and a dot product to determine the correct cacade.</span></span> <span data-ttu-id="4273d-219">Флаг CASCADE \_ Count \_ указывает количество каскадных значений.</span><span class="sxs-lookup"><span data-stu-id="4273d-219">The CASCADE\_COUNT\_FLAG specifies the number of cascades.</span></span> <span data-ttu-id="4273d-220">\_Фкаскадефрустумсэйеспацедепсс данных m \_ ограничивает разделы View фрустум.</span><span class="sxs-lookup"><span data-stu-id="4273d-220">The m\_fCascadeFrustumsEyeSpaceDepths\_data constrains the view frustum partitions.</span></span> <span data-ttu-id="4273d-221">После сравнения Фкомпарисон содержит значение 1, где текущий пиксель больше барьера, и значение 0, если текущий Каскад является меньшим.</span><span class="sxs-lookup"><span data-stu-id="4273d-221">After the comparison, the fComparison contains a value of 1 where the current pixel is larger than the barrier, and a value of 0 when the current cascade is smaller.</span></span> <span data-ttu-id="4273d-222">Элемент "точка" суммирует эти значения в индексе массива.</span><span class="sxs-lookup"><span data-stu-id="4273d-222">A dot product sums these values into an array index.</span></span>


```C++
        float4 vCurrentPixelDepth = Input.vDepth;
        float4 fComparison = ( vCurrentPixelDepth > m_fCascadeFrustumsEyeSpaceDepths_data[0]);
        float fIndex = dot(
        float4( CASCADE_COUNT_FLAG > 0,
        CASCADE_COUNT_FLAG > 1,
        CASCADE_COUNT_FLAG > 2,
        CASCADE_COUNT_FLAG > 3)
        , fComparison );

        fIndex = min( fIndex, CASCADE_COUNT_FLAG );
        iCurrentCascadeIndex = (int)fIndex;
```



<span data-ttu-id="4273d-223">После выбора Cascade Координата текстуры должна быть преобразована в правильную каскадную.</span><span class="sxs-lookup"><span data-stu-id="4273d-223">Once the cascade is selected, the texture coordinate must be transformed to the correct cascade.</span></span>


```C++
vShadowTexCoord = mul( InterpolatedPosition, m_mShadow[iCascadeIndex] );
```



<span data-ttu-id="4273d-224">Эта Координата текстуры затем используется для выборки текстуры с помощью координаты X и координаты Y.</span><span class="sxs-lookup"><span data-stu-id="4273d-224">This texture coordinate is then used to sample the texture with the X-coordinate and the Y-coordinate.</span></span> <span data-ttu-id="4273d-225">Координата Z используется для окончательного сравнения глубины.</span><span class="sxs-lookup"><span data-stu-id="4273d-225">The Z-coordinate is used to do the final depth comparison.</span></span>

### <a name="map-based-cascade-selection"></a><span data-ttu-id="4273d-226">Map-Based каскадный выбор</span><span class="sxs-lookup"><span data-stu-id="4273d-226">Map-Based Cascade Selection</span></span>

<span data-ttu-id="4273d-227">Выбор на основе карт (рис. 8) проверяет четыре стороны каскадных объектов, чтобы найти наиболее тесное соответствие, охватывающее конкретный пиксель.</span><span class="sxs-lookup"><span data-stu-id="4273d-227">Map-based selection (Figure 8) tests against the four sides of the cascades to find the tightest map that covers the specific pixel.</span></span> <span data-ttu-id="4273d-228">Вместо вычисления расположения в мировом пространстве шейдер вершин вычисляет расположение пространства в области просмотра для каждого каскада.</span><span class="sxs-lookup"><span data-stu-id="4273d-228">Instead of calculating the position in world space, the vertex shader calculates the view-space position for every cascade.</span></span> <span data-ttu-id="4273d-229">Шейдер пикселей выполняет перебор каскадов, чтобы масштабировать и сдвинуть координаты текстуры таким образом, чтобы они проиндексированы текущий Каскад.</span><span class="sxs-lookup"><span data-stu-id="4273d-229">The pixel shader iterates over the cascades in order to scale and shift the texture coordinates so that they index the current cascade.</span></span> <span data-ttu-id="4273d-230">Затем Координата текстуры проверяется на соответствие текстурным границам.</span><span class="sxs-lookup"><span data-stu-id="4273d-230">The texture coordinate is then tested against the texture bounds.</span></span> <span data-ttu-id="4273d-231">Если значения X и Y координаты текстуры находятся внутри каскадной, они используются для выборки текстуры.</span><span class="sxs-lookup"><span data-stu-id="4273d-231">When the X and Y values of the texture coordinate fall inside a cascade, they are used to sample the texture.</span></span> <span data-ttu-id="4273d-232">Координата Z используется для окончательного сравнения глубины.</span><span class="sxs-lookup"><span data-stu-id="4273d-232">The Z-coordinate is used to do the final depth comparison.</span></span>

<span data-ttu-id="4273d-233">**Рис. 8. Каскадное выделение на основе карт**</span><span class="sxs-lookup"><span data-stu-id="4273d-233">**Figure 8. Map-based cascade selection**</span></span>

![каскадное выделение на основе карт](images/map-based-cascade-selection.jpg)

### <a name="interval-based-selection-vs-map-based-selection"></a><span data-ttu-id="4273d-235">Выбор Interval-Based и выбор Map-Based</span><span class="sxs-lookup"><span data-stu-id="4273d-235">Interval-Based Selection vs. Map-Based Selection</span></span>

<span data-ttu-id="4273d-236">Выбор на основе интервалов выполняется немного быстрее, чем выбор на основе карт, поскольку каскадное выделение можно выполнить напрямую.</span><span class="sxs-lookup"><span data-stu-id="4273d-236">Interval-based selection is slightly faster than map-based selection because the cascade selection can be done directly.</span></span> <span data-ttu-id="4273d-237">Выбор на основе карт должен пересекать координату текстуры с границами Cascade.</span><span class="sxs-lookup"><span data-stu-id="4273d-237">Map-based selection must intersect the texture coordinate with the cascade bounds.</span></span>

<span data-ttu-id="4273d-238">Выбор на основе карты более эффективно использует Каскад, если теневые карты не выровнены идеально (см. рис. 8).</span><span class="sxs-lookup"><span data-stu-id="4273d-238">Map-based selection uses the cascade more efficiently when shadow maps do not align perfectly (see Figure 8).</span></span>

## <a name="blend-between-cascades"></a><span data-ttu-id="4273d-239">Переход между каскадными таблицами</span><span class="sxs-lookup"><span data-stu-id="4273d-239">Blend between Cascades</span></span>

<span data-ttu-id="4273d-240">ВСМС (см. Далее в этой статье) и методы фильтрации, такие как PCF, можно использовать с Ксмс с низким разрешением для создания мягких теней.</span><span class="sxs-lookup"><span data-stu-id="4273d-240">VSMs (discussed later in this article) and filtering techniques such as PCF can be used with low-resolution CSMs to produce soft shadows.</span></span> <span data-ttu-id="4273d-241">К сожалению, это приводит к отображению стыка (рис. 9) между каскадными слоями, так как разрешение не совпадает.</span><span class="sxs-lookup"><span data-stu-id="4273d-241">Unfortunately, this results in a visible seam (Figure 9) between cascade layers because the resolution does not match.</span></span> <span data-ttu-id="4273d-242">Решение состоит в том, чтобы создать полосу между теневыми картами, где выполняется теневая проверка обоих каскадных расположений.</span><span class="sxs-lookup"><span data-stu-id="4273d-242">The solution is to create a band between shadow maps where the shadow test is performed for both cascades.</span></span> <span data-ttu-id="4273d-243">Затем шейдер линейно выполняет интерполяцию между двумя значениями на основе расположения пикселя в полосе смешения.</span><span class="sxs-lookup"><span data-stu-id="4273d-243">The shader then linearly interpolates between the two values based on the pixel's location in the blend band.</span></span> <span data-ttu-id="4273d-244">Примеры CascadedShadowMaps11 и VarianceShadows11 предоставляют ползунок графического пользовательского интерфейса, который можно использовать для увеличения и уменьшения этого диапазона размытия.</span><span class="sxs-lookup"><span data-stu-id="4273d-244">The samples CascadedShadowMaps11 and VarianceShadows11 provide a GUI slider that can be used to increase and decrease this blur band.</span></span> <span data-ttu-id="4273d-245">Шейдер выполняет динамическую ветвь, чтобы подавляющее большинство пикселей было считано только из текущего каскада.</span><span class="sxs-lookup"><span data-stu-id="4273d-245">The shader performs a dynamic branch so that the vast majority of pixels only read from the current cascade.</span></span>

<span data-ttu-id="4273d-246">**Рис. 9. Каскадные стыки**</span><span class="sxs-lookup"><span data-stu-id="4273d-246">**Figure 9. Cascade seams**</span></span>

![каскадные стыки](images/cascade-seams.jpg)

<span data-ttu-id="4273d-248">Слева Видимый стык можно увидеть, где каскады перекрываются.</span><span class="sxs-lookup"><span data-stu-id="4273d-248">(Left) A visible seam can be seen where cascades overlap.</span></span> <span data-ttu-id="4273d-249">Справа При переходе между каскадными таблицами не происходит стыка.</span><span class="sxs-lookup"><span data-stu-id="4273d-249">(Right) When the cascades are blended between, no seam occurs.</span></span>

## <a name="filtering-shadow-maps"></a><span data-ttu-id="4273d-250">Фильтрация теневых карт</span><span class="sxs-lookup"><span data-stu-id="4273d-250">Filtering Shadow Maps</span></span>

### <a name="pcf"></a><span data-ttu-id="4273d-251">PCF</span><span class="sxs-lookup"><span data-stu-id="4273d-251">PCF</span></span>

<span data-ttu-id="4273d-252">Фильтрация обычных теневых карт не приводит к созданию мягких размытий теней.</span><span class="sxs-lookup"><span data-stu-id="4273d-252">Filtering ordinary shadow maps does not produce soft, blurred shadows.</span></span> <span data-ttu-id="4273d-253">Фильтрация оборудования разменяет значения глубины, а затем сравнивает эти размытые значения с шаг текселя пространством.</span><span class="sxs-lookup"><span data-stu-id="4273d-253">The filtering hardware blurs the depth values, and then compares those blurred values to the light space texel.</span></span> <span data-ttu-id="4273d-254">Жесткий элемент, полученный в результате теста пройден/Fail, все еще существует.</span><span class="sxs-lookup"><span data-stu-id="4273d-254">The hard edge resulting from the pass/fail test still exists.</span></span> <span data-ttu-id="4273d-255">Размытие теневые карты служат только для того, чтобы ошибочно переместить жесткое ребро.</span><span class="sxs-lookup"><span data-stu-id="4273d-255">Blurring shadow maps only serves to erroneously move the hard edge.</span></span> <span data-ttu-id="4273d-256">PCF включает фильтрацию на теневых картах.</span><span class="sxs-lookup"><span data-stu-id="4273d-256">PCF enables filtering on shadow maps.</span></span> <span data-ttu-id="4273d-257">Основная идея PCF заключается в том, чтобы вычислить процентную долю пикселя в тени на основе количества подвыборок, прошедших тест глубины по общему количеству подвыборок.</span><span class="sxs-lookup"><span data-stu-id="4273d-257">The general idea of PCF is to calculate a percentage of the pixel in shadow based on the number of subsamples that pass the depth test over the total number of subsamples.</span></span>

<span data-ttu-id="4273d-258">Direct3D 10 и Direct3D 11 могут выполнять PCF.</span><span class="sxs-lookup"><span data-stu-id="4273d-258">Direct3D 10 and Direct3D 11 hardware can perform PCF.</span></span> <span data-ttu-id="4273d-259">Входные данные для образца PCF состоят из координаты текстуры и значения глубины сравнения.</span><span class="sxs-lookup"><span data-stu-id="4273d-259">The input to a PCF sampler consists of the texture-coordinate and a comparison depth value.</span></span> <span data-ttu-id="4273d-260">Для простоты PCF объясняется с помощью фильтра с четырьмя касаниями.</span><span class="sxs-lookup"><span data-stu-id="4273d-260">For simplicity, PCF is explained with a four-tap filter.</span></span> <span data-ttu-id="4273d-261">Образец текстуры считывает текстуру четыре раза, аналогично стандартному фильтру.</span><span class="sxs-lookup"><span data-stu-id="4273d-261">The texture sampler reads the texture four times, similar to a standard filter.</span></span> <span data-ttu-id="4273d-262">Однако возвращаемый результат представляет собой процент пикселей, которые прошли тест глубины.</span><span class="sxs-lookup"><span data-stu-id="4273d-262">However, the returned result is a percentage of the pixels that passed the depth test.</span></span> <span data-ttu-id="4273d-263">На рис. 10 показано, как в теневой копии пикселя, прошедшего одну из четырех тестов глубины, является 25%.</span><span class="sxs-lookup"><span data-stu-id="4273d-263">Figure 10 shows how a pixel that passes one of the four depth tests is 25 percent in shadow.</span></span> <span data-ttu-id="4273d-264">Возвращаемое значение представляет собой линейную интерполяцию, основанную на субтексел координатах считывания текстур для создания плавного градиента.</span><span class="sxs-lookup"><span data-stu-id="4273d-264">The actual value returned is a linear interpolation based on the subtexel coordinates of the texture reads to produce a smooth gradient.</span></span> <span data-ttu-id="4273d-265">Без этой линейной интерполяции PCF с четырьмя tapи смогут возвращать только пять значений: {0,0, 0,25, 0,5, 0,75, 1,0}.</span><span class="sxs-lookup"><span data-stu-id="4273d-265">Without this linear interpolation, the four-tap PCF would only be able to return five values: { 0.0, 0.25, 0.5, 0.75, 1.0 }.</span></span>

<span data-ttu-id="4273d-266">**Рис. 10. Отфильтрованное изображение PCF с покрыто 25% от выбранного пикселя**</span><span class="sxs-lookup"><span data-stu-id="4273d-266">**Figure 10. PCF filtered image, with 25 percent of the selected pixel covered**</span></span>

![отфильтрованное изображение PCF с покрыто 25% от выбранного пикселя](images/pcf-filtered-image.png)

<span data-ttu-id="4273d-268">Также можно выполнить PCF без поддержки оборудования или расширить PCF до более крупных ядер.</span><span class="sxs-lookup"><span data-stu-id="4273d-268">It is also possible to do PCF without hardware support or extend PCF to larger kernels.</span></span> <span data-ttu-id="4273d-269">Некоторые приемы даже выборке с взвешенным ядром.</span><span class="sxs-lookup"><span data-stu-id="4273d-269">Some techniques even sample with a weighted kernel.</span></span> <span data-ttu-id="4273d-270">Для этого создайте ядро (например, значение по Гауссу) для сетки N × N.</span><span class="sxs-lookup"><span data-stu-id="4273d-270">To do this, create a kernel (such as a Gaussian) for an N × N grid.</span></span> <span data-ttu-id="4273d-271">Весовые коэффициенты должны быть не более 1.</span><span class="sxs-lookup"><span data-stu-id="4273d-271">The weights must add up to 1.</span></span> <span data-ttu-id="4273d-272">Затем текстура выдает значение N2 раз.</span><span class="sxs-lookup"><span data-stu-id="4273d-272">The texture is then sampled N2 times.</span></span> <span data-ttu-id="4273d-273">Каждый пример масштабируется по соответствующим весовым коэффициентам в ядре.</span><span class="sxs-lookup"><span data-stu-id="4273d-273">Each sample is scaled by the corresponding weights in the kernel.</span></span> <span data-ttu-id="4273d-274">Этот подход используется в образце CascadedShadowMaps11.</span><span class="sxs-lookup"><span data-stu-id="4273d-274">The CascadedShadowMaps11 sample uses this approach.</span></span>

### <a name="depth-bias"></a><span data-ttu-id="4273d-275">Смещение глубины</span><span class="sxs-lookup"><span data-stu-id="4273d-275">Depth Bias</span></span>

<span data-ttu-id="4273d-276">Сдвиг глубины еще более важен при использовании крупных ядер PCF.</span><span class="sxs-lookup"><span data-stu-id="4273d-276">Depth bias becomes even more important when large PCF kernels are used.</span></span> <span data-ttu-id="4273d-277">Это допустимо только для сравнения глубины свободного пространства в пикселях относительно пикселя, к которому он соответствует, на карте глубины.</span><span class="sxs-lookup"><span data-stu-id="4273d-277">It is only valid to compare a pixel's light-space depth against the pixel it maps to in the depth map.</span></span> <span data-ttu-id="4273d-278">Соседи шаг текселя карт глубины ссылаются на другую точку.</span><span class="sxs-lookup"><span data-stu-id="4273d-278">The depth map texel's neighbors refer to a different position.</span></span> <span data-ttu-id="4273d-279">Эта глубина, скорее всего, будет аналогичной, но она может сильно отличаться в зависимости от сцены.</span><span class="sxs-lookup"><span data-stu-id="4273d-279">This depth is likely to be similar, but can be very different depending on the scene.</span></span> <span data-ttu-id="4273d-280">На рис. 11 показаны происходящие артефакты.</span><span class="sxs-lookup"><span data-stu-id="4273d-280">Figure 11 highlights the artifacts that occur.</span></span> <span data-ttu-id="4273d-281">Одна глубина сравнивается с тремя соседними пикселей текстуры в теневой карте.</span><span class="sxs-lookup"><span data-stu-id="4273d-281">A single depth is compared to three neighboring texels in the shadow map.</span></span> <span data-ttu-id="4273d-282">Одна из тестов глубины ошибочно завершается ошибкой, так как ее глубина не соотносится с вычисленной глубиной освещения текущего геометрического пространства.</span><span class="sxs-lookup"><span data-stu-id="4273d-282">One of the depth tests erroneously fails because its depth does not correlate to the computed light-space depth of the current geometry.</span></span> <span data-ttu-id="4273d-283">Рекомендуемое решение этой проблемы — использовать более крупное смещение.</span><span class="sxs-lookup"><span data-stu-id="4273d-283">The recommended solution to this problem is to use a larger offset.</span></span> <span data-ttu-id="4273d-284">Однако слишком большое значение смещения может привести к сдвигу Питер.</span><span class="sxs-lookup"><span data-stu-id="4273d-284">Too large of an offset, however, can result in Peter Panning.</span></span> <span data-ttu-id="4273d-285">Вычисление тесного приближения плоскости и дальней плоскости позволяет снизить последствия использования смещения.</span><span class="sxs-lookup"><span data-stu-id="4273d-285">Calculating a tight near plane and far plane helps reduce the effects of using an offset.</span></span>

<span data-ttu-id="4273d-286">**Рис. 11. Ошибочное затенение**</span><span class="sxs-lookup"><span data-stu-id="4273d-286">**Figure 11. Erroneous self-shadowing**</span></span>

![ошибочное затенение](images/erroneous-self-shadowing.png)

<span data-ttu-id="4273d-288">Ошибочное затенение приводит к сравнению пикселов в глубине свободного пространства с пикселей текстуры на теневой карте, которая не взаимосвязана.</span><span class="sxs-lookup"><span data-stu-id="4273d-288">The erroneous self-shadowing results from comparing pixels in the light-space depth to the texels in the shadow map that do not correlate.</span></span> <span data-ttu-id="4273d-289">Глубина в светлом пространстве соответствует теневому шаг текселя 2 на карте глубины.</span><span class="sxs-lookup"><span data-stu-id="4273d-289">The depth in light-space correlates to shadow texel 2 in the depth map.</span></span> <span data-ttu-id="4273d-290">Шаг текселя 1 больше, чем глубина свободного пространства, а 2 равно, а 3 меньше.</span><span class="sxs-lookup"><span data-stu-id="4273d-290">Texel 1 is greater than the light-space depth while 2 is equal and 3 is less.</span></span> <span data-ttu-id="4273d-291">Пикселей текстуры 2 и 3 прошли тест глубины, в то время как шаг текселя 1 завершается ошибкой.</span><span class="sxs-lookup"><span data-stu-id="4273d-291">Texels 2 and 3 pass the depth test, while Texel 1 fails.</span></span>

### <a name="calculating-a-per-texel-depth-bias-with-ddx-and-ddy-for-large-pcfs"></a><span data-ttu-id="4273d-292">Вычисление смещения глубины Per-Texel с помощью DDX и ДДИ для крупных Пкфс</span><span class="sxs-lookup"><span data-stu-id="4273d-292">Calculating a Per-Texel Depth Bias with DDX and DDY for Large PCFs</span></span>

<span data-ttu-id="4273d-293">Вычисление смещения глубины шаг текселя с помощью **DDX** и **ДДИ** для крупных пкфс — это метод, который вычисляет правильную глубину глубины (предполагая, что поверхность плоская) для смежной теневой схемы шаг текселя.</span><span class="sxs-lookup"><span data-stu-id="4273d-293">Calculating a per texel depth bias with **ddx** and **ddy** for large PCFs is a technique that calculates the correct depth bias—assuming the surface is planar—for the adjacent shadow map texel.</span></span>

<span data-ttu-id="4273d-294">Этот метод соответствует глубине сравнения для плоскости, использующей производные сведения.</span><span class="sxs-lookup"><span data-stu-id="4273d-294">This technique fits the comparison depth to a plane using the derivative information.</span></span> <span data-ttu-id="4273d-295">Поскольку этот метод является сложным, его следует использовать, только если GPU имеет циклы вычислений для запасного.</span><span class="sxs-lookup"><span data-stu-id="4273d-295">Because this technique is computationally complex, it should be used only when a GPU has compute cycles to spare.</span></span> <span data-ttu-id="4273d-296">Если используются очень крупные ядра, это может быть единственная методика, которая позволяет удалить артефакты самотеневого копирования, не вызывая панорамирование Питер.</span><span class="sxs-lookup"><span data-stu-id="4273d-296">When very large kernels are used, this may be the only technique that works to remove self-shadowing artifacts without causing Peter Panning.</span></span>

<span data-ttu-id="4273d-297">На рис. 12 выделяется проблема.</span><span class="sxs-lookup"><span data-stu-id="4273d-297">Figure 12 highlights the problem.</span></span> <span data-ttu-id="4273d-298">Глубина свободного пространства известна для одного шаг текселя, который сравнивается.</span><span class="sxs-lookup"><span data-stu-id="4273d-298">The depth in light-space is known for the one texel that is being compared.</span></span> <span data-ttu-id="4273d-299">Глубина свободного пространства, соответствующая соседним пикселей текстуры на карте глубины, неизвестна.</span><span class="sxs-lookup"><span data-stu-id="4273d-299">The light-space depths that correspond to the neighboring texels in the depth map are unknown.</span></span>

<span data-ttu-id="4273d-300">**Рис. 12. Сцена и схема глубины**</span><span class="sxs-lookup"><span data-stu-id="4273d-300">**Figure 12. Scene and depth map**</span></span>

![Сцена и схема глубины](images/scene-and-depth-map.png)

<span data-ttu-id="4273d-302">Визуализированная сцена показана слева, а схема глубины с примером блока шаг текселя показана справа.</span><span class="sxs-lookup"><span data-stu-id="4273d-302">The rendered scene is shown at left, and the depth map with a sample texel block is shown at right.</span></span> <span data-ttu-id="4273d-303">Шаг текселя пробела сопоставляется с пикселем, обозначенным D в центре блока.</span><span class="sxs-lookup"><span data-stu-id="4273d-303">The eye-space texel maps to the pixel labeled D in the center of the block.</span></span> <span data-ttu-id="4273d-304">Это сравнение является точным.</span><span class="sxs-lookup"><span data-stu-id="4273d-304">This comparison is accurate.</span></span> <span data-ttu-id="4273d-305">Правильная глубина области видимости, связанная с пикселами, неизвестными для соседа D.</span><span class="sxs-lookup"><span data-stu-id="4273d-305">The correct depth in eye space correlating to the pixels that neighbor D is unknown.</span></span> <span data-ttu-id="4273d-306">Сопоставление соседних пикселей текстуры с пространством глаза возможно только в том случае, если предполагается, что пиксель относится к тому же треугольнику, что и D.</span><span class="sxs-lookup"><span data-stu-id="4273d-306">Mapping the neighboring texels back to eye space is possible only if we assume the pixel pertains to the same triangle as D.</span></span>

<span data-ttu-id="4273d-307">Глубина известна для шаг текселя, которая соответствует положению области освещения.</span><span class="sxs-lookup"><span data-stu-id="4273d-307">The depth is known for the texel that correlates with the light-space position.</span></span> <span data-ttu-id="4273d-308">Глубина неизвестна для соседних пикселей текстуры на карте глубины.</span><span class="sxs-lookup"><span data-stu-id="4273d-308">The depth is unknown for the neighboring texels in the depth map.</span></span>

<span data-ttu-id="4273d-309">На высоком уровне этот метод использует операции **DDX** и **ДДИ** HLSL для поиска производного места в пространстве.</span><span class="sxs-lookup"><span data-stu-id="4273d-309">At a high level, this technique uses the **ddx** and **ddy** HLSL operations to find the derivative of the light-space position.</span></span> <span data-ttu-id="4273d-310">Это нетривиальный способ, поскольку производные операции возвращают градиент глубины светлого пространства относительно пространства экрана.</span><span class="sxs-lookup"><span data-stu-id="4273d-310">This is nontrivial because the derivative operations return the gradient of the light-space depth with respect to screen space.</span></span> <span data-ttu-id="4273d-311">Чтобы преобразовать это значение в градиент глубины освещения относительно пустого пространства, необходимо вычислить матрицу преобразования.</span><span class="sxs-lookup"><span data-stu-id="4273d-311">To convert this to a gradient of the light-space depth with respect to light space, a conversion matrix must be calculated.</span></span>

### <a name="explanation-with-shader-code"></a><span data-ttu-id="4273d-312">Объяснение с помощью кода шейдера</span><span class="sxs-lookup"><span data-stu-id="4273d-312">Explanation with Shader Code</span></span>

<span data-ttu-id="4273d-313">Подробные сведения о остальном алгоритме приведены в пояснении к коду шейдера, который выполняет эту операцию.</span><span class="sxs-lookup"><span data-stu-id="4273d-313">The details of the rest of the algorithm are given as an explanation of the shader code that performs this operation.</span></span> <span data-ttu-id="4273d-314">Этот код можно найти в примере CascadedShadowMaps11.</span><span class="sxs-lookup"><span data-stu-id="4273d-314">This code can be found in the CascadedShadowMaps11 sample.</span></span> <span data-ttu-id="4273d-315">На рис. 13 показано, как координаты текстуры освещения отображают карту глубины и как производные значения в X и Y можно использовать для создания матрицы преобразования.</span><span class="sxs-lookup"><span data-stu-id="4273d-315">Figure 13 shows how the light-space texture coordinates map to the depth map and how the derivatives in X and Y can be used to create a transformation matrix.</span></span>

<span data-ttu-id="4273d-316">**Рис. 13. Пространство на экране для матрицы с небольшими пробелами**</span><span class="sxs-lookup"><span data-stu-id="4273d-316">**Figure 13. Screen-space to light-space matrix**</span></span>

![пространство на экране для матрицы с небольшими пробелами](images/screen-space-to-light-space-matrix.png)

<span data-ttu-id="4273d-318">Для создания этой матрицы используются производные от расположения места в пространстве координат X и Y.</span><span class="sxs-lookup"><span data-stu-id="4273d-318">The derivatives of the light-space position in X and Y are used to create this matrix.</span></span>

<span data-ttu-id="4273d-319">Первым шагом является вычисление производного расположения светлого пространства.</span><span class="sxs-lookup"><span data-stu-id="4273d-319">The first step is to calculate the derivative of the light-view-space position.</span></span>


```C++
          float3 vShadowTexDDX = ddx (vShadowMapTextureCoordViewSpace);
          float3 vShadowTexDDY = ddy (vShadowMapTextureCoordViewSpace);
```



<span data-ttu-id="4273d-320">Процессоры класса Direct3D 11 вычисляют эти производные, выполняя 2 × 2 четыре пикселя параллельно и вычитая координаты текстуры из соседа в X для **DDX** и из соседа в Y для **ДДИ**.</span><span class="sxs-lookup"><span data-stu-id="4273d-320">Direct3D 11 class GPUs calculate these derivatives by running 2 × 2 quad of pixels in parallel and subtracting the texture coordinates from the neighbor in X for **ddx** and from the neighbor in Y for **ddy**.</span></span> <span data-ttu-id="4273d-321">Эти два производных класса составляют строки матрицы размером 2 × 2.</span><span class="sxs-lookup"><span data-stu-id="4273d-321">These two derivatives make up the rows of a 2 × 2 matrix.</span></span> <span data-ttu-id="4273d-322">В текущей форме эту матрицу можно использовать для преобразования пространства экрана, соседних пикселов, в наклоненной.</span><span class="sxs-lookup"><span data-stu-id="4273d-322">In its current form, this matrix could be used to convert screen-space neighboring pixels to light-space slopes.</span></span> <span data-ttu-id="4273d-323">Однако требуется обратная часть этой матрицы.</span><span class="sxs-lookup"><span data-stu-id="4273d-323">However, the inverse of this matrix is needed.</span></span> <span data-ttu-id="4273d-324">Матрица, которая преобразует наклоненной, соседние пиксели, в пространстве экрана.</span><span class="sxs-lookup"><span data-stu-id="4273d-324">A matrix that transforms light-space neighboring pixels to screen-space slopes is needed.</span></span>


```C++
          float2x2 matScreentoShadow = float2x2( vShadowTexDDX.xy, vShadowTexDDY.xy );
          float fInvDeterminant = 1.0f / fDeterminant;

          float2x2 matShadowToScreen = float2x2 (
          matScreentoShadow._22 * fInvDeterminant,
          matScreentoShadow._12 * -fInvDeterminant,
          matScreentoShadow._21 * -fInvDeterminant,
          matScreentoShadow._11 * fInvDeterminant );
```



<span data-ttu-id="4273d-325">**Рис. 14. Свободное пространство на экране**</span><span class="sxs-lookup"><span data-stu-id="4273d-325">**Figure 14. Light-space to screen-space**</span></span>

![свободное пространство на экране](images/light-space-to-screen-space.png)

<span data-ttu-id="4273d-327">Эта матрица затем используется для преобразования двух пикселей текстуры выше и справа от текущего шаг текселя.</span><span class="sxs-lookup"><span data-stu-id="4273d-327">This matrix is then used to transform the two texels above and to the right of the current texel.</span></span> <span data-ttu-id="4273d-328">Эти соседи представлены в виде смещения от текущего шаг текселя.</span><span class="sxs-lookup"><span data-stu-id="4273d-328">These neighbors are represented as an offset from the current texel.</span></span>


```C++
          float2 vRightShadowTexelLocation = float2( m_fTexelSize, 0.0f );
          float2 vUpShadowTexelLocation = float2( 0.0f, m_fTexelSize );
          float2 vRightTexelDepthRatio = mul( vRightShadowTexelLocation,
          matShadowToScreen );
          float2 vUpTexelDepthRatio = mul( vUpShadowTexelLocation,
          matShadowToScreen );
```



<span data-ttu-id="4273d-329">Соотношение, которое создает матрица, в итоге умножается на производные от глубины, чтобы вычислить смещения глубины для соседних пикселов.</span><span class="sxs-lookup"><span data-stu-id="4273d-329">The ratio that the matrix creates is finally multiplied by the depth derivatives to calculate the depth offsets for the neighboring pixels.</span></span>


```C++
            float fUpTexelDepthDelta =
            vUpTexelDepthRatio.x * vShadowTexDDX.z
            + vUpTexelDepthRatio.y * vShadowTexDDY.z;
            float fRightTexelDepthDelta =
            vRightTexelDepthRatio.x * vShadowTexDDX.z
            + vRightTexelDepthRatio.y * vShadowTexDDY.z;
```



<span data-ttu-id="4273d-330">Теперь эти весовые коэффициенты можно использовать в цикле PCF для добавления смещения к позиции.</span><span class="sxs-lookup"><span data-stu-id="4273d-330">These weights can now be used in a PCF loop to add an offset to the position.</span></span>


```C++
    for( int x = m_iPCFBlurForLoopStart; x < m_iPCFBlurForLoopEnd; ++x ) 
    {
        for( int y = m_iPCFBlurForLoopStart; y < m_iPCFBlurForLoopEnd; ++y )
            {
            if ( USE_DERIVATIVES_FOR_DEPTH_OFFSET_FLAG )
            {
            depthcompare += fRightTexelDepthDelta * ( (float) x ) +
            fUpTexelDepthDelta * ( (float) y );
            }
            // Compare the transformed pixel depth to the depth read
            // from the map.
            fPercentLit += g_txShadow.SampleCmpLevelZero( g_samShadow,
            float2(
            vShadowTexCoord.x + ( ( (float) x ) * m_fNativeTexelSizeInX ) ,
            vShadowTexCoord.y + ( ( (float) y ) * m_fTexelSize )
            ),
            depthcompare
            );
            }
     }
```



## <a name="pcf-and-csms"></a><span data-ttu-id="4273d-331">PCF и Ксмс</span><span class="sxs-lookup"><span data-stu-id="4273d-331">PCF and CSMs</span></span>

<span data-ttu-id="4273d-332">PCF не работает с массивами текстур в Direct3D 10.</span><span class="sxs-lookup"><span data-stu-id="4273d-332">PCF does not work on texture arrays in Direct3D 10.</span></span> <span data-ttu-id="4273d-333">Чтобы использовать PCF, все каскады хранятся в одной большой текстуре Atlas.</span><span class="sxs-lookup"><span data-stu-id="4273d-333">To use PCF, all of the cascades are stored in one large texture atlas.</span></span>

### <a name="derivative-based-offset"></a><span data-ttu-id="4273d-334">Смещение Derivative-Based</span><span class="sxs-lookup"><span data-stu-id="4273d-334">Derivative-Based Offset</span></span>

<span data-ttu-id="4273d-335">Добавление смещений на основе производных для Ксмс представляет некоторые трудности.</span><span class="sxs-lookup"><span data-stu-id="4273d-335">Adding the derivative based offsets for CSMs presents some challenges.</span></span> <span data-ttu-id="4273d-336">Это обусловлено производным вычислением в отдельном потоке управления.</span><span class="sxs-lookup"><span data-stu-id="4273d-336">This is due to a derivative calculation within divergent flow control.</span></span> <span data-ttu-id="4273d-337">Проблема возникает из-за фундаментального способа работы GPU.</span><span class="sxs-lookup"><span data-stu-id="4273d-337">The problem occurs because of a fundamental way that GPUs operate.</span></span> <span data-ttu-id="4273d-338">Direct3D11 GPU работают в 2 × 2 четырех пикселях.</span><span class="sxs-lookup"><span data-stu-id="4273d-338">Direct3D11 GPUs operate on 2 × 2 quads of pixels.</span></span> <span data-ttu-id="4273d-339">Чтобы выполнить производный, GPU, как правило, вычитают копию переменной текущего пикселя из копии этой же переменной на соседнем пикселе.</span><span class="sxs-lookup"><span data-stu-id="4273d-339">To perform a derivative, GPUs generally subtract the current pixel's copy of a variable from the neighboring pixel's copy of that same variable.</span></span> <span data-ttu-id="4273d-340">Как это происходит от GPU до GPU.</span><span class="sxs-lookup"><span data-stu-id="4273d-340">How this happens varies from GPU to GPU.</span></span> <span data-ttu-id="4273d-341">Координаты текстуры определяются каскадным выделением на основе карт или на основе интервалов.</span><span class="sxs-lookup"><span data-stu-id="4273d-341">The texture coordinates are determined by map-based or interval-based cascade selection.</span></span> <span data-ttu-id="4273d-342">Некоторые Пиксели в пикселе имеют разную каскадную, чем остальные Пиксели.</span><span class="sxs-lookup"><span data-stu-id="4273d-342">Some pixels in a pixel quad choose a different cascade than the rest of the pixels.</span></span> <span data-ttu-id="4273d-343">Это приводит к видимым стыкам между теневыми картами, так как производные смещения теперь являются совершенно неправильными.</span><span class="sxs-lookup"><span data-stu-id="4273d-343">This results in visible seams between shadow maps because the derivative-based offsets are now completely wrong.</span></span> <span data-ttu-id="4273d-344">Решение состоит в том, чтобы выполнить производную на координатах текстуры освещения незанятого пространства.</span><span class="sxs-lookup"><span data-stu-id="4273d-344">The solution is to perform the derivative on light-view space texture coordinates.</span></span> <span data-ttu-id="4273d-345">Эти координаты одинаковы для каждого каскада.</span><span class="sxs-lookup"><span data-stu-id="4273d-345">These coordinates are the same for every cascade.</span></span>

### <a name="padding-for-pcf-kernels"></a><span data-ttu-id="4273d-346">Заполнение для ядер PCF</span><span class="sxs-lookup"><span data-stu-id="4273d-346">Padding for PCF Kernels</span></span>

<span data-ttu-id="4273d-347">PCF ядра индекса за пределами секции Cascade, если теневой буфер не заполнен.</span><span class="sxs-lookup"><span data-stu-id="4273d-347">PCF kernels index outside of a cascade partition if the shadow buffer is not padded.</span></span> <span data-ttu-id="4273d-348">Решение заключается в том, чтобы заполнить наружную rimную часть каскадом на половину размера ядра PCF.</span><span class="sxs-lookup"><span data-stu-id="4273d-348">The solution is to pad the outer rim of the cascade by one-half the size of the PCF kernel.</span></span> <span data-ttu-id="4273d-349">Эта возможность должна быть реализована в шейдере, который выбирает Каскад и в матрице проекции, которая должна отображать каскадную, достаточно большой для сохранения границы.</span><span class="sxs-lookup"><span data-stu-id="4273d-349">This must be implemented in the shader that selects the cascade and in the projection matrix that must render the cascade large enough that the border is preserved.</span></span>

## <a name="variance-shadow-maps"></a><span data-ttu-id="4273d-350">Теневые карты отклонений</span><span class="sxs-lookup"><span data-stu-id="4273d-350">Variance Shadow Maps</span></span>

<span data-ttu-id="4273d-351">ВСМС (Дополнительные сведения см. в разделе [отклонение теневых карт](https://portal.acm.org/citation.cfm?doid=1111411.1111440) по Доннелли и лауритзен). включите фильтрацию прямого теневого отображения.</span><span class="sxs-lookup"><span data-stu-id="4273d-351">VSMs (see [Variance shadow maps](https://portal.acm.org/citation.cfm?doid=1111411.1111440) by Donnelly and Lauritzen for more information) enable direct shadow map filtering.</span></span> <span data-ttu-id="4273d-352">При использовании ВСМС можно использовать все возможности оборудования, поддерживающего фильтрацию текстур.</span><span class="sxs-lookup"><span data-stu-id="4273d-352">When using VSMs, all of the power of the texture-filtering hardware can be used.</span></span> <span data-ttu-id="4273d-353">Можно использовать фильтрацию трилинейной и анизотропный (рис. 15).</span><span class="sxs-lookup"><span data-stu-id="4273d-353">Trilinear and anisotropic (Figure 15) filtering can be used.</span></span> <span data-ttu-id="4273d-354">Кроме того, ВСМС может быть размыт напрямую через свертывание.</span><span class="sxs-lookup"><span data-stu-id="4273d-354">Additionally, VSMs can be blurred directly through convolution.</span></span> <span data-ttu-id="4273d-355">ВСМС имеют некоторые недостатки. необходимо хранить два канала данных глубины (с глубиной и глубиной в квадрате).</span><span class="sxs-lookup"><span data-stu-id="4273d-355">VSMs do have some drawbacks; two channels of depth data must be stored (depth and depth squared).</span></span> <span data-ttu-id="4273d-356">Когда тени перекрываются, светло-суперсовременные является наиболее распространенным.</span><span class="sxs-lookup"><span data-stu-id="4273d-356">When shadows overlap, light-bleeding is common.</span></span> <span data-ttu-id="4273d-357">Однако они хорошо работают с более низкими разрешениями и могут сочетаться с Ксмс.</span><span class="sxs-lookup"><span data-stu-id="4273d-357">They work well, however, with lower resolutions and can be combined with CSMs.</span></span>

<span data-ttu-id="4273d-358">**Рис. 15. Анизотропная фильтрация**</span><span class="sxs-lookup"><span data-stu-id="4273d-358">**Figure 15. Anisotropic filtering**</span></span>

![Анизотропная фильтрация](images/anisotropic-filtering.png)

### <a name="algorithm-details"></a><span data-ttu-id="4273d-360">Подробные сведения об алгоритмах</span><span class="sxs-lookup"><span data-stu-id="4273d-360">Algorithm Details</span></span>

<span data-ttu-id="4273d-361">ВСМС работу, выполнив визуализацию глубины и глубины в квадрате на основе схемы с двумя каналами.</span><span class="sxs-lookup"><span data-stu-id="4273d-361">VSMs work by rendering the depth and the depth squared to a two-channel shadow map.</span></span> <span data-ttu-id="4273d-362">Затем эту схему теневой схемы с двумя каналами можно сделать размытой и отфильтровать так же, как нормальная текстура.</span><span class="sxs-lookup"><span data-stu-id="4273d-362">This two-channel shadow map can then be blurred and filtered just like a normal texture.</span></span> <span data-ttu-id="4273d-363">Затем алгоритм использует неравенство Чебичев в шейдере пикселей для оценки доли области в пикселях, которая будет проходить тест глубины.</span><span class="sxs-lookup"><span data-stu-id="4273d-363">The algorithm then uses Chebychev's Inequality in the pixel shader to estimate the fraction of pixel area that would pass the depth test.</span></span>

<span data-ttu-id="4273d-364">Построитель текстуры получает значения глубины и глубины в квадратах.</span><span class="sxs-lookup"><span data-stu-id="4273d-364">The pixel shader fetches the depth and depth-squared values.</span></span>


```C++
        float  fAvgZ  = mapDepth.x; // Filtered z
        float  fAvgZ2 = mapDepth.y; // Filtered z-squared
```



<span data-ttu-id="4273d-365">Выполняется сравнение глубины.</span><span class="sxs-lookup"><span data-stu-id="4273d-365">The depth comparison is performed.</span></span>


```C++
        if ( fDepth <= fAvgZ )
        {
        fPercentLit = 1;
        }
```



<span data-ttu-id="4273d-366">Если сравнение глубины завершается неудачно, то вычисляется процентная доля освещенного пикселя.</span><span class="sxs-lookup"><span data-stu-id="4273d-366">If the depth comparison fails, the percentage of the pixel that is lit is estimated.</span></span> <span data-ttu-id="4273d-367">Дисперсия вычисляется как среднее значение минус квадраты.</span><span class="sxs-lookup"><span data-stu-id="4273d-367">Variance is calculated as average-of-squares minus square-of-average.</span></span>


```C++
        float variance = ( fAvgZ2 ) − ( fAvgZ * fAvgZ );
        variance = min( 1.0f, max( 0.0f, variance + 0.00001f ) );
```



<span data-ttu-id="4273d-368">Значение Фперцентлит оценивается как неравенство Чебичев.</span><span class="sxs-lookup"><span data-stu-id="4273d-368">The fPercentLit value is estimated with Chebychev's Inequality.</span></span>


```C++
        float mean           = fAvgZ;
        float d              = fDepth - mean;
        float fPercentLit    = variance / ( variance + d*d );
```



## <a name="light-bleeding"></a><span data-ttu-id="4273d-369">Светло суперсовременные</span><span class="sxs-lookup"><span data-stu-id="4273d-369">Light Bleeding</span></span>

<span data-ttu-id="4273d-370">Самый большой недостаток ВСМС — светло суперсовременные (рис. 16).</span><span class="sxs-lookup"><span data-stu-id="4273d-370">The biggest drawback to VSMs is light bleeding (Figure 16).</span></span> <span data-ttu-id="4273d-371">Легкая суперсовременные возникает, когда несколько теней окклуде друг с другом вдоль краев.</span><span class="sxs-lookup"><span data-stu-id="4273d-371">Light bleeding occurs when multiple shadow casters occlude each other along edges.</span></span> <span data-ttu-id="4273d-372">ВСМС затениет края темных элементов на основе неосторожностей глубины.</span><span class="sxs-lookup"><span data-stu-id="4273d-372">VSMs shade the edges of shadows based on depth disparities.</span></span> <span data-ttu-id="4273d-373">Когда тени перекрываются, в центре области, которая должна быть скрыта, существует несоответствие глубины.</span><span class="sxs-lookup"><span data-stu-id="4273d-373">When shadows overlap each other, a depth disparity exists in the center of a region that should be shadowed.</span></span> <span data-ttu-id="4273d-374">Это проблема использования алгоритма VSM.</span><span class="sxs-lookup"><span data-stu-id="4273d-374">This is a problem with using the VSM algorithm.</span></span>

<span data-ttu-id="4273d-375">**Рис. 16. VSM Light суперсовременные**</span><span class="sxs-lookup"><span data-stu-id="4273d-375">**Figure 16. VSM light bleeding**</span></span>

![VSM Light суперсовременные](images/vsm-light-bleeding.png)

<span data-ttu-id="4273d-377">Частичное решение проблемы заключается в том, чтобы подать Фперцентлит в степень.</span><span class="sxs-lookup"><span data-stu-id="4273d-377">A partial solution to the problem is to raise the fPercentLit to a power.</span></span> <span data-ttu-id="4273d-378">Это приводит к ослаблению размытия, что может вызвать артефакты с небольшими нарушениями в глубине.</span><span class="sxs-lookup"><span data-stu-id="4273d-378">This has the effect of dampening the blur, which can cause artifacts where depth disparity is small.</span></span> <span data-ttu-id="4273d-379">Иногда существует значение Magical, которое устраняет проблему.</span><span class="sxs-lookup"><span data-stu-id="4273d-379">Sometimes there exists a magical value that alleviates the problem.</span></span>


```C++
fPercentLit = pow( p_max, MAGIC_NUMBER );
```



<span data-ttu-id="4273d-380">Альтернативой порождению процента освещенности мощности является избежание конфигураций, в которых тени перекрываются.</span><span class="sxs-lookup"><span data-stu-id="4273d-380">An alternative to raising the percent lit to a power is to avoid configurations where shadows overlap.</span></span> <span data-ttu-id="4273d-381">Даже высоко настроенные теневые конфигурации имеют несколько ограничений на освещение, камеру и геометрию.</span><span class="sxs-lookup"><span data-stu-id="4273d-381">Even highly tuned shadow configurations have several constraints on light, camera, and geometry.</span></span> <span data-ttu-id="4273d-382">Светло суперсовременные также уменьшается с помощью текстур с более высоким разрешением.</span><span class="sxs-lookup"><span data-stu-id="4273d-382">Light bleeding is also lessened by using higher resolution textures.</span></span>

<span data-ttu-id="4273d-383">Многоуровневые теневые карты расхождений (Лвсмс) позволяют решить проблему за счет нарушения фрустум в слоях, перпендикулярных источнику.</span><span class="sxs-lookup"><span data-stu-id="4273d-383">Layered variance shadow maps (LVSMs) solve the problem at the expense of breaking the frustum into layers that are perpendicular to the light.</span></span> <span data-ttu-id="4273d-384">Количество необходимых карт будет довольно большим, если Ксмс также используются.</span><span class="sxs-lookup"><span data-stu-id="4273d-384">The number of maps required would be quite large when CSMs are also being used.</span></span>

<span data-ttu-id="4273d-385">Кроме того, Эндрю Лауритзен, соавтор бумаги на ВСМС и автор документа на Лвсмс, обсуждая сочетание экспоненциальной теневой карты (Есмс) с ВСМС, чтобы противося нелегкому смешению на [форуме Beyond3D](https://forum.beyond3d.com/showthread.php?t=47427).</span><span class="sxs-lookup"><span data-stu-id="4273d-385">Additionally, Andrew Lauritzen, co-author of the paper on VSMs, and author of a paper on LVSMs, discussed combining exponential shadow maps (ESMs) with VSMs to counteract light blending in a [Beyond3D Forum](https://forum.beyond3d.com/showthread.php?t=47427).</span></span>

## <a name="vsms-with-csms"></a><span data-ttu-id="4273d-386">ВСМС с Ксмс</span><span class="sxs-lookup"><span data-stu-id="4273d-386">VSMs with CSMs</span></span>

<span data-ttu-id="4273d-387">В примере VarianceShadow11 объединяются ВСМС и Ксмс.</span><span class="sxs-lookup"><span data-stu-id="4273d-387">The sample VarianceShadow11 combines VSMs and CSMs.</span></span> <span data-ttu-id="4273d-388">Это сочетание довольно просто.</span><span class="sxs-lookup"><span data-stu-id="4273d-388">The combination is fairly straightforward.</span></span> <span data-ttu-id="4273d-389">Пример соответствует тем же действиям, что и образец CascadedShadowMaps11.</span><span class="sxs-lookup"><span data-stu-id="4273d-389">The sample follows the same steps as the CascadedShadowMaps11 sample.</span></span> <span data-ttu-id="4273d-390">Поскольку PCF не используется, тени преобразуются в отделяемыхй свертки.</span><span class="sxs-lookup"><span data-stu-id="4273d-390">Because PCF is not used, the shadows are blurred in a two-pass separable convolution.</span></span> <span data-ttu-id="4273d-391">Не используйте PCF также позволяет образцу использовать массивы текстур вместо текстуры Atlas.</span><span class="sxs-lookup"><span data-stu-id="4273d-391">Not using PCF also enables the sample to use texture arrays instead of a texture atlas.</span></span> <span data-ttu-id="4273d-392">PCF на массивах текстур — это функция Direct3D 10,1.</span><span class="sxs-lookup"><span data-stu-id="4273d-392">PCF on texture arrays is a Direct3D 10.1 feature.</span></span>

### <a name="gradients-with-csms"></a><span data-ttu-id="4273d-393">Градиенты с Ксмс</span><span class="sxs-lookup"><span data-stu-id="4273d-393">Gradients with CSMs</span></span>

<span data-ttu-id="4273d-394">Использование градиентов с Ксмс может создать стык вдоль границы между двумя каскадными таблицами, как показано на рис. 17.</span><span class="sxs-lookup"><span data-stu-id="4273d-394">Using gradients with CSMs can produce a seam along the border between two cascades as seen in Figure 17.</span></span> <span data-ttu-id="4273d-395">В образце инструкции используются производные между пикселями для вычисления информации, например уровня mipmap, необходимого для фильтра.</span><span class="sxs-lookup"><span data-stu-id="4273d-395">The sample instruction uses derivatives between pixels to calculate information, such as the mipmap level, needed by the filter.</span></span> <span data-ttu-id="4273d-396">Это вызывает проблему в частности для выбора mipmap или анизотропной фильтрации.</span><span class="sxs-lookup"><span data-stu-id="4273d-396">This causes a problem in particular for mipmap selection or anisotropic filtering.</span></span> <span data-ttu-id="4273d-397">Когда в построителе пикселей четыре ветви в шейдере, производные от оборудования GPU недопустимы.</span><span class="sxs-lookup"><span data-stu-id="4273d-397">When pixels in a quad take different branches in the shader, the derivatives calculated by the GPU hardware are invalid.</span></span> <span data-ttu-id="4273d-398">Это приводит к неровному стыку на теневой карте.</span><span class="sxs-lookup"><span data-stu-id="4273d-398">This results in a jagged seam along the shadow map.</span></span>

<span data-ttu-id="4273d-399">**Рис. 17. Стыки на каскадных границах из-за анизотропной фильтрации с использованием других элементов управления потоком**</span><span class="sxs-lookup"><span data-stu-id="4273d-399">**Figure 17. Seams on cascade borders due to anisotropic filtering with divergent flow control**</span></span>

![стыки на каскадных границах из-за анизотропной фильтрации с использованием других элементов управления потоком](images/seams-on-cascade-borders-due-to-anisotropic.jpg)

<span data-ttu-id="4273d-401">Эту проблему можно решить, вычисляя производные от места в свободном месте. Координата недостаточного пространства не зависит от выбранного каскадного представления.</span><span class="sxs-lookup"><span data-stu-id="4273d-401">This problem is solved by computing the derivatives on the position in light-view space; the light-view space coordinate is not specific to the selected cascade.</span></span> <span data-ttu-id="4273d-402">Вычисленные производные массивы могут масштабироваться по части шкалы матрицы проекций текстур до правильного уровня mipmap.</span><span class="sxs-lookup"><span data-stu-id="4273d-402">The computed derivatives can be scaled by the scale portion of the projection-texture matrix to the correct mipmap level.</span></span>


```C++
        float3 vShadowTexCoordDDX = ddx( vShadowMapTextureCoordViewSpace );
        vShadowTexCoordDDX *= m_vCascadeScale[iCascade].xyz;
        float3 vShadowTexCoordDDY = ddy( vShadowMapTextureCoordViewSpace );
        vShadowTexCoordDDY *= m_vCascadeScale[iCascade].xyz;

        mapDepth += g_txShadow.SampleGrad( g_samShadow, vShadowTexCoord.xyz,
        vShadowTexCoordDDX, vShadowTexCoordDDY );
```



## <a name="vsms-compared-to-standard-shadows-with-pcf"></a><span data-ttu-id="4273d-403">ВСМС по сравнению со стандартными тенями с PCF</span><span class="sxs-lookup"><span data-stu-id="4273d-403">VSMs Compared to Standard Shadows with PCF</span></span>

<span data-ttu-id="4273d-404">И ВСМС, и PCF попытаются приблизительно оценить долю пиксельной области, которая будет проходить тест глубины.</span><span class="sxs-lookup"><span data-stu-id="4273d-404">Both VSMs and PCF attempt to approximate the fraction of pixel area that would pass the depth test.</span></span> <span data-ttu-id="4273d-405">ВСМС работает с фильтрацией оборудования и может быть размыт с помощью ядер отделяемых.</span><span class="sxs-lookup"><span data-stu-id="4273d-405">VSMs work with filtering hardware and can be blurred with separable kernels.</span></span> <span data-ttu-id="4273d-406">Ядрам свертки отделяемых значительно дешевле для реализации, чем для полного ядра.</span><span class="sxs-lookup"><span data-stu-id="4273d-406">Separable convolution kernels are considerably cheaper to implement than a full kernel.</span></span> <span data-ttu-id="4273d-407">Кроме того, ВСМС сравнивает одну глубину свободного пространства с одним значением на карте глубины свободного пространства.</span><span class="sxs-lookup"><span data-stu-id="4273d-407">Additionally, VSMs compare one light-space depth against one value in the light-space depth map.</span></span> <span data-ttu-id="4273d-408">Это означает, что ВСМС не имеют тех же проблем со смещением, что и PCF.</span><span class="sxs-lookup"><span data-stu-id="4273d-408">This means that VSMs do not have the same offset problems as PCF.</span></span> <span data-ttu-id="4273d-409">Технически, ВСМС — это глубина выборки в большей области, а также выполнение статистического анализа.</span><span class="sxs-lookup"><span data-stu-id="4273d-409">Technically, VSMs are sampling depth over a greater area, as well as performing a statistical analysis.</span></span> <span data-ttu-id="4273d-410">Это менее точное, чем PCF.</span><span class="sxs-lookup"><span data-stu-id="4273d-410">This is less precise than PCF.</span></span> <span data-ttu-id="4273d-411">На практике ВСМС выполняет очень хорошее задание смешения, что приводит к меньшему смещению.</span><span class="sxs-lookup"><span data-stu-id="4273d-411">In practice, VSMs do a very good job of blending, which results in less offset being necessary.</span></span> <span data-ttu-id="4273d-412">Как описано выше, число, которое один недостаток в ВСМС, является светлой суперсовременные.</span><span class="sxs-lookup"><span data-stu-id="4273d-412">As described above, the number one drawback to VSMs is light bleeding.</span></span>

<span data-ttu-id="4273d-413">ВСМС и PCF представляют компромисс между производительностью вычислений GPU и текстурой GPU.</span><span class="sxs-lookup"><span data-stu-id="4273d-413">VSMs and PCF represent a trade-off between GPU compute power and GPU texture bandwidth.</span></span> <span data-ttu-id="4273d-414">Для вычисления дисперсии ВСМС требуется больше математических вычислений.</span><span class="sxs-lookup"><span data-stu-id="4273d-414">VSMs require more math to be performed to calculate the variance.</span></span> <span data-ttu-id="4273d-415">PCF требует больше пропускной способности текстурной памяти.</span><span class="sxs-lookup"><span data-stu-id="4273d-415">PCF requires more texture memory bandwidth.</span></span> <span data-ttu-id="4273d-416">Большие ядра PCF могут быстро стать узким местом по пропускной способности текстуры.</span><span class="sxs-lookup"><span data-stu-id="4273d-416">Large PCF kernels can quickly become bottlenecked by texture bandwidth.</span></span> <span data-ttu-id="4273d-417">Так как вычислительные мощности GPU растут более быстро, чем пропускная способность GPU, ВСМС становится более практичной из двух алгоритмов.</span><span class="sxs-lookup"><span data-stu-id="4273d-417">With GPU computation power growing more rapidly than GPU bandwidth, VSMs are becoming the more practical of the two algorithms.</span></span> <span data-ttu-id="4273d-418">ВСМС также лучше рассмотреть теневые карты с более низким разрешением из-за смешения и фильтрации.</span><span class="sxs-lookup"><span data-stu-id="4273d-418">VSMs also look better with lower resolution shadow maps due to blending and filtering.</span></span>

## <a name="summary"></a><span data-ttu-id="4273d-419">Сводка</span><span class="sxs-lookup"><span data-stu-id="4273d-419">Summary</span></span>

<span data-ttu-id="4273d-420">Ксмс предлагают решение проблемы с псевдонимом перспективы.</span><span class="sxs-lookup"><span data-stu-id="4273d-420">CSMs offer a solution to the perspective aliasing problem.</span></span> <span data-ttu-id="4273d-421">Существует несколько возможных конфигураций для получения необходимой визуальной точности заголовка.</span><span class="sxs-lookup"><span data-stu-id="4273d-421">There are several possible configurations to get the needed visual fidelity for a title.</span></span> <span data-ttu-id="4273d-422">PCF и ВСМС широко используются и должны сочетаться с Ксмс, чтобы сократить число псевдонимов.</span><span class="sxs-lookup"><span data-stu-id="4273d-422">PCF and VSMs are widely used and should be combined with CSMs to reduce aliasing.</span></span>

## <a name="references"></a><span data-ttu-id="4273d-423">Ссылки</span><span class="sxs-lookup"><span data-stu-id="4273d-423">References</span></span>

<span data-ttu-id="4273d-424">Доннелли, W. и Лауритзен — [теневые карты с дисперсией](https://portal.acm.org/citation.cfm?doid=1111411.1111440).</span><span class="sxs-lookup"><span data-stu-id="4273d-424">Donnelly, W. and Lauritzen, A. [Variance shadow maps](https://portal.acm.org/citation.cfm?doid=1111411.1111440).</span></span> <span data-ttu-id="4273d-425">В SI3D ' 06: материалы 2006 Symposium в интерактивной трехмерной графике и играх.</span><span class="sxs-lookup"><span data-stu-id="4273d-425">In SI3D '06: Proceedings of the 2006 symposium on Interactive 3D graphics and games.</span></span> <span data-ttu-id="4273d-426">2006.</span><span class="sxs-lookup"><span data-stu-id="4273d-426">2006.</span></span> <span data-ttu-id="4273d-427">PP. 161 – 165.</span><span class="sxs-lookup"><span data-stu-id="4273d-427">pp. 161–165.</span></span> <span data-ttu-id="4273d-428">Нью Йорк, Москва, США: ACM Press.</span><span class="sxs-lookup"><span data-stu-id="4273d-428">New York, NY, USA: ACM Press.</span></span>

<span data-ttu-id="4273d-429">Лауритзен, Эндрю и Мккул, Майкл.</span><span class="sxs-lookup"><span data-stu-id="4273d-429">Lauritzen, Andrew and McCool, Michael.</span></span> <span data-ttu-id="4273d-430">[Слоевые теневые карты расхождений](https://portal.acm.org/citation.cfm?id=1375714.1375739&coll=GUIDE&dl=GUIDE&CFID=45360327&CFTOKEN=34578992).</span><span class="sxs-lookup"><span data-stu-id="4273d-430">[Layered variance shadow maps](https://portal.acm.org/citation.cfm?id=1375714.1375739&coll=GUIDE&dl=GUIDE&CFID=45360327&CFTOKEN=34578992).</span></span> <span data-ttu-id="4273d-431">Материалы графического интерфейса 2008, 28 мая – 30, 2008, Windsor, Онтарио, Канада.</span><span class="sxs-lookup"><span data-stu-id="4273d-431">Proceedings of graphics interface 2008, May 28–30, 2008, Windsor, Ontario, Canada.</span></span>

<span data-ttu-id="4273d-432">Енжел, Вофлганг F. раздел 4.</span><span class="sxs-lookup"><span data-stu-id="4273d-432">Engel, Woflgang F. Section 4.</span></span> <span data-ttu-id="4273d-433">Каскадные теневые карты.</span><span class="sxs-lookup"><span data-stu-id="4273d-433">Cascaded Shadow Maps.</span></span> <span data-ttu-id="4273d-434">ShaderX5, дополнительные методы отрисовки, Волфганг F. Енжел, ED.</span><span class="sxs-lookup"><span data-stu-id="4273d-434">ShaderX5 , Advanced Rendering Techniques, Wolfgang F. Engel, Ed.</span></span> <span data-ttu-id="4273d-435">Чарльз River Media, Бостон, Массачусетс.</span><span class="sxs-lookup"><span data-stu-id="4273d-435">Charles River Media, Boston, Massachusetts.</span></span> <span data-ttu-id="4273d-436">2006.</span><span class="sxs-lookup"><span data-stu-id="4273d-436">2006.</span></span> <span data-ttu-id="4273d-437">PP. 197 – 206.</span><span class="sxs-lookup"><span data-stu-id="4273d-437">pp. 197–206.</span></span>

 

 