---
description: ICE63 проверяет правильность последовательности действия RemoveExistingProducts.
ms.assetid: 4dd67bb0-c08a-4a44-b687-0394a3afc2c4
title: ICE63
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5faa6f2ddbcb95cdf12966c2887fe9438a5d610
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911336"
---
# <a name="ice63"></a><span data-ttu-id="4b39a-103">ICE63</span><span class="sxs-lookup"><span data-stu-id="4b39a-103">ICE63</span></span>

<span data-ttu-id="4b39a-104">ICE63 проверяет правильность последовательности [действия RemoveExistingProducts](removeexistingproducts-action.md).</span><span class="sxs-lookup"><span data-stu-id="4b39a-104">ICE63 checks for proper sequencing of the [RemoveExistingProducts action](removeexistingproducts-action.md).</span></span> <span data-ttu-id="4b39a-105">Можно поместить действие RemoveExistingProducts:</span><span class="sxs-lookup"><span data-stu-id="4b39a-105">The RemoveExistingProducts action may be placed:</span></span>

1.  <span data-ttu-id="4b39a-106">Между Инсталлвалидате и Инсталлинитиализе</span><span class="sxs-lookup"><span data-stu-id="4b39a-106">Between InstallValidate and InstallInitialize</span></span>
2.  <span data-ttu-id="4b39a-107">Сразу после Инсталлинитиализе или после Инсталлинитиализе, если действия между Инсталлинитиализе и RemoveExistingProducts не создают никаких действий скрипта.</span><span class="sxs-lookup"><span data-stu-id="4b39a-107">Immediately after InstallInitialize, or after InstallInitialize if the actions between InstallInitialize and RemoveExistingProducts do not generate any script actions.</span></span>
3.  <span data-ttu-id="4b39a-108">Сразу после Инсталлексекуте или Инсталлексекутеагаин и до функции InstallFinalize (такое же ограничение применяется, как и ранее).</span><span class="sxs-lookup"><span data-stu-id="4b39a-108">Immediately after InstallExecute or InstallExecuteAgain and before InstallFinalize (the same restriction as above applies).</span></span>
4.  <span data-ttu-id="4b39a-109">После функции InstallFinalize.</span><span class="sxs-lookup"><span data-stu-id="4b39a-109">After InstallFinalize.</span></span>

<span data-ttu-id="4b39a-110">Ошибка при исправлении предупреждения или ошибки, о которой сообщило ICE63, приводит к сбою обновления.</span><span class="sxs-lookup"><span data-stu-id="4b39a-110">Failure to fix a warning or error reported by ICE63 leads to failure of the upgrade.</span></span>

## <a name="result"></a><span data-ttu-id="4b39a-111">Результат</span><span class="sxs-lookup"><span data-stu-id="4b39a-111">Result</span></span>

<span data-ttu-id="4b39a-112">ICE63 отправляет предупреждение или ошибку, если последовательность действия RemoveExistingProducts неверна.</span><span class="sxs-lookup"><span data-stu-id="4b39a-112">ICE63 posts a warning or error if the sequencing of the RemoveExistingProducts action is not correct.</span></span>

## <a name="example"></a><span data-ttu-id="4b39a-113">Пример</span><span class="sxs-lookup"><span data-stu-id="4b39a-113">Example</span></span>

<span data-ttu-id="4b39a-114">ICE63 сообщает об ошибке в приведенном примере.</span><span class="sxs-lookup"><span data-stu-id="4b39a-114">ICE63 reports the following error for the example shown.</span></span>

``` syntax
WARNING: Some action falls between InstallInitialize and RemoveExistingProducts.
```

<span data-ttu-id="4b39a-115">Действие "Микустомактион" происходит между Инсталлинитиализе и RemoveExistingProducts.</span><span class="sxs-lookup"><span data-stu-id="4b39a-115">The action 'MyCustomAction' occurs between InstallInitialize and RemoveExistingProducts.</span></span> <span data-ttu-id="4b39a-116">Если Микустомактион создает какие бы то ни было действия в сценарии, это вызывает проблемы в установке.</span><span class="sxs-lookup"><span data-stu-id="4b39a-116">If MyCustomAction generates any actions in the script, this causes problems in the installation.</span></span>

<span data-ttu-id="4b39a-117">Чтобы устранить эту ошибку, убедитесь, что Микустомактион не создает никаких действий скриптов или не выполняет их повторное выполнение.</span><span class="sxs-lookup"><span data-stu-id="4b39a-117">To fix this error, verify that MyCustomAction does not generate any script actions or resequence the actions.</span></span>

[<span data-ttu-id="4b39a-118">Таблица Инсталлексекутесекуенце</span><span class="sxs-lookup"><span data-stu-id="4b39a-118">InstallExecuteSequence Table</span></span>](installexecutesequence-table.md)



| <span data-ttu-id="4b39a-119">Действие</span><span class="sxs-lookup"><span data-stu-id="4b39a-119">Action</span></span>                 | <span data-ttu-id="4b39a-120">Условие</span><span class="sxs-lookup"><span data-stu-id="4b39a-120">Condition</span></span> | <span data-ttu-id="4b39a-121">Последовательность</span><span class="sxs-lookup"><span data-stu-id="4b39a-121">Sequence</span></span> |
|------------------------|-----------|----------|
| <span data-ttu-id="4b39a-122">инсталлинитиализе</span><span class="sxs-lookup"><span data-stu-id="4b39a-122">InstallInitialize</span></span>      |           | <span data-ttu-id="4b39a-123">1000</span><span class="sxs-lookup"><span data-stu-id="4b39a-123">1000</span></span>     |
| <span data-ttu-id="4b39a-124">микустомактион</span><span class="sxs-lookup"><span data-stu-id="4b39a-124">MyCustomAction</span></span>         |           | <span data-ttu-id="4b39a-125">1010</span><span class="sxs-lookup"><span data-stu-id="4b39a-125">1010</span></span>     |
| <span data-ttu-id="4b39a-126">RemoveExistingProducts</span><span class="sxs-lookup"><span data-stu-id="4b39a-126">RemoveExistingProducts</span></span> |           | <span data-ttu-id="4b39a-127">1020</span><span class="sxs-lookup"><span data-stu-id="4b39a-127">1020</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="4b39a-128">См. также</span><span class="sxs-lookup"><span data-stu-id="4b39a-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4b39a-129">Справочник по ICE</span><span class="sxs-lookup"><span data-stu-id="4b39a-129">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



