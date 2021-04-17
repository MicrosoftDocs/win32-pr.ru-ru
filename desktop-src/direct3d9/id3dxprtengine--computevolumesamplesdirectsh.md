---
description: Выполняет проекцию неудаленного освещения на основе географических (SH) векторов, представляющих радианце инцидентов в указанных местах.
ms.assetid: 4d07b288-aec1-48eb-8d27-f3d7d8cfb69e
title: 'Метод ID3DXPRTEngine:: Компутеволумесамплесдиректш (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeVolumeSamplesDirectSH
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 757e227907eab73848f43b2b8e2f40f9b4b1071b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703967"
---
# <a name="id3dxprtenginecomputevolumesamplesdirectsh-method"></a><span data-ttu-id="48b92-103">Метод ID3DXPRTEngine:: Компутеволумесамплесдиректш</span><span class="sxs-lookup"><span data-stu-id="48b92-103">ID3DXPRTEngine::ComputeVolumeSamplesDirectSH method</span></span>

<span data-ttu-id="48b92-104">Выполняет проекцию неудаленного освещения на основе географических (SH) векторов, представляющих радианце инцидентов в указанных местах.</span><span class="sxs-lookup"><span data-stu-id="48b92-104">Computes a projection of distant lighting into spherical harmonic (SH) basis vectors that represent incident radiance at specified locations.</span></span>

## <a name="syntax"></a><span data-ttu-id="48b92-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="48b92-105">Syntax</span></span>


```C++
HRESULT ComputeVolumeSamplesDirectSH(
  [in]            UINT            OrderIn,
  [in]            UINT            OrderOut,
  [in]            UINT            NumVolSamples.xml,
  [in]      const D3DXVECTOR3     *pSampleLocs,
  [in, out]       LPD3DXPRTBUFFER pDataOut
);
```



## <a name="parameters"></a><span data-ttu-id="48b92-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="48b92-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48b92-107">*Порядок* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="48b92-107">*OrderIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48b92-108">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="48b92-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="48b92-109">Порядок представления SH с удаленным освещением.</span><span class="sxs-lookup"><span data-stu-id="48b92-109">Order of the SH representation of distant lighting.</span></span> <span data-ttu-id="48b92-110">Должен находиться в диапазоне от [D3DXSH \_ МИНОРДЕР](other-d3dx-constants.md) до D3DXSH \_ максордер, включительно.</span><span class="sxs-lookup"><span data-stu-id="48b92-110">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="48b92-111">Степень оценки — Ordering-1.</span><span class="sxs-lookup"><span data-stu-id="48b92-111">The degree of the evaluation is OrderIn - 1.</span></span>

</dd> <dt>

<span data-ttu-id="48b92-112">*Заказ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="48b92-112">*OrderOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48b92-113">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="48b92-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="48b92-114">Порядок представления SH для локального освещения.</span><span class="sxs-lookup"><span data-stu-id="48b92-114">Order of the SH representation of local lighting.</span></span> <span data-ttu-id="48b92-115">Должен находиться в диапазоне от [D3DXSH \_ МИНОРДЕР](other-d3dx-constants.md) до D3DXSH \_ максордер, включительно.</span><span class="sxs-lookup"><span data-stu-id="48b92-115">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="48b92-116">Степень оценки — Ordering-1.</span><span class="sxs-lookup"><span data-stu-id="48b92-116">The degree of the evaluation is OrderOut - 1.</span></span>

</dd> <dt>

<span data-ttu-id="48b92-117">*NumVolSamples.xml* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="48b92-117">*NumVolSamples.xml* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48b92-118">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="48b92-118">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="48b92-119">Число расположений выборки.</span><span class="sxs-lookup"><span data-stu-id="48b92-119">Number of sample locations.</span></span>

</dd> <dt>

<span data-ttu-id="48b92-120">*псамплелокс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="48b92-120">*pSampleLocs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48b92-121">Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="48b92-121">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="48b92-122">Расположение для каждого образца.</span><span class="sxs-lookup"><span data-stu-id="48b92-122">Position for each sample.</span></span>

