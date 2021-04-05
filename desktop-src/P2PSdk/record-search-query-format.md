---
description: Вызов функции Пирграупсеарчрекордс требует наличия параметра строки запроса XML, который используется для определения основных критериев поиска.
ms.assetid: 2c5ab425-6959-418a-8d9a-c8155257fc7e
title: Формат запроса поиска записей
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02b475c8a449e3bcd360df5757fef508b1a744d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911624"
---
# <a name="record-search-query-format"></a><span data-ttu-id="4126b-103">Формат запроса поиска записей</span><span class="sxs-lookup"><span data-stu-id="4126b-103">Record Search Query Format</span></span>

<span data-ttu-id="4126b-104">Вызов функции [**пирграупсеарчрекордс**](/windows/desktop/api/P2P/nf-p2p-peergroupsearchrecords) требует наличия параметра строки запроса XML, который используется для определения основных критериев поиска.</span><span class="sxs-lookup"><span data-stu-id="4126b-104">A call to the [**PeerGroupSearchRecords**](/windows/desktop/api/P2P/nf-p2p-peergroupsearchrecords) function requires an XML query string parameter that is used to determine the basic criteria of a search.</span></span> <span data-ttu-id="4126b-105">Используйте следующую схему для формирования XML-строки:</span><span class="sxs-lookup"><span data-stu-id="4126b-105">Use the following schema to formulate an XML string:</span></span>

``` syntax
<?xml version="1.0" encoding="utf-8" ?>
<xs:schema xmlns:xs="https://www.w3.org/2001/XMLSchema">

  <xs:simpleType name="alphanumType">
     <xs:restriction base="xs:string">
        <xs:pattern value="\c+"/>
     </xs:restriction>
  </xs:simpleType>

  <xs:complexType name="operatorType">
      <xs:choice maxOccurs="unbounded">
         <xs:element ref="and" />
         <xs:element ref="or" />
         <xs:element ref="clause" />
      </xs:choice>
  </xs:complexType>

  <xs:element name="and" type="operatorType"/>

  <xs:element name="or" type="operatorType"/>

  <xs:element name="clause">
      <xs:complexType>
          <xs:simpleContent>
              <xs:extension base="xs:string">
        <xs:attribute name="attrib" type="alphanumType" />
        <xs:attribute name="type">
                  <xs:simpleType>
                    <xs:restriction base="xs:string">
                      <xs:enumeration value="string"/>
                      <xs:enumeration value="date"/>
                      <xs:enumeration value="int"/>
                    </xs:restriction>
                  </xs:simpleType>
                </xs:attribute>
        <xs:attribute name="compare" default="equal">
                  <xs:simpleType>
                    <xs:restriction base="xs:string">
                      <xs:enumeration value="equal"/>
                      <xs:enumeration value="greater"/>
                      <xs:enumeration value="less"/>
                      <xs:enumeration value="notequal"/>
                      <xs:enumeration value="greaterorequal"/>
                      <xs:enumeration value="lessorequal"/>
                    </xs:restriction>
                  </xs:simpleType>
                </xs:attribute>
              </xs:extension>
          </xs:simpleContent>
      </xs:complexType>
  </xs:element>

  <xs:element name="peersearch">
      <xs:complexType>
          <xs:choice>
              <xs:element ref="clause" />
              <xs:element ref="and" />
              <xs:element ref="or" />
          </xs:choice>
      </xs:complexType>
  </xs:element>
</xs:schema> 
```

### <a name="elements-to-use-for-a-record-search"></a><span data-ttu-id="4126b-106">Элементы, используемые для поиска записей</span><span class="sxs-lookup"><span data-stu-id="4126b-106">Elements to Use for a Record Search</span></span>

