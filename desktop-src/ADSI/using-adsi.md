---
title: Использование Active Directory интерфейсов служб
description: Интерфейсы служб Active Directory (ADSI) предоставляют клиентским приложениям служб каталогов возможность использовать один набор интерфейсов для взаимодействия с любым пространством имен, предоставляющим реализацию интерфейса ADSI.
ms.assetid: 58bde1ea-30d1-4601-a6fb-df0bb837e2ab
ms.tgt_platform: multiple
keywords:
- Использование интерфейсов Active Directory Service Interfaces ADSI
- ADSI ADSI, использование
- Интерфейсы служб Active Directory ADSI, использование
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e500044ec755c393f8c8287528fee7f935751fe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103887471"
---
# <a name="using-active-directory-service-interfaces"></a><span data-ttu-id="f0e0e-106">Использование Active Directory интерфейсов служб</span><span class="sxs-lookup"><span data-stu-id="f0e0e-106">Using Active Directory Service Interfaces</span></span>

<span data-ttu-id="f0e0e-107">Интерфейсы служб Active Directory (ADSI) предоставляют клиентским приложениям служб каталогов возможность использовать один набор интерфейсов для взаимодействия с любым пространством имен, предоставляющим реализацию интерфейса ADSI.</span><span class="sxs-lookup"><span data-stu-id="f0e0e-107">Active Directory Service Interfaces (ADSI) provides the means for client applications of directory services to use one set of interfaces to communicate with any namespace that provides an ADSI implementation.</span></span> <span data-ttu-id="f0e0e-108">Для упрощения доступа к службам для пространства имен клиенты ADSI используют четко определенные интерфейсы Active Directory служб вместо вызовов API, связанных с сетью.</span><span class="sxs-lookup"><span data-stu-id="f0e0e-108">ADSI clients use the well-defined Active Directory Service Interfaces in place of the network-specific API calls to gain simpler access to the services for a namespace.</span></span>

<span data-ttu-id="f0e0e-109">Active Directory интерфейсы служб соответствуют модели COM и поддерживают стандартные функции COM.</span><span class="sxs-lookup"><span data-stu-id="f0e0e-109">Active Directory Service Interfaces conform to the Component Object Model (COM) and support standard COM features.</span></span>

<span data-ttu-id="f0e0e-110">ADSI предоставляет интерфейсы, совместимые с автоматизацией для контроллеров с привязкой к имени, таких как Java, система разработки Visual Basic Майкрософт и Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="f0e0e-110">ADSI supplies interfaces that are compliant with Automation for name-bound controllers like Java, Microsoft Visual Basic development system, and Visual Basic Scripting Edition (VBScript).</span></span> <span data-ttu-id="f0e0e-111">ADSI также предоставляет интерфейс, который может оптимизировать производительность для интерфейсов, не соответствующих автоматизации, для использования с языковыми средами, такими как C и C++.</span><span class="sxs-lookup"><span data-stu-id="f0e0e-111">ADSI can also provide an interface that can optimize performance for interfaces that are not compliant with Automation, to use with language environments like C and C++.</span></span>

<span data-ttu-id="f0e0e-112">ADSI также предоставляет интерфейсы [**идиректорйобжект**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) и [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch), не поддерживающие автоматизацию, для поддержки управления объектами каталога и запросов.</span><span class="sxs-lookup"><span data-stu-id="f0e0e-112">ADSI also provides the non-automation interfaces, [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) and [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch), to support directory object management and queries.</span></span>

<span data-ttu-id="f0e0e-113">Кроме того, ADSI предоставляет собственный поставщик OLE DB, чтобы любой клиент, уже использующий OLE DB, в том числе с помощью объекты данных ActiveX, мог запрашивать службы каталогов напрямую.</span><span class="sxs-lookup"><span data-stu-id="f0e0e-113">In addition, ADSI supplies its own OLE DB provider, so that any client already using OLE DB, including those using ActiveX Data Objects, can query directory services directly.</span></span>

<span data-ttu-id="f0e0e-114">Веб-приложения, использующие Active Server страницы, также могут программировать доступ к службам каталогов через ADSI.</span><span class="sxs-lookup"><span data-stu-id="f0e0e-114">Web applications using Active Server Pages also can program access to directory services through ADSI.</span></span>

