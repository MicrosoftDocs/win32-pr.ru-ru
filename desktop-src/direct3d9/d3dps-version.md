---
description: Создайте маркер версии построителя текстуры.
ms.assetid: 70089a93-83df-4ac4-8d98-4e1bb6ad2581
title: Макрос D3DPS_VERSION (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DPS_VERSION
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: c3f30d673145ec9dfe38bd8e2a636ac04c9a195a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355050"
---
# <a name="d3dps_version-macro"></a><span data-ttu-id="36046-103">\_Макрос версии D3DPS</span><span class="sxs-lookup"><span data-stu-id="36046-103">D3DPS\_VERSION macro</span></span>

<span data-ttu-id="36046-104">Создайте маркер версии построителя текстуры.</span><span class="sxs-lookup"><span data-stu-id="36046-104">Create a pixel shader version token.</span></span>

## <a name="syntax"></a><span data-ttu-id="36046-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="36046-105">Syntax</span></span>


```C++
DWORD D3DPS_VERSION(
   int _Major,
   int _Minor
);
```



## <a name="parameters"></a><span data-ttu-id="36046-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="36046-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36046-107">*\_Большой*</span><span class="sxs-lookup"><span data-stu-id="36046-107">*\_Major*</span></span> 
</dt> <dd>

<span data-ttu-id="36046-108">Версия основного шейдера пикселей.</span><span class="sxs-lookup"><span data-stu-id="36046-108">The major pixel shader version.</span></span>

</dd> <dt>

<span data-ttu-id="36046-109">*\_Дополнительный номер*</span><span class="sxs-lookup"><span data-stu-id="36046-109">*\_Minor*</span></span> 
</dt> <dd>

<span data-ttu-id="36046-110">Версия незначительного шейдера пикселей.</span><span class="sxs-lookup"><span data-stu-id="36046-110">The minor pixel shader version.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36046-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="36046-111">Return value</span></span>

<span data-ttu-id="36046-112">Возвращает значение типа DWORD, которое является версией шейдера пикселей.</span><span class="sxs-lookup"><span data-stu-id="36046-112">Returns a DWORD value that is a pixel shader version.</span></span>

## <a name="remarks"></a><span data-ttu-id="36046-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="36046-113">Remarks</span></span>

<span data-ttu-id="36046-114">Номера версий</span><span class="sxs-lookup"><span data-stu-id="36046-114">Version Numbers</span></span>

<span data-ttu-id="36046-115">Номер версии — это сочетание основной версии и дополнительных номеров версий шейдера вершин.</span><span class="sxs-lookup"><span data-stu-id="36046-115">The version number is a combination of the major version and the minor vertex shader version numbers.</span></span> <span data-ttu-id="36046-116">Допустимые числа показаны в таблице.</span><span class="sxs-lookup"><span data-stu-id="36046-116">Valid numbers are shown in the table.</span></span>



| <span data-ttu-id="36046-117">Значительно</span><span class="sxs-lookup"><span data-stu-id="36046-117">Major</span></span> | <span data-ttu-id="36046-118">Дополнительный номер</span><span class="sxs-lookup"><span data-stu-id="36046-118">Minor</span></span> | <span data-ttu-id="36046-119">Пример</span><span class="sxs-lookup"><span data-stu-id="36046-119">Example</span></span>             |
|-------|-------|---------------------|
| <span data-ttu-id="36046-120">1</span><span class="sxs-lookup"><span data-stu-id="36046-120">1</span></span>     | <span data-ttu-id="36046-121">1</span><span class="sxs-lookup"><span data-stu-id="36046-121">1</span></span>     | <span data-ttu-id="36046-122">\_Версия D3DPS (1, 1)</span><span class="sxs-lookup"><span data-stu-id="36046-122">D3DPS\_VERSION(1,1)</span></span> |
| <span data-ttu-id="36046-123">1</span><span class="sxs-lookup"><span data-stu-id="36046-123">1</span></span>     | <span data-ttu-id="36046-124">2</span><span class="sxs-lookup"><span data-stu-id="36046-124">2</span></span>     | <span data-ttu-id="36046-125">\_Версия D3DPS (1, 2)</span><span class="sxs-lookup"><span data-stu-id="36046-125">D3DPS\_VERSION(1,2)</span></span> |
| <span data-ttu-id="36046-126">1</span><span class="sxs-lookup"><span data-stu-id="36046-126">1</span></span>     | <span data-ttu-id="36046-127">3</span><span class="sxs-lookup"><span data-stu-id="36046-127">3</span></span>     | <span data-ttu-id="36046-128">\_Версия D3DPS (1, 3)</span><span class="sxs-lookup"><span data-stu-id="36046-128">D3DPS\_VERSION(1,3)</span></span> |
| <span data-ttu-id="36046-129">1</span><span class="sxs-lookup"><span data-stu-id="36046-129">1</span></span>     | <span data-ttu-id="36046-130">4</span><span class="sxs-lookup"><span data-stu-id="36046-130">4</span></span>     | <span data-ttu-id="36046-131">\_Версия D3DPS (1, 4)</span><span class="sxs-lookup"><span data-stu-id="36046-131">D3DPS\_VERSION(1,4)</span></span> |
| <span data-ttu-id="36046-132">2</span><span class="sxs-lookup"><span data-stu-id="36046-132">2</span></span>     | <span data-ttu-id="36046-133">0</span><span class="sxs-lookup"><span data-stu-id="36046-133">0</span></span>     | <span data-ttu-id="36046-134">\_Версия D3DPS (2, 0)</span><span class="sxs-lookup"><span data-stu-id="36046-134">D3DPS\_VERSION(2,0)</span></span> |
| <span data-ttu-id="36046-135">3</span><span class="sxs-lookup"><span data-stu-id="36046-135">3</span></span>     | <span data-ttu-id="36046-136">0</span><span class="sxs-lookup"><span data-stu-id="36046-136">0</span></span>     | <span data-ttu-id="36046-137">\_Версия D3DPS (3, 0)</span><span class="sxs-lookup"><span data-stu-id="36046-137">D3DPS\_VERSION(3,0)</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="36046-138">Требования</span><span class="sxs-lookup"><span data-stu-id="36046-138">Requirements</span></span>



| <span data-ttu-id="36046-139">Требование</span><span class="sxs-lookup"><span data-stu-id="36046-139">Requirement</span></span> | <span data-ttu-id="36046-140">Значение</span><span class="sxs-lookup"><span data-stu-id="36046-140">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="36046-141">Header</span><span class="sxs-lookup"><span data-stu-id="36046-141">Header</span></span><br/> | <dl> <span data-ttu-id="36046-142"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="36046-142"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36046-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="36046-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36046-144">Макросы</span><span class="sxs-lookup"><span data-stu-id="36046-144">Macros</span></span>](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[<span data-ttu-id="36046-145">D3DCAPS9</span><span class="sxs-lookup"><span data-stu-id="36046-145">D3DCAPS9</span></span>](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)
</dt> </dl>

 

 




