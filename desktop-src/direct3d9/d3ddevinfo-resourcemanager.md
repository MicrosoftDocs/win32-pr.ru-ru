---
description: Статистика использования ресурсов.
ms.assetid: e43de550-2025-4210-a420-e41d14620704
title: Структура D3DDEVINFO_ResourceManager (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVINFO_ResourceManager
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: bf4e84fa247ca5b2603547efef73ea6b9cbe0aee
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103820980"
---
# <a name="d3ddevinfo_resourcemanager-structure"></a><span data-ttu-id="96da1-103">\_Структура RESOURCEMANAGER D3DDEVINFO</span><span class="sxs-lookup"><span data-stu-id="96da1-103">D3DDEVINFO\_ResourceManager structure</span></span>

<span data-ttu-id="96da1-104">Статистика использования ресурсов.</span><span class="sxs-lookup"><span data-stu-id="96da1-104">Resource usage statistics.</span></span>

## <a name="syntax"></a><span data-ttu-id="96da1-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="96da1-105">Syntax</span></span>


```C++
typedef struct D3DDEVINFO_ResourceManager {
  D3DRESOURCESTATS stats[D3DRTYPECOUNT];
} D3DDEVINFO_ResourceManager, *LPD3DDEVINFO_ResourceManager;
```



## <a name="members"></a><span data-ttu-id="96da1-106">Члены</span><span class="sxs-lookup"><span data-stu-id="96da1-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="96da1-107">**Статистика**</span><span class="sxs-lookup"><span data-stu-id="96da1-107">**stats**</span></span>
</dt> <dd>

<span data-ttu-id="96da1-108">Тип: **[ **D3DRESOURCESTATS**](d3dresourcestats.md)**</span><span class="sxs-lookup"><span data-stu-id="96da1-108">Type: **[**D3DRESOURCESTATS**](d3dresourcestats.md)**</span></span>

</dd> <dd>

<span data-ttu-id="96da1-109">Массив элементов статистики ресурсов.</span><span class="sxs-lookup"><span data-stu-id="96da1-109">Array of resource statistics elements.</span></span> <span data-ttu-id="96da1-110">См. [**D3DRESOURCESTATS**](d3dresourcestats.md).</span><span class="sxs-lookup"><span data-stu-id="96da1-110">See [**D3DRESOURCESTATS**](d3dresourcestats.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="96da1-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="96da1-111">Remarks</span></span>

<span data-ttu-id="96da1-112">D3DRTYPECOUNT относится к числу перечислений в [**D3DRESOURCETYPE**](./d3dresourcetype.md).</span><span class="sxs-lookup"><span data-stu-id="96da1-112">D3DRTYPECOUNT refers to the number of enumerations in [**D3DRESOURCETYPE**](./d3dresourcetype.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="96da1-113">Требования</span><span class="sxs-lookup"><span data-stu-id="96da1-113">Requirements</span></span>



| <span data-ttu-id="96da1-114">Требование</span><span class="sxs-lookup"><span data-stu-id="96da1-114">Requirement</span></span> | <span data-ttu-id="96da1-115">Значение</span><span class="sxs-lookup"><span data-stu-id="96da1-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="96da1-116">Header</span><span class="sxs-lookup"><span data-stu-id="96da1-116">Header</span></span><br/> | <dl> <span data-ttu-id="96da1-117"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="96da1-117"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96da1-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="96da1-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96da1-119">Структуры Direct3D</span><span class="sxs-lookup"><span data-stu-id="96da1-119">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
