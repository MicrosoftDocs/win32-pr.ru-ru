---
title: Привязка к Well-Known объектам с помощью ВКГУИД
description: В этом разделе показано, как выполнить привязку к объектам с помощью строки привязки ВКГУИД.
ms.assetid: cc9846c4-415e-48ee-ae08-6631636d3a63
ms.tgt_platform: multiple
keywords:
- Привязка к Well-Known объектам с помощью ВКГУИД AD
- Active Directory, использование, привязка, использование ВКГУИД для привязки к хорошо известным объектам
- хорошо известные объекты Active Directory
- хорошо известные объекты AD, привязка к использованию ВКГУИД
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddd919efa6e52d7e65c2a7cd5550f3d217f54070
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "103789636"
---
# <a name="binding-to-well-known-objects-using-wkguid"></a><span data-ttu-id="b877f-107">Привязка к Well-Known объектам с помощью ВКГУИД</span><span class="sxs-lookup"><span data-stu-id="b877f-107">Binding to Well-Known Objects Using WKGUID</span></span>

<span data-ttu-id="b877f-108">Контейнеры могут иметь один или несколько важных подобъектов, которые могут быть переименованы или перемещены.</span><span class="sxs-lookup"><span data-stu-id="b877f-108">Containers can have one, or more, important subobjects that can be renamed or moved.</span></span> <span data-ttu-id="b877f-109">Отслеживание этих подобъектов и создание правильных строк привязки для них может быть затруднено, особенно при их переименовании или перемещении.</span><span class="sxs-lookup"><span data-stu-id="b877f-109">It can be difficult to track these subobjects and build correct binding strings for them, especially if they are renamed or moved.</span></span>

<span data-ttu-id="b877f-110">Для поддержки привязки с переименованием к этим объектам в этих контейнерах службы домен Active Directory имеют два атрибута: **веллкновнобжектс** и **otherWellKnownObjects**.</span><span class="sxs-lookup"><span data-stu-id="b877f-110">To support rename-safe binding to these objects within these containers, Active Directory Domain Services have two attributes: **wellKnownObjects** and **otherWellKnownObjects**.</span></span> <span data-ttu-id="b877f-111">Эти атрибуты имеют синтаксис атрибута АДСТИПЕ \_ DN \_ с \_ двоичными данными.</span><span class="sxs-lookup"><span data-stu-id="b877f-111">These attributes have an attribute syntax of ADSTYPE\_DN\_WITH\_BINARY.</span></span> <span data-ttu-id="b877f-112">Они позволяют использовать несколько значений и содержать кортежи GUID/DN хорошо известных объектов в контейнерах, в которых они заданы.</span><span class="sxs-lookup"><span data-stu-id="b877f-112">They allow multiple values and contain the GUID/DN tuples of well-known objects within the containers on which they are set.</span></span> <span data-ttu-id="b877f-113">Active Directory сервер хранит часть имени каждой записи **веллкновнобжектс** и **otherWellKnownObjects** , чтобы она содержала текущее различающееся имя объекта, указанного при создании записи.</span><span class="sxs-lookup"><span data-stu-id="b877f-113">The Active Directory server maintains the distinguished name portion of each **wellKnownObjects** and **otherWellKnownObjects** entry so that it contains the current distinguished name of the object specified when the entry was created.</span></span>

<span data-ttu-id="b877f-114">Свойство **otherWellKnownObjects** может быть задано и использовано для любого объекта.</span><span class="sxs-lookup"><span data-stu-id="b877f-114">The **otherWellKnownObjects** property can be set and used on any object.</span></span>

<span data-ttu-id="b877f-115">Свойство **веллкновнобжектс** используется в контейнерах домаинднс и Configuration.</span><span class="sxs-lookup"><span data-stu-id="b877f-115">The **wellKnownObjects** property is used on the domainDNS and configuration containers.</span></span> <span data-ttu-id="b877f-116">Свойство **веллкновнобжектс** является системным и может изменяться только операционной системой.</span><span class="sxs-lookup"><span data-stu-id="b877f-116">The **wellKnownObjects** property is a system-only property and can only be modified by the operating system.</span></span>

<span data-ttu-id="b877f-117">Контейнер **домаинднс** имеет следующие хорошо известные объекты:</span><span class="sxs-lookup"><span data-stu-id="b877f-117">The **domainDNS** container has the following well-known objects:</span></span>

