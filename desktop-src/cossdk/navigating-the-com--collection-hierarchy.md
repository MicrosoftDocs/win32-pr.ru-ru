---
description: Навигация по иерархии коллекции COM+
ms.assetid: bd72effe-898f-40a6-973c-a26e7fe2478f
title: Навигация по иерархии коллекции COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06fc4cde6c56bc08b0326e892409067759e91be6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673124"
---
# <a name="navigating-the-com-collection-hierarchy"></a><span data-ttu-id="9785c-103">Навигация по иерархии коллекции COM+</span><span class="sxs-lookup"><span data-stu-id="9785c-103">Navigating the COM+ Collection Hierarchy</span></span>

<span data-ttu-id="9785c-104">Некоторые коллекции можно легко получить с помощью метода [**IsCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) объекта [**комадминкаталог**](comadmincatalog.md) .</span><span class="sxs-lookup"><span data-stu-id="9785c-104">Some collections you can retrieve easily by using the [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) method on the [**COMAdminCatalog**](comadmincatalog.md) object.</span></span> <span data-ttu-id="9785c-105">Этот метод получает коллекцию "верхнего уровня"; Это означает, что коллекция, например [**приложения**](applications.md), является собственной и является уникальной и не относящиеся в другую коллекцию.</span><span class="sxs-lookup"><span data-stu-id="9785c-105">This method retrieves a "top-level" collection; that is, a collection such as [**Applications**](applications.md), which stands on its own and which is unique and not logically subsumed under another collection.</span></span>

<span data-ttu-id="9785c-106">Однако многие коллекции логически относящиеся под другой коллекцией, поскольку они содержат элементы, которые являются частью некоторой большой структуры.</span><span class="sxs-lookup"><span data-stu-id="9785c-106">Many collections, however, are logically subsumed under another collection because they contain elements that are part of some larger structure.</span></span> <span data-ttu-id="9785c-107">Например, коллекция [**Components**](components.md) относящиеся или связана с коллекцией [**приложений**](applications.md) , так как она содержит компоненты, установленные в определенном приложении COM+, которое само соответствует элементу в коллекции **приложений** .</span><span class="sxs-lookup"><span data-stu-id="9785c-107">For example, the [**Components**](components.md) collection is subsumed, or related, to the [**Applications**](applications.md) collection because it contains the components installed in a particular COM+ application, which itself corresponds to an item in the **Applications** collection.</span></span> <span data-ttu-id="9785c-108">Связанные коллекции, такие как, не являются уникальными; существует коллекция **компонентов** для каждого отдельного приложения.</span><span class="sxs-lookup"><span data-stu-id="9785c-108">Related collections such as this are not unique; there is a **Components** collection for each distinct application.</span></span>

<span data-ttu-id="9785c-109">Поэтому коллекции упорядочиваются в иерархическую структуру, которая естественным образом соответствует логическим связям между элементами, которые они содержат.</span><span class="sxs-lookup"><span data-stu-id="9785c-109">Therefore, collections are arranged in a hierarchical structure that corresponds naturally to the logical relationships between the items they contain.</span></span> <span data-ttu-id="9785c-110">Схему иерархии коллекции можно найти в [коллекции администрирования com+](com--administration-collections.md).</span><span class="sxs-lookup"><span data-stu-id="9785c-110">A diagram of the collection hierarchy can be found at [COM+ Administration Collections](com--administration-collections.md).</span></span> <span data-ttu-id="9785c-111">Для многих элементов, которые необходимо настроить с помощью объектов Комадмин, необходимо перемещаться по некоторой части иерархии коллекции, чтобы получить соответствующий элемент.</span><span class="sxs-lookup"><span data-stu-id="9785c-111">For many of the elements that you want to configure using the COMAdmin objects, you need to navigate through some portion of the collection hierarchy to retrieve the appropriate item.</span></span>

