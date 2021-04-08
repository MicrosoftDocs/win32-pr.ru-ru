---
description: ICE25 проверяет, удовлетворяет ли MSI-файл всем внутренним зависимостям модуля слияния и исключениям.
ms.assetid: e6e3ea44-a1d4-451a-b326-e8fb7ed4adeb
title: ICE25
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0d966c4c374d6e61e30b44a41ad88bed8bf907f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910912"
---
# <a name="ice25"></a><span data-ttu-id="eb6e5-103">ICE25</span><span class="sxs-lookup"><span data-stu-id="eb6e5-103">ICE25</span></span>

<span data-ttu-id="eb6e5-104">ICE25 проверяет, удовлетворяет ли MSI-файл всем внутренним зависимостям [модуля слияния](merge-modules.md) и исключениям.</span><span class="sxs-lookup"><span data-stu-id="eb6e5-104">ICE25 validates that a .msi file satisfies all of its internal [merge module](merge-modules.md) dependencies and exclusions.</span></span> <span data-ttu-id="eb6e5-105">ICE проверяет следующее:</span><span class="sxs-lookup"><span data-stu-id="eb6e5-105">ICE validates the following:</span></span>

-   <span data-ttu-id="eb6e5-106">Все зависимости модуля слияния, указанные в [таблице модуледепенденци](moduledependency-table.md) файла. msi, удовлетворяются по крайней мере в одном модуле слияния, указанном в [таблице ModuleSignature](modulesignature-table.md).</span><span class="sxs-lookup"><span data-stu-id="eb6e5-106">That all merge module dependencies indicated in the .msi file's [ModuleDependency table](moduledependency-table.md) are satisfied by at least one merge module listed in the [ModuleSignature table](modulesignature-table.md).</span></span>
-   <span data-ttu-id="eb6e5-107">Что ни один из исключенных модулей слияния в [таблице модуликсклусион](moduleexclusion-table.md) несовместим с модулями слияния, перечисленными в [таблице ModuleSignature](modulesignature-table.md).</span><span class="sxs-lookup"><span data-stu-id="eb6e5-107">That none of the excluded merge modules in the [ModuleExclusion table](moduleexclusion-table.md) are incompatible with the merge modules listed in the [ModuleSignature table](modulesignature-table.md).</span></span>

## <a name="result"></a><span data-ttu-id="eb6e5-108">Результат</span><span class="sxs-lookup"><span data-stu-id="eb6e5-108">Result</span></span>

<span data-ttu-id="eb6e5-109">ICE25 отправляет сообщение об ошибке, если MSI-файл ранее был объединен с несовместимым модулем слияния или если он не был объединен с необходимым модулем слияния.</span><span class="sxs-lookup"><span data-stu-id="eb6e5-109">ICE25 posts an error message if .msi file has previously been merged with an incompatible merge module or if it has not been merged with a necessary merge module.</span></span>

## <a name="example"></a><span data-ttu-id="eb6e5-110">Пример</span><span class="sxs-lookup"><span data-stu-id="eb6e5-110">Example</span></span>

<span data-ttu-id="eb6e5-111">ICE25 отправляет следующие ошибки для показанного примера.</span><span class="sxs-lookup"><span data-stu-id="eb6e5-111">ICE25 posts the following errors for the example shown.</span></span>

``` syntax
Dependency failure: Need ModuleX@0 v2.0 
Module ModuleB@1033 v1.0 is excluded.
```

[<span data-ttu-id="eb6e5-112">Таблица ModuleSignature</span><span class="sxs-lookup"><span data-stu-id="eb6e5-112">ModuleSignature Table</span></span>](modulesignature-table.md)



| <span data-ttu-id="eb6e5-113">ModuleID</span><span class="sxs-lookup"><span data-stu-id="eb6e5-113">ModuleID</span></span> | <span data-ttu-id="eb6e5-114">Язык</span><span class="sxs-lookup"><span data-stu-id="eb6e5-114">Language</span></span> | <span data-ttu-id="eb6e5-115">Версия</span><span class="sxs-lookup"><span data-stu-id="eb6e5-115">Version</span></span> |
|----------|----------|---------|
| <span data-ttu-id="eb6e5-116">Модуль а</span><span class="sxs-lookup"><span data-stu-id="eb6e5-116">ModuleA</span></span>  | <span data-ttu-id="eb6e5-117">0</span><span class="sxs-lookup"><span data-stu-id="eb6e5-117">0</span></span>        | <span data-ttu-id="eb6e5-118">1.0</span><span class="sxs-lookup"><span data-stu-id="eb6e5-118">1.0</span></span>     |
| <span data-ttu-id="eb6e5-119">модулеб</span><span class="sxs-lookup"><span data-stu-id="eb6e5-119">ModuleB</span></span>  | <span data-ttu-id="eb6e5-120">1033</span><span class="sxs-lookup"><span data-stu-id="eb6e5-120">1033</span></span>     | <span data-ttu-id="eb6e5-121">1.0</span><span class="sxs-lookup"><span data-stu-id="eb6e5-121">1.0</span></span>     |



 

