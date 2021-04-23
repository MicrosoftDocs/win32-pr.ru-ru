---
description: Извлекает индекс кости, влияющей на одну вершину.
ms.assetid: vs|directx_sdk|~\id3dxskininfo__findbonevertexinfluenceindex.htm
title: 'Метод ID3DXSkinInfo:: Финдбоневертексинфлуенцеиндекс (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.FindBoneVertexInfluenceIndex
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 05a86e98e5001092700fdec12f2a7afc33ddf082
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713452"
---
# <a name="id3dxskininfofindbonevertexinfluenceindex-method"></a><span data-ttu-id="ba3ae-103">Метод ID3DXSkinInfo:: Финдбоневертексинфлуенцеиндекс</span><span class="sxs-lookup"><span data-stu-id="ba3ae-103">ID3DXSkinInfo::FindBoneVertexInfluenceIndex method</span></span>

<span data-ttu-id="ba3ae-104">Извлекает индекс кости, влияющей на одну вершину.</span><span class="sxs-lookup"><span data-stu-id="ba3ae-104">Retrieves the index of the bone influence affecting a single vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba3ae-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ba3ae-105">Syntax</span></span>


```C++
HRESULT FindBoneVertexInfluenceIndex(
  [in]      DWORD boneNum,
  [in]      DWORD vertexNum,
  [in, out] DWORD *pInfluenceIndex
);
```



## <a name="parameters"></a><span data-ttu-id="ba3ae-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ba3ae-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba3ae-107">*боненум* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ba3ae-107">*boneNum* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba3ae-108">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ba3ae-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ba3ae-109">Индекс кости.</span><span class="sxs-lookup"><span data-stu-id="ba3ae-109">Index of the bone.</span></span> <span data-ttu-id="ba3ae-110">Значение должно находиться в диапазоне от 0 до количества костей.</span><span class="sxs-lookup"><span data-stu-id="ba3ae-110">Must be between 0 and the number of bones.</span></span>

</dd> <dt>

<span data-ttu-id="ba3ae-111">*вертекснум* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ba3ae-111">*vertexNum* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba3ae-112">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ba3ae-112">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ba3ae-113">Индекс вершины, для которого влияет влияние на кость.</span><span class="sxs-lookup"><span data-stu-id="ba3ae-113">Index of the vertex for which the bone influence is to be found.</span></span> <span data-ttu-id="ba3ae-114">Значение должно находиться в диапазоне от 0 до количества вершин в сетке.</span><span class="sxs-lookup"><span data-stu-id="ba3ae-114">Must be between 0 and the number of vertices in the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="ba3ae-115">*пинфлуенцеиндекс* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="ba3ae-115">*pInfluenceIndex* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ba3ae-116">Тип: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="ba3ae-116">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="ba3ae-117">Указатель на индекс влияния на кость, влияющих на Вертекснум.</span><span class="sxs-lookup"><span data-stu-id="ba3ae-117">Pointer to the index of the bone influence that affects vertexNum.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba3ae-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ba3ae-118">Return value</span></span>

<span data-ttu-id="ba3ae-119">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ba3ae-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ba3ae-120">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="ba3ae-120">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="ba3ae-121">Если указанная кость не влияет на данную вершину, \_ возвращается значение false.</span><span class="sxs-lookup"><span data-stu-id="ba3ae-121">If the specified bone does not influence the given vertex, S\_FALSE is returned.</span></span> <span data-ttu-id="ba3ae-122">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="ba3ae-122">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba3ae-123">Требования</span><span class="sxs-lookup"><span data-stu-id="ba3ae-123">Requirements</span></span>



| <span data-ttu-id="ba3ae-124">Требование</span><span class="sxs-lookup"><span data-stu-id="ba3ae-124">Requirement</span></span> | <span data-ttu-id="ba3ae-125">Значение</span><span class="sxs-lookup"><span data-stu-id="ba3ae-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ba3ae-126">Header</span><span class="sxs-lookup"><span data-stu-id="ba3ae-126">Header</span></span><br/>  | <dl> <span data-ttu-id="ba3ae-127"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="ba3ae-127"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="ba3ae-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ba3ae-128">Library</span></span><br/> | <dl> <span data-ttu-id="ba3ae-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ba3ae-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ba3ae-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ba3ae-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba3ae-131">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="ba3ae-131">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> <dt>

[<span data-ttu-id="ba3ae-132">**ID3DXSkinInfo:: Жетбоневертексинфлуенце**</span><span class="sxs-lookup"><span data-stu-id="ba3ae-132">**ID3DXSkinInfo::GetBoneVertexInfluence**</span></span>](id3dxskininfo--getbonevertexinfluence.md)
</dt> <dt>

[<span data-ttu-id="ba3ae-133">**ID3DXSkinInfo:: Сетбоневертексинфлуенце**</span><span class="sxs-lookup"><span data-stu-id="ba3ae-133">**ID3DXSkinInfo::SetBoneVertexInfluence**</span></span>](id3dxskininfo--setbonevertexinfluence.md)
</dt> <dt>

[<span data-ttu-id="ba3ae-134">**ID3DXSkinInfo:: Жетбонеинфлуенце**</span><span class="sxs-lookup"><span data-stu-id="ba3ae-134">**ID3DXSkinInfo::GetBoneInfluence**</span></span>](id3dxskininfo--getboneinfluence.md)
</dt> </dl>

 

 
