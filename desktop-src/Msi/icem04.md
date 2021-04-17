---
description: ICEM04 проверяет, что необходимые пустые таблицы модуля слияния пусты. Сбой исправления ошибки, ICEM04 отчеты, может привести к неправильному объединению модуля слияния.
ms.assetid: c6f64f5e-be65-485b-8831-e377535bd335
title: ICEM04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2ef993690ae690e0651db1538196998c4dd28c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650606"
---
# <a name="icem04"></a><span data-ttu-id="b3ade-104">ICEM04</span><span class="sxs-lookup"><span data-stu-id="b3ade-104">ICEM04</span></span>

<span data-ttu-id="b3ade-105">ICEM04 проверяет, что необходимые пустые таблицы модуля слияния пусты.</span><span class="sxs-lookup"><span data-stu-id="b3ade-105">ICEM04 verifies that the merge module's required empty tables are empty.</span></span> <span data-ttu-id="b3ade-106">Сбой исправления ошибки, ICEM04 отчеты, может привести к неправильному объединению модуля слияния.</span><span class="sxs-lookup"><span data-stu-id="b3ade-106">Failure to fix an error that ICEM04 reports can result in incorrect merging of the merge module.</span></span>

## <a name="result"></a><span data-ttu-id="b3ade-107">Результат</span><span class="sxs-lookup"><span data-stu-id="b3ade-107">Result</span></span>

<span data-ttu-id="b3ade-108">ICEM04 отправляет сообщение об ошибке, если требуемые пустые таблицы модуля слияния не пусты.</span><span class="sxs-lookup"><span data-stu-id="b3ade-108">ICEM04 posts an error when the merge module's required empty tables are not empty.</span></span>

## <a name="example"></a><span data-ttu-id="b3ade-109">Пример</span><span class="sxs-lookup"><span data-stu-id="b3ade-109">Example</span></span>

<span data-ttu-id="b3ade-110">ICEM04 отправляет следующие сообщения об ошибках для модуля, содержащего отображаемые записи базы данных.</span><span class="sxs-lookup"><span data-stu-id="b3ade-110">ICEM04 posts the following error messages for a module that contains the database entries shown.</span></span>

``` syntax
An empty FeatureComponents table is required in a Merge Module.

The Merge Module contains the 'ModuleInstallExecuteSequence' table. It 
must therefore have an empty 'InstallExecuteSequence' table.

Action 'CostInitialize' found in the AdvtExecuteSequence table. This 
table must be empty in a Merge Module
```

