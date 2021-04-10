---
description: Дополнительные сведения о предложении ORDER BY
ms.assetid: e720cf0d-b034-48e2-a13e-e97dd23b2beb
title: Предложение ORDER BY
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3eaa3c834ca2fe04222ef2ae452a0119bf391b9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104144080"
---
# <a name="order-by-clause"></a><span data-ttu-id="26bd9-103">Предложение ORDER BY</span><span class="sxs-lookup"><span data-stu-id="26bd9-103">ORDER BY Clause</span></span>

<span data-ttu-id="26bd9-104">Предложение ORDER BY сортирует результаты на основе значения одного или нескольких указанных столбцов.</span><span class="sxs-lookup"><span data-stu-id="26bd9-104">The ORDER BY clause sorts the results based on the value of one or more columns you specify.</span></span> <span data-ttu-id="26bd9-105">Ниже приведен синтаксис предложения ORDER BY:</span><span class="sxs-lookup"><span data-stu-id="26bd9-105">Following is the syntax of the ORDER BY clause:</span></span>


```
ORDER BY <column> [<direction>] [,<column> [<direction>]]
```



<span data-ttu-id="26bd9-106">Спецификатор столбца должен быть допустимым столбцом.</span><span class="sxs-lookup"><span data-stu-id="26bd9-106">The column specifier must be a valid column.</span></span> <span data-ttu-id="26bd9-107">Можно использовать описатель столбца для ссылки на столбцы по порядку их появления в запросе.</span><span class="sxs-lookup"><span data-stu-id="26bd9-107">You can use the column specifier to refer to columns by the order that they appear in the query.</span></span> <span data-ttu-id="26bd9-108">Первый столбец в запросе пронумерован 1.</span><span class="sxs-lookup"><span data-stu-id="26bd9-108">The first column in the query is numbered 1.</span></span> <span data-ttu-id="26bd9-109">В предложении ORDER BY можно включить несколько столбцов, разделенных запятыми.</span><span class="sxs-lookup"><span data-stu-id="26bd9-109">You can include more than one column in the ORDER BY clause, separated by commas.</span></span>

<span data-ttu-id="26bd9-110">Необязательный спецификатор направления может быть либо "ASC" для возрастания (от низкого до высокого), либо "DESC" для нисходящего (от максимального к меньшему).</span><span class="sxs-lookup"><span data-stu-id="26bd9-110">The optional direction specifier can be either "ASC" for ascending (low to high) or "DESC" for descending (high to low).</span></span> <span data-ttu-id="26bd9-111">Если не указать описатель направления, используется значение по умолчанию (по возрастанию).</span><span class="sxs-lookup"><span data-stu-id="26bd9-111">If you do not provide a direction specifier, the default, ascending, is used.</span></span> <span data-ttu-id="26bd9-112">Если указать более одного столбца, но не указывать все направления, то направление, заданное последним, применяется к каждому столбцу до тех пор, пока не будет явно изменено направление.</span><span class="sxs-lookup"><span data-stu-id="26bd9-112">If you specify more than one column, but do not specify all directions, the direction you specify last is applied to each column until you explicitly change the direction.</span></span>

<span data-ttu-id="26bd9-113">Например, в следующем предложении ORDER BY столбцы A, B, C и G сортируются в возрастающем порядке, а столбцы D, E и F сортируются в порядке убывания.</span><span class="sxs-lookup"><span data-stu-id="26bd9-113">For example, in the following ORDER BY clause, the columns A, B, C, and G are sorted in ascending order, while columns D, E, and F are sorted in descending order.</span></span>


```
ORDER BY A ASC, B, C, D DESC, E, F, G ASC
```



## <a name="related-topics"></a><span data-ttu-id="26bd9-114">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="26bd9-114">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="26bd9-115">**Reference**</span><span class="sxs-lookup"><span data-stu-id="26bd9-115">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="26bd9-116">Предложение FROM</span><span class="sxs-lookup"><span data-stu-id="26bd9-116">FROM Clause</span></span>](-search-sql-from.md)
</dt> <dt>

[<span data-ttu-id="26bd9-117">РАНЖИРОВАНие по предложению</span><span class="sxs-lookup"><span data-stu-id="26bd9-117">RANK BY Clause</span></span>](-search-sql-rankby.md)
</dt> <dt>

[<span data-ttu-id="26bd9-118">Инструкция SELECT</span><span class="sxs-lookup"><span data-stu-id="26bd9-118">SELECT Statement</span></span>](-search-sql-select.md)
</dt> <dt>

<span data-ttu-id="26bd9-119">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="26bd9-119">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="26bd9-120">Полнотекстовые предикаты</span><span class="sxs-lookup"><span data-stu-id="26bd9-120">Full-Text Predicates</span></span>](-search-sql-fulltextpredicates.md)
</dt> <dt>

[<span data-ttu-id="26bd9-121">Неполнотекстовые предикаты</span><span class="sxs-lookup"><span data-stu-id="26bd9-121">Non-Full-Text Predicates</span></span>](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



