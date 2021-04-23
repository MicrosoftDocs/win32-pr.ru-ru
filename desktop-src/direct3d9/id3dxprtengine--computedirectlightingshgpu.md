---
description: Использует графический процессор для расчета вклада прямого освещения в трехмерные объекты, в которых исходный радианце представлен аппроксимацией по негармоническому излучению (SH). Вычисление освещения в GPU обычно выполняется гораздо быстрее, чем в ЦП.
ms.assetid: ccea5a5e-23f1-4fdf-bce8-9bfc35d45257
title: 'Метод ID3DXPRTEngine:: Компутедиректлигхтингшгпу (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeDirectLightingSHGPU
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e56dd807d28ba6952cd20c971b675b83687a3015
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105674759"
---
# <a name="id3dxprtenginecomputedirectlightingshgpu-method"></a><span data-ttu-id="5f00d-104">Метод ID3DXPRTEngine:: Компутедиректлигхтингшгпу</span><span class="sxs-lookup"><span data-stu-id="5f00d-104">ID3DXPRTEngine::ComputeDirectLightingSHGPU method</span></span>

<span data-ttu-id="5f00d-105">Использует графический процессор для расчета вклада прямого освещения в трехмерные объекты, в которых исходный радианце представлен аппроксимацией по негармоническому излучению (SH).</span><span class="sxs-lookup"><span data-stu-id="5f00d-105">Uses the GPU to compute the direct lighting contribution to 3D objects where the source radiance is represented by a spherical harmonic (SH) approximation.</span></span> <span data-ttu-id="5f00d-106">Вычисление освещения в GPU обычно выполняется гораздо быстрее, чем в ЦП.</span><span class="sxs-lookup"><span data-stu-id="5f00d-106">Computing the lighting on the GPU will generally be much faster than on the CPU.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f00d-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5f00d-107">Syntax</span></span>


```C++
HRESULT ComputeDirectLightingSHGPU(
  [in]      LPDIRECT3DDEVICE9 pDevice,
  [in]      UINT              Flags,
  [in]      UINT              Order,
  [in]      FLOAT             ZBias,
  [in]      FLOAT             ZAngleBias,
  [in, out] LPD3DXPRTBUFFER   pDataOut
);
```



## <a name="parameters"></a><span data-ttu-id="5f00d-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="5f00d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f00d-109">*пдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5f00d-109">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f00d-110">Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="5f00d-110">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="5f00d-111">Указатель на объект устройства [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , используемый для моделирования GPU.</span><span class="sxs-lookup"><span data-stu-id="5f00d-111">Pointer to the [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) device object used to run the simulation on the GPU.</span></span> <span data-ttu-id="5f00d-112">Устройство должно поддерживать шейдеры [PS \_ 2 \_ 0](../direct3dhlsl/dx9-graphics-reference-asm-ps-2-0.md) пикселей.</span><span class="sxs-lookup"><span data-stu-id="5f00d-112">The device must support [ps\_2\_0](../direct3dhlsl/dx9-graphics-reference-asm-ps-2-0.md) pixel shaders.</span></span>

