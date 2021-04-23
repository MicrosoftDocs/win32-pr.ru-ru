---
description: Описывает объект Effect.
ms.assetid: 161d3e7a-213a-4a83-a1b5-837b0aab96bf
title: Структура D3DXEFFECT_DESC (D3dx9effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXEFFECT_DESC
api_type:
- HeaderDef
api_location:
- d3dx9effect.h
ms.openlocfilehash: c8e7a3a2adf19514e2e4d1c6f61dbea888ce033d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821093"
---
# <a name="d3dxeffect_desc-structure"></a><span data-ttu-id="99849-103">\_Структура D3DXEFFECT DESC</span><span class="sxs-lookup"><span data-stu-id="99849-103">D3DXEFFECT\_DESC structure</span></span>

<span data-ttu-id="99849-104">Описывает объект Effect.</span><span class="sxs-lookup"><span data-stu-id="99849-104">Describes an effect object.</span></span>

## <a name="syntax"></a><span data-ttu-id="99849-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="99849-105">Syntax</span></span>


```C++
typedef struct D3DXEFFECT_DESC {
  LPCSTR Creator;
  UINT   Parameters;
  UINT   Techniques;
  UINT   Functions;
} D3DXEFFECT_DESC, *LPD3DXEFFECT_DESC;
```



## <a name="members"></a><span data-ttu-id="99849-106">Члены</span><span class="sxs-lookup"><span data-stu-id="99849-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="99849-107">**Автор**</span><span class="sxs-lookup"><span data-stu-id="99849-107">**Creator**</span></span>
</dt> <dd>

<span data-ttu-id="99849-108">Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="99849-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="99849-109">Строка, содержащая имя создателя эффектов.</span><span class="sxs-lookup"><span data-stu-id="99849-109">String that contains the name of the effect creator.</span></span>

</dd> <dt>

<span data-ttu-id="99849-110">**Параметры**</span><span class="sxs-lookup"><span data-stu-id="99849-110">**Parameters**</span></span>
</dt> <dd>

<span data-ttu-id="99849-111">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="99849-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="99849-112">Количество параметров, используемых для вступления в действие.</span><span class="sxs-lookup"><span data-stu-id="99849-112">Number of parameters used for effect.</span></span>

</dd> <dt>

<span data-ttu-id="99849-113">**Технологий**</span><span class="sxs-lookup"><span data-stu-id="99849-113">**Techniques**</span></span>
</dt> <dd>

<span data-ttu-id="99849-114">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="99849-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="99849-115">Количество методов, которые могут визуализировать результат.</span><span class="sxs-lookup"><span data-stu-id="99849-115">Number of techniques that can render the effect.</span></span>

</dd> <dt>

<span data-ttu-id="99849-116">**Функции**</span><span class="sxs-lookup"><span data-stu-id="99849-116">**Functions**</span></span>
</dt> <dd>

<span data-ttu-id="99849-117">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="99849-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="99849-118">Число функций, которые могут визуализировать результат.</span><span class="sxs-lookup"><span data-stu-id="99849-118">Number of functions that can render the effect.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="99849-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="99849-119">Remarks</span></span>

<span data-ttu-id="99849-120">Объект Effect может содержать несколько методов отрисовки и параметров для одного и того же результата.</span><span class="sxs-lookup"><span data-stu-id="99849-120">An effect object can contain multiple rendering techniques and parameters for the same effect.</span></span>

## <a name="requirements"></a><span data-ttu-id="99849-121">Требования</span><span class="sxs-lookup"><span data-stu-id="99849-121">Requirements</span></span>



| <span data-ttu-id="99849-122">Требование</span><span class="sxs-lookup"><span data-stu-id="99849-122">Requirement</span></span> | <span data-ttu-id="99849-123">Значение</span><span class="sxs-lookup"><span data-stu-id="99849-123">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="99849-124">Header</span><span class="sxs-lookup"><span data-stu-id="99849-124">Header</span></span><br/> | <dl> <span data-ttu-id="99849-125"><dt>D3dx9effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="99849-125"><dt>D3dx9effect.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="99849-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="99849-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99849-127">Структуры эффектов</span><span class="sxs-lookup"><span data-stu-id="99849-127">Effect Structures</span></span>](dx9-graphics-reference-effects-structures.md)
</dt> </dl>

 

 