</dd> <dt>

<span data-ttu-id="48b92-123">*pData* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="48b92-123">*pDataOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="48b92-124">Тип: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="48b92-124">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="48b92-125">Указатель на выходной объект [**ID3DXPRTBuffer**](id3dxprtbuffer.md) , который проецирует удаленное освещение в векторы экземпляра sh.</span><span class="sxs-lookup"><span data-stu-id="48b92-125">Pointer to an output [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that projects the distant lighting into SH basis vectors.</span></span> <span data-ttu-id="48b92-126">Этот буфер должен иметь правильное число цветовых каналов, выделенных для имитации.</span><span class="sxs-lookup"><span data-stu-id="48b92-126">This buffer must have the proper number of color channels allocated for the simulation.</span></span> <span data-ttu-id="48b92-127">Этот метод создает упорядочение с сортировкой \* по убыванию на канал в каждом месте выборки.</span><span class="sxs-lookup"><span data-stu-id="48b92-127">This method generates OrderIn² \* OrderOut"² scalars per channel at each sample location.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48b92-128">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="48b92-128">Return value</span></span>

<span data-ttu-id="48b92-129">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="48b92-129">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="48b92-130">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="48b92-130">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="48b92-131">В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="48b92-131">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="48b92-132">Комментарии</span><span class="sxs-lookup"><span data-stu-id="48b92-132">Remarks</span></span>

<span data-ttu-id="48b92-133">Этот метод выполняет вычисление того, как освещение от внешнего источника достигает каждой точки в пространстве, заданном параметром Псамплелокс.</span><span class="sxs-lookup"><span data-stu-id="48b92-133">This method computes how light from a distant source arrives at each point in space specified by pSampleLocs.</span></span> <span data-ttu-id="48b92-134">Коэффициенты SH представляют сопоставление (в каждой точке Псамплелокс) источника радианце с передачей радианце инцидента.</span><span class="sxs-lookup"><span data-stu-id="48b92-134">The SH coefficients represent the mapping, at each pSampleLocs point, of source radiance to transferred incident radiance.</span></span>

<span data-ttu-id="48b92-135">Чтобы успешно использовать этот метод, необходимо задать выборку для сферы с Усесфере = **true** и Усекосине = **false** в [**ID3DXPRTEngine:: сетсамплингинфо**](id3dxprtengine--setsamplinginfo.md); в противном случае этот метод возвратит ошибку с D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="48b92-135">To use this method successfully, you must set sampling over a sphere with UseSphere = **TRUE** and UseCosine = **FALSE** in [**ID3DXPRTEngine::SetSamplingInfo**](id3dxprtengine--setsamplinginfo.md); otherwise, this method will return an error with D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="48b92-136">Требования</span><span class="sxs-lookup"><span data-stu-id="48b92-136">Requirements</span></span>



| <span data-ttu-id="48b92-137">Требование</span><span class="sxs-lookup"><span data-stu-id="48b92-137">Requirement</span></span> | <span data-ttu-id="48b92-138">Значение</span><span class="sxs-lookup"><span data-stu-id="48b92-138">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="48b92-139">Header</span><span class="sxs-lookup"><span data-stu-id="48b92-139">Header</span></span><br/>  | <dl> <span data-ttu-id="48b92-140"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="48b92-140"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="48b92-141">Библиотека</span><span class="sxs-lookup"><span data-stu-id="48b92-141">Library</span></span><br/> | <dl> <span data-ttu-id="48b92-142"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="48b92-142"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="48b92-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="48b92-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48b92-144">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="48b92-144">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> <dt>

[<span data-ttu-id="48b92-145">**ID3DXPRTEngine:: Компутеволумесамплес**</span><span class="sxs-lookup"><span data-stu-id="48b92-145">**ID3DXPRTEngine::ComputeVolumeSamples**</span></span>](id3dxprtengine--computevolumesamples.md)
</dt> </dl>

 

 
