---
description: Вычисление вклада прямого освещения в трехмерные объекты, в которых источник радианце представляется приблизительно в виде аппроксимации (SH).
ms.assetid: 52d614cc-578a-4f2b-ba91-70d0c4371042
title: 'Метод ID3DXPRTEngine:: Компутедиректлигхтингш (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeDirectLightingSH
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 01b6c3cff082c40c4df5d9bee1d997599a41965b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105704019"
---
# <a name="id3dxprtenginecomputedirectlightingsh-method"></a><span data-ttu-id="72855-103">Метод ID3DXPRTEngine:: Компутедиректлигхтингш</span><span class="sxs-lookup"><span data-stu-id="72855-103">ID3DXPRTEngine::ComputeDirectLightingSH method</span></span>

<span data-ttu-id="72855-104">Вычисление вклада прямого освещения в трехмерные объекты, в которых источник радианце представляется приблизительно в виде аппроксимации (SH).</span><span class="sxs-lookup"><span data-stu-id="72855-104">Computes the direct lighting contribution to 3D objects where the source radiance is represented by a spherical harmonic (SH) approximation.</span></span>

## <a name="syntax"></a><span data-ttu-id="72855-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="72855-105">Syntax</span></span>


```C++
HRESULT ComputeDirectLightingSH(
  [in]      UINT            Order,
  [in, out] LPD3DXPRTBUFFER pDataOut
);
```



## <a name="parameters"></a><span data-ttu-id="72855-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="72855-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="72855-107">*Порядок следования* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="72855-107">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72855-108">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="72855-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="72855-109">Порядок вычисления SH.</span><span class="sxs-lookup"><span data-stu-id="72855-109">Order of the SH evaluation.</span></span> <span data-ttu-id="72855-110">Должен находиться в диапазоне от [D3DXSH \_ МИНОРДЕР](other-d3dx-constants.md) до D3DXSH \_ максордер, включительно.</span><span class="sxs-lookup"><span data-stu-id="72855-110">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="72855-111">При оценке создается коэффициент порядка ².</span><span class="sxs-lookup"><span data-stu-id="72855-111">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="72855-112">Степень оценки — Order-1.</span><span class="sxs-lookup"><span data-stu-id="72855-112">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="72855-113">*pData* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="72855-113">*pDataOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="72855-114">Тип: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="72855-114">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="72855-115">Указатель на выходной объект [**ID3DXPRTBuffer**](id3dxprtbuffer.md) , моделирующий отправку прямого освещения с приближением sh.</span><span class="sxs-lookup"><span data-stu-id="72855-115">Pointer to an output [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that models the direct lighting contribution with the SH approximation.</span></span> <span data-ttu-id="72855-116">Этот буфер должен иметь правильное число цветовых каналов, выделенных для имитации.</span><span class="sxs-lookup"><span data-stu-id="72855-116">This buffer must have the proper number of color channels allocated for the simulation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="72855-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="72855-117">Return value</span></span>

<span data-ttu-id="72855-118">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="72855-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="72855-119">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="72855-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="72855-120">В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="72855-120">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="72855-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="72855-121">Remarks</span></span>

<span data-ttu-id="72855-122">Выходные данные не включают албедо, и в симуляторе встроена только входящая лампочка.</span><span class="sxs-lookup"><span data-stu-id="72855-122">The output does not include albedo, and only incoming light is integrated in the simulator.</span></span> <span data-ttu-id="72855-123">Не умножая албедо, вы можете моделировать албедо вариации на более точном масштабе, чем исходный радианце, тем самым обеспечивая более точные результаты сжатия.</span><span class="sxs-lookup"><span data-stu-id="72855-123">By not multiplying the albedo, you can model albedo variation at a finer scale than the source radiance, thereby yielding more accurate results from compression.</span></span>

<span data-ttu-id="72855-124">Вызовите метод [**ID3DXPRTEngine:: мултиплялбедо**](id3dxprtengine--multiplyalbedo.md) , чтобы умножить каждый предварительно вычисленный вектор перемещения РАДИАНЦЕ (PRT) на албедо.</span><span class="sxs-lookup"><span data-stu-id="72855-124">Call [**ID3DXPRTEngine::MultiplyAlbedo**](id3dxprtengine--multiplyalbedo.md) to multiply each precomputed radiance transfer (PRT) vector by the albedo.</span></span>

## <a name="requirements"></a><span data-ttu-id="72855-125">Требования</span><span class="sxs-lookup"><span data-stu-id="72855-125">Requirements</span></span>



| <span data-ttu-id="72855-126">Требование</span><span class="sxs-lookup"><span data-stu-id="72855-126">Requirement</span></span> | <span data-ttu-id="72855-127">Значение</span><span class="sxs-lookup"><span data-stu-id="72855-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="72855-128">Header</span><span class="sxs-lookup"><span data-stu-id="72855-128">Header</span></span><br/>  | <dl> <span data-ttu-id="72855-129"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="72855-129"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="72855-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="72855-130">Library</span></span><br/> | <dl> <span data-ttu-id="72855-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="72855-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="72855-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="72855-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72855-133">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="72855-133">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> </dl>

 

 
