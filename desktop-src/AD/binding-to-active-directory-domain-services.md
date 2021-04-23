---
title: Привязка к службам домен Active Directory
description: В домен Active Directory Services работа по сопоставлению программного объекта с конкретным объектом служб домен Active Directory Services называется привязкой.
ms.assetid: f48de4d4-c53a-4e40-a34e-4236c3e6cb21
ms.tgt_platform: multiple
keywords:
- Привязка к службам домен Active Directory Active Directory
- Active Directory домен Active Directory Services, привязка к
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f57aef2b2a3c21ac860d05dd1b7a1e1079d1720
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990398"
---
# <a name="binding-to-active-directory-domain-services"></a><span data-ttu-id="f8e9e-105">Привязка к службам домен Active Directory</span><span class="sxs-lookup"><span data-stu-id="f8e9e-105">Binding to Active Directory Domain Services</span></span>

<span data-ttu-id="f8e9e-106">В домен Active Directory Services работа по сопоставлению программного объекта с конкретным объектом служб домен Active Directory Services называется *привязкой*.</span><span class="sxs-lookup"><span data-stu-id="f8e9e-106">In Active Directory Domain Services, the act of associating a programmatic object with a specific Active Directory Domain Services object is known as *binding*.</span></span> <span data-ttu-id="f8e9e-107">Если программный объект, такой как объект [**iAds**](/windows/desktop/api/iads/nn-iads-iads) или [DirectoryEntry](/dotnet/api/system.directoryservices.directoryentry?view=dotnet-plat-ext-3.1&preserve-view=true) , связан с конкретным объектом каталога, программный объект считается *привязанным* к объекту каталога.</span><span class="sxs-lookup"><span data-stu-id="f8e9e-107">When a programmatic object, such as an [**IADs**](/windows/desktop/api/iads/nn-iads-iads) or [DirectoryEntry](/dotnet/api/system.directoryservices.directoryentry?view=dotnet-plat-ext-3.1&preserve-view=true) object, is associated with a specific directory object, the programmatic object is considered to be *bound to* the directory object.</span></span>

## <a name="binding-functions-and-methods"></a><span data-ttu-id="f8e9e-108">Функции и методы привязки</span><span class="sxs-lookup"><span data-stu-id="f8e9e-108">Binding Functions and Methods</span></span>

<span data-ttu-id="f8e9e-109">Метод для программной привязки к объекту Active Directory будет зависеть от используемой технологии программирования.</span><span class="sxs-lookup"><span data-stu-id="f8e9e-109">The method for programmatically binding to an Active Directory object will depend on the programming technology that is used.</span></span> <span data-ttu-id="f8e9e-110">Дополнительные сведения о привязке к объектам в домен Active Directory Services с помощью определенной технологии программирования см. в разделах, перечисленных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="f8e9e-110">For more information about binding to objects in Active Directory Domain Services with a specific programming technology, see the topics listed in the following table.</span></span>



| <span data-ttu-id="f8e9e-111">Технология программирования</span><span class="sxs-lookup"><span data-stu-id="f8e9e-111">Programming technology</span></span>                                                                       | <span data-ttu-id="f8e9e-112">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="f8e9e-112">For more information</span></span>                                                           |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="f8e9e-113">Интерфейсы служб Active Directory</span><span class="sxs-lookup"><span data-stu-id="f8e9e-113">Active Directory Service Interfaces</span></span>](/windows/desktop/ADSI/active-directory-service-interfaces-adsi)         | [<span data-ttu-id="f8e9e-114">Привязка к объекту ADSI</span><span class="sxs-lookup"><span data-stu-id="f8e9e-114">Binding to an ADSI Object</span></span>](/windows/desktop/ADSI/binding-to-an-adsi-object)                    |
| [<span data-ttu-id="f8e9e-115">протокол LDAP</span><span class="sxs-lookup"><span data-stu-id="f8e9e-115">Lightweight Directory Access Protocol</span></span>](/previous-versions/windows/desktop/ldap/lightweight-directory-access-protocol-ldap-api) | [<span data-ttu-id="f8e9e-116">Установка сеанса LDAP</span><span class="sxs-lookup"><span data-stu-id="f8e9e-116">Establishing an LDAP Session</span></span>](/previous-versions/windows/desktop/ldap/establishing-an-ldap-session)              |
| [<span data-ttu-id="f8e9e-117">System.DirectoryServices</span><span class="sxs-lookup"><span data-stu-id="f8e9e-117">System.DirectoryServices</span></span>](/dotnet/api/system.directoryservices)                 | <span data-ttu-id="f8e9e-118">[Привязка к объектам каталога](/previous-versions/ms180840(v=vs.90))</span><span class="sxs-lookup"><span data-stu-id="f8e9e-118">[Binding to Directory Objects](/previous-versions/ms180840(v=vs.90))</span></span> |



 

