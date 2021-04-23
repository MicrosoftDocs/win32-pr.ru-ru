---
description: Язык запросов WMI (WQL) — это подмножество Американский национальный институт стандартов (ANSI) язык SQL (ANSI SQL) &\# 8212; с незначительными семантическими изменениями. В следующей таблице перечислены ключевые слова WQL.
ms.assetid: 72a7ec04-9af3-41ae-9189-6e1d46803fa9
ms.tgt_platform: multiple
title: WQL (SQL WMI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87498b6e8e37ab900e21eedf2c15d5cdba9f9bd7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263917"
---
# <a name="wql-sql-for-wmi"></a><span data-ttu-id="e3a5e-104">WQL (SQL WMI)</span><span class="sxs-lookup"><span data-stu-id="e3a5e-104">WQL (SQL for WMI)</span></span>

<span data-ttu-id="e3a5e-105">Язык запросов WMI (WQL) — это подмножество Американский национальный институт стандартов (ANSI) язык SQL (ANSI SQL) с незначительными семантическими изменениями.</span><span class="sxs-lookup"><span data-stu-id="e3a5e-105">The WMI Query Language (WQL) is a subset of the American National Standards Institute Structured Query Language (ANSI SQL) with minor semantic changes.</span></span> <span data-ttu-id="e3a5e-106">В следующей таблице перечислены ключевые слова WQL.</span><span class="sxs-lookup"><span data-stu-id="e3a5e-106">The following table lists the WQL keywords.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e3a5e-107">Ключевое слово WQL</span><span class="sxs-lookup"><span data-stu-id="e3a5e-107">WQL keyword</span></span></th>
<th><span data-ttu-id="e3a5e-108">Значение</span><span class="sxs-lookup"><span data-stu-id="e3a5e-108">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e3a5e-109">AND</span><span class="sxs-lookup"><span data-stu-id="e3a5e-109">AND</span></span><br/></td>
<td><span data-ttu-id="e3a5e-110">Объединяет два логических выражения и возвращает <strong>значение true</strong> , если оба выражения имеют <strong>значение true</strong>.</span><span class="sxs-lookup"><span data-stu-id="e3a5e-110">Combines two Boolean expressions, and returns <strong>TRUE</strong> when both expressions are <strong>TRUE</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e3a5e-111"><a href="associators-of-statement.md">СОЕДИНИТЕЛи</a></span><span class="sxs-lookup"><span data-stu-id="e3a5e-111"><a href="associators-of-statement.md">ASSOCIATORS OF</a></span></span></td>
<td><span data-ttu-id="e3a5e-112">Извлекает все экземпляры, связанные с исходным экземпляром.</span><span class="sxs-lookup"><span data-stu-id="e3a5e-112">Retrieves all instances that are associated with a source instance.</span></span><br/> <span data-ttu-id="e3a5e-113">Используйте эту инструкцию с запросами схемы и запросами данных.</span><span class="sxs-lookup"><span data-stu-id="e3a5e-113">Use this statement with schema queries and data queries.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e3a5e-114"><a href="--class-identifier.md">__CLASS</a></span><span class="sxs-lookup"><span data-stu-id="e3a5e-114"><a href="--class-identifier.md">__CLASS</a></span></span></td>
<td><span data-ttu-id="e3a5e-115">Ссылается на класс объекта в запросе.</span><span class="sxs-lookup"><span data-stu-id="e3a5e-115">References the class of the object in a query.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e3a5e-116">FROM</span><span class="sxs-lookup"><span data-stu-id="e3a5e-116">FROM</span></span><br/></td>
<td><span data-ttu-id="e3a5e-117">Указывает класс, содержащий свойства, перечисленные в инструкции SELECT.</span><span class="sxs-lookup"><span data-stu-id="e3a5e-117">Specifies the class that contains the properties listed in a SELECT statement.</span></span> <span data-ttu-id="e3a5e-118">Инструментарий управления Windows (WMI) (WMI) поддерживает запросы данных только из одного класса за раз.</span><span class="sxs-lookup"><span data-stu-id="e3a5e-118">Windows Management Instrumentation (WMI) supports data queries from only one class at a time.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e3a5e-119"><a href="group-clause.md">Group, предложение</a></span><span class="sxs-lookup"><span data-stu-id="e3a5e-119"><a href="group-clause.md">GROUP Clause</a></span></span></td>
<td><span data-ttu-id="e3a5e-120">Заставляет Инструментарий WMI создать одно уведомление для представления группы событий.</span><span class="sxs-lookup"><span data-stu-id="e3a5e-120">Causes WMI to generate one notification to represent a group of events.</span></span><br/> <span data-ttu-id="e3a5e-121">Используйте это предложение с запросами событий.</span><span class="sxs-lookup"><span data-stu-id="e3a5e-121">Use this clause with event queries.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e3a5e-122"><a href="having-clause.md">HAVING</a></span><span class="sxs-lookup"><span data-stu-id="e3a5e-122"><a href="having-clause.md">HAVING</a></span></span></td>
<td><span data-ttu-id="e3a5e-123">Фильтрует события, полученные в течение интервала группировки, указанного в <a href="within-clause.md">предложении Within</a>.</span><span class="sxs-lookup"><span data-stu-id="e3a5e-123">Filters the events that are received during the grouping interval that is specified in the <a href="within-clause.md">WITHIN clause</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e3a5e-124"><a href="wql-operators.md">IS</a></span><span class="sxs-lookup"><span data-stu-id="e3a5e-124"><a href="wql-operators.md">IS</a></span></span></td>
<td><span data-ttu-id="e3a5e-125">Оператор сравнения, используемый с NOT и <strong>null</strong>.</span><span class="sxs-lookup"><span data-stu-id="e3a5e-125">Comparison operator used with NOT and <strong>NULL</strong>.</span></span> <span data-ttu-id="e3a5e-126">Для этой инструкции используется следующий синтаксис:</span><span class="sxs-lookup"><span data-stu-id="e3a5e-126">The syntax for this statement is the following:</span></span><br/> <span data-ttu-id="e3a5e-127">ИМЕЕТ значение [NOT] <strong>null</strong></span><span class="sxs-lookup"><span data-stu-id="e3a5e-127">IS [NOT] <strong>NULL</strong></span></span><br/> <span data-ttu-id="e3a5e-128">(где не является обязательным)</span><span class="sxs-lookup"><span data-stu-id="e3a5e-128">(where NOT is optional)</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e3a5e-129"><a href="wql-operators.md">ISA</a></span><span class="sxs-lookup"><span data-stu-id="e3a5e-129"><a href="wql-operators.md">ISA</a></span></span></td>
<td><span data-ttu-id="e3a5e-130">Оператор, который применяет запрос к подклассам указанного класса.</span><span class="sxs-lookup"><span data-stu-id="e3a5e-130">Operator that applies a query to the subclasses of a specified class.</span></span> <span data-ttu-id="e3a5e-131">Дополнительные сведения см. в статьях <a href="isa-operator-for-event-queries.md">оператор ISA для запросов событий</a>, <a href="isa-operator-for-data-queries.md">оператор ISA для запросов данных</a>и <a href="isa-operator-for-schema-queries.md">оператор ISA для запросов схемы</a>.</span><span class="sxs-lookup"><span data-stu-id="e3a5e-131">For more information, see <a href="isa-operator-for-event-queries.md">ISA Operator for Event Queries</a>, <a href="isa-operator-for-data-queries.md">ISA Operator for Data Queries</a>, and <a href="isa-operator-for-schema-queries.md">ISA Operator for Schema Queries</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e3a5e-132">кэйсонли</span><span class="sxs-lookup"><span data-stu-id="e3a5e-132">KEYSONLY</span></span><br/></td>
<td><span data-ttu-id="e3a5e-133">Используется в <a href="references-of-statement.md">ссылках</a> и <a href="associators-of-statement.md">связывающих</a> запросов, чтобы гарантировать, что результирующие экземпляры будут заполнены только ключами экземпляров, что снижает затраты на вызов.</span><span class="sxs-lookup"><span data-stu-id="e3a5e-133">Used in <a href="references-of-statement.md">REFERENCES OF</a> and <a href="associators-of-statement.md">ASSOCIATORS OF</a> queries to ensure that the resulting instances are only populated with the keys of the instances, which reduces the overhead of the call.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e3a5e-134"><a href="wql-operators.md">LIKE</a></span><span class="sxs-lookup"><span data-stu-id="e3a5e-134"><a href="wql-operators.md">LIKE</a></span></span></td>
<td><span data-ttu-id="e3a5e-135">Оператор, определяющий, совпадает ли данная символьная строка с указанным шаблоном.</span><span class="sxs-lookup"><span data-stu-id="e3a5e-135">Operator that determines whether or not a given character string matches a specified pattern.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e3a5e-136">NOT</span><span class="sxs-lookup"><span data-stu-id="e3a5e-136">NOT</span></span><br/></td>
<td><span data-ttu-id="e3a5e-137">Оператор сравнения, который используется в запросе WQL SELECT, например:</span><span class="sxs-lookup"><span data-stu-id="e3a5e-137">Comparison operator that use in a WQL SELECT query, for example:</span></span><br/>
<pre data-space="preserve"><code>SELECT * FROM meta_class WHERE NOT __class < &quot;Win32&quot; AND NOT __this ISA &quot;Win32_Account&quot;</code></pre></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e3a5e-138"><strong>NULL</strong></span><span class="sxs-lookup"><span data-stu-id="e3a5e-138"><strong>NULL</strong></span></span></td>
<td><span data-ttu-id="e3a5e-139">Указывает, что объект не имеет явно присвоенного значения.</span><span class="sxs-lookup"><span data-stu-id="e3a5e-139">Indicates an object does not have an explicitly assigned value.</span></span> <span data-ttu-id="e3a5e-140"><strong>Значение NULL</strong> не эквивалентно нулю (0) или пусто.</span><span class="sxs-lookup"><span data-stu-id="e3a5e-140"><strong>NULL</strong> is not equivalent to zero (0) or blank.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e3a5e-141">OR</span><span class="sxs-lookup"><span data-stu-id="e3a5e-141">OR</span></span><br/></td>
<td><span data-ttu-id="e3a5e-142">Объединяет два условия.</span><span class="sxs-lookup"><span data-stu-id="e3a5e-142">Combines two conditions.</span></span><br/> <span data-ttu-id="e3a5e-143">Если в инструкции используется более одного логического оператора, то операторы или вычисляются после операторов и.</span><span class="sxs-lookup"><span data-stu-id="e3a5e-143">When more than one logical operator is used in a statement, the OR operators are evaluated after the AND operators.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e3a5e-144"><a href="references-of-statement.md">ССЫЛКИ НА</a></span><span class="sxs-lookup"><span data-stu-id="e3a5e-144"><a href="references-of-statement.md">REFERENCES OF</a></span></span></td>
<td><span data-ttu-id="e3a5e-145">Извлекает все экземпляры связей, ссылающиеся на конкретный экземпляр источника.</span><span class="sxs-lookup"><span data-stu-id="e3a5e-145">Retrieves all association instances that refer to a specific source instance.</span></span> <span data-ttu-id="e3a5e-146">Используйте эту инструкцию с запросами схемы и данных.</span><span class="sxs-lookup"><span data-stu-id="e3a5e-146">Use this statement with schema and data queries.</span></span> <span data-ttu-id="e3a5e-147"><a href="references-of-statement.md">Ссылки</a> оператора похожи на операторы- <a href="associators-of-statement.md">соединители</a> оператора.</span><span class="sxs-lookup"><span data-stu-id="e3a5e-147">The <a href="references-of-statement.md">REFERENCES OF</a> statement is similar to the <a href="associators-of-statement.md">ASSOCIATORS OF</a> statement.</span></span> <span data-ttu-id="e3a5e-148">Однако они не извлекают экземпляры конечных точек; Он извлекает экземпляры ассоциации.</span><span class="sxs-lookup"><span data-stu-id="e3a5e-148">However, it does not retrieve endpoint instances; it retrieves the association instances.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e3a5e-149">SELECT</span><span class="sxs-lookup"><span data-stu-id="e3a5e-149">SELECT</span></span><br/></td>
<td><span data-ttu-id="e3a5e-150">Задает свойства, используемые в запросе.</span><span class="sxs-lookup"><span data-stu-id="e3a5e-150">Specifies the properties that are used in a query.</span></span><br/> <span data-ttu-id="e3a5e-151">Дополнительные сведения см. в статьях <a href="select-statement-for-data-queries.md">инструкция SELECT для запросов данных</a>, <a href="select-statement-for-event-queries.md">инструкция SELECT для запросов событий</a>или <a href="select-statement-for-schema-queries.md">инструкция SELECT для запросов схемы</a>.</span><span class="sxs-lookup"><span data-stu-id="e3a5e-151">For more information, see <a href="select-statement-for-data-queries.md">SELECT Statement for Data Queries</a>, <a href="select-statement-for-event-queries.md">SELECT Statement for Event Queries</a>, or <a href="select-statement-for-schema-queries.md">SELECT Statement for Schema Queries</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e3a5e-152"><strong>TRUE</strong></span><span class="sxs-lookup"><span data-stu-id="e3a5e-152"><strong>TRUE</strong></span></span></td>
<td><span data-ttu-id="e3a5e-153">Логический оператор, результатом вычисления которого является – 1 (минус единица).</span><span class="sxs-lookup"><span data-stu-id="e3a5e-153">Boolean operator that evaluates to -1 (minus one).</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e3a5e-154"><a href="where-clause.md">WHERE</a></span><span class="sxs-lookup"><span data-stu-id="e3a5e-154"><a href="where-clause.md">WHERE</a></span></span></td>
<td><span data-ttu-id="e3a5e-155">Ограничивает область запроса данных, события или схемы.</span><span class="sxs-lookup"><span data-stu-id="e3a5e-155">Narrows the scope of a data, event, or schema query.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e3a5e-156"><a href="within-clause.md">WITHIN</a></span><span class="sxs-lookup"><span data-stu-id="e3a5e-156"><a href="within-clause.md">WITHIN</a></span></span></td>
<td><span data-ttu-id="e3a5e-157">Задает интервал опроса или группирования.</span><span class="sxs-lookup"><span data-stu-id="e3a5e-157">Specifies a polling or grouping interval.</span></span><br/> <span data-ttu-id="e3a5e-158">Используйте это предложение с запросами событий.</span><span class="sxs-lookup"><span data-stu-id="e3a5e-158">Use this clause with event queries.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e3a5e-159">FALSE</span><span class="sxs-lookup"><span data-stu-id="e3a5e-159">FALSE</span></span><br/></td>
<td><span data-ttu-id="e3a5e-160">Логический оператор, значением которого является 0 (ноль).</span><span class="sxs-lookup"><span data-stu-id="e3a5e-160">Boolean operator that evaluates to 0 (zero).</span></span></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> <span data-ttu-id="e3a5e-161">Использование ключевого слова WQL в качестве имени объекта может привести к созданию запроса, который не может быть проанализирован даже в случае, если запрос компилируется без ошибок.</span><span class="sxs-lookup"><span data-stu-id="e3a5e-161">Using a WQL key word as an object name can result in a query that cannot be parsed even when the query compiles without error.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="e3a5e-162">См. также</span><span class="sxs-lookup"><span data-stu-id="e3a5e-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e3a5e-163">Операторы WQL</span><span class="sxs-lookup"><span data-stu-id="e3a5e-163">WQL Operators</span></span>](wql-operators.md)
</dt> <dt>

[<span data-ttu-id="e3a5e-164">Форматы даты, поддерживаемые WQL</span><span class="sxs-lookup"><span data-stu-id="e3a5e-164">WQL-Supported Date Formats</span></span>](wql-supported-date-formats.md)
</dt> <dt>

[<span data-ttu-id="e3a5e-165">Поддерживаемые форматы времени WQL</span><span class="sxs-lookup"><span data-stu-id="e3a5e-165">WQL-Supported Time Formats</span></span>](wql-supported-time-formats.md)
</dt> </dl>

 

 




