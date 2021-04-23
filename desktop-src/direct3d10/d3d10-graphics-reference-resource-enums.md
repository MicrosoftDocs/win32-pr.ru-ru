---
description: Следующие перечисления используются для указания сведений о создании ресурсов и доступе к ним во время подготовки к просмотру.
ms.assetid: c986b22c-2960-4571-98bc-028c9f41ec65
title: Перечисления ресурсов (графика Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04ae6e115fe8ae9a731e5778b986940cb17a915d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072550"
---
# <a name="resource-enumerations-direct3d-10-graphics"></a><span data-ttu-id="ffa23-103">Перечисления ресурсов (графика Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="ffa23-103">Resource Enumerations (Direct3D 10 Graphics)</span></span>

<span data-ttu-id="ffa23-104">Следующие перечисления используются для указания сведений о создании ресурсов и доступе к ним во время подготовки к просмотру.</span><span class="sxs-lookup"><span data-stu-id="ffa23-104">The following enumerations are used to specify information about how resources are created and accessed during rendering.</span></span>



| <span data-ttu-id="ffa23-105">Перечисление</span><span class="sxs-lookup"><span data-stu-id="ffa23-105">Enumeration</span></span>                                                     | <span data-ttu-id="ffa23-106">Описание</span><span class="sxs-lookup"><span data-stu-id="ffa23-106">Description</span></span>                                                                                                               |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ffa23-107">**\_Флаг привязки \_ D3D10**</span><span class="sxs-lookup"><span data-stu-id="ffa23-107">**D3D10\_BIND\_FLAG**</span></span>](/windows/desktop/api/D3D10/ne-d3d10-d3d10_bind_flag)                    | <span data-ttu-id="ffa23-108">Определяет, как ресурс будет использоваться конвейером, и определяет, к каким этапам конвейера может быть привязан ресурс.</span><span class="sxs-lookup"><span data-stu-id="ffa23-108">Identifies how a resource will be used by the pipeline and determines which pipeline stage(s) a resource can be bound to.</span></span> |
| [<span data-ttu-id="ffa23-109">**\_ \_ Флаг доступа к ЦП D3D10 \_**</span><span class="sxs-lookup"><span data-stu-id="ffa23-109">**D3D10\_CPU\_ACCESS\_FLAG**</span></span>](/windows/desktop/api/D3D10/ne-d3d10-d3d10_cpu_access_flag)       | <span data-ttu-id="ffa23-110">Указывает типы доступа к ЦП, разрешенные для ресурса.</span><span class="sxs-lookup"><span data-stu-id="ffa23-110">Specifies the types of CPU access allowed for a resource.</span></span>                                                                 |
| [<span data-ttu-id="ffa23-111">**\_Измерение DSV \_ D3D10**</span><span class="sxs-lookup"><span data-stu-id="ffa23-111">**D3D10\_DSV\_DIMENSION**</span></span>](/windows/desktop/api/D3D10/ne-d3d10-d3d10_dsv_dimension)            | <span data-ttu-id="ffa23-112">Указывает, как получить доступ к ресурсу, используемому в представлении трафарета глубины.</span><span class="sxs-lookup"><span data-stu-id="ffa23-112">Specifies how to access a resource that is used in a depth-stencil view.</span></span>                                                  |
| [<span data-ttu-id="ffa23-113">**D3D10 \_ Map**</span><span class="sxs-lookup"><span data-stu-id="ffa23-113">**D3D10\_MAP**</span></span>](/windows/desktop/api/D3D10/ne-d3d10-d3d10_map)                                 | <span data-ttu-id="ffa23-114">Определяет ресурс, который должен быть сопоставлен для чтения и записи ЦП.</span><span class="sxs-lookup"><span data-stu-id="ffa23-114">Identifies a resource to be mapped for reading and writing by the CPU.</span></span>                                                    |
| [<span data-ttu-id="ffa23-115">**\_Флаг D3D10 Map \_**</span><span class="sxs-lookup"><span data-stu-id="ffa23-115">**D3D10\_MAP\_FLAG**</span></span>](/windows/desktop/api/D3D10/ne-d3d10-d3d10_map_flag)                      | <span data-ttu-id="ffa23-116">Указывает, как ЦП должен отвечать на любые методы Map, если GPU еще не завершил работу с ресурсом.</span><span class="sxs-lookup"><span data-stu-id="ffa23-116">Specifies how the CPU should respond to any Map methods when the GPU is not yet finished with the resource.</span></span>               |
| [<span data-ttu-id="ffa23-117">**\_Измерение ресурсов \_ D3D10**</span><span class="sxs-lookup"><span data-stu-id="ffa23-117">**D3D10\_RESOURCE\_DIMENSION**</span></span>](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_dimension)  | <span data-ttu-id="ffa23-118">Определяет тип используемого ресурса.</span><span class="sxs-lookup"><span data-stu-id="ffa23-118">Identifies the type of resource that is in use.</span></span>                                                                           |
| [<span data-ttu-id="ffa23-119">**\_ \_ Флаг прочих ресурсов \_ D3D10**</span><span class="sxs-lookup"><span data-stu-id="ffa23-119">**D3D10\_RESOURCE\_MISC\_FLAG**</span></span>](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_misc_flag) | <span data-ttu-id="ffa23-120">Определяет менее распространенные параметры создания ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ffa23-120">Identifies less common resource creation options.</span></span>                                                                         |
| [<span data-ttu-id="ffa23-121">**\_Измерение D3D10 РТВ \_**</span><span class="sxs-lookup"><span data-stu-id="ffa23-121">**D3D10\_RTV\_DIMENSION**</span></span>](/windows/desktop/api/D3D10/ne-d3d10-d3d10_rtv_dimension)            | <span data-ttu-id="ffa23-122">Указывает, как получить доступ к ресурсу, используемому в представлении целевого объекта прорисовки.</span><span class="sxs-lookup"><span data-stu-id="ffa23-122">Specifies how to access a resource used in a render target view.</span></span>                                                          |
| [<span data-ttu-id="ffa23-123">**\_Использование D3D10**</span><span class="sxs-lookup"><span data-stu-id="ffa23-123">**D3D10\_USAGE**</span></span>](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage)                             | <span data-ttu-id="ffa23-124">Определяет, как ожидается чтение и запись ресурса с помощью ЦП и (или) GPU.</span><span class="sxs-lookup"><span data-stu-id="ffa23-124">Identifies how a resource is expected to be read and written by the CPU and/or the GPU.</span></span>                                   |



 

## <a name="related-topics"></a><span data-ttu-id="ffa23-125">См. также</span><span class="sxs-lookup"><span data-stu-id="ffa23-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ffa23-126">Ссылка на ресурс</span><span class="sxs-lookup"><span data-stu-id="ffa23-126">Resource Reference</span></span>](d3d10-graphics-reference-resource.md)
</dt> </dl>

 

 



