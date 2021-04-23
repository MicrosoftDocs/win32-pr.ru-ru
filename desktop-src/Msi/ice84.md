---
description: ICE84 проверяет таблицу Адвтексекутесекуенце, таблицу Админексекутесекуенце и таблицу Инсталлексекутесекуенце, чтобы убедиться, что следующие стандартные действия не были заданы с условиями в поле Condition.
ms.assetid: 0d1bbf4b-ffab-409e-a292-891dfa823433
title: ICE84
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8960f53f5a01e9bec95a02bb3241487aa31aaae5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347775"
---
# <a name="ice84"></a><span data-ttu-id="b82fe-103">ICE84</span><span class="sxs-lookup"><span data-stu-id="b82fe-103">ICE84</span></span>

<span data-ttu-id="b82fe-104">ICE84 проверяет таблицу [адвтексекутесекуенце](advtexecutesequence-table.md), [таблицу Админексекутесекуенце](adminexecutesequence-table.md)и таблицу [инсталлексекутесекуенце](installexecutesequence-table.md) , чтобы убедиться, что следующие [стандартные действия](standard-actions.md) не были заданы с условиями в поле Condition.</span><span class="sxs-lookup"><span data-stu-id="b82fe-104">ICE84 checks the [AdvtExecuteSequence table](advtexecutesequence-table.md), [AdminExecuteSequence table](adminexecutesequence-table.md), and the [InstallExecuteSequence table](installexecutesequence-table.md) to verify that the following [standard actions](standard-actions.md) have not been set with conditions in the Condition field.</span></span>

-   [<span data-ttu-id="b82fe-105">Действие Костинитиализе</span><span class="sxs-lookup"><span data-stu-id="b82fe-105">CostInitialize action</span></span>](costinitialize-action.md)
-   [<span data-ttu-id="b82fe-106">Действие Костфинализе</span><span class="sxs-lookup"><span data-stu-id="b82fe-106">CostFinalize action</span></span>](costfinalize-action.md)
-   [<span data-ttu-id="b82fe-107">Действие Филекост</span><span class="sxs-lookup"><span data-stu-id="b82fe-107">FileCost action</span></span>](filecost-action.md)
-   [<span data-ttu-id="b82fe-108">Действие Инсталлвалидате</span><span class="sxs-lookup"><span data-stu-id="b82fe-108">InstallValidate action</span></span>](installvalidate-action.md)
-   [<span data-ttu-id="b82fe-109">Действие Инсталлинитиализе</span><span class="sxs-lookup"><span data-stu-id="b82fe-109">InstallInitialize action</span></span>](installinitialize-action.md)
-   [<span data-ttu-id="b82fe-110">Действие функции InstallFinalize</span><span class="sxs-lookup"><span data-stu-id="b82fe-110">InstallFinalize action</span></span>](installfinalize-action.md)
-   [<span data-ttu-id="b82fe-111">Действие Процесскомпонентс</span><span class="sxs-lookup"><span data-stu-id="b82fe-111">ProcessComponents action</span></span>](processcomponents-action.md)
-   [<span data-ttu-id="b82fe-112">Действие Публишфеатурес</span><span class="sxs-lookup"><span data-stu-id="b82fe-112">PublishFeatures action</span></span>](publishfeatures-action.md)
-   [<span data-ttu-id="b82fe-113">Действие Публишпродукт</span><span class="sxs-lookup"><span data-stu-id="b82fe-113">PublishProduct action</span></span>](publishproduct-action.md)
-   [<span data-ttu-id="b82fe-114">Действие Регистерпродукт</span><span class="sxs-lookup"><span data-stu-id="b82fe-114">RegisterProduct action</span></span>](registerproduct-action.md)
-   [<span data-ttu-id="b82fe-115">Действие Унпублишфеатурес</span><span class="sxs-lookup"><span data-stu-id="b82fe-115">UnpublishFeatures action</span></span>](unpublishfeatures-action.md)

<span data-ttu-id="b82fe-116">При обнаружении условий ICE84 отправляет предупреждение.</span><span class="sxs-lookup"><span data-stu-id="b82fe-116">If conditions are found, ICE84 posts a warning.</span></span>

## <a name="result"></a><span data-ttu-id="b82fe-117">Результат</span><span class="sxs-lookup"><span data-stu-id="b82fe-117">Result</span></span>

<span data-ttu-id="b82fe-118">ICE84 отправляет следующее предупреждение.</span><span class="sxs-lookup"><span data-stu-id="b82fe-118">ICE84 posts the following warning.</span></span>



| <span data-ttu-id="b82fe-119">ICE84, ошибка</span><span class="sxs-lookup"><span data-stu-id="b82fe-119">ICE84 error</span></span>                                                             | <span data-ttu-id="b82fe-120">Описание</span><span class="sxs-lookup"><span data-stu-id="b82fe-120">Description</span></span>                                           |
|-------------------------------------------------------------------------|-------------------------------------------------------|
| <span data-ttu-id="b82fe-121">Действие " \[ 1 \] ", найденное в таблице% s, является обязательным действием с условием.</span><span class="sxs-lookup"><span data-stu-id="b82fe-121">Action '\[1\]' found in %s table is a required action with a condition.</span></span> | <span data-ttu-id="b82fe-122">Было создано обязательное действие с условием.</span><span class="sxs-lookup"><span data-stu-id="b82fe-122">A required action has been authored with a condition.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="b82fe-123">См. также</span><span class="sxs-lookup"><span data-stu-id="b82fe-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b82fe-124">Справочник по ICE</span><span class="sxs-lookup"><span data-stu-id="b82fe-124">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



