---
title: Общие атрибуты ресурсов
description: Инструкции определения ресурсов, поддерживаемые в 16-разрядных Windows, включают параметр Load-MEM, указывающий характеристики загрузки и памяти ресурса.
ms.assetid: 53740997-854b-447c-9ab1-de8e17c0de1e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa15ae7207c80737e284151f0dfd3d7981935943
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105700599"
---
# <a name="common-resource-attributes"></a><span data-ttu-id="b0e53-103">Общие атрибуты ресурсов</span><span class="sxs-lookup"><span data-stu-id="b0e53-103">Common Resource Attributes</span></span>

<span data-ttu-id="b0e53-104">Инструкции определения ресурсов, поддерживаемые в 16-разрядных Windows, включают параметр *Load-MEM* , указывающий характеристики загрузки и памяти ресурса.</span><span class="sxs-lookup"><span data-stu-id="b0e53-104">The resource-definition statements supported on 16-bit Windows include a *load-mem* option that specifies the loading and memory characteristics of the resource.</span></span> <span data-ttu-id="b0e53-105">Эти атрибуты разрешены в скриптах ресурсов для обратной совместимости, но они не учитываются.</span><span class="sxs-lookup"><span data-stu-id="b0e53-105">These attributes are permitted in resource scripts for backward compatibility, but they are ignored.</span></span> <span data-ttu-id="b0e53-106">Ресурсы Windows загружаются при загрузке соответствующего модуля и освобождаются при выгрузке модуля.</span><span class="sxs-lookup"><span data-stu-id="b0e53-106">Windows resources are loaded when the corresponding module is loaded, and are freed when the module is unloaded.</span></span>

## <a name="load-attributes"></a><span data-ttu-id="b0e53-107">Загрузить атрибуты</span><span class="sxs-lookup"><span data-stu-id="b0e53-107">Load Attributes</span></span>

<span data-ttu-id="b0e53-108">Атрибуты нагрузки указывают время загрузки ресурса.</span><span class="sxs-lookup"><span data-stu-id="b0e53-108">The load attributes specify when the resource is to be loaded.</span></span> <span data-ttu-id="b0e53-109">Параметр Load должен быть одним из следующих атрибутов.</span><span class="sxs-lookup"><span data-stu-id="b0e53-109">The load parameter must be one of the following attributes.</span></span>



| <span data-ttu-id="b0e53-110">attribute</span><span class="sxs-lookup"><span data-stu-id="b0e53-110">Attribute</span></span>      | <span data-ttu-id="b0e53-111">Описание</span><span class="sxs-lookup"><span data-stu-id="b0e53-111">Description</span></span>                                                                  |
|----------------|------------------------------------------------------------------------------|
| <span data-ttu-id="b0e53-112">**Установка**</span><span class="sxs-lookup"><span data-stu-id="b0e53-112">**PRELOAD**</span></span>    | <span data-ttu-id="b0e53-113">Не обрабатывается.</span><span class="sxs-lookup"><span data-stu-id="b0e53-113">Ignored.</span></span> <span data-ttu-id="b0e53-114">В 16-разрядных Windows ресурс загружается с исполняемым файлом.</span><span class="sxs-lookup"><span data-stu-id="b0e53-114">In 16-bit Windows, the resource is loaded with the executable file.</span></span> |
| <span data-ttu-id="b0e53-115">**лоадонкалл**</span><span class="sxs-lookup"><span data-stu-id="b0e53-115">**LOADONCALL**</span></span> | <span data-ttu-id="b0e53-116">Не обрабатывается.</span><span class="sxs-lookup"><span data-stu-id="b0e53-116">Ignored.</span></span> <span data-ttu-id="b0e53-117">В 16-разрядных Windows ресурс загружается при вызове.</span><span class="sxs-lookup"><span data-stu-id="b0e53-117">In 16-bit Windows, the resource is loaded when called.</span></span>              |



 

## <a name="memory-attributes"></a><span data-ttu-id="b0e53-118">Атрибуты памяти</span><span class="sxs-lookup"><span data-stu-id="b0e53-118">Memory Attributes</span></span>

<span data-ttu-id="b0e53-119">Атрибуты памяти указывают, является ли ресурс фиксированным или перемещаемым, является ли он недоступным и является ли он чистым.</span><span class="sxs-lookup"><span data-stu-id="b0e53-119">The memory attributes specify whether the resource is fixed or movable, whether it is discardable, and whether it is pure.</span></span> <span data-ttu-id="b0e53-120">Параметр Memory может быть одним или несколькими следующими атрибутами.</span><span class="sxs-lookup"><span data-stu-id="b0e53-120">The memory parameter can be one or more of the following attributes.</span></span>



