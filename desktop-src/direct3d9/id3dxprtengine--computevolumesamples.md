---
description: Выдает проекцию прямого освещения, полученного от предыдущего света, в виде векторов, представляющих собой сферическую гармонию (SH), которые представляют радианце инцидентов в указанных местах.
ms.assetid: ccde7c59-cb82-4d61-822a-e1e9ecea0a28
title: 'Метод ID3DXPRTEngine:: Компутеволумесамплес (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeVolumeSamples
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: bd77fff723f0cf7e3dc2a52be6a40ff6f0d71fe1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703968"
---
# <a name="id3dxprtenginecomputevolumesamples-method"></a><span data-ttu-id="0d4fa-103">Метод ID3DXPRTEngine:: Компутеволумесамплес</span><span class="sxs-lookup"><span data-stu-id="0d4fa-103">ID3DXPRTEngine::ComputeVolumeSamples method</span></span>

<span data-ttu-id="0d4fa-104">Выдает проекцию прямого освещения, полученного от предыдущего света, в виде векторов, представляющих собой сферическую гармонию (SH), которые представляют радианце инцидентов в указанных местах.</span><span class="sxs-lookup"><span data-stu-id="0d4fa-104">Computes a projection of the direct lighting from the previous light bounce into spherical harmonic (SH) basis vectors that represent incident radiance at specified locations.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d4fa-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0d4fa-105">Syntax</span></span>


```C++
HRESULT ComputeVolumeSamples(
  [in]            LPD3DXPRTBUFFER pSurfDataIn,
  [in]            UINT            Order,
  [in]            UINT            NumVolSamples.xml,
  [in]      const D3DXVECTOR3     *pSampleLocs,
  [in, out]       LPD3DXPRTBUFFER pDataOut
);
```



## <a name="parameters"></a><span data-ttu-id="0d4fa-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0d4fa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d4fa-107">*псурфдатаин* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0d4fa-107">*pSurfDataIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d4fa-108">Тип: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="0d4fa-108">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="0d4fa-109">Указатель на входной объект [**ID3DXPRTBuffer**](id3dxprtbuffer.md) , представляющий трехмерный объект из предыдущего освещения.</span><span class="sxs-lookup"><span data-stu-id="0d4fa-109">Pointer to an input [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that represents the 3D object from the previous light bounce.</span></span>

</dd> <dt>

<span data-ttu-id="0d4fa-110">*Порядок следования* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0d4fa-110">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d4fa-111">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0d4fa-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0d4fa-112">Порядок вычисления SH.</span><span class="sxs-lookup"><span data-stu-id="0d4fa-112">Order of the SH evaluation.</span></span> <span data-ttu-id="0d4fa-113">Должен находиться в диапазоне от [D3DXSH \_ МИНОРДЕР](other-d3dx-constants.md) до D3DXSH \_ максордер, включительно.</span><span class="sxs-lookup"><span data-stu-id="0d4fa-113">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="0d4fa-114">При оценке создается коэффициент порядка ².</span><span class="sxs-lookup"><span data-stu-id="0d4fa-114">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="0d4fa-115">Степень оценки — Order-1.</span><span class="sxs-lookup"><span data-stu-id="0d4fa-115">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="0d4fa-116">*NumVolSamples.xml* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0d4fa-116">*NumVolSamples.xml* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d4fa-117">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0d4fa-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0d4fa-118">Число расположений выборки.</span><span class="sxs-lookup"><span data-stu-id="0d4fa-118">Number of sample locations.</span></span>

</dd> <dt>

