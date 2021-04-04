---
title: Строка привязки
description: Из-за количества объектов, доступных из службы каталогов, могут возникнуть конфликты именования.
ms.assetid: b4c44b19-d7b6-4dde-b44c-4a49cecbacf2
ms.tgt_platform: multiple
keywords:
- Привязка строк ADSI
- ADsPath ADSI, описание
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b13d2d8b58dd01713fa6382f27714b72651ad6f8
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "103987875"
---
# <a name="binding-string"></a><span data-ttu-id="04bcb-105">Строка привязки</span><span class="sxs-lookup"><span data-stu-id="04bcb-105">Binding String</span></span>

<span data-ttu-id="04bcb-106">Из-за количества объектов, доступных из службы каталогов, могут возникнуть конфликты именования.</span><span class="sxs-lookup"><span data-stu-id="04bcb-106">Due to the number of objects accessible from a directory service, naming collisions can occur.</span></span> <span data-ttu-id="04bcb-107">Строка привязки, которая обычно называется ADsPath, позволяет указать конкретный объект, не вызывая конфликтов именования.</span><span class="sxs-lookup"><span data-stu-id="04bcb-107">The binding string, which is commonly referred to as the ADsPath, enables you to specify a particular object without causing a naming collision.</span></span> <span data-ttu-id="04bcb-108">Это можно применить к одному поставщику службы каталогов или нескольким поставщикам служб каталогов.</span><span class="sxs-lookup"><span data-stu-id="04bcb-108">This can be applied for a single directory service provider or across multiple directory service providers.</span></span>

<span data-ttu-id="04bcb-109">ADsPath — это строка, однозначно определяющая объект ADSI в службе каталогов.</span><span class="sxs-lookup"><span data-stu-id="04bcb-109">An ADsPath is a string that uniquely identifies an ADSI object on a directory service.</span></span> <span data-ttu-id="04bcb-110">Поскольку объекты ADSI существуют в контексте пространства имен базовой службы каталогов, часть синтаксиса имени ADsPath зависит от конкретного поставщика.</span><span class="sxs-lookup"><span data-stu-id="04bcb-110">Because ADSI objects exist within the context of the namespace of the underlying directory service, part of the syntax of an ADsPath name is provider-specific.</span></span>

<span data-ttu-id="04bcb-111">В следующей таблице перечислены поставщики ADSI, предоставляемые по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="04bcb-111">The following table lists the ADSI providers provided by default.</span></span>



| <span data-ttu-id="04bcb-112">Поставщик</span><span class="sxs-lookup"><span data-stu-id="04bcb-112">Provider</span></span>         | <span data-ttu-id="04bcb-113">Описание</span><span class="sxs-lookup"><span data-stu-id="04bcb-113">Description</span></span>                                                                                                                                                     |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04bcb-114">WinNT</span><span class="sxs-lookup"><span data-stu-id="04bcb-114">WinNT</span></span><br/> | <span data-ttu-id="04bcb-115">Используется для связи с контроллерами домена Windows.</span><span class="sxs-lookup"><span data-stu-id="04bcb-115">Used to communicate with Windows domain controllers.</span></span> <span data-ttu-id="04bcb-116">Дополнительные сведения о команде WinNT ADsPath см. в разделе [WinNT ADsPath](winnt-adspath.md).</span><span class="sxs-lookup"><span data-stu-id="04bcb-116">For more information about the WinNT ADsPath, see [WinNT ADsPath](winnt-adspath.md).</span></span><br/>           |
| <span data-ttu-id="04bcb-117">LDAP</span><span class="sxs-lookup"><span data-stu-id="04bcb-117">LDAP</span></span><br/>  | <span data-ttu-id="04bcb-118">Используется для связи с серверами LDAP, например Active Directory.</span><span class="sxs-lookup"><span data-stu-id="04bcb-118">Used to communicate with LDAP servers, such as Active Directory.</span></span> <span data-ttu-id="04bcb-119">Дополнительные сведения о LDAP ADsPath см. в разделе [LDAP ADsPath](ldap-adspath.md).</span><span class="sxs-lookup"><span data-stu-id="04bcb-119">For more information about the LDAP ADsPath, see [LDAP ADsPath](ldap-adspath.md).</span></span><br/>  |
| <span data-ttu-id="04bcb-120">ADs</span><span class="sxs-lookup"><span data-stu-id="04bcb-120">ADs</span></span><br/>   | <span data-ttu-id="04bcb-121">Предоставляет реализацию [**иадснамеспацес**](/windows/desktop/api/Iads/nn-iads-iadsnamespaces) , которую можно использовать для перечисления всех поставщиков ADSI, установленных на клиенте.</span><span class="sxs-lookup"><span data-stu-id="04bcb-121">Provides an [**IADsNamespaces**](/windows/desktop/api/Iads/nn-iads-iadsnamespaces) implementation that can be used to enumerate all of the ADSI providers installed on the client.</span></span><br/> |



 

