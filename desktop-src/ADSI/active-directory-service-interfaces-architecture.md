---
title: Архитектура интерфейсов служб Active Directory
description: Многие службы каталогов являются иерархическими и, таким образом, предоставляются иерархической объектной модели. В этом разделе используются представления объектов COM для демонстрации различных функций интерфейса ADSI.
ms.assetid: ef545aea-a7a5-4f65-9133-e68b94a86311
ms.tgt_platform: multiple
keywords:
- Интерфейсы ADSI для архитектуры интерфейсов служб Active Directory
- ADSI ADSI, сведения, архитектура
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce59d8d6281aa99bd96efa38166ef658972a5f54
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773031"
---
# <a name="active-directory-service-interfaces-architecture"></a><span data-ttu-id="1d41f-106">Архитектура интерфейсов служб Active Directory</span><span class="sxs-lookup"><span data-stu-id="1d41f-106">Active Directory Service Interfaces Architecture</span></span>

<span data-ttu-id="1d41f-107">Многие службы каталогов являются иерархическими и, таким образом, предоставляются иерархической объектной модели.</span><span class="sxs-lookup"><span data-stu-id="1d41f-107">Many directory services are hierarchical and thus lend themselves to a hierarchical object model.</span></span> <span data-ttu-id="1d41f-108">В этом разделе используются представления объектов COM для демонстрации различных функций интерфейса ADSI.</span><span class="sxs-lookup"><span data-stu-id="1d41f-108">This section uses COM object representations to illustrate various ADSI features.</span></span>

<span data-ttu-id="1d41f-109">На рисунке в следующей модели объектов системный объект верхнего уровня содержит один объект пространства имен для каждого установленного поставщика ADSI.</span><span class="sxs-lookup"><span data-stu-id="1d41f-109">In the following object model figure, a top-level system object contains one Namespace object for every installed ADSI provider.</span></span>

![Объект контейнера пространств имен](images/ds2top.png)

<span data-ttu-id="1d41f-111">Каждый объект пространства имен сам является контейнером, содержащим корневые узлы верхнего уровня для каждого сервера, домена или любых других типов системных объектов каталога, определенных в каждой службе каталогов в качестве корней.</span><span class="sxs-lookup"><span data-stu-id="1d41f-111">Each of the Namespace objects is itself a container that contains the top-level root nodes of every server, domain, or whatever other kinds of directory-system objects are defined as roots in each directory service.</span></span>

<span data-ttu-id="1d41f-112">ADSI предоставляет набор предопределенных объектов и интерфейсов, чтобы клиентские приложения могли взаимодействовать со службами каталогов с помощью унифицированного набора методов.</span><span class="sxs-lookup"><span data-stu-id="1d41f-112">ADSI supplies a set of predefined objects and interfaces so that client applications can interact with directory services using a uniform set of methods.</span></span> <span data-ttu-id="1d41f-113">Однако ADSI может не предоставлять доступ ко всем функциям службы каталогов.</span><span class="sxs-lookup"><span data-stu-id="1d41f-113">However, ADSI may not provide access to all features of a directory service.</span></span> <span data-ttu-id="1d41f-114">Чтобы лучше использовать полный набор функций каждой службы каталогов, ADSI предоставляет модель схемы, которую поставщики услуг каталогов и сторонние поставщики программного обеспечения могут использовать для расширения возможностей за пределами интерфейсов, предоставляемых в ADSI.</span><span class="sxs-lookup"><span data-stu-id="1d41f-114">To better use the full feature set of each directory service, ADSI supplies a schema model that directory service providers and third-party software vendors can use to extend features beyond the interfaces provided in ADSI.</span></span>

<span data-ttu-id="1d41f-115">Объекты контейнера корневого узла, находящиеся внутри каждого объекта пространства имен provider, включают объект контейнера схемы ADSI.</span><span class="sxs-lookup"><span data-stu-id="1d41f-115">The root-node container objects, found within each provider Namespace object, include an ADSI schema container object.</span></span> <span data-ttu-id="1d41f-116">Этот объект содержит определения всех компонентов для этого поставщика.</span><span class="sxs-lookup"><span data-stu-id="1d41f-116">This object contains the definition of all features for that provider.</span></span> <span data-ttu-id="1d41f-117">Дополнительные сведения см. в разделе [модель схемы ADSI](adsi-schema-model.md).</span><span class="sxs-lookup"><span data-stu-id="1d41f-117">For more information, see [ADSI Schema Model](adsi-schema-model.md).</span></span>

<span data-ttu-id="1d41f-118">Этот раздел содержит следующие подразделы:</span><span class="sxs-lookup"><span data-stu-id="1d41f-118">This section includes the following topics:</span></span>

-   [<span data-ttu-id="1d41f-119">Объекты Active Directory интерфейсов служб</span><span class="sxs-lookup"><span data-stu-id="1d41f-119">Active Directory Service Interfaces Objects</span></span>](active-directory-service-interfaces-objects.md)
-   [<span data-ttu-id="1d41f-120">Пространства имен</span><span class="sxs-lookup"><span data-stu-id="1d41f-120">Namespaces</span></span>](namespaces.md)
-   [<span data-ttu-id="1d41f-121">Поставщик интерфейсов служб Active Directory</span><span class="sxs-lookup"><span data-stu-id="1d41f-121">Active Directory Service Interfaces Provider</span></span>](active-directory-service-interfaces-provider.md)
-   [<span data-ttu-id="1d41f-122">Модель схемы ADSI</span><span class="sxs-lookup"><span data-stu-id="1d41f-122">ADSI Schema Model</span></span>](adsi-schema-model.md)

 

 




