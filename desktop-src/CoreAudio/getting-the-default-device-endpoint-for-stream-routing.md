---
description: В Windows 7 API-интерфейсы высокоуровневой платформы, использующие основные API аудио, такие как Media Foundation, DirectSound и Wave API, реализуют функцию маршрутизации потоков путем обработки переключения потоков с существующего устройства на новую конечную точку звука по умолчанию.
ms.assetid: 4f36710c-c5a8-4f31-9b77-5253475c0715
title: Получение конечной точки устройства для маршрутизации потоков
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ed8c7546c2bd7437ed9705dc93c2a736bbb64e2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895974"
---
# <a name="getting-the-device-endpoint-for-stream-routing"></a><span data-ttu-id="a2652-103">Получение конечной точки устройства для маршрутизации потоков</span><span class="sxs-lookup"><span data-stu-id="a2652-103">Getting the Device Endpoint for Stream Routing</span></span>

<span data-ttu-id="a2652-104">В Windows 7 API-интерфейсы высокоуровневой платформы, использующие основные API аудио, такие как Media Foundation, DirectSound и Wave API, реализуют функцию маршрутизации потоков путем обработки переключения потоков с существующего устройства на новую конечную точку звука по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a2652-104">In Windows 7, high-level platform APIs that use Core Audio APIs such as Media Foundation, DirectSound, and Wave APIs, implement the stream routing feature by handling stream switching from an existing device to a new default audio endpoint.</span></span> <span data-ttu-id="a2652-105">Приложения мультимедиа, использующие эти API (например, приложение, которое активирует объект **идиректсаунд** или **Ибасефилтер** в объекте [**иммдевице**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) ), используют поведение маршрутизации потока без каких-либо изменений в источнике.</span><span class="sxs-lookup"><span data-stu-id="a2652-105">Media applications that use these APIs (for example, an application activating an **IDirectSound** or **IBaseFilter** object on an [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) object) use the stream routing behavior without any modifications to the source.</span></span>

<span data-ttu-id="a2652-106">Высокоуровневые интерфейсы API реализуют потоковую маршрутизацию для конечной точки устройства, полученную с помощью [**иммдевицеенумератор:: жетдефаултаудиоендпоинт**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint).</span><span class="sxs-lookup"><span data-stu-id="a2652-106">The high-level APIs implement stream routing for the device endpoint that is obtained through [**IMMDeviceEnumerator::GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint).</span></span> <span data-ttu-id="a2652-107">Если приложение выполняет потоковую передачу на устройство по умолчанию, функция маршрутизации потоков работает как определенная.</span><span class="sxs-lookup"><span data-stu-id="a2652-107">If an application streams to the default device, the stream routing feature operates as defined.</span></span> <span data-ttu-id="a2652-108">Потоки не переключаются на новое устройство, если оно извлекается любым другим механизмом, даже если оно совпадает с устройством по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a2652-108">Streams are not switched to the new device if it is retrieved by any other mechanism even if it is the same as the default device.</span></span>

<span data-ttu-id="a2652-109">Приложение мультимедиа, которое использует API-интерфейсы Core Audio напрямую (ВАСАПИ Client), может предоставлять собственную реализацию потоковой маршрутизации для любого устройства отрисовки или записи.</span><span class="sxs-lookup"><span data-stu-id="a2652-109">A media application that uses Core Audio APIs directly (WASAPI client) can provide a custom stream routing implementation for any rendering or capture device.</span></span> <span data-ttu-id="a2652-110">Клиент ВАСАПИ может реплицировать имплеметатион, предоставляемый интерфейсами API высокого уровня, запретив его потокам, которые открываются на устройствах, настроенных как устройства по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a2652-110">A WASAPI client can replicate the implemetation provided by the high-level APIs by restricting it to streams that are opened on devices that are set as the default device.</span></span> <span data-ttu-id="a2652-111">Чтобы получить ссылку на конечную точку устройства по умолчанию, клиент должен вызвать [**иммдевицеенумератор:: жетдефаултаудиоендпоинт**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint).</span><span class="sxs-lookup"><span data-stu-id="a2652-111">To get a reference to the default device's endpoint, the client must call [**IMMDeviceEnumerator::GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint).</span></span> <span data-ttu-id="a2652-112">В этом вызове клиент должен указать, требуется ли указатель на устройство отрисовки по умолчанию или устройство отслеживания по умолчанию, указав параметр *потока* данных.</span><span class="sxs-lookup"><span data-stu-id="a2652-112">In this call, the client must indicate whether it requires a pointer to the rendering default device or the capture default device by specifying the *dataFlow* parameter.</span></span> <span data-ttu-id="a2652-113">Клиент также должен указать соответствующую роль для конечной точки в атрибуте **ероле** (**еконсоле** или **екоммуникатионс**).</span><span class="sxs-lookup"><span data-stu-id="a2652-113">The client must also specify the appropriate role for the endpoint in the **ERole** attribute (**eConsole** or **eCommunications**).</span></span> <span data-ttu-id="a2652-114">Не используйте **емултимедиа**.</span><span class="sxs-lookup"><span data-stu-id="a2652-114">Do not use **eMultimedia**.</span></span>

<span data-ttu-id="a2652-115">Если приложение осуществляет потоковую передачу на любое другое устройство, приложение может получить устройство, указав строку идентификатора конечной точки (путем вызова [**иммдевицеенумератор:: An Device**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice)).</span><span class="sxs-lookup"><span data-stu-id="a2652-115">If the application streams to any other device, the application can get the device by specifying an endpoint ID string (by calling [**IMMDeviceEnumerator::GetDevice**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice)).</span></span>

<span data-ttu-id="a2652-116">После определения устройства клиент ВАСАПИ может предоставить реализацию потоковой маршрутизации, обрабатывая уведомления об устройстве и звуковом сеансе, отправленные для устройства.</span><span class="sxs-lookup"><span data-stu-id="a2652-116">After the device is identified, the WASAPI client can provide the implementation for stream routing by handling the device and audio session notifications sent for the device.</span></span> <span data-ttu-id="a2652-117">Дополнительные сведения об этих уведомлениях см. в разделе [релевантные уведомления для потоковой маршрутизации](relevant-device-notifications-for-stream-routing.md).</span><span class="sxs-lookup"><span data-stu-id="a2652-117">For more information about these notifications, see [Relevant Notifications for Stream Routing](relevant-device-notifications-for-stream-routing.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a2652-118">См. также</span><span class="sxs-lookup"><span data-stu-id="a2652-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a2652-119">Сведения об API Ммдевице</span><span class="sxs-lookup"><span data-stu-id="a2652-119">About MMDevice API</span></span>](mmdevice-api.md)
</dt> <dt>

[<span data-ttu-id="a2652-120">О ВАСАПИ</span><span class="sxs-lookup"><span data-stu-id="a2652-120">About WASAPI</span></span>](wasapi.md)
</dt> <dt>

[<span data-ttu-id="a2652-121">Потоковая маршрутизация</span><span class="sxs-lookup"><span data-stu-id="a2652-121">Stream Routing</span></span>](stream-routing.md)
</dt> </dl>

 

 



