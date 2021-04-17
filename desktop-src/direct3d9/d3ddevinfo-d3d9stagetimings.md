---
description: Процент времени обработки данных шейдера.
ms.assetid: 388bb943-c25f-4b50-b7e4-d6259f1186c2
title: Структура D3DDEVINFO_D3D9STAGETIMINGS (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVINFO_D3D9STAGETIMINGS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: cf8c9522decfcbb09a60aff0bee65ca05a0f5eeb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105674687"
---
# <a name="d3ddevinfo_d3d9stagetimings-structure"></a><span data-ttu-id="09827-103">\_Структура D3D9STAGETIMINGS D3DDEVINFO</span><span class="sxs-lookup"><span data-stu-id="09827-103">D3DDEVINFO\_D3D9STAGETIMINGS structure</span></span>

<span data-ttu-id="09827-104">Процент времени обработки данных шейдера.</span><span class="sxs-lookup"><span data-stu-id="09827-104">Percent of time processing shader data.</span></span>

## <a name="syntax"></a><span data-ttu-id="09827-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="09827-105">Syntax</span></span>


```C++
typedef struct D3DDEVINFO_D3D9STAGETIMINGS {
  FLOAT MemoryProcessingPercent;
  FLOAT ComputationProcessingPercent;
} D3DDEVINFO_D3D9STAGETIMINGS, *LPD3DDEVINFO_D3D9STAGETIMINGS;
```



## <a name="members"></a><span data-ttu-id="09827-106">Члены</span><span class="sxs-lookup"><span data-stu-id="09827-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="09827-107">**меморипроцессингперцент**</span><span class="sxs-lookup"><span data-stu-id="09827-107">**MemoryProcessingPercent**</span></span>
</dt> <dd>

<span data-ttu-id="09827-108">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="09827-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="09827-109">Процент времени, затраченного на доступ к памяти в шейдере.</span><span class="sxs-lookup"><span data-stu-id="09827-109">Percent of time in shader spent on memory accesses.</span></span>

</dd> <dt>

<span data-ttu-id="09827-110">**компутатионпроцессингперцент**</span><span class="sxs-lookup"><span data-stu-id="09827-110">**ComputationProcessingPercent**</span></span>
</dt> <dd>

<span data-ttu-id="09827-111">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="09827-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="09827-112">Процент времени обработки (перемещение данных по регистрам или выполнение математических операций).</span><span class="sxs-lookup"><span data-stu-id="09827-112">Percent of time processing (moving data around in registers or doing mathematical operations).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="09827-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="09827-113">Remarks</span></span>

<span data-ttu-id="09827-114">Для оптимальной производительности рекомендуется использовать сбалансированную нагрузку.</span><span class="sxs-lookup"><span data-stu-id="09827-114">For best performance, a balanced load is recommended.</span></span>

## <a name="requirements"></a><span data-ttu-id="09827-115">Требования</span><span class="sxs-lookup"><span data-stu-id="09827-115">Requirements</span></span>



| <span data-ttu-id="09827-116">Требование</span><span class="sxs-lookup"><span data-stu-id="09827-116">Requirement</span></span> | <span data-ttu-id="09827-117">Значение</span><span class="sxs-lookup"><span data-stu-id="09827-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="09827-118">Header</span><span class="sxs-lookup"><span data-stu-id="09827-118">Header</span></span><br/> | <dl> <span data-ttu-id="09827-119"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="09827-119"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09827-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="09827-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09827-121">Структуры Direct3D</span><span class="sxs-lookup"><span data-stu-id="09827-121">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="09827-122">**GetData**</span><span class="sxs-lookup"><span data-stu-id="09827-122">**GetData**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata)
</dt> </dl>

 

 
