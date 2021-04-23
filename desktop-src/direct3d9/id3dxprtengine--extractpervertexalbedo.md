---
description: Копирует значения албедо на уровне вершины из сетки.
ms.assetid: 3a6f1cc2-a870-4463-98df-599d9fbd9d78
title: 'Метод ID3DXPRTEngine:: Екстрактпервертексалбедо (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ExtractPerVertexAlbedo
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ed23b75b3113421b6242f49416e4b54bfce336f4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104000496"
---
# <a name="id3dxprtengineextractpervertexalbedo-method"></a><span data-ttu-id="f4ff7-103">Метод ID3DXPRTEngine:: Екстрактпервертексалбедо</span><span class="sxs-lookup"><span data-stu-id="f4ff7-103">ID3DXPRTEngine::ExtractPerVertexAlbedo method</span></span>

<span data-ttu-id="f4ff7-104">Копирует значения албедо на уровне вершины из сетки.</span><span class="sxs-lookup"><span data-stu-id="f4ff7-104">Copies per-vertex albedo values from a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4ff7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f4ff7-105">Syntax</span></span>


```C++
HRESULT ExtractPerVertexAlbedo(
  [in] LPD3DXMESH   pMesh,
  [in] D3DDECLUSAGE Usage,
  [in] UINT         NumChanIn
);
```



## <a name="parameters"></a><span data-ttu-id="f4ff7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f4ff7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4ff7-107">*пмеш* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f4ff7-107">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f4ff7-108">Тип: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="f4ff7-108">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="f4ff7-109">Указатель на объект сетки [**ID3DXMesh**](id3dxmesh.md) , используемый в [**D3DXCreatePRTEngine**](d3dxcreateprtengine.md) для создания объекта [**ID3DXPRTEngine**](id3dxprtengine.md) .</span><span class="sxs-lookup"><span data-stu-id="f4ff7-109">Pointer to the [**ID3DXMesh**](id3dxmesh.md) mesh object used in [**D3DXCreatePRTEngine**](d3dxcreateprtengine.md) to create the [**ID3DXPRTEngine**](id3dxprtengine.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="f4ff7-110">*Использование* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f4ff7-110">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f4ff7-111">Тип: **[ **D3DDECLUSAGE**](./d3ddeclusage.md)**</span><span class="sxs-lookup"><span data-stu-id="f4ff7-111">Type: **[**D3DDECLUSAGE**](./d3ddeclusage.md)**</span></span>

<span data-ttu-id="f4ff7-112">Описания использования вершин для копирования из сетки.</span><span class="sxs-lookup"><span data-stu-id="f4ff7-112">Vertex usage descriptions to copy from the mesh.</span></span> <span data-ttu-id="f4ff7-113">См. [**D3DDECLUSAGE**](./d3ddeclusage.md).</span><span class="sxs-lookup"><span data-stu-id="f4ff7-113">See [**D3DDECLUSAGE**](./d3ddeclusage.md).</span></span>

</dd> <dt>

<span data-ttu-id="f4ff7-114">*Нумчанин* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f4ff7-114">*NumChanIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f4ff7-115">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f4ff7-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f4ff7-116">Число цветовых каналов для копирования из сетки.</span><span class="sxs-lookup"><span data-stu-id="f4ff7-116">Number of color channels to copy from the mesh.</span></span> <span data-ttu-id="f4ff7-117">Задайте значение 1, чтобы указать серые материалы (R = G = B), или 3, чтобы включить эффекты цвета суперсовременные.</span><span class="sxs-lookup"><span data-stu-id="f4ff7-117">Set to 1 to specify gray materials (R = G = B), or 3 to enable color bleeding effects.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f4ff7-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f4ff7-118">Return value</span></span>

<span data-ttu-id="f4ff7-119">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f4ff7-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f4ff7-120">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="f4ff7-120">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="f4ff7-121">В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="f4ff7-121">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4ff7-122">Требования</span><span class="sxs-lookup"><span data-stu-id="f4ff7-122">Requirements</span></span>



| <span data-ttu-id="f4ff7-123">Требование</span><span class="sxs-lookup"><span data-stu-id="f4ff7-123">Requirement</span></span> | <span data-ttu-id="f4ff7-124">Значение</span><span class="sxs-lookup"><span data-stu-id="f4ff7-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f4ff7-125">Header</span><span class="sxs-lookup"><span data-stu-id="f4ff7-125">Header</span></span><br/>  | <dl> <span data-ttu-id="f4ff7-126"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="f4ff7-126"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="f4ff7-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f4ff7-127">Library</span></span><br/> | <dl> <span data-ttu-id="f4ff7-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f4ff7-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f4ff7-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f4ff7-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4ff7-130">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="f4ff7-130">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> </dl>

 

 
