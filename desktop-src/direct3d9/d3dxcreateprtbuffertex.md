---
description: Создает предварительно вычисленный буфер радианценой пересылки (PRT), который может быть сжат или заполнен симулятором. Эта функция должна использоваться для создания буферов на пиксель.
ms.assetid: 41e65674-e5e1-4df9-aab8-1530ebf85f25
title: Функция D3DXCreatePRTBufferTex (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreatePRTBufferTex
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e3e88073f85d281e164c002ba5180493f6217e3a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713701"
---
# <a name="d3dxcreateprtbuffertex-function"></a><span data-ttu-id="858ba-104">Функция D3DXCreatePRTBufferTex</span><span class="sxs-lookup"><span data-stu-id="858ba-104">D3DXCreatePRTBufferTex function</span></span>

<span data-ttu-id="858ba-105">Создает предварительно вычисленный буфер радианценой пересылки (PRT), который может быть сжат или заполнен симулятором.</span><span class="sxs-lookup"><span data-stu-id="858ba-105">Creates a precomputed radiance transfer (PRT) buffer that can be compressed or filled by a simulator.</span></span> <span data-ttu-id="858ba-106">Эта функция должна использоваться для создания буферов на пиксель.</span><span class="sxs-lookup"><span data-stu-id="858ba-106">This function should be used to create per-pixel buffers.</span></span>

## <a name="syntax"></a><span data-ttu-id="858ba-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="858ba-107">Syntax</span></span>


```C++
HRESULT D3DXCreatePRTBufferTex(
  _In_    UINT            Width,
  _In_    UINT            Height,
  _In_    UINT            NumCoeffs,
  _In_    UINT            NumChannels,
  _Inout_ LPD3DXPRTBUFFER *ppBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="858ba-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="858ba-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="858ba-109">*Ширина* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="858ba-109">*Width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="858ba-110">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="858ba-110">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="858ba-111">Ширина текстуры в пикселях.</span><span class="sxs-lookup"><span data-stu-id="858ba-111">Width of the texture, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="858ba-112">*Высота* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="858ba-112">*Height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="858ba-113">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="858ba-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="858ba-114">Высота текстуры (в пикселях).</span><span class="sxs-lookup"><span data-stu-id="858ba-114">Height of the texture, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="858ba-115">*Нумкоеффс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="858ba-115">*NumCoeffs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="858ba-116">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="858ba-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="858ba-117">Количество коэффициентов на расположение выборки.</span><span class="sxs-lookup"><span data-stu-id="858ba-117">Number of coefficients per sample location.</span></span> <span data-ttu-id="858ba-118">При использовании сферического гармонического (SH) PRT число коэффициентов должно быть Order ², где Order — это порядок вычисления SH.</span><span class="sxs-lookup"><span data-stu-id="858ba-118">When using spherical harmonic (SH) PRT, the number of coefficients should be Order², where Order is the order of the SH evaluation.</span></span> <span data-ttu-id="858ba-119">Порядок должен находиться в диапазоне от [D3DXSH \_ МИНОРДЕР](other-d3dx-constants.md) до D3DXSH \_ максордер, включительно.</span><span class="sxs-lookup"><span data-stu-id="858ba-119">Order must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="858ba-120">Степень оценки — Order-1.</span><span class="sxs-lookup"><span data-stu-id="858ba-120">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="858ba-121">*Нумчаннелс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="858ba-121">*NumChannels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="858ba-122">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="858ba-122">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="858ba-123">Число цветовых каналов, устанавливаемых в сетке.</span><span class="sxs-lookup"><span data-stu-id="858ba-123">Number of color channels to set in the mesh.</span></span> <span data-ttu-id="858ba-124">Задайте значение 1, чтобы указать серые материалы (R = G = B), или 3, чтобы включить эффекты цвета суперсовременные.</span><span class="sxs-lookup"><span data-stu-id="858ba-124">Set to 1 to specify gray materials (R = G = B), or 3 to enable color bleeding effects.</span></span>

</dd> <dt>

<span data-ttu-id="858ba-125">*ппбуффер* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="858ba-125">*ppBuffer* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="858ba-126">Тип: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="858ba-126">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)\***</span></span>

<span data-ttu-id="858ba-127">Адрес указателя на созданный объект [**ID3DXPRTBuffer**](id3dxprtbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="858ba-127">Address of a pointer to the created [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="858ba-128">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="858ba-128">Return value</span></span>

<span data-ttu-id="858ba-129">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="858ba-129">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="858ba-130">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="858ba-130">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="858ba-131">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="858ba-131">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="858ba-132">Комментарии</span><span class="sxs-lookup"><span data-stu-id="858ba-132">Remarks</span></span>

<span data-ttu-id="858ba-133">При создании буфера все значения инициализируются нулем.</span><span class="sxs-lookup"><span data-stu-id="858ba-133">When the buffer is created, all values are initialized to zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="858ba-134">Требования</span><span class="sxs-lookup"><span data-stu-id="858ba-134">Requirements</span></span>



| <span data-ttu-id="858ba-135">Требование</span><span class="sxs-lookup"><span data-stu-id="858ba-135">Requirement</span></span> | <span data-ttu-id="858ba-136">Значение</span><span class="sxs-lookup"><span data-stu-id="858ba-136">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="858ba-137">Header</span><span class="sxs-lookup"><span data-stu-id="858ba-137">Header</span></span><br/>  | <dl> <span data-ttu-id="858ba-138"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="858ba-138"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="858ba-139">Библиотека</span><span class="sxs-lookup"><span data-stu-id="858ba-139">Library</span></span><br/> | <dl> <span data-ttu-id="858ba-140"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="858ba-140"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="858ba-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="858ba-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="858ba-142">Предварительно вычисленные функции пересылки Радианце</span><span class="sxs-lookup"><span data-stu-id="858ba-142">Precomputed Radiance Transfer Functions</span></span>](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> <dt>

[<span data-ttu-id="858ba-143">**D3DXCreatePRTBuffer**</span><span class="sxs-lookup"><span data-stu-id="858ba-143">**D3DXCreatePRTBuffer**</span></span>](d3dxcreateprtbuffer.md)
</dt> </dl>

 

 
