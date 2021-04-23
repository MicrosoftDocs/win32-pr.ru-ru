---
title: Советы по правильности OpenGL
description: Советы по правильности OpenGL
ms.assetid: 48397fbf-823d-4ea0-adfd-2c639e20e38f
keywords:
- OpenGL, советы по исправлению
- OpenGL, рекомендации
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5294d2e989591216ea8cf66aa380933718776f2d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104410812"
---
# <a name="opengl-correctness-tips"></a><span data-ttu-id="a3989-105">Советы по правильности OpenGL</span><span class="sxs-lookup"><span data-stu-id="a3989-105">OpenGL Correctness Tips</span></span>

<span data-ttu-id="a3989-106">Следуйте приведенным ниже рекомендациям, чтобы создать приложения OpenGL, которые выполняются так, как вам нужно.</span><span class="sxs-lookup"><span data-stu-id="a3989-106">Follow these guidelines to create OpenGL applications that perform as you intend:</span></span>

-   <span data-ttu-id="a3989-107">Поведение при возникновении ошибки в части реализации OpenGL может измениться в будущем выпуске OpenGL.</span><span class="sxs-lookup"><span data-stu-id="a3989-107">Assume error behavior on the part of an OpenGL implementation may change in a future release of OpenGL.</span></span> <span data-ttu-id="a3989-108">Семантика ошибок OpenGL может измениться в будущих редакциях.</span><span class="sxs-lookup"><span data-stu-id="a3989-108">OpenGL error semantics may change in future revisions.</span></span>
-   <span data-ttu-id="a3989-109">Используйте матрицу проекции, чтобы свернуть всю геометрию в одну плоскость.</span><span class="sxs-lookup"><span data-stu-id="a3989-109">Use the projection matrix to collapse all geometry to a single plane.</span></span> <span data-ttu-id="a3989-110">Если используется матрица моделвиев, то функции OpenGL, которые работают в координатах глаз (таких как освещение и определенные приложением обтравочные плоскости), могут завершиться ошибкой.</span><span class="sxs-lookup"><span data-stu-id="a3989-110">If the modelview matrix is used, OpenGL features that operate in eye coordinates (such as lighting and application-defined clipping planes) might fail.</span></span>
-   <span data-ttu-id="a3989-111">Не вносите существенные изменения в одну матрицу.</span><span class="sxs-lookup"><span data-stu-id="a3989-111">Do not make extensive changes to a single matrix.</span></span> <span data-ttu-id="a3989-112">Например, не следует анимировать вращение, постоянно вызывая [**глротате**](glrotate.md) с инкрементным углом.</span><span class="sxs-lookup"><span data-stu-id="a3989-112">For example, do not animate a rotation by continually calling [**glRotate**](glrotate.md) with an incremental angle.</span></span> <span data-ttu-id="a3989-113">Вместо этого используйте [**гллоадидентити**](glloadidentity.md) для инициализации заданной матрицы для каждого кадра, а затем вызовите **глротате** с требуемым полным углом для этого кадра.</span><span class="sxs-lookup"><span data-stu-id="a3989-113">Rather, use [**glLoadIdentity**](glloadidentity.md) to initialize the given matrix for each frame, and then call **glRotate** with the desired complete angle for that frame.</span></span>
-   <span data-ttu-id="a3989-114">Ожидает несколько проходов через базу данных отрисовки для создания одних и тех же фрагментов пикселей, только если это поведение гарантировано правилами расхождения, установленными для совместимой реализации OpenGL.</span><span class="sxs-lookup"><span data-stu-id="a3989-114">Expect multiple passes through a rendering database to generate the same pixel fragments only if this behavior is guaranteed by the invariance rules established for a compliant OpenGL implementation.</span></span> <span data-ttu-id="a3989-115">В противном случае несколько проходов могут формировать различные наборы фрагментов.</span><span class="sxs-lookup"><span data-stu-id="a3989-115">Otherwise, multiple passes might generate varying sets of fragments.</span></span>
-   <span data-ttu-id="a3989-116">Не следует выводить сообщения об ошибках во время определения списка отображаемых данных.</span><span class="sxs-lookup"><span data-stu-id="a3989-116">Do not expect errors to be reported while a display list is being defined.</span></span> <span data-ttu-id="a3989-117">Команды в списке Отображение выводят ошибки только при выполнении списка.</span><span class="sxs-lookup"><span data-stu-id="a3989-117">The commands within a display list generate errors only when the list is executed.</span></span>
-   <span data-ttu-id="a3989-118">Чтобы оптимизировать операцию в буфере глубины, разместите ближайшую плоскость фрустум в той мере, насколько это возможно.</span><span class="sxs-lookup"><span data-stu-id="a3989-118">To optimize the operation of the depth buffer, place the near frustum plane as far from the viewpoint as possible.</span></span>
-   <span data-ttu-id="a3989-119">Вызовите [**глфлуш**](glflush.md) для принудительного выполнения всех предыдущих команд OpenGL.</span><span class="sxs-lookup"><span data-stu-id="a3989-119">Call [**glFlush**](glflush.md) to force execution of all previous OpenGL commands.</span></span> <span data-ttu-id="a3989-120">Не подсчитайте значение для [**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) или [**глисенаблед**](glisenabled.md) , чтобы очистить поток отрисовки.</span><span class="sxs-lookup"><span data-stu-id="a3989-120">Do not count on [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) or [**glIsEnabled**](glisenabled.md) to flush the rendering stream.</span></span> <span data-ttu-id="a3989-121">Команды запроса сбрасываются как часть потока, что требуется для возврата допустимых данных, но не обязательно завершать все ожидающие выполнения команды отрисовки.</span><span class="sxs-lookup"><span data-stu-id="a3989-121">Query commands flush as much of the stream as is required to return valid data but don't necessarily complete all pending rendering commands.</span></span>
-   <span data-ttu-id="a3989-122">Отключите дизеринг при подготовке изображений с отснятым смешением (например, при вызове [**глкопипикселс**](glcopypixels.md) ).</span><span class="sxs-lookup"><span data-stu-id="a3989-122">Turn off dithering when rendering predithered images (for example, when [**glCopyPixels**](glcopypixels.md) is called).</span></span>
-   <span data-ttu-id="a3989-123">Используйте весь диапазон буфера накопления.</span><span class="sxs-lookup"><span data-stu-id="a3989-123">Make use of the full range of the accumulation buffer.</span></span> <span data-ttu-id="a3989-124">Например, при накоплении четырех изображений каждый из них масштабируется по одному кварталу по мере накопления.</span><span class="sxs-lookup"><span data-stu-id="a3989-124">For example, if accumulating four images, scale each by one-quarter as it is accumulated.</span></span>
-   <span data-ttu-id="a3989-125">Чтобы получить точную двухмерную растрирование, аккуратно укажите ортогональную проекцию и вершины примитивов, которые должны быть растровыми.</span><span class="sxs-lookup"><span data-stu-id="a3989-125">To obtain exact two-dimensional rasterization, carefully specify both the orthographic projection and the vertices of the primitives that are to be rasterized.</span></span> <span data-ttu-id="a3989-126">Укажите ортогональную проекцию с целыми координатами, как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="a3989-126">Specify the orthographic projection with integer coordinates, as shown in the following example.</span></span>

    ``` syntax
    gluOrtho2D(0, width, 0, height); 
    ```

    <span data-ttu-id="a3989-127">Параметры *Width* и *Height* являются размерами окна просмотра.</span><span class="sxs-lookup"><span data-stu-id="a3989-127">The parameters *width* and *height* are the dimensions of the viewport.</span></span> <span data-ttu-id="a3989-128">Учитывая эту матрицу проекции, поместите вершины многоугольников и изображения пикселей в целочисленные координаты, чтобы выполнить прогнозируемый растрирование.</span><span class="sxs-lookup"><span data-stu-id="a3989-128">Given this projection matrix, place polygon vertices and pixel image positions at integer coordinates to rasterize predictably.</span></span> <span data-ttu-id="a3989-129">Например, [глректи](glrect-functions.md)(0, 0, 1, 1) надежно заполняет нижний левый пиксел окна просмотра, а [glRasterPos2i](glrasterpos-functions.md)(0, 0) надежно размещает немасштабное изображение в левом нижнем пикселе окна просмотра.</span><span class="sxs-lookup"><span data-stu-id="a3989-129">For example, [glRecti](glrect-functions.md)( 0, 0, 1, 1 ) reliably fills the lower-left pixel of the viewport, and [glRasterPos2i](glrasterpos-functions.md)( 0, 0 ) reliably positions an unzoomed image at the lower-left pixel of the viewport.</span></span> <span data-ttu-id="a3989-130">Однако вершины точек, вершины линий и точечных рисунков должны размещаться в половинных целых местах.</span><span class="sxs-lookup"><span data-stu-id="a3989-130">However, point vertices, line vertices, and bitmap positions should be placed at half-integer locations.</span></span> <span data-ttu-id="a3989-131">Например, линия, нарисованная от (*x* (1), 0,5) до (*x* (2), 0,5), будет надежно отображена в нижней строке пикселей в окне просмотра, а точка, нарисованная в (0,5, 0,5), будет надежно заполнять тот же пиксель, что и глректи (0, 0, 1, 1).</span><span class="sxs-lookup"><span data-stu-id="a3989-131">For example, a line drawn from (*x* (1) , 0.5) to (*x* (2) , 0.5) will be reliably rendered along the bottom row of pixels in the viewport, and a point drawn at (0.5, 0.5) will reliably fill the same pixel as glRecti( 0, 0, 1, 1 ).</span></span>

    <span data-ttu-id="a3989-132">Оптимальный компромисс, позволяющий указывать все примитивы в целых позициях, сохраняя при этом гарантированно предсказуемую растрирование, — перевод *x* и *y* на 0,375, как показано в следующем примере кода.</span><span class="sxs-lookup"><span data-stu-id="a3989-132">An optimum compromise that allows all primitives to be specified at integer positions, while still ensuring predictable rasterization, is to translate *x* and *y* by 0.375, as shown in the following code sample.</span></span> <span data-ttu-id="a3989-133">Такой перевод обеспечивает безотносительное расположение изображений многоугольников и пикселов, а также перемещение вершин линий, достаточно близкого к пикселным центрам.</span><span class="sxs-lookup"><span data-stu-id="a3989-133">Such a translation keeps polygon and pixel image edges safely away from the centers of pixels, while moving line vertices close enough to the pixel centers.</span></span>

    ``` syntax
    glViewport(0, 0, width, height);
    glMatrixMode(GL_PROJECTION);
    glLoadIdentity( );
    gluOrtho2D(0, width, 0, height);
    glMatrixMode(GL_MODELVIEW);
    glLoadIdentity( );
    glTranslatef(0.375, 0.375, 0.0);
    /* render all primitives at integer positions */
    ```

-   <span data-ttu-id="a3989-134">Избегайте использования отрицательных *координат вершин и отрицательных* координат текстуры в *q* .</span><span class="sxs-lookup"><span data-stu-id="a3989-134">Avoid using negative *w* vertex coordinates and negative *q* texture coordinates.</span></span> <span data-ttu-id="a3989-135">OpenGL может не отсекать такие координаты правильно и может привести к ошибкам интерполяции при заливке примитивов, определенных такими координатами.</span><span class="sxs-lookup"><span data-stu-id="a3989-135">OpenGL might not clip such coordinates correctly and can make interpolation errors when shading primitives defined by such coordinates.</span></span>

 

 




