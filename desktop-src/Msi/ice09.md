---
description: ICE09 проверяет, что для каждого компонента, помеченного для установки в Системфолдер, задан постоянный бит.
ms.assetid: b4e11d75-4214-49de-ac12-6f360771ad73
title: ICE09
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01cd20a1b354888877be0f5d456b6d6af2bdec82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103815200"
---
# <a name="ice09"></a><span data-ttu-id="c0350-103">ICE09</span><span class="sxs-lookup"><span data-stu-id="c0350-103">ICE09</span></span>

<span data-ttu-id="c0350-104">ICE09 проверяет, что для каждого компонента, помеченного для установки в Системфолдер, задан постоянный бит.</span><span class="sxs-lookup"><span data-stu-id="c0350-104">ICE09 validates that the permanent bit is set for every component marked for installation into the SystemFolder.</span></span> <span data-ttu-id="c0350-105">ICE09 отправляет предупреждение, поскольку следует избегать установки непостоянных системных компонентов в Системфолдер.</span><span class="sxs-lookup"><span data-stu-id="c0350-105">ICE09 posts a warning because you should avoid installing non-permanent system components to the SystemFolder.</span></span> <span data-ttu-id="c0350-106">Чтобы предотвратить это предупреждение, установите постоянный бит в столбце Attributes [таблицы Component](component-table.md) для каждого компонента, помеченного для установки в системфолдер.</span><span class="sxs-lookup"><span data-stu-id="c0350-106">To prevent this warning, set the Permanent bit in the Attributes column of the [Component table](component-table.md) for every component that is marked for installation into the SystemFolder.</span></span> <span data-ttu-id="c0350-107">Проверка не выполняется, если в базе данных отсутствует таблица компонентов.</span><span class="sxs-lookup"><span data-stu-id="c0350-107">No validation is done if the database does not have a Component table.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c0350-108">См. также</span><span class="sxs-lookup"><span data-stu-id="c0350-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c0350-109">Справочник по ICE</span><span class="sxs-lookup"><span data-stu-id="c0350-109">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



