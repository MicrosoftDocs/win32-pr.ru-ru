---
description: Структура D3DXSHPRTSPLITMESHCLUSTERDATA
ms.assetid: 6a53420c-06bc-4f52-ac2e-5adda5e34cb2
title: Структура D3DXSHPRTSPLITMESHCLUSTERDATA (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHPRTSPLITMESHCLUSTERDATA
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: e7b1bc23606dbf08f5a924860e12c9c09d719287
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713609"
---
# <a name="d3dxshprtsplitmeshclusterdata-structure"></a><span data-ttu-id="585e6-103">Структура D3DXSHPRTSPLITMESHCLUSTERDATA</span><span class="sxs-lookup"><span data-stu-id="585e6-103">D3DXSHPRTSPLITMESHCLUSTERDATA structure</span></span>

## <a name="syntax"></a><span data-ttu-id="585e6-104">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="585e6-104">Syntax</span></span>


```C++
typedef struct D3DXSHPRTSPLITMESHCLUSTERDATA {
  UINT uVertStart;
  UINT uVertLength;
  UINT uFaceStart;
  UINT uFaceLength;
  UINT uClusterStart;
  UINT uClusterLength;
} D3DXSHPRTSPLITMESHCLUSTERDATA, *LPD3DXSHPRTSPLITMESHCLUSTERDATA;
```



## <a name="members"></a><span data-ttu-id="585e6-105">Члены</span><span class="sxs-lookup"><span data-stu-id="585e6-105">Members</span></span>

<dl> <dt>

<span data-ttu-id="585e6-106">**увертстарт**</span><span class="sxs-lookup"><span data-stu-id="585e6-106">**uVertStart**</span></span>
</dt> <dd>

<span data-ttu-id="585e6-107">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="585e6-107">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="585e6-108">Начальная вершина в пересопоставленный массив вершин.</span><span class="sxs-lookup"><span data-stu-id="585e6-108">Initial vertex into remapped vertex array.</span></span>

</dd> <dt>

<span data-ttu-id="585e6-109">**увертленгс**</span><span class="sxs-lookup"><span data-stu-id="585e6-109">**uVertLength**</span></span>
</dt> <dd>

<span data-ttu-id="585e6-110">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="585e6-110">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="585e6-111">Количество вершин в этом кластере.</span><span class="sxs-lookup"><span data-stu-id="585e6-111">Number of vertices in this supercluster.</span></span>

</dd> <dt>

<span data-ttu-id="585e6-112">**уфацестарт**</span><span class="sxs-lookup"><span data-stu-id="585e6-112">**uFaceStart**</span></span>
</dt> <dd>

<span data-ttu-id="585e6-113">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="585e6-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="585e6-114">Начальный индекс в массиве лиц.</span><span class="sxs-lookup"><span data-stu-id="585e6-114">Initial index into face array.</span></span>

</dd> <dt>

<span data-ttu-id="585e6-115">**уфацеленгс**</span><span class="sxs-lookup"><span data-stu-id="585e6-115">**uFaceLength**</span></span>
</dt> <dd>

<span data-ttu-id="585e6-116">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="585e6-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="585e6-117">Количество лиц в этом кластере.</span><span class="sxs-lookup"><span data-stu-id="585e6-117">Number of faces in this supercluster.</span></span>

</dd> <dt>

<span data-ttu-id="585e6-118">**уклустерстарт**</span><span class="sxs-lookup"><span data-stu-id="585e6-118">**uClusterStart**</span></span>
</dt> <dd>

<span data-ttu-id="585e6-119">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="585e6-119">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="585e6-120">Начальный индекс в массиве кластера.</span><span class="sxs-lookup"><span data-stu-id="585e6-120">Initial index into cluster array.</span></span>

</dd> <dt>

<span data-ttu-id="585e6-121">**уклустерленгс**</span><span class="sxs-lookup"><span data-stu-id="585e6-121">**uClusterLength**</span></span>
</dt> <dd>

<span data-ttu-id="585e6-122">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="585e6-122">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="585e6-123">Количество кластеров в этом массиве.</span><span class="sxs-lookup"><span data-stu-id="585e6-123">Number of clusters in this supercluster array.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="585e6-124">Требования</span><span class="sxs-lookup"><span data-stu-id="585e6-124">Requirements</span></span>



| <span data-ttu-id="585e6-125">Требование</span><span class="sxs-lookup"><span data-stu-id="585e6-125">Requirement</span></span> | <span data-ttu-id="585e6-126">Значение</span><span class="sxs-lookup"><span data-stu-id="585e6-126">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="585e6-127">Header</span><span class="sxs-lookup"><span data-stu-id="585e6-127">Header</span></span><br/> | <dl> <span data-ttu-id="585e6-128"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="585e6-128"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="585e6-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="585e6-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="585e6-130">Структуры D3DX</span><span class="sxs-lookup"><span data-stu-id="585e6-130">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="585e6-131">**D3DXSHPRTCompSplitMeshSC**</span><span class="sxs-lookup"><span data-stu-id="585e6-131">**D3DXSHPRTCompSplitMeshSC**</span></span>](d3dxshprtcompsplitmeshsc.md)
</dt> </dl>

 

 
