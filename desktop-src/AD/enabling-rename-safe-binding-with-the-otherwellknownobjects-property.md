---
title: Включение привязки Rename-Safe с помощью свойства otherWellKnownObjects
description: Объекты класса Container имеют атрибут otherWellKnownObjects, с помощью которого можно связать идентификатор GUID с различающимся именем (DN) дочернего объекта в контейнере.
ms.assetid: 54f7468b-03e5-46b9-8b43-e3571dccdceb
ms.tgt_platform: multiple
keywords:
- otherWellKnownObjects, свойство
- Свойство otherWellKnownObjects, используемое для переименования, безопасного связывания
- Active Directory, использование, привязка, переименование, безопасного связывания
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7114fa6dfb44625433d8da1c57491a13aefa7cc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104252788"
---
# <a name="enabling-rename-safe-binding-with-the-otherwellknownobjects-property"></a><span data-ttu-id="7c03b-106">Включение привязки Rename-Safe с помощью свойства otherWellKnownObjects</span><span class="sxs-lookup"><span data-stu-id="7c03b-106">Enabling Rename-Safe Binding with the otherWellKnownObjects Property</span></span>

<span data-ttu-id="7c03b-107">Объекты класса Container имеют атрибут **otherWellKnownObjects** , с помощью которого можно связать идентификатор GUID с различающимся именем (DN) дочернего объекта в контейнере.</span><span class="sxs-lookup"><span data-stu-id="7c03b-107">Objects of the Container class have an **otherWellKnownObjects** attribute that you can use to associate a GUID with the distinguished name (DN) of a child object in the container.</span></span> <span data-ttu-id="7c03b-108">Если дочерний объект перемещается или переименовывается, сервер Active Directory обновляет DN в значении **otherWellKnownObjects** для этого дочернего объекта.</span><span class="sxs-lookup"><span data-stu-id="7c03b-108">If the child object is moved or renamed, the Active Directory server updates the DN in the **otherWellKnownObjects** value for that child object.</span></span> <span data-ttu-id="7c03b-109">Это позволяет использовать функцию привязки ВКГУИД для привязки к дочернему объекту с помощью идентификатора GUID и DN контейнера, а не различающегося имени дочернего объекта.</span><span class="sxs-lookup"><span data-stu-id="7c03b-109">This enables use of the WKGUID binding feature to bind to the child object using the GUID and the DN of the container rather than the child object's DN.</span></span>

<span data-ttu-id="7c03b-110">Атрибут **otherWellKnownObjects** эквивалентен атрибуту **веллкновнобжектс** , за исключением того, что приложения и службы могут записывать значение **otherWellKnownObjects** , но только система может записывать **веллкновнобжектс**.</span><span class="sxs-lookup"><span data-stu-id="7c03b-110">The **otherWellKnownObjects** attribute is equivalent to the **wellKnownObjects** attribute except that applications and services can write an **otherWellKnownObjects** value, but only the system can write **wellKnownObjects**.</span></span>

<span data-ttu-id="7c03b-111">Использование атрибута **otherWellKnownObjects** и привязки вкгуид полезно в следующих ситуациях, где требуется переименование привязок в отношении определенного объекта контейнера.</span><span class="sxs-lookup"><span data-stu-id="7c03b-111">Using **otherWellKnownObjects** attribute and WKGUID binding is beneficial in the following situations where rename-safe binding is required in relation to a specific container object.</span></span>

<span data-ttu-id="7c03b-112">Если объект контейнера содержит другие важные объекты или если важные объекты могут быть переименованы или перемещены.</span><span class="sxs-lookup"><span data-stu-id="7c03b-112">If a container object contains other important objects, or if important objects can be renamed or moved.</span></span>

