---
description: Пиксельный туман получает свое имя из того факта, что оно вычисляется на основе каждого пикселя в драйвере устройства.
ms.assetid: 6fcfb9fa-cacc-4dbc-bfc6-85d533dbfbf8
title: Пиксельный туман (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f62a597820fa009207d8dda7836d161cdf34c88
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103894086"
---
# <a name="pixel-fog-direct3d-9"></a><span data-ttu-id="e8523-103">Пиксельный туман (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="e8523-103">Pixel Fog (Direct3D 9)</span></span>

<span data-ttu-id="e8523-104">Пиксельный туман получает свое имя из того факта, что оно вычисляется на основе каждого пикселя в драйвере устройства.</span><span class="sxs-lookup"><span data-stu-id="e8523-104">Pixel fog gets its name from the fact that it is calculated on a per-pixel basis in the device driver.</span></span> <span data-ttu-id="e8523-105">Это отличается от вершинного тумана, вычисляемого конвейером во время вычислений преобразования и освещения.</span><span class="sxs-lookup"><span data-stu-id="e8523-105">This is different from vertex fog, which is computed by the pipeline during transformation and lighting calculations.</span></span> <span data-ttu-id="e8523-106">Пиксельные туманы иногда называются таблицами тумана, так как некоторые драйверы используют предварительно вычисленную таблицу подстановки для определения коэффициента тумана с использованием глубины каждого пикселя для применения в вычислениях смешения.</span><span class="sxs-lookup"><span data-stu-id="e8523-106">Pixel fog is sometimes called table fog because some drivers use a precalculated lookup table to determine the fog factor, using the depth of each pixel to apply in blending computations.</span></span> <span data-ttu-id="e8523-107">Его можно применить с помощью любой формулы тумана, определенной элементами перечисляемого типа [**D3DFOGMODE**](./d3dfogmode.md) .</span><span class="sxs-lookup"><span data-stu-id="e8523-107">It can be applied using any fog formula identified by members of the [**D3DFOGMODE**](./d3dfogmode.md) enumerated type.</span></span> <span data-ttu-id="e8523-108">Реализации этих формул зависят от драйвера.</span><span class="sxs-lookup"><span data-stu-id="e8523-108">The implementations of these formulas are driver-specific.</span></span> <span data-ttu-id="e8523-109">Если драйвер не поддерживает сложную формулу тумана, он должен быть снижен до менее сложной формулы.</span><span class="sxs-lookup"><span data-stu-id="e8523-109">If a driver doesn't support a complex fog formula, it should degrade to a less complex formula.</span></span>

## <a name="eye-relative-vs-z-based-depth"></a><span data-ttu-id="e8523-110">Eye-Relativeная и Z-глубина</span><span class="sxs-lookup"><span data-stu-id="e8523-110">Eye-Relative vs. Z-Based Depth</span></span>

<span data-ttu-id="e8523-111">Для смягчения связанных с туманом графических артефактов, вызванных неравномерной распределенностью z-значений в буфере глубины, большинство устройств используют глубину относительных глаз вместо z-значений глубины для пиксельного тумана.</span><span class="sxs-lookup"><span data-stu-id="e8523-111">To alleviate fog-related graphic artifacts caused by uneven distribution of z-values in a depth buffer, most hardware devices use eye-relative depth instead of z-based depth values for pixel fog.</span></span> <span data-ttu-id="e8523-112">Относительное количество глаз по сути является элементом w из однородного набора координат.</span><span class="sxs-lookup"><span data-stu-id="e8523-112">Eye-relative depth is essentially the w element from a homogeneous coordinate set.</span></span> <span data-ttu-id="e8523-113">Microsoft Direct3D берет обратную часть элемента РХВ из набора координат пространства устройства, чтобы воспроизвести значение true w.</span><span class="sxs-lookup"><span data-stu-id="e8523-113">Microsoft Direct3D takes the reciprocal of the RHW element from a device space coordinate set to reproduce true w.</span></span> <span data-ttu-id="e8523-114">Если устройство поддерживает туман, относительный от глаз, при вызове метода [**IDirect3DDevice9:: жетдевицекапс**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps) устанавливается флаг **D3DPRASTERCAPS \_ вфог** в элементе растеркапс структуры [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) .</span><span class="sxs-lookup"><span data-stu-id="e8523-114">If a device supports eye-relative fog, it sets the **D3DPRASTERCAPS\_WFOG** flag in the RasterCaps member of the [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure when you call the [**IDirect3DDevice9::GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps) method.</span></span> <span data-ttu-id="e8523-115">За исключением ссылки на средство программной прорисовки, устройства всегда используют z для вычисления эффектов Pixel тумана.</span><span class="sxs-lookup"><span data-stu-id="e8523-115">With the exception of the reference rasterizer, software devices always use z to calculate pixel fog effects.</span></span>

<span data-ttu-id="e8523-116">Когда поддерживается относительный туман, система автоматически использует глубину, отличную от глаза, а не z-глубину, если указанная матрица проекции создает в мировом пространстве z-значения, эквивалентные значениям w в пространстве устройства.</span><span class="sxs-lookup"><span data-stu-id="e8523-116">When eye-relative fog is supported, the system automatically uses eye-relative depth rather than z-based depth if the provided projection matrix produces z-values in world space that are equivalent to w-values in device space.</span></span> <span data-ttu-id="e8523-117">Чтобы задать матрицу проекции, вызовите метод [**IDirect3DDevice9:: сеттрансформ**](/windows/desktop/api) , используя \_ значение проекции D3DTS и передав структуру [**D3DMATRIX**](d3dmatrix.md) , представляющую нужную матрицу.</span><span class="sxs-lookup"><span data-stu-id="e8523-117">You set the projection matrix by calling the [**IDirect3DDevice9::SetTransform**](/windows/desktop/api) method, using the D3DTS\_PROJECTION value and passing a [**D3DMATRIX**](d3dmatrix.md) structure that represents the desired matrix.</span></span> <span data-ttu-id="e8523-118">Если матрица проекции не соответствует этому требованию, эффекты тумана не применяются должным образом.</span><span class="sxs-lookup"><span data-stu-id="e8523-118">If the projection matrix isn't compliant with this requirement, fog effects are not applied properly.</span></span> <span data-ttu-id="e8523-119">Дополнительные сведения о создании совместимой матрицы см. в разделе [преобразование проекции (Direct3D 9)](projection-transform.md).</span><span class="sxs-lookup"><span data-stu-id="e8523-119">For details about producing a compliant matrix, see [Projection Transform (Direct3D 9)](projection-transform.md).</span></span>

<span data-ttu-id="e8523-120">Direct3D использует текущую матрицу проекции при расчетах глубины вершин на основе переменной w.</span><span class="sxs-lookup"><span data-stu-id="e8523-120">Direct3D uses the currently set projection matrix in its w-based depth calculations.</span></span> <span data-ttu-id="e8523-121">В результате приложение должно установить соответствующую матрицу проекции для получения требуемых функций на основе w, даже если она не использует конвейер преобразования Direct3D.</span><span class="sxs-lookup"><span data-stu-id="e8523-121">As a result, an application must set a compliant projection matrix to receive the desired w-based features, even if it does not use the Direct3D transformation pipeline.</span></span>

<span data-ttu-id="e8523-122">Direct3D проверяет четвертый столбец матрицы проекции.</span><span class="sxs-lookup"><span data-stu-id="e8523-122">Direct3D checks the fourth column of the projection matrix.</span></span> <span data-ttu-id="e8523-123">Если коэффициенты равны \[ 0, 0, 0, 1 \] (для аффинных проекции), система будет использовать z-значения глубины для тумана.</span><span class="sxs-lookup"><span data-stu-id="e8523-123">If the coefficients are \[0,0,0,1\] (for an affine projection) the system will use z-based depth values for fog.</span></span> <span data-ttu-id="e8523-124">В этом случае необходимо также указать начальное и конечное расстояние для линейных эффектов тумана в пространстве устройства, которое находится в диапазоне от 0,0 в ближайшей точке к пользователю, а 1,0 — в самой последней точке.</span><span class="sxs-lookup"><span data-stu-id="e8523-124">In this case, you must also specify the start and end distances for linear fog effects in device space, which ranges from 0.0 at the nearest point to the user, and 1.0 at the farthest point.</span></span>

## <a name="using-pixel-fog"></a><span data-ttu-id="e8523-125">Использование пиксельного тумана</span><span class="sxs-lookup"><span data-stu-id="e8523-125">Using Pixel Fog</span></span>

<span data-ttu-id="e8523-126">Чтобы включить пиксельный туман в приложении, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="e8523-126">Use the following steps to enable pixel fog in your application.</span></span>

1.  <span data-ttu-id="e8523-127">Включите смешение тумана, установив \_ для состояния отрисовки D3DRS Фоженабле **значение true**.</span><span class="sxs-lookup"><span data-stu-id="e8523-127">Enable fog blending by setting the D3DRS\_FOGENABLE render state to **TRUE**.</span></span>
2.  <span data-ttu-id="e8523-128">Задайте нужный цвет тумана в \_ состоянии рендеринга D3DRS фогколор.</span><span class="sxs-lookup"><span data-stu-id="e8523-128">Set the desired fog color in the D3DRS\_FOGCOLOR render state.</span></span>
3.  <span data-ttu-id="e8523-129">Выберите формулу тумана, чтобы использовать ее, установив \_ для состояния отрисовки D3DRS фогтаблемоде соответствующий элемент перечисляемого типа [**D3DFOGMODE**](./d3dfogmode.md) .</span><span class="sxs-lookup"><span data-stu-id="e8523-129">Choose the fog formula to use by setting the D3DRS\_FOGTABLEMODE render state to the corresponding member of the [**D3DFOGMODE**](./d3dfogmode.md) enumerated type.</span></span>
4.  <span data-ttu-id="e8523-130">Задайте необходимые параметры тумана для выбранного режима тумана в связанных состояниях рендеринга.</span><span class="sxs-lookup"><span data-stu-id="e8523-130">Set the fog parameters as desired for the selected fog mode in the associated render states.</span></span> <span data-ttu-id="e8523-131">Сюда входят начальное и конечное расстояния для линейной тумана, а также плотность тумана для режима экспоненциального тумана.</span><span class="sxs-lookup"><span data-stu-id="e8523-131">This includes the start and end distances for linear fog, and fog density for exponential fog mode.</span></span>

<span data-ttu-id="e8523-132">В следующем примере показано, как эти шаги могут выглядеть в коде.</span><span class="sxs-lookup"><span data-stu-id="e8523-132">The following example shows what these steps might look like in code.</span></span>


```
// For brevity, error values in this example are not checked 
//   after each call. A real-world application should check 
//   these values appropriately.
//
// For the purposes of this example, g_pDevice is a valid
//   pointer to an IDirect3DDevice9 interface.
void SetupPixelFog(DWORD Color, DWORD Mode)
{
    float Start   = 0.5f;    // For linear mode
    float End     = 0.8f;
    float Density = 0.66f;   // For exponential modes
 
    // Enable fog blending.
    g_pDevice->SetRenderState(D3DRS_FOGENABLE, TRUE);
 
    // Set the fog color.
    g_pDevice->SetRenderState(D3DRS_FOGCOLOR, Color);
    
    // Set fog parameters.
    if( Mode == D3DFOG_LINEAR )
    {
        g_pDevice->SetRenderState(D3DRS_FOGTABLEMODE, Mode);
        g_pDevice->SetRenderState(D3DRS_FOGSTART, *(DWORD *)(&Start));
        g_pDevice->SetRenderState(D3DRS_FOGEND,   *(DWORD *)(&End));
    }
    else
    {
        g_pDevice->SetRenderState(D3DRS_FOGTABLEMODE, Mode);
        g_pDevice->SetRenderState(D3DRS_FOGDENSITY, *(DWORD *)(&Density));
    }
```



<span data-ttu-id="e8523-133">Некоторые параметры тумана требуются в качестве значений с плавающей запятой, хотя метод [**IDirect3DDevice9:: сетрендерстате**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) принимает только значения типа DWORD во втором параметре.</span><span class="sxs-lookup"><span data-stu-id="e8523-133">Some fog parameters are required as floating-point values, even though the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method accepts only DWORD values in the second parameter.</span></span> <span data-ttu-id="e8523-134">В предыдущем примере значения с плавающей запятой переводятся в **IDirect3DDevice9:: сетрендерстате** без преобразования данных путем приведения адресов переменных с плавающей запятой в виде УКАЗАТЕЛЕЙ типа DWORD и последующей разыменования их.</span><span class="sxs-lookup"><span data-stu-id="e8523-134">The preceding example provides the floating-point values to **IDirect3DDevice9::SetRenderState** without data translation by casting the addresses of the floating-point variables as DWORD pointers, and then dereferencing them.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e8523-135">См. также</span><span class="sxs-lookup"><span data-stu-id="e8523-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e8523-136">Типы туманов</span><span class="sxs-lookup"><span data-stu-id="e8523-136">Fog Types</span></span>](fog-types.md)
</dt> </dl>

 

 