-   <span data-ttu-id="b877f-118">Пользователи</span><span class="sxs-lookup"><span data-stu-id="b877f-118">Users</span></span>
-   <span data-ttu-id="b877f-119">Компьютеры</span><span class="sxs-lookup"><span data-stu-id="b877f-119">Computers</span></span>
-   <span data-ttu-id="b877f-120">Система</span><span class="sxs-lookup"><span data-stu-id="b877f-120">System</span></span>
-   <span data-ttu-id="b877f-121">.</span><span class="sxs-lookup"><span data-stu-id="b877f-121">Domain Controllers</span></span>
-   <span data-ttu-id="b877f-122">Инфраструктура</span><span class="sxs-lookup"><span data-stu-id="b877f-122">Infrastructure</span></span>
-   <span data-ttu-id="b877f-123">Удаленные объекты</span><span class="sxs-lookup"><span data-stu-id="b877f-123">Deleted Objects</span></span>
-   <span data-ttu-id="b877f-124">Утеряно и найдено</span><span class="sxs-lookup"><span data-stu-id="b877f-124">Lost and Found</span></span>

<span data-ttu-id="b877f-125">Контейнер конфигурации имеет хорошо известный объект: удаленные объекты.</span><span class="sxs-lookup"><span data-stu-id="b877f-125">The configuration container has the well-known object: Deleted Objects.</span></span>

<span data-ttu-id="b877f-126">Эти объекты находятся в каждом контейнере **домаинднс** и конфигурации в службе домен Active Directory.</span><span class="sxs-lookup"><span data-stu-id="b877f-126">These objects are in every **domainDNS** and configuration container in an Active Directory Domain Service.</span></span>

<span data-ttu-id="b877f-127">Можно выполнить привязку к хорошо известному объекту с помощью формата привязки ВКГУИД.</span><span class="sxs-lookup"><span data-stu-id="b877f-127">You can bind to a well-known object using the WKGUID binding format.</span></span> <span data-ttu-id="b877f-128">Привязка с ВКГУИД поддерживается только в службах домен Active Directory, то есть в поставщике LDAP.</span><span class="sxs-lookup"><span data-stu-id="b877f-128">Binding with WKGUID is only supported in Active Directory Domain Services, that is, the LDAP provider.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b877f-129">Всегда используйте формат привязки ВКГУИД для привязки к известным объектам, как указано выше, в контейнерах домена и конфигурации.</span><span class="sxs-lookup"><span data-stu-id="b877f-129">Always use the WKGUID binding format to bind to the well-known objects, as listed above, in the domain and configuration containers.</span></span> <span data-ttu-id="b877f-130">Это гарантирует, что эти контейнеры могут быть привязаны к, даже если они перемещены или переименованы.</span><span class="sxs-lookup"><span data-stu-id="b877f-130">This ensures that these containers can be bound to even if they are moved or renamed.</span></span>

 

<span data-ttu-id="b877f-131">Формат строки привязки ВКГУИД выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="b877f-131">The WKGUID binding string format is as follows:</span></span>


```C++
LDAP://<servername>/<WKGUID=<XXXXX>,<container DN>>
```



<span data-ttu-id="b877f-132">" &lt; имя сервера &gt; " — это имя сервера каталога.</span><span class="sxs-lookup"><span data-stu-id="b877f-132">"&lt;server name&gt;" is the directory server name.</span></span> <span data-ttu-id="b877f-133">&lt;Имя сервера &gt; является необязательным.</span><span class="sxs-lookup"><span data-stu-id="b877f-133">The "&lt;server name&gt;" is optional.</span></span>

