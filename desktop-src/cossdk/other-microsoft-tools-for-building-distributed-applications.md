---
description: Другие средства Майкрософт для создания распределенных приложений
ms.assetid: 518ca5b5-4285-4d69-abfe-bf6444a1deb5
title: Другие средства Майкрософт для создания распределенных приложений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 657d65bd7c61a73bedb9463e8558415c7b27fe04
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105710774"
---
# <a name="other-microsoft-tools-for-building-distributed-applications"></a><span data-ttu-id="2324f-103">Другие средства Майкрософт для создания распределенных приложений</span><span class="sxs-lookup"><span data-stu-id="2324f-103">Other Microsoft Tools for Building Distributed Applications</span></span>

<span data-ttu-id="2324f-104">Помимо инструментов в COM+, корпорация Майкрософт предоставляет следующие средства для помощи разработчикам в создании распределенных приложений:</span><span class="sxs-lookup"><span data-stu-id="2324f-104">In addition to the tools in COM+, Microsoft provides the following tools to assist the developer in creating distributed applications:</span></span>

-   <span data-ttu-id="2324f-105">Компоненты доступа к данным Microsoft (MDAC).</span><span class="sxs-lookup"><span data-stu-id="2324f-105">Microsoft Data Access Components (MDAC).</span></span> <span data-ttu-id="2324f-106">Корпорация Майкрософт предоставляет несколько способов получения данных из множества источников.</span><span class="sxs-lookup"><span data-stu-id="2324f-106">Microsoft provides several avenues for retrieving data from a myriad of sources.</span></span> <span data-ttu-id="2324f-107">Например, OLE DB предлагает набор COM-интерфейсов для создания компонентов базы данных.</span><span class="sxs-lookup"><span data-stu-id="2324f-107">For example, OLE DB offers a set of COM interfaces for building database components.</span></span> <span data-ttu-id="2324f-108">Интерфейсы определяются таким образом, чтобы поставщики данных могли реализовать различные уровни поддержки на основе возможностей базового хранилища данных.</span><span class="sxs-lookup"><span data-stu-id="2324f-108">The interfaces are defined so that data providers can implement different levels of support, based on the capabilities of the underlying data store.</span></span> <span data-ttu-id="2324f-109">Поскольку OLE DB основан на COM, его можно легко расширить, а расширения реализуются как новые интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="2324f-109">Because OLE DB is COM-based, it can easily be extended, and extensions are implemented as new interfaces.</span></span> <span data-ttu-id="2324f-110">OLE DB также включает программный интерфейс уровня приложения, именуемый объекты данных ActiveX (ADO).</span><span class="sxs-lookup"><span data-stu-id="2324f-110">OLE DB also includes an application-level programming interface, called ActiveX Data Objects (ADO).</span></span> <span data-ttu-id="2324f-111">ADO предоставляет сдвоенные интерфейсы, поэтому их можно легко использовать из языков сценариев, а также Microsoft Visual C++, Visual Basic и других средств разработчика.</span><span class="sxs-lookup"><span data-stu-id="2324f-111">ADO exposes dual interfaces, so it can easily be used from scripting languages as well as Microsoft Visual C++, Visual Basic, and other developer tools.</span></span>

    > [!Note]  
    > <span data-ttu-id="2324f-112">Разработчики также могут использовать универсальный интерфейс API, не зависящий от поставщика, такой как API Microsoft Open Database Connectivity (ODBC).</span><span class="sxs-lookup"><span data-stu-id="2324f-112">Developers can also choose to use a generic, vendor-neutral API such as the Microsoft Open Database Connectivity (ODBC) application programming interface (API).</span></span> <span data-ttu-id="2324f-113">API ODBC — это языковой интерфейс C для доступа к данным в СУБД с помощью язык SQL (SQL).</span><span class="sxs-lookup"><span data-stu-id="2324f-113">The ODBC API is a C language interface for accessing data in a DBMS by using Structured Query Language (SQL).</span></span> <span data-ttu-id="2324f-114">Диспетчер драйверов ODBC предоставляет программный интерфейс и компоненты времени выполнения для выявления драйверов, зависящих от СУБД.</span><span class="sxs-lookup"><span data-stu-id="2324f-114">An ODBC driver manager provides the programming interface and run-time components to locate DBMS-specific drivers.</span></span> <span data-ttu-id="2324f-115">Драйверы ODBC, обычно предоставляемые поставщиком СУБД, преобразуют универсальные вызовы из диспетчера драйверов ODBC в вызовы собственного метода доступа к данным.</span><span class="sxs-lookup"><span data-stu-id="2324f-115">ODBC drivers, typically supplied by the DBMS vendor, translate generic calls from the ODBC driver manager into calls to the native data access method.</span></span> <span data-ttu-id="2324f-116">Основное преимущество использования API ODBC заключается в том, что необходимо изучить только один API для доступа к широкому спектру СУБД.</span><span class="sxs-lookup"><span data-stu-id="2324f-116">The primary advantage of using the ODBC API is that you need to learn only one API to access a wide range of DBMSs.</span></span>

     

