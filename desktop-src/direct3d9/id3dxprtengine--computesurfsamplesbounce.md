---
description: Выполняет вычисление предварительно вычисленных радианце передач (PRT) для произвольной точки (и обычного вектора).
ms.assetid: 862a9067-5c5e-4428-86f4-ebef653411b9
title: 'Метод ID3DXPRTEngine:: Компутесурфсамплесбаунце (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeSurfSamplesBounce
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 55cea3e87850273b6ea8d190422bd77afeb831f4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104356053"
---
# <a name="id3dxprtenginecomputesurfsamplesbounce-method"></a><span data-ttu-id="15d2f-103">Метод ID3DXPRTEngine:: Компутесурфсамплесбаунце</span><span class="sxs-lookup"><span data-stu-id="15d2f-103">ID3DXPRTEngine::ComputeSurfSamplesBounce method</span></span>

<span data-ttu-id="15d2f-104">Выполняет вычисление предварительно вычисленных радианце передач (PRT) для произвольной точки (и обычного вектора).</span><span class="sxs-lookup"><span data-stu-id="15d2f-104">Computes precomputed radiance transfer (PRT) samples for an arbitrary point (and normal vector).</span></span>

## <a name="syntax"></a><span data-ttu-id="15d2f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="15d2f-105">Syntax</span></span>


```C++
HRESULT ComputeSurfSamplesBounce(
  [in]            LPD3DXPRTBUFFER pSurfDataIn,
  [in]            UINT            NumSamples,
  [in]      const D3DXVECTOR3     *pSampleLocs,
  [in]      const D3DXVECTOR3     *pSampleNorms,
  [in, out]       LPD3DXPRTBUFFER pDataOut,
  [in, out]       LPD3DXPRTBUFFER pDataTotal
);
```



## <a name="parameters"></a><span data-ttu-id="15d2f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="15d2f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15d2f-107">*псурфдатаин* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="15d2f-107">*pSurfDataIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15d2f-108">Тип: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="15d2f-108">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="15d2f-109">Указатель на входной объект [**ID3DXPRTBuffer**](id3dxprtbuffer.md) , представляющий исходный радианце трехмерного объекта.</span><span class="sxs-lookup"><span data-stu-id="15d2f-109">Pointer to an input [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that represents the source radiance of the 3D object.</span></span> <span data-ttu-id="15d2f-110">Этот входной буфер должен иметь правильное число цветовых каналов, выделенных для моделирования.</span><span class="sxs-lookup"><span data-stu-id="15d2f-110">This input buffer must have the proper number of color channels allocated for the simulation.</span></span>

</dd> <dt>

<span data-ttu-id="15d2f-111">*Нумсамплес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="15d2f-111">*NumSamples* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15d2f-112">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="15d2f-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="15d2f-113">Число расположений выборки.</span><span class="sxs-lookup"><span data-stu-id="15d2f-113">Number of sample locations.</span></span>

</dd> <dt>

<span data-ttu-id="15d2f-114">*псамплелокс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="15d2f-114">*pSampleLocs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15d2f-115">Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="15d2f-115">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="15d2f-116">Расположение для каждого образца.</span><span class="sxs-lookup"><span data-stu-id="15d2f-116">Position for each sample.</span></span>

</dd> <dt>

<span data-ttu-id="15d2f-117">*псампленормс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="15d2f-117">*pSampleNorms* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15d2f-118">Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="15d2f-118">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="15d2f-119">Стандартный вектор для каждого расположения выборки.</span><span class="sxs-lookup"><span data-stu-id="15d2f-119">Normal vector for each sample location.</span></span>

</dd> <dt>

<span data-ttu-id="15d2f-120">*pData* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="15d2f-120">*pDataOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="15d2f-121">Тип: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="15d2f-121">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="15d2f-122">Указатель на выходной объект [**ID3DXPRTBuffer**](id3dxprtbuffer.md) , моделирующий прямое освещение в точке, с использованием аппроксимации «сферический гармонией» (SH).</span><span class="sxs-lookup"><span data-stu-id="15d2f-122">Pointer to an output [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that models the direct lighting contribution to the point, using the spherical harmonic (SH) approximation.</span></span>

</dd> <dt>

<span data-ttu-id="15d2f-123">*пдататотал* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="15d2f-123">*pDataTotal* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="15d2f-124">Тип: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="15d2f-124">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="15d2f-125">Указатель на необязательный объект [**ID3DXPRTBuffer**](id3dxprtbuffer.md) , который является выполняющейся суммой всех предыдущих выходов pData.</span><span class="sxs-lookup"><span data-stu-id="15d2f-125">Pointer to an optional [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that is the running sum of all previous pDataOut outputs.</span></span> <span data-ttu-id="15d2f-126">Может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="15d2f-126">May be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15d2f-127">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="15d2f-127">Return value</span></span>

<span data-ttu-id="15d2f-128">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="15d2f-128">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="15d2f-129">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="15d2f-129">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="15d2f-130">В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="15d2f-130">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="15d2f-131">Требования</span><span class="sxs-lookup"><span data-stu-id="15d2f-131">Requirements</span></span>



| <span data-ttu-id="15d2f-132">Требование</span><span class="sxs-lookup"><span data-stu-id="15d2f-132">Requirement</span></span> | <span data-ttu-id="15d2f-133">Значение</span><span class="sxs-lookup"><span data-stu-id="15d2f-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="15d2f-134">Header</span><span class="sxs-lookup"><span data-stu-id="15d2f-134">Header</span></span><br/>  | <dl> <span data-ttu-id="15d2f-135"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="15d2f-135"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="15d2f-136">Библиотека</span><span class="sxs-lookup"><span data-stu-id="15d2f-136">Library</span></span><br/> | <dl> <span data-ttu-id="15d2f-137"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="15d2f-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="15d2f-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="15d2f-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15d2f-139">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="15d2f-139">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> <dt>

[<span data-ttu-id="15d2f-140">**ID3DXPRTEngine:: Компутесурфсамплесдиректш**</span><span class="sxs-lookup"><span data-stu-id="15d2f-140">**ID3DXPRTEngine::ComputeSurfSamplesDirectSH**</span></span>](id3dxprtengine--computesurfsamplesdirectsh.md)
</dt> </dl>

 

 
