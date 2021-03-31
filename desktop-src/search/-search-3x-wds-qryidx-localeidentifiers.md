---
description: Идентификаторы инпутлокале и кэйвордлокале помогают поисковой подсистеме использовать правильные средства разбиения по словам, определяя язык запросов, вводимых пользователем, и язык ключевых слов расширенных синтаксисов запросов.
ms.assetid: dc610f49-5106-47f9-b29b-84949dd2c42b
title: Аргументы идентификатора локали (Поиск Windows)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cea1549a550e4bf6b8099241a6f3d2275860a983
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896949"
---
# <a name="locale-identifier-arguments-windows-search"></a><span data-ttu-id="de586-103">Аргументы идентификатора локали (Поиск Windows)</span><span class="sxs-lookup"><span data-stu-id="de586-103">Locale Identifier Arguments (Windows Search)</span></span>

<span data-ttu-id="de586-104">`inputlocale` `keywordlocale` Идентификаторы и помогают поисковой подсистеме использовать правильные средства разбиения по словам, определяя язык запросов, вводимых пользователем, и язык ключевых слов расширенного синтаксиса запросов.</span><span class="sxs-lookup"><span data-stu-id="de586-104">The `inputlocale` and `keywordlocale` identifiers help the search engine use the correct word breakers by identifying the language of user-entered queries and the language the of Advanced Query Syntax keywords.</span></span> <span data-ttu-id="de586-105">Это не всегда одинаковые идентификаторы кода языка (LCID), так как поиск Windows предлагается в нескольких международных версиях, а также включает пакеты MUI для других языков.</span><span class="sxs-lookup"><span data-stu-id="de586-105">These are not always the same language code identifiers (LCIDs) because Windows Search is offered in a number of international versions and also includes MUI packs for more languages.</span></span> <span data-ttu-id="de586-106">Инпутлокале определяет код языка, на котором пользователи выполняют поисковый запрос в, а кэйвордлокале определяет код языка, используемый поисковой системой для ключевых слов.</span><span class="sxs-lookup"><span data-stu-id="de586-106">The inputlocale identifies the LCID for the language users input their search query in, while the keywordlocale identifies the LCID the search engine uses for keywords.</span></span>

<span data-ttu-id="de586-107">Этот раздел организован следующим образом:</span><span class="sxs-lookup"><span data-stu-id="de586-107">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="de586-108">Пример</span><span class="sxs-lookup"><span data-stu-id="de586-108">Example</span></span>](#example)
-   [<span data-ttu-id="de586-109">См. также</span><span class="sxs-lookup"><span data-stu-id="de586-109">Related topics</span></span>](#related-topics)

## <a name="example"></a><span data-ttu-id="de586-110">Пример</span><span class="sxs-lookup"><span data-stu-id="de586-110">Example</span></span>


```
 search-ms:query=matthew&inputlocale=2072&keywordlocale=1033
```



## <a name="related-topics"></a><span data-ttu-id="de586-111">См. также</span><span class="sxs-lookup"><span data-stu-id="de586-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="de586-112">Начало работы с Parameter-Valueными аргументами</span><span class="sxs-lookup"><span data-stu-id="de586-112">Getting Started with Parameter-Value Arguments</span></span>](getting-started-with-parameter-value-arguments.md)
</dt> <dt>

[<span data-ttu-id="de586-113">Переданный аргумент</span><span class="sxs-lookup"><span data-stu-id="de586-113">CRUMB Argument</span></span>](-search-3x-wds-qryidx-crumb.md)
</dt> <dt>

[<span data-ttu-id="de586-114">Аргумент СИНТАКСИСа</span><span class="sxs-lookup"><span data-stu-id="de586-114">SYNTAX Argument</span></span>](-search-3x-wds-qryidx-syntaxargument.md)
</dt> <dt>

[<span data-ttu-id="de586-115">СТАККЕДБИ, аргумент</span><span class="sxs-lookup"><span data-stu-id="de586-115">STACKEDBY Argument</span></span>](-search-3x-wds-qryidx-stackedby.md)
</dt> <dt>

[<span data-ttu-id="de586-116">Аргумент вложенного запроса</span><span class="sxs-lookup"><span data-stu-id="de586-116">SUBQUERY Argument</span></span>](-search-3x-wds-qryidx-subquery.md)
</dt> </dl>

 

 



