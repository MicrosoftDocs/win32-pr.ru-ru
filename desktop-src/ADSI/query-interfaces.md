---
title: Интерфейсы запросов
description: Для выполнения поиска по каталогу можно использовать три типа интерфейсов ADSI. Среда приложения и другие требования могут указывать, какой интерфейс используется.
ms.assetid: 42843e02-b685-492e-9046-aea460e84584
ms.tgt_platform: multiple
keywords:
- Интерфейсы интерфейсов запросов ADSI
- Запросы ADSI, интерфейсы запросов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 805303a972b4a8140a9e632857287aeebca9b32f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103887496"
---
# <a name="query-interfaces"></a><span data-ttu-id="77483-106">Интерфейсы запросов</span><span class="sxs-lookup"><span data-stu-id="77483-106">Query Interfaces</span></span>

<span data-ttu-id="77483-107">Для выполнения поиска по каталогу можно использовать три типа интерфейсов ADSI.</span><span class="sxs-lookup"><span data-stu-id="77483-107">Three types of ADSI interfaces can be used to perform directory searches.</span></span> <span data-ttu-id="77483-108">Среда приложения и другие требования могут указывать, какой интерфейс используется.</span><span class="sxs-lookup"><span data-stu-id="77483-108">The application environment and other requirements may indicate which interface is used.</span></span>

-   <span data-ttu-id="77483-109">[**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch).</span><span class="sxs-lookup"><span data-stu-id="77483-109">[**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch).</span></span> <span data-ttu-id="77483-110">**IDirectorySearch** — это базовый COM-интерфейс, доступный только программистам C/C++.</span><span class="sxs-lookup"><span data-stu-id="77483-110">**IDirectorySearch** is a basic COM interface only available to C/C++ programmers.</span></span> <span data-ttu-id="77483-111">Дополнительные сведения см. [в разделе Поиск с помощью интерфейса IDirectorySearch](searching-with-idirectorysearch.md).</span><span class="sxs-lookup"><span data-stu-id="77483-111">For more information, see [Searching With the IDirectorySearch Interface](searching-with-idirectorysearch.md).</span></span>
-   <span data-ttu-id="77483-112">Нудить.</span><span class="sxs-lookup"><span data-stu-id="77483-112">ADO.</span></span> <span data-ttu-id="77483-113">Интерфейсы объектов данных ActiveX (ADO) — это интерфейсы автоматизации, использующие OLE DB.</span><span class="sxs-lookup"><span data-stu-id="77483-113">The ActiveX Data Object (ADO) interfaces are Automation interfaces that use OLE DB.</span></span> <span data-ttu-id="77483-114">Используйте ADO для запросов в приложениях, которые используют автоматизацию.</span><span class="sxs-lookup"><span data-stu-id="77483-114">Use ADO for queries within applications that rely on Automation.</span></span> <span data-ttu-id="77483-115">К ним относятся Visual Basic приложения, Active Server страницы и т. д.</span><span class="sxs-lookup"><span data-stu-id="77483-115">These include Visual Basic applications, Active Server Pages, and so on.</span></span> <span data-ttu-id="77483-116">Дополнительные сведения см. [в разделе Поиск с помощью объекты данных ActiveX](searching-with-activex-data-objects-ado.md).</span><span class="sxs-lookup"><span data-stu-id="77483-116">For more information, see [Searching with ActiveX Data Objects](searching-with-activex-data-objects-ado.md).</span></span>
-   <span data-ttu-id="77483-117">OLE DB.</span><span class="sxs-lookup"><span data-stu-id="77483-117">OLE DB.</span></span> <span data-ttu-id="77483-118">OLE DB — это набор интерфейсов C/C++, используемых для запроса баз данных.</span><span class="sxs-lookup"><span data-stu-id="77483-118">OLE DB is a set of C/C++ interfaces used to query databases.</span></span> <span data-ttu-id="77483-119">Благодаря поддержке этих интерфейсов поставщики ADSI могут реализовывать дополнительные OLE DB функции, такие как распределенные запросы с другими поставщиками OLE DB.</span><span class="sxs-lookup"><span data-stu-id="77483-119">By supporting these interfaces, ADSI providers can implement advanced OLE DB features, such as distributed queries with other OLE DB providers.</span></span> <span data-ttu-id="77483-120">Дополнительные сведения см. [в разделе Поиск с помощью OLE DB](searching-with-ole-db.md).</span><span class="sxs-lookup"><span data-stu-id="77483-120">For more information, see [Searching with OLE DB](searching-with-ole-db.md).</span></span>

 

 




