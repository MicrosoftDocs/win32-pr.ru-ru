---
title: Привязка к глобальному каталогу
description: Глобальный каталог — это пространство имен, которое содержит данные каталога для всех доменов в лесу.
ms.assetid: c3c131c7-d9dd-4dbd-a909-abd0ffd9f375
ms.tgt_platform: multiple
keywords:
- Привязка к глобальному каталогу Active Directory
- Глобальный каталог Active Directory, привязка к
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08fe40b944130f66617b0c111b361ca51cbef126
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "104069815"
---
# <a name="binding-to-the-global-catalog"></a><span data-ttu-id="0d055-105">Привязка к глобальному каталогу</span><span class="sxs-lookup"><span data-stu-id="0d055-105">Binding to the Global Catalog</span></span>

<span data-ttu-id="0d055-106">Глобальный каталог — это пространство имен, которое содержит данные каталога для всех доменов в лесу.</span><span class="sxs-lookup"><span data-stu-id="0d055-106">The Global Catalog is a namespace that contains directory data for all domains in a forest.</span></span> <span data-ttu-id="0d055-107">Глобальный каталог содержит частичную реплику каждого каталога домена.</span><span class="sxs-lookup"><span data-stu-id="0d055-107">The Global Catalog contains a partial replica of every domain directory.</span></span> <span data-ttu-id="0d055-108">Он содержит запись для каждого объекта в корпоративном лесу, но не содержит все свойства каждого объекта.</span><span class="sxs-lookup"><span data-stu-id="0d055-108">It contains an entry for every object in the enterprise forest, but does not contain all the properties of each object.</span></span> <span data-ttu-id="0d055-109">Вместо этого он содержит только свойства, указанные для включения в глобальный каталог.</span><span class="sxs-lookup"><span data-stu-id="0d055-109">Instead, it contains only the properties specified for inclusion in the Global Catalog.</span></span>

<span data-ttu-id="0d055-110">Глобальный каталог хранится на конкретных серверах в Организации.</span><span class="sxs-lookup"><span data-stu-id="0d055-110">The Global Catalog is stored on specific servers throughout the enterprise.</span></span> <span data-ttu-id="0d055-111">В качестве серверов глобального каталога могут выступать только контроллеры домена.</span><span class="sxs-lookup"><span data-stu-id="0d055-111">Only domain controllers can serve as Global Catalog servers.</span></span> <span data-ttu-id="0d055-112">Администраторы указывают, содержит ли данный контроллер домена глобальный каталог с помощью Active Directory сайтов и диспетчеров служб.</span><span class="sxs-lookup"><span data-stu-id="0d055-112">Administrators indicate whether a given domain controller holds a Global Catalog by using the Active Directory Sites and Services Manager.</span></span>

<span data-ttu-id="0d055-113">Чтобы выполнить привязку к глобальному каталогу с помощью ADSI, используйте моникер "GC:".</span><span class="sxs-lookup"><span data-stu-id="0d055-113">To bind to the Global Catalog with ADSI, use the "GC:" moniker.</span></span>

<span data-ttu-id="0d055-114">Существует два способа привязки к глобальному каталогу для выполнения поиска в лесу:</span><span class="sxs-lookup"><span data-stu-id="0d055-114">There are two ways to bind to the Global Catalog to perform a search in a forest:</span></span>

