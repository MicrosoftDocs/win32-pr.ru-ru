---
description: Вычисление вклада прямого освещения в трехмерные объекты, в которых источник радианце представлен аппроксимацией (SH) с использованием адаптивной выборки.
ms.assetid: 792d8460-d608-4384-ac1c-556435074580
title: 'Метод ID3DXPRTEngine:: Компутедиректлигхтингшадаптиве (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeDirectLightingSHAdaptive
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8abbcfd955fa909166b53f6e050b9aff5837508d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821524"
---
# <a name="id3dxprtenginecomputedirectlightingshadaptive-method"></a><span data-ttu-id="c49a9-103">Метод ID3DXPRTEngine:: Компутедиректлигхтингшадаптиве</span><span class="sxs-lookup"><span data-stu-id="c49a9-103">ID3DXPRTEngine::ComputeDirectLightingSHAdaptive method</span></span>

<span data-ttu-id="c49a9-104">Вычисление вклада прямого освещения в трехмерные объекты, в которых источник радианце представлен аппроксимацией (SH) с использованием адаптивной выборки.</span><span class="sxs-lookup"><span data-stu-id="c49a9-104">Computes the direct lighting contribution to 3D objects where the source radiance is represented by a spherical harmonic (SH) approximation, using adaptive sampling.</span></span> <span data-ttu-id="c49a9-105">Этот метод создает новые вершины и грани в сети для более точного приближения к предварительно вычисленному сигналу передачи радианце (PRT).</span><span class="sxs-lookup"><span data-stu-id="c49a9-105">This method generates new vertices and faces on the mesh to more accurately approximate the precomputed radiance transfer (PRT) signal.</span></span>

## <a name="syntax"></a><span data-ttu-id="c49a9-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c49a9-106">Syntax</span></span>


```C++
HRESULT ComputeDirectLightingSHAdaptive(
  [in]      UINT            Order,
  [in]      FLOAT           AdaptiveThresh,
  [in]      FLOAT           MinEdgeLength,
  [in]      UINT            MaxSubdiv,
  [in, out] LPD3DXPRTBUFFER pDataOut
);
```



## <a name="parameters"></a><span data-ttu-id="c49a9-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="c49a9-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c49a9-108">*Порядок следования* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c49a9-108">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c49a9-109">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c49a9-109">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c49a9-110">Порядок вычисления SH.</span><span class="sxs-lookup"><span data-stu-id="c49a9-110">Order of the SH evaluation.</span></span> <span data-ttu-id="c49a9-111">Должен находиться в диапазоне от [D3DXSH \_ МИНОРДЕР](other-d3dx-constants.md) до D3DXSH \_ максордер, включительно.</span><span class="sxs-lookup"><span data-stu-id="c49a9-111">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="c49a9-112">При оценке создается коэффициент порядка ².</span><span class="sxs-lookup"><span data-stu-id="c49a9-112">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="c49a9-113">Степень оценки — Order-1.</span><span class="sxs-lookup"><span data-stu-id="c49a9-113">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="c49a9-114">*Адаптивесреш* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c49a9-114">*AdaptiveThresh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c49a9-115">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c49a9-115">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c49a9-116">Пороговое значение для вектора PRT, используемого для подразделения вершин сетки и граней.</span><span class="sxs-lookup"><span data-stu-id="c49a9-116">Threshold on the PRT vector to use for subdividing mesh vertices and faces.</span></span> <span data-ttu-id="c49a9-117">Если значение параметра меньше 1E-6F, то указывается по умолчанию параметр 1E-6f.</span><span class="sxs-lookup"><span data-stu-id="c49a9-117">If less than 1e-6f, a default value of 1e-6f is specified.</span></span>

</dd> <dt>

<span data-ttu-id="c49a9-118">*Минеджеленгс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c49a9-118">*MinEdgeLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c49a9-119">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c49a9-119">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c49a9-120">Минимальная длина грани, которая будет создана при адаптивной выборки.</span><span class="sxs-lookup"><span data-stu-id="c49a9-120">Minimum face edge length that will be generated in adaptive sampling.</span></span> <span data-ttu-id="c49a9-121">Если метод определяет, что значение слишком мало, задается зависящее от модели значение.</span><span class="sxs-lookup"><span data-stu-id="c49a9-121">If the method determines that the value is too small, a model-dependent value is specified.</span></span> <span data-ttu-id="c49a9-122">При нулевом значении указывается значение по умолчанию 4.</span><span class="sxs-lookup"><span data-stu-id="c49a9-122">If zero, a default value of 4 is specified.</span></span>

</dd> <dt>

<span data-ttu-id="c49a9-123">*Макссубдив* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c49a9-123">*MaxSubdiv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c49a9-124">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c49a9-124">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c49a9-125">Максимальный уровень подраздела лица, который будет использоваться в адаптивной выборки.</span><span class="sxs-lookup"><span data-stu-id="c49a9-125">Maximum level of subdivision of a face that will be used in adaptive sampling.</span></span>

</dd> <dt>

<span data-ttu-id="c49a9-126">*pData* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="c49a9-126">*pDataOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c49a9-127">Тип: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="c49a9-127">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="c49a9-128">Указатель на выходной объект [**ID3DXPRTBuffer**](id3dxprtbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="c49a9-128">Pointer to an output [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object.</span></span> <span data-ttu-id="c49a9-129">Этот буфер должен иметь правильное число цветовых каналов, выделенных для имитации.</span><span class="sxs-lookup"><span data-stu-id="c49a9-129">This buffer must have the proper number of color channels allocated for the simulation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c49a9-130">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c49a9-130">Return value</span></span>

<span data-ttu-id="c49a9-131">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c49a9-131">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c49a9-132">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="c49a9-132">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="c49a9-133">В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="c49a9-133">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="c49a9-134">Требования</span><span class="sxs-lookup"><span data-stu-id="c49a9-134">Requirements</span></span>



| <span data-ttu-id="c49a9-135">Требование</span><span class="sxs-lookup"><span data-stu-id="c49a9-135">Requirement</span></span> | <span data-ttu-id="c49a9-136">Значение</span><span class="sxs-lookup"><span data-stu-id="c49a9-136">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c49a9-137">Header</span><span class="sxs-lookup"><span data-stu-id="c49a9-137">Header</span></span><br/>  | <dl> <span data-ttu-id="c49a9-138"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="c49a9-138"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="c49a9-139">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c49a9-139">Library</span></span><br/> | <dl> <span data-ttu-id="c49a9-140"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c49a9-140"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c49a9-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c49a9-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c49a9-142">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="c49a9-142">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> <dt>

[<span data-ttu-id="c49a9-143">**ID3DXPRTEngine:: Робустмешрефине**</span><span class="sxs-lookup"><span data-stu-id="c49a9-143">**ID3DXPRTEngine::RobustMeshRefine**</span></span>](id3dxprtengine--robustmeshrefine.md)
</dt> </dl>

 

 
