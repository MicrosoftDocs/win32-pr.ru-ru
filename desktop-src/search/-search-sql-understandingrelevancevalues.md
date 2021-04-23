---
description: В реляционной базе данных строки, возвращаемые поисковым запросом, должны соответствовать всем условиям, вызванным запросом. В отличие от этого, запрос Windows Search может возвращать документы, соответствующие условиям поиска, в разные градусы.
ms.assetid: 9f37b494-9b7a-45a6-9ee4-6d582742cbd7
title: Общие сведения о значимых значениях
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a24c71ad523ad869c6ff05b81ff75367031ad38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896918"
---
# <a name="understanding-relevance-values"></a><span data-ttu-id="2de81-104">Общие сведения о значимых значениях</span><span class="sxs-lookup"><span data-stu-id="2de81-104">Understanding Relevance Values</span></span>

<span data-ttu-id="2de81-105">В реляционной базе данных строки, возвращаемые поисковым запросом, должны соответствовать всем условиям, вызванным запросом.</span><span class="sxs-lookup"><span data-stu-id="2de81-105">In a relational database, rows that are returned by a search query must meet all the conditions called for by the query.</span></span> <span data-ttu-id="2de81-106">В отличие от этого, запрос Windows Search может возвращать документы, соответствующие условиям поиска, в разные градусы.</span><span class="sxs-lookup"><span data-stu-id="2de81-106">In contrast, a Windows Search query can return documents that meet the search conditions to varying degrees.</span></span>

<span data-ttu-id="2de81-107">Например, при поиске термина «Program» в реляционной базе данных создаются записи, содержащие это конкретное написание слова.</span><span class="sxs-lookup"><span data-stu-id="2de81-107">For example, a search for the term "program" in a relational database produces records that contain that specific spelling of the word.</span></span> <span data-ttu-id="2de81-108">Значение, указывающее, содержит ли запись один или 100 экземпляров слова, не влияет на результаты.</span><span class="sxs-lookup"><span data-stu-id="2de81-108">Whether a record contains one or one hundred instances of the word has no impact on the results.</span></span> <span data-ttu-id="2de81-109">В отличие от этого, Поиск Windows возвращает значение релевантности, связанное с соответствующими документами.</span><span class="sxs-lookup"><span data-stu-id="2de81-109">In contrast, Windows Search returns a relevance value associated with the matching documents.</span></span> <span data-ttu-id="2de81-110">Релевантность документов, содержащих слово «Program» в заголовке, выше, чем в последнем абзаце.</span><span class="sxs-lookup"><span data-stu-id="2de81-110">The relevance of documents having "program" in the title is higher than those that contain the word only in the last paragraph.</span></span> <span data-ttu-id="2de81-111">Аналогичным образом, документы, содержащие вариации условия поиска, например "программы" и "программирование", также совпадают и возвращаются запросом.</span><span class="sxs-lookup"><span data-stu-id="2de81-111">Similarly, documents containing variations of the search term, for example "programs" and "programming" also match and are returned by the query.</span></span>

<span data-ttu-id="2de81-112">Запросы поиска Windows возвращают целочисленные значения релевантности в столбце с именем «Rank».</span><span class="sxs-lookup"><span data-stu-id="2de81-112">Windows Search queries return integer relevance values in the column named "rank".</span></span>

<span data-ttu-id="2de81-113">Кроме того:</span><span class="sxs-lookup"><span data-stu-id="2de81-113">In addition:</span></span>

-   <span data-ttu-id="2de81-114">Значения ранга, возвращаемые запросом, являются целыми числами в диапазоне от 0 до 1000.</span><span class="sxs-lookup"><span data-stu-id="2de81-114">Rank values returned by the query are integers ranging from 0 to 1000.</span></span>
-   <span data-ttu-id="2de81-115">Более высокие значения ранга указывают на документы, которые лучше соответствуют условиям поиска.</span><span class="sxs-lookup"><span data-stu-id="2de81-115">Higher rank values indicate documents that better match the search conditions.</span></span>
-   <span data-ttu-id="2de81-116">Значения ранжирования применяются только к текущему запросу, поэтому их нельзя сравнивать с результатами по запросам.</span><span class="sxs-lookup"><span data-stu-id="2de81-116">Rank values apply only to the current query, so they cannot be compared for results across queries.</span></span>
-   <span data-ttu-id="2de81-117">Значения ранжирования зависят от других документов, соответствующих запросу.</span><span class="sxs-lookup"><span data-stu-id="2de81-117">Rank values are relative to the other documents matching the query.</span></span> <span data-ttu-id="2de81-118">Таким образом, значение ранжирования конкретного документа зависит от других документов, которые также соответствуют запросу.</span><span class="sxs-lookup"><span data-stu-id="2de81-118">Therefore, the rank value of a particular document depends on the other documents that also match the query.</span></span>
-   <span data-ttu-id="2de81-119">Ранжирующие значения для элементов, соответствующих чисто реляционному предикату, — 1000.</span><span class="sxs-lookup"><span data-stu-id="2de81-119">Rank values for items matching a purely relational predicate are 1000.</span></span>

<span data-ttu-id="2de81-120">Вы можете манипулировать возвращаемыми значениями ранжирования, используя весовые коэффициенты столбцов в предикатах [Contains](-search-sql-contains.md) и [FREETEXT](-search-sql-freetext.md) WHERE, а также предложение Rank by.</span><span class="sxs-lookup"><span data-stu-id="2de81-120">You can manipulate the returned rank values by using column weights in the [CONTAINS](-search-sql-contains.md) and [FREETEXT](-search-sql-freetext.md) WHERE clause predicates, and the RANK BY clause.</span></span>

 

 