<span data-ttu-id="b877f-134">" &lt; XXXXX &gt; " — это строковое представление шестнадцатеричного значения идентификатора GUID, представляющего хорошо известный объект.</span><span class="sxs-lookup"><span data-stu-id="b877f-134">"&lt;XXXXX&gt;" is the string representation of the hexadecimal value of the GUID that represents the well-known object.</span></span> <span data-ttu-id="b877f-135">Строка GUID указывается в форме "КСКСКСКСКСКСКСКСКСКСКСКСКСКСКСКСКСКСКСКСКСКСКСКСКСКСКСКСКСКСКСКС" и не является той же формой, что и строка GUID, созданная функцией [**StringFromGUID2**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromguid2) , которая принимает форму "{XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX}".</span><span class="sxs-lookup"><span data-stu-id="b877f-135">The GUID string is specified in the "XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX" form and is not the same form as the GUID string produced by the [**StringFromGUID2**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromguid2) function, which takes the form "{XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX}".</span></span> <span data-ttu-id="b877f-136">Дополнительные сведения и пример кода, демонстрирующий создание связываемой строки из GUID, см. в разделе [пример кода для создания связываемого строкового представления GUID](example-code-for-creating-a-bindable-string-representation-of-a-guid.md).</span><span class="sxs-lookup"><span data-stu-id="b877f-136">For more information and a code example that shows how to create a bindable string from a GUID, see [Example Code for Creating a Bindable String Representation of a GUID](example-code-for-creating-a-bindable-string-representation-of-a-guid.md).</span></span>

