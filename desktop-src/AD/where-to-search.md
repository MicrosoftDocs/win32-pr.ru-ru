---
title: Выбор места поиска
description: В этом разделе объясняются различные операции поиска, которые могут быть выполнены в домен Active Directory Services.
ms.assetid: 4b7428c8-c246-41fc-8811-892220c4270f
ms.tgt_platform: multiple
keywords:
- Выбор места поиска в AD
- Active Directory AD, поиск, выбор места поиска
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f24baccd55e263c4d5b677996589ba57c1301e8
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "104336756"
---
# <a name="deciding-where-to-search"></a><span data-ttu-id="72788-105">Выбор места поиска</span><span class="sxs-lookup"><span data-stu-id="72788-105">Deciding Where to Search</span></span>

<span data-ttu-id="72788-106">В этом разделе объясняются различные операции поиска, которые могут быть выполнены в домен Active Directory Services.</span><span class="sxs-lookup"><span data-stu-id="72788-106">This topic explains the different searches that can be performed in Active Directory Domain Services.</span></span>

<span data-ttu-id="72788-107">Все операции поиска выполняются в одном из следующих контекстов именования:</span><span class="sxs-lookup"><span data-stu-id="72788-107">All searches are performed in one of the following naming contexts:</span></span>

-   <span data-ttu-id="72788-108">Домен, включая разделы каталога приложений</span><span class="sxs-lookup"><span data-stu-id="72788-108">Domain, including application directory partitions</span></span>
-   <span data-ttu-id="72788-109">Контейнер схемы</span><span class="sxs-lookup"><span data-stu-id="72788-109">Schema container</span></span>
-   <span data-ttu-id="72788-110">Контейнер конфигурации</span><span class="sxs-lookup"><span data-stu-id="72788-110">Configuration container</span></span>
-   <span data-ttu-id="72788-111">Глобальный каталог</span><span class="sxs-lookup"><span data-stu-id="72788-111">Global catalog</span></span>

## <a name="searching-a-domain"></a><span data-ttu-id="72788-112">Поиск в домене</span><span class="sxs-lookup"><span data-stu-id="72788-112">Searching a Domain</span></span>

<span data-ttu-id="72788-113">Домены содержат большую часть широко используемых объектов, таких как пользователи, контакты, группы, подразделения, компьютеры и т. д.</span><span class="sxs-lookup"><span data-stu-id="72788-113">Domains contain most of the highly used objects such as users, contacts, groups, organizational units, computers, and so on.</span></span> <span data-ttu-id="72788-114">Большинство запросов будут выполнять поиск в домене.</span><span class="sxs-lookup"><span data-stu-id="72788-114">Most queries will search a domain.</span></span> <span data-ttu-id="72788-115">Дополнительные сведения о поиске в домене см. в разделе [Поиск содержимого домена](searching-domain-contents.md).</span><span class="sxs-lookup"><span data-stu-id="72788-115">For more information about searching a domain, see [Searching Domain Contents](searching-domain-contents.md).</span></span>

## <a name="searching-the-schema-container"></a><span data-ttu-id="72788-116">Поиск в контейнере схемы</span><span class="sxs-lookup"><span data-stu-id="72788-116">Searching the Schema Container</span></span>

<span data-ttu-id="72788-117">Контейнер схемы содержит объекты [**classSchema**](/windows/desktop/ADSchema/c-classschema) и [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) , которые предоставляют формальное определение каждого класса и атрибута, которые могут существовать в службах домен Active Directory.</span><span class="sxs-lookup"><span data-stu-id="72788-117">The schema container contains the [**classSchema**](/windows/desktop/ADSchema/c-classschema) and [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) objects that provide the formal definition of every class and attribute that can exist in Active Directory Domain Services.</span></span> <span data-ttu-id="72788-118">Для поиска объектов в контейнере схемы выполните привязку к контейнеру схемы на любом контроллере домена.</span><span class="sxs-lookup"><span data-stu-id="72788-118">To search for objects in the schema container, bind to the schema container on any domain controller.</span></span> <span data-ttu-id="72788-119">Контейнер схемы доступен на всех контроллерах домена.</span><span class="sxs-lookup"><span data-stu-id="72788-119">The schema container is available on all domain controllers.</span></span> <span data-ttu-id="72788-120">Различающееся имя контейнера схемы берется из атрибута **счеманамингконтекст** из RootDSE.</span><span class="sxs-lookup"><span data-stu-id="72788-120">The distinguished name of the schema container is obtained from the **schemaNamingContext** attribute from rootDSE.</span></span> <span data-ttu-id="72788-121">Дополнительные сведения о rootDSE и атрибуте **счеманамингконтекст** см. в разделе [Привязка без сервера и RootDSE](serverless-binding-and-rootdse.md).</span><span class="sxs-lookup"><span data-stu-id="72788-121">For more information about rootDSE and the **schemaNamingContext** attribute, see [Serverless Binding and RootDSE](serverless-binding-and-rootdse.md).</span></span>

