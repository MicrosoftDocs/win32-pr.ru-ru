---
description: 'В запросах сопоставления схем используются те же инструкции, что и в запросах ассоциаций данных: СОЕДИНИТЕЛи и ссылки.'
ms.assetid: b5fc2d86-702a-42cd-82e6-f15c905ba6aa
ms.tgt_platform: multiple
title: Сопоставления схем
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea2f0c3b753bf4657c66a635319bab7dbe435a3b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272219"
---
# <a name="schema-associations"></a><span data-ttu-id="4cc49-103">Сопоставления схем</span><span class="sxs-lookup"><span data-stu-id="4cc49-103">Schema Associations</span></span>

<span data-ttu-id="4cc49-104">В запросах сопоставления схем используются те же инструкции, что и в запросах ассоциаций данных: СОЕДИНИТЕЛи и ссылки.</span><span class="sxs-lookup"><span data-stu-id="4cc49-104">Schema association queries use the same statements as are used in data association queries: ASSOCIATORS OF and REFERENCES OF.</span></span> <span data-ttu-id="4cc49-105">Однако при использовании запросов ассоциаций данных возвращаются экземпляры классов, а с запросами связей схем — имена классов, которые могут участвовать в отношениях взаимосвязей.</span><span class="sxs-lookup"><span data-stu-id="4cc49-105">However, with data association queries, class instances are returned, and with schema association queries, names of classes that can participate in association relationships are returned.</span></span> <span data-ttu-id="4cc49-106">Например, можно использовать запрос схемы для поиска всех классов взаимосвязей, определенных в схеме, ссылающейся на исходный класс.</span><span class="sxs-lookup"><span data-stu-id="4cc49-106">For example, use a schema query to find all of the association classes defined in the schema that reference a source class.</span></span>

<span data-ttu-id="4cc49-107">Синтаксис для СОЕДИНИТЕЛей и ссылок на инструкции одинаков для запросов связи схемы, так как он предназначен для запросов ассоциаций данных со следующими исключениями:</span><span class="sxs-lookup"><span data-stu-id="4cc49-107">The syntax for the ASSOCIATORS OF and REFERENCES OF statements is the same for schema association queries as it is for data association queries with the following exceptions:</span></span>

-   <span data-ttu-id="4cc49-108">Исходный объект является классом, а не экземпляром.</span><span class="sxs-lookup"><span data-stu-id="4cc49-108">The source object is a class rather than an instance.</span></span>
-   <span data-ttu-id="4cc49-109">Существует дополнительное ключевое слово **SchemaOnly**, которое определяет запрос как применяемый к схеме, а не к данным.</span><span class="sxs-lookup"><span data-stu-id="4cc49-109">There is an additional keyword, **SchemaOnly**, which identifies the query as applying to a schema rather than to data.</span></span>
-   <span data-ttu-id="4cc49-110">Недопустимое ключевое слово **классдефсонли** .</span><span class="sxs-lookup"><span data-stu-id="4cc49-110">The **ClassDefsOnly** keyword is not valid.</span></span>

<span data-ttu-id="4cc49-111">В следующем примере показан полный синтаксис СОЕДИНИТЕЛей оператора для запроса схемы.</span><span class="sxs-lookup"><span data-stu-id="4cc49-111">The following example shows the complete syntax of the ASSOCIATORS OF statement for a schema query.</span></span> <span data-ttu-id="4cc49-112">Подробный синтаксис см. в разделе [соединители оператора](associators-of-statement.md).</span><span class="sxs-lookup"><span data-stu-id="4cc49-112">For detailed syntax, see [ASSOCIATORS OF Statement](associators-of-statement.md).</span></span>


```sql
ASSOCIATORS OF {SourceClass} WHERE 
    AssocClass = AssocClassName
    RequiredAssocQualifier = QualifierName
    RequiredQualifier = QualifierName
    ResultClass = ClassName
    ResultRole = PropertyName
    Role = PropertyName
    SchemaOnly
```



<span data-ttu-id="4cc49-113">В следующем примере показан запрос, возвращающий классы **протокола** и **драйвера** , два класса, которые ссылаются на исходный класс.</span><span class="sxs-lookup"><span data-stu-id="4cc49-113">The following example shows a query that returns the **Protocol** and **Driver** classes, the two classes that refer to the source class.</span></span>


```sql
ASSOCIATORS OF {Adapter} WHERE SchemaOnly
```



<span data-ttu-id="4cc49-114">Следующий запрос возвращает только класс **Driver** из-за ограничения, накладываемого ключевым словом **ассоккласс** .</span><span class="sxs-lookup"><span data-stu-id="4cc49-114">The following query returns only the **Driver** class because of the restriction placed by the **AssocClass** keyword.</span></span>


```sql
ASSOCIATORS OF {Adapter} WHERE AssocClass = AdapterDriver SchemaOnly
```



<span data-ttu-id="4cc49-115">Полный синтаксис ссылок на инструкцию для запроса схемы выглядит следующим образом.</span><span class="sxs-lookup"><span data-stu-id="4cc49-115">The complete syntax of the REFERENCES OF statement for a schema query is as follows.</span></span> <span data-ttu-id="4cc49-116">Подробный синтаксис см. в разделе [ссылки на инструкцию](references-of-statement.md).</span><span class="sxs-lookup"><span data-stu-id="4cc49-116">For detailed syntax, see [REFERENCES OF Statement](references-of-statement.md).</span></span>


```sql
REFERENCES OF {SourceClass} WHERE
    ResultClass = ClassName
    Role = PropertyName
    RequiredQualifier = QualifierName
    SchemaOnly
```



> [!Note]  
> <span data-ttu-id="4cc49-117">Запросы связей схем могут возвращать дубликаты объектов.</span><span class="sxs-lookup"><span data-stu-id="4cc49-117">Schema association queries may return duplicate objects.</span></span>

 

<span data-ttu-id="4cc49-118">Например, следующий запрос будет возвращать класс [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) несколько раз при перечислении классов в **корневом пространстве имен \\ CIMV2** .</span><span class="sxs-lookup"><span data-stu-id="4cc49-118">For example, the following query will return the class [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) several times when enumerating classes in the **root\\cimv2** namespace.</span></span>


```sql
ASSOCIATORS OF {Win32_ComputerSystem} WHERE SchemaOnly
```



 

 
