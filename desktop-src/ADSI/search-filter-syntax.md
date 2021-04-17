---
title: Синтаксис фильтра поиска
description: Фильтры поиска позволяют определять условия поиска и предоставлять более эффективные и эффективные поисковые запросы.
ms.assetid: 3ce4709c-5ef7-4713-8fb7-b46ab284339f
ms.tgt_platform: multiple
keywords:
- Синтаксис фильтра поиска ADSI
- запросы, синтаксис фильтра поиска
ms.topic: article
ms.date: 09/25/2020
ms.openlocfilehash: 28875bd49a3d1df7418c37706e58852066bbe08a
ms.sourcegitcommit: 4570ac533e129ff88b23f2c2b69e0140ead3a4a4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/26/2021
ms.locfileid: "105658143"
---
# <a name="search-filter-syntax"></a><span data-ttu-id="c4265-105">Синтаксис фильтра поиска</span><span class="sxs-lookup"><span data-stu-id="c4265-105">Search Filter Syntax</span></span>

<span data-ttu-id="c4265-106">Фильтры поиска позволяют определять условия поиска и предоставлять более эффективные и эффективные поисковые запросы.</span><span class="sxs-lookup"><span data-stu-id="c4265-106">Search filters enable you to define search criteria and provide more efficient and effective searches.</span></span>

<span data-ttu-id="c4265-107">ADSI поддерживает фильтры поиска LDAP, как определено в RFC2254.</span><span class="sxs-lookup"><span data-stu-id="c4265-107">ADSI supports the LDAP search filters as defined in RFC2254.</span></span> <span data-ttu-id="c4265-108">Эти фильтры поиска представлены строками Юникода.</span><span class="sxs-lookup"><span data-stu-id="c4265-108">These search filters are represented by Unicode strings.</span></span> <span data-ttu-id="c4265-109">В следующей таблице перечислены некоторые примеры фильтров поиска LDAP.</span><span class="sxs-lookup"><span data-stu-id="c4265-109">The following table lists some examples of LDAP search filters.</span></span>



| <span data-ttu-id="c4265-110">Фильтр поиска</span><span class="sxs-lookup"><span data-stu-id="c4265-110">Search filter</span></span>                                                               | <span data-ttu-id="c4265-111">Описание</span><span class="sxs-lookup"><span data-stu-id="c4265-111">Description</span></span>                                                |
|-----------------------------------------------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="c4265-112">"(objectClass = \* )"</span><span class="sxs-lookup"><span data-stu-id="c4265-112">"(objectClass=\*)"</span></span>                                                          | <span data-ttu-id="c4265-113">Все объекты.</span><span class="sxs-lookup"><span data-stu-id="c4265-113">All objects.</span></span>                                               |
| <span data-ttu-id="c4265-114">"(& (objectCategory = Person) (objectClass = User) (! ( CN = Энди))) "</span><span class="sxs-lookup"><span data-stu-id="c4265-114">"(&(objectCategory=person)(objectClass=user)(!(cn=andy)))"</span></span>                  | <span data-ttu-id="c4265-115">Все пользовательские объекты, но «Энди».</span><span class="sxs-lookup"><span data-stu-id="c4265-115">All user objects but "andy".</span></span>                               |
| <span data-ttu-id="c4265-116">"(SN = SM \* )"</span><span class="sxs-lookup"><span data-stu-id="c4265-116">"(sn=sm\*)"</span></span>                                                                 | <span data-ttu-id="c4265-117">Все объекты с фамилией, начинающейся с "SM".</span><span class="sxs-lookup"><span data-stu-id="c4265-117">All objects with a surname that starts with "sm".</span></span>          |
| <span data-ttu-id="c4265-118">"(& (objectCategory = Person) (objectClass = Contact) ( \| (SN = Smith) (SN = Джонсон)))"</span><span class="sxs-lookup"><span data-stu-id="c4265-118">"(&(objectCategory=person)(objectClass=contact)(\|(sn=Smith)(sn=Johnson)))"</span></span> | <span data-ttu-id="c4265-119">Все контакты с фамилией, равным "Иванов" или "Джонсон".</span><span class="sxs-lookup"><span data-stu-id="c4265-119">All contacts with a surname equal to "Smith" or "Johnson".</span></span> |



 

