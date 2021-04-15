---
description: Основные функции телефонии перечислены по категориям в следующих таблицах.
ms.assetid: 09d10789-bc36-47c7-b77d-8698ae75541a
title: Справочник по базовым службам телефонии
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abe1282a406ea6746f1bb3af11d65164d8af0ce0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683159"
---
# <a name="basic-telephony-services-reference"></a><span data-ttu-id="cc892-103">Справочник по базовым службам телефонии</span><span class="sxs-lookup"><span data-stu-id="cc892-103">Basic Telephony Services Reference</span></span>

<span data-ttu-id="cc892-104">Основные функции телефонии перечислены по категориям в следующих таблицах.</span><span class="sxs-lookup"><span data-stu-id="cc892-104">The Basic Telephony functions are listed by category in the following tables.</span></span> <span data-ttu-id="cc892-105">Функция определяется как [*асинхронная*](a-tapgloss.md) , если она указывает на завершение в ответном сообщении для приложения.</span><span class="sxs-lookup"><span data-stu-id="cc892-105">A function is identified as [*asynchronous*](a-tapgloss.md) if it indicates completion in a REPLY message to the application.</span></span> <span data-ttu-id="cc892-106">Если функция всегда возвращает результат в приложение немедленно, функция считается [*синхронной*](s-tapgloss.md).</span><span class="sxs-lookup"><span data-stu-id="cc892-106">If the function always returns its result to the application immediately, the function is considered [*synchronous*](s-tapgloss.md).</span></span>

<span data-ttu-id="cc892-107">Ниже приведена функциональная группировка основных функций службы телефонии.</span><span class="sxs-lookup"><span data-stu-id="cc892-107">Following is a functional grouping of the basic telephony service functions:</span></span>