<span data-ttu-id="f0e0e-115">Клиенты ADSI могут программно обнаруживать все поставщики ADSI на сайте и использовать одни и те же интерфейсы для взаимодействия с каждым пространством имен.</span><span class="sxs-lookup"><span data-stu-id="f0e0e-115">ADSI clients can programmatically discover all the ADSI providers at a site and use the same interfaces to communicate with each namespace.</span></span> <span data-ttu-id="f0e0e-116">По мере установки дополнительных поставщиков клиенты ADSI могут обмениваться данными без повторной компиляции с новыми пространствами имен.</span><span class="sxs-lookup"><span data-stu-id="f0e0e-116">As additional providers are installed, the ADSI clients can communicate, without recompiling, with the new namespaces as well.</span></span>

<span data-ttu-id="f0e0e-117">Это руководство по программированию описывает работу ADSI и предоставляет сведения для выполнения конкретных задач в ADSI.</span><span class="sxs-lookup"><span data-stu-id="f0e0e-117">This programming guide describes how ADSI works and provides information for performing specific tasks in ADSI.</span></span> <span data-ttu-id="f0e0e-118">Рассматриваются следующие темы:</span><span class="sxs-lookup"><span data-stu-id="f0e0e-118">The following topics are discussed:</span></span>

-   [<span data-ttu-id="f0e0e-119">Привязка к объекту ADSI</span><span class="sxs-lookup"><span data-stu-id="f0e0e-119">Binding to an ADSI Object</span></span>](binding-to-an-adsi-object.md)
-   [<span data-ttu-id="f0e0e-120">Создание и удаление объектов</span><span class="sxs-lookup"><span data-stu-id="f0e0e-120">Creating and Deleting Objects</span></span>](creating-and-deleting-objects.md)
-   [<span data-ttu-id="f0e0e-121">Доступ к данным и управление ими с помощью ADSI</span><span class="sxs-lookup"><span data-stu-id="f0e0e-121">Accessing and Manipulating Data with ADSI</span></span>](accessing-and-manipulating-data-with-adsi.md)
-   [<span data-ttu-id="f0e0e-122">Использование схемы ADSI</span><span class="sxs-lookup"><span data-stu-id="f0e0e-122">Using the ADSI Schema</span></span>](using-the-adsi-schema.md)
-   [<span data-ttu-id="f0e0e-123">Коллекции и группы</span><span class="sxs-lookup"><span data-stu-id="f0e0e-123">Collections and Groups</span></span>](collections-and-groups.md)
-   [<span data-ttu-id="f0e0e-124">Перечисление объектов ADSI</span><span class="sxs-lookup"><span data-stu-id="f0e0e-124">Enumerating ADSI Objects</span></span>](enumerating-adsi-objects.md)
-   [<span data-ttu-id="f0e0e-125">Поиск Active Directory</span><span class="sxs-lookup"><span data-stu-id="f0e0e-125">Searching Active Directory</span></span>](searching-active-directory.md)
-   [<span data-ttu-id="f0e0e-126">Модель безопасности ADSI</span><span class="sxs-lookup"><span data-stu-id="f0e0e-126">ADSI Security Model</span></span>](adsi-security-model.md)
-   [<span data-ttu-id="f0e0e-127">Расширения ADSI</span><span class="sxs-lookup"><span data-stu-id="f0e0e-127">ADSI Extensions</span></span>](adsi-extensions.md)
-   [<span data-ttu-id="f0e0e-128">Использование ADSI с Exchange</span><span class="sxs-lookup"><span data-stu-id="f0e0e-128">Using ADSI with Exchange</span></span>](using-adsi-with-exchange.md)
-   [<span data-ttu-id="f0e0e-129">Интерфейсы служебной программы ADSI</span><span class="sxs-lookup"><span data-stu-id="f0e0e-129">ADSI Utility Interfaces</span></span>](adsi-utility-interfaces.md)
-   [<span data-ttu-id="f0e0e-130">Программирование ADSI с помощью Java/COM</span><span class="sxs-lookup"><span data-stu-id="f0e0e-130">Programming ADSI with Java/COM</span></span>](programming-adsi-with-javacom.md)

 

 




