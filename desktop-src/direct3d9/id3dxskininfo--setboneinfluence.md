---
description: Задает значение влияния для кости.
ms.assetid: c6dc8a33-8f5c-47d0-8637-a2492b1e3089
title: 'Метод ID3DXSkinInfo:: Сетбонеинфлуенце (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.SetBoneInfluence
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 16ed3514c986dee89f964074d18a646bcf3a1249
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713449"
---
# <a name="id3dxskininfosetboneinfluence-method"></a><span data-ttu-id="fcaf3-103">Метод ID3DXSkinInfo:: Сетбонеинфлуенце</span><span class="sxs-lookup"><span data-stu-id="fcaf3-103">ID3DXSkinInfo::SetBoneInfluence method</span></span>

<span data-ttu-id="fcaf3-104">Задает значение влияния для кости.</span><span class="sxs-lookup"><span data-stu-id="fcaf3-104">Sets the influence value for a bone.</span></span>

## <a name="syntax"></a><span data-ttu-id="fcaf3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fcaf3-105">Syntax</span></span>


```C++
HRESULT SetBoneInfluence(
  [in]       DWORD Bone,
  [in]       DWORD numInfluences,
  [in] const DWORD *vertices,
  [in] const FLOAT *weights
);
```



## <a name="parameters"></a><span data-ttu-id="fcaf3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="fcaf3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fcaf3-107">*Кость* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fcaf3-107">*Bone* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fcaf3-108">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fcaf3-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fcaf3-109">Номер кости.</span><span class="sxs-lookup"><span data-stu-id="fcaf3-109">Bone number.</span></span>

</dd> <dt>

<span data-ttu-id="fcaf3-110">*нуминфлуенцес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fcaf3-110">*numInfluences* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fcaf3-111">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fcaf3-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fcaf3-112">Количество повлияет на.</span><span class="sxs-lookup"><span data-stu-id="fcaf3-112">Number of influences.</span></span>

</dd> <dt>

<span data-ttu-id="fcaf3-113">*вершины* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fcaf3-113">*vertices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fcaf3-114">Тип: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="fcaf3-114">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="fcaf3-115">Массив вершин, на которые влияет кость.</span><span class="sxs-lookup"><span data-stu-id="fcaf3-115">The array of vertices influenced by a bone.</span></span>

</dd> <dt>

<span data-ttu-id="fcaf3-116">*весовые коэффициенты* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fcaf3-116">*weights* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fcaf3-117">Тип: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="fcaf3-117">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="fcaf3-118">Массив весов, на которые влияет кость.</span><span class="sxs-lookup"><span data-stu-id="fcaf3-118">The array of weights influenced by a bone.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fcaf3-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fcaf3-119">Return value</span></span>

<span data-ttu-id="fcaf3-120">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fcaf3-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fcaf3-121">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="fcaf3-121">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="fcaf3-122">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="fcaf3-122">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="fcaf3-123">Требования</span><span class="sxs-lookup"><span data-stu-id="fcaf3-123">Requirements</span></span>



| <span data-ttu-id="fcaf3-124">Требование</span><span class="sxs-lookup"><span data-stu-id="fcaf3-124">Requirement</span></span> | <span data-ttu-id="fcaf3-125">Значение</span><span class="sxs-lookup"><span data-stu-id="fcaf3-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fcaf3-126">Header</span><span class="sxs-lookup"><span data-stu-id="fcaf3-126">Header</span></span><br/>  | <dl> <span data-ttu-id="fcaf3-127"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="fcaf3-127"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="fcaf3-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="fcaf3-128">Library</span></span><br/> | <dl> <span data-ttu-id="fcaf3-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fcaf3-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="fcaf3-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fcaf3-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fcaf3-131">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="fcaf3-131">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> <dt>

[<span data-ttu-id="fcaf3-132">**ID3DXSkinInfo:: Жетбонеинфлуенце**</span><span class="sxs-lookup"><span data-stu-id="fcaf3-132">**ID3DXSkinInfo::GetBoneInfluence**</span></span>](id3dxskininfo--getboneinfluence.md)
</dt> <dt>

[<span data-ttu-id="fcaf3-133">**ID3DXSkinInfo:: Жетнумбонеинфлуенцес**</span><span class="sxs-lookup"><span data-stu-id="fcaf3-133">**ID3DXSkinInfo::GetNumBoneInfluences**</span></span>](id3dxskininfo--getnumboneinfluences.md)
</dt> </dl>

 

 