> [!Note]  
> <span data-ttu-id="5f00d-113">Функции обратного вызова не должны использовать объект устройства [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , используемый симулятором GPU.</span><span class="sxs-lookup"><span data-stu-id="5f00d-113">Callback functions should not use the [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) device object used by the GPU simulator.</span></span>

 

</dd> <dt>

<span data-ttu-id="5f00d-114">*Флаги* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5f00d-114">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f00d-115">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5f00d-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5f00d-116">Параметр моделирования GPU, определяющий разрешение теневого z-буфера.</span><span class="sxs-lookup"><span data-stu-id="5f00d-116">GPU simulation parameter that defines the resolution of the shadow z-buffer.</span></span> <span data-ttu-id="5f00d-117">Необходимо задать одно из значений констант из [**D3DXSHGPUSIMOPT**](./d3dxshgpusimopt.md).</span><span class="sxs-lookup"><span data-stu-id="5f00d-117">Should be set to one of the constant values from [**D3DXSHGPUSIMOPT**](./d3dxshgpusimopt.md).</span></span> <span data-ttu-id="5f00d-118">Чтобы задать модель с более высокой точностью, \_ значение D3DXSHGPUSIMOPT хигхкуалити может быть объединено с одним из \_ значений D3DXSHGPUSIMOPT шадоврескскскс.</span><span class="sxs-lookup"><span data-stu-id="5f00d-118">To specifiy higher precision simulation, the D3DXSHGPUSIMOPT\_HIGHQUALITY value may be combined with one of the D3DXSHGPUSIMOPT\_SHADOWRESxxx values.</span></span>

</dd> <dt>

<span data-ttu-id="5f00d-119">*Порядок следования* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5f00d-119">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f00d-120">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5f00d-120">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5f00d-121">Порядок вычисления SH.</span><span class="sxs-lookup"><span data-stu-id="5f00d-121">Order of the SH evaluation.</span></span> <span data-ttu-id="5f00d-122">Должен находиться в диапазоне от [D3DXSH \_ МИНОРДЕР](other-d3dx-constants.md) до D3DXSH \_ максордер, включительно.</span><span class="sxs-lookup"><span data-stu-id="5f00d-122">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="5f00d-123">При оценке создается коэффициент порядка ².</span><span class="sxs-lookup"><span data-stu-id="5f00d-123">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="5f00d-124">Степень оценки — Order-1.</span><span class="sxs-lookup"><span data-stu-id="5f00d-124">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="5f00d-125">*Збиас* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5f00d-125">*ZBias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f00d-126">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5f00d-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5f00d-127">Смещение в нормальном направлении.</span><span class="sxs-lookup"><span data-stu-id="5f00d-127">Bias in the normal direction.</span></span>

</dd> <dt>

<span data-ttu-id="5f00d-128">*Занглебиас* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5f00d-128">*ZAngleBias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f00d-129">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5f00d-129">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5f00d-130">Сдвиг в нормальном направлении с масштабированием на один минус косинус угла с голубым лучом.</span><span class="sxs-lookup"><span data-stu-id="5f00d-130">Bias in the normal direction, scaled by one minus the cosine of the angle with the light ray.</span></span>

</dd> <dt>

<span data-ttu-id="5f00d-131">*pData* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="5f00d-131">*pDataOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="5f00d-132">Тип: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="5f00d-132">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="5f00d-133">Указатель на объект [**ID3DXPRTBuffer**](id3dxprtbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="5f00d-133">Pointer to an [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object.</span></span> <span data-ttu-id="5f00d-134">Этот буфер должен иметь правильное число цветовых каналов, выделенных для имитации.</span><span class="sxs-lookup"><span data-stu-id="5f00d-134">This buffer must have the proper number of color channels allocated for the simulation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f00d-135">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5f00d-135">Return value</span></span>

<span data-ttu-id="5f00d-136">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5f00d-136">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5f00d-137">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="5f00d-137">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="5f00d-138">В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="5f00d-138">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f00d-139">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5f00d-139">Remarks</span></span>

<span data-ttu-id="5f00d-140">В этом методе албедо не умножается на сигнал освещения, и в симуляторе встроена только входящая лампочка.</span><span class="sxs-lookup"><span data-stu-id="5f00d-140">In this method, the albedo is not multiplied by the light signal, and only incoming light is integrated in the simulator.</span></span> <span data-ttu-id="5f00d-141">Не умножая албедо, вы можете моделировать албедо вариации на более точном масштабе, чем исходный радианце, тем самым обеспечивая более точные результаты сжатия.</span><span class="sxs-lookup"><span data-stu-id="5f00d-141">By not multiplying the albedo, you can model albedo variation at a finer scale than the source radiance, thereby yielding more accurate results from compression.</span></span>

<span data-ttu-id="5f00d-142">Вызовите [**мултиплялбедо**](id3dxprtengine--multiplyalbedo.md) , чтобы умножить каждый предварительно вычисленный вектор перемещения РАДИАНЦЕ (PRT) на албедо.</span><span class="sxs-lookup"><span data-stu-id="5f00d-142">Call [**MultiplyAlbedo**](id3dxprtengine--multiplyalbedo.md) to multiply each precomputed radiance transfer (PRT) vector by the albedo.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f00d-143">Требования</span><span class="sxs-lookup"><span data-stu-id="5f00d-143">Requirements</span></span>



| <span data-ttu-id="5f00d-144">Требование</span><span class="sxs-lookup"><span data-stu-id="5f00d-144">Requirement</span></span> | <span data-ttu-id="5f00d-145">Значение</span><span class="sxs-lookup"><span data-stu-id="5f00d-145">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5f00d-146">Header</span><span class="sxs-lookup"><span data-stu-id="5f00d-146">Header</span></span><br/>  | <dl> <span data-ttu-id="5f00d-147"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="5f00d-147"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="5f00d-148">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5f00d-148">Library</span></span><br/> | <dl> <span data-ttu-id="5f00d-149"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5f00d-149"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5f00d-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5f00d-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f00d-151">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="5f00d-151">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> </dl>

 

 
