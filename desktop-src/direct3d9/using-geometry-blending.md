---
description: Следующая определяемая пользователем структура может использоваться для вершин, которые будут смешиваться между двумя матрицами.
ms.assetid: 6bcabcf9-d14e-446a-8dd2-e741211cc704
title: Использование смешения геометрии (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc12c4d7d83ce4c01c76bd338a07f8e0aac7c003
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105701101"
---
# <a name="using-geometry-blending-direct3d-9"></a><span data-ttu-id="49ef8-103">Использование смешения геометрии (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="49ef8-103">Using Geometry Blending (Direct3D 9)</span></span>

<span data-ttu-id="49ef8-104">Следующая определяемая пользователем структура может использоваться для вершин, которые будут смешиваться между двумя матрицами.</span><span class="sxs-lookup"><span data-stu-id="49ef8-104">The following user-defined structure can be used for vertices that will be blended between two matrices.</span></span>


```
// The flexible vertex format (FVF) descriptor for this vertex would be:
//   FVF = D3DFVF_XYZB1 | D3DFVF_NORMAL | D3DFVF_TEX1; 

struct D3DBLENDVERTEX {
    D3DVECTOR v;
    FLOAT     blend; 
    D3DVECTOR n;
    FLOAT     tu, tv;
};
```



<span data-ttu-id="49ef8-105">Вес смешения должен располагаться после расположения и РХВ данных в ФВФ и до нормали вершины.</span><span class="sxs-lookup"><span data-stu-id="49ef8-105">The blend weight must appear after the position and RHW data in the FVF, and before the vertex normal.</span></span>

<span data-ttu-id="49ef8-106">Обратите внимание, что предыдущий формат вершины содержит только одно значение веса смешения.</span><span class="sxs-lookup"><span data-stu-id="49ef8-106">Notice that the preceding vertex format contains only one blending weight value.</span></span> <span data-ttu-id="49ef8-107">Это связано с тем, что существует две мировые матрицы, определенные в состояниях преобразования [**D3DTS \_ ворлдматрикс**](d3dts-worldmatrix.md)(0) и **D3DTS \_ ворлдматрикс**(1).</span><span class="sxs-lookup"><span data-stu-id="49ef8-107">This is because there will be two world matrices, defined in the [**D3DTS\_WORLDMATRIX**](d3dts-worldmatrix.md)(0) and **D3DTS\_WORLDMATRIX**(1) transform states.</span></span> <span data-ttu-id="49ef8-108">Система смешивает каждую вершину между этими двумя матрицами, используя значение одного веса.</span><span class="sxs-lookup"><span data-stu-id="49ef8-108">The system blends each vertex between these two matrices using the single weight value.</span></span> <span data-ttu-id="49ef8-109">Для трех матриц требуются только два веса и т. д.</span><span class="sxs-lookup"><span data-stu-id="49ef8-109">For three matrices, only two weights are required, and so on.</span></span>

> [!Note]
>
> <span data-ttu-id="49ef8-110">Определить весовые коэффициенты обложки несложно.</span><span class="sxs-lookup"><span data-stu-id="49ef8-110">Defining skin weights is easy.</span></span> <span data-ttu-id="49ef8-111">Использование линейной функции расстояния между соединениями является хорошим началом, но более гладкая сигмоидальной функция выглядит лучше.</span><span class="sxs-lookup"><span data-stu-id="49ef8-111">Using a linear function of the distance between joints is good start, but a smoother sigmoid function looks better.</span></span> <span data-ttu-id="49ef8-112">Выбор функции распределения с учетом ширины обложки может привести к резкому креасесу в соединениях при необходимости, используя большой вариации в качестве веса на коротком расстоянии.</span><span class="sxs-lookup"><span data-stu-id="49ef8-112">Choosing a skin-weight distribution function can result in sharp creases at joints, if desired, by using a large variation in skin weight over a short distance.</span></span>

 

## <a name="setting-blending-matrices"></a><span data-ttu-id="49ef8-113">Настройка матриц смешения</span><span class="sxs-lookup"><span data-stu-id="49ef8-113">Setting Blending Matrices</span></span>

<span data-ttu-id="49ef8-114">Матрицы преобразования, между которыми накладываются системы, задаются путем вызова метода [**IDirect3DDevice9:: сеттрансформ**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="49ef8-114">You set the transformation matrices between which the system blends by calling the [**IDirect3DDevice9::SetTransform**](/windows/desktop/api) method.</span></span> <span data-ttu-id="49ef8-115">Присвойте первому параметру значение, определенное в макросе [**D3DTS \_ ворлдматрикс**](d3dts-worldmatrix.md) , и задайте для второго параметра адрес матрицы, которую необходимо задать.</span><span class="sxs-lookup"><span data-stu-id="49ef8-115">Set the first parameter to a value defined by the [**D3DTS\_WORLDMATRIX**](d3dts-worldmatrix.md) macro, and set the second parameter to the address of the matrix to be set.</span></span>

<span data-ttu-id="49ef8-116">Следующий пример кода C++ задает две мировые матрицы, между которыми смешивается, чтобы создать иллюзию совместной ARM.</span><span class="sxs-lookup"><span data-stu-id="49ef8-116">The following C++ code example sets two world matrices, between which geometry is blended to create the illusion of a jointed arm.</span></span>


```
// For this example, the d3dDevice variable is assumed to be a valid pointer
//   to an IDirect3DDevice9 interface for an initialized 3D scene.

float     BendAngle = 3.1415926f / 4.0f; // 45 degrees
D3DMATRIX matUpperArm, matLowerArm;

// The upper arm is immobile. Use the identity matrix.
D3DXMatrixIdentity( matUpperArm );
d3dDevice->SetTransform( D3DTS_WORLDMATRIX(0), &matUpperArm );

// The lower arm rotates about the x-axis, attached to the upper arm.
D3DXMatrixRotationX( matLowerArm, -BendAngle ); 
d3dDevice->SetTransform( D3DTS_WORLDMATRIX(1), &matLowerArm );
```



<span data-ttu-id="49ef8-117">Настройка матрицы смешения лишь приводит к тому, что система кэширует матрицу для последующего использования. Он не указывает системе начать смешивание вершин.</span><span class="sxs-lookup"><span data-stu-id="49ef8-117">Setting a blending matrix merely causes the system to cache the matrix for later use; it doesn't instruct the system to begin blending vertices.</span></span>

## <a name="enabling-geometry-blending"></a><span data-ttu-id="49ef8-118">Включение смешения геометрии</span><span class="sxs-lookup"><span data-stu-id="49ef8-118">Enabling Geometry Blending</span></span>

<span data-ttu-id="49ef8-119">По умолчанию отключено смешение геометрических объектов.</span><span class="sxs-lookup"><span data-stu-id="49ef8-119">Geometry blending is disabled by default.</span></span> <span data-ttu-id="49ef8-120">Чтобы включить смешение геометрических объектов, вызовите метод [**IDirect3DDevice9:: сетрендерстате**](/windows/desktop/api) , чтобы установить в качестве \_ состояния отображения D3DRS вертексбленд значение из перечисляемого типа [**D3DVERTEXBLENDFLAGS**](./d3dvertexblendflags.md) .</span><span class="sxs-lookup"><span data-stu-id="49ef8-120">To enable geometry blending, call the [**IDirect3DDevice9::SetRenderState**](/windows/desktop/api) method to set the D3DRS\_VERTEXBLEND render state to a value from the [**D3DVERTEXBLENDFLAGS**](./d3dvertexblendflags.md) enumerated type.</span></span> <span data-ttu-id="49ef8-121">В следующем примере кода показано, как может выглядеть этот вызов при задании состояния отрисовки для смешения между двумя мировыми матрицами.</span><span class="sxs-lookup"><span data-stu-id="49ef8-121">The following code example shows what this call might look like when setting the render state for a blend between two world matrices.</span></span>


```
d3dDevice->SetRenderState( D3DRS_VERTEXBLEND, D3DVBF_1WEIGHTS );
```



<span data-ttu-id="49ef8-122">Если для параметра D3DRS \_ вертексбленд задано любое значение, отличное от D3DVBF \_ Disable, система предполагает, что в формат вершины будет включено соответствующее количество весовых коэффициентов смешения.</span><span class="sxs-lookup"><span data-stu-id="49ef8-122">When D3DRS\_VERTEXBLEND is set to any value other than D3DVBF\_DISABLE, the system assumes that the appropriate number of blending weights will be included in the vertex format.</span></span> <span data-ttu-id="49ef8-123">Вы обязаны предоставить совместимый формат вершин и предоставить правильное описание этого формата для методов рендеринга Direct3D.</span><span class="sxs-lookup"><span data-stu-id="49ef8-123">It is your responsibility to provide a compliant vertex format, and to provide a proper description of that format to the Direct3D rendering methods.</span></span>

<span data-ttu-id="49ef8-124">Если этот параметр включен, система выполняет смешение геометрии для всех объектов, отображаемых методами подготовки Дравпримитиве.</span><span class="sxs-lookup"><span data-stu-id="49ef8-124">When enabled, the system performs geometry blending for all objects rendered by the DrawPrimitive rendering methods.</span></span>

## <a name="see-also"></a><span data-ttu-id="49ef8-125">См. также:</span><span class="sxs-lookup"><span data-stu-id="49ef8-125">See Also</span></span>

[<span data-ttu-id="49ef8-126">Фиксированные коды ФВФ функций (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="49ef8-126">Fixed Function FVF Codes (Direct3D 9)</span></span>](fixed-function-fvf-codes.md)


## <a name="related-topics"></a><span data-ttu-id="49ef8-127">См. также</span><span class="sxs-lookup"><span data-stu-id="49ef8-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="49ef8-128">Смешение геометрических объектов</span><span class="sxs-lookup"><span data-stu-id="49ef8-128">Geometry Blending</span></span>](geometry-blending.md)
</dt> </dl>

 

 
