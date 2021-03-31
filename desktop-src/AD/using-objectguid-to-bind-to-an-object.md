---
title: Использование objectGUID для привязки к объекту
description: Различающееся имя объекта изменяется при переименовании или перемещении объекта, поэтому различающееся имя не является надежным идентификатором объекта.
ms.assetid: 6c038005-3ecb-4c00-b1a3-a231d3aea64e
ms.tgt_platform: multiple
keywords:
- Использование objectGUID для привязки к объекту Active Directory
- objectGUID Active Directory
- objectGUID AD, использование для привязки к объекту
- Active Directory, использование, привязка, использование objectGUID для привязки к объекту
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 045c6194cf27b1697cc478b547105fb10335c219
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "104069737"
---
# <a name="using-objectguid-to-bind-to-an-object"></a><span data-ttu-id="7b85d-107">Использование objectGUID для привязки к объекту</span><span class="sxs-lookup"><span data-stu-id="7b85d-107">Using objectGUID to Bind to an Object</span></span>

<span data-ttu-id="7b85d-108">Различающееся имя объекта изменяется при переименовании или перемещении объекта, поэтому различающееся имя не является надежным идентификатором объекта.</span><span class="sxs-lookup"><span data-stu-id="7b85d-108">An object distinguished name changes if the object is renamed or moved, therefore the distinguished name is not a reliable object identifier.</span></span> <span data-ttu-id="7b85d-109">В домен Active Directory Services свойство **objectGUID** объекта никогда не изменяется, даже если объект переименован или перемещен.</span><span class="sxs-lookup"><span data-stu-id="7b85d-109">In Active Directory Domain Services, an object's **objectGUID** property never changes, even if the object is renamed or moved.</span></span> <span data-ttu-id="7b85d-110">Дополнительные сведения об **objectGUID** и идентификаторах см. в разделе [имена объектов и удостоверения](object-names-and-identities.md).</span><span class="sxs-lookup"><span data-stu-id="7b85d-110">For more information about **objectGUID** and identifiers, see [Object Names and Identities](object-names-and-identities.md).</span></span>

<span data-ttu-id="7b85d-111">Поставщик Active Directory LDAP предоставляет метод для привязки к объекту с помощью идентификатора GUID объекта.</span><span class="sxs-lookup"><span data-stu-id="7b85d-111">The Active Directory LDAP provider provides a method to bind to an object using the object GUID.</span></span> <span data-ttu-id="7b85d-112">Формат строки привязки выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="7b85d-112">The binding string format is as follows:</span></span>


```C++
LDAP://servername/<GUID=XXXXX>
```



<span data-ttu-id="7b85d-113">В этом примере «ServerName» — это имя сервера каталогов, а «XXXXX» — строковое представление шестнадцатеричного значения GUID.</span><span class="sxs-lookup"><span data-stu-id="7b85d-113">In this example, "servername" is the name of the directory server and "XXXXX" is the string representation of the hexadecimal value of the GUID.</span></span> <span data-ttu-id="7b85d-114">"Servername" является необязательным.</span><span class="sxs-lookup"><span data-stu-id="7b85d-114">The "servername" is optional.</span></span> <span data-ttu-id="7b85d-115">Строка GUID указывается в форме "КСКСКСКСКСКСКСКСКСКСКСКСКСКСКСКСКСКСКСКСКСКСКСКСКСКСКСКСКСКСКСКС".</span><span class="sxs-lookup"><span data-stu-id="7b85d-115">The GUID string is specified in the "XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX" form.</span></span> <span data-ttu-id="7b85d-116">Строка GUID может также иметь форму "XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX", которая является той же формой, что и строка, созданная функцией [**StringFromGUID2**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromguid2) , без окружающих фигурных скобок " {} ".</span><span class="sxs-lookup"><span data-stu-id="7b85d-116">The GUID string can also take the form "XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX", which is the same form as the string produced by the [**StringFromGUID2**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromguid2) function, without the surrounding braces "{}".</span></span> <span data-ttu-id="7b85d-117">Дополнительные сведения и пример кода, демонстрирующий создание связываемой строки из GUID, см. в разделе [пример кода для создания связываемого строкового представления GUID](example-code-for-creating-a-bindable-string-representation-of-a-guid.md).</span><span class="sxs-lookup"><span data-stu-id="7b85d-117">For more information and a code example that shows how to create a bindable string from a GUID, see [Example Code for Creating a Bindable String Representation of a GUID](example-code-for-creating-a-bindable-string-representation-of-a-guid.md).</span></span> <span data-ttu-id="7b85d-118">Свойство [**iAds. GUID**](/windows/desktop/ADSI/iads-property-methods) можно использовать для получения правильной строки идентификатора GUID.</span><span class="sxs-lookup"><span data-stu-id="7b85d-118">The [**IADs.GUID**](/windows/desktop/ADSI/iads-property-methods) property can be used to retrieve the proper string form of the GUID.</span></span>

