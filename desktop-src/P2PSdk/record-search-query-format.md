---
description: Вызов функции Пирграупсеарчрекордс требует наличия параметра строки запроса XML, который используется для определения основных критериев поиска.
ms.assetid: 2c5ab425-6959-418a-8d9a-c8155257fc7e
title: Формат запроса поиска записей
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f26a130d937177d4f903bfe52b121b2d67f8720d
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122887010"
---
# <a name="record-search-query-format"></a>Формат запроса поиска записей

Вызов функции [**пирграупсеарчрекордс**](/windows/desktop/api/P2P/nf-p2p-peergroupsearchrecords) требует наличия параметра строки запроса XML, который используется для определения основных критериев поиска. Используйте следующую схему для формирования XML-строки:

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

### <a name="elements-to-use-for-a-record-search"></a>Элементы, используемые для поиска записей

Первичный элемент в поиске записей — **пирсеарч**, который содержит универсальный код ресурса (URI) связанной схемы в атрибуте **xmlns** . Если **пирсеарч** используется как дочерний элемент, можно использовать предложения **and**,  **and и в качестве дочерних** элементов.

-   **и** — элемент **and** выполняет логическую операцию AND над одним или несколькими предложениями, содержащимися между открывающим и закрывающим тегами. Другие теги **and** и **or** могут быть дочерними, а рекурсивные результаты их дочерних предложений включаются в операцию.

    Например, если вы хотите получить запись, содержащую имя, равное Джеймс Петерс, и Последнее обновление, которое больше 2/28/2003, или дату создания меньше 1/31/2003, используйте следующую строку запроса XML:

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

-   **— элемент** **предложения** указывает базовое правило сравнения, которое сравнивает значение определенного атрибута записи со значением, содержащимся между открывающим и закрывающим тегами. Необходимо указать атрибуты **Type** и **Compare** , чтобы **определить,** какая операция сравнения должна быть выполнена. Например, простой поиск, указывающий все совпадающие записи, должен иметь значение **пиркреаторид** , равное Джеймс Петерс, отображается в строке запроса XML следующим образом:

    ``` syntax
    <?xml version="1.0" encoding="utf-8" ?> 
    <peersearch xmlns:xs="https://www.w3.org/2001/XMLSchema">
       <clause attrib="peercreatorid" type="string" compare="equal">James Peters</clause>
    </peersearch>
    ```

    К общим атрибутам **типа** относятся **int**, **String** и **Date**. Атрибут **Date** может быть одним из стандартных форматов даты, описанных в разделе [https://www.w3.org/TR/NOTE-datetime](https://www.w3.org/TR/NOTE-datetime) .

    Значения для атрибута **Compare** **равны**, **NotEqual**, **less**, **больше**, **лессорекуал** и **греатерорекуал**.

<!-- -->

-   **или** -элемент **or** выполняет логическую операцию OR с одним или несколькими предложениями, содержащимися между открывающим и закрывающим тегами. Другие  элементы or **и and могут** быть дочерними, а рекурсивные результаты дочерних предложений включаются в операцию. Например, если вы хотите получить запись, содержащую имя, равное Джеймс Петерс, или Последнее обновление в диапазоне от 1/31/2003 до 2/28/2003, используйте следующую строку запроса XML:

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

## <a name="more-information-about-a-record-search"></a>Дополнительные сведения о поиске записей

Первый уровень узлов после **пирсеарч** может иметь только один элемент. Однако последующие дочерние элементы этого элемента могут иметь множество элементов на одном уровне.

Следующий поисковый запрос неверен:

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

Запрос завершается ошибкой, так как для соответствия возвращаются два значения без разрешения в одно значение true/false. Это означает, что одно предложение является запросом имени записи, равной Джеймс Петерс, а операция и соответствует двум предложениям компонентов. Результат — два логических значения true/false, которые являются противоречивыми.

Чтобы получить все записи, содержащие имя, равное Джеймс Петерс, и Последнее обновление, которое находится в диапазоне от 1/31/2003 до 2/28/2003,  поместите предложение **и теги,** находящееся на том же уровне между открывающим и закрывающим тегами **и** . В следующем примере показан успешный запрос:

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

В следующем списке приведены другие сведения, которые необходимо учитывать для написания успешного запроса.

-   Теги **and** и **or** не могут располагаться между открывающими и закрывающими тегами **предложения** , так как в такой конфигурации они обрабатываются как часть значения для сопоставления, что приводит к ошибке или неудачному совпадению.
-   Каждая пара **и** , **или или** открывающий и закрывающий теги должны включать по крайней мере один дочерний узел.
-   В этой схеме не допускается использование нулевого набора элементов.

## <a name="record-attributes"></a>Атрибуты записи

С помощью [схемы атрибута записи](record-attribute-schema.md)пользователь может создавать атрибуты записи, которые определяются атрибутом **attrib** XML в элементе предложения. Атрибуты для новой записи добавляются путем установки **псзаттрибутес** элемента [**одноранговой \_ записи**](/windows/desktop/api/P2P/ns-p2p-peer_record) в XML-строку с использованием формата, указанного в схеме.

Одноранговая инфраструктура резервирует следующие имена атрибутов:

-   **пирластмодифиедби**
-   **пиркреаторид**
-   **пирластмодификатионтиме**
-   **пиррекордид**
-   **пиррекордтипе**
-   **пиркреатионтиме**
-   **пирластмодификатионтиме**

## <a name="special-characters"></a>Специальные символы

Некоторые символы могут использоваться для выражения совпадающих шаблонов или для экранирования других специальных символов. Эти символы описаны в таблице ниже. 

| Шаблон символов | Описание                                                                                                                                                                                                                                                                                                                                                                                                                             |
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \*                | Подстановочный знак. Если этот символ встречается в значении предложения, он соответствует 0-n символам любого значения, включая пробелы и символы, отличные от буквенно-цифровых. Пример.<br/> " <clause attrib="peercreatorid" type="string" compare="equal"> Джеймс P \* &lt; /Клаусе &gt; "<br/> Это предложение сопоставляет все значения **пиркреаторид** с именем «Джеймс» и фамилией, начинающейся с «P».<br/> |
| \\\*              | Экранированная звездочка. Эта последовательность соответствует символу звездочки.                                                                                                                                                                                                                                                                                                                                                                       |
| ?                 | Односимвольный подстановочный знак. Если этот символ встречается в значении предложения, он соответствует любому отдельному символу, включая пробелы и символы, отличные от буквенно-цифровых. Например:<br/> " <clause attrib="filename" type="string" compare="equal"> Data-0? .xml&lt; /Клаусе &gt; "<br/> Это предложение соответствует значениям **filename** , таким как "data-01.xml" и "data-0B.xml".<br/>                              |
| \\?               | Escape-знак вопроса. Эта последовательность соответствует символу вопросительного знака.                                                                                                                                                                                                                                                                                                                                                              |
| \\\\              | Экранированная обратная косая черта. Эта последовательность соответствует одному символу обратной косой черты.                                                                                                                                                                                                                                                                                                                                                               |



 

Если последовательность символов недопустима, функция [**пирграупсеарчрекордс**](/windows/desktop/api/P2P/nf-p2p-peergroupsearchrecords) возвращает ошибку **E \_ INVALIDARG**. Недопустимая последовательность — любая последовательность, содержащая символ " \\ " (обратная косая черта), за которым не следует сразу \* символ "" (звездочка), знак "?" (вопросительный знак) или другой символ " \\ " (обратная косая черта).

 

 




