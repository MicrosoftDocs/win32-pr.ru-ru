---
description: Псевдонимы групп столбцов предоставляют способ использования более коротких имен вместо имени столбца или группы столбцов. Необязательный предикат псевдонима группы является частью предложения WHERE.
ms.assetid: 7782ac24-ea6c-4a97-b1b6-982f276fcefc
title: С параметром--AS предикат псевдонима группы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29218e11fbffe5f47128eeefba3a7fe847a5b21d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808926"
---
# <a name="with----as-group-alias-predicate"></a><span data-ttu-id="8e562-104">С параметром--AS предикат псевдонима группы</span><span class="sxs-lookup"><span data-stu-id="8e562-104">WITH -- AS Group Alias Predicate</span></span>

<span data-ttu-id="8e562-105">Псевдонимы групп столбцов предоставляют способ использования более коротких имен вместо имени столбца или группы столбцов.</span><span class="sxs-lookup"><span data-stu-id="8e562-105">Column group aliases provide a way to use shorter names in place of the name of a column or a group of columns.</span></span> <span data-ttu-id="8e562-106">Необязательный предикат псевдонима группы является частью предложения WHERE.</span><span class="sxs-lookup"><span data-stu-id="8e562-106">The optional group alias predicate is part of the WHERE clause.</span></span> <span data-ttu-id="8e562-107">Его синтаксис выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="8e562-107">Its syntax follows:</span></span>


```
...WHERE[ WITH(<columns>) AS #<alias_name>]
[,WITH(<columns>) AS #<alias_name>]
```



<span data-ttu-id="8e562-108">Можно указать более одного псевдонима группы, разделяя на... Предикаты AS запятыми.</span><span class="sxs-lookup"><span data-stu-id="8e562-108">You can specify more than one group alias, separating the WITH...AS predicates by commas.</span></span>

<span data-ttu-id="8e562-109">При ссылке на псевдоним группы в предикате предложения WHERE условие применяется к каждому столбцу в группе.</span><span class="sxs-lookup"><span data-stu-id="8e562-109">When a group alias is referred to in a WHERE clause predicate, the condition is applied to each column in the group.</span></span> <span data-ttu-id="8e562-110">Логические значения, полученные в результате сопоставления каждого столбца, объединяются с помощью логического оператора **или** .</span><span class="sxs-lookup"><span data-stu-id="8e562-110">The logical values resulting from matching each column are combined by using the logical **OR** operator.</span></span>