<span data-ttu-id="7c03b-113">Значение, если важные объекты существуют для каждого экземпляра объекта контейнера.</span><span class="sxs-lookup"><span data-stu-id="7c03b-113">If the important objects exist for each instance of the container object.</span></span> <span data-ttu-id="7c03b-114">Например, система использует атрибут **веллкновнобжектс** каждого объекта **домаинднс** для хранения значения для контейнера Users, который существует в каждом экземпляре объекта **домаинднс** .</span><span class="sxs-lookup"><span data-stu-id="7c03b-114">For example, the system uses the **wellKnownObjects** attribute of each **domainDNS** object to store a value for the Users container, which exists in every instance of a **domainDNS** object.</span></span> <span data-ttu-id="7c03b-115">Это позволяет приложениям выполнять привязку к контейнеру пользователей с помощью безопасного переименования путем указания хорошо известного идентификатора GUID и DN контейнера **домаинднс** .</span><span class="sxs-lookup"><span data-stu-id="7c03b-115">This enables applications to bind to the Users container in a rename-safe way by specifying the well-known GUID and the DN of the **domainDNS** container.</span></span> <span data-ttu-id="7c03b-116">Приложения могут использовать атрибут **otherWellKnownObjects** контейнера аналогичным образом.</span><span class="sxs-lookup"><span data-stu-id="7c03b-116">Applications can use a container's **otherWellKnownObjects** attribute similarly.</span></span>

<span data-ttu-id="7c03b-117">Если для важных объектов требуется возможность переименования и (или) поиска.</span><span class="sxs-lookup"><span data-stu-id="7c03b-117">If you require rename-safe binding and/or search capability on the important objects.</span></span>

<span data-ttu-id="7c03b-118">**Добавление безопасного переименования и возможностей поиска**</span><span class="sxs-lookup"><span data-stu-id="7c03b-118">**To add rename-safe binding and search capabilities**</span></span>

1.  <span data-ttu-id="7c03b-119">Добавьте значение в свойство **otherWellKnownObjects** объекта Container при создании важного объекта в этом контейнере.</span><span class="sxs-lookup"><span data-stu-id="7c03b-119">Add a value to the **otherWellKnownObjects** property of the container object when the important object is created within that container.</span></span> <span data-ttu-id="7c03b-120">Значение содержит идентификатор GUID, представляющий хорошо известный объект.</span><span class="sxs-lookup"><span data-stu-id="7c03b-120">The value contains the GUID that represents the well-known object.</span></span> <span data-ttu-id="7c03b-121">Имейте в виду, что это не **атрибут objectGUID** и **distinguishedName** для этого объекта.</span><span class="sxs-lookup"><span data-stu-id="7c03b-121">Be aware that this is not the **objectGUID** and the **distinguishedName** for that object.</span></span>
2.  <span data-ttu-id="7c03b-122">Используйте функцию привязки ВКГУИД для привязки к важному объекту или поиска в нем.</span><span class="sxs-lookup"><span data-stu-id="7c03b-122">Use the WKGUID binding feature to bind to or search the important object.</span></span>

<span data-ttu-id="7c03b-123">Атрибут **otherWellKnownObjects** может иметь несколько значений и содержать кортежи GUID/DN известных объектов в контейнерах, в которых они заданы.</span><span class="sxs-lookup"><span data-stu-id="7c03b-123">The **otherWellKnownObjects** attribute can have multiple values and contains the GUID/DN tuples of well-known objects within the containers on which they are set.</span></span> <span data-ttu-id="7c03b-124">Атрибут **otherWellKnownObjects** имеет синтаксис днвисбинари, в котором значения имеют следующую форму:</span><span class="sxs-lookup"><span data-stu-id="7c03b-124">The **otherWellKnownObjects** attribute has the DNWithBinary syntax in which values have the following form:</span></span>


```C++
B:<char count>:<well known GUID>:<object DN>
```



