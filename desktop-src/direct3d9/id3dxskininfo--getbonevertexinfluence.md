---
description: Извлекает коэффициент смешения и вершину, затрагиваемые указанными костями.
ms.assetid: bbed4766-e571-4a9e-b7e3-047052470cbe
title: 'Метод ID3DXSkinInfo:: Жетбоневертексинфлуенце (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.GetBoneVertexInfluence
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6e3cb7c530ed72a65f9a3e8de6b0735b1a7ae5e4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354073"
---
# <a name="id3dxskininfogetbonevertexinfluence-method"></a><span data-ttu-id="17c26-103">Метод ID3DXSkinInfo:: Жетбоневертексинфлуенце</span><span class="sxs-lookup"><span data-stu-id="17c26-103">ID3DXSkinInfo::GetBoneVertexInfluence method</span></span>

<span data-ttu-id="17c26-104">Извлекает коэффициент смешения и вершину, затрагиваемые указанными костями.</span><span class="sxs-lookup"><span data-stu-id="17c26-104">Retrieves the blend factor and vertex affected by a specified bone influence.</span></span>

## <a name="syntax"></a><span data-ttu-id="17c26-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="17c26-105">Syntax</span></span>


```C++
HRESULT GetBoneVertexInfluence(
  [in]      DWORD boneNum,
  [in]      DWORD influenceNum,
  [in, out] FLOAT *pWeight,
  [in, out] DWORD *pVertexNum
);
```



## <a name="parameters"></a><span data-ttu-id="17c26-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="17c26-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17c26-107">*боненум* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="17c26-107">*boneNum* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17c26-108">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="17c26-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="17c26-109">Индекс кости.</span><span class="sxs-lookup"><span data-stu-id="17c26-109">Index of the bone.</span></span> <span data-ttu-id="17c26-110">Значение должно находиться в диапазоне от 0 до количества костей.</span><span class="sxs-lookup"><span data-stu-id="17c26-110">Must be between 0 and the number of bones.</span></span>

</dd> <dt>

<span data-ttu-id="17c26-111">*инфлуенценум* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="17c26-111">*influenceNum* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17c26-112">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="17c26-112">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="17c26-113">Индекс массива влияния указанной кости.</span><span class="sxs-lookup"><span data-stu-id="17c26-113">Index of the influence array of the specified bone.</span></span>

</dd> <dt>

<span data-ttu-id="17c26-114">*пвеигхт* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="17c26-114">*pWeight* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="17c26-115">Тип: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="17c26-115">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="17c26-116">Указатель на коэффициент смешения, на который влияет Инфлуенценум.</span><span class="sxs-lookup"><span data-stu-id="17c26-116">Pointer to the blend factor influenced by influenceNum.</span></span>

</dd> <dt>

<span data-ttu-id="17c26-117">*пвертекснум* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="17c26-117">*pVertexNum* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="17c26-118">Тип: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="17c26-118">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="17c26-119">Указатель на вершину, на которую влияет Инфлуенценум.</span><span class="sxs-lookup"><span data-stu-id="17c26-119">Pointer to the vertex influenced by influenceNum.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17c26-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="17c26-120">Return value</span></span>

<span data-ttu-id="17c26-121">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="17c26-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="17c26-122">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="17c26-122">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="17c26-123">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="17c26-123">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="17c26-124">Требования</span><span class="sxs-lookup"><span data-stu-id="17c26-124">Requirements</span></span>



| <span data-ttu-id="17c26-125">Требование</span><span class="sxs-lookup"><span data-stu-id="17c26-125">Requirement</span></span> | <span data-ttu-id="17c26-126">Значение</span><span class="sxs-lookup"><span data-stu-id="17c26-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="17c26-127">Header</span><span class="sxs-lookup"><span data-stu-id="17c26-127">Header</span></span><br/>  | <dl> <span data-ttu-id="17c26-128"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="17c26-128"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="17c26-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="17c26-129">Library</span></span><br/> | <dl> <span data-ttu-id="17c26-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="17c26-130"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="17c26-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="17c26-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17c26-132">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="17c26-132">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> <dt>

[<span data-ttu-id="17c26-133">**ID3DXSkinInfo:: Сетбоневертексинфлуенце**</span><span class="sxs-lookup"><span data-stu-id="17c26-133">**ID3DXSkinInfo::SetBoneVertexInfluence**</span></span>](id3dxskininfo--setbonevertexinfluence.md)
</dt> <dt>

[<span data-ttu-id="17c26-134">**ID3DXSkinInfo:: Финдбоневертексинфлуенцеиндекс**</span><span class="sxs-lookup"><span data-stu-id="17c26-134">**ID3DXSkinInfo::FindBoneVertexInfluenceIndex**</span></span>](id3dxskininfo--findbonevertexinfluenceindex.md)
</dt> <dt>

[<span data-ttu-id="17c26-135">**ID3DXSkinInfo:: Жетбонеинфлуенце**</span><span class="sxs-lookup"><span data-stu-id="17c26-135">**ID3DXSkinInfo::GetBoneInfluence**</span></span>](id3dxskininfo--getboneinfluence.md)
</dt> </dl>

 

 
