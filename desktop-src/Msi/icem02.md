---
description: ICEM02 проверяет, что все зависимости и исключения модуля связаны с текущим модулем.
ms.assetid: c7d77cb6-0ee6-4857-a749-7908e1c5fcda
title: ICEM02
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9a976132dbfad42e95f4141bc00adb48a544c1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263433"
---
# <a name="icem02"></a><span data-ttu-id="94cf4-103">ICEM02</span><span class="sxs-lookup"><span data-stu-id="94cf4-103">ICEM02</span></span>

<span data-ttu-id="94cf4-104">ICEM02 проверяет, что все зависимости и исключения модуля связаны с текущим модулем.</span><span class="sxs-lookup"><span data-stu-id="94cf4-104">ICEM02 verifies that all the module dependencies and exclusions are related to the current module.</span></span>

<span data-ttu-id="94cf4-105">Модуль слияния ICEs хранится в файле слияния Module. CUB, который называется Мержемод. CUB, а не в файле. CUB, содержащем значение ICEs, используемое для проверки пакета.</span><span class="sxs-lookup"><span data-stu-id="94cf4-105">Merge module ICEs are stored in a merge module .cub file called Mergemod.cub and not in the .cub file containing the ICEs used for package validation.</span></span>

## <a name="result"></a><span data-ttu-id="94cf4-106">Результат</span><span class="sxs-lookup"><span data-stu-id="94cf4-106">Result</span></span>

<span data-ttu-id="94cf4-107">ICEM02 отправляет сообщения об ошибках, если база данных модуля пытается указать зависимости или исключения, которые не связаны с текущим модулем.</span><span class="sxs-lookup"><span data-stu-id="94cf4-107">ICEM02 posts error messages if the module database attempts to specify dependencies or exclusions that do not relate to the current module.</span></span> <span data-ttu-id="94cf4-108">ICEM02 отправляет сообщение об ошибке, если база данных модуля пытается указать текущий модуль как зависимый или исключенный самим.</span><span class="sxs-lookup"><span data-stu-id="94cf4-108">ICEM02 posts an error message if the module database attempts to specify the current module as dependent or as excluded by itself.</span></span>

## <a name="example"></a><span data-ttu-id="94cf4-109">Пример</span><span class="sxs-lookup"><span data-stu-id="94cf4-109">Example</span></span>

<span data-ttu-id="94cf4-110">ICEM02 будет размещать следующие сообщения об ошибках для модуля, содержащего записи базы данных, показанные ниже.</span><span class="sxs-lookup"><span data-stu-id="94cf4-110">ICEM02 would post the following error messages for a module containing the database entries shown below.</span></span>

``` syntax
The dependency OtherModule.GUID2.1033.OtherModule.GUID3.0 in the 
ModuleDependency table creates a dependency for an unrelated module. A 
module can only define dependencies for itself

This module is listed as depending on itself!

The exclusion OtherModule.GUID2.1033.OtherModule.GUID3.0 in the 
ModuleExclusion table creates an excluded module for an unrelated 
module. A module can only define exclusions for itself.

This module excludes itself from the target database!
```

[<span data-ttu-id="94cf4-111">Таблица ModuleSignature</span><span class="sxs-lookup"><span data-stu-id="94cf4-111">ModuleSignature Table</span></span>](modulesignature-table.md)



| <span data-ttu-id="94cf4-112">ModuleID</span><span class="sxs-lookup"><span data-stu-id="94cf4-112">ModuleID</span></span>         | <span data-ttu-id="94cf4-113">Язык</span><span class="sxs-lookup"><span data-stu-id="94cf4-113">Language</span></span> | <span data-ttu-id="94cf4-114">Версия</span><span class="sxs-lookup"><span data-stu-id="94cf4-114">Version</span></span> |
|------------------|----------|---------|
| <span data-ttu-id="94cf4-115">MyModule. *GUID1*</span><span class="sxs-lookup"><span data-stu-id="94cf4-115">MyModule.*GUID1*</span></span> | <span data-ttu-id="94cf4-116">1033</span><span class="sxs-lookup"><span data-stu-id="94cf4-116">1033</span></span>     | <span data-ttu-id="94cf4-117">1.0</span><span class="sxs-lookup"><span data-stu-id="94cf4-117">1.0</span></span>     |



 

