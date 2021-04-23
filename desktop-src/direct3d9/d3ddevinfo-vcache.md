---
description: Указания по оптимизации кэша вершин.
ms.assetid: 891624cd-03dd-4ddd-93f5-4899e1470325
title: Структура D3DDEVINFO_VCACHE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVINFO_VCACHE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 80870c330adf185a869ac5e3543055c82fc7115c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105674685"
---
# <a name="d3ddevinfo_vcache-structure"></a><span data-ttu-id="9eb7c-103">\_Структура ВКАЧЕ D3DDEVINFO</span><span class="sxs-lookup"><span data-stu-id="9eb7c-103">D3DDEVINFO\_VCACHE structure</span></span>

<span data-ttu-id="9eb7c-104">Указания по оптимизации кэша вершин.</span><span class="sxs-lookup"><span data-stu-id="9eb7c-104">Vertex cache optimization hints.</span></span>

## <a name="syntax"></a><span data-ttu-id="9eb7c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9eb7c-105">Syntax</span></span>


```C++
typedef struct D3DDEVINFO_VCACHE {
  DWORD Pattern;
  DWORD OptMethod;
  DWORD CacheSize;
  DWORD MagicNumber;
} D3DDEVINFO_VCACHE, *LPD3DDEVINFO_VCACHE;
```



## <a name="members"></a><span data-ttu-id="9eb7c-106">Члены</span><span class="sxs-lookup"><span data-stu-id="9eb7c-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="9eb7c-107">**Шаблон**</span><span class="sxs-lookup"><span data-stu-id="9eb7c-107">**Pattern**</span></span>
</dt> <dd>

<span data-ttu-id="9eb7c-108">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9eb7c-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9eb7c-109">Битовый шаблон.</span><span class="sxs-lookup"><span data-stu-id="9eb7c-109">Bit pattern.</span></span> <span data-ttu-id="9eb7c-110">Возвращаемое значение должно быть FOURCC ("C", "A", "C", "H").</span><span class="sxs-lookup"><span data-stu-id="9eb7c-110">Return value must be the FOURCC ('C', 'A', 'C', 'H').</span></span>

</dd> <dt>

<span data-ttu-id="9eb7c-111">**оптмесод**</span><span class="sxs-lookup"><span data-stu-id="9eb7c-111">**OptMethod**</span></span>
</dt> <dd>

<span data-ttu-id="9eb7c-112">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9eb7c-112">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9eb7c-113">Метод оптимизации.</span><span class="sxs-lookup"><span data-stu-id="9eb7c-113">Optimizations method.</span></span> <span data-ttu-id="9eb7c-114">Чтобы получить самые длинные полосы, используйте значение 0.</span><span class="sxs-lookup"><span data-stu-id="9eb7c-114">Use 0 to get the longest strips.</span></span> <span data-ttu-id="9eb7c-115">Чтобы оптимизировать использование кэша вершин, используйте значение 1.</span><span class="sxs-lookup"><span data-stu-id="9eb7c-115">Use 1 to optimize the vertex cache usage.</span></span>

</dd> <dt>

<span data-ttu-id="9eb7c-116">**CacheSize**</span><span class="sxs-lookup"><span data-stu-id="9eb7c-116">**CacheSize**</span></span>
</dt> <dd>

<span data-ttu-id="9eb7c-117">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9eb7c-117">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9eb7c-118">Размер кэша, используемый в качестве целевого объекта для оптимизации.</span><span class="sxs-lookup"><span data-stu-id="9eb7c-118">Cache size used as a target for optimization.</span></span> <span data-ttu-id="9eb7c-119">Это необходимо, только если Оптмесод имеет значение 1.</span><span class="sxs-lookup"><span data-stu-id="9eb7c-119">This is required only if OptMethod is 1.</span></span>

</dd> <dt>

<span data-ttu-id="9eb7c-120">**MagicNumber**</span><span class="sxs-lookup"><span data-stu-id="9eb7c-120">**MagicNumber**</span></span>
</dt> <dd>

<span data-ttu-id="9eb7c-121">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9eb7c-121">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9eb7c-122">Используется внутренними методами оптимизации для определения времени перезапуска полос.</span><span class="sxs-lookup"><span data-stu-id="9eb7c-122">Used by internal optimization methods to determine when to restart strips.</span></span> <span data-ttu-id="9eb7c-123">Он не может быть установлен или изменен пользователем.</span><span class="sxs-lookup"><span data-stu-id="9eb7c-123">This cannot be set or modified by a user.</span></span> <span data-ttu-id="9eb7c-124">Это необходимо, только если Оптмесод имеет значение 1.</span><span class="sxs-lookup"><span data-stu-id="9eb7c-124">This is required only if OptMethod is 1.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9eb7c-125">Требования</span><span class="sxs-lookup"><span data-stu-id="9eb7c-125">Requirements</span></span>



| <span data-ttu-id="9eb7c-126">Требование</span><span class="sxs-lookup"><span data-stu-id="9eb7c-126">Requirement</span></span> | <span data-ttu-id="9eb7c-127">Значение</span><span class="sxs-lookup"><span data-stu-id="9eb7c-127">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9eb7c-128">Header</span><span class="sxs-lookup"><span data-stu-id="9eb7c-128">Header</span></span><br/> | <dl> <span data-ttu-id="9eb7c-129"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="9eb7c-129"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9eb7c-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9eb7c-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9eb7c-131">Структуры Direct3D</span><span class="sxs-lookup"><span data-stu-id="9eb7c-131">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="9eb7c-132">**GetData**</span><span class="sxs-lookup"><span data-stu-id="9eb7c-132">**GetData**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata)
</dt> </dl>

 

 
