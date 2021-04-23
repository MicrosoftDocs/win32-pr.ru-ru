---
description: Правильная работа компонентов TAPI требует установки среды связи на компьютере.
ms.assetid: 3df3d974-629e-4d78-b97d-b8121b185309
title: Инициализация TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 973d67931fb9f33751fedc638ab77021d3d3d34c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684225"
---
# <a name="tapi-initialization"></a><span data-ttu-id="93919-103">Инициализация TAPI</span><span class="sxs-lookup"><span data-stu-id="93919-103">TAPI Initialization</span></span>

<span data-ttu-id="93919-104">Правильная работа компонентов TAPI требует установки среды связи на компьютере следующим образом:</span><span class="sxs-lookup"><span data-stu-id="93919-104">Proper functioning of TAPI components requires setting up the communications environment on a computer as follows:</span></span>

-   <span data-ttu-id="93919-105">[Установка](installation.md) выполняется при первом добавлении программного обеспечения или оборудования на компьютер.</span><span class="sxs-lookup"><span data-stu-id="93919-105">[Installation](installation.md) is performed when software or hardware is first added to the computer.</span></span> <span data-ttu-id="93919-106">Подробные процедуры зависят от операционной системы и самого программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="93919-106">Detailed procedures depend on the operating system and the software itself.</span></span>
-   <span data-ttu-id="93919-107">[Основная инициализация](primary-initialization.md) создает объекты и пути взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="93919-107">[Primary initialization](primary-initialization.md) creates the objects and communication paths.</span></span>
-   <span data-ttu-id="93919-108">[Согласование версий](version-negotiation.md) гарантирует, что компоненты TAPI смогут обмениваться данными.</span><span class="sxs-lookup"><span data-stu-id="93919-108">[Version negotiation](version-negotiation.md) ensures that TAPI components will be able to exchange data.</span></span>
-   <span data-ttu-id="93919-109">При [инвентаризации ресурсов](resource-inventory.md) извлекаются сведения об устройствах, доступных для использования приложением TAPI.</span><span class="sxs-lookup"><span data-stu-id="93919-109">[Resource inventory](resource-inventory.md) retrieves information concerning devices available for use by a TAPI application.</span></span>
-   <span data-ttu-id="93919-110">[Уведомление о событии](event-notification.md) указывает, как TAPI и поставщики услуг передают в приложение результаты асинхронной операции и сведения об изменении состояния.</span><span class="sxs-lookup"><span data-stu-id="93919-110">[Event notification](event-notification.md) specifies how TAPI and the service providers pass asynchronous operation results and state change information to the application.</span></span>

## <a name="summary-of-related-reference-pages"></a><span data-ttu-id="93919-111">Сводка по связанным страницам ссылок</span><span class="sxs-lookup"><span data-stu-id="93919-111">Summary of Related Reference Pages</span></span>



| <span data-ttu-id="93919-112">Функции TAPI 2. x</span><span class="sxs-lookup"><span data-stu-id="93919-112">TAPI 2.x functions</span></span>                                        | <span data-ttu-id="93919-113">Описание</span><span class="sxs-lookup"><span data-stu-id="93919-113">Description</span></span>                                                                                                                       |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="93919-114">**линеинитиализикс**</span><span class="sxs-lookup"><span data-stu-id="93919-114">**lineInitializeEx**</span></span>](/windows/win32/api/tapi/nf-tapi-lineinitializeexa)     | <span data-ttu-id="93919-115">Настраивает среду телефонии, возвращает маркер приложения и число устройств.</span><span class="sxs-lookup"><span data-stu-id="93919-115">Sets up the telephony environment, returns application handle and device count.</span></span>                                                   |
| [<span data-ttu-id="93919-116">**линежетдевкапс**</span><span class="sxs-lookup"><span data-stu-id="93919-116">**lineGetDevCaps**</span></span>](/windows/win32/api/tapi/nf-tapi-linegetdevcaps)         | <span data-ttu-id="93919-117">Возвращает возможности устройства, такие как поддерживаемые версии TAPI или типы мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="93919-117">Gets device capabilities, such as TAPI version or media types supported.</span></span>                                                          |
| [<span data-ttu-id="93919-118">**линежетаддресскапс**</span><span class="sxs-lookup"><span data-stu-id="93919-118">**lineGetAddressCaps**</span></span>](/windows/win32/api/tapi/nf-tapi-linegetaddresscaps) | <span data-ttu-id="93919-119">Получает возможности адресации, например, поддерживается ли метод парковки.</span><span class="sxs-lookup"><span data-stu-id="93919-119">Gets address capabilities, such as whether call park is supported.</span></span>                                                                |
| [<span data-ttu-id="93919-120">**линеопен**</span><span class="sxs-lookup"><span data-stu-id="93919-120">**lineOpen**</span></span>](/windows/win32/api/tapi/nf-tapi-lineopen)                     | <span data-ttu-id="93919-121">Уведомляет TAPI о том, что приложение будет использовать строку и каким образом.</span><span class="sxs-lookup"><span data-stu-id="93919-121">Notifies TAPI that the application will be using the line, and in what way.</span></span>                                                       |
| [<span data-ttu-id="93919-122">**линежетмессаже**</span><span class="sxs-lookup"><span data-stu-id="93919-122">**lineGetMessage**</span></span>](/windows/win32/api/tapi/nf-tapi-linegetmessage)         | <span data-ttu-id="93919-123">Возвращает следующее сообщение TAPI, помещенное в очередь для доставки в приложение, использующее механизм уведомления "обработчик событий"</span><span class="sxs-lookup"><span data-stu-id="93919-123">Returns the next TAPI message that is queued for delivery to an application that is using the Event Handle notification mechanism</span></span> |



 



