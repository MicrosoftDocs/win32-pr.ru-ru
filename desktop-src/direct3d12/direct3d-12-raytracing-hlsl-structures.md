---
title: Структуры HLSL райтраЦинг (Direct3D 12)
description: Следующие структуры HLSL поддерживают конвейер Direct3D 12 райтраЦинг.
ms.assetid: ''
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c48ad6bac76e200587ec76d42dfa9c86b23cd23
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/23/2019
ms.locfileid: "105719077"
---
# <a name="raytracing-hlsl-structures-direct3d-12"></a><span data-ttu-id="7609b-103">Структуры HLSL райтраЦинг (Direct3D 12)</span><span class="sxs-lookup"><span data-stu-id="7609b-103">Raytracing HLSL structures (Direct3D 12)</span></span>

<span data-ttu-id="7609b-104">Следующие структуры HLSL поддерживают конвейер Direct3D 12 райтраЦинг.</span><span class="sxs-lookup"><span data-stu-id="7609b-104">The following HLSL structures support the Direct3D 12 raytracing pipeline.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="7609b-105">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="7609b-105">In this section</span></span>



| <span data-ttu-id="7609b-106">Раздел</span><span class="sxs-lookup"><span data-stu-id="7609b-106">Topic</span></span>                                                                                                       | <span data-ttu-id="7609b-107">Описание</span><span class="sxs-lookup"><span data-stu-id="7609b-107">Description</span></span>                                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7609b-108">**Структура параметров вызова**</span><span class="sxs-lookup"><span data-stu-id="7609b-108">**Call Parameter Structure**</span></span>](call-parameter-structure.md)<br/>                              | <span data-ttu-id="7609b-109">Определяемая пользователем структура, предоставляемая как аргумент InOut для вызова Каллшадер и как параметр InOut для вызываемого шейдера.</span><span class="sxs-lookup"><span data-stu-id="7609b-109">A user-defined structure provided as an inout argument to a CallShader call, and as an inout parameter for the callable shader.</span></span><br/>                                                                                                                                                                                                                                              |
| [<span data-ttu-id="7609b-110">**Структура атрибутов пересечения**</span><span class="sxs-lookup"><span data-stu-id="7609b-110">**Intersection Attributes Structure**</span></span>](intersection-attributes.md)<br/>                              | <span data-ttu-id="7609b-111">Определяемая пользователем структура, предоставляемая как аргумент Inout в вызове [**трацерай**](traceray-function.md) , и как параметр Inout в типах шейдеров, которые могут обращаться к полезной нагрузке лучей.</span><span class="sxs-lookup"><span data-stu-id="7609b-111">A user-defined structure that is provided as an inout argument in a [**TraceRay**](traceray-function.md) call, and as an inout parameter in the shader types that may access the ray payload.</span></span><br/>                                                                                                                                                                                                                                              |
| [<span data-ttu-id="7609b-112">**Структура полезной нагрузки лучей**</span><span class="sxs-lookup"><span data-stu-id="7609b-112">**Ray Payload Structure**</span></span>](ray-payload.md)<br/>                              | <span data-ttu-id="7609b-113">Определяемая пользователем структура, предоставляемая как аргумент Inout в вызове [**трацерай**](traceray-function.md) , и как параметр Inout в типах шейдеров, которые могут обращаться к полезной нагрузке лучей.</span><span class="sxs-lookup"><span data-stu-id="7609b-113">A user-defined structure that is provided as an inout argument in a [**TraceRay**](traceray-function.md) call, and as an inout parameter in the shader types that may access the ray payload.</span></span><br/>                                                                                                                                                                                                                                              |
| [<span data-ttu-id="7609b-114">**Структура RayDesc**</span><span class="sxs-lookup"><span data-stu-id="7609b-114">**RayDesc Structure**</span></span>](raydesc.md)<br/>                              | <span data-ttu-id="7609b-115">Флаги, передаваемые функции [**трацерай**](traceray-function.md) для переопределения прозрачности, отбора и поведения при начальном выходе.</span><span class="sxs-lookup"><span data-stu-id="7609b-115">Flags passed to the [**TraceRay**](traceray-function.md) function to override transparency, culling, and early-out behavior.</span></span><br/>                                                                                                                                                                                                                                              |





 

## <a name="related-topics"></a><span data-ttu-id="7609b-116">См. также</span><span class="sxs-lookup"><span data-stu-id="7609b-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7609b-117">Справочник по основным</span><span class="sxs-lookup"><span data-stu-id="7609b-117">Core Reference</span></span>](direct3d-12-core-reference.md)
</dt> <dt>

[<span data-ttu-id="7609b-118">Справочник по Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="7609b-118">Direct3D 12 Reference</span></span>](direct3d-12-reference.md)
</dt> </dl>

 

 





