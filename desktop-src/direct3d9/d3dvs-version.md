---
description: Создайте маркер номера версии шейдера вершин.
ms.assetid: c3aa6b01-7949-4171-a8b5-2f453fd7a422
title: Макрос D3DVS_VERSION (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DVS_VERSION
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: 915d5b843287602c80572d739d8b369d8c301770
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713791"
---
# <a name="d3dvs_version-macro"></a><span data-ttu-id="05b98-103">\_Макрос версии D3DVS</span><span class="sxs-lookup"><span data-stu-id="05b98-103">D3DVS\_VERSION macro</span></span>

<span data-ttu-id="05b98-104">Создайте маркер номера версии шейдера вершин.</span><span class="sxs-lookup"><span data-stu-id="05b98-104">Create a vertex shader version number token.</span></span>

## <a name="syntax"></a><span data-ttu-id="05b98-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="05b98-105">Syntax</span></span>


```C++
DWORD D3DVS_VERSION(
   int _Major,
   int _Minor
);
```



## <a name="parameters"></a><span data-ttu-id="05b98-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="05b98-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05b98-107">*\_Большой*</span><span class="sxs-lookup"><span data-stu-id="05b98-107">*\_Major*</span></span> 
</dt> <dd>

<span data-ttu-id="05b98-108">Версия основного шейдера вершин.</span><span class="sxs-lookup"><span data-stu-id="05b98-108">The major vertex shader version.</span></span> <span data-ttu-id="05b98-109">Соответствующие значения см. в разделе Примечания.</span><span class="sxs-lookup"><span data-stu-id="05b98-109">See remarks for appropriate values.</span></span>

</dd> <dt>

<span data-ttu-id="05b98-110">*\_Дополнительный номер*</span><span class="sxs-lookup"><span data-stu-id="05b98-110">*\_Minor*</span></span> 
</dt> <dd>

<span data-ttu-id="05b98-111">Младшая версия шейдера вершин.</span><span class="sxs-lookup"><span data-stu-id="05b98-111">The minor vertex shader version.</span></span> <span data-ttu-id="05b98-112">Соответствующие значения см. в разделе Примечания.</span><span class="sxs-lookup"><span data-stu-id="05b98-112">See remarks for appropriate values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05b98-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="05b98-113">Return value</span></span>

<span data-ttu-id="05b98-114">Возвращает значение типа DWORD, которое является версией шейдера вершин.</span><span class="sxs-lookup"><span data-stu-id="05b98-114">Returns a DWORD value that is a vertex shader version.</span></span>

## <a name="remarks"></a><span data-ttu-id="05b98-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="05b98-115">Remarks</span></span>

<span data-ttu-id="05b98-116">Номера версий</span><span class="sxs-lookup"><span data-stu-id="05b98-116">Version Numbers</span></span>

<span data-ttu-id="05b98-117">Номер версии — это сочетание основной версии и дополнительных номеров версий шейдера вершин.</span><span class="sxs-lookup"><span data-stu-id="05b98-117">The version number is a combination of the major version and the minor vertex shader version numbers.</span></span> <span data-ttu-id="05b98-118">Допустимые числа показаны в таблице.</span><span class="sxs-lookup"><span data-stu-id="05b98-118">Valid numbers are shown in the table.</span></span>



| <span data-ttu-id="05b98-119">Значительно</span><span class="sxs-lookup"><span data-stu-id="05b98-119">Major</span></span> | <span data-ttu-id="05b98-120">Дополнительный номер</span><span class="sxs-lookup"><span data-stu-id="05b98-120">Minor</span></span> | <span data-ttu-id="05b98-121">Пример</span><span class="sxs-lookup"><span data-stu-id="05b98-121">Example</span></span>             |
|-------|-------|---------------------|
| <span data-ttu-id="05b98-122">1</span><span class="sxs-lookup"><span data-stu-id="05b98-122">1</span></span>     | <span data-ttu-id="05b98-123">1</span><span class="sxs-lookup"><span data-stu-id="05b98-123">1</span></span>     | <span data-ttu-id="05b98-124">\_Версия D3DVS (1, 1)</span><span class="sxs-lookup"><span data-stu-id="05b98-124">D3DVS\_VERSION(1,1)</span></span> |
| <span data-ttu-id="05b98-125">2</span><span class="sxs-lookup"><span data-stu-id="05b98-125">2</span></span>     | <span data-ttu-id="05b98-126">0</span><span class="sxs-lookup"><span data-stu-id="05b98-126">0</span></span>     | <span data-ttu-id="05b98-127">\_Версия D3DVS (2, 0)</span><span class="sxs-lookup"><span data-stu-id="05b98-127">D3DVS\_VERSION(2,0)</span></span> |
| <span data-ttu-id="05b98-128">3</span><span class="sxs-lookup"><span data-stu-id="05b98-128">3</span></span>     | <span data-ttu-id="05b98-129">0</span><span class="sxs-lookup"><span data-stu-id="05b98-129">0</span></span>     | <span data-ttu-id="05b98-130">\_Версия D3DVS (3, 0)</span><span class="sxs-lookup"><span data-stu-id="05b98-130">D3DVS\_VERSION(3,0)</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="05b98-131">Требования</span><span class="sxs-lookup"><span data-stu-id="05b98-131">Requirements</span></span>



| <span data-ttu-id="05b98-132">Требование</span><span class="sxs-lookup"><span data-stu-id="05b98-132">Requirement</span></span> | <span data-ttu-id="05b98-133">Значение</span><span class="sxs-lookup"><span data-stu-id="05b98-133">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="05b98-134">Header</span><span class="sxs-lookup"><span data-stu-id="05b98-134">Header</span></span><br/> | <dl> <span data-ttu-id="05b98-135"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="05b98-135"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05b98-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="05b98-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05b98-137">Макросы</span><span class="sxs-lookup"><span data-stu-id="05b98-137">Macros</span></span>](dx9-graphics-reference-d3d-macros.md)
</dt> </dl>

 

 




