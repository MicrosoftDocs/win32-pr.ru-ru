---
description: ССЫЛКИ на инструкцию получают все экземпляры связей, ссылающиеся на конкретный экземпляр источника.
ms.assetid: 674be546-e7fd-4150-9d7c-2888d24bf1b3
ms.tgt_platform: multiple
title: ССЫЛКИ на оператор
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1c7cc624a1e91220fc6bfc89ef0a75878a9cfb1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105647259"
---
# <a name="references-of-statement"></a><span data-ttu-id="9c3ac-103">ССЫЛКИ на оператор</span><span class="sxs-lookup"><span data-stu-id="9c3ac-103">REFERENCES OF Statement</span></span>

<span data-ttu-id="9c3ac-104">ССЫЛКИ на инструкцию получают все экземпляры связей, ссылающиеся на конкретный экземпляр источника.</span><span class="sxs-lookup"><span data-stu-id="9c3ac-104">The REFERENCES OF statement retrieves all association instances that refer to a particular source instance.</span></span> <span data-ttu-id="9c3ac-105">ССЫЛКИ оператора похожи на СОЕДИНИТЕЛи оператора в своем синтаксисе.</span><span class="sxs-lookup"><span data-stu-id="9c3ac-105">The REFERENCES OF statement is similar to the ASSOCIATORS OF statement in its syntax.</span></span> <span data-ttu-id="9c3ac-106">Однако вместо того, чтобы извлекать экземпляры конечной точки, он получает промежуточные экземпляры взаимосвязей.</span><span class="sxs-lookup"><span data-stu-id="9c3ac-106">However, rather than retrieving endpoint instances, it retrieves the intervening association instances.</span></span>

<span data-ttu-id="9c3ac-107">ССЫЛКИ предложения WHERE могут включать одно или несколько из следующих стандартных ключевых слов и их значений.</span><span class="sxs-lookup"><span data-stu-id="9c3ac-107">The REFERENCES OF WHERE clause can include one or more of the following predefined keywords and their values:</span></span>


```sql
REFERENCES OF {SourceObject} WHERE 
    ClassDefsOnly
    RequiredQualifier = QualifierName
    ResultClass = ClassName
    Role = PropertyName
```



<span data-ttu-id="9c3ac-108">Чтобы указать исходный объект, используйте любой допустимый путь к объекту для объект SourceObject.</span><span class="sxs-lookup"><span data-stu-id="9c3ac-108">To specify a source object, use any valid object path for SourceObject.</span></span> <span data-ttu-id="9c3ac-109">Как и в случае с инструкцией SELECT, предложение WHERE является необязательным и используется для дальнейшего определения запроса.</span><span class="sxs-lookup"><span data-stu-id="9c3ac-109">As with the SELECT statement, the WHERE clause is optional and is used to further define the query.</span></span> <span data-ttu-id="9c3ac-110">Таким образом, следующая инструкция вполне допустима:</span><span class="sxs-lookup"><span data-stu-id="9c3ac-110">That is, the following statement is perfectly valid:</span></span>


```sql
REFERENCES OF {Adapter="AHA-294X"}
```



<span data-ttu-id="9c3ac-111">Ключевое слово **классдефсонли** указывает, что инструкция возвращает результирующий набор объектов определения класса, а не фактических экземпляров классов взаимосвязей.</span><span class="sxs-lookup"><span data-stu-id="9c3ac-111">The **ClassDefsOnly** keyword indicates that the statement returns a result set of class definition objects rather than actual instances of the association classes.</span></span> <span data-ttu-id="9c3ac-112">Эти объекты содержат определения классов, к которым принадлежат экземпляры, ссылающиеся на исходный объект.</span><span class="sxs-lookup"><span data-stu-id="9c3ac-112">These objects contain definitions of classes to which the instances that reference the source object belong.</span></span> <span data-ttu-id="9c3ac-113">Например, следующая инструкция возвращает определения для классов **адаптердривер** и **адаптерпротокол** :</span><span class="sxs-lookup"><span data-stu-id="9c3ac-113">For example, the following statement returns definitions for the **AdapterDriver** and **AdapterProtocol** classes:</span></span>


```sql
REFERENCES OF {Adapter="AHA-294X"} WHERE ClassDefsOnly
```



<span data-ttu-id="9c3ac-114">Ключевое слово **рекуиредкуалифиер** указывает, что возвращаемые объекты связи должны включать указанный квалификатор.</span><span class="sxs-lookup"><span data-stu-id="9c3ac-114">The **RequiredQualifier** keyword indicates that the returned association objects must include the specified qualifier.</span></span> <span data-ttu-id="9c3ac-115">Ключевое слово **рекуиредкуалифиер** можно использовать для включения определенных экземпляров ассоциаций в результирующий набор.</span><span class="sxs-lookup"><span data-stu-id="9c3ac-115">The **RequiredQualifier** keyword can be used to include particular instances of associations in the result set.</span></span> <span data-ttu-id="9c3ac-116">Например, следующая инструкция возвращает экземпляры ассоциаций, которые включают квалификатор с именем **адаптертаг**:</span><span class="sxs-lookup"><span data-stu-id="9c3ac-116">For example, the following statement returns association instances that include a qualifier called **AdapterTag**:</span></span>