| <span data-ttu-id="b0e53-121">attribute</span><span class="sxs-lookup"><span data-stu-id="b0e53-121">Attribute</span></span>       | <span data-ttu-id="b0e53-122">Описание</span><span class="sxs-lookup"><span data-stu-id="b0e53-122">Description</span></span>                                                                                                                               |
|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0e53-123">**FIXED**</span><span class="sxs-lookup"><span data-stu-id="b0e53-123">**FIXED**</span></span>       | <span data-ttu-id="b0e53-124">Не обрабатывается.</span><span class="sxs-lookup"><span data-stu-id="b0e53-124">Ignored.</span></span> <span data-ttu-id="b0e53-125">В 16-разрядных Windows ресурс остается в фиксированном расположении в памяти.</span><span class="sxs-lookup"><span data-stu-id="b0e53-125">In 16-bit Windows, the resource remains at a fixed memory location.</span></span>                                                              |
| <span data-ttu-id="b0e53-126">**MOVEABLE**</span><span class="sxs-lookup"><span data-stu-id="b0e53-126">**MOVEABLE**</span></span>    | <span data-ttu-id="b0e53-127">Не обрабатывается.</span><span class="sxs-lookup"><span data-stu-id="b0e53-127">Ignored.</span></span> <span data-ttu-id="b0e53-128">В 16-разрядных Windows ресурс можно переместить, если это необходимо для сжатия памяти.</span><span class="sxs-lookup"><span data-stu-id="b0e53-128">In 16-bit Windows, the resource can be moved if necessary to compact memory.</span></span>                                                     |
| <span data-ttu-id="b0e53-129">**ОТКЛОНЕНо**</span><span class="sxs-lookup"><span data-stu-id="b0e53-129">**DISCARDABLE**</span></span> | <span data-ttu-id="b0e53-130">Не обрабатывается.</span><span class="sxs-lookup"><span data-stu-id="b0e53-130">Ignored.</span></span> <span data-ttu-id="b0e53-131">В 16-разрядных Windows ресурс может быть отклонен, если он больше не нужен.</span><span class="sxs-lookup"><span data-stu-id="b0e53-131">In 16-bit Windows, the resource can be discarded if no longer needed.</span></span>                                                            |
| <span data-ttu-id="b0e53-132">**ЧИСТЫМИ**</span><span class="sxs-lookup"><span data-stu-id="b0e53-132">**PURE**</span></span>        | <span data-ttu-id="b0e53-133">Не обрабатывается.</span><span class="sxs-lookup"><span data-stu-id="b0e53-133">Ignored.</span></span> <span data-ttu-id="b0e53-134">Принимается на совместимость с существующими скриптами ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b0e53-134">Accepted for compatibility with existing resource scripts.</span></span>                                                                       |
| <span data-ttu-id="b0e53-135">**НЕЧИСТЫМИ**</span><span class="sxs-lookup"><span data-stu-id="b0e53-135">**IMPURE**</span></span>      | <span data-ttu-id="b0e53-136">Не обрабатывается.</span><span class="sxs-lookup"><span data-stu-id="b0e53-136">Ignored.</span></span> <span data-ttu-id="b0e53-137">Принимается на совместимость с существующими скриптами ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b0e53-137">Accepted for compatibility with existing resource scripts.</span></span>                                                                       |
| <span data-ttu-id="b0e53-138">**ИСПОЛЬЗУЕМЫЙ**</span><span class="sxs-lookup"><span data-stu-id="b0e53-138">**SHARED**</span></span>      | <span data-ttu-id="b0e53-139">Не обрабатывается.</span><span class="sxs-lookup"><span data-stu-id="b0e53-139">Ignored.</span></span> <span data-ttu-id="b0e53-140">В 16-разрядных Windows для обычных модулей параметр SHARed не учитывается.</span><span class="sxs-lookup"><span data-stu-id="b0e53-140">In 16-bit Windows, SHARED is ignored for regular modules.</span></span> <span data-ttu-id="b0e53-141">Для ресурса из модуля ПЗУ Windows память является общей.</span><span class="sxs-lookup"><span data-stu-id="b0e53-141">For a resource from a ROM Windows module, the memory is shared.</span></span>        |
| <span data-ttu-id="b0e53-142">**НЕ ЯВЛЯЮЩАЯСЯ общей**</span><span class="sxs-lookup"><span data-stu-id="b0e53-142">**NONSHARED**</span></span>   | <span data-ttu-id="b0e53-143">Не обрабатывается.</span><span class="sxs-lookup"><span data-stu-id="b0e53-143">Ignored.</span></span> <span data-ttu-id="b0e53-144">В 16-разрядных Windows для обычных модулей игнорируется необщий доступ.</span><span class="sxs-lookup"><span data-stu-id="b0e53-144">In 16-bit Windows, NONSHARED is ignored for regular modules.</span></span> <span data-ttu-id="b0e53-145">Для ресурса из модуля ПЗУ Windows память не используется совместно.</span><span class="sxs-lookup"><span data-stu-id="b0e53-145">For a resource from a ROM Windows module, the memory is not shared.</span></span> |



 

 

 