<span data-ttu-id="0d4fa-119">*псамплелокс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0d4fa-119">*pSampleLocs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d4fa-120">Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="0d4fa-120">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="0d4fa-121">Расположение для каждого образца.</span><span class="sxs-lookup"><span data-stu-id="0d4fa-121">Position for each sample.</span></span> <span data-ttu-id="0d4fa-122">Если Псамплелокс имеет **значение NULL**, компутеволумесамплес вычислит матрицы перемещения на каждой вершине сетки.</span><span class="sxs-lookup"><span data-stu-id="0d4fa-122">If pSampleLocs is **NULL**, ComputeVolumeSamples will compute transfer matrices at every mesh vertex.</span></span> <span data-ttu-id="0d4fa-123">Однако, если Псамплелокс не равен **null**, необходимо выделать выборку через сферу (Set Усесфере = **true** и Усекосине = **false** в [**ID3DXPRTEngine:: сетсамплингинфо**](id3dxprtengine--setsamplinginfo.md)); в противном случае Компутеволумесамплес вернет D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="0d4fa-123">However, if pSampleLocs is not **NULL**, you must sample over a sphere (set UseSphere = **TRUE** and UseCosine = **FALSE** in [**ID3DXPRTEngine::SetSamplingInfo**](id3dxprtengine--setsamplinginfo.md)); otherwise, ComputeVolumeSamples will return D3DERR\_INVALIDCALL.</span></span>

</dd> <dt>

<span data-ttu-id="0d4fa-124">*pData* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="0d4fa-124">*pDataOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="0d4fa-125">Тип: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="0d4fa-125">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="0d4fa-126">Указатель на выходной объект [**ID3DXPRTBuffer**](id3dxprtbuffer.md) , который проецирует прямое освещение от предыдущего света, в векторы на основе SH.</span><span class="sxs-lookup"><span data-stu-id="0d4fa-126">Pointer to an output [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that projects the direct lighting from the previous light bounce into SH basis vectors.</span></span> <span data-ttu-id="0d4fa-127">Этот буфер должен иметь правильное число цветовых каналов, выделенных для имитации.</span><span class="sxs-lookup"><span data-stu-id="0d4fa-127">This buffer must have the proper number of color channels allocated for the simulation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d4fa-128">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0d4fa-128">Return value</span></span>

<span data-ttu-id="0d4fa-129">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0d4fa-129">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0d4fa-130">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="0d4fa-130">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="0d4fa-131">В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="0d4fa-131">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="0d4fa-132">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0d4fa-132">Remarks</span></span>

<span data-ttu-id="0d4fa-133">Этот метод выполняет вычисление того, как освещение от исходной функции радианце отражается на поверхности, представляющей сцену (Псурфдатаин), и приходится на каждую точку в пространстве, указанную Псамплелокс.</span><span class="sxs-lookup"><span data-stu-id="0d4fa-133">This method computes how the light from the source radiance function is reflected off the surface that represents the scene (pSurfDataIn) and arrives at each point in space specified by pSampleLocs.</span></span> <span data-ttu-id="0d4fa-134">Коэффициенты SH представляют сопоставление (в каждой точке Псамплелокс) источника радианце с передачей радианце инцидента.</span><span class="sxs-lookup"><span data-stu-id="0d4fa-134">The SH coefficients represent the mapping, at each pSampleLocs point, of source radiance to transferred incident radiance.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d4fa-135">Требования</span><span class="sxs-lookup"><span data-stu-id="0d4fa-135">Requirements</span></span>



| <span data-ttu-id="0d4fa-136">Требование</span><span class="sxs-lookup"><span data-stu-id="0d4fa-136">Requirement</span></span> | <span data-ttu-id="0d4fa-137">Значение</span><span class="sxs-lookup"><span data-stu-id="0d4fa-137">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0d4fa-138">Header</span><span class="sxs-lookup"><span data-stu-id="0d4fa-138">Header</span></span><br/>  | <dl> <span data-ttu-id="0d4fa-139"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d4fa-139"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="0d4fa-140">Библиотека</span><span class="sxs-lookup"><span data-stu-id="0d4fa-140">Library</span></span><br/> | <dl> <span data-ttu-id="0d4fa-141"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0d4fa-141"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0d4fa-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0d4fa-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d4fa-143">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="0d4fa-143">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> <dt>

[<span data-ttu-id="0d4fa-144">**ID3DXPRTEngine:: Компутеволумесамплесдиректш**</span><span class="sxs-lookup"><span data-stu-id="0d4fa-144">**ID3DXPRTEngine::ComputeVolumeSamplesDirectSH**</span></span>](id3dxprtengine--computevolumesamplesdirectsh.md)
</dt> </dl>

 

 
