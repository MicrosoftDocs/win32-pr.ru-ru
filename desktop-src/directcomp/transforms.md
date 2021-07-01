---
title: Преобразования (DirectComposition)
description: В этом разделе обсуждается поддержка Microsoft DirectComposition для двухмерных (двумерных) преобразований и описываются типы преобразований, поддерживаемых DirectComposition.
ms.assetid: a0f41cc6-e848-4831-8063-609e17d9b4c6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 991e1205422864efdec82bbd4067b9c7662aaf29
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118659"
---
# <a name="transforms-directcomposition"></a><span data-ttu-id="bb40b-103">Преобразования (DirectComposition)</span><span class="sxs-lookup"><span data-stu-id="bb40b-103">Transforms (DirectComposition)</span></span>

> [!NOTE]
> <span data-ttu-id="bb40b-104">Для приложений в Windows 10 рекомендуется использовать интерфейсы API Windows. UI. компоновки вместо DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="bb40b-104">For apps on Windows 10, we recommend using Windows.UI.Composition APIs instead of DirectComposition.</span></span> <span data-ttu-id="bb40b-105">Дополнительные сведения см. в разделе [модернизировать The классическое приложение с использованием визуального слоя](/windows/uwp/composition/visual-layer-in-desktop-apps).</span><span class="sxs-lookup"><span data-stu-id="bb40b-105">For more info, see [Modernize your desktop app using the Visual layer](/windows/uwp/composition/visual-layer-in-desktop-apps).</span></span>

<span data-ttu-id="bb40b-106">В этом разделе обсуждается поддержка Microsoft DirectComposition для двухмерных (двумерных) преобразований и описываются типы преобразований, поддерживаемых DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="bb40b-106">This topic discusses Microsoft DirectComposition support for two-dimensional (2D) affine (linear) transforms, and describes the types of transforms that DirectComposition supports.</span></span>

<span data-ttu-id="bb40b-107">DirectComposition также поддерживает трехмерные преобразования перспективы, но поскольку они нуждаются в создании промежуточного растрового изображения, DirectComposition считает их эффектными, а не преобразованиями.</span><span class="sxs-lookup"><span data-stu-id="bb40b-107">DirectComposition also supports 3D perspective transforms, but because they require the creation of an intermediate bitmap, DirectComposition considers them to be effects rather than transforms.</span></span> <span data-ttu-id="bb40b-108">Дополнительные сведения об эффектах преобразования трехмерной перспективы см. в разделе [эффекты](effects.md).</span><span class="sxs-lookup"><span data-stu-id="bb40b-108">For information about 3D perspective transform effects, see [Effects](effects.md).</span></span>

<span data-ttu-id="bb40b-109">Этот раздел включает следующие подразделы:</span><span class="sxs-lookup"><span data-stu-id="bb40b-109">This topic includes the following sections:</span></span>

