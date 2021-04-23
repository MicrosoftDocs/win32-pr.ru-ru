---
description: ICEM05 проверяет, правильно ли связан модуль слияния с компонентами в модуле. Неправильное связывание компонента с модулем приводит к тому, что компонент будет неправильно связан с целевой базой данных.
ms.assetid: 1bf4041e-b198-4897-8719-8505fd8180ec
title: ICEM05
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e62ca481ef836c2675c381817fe2242e37384818
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080676"
---
# <a name="icem05"></a><span data-ttu-id="58933-104">ICEM05</span><span class="sxs-lookup"><span data-stu-id="58933-104">ICEM05</span></span>

<span data-ttu-id="58933-105">ICEM05 проверяет, правильно ли связан модуль слияния с компонентами в модуле.</span><span class="sxs-lookup"><span data-stu-id="58933-105">ICEM05 verifies that the merge module is correctly associated with components in the module.</span></span> <span data-ttu-id="58933-106">Неправильное связывание компонента с модулем приводит к тому, что компонент будет неправильно связан с целевой базой данных.</span><span class="sxs-lookup"><span data-stu-id="58933-106">Incorrectly associating a component with a module causes the component to be incorrectly associated with the target database.</span></span>

<span data-ttu-id="58933-107">Модуль слияния ICEs хранится в файле слияния Module. CUB, который называется Мержемод. CUB, а не в файле. CUB, содержащем значение ICEs, используемое для проверки пакета.</span><span class="sxs-lookup"><span data-stu-id="58933-107">Merge module ICEs are stored in a merge module .cub file called Mergemod.cub and not in the .cub file containing the ICEs used for package validation.</span></span>

## <a name="result"></a><span data-ttu-id="58933-108">Результат</span><span class="sxs-lookup"><span data-stu-id="58933-108">Result</span></span>

<span data-ttu-id="58933-109">ICEM05 отправляет сообщение об ошибке, если база данных модуля неправильно связывает компоненты и модуль.</span><span class="sxs-lookup"><span data-stu-id="58933-109">ICEM05 posts an error if the module database incorrectly associates components and the module.</span></span>

## <a name="example"></a><span data-ttu-id="58933-110">Пример</span><span class="sxs-lookup"><span data-stu-id="58933-110">Example</span></span>

<span data-ttu-id="58933-111">ICEM05 отправляет следующие сообщения об ошибках для модуля, содержащего записи базы данных, показанные ниже.</span><span class="sxs-lookup"><span data-stu-id="58933-111">ICEM05 posts the following error messages for a module containing the database entries shown below.</span></span>

``` syntax
The component Component2.OtherModule.GUID2.1033 in the 
ModuleComponents table does not belong to this Merge Module.
The component Component1.MyModule.GUID1.1033 in the ModuleComponents 
table is not listed in the Component table.
The component 'Component3' in the Component table is not listed in the 
ModuleComponents table.
```

[<span data-ttu-id="58933-112">Таблица ModuleSignature</span><span class="sxs-lookup"><span data-stu-id="58933-112">ModuleSignature Table</span></span>](modulesignature-table.md)



| <span data-ttu-id="58933-113">ModuleID</span><span class="sxs-lookup"><span data-stu-id="58933-113">ModuleID</span></span>         | <span data-ttu-id="58933-114">Язык</span><span class="sxs-lookup"><span data-stu-id="58933-114">Language</span></span> | <span data-ttu-id="58933-115">Версия</span><span class="sxs-lookup"><span data-stu-id="58933-115">Version</span></span> |
|------------------|----------|---------|
| <span data-ttu-id="58933-116">MyModule. *GUID1*</span><span class="sxs-lookup"><span data-stu-id="58933-116">MyModule.*GUID1*</span></span> | <span data-ttu-id="58933-117">1033</span><span class="sxs-lookup"><span data-stu-id="58933-117">1033</span></span>     | <span data-ttu-id="58933-118">1.0</span><span class="sxs-lookup"><span data-stu-id="58933-118">1.0</span></span>     |



 

[<span data-ttu-id="58933-119">**Таблица Модулекомпонентс**</span><span class="sxs-lookup"><span data-stu-id="58933-119">**ModuleComponents Table**</span></span>](modulecomponents-table.md)



