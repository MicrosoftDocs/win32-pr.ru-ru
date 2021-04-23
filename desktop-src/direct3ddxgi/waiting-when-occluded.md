---
description: Приложения могут ожидать события, когда отрисовка на экране не требуется (т. е. пока они перекрыто).
ms.assetid: B9EC23C9-A311-4BD9-BBE8-908A1334A541
title: Ожидание события, если подготовка к просмотру не требуется
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b553ef52e812c5117e5d9669ba13b47b9f4280c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105682170"
---
# <a name="waiting-on-an-event-when-rendering-is-unnecessary"></a><span data-ttu-id="3059c-103">Ожидание события, если подготовка к просмотру не требуется</span><span class="sxs-lookup"><span data-stu-id="3059c-103">Waiting on an event when rendering is unnecessary</span></span>

<span data-ttu-id="3059c-104">Приложения могут ожидать события, когда отрисовка на экране не требуется (т. е. пока они перекрыто).</span><span class="sxs-lookup"><span data-stu-id="3059c-104">Apps can wait on an event when rendering to the screen is unnecessary (that is, while they are occluded).</span></span> <span data-ttu-id="3059c-105">Если диспетчер окон рабочего стола (DWM) или приложение перекрыто, то отрисовка не требуется, и операционная система может оставаться в более низких состояниях питания в течение более длительного периода времени.</span><span class="sxs-lookup"><span data-stu-id="3059c-105">When the Desktop Window Manager (DWM) or an app is occluded, no rendering is necessary and the operating system can stay in lower power states for longer periods of time.</span></span> <span data-ttu-id="3059c-106">Это экономит электроэнергию и увеличивает время работы батареи.</span><span class="sxs-lookup"><span data-stu-id="3059c-106">This saves power and extends battery life.</span></span>

<span data-ttu-id="3059c-107">Приложение может ожидать события в следующих случаях:</span><span class="sxs-lookup"><span data-stu-id="3059c-107">An app can wait on an event when:</span></span>

-   <span data-ttu-id="3059c-108">Все мониторы отключены.</span><span class="sxs-lookup"><span data-stu-id="3059c-108">All the monitors are off.</span></span>
-   <span data-ttu-id="3059c-109">Сеанс, в котором выполняется приложение, отключен.</span><span class="sxs-lookup"><span data-stu-id="3059c-109">The session that the app runs in is disconnected.</span></span>
-   <span data-ttu-id="3059c-110">Приложение выполняется в полноэкранном режиме только для одной конфигурации монитора.</span><span class="sxs-lookup"><span data-stu-id="3059c-110">The app runs in full screen exclusively on a single monitor configuration.</span></span>
-   <span data-ttu-id="3059c-111">Приложение выполняется на рабочем столе, отличном от рабочего стола Active Desktop и не имеет разрешения на подготовку к просмотру на активном рабочем столе.</span><span class="sxs-lookup"><span data-stu-id="3059c-111">The app runs on a different desktop than the active desktop and does not have permission to render on the active desktop.</span></span>

<span data-ttu-id="3059c-112">Операционная система запускает событие, когда приложение может снова выполнить визуализацию.</span><span class="sxs-lookup"><span data-stu-id="3059c-112">The operating system triggers the event when the app is able to render again.</span></span> <span data-ttu-id="3059c-113">Событие не удаляется во время обновления драйвера или обнаружения времени ожидания (ТДР) процессион, однако оно удаляется при активации нового адаптера и мониторов.</span><span class="sxs-lookup"><span data-stu-id="3059c-113">The event is not cleared during a driver upgrade, or timeout detection and recovery (TDR) procession, however it is cleared when the new adapter and monitors become active.</span></span>

<span data-ttu-id="3059c-114">Если вы хотите, чтобы приложение получало уведомления об изменениях состояния перекрытия, приложение должно зарегистрировать эти изменения.</span><span class="sxs-lookup"><span data-stu-id="3059c-114">If you want your app to be notified about changes of occlusion status, the app must register for these changes.</span></span> <span data-ttu-id="3059c-115">Приложение может зарегистрироваться, чтобы получать уведомления об изменениях состояния перекрытия через сообщение в окне или с помощью сигнализации о событиях.</span><span class="sxs-lookup"><span data-stu-id="3059c-115">An app can register to be notified about changes of occlusion status through a message to a window or through event signaling.</span></span> <span data-ttu-id="3059c-116">Чтобы зарегистрироваться для получения уведомлений в окне об изменениях состояния перекрытия, приложение вызывает метод [**IDXGIFactory2:: регистерокклусионстатусвиндов**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-registerocclusionstatuswindow) .</span><span class="sxs-lookup"><span data-stu-id="3059c-116">To register to receive notification messages to a window about occlusion status changes, an app calls the [**IDXGIFactory2::RegisterOcclusionStatusWindow**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-registerocclusionstatuswindow) method.</span></span> <span data-ttu-id="3059c-117">Чтобы зарегистрироваться для получения уведомлений об изменениях состояния перекрытия через сигнализацию события, приложение вызывает метод [**IDXGIFactory2:: регистерокклусионстатусевент**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-registerocclusionstatusevent) .</span><span class="sxs-lookup"><span data-stu-id="3059c-117">To register to receive notification of occlusion status changes via event signaling, an app calls the [**IDXGIFactory2::RegisterOcclusionStatusEvent**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-registerocclusionstatusevent) method.</span></span> <span data-ttu-id="3059c-118">Оба метода возвращают указатель на значение ключа, которое приложение может использовать для отмены регистрации уведомления.</span><span class="sxs-lookup"><span data-stu-id="3059c-118">Both methods return a pointer to a key value that the app can use to unregister the notification.</span></span> <span data-ttu-id="3059c-119">Чтобы отменить регистрацию уведомления, приложение передает значение этого ключа методу [**IDXGIFactory2:: унрегистерокклусионстатус**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-unregisterocclusionstatus) .</span><span class="sxs-lookup"><span data-stu-id="3059c-119">To unregister the notification, the app passes this key value to the [**IDXGIFactory2::UnregisterOcclusionStatus**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-unregisterocclusionstatus) method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3059c-120">См. также</span><span class="sxs-lookup"><span data-stu-id="3059c-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3059c-121">Усовершенствования DXGI 1,2</span><span class="sxs-lookup"><span data-stu-id="3059c-121">DXGI 1.2 Improvements</span></span>](dxgi-1-2-improvements.md)
</dt> </dl>

 

 



