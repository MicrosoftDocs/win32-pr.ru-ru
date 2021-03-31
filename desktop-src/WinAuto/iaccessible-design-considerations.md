---
title: Рекомендации по проектированию IAccessible
description: В этом разделе обсуждаются проблемы, с которыми сталкиваются разработчики сервера при проектировании классов на основе интерфейса IAccessible.
ms.assetid: 240cdff1-a4c3-477a-b146-2ac295d7a148
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ebb8648bd0398117f1d3da895ff4b4288aa5e7c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330560"
---
# <a name="iaccessible-design-considerations"></a><span data-ttu-id="ad86c-103">Рекомендации по проектированию IAccessible</span><span class="sxs-lookup"><span data-stu-id="ad86c-103">IAccessible Design Considerations</span></span>

<span data-ttu-id="ad86c-104">В этом разделе обсуждаются проблемы, с которыми сталкиваются разработчики сервера при проектировании классов на основе интерфейса [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .</span><span class="sxs-lookup"><span data-stu-id="ad86c-104">This section discusses the issues that server developer face when designing classes based on the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="ad86c-105">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="ad86c-105">In this section</span></span>

-   [<span data-ttu-id="ad86c-106">Выбор времени создания объектов со специальными возможностями</span><span class="sxs-lookup"><span data-stu-id="ad86c-106">Choosing When to Create Accessible Objects</span></span>](choosing-when-to-create-accessible-objects.md)
-   [<span data-ttu-id="ad86c-107">Выбор свойств для поддержки</span><span class="sxs-lookup"><span data-stu-id="ad86c-107">Choosing Which Properties to Support</span></span>](choosing-which-properties-to-support.md)
-   [<span data-ttu-id="ad86c-108">Выбор содержимого для описательных свойств</span><span class="sxs-lookup"><span data-stu-id="ad86c-108">Choosing the Content for Descriptive Properties</span></span>](choosing-the-content-for-descriptive-properties.md)
-   [<span data-ttu-id="ad86c-109">Задание свойств для анимированных или перемещаемых объектов</span><span class="sxs-lookup"><span data-stu-id="ad86c-109">Setting Properties for Animated or Moving Objects</span></span>](setting-properties-for-animated-or-moving-objects.md)
-   [<span data-ttu-id="ad86c-110">Создание подходящих Виневентс</span><span class="sxs-lookup"><span data-stu-id="ad86c-110">Generating Appropriate WinEvents</span></span>](generating-appropriate-winevents.md)
-   [<span data-ttu-id="ad86c-111">Предоставление дополнительных сведений, не охваченных интерфейсом IAccessible</span><span class="sxs-lookup"><span data-stu-id="ad86c-111">Exposing Additional Information Not Covered by IAccessible Interface</span></span>](exposing-additional-information-not-covered-by-iaccessible-interface.md)

 

 




