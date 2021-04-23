---
description: Структура D3DXSHPRTSPLITMESHVERTDATA
ms.assetid: 8799a680-bf5f-42cc-91aa-1a6aed164ca5
title: Структура D3DXSHPRTSPLITMESHVERTDATA (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHPRTSPLITMESHVERTDATA
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 55424929a3d415fc1b89f7a1af53be849cf90185
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821053"
---
# <a name="d3dxshprtsplitmeshvertdata-structure"></a><span data-ttu-id="d4ad2-103">Структура D3DXSHPRTSPLITMESHVERTDATA</span><span class="sxs-lookup"><span data-stu-id="d4ad2-103">D3DXSHPRTSPLITMESHVERTDATA structure</span></span>

## <a name="syntax"></a><span data-ttu-id="d4ad2-104">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d4ad2-104">Syntax</span></span>


```C++
typedef struct D3DXSHPRTSPLITMESHVERTDATA {
  UINT uVertRemap;
  UINT uSubCluster;
  UINT ucVertStatus;
} D3DXSHPRTSPLITMESHVERTDATA, *LPD3DXSHPRTSPLITMESHVERTDATA;
```



## <a name="members"></a><span data-ttu-id="d4ad2-105">Члены</span><span class="sxs-lookup"><span data-stu-id="d4ad2-105">Members</span></span>

<dl> <dt>

<span data-ttu-id="d4ad2-106">**увертремап**</span><span class="sxs-lookup"><span data-stu-id="d4ad2-106">**uVertRemap**</span></span>
</dt> <dd>

<span data-ttu-id="d4ad2-107">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d4ad2-107">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d4ad2-108">Вершина в исходной сетке соответствует.</span><span class="sxs-lookup"><span data-stu-id="d4ad2-108">Vertex in original mesh this corresponds to.</span></span>

</dd> <dt>

<span data-ttu-id="d4ad2-109">**усубклустер**</span><span class="sxs-lookup"><span data-stu-id="d4ad2-109">**uSubCluster**</span></span>
</dt> <dd>

<span data-ttu-id="d4ad2-110">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d4ad2-110">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d4ad2-111">Индекс кластера относительно кластера.</span><span class="sxs-lookup"><span data-stu-id="d4ad2-111">Cluster index, relative to the supercluster.</span></span>

</dd> <dt>

<span data-ttu-id="d4ad2-112">**уквертстатус**</span><span class="sxs-lookup"><span data-stu-id="d4ad2-112">**ucVertStatus**</span></span>
</dt> <dd>

<span data-ttu-id="d4ad2-113">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d4ad2-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d4ad2-114">1, если вершина содержит допустимые данные, 0, если это "Full".</span><span class="sxs-lookup"><span data-stu-id="d4ad2-114">1 if vertex has valid data, 0 if it is "full".</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d4ad2-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d4ad2-115">Remarks</span></span>

<span data-ttu-id="d4ad2-116">Выделено в [**D3DXSHPRTCompSplitMeshSC**](d3dxshprtcompsplitmeshsc.md).</span><span class="sxs-lookup"><span data-stu-id="d4ad2-116">Allocated in [**D3DXSHPRTCompSplitMeshSC**](d3dxshprtcompsplitmeshsc.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d4ad2-117">Требования</span><span class="sxs-lookup"><span data-stu-id="d4ad2-117">Requirements</span></span>



| <span data-ttu-id="d4ad2-118">Требование</span><span class="sxs-lookup"><span data-stu-id="d4ad2-118">Requirement</span></span> | <span data-ttu-id="d4ad2-119">Значение</span><span class="sxs-lookup"><span data-stu-id="d4ad2-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d4ad2-120">Header</span><span class="sxs-lookup"><span data-stu-id="d4ad2-120">Header</span></span><br/> | <dl> <span data-ttu-id="d4ad2-121"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="d4ad2-121"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4ad2-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d4ad2-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4ad2-123">Структуры D3DX</span><span class="sxs-lookup"><span data-stu-id="d4ad2-123">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
