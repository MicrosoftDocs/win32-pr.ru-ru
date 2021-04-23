---
description: Идентификаторы инпутлокале и кэйвордлокале помогают поисковой подсистеме использовать правильные средства разбиения по словам, определяя язык запросов, вводимых пользователем, и язык ключевых слов расширенных синтаксисов запросов.
title: Аргументы идентификатора локали (оболочка Windows)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 881ce3a6-6cf6-45be-9a1e-148b9053d7c4
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 403e0338b61a4dedba37a620000e3fd82c91f383
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272325"
---
# <a name="locale-identifier-arguments-the-windows-shell"></a><span data-ttu-id="28b63-103">Аргументы идентификатора локали (оболочка Windows)</span><span class="sxs-lookup"><span data-stu-id="28b63-103">Locale Identifier Arguments (The Windows Shell)</span></span>

<span data-ttu-id="28b63-104">`inputlocale` `keywordlocale` Идентификаторы и помогают поисковой подсистеме использовать правильные средства разбиения по словам, определяя язык запросов, вводимых пользователем, и язык ключевых слов расширенного синтаксиса запросов.</span><span class="sxs-lookup"><span data-stu-id="28b63-104">The `inputlocale` and `keywordlocale` identifiers help the search engine use the correct word breakers by identifying the language of user-entered queries and the language the of Advanced Query Syntax keywords.</span></span> <span data-ttu-id="28b63-105">Они не всегда являются одинаковыми идентификаторами кода языка (LCID), поскольку поиск Windows предлагается в нескольких международных версиях, а также включает пакеты многоязыкового интерфейса пользователя (MUI) для других языков.</span><span class="sxs-lookup"><span data-stu-id="28b63-105">These are not always the same language code identifiers (LCIDs) because Windows Search is offered in a number of international versions and also includes Multilingual User Interface (MUI) packs for more languages.</span></span> <span data-ttu-id="28b63-106">`inputlocale`Определяет код языка, на котором пользователи выполняют поисковый запрос в, а `keywordlocale` определяет код языка, используемый поисковой системой для ключевых слов.</span><span class="sxs-lookup"><span data-stu-id="28b63-106">The `inputlocale` identifies the LCID for the language users input their search query in, while the `keywordlocale` identifies the LCID the search engine uses for keywords.</span></span>

## <a name="example"></a><span data-ttu-id="28b63-107">Например, .</span><span class="sxs-lookup"><span data-stu-id="28b63-107">Example</span></span>


```
search:query=matthew&inputlocale=2072&keywordlocale=1033
```



### <a name="argument-information"></a><span data-ttu-id="28b63-108">Сведения о аргументе</span><span class="sxs-lookup"><span data-stu-id="28b63-108">Argument Information</span></span>



|                          |                                         |
|--------------------------|-----------------------------------------|
| <span data-ttu-id="28b63-109">Минимальная операционная система</span><span class="sxs-lookup"><span data-stu-id="28b63-109">Minimum Operating System</span></span> | <span data-ttu-id="28b63-110">Windows Vista с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="28b63-110">Windows Vista with Service Pack 1 (SP1)</span></span> |



 

 

 



