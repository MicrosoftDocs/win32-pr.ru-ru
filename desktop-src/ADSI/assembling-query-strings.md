---
title: Сборка строк запросов
description: В Active Directory использование определенных критериев фильтрации может повысить производительность поиска. Это происходит потому, что Active Directory оценивает все предикаты, определяет индексы, а затем выбирает один индекс, который, скорее всего, приведет к наименьшему набору возвращаемых значений.
ms.assetid: 4139eedb-1383-4654-9b40-5e294a71be24
ms.tgt_platform: multiple
keywords:
- Сборка строк запросов ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e56dec34f63a4a3e12385a36ad5fe5339a0f3d9c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105654149"
---
# <a name="assembling-query-strings"></a><span data-ttu-id="b80a2-105">Сборка строк запросов</span><span class="sxs-lookup"><span data-stu-id="b80a2-105">Assembling Query Strings</span></span>

<span data-ttu-id="b80a2-106">В Active Directory использование определенных критериев фильтрации может повысить производительность поиска.</span><span class="sxs-lookup"><span data-stu-id="b80a2-106">In Active Directory, using specific filtering criteria can boost search performance.</span></span> <span data-ttu-id="b80a2-107">Это происходит потому, что Active Directory оценивает все предикаты, определяет индексы, а затем выбирает один индекс, который, скорее всего, приведет к наименьшему набору возвращаемых значений.</span><span class="sxs-lookup"><span data-stu-id="b80a2-107">This is because Active Directory evaluates all predicates, identifies the indices, and then selects one index likely to yield the smallest set of returned values.</span></span>

<span data-ttu-id="b80a2-108">Старайтесь не искать текст в середине или конце строки, например "CN = \* Хилле \* " или "CN = \* лараусе".</span><span class="sxs-lookup"><span data-stu-id="b80a2-108">Avoid searching for text in the middle or the end of a string, for example, "cn=\*hille\*" or "cn=\*larouse".</span></span>

<span data-ttu-id="b80a2-109">По возможности выполните поиск индексированных атрибутов.</span><span class="sxs-lookup"><span data-stu-id="b80a2-109">When possible, search for indexed attributes.</span></span> <span data-ttu-id="b80a2-110">Индексированные атрибуты хранятся на всех контроллерах домена, поэтому запрос, скорее всего, будет выполняться быстрее, чем поиск неиндексированного атрибута.</span><span class="sxs-lookup"><span data-stu-id="b80a2-110">Indexed attributes are stored on all domain controllers, so the query will most likely be faster than searching for a non-indexed attribute.</span></span>

 

 