<span data-ttu-id="04bcb-122">Используйте эти имена поставщиков для доступа к пространству имен поставщика по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="04bcb-122">Use these provider names to access the default provider namespace.</span></span> <span data-ttu-id="04bcb-123">Например, если выполнить привязку к LDAP, ADSI привязывается к контейнеру, содержащему объект домена, вошедший в систему.</span><span class="sxs-lookup"><span data-stu-id="04bcb-123">For example, if you bind to LDAP, ADSI binds to a container that contains the domain object currently logged on.</span></span> <span data-ttu-id="04bcb-124">Если выполнить привязку к WinNT, ADSI привязывается к контейнеру, содержащему объекты, которые соответствуют всем доменам в сети.</span><span class="sxs-lookup"><span data-stu-id="04bcb-124">If you bind to WinNT, ADSI binds to a container that holds objects that correlate to all domains on the network.</span></span>

<span data-ttu-id="04bcb-125">Начальными элементами строки ADsPath являются программный идентификатор (progID) поставщика ADSI, за которым следует "://", за которым следует синтаксис, заданный пространством имен поставщика.</span><span class="sxs-lookup"><span data-stu-id="04bcb-125">The initial elements of the ADsPath string are the programmatic identifier (progID) of the ADSI provider, followed by "://", followed by syntax dictated by the provider namespace.</span></span> <span data-ttu-id="04bcb-126">Строка progID может быть или не учитываться с учетом регистра в зависимости от поставщика.</span><span class="sxs-lookup"><span data-stu-id="04bcb-126">The progID string may or may not be case-sensitive, depending on the provider.</span></span> <span data-ttu-id="04bcb-127">Строки progID для поставщиков, перечисленных выше, учитывают регистр.</span><span class="sxs-lookup"><span data-stu-id="04bcb-127">The progID strings for the providers listed above are case-sensitive.</span></span>

<span data-ttu-id="04bcb-128">Строка пути может быть или не учитываться с учетом регистра в зависимости от поставщика.</span><span class="sxs-lookup"><span data-stu-id="04bcb-128">The path string may or may not be case-sensitive, depending on the provider.</span></span> <span data-ttu-id="04bcb-129">Строки пути для поставщиков, перечисленных выше, не учитывают регистр.</span><span class="sxs-lookup"><span data-stu-id="04bcb-129">The path strings for the providers listed above are not case-sensitive.</span></span>

<span data-ttu-id="04bcb-130">Ниже приведены примеры Адспасс.</span><span class="sxs-lookup"><span data-stu-id="04bcb-130">The following are examples of ADsPaths.</span></span>

``` syntax
LDAP://CN=Jeff Smith,CN=users,DC=fabrikam,DC=com
LDAP://server01/CN=Jeff Smith,CN=users,DC=fabrikam,DC=com
 
WinNT://MyDomain/ComputerName,Computer
WinNT://MyDomain/UserAccount
```

<span data-ttu-id="04bcb-131">Чтобы найти все поставщики, установленные на компьютере, выполните привязку к поставщику ADs, как показано в следующем примере кода.</span><span class="sxs-lookup"><span data-stu-id="04bcb-131">To find all providers installed on your computer, bind to the ADs provider as shown in the following code example.</span></span>


```VB
Set x = GetObject("ADs:")
For Each provider In x
    provider.Name
Next
```



<span data-ttu-id="04bcb-132">С помощью поставщика LDAP можно указать значение ADsPath либо в форме различающегося имени X. 500 (DN), начиная с тега CN, либо можно указать его иерархическую инверсию, начиная с тега O.</span><span class="sxs-lookup"><span data-stu-id="04bcb-132">Using the LDAP provider, you can specify the ADsPath either in an X.500 distinguished name (DN) form, starting with the CN tag, or you can specify its hierarchical inverse, starting with the O tag.</span></span> <span data-ttu-id="04bcb-133">Форма, используемая в начальном параметре ADsPath, определяет порядок тегов.</span><span class="sxs-lookup"><span data-stu-id="04bcb-133">The form you use in the initial ADsPath determines the order of the tags.</span></span>

<span data-ttu-id="04bcb-134">В следующей таблице перечислены специальные символы ADsPath.</span><span class="sxs-lookup"><span data-stu-id="04bcb-134">The following table lists ADsPath special characters.</span></span>



