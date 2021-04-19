---
description: Одним из основных средств инструментарий управления Windows (WMI) (WMI) является возможность запрашивать в репозитории WMI сведения о классе и экземпляре.
ms.assetid: 0cceda42-fba0-4a08-90dd-43f022d0be41
ms.tgt_platform: multiple
title: Запрос WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdae44d4c40e1127bfc4d3436d6230eafd52146a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692710"
---
# <a name="querying-wmi"></a><span data-ttu-id="c8b0a-103">Запрос WMI</span><span class="sxs-lookup"><span data-stu-id="c8b0a-103">Querying WMI</span></span>

<span data-ttu-id="c8b0a-104">Одним из основных средств инструментарий управления Windows (WMI) (WMI) является возможность запрашивать в репозитории WMI сведения о классе и экземпляре.</span><span class="sxs-lookup"><span data-stu-id="c8b0a-104">One of the main tools of Windows Management Instrumentation (WMI) is the ability to query the WMI repository for class and instance information.</span></span> <span data-ttu-id="c8b0a-105">Например, можно запросить, чтобы инструментарий WMI возвращал все объекты, представляющие события завершения работы, из настольной системы.</span><span class="sxs-lookup"><span data-stu-id="c8b0a-105">For example, you can request that WMI return all the objects representing shut-down events from your desktop system.</span></span> <span data-ttu-id="c8b0a-106">Можно также получить данные класса, экземпляра или схемы.</span><span class="sxs-lookup"><span data-stu-id="c8b0a-106">You can also retrieve class, instance, or schema data.</span></span> <span data-ttu-id="c8b0a-107">В следующей таблице перечислены различные типы запросов, которые можно выполнить.</span><span class="sxs-lookup"><span data-stu-id="c8b0a-107">The following table lists the different types of queries you can make.</span></span>



| <span data-ttu-id="c8b0a-108">Раздел</span><span class="sxs-lookup"><span data-stu-id="c8b0a-108">Topic</span></span>                                                                | <span data-ttu-id="c8b0a-109">Описание</span><span class="sxs-lookup"><span data-stu-id="c8b0a-109">Description</span></span>                                                                                                                                                                                      |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c8b0a-110">Вызов синхронного запроса</span><span class="sxs-lookup"><span data-stu-id="c8b0a-110">Invoking a Synchronous Query</span></span>](invoking-a-synchronous-query.md)     | <span data-ttu-id="c8b0a-111">Описывается, как поддерживать связь с WMI во время выполнения запроса.</span><span class="sxs-lookup"><span data-stu-id="c8b0a-111">Describes how to maintain a link with WMI throughout the query process.</span></span> <span data-ttu-id="c8b0a-112">Синхронные запросы хорошо подходят для небольших запросов или запросов к локальной системе.</span><span class="sxs-lookup"><span data-stu-id="c8b0a-112">Synchronous queries are good for small queries or queries to a local system.</span></span><br/>                                  |
| [<span data-ttu-id="c8b0a-113">Вызов асинхронного запроса</span><span class="sxs-lookup"><span data-stu-id="c8b0a-113">Invoking an Asynchronous Query</span></span>](invoking-an-asynchronous-query.md) | <span data-ttu-id="c8b0a-114">Описывает, как настроить отдельный процесс получения запросов.</span><span class="sxs-lookup"><span data-stu-id="c8b0a-114">Describes how to set up a separate process to receive queries.</span></span> <span data-ttu-id="c8b0a-115">Асинхронные запросы более сложны и обеспечивают более низкий уровень безопасности, но обычно улучшают производительность системы.</span><span class="sxs-lookup"><span data-stu-id="c8b0a-115">Asynchronous queries are more complex and provide a lower level of security, but generally improve system performance.</span></span><br/> |



 

<span data-ttu-id="c8b0a-116">Помимо запроса к репозиторию WMI, можно также использовать [*язык запросов WMI (WQL)*](gloss-w.md) для маршрутизации событий уведомления в приложение.</span><span class="sxs-lookup"><span data-stu-id="c8b0a-116">In addition to querying the WMI repository, you can also use the [*WMI Query Language (WQL)*](gloss-w.md) to route notification events to your application.</span></span> <span data-ttu-id="c8b0a-117">Дополнительные сведения см. [в разделе Получение WMI-события](receiving-a-wmi-event.md).</span><span class="sxs-lookup"><span data-stu-id="c8b0a-117">For more information, see [Receiving a WMI Event](receiving-a-wmi-event.md).</span></span>