<span data-ttu-id="c4265-120">Эти фильтры поиска используют один из следующих форматов.</span><span class="sxs-lookup"><span data-stu-id="c4265-120">These search filters use one of the following formats.</span></span>


```C++
<filter>=(<attribute><operator><value>)
```



<span data-ttu-id="c4265-121">или</span><span class="sxs-lookup"><span data-stu-id="c4265-121">or</span></span>


```C++
(<operator><filter1><filter2>)
```



<span data-ttu-id="c4265-122">Фильтры поиска ADSI используются двумя способами.</span><span class="sxs-lookup"><span data-stu-id="c4265-122">The ADSI search filters are used in two ways.</span></span> <span data-ttu-id="c4265-123">Они формируют часть диалекта LDAP для отправки запросов через поставщика OLE DB.</span><span class="sxs-lookup"><span data-stu-id="c4265-123">They form a part of the LDAP dialect for submitting queries through the OLE DB provider.</span></span> <span data-ttu-id="c4265-124">Они также используются с интерфейсом [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) .</span><span class="sxs-lookup"><span data-stu-id="c4265-124">They are also used with the [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) interface.</span></span>

## <a name="operators"></a><span data-ttu-id="c4265-125">Операторы</span><span class="sxs-lookup"><span data-stu-id="c4265-125">Operators</span></span>

<span data-ttu-id="c4265-126">В следующей таблице перечислены часто используемые операторы фильтра поиска.</span><span class="sxs-lookup"><span data-stu-id="c4265-126">The following table lists frequently used search filter operators.</span></span>



| <span data-ttu-id="c4265-127">Логический оператор</span><span class="sxs-lookup"><span data-stu-id="c4265-127">Logical operator</span></span> | <span data-ttu-id="c4265-128">Описание</span><span class="sxs-lookup"><span data-stu-id="c4265-128">Description</span></span>                                |
|------------------|--------------------------------------------|
| =                | <span data-ttu-id="c4265-129">Равно</span><span class="sxs-lookup"><span data-stu-id="c4265-129">Equal to</span></span>                                   |
| ~=               | <span data-ttu-id="c4265-130">Приблизительно равно</span><span class="sxs-lookup"><span data-stu-id="c4265-130">Approximately equal to</span></span>                     |
| <=            | <span data-ttu-id="c4265-131">Лексикографически меньше или равно</span><span class="sxs-lookup"><span data-stu-id="c4265-131">Lexicographically less than or equal to</span></span>    |
| >=            | <span data-ttu-id="c4265-132">Лексикографически больше или равно</span><span class="sxs-lookup"><span data-stu-id="c4265-132">Lexicographically greater than or equal to</span></span> |
| &                | <span data-ttu-id="c4265-133">AND</span><span class="sxs-lookup"><span data-stu-id="c4265-133">AND</span></span>                                        |
| \|               | <span data-ttu-id="c4265-134">OR</span><span class="sxs-lookup"><span data-stu-id="c4265-134">OR</span></span>                                         |
| <span data-ttu-id="c4265-135">!</span><span class="sxs-lookup"><span data-stu-id="c4265-135">!</span></span>                | <span data-ttu-id="c4265-136">NOT</span><span class="sxs-lookup"><span data-stu-id="c4265-136">NOT</span></span>                                        |



 

<span data-ttu-id="c4265-137">В дополнение к операторам, приведенным выше, LDAP определяет два сопоставления идентификаторов объектов правил (OID), которые можно использовать для побитового сравнения числовых значений.</span><span class="sxs-lookup"><span data-stu-id="c4265-137">In addition to the operators above, LDAP defines two matching rule object identifiers (OIDs) that can be used to perform bitwise comparisons of numeric values.</span></span> <span data-ttu-id="c4265-138">Правила сопоставления имеют следующий синтаксис.</span><span class="sxs-lookup"><span data-stu-id="c4265-138">Matching rules have the following syntax.</span></span>