[<span data-ttu-id="eb6e5-122">Таблица Модуледепенденци</span><span class="sxs-lookup"><span data-stu-id="eb6e5-122">ModuleDependency Table</span></span>](moduledependency-table.md)



| <span data-ttu-id="eb6e5-123">ModuleID</span><span class="sxs-lookup"><span data-stu-id="eb6e5-123">ModuleID</span></span> | <span data-ttu-id="eb6e5-124">модулелангуаже</span><span class="sxs-lookup"><span data-stu-id="eb6e5-124">ModuleLanguage</span></span> | <span data-ttu-id="eb6e5-125">рекуиредид</span><span class="sxs-lookup"><span data-stu-id="eb6e5-125">RequiredID</span></span> | <span data-ttu-id="eb6e5-126">рекуиредлангуаже</span><span class="sxs-lookup"><span data-stu-id="eb6e5-126">RequiredLanguage</span></span> | <span data-ttu-id="eb6e5-127">RequiredVersion</span><span class="sxs-lookup"><span data-stu-id="eb6e5-127">RequiredVersion</span></span> |
|----------|----------------|------------|------------------|-----------------|
| <span data-ttu-id="eb6e5-128">Модуль а</span><span class="sxs-lookup"><span data-stu-id="eb6e5-128">ModuleA</span></span>  | <span data-ttu-id="eb6e5-129">0</span><span class="sxs-lookup"><span data-stu-id="eb6e5-129">0</span></span>              | <span data-ttu-id="eb6e5-130">модулекс</span><span class="sxs-lookup"><span data-stu-id="eb6e5-130">ModuleX</span></span>    | <span data-ttu-id="eb6e5-131">0</span><span class="sxs-lookup"><span data-stu-id="eb6e5-131">0</span></span>                | <span data-ttu-id="eb6e5-132">2.0</span><span class="sxs-lookup"><span data-stu-id="eb6e5-132">2.0</span></span>             |



 

[<span data-ttu-id="eb6e5-133">Таблица Модуликсклусион</span><span class="sxs-lookup"><span data-stu-id="eb6e5-133">ModuleExclusion Table</span></span>](moduleexclusion-table.md)



| <span data-ttu-id="eb6e5-134">ModuleID</span><span class="sxs-lookup"><span data-stu-id="eb6e5-134">ModuleID</span></span> | <span data-ttu-id="eb6e5-135">модулелангуаже</span><span class="sxs-lookup"><span data-stu-id="eb6e5-135">ModuleLanguage</span></span> | <span data-ttu-id="eb6e5-136">ексклудедид</span><span class="sxs-lookup"><span data-stu-id="eb6e5-136">ExcludedID</span></span> | <span data-ttu-id="eb6e5-137">ексклудедлангуаже</span><span class="sxs-lookup"><span data-stu-id="eb6e5-137">ExcludedLanguage</span></span> | <span data-ttu-id="eb6e5-138">ексклудедминверсион</span><span class="sxs-lookup"><span data-stu-id="eb6e5-138">ExcludedMinVersion</span></span> | <span data-ttu-id="eb6e5-139">ексклудедмаксверсион</span><span class="sxs-lookup"><span data-stu-id="eb6e5-139">ExcludedMaxVersion</span></span> |
|----------|----------------|------------|------------------|--------------------|--------------------|
| <span data-ttu-id="eb6e5-140">Модуль а</span><span class="sxs-lookup"><span data-stu-id="eb6e5-140">ModuleA</span></span>  | <span data-ttu-id="eb6e5-141">0</span><span class="sxs-lookup"><span data-stu-id="eb6e5-141">0</span></span>              | <span data-ttu-id="eb6e5-142">модулеб</span><span class="sxs-lookup"><span data-stu-id="eb6e5-142">ModuleB</span></span>    | <span data-ttu-id="eb6e5-143">1033</span><span class="sxs-lookup"><span data-stu-id="eb6e5-143">1033</span></span>             |                    |                    |



 

## <a name="related-topics"></a><span data-ttu-id="eb6e5-144">См. также</span><span class="sxs-lookup"><span data-stu-id="eb6e5-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eb6e5-145">Справочник по ICE</span><span class="sxs-lookup"><span data-stu-id="eb6e5-145">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



