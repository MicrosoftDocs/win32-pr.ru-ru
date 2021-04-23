---
description: Функция DATEADD выполняет вычисления времени и даты для соответствующих свойств с типами дат. Функция DATEADD используется для получения даты и времени в течение указанного промежутка времени до текущего.
ms.assetid: 83ef098d-85ef-4883-a1e1-9229e050247f
title: Функция DATEADD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c0b193e75ec644eb3312a61c723edeac43ee264
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104144101"
---
# <a name="dateadd-function"></a><span data-ttu-id="347dc-104">Функция DATEADD</span><span class="sxs-lookup"><span data-stu-id="347dc-104">DATEADD Function</span></span>

<span data-ttu-id="347dc-105">Функция DATEADD выполняет вычисления времени и даты для соответствующих свойств с типами дат.</span><span class="sxs-lookup"><span data-stu-id="347dc-105">The DATEADD function performs time and date calculations for matching properties having date types.</span></span> <span data-ttu-id="347dc-106">Функция DATEADD используется для получения даты и времени в течение указанного промежутка времени до текущего.</span><span class="sxs-lookup"><span data-stu-id="347dc-106">Use the DATEADD function to obtain dates and times in a specified amount of time before the present.</span></span>

## <a name="syntax"></a><span data-ttu-id="347dc-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="347dc-107">Syntax</span></span>


```
DATEADD (DateTimeUnits, OffsetValue, DateTime)
```



## <a name="arguments"></a><span data-ttu-id="347dc-108">Аргументы</span><span class="sxs-lookup"><span data-stu-id="347dc-108">Arguments</span></span>

<span data-ttu-id="347dc-109">*датетимеунитс*</span><span class="sxs-lookup"><span data-stu-id="347dc-109">*DateTimeUnits*</span></span>

<span data-ttu-id="347dc-110">Указывает единицы параметра *даты и времени* : год, квартал, месяц, неделя, день, час, минута или секунда.</span><span class="sxs-lookup"><span data-stu-id="347dc-110">Specifies the units of the *DateTime* parameter: YEAR, QUARTER, MONTH, WEEK, DAY, HOUR, MINUTE, or SECOND.</span></span> <span data-ttu-id="347dc-111">Это значение чувствительно к регистру, и кавычки не требуются вокруг параметра.</span><span class="sxs-lookup"><span data-stu-id="347dc-111">This value is case-sensitive, and quotation marks are not required around the parameter.</span></span>

<span data-ttu-id="347dc-112">*оффсетвалуе*</span><span class="sxs-lookup"><span data-stu-id="347dc-112">*OffsetValue*</span></span>

<span data-ttu-id="347dc-113">Задает смещение времени в единицах, указанных параметром *датетимеунитс* .</span><span class="sxs-lookup"><span data-stu-id="347dc-113">Specifies the time offset, in the units specified by the *DateTimeUnits* parameter.</span></span> <span data-ttu-id="347dc-114">**Оффсетвалуе** должно быть отрицательным целым числом.</span><span class="sxs-lookup"><span data-stu-id="347dc-114">**OffsetValue** must be a negative integer.</span></span> <span data-ttu-id="347dc-115">Положительные значения не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="347dc-115">Positive values are not supported.</span></span>

<span data-ttu-id="347dc-116">*DateTime*</span><span class="sxs-lookup"><span data-stu-id="347dc-116">*DateTime*</span></span>

<span data-ttu-id="347dc-117">Задает отметку времени, из которой вычисляется смещение.</span><span class="sxs-lookup"><span data-stu-id="347dc-117">Specifies a time stamp from which to calculate the offset.</span></span> <span data-ttu-id="347dc-118">Это не может быть литералом даты.</span><span class="sxs-lookup"><span data-stu-id="347dc-118">This cannot be a date literal.</span></span> <span data-ttu-id="347dc-119">Он должен быть либо ЖЕТГМТДАТЕ, либо результатом другой функции DATEADD.</span><span class="sxs-lookup"><span data-stu-id="347dc-119">It must be either GETGMTDATE or the result of another DATEADD function.</span></span>

