---
description: 'Выполняет вычисление исходного радианцеа, полученного из рассеивания подповерхности, с помощью свойств материала, заданных ID3DXPRTEngine:: Сетмешматериалс. Этот метод можно использовать только для материалов, определенных для вершины в объекте сетки.'
ms.assetid: cdf0d9c1-70e3-44d5-b97a-0521e6739daf
title: 'Метод ID3DXPRTEngine:: Compute (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeSS
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 89a69be6cc946ff6695d234b8bfb82532385526e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104356063"
---
# <a name="id3dxprtenginecomputess-method"></a><span data-ttu-id="aeddb-104">Метод ID3DXPRTEngine:: COMPUTE</span><span class="sxs-lookup"><span data-stu-id="aeddb-104">ID3DXPRTEngine::ComputeSS method</span></span>

<span data-ttu-id="aeddb-105">Выполняет вычисление исходного радианцеа, полученного из рассеивания подповерхности, с помощью свойств материала, заданных [**ID3DXPRTEngine:: сетмешматериалс**](id3dxprtengine--setmeshmaterials.md).</span><span class="sxs-lookup"><span data-stu-id="aeddb-105">Computes the source radiance resulting from subsurface scattering, using material properties set by [**ID3DXPRTEngine::SetMeshMaterials**](id3dxprtengine--setmeshmaterials.md).</span></span> <span data-ttu-id="aeddb-106">Этот метод можно использовать только для материалов, определенных для вершины в объекте сетки.</span><span class="sxs-lookup"><span data-stu-id="aeddb-106">This method can be used only for materials defined per-vertex in a mesh object.</span></span>

## <a name="syntax"></a><span data-ttu-id="aeddb-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="aeddb-107">Syntax</span></span>


```C++
HRESULT ComputeSS(
  [in]      LPD3DXPRTBUFFER pDataIn,
  [in, out] LPD3DXPRTBUFFER pDataOut,
  [in, out] LPD3DXPRTBUFFER pDataTotal
);
```



## <a name="parameters"></a><span data-ttu-id="aeddb-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="aeddb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aeddb-109">*pData* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="aeddb-109">*pDataIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aeddb-110">Тип: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="aeddb-110">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="aeddb-111">Указатель на входной объект [**ID3DXPRTBuffer**](id3dxprtbuffer.md) , представляющий трехмерный объект из предыдущего освещения.</span><span class="sxs-lookup"><span data-stu-id="aeddb-111">Pointer to an input [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that represents the 3D object from the previous light bounce.</span></span> <span data-ttu-id="aeddb-112">Этот входной буфер должен иметь правильное число цветовых каналов, выделенных для моделирования.</span><span class="sxs-lookup"><span data-stu-id="aeddb-112">This input buffer must have the proper number of color channels allocated for the simulation.</span></span>

</dd> <dt>

