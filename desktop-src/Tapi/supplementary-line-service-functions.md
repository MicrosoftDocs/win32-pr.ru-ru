---
description: Функции службы дополнительной строки перечислены по категориям в следующих разделах.
ms.assetid: d4338b3c-cd84-4abb-b74e-9df895c8355b
title: Функции службы дополнительных строк
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21a29831369fd6b886d57cfae075b5b8bf7a83b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683402"
---
# <a name="supplementary-line-service-functions"></a><span data-ttu-id="d2e0a-103">Функции службы дополнительных строк</span><span class="sxs-lookup"><span data-stu-id="d2e0a-103">Supplementary Line Service Functions</span></span>

<span data-ttu-id="d2e0a-104">Функции службы дополнительной строки перечислены по категориям в следующих разделах.</span><span class="sxs-lookup"><span data-stu-id="d2e0a-104">The supplementary line service functions are listed by category in the following topics.</span></span> <span data-ttu-id="d2e0a-105">Функция определяется как [*асинхронная*](a-tapgloss.md) , если она указывает на завершение в ответном сообщении для приложения.</span><span class="sxs-lookup"><span data-stu-id="d2e0a-105">A function is identified as [*asynchronous*](a-tapgloss.md) if it will indicate completion in a REPLY message to the application.</span></span> <span data-ttu-id="d2e0a-106">Если функция всегда возвращает результат в приложение немедленно, функция считается [*синхронной*](s-tapgloss.md).</span><span class="sxs-lookup"><span data-stu-id="d2e0a-106">If the function always returns its result to the application immediately, the function is considered [*synchronous*](s-tapgloss.md).</span></span>

<span data-ttu-id="d2e0a-107">Ниже приведена функциональная группировка функций службы дополнительных строк.</span><span class="sxs-lookup"><span data-stu-id="d2e0a-107">Following is a functional grouping of the supplementary line service functions:</span></span>

