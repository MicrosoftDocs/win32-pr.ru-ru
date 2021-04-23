---
description: 'Вычисление вектора перемещения, который сопоставляет источник радианце для выхода из радианце, полученного из рассеивания подповерхности, использование адаптивных свойств выборки и материала, заданных ID3DXPRTEngine:: Сетмешматериалс.'
ms.assetid: 34e42271-703b-4b67-8153-2eca3f8dde92
title: 'Метод ID3DXPRTEngine:: Компутессадаптиве (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeSSAdaptive
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 198a597020a0bfcbc789cc741e42048bd89eb95f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105714029"
---
# <a name="id3dxprtenginecomputessadaptive-method"></a><span data-ttu-id="9939a-103">Метод ID3DXPRTEngine:: Компутессадаптиве</span><span class="sxs-lookup"><span data-stu-id="9939a-103">ID3DXPRTEngine::ComputeSSAdaptive method</span></span>

<span data-ttu-id="9939a-104">Вычисление вектора перемещения, который сопоставляет источник радианце для выхода из радианце, полученного из рассеивания подповерхности, использование адаптивных свойств выборки и материала, заданных [**ID3DXPRTEngine:: сетмешматериалс**](id3dxprtengine--setmeshmaterials.md).</span><span class="sxs-lookup"><span data-stu-id="9939a-104">Computes a transfer vector that maps source radiance to exit radiance resulting from subsurface scattering, using adaptive sampling and material properties set by [**ID3DXPRTEngine::SetMeshMaterials**](id3dxprtengine--setmeshmaterials.md).</span></span> <span data-ttu-id="9939a-105">Метод создает новые вершины и грани в сети для более точного приближения к предварительно вычисленному сигналу передачи радианце (PRT).</span><span class="sxs-lookup"><span data-stu-id="9939a-105">The method generates new vertices and faces on the mesh to more accurately approximate the precomputed radiance transfer (PRT) signal.</span></span> <span data-ttu-id="9939a-106">Этот метод можно использовать только для материалов, определенных для вершины в объекте сетки.</span><span class="sxs-lookup"><span data-stu-id="9939a-106">This method can be used only for materials defined per-vertex in a mesh object.</span></span>

## <a name="syntax"></a><span data-ttu-id="9939a-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9939a-107">Syntax</span></span>


```C++
HRESULT ComputeSSAdaptive(
  [in]      LPD3DXPRTBUFFER pDataIn,
  [in]      FLOAT           AdaptiveThresh,
  [in]      FLOAT           MinEdgeLength,
  [in]      UINT            MaxSubdiv,
  [in, out] LPD3DXPRTBUFFER pDataOut,
  [in, out] LPD3DXPRTBUFFER pDataTotal
);
```



## <a name="parameters"></a><span data-ttu-id="9939a-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="9939a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9939a-109">*pData* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9939a-109">*pDataIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9939a-110">Тип: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="9939a-110">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="9939a-111">Указатель на входной объект [**ID3DXPRTBuffer**](id3dxprtbuffer.md) , представляющий трехмерный объект из предыдущего освещения.</span><span class="sxs-lookup"><span data-stu-id="9939a-111">Pointer to an input [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that represents the 3D object from the previous light bounce.</span></span> <span data-ttu-id="9939a-112">Этот входной буфер должен иметь правильное число цветовых каналов, выделенных для моделирования.</span><span class="sxs-lookup"><span data-stu-id="9939a-112">This input buffer must have the proper number of color channels allocated for the simulation.</span></span>

</dd> <dt>

<span data-ttu-id="9939a-113">*Адаптивесреш* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9939a-113">*AdaptiveThresh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9939a-114">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9939a-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9939a-115">Пороговое значение для вектора PRT, используемого для подразделения вершин сетки и граней.</span><span class="sxs-lookup"><span data-stu-id="9939a-115">Threshold on the PRT vector to use for subdividing mesh vertices and faces.</span></span> <span data-ttu-id="9939a-116">Если значение параметра меньше 1E-6F, то указывается по умолчанию параметр 1E-6f.</span><span class="sxs-lookup"><span data-stu-id="9939a-116">If less than 1e-6f, a default value of 1e-6f is specified.</span></span>

</dd> <dt>

<span data-ttu-id="9939a-117">*Минеджеленгс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9939a-117">*MinEdgeLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9939a-118">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9939a-118">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9939a-119">Минимальная длина грани, которая будет создана при адаптивной выборки.</span><span class="sxs-lookup"><span data-stu-id="9939a-119">Minimum face edge length that will be generated in adaptive sampling.</span></span> <span data-ttu-id="9939a-120">Если метод определяет, что значение слишком мало, задается зависящее от модели значение.</span><span class="sxs-lookup"><span data-stu-id="9939a-120">If the method determines that the value is too small, a model-dependent value is specified.</span></span>

</dd> <dt>

<span data-ttu-id="9939a-121">*Макссубдив* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9939a-121">*MaxSubdiv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9939a-122">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9939a-122">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9939a-123">Максимальный уровень подраздела лица, который будет использоваться в адаптивной выборки.</span><span class="sxs-lookup"><span data-stu-id="9939a-123">Maximum level of subdivision of a face that will be used in adaptive sampling.</span></span> <span data-ttu-id="9939a-124">При нулевом значении указывается значение по умолчанию 4.</span><span class="sxs-lookup"><span data-stu-id="9939a-124">If zero, a default value of 4 is specified.</span></span>