## <a name="remarks"></a><span data-ttu-id="347dc-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="347dc-120">Remarks</span></span>

<span data-ttu-id="347dc-121">Функцию DATEADD можно использовать только в сравнениях литеральных значений и только с правой стороны оператора сравнения.</span><span class="sxs-lookup"><span data-stu-id="347dc-121">The DATEADD function can be used only in literal value comparisons and only on the right side of the comparison operator.</span></span>

<span data-ttu-id="347dc-122">Функция ЖЕТГМТДАТЕ возвращает текущую дату и время по Гринвичу (GMT).</span><span class="sxs-lookup"><span data-stu-id="347dc-122">The GETGMTDATE function returns the current date and time in Greenwich Mean Time (GMT).</span></span> <span data-ttu-id="347dc-123">Помните, что это значение не может совпадать с местным временем компьютера.</span><span class="sxs-lookup"><span data-stu-id="347dc-123">Remember that this value may not be the same as the local time of your computer.</span></span>

<span data-ttu-id="347dc-124">Не используйте оператор сравнения Equals (=), так как внутреннее представление времени может создавать ошибки округления, которые приводят к непредвиденным результатам сопоставления.</span><span class="sxs-lookup"><span data-stu-id="347dc-124">Do not use the equals (=) comparison operator because the internal time representation can produce rounding errors that result in unexpected matching results.</span></span>

<span data-ttu-id="347dc-125">Можно использовать несколько функций DATEADD для объединения единиц смещения.</span><span class="sxs-lookup"><span data-stu-id="347dc-125">You can use multiple DATEADD functions to combine offset units.</span></span>

### <a name="examples"></a><span data-ttu-id="347dc-126">Примеры</span><span class="sxs-lookup"><span data-stu-id="347dc-126">Examples</span></span>

<span data-ttu-id="347dc-127">В следующем примере предложение WHERE соответствует документам, которые были изменены в течение последних пяти дней:</span><span class="sxs-lookup"><span data-stu-id="347dc-127">The following example WHERE clause matches documents that were modified within the last five days:</span></span>


```
...WHERE System.DateModified <=DATEADD (DAY, -5, GETGMTDATE())
```



<span data-ttu-id="347dc-128">В следующем примере предложение WHERE соответствует документам, которые были изменены в течение последних двух дней и четырех часов:</span><span class="sxs-lookup"><span data-stu-id="347dc-128">The following example WHERE clause matches documents that were modified within the last two days and four hours:</span></span>


```
...WHERE System.DateModified <=DATEADD (DAY, -2, DATEADD (HOUR, -4, GETGMTDATE()))
```



## <a name="related-topics"></a><span data-ttu-id="347dc-129">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="347dc-129">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="347dc-130">**Reference**</span><span class="sxs-lookup"><span data-stu-id="347dc-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="347dc-131">Сравнение литеральных значений</span><span class="sxs-lookup"><span data-stu-id="347dc-131">Literal Value Comparison</span></span>](-search-sql-literalvaluecomparison.md)
</dt> <dt>

[<span data-ttu-id="347dc-132">Сравнения с несколькими значениями (МАССИВы)</span><span class="sxs-lookup"><span data-stu-id="347dc-132">Multi-Valued (ARRAY) Comparisons</span></span>](-search-sql-multivaluedcomparisons.md)
</dt> <dt>

<span data-ttu-id="347dc-133">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="347dc-133">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="347dc-134">Полнотекстовые предикаты</span><span class="sxs-lookup"><span data-stu-id="347dc-134">Full-Text Predicates</span></span>](-search-sql-fulltextpredicates.md)
</dt> <dt>

[<span data-ttu-id="347dc-135">Неполнотекстовые предикаты</span><span class="sxs-lookup"><span data-stu-id="347dc-135">Non-Full-Text Predicates</span></span>](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