-   [<span data-ttu-id="d2e0a-108">Агенты</span><span class="sxs-lookup"><span data-stu-id="d2e0a-108">Agents</span></span>](#agents)
-   [<span data-ttu-id="d2e0a-109">Приоритет приложения</span><span class="sxs-lookup"><span data-stu-id="d2e0a-109">Application priority</span></span>](#application-priority)
-   [<span data-ttu-id="d2e0a-110">Режим и скорость носителя</span><span class="sxs-lookup"><span data-stu-id="d2e0a-110">Bearer mode and rate</span></span>](#bearer-mode-and-rate)
-   [<span data-ttu-id="d2e0a-111">Вызов метода Accept и Redirect</span><span class="sxs-lookup"><span data-stu-id="d2e0a-111">Call accept and redirect</span></span>](#call-accept-and-redirect)
-   [<span data-ttu-id="d2e0a-112">Завершение вызова</span><span class="sxs-lookup"><span data-stu-id="d2e0a-112">Call completion</span></span>](#call-completion)
-   [<span data-ttu-id="d2e0a-113">Позвонить на конференцию</span><span class="sxs-lookup"><span data-stu-id="d2e0a-113">Call conference</span></span>](#call-conference)
-   [<span data-ttu-id="d2e0a-114">Переадресация звонков</span><span class="sxs-lookup"><span data-stu-id="d2e0a-114">Call forwarding</span></span>](#call-forwarding)
-   [<span data-ttu-id="d2e0a-115">Удержание вызова</span><span class="sxs-lookup"><span data-stu-id="d2e0a-115">Call hold</span></span>](#call-hold)
-   [<span data-ttu-id="d2e0a-116">Приостановить вызов</span><span class="sxs-lookup"><span data-stu-id="d2e0a-116">Call park</span></span>](#call-park)
-   [<span data-ttu-id="d2e0a-117">Отправка вызова</span><span class="sxs-lookup"><span data-stu-id="d2e0a-117">Call pickup</span></span>](#call-pickup)
-   [<span data-ttu-id="d2e0a-118">Отклонить вызов</span><span class="sxs-lookup"><span data-stu-id="d2e0a-118">Call reject</span></span>](#call-reject)
-   [<span data-ttu-id="d2e0a-119">Перемещение вызовов</span><span class="sxs-lookup"><span data-stu-id="d2e0a-119">Call transfer</span></span>](#call-transfer)
-   [<span data-ttu-id="d2e0a-120">Отслеживание цифр и сбор данных</span><span class="sxs-lookup"><span data-stu-id="d2e0a-120">Digit monitoring and gathering</span></span>](#digit-monitoring-and-gathering)
-   [<span data-ttu-id="d2e0a-121">Создание нестандартных цифр и тонов</span><span class="sxs-lookup"><span data-stu-id="d2e0a-121">Generating inband digits and tones</span></span>](#generating-inband-digits-and-tones)
-   [<span data-ttu-id="d2e0a-122">Выполнение вызовов</span><span class="sxs-lookup"><span data-stu-id="d2e0a-122">Making calls</span></span>](basic-telephony-services-reference.md)
-   [<span data-ttu-id="d2e0a-123">Элемент управления мультимедиа</span><span class="sxs-lookup"><span data-stu-id="d2e0a-123">Media control</span></span>](#media-control)
-   [<span data-ttu-id="d2e0a-124">Мониторинг мультимедиа</span><span class="sxs-lookup"><span data-stu-id="d2e0a-124">Media monitoring</span></span>](#media-monitoring)
-   [<span data-ttu-id="d2e0a-125">прокси-серверы;</span><span class="sxs-lookup"><span data-stu-id="d2e0a-125">Proxies</span></span>](#proxies)
-   [<span data-ttu-id="d2e0a-126">Качество обслуживания</span><span class="sxs-lookup"><span data-stu-id="d2e0a-126">Quality of Service</span></span>](#quality-of-service)
-   [<span data-ttu-id="d2e0a-127">Отправка сведений удаленному лицу</span><span class="sxs-lookup"><span data-stu-id="d2e0a-127">Sending information to remote party</span></span>](#sending-information-to-remote-party)
-   [<span data-ttu-id="d2e0a-128">Управление поставщиками услуг</span><span class="sxs-lookup"><span data-stu-id="d2e0a-128">Service provider management</span></span>](#service-provider-management)
-   [<span data-ttu-id="d2e0a-129">Настройка терминала для телефонных разговоров</span><span class="sxs-lookup"><span data-stu-id="d2e0a-129">Setting a terminal for phone conversations</span></span>](#setting-a-terminal-for-phone-conversations)
-   [<span data-ttu-id="d2e0a-130">Мониторинг тона</span><span class="sxs-lookup"><span data-stu-id="d2e0a-130">Tone monitoring</span></span>](#tone-monitoring)

<span data-ttu-id="d2e0a-131">Существуют также [различные](#miscellaneous) функции расширенной службы дополнительных строк.</span><span class="sxs-lookup"><span data-stu-id="d2e0a-131">There are also [miscellaneous](#miscellaneous) supplementary line service functions.</span></span>

## <a name="bearer-mode-and-rate"></a><span data-ttu-id="d2e0a-132">Режим и скорость носителя</span><span class="sxs-lookup"><span data-stu-id="d2e0a-132">Bearer Mode and Rate</span></span>



| <span data-ttu-id="d2e0a-133">Функция</span><span class="sxs-lookup"><span data-stu-id="d2e0a-133">Function</span></span>                                       | <span data-ttu-id="d2e0a-134">Описание</span><span class="sxs-lookup"><span data-stu-id="d2e0a-134">Description</span></span>                                                                |
|------------------------------------------------|----------------------------------------------------------------------------|
| [<span data-ttu-id="d2e0a-135">**линесеткаллпарамс**</span><span class="sxs-lookup"><span data-stu-id="d2e0a-135">**lineSetCallParams**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetcallparams) | <span data-ttu-id="d2e0a-136">Запрашивает изменение параметров вызова существующего вызова.</span><span class="sxs-lookup"><span data-stu-id="d2e0a-136">Requests a change in the call parameters of an existing call.</span></span> <span data-ttu-id="d2e0a-137">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="d2e0a-137">Synchronous.</span></span> |



 

## <a name="media-monitoring"></a><span data-ttu-id="d2e0a-138">Мониторинг мультимедиа</span><span class="sxs-lookup"><span data-stu-id="d2e0a-138">Media Monitoring</span></span>



| <span data-ttu-id="d2e0a-139">Функция</span><span class="sxs-lookup"><span data-stu-id="d2e0a-139">Function</span></span>                                     | <span data-ttu-id="d2e0a-140">Описание</span><span class="sxs-lookup"><span data-stu-id="d2e0a-140">Description</span></span>                                                                   |
|----------------------------------------------|-------------------------------------------------------------------------------|
| [<span data-ttu-id="d2e0a-141">**линемонитормедиа**</span><span class="sxs-lookup"><span data-stu-id="d2e0a-141">**lineMonitorMedia**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linemonitormedia) | <span data-ttu-id="d2e0a-142">Включает или отключает уведомление режима мультимедиа при указанном вызове.</span><span class="sxs-lookup"><span data-stu-id="d2e0a-142">Enables or disables media mode notification on a specified call.</span></span> <span data-ttu-id="d2e0a-143">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="d2e0a-143">Synchronous.</span></span> |



 

## <a name="digit-monitoring-and-gathering"></a><span data-ttu-id="d2e0a-144">Отслеживание цифр и сбор данных</span><span class="sxs-lookup"><span data-stu-id="d2e0a-144">Digit Monitoring and Gathering</span></span>



| <span data-ttu-id="d2e0a-145">Функция</span><span class="sxs-lookup"><span data-stu-id="d2e0a-145">Function</span></span>                                       | <span data-ttu-id="d2e0a-146">Описание</span><span class="sxs-lookup"><span data-stu-id="d2e0a-146">Description</span></span>                                                                        |
|------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="d2e0a-147">**линемонитордигитс**</span><span class="sxs-lookup"><span data-stu-id="d2e0a-147">**lineMonitorDigits**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linemonitordigits) | <span data-ttu-id="d2e0a-148">Включает или отключает уведомление об обнаружении цифр при указанном вызове.</span><span class="sxs-lookup"><span data-stu-id="d2e0a-148">Enables or disables digit detection notification on a specified call.</span></span> <span data-ttu-id="d2e0a-149">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="d2e0a-149">Synchronous.</span></span> |
| [<span data-ttu-id="d2e0a-150">**линегасердигитс**</span><span class="sxs-lookup"><span data-stu-id="d2e0a-150">**lineGatherDigits**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegatherdigits)   | <span data-ttu-id="d2e0a-151">Выполняет буферизованный сбор цифр в вызове.</span><span class="sxs-lookup"><span data-stu-id="d2e0a-151">Performs the buffered gathering of digits on a call.</span></span> <span data-ttu-id="d2e0a-152">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="d2e0a-152">Synchronous.</span></span>                  |



 

## <a name="tone-monitoring"></a><span data-ttu-id="d2e0a-153">Мониторинг тона</span><span class="sxs-lookup"><span data-stu-id="d2e0a-153">Tone Monitoring</span></span>



| <span data-ttu-id="d2e0a-154">Функция</span><span class="sxs-lookup"><span data-stu-id="d2e0a-154">Function</span></span>                                     | <span data-ttu-id="d2e0a-155">Описание</span><span class="sxs-lookup"><span data-stu-id="d2e0a-155">Description</span></span>                                                       |
|----------------------------------------------|-------------------------------------------------------------------|
| [<span data-ttu-id="d2e0a-156">**линемонитортонес**</span><span class="sxs-lookup"><span data-stu-id="d2e0a-156">**lineMonitorTones**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linemonitortones) | <span data-ttu-id="d2e0a-157">Указывает, какие звуки должны обнаруживаться при указанном вызове.</span><span class="sxs-lookup"><span data-stu-id="d2e0a-157">Specifies which tones to detect on a specified call.</span></span> <span data-ttu-id="d2e0a-158">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="d2e0a-158">Synchronous.</span></span> |



 

## <a name="media-control"></a><span data-ttu-id="d2e0a-159">Элемент управления мультимедиа</span><span class="sxs-lookup"><span data-stu-id="d2e0a-159">Media Control</span></span>



| <span data-ttu-id="d2e0a-160">Функция</span><span class="sxs-lookup"><span data-stu-id="d2e0a-160">Function</span></span>                                           | <span data-ttu-id="d2e0a-161">Описание</span><span class="sxs-lookup"><span data-stu-id="d2e0a-161">Description</span></span>                                                                                                          |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d2e0a-162">**линесетмедиаконтрол**</span><span class="sxs-lookup"><span data-stu-id="d2e0a-162">**lineSetMediaControl**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetmediacontrol) | <span data-ttu-id="d2e0a-163">Настраивает поток мультимедиа вызова для элемента управления мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="d2e0a-163">Sets up a call's media stream for media control.</span></span> <span data-ttu-id="d2e0a-164">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="d2e0a-164">Synchronous.</span></span>                                                        |
| [<span data-ttu-id="d2e0a-165">**линесетмедиамоде**</span><span class="sxs-lookup"><span data-stu-id="d2e0a-165">**lineSetMediaMode**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetmediamode)       | <span data-ttu-id="d2e0a-166">Задает режим мультимедиа для указанного вызова в структуре [**линекаллинфо**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) .</span><span class="sxs-lookup"><span data-stu-id="d2e0a-166">Sets the media mode(s) of the specified call in its [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) structure.</span></span> <span data-ttu-id="d2e0a-167">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="d2e0a-167">Synchronous.</span></span> |



 

## <a name="generating-inband-digits-and-tones"></a><span data-ttu-id="d2e0a-168">Создание нестандартных цифр и тонов</span><span class="sxs-lookup"><span data-stu-id="d2e0a-168">Generating Inband Digits and Tones</span></span>



| <span data-ttu-id="d2e0a-169">Функция</span><span class="sxs-lookup"><span data-stu-id="d2e0a-169">Function</span></span>                                         | <span data-ttu-id="d2e0a-170">Описание</span><span class="sxs-lookup"><span data-stu-id="d2e0a-170">Description</span></span>                                                   |
|--------------------------------------------------|---------------------------------------------------------------|
| [<span data-ttu-id="d2e0a-171">**линеженератедигитс**</span><span class="sxs-lookup"><span data-stu-id="d2e0a-171">**lineGenerateDigits**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegeneratedigits) | <span data-ttu-id="d2e0a-172">Создает нестандартные цифры при вызове.</span><span class="sxs-lookup"><span data-stu-id="d2e0a-172">Generates inband digits on a call.</span></span> <span data-ttu-id="d2e0a-173">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="d2e0a-173">Synchronous.</span></span>               |
| [<span data-ttu-id="d2e0a-174">**линеженератетоне**</span><span class="sxs-lookup"><span data-stu-id="d2e0a-174">**lineGenerateTone**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegeneratetone)     | <span data-ttu-id="d2e0a-175">Формирует заданный набор заданных тонов при вызове.</span><span class="sxs-lookup"><span data-stu-id="d2e0a-175">Generates a given set of tones inband on a call.</span></span> <span data-ttu-id="d2e0a-176">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="d2e0a-176">Synchronous.</span></span> |



 

## <a name="call-accept-and-redirect"></a><span data-ttu-id="d2e0a-177">Вызов метода Accept и Redirect</span><span class="sxs-lookup"><span data-stu-id="d2e0a-177">Call Accept and Redirect</span></span>



| <span data-ttu-id="d2e0a-178">Функция</span><span class="sxs-lookup"><span data-stu-id="d2e0a-178">Function</span></span>                             | <span data-ttu-id="d2e0a-179">Описание</span><span class="sxs-lookup"><span data-stu-id="d2e0a-179">Description</span></span>                                                                                               |
|--------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d2e0a-180">**линеакцепт**</span><span class="sxs-lookup"><span data-stu-id="d2e0a-180">**lineAccept**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineaccept)     | <span data-ttu-id="d2e0a-181">Принимает предлагаемый вызов и начинает оповещение о вызывающем объекте (звонка) и вызываемой стороне (Ring).</span><span class="sxs-lookup"><span data-stu-id="d2e0a-181">Accepts an offered call and starts alerting both caller (ringback) and called party (ring).</span></span> <span data-ttu-id="d2e0a-182">Асинхронная.</span><span class="sxs-lookup"><span data-stu-id="d2e0a-182">Asynchronous.</span></span> |
| [<span data-ttu-id="d2e0a-183">**линередирект**</span><span class="sxs-lookup"><span data-stu-id="d2e0a-183">**lineRedirect**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineredirect) | <span data-ttu-id="d2e0a-184">Перенаправляет вызов предложения на другой адрес.</span><span class="sxs-lookup"><span data-stu-id="d2e0a-184">Redirects an offering call to another address.</span></span> <span data-ttu-id="d2e0a-185">Асинхронная.</span><span class="sxs-lookup"><span data-stu-id="d2e0a-185">Asynchronous.</span></span>                                              |



 

## <a name="call-reject"></a><span data-ttu-id="d2e0a-186">Отклонить вызов</span><span class="sxs-lookup"><span data-stu-id="d2e0a-186">Call Reject</span></span>



| <span data-ttu-id="d2e0a-187">Функция</span><span class="sxs-lookup"><span data-stu-id="d2e0a-187">Function</span></span>                     | <span data-ttu-id="d2e0a-188">Описание</span><span class="sxs-lookup"><span data-stu-id="d2e0a-188">Description</span></span>                                                               |
|------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="d2e0a-189">**линедроп**</span><span class="sxs-lookup"><span data-stu-id="d2e0a-189">**lineDrop**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linedrop) | <span data-ttu-id="d2e0a-190">Отключает вызов или прерывает выполнение попытки вызова.</span><span class="sxs-lookup"><span data-stu-id="d2e0a-190">Disconnects a call, or abandons a call attempt in progress.</span></span> <span data-ttu-id="d2e0a-191">Асинхронная.</span><span class="sxs-lookup"><span data-stu-id="d2e0a-191">Asynchronous.</span></span> |



 

## <a name="call-hold"></a><span data-ttu-id="d2e0a-192">Удержание вызова</span><span class="sxs-lookup"><span data-stu-id="d2e0a-192">Call Hold</span></span>



| <span data-ttu-id="d2e0a-193">Функция</span><span class="sxs-lookup"><span data-stu-id="d2e0a-193">Function</span></span>                         | <span data-ttu-id="d2e0a-194">Описание</span><span class="sxs-lookup"><span data-stu-id="d2e0a-194">Description</span></span>                                           |
|----------------------------------|-------------------------------------------------------|
| [<span data-ttu-id="d2e0a-195">**линехолд**</span><span class="sxs-lookup"><span data-stu-id="d2e0a-195">**lineHold**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linehold)     | <span data-ttu-id="d2e0a-196">Помещает указанный вызов на жесткий удержании.</span><span class="sxs-lookup"><span data-stu-id="d2e0a-196">Places the specified call on hard hold.</span></span> <span data-ttu-id="d2e0a-197">Асинхронная.</span><span class="sxs-lookup"><span data-stu-id="d2e0a-197">Asynchronous.</span></span> |
| [<span data-ttu-id="d2e0a-198">**линеунхолд**</span><span class="sxs-lookup"><span data-stu-id="d2e0a-198">**lineUnhold**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineunhold) | <span data-ttu-id="d2e0a-199">Извлекает Удерживаемый вызов.</span><span class="sxs-lookup"><span data-stu-id="d2e0a-199">Retrieves a held call.</span></span> <span data-ttu-id="d2e0a-200">Асинхронная.</span><span class="sxs-lookup"><span data-stu-id="d2e0a-200">Asynchronous.</span></span>                  |



 

## <a name="securing-calls"></a><span data-ttu-id="d2e0a-201">Обеспечение безопасности вызовов</span><span class="sxs-lookup"><span data-stu-id="d2e0a-201">Securing Calls</span></span>



| <span data-ttu-id="d2e0a-202">Функция</span><span class="sxs-lookup"><span data-stu-id="d2e0a-202">Function</span></span>                                 | <span data-ttu-id="d2e0a-203">Описание</span><span class="sxs-lookup"><span data-stu-id="d2e0a-203">Description</span></span>                                                                                                              |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d2e0a-204">**линесекурекалл**</span><span class="sxs-lookup"><span data-stu-id="d2e0a-204">**lineSecureCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesecurecall) | <span data-ttu-id="d2e0a-205">Обеспечивает защиту существующего вызова от помех другими событиями, такими как сигналы, ожидающие вызова, для подключений к данным.</span><span class="sxs-lookup"><span data-stu-id="d2e0a-205">Secures an existing call from interference by other events such as call-waiting beeps on data connections.</span></span> <span data-ttu-id="d2e0a-206">Асинхронная.</span><span class="sxs-lookup"><span data-stu-id="d2e0a-206">Asynchronous.</span></span> |



 

## <a name="call-transfer"></a><span data-ttu-id="d2e0a-207">Перемещение вызовов</span><span class="sxs-lookup"><span data-stu-id="d2e0a-207">Call Transfer</span></span>



| <span data-ttu-id="d2e0a-208">Функция</span><span class="sxs-lookup"><span data-stu-id="d2e0a-208">Function</span></span>                                             | <span data-ttu-id="d2e0a-209">Описание</span><span class="sxs-lookup"><span data-stu-id="d2e0a-209">Description</span></span>                                                                                                    |
|------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d2e0a-210">**линесетуптрансфер**</span><span class="sxs-lookup"><span data-stu-id="d2e0a-210">**lineSetupTransfer**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer)       | <span data-ttu-id="d2e0a-211">Подготавливает указанный вызов для перемещения на другой адрес.</span><span class="sxs-lookup"><span data-stu-id="d2e0a-211">Prepares a specified call for transfer to another address.</span></span> <span data-ttu-id="d2e0a-212">Асинхронная.</span><span class="sxs-lookup"><span data-stu-id="d2e0a-212">Asynchronous.</span></span>                                       |
| [<span data-ttu-id="d2e0a-213">**линекомплететрансфер**</span><span class="sxs-lookup"><span data-stu-id="d2e0a-213">**lineCompleteTransfer**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer) | <span data-ttu-id="d2e0a-214">Передает вызов, настроенный для передачи другому вызову, или переходит на двустороннюю конференцию.</span><span class="sxs-lookup"><span data-stu-id="d2e0a-214">Transfers a call that was set up for transfer to another call, or enters a three-way conference.</span></span> <span data-ttu-id="d2e0a-215">Асинхронная.</span><span class="sxs-lookup"><span data-stu-id="d2e0a-215">Asynchronous.</span></span> |
| [<span data-ttu-id="d2e0a-216">**линеблиндтрансфер**</span><span class="sxs-lookup"><span data-stu-id="d2e0a-216">**lineBlindTransfer**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineblindtransfer)       | <span data-ttu-id="d2e0a-217">Передает вызов другой стороне.</span><span class="sxs-lookup"><span data-stu-id="d2e0a-217">Transfers a call to another party.</span></span> <span data-ttu-id="d2e0a-218">Асинхронная.</span><span class="sxs-lookup"><span data-stu-id="d2e0a-218">Asynchronous.</span></span>                                                               |
| [<span data-ttu-id="d2e0a-219">**линесвафолд**</span><span class="sxs-lookup"><span data-stu-id="d2e0a-219">**lineSwapHold**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineswaphold)                 | <span data-ttu-id="d2e0a-220">Меняет местами активный вызов с помощью вызова, находящегося в настоящее время на момент консультаций.</span><span class="sxs-lookup"><span data-stu-id="d2e0a-220">Swaps the active call with the call currently on consultation hold.</span></span> <span data-ttu-id="d2e0a-221">Асинхронная.</span><span class="sxs-lookup"><span data-stu-id="d2e0a-221">Asynchronous.</span></span>                              |



 

## <a name="call-conference"></a><span data-ttu-id="d2e0a-222">Позвонить на конференцию</span><span class="sxs-lookup"><span data-stu-id="d2e0a-222">Call Conference</span></span>



| <span data-ttu-id="d2e0a-223">Функция</span><span class="sxs-lookup"><span data-stu-id="d2e0a-223">Function</span></span>                                                         | <span data-ttu-id="d2e0a-224">Описание</span><span class="sxs-lookup"><span data-stu-id="d2e0a-224">Description</span></span>                                                                                                                                                                                          |
|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d2e0a-225">**линесетупконференце**</span><span class="sxs-lookup"><span data-stu-id="d2e0a-225">**lineSetupConference**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetupconference)               | <span data-ttu-id="d2e0a-226">Подготавливает заданный вызов для добавления другой стороны.</span><span class="sxs-lookup"><span data-stu-id="d2e0a-226">Prepares a given call for the addition of another party.</span></span> <span data-ttu-id="d2e0a-227">Асинхронная.</span><span class="sxs-lookup"><span data-stu-id="d2e0a-227">Asynchronous.</span></span>                                                                                                                               |
| [<span data-ttu-id="d2e0a-228">**линепрепареаддтоконференце**</span><span class="sxs-lookup"><span data-stu-id="d2e0a-228">**linePrepareAddToConference**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineprepareaddtoconference) | <span data-ttu-id="d2e0a-229">Готовится к добавлению стороны к существующему вызову Конференции путем помещения вызова конференции в состояние удержания и создания вызова консультации, который можно добавить позже в конференц-телефон.</span><span class="sxs-lookup"><span data-stu-id="d2e0a-229">Prepares to add a party to an existing conference call by placing the conference call in a hold state and creating a consultation call that can be added later to the conference call.</span></span> <span data-ttu-id="d2e0a-230">Асинхронная.</span><span class="sxs-lookup"><span data-stu-id="d2e0a-230">Asynchronous.</span></span> |
| [<span data-ttu-id="d2e0a-231">**линеаддтоконференце**</span><span class="sxs-lookup"><span data-stu-id="d2e0a-231">**lineAddToConference**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineaddtoconference)               | <span data-ttu-id="d2e0a-232">Добавляет вызов консультации в существующий вызов Конференции.</span><span class="sxs-lookup"><span data-stu-id="d2e0a-232">Adds a consultation call to an existing conference call.</span></span> <span data-ttu-id="d2e0a-233">Асинхронная.</span><span class="sxs-lookup"><span data-stu-id="d2e0a-233">Asynchronous.</span></span>                                                                                                                               |
| [<span data-ttu-id="d2e0a-234">**линеремовефромконференце**</span><span class="sxs-lookup"><span data-stu-id="d2e0a-234">**lineRemoveFromConference**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineremovefromconference)     | <span data-ttu-id="d2e0a-235">Удаляет субъект из вызова конференции.</span><span class="sxs-lookup"><span data-stu-id="d2e0a-235">Removes a party from a conference call.</span></span> <span data-ttu-id="d2e0a-236">Асинхронная.</span><span class="sxs-lookup"><span data-stu-id="d2e0a-236">Asynchronous.</span></span>                                                                                                                                                |



 

## <a name="call-park"></a><span data-ttu-id="d2e0a-237">Приостановить вызов</span><span class="sxs-lookup"><span data-stu-id="d2e0a-237">Call Park</span></span>



| <span data-ttu-id="d2e0a-238">Функция</span><span class="sxs-lookup"><span data-stu-id="d2e0a-238">Function</span></span>                         | <span data-ttu-id="d2e0a-239">Описание</span><span class="sxs-lookup"><span data-stu-id="d2e0a-239">Description</span></span>                                          |
|----------------------------------|------------------------------------------------------|
| [<span data-ttu-id="d2e0a-240">**линепарк**</span><span class="sxs-lookup"><span data-stu-id="d2e0a-240">**linePark**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linepark)     | <span data-ttu-id="d2e0a-241">Парки данный вызов по другому адресу.</span><span class="sxs-lookup"><span data-stu-id="d2e0a-241">Parks a given call at another address.</span></span> <span data-ttu-id="d2e0a-242">Асинхронная.</span><span class="sxs-lookup"><span data-stu-id="d2e0a-242">Asynchronous.</span></span> |
| [<span data-ttu-id="d2e0a-243">**линеунпарк**</span><span class="sxs-lookup"><span data-stu-id="d2e0a-243">**lineUnpark**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineunpark) | <span data-ttu-id="d2e0a-244">Извлекает приостановленный вызов.</span><span class="sxs-lookup"><span data-stu-id="d2e0a-244">Retrieves a parked call.</span></span> <span data-ttu-id="d2e0a-245">Асинхронная.</span><span class="sxs-lookup"><span data-stu-id="d2e0a-245">Asynchronous.</span></span>               |



 

## <a name="call-forwarding"></a><span data-ttu-id="d2e0a-246">Переадресация вызовов</span><span class="sxs-lookup"><span data-stu-id="d2e0a-246">Call Forwarding</span></span>



| <span data-ttu-id="d2e0a-247">Функция</span><span class="sxs-lookup"><span data-stu-id="d2e0a-247">Function</span></span>                           | <span data-ttu-id="d2e0a-248">Описание</span><span class="sxs-lookup"><span data-stu-id="d2e0a-248">Description</span></span>                                             |
|------------------------------------|---------------------------------------------------------|
| [<span data-ttu-id="d2e0a-249">**линефорвард**</span><span class="sxs-lookup"><span data-stu-id="d2e0a-249">**lineForward**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineforward) | <span data-ttu-id="d2e0a-250">Задает или отменяет запросы на пересылку вызовов.</span><span class="sxs-lookup"><span data-stu-id="d2e0a-250">Sets or cancels call forwarding requests.</span></span> <span data-ttu-id="d2e0a-251">Асинхронная.</span><span class="sxs-lookup"><span data-stu-id="d2e0a-251">Asynchronous.</span></span> |



 

## <a name="call-pickup"></a><span data-ttu-id="d2e0a-252">Отправка вызова</span><span class="sxs-lookup"><span data-stu-id="d2e0a-252">Call Pickup</span></span>



| <span data-ttu-id="d2e0a-253">Функция</span><span class="sxs-lookup"><span data-stu-id="d2e0a-253">Function</span></span>                         | <span data-ttu-id="d2e0a-254">Описание</span><span class="sxs-lookup"><span data-stu-id="d2e0a-254">Description</span></span>                                                                                                                                                                                      |
|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d2e0a-255">**линепиккуп**</span><span class="sxs-lookup"><span data-stu-id="d2e0a-255">**linePickup**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linepickup) | <span data-ttu-id="d2e0a-256">Получает оповещение о вызовах по указанному адресу назначения и возвращает маркер вызова для вызова по выбранному вызову ([**линепиккуп**](/windows/desktop/api/Tapi/nf-tapi-linepickup) можно также использовать для ожидания вызова).</span><span class="sxs-lookup"><span data-stu-id="d2e0a-256">Picks up a call alerting at a specified destination address and returns a call handle for the picked-up call ([**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) can also be used for call waiting).</span></span> <span data-ttu-id="d2e0a-257">Асинхронная.</span><span class="sxs-lookup"><span data-stu-id="d2e0a-257">Asynchronous.</span></span> |



 

## <a name="sending-information-to-remote-party"></a><span data-ttu-id="d2e0a-258">Отправка сведений удаленному лицу</span><span class="sxs-lookup"><span data-stu-id="d2e0a-258">Sending Information to Remote Party</span></span>



| <span data-ttu-id="d2e0a-259">Функция</span><span class="sxs-lookup"><span data-stu-id="d2e0a-259">Function</span></span>                                                   | <span data-ttu-id="d2e0a-260">Описание</span><span class="sxs-lookup"><span data-stu-id="d2e0a-260">Description</span></span>                                                                                                         |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d2e0a-261">**линерелеасеусерусеринфо**</span><span class="sxs-lookup"><span data-stu-id="d2e0a-261">**lineReleaseUserUserInfo**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linereleaseuseruserinfo) | <span data-ttu-id="d2e0a-262">Выпускают сведения о пользователях, позволяя системе перезаписать это хранилище новыми данными.</span><span class="sxs-lookup"><span data-stu-id="d2e0a-262">Releases user-user information, permitting the system to overwrite this storage with new information.</span></span> <span data-ttu-id="d2e0a-263">Асинхронная.</span><span class="sxs-lookup"><span data-stu-id="d2e0a-263">Asynchronous.</span></span> |
| [<span data-ttu-id="d2e0a-264">**линесендусерусеринфо**</span><span class="sxs-lookup"><span data-stu-id="d2e0a-264">**lineSendUserUserInfo**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesenduseruserinfo)       | <span data-ttu-id="d2e0a-265">Отправляет сведения о пользователе в удаленную сторону в указанном вызове.</span><span class="sxs-lookup"><span data-stu-id="d2e0a-265">Sends user-user information to the remote party on the specified call.</span></span> <span data-ttu-id="d2e0a-266">Асинхронная.</span><span class="sxs-lookup"><span data-stu-id="d2e0a-266">Asynchronous.</span></span>                                |



 

## <a name="call-completion"></a><span data-ttu-id="d2e0a-267">Завершение вызова</span><span class="sxs-lookup"><span data-stu-id="d2e0a-267">Call Completion</span></span>



| <span data-ttu-id="d2e0a-268">Функция</span><span class="sxs-lookup"><span data-stu-id="d2e0a-268">Function</span></span>                                         | <span data-ttu-id="d2e0a-269">Описание</span><span class="sxs-lookup"><span data-stu-id="d2e0a-269">Description</span></span>                                      |
|--------------------------------------------------|--------------------------------------------------|
| [<span data-ttu-id="d2e0a-270">**линекомплетекалл**</span><span class="sxs-lookup"><span data-stu-id="d2e0a-270">**lineCompleteCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linecompletecall)     | <span data-ttu-id="d2e0a-271">Помещает запрос на завершение вызова.</span><span class="sxs-lookup"><span data-stu-id="d2e0a-271">Places a call completion request.</span></span> <span data-ttu-id="d2e0a-272">Асинхронная.</span><span class="sxs-lookup"><span data-stu-id="d2e0a-272">Asynchronous.</span></span>  |
| [<span data-ttu-id="d2e0a-273">**линеункомплетекалл**</span><span class="sxs-lookup"><span data-stu-id="d2e0a-273">**lineUncompleteCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineuncompletecall) | <span data-ttu-id="d2e0a-274">Отменяет запрос на завершение вызова.</span><span class="sxs-lookup"><span data-stu-id="d2e0a-274">Cancels a call completion request.</span></span> <span data-ttu-id="d2e0a-275">Асинхронная.</span><span class="sxs-lookup"><span data-stu-id="d2e0a-275">Asynchronous.</span></span> |



 

## <a name="setting-a-terminal-for-phone-conversations"></a><span data-ttu-id="d2e0a-276">Настройка терминала для телефонных разговоров</span><span class="sxs-lookup"><span data-stu-id="d2e0a-276">Setting a Terminal for Phone Conversations</span></span>



| <span data-ttu-id="d2e0a-277">Функция</span><span class="sxs-lookup"><span data-stu-id="d2e0a-277">Function</span></span>                                   | <span data-ttu-id="d2e0a-278">Описание</span><span class="sxs-lookup"><span data-stu-id="d2e0a-278">Description</span></span>                                                                                                                      |
|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d2e0a-279">**линесеттерминал**</span><span class="sxs-lookup"><span data-stu-id="d2e0a-279">**lineSetTerminal**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetterminal) | <span data-ttu-id="d2e0a-280">Указывает устройство терминала, на которое направляются указанные строки, события адреса или вызовы событий потока мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="d2e0a-280">Specifies the terminal device to which the specified line, address events, or call media stream events are routed.</span></span> <span data-ttu-id="d2e0a-281">Асинхронная.</span><span class="sxs-lookup"><span data-stu-id="d2e0a-281">Asynchronous.</span></span> |



 

## <a name="application-priority"></a><span data-ttu-id="d2e0a-282">Приоритет приложения</span><span class="sxs-lookup"><span data-stu-id="d2e0a-282">Application Priority</span></span>



| <span data-ttu-id="d2e0a-283">Функция</span><span class="sxs-lookup"><span data-stu-id="d2e0a-283">Function</span></span>                                         | <span data-ttu-id="d2e0a-284">Описание</span><span class="sxs-lookup"><span data-stu-id="d2e0a-284">Description</span></span>                                                                                       |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d2e0a-285">**линежетаппприорити**</span><span class="sxs-lookup"><span data-stu-id="d2e0a-285">**lineGetAppPriority**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetapppriority) | <span data-ttu-id="d2e0a-286">Извлекает сведения о передаче и/или помощи по приоритету телефонии для приложения.</span><span class="sxs-lookup"><span data-stu-id="d2e0a-286">Retrieves handoff and/or Assisted Telephony priority information for an application.</span></span> <span data-ttu-id="d2e0a-287">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="d2e0a-287">Synchronous.</span></span> |
| [<span data-ttu-id="d2e0a-288">**линесетаппприорити**</span><span class="sxs-lookup"><span data-stu-id="d2e0a-288">**lineSetAppPriority**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetapppriority) | <span data-ttu-id="d2e0a-289">Задает приоритет абонентской или вспомогательной телефонии для приложения.</span><span class="sxs-lookup"><span data-stu-id="d2e0a-289">Sets the handoff and/or Assisted Telephony priority for an application.</span></span> <span data-ttu-id="d2e0a-290">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="d2e0a-290">Synchronous.</span></span>              |



 

## <a name="service-provider-management"></a><span data-ttu-id="d2e0a-291">Управление поставщиками услуг</span><span class="sxs-lookup"><span data-stu-id="d2e0a-291">Service Provider Management</span></span>



| <span data-ttu-id="d2e0a-292">Функция</span><span class="sxs-lookup"><span data-stu-id="d2e0a-292">Function</span></span>                                           | <span data-ttu-id="d2e0a-293">Описание</span><span class="sxs-lookup"><span data-stu-id="d2e0a-293">Description</span></span>                                                           |
|----------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="d2e0a-294">**линеаддпровидер**</span><span class="sxs-lookup"><span data-stu-id="d2e0a-294">**lineAddProvider**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineaddprovider)         | <span data-ttu-id="d2e0a-295">Устанавливает поставщика услуг телефонии.</span><span class="sxs-lookup"><span data-stu-id="d2e0a-295">Installs a telephony service provider.</span></span> <span data-ttu-id="d2e0a-296">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="d2e0a-296">Synchronous.</span></span>                   |
| [<span data-ttu-id="d2e0a-297">**линеконфигпровидер**</span><span class="sxs-lookup"><span data-stu-id="d2e0a-297">**lineConfigProvider**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineconfigprovider)   | <span data-ttu-id="d2e0a-298">Отображает диалоговое окно конфигурации поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="d2e0a-298">Displays configuration dialog box of a service provider.</span></span> <span data-ttu-id="d2e0a-299">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="d2e0a-299">Synchronous.</span></span> |
| [<span data-ttu-id="d2e0a-300">**линеремовепровидер**</span><span class="sxs-lookup"><span data-stu-id="d2e0a-300">**lineRemoveProvider**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineremoveprovider)   | <span data-ttu-id="d2e0a-301">Удаляет существующего поставщика услуг телефонии.</span><span class="sxs-lookup"><span data-stu-id="d2e0a-301">Removes an existing telephony service provider.</span></span> <span data-ttu-id="d2e0a-302">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="d2e0a-302">Synchronous.</span></span>          |
| [<span data-ttu-id="d2e0a-303">**линежетпровидерлист**</span><span class="sxs-lookup"><span data-stu-id="d2e0a-303">**lineGetProviderList**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetproviderlist) | <span data-ttu-id="d2e0a-304">Извлекает список установленных поставщиков служб.</span><span class="sxs-lookup"><span data-stu-id="d2e0a-304">Retrieves a list of installed service providers.</span></span> <span data-ttu-id="d2e0a-305">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="d2e0a-305">Synchronous.</span></span>         |



 

## <a name="agents"></a><span data-ttu-id="d2e0a-306">Агенты</span><span class="sxs-lookup"><span data-stu-id="d2e0a-306">Agents</span></span>



| <span data-ttu-id="d2e0a-307">Функция</span><span class="sxs-lookup"><span data-stu-id="d2e0a-307">Function</span></span>                                                     | <span data-ttu-id="d2e0a-308">Описание</span><span class="sxs-lookup"><span data-stu-id="d2e0a-308">Description</span></span>                                                                                                                             |
|--------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d2e0a-309">**линеажентспеЦифик**</span><span class="sxs-lookup"><span data-stu-id="d2e0a-309">**lineAgentSpecific**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineagentspecific)               | <span data-ttu-id="d2e0a-310">Позволяет приложению обращаться к собственным функциям обработчика агента, связанным с адресом.</span><span class="sxs-lookup"><span data-stu-id="d2e0a-310">Allows the application to access proprietary handler-specific functions of the agent handler associated with the address.</span></span> <span data-ttu-id="d2e0a-311">Асинхронная.</span><span class="sxs-lookup"><span data-stu-id="d2e0a-311">Asynchronous.</span></span> |
| [<span data-ttu-id="d2e0a-312">**линежетажентактивитилист**</span><span class="sxs-lookup"><span data-stu-id="d2e0a-312">**lineGetAgentActivityList**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetagentactivitylista) | <span data-ttu-id="d2e0a-313">Получает список действий, из которых приложение выбирает функции, выполняемые агентом.</span><span class="sxs-lookup"><span data-stu-id="d2e0a-313">Obtains the list of activities from which an application selects the functions an agent is performing.</span></span> <span data-ttu-id="d2e0a-314">Асинхронная.</span><span class="sxs-lookup"><span data-stu-id="d2e0a-314">Asynchronous.</span></span>                    |
| [<span data-ttu-id="d2e0a-315">**линежетаженткапс**</span><span class="sxs-lookup"><span data-stu-id="d2e0a-315">**lineGetAgentCaps**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetagentcapsa)                 | <span data-ttu-id="d2e0a-316">Получает возможности, связанные с агентом, которые поддерживаются на указанном устройстве линии.</span><span class="sxs-lookup"><span data-stu-id="d2e0a-316">Obtains the agent-related capabilities supported on the specified line device.</span></span> <span data-ttu-id="d2e0a-317">Асинхронная.</span><span class="sxs-lookup"><span data-stu-id="d2e0a-317">Asynchronous.</span></span>                                            |
| [<span data-ttu-id="d2e0a-318">**линежетажентграуплист**</span><span class="sxs-lookup"><span data-stu-id="d2e0a-318">**lineGetAgentGroupList**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetagentgrouplista)       | <span data-ttu-id="d2e0a-319">Получает список групп агентов, в которые агент может войти в систему на автоматическом распространителе вызовов.</span><span class="sxs-lookup"><span data-stu-id="d2e0a-319">Obtains the list of agent groups into which an agent can log into on the automatic call distributor.</span></span> <span data-ttu-id="d2e0a-320">Асинхронная.</span><span class="sxs-lookup"><span data-stu-id="d2e0a-320">Asynchronous.</span></span>                      |
| [<span data-ttu-id="d2e0a-321">**линежетажентстатус**</span><span class="sxs-lookup"><span data-stu-id="d2e0a-321">**lineGetAgentStatus**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa)             | <span data-ttu-id="d2e0a-322">Получает состояние, связанное с агентом, по указанному адресу.</span><span class="sxs-lookup"><span data-stu-id="d2e0a-322">Obtains the agent-related status on the specified address.</span></span> <span data-ttu-id="d2e0a-323">Асинхронная.</span><span class="sxs-lookup"><span data-stu-id="d2e0a-323">Asynchronous.</span></span>                                                                |
| [<span data-ttu-id="d2e0a-324">**линесетажентактивити**</span><span class="sxs-lookup"><span data-stu-id="d2e0a-324">**lineSetAgentActivity**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetagentactivity)         | <span data-ttu-id="d2e0a-325">Задает код действия агента, связанный с определенным адресом.</span><span class="sxs-lookup"><span data-stu-id="d2e0a-325">Sets the agent activity code associated with a particular address.</span></span> <span data-ttu-id="d2e0a-326">Асинхронная.</span><span class="sxs-lookup"><span data-stu-id="d2e0a-326">Asynchronous.</span></span>                                                        |
| [<span data-ttu-id="d2e0a-327">**линесетажентграуп**</span><span class="sxs-lookup"><span data-stu-id="d2e0a-327">**lineSetAgentGroup**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetagentgroup)               | <span data-ttu-id="d2e0a-328">Задает группы агентов, на которые вошел агент по определенному адресу.</span><span class="sxs-lookup"><span data-stu-id="d2e0a-328">Sets the agent groups that the agent is logged into on a particular address.</span></span> <span data-ttu-id="d2e0a-329">Асинхронная.</span><span class="sxs-lookup"><span data-stu-id="d2e0a-329">Asynchronous.</span></span>                                              |
| [<span data-ttu-id="d2e0a-330">**линесетажентстате**</span><span class="sxs-lookup"><span data-stu-id="d2e0a-330">**lineSetAgentState**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetagentstate)               | <span data-ttu-id="d2e0a-331">Задает состояние агента, связанное с определенным адресом.</span><span class="sxs-lookup"><span data-stu-id="d2e0a-331">Sets the agent state associated with a particular address.</span></span> <span data-ttu-id="d2e0a-332">Асинхронная.</span><span class="sxs-lookup"><span data-stu-id="d2e0a-332">Asynchronous.</span></span>                                                                |



 

## <a name="proxies"></a><span data-ttu-id="d2e0a-333">прокси-серверы;</span><span class="sxs-lookup"><span data-stu-id="d2e0a-333">Proxies</span></span>



| <span data-ttu-id="d2e0a-334">Функция</span><span class="sxs-lookup"><span data-stu-id="d2e0a-334">Function</span></span>                                       | <span data-ttu-id="d2e0a-335">Описание</span><span class="sxs-lookup"><span data-stu-id="d2e0a-335">Description</span></span>                                                                         |
|------------------------------------------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="d2e0a-336">**линепроксимессаже**</span><span class="sxs-lookup"><span data-stu-id="d2e0a-336">**lineProxyMessage**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage)   | <span data-ttu-id="d2e0a-337">Используется зарегистрированным обработчиком прокси-запросов для создания сообщений TAPI.</span><span class="sxs-lookup"><span data-stu-id="d2e0a-337">Used by a registered proxy request handler to generate TAPI messages.</span></span> <span data-ttu-id="d2e0a-338">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="d2e0a-338">Synchronous.</span></span>  |
| [<span data-ttu-id="d2e0a-339">**линепроксиреспонсе**</span><span class="sxs-lookup"><span data-stu-id="d2e0a-339">**lineProxyResponse**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse) | <span data-ttu-id="d2e0a-340">Указывает на завершение запроса прокси-сервера зарегистрированным обработчиком прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="d2e0a-340">Indicates completion of a proxy request by a registered proxy handler.</span></span> <span data-ttu-id="d2e0a-341">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="d2e0a-341">Synchronous.</span></span> |



 

## <a name="quality-of-service"></a><span data-ttu-id="d2e0a-342">Качество обслуживания</span><span class="sxs-lookup"><span data-stu-id="d2e0a-342">Quality of Service</span></span>



| <span data-ttu-id="d2e0a-343">Функция</span><span class="sxs-lookup"><span data-stu-id="d2e0a-343">Function</span></span>                                                           | <span data-ttu-id="d2e0a-344">Описание</span><span class="sxs-lookup"><span data-stu-id="d2e0a-344">Description</span></span>                                                                                |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d2e0a-345">**линесеткаллкуалитйофсервице**</span><span class="sxs-lookup"><span data-stu-id="d2e0a-345">**lineSetCallQualityOfService**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetcallqualityofservice) | <span data-ttu-id="d2e0a-346">Запрашивает изменение параметров качества обслуживания для существующего вызова.</span><span class="sxs-lookup"><span data-stu-id="d2e0a-346">Requests a change of the quality of service parameters for an existing call.</span></span> <span data-ttu-id="d2e0a-347">Асинхронная.</span><span class="sxs-lookup"><span data-stu-id="d2e0a-347">Asynchronous.</span></span> |



 

## <a name="miscellaneous"></a><span data-ttu-id="d2e0a-348">Разное</span><span class="sxs-lookup"><span data-stu-id="d2e0a-348">Miscellaneous</span></span>



| <span data-ttu-id="d2e0a-349">Функция</span><span class="sxs-lookup"><span data-stu-id="d2e0a-349">Function</span></span>                                             | <span data-ttu-id="d2e0a-350">Описание</span><span class="sxs-lookup"><span data-stu-id="d2e0a-350">Description</span></span>                                                                                           |
|------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d2e0a-351">**линесеткаллдата**</span><span class="sxs-lookup"><span data-stu-id="d2e0a-351">**lineSetCallData**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetcalldata)           | <span data-ttu-id="d2e0a-352">Задает элемент **каллдата** структуры [**линекаллинфо**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) .</span><span class="sxs-lookup"><span data-stu-id="d2e0a-352">Sets the **CallData** member of the [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) structure.</span></span> <span data-ttu-id="d2e0a-353">Асинхронная.</span><span class="sxs-lookup"><span data-stu-id="d2e0a-353">Asynchronous.</span></span> |
| [<span data-ttu-id="d2e0a-354">**линесеткаллтреатмент**</span><span class="sxs-lookup"><span data-stu-id="d2e0a-354">**lineSetCallTreatment**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetcalltreatment) | <span data-ttu-id="d2e0a-355">Задает звуки, которые пользователь слышит при отсутствии ответа или удержании звонка.</span><span class="sxs-lookup"><span data-stu-id="d2e0a-355">Sets the sounds that the user hears when a call is unanswered or on hold.</span></span> <span data-ttu-id="d2e0a-356">Асинхронная.</span><span class="sxs-lookup"><span data-stu-id="d2e0a-356">Asynchronous.</span></span>               |
| [<span data-ttu-id="d2e0a-357">**линесетлинедевстатус**</span><span class="sxs-lookup"><span data-stu-id="d2e0a-357">**lineSetLineDevStatus**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetlinedevstatus) | <span data-ttu-id="d2e0a-358">Задает состояние устройства линии.</span><span class="sxs-lookup"><span data-stu-id="d2e0a-358">Sets the line device status.</span></span> <span data-ttu-id="d2e0a-359">Асинхронная.</span><span class="sxs-lookup"><span data-stu-id="d2e0a-359">Asynchronous.</span></span>                                                            |



 

 

 