-   [<span data-ttu-id="cc892-108">Форматы адресов</span><span class="sxs-lookup"><span data-stu-id="cc892-108">Address Formats</span></span>](#address-formats)
-   [<span data-ttu-id="cc892-109">Адреса</span><span class="sxs-lookup"><span data-stu-id="cc892-109">Addresses</span></span>](#addresses)
-   [<span data-ttu-id="cc892-110">Ответ на входящие вызовы</span><span class="sxs-lookup"><span data-stu-id="cc892-110">Answering Incoming Calls</span></span>](#answering-incoming-calls)
-   [<span data-ttu-id="cc892-111">Вызов функций Drop</span><span class="sxs-lookup"><span data-stu-id="cc892-111">Call Drop Functions</span></span>](#call-drop-functions)
-   [<span data-ttu-id="cc892-112">Обработка обработки вызовов</span><span class="sxs-lookup"><span data-stu-id="cc892-112">Call Handle Manipulation</span></span>](#call-handle-manipulation)
-   [<span data-ttu-id="cc892-113">Управление правами вызова</span><span class="sxs-lookup"><span data-stu-id="cc892-113">Call Privilege Control</span></span>](#call-privilege-control)
-   [<span data-ttu-id="cc892-114">Состояния вызовов и события</span><span class="sxs-lookup"><span data-stu-id="cc892-114">Call States and Events</span></span>](#call-states-and-events)
-   [<span data-ttu-id="cc892-115">Состояние и возможности линий</span><span class="sxs-lookup"><span data-stu-id="cc892-115">Line Status and Capabilities</span></span>](#line-status-and-capabilities)
-   [<span data-ttu-id="cc892-116">Согласование версии строки</span><span class="sxs-lookup"><span data-stu-id="cc892-116">Line Version Negotiation</span></span>](#line-version-negotiation)
-   [<span data-ttu-id="cc892-117">Сведения о расположении и стране или регионе</span><span class="sxs-lookup"><span data-stu-id="cc892-117">Location and Country/Region Information</span></span>](#location-and-countryregion-information)
-   [<span data-ttu-id="cc892-118">Выполнение вызовов</span><span class="sxs-lookup"><span data-stu-id="cc892-118">Making Calls</span></span>](#making-calls)
-   [<span data-ttu-id="cc892-119">Открытие и закрытие линейных устройств</span><span class="sxs-lookup"><span data-stu-id="cc892-119">Opening and Closing Line Devices</span></span>](#opening-and-closing-line-devices)
-   [<span data-ttu-id="cc892-120">Запрос служб получателя</span><span class="sxs-lookup"><span data-stu-id="cc892-120">Request Recipient Services</span></span>](#request-recipient-services)
-   [<span data-ttu-id="cc892-121">Инициализация и завершение работы TAPI</span><span class="sxs-lookup"><span data-stu-id="cc892-121">TAPI Initialization and Shutdown</span></span>](#tapi-initialization-and-shutdown)
-   [<span data-ttu-id="cc892-122">Поддержка платных заставок</span><span class="sxs-lookup"><span data-stu-id="cc892-122">Toll Saver Support</span></span>](#toll-saver-support)

## <a name="tapi-initialization-and-shutdown"></a><span data-ttu-id="cc892-123">Инициализация и завершение работы TAPI</span><span class="sxs-lookup"><span data-stu-id="cc892-123">TAPI Initialization and Shutdown</span></span>



| <span data-ttu-id="cc892-124">Функция</span><span class="sxs-lookup"><span data-stu-id="cc892-124">Function</span></span>                                     | <span data-ttu-id="cc892-125">Описание</span><span class="sxs-lookup"><span data-stu-id="cc892-125">Description</span></span>                                                                             |
|----------------------------------------------|-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="cc892-126">**линеинитиализикс**</span><span class="sxs-lookup"><span data-stu-id="cc892-126">**lineInitializeEx**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa) | <span data-ttu-id="cc892-127">Инициализирует абстракцию линии TAPI для использования вызывающим приложением.</span><span class="sxs-lookup"><span data-stu-id="cc892-127">Initializes the TAPI line abstraction for use by the invoking application.</span></span> <span data-ttu-id="cc892-128">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="cc892-128">Synchronous.</span></span> |
| [<span data-ttu-id="cc892-129">**линешутдовн**</span><span class="sxs-lookup"><span data-stu-id="cc892-129">**lineShutdown**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineshutdown)         | <span data-ttu-id="cc892-130">Завершает работу приложения, использующего абстракцию строки TAPI.</span><span class="sxs-lookup"><span data-stu-id="cc892-130">Shuts down the application's use of TAPI's line abstraction.</span></span> <span data-ttu-id="cc892-131">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="cc892-131">Synchronous.</span></span>               |



 

## <a name="line-version-negotiation"></a><span data-ttu-id="cc892-132">Согласование версии строки</span><span class="sxs-lookup"><span data-stu-id="cc892-132">Line Version Negotiation</span></span>



| <span data-ttu-id="cc892-133">Функция</span><span class="sxs-lookup"><span data-stu-id="cc892-133">Function</span></span>                                                   | <span data-ttu-id="cc892-134">Описание</span><span class="sxs-lookup"><span data-stu-id="cc892-134">Description</span></span>                                                            |
|------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="cc892-135">**линенеготиатеапиверсион**</span><span class="sxs-lookup"><span data-stu-id="cc892-135">**lineNegotiateAPIVersion**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linenegotiateapiversion) | <span data-ttu-id="cc892-136">Позволяет приложению согласовывать версию TAPI для использования.</span><span class="sxs-lookup"><span data-stu-id="cc892-136">Allows an application to negotiate a TAPI version to use.</span></span> <span data-ttu-id="cc892-137">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="cc892-137">Synchronous.</span></span> |



 

## <a name="line-status-and-capabilities"></a><span data-ttu-id="cc892-138">Состояние и возможности линий</span><span class="sxs-lookup"><span data-stu-id="cc892-138">Line Status and Capabilities</span></span>



| <span data-ttu-id="cc892-139">Функция</span><span class="sxs-lookup"><span data-stu-id="cc892-139">Function</span></span>                                               | <span data-ttu-id="cc892-140">Описание</span><span class="sxs-lookup"><span data-stu-id="cc892-140">Description</span></span>                                                                                                                                                    |
|--------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cc892-141">**линежетдевкапс**</span><span class="sxs-lookup"><span data-stu-id="cc892-141">**lineGetDevCaps**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetdevcaps)               | <span data-ttu-id="cc892-142">Возвращает возможности данного устройства линии.</span><span class="sxs-lookup"><span data-stu-id="cc892-142">Returns the capabilities of a given line device.</span></span> <span data-ttu-id="cc892-143">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="cc892-143">Synchronous.</span></span>                                                                                                  |
| [<span data-ttu-id="cc892-144">**линежетдевконфиг**</span><span class="sxs-lookup"><span data-stu-id="cc892-144">**lineGetDevConfig**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig)           | <span data-ttu-id="cc892-145">Возвращает конфигурацию устройства потоковой передачи мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="cc892-145">Returns configuration of a media stream device.</span></span> <span data-ttu-id="cc892-146">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="cc892-146">Synchronous.</span></span>                                                                                                   |
| [<span data-ttu-id="cc892-147">**линежетлинедевстатус**</span><span class="sxs-lookup"><span data-stu-id="cc892-147">**lineGetLineDevStatus**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus)   | <span data-ttu-id="cc892-148">Возвращает текущее состояние указанного устройства с открытым графиком.</span><span class="sxs-lookup"><span data-stu-id="cc892-148">Returns current status of the specified open line device.</span></span> <span data-ttu-id="cc892-149">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="cc892-149">Synchronous.</span></span>                                                                                         |
| [<span data-ttu-id="cc892-150">**линесетдевконфиг**</span><span class="sxs-lookup"><span data-stu-id="cc892-150">**lineSetDevConfig**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig)           | <span data-ttu-id="cc892-151">Задает конфигурацию указанного устройства потока мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="cc892-151">Sets the configuration of the specified media stream device.</span></span> <span data-ttu-id="cc892-152">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="cc892-152">Synchronous.</span></span>                                                                                      |
| [<span data-ttu-id="cc892-153">**линесетстатусмессажес**</span><span class="sxs-lookup"><span data-stu-id="cc892-153">**lineSetStatusMessages**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetstatusmessages) | <span data-ttu-id="cc892-154">Указывает изменения состояния, для которых приложение должно получать уведомления.</span><span class="sxs-lookup"><span data-stu-id="cc892-154">Specifies the status changes for which the application needs to be notified.</span></span> <span data-ttu-id="cc892-155">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="cc892-155">Synchronous.</span></span>                                                                      |
| [<span data-ttu-id="cc892-156">**линежетстатусмессажес**</span><span class="sxs-lookup"><span data-stu-id="cc892-156">**lineGetStatusMessages**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetstatusmessages) | <span data-ttu-id="cc892-157">Возвращает текущую строку приложения и параметры сообщения о состоянии адреса.</span><span class="sxs-lookup"><span data-stu-id="cc892-157">Returns the application's current line and address status message settings.</span></span> <span data-ttu-id="cc892-158">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="cc892-158">Synchronous.</span></span>                                                                       |
| [<span data-ttu-id="cc892-159">**линежетид**</span><span class="sxs-lookup"><span data-stu-id="cc892-159">**lineGetID**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetid)                         | <span data-ttu-id="cc892-160">Извлекает идентификатор устройства, связанный с указанной открытой строкой, адресом или вызовом.</span><span class="sxs-lookup"><span data-stu-id="cc892-160">Retrieves a device ID associated with the specified open line, address, or call.</span></span> <span data-ttu-id="cc892-161">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="cc892-161">Synchronous.</span></span>                                                                  |
| [<span data-ttu-id="cc892-162">**линежетикон**</span><span class="sxs-lookup"><span data-stu-id="cc892-162">**lineGetIcon**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegeticon)                     | <span data-ttu-id="cc892-163">Позволяет приложению получить значок для показа пользователю.</span><span class="sxs-lookup"><span data-stu-id="cc892-163">Allows an application to retrieve an icon for display to the user.</span></span> <span data-ttu-id="cc892-164">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="cc892-164">Synchronous.</span></span>                                                                                |
| [<span data-ttu-id="cc892-165">**линеконфигдиалог**</span><span class="sxs-lookup"><span data-stu-id="cc892-165">**lineConfigDialog**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineconfigdialog)           | <span data-ttu-id="cc892-166">Заставляет поставщик указанного устройства отображать диалоговое окно, позволяющее пользователю настраивать параметры, связанные с устройством линии.</span><span class="sxs-lookup"><span data-stu-id="cc892-166">Causes the provider of the specified line device to display a dialog box that allows the user to configure parameters related to the line device.</span></span> <span data-ttu-id="cc892-167">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="cc892-167">Synchronous.</span></span> |
| [<span data-ttu-id="cc892-168">**линеконфигдиаложедит**</span><span class="sxs-lookup"><span data-stu-id="cc892-168">**lineConfigDialogEdit**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineconfigdialogedit)   | <span data-ttu-id="cc892-169">Отображает диалоговое окно, позволяющее пользователю изменить сведения о конфигурации для линейного устройства.</span><span class="sxs-lookup"><span data-stu-id="cc892-169">Displays a dialog box allowing the user to change configuration information for a line device.</span></span> <span data-ttu-id="cc892-170">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="cc892-170">Synchronous.</span></span>                                                    |



 

## <a name="addresses"></a><span data-ttu-id="cc892-171">Адреса</span><span class="sxs-lookup"><span data-stu-id="cc892-171">Addresses</span></span>



| <span data-ttu-id="cc892-172">Функция</span><span class="sxs-lookup"><span data-stu-id="cc892-172">Function</span></span>                                             | <span data-ttu-id="cc892-173">Описание</span><span class="sxs-lookup"><span data-stu-id="cc892-173">Description</span></span>                                                                              |
|------------------------------------------------------|------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cc892-174">**линежетаддресскапс**</span><span class="sxs-lookup"><span data-stu-id="cc892-174">**lineGetAddressCaps**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps)     | <span data-ttu-id="cc892-175">Возвращает возможности телефонии адреса.</span><span class="sxs-lookup"><span data-stu-id="cc892-175">Returns the telephony capabilities of an address.</span></span> <span data-ttu-id="cc892-176">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="cc892-176">Synchronous.</span></span>                           |
| [<span data-ttu-id="cc892-177">**линежетаддрессстатус**</span><span class="sxs-lookup"><span data-stu-id="cc892-177">**lineGetAddressStatus**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetaddressstatus) | <span data-ttu-id="cc892-178">Возвращает текущее состояние указанного адреса.</span><span class="sxs-lookup"><span data-stu-id="cc892-178">Returns current status of a specified address.</span></span> <span data-ttu-id="cc892-179">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="cc892-179">Synchronous.</span></span>                              |
| [<span data-ttu-id="cc892-180">**линежетаддрессид**</span><span class="sxs-lookup"><span data-stu-id="cc892-180">**lineGetAddressID**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetaddressid)         | <span data-ttu-id="cc892-181">Извлекает идентификатор адреса, указанного в альтернативном формате.</span><span class="sxs-lookup"><span data-stu-id="cc892-181">Retrieves the address ID of an address specified using an alternate format.</span></span> <span data-ttu-id="cc892-182">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="cc892-182">Synchronous.</span></span> |



 

## <a name="opening-and-closing-line-devices"></a><span data-ttu-id="cc892-183">Открытие и закрытие линейных устройств</span><span class="sxs-lookup"><span data-stu-id="cc892-183">Opening and Closing Line Devices</span></span>



| <span data-ttu-id="cc892-184">Функция</span><span class="sxs-lookup"><span data-stu-id="cc892-184">Function</span></span>                       | <span data-ttu-id="cc892-185">Описание</span><span class="sxs-lookup"><span data-stu-id="cc892-185">Description</span></span>                                                                                                |
|--------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cc892-186">**линеопен**</span><span class="sxs-lookup"><span data-stu-id="cc892-186">**lineOpen**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineopen)   | <span data-ttu-id="cc892-187">Открывает указанное устройство линии для последующего мониторинга и (или) управления строкой.</span><span class="sxs-lookup"><span data-stu-id="cc892-187">Opens a specified line device for providing subsequent monitoring and/or control of the line.</span></span> <span data-ttu-id="cc892-188">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="cc892-188">Synchronous.</span></span> |
| [<span data-ttu-id="cc892-189">**линеклосе**</span><span class="sxs-lookup"><span data-stu-id="cc892-189">**lineClose**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineclose) | <span data-ttu-id="cc892-190">Закрывает указанное устройство Open Line.</span><span class="sxs-lookup"><span data-stu-id="cc892-190">Closes a specified opened line device.</span></span> <span data-ttu-id="cc892-191">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="cc892-191">Synchronous.</span></span>                                                        |



 

## <a name="address-formats"></a><span data-ttu-id="cc892-192">Форматы адресов</span><span class="sxs-lookup"><span data-stu-id="cc892-192">Address Formats</span></span>



| <span data-ttu-id="cc892-193">Функция</span><span class="sxs-lookup"><span data-stu-id="cc892-193">Function</span></span>                                                 | <span data-ttu-id="cc892-194">Описание</span><span class="sxs-lookup"><span data-stu-id="cc892-194">Description</span></span>                                                                                       |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cc892-195">**линетранслатеаддресс**</span><span class="sxs-lookup"><span data-stu-id="cc892-195">**lineTranslateAddress**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linetranslateaddress)     | <span data-ttu-id="cc892-196">Преобразует адрес в каноническом формате и адрес в формате с набором.</span><span class="sxs-lookup"><span data-stu-id="cc892-196">Translates between an address in canonical format and an address in dialable format.</span></span> <span data-ttu-id="cc892-197">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="cc892-197">Synchronous.</span></span> |
| [<span data-ttu-id="cc892-198">**линесеткуррентлокатион**</span><span class="sxs-lookup"><span data-stu-id="cc892-198">**lineSetCurrentLocation**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetcurrentlocation) | <span data-ttu-id="cc892-199">Задает расположение, используемое в качестве контекста для преобразования адресов.</span><span class="sxs-lookup"><span data-stu-id="cc892-199">Sets the location used as the context for address translation.</span></span> <span data-ttu-id="cc892-200">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="cc892-200">Synchronous.</span></span>                       |
| [<span data-ttu-id="cc892-201">**линесеттолллист**</span><span class="sxs-lookup"><span data-stu-id="cc892-201">**lineSetTollList**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesettolllist)               | <span data-ttu-id="cc892-202">Обрабатывает платный список.</span><span class="sxs-lookup"><span data-stu-id="cc892-202">Manipulates the toll list.</span></span> <span data-ttu-id="cc892-203">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="cc892-203">Synchronous.</span></span>                                                           |
| [<span data-ttu-id="cc892-204">**линежеттранслатекапс**</span><span class="sxs-lookup"><span data-stu-id="cc892-204">**lineGetTranslateCaps**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps)     | <span data-ttu-id="cc892-205">Возвращает возможности преобразования адресов.</span><span class="sxs-lookup"><span data-stu-id="cc892-205">Returns address translation capabilities.</span></span> <span data-ttu-id="cc892-206">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="cc892-206">Synchronous.</span></span>                                            |



 

## <a name="call-states-and-events"></a><span data-ttu-id="cc892-207">Состояния вызовов и события</span><span class="sxs-lookup"><span data-stu-id="cc892-207">Call States and Events</span></span>



| <span data-ttu-id="cc892-208">Функция</span><span class="sxs-lookup"><span data-stu-id="cc892-208">Function</span></span>                                         | <span data-ttu-id="cc892-209">Описание</span><span class="sxs-lookup"><span data-stu-id="cc892-209">Description</span></span>                                                                         |
|--------------------------------------------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="cc892-210">**линежеткаллинфо**</span><span class="sxs-lookup"><span data-stu-id="cc892-210">**lineGetCallInfo**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetcallinfo)       | <span data-ttu-id="cc892-211">Возвращает фиксированные сведения о вызове.</span><span class="sxs-lookup"><span data-stu-id="cc892-211">Returns fixed information about a call.</span></span> <span data-ttu-id="cc892-212">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="cc892-212">Synchronous.</span></span>                                |
| [<span data-ttu-id="cc892-213">**линежеткаллстатус**</span><span class="sxs-lookup"><span data-stu-id="cc892-213">**lineGetCallStatus**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetcallstatus)   | <span data-ttu-id="cc892-214">Возвращает сведения о состоянии завершения вызова для указанного вызова.</span><span class="sxs-lookup"><span data-stu-id="cc892-214">Returns complete call status information for the specified call.</span></span> <span data-ttu-id="cc892-215">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="cc892-215">Synchronous.</span></span>       |
| [<span data-ttu-id="cc892-216">**линесетаппспеЦифик**</span><span class="sxs-lookup"><span data-stu-id="cc892-216">**lineSetAppSpecific**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetappspecific) | <span data-ttu-id="cc892-217">Задает зависящее от приложения поле структуры сведений о вызове.</span><span class="sxs-lookup"><span data-stu-id="cc892-217">Sets the application-specific field of a call's information structure.</span></span> <span data-ttu-id="cc892-218">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="cc892-218">Synchronous.</span></span> |



 

## <a name="making-calls"></a><span data-ttu-id="cc892-219">Выполнение вызовов</span><span class="sxs-lookup"><span data-stu-id="cc892-219">Making Calls</span></span>



| <span data-ttu-id="cc892-220">Функция</span><span class="sxs-lookup"><span data-stu-id="cc892-220">Function</span></span>                             | <span data-ttu-id="cc892-221">Описание</span><span class="sxs-lookup"><span data-stu-id="cc892-221">Description</span></span>                                                            |
|--------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="cc892-222">**линемакекалл**</span><span class="sxs-lookup"><span data-stu-id="cc892-222">**lineMakeCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linemakecall) | <span data-ttu-id="cc892-223">Выполняет исходящий вызов и возвращает для него маркер вызова.</span><span class="sxs-lookup"><span data-stu-id="cc892-223">Makes an outbound call and returns a call handle for it.</span></span> <span data-ttu-id="cc892-224">Асинхронная.</span><span class="sxs-lookup"><span data-stu-id="cc892-224">Asynchronous.</span></span> |
| [<span data-ttu-id="cc892-225">**линедиал**</span><span class="sxs-lookup"><span data-stu-id="cc892-225">**lineDial**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linedial)         | <span data-ttu-id="cc892-226">Звонки (части одного или нескольких) коммутируемых адресов.</span><span class="sxs-lookup"><span data-stu-id="cc892-226">Dials (parts of one or more) dialable addresses.</span></span> <span data-ttu-id="cc892-227">Асинхронная.</span><span class="sxs-lookup"><span data-stu-id="cc892-227">Asynchronous.</span></span>         |



 

## <a name="answering-incoming-calls"></a><span data-ttu-id="cc892-228">Ответ на входящие вызовы</span><span class="sxs-lookup"><span data-stu-id="cc892-228">Answering Incoming Calls</span></span>



| <span data-ttu-id="cc892-229">Функция</span><span class="sxs-lookup"><span data-stu-id="cc892-229">Function</span></span>                         | <span data-ttu-id="cc892-230">Описание</span><span class="sxs-lookup"><span data-stu-id="cc892-230">Description</span></span>                             |
|----------------------------------|-----------------------------------------|
| [<span data-ttu-id="cc892-231">**линеансвер**</span><span class="sxs-lookup"><span data-stu-id="cc892-231">**lineAnswer**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineanswer) | <span data-ttu-id="cc892-232">Отвечает на входящий вызов.</span><span class="sxs-lookup"><span data-stu-id="cc892-232">Answers an incoming call.</span></span> <span data-ttu-id="cc892-233">Асинхронная.</span><span class="sxs-lookup"><span data-stu-id="cc892-233">Asynchronous.</span></span> |



 

## <a name="toll-saver-support"></a><span data-ttu-id="cc892-234">Поддержка платных заставок</span><span class="sxs-lookup"><span data-stu-id="cc892-234">Toll Saver Support</span></span>



| <span data-ttu-id="cc892-235">Функция</span><span class="sxs-lookup"><span data-stu-id="cc892-235">Function</span></span>                                   | <span data-ttu-id="cc892-236">Описание</span><span class="sxs-lookup"><span data-stu-id="cc892-236">Description</span></span>                                                                                                 |
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cc892-237">**линесетнумрингс**</span><span class="sxs-lookup"><span data-stu-id="cc892-237">**lineSetNumRings**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetnumrings) | <span data-ttu-id="cc892-238">Указывает число звонков, после которых должны быть получены ответы на входящие вызовы.</span><span class="sxs-lookup"><span data-stu-id="cc892-238">Indicates the number of rings after which incoming calls are to be answered.</span></span> <span data-ttu-id="cc892-239">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="cc892-239">Synchronous.</span></span>                   |
| [<span data-ttu-id="cc892-240">**линежетнумрингс**</span><span class="sxs-lookup"><span data-stu-id="cc892-240">**lineGetNumRings**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetnumrings) | <span data-ttu-id="cc892-241">Возвращает минимальное число колец, запрошенных с помощью [**линесетнумрингс**](/windows/desktop/api/Tapi/nf-tapi-linesetnumrings).</span><span class="sxs-lookup"><span data-stu-id="cc892-241">Returns the minimum number of rings requested with [**lineSetNumRings**](/windows/desktop/api/Tapi/nf-tapi-linesetnumrings).</span></span> <span data-ttu-id="cc892-242">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="cc892-242">Synchronous.</span></span> |



 

## <a name="call-privilege-control"></a><span data-ttu-id="cc892-243">Управление правами вызова</span><span class="sxs-lookup"><span data-stu-id="cc892-243">Call Privilege Control</span></span>



| <span data-ttu-id="cc892-244">Функция</span><span class="sxs-lookup"><span data-stu-id="cc892-244">Function</span></span>                                             | <span data-ttu-id="cc892-245">Описание</span><span class="sxs-lookup"><span data-stu-id="cc892-245">Description</span></span>                                                               |
|------------------------------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="cc892-246">**линесеткаллпривилеже**</span><span class="sxs-lookup"><span data-stu-id="cc892-246">**lineSetCallPrivilege**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetcallprivilege) | <span data-ttu-id="cc892-247">Задает привилегию приложения для указанного права.</span><span class="sxs-lookup"><span data-stu-id="cc892-247">Sets the application's privilege to the privilege specified.</span></span> <span data-ttu-id="cc892-248">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="cc892-248">Synchronous.</span></span> |



 

## <a name="call-drop-functions"></a><span data-ttu-id="cc892-249">Вызов функций Drop</span><span class="sxs-lookup"><span data-stu-id="cc892-249">Call Drop Functions</span></span>



| <span data-ttu-id="cc892-250">Функция</span><span class="sxs-lookup"><span data-stu-id="cc892-250">Function</span></span>                                         | <span data-ttu-id="cc892-251">Описание</span><span class="sxs-lookup"><span data-stu-id="cc892-251">Description</span></span>                                                               |
|--------------------------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="cc892-252">**линедроп**</span><span class="sxs-lookup"><span data-stu-id="cc892-252">**lineDrop**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linedrop)                     | <span data-ttu-id="cc892-253">Отключает вызов или прерывает выполнение попытки вызова.</span><span class="sxs-lookup"><span data-stu-id="cc892-253">Disconnects a call, or abandons a call attempt in progress.</span></span> <span data-ttu-id="cc892-254">Асинхронная.</span><span class="sxs-lookup"><span data-stu-id="cc892-254">Asynchronous.</span></span> |
| [<span data-ttu-id="cc892-255">**линедеаллокатекалл**</span><span class="sxs-lookup"><span data-stu-id="cc892-255">**lineDeallocateCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall) | <span data-ttu-id="cc892-256">Освобождает указанный маркер вызова.</span><span class="sxs-lookup"><span data-stu-id="cc892-256">Deallocates the specified call handle.</span></span> <span data-ttu-id="cc892-257">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="cc892-257">Synchronous.</span></span>                       |



 

## <a name="call-handle-manipulation"></a><span data-ttu-id="cc892-258">Обработка обработки вызовов</span><span class="sxs-lookup"><span data-stu-id="cc892-258">Call Handle Manipulation</span></span>



| <span data-ttu-id="cc892-259">Функция</span><span class="sxs-lookup"><span data-stu-id="cc892-259">Function</span></span>                                                   | <span data-ttu-id="cc892-260">Описание</span><span class="sxs-lookup"><span data-stu-id="cc892-260">Description</span></span>                                                                                                                    |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cc892-261">**линехандофф**</span><span class="sxs-lookup"><span data-stu-id="cc892-261">**lineHandoff**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linehandoff)                         | <span data-ttu-id="cc892-262">Передает права владения вызовом и (или) изменяет привилегии приложения на вызов.</span><span class="sxs-lookup"><span data-stu-id="cc892-262">Hands off call ownership and/or changes an application's privileges to a call.</span></span> <span data-ttu-id="cc892-263">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="cc892-263">Synchronous.</span></span>                                    |
| [<span data-ttu-id="cc892-264">**линежетневкаллс**</span><span class="sxs-lookup"><span data-stu-id="cc892-264">**lineGetNewCalls**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetnewcalls)                 | <span data-ttu-id="cc892-265">Возвращает дескрипторы вызовов для вызовов по указанной строке или адресу, для которых приложение еще не имеет дескрипторов.</span><span class="sxs-lookup"><span data-stu-id="cc892-265">Returns call handles to calls on a specified line or address for which the application does not yet have handles.</span></span> <span data-ttu-id="cc892-266">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="cc892-266">Synchronous.</span></span> |
| [<span data-ttu-id="cc892-267">**линежетконфрелатедкаллс**</span><span class="sxs-lookup"><span data-stu-id="cc892-267">**lineGetConfRelatedCalls**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetconfrelatedcalls) | <span data-ttu-id="cc892-268">Возвращает список дескрипторов вызовов, которые являются частью того же вызова конференции, что и вызов, указанный в качестве параметра.</span><span class="sxs-lookup"><span data-stu-id="cc892-268">Returns a list of call handles that are part of the same conference call as the call specified as a parameter.</span></span> <span data-ttu-id="cc892-269">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="cc892-269">Synchronous.</span></span>    |



 

## <a name="location-and-countryregion-information"></a><span data-ttu-id="cc892-270">Сведения о расположении и стране или регионе</span><span class="sxs-lookup"><span data-stu-id="cc892-270">Location and Country/Region Information</span></span>



| <span data-ttu-id="cc892-271">Функция</span><span class="sxs-lookup"><span data-stu-id="cc892-271">Function</span></span>                                           | <span data-ttu-id="cc892-272">Описание</span><span class="sxs-lookup"><span data-stu-id="cc892-272">Description</span></span>                                                                                           |
|----------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cc892-273">**линетранслатедиалог**</span><span class="sxs-lookup"><span data-stu-id="cc892-273">**lineTranslateDialog**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linetranslatedialog) | <span data-ttu-id="cc892-274">Отображает диалоговое окно, позволяющее пользователю изменить расположение и сведения о телефонной карточке.</span><span class="sxs-lookup"><span data-stu-id="cc892-274">Displays a dialog box allowing the user to change location and calling card information.</span></span> <span data-ttu-id="cc892-275">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="cc892-275">Synchronous.</span></span> |
| [<span data-ttu-id="cc892-276">**линежеткаунтри**</span><span class="sxs-lookup"><span data-stu-id="cc892-276">**lineGetCountry**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetcountry)           | <span data-ttu-id="cc892-277">Получает правила набора номера и другие сведения о конкретной стране или регионе.</span><span class="sxs-lookup"><span data-stu-id="cc892-277">Retrieves dialing rules and other information about a given country/region.</span></span> <span data-ttu-id="cc892-278">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="cc892-278">Synchronous.</span></span>              |



 

## <a name="request-recipient-services"></a><span data-ttu-id="cc892-279">Запрос служб получателя</span><span class="sxs-lookup"><span data-stu-id="cc892-279">Request Recipient Services</span></span>

<span data-ttu-id="cc892-280">Следующие две функции используются только для поддержки телефонной связи.</span><span class="sxs-lookup"><span data-stu-id="cc892-280">The following two functions are used only in support of Assisted Telephony.</span></span>



| <span data-ttu-id="cc892-281">Функция</span><span class="sxs-lookup"><span data-stu-id="cc892-281">Function</span></span>                                                             | <span data-ttu-id="cc892-282">Описание</span><span class="sxs-lookup"><span data-stu-id="cc892-282">Description</span></span>                                                                                                  |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cc892-283">**линерегистеррекуестреЦипиент**</span><span class="sxs-lookup"><span data-stu-id="cc892-283">**lineRegisterRequestRecipient**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineregisterrequestrecipient) | <span data-ttu-id="cc892-284">Регистрирует или отменяет регистрацию приложения в качестве получателя запроса для указанного режима запроса.</span><span class="sxs-lookup"><span data-stu-id="cc892-284">Registers or deregisters the application as a request recipient for the specified request mode.</span></span> <span data-ttu-id="cc892-285">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="cc892-285">Synchronous.</span></span> |
| [<span data-ttu-id="cc892-286">**линежетрекуест**</span><span class="sxs-lookup"><span data-stu-id="cc892-286">**lineGetRequest**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetrequest)                             | <span data-ttu-id="cc892-287">Получает следующий запрос из библиотеки динамической компоновки телефонии.</span><span class="sxs-lookup"><span data-stu-id="cc892-287">Gets the next request from the Telephony dynamic link library.</span></span> <span data-ttu-id="cc892-288">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="cc892-288">Synchronous.</span></span>                                  |



 

 

 



