---
title: Начальные, срединного и окончательные строки поиска
description: Существует три типа поиска с подстановочными знаками, упоминаемых в документации по созданию запросов к строкам поиска. Эти поисковые запросы являются строками Initial-, срединного-и Final-Search. В этом разделе описываются эти операции поиска.
ms.assetid: 23cc4771-2dd6-478c-9c7a-43052594cb71
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76f502753a87afc81856524c7ae5565db3af678d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105654171"
---
# <a name="initial-medial-and-final-search-strings"></a><span data-ttu-id="4c4ae-105">Начальные, срединного и окончательные строки поиска</span><span class="sxs-lookup"><span data-stu-id="4c4ae-105">Initial, Medial, and Final Search Strings</span></span>

<span data-ttu-id="4c4ae-106">Существует три типа поиска с подстановочными знаками, упоминаемых в документации по созданию запросов к строкам поиска.</span><span class="sxs-lookup"><span data-stu-id="4c4ae-106">There are three types of wildcard searches that are referenced throughout the documentation about construction search string queries.</span></span> <span data-ttu-id="4c4ae-107">Это поиск с подстановочными знаками: Initial-, срединного-и Final-Поиск строк.</span><span class="sxs-lookup"><span data-stu-id="4c4ae-107">These wildcard searches are: initial-, medial-, and final-search strings.</span></span> <span data-ttu-id="4c4ae-108">В этом разделе описываются эти операции поиска.</span><span class="sxs-lookup"><span data-stu-id="4c4ae-108">This topics describes these searches.</span></span>

## <a name="initial-search-strings"></a><span data-ttu-id="4c4ae-109">Начальные строки поиска</span><span class="sxs-lookup"><span data-stu-id="4c4ae-109">Initial Search Strings</span></span>

<span data-ttu-id="4c4ae-110">Начальные строки поиска соответствуют заданному набору символов в начале строки, за которым следует подстановочный знак.</span><span class="sxs-lookup"><span data-stu-id="4c4ae-110">Initial-search strings match a given set of characters at the beginning of a string, followed by a wildcard.</span></span> <span data-ttu-id="4c4ae-111">Например, строка начального поиска `Act*` будет соответствовать "Active Directory".</span><span class="sxs-lookup"><span data-stu-id="4c4ae-111">For example, the initial-search string `Act*` would match "Active Directory".</span></span>

## <a name="medial-search-strings"></a><span data-ttu-id="4c4ae-112">Строки Medial-Search</span><span class="sxs-lookup"><span data-stu-id="4c4ae-112">Medial-Search Strings</span></span>

<span data-ttu-id="4c4ae-113">Срединного — строки поиска соответствуют заданному набору символов в середине строки с префиксом и/или с последующим символом-шаблоном.</span><span class="sxs-lookup"><span data-stu-id="4c4ae-113">Medial-search strings match a given set of characters in the middle of a string, preceded by and/or followed by a wildcard.</span></span> <span data-ttu-id="4c4ae-114">Строки срединного-Search `*Dir*` , `*ive*Dir*` и `*ve*Dir*tor*` будут соответствовать "Active Directory".</span><span class="sxs-lookup"><span data-stu-id="4c4ae-114">The medial-search strings `*Dir*`, `*ive*Dir*`, and `*ve*Dir*tor*` would all match "Active Directory".</span></span>

## <a name="final-search-strings"></a><span data-ttu-id="4c4ae-115">Итоговые строки поиска</span><span class="sxs-lookup"><span data-stu-id="4c4ae-115">Final-search Strings</span></span>

<span data-ttu-id="4c4ae-116">Конечные строки поиска соответствуют заданному набору символов в конце строки, перед которыми ставится символ-шаблон.</span><span class="sxs-lookup"><span data-stu-id="4c4ae-116">Final-search strings match a given set of characters at the end of a string, preceded by a wildcard.</span></span> <span data-ttu-id="4c4ae-117">Например, строка окончательного поиска `*ory` будет соответствовать "Active Directory".</span><span class="sxs-lookup"><span data-stu-id="4c4ae-117">For example, the final-search string `*ory` would match "Active Directory".</span></span>

 

 