```C++
<attribute name>:<matching rule OID>:=<value>
```



<span data-ttu-id="c4265-139">" &lt; имя атрибута &gt; " — это атрибут **lDAPDisplayName** атрибута, " &lt; rule OID &gt; " — OID для правила сопоставления, а " &lt; value &gt; " — это значение, используемое для сравнения.</span><span class="sxs-lookup"><span data-stu-id="c4265-139">"&lt;attribute name&gt;" is the **lDAPDisplayName** of the attribute, "&lt;rule OID&gt;" is the OID for the matching rule, and "&lt;value&gt;" is the value to use for comparison.</span></span> <span data-ttu-id="c4265-140">Имейте в виду, что в этой строке нельзя использовать пробелы.</span><span class="sxs-lookup"><span data-stu-id="c4265-140">Be aware that spaces cannot be used in this string.</span></span> <span data-ttu-id="c4265-141">" &lt; значение &gt; " должно быть десятичным числом; оно не может быть шестнадцатеричным числом или постоянным именем, таким как " **\_ \_ \_ \_ Включение безопасности типа группы баннеров**".</span><span class="sxs-lookup"><span data-stu-id="c4265-141">"&lt;value&gt;" must be a decimal number; it cannot be a hexadecimal number or a constant name such as **ADS\_GROUP\_TYPE\_SECURITY\_ENABLED**.</span></span> <span data-ttu-id="c4265-142">Дополнительные сведения о доступных атрибутах Active Directory см. в разделе [все атрибуты](/windows/desktop/ADSchema/attributes-all).</span><span class="sxs-lookup"><span data-stu-id="c4265-142">For more information about the available Active Directory attributes, see [All Attributes](/windows/desktop/ADSchema/attributes-all).</span></span>

<span data-ttu-id="c4265-143">В следующей таблице перечислены идентификаторы объектов правил сопоставления, реализованные в LDAP.</span><span class="sxs-lookup"><span data-stu-id="c4265-143">The following table lists the matching rule OIDs implemented by LDAP.</span></span>



| <span data-ttu-id="c4265-144">Идентификатор объекта правила сопоставления</span><span class="sxs-lookup"><span data-stu-id="c4265-144">Matching rule OID</span></span>       | <span data-ttu-id="c4265-145">Идентификатор строки (из Нтлдап. h)</span><span class="sxs-lookup"><span data-stu-id="c4265-145">String identifier (from Ntldap.h)</span></span>   | <span data-ttu-id="c4265-146">Описание</span><span class="sxs-lookup"><span data-stu-id="c4265-146">Description</span></span>                                                                                                                                                                                   |
|-------------------------|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4265-147">1.2.840.113556.1.4.803</span><span class="sxs-lookup"><span data-stu-id="c4265-147">1.2.840.113556.1.4.803</span></span>  | <span data-ttu-id="c4265-148">**\_ \_ бит правила сопоставления \_ LDAP \_ и**</span><span class="sxs-lookup"><span data-stu-id="c4265-148">**LDAP\_MATCHING\_RULE\_BIT\_AND**</span></span>  | <span data-ttu-id="c4265-149">Совпадение обнаруживается только в том случае, если все биты атрибута соответствуют значению.</span><span class="sxs-lookup"><span data-stu-id="c4265-149">A match is found only if all bits from the attribute match the value.</span></span> <span data-ttu-id="c4265-150">Это правило эквивалентно побитовому оператору **и** .</span><span class="sxs-lookup"><span data-stu-id="c4265-150">This rule is equivalent to a bitwise **AND** operator.</span></span>                                                                  |
| <span data-ttu-id="c4265-151">1.2.840.113556.1.4.804</span><span class="sxs-lookup"><span data-stu-id="c4265-151">1.2.840.113556.1.4.804</span></span>  | <span data-ttu-id="c4265-152">**\_ \_ бит правила сопоставления \_ LDAP \_ или**</span><span class="sxs-lookup"><span data-stu-id="c4265-152">**LDAP\_MATCHING\_RULE\_BIT\_OR**</span></span>   | <span data-ttu-id="c4265-153">Совпадение обнаруживается, если все биты атрибута соответствуют значению.</span><span class="sxs-lookup"><span data-stu-id="c4265-153">A match is found if any bits from the attribute match the value.</span></span> <span data-ttu-id="c4265-154">Это правило эквивалентно побитовому оператору **или** .</span><span class="sxs-lookup"><span data-stu-id="c4265-154">This rule is equivalent to a bitwise **OR** operator.</span></span>                                                                        |
| <span data-ttu-id="c4265-155">1.2.840.113556.1.4.1941</span><span class="sxs-lookup"><span data-stu-id="c4265-155">1.2.840.113556.1.4.1941</span></span> | <span data-ttu-id="c4265-156">**\_правило СОПОСТАВЛЕНИЯ \_ LDAP \_ в \_ цепочке**</span><span class="sxs-lookup"><span data-stu-id="c4265-156">**LDAP\_MATCHING\_RULE\_IN\_CHAIN**</span></span> | <span data-ttu-id="c4265-157">Это правило ограничено фильтрами, применяемыми к DN.</span><span class="sxs-lookup"><span data-stu-id="c4265-157">This rule is limited to filters that apply to the DN.</span></span> <span data-ttu-id="c4265-158">Это специальный расширенный оператор match, который просматривает цепочку происхождение в объектах до корня до тех пор, пока не обнаружит совпадение.</span><span class="sxs-lookup"><span data-stu-id="c4265-158">This is a special "extended" match operator that walks the chain of ancestry in objects all the way to the root until it finds a match.</span></span> |



 