<span data-ttu-id="72788-122">Дополнительные сведения о чтении из контейнера схемы или абстрактной схемы см. в разделе [рекомендации по привязке к схеме](guidelines-for-binding-to-the-schema.md).</span><span class="sxs-lookup"><span data-stu-id="72788-122">For more information about reading from the schema or abstract schema container, see [Guidelines for Binding to the Schema](guidelines-for-binding-to-the-schema.md).</span></span>

## <a name="searching-the-configuration-container"></a><span data-ttu-id="72788-123">Поиск в контейнере конфигурации</span><span class="sxs-lookup"><span data-stu-id="72788-123">Searching the Configuration Container</span></span>

<span data-ttu-id="72788-124">Контейнер конфигурации содержит сведения о конфигурации, такие как сайты, службы и описатели экрана для всего леса.</span><span class="sxs-lookup"><span data-stu-id="72788-124">The configuration container contains configuration information, such as sites, services and display specifiers, for the entire forest.</span></span> <span data-ttu-id="72788-125">Чтобы найти объекты в контейнере конфигурации, выполните привязку к контейнеру конфигурации на любом контроллере домена.</span><span class="sxs-lookup"><span data-stu-id="72788-125">To search for objects in the configuration container, bind to the configuration container on any domain controller.</span></span> <span data-ttu-id="72788-126">Контейнер конфигурации доступен на всех контроллерах домена.</span><span class="sxs-lookup"><span data-stu-id="72788-126">The configuration container is available on all domain controllers.</span></span> <span data-ttu-id="72788-127">Различающееся имя контейнера конфигурации берется из атрибута **конфигуратионнамингконтекст** из RootDSE.</span><span class="sxs-lookup"><span data-stu-id="72788-127">The distinguished name of the configuration container is obtained from the **configurationNamingContext** attribute from rootDSE.</span></span> <span data-ttu-id="72788-128">Дополнительные сведения о rootDSE и атрибуте **конфигуратионнамингконтекст** см. в разделе [Привязка без сервера и RootDSE](serverless-binding-and-rootdse.md).</span><span class="sxs-lookup"><span data-stu-id="72788-128">For more information about rootDSE and the **configurationNamingContext** attribute, see [Serverless Binding and RootDSE](serverless-binding-and-rootdse.md).</span></span>

## <a name="searching-the-global-catalog"></a><span data-ttu-id="72788-129">Поиск в глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="72788-129">Searching the Global Catalog</span></span>

<span data-ttu-id="72788-130">Глобальный каталог содержит реплику каждого объекта в службах домен Active Directory Services, но с небольшим количеством их атрибутов.</span><span class="sxs-lookup"><span data-stu-id="72788-130">The global catalog holds a replica of every object in Active Directory Domain Services, but with only a small number of their attributes.</span></span> <span data-ttu-id="72788-131">Атрибуты в глобальном каталоге чаще всего используются в операциях поиска, таких как имена и фамилии пользователей, имена входа и т. д.</span><span class="sxs-lookup"><span data-stu-id="72788-131">The attributes in the global catalog are those most frequently used in search operations, such as a user's first and last names, login names, and so on.</span></span> <span data-ttu-id="72788-132">Дополнительные сведения о поиске в глобальном каталоге см. [в разделе Поиск в глобальном каталоге](searching-global-catalog-contents.md).</span><span class="sxs-lookup"><span data-stu-id="72788-132">For more information about searching the global catalog, see [Searching the Global Catalog](searching-global-catalog-contents.md).</span></span>

 

 