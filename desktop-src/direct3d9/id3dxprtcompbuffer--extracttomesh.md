---
description: Извлекает коэффициенты проекции на основе анализа основных компонентов (PCA) из буфера сжатых данных ID3DXPRTCompBuffer и добавляет их в объект ID3DXMesh.
ms.assetid: 0680d626-f07a-43d3-acb9-e8db82b5e933
title: 'Метод ID3DXPRTCompBuffer:: Екстракттомеш (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTCompBuffer.ExtractToMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 607b583b89358d2d28030a4187b1608174d849c0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703689"
---
# <a name="id3dxprtcompbufferextracttomesh-method"></a><span data-ttu-id="215b4-103">Метод ID3DXPRTCompBuffer:: Екстракттомеш</span><span class="sxs-lookup"><span data-stu-id="215b4-103">ID3DXPRTCompBuffer::ExtractToMesh method</span></span>

<span data-ttu-id="215b4-104">Извлекает коэффициенты проекции на основе анализа основных компонентов (PCA) из буфера сжатых данных [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) и добавляет их в объект [**ID3DXMesh**](id3dxmesh.md) .</span><span class="sxs-lookup"><span data-stu-id="215b4-104">Extracts the per-sample principal component analysis (PCA) projection coefficients from an [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) compressed data buffer and adds the data to an [**ID3DXMesh**](id3dxmesh.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="215b4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="215b4-105">Syntax</span></span>


```C++
HRESULT ExtractToMesh(
  [in] UINT         NumPCA,
  [in] D3DDECLUSAGE Usage,
  [in] UINT         UsageIndexStart,
  [in] LPD3DXMESH   pScene
);
```



## <a name="parameters"></a><span data-ttu-id="215b4-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="215b4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="215b4-107">*Нумпка* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="215b4-107">*NumPCA* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="215b4-108">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="215b4-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="215b4-109">Количество коэффициентов PCA для извлечения из буфера.</span><span class="sxs-lookup"><span data-stu-id="215b4-109">Number of PCA coefficients to extract from the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="215b4-110">*Использование* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="215b4-110">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="215b4-111">Тип: **[ **D3DDECLUSAGE**](./d3ddeclusage.md)**</span><span class="sxs-lookup"><span data-stu-id="215b4-111">Type: **[**D3DDECLUSAGE**](./d3ddeclusage.md)**</span></span>

<span data-ttu-id="215b4-112">Описание использования вершин сетки.</span><span class="sxs-lookup"><span data-stu-id="215b4-112">Vertex usage descriptions of the mesh.</span></span> <span data-ttu-id="215b4-113">См. [**D3DDECLUSAGE**](./d3ddeclusage.md).</span><span class="sxs-lookup"><span data-stu-id="215b4-113">See [**D3DDECLUSAGE**](./d3ddeclusage.md).</span></span>

</dd> <dt>

<span data-ttu-id="215b4-114">*Усажеиндексстарт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="215b4-114">*UsageIndexStart* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="215b4-115">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="215b4-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="215b4-116">Начальный индекс для коэффициентов PCA должен храниться в сетке.</span><span class="sxs-lookup"><span data-stu-id="215b4-116">Starting index for PCA coefficients to be stored in the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="215b4-117">*псцене* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="215b4-117">*pScene* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="215b4-118">Тип: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="215b4-118">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="215b4-119">Указатель на объект сетки [**ID3DXMesh**](id3dxmesh.md) , в котором будут храниться коэффициенты PCA.</span><span class="sxs-lookup"><span data-stu-id="215b4-119">Pointer to an [**ID3DXMesh**](id3dxmesh.md) mesh object that will store PCA coefficients.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="215b4-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="215b4-120">Return value</span></span>

<span data-ttu-id="215b4-121">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="215b4-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="215b4-122">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="215b4-122">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="215b4-123">В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="215b4-123">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="215b4-124">Требования</span><span class="sxs-lookup"><span data-stu-id="215b4-124">Requirements</span></span>



| <span data-ttu-id="215b4-125">Требование</span><span class="sxs-lookup"><span data-stu-id="215b4-125">Requirement</span></span> | <span data-ttu-id="215b4-126">Значение</span><span class="sxs-lookup"><span data-stu-id="215b4-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="215b4-127">Header</span><span class="sxs-lookup"><span data-stu-id="215b4-127">Header</span></span><br/>  | <dl> <span data-ttu-id="215b4-128"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="215b4-128"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="215b4-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="215b4-129">Library</span></span><br/> | <dl> <span data-ttu-id="215b4-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="215b4-130"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="215b4-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="215b4-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="215b4-132">ID3DXPRTCompBuffer</span><span class="sxs-lookup"><span data-stu-id="215b4-132">ID3DXPRTCompBuffer</span></span>](id3dxprtcompbuffer.md)
</dt> </dl>

 

 
