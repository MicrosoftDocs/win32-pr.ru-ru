---
title: Создание фильтра запросов
description: Фильтр запросов дает домен Active Directory службам искать данные в синтаксисе запросов LDAP. Все указанные технологии доступа к данным, перечисленные в разделе Выбор технологии поиска, поддерживают синтаксис запросов LDAP.
ms.assetid: 0bd652f0-41a6-4a0d-8742-9d6a2a7f168a
ms.tgt_platform: multiple
keywords:
- Active Directory примеры Active Directory, создание фильтра запросов
- фильтры запросов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc2e0a4e4a02312fcc9affb681407044ba0d8e18
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103887439"
---
# <a name="creating-a-query-filter"></a><span data-ttu-id="32286-106">Создание фильтра запросов</span><span class="sxs-lookup"><span data-stu-id="32286-106">Creating a Query Filter</span></span>

<span data-ttu-id="32286-107">Фильтр запросов дает домен Active Directory службам искать данные в синтаксисе запросов LDAP.</span><span class="sxs-lookup"><span data-stu-id="32286-107">A query filter instructs Active Directory Domain Services to find data in an LDAP query syntax.</span></span> <span data-ttu-id="32286-108">Все указанные технологии доступа к данным, перечисленные в разделе [Выбор технологии поиска,](choosing-the-search-technology.md) поддерживают синтаксис запросов LDAP.</span><span class="sxs-lookup"><span data-stu-id="32286-108">All the specified data access technologies listed in the [Choosing the Search Technology](choosing-the-search-technology.md) topic support LDAP query syntax.</span></span>

<span data-ttu-id="32286-109">Синтаксис запроса LDAP выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="32286-109">The LDAP query syntax is as follows:</span></span>


```C++
<expression><expression>...
```



<span data-ttu-id="32286-110">Фильтр может содержать одно или несколько выражений.</span><span class="sxs-lookup"><span data-stu-id="32286-110">A filter can contain one, or more, expressions.</span></span> <span data-ttu-id="32286-111">Выражение имеет следующий вид:</span><span class="sxs-lookup"><span data-stu-id="32286-111">An expression has the following form:</span></span>


```C++
(<logicaloperator><comparison><comparison...>)
```



<span data-ttu-id="32286-112">где " &lt; оператор logicaloperator &gt; " является одним из следующих.</span><span class="sxs-lookup"><span data-stu-id="32286-112">where "&lt;logicaloperator&gt;" is one of the following.</span></span>



| <span data-ttu-id="32286-113">Оператор</span><span class="sxs-lookup"><span data-stu-id="32286-113">Operator</span></span>        | <span data-ttu-id="32286-114">Описание</span><span class="sxs-lookup"><span data-stu-id="32286-114">Description</span></span>                |
|-----------------|----------------------------|
| <span data-ttu-id="32286-115">"\|"</span><span class="sxs-lookup"><span data-stu-id="32286-115">"\|"</span></span><br/> | <span data-ttu-id="32286-116">Логическое **или**</span><span class="sxs-lookup"><span data-stu-id="32286-116">Logical **OR**</span></span><br/>  |
| <span data-ttu-id="32286-117">"&"</span><span class="sxs-lookup"><span data-stu-id="32286-117">"&"</span></span><br/>  | <span data-ttu-id="32286-118">Логическое **и**</span><span class="sxs-lookup"><span data-stu-id="32286-118">Logical **AND**</span></span><br/> |
| <span data-ttu-id="32286-119">"!"</span><span class="sxs-lookup"><span data-stu-id="32286-119">"!"</span></span><br/>  | <span data-ttu-id="32286-120">Логическое **не**</span><span class="sxs-lookup"><span data-stu-id="32286-120">Logical **NOT**</span></span><br/> |



 

<span data-ttu-id="32286-121">и " &lt; Сравнение &gt; " является следующим:</span><span class="sxs-lookup"><span data-stu-id="32286-121">and "&lt;comparison&gt;" is the following:</span></span>


```C++
(<attribute><operator><value>)
```



<span data-ttu-id="32286-122">где " &lt; атрибут &gt; " — это атрибут **lDAPDisplayName** проверяемого атрибута, " &lt; value &gt; " — это сравниваемое значение, а " &lt; operator &gt; " — один из следующих операторов сравнения.</span><span class="sxs-lookup"><span data-stu-id="32286-122">where "&lt;attribute&gt;" is the **lDAPDisplayName** of the attribute to evaluate, "&lt;value&gt;" is the value to compare against, and "&lt;operator&gt;" is one of the following comparison operators.</span></span>



