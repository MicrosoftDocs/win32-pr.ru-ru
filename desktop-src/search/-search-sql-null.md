---
description: Предикат NULL указывает, имеет ли документ значение для указанного столбца.
ms.assetid: 078ffd99-2020-4da2-8968-301dba8cc436
title: Предикат NULL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea02a04313ac2b86afe809633bee5ad2cbcf764e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701386"
---
# <a name="null-predicate"></a><span data-ttu-id="7798a-103">Предикат NULL</span><span class="sxs-lookup"><span data-stu-id="7798a-103">NULL Predicate</span></span>

<span data-ttu-id="7798a-104">Предикат **null** указывает, имеет ли документ значение для указанного столбца.</span><span class="sxs-lookup"><span data-stu-id="7798a-104">The **NULL** predicate indicates whether the document has a value for the indicated column.</span></span>

<span data-ttu-id="7798a-105">Предикат **null** имеет следующий синтаксис:</span><span class="sxs-lookup"><span data-stu-id="7798a-105">The **NULL** predicate has the following syntax:</span></span>


```
...WHERE <column> IS [NOT] NULL
```



<span data-ttu-id="7798a-106">Необязательное ключевое слово NOT инвертирует результат.</span><span class="sxs-lookup"><span data-stu-id="7798a-106">The optional NOT keyword negates the result.</span></span> <span data-ttu-id="7798a-107">Столбец может быть обычным или [идентификатором](-search-sql-identifiers.md)с разделителями.</span><span class="sxs-lookup"><span data-stu-id="7798a-107">The column can be a regular or delimited [identifier](-search-sql-identifiers.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7798a-108">Чтобы проверить, имеет ли столбец значение **null** , необходимо использовать предикат **null** .</span><span class="sxs-lookup"><span data-stu-id="7798a-108">To test whether a column has the **NULL** value, you must use the **NULL** predicate.</span></span> <span data-ttu-id="7798a-109">Недопустимо использовать значение **null** в предикате сравнения.</span><span class="sxs-lookup"><span data-stu-id="7798a-109">It is not valid to use the **NULL** value in a comparison predicate.</span></span> <span data-ttu-id="7798a-110">"Где column имеет **значение NULL**" является правильным.</span><span class="sxs-lookup"><span data-stu-id="7798a-110">"WHERE column IS **NULL**" is correct.</span></span> <span data-ttu-id="7798a-111">Недопустимое значение "WHERE Column = **null**".</span><span class="sxs-lookup"><span data-stu-id="7798a-111">"WHERE column = **NULL**" is not valid.</span></span>

 

## <a name="example"></a><span data-ttu-id="7798a-112">Пример</span><span class="sxs-lookup"><span data-stu-id="7798a-112">Example</span></span>

<span data-ttu-id="7798a-113">В следующем примере возвращаются документы, не имеющие значения System. Video. режиссер.</span><span class="sxs-lookup"><span data-stu-id="7798a-113">The following example returns documents that do not have a System.Video.Director value.</span></span>


```
...WHERE System.Video.Director IS NULL
```



## <a name="related-topics"></a><span data-ttu-id="7798a-114">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="7798a-114">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="7798a-115">**Reference**</span><span class="sxs-lookup"><span data-stu-id="7798a-115">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="7798a-116">Предикат LIKE</span><span class="sxs-lookup"><span data-stu-id="7798a-116">LIKE Predicate</span></span>](-search-sql-like.md)
</dt> <dt>

[<span data-ttu-id="7798a-117">Сравнение литеральных значений</span><span class="sxs-lookup"><span data-stu-id="7798a-117">Literal Value Comparison</span></span>](-search-sql-literalvaluecomparison.md)
</dt> <dt>

[<span data-ttu-id="7798a-118">Сравнения с несколькими значениями (МАССИВы)</span><span class="sxs-lookup"><span data-stu-id="7798a-118">Multi-Valued (ARRAY) Comparisons</span></span>](-search-sql-multivaluedcomparisons.md)
</dt> <dt>

<span data-ttu-id="7798a-119">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="7798a-119">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="7798a-120">Полнотекстовые предикаты</span><span class="sxs-lookup"><span data-stu-id="7798a-120">Full-Text Predicates</span></span>](-search-sql-fulltextpredicates.md)
</dt> <dt>

[<span data-ttu-id="7798a-121">Неполнотекстовые предикаты</span><span class="sxs-lookup"><span data-stu-id="7798a-121">Non-Full-Text Predicates</span></span>](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