[<span data-ttu-id="94cf4-118">Таблица Модуледепенденци</span><span class="sxs-lookup"><span data-stu-id="94cf4-118">ModuleDependency Table</span></span>](moduledependency-table.md)



| <span data-ttu-id="94cf4-119">ModuleID</span><span class="sxs-lookup"><span data-stu-id="94cf4-119">ModuleID</span></span>            | <span data-ttu-id="94cf4-120">модулелангуаже</span><span class="sxs-lookup"><span data-stu-id="94cf4-120">ModuleLanguage</span></span> | <span data-ttu-id="94cf4-121">рекуиредид</span><span class="sxs-lookup"><span data-stu-id="94cf4-121">RequiredID</span></span>          | <span data-ttu-id="94cf4-122">рекуиредлангуаже</span><span class="sxs-lookup"><span data-stu-id="94cf4-122">RequiredLanguage</span></span> | <span data-ttu-id="94cf4-123">RequiredVersion</span><span class="sxs-lookup"><span data-stu-id="94cf4-123">RequiredVersion</span></span> |
|---------------------|----------------|---------------------|------------------|-----------------|
| <span data-ttu-id="94cf4-124">Осермодуле. *GUID2*</span><span class="sxs-lookup"><span data-stu-id="94cf4-124">OtherModule.*GUID2*</span></span> | <span data-ttu-id="94cf4-125">1033</span><span class="sxs-lookup"><span data-stu-id="94cf4-125">1033</span></span>           | <span data-ttu-id="94cf4-126">Осермодуле. *GUID3*</span><span class="sxs-lookup"><span data-stu-id="94cf4-126">OtherModule.*GUID3*</span></span> | <span data-ttu-id="94cf4-127">0</span><span class="sxs-lookup"><span data-stu-id="94cf4-127">0</span></span>                | <span data-ttu-id="94cf4-128">1.0</span><span class="sxs-lookup"><span data-stu-id="94cf4-128">1.0</span></span>             |
| <span data-ttu-id="94cf4-129">MyModule. *GUID1*</span><span class="sxs-lookup"><span data-stu-id="94cf4-129">MyModule.*GUID1*</span></span>    | <span data-ttu-id="94cf4-130">1033</span><span class="sxs-lookup"><span data-stu-id="94cf4-130">1033</span></span>           | <span data-ttu-id="94cf4-131">MyModule. *GUID1*</span><span class="sxs-lookup"><span data-stu-id="94cf4-131">MyModule.*GUID1*</span></span>    | <span data-ttu-id="94cf4-132">1033</span><span class="sxs-lookup"><span data-stu-id="94cf4-132">1033</span></span>             | <span data-ttu-id="94cf4-133">1.2</span><span class="sxs-lookup"><span data-stu-id="94cf4-133">1.2</span></span>             |



 