<span data-ttu-id="8e562-111">Псевдоним должен быть определен до того, как его можно будет использовать, и его можно использовать только в предложении WHERE.</span><span class="sxs-lookup"><span data-stu-id="8e562-111">An alias must be defined before it can be used, and it can be used only within the WHERE clause.</span></span> <span data-ttu-id="8e562-112">Имя псевдонима должно быть обычным идентификатором, которому предшествует обязательный знак решетки ( \# ).</span><span class="sxs-lookup"><span data-stu-id="8e562-112">The alias name must be a regular identifier preceded by a required pound sign (\#).</span></span>

<span data-ttu-id="8e562-113">Описатель столбца может содержать один или несколько описателей столбцов, разделенных запятыми.</span><span class="sxs-lookup"><span data-stu-id="8e562-113">The column specifier can contain one or more column specifiers, separated by commas.</span></span> <span data-ttu-id="8e562-114">Список столбцов должен быть заключен в круглые скобки, и для каждого из них можно назначить весовые значения.</span><span class="sxs-lookup"><span data-stu-id="8e562-114">The list of columns must be enclosed in parentheses and weighting can be assigned to each.</span></span> <span data-ttu-id="8e562-115">Каждый столбец имеет следующий синтаксис:</span><span class="sxs-lookup"><span data-stu-id="8e562-115">Each column has the following syntax:</span></span>


```
<column_identifier> [<weight_assignment>]
```



<span data-ttu-id="8e562-116">Сведения об указании веса столбцов см. в разделе [предикат FREETEXT](-search-sql-freetext.md) и [предикат CONTAINS](-search-sql-contains.md).</span><span class="sxs-lookup"><span data-stu-id="8e562-116">For information on specifying column weights, see [FREETEXT Predicate](-search-sql-freetext.md) and [CONTAINS Predicate](-search-sql-contains.md).</span></span>

<span data-ttu-id="8e562-117">Идентификатор столбца может быть обычным или разделителем.</span><span class="sxs-lookup"><span data-stu-id="8e562-117">The column identifier can be regular or delimited.</span></span>

## <a name="examples"></a><span data-ttu-id="8e562-118">Примеры</span><span class="sxs-lookup"><span data-stu-id="8e562-118">Examples</span></span>

<span data-ttu-id="8e562-119">В следующих примерах предложения WHERE демонстрируется, когда и как можно использовать предикат псевдонима группы.</span><span class="sxs-lookup"><span data-stu-id="8e562-119">The following WHERE clause examples demonstrate when and how you can use the group alias predicate.</span></span> <span data-ttu-id="8e562-120">В первом примере показано более повторяющееся предложение WHERE, которое не использует Псевдонимы групп.</span><span class="sxs-lookup"><span data-stu-id="8e562-120">The first example shows a more repetitive WHERE clause that does not use group aliasing.</span></span>


```
...WHERE
    FREETEXT("System.ItemNameDisplay",'"computer software"')
    OR
    FREETEXT("System.Title",'"computer software"')
    OR 
    FREETEXT("System.Keywords",'"computer software"')
```



<span data-ttu-id="8e562-121">Предыдущий пример можно упростить с помощью псевдонима группы, как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="8e562-121">The preceding example can be simplified by using a group alias, as shown in the following example.</span></span>


```
...WHERE
    WITH("System.ItemNameDisplay","System.Title","System.Keywords")
    AS #Doc-Descriptions
    FREETEXT(#Doc-Descriptions,'"computer software"')
```



<span data-ttu-id="8e562-122">Ниже приведен пример положительного веса, в котором свойству **Title** присваивается больший вес при определении относительного ранга.</span><span class="sxs-lookup"><span data-stu-id="8e562-122">The following is an example of positive weighting where the **Title** property is given more weight in determining the relative rank.</span></span>


```
...WHERE
    WITH("System.Title":0.8,*:0.5,
         "System.Keywords")
    AS #Doc-Descriptions
    FREETEXT(#Doc-Descriptions,'"computer software"')
```



<span data-ttu-id="8e562-123">Ниже приведен пример отрицательного веса, при котором свойство **Title** с весом 0 не учитывается.</span><span class="sxs-lookup"><span data-stu-id="8e562-123">The following is an example of negative weighting where the **Title** property with weight of 0 is not considered.</span></span>


```
...WHERE
    WITH("System.Title":0,*:1.0,
         "System.Keywords")
    AS #Doc-Descriptions
    FREETEXT(#Doc-Descriptions,'"computer software"')
```



## <a name="related-topics"></a><span data-ttu-id="8e562-124">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="8e562-124">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="8e562-125">**Reference**</span><span class="sxs-lookup"><span data-stu-id="8e562-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="8e562-126">Предикат FREETEXT</span><span class="sxs-lookup"><span data-stu-id="8e562-126">FREETEXT Predicate</span></span>](-search-sql-freetext.md)
</dt> <dt>

<span data-ttu-id="8e562-127">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="8e562-127">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="8e562-128">Полнотекстовые предикаты</span><span class="sxs-lookup"><span data-stu-id="8e562-128">Full-Text Predicates</span></span>](-search-sql-fulltextpredicates.md)
</dt> <dt>

[<span data-ttu-id="8e562-129">Неполнотекстовые предикаты</span><span class="sxs-lookup"><span data-stu-id="8e562-129">Non-Full-Text Predicates</span></span>](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



