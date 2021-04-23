---
description: Создание временной шкалы
ms.assetid: 4909f797-d296-4c9f-83fb-543e48bbe75d
title: Создание временной шкалы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c16b1134eb92b3e3ac5a0f1919d7c4a2736b206
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104422990"
---
# <a name="constructing-a-timeline"></a><span data-ttu-id="30730-103">Создание временной шкалы</span><span class="sxs-lookup"><span data-stu-id="30730-103">Constructing a Timeline</span></span>

<span data-ttu-id="30730-104">\[Этот API не поддерживается и может быть изменен или недоступен в будущем.\]</span><span class="sxs-lookup"><span data-stu-id="30730-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="30730-105">В этой статье описывается создание временной шкалы в [службах редактирования DirectShow](directshow-editing-services.md) (DES).</span><span class="sxs-lookup"><span data-stu-id="30730-105">This article describes how to construct a timeline in [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span> <span data-ttu-id="30730-106">В нем представлен пример консольного приложения, которое создает временную шкалу и готовит ее к просмотру.</span><span class="sxs-lookup"><span data-stu-id="30730-106">It presents an example console application that creates a timeline and renders it.</span></span> <span data-ttu-id="30730-107">Временная шкала является минимальной, состоящей из одной видеогруппы с одним исходным клипом, но она демонстрирует большинство концепций, необходимых для создания более сложных временных шкал.</span><span class="sxs-lookup"><span data-stu-id="30730-107">The timeline is minimal, consisting of a single video group with one source clip, but it demonstrates most of the concepts needed to create more complex timelines.</span></span>

<span data-ttu-id="30730-108">Эта статья содержит следующие разделы.</span><span class="sxs-lookup"><span data-stu-id="30730-108">This article contains the following topics.</span></span>

-   [<span data-ttu-id="30730-109">Создание объектов временной шкалы</span><span class="sxs-lookup"><span data-stu-id="30730-109">Creating Timeline Objects</span></span>](creating-timeline-objects.md)
-   [<span data-ttu-id="30730-110">Создание групп, композиций и дорожек</span><span class="sxs-lookup"><span data-stu-id="30730-110">Creating Groups, Compositions, and Tracks</span></span>](creating-groups-compositions-and-tracks.md)
-   [<span data-ttu-id="30730-111">Настройка типа носителя группы</span><span class="sxs-lookup"><span data-stu-id="30730-111">Setting the Group Media Type</span></span>](setting-the-group-media-type.md)
-   [<span data-ttu-id="30730-112">Добавление источника</span><span class="sxs-lookup"><span data-stu-id="30730-112">Adding a Source</span></span>](adding-a-source.md)
-   [<span data-ttu-id="30730-113">Создание временной шкалы: пример кода</span><span class="sxs-lookup"><span data-stu-id="30730-113">Creating a Timeline: Example Code</span></span>](creating-a-timeline--example-code.md)

## <a name="related-topics"></a><span data-ttu-id="30730-114">См. также</span><span class="sxs-lookup"><span data-stu-id="30730-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="30730-115">Использование служб редактирования DirectShow</span><span class="sxs-lookup"><span data-stu-id="30730-115">Using DirectShow Editing Services</span></span>](using-directshow-editing-services.md)
</dt> </dl>

 

 



