---
description: .
ms.assetid: ACAC2375-EA6C-4AA1-90B7-0BF237A51C02
title: Устранение проблем совместимости в веб-приложениях с помощью представления совместимости
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a43f4ff54a919058127a5f72ba60f3683c6583e1
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105713269"
---
# <a name="fixing-compatibility-issues-in-web-applications-by-using-compatibility-view"></a><span data-ttu-id="02bf4-103">Устранение проблем совместимости в веб-приложениях с помощью представления совместимости</span><span class="sxs-lookup"><span data-stu-id="02bf4-103">Fixing Compatibility Issues in Web Applications by Using Compatibility View</span></span>

<span data-ttu-id="02bf4-104">В этом разделе описаны основные шаги по устранению рисков и способы планирования будущей совместимости приложений в настоящее время.</span><span class="sxs-lookup"><span data-stu-id="02bf4-104">This section describes basic mitigation steps and how to plan for future application compatibility while you are addressing any issues now.</span></span>

<span data-ttu-id="02bf4-105">Windows Internet Explorer поддерживает устаревшие модели Internet Explorer, когда это возможно, так что сайты, разрабатываемые для них, продолжают работать в более новых версиях Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="02bf4-105">Windows Internet Explorer supports the legacy Internet Explorer models whenever feasible so that sites that you develop to them continue to behave as expected in newer versions of Internet Explorer.</span></span> <span data-ttu-id="02bf4-106">Начиная с Windows Internet Explorer 8, можно выбрать поддержку устаревшего поведения, выбрав режим рендеринга отдельно для каждой страницы.</span><span class="sxs-lookup"><span data-stu-id="02bf4-106">Starting with Windows Internet Explorer 8, you can choose to support legacy behaviors by selecting the rendering mode on a page-by-page basis.</span></span>

<span data-ttu-id="02bf4-107">Internet Explorer 8 включает следующие режимы рендеринга, которые можно задать с помощью заголовка X-UA-Compatible.</span><span class="sxs-lookup"><span data-stu-id="02bf4-107">Internet Explorer 8 includes the following rendering modes that you can set by using the X-UA-Compatible header.</span></span>



| <span data-ttu-id="02bf4-108">Значение содержимого</span><span class="sxs-lookup"><span data-stu-id="02bf4-108">Content value</span></span> | <span data-ttu-id="02bf4-109">Описание</span><span class="sxs-lookup"><span data-stu-id="02bf4-109">Description</span></span>                                                                           |
|---------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="02bf4-110">IE=5</span><span class="sxs-lookup"><span data-stu-id="02bf4-110">IE=5</span></span>          | <span data-ttu-id="02bf4-111">Используйте режим "несовместимости".</span><span class="sxs-lookup"><span data-stu-id="02bf4-111">Use quirks mode.</span></span>                                                                      |
| <span data-ttu-id="02bf4-112">IE = 7</span><span class="sxs-lookup"><span data-stu-id="02bf4-112">IE=7</span></span>          | <span data-ttu-id="02bf4-113">Всегда используйте режим Windows Internet Explorer 7.</span><span class="sxs-lookup"><span data-stu-id="02bf4-113">Always use Windows Internet Explorer 7 mode.</span></span>                                          |
| <span data-ttu-id="02bf4-114">IE = EmulateIE7</span><span class="sxs-lookup"><span data-stu-id="02bf4-114">IE=EmulateIE7</span></span> | <span data-ttu-id="02bf4-115">Отображать в режиме Internet Explorer 7, если только сайт не имеет случайного DOCTYPE.</span><span class="sxs-lookup"><span data-stu-id="02bf4-115">Display in Internet Explorer 7 mode unless the site has the quirks DOCTYPE.</span></span>           |
| <span data-ttu-id="02bf4-116">IE = 8</span><span class="sxs-lookup"><span data-stu-id="02bf4-116">IE=8</span></span>          | <span data-ttu-id="02bf4-117">Всегда используйте режим Internet Explorer 8.</span><span class="sxs-lookup"><span data-stu-id="02bf4-117">Always use Internet Explorer 8 mode.</span></span>                                                  |
| <span data-ttu-id="02bf4-118">IE = EmulateIE8</span><span class="sxs-lookup"><span data-stu-id="02bf4-118">IE=EmulateIE8</span></span> | <span data-ttu-id="02bf4-119">Переопределение представления совместимости на клиентских компьютерах и использование режима Internet Explorer 8.</span><span class="sxs-lookup"><span data-stu-id="02bf4-119">Override Compatibility View on client machines and use Internet Explorer 8 mode.</span></span>      |
| <span data-ttu-id="02bf4-120">IE=Edge</span><span class="sxs-lookup"><span data-stu-id="02bf4-120">IE=Edge</span></span>       | <span data-ttu-id="02bf4-121">Отображение в последнем режиме.</span><span class="sxs-lookup"><span data-stu-id="02bf4-121">Display in the latest mode.</span></span> <span data-ttu-id="02bf4-122">В Internet Explorer 8 это значение эквивалентно IE = 8.</span><span class="sxs-lookup"><span data-stu-id="02bf4-122">In Internet Explorer 8, this value is equivalent to IE=8.</span></span> |



 

<span data-ttu-id="02bf4-123">В следующих разделах описывается обновление веб-приложений с помощью представления совместимости.</span><span class="sxs-lookup"><span data-stu-id="02bf4-123">The following topics describe how to update web applications by using Compatibility View.</span></span>



| <span data-ttu-id="02bf4-124">Раздел</span><span class="sxs-lookup"><span data-stu-id="02bf4-124">Topic</span></span>                                                                                                  | <span data-ttu-id="02bf4-125">Описание</span><span class="sxs-lookup"><span data-stu-id="02bf4-125">Description</span></span>                                                                    |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="02bf4-126">Что такое представление совместимости</span><span class="sxs-lookup"><span data-stu-id="02bf4-126">What Is Compatibility View</span></span>](what-is-compatibility-view-.md)                                          | <span data-ttu-id="02bf4-127">Описывает представление совместимости.</span><span class="sxs-lookup"><span data-stu-id="02bf4-127">Describes Compatibility View.</span></span>                                                  |
| [<span data-ttu-id="02bf4-128">Зачем нужно представление совместимости?</span><span class="sxs-lookup"><span data-stu-id="02bf4-128">Why Do You Need Compatibility View?</span></span>](why-do-you-need-compatibility-view-.md)                         | <span data-ttu-id="02bf4-129">Описание причин использования представления совместимости.</span><span class="sxs-lookup"><span data-stu-id="02bf4-129">Describes why you should use Compatibility View.</span></span>                               |
| [<span data-ttu-id="02bf4-130">Использование тега meta для обеспечения совместимости в будущем</span><span class="sxs-lookup"><span data-stu-id="02bf4-130">Use the Meta Tag to Ensure Future Compatibility</span></span>](use-the-meta-tag-to-ensure-future-compatibility.md) | <span data-ttu-id="02bf4-131">Описывает, как можно использовать элемент **meta** для обеспечения совместимости в будущем.</span><span class="sxs-lookup"><span data-stu-id="02bf4-131">Describes how you can use the **meta** element to ensure future compatibility.</span></span> |



 

 

 



