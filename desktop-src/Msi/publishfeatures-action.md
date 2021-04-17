---
description: Действие Публишфеатурес записывает состояние каждого компонента в системный реестр.
ms.assetid: 8205e865-e625-43b9-8ce9-cff8026b2717
title: Действие Публишфеатурес
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f5356ef89aa2651c470917a9b8d81b79ee83d01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673678"
---
# <a name="publishfeatures-action"></a><span data-ttu-id="4d875-103">Действие Публишфеатурес</span><span class="sxs-lookup"><span data-stu-id="4d875-103">PublishFeatures Action</span></span>

<span data-ttu-id="4d875-104">Действие Публишфеатурес записывает состояние каждого компонента в системный реестр.</span><span class="sxs-lookup"><span data-stu-id="4d875-104">The PublishFeatures action writes each feature's state into the system registry.</span></span> <span data-ttu-id="4d875-105">Состояние компонента может отсутствовать, объявляться или быть установлено.</span><span class="sxs-lookup"><span data-stu-id="4d875-105">The feature state may be either absent, advertised, or installed.</span></span> <span data-ttu-id="4d875-106">Действие Публишфеатурес также записывает сопоставление компонентов компонента в системный реестр для каждого установленного компонента.</span><span class="sxs-lookup"><span data-stu-id="4d875-106">The PublishFeatures action also writes the feature-component mapping into the system registry for each installed feature.</span></span>

<span data-ttu-id="4d875-107">Действие Публишфеатурес запрашивает [таблицу феатурекомпонентс](featurecomponents-table.md), [таблицу функций](feature-table.md)и [таблицу компонентов](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="4d875-107">The PublishFeatures action queries the [FeatureComponents table](featurecomponents-table.md), [Feature table](feature-table.md), and [Component table](component-table.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="4d875-108">Ограничения последовательности</span><span class="sxs-lookup"><span data-stu-id="4d875-108">Sequence Restrictions</span></span>

<span data-ttu-id="4d875-109">Действие Публишфеатурес должно предшествовать [публишпродукт](publishproduct-action.md).</span><span class="sxs-lookup"><span data-stu-id="4d875-109">The PublishFeatures action must come before [PublishProduct](publishproduct-action.md).</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="4d875-110">Сообщения Актиондата</span><span class="sxs-lookup"><span data-stu-id="4d875-110">ActionData Messages</span></span>



| <span data-ttu-id="4d875-111">Поле</span><span class="sxs-lookup"><span data-stu-id="4d875-111">Field</span></span> | <span data-ttu-id="4d875-112">Описание данных действия</span><span class="sxs-lookup"><span data-stu-id="4d875-112">Description of action data</span></span>        |
|-------|-----------------------------------|
| <span data-ttu-id="4d875-113">\[1\]</span><span class="sxs-lookup"><span data-stu-id="4d875-113">\[1\]</span></span> | <span data-ttu-id="4d875-114">Идентификатор объявленной функции.</span><span class="sxs-lookup"><span data-stu-id="4d875-114">Identifier of advertised feature.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="4d875-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4d875-115">Remarks</span></span>

<span data-ttu-id="4d875-116">Действие Публишфеатурес публикует композицию всех выбранных для объявления или установки компонентов.</span><span class="sxs-lookup"><span data-stu-id="4d875-116">The PublishFeatures action publishes the composition of all features that are selected to be advertised or installed.</span></span>

 

 



