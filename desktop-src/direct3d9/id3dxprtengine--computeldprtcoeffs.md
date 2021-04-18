---
description: Выполняет вычисление локально-определяемых предварительно вычисляемых радианценых перенаправлений (ЛДПРТ), относящихся к образцу обычных векторов, чтобы избежать ошибок с наименьшими квадратами по отношению к входным ID3DXPRTBuffer данным.
ms.assetid: 302c20cd-d495-4a23-9692-7456355471eb
title: 'Метод ID3DXPRTEngine:: Компутелдпрткоеффс (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeLDPRTCoeffs
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 351ecb8022e06b1a5a24abad8fa8541798d13ba0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105714030"
---
# <a name="id3dxprtenginecomputeldprtcoeffs-method"></a><span data-ttu-id="a37b5-103">Метод ID3DXPRTEngine:: Компутелдпрткоеффс</span><span class="sxs-lookup"><span data-stu-id="a37b5-103">ID3DXPRTEngine::ComputeLDPRTCoeffs method</span></span>

<span data-ttu-id="a37b5-104">Выполняет вычисление локально-определяемых предварительно вычисляемых радианценых перенаправлений (ЛДПРТ), относящихся к образцу обычных векторов, чтобы избежать ошибок с наименьшими квадратами по отношению к входным [**ID3DXPRTBuffer**](id3dxprtbuffer.md) данным.</span><span class="sxs-lookup"><span data-stu-id="a37b5-104">Computes locally-deformable precomputed radiance transfer (LDPRT) coefficients relative to per-sample normal vectors to minimize the least-squares error with respect to input [**ID3DXPRTBuffer**](id3dxprtbuffer.md) data.</span></span> <span data-ttu-id="a37b5-105">Эти коэффициенты можно использовать с обложками или преобразованными векторами, чтобы моделировать глобальные эффекты для динамических объектов.</span><span class="sxs-lookup"><span data-stu-id="a37b5-105">These coefficients can be used with skinned or transformed normal vectors to model global effects on dynamic objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="a37b5-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a37b5-106">Syntax</span></span>


```C++
HRESULT ComputeLDPRTCoeffs(
  [in]      LPD3DXPRTBUFFER pDataIn,
  [in]      UINT            Order,
  [in, out] D3DXVECTOR3     *pNormOut,
  [in, out] LPD3DXPRTBUFFER pDataOut
);
```



## <a name="parameters"></a><span data-ttu-id="a37b5-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="a37b5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a37b5-108">*pData* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a37b5-108">*pDataIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a37b5-109">Тип: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="a37b5-109">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="a37b5-110">Указатель на входный объект данных радианце (PRT), который является [**ID3DXPRTBufferным**](id3dxprtbuffer.md) (SH).</span><span class="sxs-lookup"><span data-stu-id="a37b5-110">Pointer to an input [**ID3DXPRTBuffer**](id3dxprtbuffer.md) spherical harmonic (SH) precomputed radiance transfer (PRT) data object.</span></span>

</dd> <dt>

<span data-ttu-id="a37b5-111">*Порядок следования* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a37b5-111">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a37b5-112">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a37b5-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a37b5-113">Порядок вычисления SH.</span><span class="sxs-lookup"><span data-stu-id="a37b5-113">Order of the SH evaluation.</span></span> <span data-ttu-id="a37b5-114">Должен находиться в диапазоне от [D3DXSH \_ МИНОРДЕР](other-d3dx-constants.md) до D3DXSH \_ максордер, включительно.</span><span class="sxs-lookup"><span data-stu-id="a37b5-114">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="a37b5-115">При оценке создается коэффициент порядка ².</span><span class="sxs-lookup"><span data-stu-id="a37b5-115">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="a37b5-116">Степень оценки — Order-1.</span><span class="sxs-lookup"><span data-stu-id="a37b5-116">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="a37b5-117">*пнормаут* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="a37b5-117">*pNormOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a37b5-118">Тип: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="a37b5-118">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="a37b5-119">Необязательный Векторный массив, который должен быть заполнен с помощью оптимальных векторов нормали, для которых оптимизированы коэффициенты ЛДПРТ.</span><span class="sxs-lookup"><span data-stu-id="a37b5-119">Optional vector array to be filled with shader-optimal normal vectors for which LDPRT coefficients are optimized.</span></span> <span data-ttu-id="a37b5-120">Этот массив должен иметь тот же размер, что и число выборок в pData.</span><span class="sxs-lookup"><span data-stu-id="a37b5-120">This array must be the same size as the number of samples in pDataIn.</span></span> <span data-ttu-id="a37b5-121">Если **значение равно NULL**, используются векторы нормали Surface.</span><span class="sxs-lookup"><span data-stu-id="a37b5-121">If **NULL**, surface normal vectors are used.</span></span>