-   <span data-ttu-id="0d055-115">Выполните привязку к корневому объекту Enterprise для поиска по всем доменам в лесу.</span><span class="sxs-lookup"><span data-stu-id="0d055-115">Bind to the enterprise root object to search across all domains in the forest.</span></span>
-   <span data-ttu-id="0d055-116">Выполните привязку к конкретному объекту для поиска этого объекта и его дочерних элементов.</span><span class="sxs-lookup"><span data-stu-id="0d055-116">Bind to a specific object to search that object and its children.</span></span> <span data-ttu-id="0d055-117">Например, при привязке к домену с двумя доменами, расположенными под ним в дереве доменов леса, можно выполнять поиск по этим трем доменам.</span><span class="sxs-lookup"><span data-stu-id="0d055-117">For example, if you bind to a domain that has two domains beneath it in a domain tree in the forest, you can search across those three domains.</span></span> <span data-ttu-id="0d055-118">Обратите внимание, что различающееся имя объекта, с которым выполняется привязка, точно совпадает с различающимся именем, используемым для привязки к пространству имен «LDAP:».</span><span class="sxs-lookup"><span data-stu-id="0d055-118">Be aware that the distinguished name for the object to bind to is exactly the same as the distinguished name used to bind to the "LDAP:" namespace.</span></span> <span data-ttu-id="0d055-119">Помните, что "LDAP:" является полной репликой одного домена, а "GC:" является частичной репликой всех доменов в лесу.</span><span class="sxs-lookup"><span data-stu-id="0d055-119">Recall that "LDAP:" is a full replica of a single domain and that "GC:" is a partial replica of all domains in the forest.</span></span>

<span data-ttu-id="0d055-120">Как и в случае с моникером "LDAP:", можно использовать бессерверную привязку или привязку к конкретному серверу глобального каталога.</span><span class="sxs-lookup"><span data-stu-id="0d055-120">As with the "LDAP:" moniker, you can use serverless binding or bind to a specific Global Catalog server.</span></span> <span data-ttu-id="0d055-121">При поиске в текущем лесу используйте бессерверную привязку.</span><span class="sxs-lookup"><span data-stu-id="0d055-121">If searching in the current forest, use serverless binding.</span></span> <span data-ttu-id="0d055-122">Однако при поиске в другом лесу укажите либо доменное имя, либо сервер глобального каталога для привязки, как показано в следующих примерах.</span><span class="sxs-lookup"><span data-stu-id="0d055-122">However, if searching in another forest, specify either a domain name or a Global Catalog server to bind to, such as shown in the following examples.</span></span>

<span data-ttu-id="0d055-123">Привяжите с помощью доменного имени:</span><span class="sxs-lookup"><span data-stu-id="0d055-123">Bind using the domain name:</span></span>

``` syntax
GC://fabrikam.com
```

<span data-ttu-id="0d055-124">Привяжите с использованием имени сервера:</span><span class="sxs-lookup"><span data-stu-id="0d055-124">Bind using the server name:</span></span>

``` syntax
GC://servername
```

<span data-ttu-id="0d055-125">Также можно выполнить привязку к конкретному объекту в глобальном каталоге.</span><span class="sxs-lookup"><span data-stu-id="0d055-125">You can also bind to a specific object within the Global Catalog.</span></span> <span data-ttu-id="0d055-126">Чтобы выполнить привязку к объекту Sales в домене Fabrikam, используйте следующий формат.</span><span class="sxs-lookup"><span data-stu-id="0d055-126">To bind to the sales object in the fabrikam domain, use the following format.</span></span>

``` syntax
GC://fabrikam.com/DC=sales,DC=fabrikam,DC=com
```

<span data-ttu-id="0d055-127">Или, чтобы выполнить привязку к объекту Sales на сервере, используйте следующий формат.</span><span class="sxs-lookup"><span data-stu-id="0d055-127">Or, to bind to the sales object on the server, use the following format.</span></span>

``` syntax
GC://servername.fabrikam.com/DC=sales,DC=fabrikam,DC=com
```

<span data-ttu-id="0d055-128">**Поиск по всему лесу**</span><span class="sxs-lookup"><span data-stu-id="0d055-128">**To search the entire forest**</span></span>