-   [<span data-ttu-id="bb40b-110">Что такое DirectComposition 2D-преобразование?</span><span class="sxs-lookup"><span data-stu-id="bb40b-110">What is a DirectComposition 2D transform?</span></span>](#what-is-a-directcomposition-2d-transform)
-   [<span data-ttu-id="bb40b-111">DirectComposition 2D-координатное пространство</span><span class="sxs-lookup"><span data-stu-id="bb40b-111">The DirectComposition 2D coordinate space</span></span>](#the-directcomposition-2d-coordinate-space)
-   [<span data-ttu-id="bb40b-112">Поддержка аффинных двумерных преобразований</span><span class="sxs-lookup"><span data-stu-id="bb40b-112">Support for affine 2D transforms</span></span>](#support-for-affine-2d-transforms)
-   [<span data-ttu-id="bb40b-113">Двумерные преобразования матрицы</span><span class="sxs-lookup"><span data-stu-id="bb40b-113">Matrix 2D transforms</span></span>](#matrix-2d-transforms)
-   [<span data-ttu-id="bb40b-114">Группы преобразований</span><span class="sxs-lookup"><span data-stu-id="bb40b-114">Transform Groups</span></span>](#transform-groups)
-   [<span data-ttu-id="bb40b-115">Преобразовать анимацию</span><span class="sxs-lookup"><span data-stu-id="bb40b-115">Transform animation</span></span>](#transform-animation)
-   [<span data-ttu-id="bb40b-116">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="bb40b-116">Related topics</span></span>](#related-topics)

## <a name="what-is-a-directcomposition-2d-transform"></a><span data-ttu-id="bb40b-117">Что такое DirectComposition 2D-преобразование?</span><span class="sxs-lookup"><span data-stu-id="bb40b-117">What is a DirectComposition 2D transform?</span></span>

<span data-ttu-id="bb40b-118">2D-преобразование позволяет изменять положение, размер или природу визуального элемента в двух измерениях, перемещая визуальный элемент в другое расположение (перевод), делая его большим или меньшим (масштабирование), включая его (вращение) или искажение фигуры (асимметрия).</span><span class="sxs-lookup"><span data-stu-id="bb40b-118">A 2D transform enables you to alter the position, size, or nature of a visual in two dimensions by moving the visual to another location (translation), making it larger or smaller (scaling), turning it (rotation), or distorting its shape (skewing).</span></span>

<span data-ttu-id="bb40b-119">2D-преобразование достигается путем сопоставления точек визуального элемента от одной позиции к другой внутри одного и того же пространства координат или из одного пространства координат в другое.</span><span class="sxs-lookup"><span data-stu-id="bb40b-119">A 2D transform is achieved by mapping the points of a visual from one position to another within the same coordinate space, or from one coordinate space to another.</span></span> <span data-ttu-id="bb40b-120">Это сопоставление описывается таблицей значений, называемой матрицей преобразования, определенной как коллекция из трех строк с тремя столбцами значений с плавающей запятой, как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="bb40b-120">This mapping is described by a table of values called a transformation matrix, defined as a collection of three rows with three columns of floating-point values as shown in the following table.</span></span>

:::row:::
    :::column:::
        <span data-ttu-id="bb40b-121">M11Default: 1,0</span><span class="sxs-lookup"><span data-stu-id="bb40b-121">M11Default: 1.0</span></span><br/>
        <span data-ttu-id="bb40b-122">M21Default: 0,0</span><span class="sxs-lookup"><span data-stu-id="bb40b-122">M21Default: 0.0</span></span><br/>
        <span data-ttu-id="bb40b-123">M31OffsetX: 0,0</span><span class="sxs-lookup"><span data-stu-id="bb40b-123">M31OffsetX: 0.0</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="bb40b-124">M12Default: 0,0</span><span class="sxs-lookup"><span data-stu-id="bb40b-124">M12Default: 0.0</span></span><br/>
        <span data-ttu-id="bb40b-125">M22Default: 1,0</span><span class="sxs-lookup"><span data-stu-id="bb40b-125">M22Default: 1.0</span></span><br/>
        <span data-ttu-id="bb40b-126">M32OffsetY: 0,0</span><span class="sxs-lookup"><span data-stu-id="bb40b-126">M32OffsetY: 0.0</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="bb40b-127">0,0</span><span class="sxs-lookup"><span data-stu-id="bb40b-127">0.0</span></span><br/>
        <span data-ttu-id="bb40b-128">0,0</span><span class="sxs-lookup"><span data-stu-id="bb40b-128">0.0</span></span><br/>
        <span data-ttu-id="bb40b-129">1,0</span><span class="sxs-lookup"><span data-stu-id="bb40b-129">1.0</span></span>
    :::column-end:::
:::row-end:::

<span data-ttu-id="bb40b-130">Матрица преобразования для аффинных двумерных преобразований представляет собой матрицу размером 3 на 2, которая опускает третий столбец из предыдущей матрицы преобразования.</span><span class="sxs-lookup"><span data-stu-id="bb40b-130">The transformation matrix for affine 2D transforms is a 3-by-2 matrix that omits the third column from the previous transformation matrix.</span></span> <span data-ttu-id="bb40b-131">В следующей таблице показан макет этой матрицы.</span><span class="sxs-lookup"><span data-stu-id="bb40b-131">The following table shows the layout of this matrix.</span></span>

:::row:::
    :::column:::
        <span data-ttu-id="bb40b-132">M11Default: 1,0</span><span class="sxs-lookup"><span data-stu-id="bb40b-132">M11Default: 1.0</span></span><br/>
        <span data-ttu-id="bb40b-133">M21Default: 0,0</span><span class="sxs-lookup"><span data-stu-id="bb40b-133">M21Default: 0.0</span></span><br/>
        <span data-ttu-id="bb40b-134">M31OffsetX: 0,0</span><span class="sxs-lookup"><span data-stu-id="bb40b-134">M31OffsetX: 0.0</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="bb40b-135">M12Default: 0,0</span><span class="sxs-lookup"><span data-stu-id="bb40b-135">M12Default: 0.0</span></span><br/>
        <span data-ttu-id="bb40b-136">M22Default: 1,0</span><span class="sxs-lookup"><span data-stu-id="bb40b-136">M22Default: 1.0</span></span><br/>
        <span data-ttu-id="bb40b-137">M32OffsetY: 0,0</span><span class="sxs-lookup"><span data-stu-id="bb40b-137">M32OffsetY: 0.0</span></span>
    :::column-end:::
:::row-end:::

> [!Note]  
> <span data-ttu-id="bb40b-138">DirectComposition не выполняет специальной обработки при применении 2D-преобразований к стерео-содержимому.</span><span class="sxs-lookup"><span data-stu-id="bb40b-138">DirectComposition does no special processing when applying 2D transforms to stereo content.</span></span> <span data-ttu-id="bb40b-139">Это означает, что при применении к нему 2D-преобразования трехмерное содержимое может показаться искаженным.</span><span class="sxs-lookup"><span data-stu-id="bb40b-139">This means the 3D content might appear distorted when a 2D transform is applied to it.</span></span>

 

## <a name="the-directcomposition-2d-coordinate-space"></a><span data-ttu-id="bb40b-140">DirectComposition 2D-координатное пространство</span><span class="sxs-lookup"><span data-stu-id="bb40b-140">The DirectComposition 2D coordinate space</span></span>

<span data-ttu-id="bb40b-141">В DirectComposition используется левое 2D-пространство координат; то есть положительные значения оси x увеличиваются вправо, а положительные значения оси y увеличиваются вниз.</span><span class="sxs-lookup"><span data-stu-id="bb40b-141">DirectComposition uses a left-handed 2D coordinate space; that is, positive x-axis values increase to the right and positive y-axis values increase downward.</span></span> <span data-ttu-id="bb40b-142">Визуальные элементы располагаются относительно источника, то есть точки, в которой пересекаются ось x и y (0,0), как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="bb40b-142">Visuals are positioned relative to the origin, which is the point where the x-axis and y-axis intersect (0, 0), as shown in the following illustration.</span></span>

![ось x и ось y левого пространства координат](images/coordinatespace.png)

<span data-ttu-id="bb40b-144">Управляя значениями в матрице преобразования объемом 3 по 2, можно поворачивать, масштабировать, отклонять и преобразовывать объекты в двух измерениях.</span><span class="sxs-lookup"><span data-stu-id="bb40b-144">By manipulating values in a 3-by-2 transformation matrix, you can rotate, scale, skew, and translate an object in two dimensions.</span></span> <span data-ttu-id="bb40b-145">Например, если для Оффсеткс задано значение 100, а для параметра offset — 200, то объект перемещается вправо на 100 пикселей и вниз 200 пикселей.</span><span class="sxs-lookup"><span data-stu-id="bb40b-145">For example, if you set OffsetX to 100 and OffsetY to 200, you move the object to the right 100 pixels and down 200 pixels.</span></span>

## <a name="support-for-affine-2d-transforms"></a><span data-ttu-id="bb40b-146">Поддержка аффинных двумерных преобразований</span><span class="sxs-lookup"><span data-stu-id="bb40b-146">Support for affine 2D transforms</span></span>

<span data-ttu-id="bb40b-147">В следующей таблице описаны типы аффинных преобразований, поддерживаемых DirectComposition, и перечислены интерфейсы, которые можно использовать для выполнения различных типов преобразований.</span><span class="sxs-lookup"><span data-stu-id="bb40b-147">The following table describes the types of affine 2D transforms supported by DirectComposition, and lists the interfaces that you can use to perform the various types of transformations.</span></span>



| <span data-ttu-id="bb40b-148">Преобразование или интерфейс</span><span class="sxs-lookup"><span data-stu-id="bb40b-148">Transform/interface</span></span>                                                                               | <span data-ttu-id="bb40b-149">Описание</span><span class="sxs-lookup"><span data-stu-id="bb40b-149">Description</span></span>                                                                                              | <span data-ttu-id="bb40b-150">Иллюстрация</span><span class="sxs-lookup"><span data-stu-id="bb40b-150">Illustration</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb40b-151">Вращение двухмерной [**идкомпоситионротатетрансформ**](/windows/win32/api/dcomp/nn-dcomp-idcompositionrotatetransform) \[ новой строки\]</span><span class="sxs-lookup"><span data-stu-id="bb40b-151">Rotate 2D [**idcompositionrotatetransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionrotatetransform)\[newline\]</span></span>          | <span data-ttu-id="bb40b-152">поворот визуального элемента на указанный угол относительно указанной центральной точки.</span><span class="sxs-lookup"><span data-stu-id="bb40b-152">rotate a visual by the specified angle about the specified center point.</span></span>                                 | ![Иллюстрация квадрата, повернутого на 45 градусов по часовой стрелке относительно центра исходного квадрата](images/rotate.png)               |
| <span data-ttu-id="bb40b-154">Масштабирование строки 2D-[**идкомпоситионскалетрансформ**](/windows/win32/api/dcomp/nn-dcomp-idcompositionscaletransform) \[\]</span><span class="sxs-lookup"><span data-stu-id="bb40b-154">Scale 2D [**idcompositionscaletransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionscaletransform)\[newline\]</span></span>             | <span data-ttu-id="bb40b-155">масштабирование визуального элемента на указанный коэффициент относительно указанной центральной точки.</span><span class="sxs-lookup"><span data-stu-id="bb40b-155">scale a visual by the specified factor about the specified center point.</span></span>                                 | ![Иллюстрация квадратной шкалы 130%](images/scale.png)                                                                  |
| <span data-ttu-id="bb40b-157">Наклон строки 2D [**идкомпоситионскевтрансформ**](/windows/win32/api/dcomp/nn-dcomp-idcompositionskewtransform) \[\]</span><span class="sxs-lookup"><span data-stu-id="bb40b-157">Skew 2D [**idcompositionskewtransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionskewtransform)\[newline\]</span></span>                | <span data-ttu-id="bb40b-158">наклон визуального элемента на указанный угол вдоль оси x и оси y и вокруг указанной центральной точки.</span><span class="sxs-lookup"><span data-stu-id="bb40b-158">skew a visual by the specified angle along the x-axis and y-axis, and around the specified center point.</span></span> | ![Иллюстрация квадратно наклоненного 30 градусов против часовой стрелки от оси y](images/skew.png)                                   |
| <span data-ttu-id="bb40b-160">Перевод строки 2D [**идкомпоситионтранслатетрансформ**](/windows/win32/api/dcomp/nn-dcomp-idcompositiontranslatetransform) \[\]</span><span class="sxs-lookup"><span data-stu-id="bb40b-160">Translate 2D [**idcompositiontranslatetransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositiontranslatetransform)\[newline\]</span></span> | <span data-ttu-id="bb40b-161">изменение расположения визуального элемента в направлении оси x и оси y.</span><span class="sxs-lookup"><span data-stu-id="bb40b-161">change the position of a visual in the direction of the x-axis and y-axis.</span></span>                               | ![Иллюстрация квадрата, перемещенного на 20 единиц вдоль положительной оси x и 10 единиц вдоль положительной оси y](images/translate.png) |



 

## <a name="matrix-2d-transforms"></a><span data-ttu-id="bb40b-163">Двумерные преобразования матрицы</span><span class="sxs-lookup"><span data-stu-id="bb40b-163">Matrix 2D transforms</span></span>

<span data-ttu-id="bb40b-164">Интерфейс [**идкомпоситионматрикстрансформ**](/windows/win32/api/dcomp/nn-dcomp-idcompositionmatrixtransform) позволяет определить собственную матрицу «3 на 2 аффинного преобразования» и применить ее к визуальному элементу.</span><span class="sxs-lookup"><span data-stu-id="bb40b-164">The [**IDCompositionMatrixTransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionmatrixtransform) interface enables you to define your own 3-by-2 affine 2D transform matrix and apply it to a visual.</span></span> <span data-ttu-id="bb40b-165">Этот интерфейс полезен, если необходимо применить тип аффинных 2D-преобразования, недоступного через другие интерфейсы преобразования DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="bb40b-165">This interface is useful if you need to apply a type of affine 2D transform that is not available through the other DirectComposition transform interfaces.</span></span> <span data-ttu-id="bb40b-166">Вы определяете матрицу, заполняя структуру [**D2D \_ \_ 3X2 \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f) и передавая ее в метод [**идкомпоситионматрикстрансформ:: сетматрикс**](/windows/win32/api/dcomp/nf-dcomp-idcompositionmatrixtransform-setmatrix) .</span><span class="sxs-lookup"><span data-stu-id="bb40b-166">You define the matrix by filling a [**D2D\_MATRIX\_3X2\_F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f) structure and passing it to the [**IDCompositionMatrixTransform::SetMatrix**](/windows/win32/api/dcomp/nf-dcomp-idcompositionmatrixtransform-setmatrix) method.</span></span>

## <a name="transform-groups"></a><span data-ttu-id="bb40b-167">Группы преобразований</span><span class="sxs-lookup"><span data-stu-id="bb40b-167">Transform Groups</span></span>

<span data-ttu-id="bb40b-168">Группы преобразования можно использовать для объединения нескольких преобразований в один.</span><span class="sxs-lookup"><span data-stu-id="bb40b-168">You can use transform groups to combine multiple transforms into one.</span></span> <span data-ttu-id="bb40b-169">Группа преобразования определяет коллекцию объектов Transform, матрицы которых умножаются в том порядке, в котором они указаны в коллекции.</span><span class="sxs-lookup"><span data-stu-id="bb40b-169">A transform group defines a collection of transform objects whose matrices are multiplied together in the order in which they are specified in the collection.</span></span> <span data-ttu-id="bb40b-170">Полученная матрица преобразования затем применяется к визуальному элементу.</span><span class="sxs-lookup"><span data-stu-id="bb40b-170">The resulting transform matrix is then applied to the visual.</span></span> <span data-ttu-id="bb40b-171">Группа преобразования дает тот же результат, что и применение каждого преобразования отдельно.</span><span class="sxs-lookup"><span data-stu-id="bb40b-171">A transform group produces the same result as applying each transform separately.</span></span>

<span data-ttu-id="bb40b-172">Помните, что порядок объектов Transform в группе преобразований важен.</span><span class="sxs-lookup"><span data-stu-id="bb40b-172">Keep in mind that the order of the transform objects in a transform group is important.</span></span> <span data-ttu-id="bb40b-173">Например, если визуальный элемент сначала поворачивается, затем масштабируется, а затем преобразуется, результат будет отличаться от результата, который сначала преобразуется, затем поворачивается, а затем масштабируется.</span><span class="sxs-lookup"><span data-stu-id="bb40b-173">For example, if a visual is first rotated, then scaled, and then translated, the result is different than if the visual is first translated, then rotated, and then scaled.</span></span> <span data-ttu-id="bb40b-174">DirectComposition всегда применяет преобразования к визуальному элементу в том порядке, в котором они указаны в коллекции.</span><span class="sxs-lookup"><span data-stu-id="bb40b-174">DirectComposition always applies the transforms to a visual in the order in which they are specified in the collection.</span></span>

<span data-ttu-id="bb40b-175">Чтобы создать группу преобразования, сначала создайте объекты преобразования, которые необходимо включить в группу, а затем передайте массив указателей объектов преобразования в метод [**идкомпоситиондевице:: креатетрансформграуп**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtransformgroup) .</span><span class="sxs-lookup"><span data-stu-id="bb40b-175">To create a transform group, first create the transform objects that you want to include in the group, and then pass an array of transform object pointers to the [**IDCompositionDevice::CreateTransformGroup**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtransformgroup) method.</span></span> <span data-ttu-id="bb40b-176">После создания группы преобразований нельзя добавлять или удалять объекты преобразования.</span><span class="sxs-lookup"><span data-stu-id="bb40b-176">After you create a transform group, you cannot add or remove any transform objects.</span></span> <span data-ttu-id="bb40b-177">Однако можно изменить свойства отдельных объектов Transform в коллекции, и изменения будут отражены в результирующей матрице преобразования.</span><span class="sxs-lookup"><span data-stu-id="bb40b-177">However, you can modify the properties of the individual transform objects in the collection, and the changes will be reflected in the resulting transform matrix.</span></span>

## <a name="transform-animation"></a><span data-ttu-id="bb40b-178">Преобразовать анимацию</span><span class="sxs-lookup"><span data-stu-id="bb40b-178">Transform animation</span></span>

<span data-ttu-id="bb40b-179">Свойства преобразования можно анимировать.</span><span class="sxs-lookup"><span data-stu-id="bb40b-179">The properties of a transform can be animated.</span></span> <span data-ttu-id="bb40b-180">При анимации свойства DirectComposition изменяет значение свойства с течением времени, а не сразу.</span><span class="sxs-lookup"><span data-stu-id="bb40b-180">When a property is animated, DirectComposition changes the value of the property over time, rather than all at once.</span></span> <span data-ttu-id="bb40b-181">Это особенно полезно при создании переходов.</span><span class="sxs-lookup"><span data-stu-id="bb40b-181">This is particularly useful when creating transitions.</span></span> <span data-ttu-id="bb40b-182">Дополнительные сведения см. в разделе [анимация](animation.md).</span><span class="sxs-lookup"><span data-stu-id="bb40b-182">For more information, see [Animation](animation.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="bb40b-183">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="bb40b-183">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bb40b-184">Основные понятия DirectComposition</span><span class="sxs-lookup"><span data-stu-id="bb40b-184">DirectComposition Concepts</span></span>](directcomposition-concepts.md)
</dt> </dl>

 

 
