---
title: Быть не эксклюзивным
description: Быть не эксклюзивным
ms.assetid: 7a44840d-6bf9-4c12-ba14-66d7067a984d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b637bcf0860ccc4917b1af344664f9828b0da8d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104410780"
---
# <a name="be-non-exclusive"></a><span data-ttu-id="3af01-103">Быть не эксклюзивным</span><span class="sxs-lookup"><span data-stu-id="3af01-103">Be Non-Exclusive</span></span>

<span data-ttu-id="3af01-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="3af01-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="3af01-105">Интерактивные символы могут использоваться в пользовательском интерфейсе в качестве помощников, руководств, представительов, Обучайтесь, агентов по продажам или в различных других ролях.</span><span class="sxs-lookup"><span data-stu-id="3af01-105">Interactive characters can be employed in the user interface as assistants, guides, entertainers, storytellers, sales agents, or in a variety of other roles.</span></span> <span data-ttu-id="3af01-106">Символ, автоматически выполняемый или помогающий, не должен быть спроектирован в противоположность принципу разработки, позволяющей пользователю управлять.</span><span class="sxs-lookup"><span data-stu-id="3af01-106">A character that automatically performs or assists should not be designed contrary to the design principle of keeping the user in control.</span></span> <span data-ttu-id="3af01-107">При добавлении символа в интерфейс веб-сайта или обычного приложения используйте символ в качестве расширения, а не замены основного интерфейса.</span><span class="sxs-lookup"><span data-stu-id="3af01-107">When adding a character to the interface of a website or conventional application, use the character as an enhancement, rather than a replacement of, the primary interface.</span></span> <span data-ttu-id="3af01-108">Избегайте реализации какой-либо функции или операции, для которой требуется только символ.</span><span class="sxs-lookup"><span data-stu-id="3af01-108">Avoid implementing any feature or operation that exclusively requires a character.</span></span>

<span data-ttu-id="3af01-109">Аналогичным образом позвольте пользователю выбрать, когда им нужно взаимодействовать с вашим символом.</span><span class="sxs-lookup"><span data-stu-id="3af01-109">Similarly, let the user choose when they want to interact with your character.</span></span> <span data-ttu-id="3af01-110">Пользователь должен иметь возможность отклонить символ и вернуть его только с разрешением пользователя.</span><span class="sxs-lookup"><span data-stu-id="3af01-110">A user should be able to dismiss the character and have it return only with the user's permission.</span></span> <span data-ttu-id="3af01-111">Принудительное взаимодействие с символами для пользователей может иметь серьезные негативные последствия.</span><span class="sxs-lookup"><span data-stu-id="3af01-111">Forcing character interaction on users can have a serious negative effect.</span></span> <span data-ttu-id="3af01-112">Для поддержки пользовательского управления взаимодействием с символами Microsoft Agent автоматически включает команды "скрыть" и "Показать".</span><span class="sxs-lookup"><span data-stu-id="3af01-112">To support user control of character interaction, Microsoft Agent automatically includes Hide and Show commands.</span></span> <span data-ttu-id="3af01-113">API Microsoft Agent также поддерживает эти методы, поэтому вы можете включить поддержку этих функций в своем интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="3af01-113">The Microsoft Agent API also supports these methods, so you can include support for these functions in your own interface.</span></span> <span data-ttu-id="3af01-114">Кроме того, Пользовательский интерфейс Microsoft Agent включает глобальные свойства, позволяющие пользователю переопределить определенные параметры вывода символов.</span><span class="sxs-lookup"><span data-stu-id="3af01-114">In addition, Microsoft Agent's user interface includes global properties that enable the user to override certain character output options.</span></span> <span data-ttu-id="3af01-115">Чтобы обеспечить соблюдение настроек пользователя, эти свойства не могут быть переопределены через API.</span><span class="sxs-lookup"><span data-stu-id="3af01-115">To ensure that the user's preferences are maintained, these properties cannot be overridden through the API.</span></span>

 

 




