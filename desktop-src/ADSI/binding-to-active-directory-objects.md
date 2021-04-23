---
title: Привязка к Active Directory объектам
description: Прежде чем продолжить работу с этим сценарием, необходимо понять, как именуются объекты ADSI в Active Directory и как привязать их. Привязка объекта ADSI подключает объект к службе каталогов и позволяет получить доступ к методам объекта.
ms.assetid: 0d8d8f1c-786f-4d87-977c-91a167bcf118
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fa54f2015e0d5663db2917eb27b250f39eb4c0c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067333"
---
# <a name="binding-to-active-directory-objects"></a><span data-ttu-id="a1c45-104">Привязка к Active Directory объектам</span><span class="sxs-lookup"><span data-stu-id="a1c45-104">Binding to Active Directory Objects</span></span>

<span data-ttu-id="a1c45-105">Прежде чем продолжить работу с этим сценарием, необходимо понять, как именуются объекты ADSI в Active Directory и как привязать их.</span><span class="sxs-lookup"><span data-stu-id="a1c45-105">Before you continue with this scenario, you must understand how ADSI objects are named in Active Directory, and how to bind them.</span></span> <span data-ttu-id="a1c45-106">Привязка объекта ADSI подключает объект к службе каталогов и позволяет получить доступ к методам объекта.</span><span class="sxs-lookup"><span data-stu-id="a1c45-106">Binding an ADSI object connects the object with the directory service, and allows you to access the methods of the object.</span></span>

## <a name="adspath"></a><span data-ttu-id="a1c45-107">Действитель</span><span class="sxs-lookup"><span data-stu-id="a1c45-107">ADsPath</span></span>

<span data-ttu-id="a1c45-108">Объект ADSI однозначно идентифицируется его строкой привязки, которая также называется ADsPath.</span><span class="sxs-lookup"><span data-stu-id="a1c45-108">An ADSI object is uniquely identified by its binding string, which is also referred to as an ADsPath.</span></span> <span data-ttu-id="a1c45-109">Путь ADsPath представляет собой сочетание программного идентификатора (progID) поставщика ADSI и различающегося имени (DN) объекта.</span><span class="sxs-lookup"><span data-stu-id="a1c45-109">An ADsPath is a combination of a programmatic identifier (progID) of the ADSI provider, and the distinguished name (DN) of the object.</span></span>

<span data-ttu-id="a1c45-110">Вот формат ADsPath:</span><span class="sxs-lookup"><span data-stu-id="a1c45-110">Here's the format of an ADsPath:</span></span>

<span data-ttu-id="a1c45-111">"progID://DN"</span><span class="sxs-lookup"><span data-stu-id="a1c45-111">"progID://DN"</span></span>

-   <span data-ttu-id="a1c45-112">Погид — программный идентификатор поставщика ADSI, например LDAP или WinNT.</span><span class="sxs-lookup"><span data-stu-id="a1c45-112">pogID — the programmatic identifier of the ADSI provider, such as LDAP or WinNT.</span></span>

-   <span data-ttu-id="a1c45-113">://— отделяет идентификатор progID от DN.</span><span class="sxs-lookup"><span data-stu-id="a1c45-113">:// — separates the progID from the DN.</span></span>

-   <span data-ttu-id="a1c45-114">DN — различающееся имя объекта ADSI, которое является полным путем к объекту, где путь состоит из относительных различающихся имен (Рднс).</span><span class="sxs-lookup"><span data-stu-id="a1c45-114">DN — the distinguished name of the ADSI object, which is the full path of the object, where the path consists of relative distinguished names (RDNs).</span></span>

<span data-ttu-id="a1c45-115">RDN — это имя объекта без пути, которое является уникальным для объектов того же уровня.</span><span class="sxs-lookup"><span data-stu-id="a1c45-115">An RDN is the name of the object without the path, and is unique from its sibling objects.</span></span> <span data-ttu-id="a1c45-116">RDN состоит из идентификатора атрибута и значения, например "DC = Fabrikam", где DC — это атрибут, а Fabrikam — это значение.</span><span class="sxs-lookup"><span data-stu-id="a1c45-116">An RDN consists of an attribute ID and value, such as "DC=Fabrikam", where DC is the attribute, and Fabrikam is the value.</span></span> <span data-ttu-id="a1c45-117">DC — это идентификатор атрибута RDN, который обозначает компонент домена.</span><span class="sxs-lookup"><span data-stu-id="a1c45-117">DC is an RDN attribute ID that stands for domain component.</span></span>

