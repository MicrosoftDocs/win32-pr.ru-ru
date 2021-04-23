---
description: Описывает операторы WQL, используемые в предложении WHERE или инструкции SELECT.
ms.assetid: a62de66d-d5ba-49a1-8262-bfa10ac2db75
ms.tgt_platform: multiple
title: Операторы WQL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f5cc37d03884a3609abf3f76d2c78ba22b3c9f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712095"
---
# <a name="wql-operators"></a><span data-ttu-id="4b24a-103">Операторы WQL</span><span class="sxs-lookup"><span data-stu-id="4b24a-103">WQL Operators</span></span>

<span data-ttu-id="4b24a-104">Язык запросов инструментарий управления Windows (WMI) (WQL) поддерживает набор стандартных операторов, которые используются в [предложении WHERE](where-clause.md) инструкции SELECT, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="4b24a-104">The Windows Management Instrumentation Query Language (WQL) supports a set of standard operators that are used in the [WHERE clause](where-clause.md) of a SELECT statement, as follows.</span></span>



| <span data-ttu-id="4b24a-105">Оператор</span><span class="sxs-lookup"><span data-stu-id="4b24a-105">Operator</span></span>       | <span data-ttu-id="4b24a-106">Описание</span><span class="sxs-lookup"><span data-stu-id="4b24a-106">Description</span></span>              |
|----------------|--------------------------|
| =              | <span data-ttu-id="4b24a-107">Равно</span><span class="sxs-lookup"><span data-stu-id="4b24a-107">Equal to</span></span>                 |
| <           | <span data-ttu-id="4b24a-108">Меньше чем</span><span class="sxs-lookup"><span data-stu-id="4b24a-108">Less than</span></span>                |
| >           | <span data-ttu-id="4b24a-109">Больше чем</span><span class="sxs-lookup"><span data-stu-id="4b24a-109">Greater than</span></span>             |
| <=          | <span data-ttu-id="4b24a-110">Меньше или равно</span><span class="sxs-lookup"><span data-stu-id="4b24a-110">Less than or equal to</span></span>    |
| >=          | <span data-ttu-id="4b24a-111">Больше или равно</span><span class="sxs-lookup"><span data-stu-id="4b24a-111">Greater than or equal to</span></span> |
| <span data-ttu-id="4b24a-112">! = или <></span><span class="sxs-lookup"><span data-stu-id="4b24a-112">!= or <></span></span> | <span data-ttu-id="4b24a-113">Не равно</span><span class="sxs-lookup"><span data-stu-id="4b24a-113">Not equal to</span></span>             |



 

<span data-ttu-id="4b24a-114">Существует несколько дополнительных операторов, характерных для WQL: имеет значение, а не, ISA и LIKE.</span><span class="sxs-lookup"><span data-stu-id="4b24a-114">There are a few additional WQL-specific operators: IS, IS NOT, ISA, and LIKE.</span></span> <span data-ttu-id="4b24a-115">Операторы-и не являются допустимыми в предложении WHERE, только если константа имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="4b24a-115">The IS and IS NOT operators are valid in the WHERE clause only if the constant is **NULL**.</span></span> <span data-ttu-id="4b24a-116">Например, допустимы следующие запросы:</span><span class="sxs-lookup"><span data-stu-id="4b24a-116">For example, the following queries are valid:</span></span>


```sql
SELECT * FROM Win32_LogicalDisk WHERE FileSystem IS NULL
SELECT * FROM Win32_LogicalDisk WHERE FileSystem IS NOT NULL
```



<span data-ttu-id="4b24a-117">В следующих запросах показаны недопустимые варианты использования параметра имеет значение, а не значение.</span><span class="sxs-lookup"><span data-stu-id="4b24a-117">The following queries show invalid uses of IS and IS NOT:</span></span>


```sql
SELECT * FROM Win32_LogicalDisk WHERE DriveType IS 5
SELECT * FROM Win32_LogicalDisk WHERE FileSystem IS NOT "NTFS"
```



<span data-ttu-id="4b24a-118">Оператор ISA используется в предложении WHERE данных и запросов событий для тестирования внедренных объектов для иерархии классов.</span><span class="sxs-lookup"><span data-stu-id="4b24a-118">The ISA operator is used in the WHERE clause of data and event queries to test embedded objects for a class hierarchy.</span></span> <span data-ttu-id="4b24a-119">Оператор ISA устраняет необходимость отслеживания новых производных классов при запросе иерархии классов.</span><span class="sxs-lookup"><span data-stu-id="4b24a-119">The ISA operator eliminates the need for keeping track of newly derived classes when requesting a hierarchy of classes.</span></span> <span data-ttu-id="4b24a-120">При использовании ISA вновь созданные и существующие подклассы запрошенного класса автоматически включаются в результирующий набор.</span><span class="sxs-lookup"><span data-stu-id="4b24a-120">When you use ISA, newly created and existing subclasses of the requested class are automatically included in the result set.</span></span>

<span data-ttu-id="4b24a-121">Дополнительные сведения о синтаксисе и использовании этого оператора см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="4b24a-121">For more information about the syntax and use of this operator, see the following topics:</span></span>

-   [<span data-ttu-id="4b24a-122">Оператор ISA для запросов данных</span><span class="sxs-lookup"><span data-stu-id="4b24a-122">ISA Operator for Data Queries</span></span>](isa-operator-for-data-queries.md)
-   [<span data-ttu-id="4b24a-123">Оператор ISA для запросов событий</span><span class="sxs-lookup"><span data-stu-id="4b24a-123">ISA Operator for Event Queries</span></span>](isa-operator-for-event-queries.md)
-   [<span data-ttu-id="4b24a-124">Оператор ISA для запросов схемы</span><span class="sxs-lookup"><span data-stu-id="4b24a-124">ISA Operator for Schema Queries</span></span>](isa-operator-for-schema-queries.md)

<span data-ttu-id="4b24a-125">Оператор LIKE является допустимым в предложении WHERE и используется для определения того, соответствует ли данная символьная строка указанному шаблону.</span><span class="sxs-lookup"><span data-stu-id="4b24a-125">The LIKE operator is valid in the WHERE clause and is used to determine whether a given character string matches a specified pattern.</span></span> <span data-ttu-id="4b24a-126">Например, следующий запрос возвращает все экземпляры \_ классов Win32.</span><span class="sxs-lookup"><span data-stu-id="4b24a-126">For example, the following query returns all instances of Win32\_ classes.</span></span>


```sql
SELECT * FROM Meta_Class WHERE __Class LIKE "%Win32%"
```



<span data-ttu-id="4b24a-127">Дополнительные сведения о синтаксисе и использовании этого оператора см. в разделе [оператор Like](like-operator.md).</span><span class="sxs-lookup"><span data-stu-id="4b24a-127">For more information about the syntax and use of this operator, see [LIKE Operator](like-operator.md).</span></span>

 

 