<span data-ttu-id="aeddb-113">*pData* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="aeddb-113">*pDataOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="aeddb-114">Тип: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="aeddb-114">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="aeddb-115">Указатель на выходной объект [**ID3DXPRTBuffer**](id3dxprtbuffer.md) , моделирующий один элемент отскока точечной светлой поверхности.</span><span class="sxs-lookup"><span data-stu-id="aeddb-115">Pointer to an output [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that models a single bounce of the subsurface-scattered light.</span></span> <span data-ttu-id="aeddb-116">Этот выходной буфер должен иметь правильное число цветовых каналов, выделенных для моделирования.</span><span class="sxs-lookup"><span data-stu-id="aeddb-116">This output buffer must have the proper number of color channels allocated for the simulation.</span></span>

</dd> <dt>

<span data-ttu-id="aeddb-117">*пдататотал* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="aeddb-117">*pDataTotal* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="aeddb-118">Тип: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="aeddb-118">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="aeddb-119">Указатель на необязательный объект [**ID3DXPRTBuffer**](id3dxprtbuffer.md) , который является выполняющейся суммой всех предыдущих выходов pData.</span><span class="sxs-lookup"><span data-stu-id="aeddb-119">Pointer to an optional [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that is the running sum of all previous pDataOut outputs.</span></span> <span data-ttu-id="aeddb-120">Может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="aeddb-120">May be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aeddb-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="aeddb-121">Return value</span></span>

<span data-ttu-id="aeddb-122">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="aeddb-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="aeddb-123">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="aeddb-123">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="aeddb-124">В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="aeddb-124">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="aeddb-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="aeddb-125">Remarks</span></span>

<span data-ttu-id="aeddb-126">Чтобы смоделировать подложку, вызывайте этот метод для каждого освещения после вызова метода ID3DXPRTEngine:: Компутедиректлигхтинг.</span><span class="sxs-lookup"><span data-stu-id="aeddb-126">To model subsurface scattering, call this method for each light bounce after an ID3DXPRTEngine::ComputeDirectLighting method is called.</span></span>

<span data-ttu-id="aeddb-127">Используйте следующую последовательность вызовов для моделирования рассеивания подповерхности.</span><span class="sxs-lookup"><span data-stu-id="aeddb-127">Use the following calling sequence to model subsurface scattering.</span></span>


```
LPD3DXPRTBUFFER pDataA, pDataB, pDataC; // initialization
ID3DXPRTEngine* m_pPRTEngine;
    
hr = m_pPRTEngine->ComputeDirectLightingSH( SHOrder, pDataA );
    
// *pDataC should be set to zero. The ComputeSS call will add together the    
// direct lighting results from pDataA for non-subsurface scattering elements   
// and subsurface scattering results for the subsurface scattering elements.
    
hr = m_pPRTEngine->ComputeSS( pDataA, pDataB, pDataC );
if ( FAILED( hr ) ) goto Exit;
```



<span data-ttu-id="aeddb-128">Выходные данные этого метода не включают албедо, и в симуляторе встроена только входящая лампочка.</span><span class="sxs-lookup"><span data-stu-id="aeddb-128">The output of this method does not include albedo, and only incoming light is integrated in the simulator.</span></span> <span data-ttu-id="aeddb-129">Не умножая албедо, вы можете моделировать албедо вариации на более точном масштабе, чем исходный радианце, тем самым обеспечивая более точные результаты сжатия.</span><span class="sxs-lookup"><span data-stu-id="aeddb-129">By not multiplying the albedo, you can model albedo variation at a finer scale than the source radiance, thereby yielding more accurate results from compression.</span></span>

<span data-ttu-id="aeddb-130">Вызовите метод [**ID3DXPRTEngine:: мултиплялбедо**](id3dxprtengine--multiplyalbedo.md) , чтобы умножить каждый предварительно вычисленный вектор перемещения РАДИАНЦЕ (PRT) на албедо.</span><span class="sxs-lookup"><span data-stu-id="aeddb-130">Call [**ID3DXPRTEngine::MultiplyAlbedo**](id3dxprtengine--multiplyalbedo.md) to multiply each precomputed radiance transfer (PRT) vector by the albedo.</span></span>

## <a name="requirements"></a><span data-ttu-id="aeddb-131">Требования</span><span class="sxs-lookup"><span data-stu-id="aeddb-131">Requirements</span></span>



| <span data-ttu-id="aeddb-132">Требование</span><span class="sxs-lookup"><span data-stu-id="aeddb-132">Requirement</span></span> | <span data-ttu-id="aeddb-133">Значение</span><span class="sxs-lookup"><span data-stu-id="aeddb-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="aeddb-134">Header</span><span class="sxs-lookup"><span data-stu-id="aeddb-134">Header</span></span><br/>  | <dl> <span data-ttu-id="aeddb-135"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="aeddb-135"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="aeddb-136">Библиотека</span><span class="sxs-lookup"><span data-stu-id="aeddb-136">Library</span></span><br/> | <dl> <span data-ttu-id="aeddb-137"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="aeddb-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="aeddb-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="aeddb-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aeddb-139">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="aeddb-139">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> <dt>

[<span data-ttu-id="aeddb-140">**ID3DXPRTEngine:: Компутебаунце**</span><span class="sxs-lookup"><span data-stu-id="aeddb-140">**ID3DXPRTEngine::ComputeBounce**</span></span>](id3dxprtengine--computebounce.md)
</dt> </dl>

 

 




