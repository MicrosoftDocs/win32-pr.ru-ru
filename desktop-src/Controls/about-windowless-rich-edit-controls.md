---
title: О безоконном редактировании элементов управления
description: Безоконный элемент управления "поле ввода", также называемый объектом текстовых служб, является объектом, предоставляющим функциональные возможности элемента управления Rich Edit без предоставления окна.
ms.assetid: 880a704d-776a-49d3-be31-0328af408e3b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc1c8bc685dff5f8ddb041011089a84eb2e12008
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "103987904"
---
# <a name="about-windowless-rich-edit-controls"></a><span data-ttu-id="e25f7-103">О безоконном редактировании элементов управления</span><span class="sxs-lookup"><span data-stu-id="e25f7-103">About Windowless Rich Edit Controls</span></span>

<span data-ttu-id="e25f7-104">Безоконный элемент управления "поле ввода", также называемый объектом текстовых служб, является объектом, предоставляющим функциональные возможности [элемента управления Rich Edit](rich-edit-controls.md) без предоставления окна.</span><span class="sxs-lookup"><span data-stu-id="e25f7-104">A windowless rich edit control, also known as a text services object, is an object that provides the functionality of a [rich edit control](rich-edit-controls.md) without providing the window.</span></span> <span data-ttu-id="e25f7-105">Чтобы обеспечить функциональные возможности окна, например возможность получения сообщений и контекста устройства, в котором он может рисовать, элементы управления безоконное редактирование используют пару интерфейсов: [**итекстсервицес**](/windows/desktop/api/Textserv/nl-textserv-itextservices) и [**итекссост**](/windows/desktop/api/Textserv/nl-textserv-itexthost).</span><span class="sxs-lookup"><span data-stu-id="e25f7-105">To provide the functionality of a window, such as the ability to receive messages and a device context into which it can draw, windowless rich edit controls use a pair of interfaces: [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) and [**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost).</span></span>

<span data-ttu-id="e25f7-106">Чтобы создать безоконный элемент управления "поле ввода", вызовите функцию [**креатетекстсервицес**](/windows/desktop/api/Textserv/nf-textserv-createtextservices) с указателем на реализацию интерфейса [**итекссост**](/windows/desktop/api/Textserv/nl-textserv-itexthost) .</span><span class="sxs-lookup"><span data-stu-id="e25f7-106">To create a windowless rich edit control, call the [**CreateTextServices**](/windows/desktop/api/Textserv/nf-textserv-createtextservices) function with a pointer to your implementation of the [**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost) interface.</span></span> <span data-ttu-id="e25f7-107">**Креатетекстсервицес** возвращает указатель [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , который можно запросить для получения указателя на реализацию [**итекстсервицес**](/windows/desktop/api/Textserv/nl-textserv-itextservices) для элемента управления без окон.</span><span class="sxs-lookup"><span data-stu-id="e25f7-107">**CreateTextServices** returns an [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) pointer that you can query to retrieve a pointer to the [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) implementation of the windowless control.</span></span>

<span data-ttu-id="e25f7-108">Msftedit.dll экспортирует идентификатор интерфейса (IID) с именем **IID \_ итекстсервицес** , который можно использовать для запроса указателя [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) для интерфейса [**итекстсервицес**](/windows/desktop/api/Textserv/nl-textserv-itextservices) .</span><span class="sxs-lookup"><span data-stu-id="e25f7-108">Msftedit.dll exports an interface identifier (IID) called **IID\_ITextServices** that you can use to query the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) pointer for the [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) interface.</span></span> <span data-ttu-id="e25f7-109">В следующем примере показано, как получить **\_ итекстсервицес IID** и использовать его для получения интерфейса **итекстсервицес** .</span><span class="sxs-lookup"><span data-stu-id="e25f7-109">The following example shows how to retrieve **IID\_ITextServices** and use it to get the **ITextServices** interface.</span></span>


```
    .
    .
    .
    HRESULT hr;
    IUnknown* pUnk = NULL;
    ITextServices* pTextServices =  NULL;
    
    // Create an instance of the application-defined object that implements the 
    // ITextHost interface.
    TextHost* pTextHost = new TextHost();
    if (pTextHost == NULL) 
        goto errorHandler;

    // Create an instance of the text services object.
    hr = CreateTextServices(NULL, pTextHost, &pUnk);
    if (FAILED(hr))
        goto errorHandler;
        
    // Retrieve the IID_ITextServices interface identifier from 
    // Msftedit.dll. The hmodRichEdit parameter is a handle to the 
    // Msftedit.dll module retrieved by a previous call to the 
    // GetModuleHandle function.
    IID* pIID_ITS = (IID*) (VOID*) GetProcAddress(hmodRichEdit, 
        "IID_ITextServices");
               
    // Retrieve the ITextServices interface.    
    hr = pUnk->QueryInterface(*pIID_ITS, (void **)&pTextServices);
    if (FAILED(hr))
        goto errorHandler;
     .
     . 
     .   
     
```



