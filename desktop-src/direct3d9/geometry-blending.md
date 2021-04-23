---
description: Direct3D позволяет приложению повысить реальную работу, выполнив визуализацию сегментированных объектов-многоугольников (особенно символов), имеющих гладкие смешивание.
ms.assetid: 190d5865-c45b-42ea-8a16-10a4f0bda743
title: Смешение геометрических объектов (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a19daa40f7d7d8193ae486640bc613dd7a666ec7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103805188"
---
# <a name="geometry-blending-direct3d-9"></a><span data-ttu-id="0fa90-103">Смешение геометрических объектов (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="0fa90-103">Geometry Blending (Direct3D 9)</span></span>

<span data-ttu-id="0fa90-104">Direct3D позволяет приложению повысить реальную работу, выполнив визуализацию сегментированных объектов-многоугольников (особенно символов), имеющих гладкие смешивание.</span><span class="sxs-lookup"><span data-stu-id="0fa90-104">Direct3D enables an application to increase the realism of its scenes by rendering segmented polygonal objects - especially characters - that have smoothly blended joints.</span></span> <span data-ttu-id="0fa90-105">Эти эффекты часто называются обложками.</span><span class="sxs-lookup"><span data-stu-id="0fa90-105">These effects are often referred to as skinning.</span></span> <span data-ttu-id="0fa90-106">Система достигает этого результата, применяя дополнительные матрицы универсального преобразования к одному набору вершин для создания нескольких результатов, а затем выполняет линейное смешение между результирующими вершинами для создания одного набора геометрии для отрисовки.</span><span class="sxs-lookup"><span data-stu-id="0fa90-106">The system achieves this effect by applying additional world transformation matrices to a single set of vertices to create multiple results, and then performing a linear blend between the resultant vertices to create a single set of geometry for rendering.</span></span> <span data-ttu-id="0fa90-107">Этот процесс показан на следующей иллюстрации.</span><span class="sxs-lookup"><span data-stu-id="0fa90-107">The following illustration of a banana shows this process.</span></span>

![Иллюстрация процесса смешения двух объектов с текстурой с неменяющими скобками](images/geometry-blend.png)

<span data-ttu-id="0fa90-109">На предыдущем рисунке показано, как можно представить процесс смешивания геометрического смешения.</span><span class="sxs-lookup"><span data-stu-id="0fa90-109">The preceding illustration shows how you might imagine the geometry-blending process.</span></span> <span data-ttu-id="0fa90-110">В одном вызове подготовки к просмотру система принимает вершины для «вниз», преобразует их дважды, без изменения, и один раз с простым поворотом и объединяет результаты, чтобы создать изогнутое значение «вниз».</span><span class="sxs-lookup"><span data-stu-id="0fa90-110">In a single rendering call, the system takes the vertices for the banana, transforms them twice - once without modification, and once with a simple rotation - and blends the results to create a bent banana.</span></span> <span data-ttu-id="0fa90-111">Система смешивает расположение вершины, а также нормальную вершину, когда освещение включено.</span><span class="sxs-lookup"><span data-stu-id="0fa90-111">The system blends the vertex position, as well as the vertex normal when lighting is enabled.</span></span> <span data-ttu-id="0fa90-112">Приложения не ограничиваются двумя путями смешивания. С помощью Direct3D можно смешивать геометрические объекты, накладываемые на четыре мировых матрицы, включая стандартную матрицу мира [**D3DTS \_ World**](d3dts-world.md).</span><span class="sxs-lookup"><span data-stu-id="0fa90-112">Applications are not limited to two blending paths; Direct3D can blend geometry between as many as four world matrices, including the standard world matrix, [**D3DTS\_WORLD**](d3dts-world.md).</span></span>

> [!Note]
>
> <span data-ttu-id="0fa90-113">Если освещение включено, нормали вершин преобразуются в соответствующую матрицу представления мира, взвешенную таким же образом, как и при вычислении расположения вершины.</span><span class="sxs-lookup"><span data-stu-id="0fa90-113">When lighting is enabled, vertex normals are transformed by a corresponding inverse world-view matrix, weighted in the same way as the vertex position computations.</span></span> <span data-ttu-id="0fa90-114">Система нормализует результирующий нормальный вектор, если \_ состояние визуализации D3DRS нормализенормалс имеет значение **true**.</span><span class="sxs-lookup"><span data-stu-id="0fa90-114">The system normalizes the resulting normal vector if the D3DRS\_NORMALIZENORMALS render state is set to **TRUE**.</span></span>

 

<span data-ttu-id="0fa90-115">При отсутствии смешения геометрии динамически построенные модели часто подготавливаются к просмотру в виде сегментов.</span><span class="sxs-lookup"><span data-stu-id="0fa90-115">Without geometry blending, dynamic articulated models are often rendered in segments.</span></span> <span data-ttu-id="0fa90-116">Например, рассмотрим трехмерную модель человеческих рычагов.</span><span class="sxs-lookup"><span data-stu-id="0fa90-116">For instance, consider a 3D model of the human arm.</span></span> <span data-ttu-id="0fa90-117">В самом простом представлении ARM состоит из двух частей: верхней ARM, который подключается к телу, и нижней ARM, который подключается к руки.</span><span class="sxs-lookup"><span data-stu-id="0fa90-117">In the simplest view, an arm has two parts: the upper arm which connects to the body, and the lower arm, which connects to the hand.</span></span> <span data-ttu-id="0fa90-118">Эти два соединения соединены с изгибом, а нижняя точка вращения — на этом этапе.</span><span class="sxs-lookup"><span data-stu-id="0fa90-118">The two are connected at the elbow, and the lower arm rotates at that point.</span></span> <span data-ttu-id="0fa90-119">Приложение, обрабатывающее ARM, может хранить данные вершин для верхней и нижней ARM, каждый из которых имеет отдельную матрицу преобразования мира.</span><span class="sxs-lookup"><span data-stu-id="0fa90-119">An application that renders an arm might retain vertex data for the upper and lower arm, each with a separate world transformation matrix.</span></span> <span data-ttu-id="0fa90-120">Это показано в следующем примере кода.</span><span class="sxs-lookup"><span data-stu-id="0fa90-120">The following code example illustrates this.</span></span>


```
typedef struct _Arm
{
    VERTEX upper_arm_verts[200];
    D3DMATRIX matWorld_Upper;

    VERTEX lower_arm_verts[200];
    D3DMATRIX matWorld_Lower;
} ARM, *LPARM;

ARM MyArm; // This needs to be initialized.
```



<span data-ttu-id="0fa90-121">Для визуализации ARM создаются два вызова отрисовки, как показано в следующем коде.</span><span class="sxs-lookup"><span data-stu-id="0fa90-121">To render the arm, two rendering calls are made, as shown in the following code.</span></span>


```
// Render the upper arm.
d3dDevice->SetTransform( D3DTS_WORLD, &MyArm.matWorld_Upper );
d3dDevice->DrawPrimitive( D3DPT_TRIANGLELIST, 0, numFaces );

// Render the lower arm, updating its world matrix to articulate
// the arm by pi/4 radians (45 degrees) at the elbow.
MyArm.matWorld_Lower = RotateMyArm(MyArm.matWorld, pi/4);
d3dDevice->SetTransform( D3DTS_WORLD, &MyArm.matWorld_Lower );
d3dDevice->DrawPrimitive( D3DPT_TRIANGLELIST, 0, numFaces );
```



<span data-ttu-id="0fa90-122">На следующем рисунке для использования этого метода изменено значение «неменяющий».</span><span class="sxs-lookup"><span data-stu-id="0fa90-122">The following illustration is a banana, modified to use this technique.</span></span>

![Иллюстрация смешенного вниз без смешения геометрии](images/noblend.png)

<span data-ttu-id="0fa90-124">Различия между смешиванием и несмешением геометрии очевидны.</span><span class="sxs-lookup"><span data-stu-id="0fa90-124">The differences between the blended geometry and the nonblended geometry are obvious.</span></span> <span data-ttu-id="0fa90-125">Этот пример является несколько крайним.</span><span class="sxs-lookup"><span data-stu-id="0fa90-125">This example is somewhat extreme.</span></span> <span data-ttu-id="0fa90-126">В реальных приложениях соединения сегментированных моделей разрабатываются так, чтобы стыки не настолько очевидны.</span><span class="sxs-lookup"><span data-stu-id="0fa90-126">In a real-world application, the joints of segmented models are designed so that seams are not as obvious.</span></span> <span data-ttu-id="0fa90-127">Однако стыки видны во времени, что представляет собой постоянные проблемы, связанные с конструкторами моделей.</span><span class="sxs-lookup"><span data-stu-id="0fa90-127">However, seams are visible at times, which presents constant challenges for model designers.</span></span>

<span data-ttu-id="0fa90-128">Смешивание геометрии в Direct3D представляет собой альтернативу классическому сценарию сегментированного моделирования.</span><span class="sxs-lookup"><span data-stu-id="0fa90-128">Geometry blending in Direct3D presents an alternative to the classic segmented-modeling scenario.</span></span> <span data-ttu-id="0fa90-129">Однако улучшенное визуальное качество сегментированных объектов достигается за счет использования вычислений смешения во время отрисовки.</span><span class="sxs-lookup"><span data-stu-id="0fa90-129">However, the improved visual quality of segmented objects comes at the cost of the blending computations during rendering.</span></span> <span data-ttu-id="0fa90-130">Чтобы уменьшить влияние этих дополнительных операций, конвейер обработки геометрии Direct3D оптимизирован для смешивания геометрии с минимально возможными издержками.</span><span class="sxs-lookup"><span data-stu-id="0fa90-130">To minimize the impact of these additional operations, the Direct3D geometry pipeline is optimized to blend geometry with the least possible overhead.</span></span> <span data-ttu-id="0fa90-131">Приложения, которые эффективно используют службы смешения геометрических объектов, предлагаемые Direct3D, могут улучшить реальную работу своих символов и избежать серьезных последствий в производительности.</span><span class="sxs-lookup"><span data-stu-id="0fa90-131">Applications that intelligently use the geometry blending services offered by Direct3D can improve the realism of their characters while avoiding serious performance repercussions.</span></span>

## <a name="blending-transform-and-render-states"></a><span data-ttu-id="0fa90-132">Смешение преобразований и состояний отрисовки</span><span class="sxs-lookup"><span data-stu-id="0fa90-132">Blending Transform and Render States</span></span>

<span data-ttu-id="0fa90-133">Метод [**IDirect3DDevice9:: сеттрансформ**](/windows/desktop/api) распознает макросы [**D3DTS \_ World**](d3dts-world.md) и [**D3DTS \_ ворлдн**](d3dts-worldn.md) , соответствующие значениям, которые могут быть определены с помощью макроса [**D3DTS \_ ворлдматрикс**](d3dts-worldmatrix.md) .</span><span class="sxs-lookup"><span data-stu-id="0fa90-133">The [**IDirect3DDevice9::SetTransform**](/windows/desktop/api) method recognizes the [**D3DTS\_WORLD**](d3dts-world.md) and [**D3DTS\_WORLDn**](d3dts-worldn.md) macros, which correspond to values that can be defined by the [**D3DTS\_WORLDMATRIX**](d3dts-worldmatrix.md) macro.</span></span> <span data-ttu-id="0fa90-134">Эти макросы используются для указания матриц, между которыми будет осуществляться смешение геометрического объекта.</span><span class="sxs-lookup"><span data-stu-id="0fa90-134">These macros are used to identify the matrices between which geometry will be blended.</span></span>

<span data-ttu-id="0fa90-135">Перечислимый тип [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md) включает \_ состояние отображения D3DRS вертексбленд, чтобы включить и контролировать смешение геометрических объектов.</span><span class="sxs-lookup"><span data-stu-id="0fa90-135">The [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md) enumerated type includes the D3DRS\_VERTEXBLEND render state to enable and control geometry blending.</span></span> <span data-ttu-id="0fa90-136">Допустимые значения для этого состояния рендеринга определяются перечисляемым типом [**D3DVERTEXBLENDFLAGS**](./d3dvertexblendflags.md) .</span><span class="sxs-lookup"><span data-stu-id="0fa90-136">Valid values for this render state are defined by the [**D3DVERTEXBLENDFLAGS**](./d3dvertexblendflags.md) enumerated type.</span></span> <span data-ttu-id="0fa90-137">Если включено смешение геометрических объектов, формат вершины должен включать соответствующее число весов.</span><span class="sxs-lookup"><span data-stu-id="0fa90-137">If geometry blending is enabled, the vertex format must include the appropriate number of blending weights.</span></span>

## <a name="blending-weights"></a><span data-ttu-id="0fa90-138">Весовые коэффициенты смешения</span><span class="sxs-lookup"><span data-stu-id="0fa90-138">Blending Weights</span></span>

<span data-ttu-id="0fa90-139">Вес смешения, иногда называемый весом бета-версии, управляет степенью, в которой данная матрица мира влияет на вершину.</span><span class="sxs-lookup"><span data-stu-id="0fa90-139">A blending weight, sometimes called a beta weight, controls the extent to which a given world matrix affects a vertex.</span></span> <span data-ttu-id="0fa90-140">Весовые коэффициенты смешения — это значения с плавающей запятой в диапазоне от 0,0 до 1,0, закодированные в формате вершин, где значение 0,0 означает, что вершина не смешивается с этой матрицей, а 1,0 означает, что вершина затронута матрицей полностью.</span><span class="sxs-lookup"><span data-stu-id="0fa90-140">Blending weights are floating-point values that range from 0.0 to 1.0, encoded in the vertex format, where a value of 0.0 means the vertex is not blended with that matrix, and 1.0 means that the vertex is affected in full by the matrix.</span></span>

<span data-ttu-id="0fa90-141">Весовые коэффициенты смешивания геометрических значений кодируются в формате вершин, который отображается сразу после расположения для каждой вершины, как описано в разделе [фиксированная функция Фвф Codes (Direct3D 9)](fixed-function-fvf-codes.md).</span><span class="sxs-lookup"><span data-stu-id="0fa90-141">Geometry blending weights are encoded in the vertex format, appearing immediately after the position for each vertex, as described in [Fixed Function FVF Codes (Direct3D 9)](fixed-function-fvf-codes.md).</span></span> <span data-ttu-id="0fa90-142">Вы сообщаете о числе весовых коэффициентов смешения в формате вершин, включая одну из [констант фвф](d3dfvf.md) в описание вершины, которое предоставляется методам подготовки к просмотру.</span><span class="sxs-lookup"><span data-stu-id="0fa90-142">You communicate the number of blending weights in the vertex format by including one of the [FVF constants](d3dfvf.md) in the vertex description that you provide to the rendering methods.</span></span>

<span data-ttu-id="0fa90-143">Система выполняет линейное смешение между взвешенными результатами матриц смешения.</span><span class="sxs-lookup"><span data-stu-id="0fa90-143">The system performs a linear blend between the weighted results of the blend matrices.</span></span> <span data-ttu-id="0fa90-144">Следующее уравнение является полной формулой смешения.</span><span class="sxs-lookup"><span data-stu-id="0fa90-144">The following equation is the complete blending formula.</span></span>

![уравнение линейного смешения, использование матриц мирового преобразования](images/vert-blend-formula.png)

<span data-ttu-id="0fa90-146">В предыдущем уравнении Вбленд — это вершина вывода, v-элементы — это вершины, создаваемые примененной матрицей мира ([**D3DTS \_ ворлдн**](d3dts-worldn.md)).</span><span class="sxs-lookup"><span data-stu-id="0fa90-146">In the preceding equation, vBlend is the output vertex, the v-elements are the vertices produced by the applied world matrix ([**D3DTS\_WORLDn**](d3dts-worldn.md)).</span></span> <span data-ttu-id="0fa90-147">Элементы W являются соответствующими значениями веса в формате вершины.</span><span class="sxs-lookup"><span data-stu-id="0fa90-147">The W elements are the corresponding weight values within the vertex format.</span></span> <span data-ttu-id="0fa90-148">Вершина, накладываемая между n матрицами, может иметь значения веса смешения, по одному для каждой матрицы смешения, за исключением последней.</span><span class="sxs-lookup"><span data-stu-id="0fa90-148">A vertex blended between n matrices can have - 1 blending weight values, one for each blending matrix, except the last.</span></span> <span data-ttu-id="0fa90-149">Система автоматически создает вес для последней матрицы мира, чтобы сумма всех весов была 1,0, выраженная в нотации Сигма.</span><span class="sxs-lookup"><span data-stu-id="0fa90-149">The system automatically generates the weight for the last world matrix so that the sum of all weights is 1.0, expressed in sigma notation here.</span></span> <span data-ttu-id="0fa90-150">Эту формулу можно упростить для каждого варианта, поддерживаемого Direct3D, который показан в следующих уравнениях.</span><span class="sxs-lookup"><span data-stu-id="0fa90-150">This formula can be simplified for each of the cases supported by Direct3D, which is shown in the following equations.</span></span>

![формулы линейного смешения для трех вариантов смешивания](images/vert-blend-formulas-simple.png)

<span data-ttu-id="0fa90-152">Это упрощенные формы полной формулы смешения для двух, трех и четырех вариантов матрицы смешения.</span><span class="sxs-lookup"><span data-stu-id="0fa90-152">These are the simplified forms of the complete blending formula for the two, three, and four blend matrix cases.</span></span>

> [!Note]  
> <span data-ttu-id="0fa90-153">Хотя Direct3D включает дескрипторы ФВФ для определения вершин, которые содержат до пяти весов смешения, в этом выпуске DirectX можно использовать только три.</span><span class="sxs-lookup"><span data-stu-id="0fa90-153">Although Direct3D includes FVF descriptors to define vertices that contain up to five blending weights, only three can be used in this release of DirectX.</span></span>

 

<span data-ttu-id="0fa90-154">Дополнительные сведения содержатся в следующих разделах.</span><span class="sxs-lookup"><span data-stu-id="0fa90-154">Additional information is contained in the following topics.</span></span>

-   [<span data-ttu-id="0fa90-155">Использование смешения геометрии (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="0fa90-155">Using Geometry Blending (Direct3D 9)</span></span>](using-geometry-blending.md)
-   [<span data-ttu-id="0fa90-156">Индексированное смешение вершин (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="0fa90-156">Indexed Vertex Blending (Direct3D 9)</span></span>](indexed-vertex-blending.md)
-   [<span data-ttu-id="0fa90-157">Анимированная анимация вершин (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="0fa90-157">Vertex Tweening (Direct3D 9)</span></span>](vertex-tweening.md)

## <a name="related-topics"></a><span data-ttu-id="0fa90-158">См. также</span><span class="sxs-lookup"><span data-stu-id="0fa90-158">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0fa90-159">Конвейер вершин</span><span class="sxs-lookup"><span data-stu-id="0fa90-159">Vertex Pipeline</span></span>](vertex-pipeline.md)
</dt> </dl>

 

 
