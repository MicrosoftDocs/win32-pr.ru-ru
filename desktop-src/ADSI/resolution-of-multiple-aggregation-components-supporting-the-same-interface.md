---
title: Разрешение нескольких компонентов статистической обработки, поддерживающих один и тот же интерфейс
description: Обычно два расширения предоставляют один и тот же интерфейс ADSI.
ms.assetid: 87cb1a17-04f7-4ad0-989a-a9506dfdca05
ms.tgt_platform: multiple
keywords:
- Разрешение нескольких компонентов статистической обработки, поддерживающих интерфейс ADSI
- Разрешение нескольких компонентов статистической обработки, поддерживающих интерфейс ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f58b7b606a05543444a172e2f76b436f6048431
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105654111"
---
# <a name="resolution-of-multiple-aggregation-components-supporting-the-same-interface"></a><span data-ttu-id="bf2cf-105">Разрешение нескольких компонентов статистической обработки, поддерживающих один и тот же интерфейс</span><span class="sxs-lookup"><span data-stu-id="bf2cf-105">Resolution of Multiple Aggregation Components Supporting the Same Interface</span></span>

<span data-ttu-id="bf2cf-106">Обычно два расширения предоставляют один и тот же интерфейс ADSI.</span><span class="sxs-lookup"><span data-stu-id="bf2cf-106">It is uncommon that two extensions expose the same interface to ADSI.</span></span> <span data-ttu-id="bf2cf-107">В этом случае применяются следующие правила.</span><span class="sxs-lookup"><span data-stu-id="bf2cf-107">If this happens, the following rules apply:</span></span>

-   <span data-ttu-id="bf2cf-108">Если интерфейс, например **IMyInterface**, поддерживается как агрегатором (ADSI), так и любыми объектами расширения, **QueryInterface** всегда возвращает **IMyInterface** для ADSI.</span><span class="sxs-lookup"><span data-stu-id="bf2cf-108">If an interface, such as **IMyInterface**, is supported by both the aggregator (ADSI) and any extension objects, **QueryInterface** always returns the **IMyInterface** for ADSI.</span></span>
-   <span data-ttu-id="bf2cf-109">Если интерфейс, например **IMyInterface**, не поддерживается агрегатором (ADSI), но поддерживается более чем одним объектом расширения, то **QueryInterface** возвращает **IMyInterface** первого объекта расширения, указанного в реестре, который поддерживает интерфейс.</span><span class="sxs-lookup"><span data-stu-id="bf2cf-109">If an interface, such as **IMyInterface**, is not supported by the aggregator (ADSI), but is supported by more than one extension object, **QueryInterface** returns the **IMyInterface** of the first extension object listed in the registry that supports the interface.</span></span>

<span data-ttu-id="bf2cf-110">Имейте в виду, что порядок компонентов в реестре также влияет на разрешение конфликтов имен в службе автоматизации.</span><span class="sxs-lookup"><span data-stu-id="bf2cf-110">Be aware that the order of components in the registry also affects the resolution of name conflicts in Automation.</span></span> <span data-ttu-id="bf2cf-111">Дополнительные сведения см. [в разделе разрешение конфликтов имен функций и свойств в службе автоматизации в расширениях](resolution-of-functionproperty-name-conflicts-in-automation-in-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="bf2cf-111">For more information, see [Resolution of Function/Property Name Conflicts in Automation in Extensions](resolution-of-functionproperty-name-conflicts-in-automation-in-extensions.md).</span></span>

 

 