| <span data-ttu-id="32286-123">Оператор</span><span class="sxs-lookup"><span data-stu-id="32286-123">Operator</span></span>           | <span data-ttu-id="32286-124">Описание</span><span class="sxs-lookup"><span data-stu-id="32286-124">Description</span></span>                         |
|--------------------|-------------------------------------|
| <span data-ttu-id="32286-125">"="</span><span class="sxs-lookup"><span data-stu-id="32286-125">"="</span></span><br/>     | <span data-ttu-id="32286-126">Равно</span><span class="sxs-lookup"><span data-stu-id="32286-126">Equals</span></span><br/>                   |
| <span data-ttu-id="32286-127">"~="</span><span class="sxs-lookup"><span data-stu-id="32286-127">"~="</span></span><br/>    | <span data-ttu-id="32286-128">Приблизительно равно</span><span class="sxs-lookup"><span data-stu-id="32286-128">Approximately equals</span></span><br/>     |
| <span data-ttu-id="32286-129">"<="</span><span class="sxs-lookup"><span data-stu-id="32286-129">"<="</span></span><br/> | <span data-ttu-id="32286-130">Меньше или равно</span><span class="sxs-lookup"><span data-stu-id="32286-130">Less than or equal to</span></span><br/>    |
| <span data-ttu-id="32286-131">">="</span><span class="sxs-lookup"><span data-stu-id="32286-131">">="</span></span><br/> | <span data-ttu-id="32286-132">Больше или равно</span><span class="sxs-lookup"><span data-stu-id="32286-132">Greater than or equal to</span></span><br/> |



 

<span data-ttu-id="32286-133">Кроме того, в зависимости от синтаксиса атрибута " &lt; значение &gt; " может содержать символ-шаблон (" \* ").</span><span class="sxs-lookup"><span data-stu-id="32286-133">In addition, depending on the attribute syntax, the "&lt;value&gt;" may contain the wildcard symbol ("\*").</span></span> <span data-ttu-id="32286-134">" &lt; Значение &gt; ", содержащее только подстановочный знак, проверяет наличие любого значения в " &lt; Attribute &gt; ".</span><span class="sxs-lookup"><span data-stu-id="32286-134">A "&lt;value&gt;" that contains only a wildcard will check for the existence of any value in "&lt;attribute&gt;".</span></span> <span data-ttu-id="32286-135">Если значение атрибута не задано &lt; &gt; , тест завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="32286-135">If no value is set for "&lt;attribute&gt;", the test will fail.</span></span>

<span data-ttu-id="32286-136">Если любой из следующих специальных символов должен появиться в фильтре запроса в виде литералов, они должны быть заменены указанной escape-последовательностью.</span><span class="sxs-lookup"><span data-stu-id="32286-136">If any of the following special characters must appear in the query filter as literals, they must be replaced by the listed escape sequence.</span></span>



| <span data-ttu-id="32286-137">Символ ASCII</span><span class="sxs-lookup"><span data-stu-id="32286-137">ASCII character</span></span>    | <span data-ttu-id="32286-138">Замена escape-последовательности</span><span class="sxs-lookup"><span data-stu-id="32286-138">Escape sequence substitute</span></span> |
|--------------------|----------------------------|
| \*<br/>      | <span data-ttu-id="32286-139">\\2A</span><span class="sxs-lookup"><span data-stu-id="32286-139">"\\2a"</span></span><br/>          |
| <span data-ttu-id="32286-140">(</span><span class="sxs-lookup"><span data-stu-id="32286-140">(</span></span><br/>       | <span data-ttu-id="32286-141">\\28</span><span class="sxs-lookup"><span data-stu-id="32286-141">"\\28"</span></span><br/>          |
| <span data-ttu-id="32286-142">)</span><span class="sxs-lookup"><span data-stu-id="32286-142">)</span></span><br/>       | <span data-ttu-id="32286-143">" \\ 29"</span><span class="sxs-lookup"><span data-stu-id="32286-143">"\\29"</span></span><br/>          |
| \\<br/>      | <span data-ttu-id="32286-144">" \\ 5C"</span><span class="sxs-lookup"><span data-stu-id="32286-144">"\\5c"</span></span><br/>          |
| <span data-ttu-id="32286-145">**NUL**</span><span class="sxs-lookup"><span data-stu-id="32286-145">**NUL**</span></span><br/> | <span data-ttu-id="32286-146">" \\ 00"</span><span class="sxs-lookup"><span data-stu-id="32286-146">"\\00"</span></span><br/>          |



 