```sql
REFERENCES OF {Adapter="AHA-294X"}  WHERE RequiredQualifier = AdapterTag
```



<span data-ttu-id="9c3ac-117">Ключевое слово **ресулткласс** указывает, что возвращаемые объекты связи должны принадлежать или быть производными от указанного класса.</span><span class="sxs-lookup"><span data-stu-id="9c3ac-117">The **ResultClass** keyword indicates that the returned association objects must belong to or be derived from the specified class.</span></span> <span data-ttu-id="9c3ac-118">Например, следующая инструкция возвращает ассоциации класса **адаптердривер** или подклассов **адаптердривер**:</span><span class="sxs-lookup"><span data-stu-id="9c3ac-118">For example, the following statement returns associations of the **AdapterDriver** class or subclasses of **AdapterDriver**:</span></span>


```sql
REFERENCES OF {Adapter="AHA-294X"} WHERE ResultClass = AdapterDriver
```



<span data-ttu-id="9c3ac-119">Ключевые слова **классдефсонли** и **ресулткласс** являются взаимоисключающими.</span><span class="sxs-lookup"><span data-stu-id="9c3ac-119">The **ClassDefsOnly** and **ResultClass** keywords are mutually exclusive.</span></span> <span data-ttu-id="9c3ac-120">Их использование вместе приводит к ошибке недопустимого запроса.</span><span class="sxs-lookup"><span data-stu-id="9c3ac-120">Using them together causes an invalid query error.</span></span>

<span data-ttu-id="9c3ac-121">Ключевое слово **Role** указывает, что возвращенные связи являются только теми, в которых исходный объект играет определенную роль.</span><span class="sxs-lookup"><span data-stu-id="9c3ac-121">The **Role** keyword indicates that the returned associations are only those in which the source object plays a particular role.</span></span> <span data-ttu-id="9c3ac-122">Роль определяется указанным свойством, ссылочным свойством типа [ref](references.md). Ключевое слово **Role** полезно в ассоциациях, где определенный объект может играть одну роль в некоторых случаях, а другую — в других — например, в иерархических ассоциациях.</span><span class="sxs-lookup"><span data-stu-id="9c3ac-122">The role is defined by the specified property, a reference property of type [ref](references.md). The **Role** keyword is useful in associations where a certain object can play one role in some cases and another role in others, such as in hierarchical associations.</span></span> <span data-ttu-id="9c3ac-123">Ключевое слово **Role** можно использовать для получения всех связей, в которых исходный объект играет роль родителя, например.</span><span class="sxs-lookup"><span data-stu-id="9c3ac-123">The **Role** keyword can be used to retrieve all of the associations in which the source object plays the role of parent, for example.</span></span> <span data-ttu-id="9c3ac-124">Следующая инструкция иллюстрирует синтаксис для получения ассоциаций, имеющих **родительское** свойство, ссылающееся на исходный объект в качестве родителя:</span><span class="sxs-lookup"><span data-stu-id="9c3ac-124">The following statement illustrates the syntax for retrieving associations that have a **parent** property referencing the source object as the parent:</span></span>


```sql
REFERENCES OF {Adapter="AHA-294X"} WHERE Role = parent
```



> [!Note]  
> <span data-ttu-id="9c3ac-125">Сложные запросы не могут использовать "and" или "or" для разделения ключевых слов для СОЕДИНИТЕЛей и ссылок на инструкции.</span><span class="sxs-lookup"><span data-stu-id="9c3ac-125">Complex queries cannot use "And" or "Or" to separate keywords for ASSOCIATORS OF and REFERENCES OF statements.</span></span> <span data-ttu-id="9c3ac-126">Более того, знак равенства является единственным допустимым оператором, который можно использовать с ключевыми словами в этих запросах.</span><span class="sxs-lookup"><span data-stu-id="9c3ac-126">Furthermore, the equal sign is the only valid operator that can be used with the keywords in these queries.</span></span> <span data-ttu-id="9c3ac-127">Например, допустим следующий запрос:</span><span class="sxs-lookup"><span data-stu-id="9c3ac-127">For example, the following query is valid:</span></span>

 


```sql
"REFERENCES OF {Win32_NetworkAdapter.DeviceID="0"} " +
    "WHERE resultclass = Win32_NetworkAdapterSetting " +
    "requiredQualifier = Dynamic"
```



> [!Note]  
> <span data-ttu-id="9c3ac-128">Следующие примеры недопустимы.</span><span class="sxs-lookup"><span data-stu-id="9c3ac-128">The next examples are not valid.</span></span> <span data-ttu-id="9c3ac-129">В первом примере не используется знак равенства, а во втором примере по ошибке предпринимается попытка использовать ключевое слово **и** .</span><span class="sxs-lookup"><span data-stu-id="9c3ac-129">The first example does not use the equal sign and the second example erroneously attempts to use the **AND** keyword:</span></span>

 


```sql
"REFERENCES OF {Win32_NetworkAdapter.DeviceID="0"} " +
    "WHERE resultclass = Win32_NetworkAdapterSetting " +
    "requiredQualifier <> Dynamic"

"REFERENCES OF {Win32_NetworkAdapter.DeviceID="0"} " +
"WHERE resultclass = Win32_NetworkAdapterSetting " +
"AND requiredQualifier = Dynamic"
```



 

 