## <a name="binding-strings"></a><span data-ttu-id="f8e9e-119">Привязка строк</span><span class="sxs-lookup"><span data-stu-id="f8e9e-119">Binding Strings</span></span>

<span data-ttu-id="f8e9e-120">Для всех функций и методов привязки требуется строка привязки.</span><span class="sxs-lookup"><span data-stu-id="f8e9e-120">All bind functions and methods require a binding string.</span></span> <span data-ttu-id="f8e9e-121">Форма строки привязки зависит от поставщика.</span><span class="sxs-lookup"><span data-stu-id="f8e9e-121">The form of the binding string depends on the provider.</span></span> <span data-ttu-id="f8e9e-122">Службы домен Active Directory поддерживаются двумя поставщиками, LDAP и WinNT.</span><span class="sxs-lookup"><span data-stu-id="f8e9e-122">Active Directory Domain Services are supported by two providers, LDAP and WinNT.</span></span>

<span data-ttu-id="f8e9e-123">Начиная с Windows 2000, поставщик LDAP используется для доступа к службам домен Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f8e9e-123">Beginning with Windows 2000, the LDAP provider is used to access Active Directory Domain Services.</span></span> <span data-ttu-id="f8e9e-124">Строка привязки LDAP может принимать одну из следующих форм:</span><span class="sxs-lookup"><span data-stu-id="f8e9e-124">The LDAP binding string can take one of the following forms:</span></span>

-   <span data-ttu-id="f8e9e-125">"LDAP:// <host name> / <object name> "</span><span class="sxs-lookup"><span data-stu-id="f8e9e-125">"LDAP://<host name>/<object name>"</span></span>
-   <span data-ttu-id="f8e9e-126">"GC:// <host name> / <object name> "</span><span class="sxs-lookup"><span data-stu-id="f8e9e-126">"GC://<host name>/<object name>"</span></span>

<span data-ttu-id="f8e9e-127">В приведенных выше примерах "LDAP:" указывает поставщика LDAP.</span><span class="sxs-lookup"><span data-stu-id="f8e9e-127">In the examples above, "LDAP:" specifies the LDAP provider.</span></span> <span data-ttu-id="f8e9e-128">"GC:" использует поставщик LDAP для привязки к службе глобального каталога для выполнения быстрых запросов.</span><span class="sxs-lookup"><span data-stu-id="f8e9e-128">"GC:" uses the LDAP provider to bind to the Global Catalog service to execute fast queries.</span></span>

<span data-ttu-id="f8e9e-129">" &lt; имя узла &gt; " указывает сервер для привязки и является необязательным.</span><span class="sxs-lookup"><span data-stu-id="f8e9e-129">"&lt;host name&gt;" specifies the server to bind to and is optional.</span></span> <span data-ttu-id="f8e9e-130">Если это возможно, не указывайте сервер.</span><span class="sxs-lookup"><span data-stu-id="f8e9e-130">If possible, do not specify a server.</span></span> <span data-ttu-id="f8e9e-131">Также можно выполнить привязку к объекту в другом домене.</span><span class="sxs-lookup"><span data-stu-id="f8e9e-131">It is also possible to bind to an object in a different domain.</span></span> <span data-ttu-id="f8e9e-132">Для этого передайте доменное имя целевого домена (DNS) для " &lt; имя узла &gt; ".</span><span class="sxs-lookup"><span data-stu-id="f8e9e-132">To do this pass the domain naming system (DNS) name of the target domain for "&lt;host name&gt;".</span></span> <span data-ttu-id="f8e9e-133">Например, чтобы выполнить привязку к контейнеру Users в домене Домен2 объекта fabrikam.com, строка привязки будет иметь значение «LDAP://domain2.fabrikam.com/CN=Users,DC=domain2,DC=fabrikam,DC=com».</span><span class="sxs-lookup"><span data-stu-id="f8e9e-133">For example, to bind to the Users container in the domain2 domain of fabrikam.com, the binding string would be "LDAP://domain2.fabrikam.com/CN=Users,DC=domain2,DC=fabrikam,DC=com".</span></span>

<span data-ttu-id="f8e9e-134">" &lt; имя объекта &gt; " представляет конкретный объект в домен Active Directory Services.</span><span class="sxs-lookup"><span data-stu-id="f8e9e-134">"&lt;object name&gt;" represents a specific object in Active Directory Domain Services.</span></span> <span data-ttu-id="f8e9e-135">Имя объекта может быть различающимся именем или идентификатором GUID объекта.</span><span class="sxs-lookup"><span data-stu-id="f8e9e-135">The object name can be a distinguished name or an object GUID.</span></span>

