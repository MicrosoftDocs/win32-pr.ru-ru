---
description: ICEM08 гарантирует, что модуль не исключит другой модуль, от которого он зависит.
ms.assetid: 56d115b4-7410-4db2-a9af-bc6716f3358d
title: ICEM08
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a9767c6748f5a21d83bddb3b5fe93a0a8d7ea67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265422"
---
# <a name="icem08"></a><span data-ttu-id="c396d-103">ICEM08</span><span class="sxs-lookup"><span data-stu-id="c396d-103">ICEM08</span></span>

<span data-ttu-id="c396d-104">ICEM08 гарантирует, что модуль не исключит другой модуль, от которого он зависит.</span><span class="sxs-lookup"><span data-stu-id="c396d-104">ICEM08 ensures that a module does not exclude another module that it depends on.</span></span>

## <a name="result"></a><span data-ttu-id="c396d-105">Результат</span><span class="sxs-lookup"><span data-stu-id="c396d-105">Result</span></span>

<span data-ttu-id="c396d-106">ICEM08 отправляет сообщение об ошибке, когда модуль исключает другой модуль, от которого он зависит.</span><span class="sxs-lookup"><span data-stu-id="c396d-106">ICEM08 posts an error when a module excludes another module that it depends on.</span></span>

## <a name="example"></a><span data-ttu-id="c396d-107">Пример</span><span class="sxs-lookup"><span data-stu-id="c396d-107">Example</span></span>

<span data-ttu-id="c396d-108">ICEM08 отправляет следующее сообщение об ошибке для модуля, содержащего записи базы данных, показанные в примере.</span><span class="sxs-lookup"><span data-stu-id="c396d-108">ICEM08 posts the following error message for a module containing the database entries shown in the example.</span></span>

``` syntax
Error: This module requires module ModuleB.<GUID> (1033v1.0) but also 
lists it as an exclusion.
```

[<span data-ttu-id="c396d-109">Таблица Модуледепенденци</span><span class="sxs-lookup"><span data-stu-id="c396d-109">ModuleDependency Table</span></span>](moduledependency-table.md)



| <span data-ttu-id="c396d-110">ModuleID</span><span class="sxs-lookup"><span data-stu-id="c396d-110">ModuleID</span></span>             | <span data-ttu-id="c396d-111">модулелангуаже</span><span class="sxs-lookup"><span data-stu-id="c396d-111">ModuleLanguage</span></span> | <span data-ttu-id="c396d-112">рекуиредид</span><span class="sxs-lookup"><span data-stu-id="c396d-112">RequiredID</span></span>           | <span data-ttu-id="c396d-113">рекуиредлангуаже</span><span class="sxs-lookup"><span data-stu-id="c396d-113">RequiredLanguage</span></span> | <span data-ttu-id="c396d-114">RequiredVersion</span><span class="sxs-lookup"><span data-stu-id="c396d-114">RequiredVersion</span></span> |
|----------------------|----------------|----------------------|------------------|-----------------|
| <span data-ttu-id="c396d-115">Модуль а.<GUID></span><span class="sxs-lookup"><span data-stu-id="c396d-115">ModuleA.<GUID></span></span> | <span data-ttu-id="c396d-116">1033</span><span class="sxs-lookup"><span data-stu-id="c396d-116">1033</span></span>           | <span data-ttu-id="c396d-117">Модулеб.<GUID></span><span class="sxs-lookup"><span data-stu-id="c396d-117">ModuleB.<GUID></span></span> | <span data-ttu-id="c396d-118">1033</span><span class="sxs-lookup"><span data-stu-id="c396d-118">1033</span></span>             | <span data-ttu-id="c396d-119">1.0</span><span class="sxs-lookup"><span data-stu-id="c396d-119">1.0</span></span>             |



 

[<span data-ttu-id="c396d-120">Таблица Модуликсклусион</span><span class="sxs-lookup"><span data-stu-id="c396d-120">ModuleExclusion Table</span></span>](moduleexclusion-table.md)



| <span data-ttu-id="c396d-121">ModuleID</span><span class="sxs-lookup"><span data-stu-id="c396d-121">ModuleID</span></span>             | <span data-ttu-id="c396d-122">модулелангуаже</span><span class="sxs-lookup"><span data-stu-id="c396d-122">ModuleLanguage</span></span> | <span data-ttu-id="c396d-123">ексклудедид</span><span class="sxs-lookup"><span data-stu-id="c396d-123">ExcludedID</span></span>           | <span data-ttu-id="c396d-124">ексклудедлангуаже</span><span class="sxs-lookup"><span data-stu-id="c396d-124">ExcludedLanguage</span></span> | <span data-ttu-id="c396d-125">ексклудедминверсион</span><span class="sxs-lookup"><span data-stu-id="c396d-125">ExcludedMinVersion</span></span> | <span data-ttu-id="c396d-126">ексклудедмаксверсион</span><span class="sxs-lookup"><span data-stu-id="c396d-126">ExcludedMaxVersion</span></span> |
|----------------------|----------------|----------------------|------------------|--------------------|--------------------|
| <span data-ttu-id="c396d-127">Модуль а.<GUID></span><span class="sxs-lookup"><span data-stu-id="c396d-127">ModuleA.<GUID></span></span> | <span data-ttu-id="c396d-128">1033</span><span class="sxs-lookup"><span data-stu-id="c396d-128">1033</span></span>           | <span data-ttu-id="c396d-129">Модулеб.<GUID></span><span class="sxs-lookup"><span data-stu-id="c396d-129">ModuleB.<GUID></span></span> | <span data-ttu-id="c396d-130">1033</span><span class="sxs-lookup"><span data-stu-id="c396d-130">1033</span></span>             |                    | <span data-ttu-id="c396d-131">1.0</span><span class="sxs-lookup"><span data-stu-id="c396d-131">1.0</span></span>                |



 

<span data-ttu-id="c396d-132">Чтобы устранить эту ошибку, удалите либо зависимость, либо исключение.</span><span class="sxs-lookup"><span data-stu-id="c396d-132">To fix the error, remove either the dependency or the exclusion.</span></span> <span data-ttu-id="c396d-133">Если Модулеб является зависимостью (Рекуиредид) модуля a, его нельзя исключить (как показано в столбце Екслудедид таблицы Модуликсклусион).</span><span class="sxs-lookup"><span data-stu-id="c396d-133">If ModuleB is a dependency (RequiredID) of ModuleA, you cannot exclude it (as shown in the ExludedID column of the ModuleExclusion table).</span></span> <span data-ttu-id="c396d-134">Если необходимо исключить Модулеб, необходимо удалить зависимость от модуля а.</span><span class="sxs-lookup"><span data-stu-id="c396d-134">If you must exclude ModuleB, then you must remove ModuleA's dependency on it.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c396d-135">См. также</span><span class="sxs-lookup"><span data-stu-id="c396d-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c396d-136">Ссылка на модуль слияния ICE</span><span class="sxs-lookup"><span data-stu-id="c396d-136">Merge Module ICE Reference</span></span>](merge-module-ice-reference.md)
</dt> </dl>

 

 