<span data-ttu-id="4126b-107">Первичный элемент в поиске записей — **пирсеарч**, который содержит универсальный код ресурса (URI) связанной схемы в атрибуте **xmlns** .</span><span class="sxs-lookup"><span data-stu-id="4126b-107">The primary element in a record search is **peersearch**, which contains the Uniform Resource Identifier (URI) of the associated schema in the **xmlns** attribute.</span></span> <span data-ttu-id="4126b-108">Если **пирсеарч** используется как дочерний элемент, можно использовать предложения **and**,  **and и в качестве дочерних** элементов.</span><span class="sxs-lookup"><span data-stu-id="4126b-108">When **peersearch** is used as a child element, you can use **and**, **clause**, and **or** as child elements.</span></span>

-   <span data-ttu-id="4126b-109">**и** — элемент **and** выполняет логическую операцию AND над одним или несколькими предложениями, содержащимися между открывающим и закрывающим тегами.</span><span class="sxs-lookup"><span data-stu-id="4126b-109">**and** - The **and** element performs a logical AND operation on one or more clauses contained between the opening and closing tags.</span></span> <span data-ttu-id="4126b-110">Другие теги **and** и **or** могут быть дочерними, а рекурсивные результаты их дочерних предложений включаются в операцию.</span><span class="sxs-lookup"><span data-stu-id="4126b-110">Other **and** and **or** tags can be children, and recursive results of their child clauses are included in the operation.</span></span>

    <span data-ttu-id="4126b-111">Например, если вы хотите получить запись, содержащую имя, равное Джеймс Петерс, и Последнее обновление, которое больше 2/28/2003, или дату создания меньше 1/31/2003, используйте следующую строку запроса XML:</span><span class="sxs-lookup"><span data-stu-id="4126b-111">For example, if you want to obtain a record that contains a name equal to James Peters, and a last update that is greater than 2/28/2003, or a creation date that is less than 1/31/2003, use the following XML query string:</span></span>

    ``` syntax
    <?xml version="1.0" encoding="utf-8" ?> 
    <peersearch xmlns:xs="https://www.w3.org/2001/XMLSchema">
       <and>
          <clause attrib="peercreatorid" type="string" compare="equal">James Peters</clause>
          <or>
             <clause attrib="peerlastmodificationtime" type="date" compare="greater">2003-01-31</clause>
             <clause attrib="peercreationtime" type="date" compare="less">2003-02-328</clause>
          </or>
       </and>
    </peersearch>
    ```

<!-- -->

