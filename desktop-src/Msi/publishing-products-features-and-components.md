---
description: Чтобы опубликовать продукт, компонент или компонент, используйте одно из действий публикации.
ms.assetid: 2c395d81-4f46-444e-a275-7a5d806e473c
title: Публикация продуктов, компонентов и компонентов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cdd8c8445491646399c7d118a69ae497d27faff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264384"
---
# <a name="publishing-products-features-and-components"></a><span data-ttu-id="98646-103">Публикация продуктов, компонентов и компонентов</span><span class="sxs-lookup"><span data-stu-id="98646-103">Publishing Products, Features, and Components</span></span>

<span data-ttu-id="98646-104">Чтобы [опубликовать](components-and-features.md) продукт, компонент или компонент, используйте одно из действий публикации.</span><span class="sxs-lookup"><span data-stu-id="98646-104">To [publish](components-and-features.md) a product, component, or feature, use one of the publishing actions.</span></span> <span data-ttu-id="98646-105">[Действие публишпродукт](publishproduct-action.md) регистрирует сведения о продукте в системе.</span><span class="sxs-lookup"><span data-stu-id="98646-105">The [PublishProduct action](publishproduct-action.md) registers the product information with the system.</span></span> <span data-ttu-id="98646-106">После выполнения действия Публишпродукт опубликуйте компоненты с помощью [действия публишкомпонентс](publishcomponents-action.md), которое, в свою очередь, использует [таблицу публишкомпонент](publishcomponent-table.md) для определения компонентов, которые заданы как объявленные.</span><span class="sxs-lookup"><span data-stu-id="98646-106">After executing the PublishProduct action, publish the components with the [PublishComponents action](publishcomponents-action.md), which in turn uses the [PublishComponent table](publishcomponent-table.md) to determine the components that are set as advertised.</span></span> <span data-ttu-id="98646-107">Для публикации на основе каждого компонента следует вызвать [действие публишфеатурес](publishfeatures-action.md).</span><span class="sxs-lookup"><span data-stu-id="98646-107">To publish on a per-feature basis, invoke the [PublishFeatures action](publishfeatures-action.md).</span></span> <span data-ttu-id="98646-108">Это действие использует [таблицу феатурекомпонентс](featurecomponents-table.md) в качестве данных для разрешения того, какие функции объявляются.</span><span class="sxs-lookup"><span data-stu-id="98646-108">This action uses the [FeatureComponents table](featurecomponents-table.md) as data to resolve which features are advertised.</span></span>

<span data-ttu-id="98646-109">Существуют также два соответствующих действия, которые отменяют публикацию компонента или компонента: [действие унпублишкомпонентс](unpublishcomponents-action.md) и [действие унпублишфеатурес](unpublishfeatures-action.md).</span><span class="sxs-lookup"><span data-stu-id="98646-109">There are also two corresponding actions that unpublish a feature or a component: the [UnpublishComponents action](unpublishcomponents-action.md) and the [UnpublishFeatures action](unpublishfeatures-action.md).</span></span>

 

 



