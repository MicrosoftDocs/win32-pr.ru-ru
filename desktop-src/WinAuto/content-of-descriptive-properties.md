---
title: Содержимое описательных свойств
description: Интерфейс IAccessible предоставляет описательные свойства, описывающие различные аспекты объекта.
ms.assetid: e6c1d1a3-417d-4aea-abac-f84a55f666b7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 271dc920034802b87afd4c76ab7ede6bb9476d99
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532183"
---
# <a name="content-of-descriptive-properties"></a><span data-ttu-id="72a3f-103">Содержимое описательных свойств</span><span class="sxs-lookup"><span data-stu-id="72a3f-103">Content of Descriptive Properties</span></span>

<span data-ttu-id="72a3f-104">Интерфейс [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) предоставляет описательные свойства, описывающие различные аспекты объекта.</span><span class="sxs-lookup"><span data-stu-id="72a3f-104">The [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface provides descriptive properties, which describe various aspects of an object.</span></span> <span data-ttu-id="72a3f-105">Некоторые из этих свойств относятся к содержимому; другие свойства имеют содержимое, состоящее из описательного текста, предоставляемого сервером.</span><span class="sxs-lookup"><span data-stu-id="72a3f-105">Some of these properties are content specific; other properties have content consisting of descriptive text that is provided by the server.</span></span> <span data-ttu-id="72a3f-106">Тип сведений для каждого свойства зависит от объекта.</span><span class="sxs-lookup"><span data-stu-id="72a3f-106">The type of information for each property varies depending on the object.</span></span>

<span data-ttu-id="72a3f-107">В следующих разделах описываются сведения, которые клиенты получают из этих свойств.</span><span class="sxs-lookup"><span data-stu-id="72a3f-107">The following topics describe information that clients obtain from these properties.</span></span> <span data-ttu-id="72a3f-108">Они также предоставляют серверы с предложениями по выбору содержимого.</span><span class="sxs-lookup"><span data-stu-id="72a3f-108">They also provide servers with suggestions for choosing content.</span></span>

-   [<span data-ttu-id="72a3f-109">Свойство Name</span><span class="sxs-lookup"><span data-stu-id="72a3f-109">Name Property</span></span>](name-property.md)
-   [<span data-ttu-id="72a3f-110">Свойство Role</span><span class="sxs-lookup"><span data-stu-id="72a3f-110">Role Property</span></span>](role-property.md)
-   [<span data-ttu-id="72a3f-111">Свойство State</span><span class="sxs-lookup"><span data-stu-id="72a3f-111">State Property</span></span>](state-property.md)
-   [<span data-ttu-id="72a3f-112">Value, свойство</span><span class="sxs-lookup"><span data-stu-id="72a3f-112">Value Property</span></span>](value-property.md)
-   [<span data-ttu-id="72a3f-113">Свойство Description</span><span class="sxs-lookup"><span data-stu-id="72a3f-113">Description Property</span></span>](description-property.md)
-   [<span data-ttu-id="72a3f-114">Свойство справки</span><span class="sxs-lookup"><span data-stu-id="72a3f-114">Help Property</span></span>](help-property.md)
-   [<span data-ttu-id="72a3f-115">Хелптопик, свойство</span><span class="sxs-lookup"><span data-stu-id="72a3f-115">HelpTopic Property</span></span>](helptopic-property.md)
-   [<span data-ttu-id="72a3f-116">Кэйбоардшорткут, свойство</span><span class="sxs-lookup"><span data-stu-id="72a3f-116">KeyboardShortcut Property</span></span>](keyboardshortcut-property.md)
-   [<span data-ttu-id="72a3f-117">DefaultAction, свойство</span><span class="sxs-lookup"><span data-stu-id="72a3f-117">DefaultAction Property</span></span>](defaultaction-property.md)

<span data-ttu-id="72a3f-118">При проектировании объектов со специальными возможностями разработчики сервера также должны обратиться к следующим разделам:</span><span class="sxs-lookup"><span data-stu-id="72a3f-118">When designing accessible objects, server developers should also refer to the following topics:</span></span>

-   [<span data-ttu-id="72a3f-119">Выбор свойств для поддержки</span><span class="sxs-lookup"><span data-stu-id="72a3f-119">Choosing Which Properties to Support</span></span>](choosing-which-properties-to-support.md)
-   [<span data-ttu-id="72a3f-120">Выбор содержимого для описательных свойств</span><span class="sxs-lookup"><span data-stu-id="72a3f-120">Choosing the Content for Descriptive Properties</span></span>](choosing-the-content-for-descriptive-properties.md)

<span data-ttu-id="72a3f-121">Сведения о параметрах и возвращаемых значениях этих свойств см. в разделе [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) справочника по Microsoft Active Accessibility [C/C++](c-c---reference.md).</span><span class="sxs-lookup"><span data-stu-id="72a3f-121">For information about the parameters and return values of these properties, see the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) section of the Microsoft Active Accessibility[C/C++ Reference](c-c---reference.md).</span></span>

 

 




