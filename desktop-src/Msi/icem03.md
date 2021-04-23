---
description: ICEM03 проверяет, что все действия в модуле являются базовыми действиями или являются производными от действительного базового действия.
ms.assetid: 8e2b5921-32cf-45e8-9906-30002574a712
title: ICEM03
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f368fa50a71153c41eebaa9ee5084449cf824993
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105650859"
---
# <a name="icem03"></a><span data-ttu-id="7c9c4-103">ICEM03</span><span class="sxs-lookup"><span data-stu-id="7c9c4-103">ICEM03</span></span>

<span data-ttu-id="7c9c4-104">ICEM03 проверяет, что все действия в модуле являются базовыми действиями или являются производными от действительного базового действия.</span><span class="sxs-lookup"><span data-stu-id="7c9c4-104">ICEM03 verifies that all actions in the module are either base actions or derive from a valid base action.</span></span>

<span data-ttu-id="7c9c4-105">Модуль слияния ICEs хранится в файле слияния Module. CUB, который называется Мержемод. CUB, а не в файле. CUB, содержащем значение ICEs, используемое для проверки пакета.</span><span class="sxs-lookup"><span data-stu-id="7c9c4-105">Merge module ICEs are stored in a merge module .cub file called Mergemod.cub and not in the .cub file containing the ICEs used for package validation.</span></span>

## <a name="result"></a><span data-ttu-id="7c9c4-106">Результат</span><span class="sxs-lookup"><span data-stu-id="7c9c4-106">Result</span></span>

<span data-ttu-id="7c9c4-107">ICEM03 отправляет сообщения об ошибках для модуля, содержащего действия в таблице последовательности, которые не являются базовым действием или являются производными от действительного базового действия.</span><span class="sxs-lookup"><span data-stu-id="7c9c4-107">ICEM03 posts the error messages for a module containing actions in a sequence table that is not a base action or derived from a valid base action.</span></span>

## <a name="example"></a><span data-ttu-id="7c9c4-108">Пример</span><span class="sxs-lookup"><span data-stu-id="7c9c4-108">Example</span></span>

<span data-ttu-id="7c9c4-109">ICEM03 отправляет следующие сообщения об ошибках для модуля, содержащего записи базы данных, показанные ниже.</span><span class="sxs-lookup"><span data-stu-id="7c9c4-109">ICEM03 posts the following error messages for a module containing the database entries shown below.</span></span>

``` syntax
The action 'Action1' in the 'ModuleInstallExecuteSequence' table is 
orphaned. It is not a valid base action and does not derive from a 
valid base action.
The action 'Action2' in the 'ModuleInstallExecuteSequence' table is 
orphaned. It is not a valid base action and does not derive from a 
valid base action.
```

[<span data-ttu-id="7c9c4-110">Таблица Модулеинсталлексекутесекуенце</span><span class="sxs-lookup"><span data-stu-id="7c9c4-110">ModuleInstallExecuteSequence Table</span></span>](moduleinstallexecutesequence-table.md)



| <span data-ttu-id="7c9c4-111">Действие</span><span class="sxs-lookup"><span data-stu-id="7c9c4-111">Action</span></span>  | <span data-ttu-id="7c9c4-112">Последовательность</span><span class="sxs-lookup"><span data-stu-id="7c9c4-112">Sequence</span></span> | <span data-ttu-id="7c9c4-113">басеактион</span><span class="sxs-lookup"><span data-stu-id="7c9c4-113">BaseAction</span></span> | <span data-ttu-id="7c9c4-114">После</span><span class="sxs-lookup"><span data-stu-id="7c9c4-114">After</span></span> | <span data-ttu-id="7c9c4-115">Условие</span><span class="sxs-lookup"><span data-stu-id="7c9c4-115">Condition</span></span> |
|---------|----------|------------|-------|-----------|
| <span data-ttu-id="7c9c4-116">Action1 превышают</span><span class="sxs-lookup"><span data-stu-id="7c9c4-116">Action1</span></span> |          | <span data-ttu-id="7c9c4-117">Action2</span><span class="sxs-lookup"><span data-stu-id="7c9c4-117">Action2</span></span>    | <span data-ttu-id="7c9c4-118">0</span><span class="sxs-lookup"><span data-stu-id="7c9c4-118">0</span></span>     |           |
| <span data-ttu-id="7c9c4-119">Action2</span><span class="sxs-lookup"><span data-stu-id="7c9c4-119">Action2</span></span> |          | <span data-ttu-id="7c9c4-120">Action1 превышают</span><span class="sxs-lookup"><span data-stu-id="7c9c4-120">Action1</span></span>    | <span data-ttu-id="7c9c4-121">0</span><span class="sxs-lookup"><span data-stu-id="7c9c4-121">0</span></span>     |           |



 

<span data-ttu-id="7c9c4-122">ICEM03 отправляет ошибки для этих двух действий, так как они ссылаются друг на друга как на базовые действия в таблице Модулеинсталлексекутесекуенце.</span><span class="sxs-lookup"><span data-stu-id="7c9c4-122">ICEM03 posts errors for these two actions because they refer to each other as base actions in the ModuleInstallExecuteSequence table.</span></span> <span data-ttu-id="7c9c4-123">Все действия в таблицах [модулеадминуисекуенце](moduleadminuisequence-table.md), [модулеадминексекутесекуенце](moduleadminexecutesequence-table.md), [модулеадвтуисекуенце](moduleadvtuisequence-table.md), [модулеадвтексекутесекуенце](moduleadvtexecutesequence-table.md), [ModuleInstallUISequence](moduleinstalluisequence-table.md)и [ModuleInstallExecuteSequence](moduleinstallexecutesequence-table.md) должны быть базовыми или производными от сочетания другого действия и флага Before и After.</span><span class="sxs-lookup"><span data-stu-id="7c9c4-123">All actions in the [ModuleAdminUISequence](moduleadminuisequence-table.md), [ModuleAdminExecuteSequence](moduleadminexecutesequence-table.md), [ModuleAdvtUISequence](moduleadvtuisequence-table.md), [ModuleAdvtExecuteSequence](moduleadvtexecutesequence-table.md), [ModuleInstallUISequence](moduleinstalluisequence-table.md), and [ModuleInstallExecuteSequence](moduleinstallexecutesequence-table.md) tables must either be base actions or derive their position from the combination of another action and a before and after flag.</span></span>

<span data-ttu-id="7c9c4-124">Чтобы устранить эту ошибку, определите базовые действия для двух действий.</span><span class="sxs-lookup"><span data-stu-id="7c9c4-124">To fix this error, determine the base actions for the two actions.</span></span> <span data-ttu-id="7c9c4-125">Добавьте запись для базовых действий с порядковым номером по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7c9c4-125">Add a record for the base actions with a default sequence number.</span></span> <span data-ttu-id="7c9c4-126">Для Action1 превышают и Action2 введите имена базовых действий в столбце Басеактион и 0 или 1 в столбце After.</span><span class="sxs-lookup"><span data-stu-id="7c9c4-126">For Action1 and Action2 enter the base action names in the BaseAction column and 0 or 1 in the After column.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7c9c4-127">См. также</span><span class="sxs-lookup"><span data-stu-id="7c9c4-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7c9c4-128">Ссылка на модуль слияния ICE</span><span class="sxs-lookup"><span data-stu-id="7c9c4-128">Merge Module ICE Reference</span></span>](merge-module-ice-reference.md)
</dt> </dl>

 

 