<span data-ttu-id="a1c45-118">Ниже приведен пример ADsPath:</span><span class="sxs-lookup"><span data-stu-id="a1c45-118">Here’s an example of an ADsPath:</span></span>

<span data-ttu-id="a1c45-119">"LDAP://ДК = Fabrikam, DC = com"</span><span class="sxs-lookup"><span data-stu-id="a1c45-119">"LDAP://DC=Fabrikam,DC=Com"</span></span>

## <a name="binding-the-object"></a><span data-ttu-id="a1c45-120">Привязка объекта</span><span class="sxs-lookup"><span data-stu-id="a1c45-120">Binding the object</span></span>

<span data-ttu-id="a1c45-121">Вот как можно привязать объект Domain в этом сценарии:</span><span class="sxs-lookup"><span data-stu-id="a1c45-121">Here's how you can bind the domain object in this scenario:</span></span>


```VB
Set dom = GetObject("LDAP://DC=Fabrikam,DC=Com")
```



<span data-ttu-id="a1c45-122">При выполнении этого примера кода ADSI использует различающееся имя для определения объектов ADSI для привязки.</span><span class="sxs-lookup"><span data-stu-id="a1c45-122">When you run this code example, ADSI uses the DN to determine the ADSI objects to bind.</span></span> <span data-ttu-id="a1c45-123">После того как ADSI привязывает эти объекты, можно получить доступ к их методам.</span><span class="sxs-lookup"><span data-stu-id="a1c45-123">After ADSI binds these objects, you can access their methods.</span></span> <span data-ttu-id="a1c45-124">В предыдущем примере кода объект домена привязывается к [**iAds**](/windows/desktop/api/Iads/nn-iads-iads) и [**иадсконтаинер**](/windows/desktop/api/Iads/nn-iads-iadscontainer).</span><span class="sxs-lookup"><span data-stu-id="a1c45-124">The previous code example binds a domain object to [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) and [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer).</span></span> <span data-ttu-id="a1c45-125">Теперь можно использовать методы в таких интерфейсах, как [**Get**](/windows/desktop/api/Iads/nf-iads-iads-get), [**WHERE**](/windows/desktop/api/Iads/nf-iads-iads-put), [**CREATE**](/windows/desktop/api/Iads/nf-iads-iadscontainer-create), [**Delete**](/windows/desktop/api/Iads/nf-iads-iadscontainer-delete)и [**мовехере**](/windows/desktop/api/Iads/nf-iads-iadscontainer-movehere).</span><span class="sxs-lookup"><span data-stu-id="a1c45-125">You can now use methods on those interfaces such as [**Get**](/windows/desktop/api/Iads/nf-iads-iads-get), [**Put**](/windows/desktop/api/Iads/nf-iads-iads-put), [**Create**](/windows/desktop/api/Iads/nf-iads-iadscontainer-create), [**Delete**](/windows/desktop/api/Iads/nf-iads-iadscontainer-delete), and [**MoveHere**](/windows/desktop/api/Iads/nf-iads-iadscontainer-movehere).</span></span>

<span data-ttu-id="a1c45-126">После привязки объекта домена можно напечатать некоторые его атрибуты:</span><span class="sxs-lookup"><span data-stu-id="a1c45-126">After you bind a domain object, you can print some of its attributes:</span></span>


```VB
Debug.Print dom.Get("Name")
Debug.Print dom.Get("whenCreated")
```



<span data-ttu-id="a1c45-127">Дополнительные сведения о параметре ADsPath см. в разделе [Строка привязки](binding-string.md).</span><span class="sxs-lookup"><span data-stu-id="a1c45-127">For more information about ADsPath, see [Binding String](binding-string.md).</span></span> <span data-ttu-id="a1c45-128">Дополнительные сведения о привязке см. [в разделе Привязка к объекту ADSI](binding-to-an-adsi-object.md).</span><span class="sxs-lookup"><span data-stu-id="a1c45-128">For more information about binding, see [Binding to an ADSI Object](binding-to-an-adsi-object.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a1c45-129">См. также</span><span class="sxs-lookup"><span data-stu-id="a1c45-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a1c45-130">Создание подразделения</span><span class="sxs-lookup"><span data-stu-id="a1c45-130">Creating an Organizational Unit</span></span>](creating-an-organizational-unit.md)
</dt> </dl>

 

 