| <span data-ttu-id="93919-124">Интерфейсы или методы интерфейса TAPI 3. x</span><span class="sxs-lookup"><span data-stu-id="93919-124">TAPI 3.x interfaces or methods</span></span>                                                | <span data-ttu-id="93919-125">Описание</span><span class="sxs-lookup"><span data-stu-id="93919-125">Description</span></span>                                                                                                                                |
|-------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="93919-126">**ИТТАПИ:: Initialize**</span><span class="sxs-lookup"><span data-stu-id="93919-126">**ITTAPI::Initialize**</span></span>](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-initialize)                               | <span data-ttu-id="93919-127">Настройка среды телефонии.</span><span class="sxs-lookup"><span data-stu-id="93919-127">Sets up telephony environment.</span></span>                                                                                                             |
| [<span data-ttu-id="93919-128">**ИТТАПИ:: Енумератеаддрессес**</span><span class="sxs-lookup"><span data-stu-id="93919-128">**ITTAPI::EnumerateAddresses**</span></span>](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-enumerateaddresses)               | <span data-ttu-id="93919-129">Перечисляет адреса, доступные в настоящее время.</span><span class="sxs-lookup"><span data-stu-id="93919-129">Enumerates addresses currently available.</span></span>                                                                                                  |
| [<span data-ttu-id="93919-130">**ИТТАПИ:: получение \_ адресов**</span><span class="sxs-lookup"><span data-stu-id="93919-130">**ITTAPI::get\_Addresses**</span></span>](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-get_addresses)                        | <span data-ttu-id="93919-131">Создает коллекцию адресов, доступных в данный момент.</span><span class="sxs-lookup"><span data-stu-id="93919-131">Creates a collection of addresses currently available.</span></span> <span data-ttu-id="93919-132">Предоставляется для клиентских приложений автоматизации, например, написанных на Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="93919-132">Provided for Automation client applications, such as those written in Visual Basic.</span></span> |
| [<span data-ttu-id="93919-133">**Иттапиевентнотификатион:: Event**</span><span class="sxs-lookup"><span data-stu-id="93919-133">**ITTAPIEventNotification::Event**</span></span>](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event)       | <span data-ttu-id="93919-134">Определяет ответ на асинхронное уведомление о событии.</span><span class="sxs-lookup"><span data-stu-id="93919-134">Determines response to an asynchronous event notification.</span></span> <span data-ttu-id="93919-135">Реализовано приложением, вызванным TAPI.</span><span class="sxs-lookup"><span data-stu-id="93919-135">Implemented by the application, invoked by TAPI.</span></span>                                |
| [<span data-ttu-id="93919-136">**ИТТАПИ::p UT \_ EventFilter**</span><span class="sxs-lookup"><span data-stu-id="93919-136">**ITTAPI::put\_EventFilter**</span></span>](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter)                    | <span data-ttu-id="93919-137">Задает маску фильтра событий, которая уведомляет TAPI о том, какие события требуются приложению.</span><span class="sxs-lookup"><span data-stu-id="93919-137">Sets the event filter mask, which notifies TAPI which events the application requires.</span></span>                                                     |
| [<span data-ttu-id="93919-138">**ИТТАПИ:: Регистеркаллнотификатионс**</span><span class="sxs-lookup"><span data-stu-id="93919-138">**ITTAPI::RegisterCallNotifications**</span></span>](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-registercallnotifications) | <span data-ttu-id="93919-139">Указывает TAPI передать входящие сеансы приложения для указанного адреса и набора типов носителей.</span><span class="sxs-lookup"><span data-stu-id="93919-139">Instructs TAPI to pass the application incoming sessions for a specified address and set of media types.</span></span>                                   |
| [<span data-ttu-id="93919-140">**итмедиасуппорт**</span><span class="sxs-lookup"><span data-stu-id="93919-140">**ITMediaSupport**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itmediasupport)                                      | <span data-ttu-id="93919-141">Позволяет приложению обнаруживать возможности поддержки мультимедиа для адреса.</span><span class="sxs-lookup"><span data-stu-id="93919-141">Allows an application to discover the media support capabilities for an address.</span></span>                                                           |



 

 

 
