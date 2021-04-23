---
description: Выполняет вычисление, в произвольных точках, не применяя сетку, вектор перемещения, который сопоставляет исходный радианце (представленный приблизительно гармонической (SH) аппроксимацию) для выхода из радианце.
ms.assetid: 44790465-440d-4426-b780-ed872fbf8efb
title: 'Метод ID3DXPRTEngine:: Компутесурфсамплесдиректш (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeSurfSamplesDirectSH
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 03adb1729a8a2e771ea681ccbdd180999d3adcbf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104356043"
---
# <a name="id3dxprtenginecomputesurfsamplesdirectsh-method"></a><span data-ttu-id="c81a7-103">Метод ID3DXPRTEngine:: Компутесурфсамплесдиректш</span><span class="sxs-lookup"><span data-stu-id="c81a7-103">ID3DXPRTEngine::ComputeSurfSamplesDirectSH method</span></span>

<span data-ttu-id="c81a7-104">Выполняет вычисление, в произвольных точках, не применяя сетку, вектор перемещения, который сопоставляет исходный радианце (представленный приблизительно гармонической (SH) аппроксимацию) для выхода из радианце.</span><span class="sxs-lookup"><span data-stu-id="c81a7-104">Computes, at an arbitrary point not on a mesh, a transfer vector that maps source radiance (represented by a spherical harmonic (SH) approximation) to exit radiance.</span></span>

## <a name="syntax"></a><span data-ttu-id="c81a7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c81a7-105">Syntax</span></span>


```C++
HRESULT ComputeSurfSamplesDirectSH(
  [in]            UINT            SHOrder,
  [in]            UINT            NumSamples,
  [in]      const D3DXVECTOR3     *pSampleLocs,
  [in]      const D3DXVECTOR3     *pSampleNorms,
  [in, out]       LPD3DXPRTBUFFER pDataOut
);
```



## <a name="parameters"></a><span data-ttu-id="c81a7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c81a7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c81a7-107">*Шордер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c81a7-107">*SHOrder* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c81a7-108">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c81a7-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c81a7-109">Порядок использования аппроксимации.</span><span class="sxs-lookup"><span data-stu-id="c81a7-109">Order of the SH approximation to use.</span></span>

</dd> <dt>

<span data-ttu-id="c81a7-110">*Нумсамплес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c81a7-110">*NumSamples* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c81a7-111">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c81a7-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c81a7-112">Число расположений выборки.</span><span class="sxs-lookup"><span data-stu-id="c81a7-112">Number of sample locations.</span></span>

</dd> <dt>

<span data-ttu-id="c81a7-113">*псамплелокс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c81a7-113">*pSampleLocs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c81a7-114">Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="c81a7-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="c81a7-115">Расположение для каждого образца.</span><span class="sxs-lookup"><span data-stu-id="c81a7-115">Position for each sample.</span></span>

</dd> <dt>

<span data-ttu-id="c81a7-116">*псампленормс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c81a7-116">*pSampleNorms* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c81a7-117">Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="c81a7-117">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="c81a7-118">Стандартный вектор для каждого расположения выборки.</span><span class="sxs-lookup"><span data-stu-id="c81a7-118">Normal vector for each sample location.</span></span>

</dd> <dt>

<span data-ttu-id="c81a7-119">*pData* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="c81a7-119">*pDataOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c81a7-120">Тип: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="c81a7-120">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="c81a7-121">Указатель на выходной объект [**ID3DXPRTBuffer**](id3dxprtbuffer.md) , моделирующий прямое освещение в точке с использованием аппроксимации sh.</span><span class="sxs-lookup"><span data-stu-id="c81a7-121">Pointer to an output [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that models the direct lighting contribution to the point, using the SH approximation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c81a7-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c81a7-122">Return value</span></span>

<span data-ttu-id="c81a7-123">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c81a7-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c81a7-124">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="c81a7-124">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="c81a7-125">В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="c81a7-125">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="c81a7-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c81a7-126">Remarks</span></span>

<span data-ttu-id="c81a7-127">Не используйте буфер текстуры при вызове этого метода.</span><span class="sxs-lookup"><span data-stu-id="c81a7-127">Do not use a texture buffer when calling this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="c81a7-128">Требования</span><span class="sxs-lookup"><span data-stu-id="c81a7-128">Requirements</span></span>



| <span data-ttu-id="c81a7-129">Требование</span><span class="sxs-lookup"><span data-stu-id="c81a7-129">Requirement</span></span> | <span data-ttu-id="c81a7-130">Значение</span><span class="sxs-lookup"><span data-stu-id="c81a7-130">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c81a7-131">Header</span><span class="sxs-lookup"><span data-stu-id="c81a7-131">Header</span></span><br/>  | <dl> <span data-ttu-id="c81a7-132"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="c81a7-132"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="c81a7-133">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c81a7-133">Library</span></span><br/> | <dl> <span data-ttu-id="c81a7-134"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c81a7-134"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c81a7-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c81a7-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c81a7-136">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="c81a7-136">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> <dt>

[<span data-ttu-id="c81a7-137">**ID3DXPRTEngine:: Компутедиректлигхтингш**</span><span class="sxs-lookup"><span data-stu-id="c81a7-137">**ID3DXPRTEngine::ComputeDirectLightingSH**</span></span>](id3dxprtengine--computedirectlightingsh.md)
</dt> <dt>

[<span data-ttu-id="c81a7-138">**ID3DXPRTEngine:: Компутесурфсамплесбаунце**</span><span class="sxs-lookup"><span data-stu-id="c81a7-138">**ID3DXPRTEngine::ComputeSurfSamplesBounce**</span></span>](id3dxprtengine--computesurfsamplesbounce.md)
</dt> </dl>

 

 
