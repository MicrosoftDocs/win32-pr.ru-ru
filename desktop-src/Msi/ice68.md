---
description: ICE68 проверяет, что все типы пользовательских действий, необходимые для установки, являются допустимыми.
ms.assetid: a37d6d6c-3005-425b-883a-6fe074b9d708
title: ICE68
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1392db6ec05085c672ed70c8f035ea8eed3015e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664549"
---
# <a name="ice68"></a><span data-ttu-id="01458-103">ICE68</span><span class="sxs-lookup"><span data-stu-id="01458-103">ICE68</span></span>

<span data-ttu-id="01458-104">ICE68 проверяет, что все типы пользовательских действий, необходимые для установки, являются допустимыми.</span><span class="sxs-lookup"><span data-stu-id="01458-104">ICE68 checks that all custom action types needed for an installation are valid.</span></span> <span data-ttu-id="01458-105">Ошибка исправления ошибки, о которой сообщила ICE68, приводит к сбою установки, которая пытается выполнить действие.</span><span class="sxs-lookup"><span data-stu-id="01458-105">Failure to fix the error reported by ICE68 causes an installation that attempts to execute the action to fail.</span></span> <span data-ttu-id="01458-106">ICE68 выдает предупреждение, если атрибут **msidbCustomActionTypeNoImpersonate** задан без установки атрибута **мсидбкустомактионтипеинскрипт** .</span><span class="sxs-lookup"><span data-stu-id="01458-106">ICE68 issues a warning if the **msidbCustomActionTypeNoImpersonate** attribute is set without also setting the **msidbCustomActionTypeInScript** attribute.</span></span>

## <a name="result"></a><span data-ttu-id="01458-107">Результат</span><span class="sxs-lookup"><span data-stu-id="01458-107">Result</span></span>

<span data-ttu-id="01458-108">ICE68 возвращает ошибку, если тип действия, необходимый для установки, является недопустимым.</span><span class="sxs-lookup"><span data-stu-id="01458-108">ICE68 returns an error if an action type needed for an installation is invalid.</span></span>

## <a name="example"></a><span data-ttu-id="01458-109">Пример</span><span class="sxs-lookup"><span data-stu-id="01458-109">Example</span></span>

<span data-ttu-id="01458-110">ICE68 отправляет следующее предупреждение, если в настраиваемом действии задан бит **msidbCustomActionTypeNoImpersonate** , установленный в поле Type таблицы CustomAction, без **мсидбкустомактионтипеинскрипт** также.</span><span class="sxs-lookup"><span data-stu-id="01458-110">ICE68 posts the following warning if a custom action has the **msidbCustomActionTypeNoImpersonate** bit set in the Type field of the CustomAction table without the **msidbCustomActionTypeInScript** also set.</span></span>

``` syntax
Even though custom action '[2]' is marked to be elevated (with 
attribute msidbCustomActionTypeNoImpersonate), it will not be run with elevated 
privileges because it's not deferred (with attribute msidbCustomActionTypeInScript).
```

<span data-ttu-id="01458-111">Чтобы устранить это предупреждение, включите **мсидбкустомактионтипеинскрипт** (0x400), если настраиваемое действие содержит **msidbCustomActionTypeNoImpersonate** (0x800).</span><span class="sxs-lookup"><span data-stu-id="01458-111">To fix this warning, include **msidbCustomActionTypeInScript** (0x400) if the custom action includes **msidbCustomActionTypeNoImpersonate** (0x800).</span></span> <span data-ttu-id="01458-112">В противном случае установщик игнорирует атрибут **msidbCustomActionTypeNoImpersonate** .</span><span class="sxs-lookup"><span data-stu-id="01458-112">Otherwise the installer ignores the **msidbCustomActionTypeNoImpersonate** attribute.</span></span> <span data-ttu-id="01458-113">Дополнительные сведения см. в разделе [пользовательские действия In-Script параметры выполнения](custom-action-in-script-execution-options.md).</span><span class="sxs-lookup"><span data-stu-id="01458-113">For more information, see [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

<span data-ttu-id="01458-114">ICE68 сообщает об ошибке в приведенном примере:</span><span class="sxs-lookup"><span data-stu-id="01458-114">ICE68 reports the following error for the example shown:</span></span>

``` syntax
Invalid custom action type for action 'Action1'.
```

<span data-ttu-id="01458-115">1027 не является допустимым типом действия.</span><span class="sxs-lookup"><span data-stu-id="01458-115">1027 is not a valid action type.</span></span>

<span data-ttu-id="01458-116">Чтобы устранить эту ошибку, выберите допустимый тип настраиваемого действия.</span><span class="sxs-lookup"><span data-stu-id="01458-116">To fix this error, choose a valid custom action type.</span></span>

<span data-ttu-id="01458-117">[Таблица CustomAction](customaction-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="01458-117">[CustomAction Table](customaction-table.md) (partial)</span></span>



| <span data-ttu-id="01458-118">Действие</span><span class="sxs-lookup"><span data-stu-id="01458-118">Action</span></span>  | <span data-ttu-id="01458-119">Тип</span><span class="sxs-lookup"><span data-stu-id="01458-119">Type</span></span> | <span data-ttu-id="01458-120">Источник</span><span class="sxs-lookup"><span data-stu-id="01458-120">Source</span></span>   | <span data-ttu-id="01458-121">Назначение</span><span class="sxs-lookup"><span data-stu-id="01458-121">Target</span></span>     |
|---------|------|----------|------------|
| <span data-ttu-id="01458-122">Action1 превышают</span><span class="sxs-lookup"><span data-stu-id="01458-122">Action1</span></span> | <span data-ttu-id="01458-123">1027</span><span class="sxs-lookup"><span data-stu-id="01458-123">1027</span></span> | <span data-ttu-id="01458-124">Аргумент</span><span class="sxs-lookup"><span data-stu-id="01458-124">Argument</span></span> | <span data-ttu-id="01458-125">Component1</span><span class="sxs-lookup"><span data-stu-id="01458-125">Component1</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="01458-126">См. также</span><span class="sxs-lookup"><span data-stu-id="01458-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="01458-127">Справочник по ICE</span><span class="sxs-lookup"><span data-stu-id="01458-127">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