<span data-ttu-id="f8e9e-136">Дополнительные сведения о строках привязки LDAP см. в разделе [LDAP ADsPath](/windows/desktop/ADSI/ldap-adspath).</span><span class="sxs-lookup"><span data-stu-id="f8e9e-136">For more information about LDAP binding strings, see [LDAP ADsPath](/windows/desktop/ADSI/ldap-adspath).</span></span>

<span data-ttu-id="f8e9e-137">Для Windows NT 4,0 поставщик WinNT используется для доступа к данным каталога, таким как пользователи, группы пользователей, компьютеры, службы и другие сетевые объекты в Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="f8e9e-137">For Windows NT 4.0, the WinNT provider is used for access to directory data such as users, user groups, computers, services, and other network objects in the Windows 2000.</span></span> <span data-ttu-id="f8e9e-138">Поставщик WinNT в Windows 2000 и более поздних системах имеет ограниченную функциональность по сравнению с поставщиком LDAP.</span><span class="sxs-lookup"><span data-stu-id="f8e9e-138">The WinNT provider on Windows 2000 and later systems has limited functionality compared to the LDAP provider.</span></span> <span data-ttu-id="f8e9e-139">Дополнительные сведения о строках привязки WinNT см. в разделе [WinNT ADsPath](/windows/desktop/ADSI/winnt-adspath).</span><span class="sxs-lookup"><span data-stu-id="f8e9e-139">For more information about WinNT binding strings, see [WinNT ADsPath](/windows/desktop/ADSI/winnt-adspath).</span></span>

<span data-ttu-id="f8e9e-140">Значение ADsPath "LDAP://" или "GC://" можно использовать для привязки к корню пространства имен.</span><span class="sxs-lookup"><span data-stu-id="f8e9e-140">An ADsPath of "LDAP://" or "GC://" can be used to bind to the root of the namespace.</span></span> <span data-ttu-id="f8e9e-141">При привязке к корню пространства имен указанный объект пространства имен не содержит свойств и содержит объект домена для LDAP и объект контейнера, содержащий частичную реплику всех доменов в лесу для GC.</span><span class="sxs-lookup"><span data-stu-id="f8e9e-141">When bound to the root of the namespace, the supplied namespace object contains no properties and contains the domain object for LDAP and a container object containing a partial replica of all domains in the forest for GC.</span></span>

<span data-ttu-id="f8e9e-142">Дополнительные сведения о привязке в домен Active Directory Services см. в следующих статьях:</span><span class="sxs-lookup"><span data-stu-id="f8e9e-142">For more information about binding in Active Directory Domain Services, see:</span></span>

-   [<span data-ttu-id="f8e9e-143">Бессерверная привязка и RootDSE</span><span class="sxs-lookup"><span data-stu-id="f8e9e-143">Serverless Binding and RootDSE</span></span>](serverless-binding-and-rootdse.md)
-   [<span data-ttu-id="f8e9e-144">Привязка к глобальному каталогу</span><span class="sxs-lookup"><span data-stu-id="f8e9e-144">Binding to the Global Catalog</span></span>](binding-to-the-global-catalog.md)
-   [<span data-ttu-id="f8e9e-145">Использование objectGUID для привязки к объекту</span><span class="sxs-lookup"><span data-stu-id="f8e9e-145">Using objectGUID to Bind to an Object</span></span>](using-objectguid-to-bind-to-an-object.md)
-   [<span data-ttu-id="f8e9e-146">Привязка к Well-Known объектам с помощью ВКГУИД</span><span class="sxs-lookup"><span data-stu-id="f8e9e-146">Binding to Well-Known Objects Using WKGUID</span></span>](binding-to-well-known-objects-using-wkguid.md)
-   [<span data-ttu-id="f8e9e-147">Привязка к объекту с помощью идентификатора безопасности</span><span class="sxs-lookup"><span data-stu-id="f8e9e-147">Binding to an Object Using a SID</span></span>](binding-to-an-object-using-a-sid.md)
-   [<span data-ttu-id="f8e9e-148">Включение привязки Rename-Safe с помощью свойства otherWellKnownObjects</span><span class="sxs-lookup"><span data-stu-id="f8e9e-148">Enabling Rename-Safe Binding with the otherWellKnownObjects Property</span></span>](enabling-rename-safe-binding-with-the-otherwellknownobjects-property.md)
-   [<span data-ttu-id="f8e9e-149">Аутентификация</span><span class="sxs-lookup"><span data-stu-id="f8e9e-149">Authentication</span></span>](authentication.md)

 

 