<span data-ttu-id="7c03b-125">В этом примере " &lt; число символов &gt; " — это число шестнадцатеричных цифр в " &lt; известном идентификаторе GUID &gt; ", которое равно 32 (число шестнадцатеричных цифр в GUID) для **otherWellKnownObjects** и **веллкновнобжектс**.</span><span class="sxs-lookup"><span data-stu-id="7c03b-125">In this example, "&lt;char count&gt;" is the count of hexadecimal digits in "&lt;well known GUID&gt;", which is 32 (number of hex digits in a GUID) for both **otherWellKnownObjects** and **wellKnownObjects**.</span></span> <span data-ttu-id="7c03b-126">" &lt; хорошо известный идентификатор GUID &gt; " — шестнадцатеричное цифровое представление ИЗВЕСТНОГО идентификатора GUID.</span><span class="sxs-lookup"><span data-stu-id="7c03b-126">"&lt;well known GUID&gt;" is the hexadecimal digit representation of the well-known GUID.</span></span> <span data-ttu-id="7c03b-127">" &lt; DN объекта &gt; " — это различающееся имя объекта, представленного этим значением ВКО.</span><span class="sxs-lookup"><span data-stu-id="7c03b-127">"&lt;object DN&gt;" is the distinguished name of the object represented by this WKO value.</span></span> <span data-ttu-id="7c03b-128">Сервер поддерживает ObjectDN часть каждого значения **веллкновнобжектс** и **otherWellKnownObjects** , чтобы она содержала текущее различающееся имя объекта, первоначально указанного при создании значения.</span><span class="sxs-lookup"><span data-stu-id="7c03b-128">The server maintains the ObjectDN portion of each **wellKnownObjects** and **otherWellKnownObjects** value so that it contains the current distinguished name of the object originally specified when the value was created.</span></span>

<span data-ttu-id="7c03b-129">Например, если {df447b5e-aa5b-11d2-8d53-00c04f79ab81} является известным идентификатором GUID объекта MyObject в контейнере MyContainer в домене Fabrikam.com, значение **otherWellKnownObjects** будет указывать известный GUID и различающееся имя для MyObject:</span><span class="sxs-lookup"><span data-stu-id="7c03b-129">For example, if {df447b5e-aa5b-11d2-8d53-00c04f79ab81} is the well-known GUID of the MyObject object in the MyContainer container in the Fabrikam.com domain, the **otherWellKnownObjects** value would specify the well-known GUID and the DN of MyObject:</span></span>


```C++
B:32:df447b5eaa5b11d28d5300c04f79ab81:cn=MyObject,cn=MyContainer,dc=Fabrikam,dc=com
```



<span data-ttu-id="7c03b-130">Чтобы выполнить привязку к этому объекту, используйте следующую строку привязки ВКГУИД, которая указывает известный идентификатор GUID объекта и DN контейнера:</span><span class="sxs-lookup"><span data-stu-id="7c03b-130">To bind to this object, use the following WKGUID binding string that specifies the well-known GUID of the object and the DN of the container:</span></span>


```C++
LDAP://<WKGUID=df447b5eaa5b11d28d5300c04f79ab81,cn=MyContainer,dc=Fabrikam,dc=com>
```



<span data-ttu-id="7c03b-131">После привязки к этому объекту можно использовать интерфейсы COM ADSI для поиска, чтения, изменения или удаления объекта.</span><span class="sxs-lookup"><span data-stu-id="7c03b-131">After binding to this object, you can use the ADSI COM interfaces to search, read, modify, or delete the object.</span></span>

<span data-ttu-id="7c03b-132">Дополнительные сведения и пример кода, демонстрирующий Добавление объекта в атрибут **otherWellKnownObjects** , см. в разделе [пример кода для создания объекта контейнера](example-code-for-creating-a-container-object.md).</span><span class="sxs-lookup"><span data-stu-id="7c03b-132">For more information and a code example that shows how to add an object to the **otherWellKnownObjects** attribute, see [Example Code for Creating a Container Object](example-code-for-creating-a-container-object.md).</span></span>

 

 