<span data-ttu-id="c4265-159">В следующем примере строки запроса выполняется поиск объектов Group, для которых установлен флаг **\_ \_ \_ \_ включения безопасности типа группы ADS** .</span><span class="sxs-lookup"><span data-stu-id="c4265-159">The following example query string searches for group objects that have the **ADS\_GROUP\_TYPE\_SECURITY\_ENABLED** flag set.</span></span> <span data-ttu-id="c4265-160">Имейте в виду, что для значения сравнения используется десятичное значение **\_ \_ \_ безопасности типа \_ группы ADS** (0x80000000 = 2147483648).</span><span class="sxs-lookup"><span data-stu-id="c4265-160">Be aware that the decimal value of **ADS\_GROUP\_TYPE\_SECURITY\_ENABLED** (0x80000000 = 2147483648) is used for the comparison value.</span></span>


```C++
(&(objectCategory=group)(groupType:1.2.840.113556.1.4.803:=2147483648))
```



<span data-ttu-id="c4265-161">**\_ Правило сопоставления LDAP \_ \_ в \_ цепочке** — это идентификатор OID правила сопоставления, предназначенный для предоставления метода для поиска происхождение объекта.</span><span class="sxs-lookup"><span data-stu-id="c4265-161">The **LDAP\_MATCHING\_RULE\_IN\_CHAIN** is a matching rule OID that is designed to provide a method to look up the ancestry of an object.</span></span> <span data-ttu-id="c4265-162">Многие приложения, использующие AD и AD LDS, обычно работают с иерархическими данными, упорядоченными по связям типа «родители-потомки».</span><span class="sxs-lookup"><span data-stu-id="c4265-162">Many applications using AD and AD LDS usually work with hierarchical data, which is ordered by parent-child relationships.</span></span> <span data-ttu-id="c4265-163">Ранее приложения выполнили расширение транзитивных групп, чтобы определить членство в группе, которое использовало слишком много пропускной способности сети. приложения, которые требовали несколько обращений для определения того, находился ли объект в цепочке в случае прохода по ссылке до конца.</span><span class="sxs-lookup"><span data-stu-id="c4265-163">Previously, applications performed transitive group expansion to figure out group membership, which used too much network bandwidth; applications needed to make multiple roundtrips to figure out if an object fell "in the chain" if a link is traversed through to the end.</span></span>

