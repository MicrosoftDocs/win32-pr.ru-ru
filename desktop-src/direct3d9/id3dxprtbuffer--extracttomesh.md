---
description: Извлекает коэффициенты из одноканального буфера и добавляет данные в объект ID3DXMesh.
ms.assetid: 4fada987-ddd7-4c02-a177-dd81f3790588
title: 'Метод ID3DXPRTBuffer:: Екстракттомеш (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.ExtractToMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e6dfe545a934f541938d6030cdc3814f451d93c8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105704023"
---
# <a name="id3dxprtbufferextracttomesh-method"></a><span data-ttu-id="f3503-103">Метод ID3DXPRTBuffer:: Екстракттомеш</span><span class="sxs-lookup"><span data-stu-id="f3503-103">ID3DXPRTBuffer::ExtractToMesh method</span></span>

<span data-ttu-id="f3503-104">Извлекает коэффициенты из одноканального буфера и добавляет данные в объект [**ID3DXMesh**](id3dxmesh.md) .</span><span class="sxs-lookup"><span data-stu-id="f3503-104">Extracts coefficient data from a single-channel buffer and adds the data to an [**ID3DXMesh**](id3dxmesh.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3503-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f3503-105">Syntax</span></span>


```C++
HRESULT ExtractToMesh(
  [in] UINT         NumCoefficients,
  [in] D3DDECLUSAGE Usage,
  [in] UINT         UsageIndexStart,
  [in] LPD3DXMESH   pScene
);
```



## <a name="parameters"></a><span data-ttu-id="f3503-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f3503-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3503-107">*НумкоеффиЦиентс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f3503-107">*NumCoefficients* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3503-108">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f3503-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f3503-109">Количество коэффициентов, которые необходимо извлечь из буфера.</span><span class="sxs-lookup"><span data-stu-id="f3503-109">Number of coefficients to extract from the buffer.</span></span> <span data-ttu-id="f3503-110">При использовании радианценого (PRT) предварительно вычисленного коэффициента просчетного гармонического (SH) число коэффективных должно быть Order ².</span><span class="sxs-lookup"><span data-stu-id="f3503-110">When using spherical harmonic (SH) precomputed radiance transfer (PRT), the number of coefficients should be Order ².</span></span> <span data-ttu-id="f3503-111">Порядок должен находиться в диапазоне от [D3DXSH \_ МИНОРДЕР](other-d3dx-constants.md) до D3DXSH \_ максордер, включительно.</span><span class="sxs-lookup"><span data-stu-id="f3503-111">Order must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span>

</dd> <dt>

<span data-ttu-id="f3503-112">*Использование* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f3503-112">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3503-113">Тип: **[ **D3DDECLUSAGE**](./d3ddeclusage.md)**</span><span class="sxs-lookup"><span data-stu-id="f3503-113">Type: **[**D3DDECLUSAGE**](./d3ddeclusage.md)**</span></span>

<span data-ttu-id="f3503-114">Описание использования вершин сетки.</span><span class="sxs-lookup"><span data-stu-id="f3503-114">Vertex usage descriptions of the mesh.</span></span> <span data-ttu-id="f3503-115">См. [**D3DDECLUSAGE**](./d3ddeclusage.md).</span><span class="sxs-lookup"><span data-stu-id="f3503-115">See [**D3DDECLUSAGE**](./d3ddeclusage.md).</span></span>

</dd> <dt>

<span data-ttu-id="f3503-116">*Усажеиндексстарт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f3503-116">*UsageIndexStart* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3503-117">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f3503-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f3503-118">Начальный индекс для коэффициентов хранится в сетке.</span><span class="sxs-lookup"><span data-stu-id="f3503-118">Starting index for coefficients to be stored in the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="f3503-119">*псцене* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f3503-119">*pScene* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3503-120">Тип: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="f3503-120">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="f3503-121">Указатель на объект сетки [**ID3DXMesh**](id3dxmesh.md) , который будет хранить коэффициенты.</span><span class="sxs-lookup"><span data-stu-id="f3503-121">Pointer to an [**ID3DXMesh**](id3dxmesh.md) mesh object that will store coefficients.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3503-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f3503-122">Return value</span></span>

<span data-ttu-id="f3503-123">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f3503-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f3503-124">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="f3503-124">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="f3503-125">В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="f3503-125">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3503-126">Требования</span><span class="sxs-lookup"><span data-stu-id="f3503-126">Requirements</span></span>



| <span data-ttu-id="f3503-127">Требование</span><span class="sxs-lookup"><span data-stu-id="f3503-127">Requirement</span></span> | <span data-ttu-id="f3503-128">Значение</span><span class="sxs-lookup"><span data-stu-id="f3503-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f3503-129">Header</span><span class="sxs-lookup"><span data-stu-id="f3503-129">Header</span></span><br/>  | <dl> <span data-ttu-id="f3503-130"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="f3503-130"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="f3503-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f3503-131">Library</span></span><br/> | <dl> <span data-ttu-id="f3503-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f3503-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f3503-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f3503-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3503-134">ID3DXPRTBuffer</span><span class="sxs-lookup"><span data-stu-id="f3503-134">ID3DXPRTBuffer</span></span>](id3dxprtbuffer.md)
</dt> </dl>

 

 
