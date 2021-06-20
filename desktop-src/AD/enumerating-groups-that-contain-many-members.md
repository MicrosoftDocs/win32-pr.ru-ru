---
title: Перечисление групп, содержащих много элементов
description: Дополнительные сведения о перечислении групп Azure Active Directory, содержащих много элементов, с помощью добавочного извлечения данных (извлечение диапазона).
ms.assetid: 78f81b09-2223-4b74-b8d5-7a97494c0324
ms.tgt_platform: multiple
keywords:
- Перечисление групп, содержащих множество членов Active Directory
- группы Active Directory, перечисление групп с множеством членов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7cab63b809fdbd2666f39a09d32f601346da00e
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405157"
---
# <a name="enumerating-groups-that-contain-many-members"></a><span data-ttu-id="ab195-105">Перечисление групп, содержащих много элементов</span><span class="sxs-lookup"><span data-stu-id="ab195-105">Enumerating Groups That Contain Many Members</span></span>

<span data-ttu-id="ab195-106">Члены группы хранятся в атрибуте с несколькими значениями, называемом **member**.</span><span class="sxs-lookup"><span data-stu-id="ab195-106">The members of a group are stored in a multi-value attribute called **member**.</span></span> <span data-ttu-id="ab195-107">Атрибут **member** может содержать большое количество значений.</span><span class="sxs-lookup"><span data-stu-id="ab195-107">The **member** attribute can contain a large number of values.</span></span> <span data-ttu-id="ab195-108">Перечисление элементов может быть неэффективным, если число значений в атрибуте с несколькими значениями станет большим.</span><span class="sxs-lookup"><span data-stu-id="ab195-108">Enumerating members can be inefficient when the number of values in a multi-valued attribute becomes large.</span></span> <span data-ttu-id="ab195-109">Сервер также будет ограничивать максимальное количество значений, которые могут быть получены в одном запросе.</span><span class="sxs-lookup"><span data-stu-id="ab195-109">The server will also limit the maximum number of values that can be retrieved in a single query.</span></span> <span data-ttu-id="ab195-110">Это означает, что если группа может содержать больше элементов, чем может предоставить сервер, единственным способом перечисления всех членов является использование добавочного извлечения данных, известного как *Извлечение диапазона*.</span><span class="sxs-lookup"><span data-stu-id="ab195-110">This means that if a group may have more members than can be supplied by the server, the only way to enumerate all members is to use incremental retrieval of data, known as *range retrieval*.</span></span>

<span data-ttu-id="ab195-111">Извлечение диапазона включает в себя запрос ограниченного числа значений атрибутов в одном запросе.</span><span class="sxs-lookup"><span data-stu-id="ab195-111">Range retrieval involves requesting a limited number of attribute values in a single query.</span></span> <span data-ttu-id="ab195-112">Количество запрошенных значений должно быть меньше или равно максимальному количеству значений, поддерживаемых сервером.</span><span class="sxs-lookup"><span data-stu-id="ab195-112">The number of values requested must be less than, or equal to, the maximum number of values supported by the server.</span></span> <span data-ttu-id="ab195-113">Чтобы сократить количество обращений запроса к серверу, количество запрошенных значений должно быть максимально близко к этому максимуму.</span><span class="sxs-lookup"><span data-stu-id="ab195-113">To reduce the number of times the query must contact the server, the number of values requested should be as close, as possible, to this maximum.</span></span> <span data-ttu-id="ab195-114">Чтобы обеспечить правильную работу приложения со всеми серверами, следует использовать максимальное число 1000.</span><span class="sxs-lookup"><span data-stu-id="ab195-114">To enable an application to work correctly with all servers, a maximum number of 1000 should be used.</span></span>

<span data-ttu-id="ab195-115">Версия сервера, предоставляющего запрошенные данные, определяет максимальное количество значений, которые могут быть получены в одном запросе.</span><span class="sxs-lookup"><span data-stu-id="ab195-115">The version of the server that supplies the requested data determines the maximum number of values that can be retrieved in a single query.</span></span> <span data-ttu-id="ab195-116">В следующей таблице перечислены версии сервера и максимальное количество значений, которые могут быть получены в одном запросе.</span><span class="sxs-lookup"><span data-stu-id="ab195-116">The following table lists the server version and the maximum number of values that can be retrieved in a single query.</span></span>



| <span data-ttu-id="ab195-117">Версия операционной системы сервера</span><span class="sxs-lookup"><span data-stu-id="ab195-117">Server operating system version</span></span> | <span data-ttu-id="ab195-118">Максимальное число полученных значений</span><span class="sxs-lookup"><span data-stu-id="ab195-118">Maximum values retrieved</span></span> |
|---------------------------------|--------------------------|
| <span data-ttu-id="ab195-119">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="ab195-119">Windows 2000</span></span>                    | <span data-ttu-id="ab195-120">1000</span><span class="sxs-lookup"><span data-stu-id="ab195-120">1000</span></span>                     |
| <span data-ttu-id="ab195-121">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ab195-121">Windows Server 2003</span></span>             | <span data-ttu-id="ab195-122">1500</span><span class="sxs-lookup"><span data-stu-id="ab195-122">1500</span></span>                     |



 

<span data-ttu-id="ab195-123">Дополнительные сведения о получении диапазонов значений атрибутов с помощью ADSI см. в разделе [получение диапазона атрибутов](/windows/desktop/ADSI/attribute-range-retrieval).</span><span class="sxs-lookup"><span data-stu-id="ab195-123">For more information about retrieving ranges of attribute values with ADSI, see [Attribute Range Retrieval](/windows/desktop/ADSI/attribute-range-retrieval).</span></span>

<span data-ttu-id="ab195-124">Дополнительные сведения о получении диапазонов значений атрибутов с помощью [System. DirectoryServices](/dotnet/api/system.directoryservices)см. [в разделе перечисление элементов в большой группе](https://msdn.microsoft.com/library/ms180907(v=VS.80).aspx).</span><span class="sxs-lookup"><span data-stu-id="ab195-124">For more information about retrieving ranges of attribute values with [System.DirectoryServices](/dotnet/api/system.directoryservices), see [Enumerating Members in a Large Group](https://msdn.microsoft.com/library/ms180907(v=VS.80).aspx).</span></span>

 

 