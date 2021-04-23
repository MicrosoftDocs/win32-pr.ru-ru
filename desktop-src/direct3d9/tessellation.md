---
description: Тесселяция (Direct3D 9)
ms.assetid: ae39b0e1-d2ae-449e-89db-0a2b24171531
title: Тесселяция (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82378caac1218158ffc1834c9a9b56fb8cbd250e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103806352"
---
# <a name="tessellation-direct3d-9"></a><span data-ttu-id="883f8-103">Тесселяция (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="883f8-103">Tessellation (Direct3D 9)</span></span>

## <a name="tessellator-unit"></a><span data-ttu-id="883f8-104">Блок тесселяции</span><span class="sxs-lookup"><span data-stu-id="883f8-104">Tessellator Unit</span></span>

<span data-ttu-id="883f8-105">Модуль тесселяции улучшен.</span><span class="sxs-lookup"><span data-stu-id="883f8-105">The tessellator unit has been enhanced.</span></span> <span data-ttu-id="883f8-106">Теперь его можно использовать для:</span><span class="sxs-lookup"><span data-stu-id="883f8-106">You can now use it to:</span></span>

-   <span data-ttu-id="883f8-107">Выполните адаптивную тесселяцию всех примитивов более высокого порядка.</span><span class="sxs-lookup"><span data-stu-id="883f8-107">Perform adaptive tessellation of all higher-order primitives.</span></span>
-   <span data-ttu-id="883f8-108">Поиск значений смещения по вершинам на карте смещения и их передача в шейдер вершин.</span><span class="sxs-lookup"><span data-stu-id="883f8-108">Look up per-vertex displacement values from a displacement map and pass them on to a vertex shader.</span></span>
-   <span data-ttu-id="883f8-109">Поддержка тесселяции исправлений прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="883f8-109">Support rectangle-patch tessellation.</span></span> <span data-ttu-id="883f8-110">Это указывается через объявление вершины с помощью D3DDECLMETHOD \_ партиалу или D3DDECLMETHOD \_ партиалв.</span><span class="sxs-lookup"><span data-stu-id="883f8-110">This is specified through a vertex declaration using D3DDECLMETHOD\_PARTIALU or D3DDECLMETHOD\_PARTIALV.</span></span> <span data-ttu-id="883f8-111">Если объявление вершины, содержащее эти методы, используется для прорисовки исправления треугольника, [**IDirect3DDevice9::D равтрипатч**](/windows/desktop/api) не удастся.</span><span class="sxs-lookup"><span data-stu-id="883f8-111">If a vertex declaration containing these methods is used to draw a triangle patch, [**IDirect3DDevice9::DrawTriPatch**](/windows/desktop/api) will fail.</span></span> <span data-ttu-id="883f8-112">Дополнительные сведения об объявлениях вершин см. в разделе [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).</span><span class="sxs-lookup"><span data-stu-id="883f8-112">For more information about vertex declarations, see [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).</span></span>

<span data-ttu-id="883f8-113">В DirectX 8. x то, что называлось ORDER, было действительно степенью.</span><span class="sxs-lookup"><span data-stu-id="883f8-113">In DirectX 8.x, what was called ORDER was really the degree.</span></span> <span data-ttu-id="883f8-114">В Direct3D 9 уровень теперь определяется [**D3DDEGREETYPE**](./d3ddegreetype.md).</span><span class="sxs-lookup"><span data-stu-id="883f8-114">In Direct3D 9, the degree is now specified by [**D3DDEGREETYPE**](./d3ddegreetype.md).</span></span>


```
 // This used to be D3DORDERTYPE and D3DORDER* 
 typedef enum _D3DDEGREETYPE 
 { 
 D3DDEGREE_LINEAR = 1, 
 D3DDEGREE_QUADRATIC = 2, 
 D3DDEGREE_CUBIC = 3, 
 D3DDEGREE_QUINTIC = 5, 
 D3DDEGREE_FORCE_DWORD = 0x7fffffff, 
 } D3DDEGREETYPE; 
```



<span data-ttu-id="883f8-115">Изменение типа градуса затронуло две другие структуры.</span><span class="sxs-lookup"><span data-stu-id="883f8-115">The change in degree type affected two other structures.</span></span>


```
typedef struct _D3DRECTPATCH_INFO 
 { 
 UINT StartVertexOffsetWidth; 
 UINT StartVertexOffsetHeight; 
 UINT Width; 
 UINT Height; 
 UINT Stride; 
 D3DBASISTYPE Basis; 
 D3DDEGREETYPE Degree; 
 } D3DRECTPATCH_INFO; 
```




```
 typedef struct _D3DTRIPATCH_INFO 
 { 
 UINT StartVertexOffset; 
 UINT NumVertices; 
 D3DBASISTYPE Basis; 
 D3DDEGREETYPE Degree; 
 } D3DTRIPATCH_INFO; 
```



<span data-ttu-id="883f8-116">Драйверы должны исправить ошибки компиляции, которые будут вызваны этим изменением при компиляции с новыми заголовками.</span><span class="sxs-lookup"><span data-stu-id="883f8-116">Drivers need to fix compilation errors that will result from this change when they compile with the new headers.</span></span> <span data-ttu-id="883f8-117">Функциональность не требуется изменять.</span><span class="sxs-lookup"><span data-stu-id="883f8-117">No functionality has to be changed.</span></span>

## <a name="adaptive-tessellation"></a><span data-ttu-id="883f8-118">Адаптивная тесселяция</span><span class="sxs-lookup"><span data-stu-id="883f8-118">Adaptive Tessellation</span></span>

<span data-ttu-id="883f8-119">Адаптивную тесселяцию можно применять к примитивам высокого порядка, включая N-исправления, прямоугольники и исправления треугольников.</span><span class="sxs-lookup"><span data-stu-id="883f8-119">Adaptive tessellation can be applied to high-order primitives including N-patches, rectangle patches, and triangle patches.</span></span> <span data-ttu-id="883f8-120">Эта функция включена D3DRS \_ енаблеадаптиветесселлатион и адаптирует исправление на основе значения глубины вершины элемента управления в области глаз.</span><span class="sxs-lookup"><span data-stu-id="883f8-120">This feature is enabled by the D3DRS\_ENABLEADAPTIVETESSELLATION and adaptively tessellates a patch, based on the depth value of the control vertex in eye space.</span></span>

<span data-ttu-id="883f8-121">Координаты z (Zi) элементов управления (VI), которые преобразуются в область видимости (Зиэйе), выполняя точку с 4 векторами, используются в качестве значений глубины.</span><span class="sxs-lookup"><span data-stu-id="883f8-121">The z-coordinates (Zi) of control vertices (Vi), which are transformed into eye space (Zieye) by performing a dot product with a 4-vector, are used as the depth values.</span></span> <span data-ttu-id="883f8-122">Объект 4D Vector (MDM) задается приложением, использующим четыре состояния отрисовки (D3DRS \_ адаптиветесс \_ X, D3DRS \_ АДАПТИВЕТЕСС \_ Y, D3DRS \_ адаптиветесс \_ Z и D3DRS \_ адаптиветесс \_ W).</span><span class="sxs-lookup"><span data-stu-id="883f8-122">The 4D vector (Mdm) is specified by the application using four render states (D3DRS\_ADAPTIVETESS\_X, D3DRS\_ADAPTIVETESS\_Y, D3DRS\_ADAPTIVETESS\_Z, and D3DRS\_ADAPTIVETESS\_W).</span></span> <span data-ttu-id="883f8-123">Этот 4-вектор может быть третьим столбцом объединенного мира и матрицами представления.</span><span class="sxs-lookup"><span data-stu-id="883f8-123">This 4-vector could be the third column of the concatenated world and view matrices.</span></span> <span data-ttu-id="883f8-124">Его также можно использовать для применения шкалы к Зиэйе.</span><span class="sxs-lookup"><span data-stu-id="883f8-124">It also could be used to apply a scale to Zieye.</span></span>

<span data-ttu-id="883f8-125">Функция для расчета уровня тесселяции Ti из Зиэйе предполагается (Макстесселлатионлевел/Зиэйе), что означает, что Макстесселлатионлевел является уровнем тесселяции Z = 1 в пространстве глаз.</span><span class="sxs-lookup"><span data-stu-id="883f8-125">The function to compute a tessellation level Ti from Zieye is assumed to be (MaxTessellationLevel/Zieye), which means that the MaxTessellationLevel is the tessellation level at Z = 1 in eye space.</span></span> <span data-ttu-id="883f8-126">Макстесселлатионлевел равно значению, заданному параметром [**IDirect3DDevice9:: сетнпатчмоде**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode) для N-патчей и, для обновлений RT-патчей, он равен пнумсегс.</span><span class="sxs-lookup"><span data-stu-id="883f8-126">The MaxTessellationLevel is equal to a value set by [**IDirect3DDevice9::SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode) for N-patches and, for RT-patches, it is equal to pNumSegs.</span></span> <span data-ttu-id="883f8-127">Затем уровень тесселяции копируется в значения, определенные двумя дополнительными состояниями отрисовки D3DRS \_ минтесселлатионлевел и D3DRS \_ макстесселлатионлевел, которые определяют минимальный и максимальный уровни тесселяции, на которые будут относиться.</span><span class="sxs-lookup"><span data-stu-id="883f8-127">The tessellation level is then clamped to values, defined by the two additional render states D3DRS\_MINTESSELLATIONLEVEL and D3DRS\_MAXTESSELLATIONLEVEL, which define the minimum and maximum tessellation levels to be clamped to.</span></span> <span data-ttu-id="883f8-128">Для каждой вершины, расположенной вдоль края исправления, вычисляется среднее значение, чтобы получить уровень тесселяции для этого края.</span><span class="sxs-lookup"><span data-stu-id="883f8-128">The Ti's for each vertex along an edge of a patch are averaged to obtain a tessellation level for that edge.</span></span> <span data-ttu-id="883f8-129">Алгоритм вычисления TI для обновления прямоугольников, исправлений треугольников и N-патчей отличается в зависимости от того, какие вершины управления используются для вычисления уровня тесселяции.</span><span class="sxs-lookup"><span data-stu-id="883f8-129">The algorithm for computing Ti for rectangle patches, triangle patches, and N-patches differs in what control vertices are used to compute the tessellation level.</span></span>

<span data-ttu-id="883f8-130">Для исправлений прямоугольника с использованием B-сплайна используются четыре внешних вершины элемента управления.</span><span class="sxs-lookup"><span data-stu-id="883f8-130">For the rectangle patches with a B-spline basis, the four outermost control vertices are used.</span></span> <span data-ttu-id="883f8-131">Например, с D3DORDER \_ кубическим порядком: вершины (1, 1) и (1, Width-2) используются с пнумсегс \[ 0 \] , вершинами (1, Width-2) и (высота-2, высота-2) с пнумсегс \[ 1 \] , вершинами (высота-2, Width-2) и (1, Width-2) с пнумсегс \[ 2 \] , а вершины (2, 1) и (1, 1) используются с пнумсегс \[ 3 \] .</span><span class="sxs-lookup"><span data-stu-id="883f8-131">For example, with D3DORDER\_CUBIC order: vertices (1,1) and (1,width-2) are used with pNumSegs\[0\], vertices (1,width-2) and (height-2,height-2) are used with pNumSegs\[1\], vertices (height-2,width-2) and (1,width-2) are used with pNumSegs\[2\], and vertices (2,1) and (1,1) are used with pNumSegs\[3\].</span></span>

<span data-ttu-id="883f8-132">Для исправлений треугольника используются вершины углов исправлений.</span><span class="sxs-lookup"><span data-stu-id="883f8-132">For the triangle patches, the corner patch vertices are used.</span></span> <span data-ttu-id="883f8-133">С D3DORDER \_ кубическим порядком: вершины (0) и (9) используются с пнумсегс \[ 0 \] , вершинами (9) и (6) с пнумсегс \[ 1 \] и вершинами (6) и (0) используются с пнумсегс \[ 3 \] .</span><span class="sxs-lookup"><span data-stu-id="883f8-133">With D3DORDER\_CUBIC order: vertices (0) and (9) are used with pNumSegs\[0\], vertices (9) and (6) are used with pNumSegs\[1\] and vertices (6) and (0) are used with pNumSegs\[3\].</span></span>

<span data-ttu-id="883f8-134">Для N-патчей используются вершины треугольника.</span><span class="sxs-lookup"><span data-stu-id="883f8-134">For N-patches the triangle vertices are used.</span></span>

<span data-ttu-id="883f8-135">Для исправлений прямоугольника и треугольника с учетом Безье используются вершины угловой панели.</span><span class="sxs-lookup"><span data-stu-id="883f8-135">For the rectangle and triangle patches with a Bezier basis, the corner-control vertices are used.</span></span>

<span data-ttu-id="883f8-136">Управление скоростью тесселяции на вершину.</span><span class="sxs-lookup"><span data-stu-id="883f8-136">Per-vertex tessellation rate control.</span></span> <span data-ttu-id="883f8-137">Приложение может дополнительно предоставить одно положительное значение с плавающей запятой на вершину, которое можно использовать для управления частотой тесселяции.</span><span class="sxs-lookup"><span data-stu-id="883f8-137">An application can optionally supply a single positive floating-point value per vertex, which can be used to control the rate of tessellation.</span></span> <span data-ttu-id="883f8-138">Он предоставляется с помощью D3DDECLUSAGE \_ тессфактор, для которого индекс использования должен быть равен 0, а тип входных данных должен быть D3DDECLTYPE \_ FLOAT1.</span><span class="sxs-lookup"><span data-stu-id="883f8-138">This is supplied using the D3DDECLUSAGE\_TESSFACTOR, for which usage index must be 0 and input type must be D3DDECLTYPE\_FLOAT1.</span></span> <span data-ttu-id="883f8-139">Это умножается на уровень тесселяции на вершину.</span><span class="sxs-lookup"><span data-stu-id="883f8-139">This is multiplied to the per-vertex tessellation level.</span></span>

### <a name="math"></a><span data-ttu-id="883f8-140">Математический</span><span class="sxs-lookup"><span data-stu-id="883f8-140">Math</span></span>

<span data-ttu-id="883f8-141">Уровень тесселяции (TE) для пограничной e, представленный двумя вершинами управления (Ve1, Ve2), вычисляются, как показано ниже:</span><span class="sxs-lookup"><span data-stu-id="883f8-141">The tessellation level (Te) for an edge e, represented by two control vertices (Ve1, Ve2), is computed as shown below :</span></span>


```
Vertex Vi: (Xi, Yi, Zi, TFactori (optional)). 
Ze1eye = Ve1 . Mdm 
Ze2eye = Ve2 . Mdm 
Te1 = MaxTessellationLevel * TFactore1 / Ze1eye 
Te2 = MaxTessellationLevel * TFactore2 / Ze2eye 
Te = ( Te1 + Te2 ) / 2; 
if Te > D3DRS_MAXTESSELLATIONLEVEL || Te < 0, then Te = D3DRS_MAXTESSELLATIONLEVEL 
if Te < D3DRS_MINTESSELLATIONLEVEL, then Te = D3DRS_MINTESSELLATIONLEVEL 
```



<span data-ttu-id="883f8-142">Если D3DRS \_ енаблеадаптиветесселлатион имеет **значение true**, примитивы треугольника (списки треугольников, вентиляторы, полосы) рисуются как N-патчs, [**IDirect3DDevice9:: сетнпатчмоде**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode) имеет значение меньше 1,0.</span><span class="sxs-lookup"><span data-stu-id="883f8-142">When D3DRS\_ENABLEADAPTIVETESSELLATION is **TRUE**, triangle primitives (triangle lists, fans, strips) are drawn as N-patches, [**IDirect3DDevice9::SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode) has set value less than 1.0.</span></span>

### <a name="api-changes"></a><span data-ttu-id="883f8-143">Изменения API</span><span class="sxs-lookup"><span data-stu-id="883f8-143">API Changes</span></span>

<span data-ttu-id="883f8-144">Новые состояния рендеринга:</span><span class="sxs-lookup"><span data-stu-id="883f8-144">New render states:</span></span>


```
 D3DRS_ENABLEADAPTIVETESSELLATION // BOOL 
 D3DRS_MAXTESSELLATIONLEVEL       // Float 
 D3DRS_MINTESSELLATIONLEVEL       // Float 
 D3DRS_ADAPTIVETESS_X             // Float 
 D3DRS_ADAPTIVETESS_Y             // Float 
 D3DRS_ADAPTIVETESS_Z             // Float 
 D3DRS_ADAPTIVETESS_W             // Float 
 
 // D3DRS_MINTESSELLATIONLEVEL and D3DRS_MAXTESSELLATIONLEVEL 
 // cannot be less than 1 
```



<span data-ttu-id="883f8-145">И их значения по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="883f8-145">And their default values:</span></span>


```
D3DRS_MAXTESSELLATIONLEVEL = 1.0f 
D3DRS_MINTESSELLATIONLEVEL = 1.0f 
D3DRS_ADAPTIVETESS_X = 0.0f 
D3DRS_ADAPTIVETESS_Y = 0.0f 
D3DRS_ADAPTIVETESS_Z = 1.0f 
D3DRS_ADAPTIVETESS_W = 0.0f 
D3DRS_ENABLEADAPTIVETESSELLATION = FALSE 
```



<span data-ttu-id="883f8-146">Новые ограничения оборудования:</span><span class="sxs-lookup"><span data-stu-id="883f8-146">New hardware caps:</span></span>


```
D3DDEVCAPS2_ADAPTIVETESSRTPATCH // Can adaptively tessellate RT-patches 
D3DDEVCAPS2_ADAPTIVETESSNPATCH  // Can adaptively tessellate N-patches 
```



## <a name="related-topics"></a><span data-ttu-id="883f8-147">См. также</span><span class="sxs-lookup"><span data-stu-id="883f8-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="883f8-148">Конвейер вершин</span><span class="sxs-lookup"><span data-stu-id="883f8-148">Vertex Pipeline</span></span>](vertex-pipeline.md)
</dt> </dl>

 

 
