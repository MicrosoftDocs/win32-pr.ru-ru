---
description: Ниже показан базовый синтаксис инструкции SELECT для локального запроса.
ms.assetid: 334aa2b9-0ef2-4a4b-9352-de5ded95afa6
title: Инструкция SELECT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e05832dab0184870a626fa4bce502d908c9b05f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701381"
---
# <a name="select-statement"></a><span data-ttu-id="7fc50-103">Инструкция SELECT</span><span class="sxs-lookup"><span data-stu-id="7fc50-103">SELECT Statement</span></span>

<span data-ttu-id="7fc50-104">Ниже показан базовый синтаксис инструкции SELECT для локального запроса.</span><span class="sxs-lookup"><span data-stu-id="7fc50-104">The following shows the basic syntax of the SELECT statement for a local query:</span></span>


```
SELECT [TOP <positive integer>] <columns>
FROM [machinename.]SystemIndex
[WHERE <conditions>]
[ORDER BY <column>] 
            
```



<span data-ttu-id="7fc50-105">Ниже показана часть столбца синтаксиса инструкции SELECT:</span><span class="sxs-lookup"><span data-stu-id="7fc50-105">The following shows the column portion of the SELECT statement syntax:</span></span>


```
SELECT [TOP <positive integer>] <column> [ {, <column>} ...]
```



<span data-ttu-id="7fc50-106">Описатели столбцов должны быть допустимыми столбцами имени свойства, разделенными запятыми.</span><span class="sxs-lookup"><span data-stu-id="7fc50-106">The column specifier(s) must be valid property name columns, separated by commas.</span></span> <span data-ttu-id="7fc50-107">Допустимые имена столбцов являются зарегистрированными описаниями свойств или определяются схемой системы свойств оболочки.</span><span class="sxs-lookup"><span data-stu-id="7fc50-107">Valid column names are registered property descriptions or are defined by the Shell's Property System Schema.</span></span> <span data-ttu-id="7fc50-108">Можно выбрать только те столбцы, которые помечены как доступные для получения в схеме системы свойств.</span><span class="sxs-lookup"><span data-stu-id="7fc50-108">You can select only those columns that are marked as retrievable in the Property System Schema.</span></span> <span data-ttu-id="7fc50-109">Если для определения свойств, которые не являются системно-определенными свойствами, используется смешанный регистр, необходимо заключить спецификатор столбца в двойные кавычки.</span><span class="sxs-lookup"><span data-stu-id="7fc50-109">If you use mixed case to identify properties that are not system-defined properties, you must enclose the column specifier in double quotation marks.</span></span> <span data-ttu-id="7fc50-110">Системные имена свойств включают все свойства, начинающиеся с "System" (например, System. Contact. FirstName) и не требующие кавычек.</span><span class="sxs-lookup"><span data-stu-id="7fc50-110">System-defined property names include all properties beginning with "System" (for example, System.Contact.FirstName) and do not require quotation marks.</span></span>

> [!Note]  
> <span data-ttu-id="7fc50-111">Для удобочитаемости можно также заключить имена системных свойств в двойные кавычки.</span><span class="sxs-lookup"><span data-stu-id="7fc50-111">You can also enclose system-defined property names in double quotation marks for readability.</span></span> <span data-ttu-id="7fc50-112">Это не влияет на совместимость.</span><span class="sxs-lookup"><span data-stu-id="7fc50-112">This does not affect compatibility.</span></span>

 

<span data-ttu-id="7fc50-113">Если запрос возвращает документ, в котором нет запрошенного столбца, значение этого столбца для документа равно **null**.</span><span class="sxs-lookup"><span data-stu-id="7fc50-113">When the query returns a document that does not have the requested column, the value of that column for the document is **NULL**.</span></span>

