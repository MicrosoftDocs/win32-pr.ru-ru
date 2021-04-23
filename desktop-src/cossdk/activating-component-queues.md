---
description: Активация очередей компонентов
ms.assetid: cfbf7c73-2521-40cf-8c6e-436f64c07e31
title: Активация очередей компонентов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a13dadad287facd5555b4e1ed84fee9f764b1c32
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423321"
---
# <a name="activating-component-queues"></a><span data-ttu-id="b33bb-103">Активация очередей компонентов</span><span class="sxs-lookup"><span data-stu-id="b33bb-103">Activating Component Queues</span></span>

<span data-ttu-id="b33bb-104">Выполнение вызовов метода в компоненте в очереди не приводит к непосредственному выполнению метода.</span><span class="sxs-lookup"><span data-stu-id="b33bb-104">Making method calls on a queued component does not directly execute the method.</span></span> <span data-ttu-id="b33bb-105">Вместо этого [Служба очереди сообщений](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) маршалирует и сохраняет вызовы методов и параметры в очереди, где они затем извлекаются и выполняются компонентом очереди.</span><span class="sxs-lookup"><span data-stu-id="b33bb-105">Rather, [Message Queuing](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) marshals and stores method calls and parameters in a queue where they are later retrieved and executed by the queued component.</span></span> <span data-ttu-id="b33bb-106">В отличие от активации удаленного объекта DCOM, компонент, расположенный в очереди, не создается при вызове метода.</span><span class="sxs-lookup"><span data-stu-id="b33bb-106">Unlike activating a remote DCOM object, the queued component is not instantiated when a method is called.</span></span> <span data-ttu-id="b33bb-107">Это основная идея использования компонентов в очереди — компоненты, помещенные в очередь, не должны создаваться одновременно с вызывающим приложением.</span><span class="sxs-lookup"><span data-stu-id="b33bb-107">This is the basic idea behind using queued components—queued components need not be instantiated at the same time as the calling application.</span></span>

> [!Note]  
> <span data-ttu-id="b33bb-108">В описаниях активации приложения, использующего очереди, предполагается, что приложение помечено как поставленное в очередь, а флажок прослушиватель включен.</span><span class="sxs-lookup"><span data-stu-id="b33bb-108">The descriptions for activating a queued application assume that the application is marked as queued and that the listener check box is enabled.</span></span>

 

<span data-ttu-id="b33bb-109">Можно использовать скрипты для запуска и завершения приложения в очереди.</span><span class="sxs-lookup"><span data-stu-id="b33bb-109">You can use scripting to start and stop a queued application.</span></span> <span data-ttu-id="b33bb-110">Можно разместить скрипт под управлением планировщика заданий, чтобы выполнить его при необходимости.</span><span class="sxs-lookup"><span data-stu-id="b33bb-110">You can put the script under the control of the task scheduler to run it as required.</span></span> <span data-ttu-id="b33bb-111">Например, сценарий может выполняться при перезагрузке системы, если приложения должны быть постоянно доступны.</span><span class="sxs-lookup"><span data-stu-id="b33bb-111">For example, the script can be run on system reboot if the applications are to be permanently available.</span></span> <span data-ttu-id="b33bb-112">Если приложение обрабатывает транзакции в пакетном режиме, сценарий может выполняться в определенное время каждый день в сочетании с сценарием завершения работы, чтобы обеспечить остановку пакетной обработки в определенное время.</span><span class="sxs-lookup"><span data-stu-id="b33bb-112">If the application is to process transactions in batch mode, the script can be run at a certain time each day in conjunction with a shutdown script to be sure the batch processing stops at a specific time.</span></span>

## <a name="component-services-administrative-tool"></a><span data-ttu-id="b33bb-113">Средство администрирования служб компонентов</span><span class="sxs-lookup"><span data-stu-id="b33bb-113">Component Services Administrative Tool</span></span>

<span data-ttu-id="b33bb-114">Чтобы запустить приложение в очереди, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="b33bb-114">To start a queued application, use the following steps:</span></span>

1.  <span data-ttu-id="b33bb-115">В дереве консоли средства администрирования "службы компонентов" в разделе " **службы компонентов**" Откройте папку **приложения COM+** , связанную с компьютером, которым вы хотите управлять.</span><span class="sxs-lookup"><span data-stu-id="b33bb-115">In the console tree of the Component Services administrative tool, under **Component Services**, open the **COM+ Applications** folder associated with the computer you wish to manage.</span></span>

2.  <span data-ttu-id="b33bb-116">Щелкните правой кнопкой мыши приложение, очередь которого требуется активировать.</span><span class="sxs-lookup"><span data-stu-id="b33bb-116">Right-click the application whose queue you want to activate.</span></span>

3.  <span data-ttu-id="b33bb-117">Щелкните **Запуск**.</span><span class="sxs-lookup"><span data-stu-id="b33bb-117">Click **Start**.</span></span>

## <a name="visual-basic"></a><span data-ttu-id="b33bb-118">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="b33bb-118">Visual Basic</span></span>

<span data-ttu-id="b33bb-119">См. пример Комадминкаталог. Стартаппликатион.</span><span class="sxs-lookup"><span data-stu-id="b33bb-119">See the COMAdminCatalog.StartApplication example.</span></span>

## <a name="cc"></a><span data-ttu-id="b33bb-120">C/C++</span><span class="sxs-lookup"><span data-stu-id="b33bb-120">C/C++</span></span>

<span data-ttu-id="b33bb-121">См. пример [**икомадминкаталог:: стартаппликатион**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-startapplication) .</span><span class="sxs-lookup"><span data-stu-id="b33bb-121">See the [**ICOMAdminCatalog::StartApplication**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-startapplication) example.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b33bb-122">См. также</span><span class="sxs-lookup"><span data-stu-id="b33bb-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b33bb-123">Использование моникера очереди</span><span class="sxs-lookup"><span data-stu-id="b33bb-123">Using the Queue Moniker</span></span>](using-the-queue-moniker.md)
</dt> </dl>

 

 



