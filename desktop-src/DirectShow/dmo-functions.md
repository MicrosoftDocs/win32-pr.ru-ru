---
description: Функции DMO
ms.assetid: 0a380dc0-23f0-4ef0-898a-3b5afddf5eaa
title: Функции DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70f41750f5e442d93d3cacb2499bf2986a53cda6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104494256"
---
# <a name="dmo-functions"></a><span data-ttu-id="c1b35-103">Функции DMO</span><span class="sxs-lookup"><span data-stu-id="c1b35-103">DMO Functions</span></span>

<span data-ttu-id="c1b35-104">В этом разделе описываются функции объектов мультимедиа Microsoft DirectX (DMO).</span><span class="sxs-lookup"><span data-stu-id="c1b35-104">This section describes the Microsoft DirectX Media Object (DMO) functions.</span></span>



| <span data-ttu-id="c1b35-105">Функция</span><span class="sxs-lookup"><span data-stu-id="c1b35-105">Function</span></span>                                             | <span data-ttu-id="c1b35-106">Описание</span><span class="sxs-lookup"><span data-stu-id="c1b35-106">Description</span></span>                                                   |
|------------------------------------------------------|---------------------------------------------------------------|
| [<span data-ttu-id="c1b35-107">**дмоенум**</span><span class="sxs-lookup"><span data-stu-id="c1b35-107">**DMOEnum**</span></span>](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoenum)                           | <span data-ttu-id="c1b35-108">Перечисляет дмос, перечисленные в реестре.</span><span class="sxs-lookup"><span data-stu-id="c1b35-108">Enumerates DMOs listed in the registry.</span></span>                       |
| [<span data-ttu-id="c1b35-109">**дможетнаме**</span><span class="sxs-lookup"><span data-stu-id="c1b35-109">**DMOGetName**</span></span>](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmogetname)                     | <span data-ttu-id="c1b35-110">Извлекает имя объекта DMO из реестра.</span><span class="sxs-lookup"><span data-stu-id="c1b35-110">Retrieves the name of a DMO from the registry.</span></span>                |
| [<span data-ttu-id="c1b35-111">**дможеттипес**</span><span class="sxs-lookup"><span data-stu-id="c1b35-111">**DMOGetTypes**</span></span>](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmogettypes)                   | <span data-ttu-id="c1b35-112">Извлекает типы носителей, зарегистрированные для DMO.</span><span class="sxs-lookup"><span data-stu-id="c1b35-112">Retrieves the media types registered for a DMO.</span></span>               |
| [<span data-ttu-id="c1b35-113">**дморегистер**</span><span class="sxs-lookup"><span data-stu-id="c1b35-113">**DMORegister**</span></span>](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoregister)                   | <span data-ttu-id="c1b35-114">Регистрирует DMO.</span><span class="sxs-lookup"><span data-stu-id="c1b35-114">Registers a DMO.</span></span>                                              |
| [<span data-ttu-id="c1b35-115">**дмаунрегистер**</span><span class="sxs-lookup"><span data-stu-id="c1b35-115">**DMOUnregister**</span></span>](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmounregister)               | <span data-ttu-id="c1b35-116">Отменяет регистрацию DMO.</span><span class="sxs-lookup"><span data-stu-id="c1b35-116">Unregisters a DMO.</span></span>                                            |
| [<span data-ttu-id="c1b35-117">**мокопимедиатипе**</span><span class="sxs-lookup"><span data-stu-id="c1b35-117">**MoCopyMediaType**</span></span>](/previous-versions/windows/desktop/api/Dmort/nf-dmort-mocopymediatype)           | <span data-ttu-id="c1b35-118">Копирует одну структуру типа мультимедиа в другую.</span><span class="sxs-lookup"><span data-stu-id="c1b35-118">Copies one media type structure to another.</span></span>                   |
| [<span data-ttu-id="c1b35-119">**мокреатемедиатипе**</span><span class="sxs-lookup"><span data-stu-id="c1b35-119">**MoCreateMediaType**</span></span>](/previous-versions/windows/desktop/api/Dmort/nf-dmort-mocreatemediatype)       | <span data-ttu-id="c1b35-120">Выделяет новую структуру типа мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="c1b35-120">Allocates a new media type structure.</span></span>                         |
| [<span data-ttu-id="c1b35-121">**моделетемедиатипе**</span><span class="sxs-lookup"><span data-stu-id="c1b35-121">**MoDeleteMediaType**</span></span>](/previous-versions/windows/desktop/api/Dmort/nf-dmort-modeletemediatype)       | <span data-ttu-id="c1b35-122">Удаляет ранее выделенную структуру типа мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="c1b35-122">Deletes a media type structure that was previously allocated.</span></span> |
| [<span data-ttu-id="c1b35-123">**модупликатемедиатипе**</span><span class="sxs-lookup"><span data-stu-id="c1b35-123">**MoDuplicateMediaType**</span></span>](/previous-versions/windows/desktop/api/Dmort/nf-dmort-moduplicatemediatype) | <span data-ttu-id="c1b35-124">Дублирует структуру типа мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="c1b35-124">Duplicates a media type structure.</span></span>                            |
| [<span data-ttu-id="c1b35-125">**мофримедиатипе**</span><span class="sxs-lookup"><span data-stu-id="c1b35-125">**MoFreeMediaType**</span></span>](/previous-versions/windows/desktop/api/Dmort/nf-dmort-mofreemediatype)           | <span data-ttu-id="c1b35-126">Освобождает выделенные элементы структуры типа мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="c1b35-126">Frees the allocated members of a media type structure.</span></span>        |
| [<span data-ttu-id="c1b35-127">**моинитмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="c1b35-127">**MoInitMediaType**</span></span>](/previous-versions/windows/desktop/api/Dmort/nf-dmort-moinitmediatype)           | <span data-ttu-id="c1b35-128">Инициализирует структуру типа мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="c1b35-128">Initializes a media type structure.</span></span>                           |



 

## <a name="related-topics"></a><span data-ttu-id="c1b35-129">См. также</span><span class="sxs-lookup"><span data-stu-id="c1b35-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c1b35-130">Справочник по DMO</span><span class="sxs-lookup"><span data-stu-id="c1b35-130">DMO Reference</span></span>](dmo-reference.md)
</dt> </dl>

 

 