| <span data-ttu-id="04bcb-135">Имя</span><span class="sxs-lookup"><span data-stu-id="04bcb-135">Name</span></span>                      | <span data-ttu-id="04bcb-136">Знак</span><span class="sxs-lookup"><span data-stu-id="04bcb-136">Character</span></span>           | <span data-ttu-id="04bcb-137">Описание</span><span class="sxs-lookup"><span data-stu-id="04bcb-137">Description</span></span>                                                                                                                                                                                           |
|---------------------------|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04bcb-138">Двойная кавычка</span><span class="sxs-lookup"><span data-stu-id="04bcb-138">Double quote</span></span><br/>   | <span data-ttu-id="04bcb-139">"</span><span class="sxs-lookup"><span data-stu-id="04bcb-139">"</span></span><br/>        | <span data-ttu-id="04bcb-140">Используется для заключения в кавычки любой части ADsPath, которая может содержать специальный символ, чтобы строка считалась буквальной.</span><span class="sxs-lookup"><span data-stu-id="04bcb-140">Used to quote any part of the ADsPath that may contain a special character so that the string is interpreted literally.</span></span> <span data-ttu-id="04bcb-141">Например, "CN = Name/prefix".</span><span class="sxs-lookup"><span data-stu-id="04bcb-141">For example, "CN=Name/Prefix".</span></span><br/>                                     |
| <span data-ttu-id="04bcb-142">Обратная косая черта</span><span class="sxs-lookup"><span data-stu-id="04bcb-142">Backslash</span></span><br/>      | \\<br/>       | <span data-ttu-id="04bcb-143">Используется для перед специальными символами для обозначения того, что они должны использоваться в качестве литералов.</span><span class="sxs-lookup"><span data-stu-id="04bcb-143">Used to precede special characters to signify they should be used as literals.</span></span> <span data-ttu-id="04bcb-144">Дополнительные сведения и список специальных символов см. в разделе [отличительные имена](/previous-versions/windows/desktop/ldap/distinguished-names).</span><span class="sxs-lookup"><span data-stu-id="04bcb-144">For more information and a list of special characters, see [Distinguished Names](/previous-versions/windows/desktop/ldap/distinguished-names).</span></span><br/> |
| <span data-ttu-id="04bcb-145">Подряд</span><span class="sxs-lookup"><span data-stu-id="04bcb-145">Slash</span></span><br/>          | /<br/>        | <span data-ttu-id="04bcb-146">Разделитель компонентов.</span><span class="sxs-lookup"><span data-stu-id="04bcb-146">Component separator.</span></span><br/>                                                                                                                                                                       |
| <span data-ttu-id="04bcb-147">Угловые скобки</span><span class="sxs-lookup"><span data-stu-id="04bcb-147">Angle brackets</span></span><br/> | <><br/> | <span data-ttu-id="04bcb-148">Разделять путь ADsPath в другом соглашении об именовании.</span><span class="sxs-lookup"><span data-stu-id="04bcb-148">Delimit an ADsPath within another naming convention.</span></span><br/>                                                                                                                                       |



 

<span data-ttu-id="04bcb-149">Чтобы разделить путь ADsPath в спецификации поиска или в составе URL-адреса, используйте левую и правую угловую скобку (< >).</span><span class="sxs-lookup"><span data-stu-id="04bcb-149">To delimit an ADsPath in a search specification or as part of a URL, use the left and right angle bracket (< >).</span></span> <span data-ttu-id="04bcb-150">Например, " &lt; WinNT://mydomain/UserAccount &gt; ".</span><span class="sxs-lookup"><span data-stu-id="04bcb-150">For example, "&lt;WinNT://MyDomain/UserAccount&gt;".</span></span>

<span data-ttu-id="04bcb-151">Некоторые поставщики ADSI могут добавить ограничения синтаксиса из-за требований к пространству имен.</span><span class="sxs-lookup"><span data-stu-id="04bcb-151">Some ADSI providers may have added syntax restrictions due to namespace requirements.</span></span>

## <a name="active-directory-binding-options"></a><span data-ttu-id="04bcb-152">Параметры привязки Active Directory</span><span class="sxs-lookup"><span data-stu-id="04bcb-152">Active Directory Binding Options</span></span>

<span data-ttu-id="04bcb-153">Active Directory предоставляет возможность привязки к объекту с помощью нескольких других типов строк привязки, таких как глобальный уникальный идентификатор (GUID) COM или идентификатор безопасности (SID).</span><span class="sxs-lookup"><span data-stu-id="04bcb-153">Active Directory provides the ability to bind to an object using several other types of binding strings, such as a COM globally unique identifier (GUID) or a security identifier (SID).</span></span> <span data-ttu-id="04bcb-154">Дополнительные сведения см. [в разделе Binding to Active Directory](/windows/desktop/AD/binding-to-active-directory-domain-services).</span><span class="sxs-lookup"><span data-stu-id="04bcb-154">For more information, see [Binding to Active Directory](/windows/desktop/AD/binding-to-active-directory-domain-services).</span></span>

 

