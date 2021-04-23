---
description: Описывает ключ кватернион для использования в анимации по ключевым кадрам. Ключ кватернион — это значение кватерниона в заданный момент времени.
ms.assetid: 8f5b74a3-f712-40ac-942c-a2189c2327c8
title: Структура D3DXKEY_QUATERNION (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXKEY_QUATERNION
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 12e4deead606c1a2c5b103ed9fd0e31e23515982
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354810"
---
# <a name="d3dxkey_quaternion-structure"></a><span data-ttu-id="6ee93-104">\_Структура КВАТЕРНИОНА D3DXKEY</span><span class="sxs-lookup"><span data-stu-id="6ee93-104">D3DXKEY\_QUATERNION structure</span></span>

<span data-ttu-id="6ee93-105">Описывает ключ кватернион для использования в анимации по ключевым кадрам.</span><span class="sxs-lookup"><span data-stu-id="6ee93-105">Describes a quaternion key for use in key frame animation.</span></span> <span data-ttu-id="6ee93-106">Ключ кватернион — это значение кватерниона в заданный момент времени.</span><span class="sxs-lookup"><span data-stu-id="6ee93-106">A quaternion key is a quaternion value at a given time.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ee93-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6ee93-107">Syntax</span></span>


```C++
typedef struct D3DXKEY_QUATERNION {
  FLOAT          Time;
  D3DXQUATERNION Value;
} D3DXKEY_QUATERNION, *LPD3DXKEY_QUATERNION;
```



## <a name="members"></a><span data-ttu-id="6ee93-108">Члены</span><span class="sxs-lookup"><span data-stu-id="6ee93-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="6ee93-109">**Time**</span><span class="sxs-lookup"><span data-stu-id="6ee93-109">**Time**</span></span>
</dt> <dd>

<span data-ttu-id="6ee93-110">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6ee93-110">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6ee93-111">Значение времени.</span><span class="sxs-lookup"><span data-stu-id="6ee93-111">Time value.</span></span>

</dd> <dt>

<span data-ttu-id="6ee93-112">**Значение**</span><span class="sxs-lookup"><span data-stu-id="6ee93-112">**Value**</span></span>
</dt> <dd>

<span data-ttu-id="6ee93-113">Тип: **[ **D3DXQUATERNION**](d3dxquaternion.md)**</span><span class="sxs-lookup"><span data-stu-id="6ee93-113">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6ee93-114">[**D3DXQUATERNION**](d3dxquaternion.md) кватернион, предоставляющий значения поворота.</span><span class="sxs-lookup"><span data-stu-id="6ee93-114">[**D3DXQUATERNION**](d3dxquaternion.md) quaternion that supplies rotation values.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6ee93-115">Требования</span><span class="sxs-lookup"><span data-stu-id="6ee93-115">Requirements</span></span>



| <span data-ttu-id="6ee93-116">Требование</span><span class="sxs-lookup"><span data-stu-id="6ee93-116">Requirement</span></span> | <span data-ttu-id="6ee93-117">Значение</span><span class="sxs-lookup"><span data-stu-id="6ee93-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6ee93-118">Header</span><span class="sxs-lookup"><span data-stu-id="6ee93-118">Header</span></span><br/> | <dl> <span data-ttu-id="6ee93-119"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="6ee93-119"><dt>D3dx9anim.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ee93-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6ee93-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ee93-121">Структуры D3DX</span><span class="sxs-lookup"><span data-stu-id="6ee93-121">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
