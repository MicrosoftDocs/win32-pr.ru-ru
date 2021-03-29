---
title: Реализация поставщиков интерфейсов служб Active Directory
description: Active Directory интерфейсы ADSI — это COM-интерфейсы, которые переносят объекты службы каталогов для предоставления их клиентам служб каталогов. Предоставляя реализацию ADSI, вы расширяете клиентскую базу до набора клиентских приложений ADSI.
ms.assetid: f86f36f0-44ff-41b7-8cf6-b97b721a8572
ms.tgt_platform: multiple
keywords:
- Реализация поставщиков интерфейсов служб Active Directory ADSI
- Реализация поставщиков ADSI ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30bdd0da406d9e65af898664e76b5e455540ebeb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103772950"
---
# <a name="implementing-active-directory-service-interfaces-providers"></a><span data-ttu-id="e1feb-106">Реализация поставщиков интерфейсов служб Active Directory</span><span class="sxs-lookup"><span data-stu-id="e1feb-106">Implementing Active Directory Service Interfaces Providers</span></span>

<span data-ttu-id="e1feb-107">Active Directory интерфейсы ADSI — это COM-интерфейсы, которые переносят объекты службы каталогов для предоставления их клиентам служб каталогов.</span><span class="sxs-lookup"><span data-stu-id="e1feb-107">Active Directory Service Interfaces (ADSI) are COM interfaces that wrap directory service objects to expose them to clients of directory services.</span></span> <span data-ttu-id="e1feb-108">Предоставляя реализацию ADSI, вы расширяете клиентскую базу до набора клиентских приложений ADSI.</span><span class="sxs-lookup"><span data-stu-id="e1feb-108">By supplying an implementation of ADSI, you expand your client-base to the set of ADSI client applications.</span></span>

<span data-ttu-id="e1feb-109">Как и любая реализация COM, поставщик ADSI можно написать на многих языках.</span><span class="sxs-lookup"><span data-stu-id="e1feb-109">As with any COM implementation, you can write an ADSI provider in many languages.</span></span> <span data-ttu-id="e1feb-110">Интерфейсы COM ADSI определяются как сдвоенные интерфейсы, обеспечивающие разрешение имен во время выполнения и во время компиляции, и могут вызываться поддерживающими автоматизацией языками, такими как Visual Basic, Visual Basic Scripting Edition, а также более производительные и эффективные языки, такие как C и C++.</span><span class="sxs-lookup"><span data-stu-id="e1feb-110">The ADSI COM interfaces are defined as dual interfaces that allow both run-time and compile-time name resolution and can be called by Automation-compliant languages such as Visual Basic, Visual Basic Scripting Edition, and also the more performance and efficiency-conscious languages such as C and C++.</span></span> <span data-ttu-id="e1feb-111">Клиенты ADSI также включают веб-приложения, использующие Active Server страницы и оснастки администрирования с помощью консоли управления (MMC).</span><span class="sxs-lookup"><span data-stu-id="e1feb-111">ADSI clients also include web applications using Active Server Pages and administration snap-ins through the Microsoft Management Console.</span></span>

<span data-ttu-id="e1feb-112">Поскольку ADSI предоставляет собственный поставщик OLE DB, реализация функций поиска, определенных [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) , также позволяет клиентам ADSI запрашивать данные в службе каталогов.</span><span class="sxs-lookup"><span data-stu-id="e1feb-112">Because ADSI supplies its own OLE DB provider, implementing the search features defined by [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) also enables ADSI clients to query your directory service for data.</span></span>

<span data-ttu-id="e1feb-113">Все объекты службы каталогов могут быть представлены через универсальный объект ADSI, поддерживающий [**идиректорйобжект**](/windows/desktop/api/Iads/nn-iads-idirectoryobject).</span><span class="sxs-lookup"><span data-stu-id="e1feb-113">All directory service objects can be represented through a generic ADSI object supporting [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject).</span></span> <span data-ttu-id="e1feb-114">ADSI предоставляет стандартные блоки, необходимые для представления функций и служб любой службы каталогов.</span><span class="sxs-lookup"><span data-stu-id="e1feb-114">ADSI supplies the building blocks necessary to represent the features and services of any directory service.</span></span>

<span data-ttu-id="e1feb-115">Кроме того, Meta-интерфейсы ADSI представляют общие объекты, используемые администраторами каталогов.</span><span class="sxs-lookup"><span data-stu-id="e1feb-115">In addition, the ADSI meta-interfaces represent common objects used by directory administrators.</span></span> <span data-ttu-id="e1feb-116">Свойства мета-интерфейсов сопоставляются со свойствами, поддерживаемыми службой каталогов.</span><span class="sxs-lookup"><span data-stu-id="e1feb-116">You map the properties of the meta-interfaces to the properties supported by your directory service.</span></span> <span data-ttu-id="e1feb-117">Клиенты ADSI, программирование на интерфейсы Active Directory служб, получают доступ к службе каталогов сразу после установки поставщика и перезапуска системы.</span><span class="sxs-lookup"><span data-stu-id="e1feb-117">ADSI clients programming to the Active Directory Service Interfaces gain access to your directory service as soon as the provider is installed and the system restarted.</span></span>

<span data-ttu-id="e1feb-118">Если служба каталогов поддерживает представление схемы, поддержка интерфейсов управления схемой делает пространство имен доступным для обозревателей службы каталогов напрямую.</span><span class="sxs-lookup"><span data-stu-id="e1feb-118">If your directory service supports a schema representation, supporting the schema management interfaces makes your namespace directly accessible to directory service browsers.</span></span> <span data-ttu-id="e1feb-119">Публикуя свои функции с помощью схемы, клиенты могут запрашивать службу каталогов в Интернете и использовать преимущества предоставляемых вами служб.</span><span class="sxs-lookup"><span data-stu-id="e1feb-119">By publishing your features through the schema, clients can query your directory service online and take advantage of the services you offer.</span></span> <span data-ttu-id="e1feb-120">Из-за доступности схемы в сети и преимуществ интерфейса COM вы можете по-прежнему предоставлять новые функции клиентскому программному обеспечению при поддержке версий нижнего уровня.</span><span class="sxs-lookup"><span data-stu-id="e1feb-120">Because of the online schema availability and the COM interface advantage, you can continue to make new features available to your client software while supporting down-level versions.</span></span>

 

 




