---
title: Диспетчер потоков
description: Диспетчер потоков является базовым компонентом диспетчера TSF.
ms.assetid: fd43b4c3-80bb-4118-a880-bdea07022c95
keywords:
- Платформа текстовых служб (TSF), диспетчер потоков
- TSF (платформа текстовых служб), диспетчер потоков
- текстовые службы, диспетчер потоков
- Приложения с поддержкой TSF, диспетчер потоков
- Диспетчер потоков
- Диспетчер TSF
- уведомления о событиях
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b29596c5c39267181c6a2c301aede3f15ca7297
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070251"
---
# <a name="thread-manager"></a><span data-ttu-id="6fd85-110">Диспетчер потоков</span><span class="sxs-lookup"><span data-stu-id="6fd85-110">Thread Manager</span></span>

<span data-ttu-id="6fd85-111">Диспетчер потоков является базовым компонентом диспетчера TSF.</span><span class="sxs-lookup"><span data-stu-id="6fd85-111">The thread manager is the base component of the TSF manager.</span></span> <span data-ttu-id="6fd85-112">Диспетчер потоков выполняет стандартные задачи, связанные с приложениями и текстовыми службами (клиентами).</span><span class="sxs-lookup"><span data-stu-id="6fd85-112">The thread manager performs common tasks related to both applications and text services (clients).</span></span> <span data-ttu-id="6fd85-113">Эти задачи включают, но не ограничиваются, активацию и деактивацию текстовых служб TSF, создание диспетчеров документов и обслуживание правильной связи между документами и фокусом ввода.</span><span class="sxs-lookup"><span data-stu-id="6fd85-113">These tasks include, but are not limited to, the activation and deactivation of TSF text services, the creation of document managers, and maintenance of the proper relationship between documents and the input focus.</span></span> <span data-ttu-id="6fd85-114">Диспетчер потоков определяется интерфейсом [ITfThreadMgr](/windows/desktop/api/Msctf/nn-msctf-itfthreadmgr) .</span><span class="sxs-lookup"><span data-stu-id="6fd85-114">The thread manager is defined by the [ITfThreadMgr](/windows/desktop/api/Msctf/nn-msctf-itfthreadmgr) interface.</span></span>

<span data-ttu-id="6fd85-115">Большинство интерфейсов и объектов, предоставляемых диспетчером TSF, можно получить с помощью методов, предоставляемых интерфейсом диспетчера потоков.</span><span class="sxs-lookup"><span data-stu-id="6fd85-115">The majority of the interfaces and objects provided by the TSF manager can be obtained using the methods that the thread manager interface provides.</span></span>

## <a name="applications"></a><span data-ttu-id="6fd85-116">Приложения</span><span class="sxs-lookup"><span data-stu-id="6fd85-116">Applications</span></span>

<span data-ttu-id="6fd85-117">Приложение создает объект диспетчера потоков путем вызова [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) с помощью CLSID \_ тфсреадмгр.</span><span class="sxs-lookup"><span data-stu-id="6fd85-117">An application creates a thread manager object by calling [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) with CLSID\_TFThreadMgr.</span></span>

## <a name="text-services"></a><span data-ttu-id="6fd85-118">Текстовые службы</span><span class="sxs-lookup"><span data-stu-id="6fd85-118">Text Services</span></span>

<span data-ttu-id="6fd85-119">Служба текстового ввода получает объект диспетчера потоков в метод Text службы [итфтекстинпутпроцессор:: Activate](/windows/desktop/api/Msctf/nf-msctf-itftextinputprocessor-activate) .</span><span class="sxs-lookup"><span data-stu-id="6fd85-119">A text service obtains a thread manager object in the text service [ITfTextInputProcessor::Activate](/windows/desktop/api/Msctf/nf-msctf-itftextinputprocessor-activate) method.</span></span>

## <a name="event-notifications"></a><span data-ttu-id="6fd85-120">Уведомления о событиях</span><span class="sxs-lookup"><span data-stu-id="6fd85-120">Event Notifications</span></span>

<span data-ttu-id="6fd85-121">Диспетчер потоков также предоставляет клиентам уведомления о событиях.</span><span class="sxs-lookup"><span data-stu-id="6fd85-121">The thread manager also provides event notification to clients.</span></span> <span data-ttu-id="6fd85-122">В TSF уведомления о событиях предоставляются с помощью приемника событий, который является COM-объектом.</span><span class="sxs-lookup"><span data-stu-id="6fd85-122">In TSF, event notifications are provided by means of an event sink, which is a COM object.</span></span> <span data-ttu-id="6fd85-123">Чтобы получать уведомления от диспетчера потоков, клиент реализует объект [итфсреадмгревентсинк](/windows/desktop/api/Msctf/nn-msctf-itfthreadmgreventsink) и устанавливает приемник событий.</span><span class="sxs-lookup"><span data-stu-id="6fd85-123">To receive notifications from the thread manager, a client implements an [ITfThreadMgrEventSink](/windows/desktop/api/Msctf/nn-msctf-itfthreadmgreventsink) object and installs the event sink.</span></span> <span data-ttu-id="6fd85-124">Приемник событий устанавливается путем запроса диспетчера потоков для IID \_ итфсаурце и вызова [итфсаурце:: ADVISESINK](/windows/desktop/api/Msctf/nf-msctf-itfsource-advisesink) с IID \_ итфсреадмгревентсинк.</span><span class="sxs-lookup"><span data-stu-id="6fd85-124">The event sink is installed by querying the thread manager for IID\_ITfSource and calling [ITfSource::AdviseSink](/windows/desktop/api/Msctf/nf-msctf-itfsource-advisesink) with IID\_ITfThreadMgrEventSink.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6fd85-125">См. также</span><span class="sxs-lookup"><span data-stu-id="6fd85-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6fd85-126">ITfThreadMgr</span><span class="sxs-lookup"><span data-stu-id="6fd85-126">ITfThreadMgr</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfthreadmgr)
</dt> <dt>

[<span data-ttu-id="6fd85-127">CoCreateInstance</span><span class="sxs-lookup"><span data-stu-id="6fd85-127">CoCreateInstance</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)
</dt> <dt>

[<span data-ttu-id="6fd85-128">Итфтекстинпутпроцессор:: Activate</span><span class="sxs-lookup"><span data-stu-id="6fd85-128">ITfTextInputProcessor::Activate</span></span>](/windows/desktop/api/Msctf/nf-msctf-itftextinputprocessor-activate)
</dt> <dt>

[<span data-ttu-id="6fd85-129">итфсреадмгревентсинк</span><span class="sxs-lookup"><span data-stu-id="6fd85-129">ITfThreadMgrEventSink</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfthreadmgreventsink)
</dt> <dt>

[<span data-ttu-id="6fd85-130">Итфсаурце:: AdviseSink</span><span class="sxs-lookup"><span data-stu-id="6fd85-130">ITfSource::AdviseSink</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfsource-advisesink)
</dt> </dl>

 

 