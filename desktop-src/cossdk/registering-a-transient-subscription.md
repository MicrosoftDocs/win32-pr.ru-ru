---
description: Нельзя задать временные подписки с помощью средства администрирования "службы компонентов". Для создания или обновления временной подписки необходимо использовать административные интерфейсы COM+.
ms.assetid: 28d48d59-abb2-4682-ab54-60b6aa7b31b1
title: Регистрация временной подписки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3fc85f189d14fbe6220d6f3760509e1ba0248a4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141455"
---
# <a name="registering-a-transient-subscription"></a><span data-ttu-id="751d6-104">Регистрация временной подписки</span><span class="sxs-lookup"><span data-stu-id="751d6-104">Registering a Transient Subscription</span></span>

<span data-ttu-id="751d6-105">Временные подписки запрашивают событие для определенного объекта подписчика, который уже существует.</span><span class="sxs-lookup"><span data-stu-id="751d6-105">Transient subscriptions request an event for a specific subscriber object that already exists.</span></span> <span data-ttu-id="751d6-106">Временные подписки хранятся в каталоге COM+, но подписка удаляется при остановке системы событий или операционной системы.</span><span class="sxs-lookup"><span data-stu-id="751d6-106">Transient subscriptions are stored in the COM+ catalog, but the subscription is deleted if the event system or operating system is stopped.</span></span> <span data-ttu-id="751d6-107">В отличие от постоянных подписок, временные подписки привязаны к определенному объекту и хранятся только в системе событий.</span><span class="sxs-lookup"><span data-stu-id="751d6-107">Unlike persistent subscriptions, transient subscriptions are tied to a particular object and are stored only in the event system.</span></span> <span data-ttu-id="751d6-108">Если возникла проблема с системой событий или операционной системой, подписка исчезнет.</span><span class="sxs-lookup"><span data-stu-id="751d6-108">If there is a problem with the event system or operating system, the subscription disappears.</span></span> <span data-ttu-id="751d6-109">Временные подписки могут быть более эффективными, чем постоянные подписки, но необходимо управлять жизненным циклом объектов.</span><span class="sxs-lookup"><span data-stu-id="751d6-109">Transient subscriptions can be more efficient than persistent subscriptions, but you must manage their object life cycles.</span></span>

<span data-ttu-id="751d6-110">Нельзя задать временные подписки с помощью средства администрирования "службы компонентов".</span><span class="sxs-lookup"><span data-stu-id="751d6-110">Transient subscriptions cannot be set by using the Component Services administration tool.</span></span> <span data-ttu-id="751d6-111">Для создания или обновления временной подписки необходимо использовать административные интерфейсы COM+.</span><span class="sxs-lookup"><span data-stu-id="751d6-111">You must use the COM+ administrative interfaces to create or update a transient subscription.</span></span>

## <a name="visual-basic"></a><span data-ttu-id="751d6-112">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="751d6-112">Visual Basic</span></span>

<span data-ttu-id="751d6-113">В следующей процедуре описано, как создать временную подписку с помощью Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="751d6-113">The following procedure describes how to create a transient subscription using Microsoft Visual Basic:</span></span>