</dd> <dt>

<span data-ttu-id="9939a-125">*pData* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="9939a-125">*pDataOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="9939a-126">Тип: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="9939a-126">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="9939a-127">Указатель на выходной объект [**ID3DXPRTBuffer**](id3dxprtbuffer.md) , моделирующий один элемент отскока точечной светлой поверхности.</span><span class="sxs-lookup"><span data-stu-id="9939a-127">Pointer to an output [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that models a single bounce of the subsurface-scattered light.</span></span> <span data-ttu-id="9939a-128">Этот выходной буфер должен иметь правильное число цветовых каналов, выделенных для моделирования.</span><span class="sxs-lookup"><span data-stu-id="9939a-128">This output buffer must have the proper number of color channels allocated for the simulation.</span></span>

</dd> <dt>

<span data-ttu-id="9939a-129">*пдататотал* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="9939a-129">*pDataTotal* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="9939a-130">Тип: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="9939a-130">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="9939a-131">Указатель на необязательный объект [**ID3DXPRTBuffer**](id3dxprtbuffer.md) , который является выполняющейся суммой всех предыдущих выходов pData.</span><span class="sxs-lookup"><span data-stu-id="9939a-131">Pointer to an optional [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that is the running sum of all previous pDataOut outputs.</span></span> <span data-ttu-id="9939a-132">Может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="9939a-132">May be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9939a-133">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9939a-133">Return value</span></span>

<span data-ttu-id="9939a-134">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9939a-134">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9939a-135">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="9939a-135">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="9939a-136">В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="9939a-136">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="9939a-137">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9939a-137">Remarks</span></span>

<span data-ttu-id="9939a-138">Чтобы смоделировать подложку, вызывайте этот метод для каждого освещения после вызова метода [**ID3DXPRTEngine:: компутедиректлигхтингшадаптиве**](id3dxprtengine--computedirectlightingshadaptive.md) .</span><span class="sxs-lookup"><span data-stu-id="9939a-138">To model subsurface scattering, call this method for each light bounce after an [**ID3DXPRTEngine::ComputeDirectLightingSHAdaptive**](id3dxprtengine--computedirectlightingshadaptive.md) method is called.</span></span>

<span data-ttu-id="9939a-139">Выходные данные этого метода не включают албедо, и в симуляторе встроена только входящая лампочка.</span><span class="sxs-lookup"><span data-stu-id="9939a-139">The output of this method does not include albedo, and only incoming light is integrated in the simulator.</span></span> <span data-ttu-id="9939a-140">Не умножая албедо, вы можете моделировать албедо вариации на более точном масштабе, чем исходный радианце, тем самым обеспечивая более точные результаты сжатия.</span><span class="sxs-lookup"><span data-stu-id="9939a-140">By not multiplying the albedo, you can model albedo variation at a finer scale than the source radiance, thereby yielding more accurate results from compression.</span></span>

<span data-ttu-id="9939a-141">Вызовите метод [**ID3DXPRTEngine:: мултиплялбедо**](id3dxprtengine--multiplyalbedo.md) , чтобы умножить каждый вектор PRT на албедо.</span><span class="sxs-lookup"><span data-stu-id="9939a-141">Call [**ID3DXPRTEngine::MultiplyAlbedo**](id3dxprtengine--multiplyalbedo.md) to multiply each PRT vector by the albedo.</span></span>

## <a name="requirements"></a><span data-ttu-id="9939a-142">Требования</span><span class="sxs-lookup"><span data-stu-id="9939a-142">Requirements</span></span>



| <span data-ttu-id="9939a-143">Требование</span><span class="sxs-lookup"><span data-stu-id="9939a-143">Requirement</span></span> | <span data-ttu-id="9939a-144">Значение</span><span class="sxs-lookup"><span data-stu-id="9939a-144">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9939a-145">Header</span><span class="sxs-lookup"><span data-stu-id="9939a-145">Header</span></span><br/>  | <dl> <span data-ttu-id="9939a-146"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="9939a-146"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="9939a-147">Библиотека</span><span class="sxs-lookup"><span data-stu-id="9939a-147">Library</span></span><br/> | <dl> <span data-ttu-id="9939a-148"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9939a-148"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9939a-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9939a-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9939a-150">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="9939a-150">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> <dt>

[<span data-ttu-id="9939a-151">**ID3DXPRTEngine:: Компутебаунце**</span><span class="sxs-lookup"><span data-stu-id="9939a-151">**ID3DXPRTEngine::ComputeBounce**</span></span>](id3dxprtengine--computebounce.md)
</dt> <dt>

[<span data-ttu-id="9939a-152">**ID3DXPRTEngine:: COMPUTE**</span><span class="sxs-lookup"><span data-stu-id="9939a-152">**ID3DXPRTEngine::ComputeSS**</span></span>](id3dxprtengine--computess.md)
</dt> </dl>

 

 
