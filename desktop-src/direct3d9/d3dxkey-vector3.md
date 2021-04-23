---
description: Описывает Векторный ключ для использования в анимации по ключевым кадрам. Задает вектор в заданный момент времени. Используется для ключей масштабирования и преобразования.
ms.assetid: 7a7ba2ce-c9f3-4a04-b865-39de9070868b
title: Структура D3DXKEY_VECTOR3 (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXKEY_VECTOR3
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 41aec16da30a6e8742290b747b844b7fb22f6650
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105720889"
---
# <a name="d3dxkey_vector3-structure"></a><span data-ttu-id="47780-105">\_Структура VECTOR3 D3DXKEY</span><span class="sxs-lookup"><span data-stu-id="47780-105">D3DXKEY\_VECTOR3 structure</span></span>

<span data-ttu-id="47780-106">Описывает Векторный ключ для использования в анимации по ключевым кадрам.</span><span class="sxs-lookup"><span data-stu-id="47780-106">Describes a vector key for use in key frame animation.</span></span> <span data-ttu-id="47780-107">Задает вектор в заданный момент времени.</span><span class="sxs-lookup"><span data-stu-id="47780-107">It specifies a vector at a given time.</span></span> <span data-ttu-id="47780-108">Используется для ключей масштабирования и преобразования.</span><span class="sxs-lookup"><span data-stu-id="47780-108">This is used for scale and translation keys.</span></span>

## <a name="syntax"></a><span data-ttu-id="47780-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="47780-109">Syntax</span></span>


```C++
typedef struct D3DXKEY_VECTOR3 {
  FLOAT       Time;
  D3DXVECTOR3 Value;
} D3DXKEY_VECTOR3, *LPD3DXKEY_VECTOR3;
```



## <a name="members"></a><span data-ttu-id="47780-110">Члены</span><span class="sxs-lookup"><span data-stu-id="47780-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="47780-111">**Time**</span><span class="sxs-lookup"><span data-stu-id="47780-111">**Time**</span></span>
</dt> <dd>

<span data-ttu-id="47780-112">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="47780-112">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="47780-113">Метка времени ключевого кадра.</span><span class="sxs-lookup"><span data-stu-id="47780-113">Key frame time stamp.</span></span>

</dd> <dt>

<span data-ttu-id="47780-114">**Значение**</span><span class="sxs-lookup"><span data-stu-id="47780-114">**Value**</span></span>
</dt> <dd>

<span data-ttu-id="47780-115">Тип: **[ **D3DXVECTOR3**](d3dxvector3.md)**</span><span class="sxs-lookup"><span data-stu-id="47780-115">Type: **[**D3DXVECTOR3**](d3dxvector3.md)**</span></span>

</dd> <dd>

<span data-ttu-id="47780-116">[**D3DXVECTOR3**](d3dxvector3.md) трехмерный вектор, предоставляющий значения для масштабирования и (или) преобразования.</span><span class="sxs-lookup"><span data-stu-id="47780-116">[**D3DXVECTOR3**](d3dxvector3.md) 3D vector that supplies scale and/or translation values.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="47780-117">Требования</span><span class="sxs-lookup"><span data-stu-id="47780-117">Requirements</span></span>



| <span data-ttu-id="47780-118">Требование</span><span class="sxs-lookup"><span data-stu-id="47780-118">Requirement</span></span> | <span data-ttu-id="47780-119">Значение</span><span class="sxs-lookup"><span data-stu-id="47780-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="47780-120">Header</span><span class="sxs-lookup"><span data-stu-id="47780-120">Header</span></span><br/> | <dl> <span data-ttu-id="47780-121"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="47780-121"><dt>D3dx9anim.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="47780-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="47780-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47780-123">Структуры D3DX</span><span class="sxs-lookup"><span data-stu-id="47780-123">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
