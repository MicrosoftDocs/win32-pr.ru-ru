---
description: Композиция и разложение
ms.assetid: c1aefd92-b47f-4af1-8299-9ba401ad5fe8
title: Композиция и разложение
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7dce1e1df87b5ffc5c65e9090c6fb7266b972d3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105672982"
---
# <a name="composition-and-layering"></a><span data-ttu-id="87719-103">Композиция и разложение</span><span class="sxs-lookup"><span data-stu-id="87719-103">Composition and Layering</span></span>

<span data-ttu-id="87719-104">\[Этот API не поддерживается и может быть изменен или недоступен в будущем.\]</span><span class="sxs-lookup"><span data-stu-id="87719-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="87719-105">В коллекции дорожек первая дорожка имеет самый низкий приоритет (приоритет 0), а каждая последующая дорожка имеет приоритет на один уровень выше.</span><span class="sxs-lookup"><span data-stu-id="87719-105">In a collection of tracks, the first track has the lowest priority (priority 0) and each subsequent track has a priority one level higher.</span></span> <span data-ttu-id="87719-106">На каждом уровне приоритета исходные клипы в этой дорожке скрывают исходные клипы в дорожках, за исключением случаев, когда этот слой также содержит переход.</span><span class="sxs-lookup"><span data-stu-id="87719-106">At each priority level, the source clips in that track hide the source clips in the tracks below it, unless that layer also contains a transition.</span></span> <span data-ttu-id="87719-107">Поэтому вы можете представить DES, делая несколько проходов при подготовке к просмотру.</span><span class="sxs-lookup"><span data-stu-id="87719-107">Thus you can imagine DES making several passes when it renders.</span></span>

<span data-ttu-id="87719-108">Во первых, он отображает значение Track 0.</span><span class="sxs-lookup"><span data-stu-id="87719-108">First, it renders track 0.</span></span> <span data-ttu-id="87719-109">В разделе "Track 0" нет ничего, поэтому пустые регионы подготавливаются к просмотру как сплошной черный рисунок.</span><span class="sxs-lookup"><span data-stu-id="87719-109">There is nothing "under" Track 0, so empty regions are rendered as a solid black image.</span></span> <span data-ttu-id="87719-110">Переходы в этом слое происходят между черным изображением и отслеживанием 0 или наоборот.</span><span class="sxs-lookup"><span data-stu-id="87719-110">Transitions in this layer occur between the black image and track 0 or vice versa.</span></span> <span data-ttu-id="87719-111">DES помещает 1 на начало дорожки 0, создавая все переходы между двумя дорожками.</span><span class="sxs-lookup"><span data-stu-id="87719-111">DES lays track 1 on top of track 0, generating any transitions between the two tracks.</span></span> <span data-ttu-id="87719-112">Результатом является совмещение двух дорожек.</span><span class="sxs-lookup"><span data-stu-id="87719-112">The result is the composite of the two tracks.</span></span> <span data-ttu-id="87719-113">Затем он помещает на этот составной части Track 2.</span><span class="sxs-lookup"><span data-stu-id="87719-113">Next, it places track 2 onto this composite.</span></span> <span data-ttu-id="87719-114">Переходы на этом уровне происходят между составным и отслеживающим 2.</span><span class="sxs-lookup"><span data-stu-id="87719-114">Transitions at this layer occur between the composite and track 2.</span></span> <span data-ttu-id="87719-115">Процесс продолжится до тех пор, пока не будет выводится последняя (самая приоритетная) запись.</span><span class="sxs-lookup"><span data-stu-id="87719-115">The process continues until the last (highest-priority) track is put down.</span></span>

<span data-ttu-id="87719-116">Если несколько дорожек объединены, они ведут себя как одна дорожка (называемая виртуальной дорожкой).</span><span class="sxs-lookup"><span data-stu-id="87719-116">When several tracks are composited together, they behave like a single track (called a virtual track).</span></span> <span data-ttu-id="87719-117">Объект композиции инкапсулирует это поведение, делая возможными сложные переходы.</span><span class="sxs-lookup"><span data-stu-id="87719-117">The composition object encapsulates this behavior, making complex transitions possible.</span></span> <span data-ttu-id="87719-118">Например, один видеоклип может стереть второй клип, а совмещенный (оба — и стирание) постепенно пересекаться с третьим.</span><span class="sxs-lookup"><span data-stu-id="87719-118">For example, one video clip can wipe to a second clip, while the composite (both clips plus the wipe) fades to a third clip.</span></span>

## <a name="related-topics"></a><span data-ttu-id="87719-119">См. также</span><span class="sxs-lookup"><span data-stu-id="87719-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="87719-120">начало работы с помощью служб редактирования DirectShow</span><span class="sxs-lookup"><span data-stu-id="87719-120">Getting Started with DirectShow Editing Services</span></span>](getting-started-with-directshow-editing-services.md)
</dt> </dl>

 

 



