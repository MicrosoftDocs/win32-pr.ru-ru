---
description: Обновляет сведения, влияющие на кости, для сопоставления вершин после их переупорядочивания. Этот метод должен вызываться, если целевой буфер вершин был изменен заказа извне.
ms.assetid: bff5229f-e547-4ab3-84c6-58b15a7825e9
title: 'Метод ID3DXSkinInfo:: пересопоставления (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.Remap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 657cf0977592a8e19e68b8aeb950c62d404e7cdb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694080"
---
# <a name="id3dxskininforemap-method"></a><span data-ttu-id="3bbdf-104">Метод ID3DXSkinInfo:: пересопоставления</span><span class="sxs-lookup"><span data-stu-id="3bbdf-104">ID3DXSkinInfo::Remap method</span></span>

<span data-ttu-id="3bbdf-105">Обновляет сведения, влияющие на кости, для сопоставления вершин после их переупорядочивания.</span><span class="sxs-lookup"><span data-stu-id="3bbdf-105">Updates bone influence information to match vertices after they are reordered.</span></span> <span data-ttu-id="3bbdf-106">Этот метод должен вызываться, если целевой буфер вершин был изменен заказа извне.</span><span class="sxs-lookup"><span data-stu-id="3bbdf-106">This method should be called if the target vertex buffer has been reordered externally.</span></span>

## <a name="syntax"></a><span data-ttu-id="3bbdf-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3bbdf-107">Syntax</span></span>


```C++
HRESULT Remap(
  [in] DWORD NumVertices,
  [in] DWORD *pVertexRemap
);
```



## <a name="parameters"></a><span data-ttu-id="3bbdf-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="3bbdf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3bbdf-109">*Нумвертицес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3bbdf-109">*NumVertices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3bbdf-110">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3bbdf-110">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3bbdf-111">Число вершин для повторного сопоставления.</span><span class="sxs-lookup"><span data-stu-id="3bbdf-111">Number of vertices to remap.</span></span>

</dd> <dt>

<span data-ttu-id="3bbdf-112">*пвертексремап* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3bbdf-112">*pVertexRemap* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3bbdf-113">Тип: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="3bbdf-113">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="3bbdf-114">Массив DWORD, длина которого задается параметром Нумвертицес.</span><span class="sxs-lookup"><span data-stu-id="3bbdf-114">Array of DWORDS whose length is specified by NumVertices.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3bbdf-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3bbdf-115">Return value</span></span>

<span data-ttu-id="3bbdf-116">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3bbdf-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3bbdf-117">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="3bbdf-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="3bbdf-118">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="3bbdf-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="3bbdf-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3bbdf-119">Remarks</span></span>

<span data-ttu-id="3bbdf-120">Каждый элемент в Пвертексремап указывает предыдущий индекс вершины для этой позиции.</span><span class="sxs-lookup"><span data-stu-id="3bbdf-120">Each element in pVertexRemap specifies the previous vertex index for that position.</span></span> <span data-ttu-id="3bbdf-121">Например, если вершина находится в положении 3, но была повторно сопоставлена с позицией 5, то Пятый элемент Пвертексремап должен содержать 3.</span><span class="sxs-lookup"><span data-stu-id="3bbdf-121">For example, if a vertex was in position 3 but has been remapped to position 5, then the fifth element of pVertexRemap should contain 3.</span></span> <span data-ttu-id="3bbdf-122">Можно использовать массив сопоставления вершин, возвращаемый [**ID3DXMesh:: optimize**](id3dxmesh--optimize.md) .</span><span class="sxs-lookup"><span data-stu-id="3bbdf-122">The vertex remap array returned by [**ID3DXMesh::Optimize**](id3dxmesh--optimize.md) can be used.</span></span>

## <a name="requirements"></a><span data-ttu-id="3bbdf-123">Требования</span><span class="sxs-lookup"><span data-stu-id="3bbdf-123">Requirements</span></span>



| <span data-ttu-id="3bbdf-124">Требование</span><span class="sxs-lookup"><span data-stu-id="3bbdf-124">Requirement</span></span> | <span data-ttu-id="3bbdf-125">Значение</span><span class="sxs-lookup"><span data-stu-id="3bbdf-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3bbdf-126">Header</span><span class="sxs-lookup"><span data-stu-id="3bbdf-126">Header</span></span><br/>  | <dl> <span data-ttu-id="3bbdf-127"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="3bbdf-127"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="3bbdf-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="3bbdf-128">Library</span></span><br/> | <dl> <span data-ttu-id="3bbdf-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3bbdf-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="3bbdf-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3bbdf-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3bbdf-131">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="3bbdf-131">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> </dl>

 

 
