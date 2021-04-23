---
description: Когда система выполняет фоггинг вершин, она применяет вычисления тумана на каждой вершине многоугольника, а затем интерполирует результаты по грани многоугольника во время растрирования.
ms.assetid: 76989eb3-cd95-4dfc-ba0f-7563860b531c
title: Вершинный туман (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35cd880bda7ebffd36bd95bec5f8565e104eaa15
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104139210"
---
# <a name="vertex-fog-direct3d-9"></a><span data-ttu-id="10393-103">Вершинный туман (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="10393-103">Vertex Fog (Direct3D 9)</span></span>

<span data-ttu-id="10393-104">Когда система выполняет фоггинг вершин, она применяет вычисления тумана на каждой вершине многоугольника, а затем интерполирует результаты по грани многоугольника во время растрирования.</span><span class="sxs-lookup"><span data-stu-id="10393-104">When the system performs vertex fogging, it applies fog calculations at each vertex in a polygon, and then interpolates the results across the face of the polygon during rasterization.</span></span> <span data-ttu-id="10393-105">Эффекты вершинных туманов вычисляются с помощью модуля освещения Direct3D и механизма преобразования.</span><span class="sxs-lookup"><span data-stu-id="10393-105">Vertex fog effects are computed by the Direct3D lighting and transformation engine.</span></span> <span data-ttu-id="10393-106">Дополнительные сведения см. в разделе [Параметры тумана (Direct3D 9)](fog-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="10393-106">For more information, see [Fog Parameters (Direct3D 9)](fog-parameters.md).</span></span>

<span data-ttu-id="10393-107">Если приложение не использует Direct3D для преобразования и освещения, приложение должно выполнять вычисления тумана.</span><span class="sxs-lookup"><span data-stu-id="10393-107">If your application does not use Direct3D for transformation and lighting, the application must perform fog calculations.</span></span> <span data-ttu-id="10393-108">В этом случае поместите коэффициент тумана, который будет вычислен в альфа-компоненте отраженного цвета для каждой вершины.</span><span class="sxs-lookup"><span data-stu-id="10393-108">In this case, place the fog factor that is computed in the alpha component of the specular color for each vertex.</span></span> <span data-ttu-id="10393-109">Вы можете использовать любые формулы, которые должны быть основаны на диапазоне, объемные или иным образом.</span><span class="sxs-lookup"><span data-stu-id="10393-109">You are free to use whatever formulas you want - range-based, volumetric, or otherwise.</span></span> <span data-ttu-id="10393-110">Direct3D использует указанный коэффициент тумана для интерполяции по грани каждого многоугольника.</span><span class="sxs-lookup"><span data-stu-id="10393-110">Direct3D uses the supplied fog factor to interpolate across the face of each polygon.</span></span> <span data-ttu-id="10393-111">Приложения, выполняющие собственное преобразование и освещение, должны также выполнять собственные вычисления вершинных туманов.</span><span class="sxs-lookup"><span data-stu-id="10393-111">Applications that perform their own transformation and lighting must also perform their own vertex fog calculations.</span></span> <span data-ttu-id="10393-112">В результате такого приложения требуется только включить смешение тумана и задать цвет тумана с помощью связанных состояний рендеринга, как описано в разделе [смешение тумана (Direct3D 9)](fog-blending.md) и [Цвет тумана (Direct3D 9)](fog-color.md).</span><span class="sxs-lookup"><span data-stu-id="10393-112">As a result, such an application need only enable fog blending and set the fog color through the associated render states, as described in [Fog Blending (Direct3D 9)](fog-blending.md) and [Fog Color (Direct3D 9)](fog-color.md).</span></span>

> [!Note]  
> <span data-ttu-id="10393-113">При использовании шейдера вершин необходимо использовать вершинный туман.</span><span class="sxs-lookup"><span data-stu-id="10393-113">When using a vertex shader, you must use vertex fog.</span></span> <span data-ttu-id="10393-114">Это достигается с помощью шейдера вершин для записи интенсивности тумана на вершину в регистр Офог.</span><span class="sxs-lookup"><span data-stu-id="10393-114">This is accomplished by using the vertex shader to write the per-vertex fog intensity to the oFog register.</span></span> <span data-ttu-id="10393-115">После завершения построителя текстуры данные Офог используются для линейной интерполяции с помощью цвета тумана.</span><span class="sxs-lookup"><span data-stu-id="10393-115">After the pixel shader completes, the oFog data is used to linearly interpolate with the fog color.</span></span> <span data-ttu-id="10393-116">Эта интенсивность недоступна в шейдере пикселей.</span><span class="sxs-lookup"><span data-stu-id="10393-116">This intensity is not available in a pixel shader.</span></span>

 

## <a name="range-based-fog"></a><span data-ttu-id="10393-117">Range-Based туман</span><span class="sxs-lookup"><span data-stu-id="10393-117">Range-Based Fog</span></span>

> [!Note]  
> <span data-ttu-id="10393-118">Direct3D использует вычисления тумана на основе диапазонов только при использовании вершинного тумана с модулем преобразования и освещения Direct3D.</span><span class="sxs-lookup"><span data-stu-id="10393-118">Direct3D uses range-based fog calculations only when using vertex fog with the Direct3D transformation and lighting engine.</span></span> <span data-ttu-id="10393-119">Это связано с тем, что пиксельный туман реализован в драйвере устройства и не существует оборудования для поддержки тумана, основанного на диапазоне пикселей.</span><span class="sxs-lookup"><span data-stu-id="10393-119">This is because pixel fog is implemented in the device driver, and no hardware currently exists to support per-pixel range-based fog.</span></span> <span data-ttu-id="10393-120">Если приложение выполняет собственное преобразование и освещение, оно должно выполнять собственные вычисления тумана, основанные на диапазоне или иным образом.</span><span class="sxs-lookup"><span data-stu-id="10393-120">If your application performs its own transformation and lighting, it must perform its own fog calculations, range-based or otherwise.</span></span>

 

<span data-ttu-id="10393-121">В некоторых случаях использование тумана может привести к созданию графических артефактов, которые приводят к тому, что объекты будут смешиваться с цветом тумана неинтуитивно понятными способами.</span><span class="sxs-lookup"><span data-stu-id="10393-121">Sometimes, using fog can introduce graphic artifacts that cause objects to be blended with the fog color in nonintuitive ways.</span></span> <span data-ttu-id="10393-122">Например, представьте себе сцену, в которой есть два видимых объекта: один отдаленный, на который повлияет туман, а другой — достаточно, чтобы не затронуть.</span><span class="sxs-lookup"><span data-stu-id="10393-122">For example, imagine a scene in which there are two visible objects: one distant enough to be affected by fog, and the other near enough to be unaffected.</span></span> <span data-ttu-id="10393-123">Если область просмотра поворачивается на месте, видимые эффекты тумана могут измениться, даже если объекты являются стационарными.</span><span class="sxs-lookup"><span data-stu-id="10393-123">If the viewing area rotates in place, the apparent fog effects can change, even if the objects are stationary.</span></span> <span data-ttu-id="10393-124">На следующей диаграмме показано представление такой ситуации сверху вниз.</span><span class="sxs-lookup"><span data-stu-id="10393-124">The following diagram shows a top-down view of such a situation.</span></span>

![схема двух точек зрения и их влияние на туман для двух объектов](images/artifog.png)

<span data-ttu-id="10393-126">Туман на основе диапазона — это еще один, более точный способ определения эффектов тумана.</span><span class="sxs-lookup"><span data-stu-id="10393-126">Range-based fog is another, more accurate, way to determine the fog effects.</span></span> <span data-ttu-id="10393-127">В тумане на основе диапазона Direct3D использует фактическое расстояние от точки зрения до вершины для вычислений тумана.</span><span class="sxs-lookup"><span data-stu-id="10393-127">In range-based fog, Direct3D uses the actual distance from the viewpoint to a vertex for its fog calculations.</span></span> <span data-ttu-id="10393-128">Direct3D увеличивает воздействие тумана по мере увеличения расстояния между двумя точками, а не глубиной вершины внутри сцены, тем самым избегая вращения артефактов.</span><span class="sxs-lookup"><span data-stu-id="10393-128">Direct3D increases the effect of fog as the distance between the two points increases, rather than the depth of the vertex within in the scene, thereby avoiding rotational artifacts.</span></span>

<span data-ttu-id="10393-129">Если текущее устройство поддерживает туман на основе диапазонов, то \_ при вызове метода [**IDirect3DDevice9:: жетдевицекапс**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps) будет задано значение D3DPRASTERCAPS Фогранже в элементе растеркапс [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) .</span><span class="sxs-lookup"><span data-stu-id="10393-129">If the current device supports range-based fog, it will set the D3DPRASTERCAPS\_FOGRANGE value in the RasterCaps member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) when you call the [**IDirect3DDevice9::GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps) method.</span></span> <span data-ttu-id="10393-130">Чтобы включить туман на основе диапазона, установите \_ для состояния отрисовки D3DRS Ранжефоженабле **значение true**.</span><span class="sxs-lookup"><span data-stu-id="10393-130">To enable range-based fog, set the D3DRS\_RANGEFOGENABLE render state to **TRUE**.</span></span>

<span data-ttu-id="10393-131">Туман на основе диапазона вычисляются Direct3D во время преобразования и освещения.</span><span class="sxs-lookup"><span data-stu-id="10393-131">Range-based fog is computed by Direct3D during transformation and lighting.</span></span> <span data-ttu-id="10393-132">Приложения, которые не используют механизм преобразования и освещения Direct3D, также должны выполнять собственные вычисления вершинных туманов.</span><span class="sxs-lookup"><span data-stu-id="10393-132">Applications that don't use the Direct3D transformation and lighting engine must also perform their own vertex fog calculations.</span></span> <span data-ttu-id="10393-133">В этом случае укажите коэффициент тумана на основе диапазона в альфа-компоненте отраженного компонента для каждой вершины.</span><span class="sxs-lookup"><span data-stu-id="10393-133">In this case, provide the range-based fog factor in the alpha component of the specular component for each vertex.</span></span>

## <a name="using-vertex-fog"></a><span data-ttu-id="10393-134">Использование вершинного тумана</span><span class="sxs-lookup"><span data-stu-id="10393-134">Using Vertex Fog</span></span>

<span data-ttu-id="10393-135">Чтобы включить вершину тумана в приложении, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="10393-135">Use the following steps to enable vertex fog in your application.</span></span>

1.  <span data-ttu-id="10393-136">Включите смешение тумана, задав \_ для D3DRS Фоженабле **значение true**.</span><span class="sxs-lookup"><span data-stu-id="10393-136">Enable fog blending by setting D3DRS\_FOGENABLE to **TRUE**.</span></span>
2.  <span data-ttu-id="10393-137">Задайте цвет тумана в \_ состоянии рендеринга D3DRS фогколор.</span><span class="sxs-lookup"><span data-stu-id="10393-137">Set the fog color in the D3DRS\_FOGCOLOR render state.</span></span>
3.  <span data-ttu-id="10393-138">Выберите нужную формулу тумана, задав \_ для состояния отрисовки D3DRS фогвертексмоде элемент перечисляемого типа [**D3DFOGMODE**](./d3dfogmode.md) .</span><span class="sxs-lookup"><span data-stu-id="10393-138">Choose the desired fog formula by setting the D3DRS\_FOGVERTEXMODE render state to a member of the [**D3DFOGMODE**](./d3dfogmode.md) enumerated type.</span></span>
4.  <span data-ttu-id="10393-139">Задайте необходимые параметры тумана для выбранной формулы тумана в состояниях рендеринга.</span><span class="sxs-lookup"><span data-stu-id="10393-139">Set the fog parameters as desired for the selected fog formula in the render states.</span></span>

<span data-ttu-id="10393-140">В следующем примере, написанном на C++, показано, как эти шаги могут выглядеть в коде.</span><span class="sxs-lookup"><span data-stu-id="10393-140">The following example, written in C++, shows what these steps might look like in code.</span></span>


```
// For brevity, error values in this example are not checked 
//   after each call. A real-world application should check 
//   these values appropriately.
//
// For the purposes of this example, g_pDevice is a valid
//   pointer to an IDirect3DDevice9 interface.
void SetupVertexFog(DWORD Color, DWORD Mode, BOOL UseRange, FLOAT Density)
{
    float Start = 0.5f,    // Linear fog distances
          End   = 0.8f;
 
    // Enable fog blending.
    g_pDevice->SetRenderState(D3DRS_FOGENABLE, TRUE);
 
    // Set the fog color.
    g_pDevice->SetRenderState(D3DRS_FOGCOLOR, Color);
    
    // Set fog parameters.
    if(D3DFOG_LINEAR == Mode)
    {
        g_pDevice->SetRenderState(D3DRS_FOGVERTEXMODE, Mode);
        g_pDevice->SetRenderState(D3DRS_FOGSTART, *(DWORD *)(&Start));
        g_pDevice->SetRenderState(D3DRS_FOGEND,   *(DWORD *)(&End));
    }
    else
    {
        g_pDevice->SetRenderState(D3DRS_FOGVERTEXMODE, Mode);
        g_pDevice->SetRenderState(D3DRS_FOGDENSITY, *(DWORD *)(&Density));
    }

    // Enable range-based fog if desired (only supported for
    //   vertex fog). For this example, it is assumed that UseRange
    //   is set to a nonzero value only if the driver exposes the 
    //   D3DPRASTERCAPS_FOGRANGE capability.
    // Note: This is slightly more performance intensive
    //   than non-range-based fog.
    if(UseRange)
        g_pDevice->SetRenderState(D3DRS_RANGEFOGENABLE, TRUE);
}
```



<span data-ttu-id="10393-141">Некоторые параметры тумана требуются в качестве значений с плавающей запятой, хотя метод [**IDirect3DDevice9:: сетрендерстате**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) принимает только значения типа DWORD во втором параметре.</span><span class="sxs-lookup"><span data-stu-id="10393-141">Some fog parameters are required as floating-point values, even though the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method only accepts DWORD values in the second parameter.</span></span> <span data-ttu-id="10393-142">В этом примере значения с плавающей запятой успешно предоставляются этим методам без преобразования данных путем приведения адресов переменных с плавающей запятой в виде указателей типа DWORD, а затем разыменования их.</span><span class="sxs-lookup"><span data-stu-id="10393-142">This example successfully provides the floating-point values to these methods without data translation by casting the addresses of the floating-point variables as DWORD pointers, and then dereferencing them.</span></span>

## <a name="related-topics"></a><span data-ttu-id="10393-143">См. также</span><span class="sxs-lookup"><span data-stu-id="10393-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="10393-144">Типы туманов</span><span class="sxs-lookup"><span data-stu-id="10393-144">Fog Types</span></span>](fog-types.md)
</dt> </dl>

 

 
