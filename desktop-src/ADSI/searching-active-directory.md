---
title: Поиск Active Directory
description: Важной функцией Active Directory является разрешение запросов данных для людей, а также данных конфигурации для компьютеров и служб.
ms.assetid: 8427d69b-0974-4adc-9732-790e5d31db7a
ms.tgt_platform: multiple
keywords:
- Поиск Active Directory ADSI
- ADSI ADSI, поиск Active Directory
- запросы к ADSI, поиск Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1881872be6092312015f22eba477599ed9394df7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328355"
---
# <a name="searching-active-directory"></a><span data-ttu-id="ca5c9-106">Поиск Active Directory</span><span class="sxs-lookup"><span data-stu-id="ca5c9-106">Searching Active Directory</span></span>

<span data-ttu-id="ca5c9-107">Важной функцией Active Directory является разрешение запросов данных для людей, а также данных конфигурации для компьютеров и служб.</span><span class="sxs-lookup"><span data-stu-id="ca5c9-107">An important function of Active Directory is to resolve data queries for people, as well as configuration data for computers and services.</span></span> <span data-ttu-id="ca5c9-108">Чтобы написать эффективные запросы для Active Directory, полезно ознакомиться со следующими сведениями:</span><span class="sxs-lookup"><span data-stu-id="ca5c9-108">To write efficient queries for Active Directory, it is helpful to be familiar with the following:</span></span>

-   <span data-ttu-id="ca5c9-109">Определение области запроса: должен ли клиент находить свойства для объектов, которые могут находиться в любом месте леса или только в пределах одного домена или в рамках данного подразделения?</span><span class="sxs-lookup"><span data-stu-id="ca5c9-109">Determining the scope of the query: Must the client find properties for objects that might be located anywhere within a forest, or only within one domain, or within a given organizational unit (OU)?</span></span>
-   <span data-ttu-id="ca5c9-110">Определение глубины запроса: должен ли запрос искать только один уровень или пересекаться с другими каталогами LDAP?</span><span class="sxs-lookup"><span data-stu-id="ca5c9-110">Determining the depth of the query: Must the query only search one level or might it cross into other LDAP directories?</span></span>
-   <span data-ttu-id="ca5c9-111">Производительность и обработка больших результирующих наборов: как обеспечить эффективную обработку клиентом потенциального большого результирующего набора?</span><span class="sxs-lookup"><span data-stu-id="ca5c9-111">Performance and handling large result sets: How should the client effectively handle the potential of a large result set?</span></span>
-   <span data-ttu-id="ca5c9-112">Определение лучших запросов: какой тип запросов обеспечивает наиболее эффективные результаты?</span><span class="sxs-lookup"><span data-stu-id="ca5c9-112">Determining the best queries: What type of queries provide the most efficient results?</span></span> <span data-ttu-id="ca5c9-113">Какой тип запросов следует избегать для разработчиков?</span><span class="sxs-lookup"><span data-stu-id="ca5c9-113">What type of queries should the developer avoid?</span></span>
-   <span data-ttu-id="ca5c9-114">Основные сведения о синтаксисе запросов: ADSI поддерживает синтаксис LDAP, как описано в RFC 2254, а также подмножество SQL.</span><span class="sxs-lookup"><span data-stu-id="ca5c9-114">Understanding the query syntax: ADSI supports both the LDAP syntax as documented in RFC 2254, as well as a subset of SQL.</span></span>
-   <span data-ttu-id="ca5c9-115">Возможности выбора интерфейсов. ADSI предоставляет как поддержку OLE DB, так и интерфейс C/C++, именуемый [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch).</span><span class="sxs-lookup"><span data-stu-id="ca5c9-115">Choice of interfaces: ADSI provides both OLE DB support as well as a C/C++ interface called [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch).</span></span> <span data-ttu-id="ca5c9-116">Так как ADSI работает для нескольких пространств имен, эти интерфейсы можно использовать для запроса других пространств имен, таких как Exchange, а также Active Directory.</span><span class="sxs-lookup"><span data-stu-id="ca5c9-116">Because ADSI works for multiple namespaces, you can use these interfaces for querying other namespaces such as Exchange, as well as Active Directory.</span></span> <span data-ttu-id="ca5c9-117">Поскольку объект данных ActiveX (ADO) — это простая модель объектов доступа к данным, поддерживающая сценарии, поверх OLE DB, интерфейсы OLE DB хорошо работают для Visual Basic программистов и средств записи сценариев веб-страниц.</span><span class="sxs-lookup"><span data-stu-id="ca5c9-117">Because the ActiveX Data Object (ADO) is a simple scriptable data access object model on top of OLE DB, the OLE DB interfaces work well for Visual Basic programmers and webpage script writers.</span></span> <span data-ttu-id="ca5c9-118">Новые функции доступа к данным в приложениях Visual Studio и Office, использующие преимущества ADO и OLE DB теперь могут получать доступ к Active Directory данным так же, как и к данным других поставщиков OLE DB, таких как SQL Server.</span><span class="sxs-lookup"><span data-stu-id="ca5c9-118">The new data access features within Visual Studio and Office applications that take advantage of ADO and OLE DB can now access Active Directory data in the same way that they access data from other OLE DB providers, such as SQL Server.</span></span> <span data-ttu-id="ca5c9-119">Однако если разработчик C/C++ должен выполнить простой поиск в каталоге, интерфейс **IDirectorySearch** может оказаться более подходящим, чем интерфейсы OLE DB.</span><span class="sxs-lookup"><span data-stu-id="ca5c9-119">However, if a C/C++ developer must perform a simple directory search, the **IDirectorySearch** interface might be more appropriate than the OLE DB interfaces.</span></span>

<span data-ttu-id="ca5c9-120">В следующих разделах описано, как выполнить поиск Active Directory чтобы убедиться, что приложение выдает наиболее эффективный запрос, учитывая требования клиента:</span><span class="sxs-lookup"><span data-stu-id="ca5c9-120">The following topics describe how to search Active Directory to ensure your application issues the most efficient query, given the requirements of the client:</span></span>

-   [<span data-ttu-id="ca5c9-121">Область запроса</span><span class="sxs-lookup"><span data-stu-id="ca5c9-121">Scope of Query</span></span>](scope-of-query.md)
-   [<span data-ttu-id="ca5c9-122">Производительность и обработка больших результирующих наборов</span><span class="sxs-lookup"><span data-stu-id="ca5c9-122">Performance and Handling Large Result Sets</span></span>](performance-and-handling-large-result-sets.md)
-   [<span data-ttu-id="ca5c9-123">Синтаксис фильтра поиска</span><span class="sxs-lookup"><span data-stu-id="ca5c9-123">Search Filter Syntax</span></span>](search-filter-syntax.md)
-   [<span data-ttu-id="ca5c9-124">Интерфейсы запросов</span><span class="sxs-lookup"><span data-stu-id="ca5c9-124">Query Interfaces</span></span>](query-interfaces.md)
-   [<span data-ttu-id="ca5c9-125">Поиск двоичных данных</span><span class="sxs-lookup"><span data-stu-id="ca5c9-125">Searching Binary Data</span></span>](searching-binary-data.md)
-   [<span data-ttu-id="ca5c9-126">Распределенный запрос</span><span class="sxs-lookup"><span data-stu-id="ca5c9-126">Distributed Query</span></span>](distributed-query.md)

 

 