<span data-ttu-id="c4265-164">Примером такого запроса является проверка того, является ли пользователь user1 членом группы "Group1".</span><span class="sxs-lookup"><span data-stu-id="c4265-164">An example of such a query is one designed to check if a user "user1" is a member of group "group1".</span></span> <span data-ttu-id="c4265-165">Необходимо задать для базы данных имя пользователя `(cn=user1, cn=users, dc=x)` и область `base` , а затем использовать следующий запрос.</span><span class="sxs-lookup"><span data-stu-id="c4265-165">You would set the base to the user DN `(cn=user1, cn=users, dc=x)` and the scope to `base`, and use the following query.</span></span>


```C++
(memberof:1.2.840.113556.1.4.1941:=cn=Group1,OU=groupsOU,DC=x)
```



<span data-ttu-id="c4265-166">Аналогично, чтобы найти все группы, членом которых является Пользователь1, установите базовое имя для контейнера групп. например `(OU=groupsOU, dc=x)` , и область `subtree` , и используйте следующий фильтр.</span><span class="sxs-lookup"><span data-stu-id="c4265-166">Similarly, to find all the groups that "user1" is a member of, set the base to the groups container DN; for example `(OU=groupsOU, dc=x)` and the scope to `subtree`, and use the following filter.</span></span>


```C++
(member:1.2.840.113556.1.4.1941:=cn=user1,cn=users,DC=x)
```



<span data-ttu-id="c4265-167">Обратите внимание, что при использовании **\_ правила сопоставления LDAP \_ \_ в \_ цепочке** область ограниченна — это может быть `base` , `one-level` или `subtree` .</span><span class="sxs-lookup"><span data-stu-id="c4265-167">Note that when using **LDAP\_MATCHING\_RULE\_IN\_CHAIN**, scope is not limited—it can be `base`, `one-level`, or `subtree`.</span></span> <span data-ttu-id="c4265-168">Некоторые запросы к поддеревьям могут потребовать больше ресурсов процессора, таких как отслеживание ссылок с высоким уровнем их вращения. то есть список всех групп, членом которых является пользователь.</span><span class="sxs-lookup"><span data-stu-id="c4265-168">Some such queries on subtrees may be more processor intensive, such as chasing links with a high fan-out; that is, listing all the groups that a user is a member of.</span></span> <span data-ttu-id="c4265-169">При неэффективном поиске будут регистрироваться соответствующие сообщения журнала событий, как в случае любого другого типа запросов.</span><span class="sxs-lookup"><span data-stu-id="c4265-169">Inefficient searches will log appropriate event log messages, as with any other type of query.</span></span>

## <a name="wildcards"></a><span data-ttu-id="c4265-170">Подстановочные знаки</span><span class="sxs-lookup"><span data-stu-id="c4265-170">Wildcards</span></span>

<span data-ttu-id="c4265-171">В фильтр поиска LDAP также можно добавить подстановочные знаки и условия.</span><span class="sxs-lookup"><span data-stu-id="c4265-171">You can also add wildcards and conditions to an LDAP search filter.</span></span> <span data-ttu-id="c4265-172">В следующих примерах показаны подстроки, которые можно использовать для поиска в каталоге.</span><span class="sxs-lookup"><span data-stu-id="c4265-172">The following examples show substrings that can be used to search the directory.</span></span>

<span data-ttu-id="c4265-173">Получить все записи:</span><span class="sxs-lookup"><span data-stu-id="c4265-173">Get all entries:</span></span>


```C++
(objectClass=*)
```



<span data-ttu-id="c4265-174">Получение записей, содержащих "Bob" где-нибудь в общем имени:</span><span class="sxs-lookup"><span data-stu-id="c4265-174">Get entries containing "bob" somewhere in the common name:</span></span>


```C++
(cn=*bob*)
```



<span data-ttu-id="c4265-175">Получить записи с общим именем, большим или равным "Bob":</span><span class="sxs-lookup"><span data-stu-id="c4265-175">Get entries with a common name greater than or equal to "bob":</span></span>


```C++
(cn>='bob')
```



<span data-ttu-id="c4265-176">Получить всех пользователей с атрибутом email:</span><span class="sxs-lookup"><span data-stu-id="c4265-176">Get all users with an email attribute:</span></span>


```C++
(&(objectClass=user)(email=*))
```