<span data-ttu-id="32286-147">Кроме того, произвольные двоичные данные могут быть представлены с помощью синтаксиса escape-последовательности путем кодирования каждого байта двоичных данных с помощью обратной косой черты, за которой следуют две шестнадцатеричные цифры.</span><span class="sxs-lookup"><span data-stu-id="32286-147">In addition, arbitrary binary data may be represented using the escape sequence syntax by encoding each byte of binary data with the backslash followed by two hexadecimal digits.</span></span> <span data-ttu-id="32286-148">Например, 4-байтовый параметр 0x00000004 кодируется как " \\ 00 \\ 00 \\ 00 \\ 04" в строке фильтра.</span><span class="sxs-lookup"><span data-stu-id="32286-148">For example, the four-byte value 0x00000004 is encoded as "\\00\\00\\00\\04" in a filter string.</span></span>

## <a name="examples"></a><span data-ttu-id="32286-149">Примеры</span><span class="sxs-lookup"><span data-stu-id="32286-149">Examples</span></span>

<span data-ttu-id="32286-150">Следующая строка запроса будет искать все объекты типа "Computer".</span><span class="sxs-lookup"><span data-stu-id="32286-150">The following query string will search for all objects of type "computer".</span></span>


```C++
(objectCategory=computer)
```



<span data-ttu-id="32286-151">Следующая строка запроса будет искать все объекты типа "Computer" с именем, которое начинается с "Desktop".</span><span class="sxs-lookup"><span data-stu-id="32286-151">The following query string will search for all objects of type "computer" with a name that begins with "desktop".</span></span>


```C++
(&(objectCategory=computer)(name=desktop*))
```



<span data-ttu-id="32286-152">Следующая строка запроса будет искать все объекты типа "Computer" с именем, начинающимся с "Desktop", или именем, которое начинается с "Записная книжка".</span><span class="sxs-lookup"><span data-stu-id="32286-152">The following query string will search for all objects of type "computer" with a name that begins with "desktop" or a name that begins with "notebook".</span></span>


```C++
(&(objectCategory=computer)(|(name=desktop*)(name=notebook*)))
```



<span data-ttu-id="32286-153">Следующая строка запроса будет искать все объекты типа "User" с номером домашнего телефона.</span><span class="sxs-lookup"><span data-stu-id="32286-153">The following query string will search for all objects of type "user" that have a home phone number.</span></span>


```C++
(&(objectCategory=user)(homePhone=*))
```



<span data-ttu-id="32286-154">Дополнительные сведения о строках фильтра запросов и примеры использования см. в следующих статьях:</span><span class="sxs-lookup"><span data-stu-id="32286-154">For more information about query filter strings, and usage examples, see:</span></span>

-   [<span data-ttu-id="32286-155">Поиск объектов по классу</span><span class="sxs-lookup"><span data-stu-id="32286-155">Finding Objects by Class</span></span>](finding-objects-by-class.md)
-   [<span data-ttu-id="32286-156">Поиск объектов по имени</span><span class="sxs-lookup"><span data-stu-id="32286-156">Finding Objects by Name</span></span>](finding-objects-by-name.md)
-   [<span data-ttu-id="32286-157">Поиск списка атрибутов для запроса</span><span class="sxs-lookup"><span data-stu-id="32286-157">Finding a List of Attributes To Query</span></span>](finding-a-list-of-attributes-to-query.md)
-   [<span data-ttu-id="32286-158">Проверка синтаксиса фильтра запросов</span><span class="sxs-lookup"><span data-stu-id="32286-158">Checking the Query Filter Syntax</span></span>](checking-the-query-filter-syntax.md)
-   [<span data-ttu-id="32286-159">Как указать значения для сравнения</span><span class="sxs-lookup"><span data-stu-id="32286-159">How to Specify Comparison Values</span></span>](how-to-specify-comparison-values.md)

 

 





