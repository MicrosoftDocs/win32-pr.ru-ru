---
description: Создает предварительно вычисленный буфер радианценой пересылки (PRT), который может быть сжат или заполнен симулятором. Эта функция должна использоваться для создания буферов на уровне вершины или тома.
ms.assetid: f79a3691-ab5f-4404-aafd-f9635ff88e71
title: Функция D3DXCreatePRTBuffer (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreatePRTBuffer
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8107edfec436d9eda35324f6934b3f70df6a05d2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713702"
---
# <a name="d3dxcreateprtbuffer-function"></a><span data-ttu-id="9f9cf-104">Функция D3DXCreatePRTBuffer</span><span class="sxs-lookup"><span data-stu-id="9f9cf-104">D3DXCreatePRTBuffer function</span></span>

<span data-ttu-id="9f9cf-105">Создает предварительно вычисленный буфер радианценой пересылки (PRT), который может быть сжат или заполнен симулятором.</span><span class="sxs-lookup"><span data-stu-id="9f9cf-105">Creates a precomputed radiance transfer (PRT) buffer that can be compressed or filled by a simulator.</span></span> <span data-ttu-id="9f9cf-106">Эта функция должна использоваться для создания буферов на уровне вершины или тома.</span><span class="sxs-lookup"><span data-stu-id="9f9cf-106">This function should be used to create per-vertex or volume buffers.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f9cf-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9f9cf-107">Syntax</span></span>


```C++
HRESULT D3DXCreatePRTBuffer(
  _In_    UINT            NumSamples,
  _In_    UINT            NumCoeffs,
  _In_    UINT            NumChannels,
  _Inout_ LPD3DXPRTBUFFER *ppBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="9f9cf-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="9f9cf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f9cf-109">*Нумсамплес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9f9cf-109">*NumSamples* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f9cf-110">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9f9cf-110">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9f9cf-111">Количество вершин (или пикселей текстуры) с выборкой.</span><span class="sxs-lookup"><span data-stu-id="9f9cf-111">Number of vertices (or texels) sampled.</span></span>

</dd> <dt>

<span data-ttu-id="9f9cf-112">*Нумкоеффс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9f9cf-112">*NumCoeffs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f9cf-113">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9f9cf-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9f9cf-114">Количество коэффициентов на расположение выборки.</span><span class="sxs-lookup"><span data-stu-id="9f9cf-114">Number of coefficients per sample location.</span></span> <span data-ttu-id="9f9cf-115">При использовании сферического гармонического (SH) PRT число коэффициентов должно быть Order ², где Order — это порядок вычисления SH.</span><span class="sxs-lookup"><span data-stu-id="9f9cf-115">When using spherical harmonic (SH) PRT, the number of coefficients should be Order², where Order is the order of the SH evaluation.</span></span> <span data-ttu-id="9f9cf-116">Порядок должен находиться в диапазоне от [D3DXSH \_ МИНОРДЕР](other-d3dx-constants.md) до D3DXSH \_ максордер, включительно.</span><span class="sxs-lookup"><span data-stu-id="9f9cf-116">Order must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="9f9cf-117">Степень оценки — Order-1.</span><span class="sxs-lookup"><span data-stu-id="9f9cf-117">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="9f9cf-118">*Нумчаннелс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9f9cf-118">*NumChannels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f9cf-119">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9f9cf-119">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9f9cf-120">Число цветовых каналов, устанавливаемых в сетке.</span><span class="sxs-lookup"><span data-stu-id="9f9cf-120">Number of color channels to set in the mesh.</span></span> <span data-ttu-id="9f9cf-121">Задайте значение 1, чтобы указать серые материалы (R = G = B), или 3, чтобы включить эффекты цвета суперсовременные.</span><span class="sxs-lookup"><span data-stu-id="9f9cf-121">Set to 1 to specify gray materials (R = G = B), or 3 to enable color bleeding effects.</span></span>

</dd> <dt>

<span data-ttu-id="9f9cf-122">*ппбуффер* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="9f9cf-122">*ppBuffer* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="9f9cf-123">Тип: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="9f9cf-123">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)\***</span></span>

<span data-ttu-id="9f9cf-124">Адрес указателя на созданный объект [**ID3DXPRTBuffer**](id3dxprtbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="9f9cf-124">Address of a pointer to the created [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f9cf-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9f9cf-125">Return value</span></span>

<span data-ttu-id="9f9cf-126">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9f9cf-126">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9f9cf-127">Если функция выполнена успешно, возвращается значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="9f9cf-127">If the function succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="9f9cf-128">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="9f9cf-128">If the function fails, the return value can be one of these: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f9cf-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9f9cf-129">Remarks</span></span>

<span data-ttu-id="9f9cf-130">При создании буфера все значения инициализируются нулем.</span><span class="sxs-lookup"><span data-stu-id="9f9cf-130">When the buffer is created, all values are initialized to zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f9cf-131">Требования</span><span class="sxs-lookup"><span data-stu-id="9f9cf-131">Requirements</span></span>



| <span data-ttu-id="9f9cf-132">Требование</span><span class="sxs-lookup"><span data-stu-id="9f9cf-132">Requirement</span></span> | <span data-ttu-id="9f9cf-133">Значение</span><span class="sxs-lookup"><span data-stu-id="9f9cf-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9f9cf-134">Header</span><span class="sxs-lookup"><span data-stu-id="9f9cf-134">Header</span></span><br/>  | <dl> <span data-ttu-id="9f9cf-135"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="9f9cf-135"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="9f9cf-136">Библиотека</span><span class="sxs-lookup"><span data-stu-id="9f9cf-136">Library</span></span><br/> | <dl> <span data-ttu-id="9f9cf-137"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9f9cf-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9f9cf-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9f9cf-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f9cf-139">Предварительно вычисленные функции пересылки Радианце</span><span class="sxs-lookup"><span data-stu-id="9f9cf-139">Precomputed Radiance Transfer Functions</span></span>](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> <dt>

[<span data-ttu-id="9f9cf-140">**D3DXCreatePRTBufferTex**</span><span class="sxs-lookup"><span data-stu-id="9f9cf-140">**D3DXCreatePRTBufferTex**</span></span>](d3dxcreateprtbuffertex.md)
</dt> </dl>

 

 
