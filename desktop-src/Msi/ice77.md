---
description: ICE77 проверяет, что настраиваемые действия с набором Мсидбкустомактионтипеинскрипт bit упорядочены после действия Инсталлинитиализе и перед действием функции InstallFinalize.
ms.assetid: 291cf731-b7e6-44c2-a8ec-78e0e037d1f5
title: ICE77
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15e072692b76cfd63bf62c5fd23f612a445e5fd7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154818"
---
# <a name="ice77"></a><span data-ttu-id="42fb2-103">ICE77</span><span class="sxs-lookup"><span data-stu-id="42fb2-103">ICE77</span></span>

<span data-ttu-id="42fb2-104">ICE77 проверяет, что настраиваемые действия с набором **мсидбкустомактионтипеинскрипт** bit упорядочены после [действия инсталлинитиализе](installinitialize-action.md) и перед [действием функции InstallFinalize](installfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="42fb2-104">ICE77 verifies that custom actions with the **msidbCustomActionTypeInScript** bit set are sequenced after the [InstallInitialize action](installinitialize-action.md) and before the [InstallFinalize action](installfinalize-action.md).</span></span> <span data-ttu-id="42fb2-105">ICE77 проверяет последовательность в [таблице инсталлексекутесекуенце](installexecutesequence-table.md) и [таблице админексекутесекуенце](adminexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="42fb2-105">ICE77 checks the sequence in the [InstallExecuteSequence table](installexecutesequence-table.md) and [AdminExecuteSequence table](adminexecutesequence-table.md).</span></span>

## <a name="result"></a><span data-ttu-id="42fb2-106">Результат</span><span class="sxs-lookup"><span data-stu-id="42fb2-106">Result</span></span>

<span data-ttu-id="42fb2-107">ICE77 отправляет ошибку, если настраиваемое действие в скрипте выполняется последовательно перед действием Инсталлинитиализе или после действия функции InstallFinalize.</span><span class="sxs-lookup"><span data-stu-id="42fb2-107">ICE77 posts an error if an in-script custom action is sequenced before the InstallInitialize action or after the InstallFinalize action.</span></span>

<span data-ttu-id="42fb2-108">ICE77 отправляет сообщение об ошибке, если отсутствует действие Инсталлинитиализе или функции InstallFinalize.</span><span class="sxs-lookup"><span data-stu-id="42fb2-108">ICE77 posts an error if the InstallInitialize action or the InstallFinalize action is missing.</span></span>

## <a name="example"></a><span data-ttu-id="42fb2-109">Пример</span><span class="sxs-lookup"><span data-stu-id="42fb2-109">Example</span></span>

<span data-ttu-id="42fb2-110">ICE77 сообщает о следующих ошибках в примере:</span><span class="sxs-lookup"><span data-stu-id="42fb2-110">ICE77 reports the following errors for the example:</span></span>

``` syntax
InstallFinalize is missing from 'InstallExecuteSequence'. 
CA_InScriptInstall is a in-script custom action. It must be sequenced 
before the InstallFinalize action.
 
CA_InScriptAdmin is a in-script custom action.  It must be sequenced 
in between the InstallInitialize action and the InstallFinalize action 
in the AdminExecuteSequence Sequence table.
```

<span data-ttu-id="42fb2-111">[Таблица CustomAction](customaction-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="42fb2-111">[CustomAction Table](customaction-table.md) (partial)</span></span>



| <span data-ttu-id="42fb2-112">Действие</span><span class="sxs-lookup"><span data-stu-id="42fb2-112">Action</span></span>              | <span data-ttu-id="42fb2-113">Тип</span><span class="sxs-lookup"><span data-stu-id="42fb2-113">Type</span></span> |
|---------------------|------|
| <span data-ttu-id="42fb2-114">\_ИНСКРИПТИНСТАЛЛ CA</span><span class="sxs-lookup"><span data-stu-id="42fb2-114">CA\_InScriptInstall</span></span> | <span data-ttu-id="42fb2-115">1025</span><span class="sxs-lookup"><span data-stu-id="42fb2-115">1025</span></span> |
| <span data-ttu-id="42fb2-116">\_ИНСКРИПТАДМИН CA</span><span class="sxs-lookup"><span data-stu-id="42fb2-116">CA\_InScriptAdmin</span></span>   | <span data-ttu-id="42fb2-117">1026</span><span class="sxs-lookup"><span data-stu-id="42fb2-117">1026</span></span> |



 

<span data-ttu-id="42fb2-118">[Таблица инсталлексекутесекуенце](installexecutesequence-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="42fb2-118">[InstallExecuteSequence Table](installexecutesequence-table.md) (partial)</span></span>



| <span data-ttu-id="42fb2-119">Действие</span><span class="sxs-lookup"><span data-stu-id="42fb2-119">Action</span></span>              | <span data-ttu-id="42fb2-120">Последовательность</span><span class="sxs-lookup"><span data-stu-id="42fb2-120">Sequence</span></span> |
|---------------------|----------|
| <span data-ttu-id="42fb2-121">\_ИНСКРИПТИНСТАЛЛ CA</span><span class="sxs-lookup"><span data-stu-id="42fb2-121">CA\_InScriptInstall</span></span> | <span data-ttu-id="42fb2-122">2000</span><span class="sxs-lookup"><span data-stu-id="42fb2-122">2000</span></span>     |
| <span data-ttu-id="42fb2-123">инсталлинитиализе</span><span class="sxs-lookup"><span data-stu-id="42fb2-123">InstallInitialize</span></span>   | <span data-ttu-id="42fb2-124">1500</span><span class="sxs-lookup"><span data-stu-id="42fb2-124">1500</span></span>     |



 

<span data-ttu-id="42fb2-125">[Таблица админексекутесекуенце](adminexecutesequence-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="42fb2-125">[AdminExecuteSequence Table](adminexecutesequence-table.md) (partial)</span></span>



| <span data-ttu-id="42fb2-126">Действие</span><span class="sxs-lookup"><span data-stu-id="42fb2-126">Action</span></span>            | <span data-ttu-id="42fb2-127">Последовательность</span><span class="sxs-lookup"><span data-stu-id="42fb2-127">Sequence</span></span> |
|-------------------|----------|
| <span data-ttu-id="42fb2-128">\_ИНСКРИПТАДМИН CA</span><span class="sxs-lookup"><span data-stu-id="42fb2-128">CA\_InScriptAdmin</span></span> | <span data-ttu-id="42fb2-129">1400</span><span class="sxs-lookup"><span data-stu-id="42fb2-129">1400</span></span>     |
| <span data-ttu-id="42fb2-130">инсталлинитиализе</span><span class="sxs-lookup"><span data-stu-id="42fb2-130">InstallInitialize</span></span> | <span data-ttu-id="42fb2-131">1500</span><span class="sxs-lookup"><span data-stu-id="42fb2-131">1500</span></span>     |
| <span data-ttu-id="42fb2-132">Функции InstallFinalize</span><span class="sxs-lookup"><span data-stu-id="42fb2-132">InstallFinalize</span></span>   | <span data-ttu-id="42fb2-133">6600</span><span class="sxs-lookup"><span data-stu-id="42fb2-133">6600</span></span>     |



 

<span data-ttu-id="42fb2-134">Чтобы устранить ошибки, поочередно заполните пользовательские действия в скрипте после действия Инсталлинитиализе и перед действием функции InstallFinalize.</span><span class="sxs-lookup"><span data-stu-id="42fb2-134">To fix the errors, sequence the in-script custom actions after the InstallInitialize action and before the InstallFinalize action.</span></span> <span data-ttu-id="42fb2-135">Действия Инсталлинитиализе и функции InstallFinalize должны присутствовать в таблице Инсталлексекутесекуенце и таблице Админексекутесекуенце.</span><span class="sxs-lookup"><span data-stu-id="42fb2-135">The InstallInitialize and InstallFinalize actions must be present in the InstallExecuteSequence table and the AdminExecuteSequence table.</span></span>

## <a name="related-topics"></a><span data-ttu-id="42fb2-136">См. также</span><span class="sxs-lookup"><span data-stu-id="42fb2-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="42fb2-137">Справочник по ICE</span><span class="sxs-lookup"><span data-stu-id="42fb2-137">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



