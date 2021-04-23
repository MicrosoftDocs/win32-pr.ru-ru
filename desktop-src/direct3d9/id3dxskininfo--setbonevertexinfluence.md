---
description: Задает значение влияния кости на одну вершину.
ms.assetid: 9283866f-3dfe-467d-a74f-77e89c2778c4
title: 'Метод ID3DXSkinInfo:: Сетбоневертексинфлуенце (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.SetBoneVertexInfluence
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: db84cdf9a1647bc5302c421e52d50f812e74596e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703626"
---
# <a name="id3dxskininfosetbonevertexinfluence-method"></a><span data-ttu-id="85535-103">Метод ID3DXSkinInfo:: Сетбоневертексинфлуенце</span><span class="sxs-lookup"><span data-stu-id="85535-103">ID3DXSkinInfo::SetBoneVertexInfluence method</span></span>

<span data-ttu-id="85535-104">Задает значение влияния кости на одну вершину.</span><span class="sxs-lookup"><span data-stu-id="85535-104">Sets an influence value of a bone on a single vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="85535-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="85535-105">Syntax</span></span>


```C++
HRESULT SetBoneVertexInfluence(
  [in] DWORD boneNum,
  [in] DWORD influenceNum,
  [in] FLOAT weight
);
```



## <a name="parameters"></a><span data-ttu-id="85535-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="85535-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85535-107">*боненум* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="85535-107">*boneNum* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85535-108">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="85535-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="85535-109">Индекс кости.</span><span class="sxs-lookup"><span data-stu-id="85535-109">Index of the bone.</span></span> <span data-ttu-id="85535-110">Значение должно находиться в диапазоне от 0 до количества костей.</span><span class="sxs-lookup"><span data-stu-id="85535-110">Must be between 0 and the number of bones.</span></span>

</dd> <dt>

<span data-ttu-id="85535-111">*инфлуенценум* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="85535-111">*influenceNum* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85535-112">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="85535-112">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="85535-113">Индекс массива влияния указанной кости.</span><span class="sxs-lookup"><span data-stu-id="85535-113">Index of the influence array of the specified bone.</span></span>

</dd> <dt>

<span data-ttu-id="85535-114">*вес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="85535-114">*weight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85535-115">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="85535-115">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="85535-116">Влияние коэффициента смешения на указанную кость.</span><span class="sxs-lookup"><span data-stu-id="85535-116">Blend factor of the specified bone influence.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85535-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="85535-117">Return value</span></span>

<span data-ttu-id="85535-118">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="85535-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="85535-119">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="85535-119">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="85535-120">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="85535-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="85535-121">Требования</span><span class="sxs-lookup"><span data-stu-id="85535-121">Requirements</span></span>



| <span data-ttu-id="85535-122">Требование</span><span class="sxs-lookup"><span data-stu-id="85535-122">Requirement</span></span> | <span data-ttu-id="85535-123">Значение</span><span class="sxs-lookup"><span data-stu-id="85535-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="85535-124">Header</span><span class="sxs-lookup"><span data-stu-id="85535-124">Header</span></span><br/>  | <dl> <span data-ttu-id="85535-125"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="85535-125"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="85535-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="85535-126">Library</span></span><br/> | <dl> <span data-ttu-id="85535-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="85535-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="85535-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="85535-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85535-129">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="85535-129">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> <dt>

[<span data-ttu-id="85535-130">**ID3DXSkinInfo:: Жетбоневертексинфлуенце**</span><span class="sxs-lookup"><span data-stu-id="85535-130">**ID3DXSkinInfo::GetBoneVertexInfluence**</span></span>](id3dxskininfo--getbonevertexinfluence.md)
</dt> <dt>

[<span data-ttu-id="85535-131">**ID3DXSkinInfo:: Финдбоневертексинфлуенцеиндекс**</span><span class="sxs-lookup"><span data-stu-id="85535-131">**ID3DXSkinInfo::FindBoneVertexInfluenceIndex**</span></span>](id3dxskininfo--findbonevertexinfluenceindex.md)
</dt> <dt>

[<span data-ttu-id="85535-132">**ID3DXSkinInfo:: Жетбонеинфлуенце**</span><span class="sxs-lookup"><span data-stu-id="85535-132">**ID3DXSkinInfo::GetBoneInfluence**</span></span>](id3dxskininfo--getboneinfluence.md)
</dt> </dl>

 

 
