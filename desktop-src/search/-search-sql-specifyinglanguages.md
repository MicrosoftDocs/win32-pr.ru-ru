---
description: Можно указать язык, используемый в поисковых запросах.
ms.assetid: 3a7ecf8f-38ae-41d1-be70-e9ab23977a01
title: Указание языков
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e50b3f65a41670989d41e235831ec8c008a6d8cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540663"
---
# <a name="specifying-languages"></a><span data-ttu-id="fb122-103">Указание языков</span><span class="sxs-lookup"><span data-stu-id="fb122-103">Specifying Languages</span></span>

<span data-ttu-id="fb122-104">Можно указать язык, используемый в поисковых запросах.</span><span class="sxs-lookup"><span data-stu-id="fb122-104">You can specify the language used in search queries.</span></span> <span data-ttu-id="fb122-105">Предикаты FREETEXT и CONTAINS в предложении WHERE поддерживают указание языка.</span><span class="sxs-lookup"><span data-stu-id="fb122-105">Both the FREETEXT and CONTAINS predicates in the WHERE clause support specifying a language.</span></span> <span data-ttu-id="fb122-106">Язык запроса можно указать, предоставив числовой идентификатор кода языка (LCID) в предикате CONTAINS или FREETEXT.</span><span class="sxs-lookup"><span data-stu-id="fb122-106">You can indicate the query language by providing a numeric language code identifier (LCID) in the CONTAINS or FREETEXT predicate.</span></span> <span data-ttu-id="fb122-107">Этот код языка определяет, какой средство разбиения по словам следует использовать для синтаксического анализа строки запроса.</span><span class="sxs-lookup"><span data-stu-id="fb122-107">This LCID specifies which word breaker to use to parse the query string.</span></span> <span data-ttu-id="fb122-108">Для этого используется следующий синтаксис:</span><span class="sxs-lookup"><span data-stu-id="fb122-108">It uses the following syntax:</span></span>


```
CONTAINS | FREETEXT
([<column_identifier>,]'<content_search_condition>' [,LCID]) 
```



<span data-ttu-id="fb122-109">Дополнительные сведения см. в описании синтаксиса предикатов [Contains](-search-sql-contains.md) и [FREETEXT](-search-sql-freetext.md) .</span><span class="sxs-lookup"><span data-stu-id="fb122-109">For more information, see the syntax for the [CONTAINS](-search-sql-contains.md) and [FREETEXT](-search-sql-freetext.md) predicates.</span></span>

 

 



