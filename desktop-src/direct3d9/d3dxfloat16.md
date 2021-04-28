---
description: Структура D3DXFLOAT16 (D3dx9math. h) — описывает 16-разрядный вектор с плавающей точкой.
ms.assetid: f823a327-f07a-44e9-b58a-7865e11e80eb
title: Структура D3DXFLOAT16 (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFLOAT16
api_type:
- HeaderDef
api_location:
- d3dx9math.h
ms.openlocfilehash: dc878575de4338a2a399f329362d79ff2e7654f0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094272"
---
# <a name="d3dxfloat16-structure-d3dx9mathh"></a><span data-ttu-id="5edc4-103">Структура D3DXFLOAT16 (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="5edc4-103">D3DXFLOAT16 structure (D3dx9math.h)</span></span>

<span data-ttu-id="5edc4-104">Описывает 16-разрядный вектор с плавающей точкой.</span><span class="sxs-lookup"><span data-stu-id="5edc4-104">Describes a 16-bit floating point vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="5edc4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5edc4-105">Syntax</span></span>


```C++
typedef struct D3DXFLOAT16 {
  WORD Value;
} D3DXFLOAT16, *LPD3DXFLOAT16;
```



## <a name="members"></a><span data-ttu-id="5edc4-106">Члены</span><span class="sxs-lookup"><span data-stu-id="5edc4-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="5edc4-107">**Значение**</span><span class="sxs-lookup"><span data-stu-id="5edc4-107">**Value**</span></span>
</dt> <dd>

<span data-ttu-id="5edc4-108">Тип: **[ **слово**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5edc4-108">Type: **[**WORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="5edc4-109">16-разрядные данные.</span><span class="sxs-lookup"><span data-stu-id="5edc4-109">The 16-bit data.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5edc4-110">Remarks</span><span class="sxs-lookup"><span data-stu-id="5edc4-110">Remarks</span></span>

<span data-ttu-id="5edc4-111">Программисты C++ могут воспользоваться преимуществами перегрузки операторов и приведения типов с помощью [**расширений D3DXFLOAT16**](d3dxfloat16-extensions.md), реализующих перегруженные конструкторы и операторы присваивания, унарные и бинарные (включая равенство).</span><span class="sxs-lookup"><span data-stu-id="5edc4-111">C++ programmers can take advantage of operator overloading and type casting with the [**D3DXFLOAT16 Extensions**](d3dxfloat16-extensions.md), which implement overloaded constructors and assignment, unary, and binary (including equality) operators.</span></span>

## <a name="requirements"></a><span data-ttu-id="5edc4-112">Требования</span><span class="sxs-lookup"><span data-stu-id="5edc4-112">Requirements</span></span>



| <span data-ttu-id="5edc4-113">Требование</span><span class="sxs-lookup"><span data-stu-id="5edc4-113">Requirement</span></span> | <span data-ttu-id="5edc4-114">Значение</span><span class="sxs-lookup"><span data-stu-id="5edc4-114">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5edc4-115">Header</span><span class="sxs-lookup"><span data-stu-id="5edc4-115">Header</span></span><br/> | <dl> <span data-ttu-id="5edc4-116"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="5edc4-116"><dt>D3dx9math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5edc4-117">См. также</span><span class="sxs-lookup"><span data-stu-id="5edc4-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5edc4-118">Структуры D3DX</span><span class="sxs-lookup"><span data-stu-id="5edc4-118">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
