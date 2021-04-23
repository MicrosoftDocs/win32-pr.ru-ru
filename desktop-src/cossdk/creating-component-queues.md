---
description: Приложение, содержащее по крайней мере один компонент куеуабле, может быть помечено как помещенное в очередь с помощью средства администрирования "службы компонентов".
ms.assetid: 7d9fec63-0bb7-45f3-9d40-736a60d69185
title: Создание очередей компонентов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bc6f6731144a1744a7648d2d3d2bd5c3c4b217b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701211"
---
# <a name="creating-component-queues"></a><span data-ttu-id="3dd8c-103">Создание очередей компонентов</span><span class="sxs-lookup"><span data-stu-id="3dd8c-103">Creating Component Queues</span></span>

<span data-ttu-id="3dd8c-104">Приложение, содержащее по крайней мере один компонент куеуабле, может быть помечено как помещенное в очередь с помощью средства администрирования "службы компонентов".</span><span class="sxs-lookup"><span data-stu-id="3dd8c-104">An application that contains at least one queuable component can be marked as queued using the component services administrative tool.</span></span>

<span data-ttu-id="3dd8c-105">Если приложение помечено как помещенное в очередь, COM+ автоматически создает для него очередь сообщений.</span><span class="sxs-lookup"><span data-stu-id="3dd8c-105">When an application is marked as queued, COM+ automatically creates a message queuing queue for it.</span></span> <span data-ttu-id="3dd8c-106">Имя очереди — это имя приложения; Если имя очереди совпадает с именем существующей очереди, COM+ будет использовать существующую очередь.</span><span class="sxs-lookup"><span data-stu-id="3dd8c-106">The queue name is the name of the application; if the queue name matches the name of an existing queue, COM+ will use the existing queue.</span></span>

> [!Note]  
> <span data-ttu-id="3dd8c-107">Параметр *пути* к очереди сообщений — это сочетание имени удаленного сервера (RSN) и имени приложения COM+.</span><span class="sxs-lookup"><span data-stu-id="3dd8c-107">The Message Queuing *PathName* parameter is a combination of the Remote Server Name (RSN) and the COM+ application name.</span></span> <span data-ttu-id="3dd8c-108">RSN относится к цели удаленной активации.</span><span class="sxs-lookup"><span data-stu-id="3dd8c-108">The RSN refers to the target of a remote activation.</span></span> <span data-ttu-id="3dd8c-109">Параметр RSN указывается во время установки приложения, экспортируемого клиентом, на клиентском компьютере.</span><span class="sxs-lookup"><span data-stu-id="3dd8c-109">You specify an RSN during the installation of a client exportable application on a client computer.</span></span> <span data-ttu-id="3dd8c-110">Процедура установки использует RSN для направления активации на указанный клиентский компьютер.</span><span class="sxs-lookup"><span data-stu-id="3dd8c-110">The installation procedure uses the RSN to direct activation to a specified client computer.</span></span> <span data-ttu-id="3dd8c-111">Дополнительные сведения об именах очередей см. в таблице параметров в подразделе "Параметры моникера очереди" раздела [Использование моникера очереди](using-the-queue-moniker.md).</span><span class="sxs-lookup"><span data-stu-id="3dd8c-111">For more information about queue names, refer to the table of parameters in the "Queue Moniker Parameters" section in [Using the Queue Moniker](using-the-queue-moniker.md).</span></span>

 

## <a name="component-services-administrative-tool"></a><span data-ttu-id="3dd8c-112">Средство администрирования служб компонентов</span><span class="sxs-lookup"><span data-stu-id="3dd8c-112">Component Services Administrative Tool</span></span>

<span data-ttu-id="3dd8c-113">Чтобы указать приложение COM+ в очереди, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="3dd8c-113">To specify a COM+ application as queued, use the following steps:</span></span>

1.  <span data-ttu-id="3dd8c-114">В дереве консоли средства администрирования "службы компонентов" в разделе " **службы компонентов**" Откройте папку **приложения COM+** , связанную с компьютером, которым вы хотите управлять.</span><span class="sxs-lookup"><span data-stu-id="3dd8c-114">In the console tree of the Component Services administrative tool, under **Component Services**, open the **COM+ Applications** folder associated with the computer you wish to manage.</span></span>

2.  <span data-ttu-id="3dd8c-115">Щелкните правой кнопкой мыши приложение, для которого требуется создать очередь, и выберите пункт **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="3dd8c-115">Right-click the application for which you wish to create a queue, and then click **Properties**.</span></span>

3.  <span data-ttu-id="3dd8c-116">Выберите вкладку **очередь** в диалоговом окне Свойства.</span><span class="sxs-lookup"><span data-stu-id="3dd8c-116">Select the **Queuing** tab in the properties dialog.</span></span>

4.  <span data-ttu-id="3dd8c-117">Активируйте флажок с меткой **поставлено в очередь — это приложение может быть достигнуто с помощью очередей MSMQ**.</span><span class="sxs-lookup"><span data-stu-id="3dd8c-117">Activate the check box labeled **Queued – This application can be reached by MSMQ queues**.</span></span>

    > [!Note]  
    > <span data-ttu-id="3dd8c-118">Если флажок в **очереди** неактивен, приложение не содержит компонентов куеуабле.</span><span class="sxs-lookup"><span data-stu-id="3dd8c-118">If the **Queued** check box is grayed out, the application contains no queuable components.</span></span>

     

5.  <span data-ttu-id="3dd8c-119">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="3dd8c-119">Click **OK**.</span></span>

## <a name="visual-basic"></a><span data-ttu-id="3dd8c-120">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="3dd8c-120">Visual Basic</span></span>

<span data-ttu-id="3dd8c-121">Не применяется.</span><span class="sxs-lookup"><span data-stu-id="3dd8c-121">Does not apply.</span></span>

## <a name="cc"></a><span data-ttu-id="3dd8c-122">C/C++</span><span class="sxs-lookup"><span data-stu-id="3dd8c-122">C/C++</span></span>

<span data-ttu-id="3dd8c-123">Не применяется.</span><span class="sxs-lookup"><span data-stu-id="3dd8c-123">Does not apply.</span></span>

## <a name="remarks"></a><span data-ttu-id="3dd8c-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3dd8c-124">Remarks</span></span>

<span data-ttu-id="3dd8c-125">Очереди, созданные библиотекой администрирования COM+ или средством администрирования служб компонентов, помечаются атрибутом транзакционной очереди сообщений.</span><span class="sxs-lookup"><span data-stu-id="3dd8c-125">Queues created by the COM+ Administration Library or the Component Services administrative tool are marked with the Message Queuing transactional attribute.</span></span>

<span data-ttu-id="3dd8c-126">После установки приложения из очереди на сервере его можно сделать доступным для клиентов, экспортировав приложение, а затем импортировав приложение на каждом клиенте.</span><span class="sxs-lookup"><span data-stu-id="3dd8c-126">After a queued application is installed at the server, it can be made available to clients by exporting the application and then importing the application at each client.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3dd8c-127">См. также</span><span class="sxs-lookup"><span data-stu-id="3dd8c-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3dd8c-128">Создание компонентов Куеуабле</span><span class="sxs-lookup"><span data-stu-id="3dd8c-128">Creating Queuable Components</span></span>](creating-queuable-components.md)
</dt> <dt>

[<span data-ttu-id="3dd8c-129">Архитектура очередей компонентов</span><span class="sxs-lookup"><span data-stu-id="3dd8c-129">Queued Components Architecture</span></span>](queued-components-architecture.md)
</dt> </dl>

 

 