-   <span data-ttu-id="4126b-112">**— элемент** **предложения** указывает базовое правило сравнения, которое сравнивает значение определенного атрибута записи со значением, содержащимся между открывающим и закрывающим тегами.</span><span class="sxs-lookup"><span data-stu-id="4126b-112">**clause** - The **clause** element specifies a basic comparative rule that compares the value of a specific record attribute with the value contained between the opening and closing tags.</span></span> <span data-ttu-id="4126b-113">Необходимо указать атрибуты **Type** и **Compare** , чтобы **определить,** какая операция сравнения должна быть выполнена.</span><span class="sxs-lookup"><span data-stu-id="4126b-113">The **type** and **compare** attributes must be provided **compare** indicates the comparison operation to be performed.</span></span> <span data-ttu-id="4126b-114">Например, простой поиск, указывающий все совпадающие записи, должен иметь значение **пиркреаторид** , равное Джеймс Петерс, отображается в строке запроса XML следующим образом:</span><span class="sxs-lookup"><span data-stu-id="4126b-114">For example, a simple search that indicates all matched records must have a **peercreatorid** value equal to James Peters appears in the XML query string as the following:</span></span>

    ``` syntax
    <?xml version="1.0" encoding="utf-8" ?> 
    <peersearch xmlns:xs="https://www.w3.org/2001/XMLSchema">
       <clause attrib="peercreatorid" type="string" compare="equal">James Peters</clause>
    </peersearch>
    ```

    <span data-ttu-id="4126b-115">К общим атрибутам **типа** относятся **int**, **String** и **Date**.</span><span class="sxs-lookup"><span data-stu-id="4126b-115">Common **type** attributes include **int**, **string**, and **date**.</span></span> <span data-ttu-id="4126b-116">Атрибут **Date** может быть одним из стандартных форматов даты, описанных в разделе [https://www.w3.org/TR/NOTE-datetime](https://www.w3.org/TR/NOTE-datetime) .</span><span class="sxs-lookup"><span data-stu-id="4126b-116">The **date** attribute can be one of the standard date formats described at [https://www.w3.org/TR/NOTE-datetime](https://www.w3.org/TR/NOTE-datetime).</span></span>

    <span data-ttu-id="4126b-117">Значения для атрибута **Compare** **равны**, **NotEqual**, **less**, **больше**, **лессорекуал** и **греатерорекуал**.</span><span class="sxs-lookup"><span data-stu-id="4126b-117">Values for the **compare** attribute are **equal**, **notequal**, **less**, **greater**, **lessorequal**, and **greaterorequal**.</span></span>

<!-- -->

-   <span data-ttu-id="4126b-118">**или** -элемент **or** выполняет логическую операцию OR с одним или несколькими предложениями, содержащимися между открывающим и закрывающим тегами.</span><span class="sxs-lookup"><span data-stu-id="4126b-118">**or** - The **or** element performs a logical OR operation on one or more clauses contained between the opening and closing tags.</span></span> <span data-ttu-id="4126b-119">Другие  элементы or **и and могут** быть дочерними, а рекурсивные результаты дочерних предложений включаются в операцию.</span><span class="sxs-lookup"><span data-stu-id="4126b-119">Other **or** and **and** elements can be children, and recursive results of the child clauses are included in the operation.</span></span> <span data-ttu-id="4126b-120">Например, если вы хотите получить запись, содержащую имя, равное Джеймс Петерс, или Последнее обновление в диапазоне от 1/31/2003 до 2/28/2003, используйте следующую строку запроса XML:</span><span class="sxs-lookup"><span data-stu-id="4126b-120">For example, if you want to obtain a record that contains a name equal to James Peters, or a last update that is between 1/31/2003 and 2/28/2003, use the following XML query string:</span></span>

``` syntax
<?xml version="1.0" encoding="utf-8" ?> 
<peersearch xmlns:xs="https://www.w3.org/2001/XMLSchema">
   <or>
      <clause attrib="peercreatorid" type="string" compare="equal">James Peters</clause>
      <and>
         <clause attrib="peerlastmodificationtime" type="date" compare="greater">2003-01-31</clause>
         <clause attrib="peerlastmodificationtime" type="date" compare="less">2003-02-28</clause>
      </and>
   </or>
</peersearch>
```

## <a name="more-information-about-a-record-search"></a><span data-ttu-id="4126b-121">Дополнительные сведения о поиске записей</span><span class="sxs-lookup"><span data-stu-id="4126b-121">More Information About a Record Search</span></span>

<span data-ttu-id="4126b-122">Первый уровень узлов после **пирсеарч** может иметь только один элемент.</span><span class="sxs-lookup"><span data-stu-id="4126b-122">The first level of nodes after **peersearch** can have only one element.</span></span> <span data-ttu-id="4126b-123">Однако последующие дочерние элементы этого элемента могут иметь множество элементов на одном уровне.</span><span class="sxs-lookup"><span data-stu-id="4126b-123">However, subsequent children of that element can have many elements at the same level.</span></span>

<span data-ttu-id="4126b-124">Следующий поисковый запрос неверен:</span><span class="sxs-lookup"><span data-stu-id="4126b-124">The following search query is incorrect:</span></span>

``` syntax
<?xml version="1.0" encoding="utf-8" ?> 
<peersearch xmlns:xs="https://www.w3.org/2001/XMLSchema">
   <clause attrib="peercreatorid" type="string" compare="equal">James Peters</clause>
   <and>
      <clause attrib="peerlastmodificationtime" type="date" compare="greater">2003-01-31</clause>
      <clause attrib="peerlastmodificationtime" type="date" compare="less">2003-02-28</clause>
   </and>
</peersearch>
```

<span data-ttu-id="4126b-125">Запрос завершается ошибкой, так как для соответствия возвращаются два значения без разрешения в одно значение true/false. Это означает, что одно предложение является запросом имени записи, равной Джеймс Петерс, а операция и соответствует двум предложениям компонентов.</span><span class="sxs-lookup"><span data-stu-id="4126b-125">The query fails because two values are returned for the match without being resolved into one true/false value, which means that one clause is a query for the name of a record that equals James Peters, and the AND operation matches the two component clauses.</span></span> <span data-ttu-id="4126b-126">Результат — два логических значения true/false, которые являются противоречивыми.</span><span class="sxs-lookup"><span data-stu-id="4126b-126">The result is two logical true/false values that are contradictory.</span></span>

<span data-ttu-id="4126b-127">Чтобы получить все записи, содержащие имя, равное Джеймс Петерс, и Последнее обновление, которое находится в диапазоне от 1/31/2003 до 2/28/2003,  поместите предложение **и теги,** находящееся на том же уровне между открывающим и закрывающим тегами **и** .</span><span class="sxs-lookup"><span data-stu-id="4126b-127">To obtain all records that contain a name equal to James Peters, and a last update that is between 1/31/2003 and 2/28/2003, place the **clause** and **and** tags that are at the same level between opening and closing **and** tags.</span></span> <span data-ttu-id="4126b-128">В следующем примере показан успешный запрос:</span><span class="sxs-lookup"><span data-stu-id="4126b-128">The following example shows you the successful query:</span></span>

``` syntax
<?xml version="1.0" encoding="utf-8" ?> 
<peersearch xmlns:xs="https://www.w3.org/2001/XMLSchema">
    <and>
      <clause attrib="peercreatorid" type="string" compare="equal">James Peters</clause>
      <and>
         <clause attrib="peerlastmodificationtime" type="date" compare="greater">2003-01-31</clause>
         <clause attrib="peerlastmodificationtime" type="date" compare="less">2003-02-28</clause>
      </and>
   </and>
</peersearch>
```

<span data-ttu-id="4126b-129">В следующем списке приведены другие сведения, которые необходимо учитывать для написания успешного запроса.</span><span class="sxs-lookup"><span data-stu-id="4126b-129">The following list identifies other specific information that you must know to write a successful query:</span></span>

-   <span data-ttu-id="4126b-130">Теги **and** и **or** не могут располагаться между открывающими и закрывающими тегами **предложения** , так как в такой конфигурации они обрабатываются как часть значения для сопоставления, что приводит к ошибке или неудачному совпадению.</span><span class="sxs-lookup"><span data-stu-id="4126b-130">The **and** and **or** tags cannot be located between opening and closing **clause** tags because, in that configuration, they are interpreted as part of the value to match against, which results in an error or a failed match.</span></span>
-   <span data-ttu-id="4126b-131">Каждая пара **и** , **или или** открывающий и закрывающий теги должны включать по крайней мере один дочерний узел.</span><span class="sxs-lookup"><span data-stu-id="4126b-131">Each pair of **and** and **or** opening and closing tags must include at least one or more child nodes.</span></span>
-   <span data-ttu-id="4126b-132">В этой схеме не допускается использование нулевого набора элементов.</span><span class="sxs-lookup"><span data-stu-id="4126b-132">A zero set of elements is not allowed in this schema.</span></span>

## <a name="record-attributes"></a><span data-ttu-id="4126b-133">Атрибуты записи</span><span class="sxs-lookup"><span data-stu-id="4126b-133">Record Attributes</span></span>

<span data-ttu-id="4126b-134">С помощью [схемы атрибута записи](record-attribute-schema.md)пользователь может создавать атрибуты записи, которые определяются атрибутом **attrib** XML в элементе предложения.</span><span class="sxs-lookup"><span data-stu-id="4126b-134">By using the [Record Attribute Schema](record-attribute-schema.md), a user can create record attributes that the **attrib** XML attribute in a clause element specifies.</span></span> <span data-ttu-id="4126b-135">Атрибуты для новой записи добавляются путем установки **псзаттрибутес** элемента [**одноранговой \_ записи**](/windows/desktop/api/P2P/ns-p2p-peer_record) в XML-строку с использованием формата, указанного в схеме.</span><span class="sxs-lookup"><span data-stu-id="4126b-135">Attributes for a new record are added by setting the **pszAttributes** member of [**PEER\_RECORD**](/windows/desktop/api/P2P/ns-p2p-peer_record) to an XML string using the format specified in the schema.</span></span>

<span data-ttu-id="4126b-136">Одноранговая инфраструктура резервирует следующие имена атрибутов:</span><span class="sxs-lookup"><span data-stu-id="4126b-136">The Peer Infrastructure reserves the following attribute names:</span></span>

-   <span data-ttu-id="4126b-137">**пирластмодифиедби**</span><span class="sxs-lookup"><span data-stu-id="4126b-137">**peerlastmodifiedby**</span></span>
-   <span data-ttu-id="4126b-138">**пиркреаторид**</span><span class="sxs-lookup"><span data-stu-id="4126b-138">**peercreatorid**</span></span>
-   <span data-ttu-id="4126b-139">**пирластмодификатионтиме**</span><span class="sxs-lookup"><span data-stu-id="4126b-139">**peerlastmodificationtime**</span></span>
-   <span data-ttu-id="4126b-140">**пиррекордид**</span><span class="sxs-lookup"><span data-stu-id="4126b-140">**peerrecordid**</span></span>
-   <span data-ttu-id="4126b-141">**пиррекордтипе**</span><span class="sxs-lookup"><span data-stu-id="4126b-141">**peerrecordtype**</span></span>
-   <span data-ttu-id="4126b-142">**пиркреатионтиме**</span><span class="sxs-lookup"><span data-stu-id="4126b-142">**peercreationtime**</span></span>
-   <span data-ttu-id="4126b-143">**пирластмодификатионтиме**</span><span class="sxs-lookup"><span data-stu-id="4126b-143">**peerlastmodificationtime**</span></span>

## <a name="special-characters"></a><span data-ttu-id="4126b-144">Специальные символы</span><span class="sxs-lookup"><span data-stu-id="4126b-144">Special Characters</span></span>

<span data-ttu-id="4126b-145">Некоторые символы могут использоваться для выражения совпадающих шаблонов или для экранирования других специальных символов.</span><span class="sxs-lookup"><span data-stu-id="4126b-145">Certain characters can be used to express matching patterns, or to escape other special characters.</span></span> <span data-ttu-id="4126b-146">Эти символы описаны в таблице ниже.</span><span class="sxs-lookup"><span data-stu-id="4126b-146">These characters are described in the table below.</span></span> 

| <span data-ttu-id="4126b-147">Шаблон символов</span><span class="sxs-lookup"><span data-stu-id="4126b-147">Character pattern</span></span> | <span data-ttu-id="4126b-148">Описание</span><span class="sxs-lookup"><span data-stu-id="4126b-148">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                             |
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \*                | <span data-ttu-id="4126b-149">Подстановочный знак.</span><span class="sxs-lookup"><span data-stu-id="4126b-149">The wildcard character.</span></span> <span data-ttu-id="4126b-150">Если этот символ встречается в значении предложения, он соответствует 0-n символам любого значения, включая пробелы и символы, отличные от буквенно-цифровых.</span><span class="sxs-lookup"><span data-stu-id="4126b-150">When this character is encountered in a clause value, it matches 0-n characters of any value, including whitespace and nonalphanumeric characters.</span></span> <span data-ttu-id="4126b-151">Пример:</span><span class="sxs-lookup"><span data-stu-id="4126b-151">For example:</span></span><br/> <span data-ttu-id="4126b-152">"<clause attrib="peercreatorid" type="string" compare="equal">Джеймс P \* </clause>"</span><span class="sxs-lookup"><span data-stu-id="4126b-152">"<clause attrib="peercreatorid" type="string" compare="equal">James P\*</clause>"</span></span><br/> <span data-ttu-id="4126b-153">Это предложение сопоставляет все значения **пиркреаторид** с именем «Джеймс» и фамилией, начинающейся с «P».</span><span class="sxs-lookup"><span data-stu-id="4126b-153">This clause matches all **peercreatorid** values with a first name of "James" and a last name starting with "P".</span></span><br/> |
| \\\*              | <span data-ttu-id="4126b-154">Экранированная звездочка.</span><span class="sxs-lookup"><span data-stu-id="4126b-154">An escaped asterisk.</span></span> <span data-ttu-id="4126b-155">Эта последовательность соответствует символу звездочки.</span><span class="sxs-lookup"><span data-stu-id="4126b-155">This sequence matches an asterisk character.</span></span>                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="4126b-156">?</span><span class="sxs-lookup"><span data-stu-id="4126b-156">?</span></span>                 | <span data-ttu-id="4126b-157">Односимвольный подстановочный знак.</span><span class="sxs-lookup"><span data-stu-id="4126b-157">The single-character wildcard character.</span></span> <span data-ttu-id="4126b-158">Если этот символ встречается в значении предложения, он соответствует любому отдельному символу, включая пробелы и символы, отличные от буквенно-цифровых. Например:</span><span class="sxs-lookup"><span data-stu-id="4126b-158">When this character is encountered in a clause value, it matches any single character, including whitespace and nonalphanumeric characters.For example:</span></span><br/> <span data-ttu-id="4126b-159">"<clause attrib="filename" type="string" compare="equal">Data-0?. XML</clause>"</span><span class="sxs-lookup"><span data-stu-id="4126b-159">"<clause attrib="filename" type="string" compare="equal">data-0?.xml</clause>"</span></span><br/> <span data-ttu-id="4126b-160">Это предложение соответствует значениям **filename** , таким как "data-01.xml" и "data-0B.xml".</span><span class="sxs-lookup"><span data-stu-id="4126b-160">This clause matches **filename** values like "data-01.xml" and "data-0B.xml".</span></span><br/>                              |
| <span data-ttu-id="4126b-161">\\?</span><span class="sxs-lookup"><span data-stu-id="4126b-161">\\?</span></span>               | <span data-ttu-id="4126b-162">Escape-знак вопроса.</span><span class="sxs-lookup"><span data-stu-id="4126b-162">An escaped question mark.</span></span> <span data-ttu-id="4126b-163">Эта последовательность соответствует символу вопросительного знака.</span><span class="sxs-lookup"><span data-stu-id="4126b-163">This sequence matches a question mark character.</span></span>                                                                                                                                                                                                                                                                                                                                                              |
| \\\\              | <span data-ttu-id="4126b-164">Экранированная обратная косая черта.</span><span class="sxs-lookup"><span data-stu-id="4126b-164">An escaped backslash.</span></span> <span data-ttu-id="4126b-165">Эта последовательность соответствует одному символу обратной косой черты.</span><span class="sxs-lookup"><span data-stu-id="4126b-165">This sequence matches a single backslash character.</span></span>                                                                                                                                                                                                                                                                                                                                                               |



 

<span data-ttu-id="4126b-166">Если последовательность символов недопустима, функция [**пирграупсеарчрекордс**](/windows/desktop/api/P2P/nf-p2p-peergroupsearchrecords) возвращает ошибку **E \_ INVALIDARG**.</span><span class="sxs-lookup"><span data-stu-id="4126b-166">If the character sequence is not valid, the [**PeerGroupSearchRecords**](/windows/desktop/api/P2P/nf-p2p-peergroupsearchrecords) function returns the error **E\_INVALIDARG**.</span></span> <span data-ttu-id="4126b-167">Недопустимая последовательность — любая последовательность, содержащая символ " \\ " (обратная косая черта), за которым не следует сразу \* символ "" (звездочка), знак "?" (вопросительный знак) или другой символ " \\ " (обратная косая черта).</span><span class="sxs-lookup"><span data-stu-id="4126b-167">An invalid sequence is any sequence that contains a "\\" (backslash) character not immediately followed by either an "\*" (asterisk) character, a "?" (question mark) character, or another "\\" (backslash) character.</span></span>

 

 