<span data-ttu-id="9785c-112">На практике это означает, что если требуется получить элемент в связанной коллекции, необходимо сначала пройти все необходимые более высокие уровни, субсуминг коллекции.</span><span class="sxs-lookup"><span data-stu-id="9785c-112">What this means in practice is that if you want to get an item in a related collection, you need to go through all the necessary higher level, subsuming collections first.</span></span> <span data-ttu-id="9785c-113">Чтобы получить связанную коллекцию, необходимо получить конкретный элемент в родительской коллекции, с которой связана Дочерняя коллекция.</span><span class="sxs-lookup"><span data-stu-id="9785c-113">And to retrieve a related collection, you need to retrieve the specific item in the parent collection to which the child collection is related.</span></span> <span data-ttu-id="9785c-114">Например, если требуется настроить элемент, соответствующий компоненту в определенном приложении COM+, необходимо выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="9785c-114">For example, if you want to configure an item corresponding to a component in a particular COM+ application, you must perform the following steps:</span></span>

1.  <span data-ttu-id="9785c-115">Получите коллекцию [**приложений**](applications.md) и заполните ее.</span><span class="sxs-lookup"><span data-stu-id="9785c-115">Get the [**Applications**](applications.md) collection and populate it.</span></span>
2.  <span data-ttu-id="9785c-116">Перечислите содержимое коллекции [**приложений**](applications.md) , чтобы перейти к элементу, соответствующему нужному приложению COM+.</span><span class="sxs-lookup"><span data-stu-id="9785c-116">Enumerate through the contents of the [**Applications**](applications.md) collection until you get to the item corresponding to the correct COM+ application.</span></span>
3.  <span data-ttu-id="9785c-117">Получите и заполните коллекцию [**компонентов**](components.md) для конкретного приложения COM+.</span><span class="sxs-lookup"><span data-stu-id="9785c-117">Get and populate the [**Components**](components.md) collection for that particular COM+ application.</span></span>
4.  <span data-ttu-id="9785c-118">Перечислите содержимое коллекции [**Components**](components.md) , пока не будет получен элемент, соответствующий нужному компоненту.</span><span class="sxs-lookup"><span data-stu-id="9785c-118">Enumerate through the contents of the [**Components**](components.md) collection until you get to the item corresponding to the correct component.</span></span>

<span data-ttu-id="9785c-119">В следующем примере Microsoft Visual Basic показано, как выполнить описанные выше действия.</span><span class="sxs-lookup"><span data-stu-id="9785c-119">The following Microsoft Visual Basic example shows how to perform the preceding steps:</span></span>


```VB
On Error GoTo My_Error_Handler

Dim Catalog As COMAdminCatalog 
Set Catalog = CreateObject("COMAdmin.COMAdminCatalog")

' Get the Applications collection and populate it.
Dim Applications As COMAdminCatalogCollection 
Set Applications = Catalog.GetCollection("Applications") 
Applications.Populate

' Get the correct application, "My Application".
Dim AppObject As COMAdminCatalogObject 
For Each AppObject in Applications 
    If AppObject.Name = "My Application" Then 
        Exit For 
    End If
Next 

' Get and populate the Components collection for "My Application".
Dim Components As COMAdminCatalogCollection 
Set Components = Applications.GetCollection("Components", AppObject.Key) 
Components.Populate

' Get the correct component, "My Component".
Dim CompObject As COMAdminCatalogObject 
For Each CompObject in Components 
    If CompObject.Name = "My Component" Then 
        Exit For 
    End If
Next 

```