1.  <span data-ttu-id="0d055-129">Выполните привязку к корню пространства имен глобального каталога.</span><span class="sxs-lookup"><span data-stu-id="0d055-129">Bind to the root of the Global Catalog namespace.</span></span>
2.  <span data-ttu-id="0d055-130">Перечисление контейнера глобального каталога.</span><span class="sxs-lookup"><span data-stu-id="0d055-130">Enumerate the Global Catalog container.</span></span> <span data-ttu-id="0d055-131">Контейнер глобального каталога содержит один объект, который можно использовать для поиска в целом лесу.</span><span class="sxs-lookup"><span data-stu-id="0d055-131">The Global Catalog container contains a single object that you can use to search the entire forest.</span></span>
3.  <span data-ttu-id="0d055-132">Используйте объект в контейнере для выполнения поиска.</span><span class="sxs-lookup"><span data-stu-id="0d055-132">Use the object in the container to perform the search.</span></span> <span data-ttu-id="0d055-133">В C/C++ вызовите [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) , чтобы получить указатель [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) на объект, чтобы можно было использовать интерфейс **IDirectorySearch** для выполнения поиска.</span><span class="sxs-lookup"><span data-stu-id="0d055-133">In C/C++, call [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) to get an [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) pointer on the object so that you can use the **IDirectorySearch** interface to perform the search.</span></span> <span data-ttu-id="0d055-134">В Visual Basic используйте объект, возвращенный из перечисления в запросе ADO.</span><span class="sxs-lookup"><span data-stu-id="0d055-134">In Visual Basic, use the object returned from the enumeration in your ADO query.</span></span>

<span data-ttu-id="0d055-135">Чтобы перечислить серверы глобального каталога в сайте, выполните поиск по поддереву LDAP "CN = <yoursite> , CN = Sites <DN of the configurationNamingContext> ", используя следующую строку фильтра.</span><span class="sxs-lookup"><span data-stu-id="0d055-135">To enumerate the Global Catalog servers in a site, perform an LDAP subtree search of "cn=<yoursite>,cn=sites,<DN of the configurationNamingContext>", using the following filter string.</span></span>

``` syntax
(&(objectCategory=nTDSDSA)(options:1.2.840.113556.1.4.803:=1))
```

<span data-ttu-id="0d055-136">Этот фильтр использует **\_ \_ бит правила сопоставления LDAP \_ \_ и** оператор правила сопоставления (1.2.840.113556.1.4.803) для поиска объектов **нтдсдса** с установленным битом низкого порядка в битовой маске атрибута **Options** .</span><span class="sxs-lookup"><span data-stu-id="0d055-136">This filter uses the **LDAP\_MATCHING\_RULE\_BIT\_AND** matching rule operator (1.2.840.113556.1.4.803) to find **nTDSDSA** objects that have the low-order bit set in the bitmask of the **options** attribute.</span></span> <span data-ttu-id="0d055-137">Бит низкого порядка, соответствующий **нтдсдса opt, — константа \_ \_ \_ GC** , определенная в NTDSAPI. h, идентифицирует объект **нтдсдса** сервера глобального каталога.</span><span class="sxs-lookup"><span data-stu-id="0d055-137">The low-order bit, which corresponds to the **NTDSDSA\_OPT\_IS\_GC** constant defined in Ntdsapi.h, identifies the **nTDSDSA** object of a Global Catalog server.</span></span> <span data-ttu-id="0d055-138">Дополнительные сведения о правилах сопоставления см. в разделе [синтаксис фильтра поиска](/windows/desktop/ADSI/search-filter-syntax).</span><span class="sxs-lookup"><span data-stu-id="0d055-138">For more information about matching rules, see [Search Filter Syntax](/windows/desktop/ADSI/search-filter-syntax).</span></span>

<span data-ttu-id="0d055-139">Родительским объектом объекта **нтдсдса** является серверный объект, а свойство **dNSHostName** объекта Server — DNS-имя сервера глобального каталога.</span><span class="sxs-lookup"><span data-stu-id="0d055-139">The parent of the **nTDSDSA** object is the server object, and the **dNSHostName** property of the server object is the DNS name of the Global Catalog server.</span></span>