> [!Note]
>
> <span data-ttu-id="c8b0a-118">Чтобы правильно запрашивать Инструментарий WMI, необходимо иметь хорошее представление о WQL.</span><span class="sxs-lookup"><span data-stu-id="c8b0a-118">To properly query WMI, you must have a good understanding of WQL.</span></span> <span data-ttu-id="c8b0a-119">Запрос, который является неправильным, слишком сложным или неприемлемым, может привести к тому, что обработчик запросов возвратит ошибку или непредвиденные результаты.</span><span class="sxs-lookup"><span data-stu-id="c8b0a-119">A query that is incorrect, too complex, or inappropriate can cause the query processor to return an error or unexpected results.</span></span> <span data-ttu-id="c8b0a-120">Полный обзор WQL см. в разделе [запросы с помощью WQL](querying-with-wql.md).</span><span class="sxs-lookup"><span data-stu-id="c8b0a-120">For a comprehensive guide to WQL, see [Querying with WQL](querying-with-wql.md).</span></span>
>
> <span data-ttu-id="c8b0a-121">Существует ряд ограничений на количество ключевых слов **and** и **or** , которые могут использоваться в запросах WQL.</span><span class="sxs-lookup"><span data-stu-id="c8b0a-121">There are limits to the number of **AND** and **OR** keywords that can be used in WQL queries.</span></span> <span data-ttu-id="c8b0a-122">Большое количество ключевых слов WQL, используемых в сложном запросе, может привести к тому, что WMI вернет код ошибки **\_ \_ \_ нарушения квоты WBEM E** как значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c8b0a-122">Large numbers of WQL keywords used in a complex query can cause WMI to return the **WBEM\_E\_QUOTA\_VIOLATION** error code as an **HRESULT** value.</span></span> <span data-ttu-id="c8b0a-123">Ограничение ключевых слов WQL зависит от того, насколько сложным является запрос.</span><span class="sxs-lookup"><span data-stu-id="c8b0a-123">The limit of WQL keywords depends on how complex the query is.</span></span>
>
> <span data-ttu-id="c8b0a-124">При запросе значений свойств с типом данных **UInt64** или **sint64** в языке сценариев, например VBScript, Инструментарий WMI возвращает строковые значения.</span><span class="sxs-lookup"><span data-stu-id="c8b0a-124">When querying for property values with a **uint64** or **sint64** data type in a scripting language like VBScript, WMI returns string values.</span></span> <span data-ttu-id="c8b0a-125">При сравнении этих значений могут возникать непредвиденные результаты, поскольку сравнение строк возвращает разные результаты, чем сравнение чисел.</span><span class="sxs-lookup"><span data-stu-id="c8b0a-125">Unexpected results can occur when comparing these values, because comparing strings returns different results than comparing numbers.</span></span> <span data-ttu-id="c8b0a-126">Например, значение "10000000000" меньше "9" при сравнении строк, а значение 9 меньше 10000000000 при сравнении чисел.</span><span class="sxs-lookup"><span data-stu-id="c8b0a-126">For example, "10000000000" is less than "9" when comparing strings, and 9 is less than 10000000000 when comparing numbers.</span></span> <span data-ttu-id="c8b0a-127">Чтобы избежать путаницы, следует использовать метод [CDbl](/previous-versions//ftekwwt0(v=vs.85)) в VBScript при получении свойств типа **UInt64** или **sint64** из WMI.</span><span class="sxs-lookup"><span data-stu-id="c8b0a-127">To avoid confusion you should use the [CDbl](/previous-versions//ftekwwt0(v=vs.85)) method in VBScript when properties of type **uint64** or **sint64** are retrieved from WMI.</span></span>

 

> [!Note]  

 

<span data-ttu-id="c8b0a-128">Дополнительные сведения см. в разделе [Управление сведениями о классе и экземпляре](manipulating-class-and-instance-information.md).</span><span class="sxs-lookup"><span data-stu-id="c8b0a-128">For more information, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md).</span></span>

 