<span data-ttu-id="9785c-120">В предыдущем примере используются два различных метода **IsCollection** .</span><span class="sxs-lookup"><span data-stu-id="9785c-120">Two distinct **GetCollection** methods are used in the preceding example.</span></span> <span data-ttu-id="9785c-121">Первый объект предоставляется [**комадминкаталог**](comadmincatalog.md) и используется для получения коллекции верхнего уровня — в данном случае — «Applications».</span><span class="sxs-lookup"><span data-stu-id="9785c-121">The first is exposed by [**COMAdminCatalog**](comadmincatalog.md) and is used to get a top-level collection—in this case, "Applications".</span></span> <span data-ttu-id="9785c-122">Второй объект предоставляется [**комадминкаталогколлектион**](comadmincatalogcollection.md) и используется для получения коллекции, связанной с текущей коллекцией. точно указывается, какая коллекция нужна, передав имя "Components" и значение свойства ключа родительского объекта.</span><span class="sxs-lookup"><span data-stu-id="9785c-122">The second is exposed by [**COMAdminCatalogCollection**](comadmincatalogcollection.md) and is used to get a collection related to the present collection; you indicate precisely which collection you want by passing in the name "Components" and the Key property value of the parent object.</span></span> <span data-ttu-id="9785c-123">Значение ключевого свойства часто является именем или идентификатором GUID, уникальным образом определяющим объект. Это значение определяется в документации по каждой коллекции.</span><span class="sxs-lookup"><span data-stu-id="9785c-123">The Key property value is often a name or a GUID that uniquely identifies the object; this value is identified in the documentation for each collection.</span></span>

<span data-ttu-id="9785c-124">В общем случае необходимо получить связанные коллекции итеративно вниз по иерархии коллекции, пока вы не получите нужную коллекцию.</span><span class="sxs-lookup"><span data-stu-id="9785c-124">In the most general case, you need to get related collections iteratively down the collection hierarchy until you retrieve the collection you want.</span></span> <span data-ttu-id="9785c-125">Действия, которые необходимо выполнить в одной и той же общей модели, повторяются повторно.</span><span class="sxs-lookup"><span data-stu-id="9785c-125">The steps you would take follow the same general model, repetitively.</span></span> <span data-ttu-id="9785c-126">Полный список коллекций см. в разделе [com+ Administration Collections](com--administration-collections.md).</span><span class="sxs-lookup"><span data-stu-id="9785c-126">For a complete list of collections, see [COM+ Administration Collections](com--administration-collections.md).</span></span>

<span data-ttu-id="9785c-127">В некоторых случаях может потребоваться использовать метод ярлыка во второй раз после пути через иерархию коллекции.</span><span class="sxs-lookup"><span data-stu-id="9785c-127">In some cases, you might want to use a shortcut method the second time you follow a path through the collection hierarchy.</span></span> <span data-ttu-id="9785c-128">Этот метод можно использовать только после кэширования всех промежуточных значений ключей.</span><span class="sxs-lookup"><span data-stu-id="9785c-128">You can use this method only after you have already cached all the intervening Key values.</span></span> <span data-ttu-id="9785c-129">Дополнительные сведения см. в разделе [**икомадминкаталог:: жетколлектионбикуери**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollectionbyquery).</span><span class="sxs-lookup"><span data-stu-id="9785c-129">For details, see [**ICOMAdminCatalog::GetCollectionByQuery**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollectionbyquery).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9785c-130">См. также</span><span class="sxs-lookup"><span data-stu-id="9785c-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9785c-131">Заполнение коллекций COM+</span><span class="sxs-lookup"><span data-stu-id="9785c-131">Populating COM+ Collections</span></span>](populating-com--collections.md)
</dt> <dt>

[<span data-ttu-id="9785c-132">Запросы к доступным связанным коллекциям</span><span class="sxs-lookup"><span data-stu-id="9785c-132">Querying for Available Related Collections</span></span>](querying-for-available-related-collections.md)
</dt> <dt>

[<span data-ttu-id="9785c-133">Получение коллекций в каталоге COM+</span><span class="sxs-lookup"><span data-stu-id="9785c-133">Retrieving Collections on the COM+ Catalog</span></span>](retrieving-collections-on-the-com--catalog.md)
</dt> </dl>

 

 



