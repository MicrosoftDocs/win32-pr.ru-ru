---
title: Регистр позиций
description: Этот выходной регистр шейдера вершин содержит данные о положении на вершину.
ms.assetid: 98f71027-d94b-4dd0-a6b6-4b263954eff9
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 89470bb920db7c612b21cefb2c44c2c89d48ce28
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103776622"
---
# <a name="position-register"></a><span data-ttu-id="ec3d3-103">Регистр позиций</span><span class="sxs-lookup"><span data-stu-id="ec3d3-103">Position Register</span></span>

<span data-ttu-id="ec3d3-104">Этот выходной регистр шейдера вершин содержит данные о положении на вершину.</span><span class="sxs-lookup"><span data-stu-id="ec3d3-104">This vertex shader output register contains per-vertex position data.</span></span>



| <span data-ttu-id="ec3d3-105">Версии шейдеров вершин</span><span class="sxs-lookup"><span data-stu-id="ec3d3-105">Vertex shader versions</span></span> | <span data-ttu-id="ec3d3-106">1\_1</span><span class="sxs-lookup"><span data-stu-id="ec3d3-106">1\_1</span></span> | <span data-ttu-id="ec3d3-107">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="ec3d3-107">2\_0</span></span> | <span data-ttu-id="ec3d3-108">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="ec3d3-108">2\_sw</span></span> | <span data-ttu-id="ec3d3-109">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="ec3d3-109">2\_x</span></span> | <span data-ttu-id="ec3d3-110">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="ec3d3-110">3\_0</span></span> | <span data-ttu-id="ec3d3-111">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="ec3d3-111">3\_sw</span></span> |
|------------------------|------|------|-------|------|------|-------|
| <span data-ttu-id="ec3d3-112">Регистр позиций</span><span class="sxs-lookup"><span data-stu-id="ec3d3-112">Position Register</span></span>      | <span data-ttu-id="ec3d3-113">x</span><span class="sxs-lookup"><span data-stu-id="ec3d3-113">x</span></span>    | <span data-ttu-id="ec3d3-114">x</span><span class="sxs-lookup"><span data-stu-id="ec3d3-114">x</span></span>    | <span data-ttu-id="ec3d3-115">x</span><span class="sxs-lookup"><span data-stu-id="ec3d3-115">x</span></span>     | <span data-ttu-id="ec3d3-116">x</span><span class="sxs-lookup"><span data-stu-id="ec3d3-116">x</span></span>    | <span data-ttu-id="ec3d3-117">x</span><span class="sxs-lookup"><span data-stu-id="ec3d3-117">x</span></span>    | <span data-ttu-id="ec3d3-118">x</span><span class="sxs-lookup"><span data-stu-id="ec3d3-118">x</span></span>     |



 

<span data-ttu-id="ec3d3-119">Регистр состоит из свойств, определяющих принцип работы каждой ККМ.</span><span class="sxs-lookup"><span data-stu-id="ec3d3-119">A register consists of properties that determine how each register behaves.</span></span>



| <span data-ttu-id="ec3d3-120">Свойство</span><span class="sxs-lookup"><span data-stu-id="ec3d3-120">Property</span></span>        | <span data-ttu-id="ec3d3-121">Описание</span><span class="sxs-lookup"><span data-stu-id="ec3d3-121">Description</span></span> |
|-----------------|-------------|
| <span data-ttu-id="ec3d3-122">Имя</span><span class="sxs-lookup"><span data-stu-id="ec3d3-122">Name</span></span>            | <span data-ttu-id="ec3d3-123">oPos</span><span class="sxs-lookup"><span data-stu-id="ec3d3-123">oPos</span></span>        |
| <span data-ttu-id="ec3d3-124">Count</span><span class="sxs-lookup"><span data-stu-id="ec3d3-124">Count</span></span>           | <span data-ttu-id="ec3d3-125">1 вектор</span><span class="sxs-lookup"><span data-stu-id="ec3d3-125">1 vector</span></span>    |
| <span data-ttu-id="ec3d3-126">Разрешения ввода-вывода</span><span class="sxs-lookup"><span data-stu-id="ec3d3-126">I/O permissions</span></span> | <span data-ttu-id="ec3d3-127">Доступный только на запись.</span><span class="sxs-lookup"><span data-stu-id="ec3d3-127">Write-only.</span></span> |



 

<span data-ttu-id="ec3d3-128">Значение является позицией в однородной вырезанной области.</span><span class="sxs-lookup"><span data-stu-id="ec3d3-128">The value is the position in homogeneous clipping space.</span></span> <span data-ttu-id="ec3d3-129">Это значение должно быть записано шейдером вершин.</span><span class="sxs-lookup"><span data-stu-id="ec3d3-129">This value must be written by the vertex shader.</span></span>

<span data-ttu-id="ec3d3-130">Например, .</span><span class="sxs-lookup"><span data-stu-id="ec3d3-130">Example</span></span>


```
    dcl_position v0
    
    def c40, 0.0f,0.0f,0.0f,0.0f;
    // transform into projection space
    m4x4 r0,v0,c8
    max r0.z,c40.z,r0.z //clamp to 0
    max r0.w,c12.x,r0.w //clamp to near clip plane
    mov oPos,r0   
```



## <a name="related-topics"></a><span data-ttu-id="ec3d3-131">См. также</span><span class="sxs-lookup"><span data-stu-id="ec3d3-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ec3d3-132">Регистры шейдеров вершин</span><span class="sxs-lookup"><span data-stu-id="ec3d3-132">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