<span data-ttu-id="e25f7-110">Msftedit.dll также экспортирует идентификатор интерфейса (IID) с именем **IID \_ итекссост** , который можно использовать аналогичным образом для запроса интерфейса [**итекссост**](/windows/desktop/api/Textserv/nl-textserv-itexthost) .</span><span class="sxs-lookup"><span data-stu-id="e25f7-110">Msftedit.dll also exports an interface identifier (IID) called **IID\_ITextHost** that can be used in a similar manner to query for the [**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost) interface.</span></span>

<span data-ttu-id="e25f7-111">Интерфейс [**итекссост**](/windows/desktop/api/Textserv/nl-textserv-itexthost) содержит методы, управляющие вызовами безоконного вызова для получения сведений о вашем окне.</span><span class="sxs-lookup"><span data-stu-id="e25f7-111">The [**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost) interface has methods that the windowless control calls to retrieve information about your window.</span></span> <span data-ttu-id="e25f7-112">Например, объект текстовых служб вызывает метод [**тксжетдк**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txgetdc) для получения контекста устройства, в котором он может рисовать.</span><span class="sxs-lookup"><span data-stu-id="e25f7-112">For example, the text services object calls the [**TxGetDC**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txgetdc) method to retrieve a device context into which it can draw.</span></span> <span data-ttu-id="e25f7-113">Безоконный элемент управления вызывает метод [**ткснотифи**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txnotify) для отправки уведомлений, таких как подробные сообщения уведомления об изменении, на узел текста.</span><span class="sxs-lookup"><span data-stu-id="e25f7-113">The windowless control calls the [**TxNotify**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txnotify) method to send notifications, such as the rich edit notification messages, to the text host.</span></span> <span data-ttu-id="e25f7-114">Объект служб Text Services вызывает другие методы **итекссост** для запроса размещения текста для выполнения других служб, связанных с окном.</span><span class="sxs-lookup"><span data-stu-id="e25f7-114">The text services object calls other **ITextHost** methods to request the text host to perform other window-related services.</span></span> <span data-ttu-id="e25f7-115">Например, метод [**тксинвалидатерект**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txinvalidaterect) запрашивает у узла текста Добавление прямоугольника в область обновления окна.</span><span class="sxs-lookup"><span data-stu-id="e25f7-115">For example, the [**TxInvalidateRect**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txinvalidaterect) method requests the text host to add a rectangle to the window's update region.</span></span>

<span data-ttu-id="e25f7-116">Стандартный расширенный элемент управления "поле ввода" содержит процедуру окна, которая обрабатывает системные сообщения и сообщения из приложения.</span><span class="sxs-lookup"><span data-stu-id="e25f7-116">A standard rich edit control has a window procedure that processes system messages and messages from your application.</span></span> <span data-ttu-id="e25f7-117">Можно использовать маркер окна элемента управления для отправки ИТ сообщений для выполнения редактирования текста и других операций.</span><span class="sxs-lookup"><span data-stu-id="e25f7-117">You can use the control's window handle to send it messages for performing text editing and other operations.</span></span> <span data-ttu-id="e25f7-118">Но в безоконном элементе управления "поле ввода" не предусмотрена процедура окна для получения и обработки сообщений.</span><span class="sxs-lookup"><span data-stu-id="e25f7-118">But a windowless rich edit control has no window procedure to receive and process messages.</span></span> <span data-ttu-id="e25f7-119">Вместо этого он предоставляет интерфейс [**итекстсервицес**](/windows/desktop/api/Textserv/nl-textserv-itextservices) .</span><span class="sxs-lookup"><span data-stu-id="e25f7-119">Instead, it provides an [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) interface.</span></span> <span data-ttu-id="e25f7-120">Чтобы отправить сообщения в безоконный элемент управления "поле ввода", вызовите метод [**ткссендмессаже**](/windows/desktop/api/Textserv/nf-textserv-itextservices-txsendmessage) .</span><span class="sxs-lookup"><span data-stu-id="e25f7-120">To send messages to a windowless rich edit control, call the [**TxSendMessage**](/windows/desktop/api/Textserv/nf-textserv-itextservices-txsendmessage) method.</span></span> <span data-ttu-id="e25f7-121">Этот метод можно использовать для отправки любого из сообщений с богатыми возможностями редактирования или передачи другим сообщениям, влияющим на элемент управления, например системных сообщений для ввода с клавиатуры или мыши.</span><span class="sxs-lookup"><span data-stu-id="e25f7-121">You can use this method to send any of the rich edit messages or to pass on other messages that affect the control, such as system messages for mouse or keyboard input.</span></span>

<span data-ttu-id="e25f7-122">Также можно создать объект текстовых служб как часть [статистического объекта COM](/windows/desktop/com/aggregation).</span><span class="sxs-lookup"><span data-stu-id="e25f7-122">You can also create the text services object as part of a [COM-aggregated object](/windows/desktop/com/aggregation).</span></span> <span data-ttu-id="e25f7-123">Это упрощает статистическую обработку объекта текстовых служб с помощью объекта модели COM.</span><span class="sxs-lookup"><span data-stu-id="e25f7-123">This makes it easy to aggregate the text services object with a windowless Component Object Model (COM) object.</span></span>

 

 