<span data-ttu-id="b3ade-111">В следующей таблице показана частичная [Таблица адвтексекутесекуенце](advtexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="b3ade-111">The following table shows you a partial [AdvtExecuteSequence Table](advtexecutesequence-table.md).</span></span>



| <span data-ttu-id="b3ade-112">Действие</span><span class="sxs-lookup"><span data-stu-id="b3ade-112">Action</span></span>         | <span data-ttu-id="b3ade-113">Последовательность</span><span class="sxs-lookup"><span data-stu-id="b3ade-113">Sequence</span></span> |
|----------------|----------|
| <span data-ttu-id="b3ade-114">костинитиализе</span><span class="sxs-lookup"><span data-stu-id="b3ade-114">CostInitialize</span></span> | <span data-ttu-id="b3ade-115">1</span><span class="sxs-lookup"><span data-stu-id="b3ade-115">1</span></span>        |



 

<span data-ttu-id="b3ade-116">В следующем списке показано частичное содержимое установочного модуля:</span><span class="sxs-lookup"><span data-stu-id="b3ade-116">The following list shows you the partial contents of MergeModule:</span></span>

-   <span data-ttu-id="b3ade-117">модулеинсталлексекутесекуенце</span><span class="sxs-lookup"><span data-stu-id="b3ade-117">ModuleInstallExecuteSequence</span></span>
-   <span data-ttu-id="b3ade-118">модулеадвтексекутесекуенце</span><span class="sxs-lookup"><span data-stu-id="b3ade-118">ModuleAdvtExecuteSequence</span></span>
-   <span data-ttu-id="b3ade-119">инсталлуисекуенце</span><span class="sxs-lookup"><span data-stu-id="b3ade-119">InstallUISequence</span></span>

<span data-ttu-id="b3ade-120">В следующем примере показана Другая возможная ошибка.</span><span class="sxs-lookup"><span data-stu-id="b3ade-120">The following example shows you another possible error.</span></span>

``` syntax
Feature-Component '[1].[2]' found in the FeatureComponents table. The 
FeatureComponents table must be empty in a Merge Module.
```

<span data-ttu-id="b3ade-121">Если модуль слияния содержит таблицу последовательности модулей, она должна содержать соответствующую пустую таблицу, независимо от того, пуста ли таблица последовательности модуля.</span><span class="sxs-lookup"><span data-stu-id="b3ade-121">If a merge module contains a module sequence table, it must contain the corresponding empty sequence table, whether or not the module sequence table is empty.</span></span> <span data-ttu-id="b3ade-122">Например, если модуль слияния содержит [таблицу модулеадминексекутесекуенце](moduleadminexecutesequence-table.md), она также должна содержать пустую таблицу админексекутесекуенце.</span><span class="sxs-lookup"><span data-stu-id="b3ade-122">For example, if the merge module contains the [ModuleAdminExecuteSequence Table](moduleadminexecutesequence-table.md), it must also contain an empty AdminExecuteSequence table.</span></span>

<span data-ttu-id="b3ade-123">[Таблица феатурекомпонентс](featurecomponents-table.md) является обязательной во всех модулях слияния и должна быть пустой.</span><span class="sxs-lookup"><span data-stu-id="b3ade-123">The [FeatureComponents Table](featurecomponents-table.md) is required in all merge modules and must be empty.</span></span>

<span data-ttu-id="b3ade-124">В следующей процедуре показано, как исправить ошибки.</span><span class="sxs-lookup"><span data-stu-id="b3ade-124">The following procedure shows you how to fix errors.</span></span>

<span data-ttu-id="b3ade-125">**Устранение ошибок**</span><span class="sxs-lookup"><span data-stu-id="b3ade-125">**To fix errors**</span></span>

1.  <span data-ttu-id="b3ade-126">Добавьте пустую [таблицу феатурекомпонентс](featurecomponents-table.md) в модуль слияния.</span><span class="sxs-lookup"><span data-stu-id="b3ade-126">Add an empty [FeatureComponents Table](featurecomponents-table.md) to the merge module.</span></span>
2.  <span data-ttu-id="b3ade-127">Добавьте пустую [таблицу инсталлексекутесекуенце](installexecutesequence-table.md) в модуль слияния.</span><span class="sxs-lookup"><span data-stu-id="b3ade-127">Add an empty [InstallExecuteSequence Table](installexecutesequence-table.md) to the merge module.</span></span>
3.  <span data-ttu-id="b3ade-128">Удалите действие "Костинитиализе" из [таблицы адвтексекутесекуенце](advtexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="b3ade-128">Remove the 'CostInitialize' action from the [AdvtExecuteSequence Table](advtexecutesequence-table.md).</span></span>
    > [!Note]  
    > <span data-ttu-id="b3ade-129">Эта таблица должна быть пустой в модуле слияния.</span><span class="sxs-lookup"><span data-stu-id="b3ade-129">This table must be empty in a merge module.</span></span> <span data-ttu-id="b3ade-130">Действия должны присутствовать только в таблице Модулеадвтексекутесекуенце.</span><span class="sxs-lookup"><span data-stu-id="b3ade-130">Actions should only appear in the ModuleAdvtExecuteSequence table.</span></span>

     

## <a name="tables-used-during-execution"></a><span data-ttu-id="b3ade-131">Таблицы, используемые во время выполнения</span><span class="sxs-lookup"><span data-stu-id="b3ade-131">Tables Used During Execution</span></span>

<span data-ttu-id="b3ade-132">В следующем списке указаны таблицы, используемые во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="b3ade-132">The following list identifies the tables that are used during execution:</span></span>

-   [<span data-ttu-id="b3ade-133">Таблица Феатурекомпонентс</span><span class="sxs-lookup"><span data-stu-id="b3ade-133">FeatureComponents Table</span></span>](featurecomponents-table.md)
-   <span data-ttu-id="b3ade-134">\*Таблицы последовательностей модулей и соответствующие \* таблицы последовательностей.</span><span class="sxs-lookup"><span data-stu-id="b3ade-134">Module\*Sequence tables and corresponding \*Sequence tables.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b3ade-135">См. также</span><span class="sxs-lookup"><span data-stu-id="b3ade-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b3ade-136">О модулях слияния</span><span class="sxs-lookup"><span data-stu-id="b3ade-136">About Merge Modules</span></span>](about-merge-modules.md)
</dt> <dt>

[<span data-ttu-id="b3ade-137">Ссылка на модуль слияния ICE</span><span class="sxs-lookup"><span data-stu-id="b3ade-137">Merge Module ICE Reference</span></span>](merge-module-ice-reference.md)
</dt> </dl>

 

 



