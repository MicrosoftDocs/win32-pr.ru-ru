---
title: Использование ADO для получения диапазона
description: Если используется язык автоматизации, то для получения диапазона значений свойств следует использовать объекты каталогов ActiveX (ADO). При использовании ADO для извлечения диапазона существует одна проблема, которая должна быть специально решена.
ms.assetid: ca06169d-7de7-4552-aa7d-e9427353e49e
ms.tgt_platform: multiple
keywords:
- Использование ADO для получения диапазона ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cb8950a71708bd9c824c90842f043808c897554
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103772902"
---
# <a name="using-ado-for-range-retrieval"></a><span data-ttu-id="21499-104">Использование ADO для получения диапазона</span><span class="sxs-lookup"><span data-stu-id="21499-104">Using ADO for Range Retrieval</span></span>

<span data-ttu-id="21499-105">Если используется язык автоматизации, то для получения диапазона значений свойств следует использовать объекты каталогов ActiveX (ADO).</span><span class="sxs-lookup"><span data-stu-id="21499-105">If an automation language is used, the ActiveX Directory Objects (ADO) should be used to retrieve a range of property values.</span></span>

<span data-ttu-id="21499-106">При использовании ADO для извлечения диапазона существует одна проблема, которая должна быть специально решена.</span><span class="sxs-lookup"><span data-stu-id="21499-106">When using ADO for range retrieval, there is one problem that must be specifically addressed.</span></span> <span data-ttu-id="21499-107">При запросе итоговой группы значений свойств объект ADO извлечет нулевые объекты, даже если они больше остаются.</span><span class="sxs-lookup"><span data-stu-id="21499-107">When querying for the final group of property values, the ADO object will retrieve zero objects, even though more remain.</span></span> <span data-ttu-id="21499-108">Чтобы получить оставшиеся значения, используйте подстановочный знак " \* ".</span><span class="sxs-lookup"><span data-stu-id="21499-108">To retrieve the remaining values, use the range wildcard '\*'.</span></span> <span data-ttu-id="21499-109">Например, если группа содержит 150 членов, значения элементов 0-100 можно получить обычным образом, используя извлечение по диапазону.</span><span class="sxs-lookup"><span data-stu-id="21499-109">For example, if a group contains 150 members, member values 0-100 can be retrieved normally using ranged retrieval.</span></span> <span data-ttu-id="21499-110">Если затем запрашивается диапазон 101-200, объект ADO возвратит нулевые объекты.</span><span class="sxs-lookup"><span data-stu-id="21499-110">If range 101-200 is then requested, the ADO object will return zero objects.</span></span> <span data-ttu-id="21499-111">На этом этапе необходимо изменить запрос в диапазон запросов 101- \* .</span><span class="sxs-lookup"><span data-stu-id="21499-111">At this point, it is necessary to modify the query to request range 101-\*.</span></span> <span data-ttu-id="21499-112">Это позволит получить значения от 101 до 150.</span><span class="sxs-lookup"><span data-stu-id="21499-112">This will retrieve values from 101 to 150.</span></span> <span data-ttu-id="21499-113">Дополнительные сведения и пример кода см. в разделе [пример кода для использования для получения элементов группы](example-code-for-using-ranging-to-retrieve-members-of-a-group.md).</span><span class="sxs-lookup"><span data-stu-id="21499-113">For more information and a code example, see [Example Code for Using Ranging to Retrieve Members of a Group](example-code-for-using-ranging-to-retrieve-members-of-a-group.md).</span></span>

<span data-ttu-id="21499-114">Дополнительные сведения об использовании ADO для извлечения диапазона см. в следующих статьях:</span><span class="sxs-lookup"><span data-stu-id="21499-114">For more information about using ADO for range retrieval, see:</span></span>

-   [<span data-ttu-id="21499-115">Диалект языка ADO LDAP</span><span class="sxs-lookup"><span data-stu-id="21499-115">ADO LDAP Ranging Dialect</span></span>](ado-ldap-ranging-dialect.md)
-   [<span data-ttu-id="21499-116">Диалект языка многомерных объектов ADO SQL</span><span class="sxs-lookup"><span data-stu-id="21499-116">ADO SQL Ranging Dialect</span></span>](ado-sql-ranging-dialect.md)
-   [<span data-ttu-id="21499-117">Пример кода для использования в качестве значения для получения членов группы</span><span class="sxs-lookup"><span data-stu-id="21499-117">Example Code for Using Ranging to Retrieve Members of a Group</span></span>](example-code-for-using-ranging-to-retrieve-members-of-a-group.md)

 

 