-   <span data-ttu-id="2324f-117">Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="2324f-117">Microsoft SQL Server.</span></span> <span data-ttu-id="2324f-118">Помимо обеспечения надежной и Милнером реляционной базы данных, Microsoft SQL Server может предоставить распределенное приложение с использованием пулов и безопасности подключений, которое может интегрироваться с моделью безопасности Windows.</span><span class="sxs-lookup"><span data-stu-id="2324f-118">In addition to providing a robust and eloquent relational database system, Microsoft SQL Server can provide a distributed application with connection pooling and security that can integrate with the Windows security model.</span></span>

-   <span data-ttu-id="2324f-119">Интеграция транзакций COM (COMTI).</span><span class="sxs-lookup"><span data-stu-id="2324f-119">COM Transaction Integration (COMTI).</span></span> <span data-ttu-id="2324f-120">COMTI можно использовать для интеграции мэйнфреймов в системы Windows, включая приложения COM+.</span><span class="sxs-lookup"><span data-stu-id="2324f-120">COMTI can be used to integrate mainframe systems into Windows systems, including COM+ applications.</span></span> <span data-ttu-id="2324f-121">COMTI использует стандартные протоколы связи (например, LU 6,2) для обмена данными между компьютерами Windows и мэйнфреймом и миникомпьютеры.</span><span class="sxs-lookup"><span data-stu-id="2324f-121">COMTI uses standard communication protocols (for example, LU 6.2) for communicating between Windows computers and mainframe and minicomputers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2324f-122">См. также</span><span class="sxs-lookup"><span data-stu-id="2324f-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2324f-123">Предположения и принципы разработки COM+</span><span class="sxs-lookup"><span data-stu-id="2324f-123">COM+ Design Assumptions and Principles</span></span>](com--design-assumptions-and-principles.md)
</dt> <dt>

[<span data-ttu-id="2324f-124">Проектирование приложения COM+ с помощью UML</span><span class="sxs-lookup"><span data-stu-id="2324f-124">Designing the COM+ Application Using UML</span></span>](designing-the-com--application-using-uml.md)
</dt> <dt>

[<span data-ttu-id="2324f-125">Общие рекомендации по проектированию для использования COM+</span><span class="sxs-lookup"><span data-stu-id="2324f-125">General Design Tips for Using COM+</span></span>](general-design-tips-for-using-com-.md)
</dt> <dt>

[<span data-ttu-id="2324f-126">Оптимизация взаимодействия с уровнем бизнес-логики COM+</span><span class="sxs-lookup"><span data-stu-id="2324f-126">Optimizing Interactions with the COM+ Business Logic Tier</span></span>](optimizing-interactions-with-the-com--business-logic-tier.md)
</dt> </dl>

 

 



