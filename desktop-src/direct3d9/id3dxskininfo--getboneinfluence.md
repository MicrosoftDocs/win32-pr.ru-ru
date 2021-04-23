---
description: Возвращает вершины и весовые коэффициенты, влияющие на кость.
ms.assetid: 84cb064b-b6b2-402d-81cc-8c02de6f8b52
title: 'Метод ID3DXSkinInfo:: Жетбонеинфлуенце (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.GetBoneInfluence
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8b4b31ab08aca476ced1cb28dfc5ed5bfe61d044
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713451"
---
# <a name="id3dxskininfogetboneinfluence-method"></a><span data-ttu-id="5392f-103">Метод ID3DXSkinInfo:: Жетбонеинфлуенце</span><span class="sxs-lookup"><span data-stu-id="5392f-103">ID3DXSkinInfo::GetBoneInfluence method</span></span>

<span data-ttu-id="5392f-104">Возвращает вершины и весовые коэффициенты, влияющие на кость.</span><span class="sxs-lookup"><span data-stu-id="5392f-104">Gets the vertices and weights that a bone influences.</span></span>

## <a name="syntax"></a><span data-ttu-id="5392f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5392f-105">Syntax</span></span>


```C++
HRESULT GetBoneInfluence(
  [in]      DWORD Bone,
  [in, out] DWORD *vertices,
  [in, out] FLOAT *weights
);
```



## <a name="parameters"></a><span data-ttu-id="5392f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5392f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5392f-107">*Кость* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5392f-107">*Bone* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5392f-108">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5392f-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5392f-109">Номер кости.</span><span class="sxs-lookup"><span data-stu-id="5392f-109">Bone number.</span></span>

</dd> <dt>

<span data-ttu-id="5392f-110">*вершины* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="5392f-110">*vertices* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="5392f-111">Тип: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="5392f-111">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="5392f-112">Получение массива вершин, на которые влияет кость.</span><span class="sxs-lookup"><span data-stu-id="5392f-112">Get the array of vertices influenced by a bone.</span></span>

</dd> <dt>

<span data-ttu-id="5392f-113">*весовые коэффициенты* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="5392f-113">*weights* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="5392f-114">Тип: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="5392f-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="5392f-115">Получение массива весов, на которые влияет кость.</span><span class="sxs-lookup"><span data-stu-id="5392f-115">Get the array of weights influenced by a bone.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5392f-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5392f-116">Return value</span></span>

<span data-ttu-id="5392f-117">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5392f-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5392f-118">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="5392f-118">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="5392f-119">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="5392f-119">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="5392f-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5392f-120">Remarks</span></span>

<span data-ttu-id="5392f-121">Используйте [**ID3DXSkinInfo:: жетнумбонеинфлуенцес**](id3dxskininfo--getnumboneinfluences.md) , чтобы узнать, сколько вершин влияет на кость.</span><span class="sxs-lookup"><span data-stu-id="5392f-121">Use [**ID3DXSkinInfo::GetNumBoneInfluences**](id3dxskininfo--getnumboneinfluences.md) to find out how many vertices the bone influences.</span></span>

## <a name="requirements"></a><span data-ttu-id="5392f-122">Требования</span><span class="sxs-lookup"><span data-stu-id="5392f-122">Requirements</span></span>



| <span data-ttu-id="5392f-123">Требование</span><span class="sxs-lookup"><span data-stu-id="5392f-123">Requirement</span></span> | <span data-ttu-id="5392f-124">Значение</span><span class="sxs-lookup"><span data-stu-id="5392f-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5392f-125">Header</span><span class="sxs-lookup"><span data-stu-id="5392f-125">Header</span></span><br/>  | <dl> <span data-ttu-id="5392f-126"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="5392f-126"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="5392f-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5392f-127">Library</span></span><br/> | <dl> <span data-ttu-id="5392f-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5392f-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5392f-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5392f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5392f-130">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="5392f-130">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> <dt>

[<span data-ttu-id="5392f-131">**ID3DXSkinInfo:: Сетбонеинфлуенце**</span><span class="sxs-lookup"><span data-stu-id="5392f-131">**ID3DXSkinInfo::SetBoneInfluence**</span></span>](id3dxskininfo--setboneinfluence.md)
</dt> </dl>

 

 