| <span data-ttu-id="58933-120">Компонент</span><span class="sxs-lookup"><span data-stu-id="58933-120">Component</span></span>  | <span data-ttu-id="58933-121">ModuleID</span><span class="sxs-lookup"><span data-stu-id="58933-121">ModuleID</span></span>            | <span data-ttu-id="58933-122">Язык</span><span class="sxs-lookup"><span data-stu-id="58933-122">Language</span></span> |
|------------|---------------------|----------|
| <span data-ttu-id="58933-123">Component1</span><span class="sxs-lookup"><span data-stu-id="58933-123">Component1</span></span> | <span data-ttu-id="58933-124">MyModule. *GUID1*</span><span class="sxs-lookup"><span data-stu-id="58933-124">MyModule.*GUID1*</span></span>    | <span data-ttu-id="58933-125">1033</span><span class="sxs-lookup"><span data-stu-id="58933-125">1033</span></span>     |
| <span data-ttu-id="58933-126">Component2</span><span class="sxs-lookup"><span data-stu-id="58933-126">Component2</span></span> | <span data-ttu-id="58933-127">Осермодуле. *GUID2*</span><span class="sxs-lookup"><span data-stu-id="58933-127">OtherModule.*GUID2*</span></span> | <span data-ttu-id="58933-128">1033</span><span class="sxs-lookup"><span data-stu-id="58933-128">1033</span></span>     |



 

<span data-ttu-id="58933-129">[Таблица Component](component-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="58933-129">[Component Table](component-table.md) (partial)</span></span>



| <span data-ttu-id="58933-130">Компонент</span><span class="sxs-lookup"><span data-stu-id="58933-130">Component</span></span>  | <span data-ttu-id="58933-131">ComponentID</span><span class="sxs-lookup"><span data-stu-id="58933-131">ComponentID</span></span> |
|------------|-------------|
| <span data-ttu-id="58933-132">Component3</span><span class="sxs-lookup"><span data-stu-id="58933-132">Component3</span></span> | <span data-ttu-id="58933-133">*GUID4*</span><span class="sxs-lookup"><span data-stu-id="58933-133">*GUID4*</span></span>     |
| <span data-ttu-id="58933-134">Component2</span><span class="sxs-lookup"><span data-stu-id="58933-134">Component2</span></span> | <span data-ttu-id="58933-135">*GUID5*</span><span class="sxs-lookup"><span data-stu-id="58933-135">*GUID5*</span></span>     |



 

<span data-ttu-id="58933-136">Модуль слияния сообщает о первой ошибке, так как таблица Модулекомпонентс пытается связать компонент с другим модулем, который не является текущим модулем, указанным в таблице ModuleSignature.</span><span class="sxs-lookup"><span data-stu-id="58933-136">The merge module ICE reports the first error because the ModuleComponents table attempts to associate a component with another module that is not the current module specified in the ModuleSignature table.</span></span> <span data-ttu-id="58933-137">Чтобы устранить эту проблему, измените столбцы ModuleID и Language записи Модулекомпонентс для Component2 на значение для текущего модуля MyModule. *GUID1*.</span><span class="sxs-lookup"><span data-stu-id="58933-137">To fix this, change the ModuleID and Language columns of the ModuleComponents record for Component2 to that for the current module, MyModule.*GUID1*.</span></span>

<span data-ttu-id="58933-138">Модуль слияния сообщает о второй ошибке, так как первая запись в таблице Модулекомпонентс пытается связать Component1 с модулем.</span><span class="sxs-lookup"><span data-stu-id="58933-138">The merge module ICE reports the second error because the first record in the ModuleComponents table attempts to associate Component1 with the module.</span></span> <span data-ttu-id="58933-139">Этот компонент не существует в таблице Component модуля слияния.</span><span class="sxs-lookup"><span data-stu-id="58933-139">This component does not exist in the Component Table of the merge module.</span></span> <span data-ttu-id="58933-140">Модуль может быть связан только с компонентом, который существует в модуле.</span><span class="sxs-lookup"><span data-stu-id="58933-140">A module can only be associated with a component that exists in the module.</span></span> <span data-ttu-id="58933-141">Чтобы устранить эту проблему, удалите запись для несуществующего компонента.</span><span class="sxs-lookup"><span data-stu-id="58933-141">To fix this, remove the record for the non-existent component.</span></span>

<span data-ttu-id="58933-142">Модуль слияния сообщает третью ошибку, так как модуль пытается добавить Component3 в целевую базу данных.</span><span class="sxs-lookup"><span data-stu-id="58933-142">The merge module ICE reports the third error because the module attempts to add Component3 to the target database.</span></span> <span data-ttu-id="58933-143">Этот компонент не был связан с модулем в таблице Модулекомпонентс.</span><span class="sxs-lookup"><span data-stu-id="58933-143">This component has not been associated with the module in the ModuleComponents table.</span></span> <span data-ttu-id="58933-144">Чтобы устранить эту ошибку, добавьте запись для Component3 в таблицу Модулекомпонентс.</span><span class="sxs-lookup"><span data-stu-id="58933-144">To fix this error, add a record for Component3 to the ModuleComponents table.</span></span>

## <a name="related-topics"></a><span data-ttu-id="58933-145">См. также</span><span class="sxs-lookup"><span data-stu-id="58933-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="58933-146">Ссылка на модуль слияния ICE</span><span class="sxs-lookup"><span data-stu-id="58933-146">Merge Module ICE Reference</span></span>](merge-module-ice-reference.md)
</dt> </dl>

 

 