1.  <span data-ttu-id="751d6-114">Укажите временную подписку, добавив новую запись в коллекцию [**трансиентсубскриптионс**](transientsubscriptions.md) и задав для свойства Субскриберинтерфаце интерфейс [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) объекта подписчика.</span><span class="sxs-lookup"><span data-stu-id="751d6-114">Specify a subscription as transient by adding a new entry to the [**TransientSubscriptions**](transientsubscriptions.md) collection and setting the SubscriberInterface property to the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface of the subscriber object.</span></span> <span data-ttu-id="751d6-115">События COM+ не создают новый экземпляр объекта подписчика при срабатывании события, а используют указанный вами экземпляр.</span><span class="sxs-lookup"><span data-stu-id="751d6-115">COM+ Events does not create a new instance of the subscriber object when firing an event but instead uses the instance you specify.</span></span> <span data-ttu-id="751d6-116">События COM+ содержат счетчик ссылок для объекта подписчика до тех пор, пока подписка не будет удалена из системы.</span><span class="sxs-lookup"><span data-stu-id="751d6-116">COM+ Events holds a reference count for the subscriber object until the subscription is removed from the system.</span></span>
2.  <span data-ttu-id="751d6-117">Создайте серверное приложение COM+ (exe, DLL или OCX-файл) с объектом, реализующим интерфейсы или методы, на которые необходимо подписываться.</span><span class="sxs-lookup"><span data-stu-id="751d6-117">Create a COM+ server application (an .exe, a .dll, or an .ocx file) with an object that implements the interfaces or methods you want to subscribe to.</span></span>
3.  <span data-ttu-id="751d6-118">Создайте временную подписку с помощью следующего кода, передав идентификатор CLSID объекта [класса событий](the-com--event-class-object.md) и экземпляра объекта подписчика.</span><span class="sxs-lookup"><span data-stu-id="751d6-118">Create your transient subscription using the following code, by passing in the CLSID of the [event class](the-com--event-class-object.md) object and the instance of the subscriber object.</span></span> <span data-ttu-id="751d6-119">С помощью средства администрирования "службы компонентов" можно получить свойство Евентклсид, щелкнув правой кнопкой мыши компонент COM+, выбрав пункт " **Свойства**" и выбрав вкладку " **Общие** ".</span><span class="sxs-lookup"><span data-stu-id="751d6-119">Using the Component Services administrative tool, you can get the EventCLSID property by right-clicking the COM+ component, selecting **Properties**, and selecting the **General** tab.</span></span>

    ``` syntax
    Public Function CreateTransientSubscription( _
      ByVal clsid As String, ByVal objref As Object) As String 
        Dim oCOMAdminCatalog As COMAdmin.COMAdminCatalog
        Dim oTSCol As COMAdminCatalogCollection
        Dim oSubscription As ICatalogObject
        Dim objvar As Variant
        On Error GoTo CreateTransientSubscriptionError
        Set oCOMAdminCatalog = CreateObject("COMAdmin.COMAdminCatalog")
        'Gets the TransientSubscriptions collection
        Set oTSCol = oCOMAdminCatalog.GetCollection( _
          "TransientSubscriptions")
        Set oSubscription = oTSCol.Add
        Set objvar = objref
        oSubscription.Value("SubscriberInterface") = objref
        oSubscription.Value("EventCLSID") = clsid
        oSubscription.Value("Name") = "TransientSubscription"
        oTSCol.SaveChanges
        CreateTransientSubscription = oSubscription.Value("ID")
        Set oSubscription = Nothing
        Set oTSCol = Nothing
        Set oCOMAdminCatalog = Nothing
        Set objvar = Nothing
        Exit Function
    CreateTransientSubscriptionError:
        CreateTransientSubscription = ""
        Err.Raise Err.Number, "[CreateTransientSubscription]" & _
          Err.Source, Err.Description
    End Function
    ```

<span data-ttu-id="751d6-120">В следующем примере показано, как вызвать функцию Креатетрансиентсубскриптион для подписки на интерфейс с именем Истокктиккер, который имеет метод с именем Упдатестокк.</span><span class="sxs-lookup"><span data-stu-id="751d6-120">The following example illustrates how to call the CreateTransientSubscription function to subscribe to an interface called IStockTicker, which has a method called UpdateStock.</span></span>

1.  <span data-ttu-id="751d6-121">Создайте класс событий, который поддерживает интерфейс Истокктиккер с одним методом Упдатестокк.</span><span class="sxs-lookup"><span data-stu-id="751d6-121">Create an event class that supports the interface IStockTicker, which has one method, UpdateStock.</span></span>
2.  <span data-ttu-id="751d6-122">В проекте подписчика добавьте класс, реализующий интерфейс Истокктиккер.</span><span class="sxs-lookup"><span data-stu-id="751d6-122">In your subscriber project, add a class that implements the IStockTicker interface.</span></span>
3.  <span data-ttu-id="751d6-123">Если вы хотите подписываться, выполните следующий код:</span><span class="sxs-lookup"><span data-stu-id="751d6-123">When you want to subscribe execute the following code:</span></span>

    ``` syntax
    Dim oMyTicker As Object
    Dim sSubscriptionID As String
    Set oMyTicker = CreateObject("TheProject.CMyTicker")
    sSubscriptionID = CreateTransientSubscription( _
      "{..CLSID for the Event Class..}", oMyTicker)
    ```

<span data-ttu-id="751d6-124">Функция Креатетрансиентсубскриптион возвращает строку, которая представляет собой идентификатор GUID, который можно использовать в качестве обработчика или файла cookie для последующего отзыва подписки.</span><span class="sxs-lookup"><span data-stu-id="751d6-124">The CreateTransientSubscription function returns a string, which is a GUID that can be used as a handle or a cookie to revoke the subscription later.</span></span> <span data-ttu-id="751d6-125">Чтобы удалить подписку, вызовите метод [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) объекта [**Комадминкаталогколлектион**](comadmincatalogcollection.md) в коллекции [**трансиентсубскриптионс**](transientsubscriptions.md) , передав индекс, соответствующий подписке, с ранее полученным идентификатором GUID.</span><span class="sxs-lookup"><span data-stu-id="751d6-125">To remove the subscription, call the [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) method of [**COMAdminCatalogCollection**](comadmincatalogcollection.md) on the [**TransientSubscriptions**](transientsubscriptions.md) collection, passing in the index corresponding to the subscription with the GUID previously received.</span></span>

## <a name="related-topics"></a><span data-ttu-id="751d6-126">См. также</span><span class="sxs-lookup"><span data-stu-id="751d6-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="751d6-127">Регистрация подписки</span><span class="sxs-lookup"><span data-stu-id="751d6-127">Registering a Subscription</span></span>](registering-a-subscription.md)
</dt> </dl>

 

 
