---
description: Используйте предложение WHERE, чтобы ограничить область запроса данных, события или схемы.
ms.assetid: b275f8e0-773d-422c-be21-b427e7a1fb6b
ms.tgt_platform: multiple
title: Предложение WHERE (WMI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a72e68d8266b72f6e41e17c0b85766b7a58bb197
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703249"
---
# <a name="where-clause-wmi"></a>Предложение WHERE (WMI)

Используйте предложение WHERE, чтобы ограничить область запроса данных, события или схемы. Дополнительные сведения см. [в разделе запросы с помощью WQL](querying-with-wql.md). Предложение WHERE состоит из свойства или ключевого слова, оператора и константы. Все предложения WHERE должны указывать один из предопределенных операторов, которые включены в инструментарий управления Windows (WMI) (WQL) Language. К инструкции SELECT можно добавить предложение WHERE, используя одну из следующих форм:


```sql
SELECT * FROM class WHERE property operator constant
SELECT * FROM class WHERE constant operator property
```



где \* — запрашивается элемент, класс — это класс, в котором следует запрашивать, а константа, оператор и свойство — константа, оператор, свойство или ключевое слово для использования. Дополнительные сведения об инструкции SELECT см. в статьях [инструкция SELECT для запросов данных](select-statement-for-data-queries.md), [инструкция SELECT для запросов событий](select-statement-for-event-queries.md)или [инструкция SELECT для запросов схемы](select-statement-for-schema-queries.md).

Значение константы должно иметь правильный тип для свойства. Более того, оператор должен быть в списке допустимых [операторов WQL](wql-operators.md). Либо имя свойства, либо константа должны присутствовать в обеих сторонах оператора в предложении WHERE.

В предложении WHERE можно использовать строковые литералы, например "NTFS". Если вы хотите включить в строку следующие специальные символы, необходимо сначала выполнить escape-последовательность символа, добавив обратную косую черту ( \) :

-   знака\\\)
-   двойные кавычки ( \\ ")
-   одинарные кавычки ( \\ ')

Нельзя использовать произвольные арифметические выражения. Например, следующий запрос возвращает только экземпляры класса [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) , представляющие диски NTFS:


```sql
SELECT * FROM Win32_LogicalDisk WHERE FileSystem = "NTFS"
```



Имена свойств не могут присутствовать на обеих сторонах оператора. Следующий запрос является примером недопустимого запроса:


```sql
SELECT * FROM PhysicalDisk WHERE Partitions < (4 + 7 - 2) 
    OR   (Partitions = SectorsPerTrack / 7)
```



Для большинства случаев использования дескрипторов классов в предложении WHERE WMI помечает запрос как недопустимый и возвращает ошибку. Однако используйте оператор dot (.) для свойств типа **Object** в WMI. Например, следующий запрос допустим, если свойство prop является допустимым свойством MyClass и имеет тип **Object**:

``` syntax
SELECT * FROM MyClass WHERE Prop.embedprop = 5
```

В тестах сравнения всегда учитывается регистр. То есть следующие три оператора имеют **значение true**:


```sql
SELECT * FROM MyClass WHERE Prop1 = "cat"
SELECT * FROM MyClass WHERE Prop1 = "CAT"
SELECT * FROM MyClass WHERE Prop1 = "cAt"
```



Можно создать запрос, включающий логические типы данных, но единственными допустимыми типами логических операндов являются типы =,! = и <> . Значение **true** эквивалентно числу 1, а значение **false** эквивалентно числу 0. Следующие примеры представляют собой запросы, которые сравнивают логическое значение со значениями **true** или **false**.


```sql
SELECT * FROM MyClass WHERE BoolProp = 1
SELECT * FROM MyClass WHERE BoolProp = TRUE
SELECT * FROM MyClass WHERE BoolProp <> FALSE
SELECT * FROM MyClass WHERE BoolProp = 0
SELECT * FROM MyClass WHERE BoolProp = FALSE
SELECT * FROM MyClass WHERE BoolProp != 1
SELECT * FROM MyClass WHERE BoolProp != FALSE
SELECT * FROM MyClass WHERE BoolProp <> FALSE
```



Следующие примеры имеют недопустимые запросы, пытающиеся использовать недопустимые операнды.


```sql
SELECT * FROM MyClass WHERE BoolProp <= TRUE
SELECT * FROM MyClass WHERE BoolProp >= 0
SELECT * FROM MyClass WHERE BoolProp > FALSE
SELECT * FROM win32_computersystem WHERE infraredsupported >= null
```



Несколько групп свойств, операторов и констант можно комбинировать в предложении WHERE с помощью логических операторов и вложенных выражений в скобках. Каждая группа должна быть соединена с [операторами](wql-operators.md) and, or или not, как показано в следующих запросах. Первый запрос получает все экземпляры класса [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) , для свойства **Name** которых задано значение C или D:


```sql
SELECT * FROM Win32_LogicalDisk WHERE Name = "C:" OR Name = "D:"
```



Второй запрос извлекает диски с именем "C:" или "D:" только в том случае, если они имеют определенный объем свободного места и имеют файловые системы NTFS:


```sql
SELECT * FROM Win32_LogicalDisk WHERE (Name = "C:" OR Name = "D:") 
    AND  FreeSpace > 2000000  AND   FileSystem = "NTFS"
```



В этом примере показан запрос схемы с помощью предложения WHERE.


```sql
SELECT * FROM meta_class WHERE __this ISA "myClassName"
```



Класс meta класса \_ определяет это как запрос схемы, свойство, именуемое, \_ \_ определяет целевой класс запроса, а [оператор ISA](isa-operator-for-schema-queries.md) запрашивает определения для подклассов целевого класса. Таким образом, предыдущий запрос возвращает определение класса Микласснаме и определения для всех его подклассов.

В следующем примере показан запрос данных с помощью [соединителей оператора с предложением](associators-of-statement.md) WHERE:


```sql
ASSOCIATORS OF {myClass.keyVal="Value1"} WHERE ClassDefsOnly
```



В следующем примере показан запрос схемы, использующий СОЕДИНИТЕЛи и где:


```sql
ASSOCIATORS OF {myClass} WHERE SchemaOnly
```



Следующий пример представляет собой запрос данных, использующий [ссылки на инструкцию](references-of-statement.md) и где:


```sql
REFERENCES OF {myClass.keyVal="Value1"} 
    WHERE RequiredQualifier = myQual
```



Последний пример — запрос схемы, в котором используются ссылки и где:


```sql
REFERENCES OF {myClass} WHERE SchemaOnly
```



Помимо формата [DateTime](date-and-time-format.md) WMI, предложение WHERE языка WQL поддерживает несколько других форматов даты и времени:

-   [Форматы даты, поддерживаемые WQL](wql-supported-date-formats.md)
-   [Поддерживаемые форматы времени WQL](wql-supported-time-formats.md)

 

 