<span data-ttu-id="b877f-137">Чтобы выполнить привязку к объекту, указанному в **otherWellKnownObjects** в объекте, укажите " &lt; XXXXX &gt; " в качестве строки привязки хорошо известного идентификатора GUID объекта.</span><span class="sxs-lookup"><span data-stu-id="b877f-137">To bind to an object specified in **otherWellKnownObjects** in an object, specify "&lt;XXXXX&gt;" as the bind string form of the well-known object GUID of the object.</span></span> <span data-ttu-id="b877f-138">Дополнительные сведения см. в разделе [Чтение ObjectGUID объекта и создание строкового представления GUID](reading-an-objectampaposs-objectguid-and-creating-a-string-representation-of-the-guid.md).</span><span class="sxs-lookup"><span data-stu-id="b877f-138">For more information, see [Reading an Object's objectGUID and Creating a String Representation of the GUID](reading-an-objectampaposs-objectguid-and-creating-a-string-representation-of-the-guid.md).</span></span> <span data-ttu-id="b877f-139">Дополнительные сведения о задании свойства **otherWellKnownObjects** для объектов см. в разделе [Включение привязки Rename-Safe со свойством otherWellKnownObjects](enabling-rename-safe-binding-with-the-otherwellknownobjects-property.md).</span><span class="sxs-lookup"><span data-stu-id="b877f-139">For more information about setting the **otherWellKnownObjects** property on objects, see [Enabling Rename-Safe Binding with the otherWellKnownObjects Property](enabling-rename-safe-binding-with-the-otherwellknownobjects-property.md).</span></span>

<span data-ttu-id="b877f-140">Чтобы выполнить привязку к объекту, указанному в **веллкновнобжектс** в контейнерах домаинднс или конфигурации, укажите " &lt; XXXXX &gt; " как одну из следующих констант, перечисленных в следующей таблице, как определено в NTDSAPI. h.</span><span class="sxs-lookup"><span data-stu-id="b877f-140">To bind to an object specified in **wellKnownObjects** in domainDNS or configuration containers, specify "&lt;XXXXX&gt;" as one of the following constants, listed in the following table, as defined in Ntdsapi.h.</span></span>



| <span data-ttu-id="b877f-141">Контейнер</span><span class="sxs-lookup"><span data-stu-id="b877f-141">Container</span></span>          | <span data-ttu-id="b877f-142">Идентификатор GUID</span><span class="sxs-lookup"><span data-stu-id="b877f-142">GUID Identifier</span></span>                         |
|--------------------|-----------------------------------------|
| <span data-ttu-id="b877f-143">Пользователи</span><span class="sxs-lookup"><span data-stu-id="b877f-143">Users</span></span>              | <span data-ttu-id="b877f-144">контейнер пользователей с идентификаторами GUID \_ \_ \_ W</span><span class="sxs-lookup"><span data-stu-id="b877f-144">GUID\_USERS\_CONTAINER\_W</span></span>               |
| <span data-ttu-id="b877f-145">Компьютеры</span><span class="sxs-lookup"><span data-stu-id="b877f-145">Computers</span></span>          | <span data-ttu-id="b877f-146">GUID \_ компутрс \_ контейнер \_ W</span><span class="sxs-lookup"><span data-stu-id="b877f-146">GUID\_COMPUTRS\_CONTAINER\_W</span></span>            |
| <span data-ttu-id="b877f-147">Система</span><span class="sxs-lookup"><span data-stu-id="b877f-147">System</span></span>             | <span data-ttu-id="b877f-148">Идентификатор \_ системы GUID, \_ контейнер \_</span><span class="sxs-lookup"><span data-stu-id="b877f-148">GUID\_SYSTEMS\_CONTAINER\_W</span></span>             |
| <span data-ttu-id="b877f-149">.</span><span class="sxs-lookup"><span data-stu-id="b877f-149">Domain Controllers</span></span> | <span data-ttu-id="b877f-150">GUID \_ \_ контроллеров домена, \_ контейнер \_</span><span class="sxs-lookup"><span data-stu-id="b877f-150">GUID\_DOMAIN\_CONTROLLERS\_CONTAINER\_W</span></span> |
| <span data-ttu-id="b877f-151">Инфраструктура</span><span class="sxs-lookup"><span data-stu-id="b877f-151">Infrastructure</span></span>     | <span data-ttu-id="b877f-152">\_контейнер инфраструктуры \_ GUID \_ W</span><span class="sxs-lookup"><span data-stu-id="b877f-152">GUID\_INFRASTRUCTURE\_CONTAINER\_W</span></span>      |
| <span data-ttu-id="b877f-153">Удаленные объекты</span><span class="sxs-lookup"><span data-stu-id="b877f-153">Deleted Objects</span></span>    | <span data-ttu-id="b877f-154">GUID \_ удаленных \_ объектов, \_ контейнер \_</span><span class="sxs-lookup"><span data-stu-id="b877f-154">GUID\_DELETED\_OBJECTS\_CONTAINER\_W</span></span>    |
| <span data-ttu-id="b877f-155">Утеряно и найдено</span><span class="sxs-lookup"><span data-stu-id="b877f-155">Lost and Found</span></span>     | <span data-ttu-id="b877f-156">GUID \_ LOSTANDFOUND \_ контейнера \_ W</span><span class="sxs-lookup"><span data-stu-id="b877f-156">GUID\_LOSTANDFOUND\_CONTAINER\_W</span></span>        |



 

<span data-ttu-id="b877f-157">Например, чтобы выполнить привязку к контейнеру пользователя в домене, укажите **GUID \_ пользователей \_ контейнера \_ W** как " &lt; XXXXX &gt; ".</span><span class="sxs-lookup"><span data-stu-id="b877f-157">For example, to bind to the user container in a domain, specify **GUID\_USERS\_CONTAINER\_W** as "&lt;XXXXX&gt;".</span></span>

<span data-ttu-id="b877f-158">" &lt; DN контейнера &gt; " — это различающееся имя объекта контейнера, в котором этот объект представлен как значение в его свойстве **веллкновнобжектс** .</span><span class="sxs-lookup"><span data-stu-id="b877f-158">"&lt;container DN&gt;" is the distinguished name of the container object that has this object represented as a value in its **wellKnownObjects** property.</span></span> <span data-ttu-id="b877f-159">Например, чтобы выполнить привязку к контейнеру Users в домене, укажите различающееся имя домена в качестве " &lt; различающегося имени контейнера &gt; ".</span><span class="sxs-lookup"><span data-stu-id="b877f-159">For example, to bind to the users container in a domain, specify the domain distinguished name as the "&lt;container DN&gt;".</span></span>

<span data-ttu-id="b877f-160">Например, чтобы выполнить привязку к контейнеру Users Fabrikam.com домена, используйте следующую строку привязки.</span><span class="sxs-lookup"><span data-stu-id="b877f-160">For example, to bind to the users container of the domain Fabrikam.com, use the following binding string.</span></span>

``` syntax
LDAP://<WKGUID=a9d1ca15768811d1aded00c04fd8d5cd,dc=Fabrikam,dc=com>
```

<span data-ttu-id="b877f-161">Дополнительные сведения и пример кода, демонстрирующий привязку к известному идентификатору GUID, см. в разделе [пример кода для привязки к хорошо известным объектам](example-code-for-binding-to-well-known-objects.md).</span><span class="sxs-lookup"><span data-stu-id="b877f-161">For more information and a code example that shows how to bind to a well-known GUID, see [Example Code for Binding to Well Known Objects](example-code-for-binding-to-well-known-objects.md).</span></span>

 

 