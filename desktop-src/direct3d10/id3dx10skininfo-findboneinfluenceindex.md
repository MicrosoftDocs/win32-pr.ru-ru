---
description: Найдите индекс, указывающий, где заданная вершина находится в списке заданных вершин на заданной кости.
ms.assetid: vs|directx_sdk|~\id3dx10skininfo_findboneinfluenceindex.htm
title: 'Метод ID3DX10SkinInfo:: Финдбонеинфлуенцеиндекс (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.FindBoneInfluenceIndex
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 1468fed3c0cf999e7635ba0f5ae53cee72fe70c6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273871"
---
# <a name="id3dx10skininfofindboneinfluenceindex-method"></a><span data-ttu-id="69f02-103">Метод ID3DX10SkinInfo:: Финдбонеинфлуенцеиндекс</span><span class="sxs-lookup"><span data-stu-id="69f02-103">ID3DX10SkinInfo::FindBoneInfluenceIndex method</span></span>

<span data-ttu-id="69f02-104">Найдите индекс, указывающий, где заданная вершина находится в списке заданных вершин на заданной кости.</span><span class="sxs-lookup"><span data-stu-id="69f02-104">Find the index that indicates where a given vertex is in a given bone's list of influenced vertices.</span></span>

## <a name="syntax"></a><span data-ttu-id="69f02-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="69f02-105">Syntax</span></span>


```C++
HRESULT FindBoneInfluenceIndex(
  [in] UINT BoneIndex,
  [in] UINT VertexIndex,
  [in] UINT *pInfluenceIndex
);
```



## <a name="parameters"></a><span data-ttu-id="69f02-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="69f02-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69f02-107">*Бонеиндекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="69f02-107">*BoneIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69f02-108">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="69f02-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="69f02-109">Индекс, указывающий существующую кость.</span><span class="sxs-lookup"><span data-stu-id="69f02-109">An index that specifies an existing bone.</span></span> <span data-ttu-id="69f02-110">Значение должно находиться в диапазоне от 0 до значения, возвращаемого [**ID3DX10SkinInfo:: жетнумбонес**](id3dx10skininfo-getnumbones.md).</span><span class="sxs-lookup"><span data-stu-id="69f02-110">Must be between 0 and the value returned by [**ID3DX10SkinInfo::GetNumBones**](id3dx10skininfo-getnumbones.md).</span></span>

</dd> <dt>

<span data-ttu-id="69f02-111">*Вертексиндекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="69f02-111">*VertexIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69f02-112">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="69f02-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="69f02-113">Индекс вершины в буфере вершин.</span><span class="sxs-lookup"><span data-stu-id="69f02-113">The index of the vertex in the vertex buffer.</span></span>

</dd> <dt>

<span data-ttu-id="69f02-114">*пинфлуенцеиндекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="69f02-114">*pInfluenceIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69f02-115">Тип: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="69f02-115">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="69f02-116">Индекс вершины в списке завлияния вершин.</span><span class="sxs-lookup"><span data-stu-id="69f02-116">The index of the vertex in the bone's list of influenced vertices.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69f02-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="69f02-117">Return value</span></span>

<span data-ttu-id="69f02-118">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="69f02-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="69f02-119">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="69f02-119">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="69f02-120">Если метод завершается со сбоем, возвращаемое значение может быть следующим: E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="69f02-120">If the method fails, the return value can be: E\_INVALIDARG.</span></span>

## <a name="requirements"></a><span data-ttu-id="69f02-121">Требования</span><span class="sxs-lookup"><span data-stu-id="69f02-121">Requirements</span></span>



| <span data-ttu-id="69f02-122">Требование</span><span class="sxs-lookup"><span data-stu-id="69f02-122">Requirement</span></span> | <span data-ttu-id="69f02-123">Значение</span><span class="sxs-lookup"><span data-stu-id="69f02-123">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="69f02-124">Header</span><span class="sxs-lookup"><span data-stu-id="69f02-124">Header</span></span><br/>  | <dl> <span data-ttu-id="69f02-125"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="69f02-125"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="69f02-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="69f02-126">Library</span></span><br/> | <dl> <span data-ttu-id="69f02-127"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="69f02-127"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69f02-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="69f02-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69f02-129">ID3DX10SkinInfo</span><span class="sxs-lookup"><span data-stu-id="69f02-129">ID3DX10SkinInfo</span></span>](id3dx10skininfo.md)
</dt> <dt>

[<span data-ttu-id="69f02-130">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="69f02-130">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
