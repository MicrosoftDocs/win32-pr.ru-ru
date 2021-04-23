---
description: Описывает параметры представления.
ms.assetid: d677aeb7-a188-4ddc-b8c9-48e13676e9c8
title: Структура D3DPRESENT_PARAMETERS (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DPRESENT_PARAMETERS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: f83ab03773356a01c8c6ac490bb099c6e7508be2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355060"
---
# <a name="d3dpresent_parameters-structure"></a><span data-ttu-id="110f8-103">\_Структура параметров D3DPRESENT</span><span class="sxs-lookup"><span data-stu-id="110f8-103">D3DPRESENT\_PARAMETERS structure</span></span>

<span data-ttu-id="110f8-104">Описывает параметры представления.</span><span class="sxs-lookup"><span data-stu-id="110f8-104">Describes the presentation parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="110f8-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="110f8-105">Syntax</span></span>


```C++
typedef struct D3DPRESENT_PARAMETERS {
  UINT                BackBufferWidth;
  UINT                BackBufferHeight;
  D3DFORMAT           BackBufferFormat;
  UINT                BackBufferCount;
  D3DMULTISAMPLE_TYPE MultiSampleType;
  DWORD               MultiSampleQuality;
  D3DSWAPEFFECT       SwapEffect;
  HWND                hDeviceWindow;
  BOOL                Windowed;
  BOOL                EnableAutoDepthStencil;
  D3DFORMAT           AutoDepthStencilFormat;
  DWORD               Flags;
  UINT                FullScreen_RefreshRateInHz;
  UINT                PresentationInterval;
} D3DPRESENT_PARAMETERS, *LPD3DPRESENT_PARAMETERS;
```



## <a name="members"></a><span data-ttu-id="110f8-106">Члены</span><span class="sxs-lookup"><span data-stu-id="110f8-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="110f8-107">**баккбуффервидс**</span><span class="sxs-lookup"><span data-stu-id="110f8-107">**BackBufferWidth**</span></span>
</dt> <dd>

<span data-ttu-id="110f8-108">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="110f8-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="110f8-109">Ширина задних буферов новой цепочки перекачки в пикселях.</span><span class="sxs-lookup"><span data-stu-id="110f8-109">Width of the new swap chain's back buffers, in pixels.</span></span> <span data-ttu-id="110f8-110">Если **окно** имеет **значение false** (презентация находится в полноэкранном режиме), это значение должно быть равно ширине одного из перечисляемых режимов отображения, найденных с помощью [**енумадаптермодес**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes).</span><span class="sxs-lookup"><span data-stu-id="110f8-110">If **Windowed** is **FALSE** (the presentation is full-screen), this value must equal the width of one of the enumerated display modes found through [**EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes).</span></span> <span data-ttu-id="110f8-111">Если **окно** имеет **значение true** , а **либо баккбуффервидс** , либо **баккбуфферхеигхт** равны нулю, выполняется соответствующее измерение клиентской области **хдевицевиндов** (или окна фокуса, если **хдевицевиндов** имеет **значение NULL**).</span><span class="sxs-lookup"><span data-stu-id="110f8-111">If **Windowed** is **TRUE** and either **BackBufferWidth** or **BackBufferHeight** is zero, the corresponding dimension of the client area of the **hDeviceWindow** (or the focus window, if **hDeviceWindow** is **NULL**) is taken.</span></span>

</dd> <dt>

<span data-ttu-id="110f8-112">**баккбуфферхеигхт**</span><span class="sxs-lookup"><span data-stu-id="110f8-112">**BackBufferHeight**</span></span>
</dt> <dd>

<span data-ttu-id="110f8-113">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="110f8-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="110f8-114">Высота задних буферов новой цепочки перекачки в пикселях.</span><span class="sxs-lookup"><span data-stu-id="110f8-114">Height of the new swap chain's back buffers, in pixels.</span></span> <span data-ttu-id="110f8-115">Если **окно** имеет **значение false** (презентация находится в полноэкранном режиме), это значение должно равняться высоте одного из перечисляемых режимов отображения, найденных с помощью [**енумадаптермодес**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes).</span><span class="sxs-lookup"><span data-stu-id="110f8-115">If **Windowed** is **FALSE** (the presentation is full-screen), this value must equal the height of one of the enumerated display modes found through [**EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes).</span></span> <span data-ttu-id="110f8-116">Если **окно** имеет **значение true** , а **либо баккбуффервидс** , либо **баккбуфферхеигхт** равны нулю, выполняется соответствующее измерение клиентской области **хдевицевиндов** (или окна фокуса, если **хдевицевиндов** имеет **значение NULL**).</span><span class="sxs-lookup"><span data-stu-id="110f8-116">If **Windowed** is **TRUE** and either **BackBufferWidth** or **BackBufferHeight** is zero, the corresponding dimension of the client area of the **hDeviceWindow** (or the focus window, if **hDeviceWindow** is **NULL**) is taken.</span></span>

</dd> <dt>

<span data-ttu-id="110f8-117">**баккбуфферформат**</span><span class="sxs-lookup"><span data-stu-id="110f8-117">**BackBufferFormat**</span></span>
</dt> <dd>

<span data-ttu-id="110f8-118">Тип: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="110f8-118">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="110f8-119">Формат заднего буфера.</span><span class="sxs-lookup"><span data-stu-id="110f8-119">The back buffer format.</span></span> <span data-ttu-id="110f8-120">Дополнительные сведения о форматах см. в разделе [D3DFORMAT](d3dformat.md).</span><span class="sxs-lookup"><span data-stu-id="110f8-120">For more information about formats, see [D3DFORMAT](d3dformat.md).</span></span> <span data-ttu-id="110f8-121">Это значение должно быть одним из форматов подготовки к просмотру, как проверено [**чеккдевицетипе**](/windows/desktop/api).</span><span class="sxs-lookup"><span data-stu-id="110f8-121">This value must be one of the render-target formats as validated by [**CheckDeviceType**](/windows/desktop/api).</span></span> <span data-ttu-id="110f8-122">Для получения текущего формата можно использовать [**жетдисплаймоде**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdisplaymode) .</span><span class="sxs-lookup"><span data-stu-id="110f8-122">You can use [**GetDisplayMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdisplaymode) to obtain the current format.</span></span>

<span data-ttu-id="110f8-123">На самом деле D3DFMT \_ Unknown можно указать для **баккбуфферформат** в оконном режиме.</span><span class="sxs-lookup"><span data-stu-id="110f8-123">In fact, D3DFMT\_UNKNOWN can be specified for the **BackBufferFormat** while in windowed mode.</span></span> <span data-ttu-id="110f8-124">Это указывает среде выполнения использовать текущий формат режима экрана и устраняет необходимость вызова [**жетдисплаймоде**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdisplaymode).</span><span class="sxs-lookup"><span data-stu-id="110f8-124">This tells the runtime to use the current display-mode format and eliminates the need to call [**GetDisplayMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdisplaymode).</span></span>

<span data-ttu-id="110f8-125">Для оконных приложений формат заднего буфера больше не должен соответствовать формату режима экрана, так как преобразование цветов теперь может быть выполнено оборудованием (если оборудование поддерживает преобразование цветов).</span><span class="sxs-lookup"><span data-stu-id="110f8-125">For windowed applications, the back buffer format no longer needs to match the display-mode format because color conversion can now be done by the hardware (if the hardware supports color conversion).</span></span> <span data-ttu-id="110f8-126">Набор возможных форматов заднего буфера ограничен, но среда выполнения позволит представить любой допустимый формат заднего буфера в любой формат рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="110f8-126">The set of possible back buffer formats is constrained, but the runtime will allow any valid back buffer format to be presented to any desktop format.</span></span> <span data-ttu-id="110f8-127">(Существует дополнительное требование, которое устройство должно быть работоспособным на рабочем столе; обычно устройства не работают в режиме 8 бит на пиксель.)</span><span class="sxs-lookup"><span data-stu-id="110f8-127">(There is the additional requirement that the device be operable in the desktop; devices typically do not operate in 8 bits per pixel modes.)</span></span>

<span data-ttu-id="110f8-128">Полноэкранные приложения не могут выполнять преобразование цветов.</span><span class="sxs-lookup"><span data-stu-id="110f8-128">Full-screen applications cannot do color conversion.</span></span>

</dd> <dt>

<span data-ttu-id="110f8-129">**баккбуфферкаунт**</span><span class="sxs-lookup"><span data-stu-id="110f8-129">**BackBufferCount**</span></span>
</dt> <dd>

<span data-ttu-id="110f8-130">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="110f8-130">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="110f8-131">Это значение может находиться в диапазоне от 0 до [D3DPRESENT \_ задних \_ буферов \_ максимум](d3dpresent-back-buffers.md) (или [D3DPRESENT в \_ обратном \_ буфере с \_ максимальным \_ ](d3dpresent-back-buffers.md) значением при использовании Direct3D 9Ex).</span><span class="sxs-lookup"><span data-stu-id="110f8-131">This value can be between 0 and [D3DPRESENT\_BACK\_BUFFERS\_MAX](d3dpresent-back-buffers.md) (or [D3DPRESENT\_BACK\_BUFFERS\_MAX\_EX](d3dpresent-back-buffers.md) when using Direct3D 9Ex).</span></span> <span data-ttu-id="110f8-132">Значения 0 обрабатываются как 1.</span><span class="sxs-lookup"><span data-stu-id="110f8-132">Values of 0 are treated as 1.</span></span> <span data-ttu-id="110f8-133">Если число задних буферов не может быть создано, среда выполнения не сможет вызвать метод и заполнит это значение количеством буферов, которые могли быть созданы.</span><span class="sxs-lookup"><span data-stu-id="110f8-133">If the number of back buffers cannot be created, the runtime will fail the method call and fill this value with the number of back buffers that could be created.</span></span> <span data-ttu-id="110f8-134">В результате приложение может вызывать метод дважды с той же \_ структурой параметров D3DPRESENT и ждать, когда она будет работать второй раз.</span><span class="sxs-lookup"><span data-stu-id="110f8-134">As a result, an application can call the method twice with the same D3DPRESENT\_PARAMETERS structure and expect it to work the second time.</span></span>

<span data-ttu-id="110f8-135">Метод завершается ошибкой, если невозможно создать один задний буфер.</span><span class="sxs-lookup"><span data-stu-id="110f8-135">The method fails if one back buffer cannot be created.</span></span> <span data-ttu-id="110f8-136">Значение **баккбуфферкаунт** влияет на то, какой набор эффектов переключения разрешен.</span><span class="sxs-lookup"><span data-stu-id="110f8-136">The value of **BackBufferCount** influences what set of swap effects are allowed.</span></span> <span data-ttu-id="110f8-137">В частности, любой \_ из D3DSWAPEFFECTых эффектов переключения копирования требует ровно один задний буфер.</span><span class="sxs-lookup"><span data-stu-id="110f8-137">Specifically, any D3DSWAPEFFECT\_COPY swap effect requires that there be exactly one back buffer.</span></span>

</dd> <dt>

<span data-ttu-id="110f8-138">**мултисамплетипе**</span><span class="sxs-lookup"><span data-stu-id="110f8-138">**MultiSampleType**</span></span>
</dt> <dd>

<span data-ttu-id="110f8-139">Тип: **[ **D3DMULTISAMPLE \_ тип**](./d3dmultisample-type.md)**</span><span class="sxs-lookup"><span data-stu-id="110f8-139">Type: **[**D3DMULTISAMPLE\_TYPE**](./d3dmultisample-type.md)**</span></span>

</dd> <dd>

<span data-ttu-id="110f8-140">Член перечисляемого [**типа \_ D3DMULTISAMPLE**](./d3dmultisample-type.md) .</span><span class="sxs-lookup"><span data-stu-id="110f8-140">Member of the [**D3DMULTISAMPLE\_TYPE**](./d3dmultisample-type.md) enumerated type.</span></span> <span data-ttu-id="110f8-141">Значение должно быть D3DMULTISAMPLE \_ None, если только для **SwapEffect** не задано D3DSWAPEFFECT \_ Discard.</span><span class="sxs-lookup"><span data-stu-id="110f8-141">The value must be D3DMULTISAMPLE\_NONE unless **SwapEffect** has been set to D3DSWAPEFFECT\_DISCARD.</span></span> <span data-ttu-id="110f8-142">Множественная выборка поддерживается только в том случае, если в результате переключения используется D3DSWAPEFFECT \_ Discard.</span><span class="sxs-lookup"><span data-stu-id="110f8-142">Multisampling is supported only if the swap effect is D3DSWAPEFFECT\_DISCARD.</span></span>

</dd> <dt>

<span data-ttu-id="110f8-143">**мултисамплекуалити**</span><span class="sxs-lookup"><span data-stu-id="110f8-143">**MultiSampleQuality**</span></span>
</dt> <dd>

<span data-ttu-id="110f8-144">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="110f8-144">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="110f8-145">Уровень качества.</span><span class="sxs-lookup"><span data-stu-id="110f8-145">Quality level.</span></span> <span data-ttu-id="110f8-146">Диапазон допустимых значений — от нуля до уровня, возвращенного Пкуалитилевелс, используемым [**чеккдевицемултисамплетипе**](/windows/desktop/api).</span><span class="sxs-lookup"><span data-stu-id="110f8-146">The valid range is between zero and one less than the level returned by pQualityLevels used by [**CheckDeviceMultiSampleType**](/windows/desktop/api).</span></span> <span data-ttu-id="110f8-147">Передача большего значения возвращает ошибку D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="110f8-147">Passing a larger value returns the error D3DERR\_INVALIDCALL.</span></span> <span data-ttu-id="110f8-148">Парные значения целевых объектов прорисовки или поверхности трафарета набора элементов и [**\_ типа D3DMULTISAMPLE**](./d3dmultisample-type.md) должны совпадать.</span><span class="sxs-lookup"><span data-stu-id="110f8-148">Paired values of render targets or of depth stencil surfaces and [**D3DMULTISAMPLE\_TYPE**](./d3dmultisample-type.md) must match.</span></span>

</dd> <dt>

<span data-ttu-id="110f8-149">**SwapEffect**</span><span class="sxs-lookup"><span data-stu-id="110f8-149">**SwapEffect**</span></span>
</dt> <dd>

<span data-ttu-id="110f8-150">Тип: **[ **D3DSWAPEFFECT**](./d3dswapeffect.md)**</span><span class="sxs-lookup"><span data-stu-id="110f8-150">Type: **[**D3DSWAPEFFECT**](./d3dswapeffect.md)**</span></span>

</dd> <dd>

<span data-ttu-id="110f8-151">Член перечисляемого типа [**D3DSWAPEFFECT**](./d3dswapeffect.md) .</span><span class="sxs-lookup"><span data-stu-id="110f8-151">Member of the [**D3DSWAPEFFECT**](./d3dswapeffect.md) enumerated type.</span></span> <span data-ttu-id="110f8-152">Среда выполнения гарантирует подразумеваемую семантику, касающуюся поведения буфера обмена. Таким образом, если **окно** имеет **значение true** , а для **SwapEffect** задано значение D3DSWAPEFFECT \_ reпереворот, среда выполнения создаст один лишний задний буфер и скопирует их, когда станет передним буфером во время презентации.</span><span class="sxs-lookup"><span data-stu-id="110f8-152">The runtime will guarantee the implied semantics concerning buffer swap behavior; therefore, if **Windowed** is **TRUE** and **SwapEffect** is set to D3DSWAPEFFECT\_FLIP, the runtime will create one extra back buffer and copy whichever becomes the front buffer at presentation time.</span></span>

<span data-ttu-id="110f8-153">D3DSWAPEFFECT \_ Copy требует, чтобы **баккбуфферкаунт** было установлено значение 1.</span><span class="sxs-lookup"><span data-stu-id="110f8-153">D3DSWAPEFFECT\_COPY requires that **BackBufferCount** be set to 1.</span></span>

<span data-ttu-id="110f8-154">D3DSWAPEFFECT \_ Отмена будет применена в отладочной среде выполнения путем заполнения любого буфера с шумом после его представления.</span><span class="sxs-lookup"><span data-stu-id="110f8-154">D3DSWAPEFFECT\_DISCARD will be enforced in the debug runtime by filling any buffer with noise after it is presented.</span></span>



|                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="110f8-155">Различия между Direct3D9 и Direct3D9Ex</span><span class="sxs-lookup"><span data-stu-id="110f8-155">Differences between Direct3D9 and Direct3D9Ex</span></span><br/> <span data-ttu-id="110f8-156">В Direct3D9Ex \_ добавляется D3DSWAPEFFECT флипекс, чтобы обозначить, когда приложение использует режим перелистывания.</span><span class="sxs-lookup"><span data-stu-id="110f8-156">In Direct3D9Ex, D3DSWAPEFFECT\_FLIPEX is added to designate when an application is adopting flip mode.</span></span> <span data-ttu-id="110f8-157">То есть вхан фрейм приложения передается в режим окна (вместо копирования) в диспетчер окон рабочего стола (DWM) для композиции.</span><span class="sxs-lookup"><span data-stu-id="110f8-157">That is, whan an application's frame is passed in window's mode (instead of copied) to the Desktop Window Manager(DWM) for composition.</span></span> <span data-ttu-id="110f8-158">Режим перелистывания обеспечивает более эффективную пропускную способность памяти и позволяет приложению воспользоваться преимуществами полноценного отображения статистики.</span><span class="sxs-lookup"><span data-stu-id="110f8-158">Flip mode provides more efficient memory bandwidth and enables an application to take advantage of full-screen-present statistics.</span></span> <span data-ttu-id="110f8-159">Он не изменяет режим работы во весь экран.</span><span class="sxs-lookup"><span data-stu-id="110f8-159">It does not change full screen behavior.</span></span> <span data-ttu-id="110f8-160">Поведение режима отражения доступно начиная с Windows 7.</span><span class="sxs-lookup"><span data-stu-id="110f8-160">Flip mode behavior is available beginning with Windows 7.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="110f8-161">**хдевицевиндов**</span><span class="sxs-lookup"><span data-stu-id="110f8-161">**hDeviceWindow**</span></span>
</dt> <dd>

<span data-ttu-id="110f8-162">Тип: **[ **HWND**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="110f8-162">Type: **[**HWND**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="110f8-163">Окно устройства определяет расположение и размер заднего буфера на экране.</span><span class="sxs-lookup"><span data-stu-id="110f8-163">The device window determines the location and size of the back buffer on screen.</span></span> <span data-ttu-id="110f8-164">Это используется Direct3D, когда содержимое заднего буфера копируется в передний буфер во время их [**присутствия**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present).</span><span class="sxs-lookup"><span data-stu-id="110f8-164">This is used by Direct3D when the back buffer contents are copied to the front buffer during [**Present**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present).</span></span>

-   <span data-ttu-id="110f8-165">Для полноэкранного приложения это является обработчиком для верхнего окна (которое является окном фокуса).</span><span class="sxs-lookup"><span data-stu-id="110f8-165">For a full-screen application, this is a handle to the top window (which is the focus window).</span></span>

    <span data-ttu-id="110f8-166">Для приложений, использующих несколько полноэкранных устройств (например, систему с несколькими мониторами), в качестве окна устройства можно использовать только одно устройство.</span><span class="sxs-lookup"><span data-stu-id="110f8-166">For applications that use multiple full-screen devices (such as a multimonitor system), exactly one device can use the focus window as the device window.</span></span> <span data-ttu-id="110f8-167">Все остальные устройства должны иметь уникальные окна устройств.</span><span class="sxs-lookup"><span data-stu-id="110f8-167">All other devices must have unique device windows.</span></span>

-   <span data-ttu-id="110f8-168">Для оконного приложения этот обработчик будет использоваться в качестве целевого окна по умолчанию для [**представления**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present).</span><span class="sxs-lookup"><span data-stu-id="110f8-168">For a windowed-mode application, this handle will be the default target window for [**Present**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present).</span></span> <span data-ttu-id="110f8-169">Если этот маркер имеет **значение NULL**, то окно фокуса будет принято.</span><span class="sxs-lookup"><span data-stu-id="110f8-169">If this handle is **NULL**, the focus window will be taken.</span></span>

<span data-ttu-id="110f8-170">Обратите внимание, что среда выполнения не предоставила никаких попыток, чтобы отразить изменения, внесенные пользователем в размер окна.</span><span class="sxs-lookup"><span data-stu-id="110f8-170">Note that no attempt is made by the runtime to reflect user changes in window size.</span></span> <span data-ttu-id="110f8-171">Задний буфер не будет неявно сброшен при сбросе этого окна.</span><span class="sxs-lookup"><span data-stu-id="110f8-171">The back buffer is not implicitly reset when this window is reset.</span></span> <span data-ttu-id="110f8-172">Однако [**текущий**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) метод автоматически следит за изменениями расположения окна.</span><span class="sxs-lookup"><span data-stu-id="110f8-172">However, the [**Present**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) method does automatically track window position changes.</span></span>

</dd> <dt>

<span data-ttu-id="110f8-173">**Оконные**</span><span class="sxs-lookup"><span data-stu-id="110f8-173">**Windowed**</span></span>
</dt> <dd>

<span data-ttu-id="110f8-174">Тип: **[ **bool** .](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="110f8-174">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="110f8-175">**Значение true** , если приложение запускается с окнами; **Значение false** , если приложение работает в полноэкранном режиме.</span><span class="sxs-lookup"><span data-stu-id="110f8-175">**TRUE** if the application runs windowed; **FALSE** if the application runs full-screen.</span></span>

</dd> <dt>

<span data-ttu-id="110f8-176">**енаблеаутодепсстенЦил**</span><span class="sxs-lookup"><span data-stu-id="110f8-176">**EnableAutoDepthStencil**</span></span>
</dt> <dd>

<span data-ttu-id="110f8-177">Тип: **[ **bool** .](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="110f8-177">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="110f8-178">Если это значение равно **true**, то Direct3D будет управлять буферами глубины для приложения.</span><span class="sxs-lookup"><span data-stu-id="110f8-178">If this value is **TRUE**, Direct3D will manage depth buffers for the application.</span></span> <span data-ttu-id="110f8-179">Устройство создаст буфер шаблона глубины при его создании.</span><span class="sxs-lookup"><span data-stu-id="110f8-179">The device will create a depth-stencil buffer when it is created.</span></span> <span data-ttu-id="110f8-180">Буфер шаблона глубины будет автоматически установлен в качестве целевого объекта рендеринга для устройства.</span><span class="sxs-lookup"><span data-stu-id="110f8-180">The depth-stencil buffer will be automatically set as the render target of the device.</span></span> <span data-ttu-id="110f8-181">При сбросе устройства буфер шаблона глубины автоматически уничтожается и создается заново в новом размере.</span><span class="sxs-lookup"><span data-stu-id="110f8-181">When the device is reset, the depth-stencil buffer will be automatically destroyed and recreated in the new size.</span></span>

<span data-ttu-id="110f8-182">Если ЕнаблеаутодепсстенЦил имеет **значение true**, то аутодепсстенЦилформат должен быть допустимым форматом трафарета глубины.</span><span class="sxs-lookup"><span data-stu-id="110f8-182">If EnableAutoDepthStencil is **TRUE**, then AutoDepthStencilFormat must be a valid depth-stencil format.</span></span>

</dd> <dt>

<span data-ttu-id="110f8-183">**аутодепсстенЦилформат**</span><span class="sxs-lookup"><span data-stu-id="110f8-183">**AutoDepthStencilFormat**</span></span>
</dt> <dd>

<span data-ttu-id="110f8-184">Тип: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="110f8-184">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="110f8-185">Член перечисляемого типа [D3DFORMAT](d3dformat.md) .</span><span class="sxs-lookup"><span data-stu-id="110f8-185">Member of the [D3DFORMAT](d3dformat.md) enumerated type.</span></span> <span data-ttu-id="110f8-186">Формат поверхности автоматического набора элементов глубины, который будет создан устройством.</span><span class="sxs-lookup"><span data-stu-id="110f8-186">The format of the automatic depth-stencil surface that the device will create.</span></span> <span data-ttu-id="110f8-187">Этот элемент игнорируется, если **енаблеаутодепсстенЦил** имеет **значение true**.</span><span class="sxs-lookup"><span data-stu-id="110f8-187">This member is ignored unless **EnableAutoDepthStencil** is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="110f8-188">**Флаги**</span><span class="sxs-lookup"><span data-stu-id="110f8-188">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="110f8-189">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="110f8-189">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="110f8-190">Одна из констант [D3DPRESENTFLAG](d3dpresentflag.md) .</span><span class="sxs-lookup"><span data-stu-id="110f8-190">One of the [D3DPRESENTFLAG](d3dpresentflag.md) constants.</span></span>

</dd> <dt>

<span data-ttu-id="110f8-191">**Полноэкранный \_ рефрешратеинхз**</span><span class="sxs-lookup"><span data-stu-id="110f8-191">**FullScreen\_RefreshRateInHz**</span></span>
</dt> <dd>

<span data-ttu-id="110f8-192">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="110f8-192">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="110f8-193">Скорость, с которой адаптер отображения обновляет экран.</span><span class="sxs-lookup"><span data-stu-id="110f8-193">The rate at which the display adapter refreshes the screen.</span></span> <span data-ttu-id="110f8-194">Значение зависит от режима, в котором выполняется приложение:</span><span class="sxs-lookup"><span data-stu-id="110f8-194">The value depends on the mode in which the application is running:</span></span>

-   <span data-ttu-id="110f8-195">Для оконного режима частота обновления должна быть равна 0.</span><span class="sxs-lookup"><span data-stu-id="110f8-195">For windowed mode, the refresh rate must be 0.</span></span>
-   <span data-ttu-id="110f8-196">Для полноэкранного режима частота обновления является одной из частот обновления, возвращаемых функцией [**енумадаптермодес**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes).</span><span class="sxs-lookup"><span data-stu-id="110f8-196">For full-screen mode, the refresh rate is one of the refresh rates returned by [**EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes).</span></span>

</dd> <dt>

<span data-ttu-id="110f8-197">**пресентатионинтервал**</span><span class="sxs-lookup"><span data-stu-id="110f8-197">**PresentationInterval**</span></span>
</dt> <dd>

<span data-ttu-id="110f8-198">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="110f8-198">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="110f8-199">Максимальная скорость, с которой задние буферы цепочки перекачки можно представить в передний буфер.</span><span class="sxs-lookup"><span data-stu-id="110f8-199">The maximum rate at which the swap chain's back buffers can be presented to the front buffer.</span></span> <span data-ttu-id="110f8-200">Подробное описание режимов и поддерживаемых интервалов см. в разделе [D3DPRESENT](d3dpresent.md).</span><span class="sxs-lookup"><span data-stu-id="110f8-200">For a detailed explanation of the modes and the intervals that are supported, see [D3DPRESENT](d3dpresent.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="110f8-201">Требования</span><span class="sxs-lookup"><span data-stu-id="110f8-201">Requirements</span></span>



| <span data-ttu-id="110f8-202">Требование</span><span class="sxs-lookup"><span data-stu-id="110f8-202">Requirement</span></span> | <span data-ttu-id="110f8-203">Значение</span><span class="sxs-lookup"><span data-stu-id="110f8-203">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="110f8-204">Header</span><span class="sxs-lookup"><span data-stu-id="110f8-204">Header</span></span><br/> | <dl> <span data-ttu-id="110f8-205"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="110f8-205"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="110f8-206">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="110f8-206">See also</span></span>

<dl> <dt>

[<span data-ttu-id="110f8-207">Структуры Direct3D</span><span class="sxs-lookup"><span data-stu-id="110f8-207">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="110f8-208">**креатедевице**</span><span class="sxs-lookup"><span data-stu-id="110f8-208">**CreateDevice**</span></span>](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice)
</dt> <dt>

[<span data-ttu-id="110f8-209">**креатеаддитионалсвапчаин**</span><span class="sxs-lookup"><span data-stu-id="110f8-209">**CreateAdditionalSwapChain**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createadditionalswapchain)
</dt> <dt>

[<span data-ttu-id="110f8-210">**Настоящее**</span><span class="sxs-lookup"><span data-stu-id="110f8-210">**Present**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present)
</dt> <dt>

[<span data-ttu-id="110f8-211">**Reset**</span><span class="sxs-lookup"><span data-stu-id="110f8-211">**Reset**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)
</dt> </dl>

 

 