<span data-ttu-id="7fc50-114">В инструкции SELECT необходимо указать хотя бы одно имя столбца.</span><span class="sxs-lookup"><span data-stu-id="7fc50-114">You must provide at least one column name in a SELECT statement.</span></span> <span data-ttu-id="7fc50-115">В запросе язык SQL (SQL) вы можете использовать звездочку ( \* ), чтобы указать, что должны возвращаться все столбцы в таблице.</span><span class="sxs-lookup"><span data-stu-id="7fc50-115">In the Structured Query Language (SQL) query, you are allowed to use the asterisk (\*) to specify that all columns in a table are to be returned.</span></span> <span data-ttu-id="7fc50-116">Однако определенный и фиксированный набор свойств не применяется ко всем документам.</span><span class="sxs-lookup"><span data-stu-id="7fc50-116">However, no defined and fixed set of properties applies to all documents.</span></span> <span data-ttu-id="7fc50-117">По этой причине в спецификаторе инструкции SELECT не допускается использование звездочки SQL <columns> .</span><span class="sxs-lookup"><span data-stu-id="7fc50-117">For this reason, the SQL asterisk is not permitted in the <columns> specifier of the SELECT statement.</span></span>

## <a name="getting-the-top-n-results"></a><span data-ttu-id="7fc50-118">Получение первых n результатов</span><span class="sxs-lookup"><span data-stu-id="7fc50-118">Getting the Top n Results</span></span>

<span data-ttu-id="7fc50-119">Можно указать максимальное число возвращаемых результатов с помощью верхнего синтаксиса:</span><span class="sxs-lookup"><span data-stu-id="7fc50-119">You can specify a maximum number of results to return by using the TOP syntax:</span></span>


```
SELECT TOP <positive integer> <column> [ {, <column>} ...]
```



## <a name="casting-column-data-types"></a><span data-ttu-id="7fc50-120">Типы данных столбцов приведения</span><span class="sxs-lookup"><span data-stu-id="7fc50-120">Casting Column Data Types</span></span>

<span data-ttu-id="7fc50-121">Иногда может потребоваться привести строковые данные, извлеченные из документов, в качестве другого типа данных, чтобы можно было выполнить соответствующее сравнение.</span><span class="sxs-lookup"><span data-stu-id="7fc50-121">At times, you might need to cast string data extracted from documents as another data type so that an appropriate comparison can be made.</span></span> <span data-ttu-id="7fc50-122">Дополнительные сведения см. в разделе [приведение типа данных столбца](-search-sql-castingdatacolumntype.md).</span><span class="sxs-lookup"><span data-stu-id="7fc50-122">For more information, refer to [Casting the Data Type of a Column](-search-sql-castingdatacolumntype.md).</span></span>

## <a name="examples"></a><span data-ttu-id="7fc50-123">Примеры</span><span class="sxs-lookup"><span data-stu-id="7fc50-123">Examples</span></span>

<span data-ttu-id="7fc50-124">В следующих примерах возвращается имя и URL-адрес соответствующих документов.</span><span class="sxs-lookup"><span data-stu-id="7fc50-124">The following examples return the name and URL of matching documents.</span></span>


```
SELECT System.ItemName, System.ItemUrl FROM SystemIndex WHERE CONTAINS('Microsoft')

SELECT TOP 10 System.ItemName, System.ItemUrl FROM SystemIndex WHERE CONTAINS('Microsoft') 
```



## <a name="related-topics"></a><span data-ttu-id="7fc50-125">См. также</span><span class="sxs-lookup"><span data-stu-id="7fc50-125">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="7fc50-126">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="7fc50-126">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="7fc50-127">Приведение типа данных столбца</span><span class="sxs-lookup"><span data-stu-id="7fc50-127">Casting the Data Type of a Column</span></span>](-search-sql-castingdatacolumntype.md)
</dt> <dt>

<span data-ttu-id="7fc50-128">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="7fc50-128">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="7fc50-129">[Свойства системы](https://msdn.microsoft.com/library/bb763010(VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="7fc50-129">[System Properties](https://msdn.microsoft.com/library/bb763010(VS.85).aspx)</span></span>
</dt> </dl>

 

 



