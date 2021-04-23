---
description: По умолчанию механизм поиска Windows и каталог не зависят от диакритических знаков, которые являются знаками ударения, добавленными к буквам для изменения значения или произношения слова.
ms.assetid: 71007bd4-5232-469c-982b-ff0d24bd0c1f
title: Чувствительность диакритических знаков в поиске
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46fb68676418fc109fa24ed2d55fb9602b7ad41d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105710915"
---
# <a name="diacritic-sensitivity-in-searches"></a><span data-ttu-id="3fd2d-103">Чувствительность диакритических знаков в поиске</span><span class="sxs-lookup"><span data-stu-id="3fd2d-103">Diacritic Sensitivity in Searches</span></span>

<span data-ttu-id="3fd2d-104">По умолчанию механизм поиска Windows и каталог не зависят от диакритических знаков, которые являются знаками ударения, добавленными к буквам для изменения значения или произношения слова.</span><span class="sxs-lookup"><span data-stu-id="3fd2d-104">By default, the Windows Search engine and catalog are insensitive to diacritics, which are accent marks added to letters to alter a word's meaning or pronunciation.</span></span> <span data-ttu-id="3fd2d-105">Однако поиск Windows позволяет изменить это значение для каталога с помощью [диспетчера каталогов](-search-3x-wds-mngidx-catalog-manager.md) , чтобы задать чувствительность диакритических знаков.</span><span class="sxs-lookup"><span data-stu-id="3fd2d-105">However, Windows Search enables you to change this for your catalog using the [Catalog Manager](-search-3x-wds-mngidx-catalog-manager.md) to set diacritic sensitivity.</span></span> <span data-ttu-id="3fd2d-106">Например, если параметр чувствительность диакритических знаков имеет значение **false**, каталог будет считаться «Resume» и «ресумé», как если бы они были одним словом.</span><span class="sxs-lookup"><span data-stu-id="3fd2d-106">For example, with diacritic sensitivity set to **FALSE**, the catalog would treat "resume" and "resumé" as if they were the same word.</span></span>

<span data-ttu-id="3fd2d-107">На уровне запроса термины запроса с диакритическими знаками в FREETEXT и предложениями CONTAINS передаются в подсистему и затем нормализованы (так же, как и во время индексирования) для сопоставления.</span><span class="sxs-lookup"><span data-stu-id="3fd2d-107">At the query layer, query terms with diacritics in FREETEXT and CONTAINS clauses are passed through to the engine and are then normalized (as they would be at index time) for matching.</span></span> <span data-ttu-id="3fd2d-108">Сопоставление с каталогом всегда учитывает диакритические знаки.</span><span class="sxs-lookup"><span data-stu-id="3fd2d-108">Matching against the catalog is always diacritic sensitive.</span></span>

> [!Note]  
> <span data-ttu-id="3fd2d-109">Это не так для диапазонов символов 0x2e81-f8ff и 0x1100-0x11ff.</span><span class="sxs-lookup"><span data-stu-id="3fd2d-109">This is not the case for the character ranges 0x2e81-f8ff and 0x1100-0x11ff.</span></span>

 

 

 