</dd> <dt>

<span data-ttu-id="a37b5-122">*pData* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="a37b5-122">*pDataOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a37b5-123">Тип: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="a37b5-123">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="a37b5-124">Указатель на выходной объект [**ID3DXPRTBuffer**](id3dxprtbuffer.md) , содержащий количество коэффициентов гармониой зональныеа для каждого цветового канала на выборку.</span><span class="sxs-lookup"><span data-stu-id="a37b5-124">Pointer to an output [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that contains Order zonal harmonic coefficients per color channel per sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a37b5-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a37b5-125">Return value</span></span>

<span data-ttu-id="a37b5-126">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a37b5-126">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a37b5-127">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="a37b5-127">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="a37b5-128">В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="a37b5-128">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="a37b5-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a37b5-129">Remarks</span></span>

<span data-ttu-id="a37b5-130">При необходимости можно получить решения для заливки обычных векторов с помощью этого метода.</span><span class="sxs-lookup"><span data-stu-id="a37b5-130">Solutions for shading normal vectors can optionally be obtained with this method.</span></span> <span data-ttu-id="a37b5-131">Эти обычные векторы, вместе с коэффициентами ЛДПРТ, могут точнее представлять сигнал PRT.</span><span class="sxs-lookup"><span data-stu-id="a37b5-131">These normal vectors, along with the LDPRT coefficients, can more accurately represent the PRT signal.</span></span> <span data-ttu-id="a37b5-132">В этом случае коэффициенты представляют гармонические зональные, ориентированные на нормальное направление.</span><span class="sxs-lookup"><span data-stu-id="a37b5-132">In this case, the coefficients represent zonal harmonics oriented in the normal direction.</span></span>

<span data-ttu-id="a37b5-133">Этот метод не может использоваться с результатами из [**ID3DXPRTEngine:: компутесурфсамплесбаунце**](id3dxprtengine--computesurfsamplesbounce.md) или [**ID3DXPRTEngine:: компутесурфсамплесдиректш**](id3dxprtengine--computesurfsamplesdirectsh.md).</span><span class="sxs-lookup"><span data-stu-id="a37b5-133">This method cannot be used with results from [**ID3DXPRTEngine::ComputeSurfSamplesBounce**](id3dxprtengine--computesurfsamplesbounce.md) or [**ID3DXPRTEngine::ComputeSurfSamplesDirectSH**](id3dxprtengine--computesurfsamplesdirectsh.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a37b5-134">Требования</span><span class="sxs-lookup"><span data-stu-id="a37b5-134">Requirements</span></span>



| <span data-ttu-id="a37b5-135">Требование</span><span class="sxs-lookup"><span data-stu-id="a37b5-135">Requirement</span></span> | <span data-ttu-id="a37b5-136">Значение</span><span class="sxs-lookup"><span data-stu-id="a37b5-136">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a37b5-137">Header</span><span class="sxs-lookup"><span data-stu-id="a37b5-137">Header</span></span><br/>  | <dl> <span data-ttu-id="a37b5-138"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="a37b5-138"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="a37b5-139">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a37b5-139">Library</span></span><br/> | <dl> <span data-ttu-id="a37b5-140"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a37b5-140"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a37b5-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a37b5-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a37b5-142">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="a37b5-142">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> </dl>

 

 
