---
description: Создает сжатый предварительно вычисленный буфер радианценой пересылки (PRT) из несжатого объекта ID3DXPRTBuffer. Эта функция должна использоваться с буферами на уровне вершины или тома.
ms.assetid: 1464d2dd-05db-4d9a-84ac-39d57b6fff4f
title: Функция D3DXCreatePRTCompBuffer (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreatePRTCompBuffer
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6906067c8f2b412b58c728756ecaa6415168f05a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354920"
---
# <a name="d3dxcreateprtcompbuffer-function"></a><span data-ttu-id="702a0-104">Функция D3DXCreatePRTCompBuffer</span><span class="sxs-lookup"><span data-stu-id="702a0-104">D3DXCreatePRTCompBuffer function</span></span>

<span data-ttu-id="702a0-105">Создает сжатый предварительно вычисленный буфер радианценой пересылки (PRT) из несжатого объекта [**ID3DXPRTBuffer**](id3dxprtbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="702a0-105">Creates a compressed precomputed radiance transfer (PRT) buffer from an uncompressed [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object.</span></span> <span data-ttu-id="702a0-106">Эта функция должна использоваться с буферами на уровне вершины или тома.</span><span class="sxs-lookup"><span data-stu-id="702a0-106">This function should be used with per-vertex or volume buffers.</span></span>

## <a name="syntax"></a><span data-ttu-id="702a0-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="702a0-107">Syntax</span></span>


```C++
HRESULT D3DXCreatePRTCompBuffer(
  _In_    D3DXSHCOMPRESSQUALITYTYPE Quality,
  _In_    UINT                      NumClusters,
  _In_    UINT                      NumPCA,
  _In_    LPD3DXSHPRTSIMCB          pCB,
  _In_    LPVOID                    lpUserContext,
  _In_    LPD3DXPRTBUFFER           pBuffer,
  _Inout_ LPD3DXPRTCOMPBUFFER       *ppBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="702a0-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="702a0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="702a0-109">*Качество* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="702a0-109">*Quality* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="702a0-110">Тип: **[ **D3DXSHCOMPRESSQUALITYTYPE**](./d3dxshcompressqualitytype.md)**</span><span class="sxs-lookup"><span data-stu-id="702a0-110">Type: **[**D3DXSHCOMPRESSQUALITYTYPE**](./d3dxshcompressqualitytype.md)**</span></span>

<span data-ttu-id="702a0-111">Качество сжатия сферических гармонических излучений (SH).</span><span class="sxs-lookup"><span data-stu-id="702a0-111">Quality of spherical harmonic (SH) compression.</span></span> <span data-ttu-id="702a0-112">См. [**D3DXSHCOMPRESSQUALITYTYPE**](./d3dxshcompressqualitytype.md).</span><span class="sxs-lookup"><span data-stu-id="702a0-112">See [**D3DXSHCOMPRESSQUALITYTYPE**](./d3dxshcompressqualitytype.md).</span></span>

</dd> <dt>

<span data-ttu-id="702a0-113">*Нумклустерс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="702a0-113">*NumClusters* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="702a0-114">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="702a0-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="702a0-115">Количество кластеров, используемых для сжатия.</span><span class="sxs-lookup"><span data-stu-id="702a0-115">Number of clusters to use for compression.</span></span>

</dd> <dt>

<span data-ttu-id="702a0-116">*Нумпка* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="702a0-116">*NumPCA* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="702a0-117">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="702a0-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="702a0-118">Количество отдельных векторов анализа основных компонентов (PCA) для использования в каждом кластере.</span><span class="sxs-lookup"><span data-stu-id="702a0-118">Number of principal component analysis (PCA) basis vectors to use in each cluster.</span></span>

</dd> <dt>

<span data-ttu-id="702a0-119">*ПКБ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="702a0-119">*pCB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="702a0-120">Тип: **[LPD3DXSHPRTSIMCB](lpd3dxshprtsimcb.md)**</span><span class="sxs-lookup"><span data-stu-id="702a0-120">Type: **[LPD3DXSHPRTSIMCB](lpd3dxshprtsimcb.md)**</span></span>

<span data-ttu-id="702a0-121">Необязательный указатель на функцию обратного вызова [LPD3DXSHPRTSIMCB](lpd3dxshprtsimcb.md) , используемый для вычисления процента завершенных вычислений сжатия PRT.</span><span class="sxs-lookup"><span data-stu-id="702a0-121">Optional pointer to the [LPD3DXSHPRTSIMCB](lpd3dxshprtsimcb.md) callback function that is used to compute the percentage of PRT compression computations completed.</span></span> <span data-ttu-id="702a0-122">Функция обратного вызова должна быть реализована, чтобы вернуть значение S \_ ОК для сохранения выполнения программы сжатия.</span><span class="sxs-lookup"><span data-stu-id="702a0-122">The callback function must be implemented to return S\_OK to keep running the compression routine.</span></span> <span data-ttu-id="702a0-123">Любое другое значение приведет к прерыванию сжатия.</span><span class="sxs-lookup"><span data-stu-id="702a0-123">Any other value will halt compression.</span></span> <span data-ttu-id="702a0-124">Может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="702a0-124">May be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="702a0-125">*лпусерконтекст* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="702a0-125">*lpUserContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="702a0-126">Тип: **[ **лпвоид**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="702a0-126">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="702a0-127">Необязательный указатель на определяемое пользователем значение, передаваемое функции обратного вызова [LPD3DXSHPRTSIMCB](lpd3dxshprtsimcb.md) .</span><span class="sxs-lookup"><span data-stu-id="702a0-127">Optional pointer to a user-defined value passed to the [LPD3DXSHPRTSIMCB](lpd3dxshprtsimcb.md) callback function.</span></span> <span data-ttu-id="702a0-128">Обычно используется приложением для передачи указателя на структуру данных, которая предоставляет сведения о контексте для функции обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="702a0-128">Typically used by an application to pass a pointer to a data structure that provides context information for the callback function.</span></span> <span data-ttu-id="702a0-129">Может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="702a0-129">May be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="702a0-130">*pBuffer* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="702a0-130">*pBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="702a0-131">Тип: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="702a0-131">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="702a0-132">Адрес указателя на несжатый объект [**ID3DXPRTBuffer**](id3dxprtbuffer.md) , который будет сжат.</span><span class="sxs-lookup"><span data-stu-id="702a0-132">Address of a pointer to the uncompressed [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that will be compressed.</span></span>

</dd> <dt>

<span data-ttu-id="702a0-133">*ппбуффер* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="702a0-133">*ppBuffer* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="702a0-134">Тип: **[ **LPD3DXPRTCOMPBUFFER**](id3dxprtcompbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="702a0-134">Type: **[**LPD3DXPRTCOMPBUFFER**](id3dxprtcompbuffer.md)\***</span></span>

<span data-ttu-id="702a0-135">Адрес указателя на выходной объект [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="702a0-135">Address of a pointer to the output [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="702a0-136">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="702a0-136">Return value</span></span>

<span data-ttu-id="702a0-137">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="702a0-137">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="702a0-138">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="702a0-138">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="702a0-139">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="702a0-139">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="702a0-140">Требования</span><span class="sxs-lookup"><span data-stu-id="702a0-140">Requirements</span></span>



| <span data-ttu-id="702a0-141">Требование</span><span class="sxs-lookup"><span data-stu-id="702a0-141">Requirement</span></span> | <span data-ttu-id="702a0-142">Значение</span><span class="sxs-lookup"><span data-stu-id="702a0-142">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="702a0-143">Header</span><span class="sxs-lookup"><span data-stu-id="702a0-143">Header</span></span><br/>  | <dl> <span data-ttu-id="702a0-144"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="702a0-144"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="702a0-145">Библиотека</span><span class="sxs-lookup"><span data-stu-id="702a0-145">Library</span></span><br/> | <dl> <span data-ttu-id="702a0-146"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="702a0-146"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="702a0-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="702a0-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="702a0-148">Предварительно вычисленные функции пересылки Радианце</span><span class="sxs-lookup"><span data-stu-id="702a0-148">Precomputed Radiance Transfer Functions</span></span>](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> <dt>

[<span data-ttu-id="702a0-149">**D3DXCreatePRTBuffer**</span><span class="sxs-lookup"><span data-stu-id="702a0-149">**D3DXCreatePRTBuffer**</span></span>](d3dxcreateprtbuffer.md)
</dt> <dt>

[<span data-ttu-id="702a0-150">**D3DXCreatePRTBufferTex**</span><span class="sxs-lookup"><span data-stu-id="702a0-150">**D3DXCreatePRTBufferTex**</span></span>](d3dxcreateprtbuffertex.md)
</dt> </dl>

 

 
