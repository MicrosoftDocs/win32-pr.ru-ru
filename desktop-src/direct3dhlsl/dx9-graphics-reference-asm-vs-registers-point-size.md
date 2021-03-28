---
title: Регистр размера точки
description: Этот выходной регистр шейдера вершин содержит данные о размере точек вершин.
ms.assetid: 1aa6cd7d-9d29-4e7e-8448-8b9a6b251a02
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 36dbc6dc20d61baf4e0820dd0b6e10d3e6e918ae
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104410860"
---
# <a name="point-size-register"></a><span data-ttu-id="7b0d0-103">Регистр размера точки</span><span class="sxs-lookup"><span data-stu-id="7b0d0-103">Point Size Register</span></span>

<span data-ttu-id="7b0d0-104">Этот выходной регистр шейдера вершин содержит данные о размере точек вершин.</span><span class="sxs-lookup"><span data-stu-id="7b0d0-104">This vertex shader output register contains per-vertex point size data.</span></span>



| <span data-ttu-id="7b0d0-105">Версии шейдеров вершин</span><span class="sxs-lookup"><span data-stu-id="7b0d0-105">Vertex shader versions</span></span> | <span data-ttu-id="7b0d0-106">1\_1</span><span class="sxs-lookup"><span data-stu-id="7b0d0-106">1\_1</span></span> | <span data-ttu-id="7b0d0-107">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="7b0d0-107">2\_0</span></span> | <span data-ttu-id="7b0d0-108">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="7b0d0-108">2\_sw</span></span> | <span data-ttu-id="7b0d0-109">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="7b0d0-109">2\_x</span></span> | <span data-ttu-id="7b0d0-110">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="7b0d0-110">3\_0</span></span> | <span data-ttu-id="7b0d0-111">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="7b0d0-111">3\_sw</span></span> |
|------------------------|------|------|-------|------|------|-------|
| <span data-ttu-id="7b0d0-112">Регистр размера точки</span><span class="sxs-lookup"><span data-stu-id="7b0d0-112">Point Size Register</span></span>    | <span data-ttu-id="7b0d0-113">x</span><span class="sxs-lookup"><span data-stu-id="7b0d0-113">x</span></span>    | <span data-ttu-id="7b0d0-114">x</span><span class="sxs-lookup"><span data-stu-id="7b0d0-114">x</span></span>    | <span data-ttu-id="7b0d0-115">x</span><span class="sxs-lookup"><span data-stu-id="7b0d0-115">x</span></span>     | <span data-ttu-id="7b0d0-116">x</span><span class="sxs-lookup"><span data-stu-id="7b0d0-116">x</span></span>    | <span data-ttu-id="7b0d0-117">x</span><span class="sxs-lookup"><span data-stu-id="7b0d0-117">x</span></span>    | <span data-ttu-id="7b0d0-118">x</span><span class="sxs-lookup"><span data-stu-id="7b0d0-118">x</span></span>     |



 

<span data-ttu-id="7b0d0-119">Регистр состоит из свойств, определяющих принцип работы каждой ККМ.</span><span class="sxs-lookup"><span data-stu-id="7b0d0-119">A register consists of properties that determine how each register behaves.</span></span>



| <span data-ttu-id="7b0d0-120">Свойство</span><span class="sxs-lookup"><span data-stu-id="7b0d0-120">Property</span></span>        | <span data-ttu-id="7b0d0-121">Описание</span><span class="sxs-lookup"><span data-stu-id="7b0d0-121">Description</span></span>                                                                                     |
|-----------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b0d0-122">Имя</span><span class="sxs-lookup"><span data-stu-id="7b0d0-122">Name</span></span>            | <span data-ttu-id="7b0d0-123">Решает</span><span class="sxs-lookup"><span data-stu-id="7b0d0-123">oPts</span></span>                                                                                            |
| <span data-ttu-id="7b0d0-124">Count</span><span class="sxs-lookup"><span data-stu-id="7b0d0-124">Count</span></span>           | <span data-ttu-id="7b0d0-125">1 вектор, из которого можно использовать только один компонент, и должен быть задан маской компонента.</span><span class="sxs-lookup"><span data-stu-id="7b0d0-125">1 vector, of which of only 1 component can be used and must be specified by the component mask.</span></span> |
| <span data-ttu-id="7b0d0-126">Разрешения ввода-вывода</span><span class="sxs-lookup"><span data-stu-id="7b0d0-126">I/O permissions</span></span> | <span data-ttu-id="7b0d0-127">Доступный только на запись.</span><span class="sxs-lookup"><span data-stu-id="7b0d0-127">Write-only.</span></span>                                                                                     |



 

<span data-ttu-id="7b0d0-128">Используется только скалярный x-компонент размера точки.</span><span class="sxs-lookup"><span data-stu-id="7b0d0-128">Only the scalar x-component of the point size is used.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7b0d0-129">См. также</span><span class="sxs-lookup"><span data-stu-id="7b0d0-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7b0d0-130">Регистры шейдеров вершин</span><span class="sxs-lookup"><span data-stu-id="7b0d0-130">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




