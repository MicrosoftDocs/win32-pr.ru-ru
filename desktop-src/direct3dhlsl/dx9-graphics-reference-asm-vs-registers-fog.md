---
title: Регистр тумана
description: Этот выходной регистр шейдера вершин содержит цвет тумана для вершины.
ms.assetid: b2b06aa9-ad75-48df-857d-fd8719176713
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3c3f0e39c0670176b6233f61f0ba50596c92ca4d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104983712"
---
# <a name="fog-register"></a><span data-ttu-id="0082f-103">Регистр тумана</span><span class="sxs-lookup"><span data-stu-id="0082f-103">Fog Register</span></span>

<span data-ttu-id="0082f-104">Этот выходной регистр шейдера вершин содержит цвет тумана для вершины.</span><span class="sxs-lookup"><span data-stu-id="0082f-104">This vertex shader output register contains a per-vertex fog color.</span></span>

<span data-ttu-id="0082f-105">Регистр состоит из свойств, определяющих принцип работы каждой ККМ.</span><span class="sxs-lookup"><span data-stu-id="0082f-105">A register consists of properties that determine how each register behaves.</span></span>



| <span data-ttu-id="0082f-106">Свойство</span><span class="sxs-lookup"><span data-stu-id="0082f-106">Property</span></span>        | <span data-ttu-id="0082f-107">Описание</span><span class="sxs-lookup"><span data-stu-id="0082f-107">Description</span></span>                                                                                     |
|-----------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0082f-108">Имя</span><span class="sxs-lookup"><span data-stu-id="0082f-108">Name</span></span>            | <span data-ttu-id="0082f-109">офог</span><span class="sxs-lookup"><span data-stu-id="0082f-109">oFog</span></span>                                                                                            |
| <span data-ttu-id="0082f-110">Count</span><span class="sxs-lookup"><span data-stu-id="0082f-110">Count</span></span>           | <span data-ttu-id="0082f-111">Один вектор, из которого можно использовать только один компонент и должен быть задан маской компонента</span><span class="sxs-lookup"><span data-stu-id="0082f-111">One vector, of which only one component can be used and must be specified by the component mask</span></span> |
| <span data-ttu-id="0082f-112">Разрешения ввода-вывода</span><span class="sxs-lookup"><span data-stu-id="0082f-112">I/O permissions</span></span> | <span data-ttu-id="0082f-113">Доступный только на запись.</span><span class="sxs-lookup"><span data-stu-id="0082f-113">Write-only.</span></span>                                                                                     |



 

<span data-ttu-id="0082f-114">Регистры значений выходных тумана.</span><span class="sxs-lookup"><span data-stu-id="0082f-114">The output fog value registers.</span></span> <span data-ttu-id="0082f-115">Значение — это коэффициент тумана для интерполяции, который затем направляется в таблицу тумана.</span><span class="sxs-lookup"><span data-stu-id="0082f-115">The value is the fog factor to be interpolated and then routed to the fog table.</span></span> <span data-ttu-id="0082f-116">Используется только скалярный компонент x-компонента тумана.</span><span class="sxs-lookup"><span data-stu-id="0082f-116">Only the scalar x-component of the fog is used.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0082f-117">См. также</span><span class="sxs-lookup"><span data-stu-id="0082f-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0082f-118">Регистры шейдеров вершин</span><span class="sxs-lookup"><span data-stu-id="0082f-118">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