<span data-ttu-id="7b85d-119">При привязке с использованием идентификатора GUID объекта некоторые методы и свойства метода [**iAds**](/windows/desktop/api/iads/nn-iads-iads) и [**иадсконтаинер**](/windows/desktop/api/iads/nn-iads-iadscontainer) не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="7b85d-119">When binding using the object GUID, some [**IADs**](/windows/desktop/api/iads/nn-iads-iads) and [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) methods and properties are not supported.</span></span> <span data-ttu-id="7b85d-120">Следующие свойства **iAds** не поддерживаются объектами, полученными при помощи привязки с использованием идентификатора GUID объекта:</span><span class="sxs-lookup"><span data-stu-id="7b85d-120">The following **IADs** properties are not supported by objects obtained by binding using the object GUID:</span></span>

-   [<span data-ttu-id="7b85d-121">**Действитель**</span><span class="sxs-lookup"><span data-stu-id="7b85d-121">**ADsPath**</span></span>](/windows/desktop/ADSI/iads-property-methods)
-   [<span data-ttu-id="7b85d-122">**Имя**</span><span class="sxs-lookup"><span data-stu-id="7b85d-122">**Name**</span></span>](/windows/desktop/ADSI/iads-property-methods)
-   [<span data-ttu-id="7b85d-123">**Parent**</span><span class="sxs-lookup"><span data-stu-id="7b85d-123">**Parent**</span></span>](/windows/desktop/ADSI/iads-property-methods)

<span data-ttu-id="7b85d-124">Следующие методы **иадсконтаинер** не поддерживаются объектами, полученными при помощи привязки с использованием идентификатора GUID объекта:</span><span class="sxs-lookup"><span data-stu-id="7b85d-124">The following **IADsContainer** methods are not supported by objects obtained by binding using the object GUID:</span></span>

-   [<span data-ttu-id="7b85d-125">**GetObject**</span><span class="sxs-lookup"><span data-stu-id="7b85d-125">**GetObject**</span></span>](/windows/desktop/api/iads/nf-iads-iadscontainer-getobject)
-   [<span data-ttu-id="7b85d-126">**Создать**</span><span class="sxs-lookup"><span data-stu-id="7b85d-126">**Create**</span></span>](/windows/desktop/api/iads/nf-iads-iadscontainer-create)
-   [<span data-ttu-id="7b85d-127">**Удалить**</span><span class="sxs-lookup"><span data-stu-id="7b85d-127">**Delete**</span></span>](/windows/desktop/api/iads/nf-iads-iadscontainer-delete)
-   [<span data-ttu-id="7b85d-128">**копихере**</span><span class="sxs-lookup"><span data-stu-id="7b85d-128">**CopyHere**</span></span>](/windows/desktop/api/iads/nf-iads-iadscontainer-copyhere)
-   [<span data-ttu-id="7b85d-129">**мовехере**</span><span class="sxs-lookup"><span data-stu-id="7b85d-129">**MoveHere**</span></span>](/windows/desktop/api/iads/nf-iads-iadscontainer-movehere)

<span data-ttu-id="7b85d-130">Чтобы использовать эти методы и свойства после привязки к объекту с помощью идентификатора GUID объекта, используйте метод [**iAds. Get**](/windows/desktop/api/iads/nf-iads-iads-get) , чтобы получить различающееся имя объекта, а затем используйте различающееся имя для повторной привязки к объекту.</span><span class="sxs-lookup"><span data-stu-id="7b85d-130">To use these methods and properties after binding to an object using the object GUID, use the [**IADs.Get**](/windows/desktop/api/iads/nf-iads-iads-get) method to retrieve the object distinguished name and then use the distinguished name to bind to the object again.</span></span>

<span data-ttu-id="7b85d-131">Если приложение хранит или кэширует идентификаторы или ссылки на объекты, хранящиеся в домен Active Directory Services, идентификатор GUID объекта лучше использовать по нескольким причинам:</span><span class="sxs-lookup"><span data-stu-id="7b85d-131">If an application stores or caches identifiers or references to objects stored in Active Directory Domain Services, the object GUID is the best identifier to use for several reasons:</span></span>

-   <span data-ttu-id="7b85d-132">Свойство **objectGUID** объекта On не изменяется даже при переименовании или перемещении объекта.</span><span class="sxs-lookup"><span data-stu-id="7b85d-132">The **objectGUID** property of on object never changes even if the object is renamed or moved.</span></span>
-   <span data-ttu-id="7b85d-133">Можно легко выполнить привязку к объекту с помощью идентификатора GUID объекта.</span><span class="sxs-lookup"><span data-stu-id="7b85d-133">It is easy to bind to the object using the object GUID.</span></span>
-   <span data-ttu-id="7b85d-134">Если объект переименовывается или перемещается, свойство **objectGUID** предоставляет единый идентификатор, который можно использовать для быстрого поиска и идентификации объекта, а не для создания запроса с условиями для всех свойств, которые определяли этот объект.</span><span class="sxs-lookup"><span data-stu-id="7b85d-134">If the object is renamed or moved, the **objectGUID** property provides a single identifier that can be used to quickly find and identify the object rather than having to compose a query that has conditions for all properties that would identify that object.</span></span>

 

 