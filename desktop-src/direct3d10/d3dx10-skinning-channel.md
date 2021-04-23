---
description: Член decl в соответствии с тем, для чего выполняется выборка программного обеспечения. Он используется с API ID3DX10SkinInfo::D Ософтварескиннинг.
ms.assetid: 67c817cd-ce78-4e8b-bdc3-7c4d6670dee1
title: Структура D3DX10_SKINNING_CHANNEL (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_SKINNING_CHANNEL
api_type:
- HeaderDef
api_location:
- D3DX10.h
ms.openlocfilehash: 79f5807dc2539d770d3caa41bddf7aa4960ce682
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273838"
---
# <a name="d3dx10_skinning_channel-structure"></a><span data-ttu-id="dfb70-104">\_Структура канала обложки D3DX10 \_</span><span class="sxs-lookup"><span data-stu-id="dfb70-104">D3DX10\_SKINNING\_CHANNEL structure</span></span>

<span data-ttu-id="dfb70-105">Член decl в соответствии с тем, для чего выполняется выборка программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="dfb70-105">The member of the vertex decl to do the software skinning on.</span></span> <span data-ttu-id="dfb70-106">Он используется с API [**ID3DX10SkinInfo::D ософтварескиннинг**](id3dx10skininfo-dosoftwareskinning.md) .</span><span class="sxs-lookup"><span data-stu-id="dfb70-106">This is used with the [**ID3DX10SkinInfo::DoSoftwareSkinning**](id3dx10skininfo-dosoftwareskinning.md) API.</span></span>

## <a name="syntax"></a><span data-ttu-id="dfb70-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dfb70-107">Syntax</span></span>


```C++
typedef struct D3DX10_SKINNING_CHANNEL {
  UINT SrcOffset;
  UINT DestOffset;
  BOOL IsNormal;
} D3DX10_SKINNING_CHANNEL, *LPD3DX10_SKINNING_CHANNEL;
```



## <a name="members"></a><span data-ttu-id="dfb70-108">Члены</span><span class="sxs-lookup"><span data-stu-id="dfb70-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="dfb70-109">**сркоффсет**</span><span class="sxs-lookup"><span data-stu-id="dfb70-109">**SrcOffset**</span></span>
</dt> <dd>

<span data-ttu-id="dfb70-110">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dfb70-110">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="dfb70-111">Смещение от начала каждой исходной вершины.</span><span class="sxs-lookup"><span data-stu-id="dfb70-111">Offset from the beginning of each source vertex.</span></span>

</dd> <dt>

<span data-ttu-id="dfb70-112">**дестоффсет**</span><span class="sxs-lookup"><span data-stu-id="dfb70-112">**DestOffset**</span></span>
</dt> <dd>

<span data-ttu-id="dfb70-113">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dfb70-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="dfb70-114">Смещение от начала каждой конечной вершины.</span><span class="sxs-lookup"><span data-stu-id="dfb70-114">Offset from the beginning of each destination vertex.</span></span>

</dd> <dt>

<span data-ttu-id="dfb70-115">**Обычная**</span><span class="sxs-lookup"><span data-stu-id="dfb70-115">**IsNormal**</span></span>
</dt> <dd>

<span data-ttu-id="dfb70-116">Тип: **[ **bool** .](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dfb70-116">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="dfb70-117">Определяет, какой массив матриц используется в API [**ID3DX10SkinInfo::D ософтварескиннинг**](id3dx10skininfo-dosoftwareskinning.md) .</span><span class="sxs-lookup"><span data-stu-id="dfb70-117">Determines which array of matrices to use in the [**ID3DX10SkinInfo::DoSoftwareSkinning**](id3dx10skininfo-dosoftwareskinning.md) API.</span></span> <span data-ttu-id="dfb70-118">Если это так, будет использоваться *пинверсетранспосебонематрицес* , в противном случае будет использоваться *пбонематрицес* .</span><span class="sxs-lookup"><span data-stu-id="dfb70-118">If this is true, the *pInverseTransposeBoneMatrices* will be used, otherwise *pBoneMatrices* will be used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dfb70-119">Требования</span><span class="sxs-lookup"><span data-stu-id="dfb70-119">Requirements</span></span>



| <span data-ttu-id="dfb70-120">Требование</span><span class="sxs-lookup"><span data-stu-id="dfb70-120">Requirement</span></span> | <span data-ttu-id="dfb70-121">Значение</span><span class="sxs-lookup"><span data-stu-id="dfb70-121">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="dfb70-122">Header</span><span class="sxs-lookup"><span data-stu-id="dfb70-122">Header</span></span><br/> | <dl> <span data-ttu-id="dfb70-123"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="dfb70-123"><dt>D3DX10.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dfb70-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dfb70-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dfb70-125">Структуры D3DX</span><span class="sxs-lookup"><span data-stu-id="dfb70-125">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