<span data-ttu-id="c4265-177">Получить все записи пользователей с атрибутом сообщения электронной почты и фамилией, равной Smith:</span><span class="sxs-lookup"><span data-stu-id="c4265-177">Get all user entries with an email attribute and a surname equal to "smith":</span></span>


```C++
(&(sn=smith)(objectClass=user)(email=*))
```



<span data-ttu-id="c4265-178">Получить все записи пользователей с общим именем, которое начинается с "Энди", "Стив" или "Margaret":</span><span class="sxs-lookup"><span data-stu-id="c4265-178">Get all user entries with a common name that starts with "andy", "steve", or "margaret":</span></span>


```C++
(&(objectClass=user)(| (cn=andy*)(cn=steve*)(cn=margaret*)))
```



<span data-ttu-id="c4265-179">Получить все записи без атрибута email:</span><span class="sxs-lookup"><span data-stu-id="c4265-179">Get all entries without an email attribute:</span></span>


```C++
(!(email=*))
```



<span data-ttu-id="c4265-180">Формальное определение фильтра поиска выглядит следующим образом (из [RFC 2254](https://tools.ietf.org/html/rfc2254)):</span><span class="sxs-lookup"><span data-stu-id="c4265-180">The formal definition of the search filter is as follows (from [RFC 2254](https://tools.ietf.org/html/rfc2254)):</span></span>


```C++
<filter> ::= '(' <filtercomp> ')'
<filtercomp> ::= <and> | <or> | <not> | <item>
<and> ::= '&' <filterlist>
<or> ::= '|' <filterlist>
<not> ::= '!' <filter>
<filterlist> ::= <filter> | <filter> <filterlist>
<item>::= <simple> | <present> | <substring>
<simple> ::= <attr> <filtertype> <value><filtertype> ::= <equal> | <approx> | <ge> | <le>
<equal> ::= '='
<approx> ::= '~='
<ge> ::= '>='
<le> ::= '<='
<present> ::= <attr> '=*'
<substring> ::= <attr> '=' <initial> <any> <final>
<initial> ::= NULL | <value><any> ::= '*' <starval>
<starval> ::= NULL | <value>'*' <starval>
<final> ::= NULL | <value>
```



<span data-ttu-id="c4265-181">&lt;Attr токена &gt; — это строка, представляющая attributeType.</span><span class="sxs-lookup"><span data-stu-id="c4265-181">The token &lt;attr&gt; is a string that represents an AttributeType.</span></span> <span data-ttu-id="c4265-182">&lt;Значение токена &gt; — это строка, представляющая значение AttributeValue, формат которого определяется базовой службой каталогов.</span><span class="sxs-lookup"><span data-stu-id="c4265-182">The token &lt;value&gt; is a string that represents an AttributeValue whose format is defined by the underlying directory service.</span></span>

<span data-ttu-id="c4265-183">Если &lt; значение &gt; должно содержать символ звездочки ( \* ), открывающую круглую скобку (() или правую круглую скобку ()), перед символом должен стоять escape-символ обратной косой черты ( \\ ).</span><span class="sxs-lookup"><span data-stu-id="c4265-183">If a &lt;value&gt; must contain the asterisk (\*), left parenthesis ((), or right parenthesis ()) character, the character should be preceded by the backslash escape character (\\).</span></span>

## <a name="special-characters"></a><span data-ttu-id="c4265-184">Специальные символы</span><span class="sxs-lookup"><span data-stu-id="c4265-184">Special Characters</span></span>

<span data-ttu-id="c4265-185">Если какой-либо из следующих специальных символов должен отображаться в фильтре поиска как литералы, они должны быть заменены указанной escape-последовательностью.</span><span class="sxs-lookup"><span data-stu-id="c4265-185">If any of the following special characters must appear in the search filter as literals, they must be replaced by the listed escape sequence.</span></span>



| <span data-ttu-id="c4265-186">Символ ASCII</span><span class="sxs-lookup"><span data-stu-id="c4265-186">ASCII character</span></span> | <span data-ttu-id="c4265-187">Замена escape-последовательности</span><span class="sxs-lookup"><span data-stu-id="c4265-187">Escape sequence substitute</span></span> |
|-----------------|----------------------------|
| \*              | <span data-ttu-id="c4265-188">\\2а</span><span class="sxs-lookup"><span data-stu-id="c4265-188">\\2a</span></span>                       |
| <span data-ttu-id="c4265-189">(</span><span class="sxs-lookup"><span data-stu-id="c4265-189">(</span></span>               | <span data-ttu-id="c4265-190">\\8</span><span class="sxs-lookup"><span data-stu-id="c4265-190">\\28</span></span>                       |
| <span data-ttu-id="c4265-191">)</span><span class="sxs-lookup"><span data-stu-id="c4265-191">)</span></span>               | <span data-ttu-id="c4265-192">\\29</span><span class="sxs-lookup"><span data-stu-id="c4265-192">\\29</span></span>                       |
| \\              | <span data-ttu-id="c4265-193">\\5C</span><span class="sxs-lookup"><span data-stu-id="c4265-193">\\5c</span></span>                       |
| <span data-ttu-id="c4265-194">NUL</span><span class="sxs-lookup"><span data-stu-id="c4265-194">NUL</span></span>             | <span data-ttu-id="c4265-195">\\100,00</span><span class="sxs-lookup"><span data-stu-id="c4265-195">\\00</span></span>                       |
| /               | <span data-ttu-id="c4265-196">\\2F</span><span class="sxs-lookup"><span data-stu-id="c4265-196">\\2f</span></span>                       |



 

> [!Note]  
> <span data-ttu-id="c4265-197">В случаях, когда используется многобайтовый набор символов, необходимо использовать escape-последовательности, перечисленные выше, если поиск выполняется ADO с использованием диалекта SQL.</span><span class="sxs-lookup"><span data-stu-id="c4265-197">In cases where a MultiByte Character Set is being used, the escape sequences listed above must be used if the search is performed by ADO with the SQL dialect.</span></span>

 

<span data-ttu-id="c4265-198">Кроме того, произвольные двоичные данные могут быть представлены с помощью синтаксиса escape-последовательности путем кодирования каждого байта двоичных данных с помощью обратной косой черты ( \\ ), за которой следуют две шестнадцатеричные цифры.</span><span class="sxs-lookup"><span data-stu-id="c4265-198">In addition, arbitrary binary data may be represented by using the escape sequence syntax by encoding each byte of binary data with the backslash (\\) followed by two hexadecimal digits.</span></span> <span data-ttu-id="c4265-199">Например, 4-байтовый параметр 0x00000004 кодируется как \\ 00 \\ 00 \\ 00 \\ 04 в строке фильтра.</span><span class="sxs-lookup"><span data-stu-id="c4265-199">For example, the four-byte value 0x00000004 is encoded as \\00\\00\\00\\04 in a filter string.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c4265-200">См. также</span><span class="sxs-lookup"><span data-stu-id="c4265-200">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c4265-201">Диалект LDAP</span><span class="sxs-lookup"><span data-stu-id="c4265-201">LDAP dialect</span></span>](ldap-dialect.md)
</dt> <dt>

[<span data-ttu-id="c4265-202">Диалект SQL</span><span class="sxs-lookup"><span data-stu-id="c4265-202">SQL dialect</span></span>](sql-dialect.md)
</dt> <dt>

[<span data-ttu-id="c4265-203">Поиск с помощью интерфейса IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="c4265-203">Searching with the IDirectorySearch Interface</span></span>](searching-with-idirectorysearch.md)
</dt> <dt>

[<span data-ttu-id="c4265-204">Поиск с помощью объекты данных ActiveX</span><span class="sxs-lookup"><span data-stu-id="c4265-204">Searching with ActiveX Data Objects</span></span>](searching-with-activex-data-objects-ado.md)
</dt> <dt>

[<span data-ttu-id="c4265-205">Поиск с помощью OLE DB</span><span class="sxs-lookup"><span data-stu-id="c4265-205">Searching with OLE DB</span></span>](searching-with-ole-db.md)
</dt> </dl>

 

 
