---
description: Описывает 16-разрядный вектор с плавающей точкой.
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
ms.openlocfilehash: 4b469c770b811ed11ec21b21d2b449df1fd75b1c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105720894"
---
# <a name="d3dxfloat16-structure-d3dx9mathh"></a><span data-ttu-id="8c8f8-103">Структура D3DXFLOAT16 (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="8c8f8-103">D3DXFLOAT16 structure (D3dx9math.h)</span></span>

<span data-ttu-id="8c8f8-104">Описывает 16-разрядный вектор с плавающей точкой.</span><span class="sxs-lookup"><span data-stu-id="8c8f8-104">Describes a 16-bit floating point vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c8f8-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8c8f8-105">Syntax</span></span>


```C++
typedef struct D3DXFLOAT16 {
  WORD Value;
} D3DXFLOAT16, *LPD3DXFLOAT16;
```



## <a name="members"></a><span data-ttu-id="8c8f8-106">Члены</span><span class="sxs-lookup"><span data-stu-id="8c8f8-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="8c8f8-107">**Значение**</span><span class="sxs-lookup"><span data-stu-id="8c8f8-107">**Value**</span></span>
</dt> <dd>

<span data-ttu-id="8c8f8-108">Тип: **[ **слово**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8c8f8-108">Type: **[**WORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="8c8f8-109">16-разрядные данные.</span><span class="sxs-lookup"><span data-stu-id="8c8f8-109">The 16-bit data.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8c8f8-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8c8f8-110">Remarks</span></span>

<span data-ttu-id="8c8f8-111">Программисты C++ могут воспользоваться преимуществами перегрузки операторов и приведения типов с помощью [**расширений D3DXFLOAT16**](d3dxfloat16-extensions.md), реализующих перегруженные конструкторы и операторы присваивания, унарные и бинарные (включая равенство).</span><span class="sxs-lookup"><span data-stu-id="8c8f8-111">C++ programmers can take advantage of operator overloading and type casting with the [**D3DXFLOAT16 Extensions**](d3dxfloat16-extensions.md), which implement overloaded constructors and assignment, unary, and binary (including equality) operators.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c8f8-112">Требования</span><span class="sxs-lookup"><span data-stu-id="8c8f8-112">Requirements</span></span>



| <span data-ttu-id="8c8f8-113">Требование</span><span class="sxs-lookup"><span data-stu-id="8c8f8-113">Requirement</span></span> | <span data-ttu-id="8c8f8-114">Значение</span><span class="sxs-lookup"><span data-stu-id="8c8f8-114">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8c8f8-115">Header</span><span class="sxs-lookup"><span data-stu-id="8c8f8-115">Header</span></span><br/> | <dl> <span data-ttu-id="8c8f8-116"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="8c8f8-116"><dt>D3dx9math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c8f8-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8c8f8-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c8f8-118">Структуры D3DX</span><span class="sxs-lookup"><span data-stu-id="8c8f8-118">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
