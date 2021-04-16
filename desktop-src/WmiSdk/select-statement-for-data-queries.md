---
description: Опишите инструкцию SELECT для запроса данных.
ms.assetid: 9c1a164e-4728-4fbe-8a49-b571005a46ec
ms.tgt_platform: multiple
title: Инструкция SELECT для запросов данных
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06905cfd9ef5e55022b3fc2275ed705a670a0ecc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701987"
---
# <a name="select-statement-for-data-queries"></a><span data-ttu-id="eb309-103">Инструкция SELECT для запросов данных</span><span class="sxs-lookup"><span data-stu-id="eb309-103">SELECT Statement for Data Queries</span></span>

<span data-ttu-id="eb309-104">Для запроса сведений можно использовать разнообразные инструкции SELECT.</span><span class="sxs-lookup"><span data-stu-id="eb309-104">You can use a variety of SELECT statements to query for information.</span></span> <span data-ttu-id="eb309-105">Инструкции могут быть основными операторами, или они могут быть более ограничивающими, чтобы сократить результирующий набор, возвращаемый запросом.</span><span class="sxs-lookup"><span data-stu-id="eb309-105">The statements can be basic statements or they can be more restrictive to narrow the result set that is returned from the query.</span></span>

<span data-ttu-id="eb309-106">В следующем примере показана базовая инструкция SELECT, которая используется для запроса данных.</span><span class="sxs-lookup"><span data-stu-id="eb309-106">The following example is a basic SELECT statement that is used to query for data.</span></span>


```sql
SELECT * FROM Class
```



<span data-ttu-id="eb309-107">Эта инструкция возвращает экземпляры указанного класса и любого из его подклассов.</span><span class="sxs-lookup"><span data-stu-id="eb309-107">This statement returns instances of the specified class and any of its subclasses.</span></span> <span data-ttu-id="eb309-108">Все системные и определяемые пользователем свойства для классов включены.</span><span class="sxs-lookup"><span data-stu-id="eb309-108">All of the system and user-defined properties for the classes are included.</span></span> <span data-ttu-id="eb309-109">Если системное свойство не относится к конкретному запросу, оно содержит **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="eb309-109">If a system property is not relevant for a particular query, it contains **NULL**.</span></span>

<span data-ttu-id="eb309-110">Можно использовать несколько методов для уменьшения пропускной способности, необходимой для получения результирующего набора, если выполнение запроса приводит к чрезмерному увеличению нагрузки, и пользователь заинтересован в подмножестве свойств.</span><span class="sxs-lookup"><span data-stu-id="eb309-110">You can use several techniques to reduce the bandwidth required to retrieve the result set, if the execution of the query results in too much overhead and the user is only interested in a subset of the properties.</span></span> <span data-ttu-id="eb309-111">Во первых, запросы могут заменить звездочку требуемыми свойствами.</span><span class="sxs-lookup"><span data-stu-id="eb309-111">First, queries can replace the asterisk with the desired properties.</span></span>

<span data-ttu-id="eb309-112">В следующем примере показано, как запросить определенные свойства.</span><span class="sxs-lookup"><span data-stu-id="eb309-112">The following example shows how to query for specific properties.</span></span>


```sql
SELECT property_1, property_2, property_3 FROM class
```



<span data-ttu-id="eb309-113">Результирующий набор содержит все системные свойства и указанные несистемные свойства.</span><span class="sxs-lookup"><span data-stu-id="eb309-113">The result set includes all system properties and the specified nonsystem properties.</span></span>

<span data-ttu-id="eb309-114">Другой способ ограничить область результирующего набора запроса — использовать системное свойство [**\_ \_ класса**](wmi-system-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="eb309-114">Another technique for narrowing the scope of a query's result set is to use the [**\_\_CLASS**](wmi-system-properties.md) system property.</span></span> <span data-ttu-id="eb309-115">Запросы по умолчанию возвращают все экземпляры указанного класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="eb309-115">Queries by default return all instances of the specified class and its subclasses.</span></span> <span data-ttu-id="eb309-116">Свойство системы **\_ \_ класса** можно использовать для запроса только экземпляров указанного класса, исключая его подклассы.</span><span class="sxs-lookup"><span data-stu-id="eb309-116">You can use the **\_\_CLASS** system property to request only instances of the specified class, excluding its subclasses.</span></span>

<span data-ttu-id="eb309-117">В следующем примере показано, как использовать свойство системы [**\_ \_ класса**](wmi-system-properties.md) в предложении WHERE.</span><span class="sxs-lookup"><span data-stu-id="eb309-117">The following example shows how to use the [**\_\_CLASS**](wmi-system-properties.md) system property in a WHERE clause.</span></span>


```sql
SELECT * FROM Device WHERE __CLASS = "Device"
```



<span data-ttu-id="eb309-118">Можно также использовать свойство системы [**\_ \_ класса**](wmi-system-properties.md) , чтобы ограничить результирующий набор экземплярами определенных подклассов.</span><span class="sxs-lookup"><span data-stu-id="eb309-118">You can also use the [**\_\_CLASS**](wmi-system-properties.md) system property to restrict the result set to instances of particular subclasses.</span></span>

<span data-ttu-id="eb309-119">В следующем примере показано, как ограничить результирующий набор экземплярами определенных подклассов.</span><span class="sxs-lookup"><span data-stu-id="eb309-119">The following example shows how to restrict the result set to instances of particular subclasses.</span></span>


```sql
SELECT * FROM Device WHERE __CLASS = "Modem" OR __CLASS = "Keyboard"
```



> [!Note]  
> <span data-ttu-id="eb309-120">При создании запроса с недопустимым путем к внедренному объекту запрос не возвращает ошибку или результаты.</span><span class="sxs-lookup"><span data-stu-id="eb309-120">If you construct a query with an invalid path for an embedded object, your query does not return an error or any results.</span></span>

 

<span data-ttu-id="eb309-121">В следующем примере возвращается экземпляр **маинкласс**, предполагая, что существует экземпляр **маинкласс** , содержащий внедренный объект **ембедобж** со свойством **P \_ UInt32** , равным "70011".</span><span class="sxs-lookup"><span data-stu-id="eb309-121">The following example returns an instance of **MainClass**, assuming that an instance of **MainClass** exists containing the embedded object **EmbedObj** with a property **P\_Uint32** that is equal to "70011".</span></span>


```sql
SELECT * FROM MainClass WHERE EmbedObj.P_Uint32 = 70011
```



<span data-ttu-id="eb309-122">В следующем примере не возвращаются результаты и не возвращается сообщение об ошибке, предполагая, что внедренный объект **ембедобж** в экземпляре **Маинкласс** не имеет **недопустимого** свойства.</span><span class="sxs-lookup"><span data-stu-id="eb309-122">The following example returns no results and does not return an error, assuming that the embedded object **EmbedObj** in the instance of **MainClass** does not have a property **INVALID**.</span></span>


```sql
SELECT * FROM MainClass WHERE StrongEmbedObj.INVALID = 70011
```



 

 