<span data-ttu-id="0d055-140">Нельзя использовать \# определенную константу, например **нтдсдса \_ OPT \_ — это \_** **\_ \_ бит правила сопоставления \_ \_ GC и LDAP и** непосредственно в строке фильтра поиска.</span><span class="sxs-lookup"><span data-stu-id="0d055-140">You cannot use \#define constants such as **NTDSDSA\_OPT\_IS\_GC** and **LDAP\_MATCHING\_RULE\_BIT\_AND** directly in a search filter string.</span></span> <span data-ttu-id="0d055-141">Однако эти константы можно использовать как аргументы для функции, например [**swprintf \_ s**](/windows/win32/api/winuser/nf-winuser-wsprintfa) , чтобы вставить постоянные значения в строку фильтра.</span><span class="sxs-lookup"><span data-stu-id="0d055-141">However, you could use these constants as arguments to a function such as [**swprintf\_s**](/windows/win32/api/winuser/nf-winuser-wsprintfa) to insert the constant values into a filter string.</span></span>

<span data-ttu-id="0d055-142">Глобальный каталог не представляет всю структуру дерева леса.</span><span class="sxs-lookup"><span data-stu-id="0d055-142">The global catalog does not represent the entire forest tree structure.</span></span> <span data-ttu-id="0d055-143">Например, вы можете ожидать, что в следующем примере кода будут перечислены все домены в лесу и все дочерние объекты каждого домена.</span><span class="sxs-lookup"><span data-stu-id="0d055-143">For example, you might expect that the following code example would enumerate all of the domains in the forest and all child objects of each domain.</span></span> <span data-ttu-id="0d055-144">На практике, то, что действительно делает, — перечисляет все домены в лесу, но ни один из перечисляемых объектов домена не содержит дочерних элементов.</span><span class="sxs-lookup"><span data-stu-id="0d055-144">In reality, what it actually does is enumerate all of the domains in the forest, but none of the enumerated domain objects contain any children.</span></span> <span data-ttu-id="0d055-145">Это ограничение глобального каталога.</span><span class="sxs-lookup"><span data-stu-id="0d055-145">This is a limitation of the global catalog.</span></span>


```VB
Dim oGC As IADs
Dim oDomain As IADs
Dim oChild As IADs

Set oGC = GetObject("GC:")
For Each oDomain In oGC
    ' Print the name of the domain.
    Debug.Print oDomain.Name
    
    ' Enumerate the child objects of the domain.
    For Each oChild In oDomain
        Debug.Print oChild.Name
    Next
Next
```



<span data-ttu-id="0d055-146">Чтобы исправить это, необходимо выполнить привязку к каждому объекту домена, а затем перечислить дочерние объекты каждого домена.</span><span class="sxs-lookup"><span data-stu-id="0d055-146">To correct this, it is necessary to bind to each domain object and then enumerate the child objects of each domain.</span></span> <span data-ttu-id="0d055-147">В следующем примере кода показан соответствующий метод.</span><span class="sxs-lookup"><span data-stu-id="0d055-147">The proper technique is shown in the following code example.</span></span>


```VB
Dim oGC As IADs
Dim oDomainEnum As IADs
Dim oDomainBind As IADs
Dim oChild As IADs

Set oGC = GetObject("GC:")
For Each oDomainEnum In oGC
    ' Print the name of the domain.
    Debug.Print oDomainEnum.Name
    
    ' Bind to the domain.
    Set oDomainBind = GetObject("LDAP://" + oDomainEnum.Name)
    
    ' Enumerate the child objects of the domain.
    For Each oChild In oDomainBind
        Debug.Print oChild.Name
    Next
Next
```



<span data-ttu-id="0d055-148">Дополнительные сведения и примеры кода, демонстрирующие Поиск в целом лесу, см. в разделе [пример кода для поиска в лесу](example-code-for-searching-a-forest.md).</span><span class="sxs-lookup"><span data-stu-id="0d055-148">For more information and code examples that show how to search an entire forest, see [Example Code for Searching a Forest](example-code-for-searching-a-forest.md).</span></span>

 

 