<span data-ttu-id="94cf4-134">[Таблица модуликсклусион](moduleexclusion-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="94cf4-134">[ModuleExclusion Table](moduleexclusion-table.md) (partial)</span></span>



| <span data-ttu-id="94cf4-135">ModuleID</span><span class="sxs-lookup"><span data-stu-id="94cf4-135">ModuleID</span></span>            | <span data-ttu-id="94cf4-136">модулелангуаже</span><span class="sxs-lookup"><span data-stu-id="94cf4-136">ModuleLanguage</span></span> | <span data-ttu-id="94cf4-137">ексклудедид</span><span class="sxs-lookup"><span data-stu-id="94cf4-137">ExcludedID</span></span>          | <span data-ttu-id="94cf4-138">ексклудедлангуаже</span><span class="sxs-lookup"><span data-stu-id="94cf4-138">ExcludedLanguage</span></span> |
|---------------------|----------------|---------------------|------------------|
| <span data-ttu-id="94cf4-139">Осермодуле. *GUID2*</span><span class="sxs-lookup"><span data-stu-id="94cf4-139">OtherModule.*GUID2*</span></span> | <span data-ttu-id="94cf4-140">1033</span><span class="sxs-lookup"><span data-stu-id="94cf4-140">1033</span></span>           | <span data-ttu-id="94cf4-141">Осермодуле. *GUID3*</span><span class="sxs-lookup"><span data-stu-id="94cf4-141">OtherModule.*GUID3*</span></span> | <span data-ttu-id="94cf4-142">0</span><span class="sxs-lookup"><span data-stu-id="94cf4-142">0</span></span>                |
| <span data-ttu-id="94cf4-143">MyModule. *GUID1*</span><span class="sxs-lookup"><span data-stu-id="94cf4-143">MyModule.*GUID1*</span></span>    | <span data-ttu-id="94cf4-144">1033</span><span class="sxs-lookup"><span data-stu-id="94cf4-144">1033</span></span>           | <span data-ttu-id="94cf4-145">MyModule. *GUID1*</span><span class="sxs-lookup"><span data-stu-id="94cf4-145">MyModule.*GUID1*</span></span>    | <span data-ttu-id="94cf4-146">1033</span><span class="sxs-lookup"><span data-stu-id="94cf4-146">1033</span></span>             |



 

<span data-ttu-id="94cf4-147">Модуль слияния ICE публикует первую ошибку из-за первой строки в таблице Модуледепенденци, которая не указывает требуемую зависимость для текущего модуля, указанного в таблице ModuleSignature.</span><span class="sxs-lookup"><span data-stu-id="94cf4-147">The merge module ICE posts the first error because the of the first row in the ModuleDependency table, which does not specify a required dependency for the current module specified in the ModuleSignature table.</span></span> <span data-ttu-id="94cf4-148">Зависимости модуля можно указывать только в собственной таблице Модуледепенденци.</span><span class="sxs-lookup"><span data-stu-id="94cf4-148">The dependencies of a module can only be specified in its own ModuleDependency table.</span></span> <span data-ttu-id="94cf4-149">Если Осермодуле. *GUID3* является обязательным для текущего модуля, замените первые два столбца строки данными из таблицы ModuleSignature.</span><span class="sxs-lookup"><span data-stu-id="94cf4-149">If OtherModule.*GUID3* is required by the current module, replace the first two columns of the row with the data from the ModuleSignature table.</span></span> <span data-ttu-id="94cf4-150">Если Осермодуле. *GUID3* не требуется для этого модуля, удалите эту строку.</span><span class="sxs-lookup"><span data-stu-id="94cf4-150">If OtherModule.*GUID3* is not required by this module, delete this row.</span></span>

<span data-ttu-id="94cf4-151">Модуль слияния ICE отправляет вторую ошибку, так как модуль не может задать зависимость от самого себя.</span><span class="sxs-lookup"><span data-stu-id="94cf4-151">The merge module ICE posts the second error because a module cannot specify a dependency upon itself.</span></span>

<span data-ttu-id="94cf4-152">Модуль слияния ICE публикует третью ошибку из-за первой строки в таблице Модуликсклусион, которая не указывает требуемое исключение для текущего модуля, указанного в таблице ModuleSignature.</span><span class="sxs-lookup"><span data-stu-id="94cf4-152">The merge module ICE posts the third error because of the first row in the ModuleExclusion table, which does not specify a required exclusion for the current module specified in the ModuleSignature table.</span></span> <span data-ttu-id="94cf4-153">Исключения модуля могут быть указаны только в собственной таблице Модуликсклусион.</span><span class="sxs-lookup"><span data-stu-id="94cf4-153">The exclusions of a module can only be specified in its own ModuleExclusion table.</span></span> <span data-ttu-id="94cf4-154">Если текущий модуль исключает Осермодуле. *GUID3* замените первые два столбца строки данными из таблицы ModuleSignature.</span><span class="sxs-lookup"><span data-stu-id="94cf4-154">If the current module excludes OtherModule.*GUID3*, replace the first two columns of the row with the data from the ModuleSignature table.</span></span> <span data-ttu-id="94cf4-155">Если текущий модуль не исключает Осермодуле. *GUID3*, удалите эту строку.</span><span class="sxs-lookup"><span data-stu-id="94cf4-155">If the current module does not exclude OtherModule.*GUID3*, delete this row.</span></span>

<span data-ttu-id="94cf4-156">Модуль слияния ICE отправляет четвертую ошибку, так как модуль не может указать, что он исключается.</span><span class="sxs-lookup"><span data-stu-id="94cf4-156">The merge module ICE posts the fourth error because a module cannot specify that it exclude itself.</span></span>

## <a name="related-topics"></a><span data-ttu-id="94cf4-157">См. также</span><span class="sxs-lookup"><span data-stu-id="94cf4-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="94cf4-158">Ссылка на модуль слияния ICE</span><span class="sxs-lookup"><span data-stu-id="94cf4-158">Merge Module ICE Reference</span></span>](merge-module-ice-reference.md)
</dt> </dl>

 

 



