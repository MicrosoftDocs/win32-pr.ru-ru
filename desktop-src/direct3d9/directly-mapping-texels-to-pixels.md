---
description: При отрисовке двумерных выходных данных с помощью предварительно преобразованных вершин необходимо соблюдать осторожность, чтобы каждая область шаг текселя правильно соответствовала одной области пикселя, в противном случае может произойти искажение текстур.
ms.assetid: 6faeb1e3-ea6e-4cb1-a1e6-2a9a81b4c0c7
title: Прямое сопоставление пикселей текстуры с пикселами (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f86e9d05acff402128ddb83fc97898ff6a21d7c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104262407"
---
# <a name="directly-mapping-texels-to-pixels-direct3d-9"></a><span data-ttu-id="94269-103">Прямое сопоставление пикселей текстуры с пикселами (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="94269-103">Directly Mapping Texels to Pixels (Direct3D 9)</span></span>

<span data-ttu-id="94269-104">При отрисовке двумерных выходных данных с помощью предварительно преобразованных вершин необходимо соблюдать осторожность, чтобы каждая область шаг текселя правильно соответствовала одной области пикселя, в противном случае может произойти искажение текстур.</span><span class="sxs-lookup"><span data-stu-id="94269-104">When rendering 2D output using pre-transformed vertices, care must be taken to ensure that each texel area correctly corresponds to a single pixel area, otherwise texture distortion can occur.</span></span> <span data-ttu-id="94269-105">Изменяя основные принципы процесса, который используется Direct3D для растрирования и текстурирования треугольников, можно убедиться, что приложение Direct3D правильно отображает 2D-выходные данные.</span><span class="sxs-lookup"><span data-stu-id="94269-105">By understanding the basics of the process that Direct3D follows when rasterizing and texturing triangles, you can ensure your Direct3D application correctly renders 2D output.</span></span>

![Иллюстрация экрана разрешения 6x6](images/maptex-fig1.png)

<span data-ttu-id="94269-107">На предыдущей диаграмме показаны пиксели, смоделированные как квадраты.</span><span class="sxs-lookup"><span data-stu-id="94269-107">The preceding diagram shows pixels that are modeled as squares.</span></span> <span data-ttu-id="94269-108">Однако в реальности Пиксели — это точки, а не квадраты.</span><span class="sxs-lookup"><span data-stu-id="94269-108">In reality, however, pixels are dots, not squares.</span></span> <span data-ttu-id="94269-109">Каждый квадрат на предыдущей схеме указывает область, освещенную пикселю, но пиксель всегда является точкой в центре квадрата.</span><span class="sxs-lookup"><span data-stu-id="94269-109">Each square in the preceding diagram indicates the area lit by the pixel, but a pixel is always just a dot at the center of a square.</span></span> <span data-ttu-id="94269-110">Это различие, хотя и кажется небольшим, очень важно.</span><span class="sxs-lookup"><span data-stu-id="94269-110">This distinction, though seemingly small, is important.</span></span> <span data-ttu-id="94269-111">На следующей схеме показана более высокая иллюстрация того же отображения.</span><span class="sxs-lookup"><span data-stu-id="94269-111">A better illustration of the same display is shown in the following diagram.</span></span>

![Иллюстрация экрана, состоящего из пикселей](images/maptex-fig2.png)

<span data-ttu-id="94269-113">На предыдущей схеме каждый физический пиксель отображается правильно в качестве точки в центре каждой ячейки.</span><span class="sxs-lookup"><span data-stu-id="94269-113">The preceding diagram correctly shows each physical pixel as a point in the center of each cell.</span></span> <span data-ttu-id="94269-114">Координата экранного пространства (0, 0) расположена непосредственно в левом верхнем углу и, следовательно, в центре верхней левой ячейки.</span><span class="sxs-lookup"><span data-stu-id="94269-114">The screen space coordinate (0, 0) is located directly at the top-left pixel, and therefore at the center of the top-left cell.</span></span> <span data-ttu-id="94269-115">Таким образом, левый верхний угол отображается в (-0,5,-0,5), так как он равен 0,5 ячейки слева и 0,5 ячейки вверх от верхнего левого пикселя.</span><span class="sxs-lookup"><span data-stu-id="94269-115">The top-left corner of the display is therefore at (-0.5, -0.5) because it is 0.5 cells to the left and 0.5 cells up from the top-left pixel.</span></span> <span data-ttu-id="94269-116">Direct3D выполнит четыре угла с углами в (0, 0) и (4, 4), как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="94269-116">Direct3D will render a quad with corners at (0, 0) and (4, 4), as shown in the following illustration.</span></span>

![Иллюстрация нерастрового изображения с четырьмя значениями (0, 0) и (4, 4)](images/maptex-fig3.png)

<span data-ttu-id="94269-118">На предыдущем рисунке показано, где математические четыре приводятся к отображению, но не показывают, что четыре будут выглядеть, как только Direct3D преобразует его и отправляет на экран.</span><span class="sxs-lookup"><span data-stu-id="94269-118">The preceding illustration shows where the mathematical quad is in relation to the display, but does not show what the quad will look like once Direct3D rasterizes it and sends it to the display.</span></span> <span data-ttu-id="94269-119">На самом деле, Растровое изображение невозможно заполнить четырьмя, как показано, так как края четырех не совпадают с границами между ячейками в пикселях.</span><span class="sxs-lookup"><span data-stu-id="94269-119">In fact, it is impossible for a raster display to fill the quad exactly as shown because the edges of the quad do not coincide with the boundaries between pixel cells.</span></span> <span data-ttu-id="94269-120">Иными словами, поскольку каждый пиксель может отображать только один цвет, каждая ячейка пикселя заполняется только одним цветом. Если отрисовка отображалась в точности так, как показано, то в точках с четырьмя краями должно отобразиться два различных цвета: синий, где покрывается только фон.</span><span class="sxs-lookup"><span data-stu-id="94269-120">In other words, because each pixel can only display a single color, each pixel cell is filled with only a single color; if the display were to render the quad exactly as shown, the pixel cells along the quad's edge would need to show two distinct colors: blue where covered by the quad and white where only the background is visible.</span></span>

<span data-ttu-id="94269-121">Вместо этого для графического оборудования устанавливается определение пикселов, которые должны быть приблизительны на четыре.</span><span class="sxs-lookup"><span data-stu-id="94269-121">Instead, the graphics hardware is tasked with determining which pixels should be filled to approximate the quad.</span></span> <span data-ttu-id="94269-122">Этот процесс называется растрирование и подробно описан в [правилах растрирования (Direct3D 9)](rasterization-rules.md).</span><span class="sxs-lookup"><span data-stu-id="94269-122">This process is called rasterization, and is detailed in [Rasterization Rules (Direct3D 9)](rasterization-rules.md).</span></span> <span data-ttu-id="94269-123">В этом конкретном случае растровое восданное изображение показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="94269-123">For this particular case, the rasterized quad is shown in the following illustration.</span></span>

![Иллюстрация нетекстурной нерисованной части (от 0, 0) до (4, 4)](images/maptex-fig4.png)

<span data-ttu-id="94269-125">Обратите внимание, что четыре, передаваемые Direct3D, имеют углы в (0, 0) и (4, 4), но растровые выходные данные (на предыдущем рисунке) имеют углы в (-0.5,-0,5) и (3,5, 3,5).</span><span class="sxs-lookup"><span data-stu-id="94269-125">Note that the quad passed to Direct3D has corners at (0, 0) and (4, 4), but the rasterized output (the preceding illustration) has corners at (-0.5,-0.5) and (3.5,3.5).</span></span> <span data-ttu-id="94269-126">Сравните два приведенных выше рисунка с различиями в отрисовке.</span><span class="sxs-lookup"><span data-stu-id="94269-126">Compare the preceding two illustrations for rendering differences.</span></span> <span data-ttu-id="94269-127">Видно, что отображаемые на самом деле изображения имеют правильный размер, но были смещены на 0,5 ячеек в направлениях x и y.</span><span class="sxs-lookup"><span data-stu-id="94269-127">You can see that what the display actually renders is the correct size, but has been shifted by -0.5 cells in the x and y directions.</span></span> <span data-ttu-id="94269-128">Тем не менее, за исключением многофакторной выборки, это лучшее приближение к четырем.</span><span class="sxs-lookup"><span data-stu-id="94269-128">However, except for multi-sampling techniques, this is the best possible approximation to the quad.</span></span> <span data-ttu-id="94269-129">(Дополнительные сведения о множественной выборки см. в [примере антипсевдонима](https://msdn.microsoft.com/library/Ee415231(v=VS.85).aspx) .) Имейте в виду, что если средство программной прорисовки заполнило каждую ячейку с четырьмя перекрестными крестиками, результирующая область будет иметь размер 5 x 5 вместо требуемых 4 x 4.</span><span class="sxs-lookup"><span data-stu-id="94269-129">(See the [Antialias Sample](https://msdn.microsoft.com/library/Ee415231(v=VS.85).aspx) for thorough coverage of multi-sampling.) Be aware that if the rasterizer filled every cell the quad crossed, the resulting area would be of dimension 5 x 5 instead of the desired 4 x 4.</span></span>

<span data-ttu-id="94269-130">Если предполагается, что экранные координаты поступают в верхний левый угол сетки отображения вместо верхнего левого пикселя, четыре будут выглядеть точно так, как ожидалось.</span><span class="sxs-lookup"><span data-stu-id="94269-130">If you assume that screen coordinates originate at the top-left corner of the display grid instead of the top-left pixel, the quad appears exactly as expected.</span></span> <span data-ttu-id="94269-131">Тем не менее, разница становится ясной, когда для Quad задается текстура.</span><span class="sxs-lookup"><span data-stu-id="94269-131">However, the difference becomes clear when the quad is given a texture.</span></span> <span data-ttu-id="94269-132">На следующем рисунке показана текстура 4 x 4, которая будет напрямую сопоставлена с четырьмя.</span><span class="sxs-lookup"><span data-stu-id="94269-132">The following illustration shows the 4 x 4 texture you'll map directly onto the quad.</span></span>

![Иллюстрация текстуры 4x4](images/maptex-fig5.png)

<span data-ttu-id="94269-134">Так как текстура имеет 4 x 4 пикселей текстуры, а четыре – 4 x 4 пикселя, то, возможно, вы, вероятно, предполагалось, что все, что может показаться, выглядит точно так же, как текстура, независимо от расположения на экране, где нарисована Quad</span><span class="sxs-lookup"><span data-stu-id="94269-134">Because the texture is 4 x 4 texels and the quad is 4 x 4 pixels, you might expect the textured quad to appear exactly like the texture regardless of the location on the screen where the quad is drawn.</span></span> <span data-ttu-id="94269-135">Однако это не так. даже небольшие изменения в положении влияют на отображение текстуры.</span><span class="sxs-lookup"><span data-stu-id="94269-135">However, this is not the case; even slight changes in position influence how the texture is displayed.</span></span> <span data-ttu-id="94269-136">На следующем рисунке показано, как четыре между (0, 0) и (4, 4) отображаются после растрирования и текстурирования.</span><span class="sxs-lookup"><span data-stu-id="94269-136">The following illustration shows how a quad between (0, 0) and (4, 4) is displayed after being rasterized and textured.</span></span>

![Иллюстрация восрисованной четырехъядерной части (0, 0) и (4, 4)](images/maptex-fig6.png)

<span data-ttu-id="94269-138">На предыдущем рисунке показана Текстурная прорисовка (с режимом линейной фильтрации и режимом адресации в виде вектора) с наложенным растровым контуром.</span><span class="sxs-lookup"><span data-stu-id="94269-138">The quad drawn in the preceding illustration shows the textured output (with a linear filtering mode and a clamp addressing mode) with the superimposed rasterized outline.</span></span> <span data-ttu-id="94269-139">В оставшейся части этой статьи объясняется, почему выходные данные выглядят так, как это делается вместо текстуры, но для тех, кто хочет решить это решение: края входных данных должны находиться на границах линий между ячейками.</span><span class="sxs-lookup"><span data-stu-id="94269-139">The rest of this article explains exactly why the output looks the way it does instead of looking like the texture, but for those who want the solution, here it is: The edges of the input quad need to lie upon the boundary lines between pixel cells.</span></span> <span data-ttu-id="94269-140">Путем простого сдвига координат x и y на единицу-0,5, шаг текселя ячейки будут полностью раскрывать пикселные ячейки, а четыре могут быть вполне воссозданы на экране.</span><span class="sxs-lookup"><span data-stu-id="94269-140">By simply shifting the x and y quad coordinates by -0.5 units, texel cells will perfectly cover pixel cells and the quad can be perfectly recreated on the screen.</span></span> <span data-ttu-id="94269-141">(Последнее изображение в этом разделе показывает четыре по исправленным координатам.)</span><span class="sxs-lookup"><span data-stu-id="94269-141">(The last illustration in this topic shows the quad at the corrected coordinates.)</span></span>

<span data-ttu-id="94269-142">Сведения о том, почему растровые выходные данные имеют незначительное сходство с текстурой ввода, напрямую связаны с тем, как Direct3D решает и выбирает текстуры.</span><span class="sxs-lookup"><span data-stu-id="94269-142">The details of why the rasterized output only bears slight resemblance to the input texture are directly related to the way Direct3D addresses and samples textures.</span></span> <span data-ttu-id="94269-143">Далее предполагается, что вы хорошо понимаете [пространство координат текстуры](texture-coordinates.md) и [билинейнойную фильтрацию текстур](bilinear-texture-filtering.md).</span><span class="sxs-lookup"><span data-stu-id="94269-143">What follows assumes you have a good understanding of [texture coordinate space](texture-coordinates.md) And [bilinear texture filtering](bilinear-texture-filtering.md).</span></span>

<span data-ttu-id="94269-144">Вернемся к нашему исследованию странного вывода пикселов, имеет смысл отследить выходной цвет обратно в шейдер пикселей: построитель текстуры вызывается для каждого пикселя, выделенного как часть растровой фигуры.</span><span class="sxs-lookup"><span data-stu-id="94269-144">Getting back to our investigation of the strange pixel output, it makes sense to trace the output color back to the pixel shader: The pixel shader is called for each pixel selected to be part of the rasterized shape.</span></span> <span data-ttu-id="94269-145">Сплошной синий объект, изображенный на предыдущем рисунке, может иметь особенно простой шейдер:</span><span class="sxs-lookup"><span data-stu-id="94269-145">The solid blue quad depicted in an earlier illustration could have a particularly simple shader:</span></span>


```
float4 SolidBluePS() : COLOR
{ 
    return float4( 0, 0, 1, 1 );
} 
```



<span data-ttu-id="94269-146">Для четырехъядерного построителя текстуры необходимо немного изменить:</span><span class="sxs-lookup"><span data-stu-id="94269-146">For the textured quad, the pixel shader has to be changed slightly:</span></span>


```
texture MyTexture;

sampler MySampler = 
sampler_state 
{ 
    Texture = <MyTexture>;
    MinFilter = Linear;
    MagFilter = Linear;
    AddressU = Clamp;
    AddressV = Clamp;
};

float4 TextureLookupPS( float2 vTexCoord : TEXCOORD0 ) : COLOR
{
    return tex2D( MySampler, vTexCoord );
} 
```



<span data-ttu-id="94269-147">Этот код предполагает, что текстура 4 x 4 хранится в Митекстуре.</span><span class="sxs-lookup"><span data-stu-id="94269-147">That code assumes the 4 x 4 texture is stored in MyTexture.</span></span> <span data-ttu-id="94269-148">Как показано ниже, образец текстуры Мисамплер настроен на выполнение фильтрации билинейной на Митекстуре.</span><span class="sxs-lookup"><span data-stu-id="94269-148">As shown, the MySampler texture sampler is set to perform bilinear filtering on MyTexture.</span></span> <span data-ttu-id="94269-149">Построитель текстуры вызывается один раз для каждого растрового пикселя, и каждый раз, когда возвращенный цвет представляет собой образец цвета текстуры в Втекскурд.</span><span class="sxs-lookup"><span data-stu-id="94269-149">The pixel shader gets called once for each rasterized pixel, and each time the returned color is the sampled texture color at vTexCoord.</span></span> <span data-ttu-id="94269-150">Каждый раз при вызове шейдера пикселей аргумент Втекскурд устанавливается в координаты текстуры в этом пикселе.</span><span class="sxs-lookup"><span data-stu-id="94269-150">Each time the pixel shader is called, the vTexCoord argument is set to the texture coordinates at that pixel.</span></span> <span data-ttu-id="94269-151">Это означает, что шейдер запрашивает образец текстуры для фильтрованного цвета текстуры в определенном месте пикселя, как описано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="94269-151">That means the shader is asking the texture sampler for the filtered texture color at the exact location of the pixel, as detailed in the following illustration.</span></span>

![Иллюстрация расположения выборки для координат текстуры](images/maptex-fig7.png)

<span data-ttu-id="94269-153">Текстура (показана наложенная) выводится непосредственно в положениях пикселов (показанных в виде черных точек).</span><span class="sxs-lookup"><span data-stu-id="94269-153">The texture (shown superimposed) is sampled directly at pixel locations (shown as black dots).</span></span> <span data-ttu-id="94269-154">Растровые координаты не зависят от растрирования (они остаются в проектируемом пространстве исходного экрана).</span><span class="sxs-lookup"><span data-stu-id="94269-154">Texture coordinates are not affected by rasterization (they remain in the projected screen-space of the original quad).</span></span> <span data-ttu-id="94269-155">Черные точки показывают, где находятся пикселы растрирования.</span><span class="sxs-lookup"><span data-stu-id="94269-155">The black dots show where the rasterization pixels are.</span></span> <span data-ttu-id="94269-156">Координаты текстуры на каждом пикселе легко определяются путем интерполяции координат, хранящихся на каждой вершине: пиксель в (0, 0) совпадает с вершиной в (0, 0); Таким образом, координаты текстуры в этом пикселе представляют собой просто координаты текстуры, хранящиеся на этой вершине, UV (0,0, 0,0).</span><span class="sxs-lookup"><span data-stu-id="94269-156">The texture coordinates at each pixel are easily determined by interpolating the coordinates stored at each vertex: The pixel at (0,0) coincides with the vertex at (0, 0); therefore, the texture coordinates at that pixel are simply the texture coordinates stored at that vertex, UV (0.0, 0.0).</span></span> <span data-ttu-id="94269-157">Для пикселя в (3, 1) для интерполяции используются UV (0,75, 0,25), так как этот пиксель расположен в трех четвертях от ширины текстуры и одна четвертая из ее высоты.</span><span class="sxs-lookup"><span data-stu-id="94269-157">For the pixel at (3, 1), the interpolated coordinates are UV (0.75, 0.25) because that pixel is located at three-fourths of the texture's width and one-fourth of its height.</span></span> <span data-ttu-id="94269-158">Эти интерполяции координат передаются в шейдер пикселей.</span><span class="sxs-lookup"><span data-stu-id="94269-158">These interpolated coordinates are what get passed to the pixel shader.</span></span>

<span data-ttu-id="94269-159">Пикселей текстуры не выровнять с пикселями в этом примере; Каждый пиксель (и, следовательно, каждая точка выборки) располагается в углу четырех пикселей текстуры.</span><span class="sxs-lookup"><span data-stu-id="94269-159">The texels do not line up with the pixels in this example; each pixel (and therefore each sampling point) is positioned at the corner of four texels.</span></span> <span data-ttu-id="94269-160">Так как для режима фильтрации задано значение линейная, в этом образце будут средниеся цвета четырех пикселей текстуры, совместно использующих этот угол.</span><span class="sxs-lookup"><span data-stu-id="94269-160">Because the filtering mode is set to Linear, the sampler will average the colors of the four texels sharing that corner.</span></span> <span data-ttu-id="94269-161">Это объясняется тем, почему пиксел, ожидаемый красным, на деле состоит из трех четвертых оттенков серого и 1-Четвертый красный, пиксел, который должен быть зеленым, — половина серого плюс один четвертый красный плюс один четвертый зеленый и т. д.</span><span class="sxs-lookup"><span data-stu-id="94269-161">This explains why the pixel expected to be red is actually three-fourths gray plus one-fourth red, the pixel expected to be green is one-half gray plus one-fourth red plus one-fourth green, and so on.</span></span>

<span data-ttu-id="94269-162">Чтобы устранить эту проблему, все, что необходимо сделать, правильно соотнесение к пикселям, на которые она будет растрирования, и таким образом правильно соотнести пикселей текстуры с пикселами.</span><span class="sxs-lookup"><span data-stu-id="94269-162">To fix this problem, all you need to do is correctly map the quad to the pixels to which it will be rasterized, and thereby correctly map the texels to pixels.</span></span> <span data-ttu-id="94269-163">На следующем рисунке показаны результаты рисования одних и тех же четырех чисел (-0,5,-0,5) и (3,5, 3,5), которые являются четырехъядерными.</span><span class="sxs-lookup"><span data-stu-id="94269-163">The following illustration shows the results of drawing the same quad between (-0.5, -0.5) and (3.5, 3.5), which is the quad intended from the outset.</span></span>

![Рисунок с изображением четырех, которые соответствуют растровым четырем](images/maptex-fig8.png)

<span data-ttu-id="94269-165">На предыдущем рисунке показано, что четыре (показанные от (-0,5,-0,5) до (3,5, 3,5)) точно соответствуют растровой области.</span><span class="sxs-lookup"><span data-stu-id="94269-165">The preceding illustration demonstrates that the quad (shown outlined from (-0.5, -0.5) to (3.5, 3.5)) exactly matches the rasterized area.</span></span>

## <a name="summary"></a><span data-ttu-id="94269-166">Сводка</span><span class="sxs-lookup"><span data-stu-id="94269-166">Summary</span></span>

<span data-ttu-id="94269-167">В целом, Пиксели и пикселей текстуры фактически являются точками, а не сплошными блоками.</span><span class="sxs-lookup"><span data-stu-id="94269-167">In summary, pixels and texels are actually points, not solid blocks.</span></span> <span data-ttu-id="94269-168">Область экрана находится в левом верхнем углу, но Координата текстуры начинается в левом верхнего угла сетки текстуры.</span><span class="sxs-lookup"><span data-stu-id="94269-168">Screen space originates at the top-left pixel, but texture coordinates originate at the top-left corner of the texture's grid.</span></span> <span data-ttu-id="94269-169">Что важнее всего, не забывайте вычитать единицы 0,5 из компонентов x и y положений вершин при работе с преобразованным экранным пространством для правильного совмещения пикселей текстуры с пикселами.</span><span class="sxs-lookup"><span data-stu-id="94269-169">Most importantly, remember to subtract 0.5 units from the x and y components of your vertex positions when working in transformed screen space in order to correctly align texels with pixels.</span></span>

<span data-ttu-id="94269-170">Следующий код представляет собой пример смещения вершин в 256 на 256 квадрата для правильного отображения в преобразованном экране текстуры 256 by 256.</span><span class="sxs-lookup"><span data-stu-id="94269-170">The following code is an example of offsetting the vertices of a 256 by 256 square to properly display a 256 by 256 texture in transformed screen space.</span></span>


```C++
//define FVF with vertex values in transformed screen space
#define D3DFVF_CUSTOMVERTEX (D3DFVF_XYZRHW|D3DFVF_TEX1)

struct CUSTOMVERTEX
{
    FLOAT x, y, z, rhw; // position
    FLOAT tu, tv;       // texture coordinates
};

//unadjusted vertex values
float left = 0.0f;
float right = 255.0f;
float top = 0.0f;
float bottom = 255.0f;


//256 by 256 rectangle matching 256 by 256 texture
CUSTOMVERTEX vertices[] =
{
    { left,  top,    0.5f, 1.0f, 0.0f, 0.0f}, // x, y, z, rhw, u, v
    { right, top,    0.5f, 1.0f, 1.0f, 0.0f},
    { right, bottom, 0.5f, 1.0f, 1.0f, 1.0f},
    { left,  top,    0.5f, 1.0f, 0.0f, 0.0f},
    { right, bottom, 0.5f, 1.0f, 1.0f, 1.0f},
    { left,  bottom, 0.5f, 1.0f, 0.0f, 1.0f},
    
};
```




```C++
//adjust all the vertices to correctly line up texels with pixels 
for (int i=0; i<6; i++)
{
    vertices[i].x -= 0.5f;
    vertices[i].y -= 0.5f;
}
```



## <a name="related-topics"></a><span data-ttu-id="94269-171">См. также</span><span class="sxs-lookup"><span data-stu-id="94269-171">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="94269-172">Координаты текстуры</span><span class="sxs-lookup"><span data-stu-id="94269-172">Texture Coordinates</span></span>](texture-coordinates.md)
</dt> </dl>

 

 



