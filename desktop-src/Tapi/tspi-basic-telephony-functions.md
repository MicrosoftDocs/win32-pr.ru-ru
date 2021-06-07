---
description: Все поставщики служб должны реализовывать базовые функции телефонии.
ms.assetid: 4250f3a0-a66a-4a6e-8566-d71be7463179
title: Базовые функции телефонии ТСПИ
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5308def0c94df9fa59f2022bf25c4dbb1843e2f8
ms.sourcegitcommit: 8ebcf6cd36f67f8bcf78e76ae8923d65b8995c8a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/05/2021
ms.locfileid: "111524158"
---
# <a name="tspi-basic-telephony-functions"></a><span data-ttu-id="72e68-103">Базовые функции телефонии ТСПИ</span><span class="sxs-lookup"><span data-stu-id="72e68-103">TSPI Basic Telephony Functions</span></span>

<span data-ttu-id="72e68-104">Все поставщики служб должны реализовывать базовые функции телефонии.</span><span class="sxs-lookup"><span data-stu-id="72e68-104">All service providers must implement Basic Telephony functions.</span></span> <span data-ttu-id="72e68-105">Ниже приведен список таких функций по категориям.</span><span class="sxs-lookup"><span data-stu-id="72e68-105">The following is a list of such functions by category.</span></span> <span data-ttu-id="72e68-106">Функция определяется как *асинхронная* , если она указывает на завершение в ответном сообщении для приложения.</span><span class="sxs-lookup"><span data-stu-id="72e68-106">A function is identified as *asynchronous* if it indicates completion in a REPLY message to the application.</span></span> <span data-ttu-id="72e68-107">Если функция всегда возвращает результат немедленно, функция считается *синхронной*.</span><span class="sxs-lookup"><span data-stu-id="72e68-107">If the function always returns its result immediately, the function is considered *synchronous*.</span></span>

-   [<span data-ttu-id="72e68-108">Адреса</span><span class="sxs-lookup"><span data-stu-id="72e68-108">Addresses</span></span>](#addresses)
-   [<span data-ttu-id="72e68-109">Ответ на входящие вызовы</span><span class="sxs-lookup"><span data-stu-id="72e68-109">Answering Incoming Calls</span></span>](#answering-incoming-calls)
-   [<span data-ttu-id="72e68-110">Вызов функций Drop</span><span class="sxs-lookup"><span data-stu-id="72e68-110">Call Drop Functions</span></span>](#call-drop-functions)
-   [<span data-ttu-id="72e68-111">Состояния вызовов и события</span><span class="sxs-lookup"><span data-stu-id="72e68-111">Call States and Events</span></span>](#call-states-and-events)
-   [<span data-ttu-id="72e68-112">Состояние и возможности линий</span><span class="sxs-lookup"><span data-stu-id="72e68-112">Line Status and Capabilities</span></span>](#line-status-and-capabilities)
-   [<span data-ttu-id="72e68-113">Согласование версии строки</span><span class="sxs-lookup"><span data-stu-id="72e68-113">Line Version Negotiation</span></span>](#line-version-negotiation)
-   [<span data-ttu-id="72e68-114">Выполнение вызовов</span><span class="sxs-lookup"><span data-stu-id="72e68-114">Making Calls</span></span>](#making-calls)
-   [<span data-ttu-id="72e68-115">Открытие и закрытие линейных устройств</span><span class="sxs-lookup"><span data-stu-id="72e68-115">Opening and Closing Line Devices</span></span>](#opening-and-closing-line-devices)
-   [<span data-ttu-id="72e68-116">Согласование версии телефона</span><span class="sxs-lookup"><span data-stu-id="72e68-116">Phone Version Negotiation</span></span>](#phone-version-negotiation)
-   [<span data-ttu-id="72e68-117">Инициализация и завершение работы TSP</span><span class="sxs-lookup"><span data-stu-id="72e68-117">TSP Initialization and Shutdown</span></span>](#tsp-initialization-and-shutdown)

## <a name="tsp-initialization-and-shutdown"></a><span data-ttu-id="72e68-118">Инициализация и завершение работы TSP</span><span class="sxs-lookup"><span data-stu-id="72e68-118">TSP Initialization and Shutdown</span></span>



|  <span data-ttu-id="72e68-119">Функция</span><span class="sxs-lookup"><span data-stu-id="72e68-119">Function</span></span>                                                         |   <span data-ttu-id="72e68-120">Описание</span><span class="sxs-lookup"><span data-stu-id="72e68-120">Description</span></span>                                                        |
|-----------------------------------------------------------|-----------------------------------------------------------|
| [<span data-ttu-id="72e68-121">**ТУИСПИ \_ провидеринсталл**</span><span class="sxs-lookup"><span data-stu-id="72e68-121">**TUISPI\_providerInstall**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_providerinstall) | <span data-ttu-id="72e68-122">Устанавливает TSP.</span><span class="sxs-lookup"><span data-stu-id="72e68-122">Installs a TSP.</span></span> <span data-ttu-id="72e68-123">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="72e68-123">Synchronous.</span></span>                              |
| [<span data-ttu-id="72e68-124">**ТСПИ \_ провидеринсталл**</span><span class="sxs-lookup"><span data-stu-id="72e68-124">**TSPI\_providerInstall**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_providerinstall)     | <span data-ttu-id="72e68-125">Устанавливает TSP.</span><span class="sxs-lookup"><span data-stu-id="72e68-125">Installs the TSP.</span></span> <span data-ttu-id="72e68-126">Устарело с версией 2,0.</span><span class="sxs-lookup"><span data-stu-id="72e68-126">Obsolete with Version 2.0.</span></span> <span data-ttu-id="72e68-127">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="72e68-127">Synchronous.</span></span> |
| [<span data-ttu-id="72e68-128">**ТСПИ \_ провидеринит**</span><span class="sxs-lookup"><span data-stu-id="72e68-128">**TSPI\_providerInit**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_providerinit)           | <span data-ttu-id="72e68-129">Инициализирует TSP.</span><span class="sxs-lookup"><span data-stu-id="72e68-129">Initializes the TSP.</span></span> <span data-ttu-id="72e68-130">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="72e68-130">Synchronous.</span></span>                         |
| [<span data-ttu-id="72e68-131">**ТСПИ \_ провидершутдовн**</span><span class="sxs-lookup"><span data-stu-id="72e68-131">**TSPI\_providerShutdown**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_providershutdown)   | <span data-ttu-id="72e68-132">Завершает работу поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="72e68-132">Shuts down the service provider.</span></span>                          |
| [<span data-ttu-id="72e68-133">**ТУИСПИ \_ провидерремове**</span><span class="sxs-lookup"><span data-stu-id="72e68-133">**TUISPI\_providerRemove**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_providerremove)   | <span data-ttu-id="72e68-134">Удаляет TSP.</span><span class="sxs-lookup"><span data-stu-id="72e68-134">Removes a TSP.</span></span> <span data-ttu-id="72e68-135">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="72e68-135">Synchronous.</span></span>                               |
| [<span data-ttu-id="72e68-136">**ТСПИ \_ провидерремове**</span><span class="sxs-lookup"><span data-stu-id="72e68-136">**TSPI\_providerRemove**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_providerremove)       | <span data-ttu-id="72e68-137">Удаляет TSP.</span><span class="sxs-lookup"><span data-stu-id="72e68-137">Removes a TSP.</span></span> <span data-ttu-id="72e68-138">Устарело с версией 2,0.</span><span class="sxs-lookup"><span data-stu-id="72e68-138">Obsolete with Version 2.0.</span></span> <span data-ttu-id="72e68-139">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="72e68-139">Synchronous.</span></span>    |



 

## <a name="phone-version-negotiation"></a><span data-ttu-id="72e68-140">Согласование версии телефона</span><span class="sxs-lookup"><span data-stu-id="72e68-140">Phone Version Negotiation</span></span>



|  <span data-ttu-id="72e68-141">Функция</span><span class="sxs-lookup"><span data-stu-id="72e68-141">Function</span></span>                                                         |   <span data-ttu-id="72e68-142">Описание</span><span class="sxs-lookup"><span data-stu-id="72e68-142">Description</span></span>                                                        |
|---------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="72e68-143">**ТСПИ \_ фоненеготиатетспиверсион**</span><span class="sxs-lookup"><span data-stu-id="72e68-143">**TSPI\_phoneNegotiateTSPIVersion**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_phonenegotiatetspiversion) | <span data-ttu-id="72e68-144">Возвращает максимальную версию SPI, для которой может действовать поставщик служб для этого устройства.</span><span class="sxs-lookup"><span data-stu-id="72e68-144">Returns the highest SPI version the service provider can operate under for this device.</span></span> |



 

## <a name="line-version-negotiation"></a><span data-ttu-id="72e68-145">Согласование версии строки</span><span class="sxs-lookup"><span data-stu-id="72e68-145">Line Version Negotiation</span></span>



|  <span data-ttu-id="72e68-146">Функция</span><span class="sxs-lookup"><span data-stu-id="72e68-146">Function</span></span>                                                         |   <span data-ttu-id="72e68-147">Описание</span><span class="sxs-lookup"><span data-stu-id="72e68-147">Description</span></span>                                                        |
|-------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="72e68-148">**ТСПИ \_ линенеготиатетспиверсион**</span><span class="sxs-lookup"><span data-stu-id="72e68-148">**TSPI\_lineNegotiateTSPIVersion**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linenegotiatetspiversion) | <span data-ttu-id="72e68-149">Позволяет приложению согласовывать версию ТСПИ для использования с заданным устройством.</span><span class="sxs-lookup"><span data-stu-id="72e68-149">Allows an application to negotiate a TSPI version to use with a given line device.</span></span> <span data-ttu-id="72e68-150">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="72e68-150">Synchronous.</span></span> |



 

## <a name="line-status-and-capabilities"></a><span data-ttu-id="72e68-151">Состояние и возможности линий</span><span class="sxs-lookup"><span data-stu-id="72e68-151">Line Status and Capabilities</span></span>



|  <span data-ttu-id="72e68-152">Функция</span><span class="sxs-lookup"><span data-stu-id="72e68-152">Function</span></span>                                                         |   <span data-ttu-id="72e68-153">Описание</span><span class="sxs-lookup"><span data-stu-id="72e68-153">Description</span></span>                                                        |
|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="72e68-154">**ТСПИ \_ линежетдевкапс**</span><span class="sxs-lookup"><span data-stu-id="72e68-154">**TSPI\_lineGetDevCaps**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetdevcaps)                 | <span data-ttu-id="72e68-155">Возвращает возможности данного устройства линии.</span><span class="sxs-lookup"><span data-stu-id="72e68-155">Returns the capabilities of a given line device.</span></span> <span data-ttu-id="72e68-156">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="72e68-156">Synchronous.</span></span>                                                                                                  |
| [<span data-ttu-id="72e68-157">**ТСПИ \_ линежетдевконфиг**</span><span class="sxs-lookup"><span data-stu-id="72e68-157">**TSPI\_lineGetDevConfig**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetdevconfig)             | <span data-ttu-id="72e68-158">Возвращает конфигурацию устройства потоковой передачи мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="72e68-158">Returns configuration of a media stream device.</span></span> <span data-ttu-id="72e68-159">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="72e68-159">Synchronous.</span></span>                                                                                                   |
| [<span data-ttu-id="72e68-160">**ТСПИ \_ линежетлинедевстатус**</span><span class="sxs-lookup"><span data-stu-id="72e68-160">**TSPI\_lineGetLineDevStatus**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetlinedevstatus)     | <span data-ttu-id="72e68-161">Возвращает текущее состояние указанного устройства с открытым графиком.</span><span class="sxs-lookup"><span data-stu-id="72e68-161">Returns current status of the specified open line device.</span></span> <span data-ttu-id="72e68-162">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="72e68-162">Synchronous.</span></span>                                                                                         |
| [<span data-ttu-id="72e68-163">**ТСПИ \_ линесетдевконфиг**</span><span class="sxs-lookup"><span data-stu-id="72e68-163">**TSPI\_lineSetDevConfig**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetdevconfig)             | <span data-ttu-id="72e68-164">Задает конфигурацию указанного устройства потока мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="72e68-164">Sets the configuration of the specified media stream device.</span></span> <span data-ttu-id="72e68-165">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="72e68-165">Synchronous.</span></span>                                                                                      |
| [<span data-ttu-id="72e68-166">**ТСПИ \_ линесетстатусмессажес**</span><span class="sxs-lookup"><span data-stu-id="72e68-166">**TSPI\_lineSetStatusMessages**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetstatusmessages)   | <span data-ttu-id="72e68-167">Указывает изменения состояния, для которых приложение должно получать уведомления.</span><span class="sxs-lookup"><span data-stu-id="72e68-167">Specifies the status changes for which the application needs to be notified.</span></span> <span data-ttu-id="72e68-168">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="72e68-168">Synchronous.</span></span>                                                                      |
| [<span data-ttu-id="72e68-169">**ТСПИ \_ линежетид**</span><span class="sxs-lookup"><span data-stu-id="72e68-169">**TSPI\_lineGetID**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetid)                           | <span data-ttu-id="72e68-170">Извлекает идентификатор устройства, связанный с указанной открытой строкой, адресом или вызовом.</span><span class="sxs-lookup"><span data-stu-id="72e68-170">Retrieves a device ID associated with the specified open line, address, or call.</span></span> <span data-ttu-id="72e68-171">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="72e68-171">Synchronous.</span></span>                                                                  |
| [<span data-ttu-id="72e68-172">**ТСПИ \_ линежетикон**</span><span class="sxs-lookup"><span data-stu-id="72e68-172">**TSPI\_lineGetIcon**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegeticon)                       | <span data-ttu-id="72e68-173">Позволяет приложению получить значок для показа пользователю.</span><span class="sxs-lookup"><span data-stu-id="72e68-173">Allows an application to retrieve an icon for display to the user.</span></span> <span data-ttu-id="72e68-174">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="72e68-174">Synchronous.</span></span>                                                                                |
| [<span data-ttu-id="72e68-175">**ТУИСПИ \_ линеконфигдиалог**</span><span class="sxs-lookup"><span data-stu-id="72e68-175">**TUISPI\_lineConfigDialog**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_lineconfigdialog)         | <span data-ttu-id="72e68-176">Заставляет поставщик указанного устройства отображать диалоговое окно, позволяющее пользователю настраивать параметры, связанные с устройством линии.</span><span class="sxs-lookup"><span data-stu-id="72e68-176">Causes the provider of the specified line device to display a dialog box that allows the user to configure parameters related to the line device.</span></span> <span data-ttu-id="72e68-177">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="72e68-177">Synchronous.</span></span> |
| [<span data-ttu-id="72e68-178">**ТУИСПИ \_ линеконфигдиаложедит**</span><span class="sxs-lookup"><span data-stu-id="72e68-178">**TUISPI\_lineConfigDialogEdit**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_lineconfigdialogedit) | <span data-ttu-id="72e68-179">Отображает диалоговое окно, позволяющее пользователю изменить сведения о конфигурации для линейного устройства.</span><span class="sxs-lookup"><span data-stu-id="72e68-179">Displays a dialog box allowing the user to change configuration information for a line device.</span></span> <span data-ttu-id="72e68-180">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="72e68-180">Synchronous.</span></span>                                                    |



 

## <a name="addresses"></a><span data-ttu-id="72e68-181">Адреса</span><span class="sxs-lookup"><span data-stu-id="72e68-181">Addresses</span></span>



|  <span data-ttu-id="72e68-182">Функция</span><span class="sxs-lookup"><span data-stu-id="72e68-182">Function</span></span>                                                         |   <span data-ttu-id="72e68-183">Описание</span><span class="sxs-lookup"><span data-stu-id="72e68-183">Description</span></span>                                                        |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [<span data-ttu-id="72e68-184">**ТСПИ \_ линежетаддресскапс**</span><span class="sxs-lookup"><span data-stu-id="72e68-184">**TSPI\_lineGetAddressCaps**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddresscaps)     | <span data-ttu-id="72e68-185">Возвращает возможности телефонии адреса.</span><span class="sxs-lookup"><span data-stu-id="72e68-185">Returns the telephony capabilities of an address.</span></span> <span data-ttu-id="72e68-186">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="72e68-186">Synchronous.</span></span>                           |
| [<span data-ttu-id="72e68-187">**ТСПИ \_ линежетаддрессстатус**</span><span class="sxs-lookup"><span data-stu-id="72e68-187">**TSPI\_lineGetAddressStatus**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddressstatus) | <span data-ttu-id="72e68-188">Возвращает текущее состояние указанного адреса.</span><span class="sxs-lookup"><span data-stu-id="72e68-188">Returns current status of a specified address.</span></span> <span data-ttu-id="72e68-189">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="72e68-189">Synchronous.</span></span>                              |
| [<span data-ttu-id="72e68-190">**ТСПИ \_ линежетнумаддрессидс**</span><span class="sxs-lookup"><span data-stu-id="72e68-190">**TSPI\_lineGetNumAddressIDs**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetnumaddressids) | <span data-ttu-id="72e68-191">Извлекает количество идентификаторов адресов, поддерживаемое в указанной строке.</span><span class="sxs-lookup"><span data-stu-id="72e68-191">Retrieves the number of address identifiers supported on the indicated line.</span></span>             |
| [<span data-ttu-id="72e68-192">**ТСПИ \_ линежетаддрессид**</span><span class="sxs-lookup"><span data-stu-id="72e68-192">**TSPI\_lineGetAddressID**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddressid)         | <span data-ttu-id="72e68-193">Извлекает идентификатор адреса, указанного в альтернативном формате.</span><span class="sxs-lookup"><span data-stu-id="72e68-193">Retrieves the address ID of an address specified using an alternate format.</span></span> <span data-ttu-id="72e68-194">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="72e68-194">Synchronous.</span></span> |



 

## <a name="opening-and-closing-line-devices"></a><span data-ttu-id="72e68-195">Открытие и закрытие линейных устройств</span><span class="sxs-lookup"><span data-stu-id="72e68-195">Opening and Closing Line Devices</span></span>



|  <span data-ttu-id="72e68-196">Функция</span><span class="sxs-lookup"><span data-stu-id="72e68-196">Function</span></span>                                                         |   <span data-ttu-id="72e68-197">Описание</span><span class="sxs-lookup"><span data-stu-id="72e68-197">Description</span></span>                                                        |
|-------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="72e68-198">**ТСПИ \_ линеопен**</span><span class="sxs-lookup"><span data-stu-id="72e68-198">**TSPI\_lineOpen**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineopen)   | <span data-ttu-id="72e68-199">Открывает указанное устройство линии для последующего мониторинга и (или) управления строкой.</span><span class="sxs-lookup"><span data-stu-id="72e68-199">Opens a specified line device for providing subsequent monitoring and/or control of the line.</span></span> <span data-ttu-id="72e68-200">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="72e68-200">Synchronous.</span></span> |
| [<span data-ttu-id="72e68-201">**ТСПИ \_ линеклосе**</span><span class="sxs-lookup"><span data-stu-id="72e68-201">**TSPI\_lineClose**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineclose) | <span data-ttu-id="72e68-202">Закрывает указанное устройство Open Line.</span><span class="sxs-lookup"><span data-stu-id="72e68-202">Closes a specified opened line device.</span></span> <span data-ttu-id="72e68-203">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="72e68-203">Synchronous.</span></span>                                                        |



 

## <a name="call-states-and-events"></a><span data-ttu-id="72e68-204">Состояния вызовов и события</span><span class="sxs-lookup"><span data-stu-id="72e68-204">Call States and Events</span></span>



|  <span data-ttu-id="72e68-205">Функция</span><span class="sxs-lookup"><span data-stu-id="72e68-205">Function</span></span>                                                         |   <span data-ttu-id="72e68-206">Описание</span><span class="sxs-lookup"><span data-stu-id="72e68-206">Description</span></span>                                                        |
|-------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="72e68-207">**ТСПИ \_ линежеткаллинфо**</span><span class="sxs-lookup"><span data-stu-id="72e68-207">**TSPI\_lineGetCallInfo**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetcallinfo)       | <span data-ttu-id="72e68-208">Возвращает фиксированные сведения о вызове.</span><span class="sxs-lookup"><span data-stu-id="72e68-208">Returns fixed information about a call.</span></span> <span data-ttu-id="72e68-209">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="72e68-209">Synchronous.</span></span>                                |
| [<span data-ttu-id="72e68-210">**ТСПИ \_ линежеткаллстатус**</span><span class="sxs-lookup"><span data-stu-id="72e68-210">**TSPI\_lineGetCallStatus**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetcallstatus)   | <span data-ttu-id="72e68-211">Возвращает сведения о состоянии завершения вызова для указанного вызова.</span><span class="sxs-lookup"><span data-stu-id="72e68-211">Returns complete call status information for the specified call.</span></span> <span data-ttu-id="72e68-212">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="72e68-212">Synchronous.</span></span>       |
| [<span data-ttu-id="72e68-213">**ТСПИ \_ линесетаппспеЦифик**</span><span class="sxs-lookup"><span data-stu-id="72e68-213">**TSPI\_lineSetAppSpecific**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetappspecific) | <span data-ttu-id="72e68-214">Задает зависящее от приложения поле структуры сведений о вызове.</span><span class="sxs-lookup"><span data-stu-id="72e68-214">Sets the application-specific field of a call's information structure.</span></span> <span data-ttu-id="72e68-215">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="72e68-215">Synchronous.</span></span> |



 

## <a name="making-calls"></a><span data-ttu-id="72e68-216">Выполнение вызовов</span><span class="sxs-lookup"><span data-stu-id="72e68-216">Making Calls</span></span>



|  <span data-ttu-id="72e68-217">Функция</span><span class="sxs-lookup"><span data-stu-id="72e68-217">Function</span></span>                                                         |   <span data-ttu-id="72e68-218">Описание</span><span class="sxs-lookup"><span data-stu-id="72e68-218">Description</span></span>                                                        |
|-------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="72e68-219">**ТСПИ \_ линемакекалл**</span><span class="sxs-lookup"><span data-stu-id="72e68-219">**TSPI\_lineMakeCall**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall) | <span data-ttu-id="72e68-220">Выполняет исходящий вызов и возвращает для него маркер вызова.</span><span class="sxs-lookup"><span data-stu-id="72e68-220">Makes an outbound call and returns a call handle for it.</span></span> <span data-ttu-id="72e68-221">Асинхронная.</span><span class="sxs-lookup"><span data-stu-id="72e68-221">Asynchronous.</span></span> |
| [<span data-ttu-id="72e68-222">**ТСПИ \_ линедиал**</span><span class="sxs-lookup"><span data-stu-id="72e68-222">**TSPI\_lineDial**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linedial)         | <span data-ttu-id="72e68-223">Звонки (части одного или нескольких) коммутируемых адресов.</span><span class="sxs-lookup"><span data-stu-id="72e68-223">Dials (parts of one or more) dialable addresses.</span></span> <span data-ttu-id="72e68-224">Асинхронная.</span><span class="sxs-lookup"><span data-stu-id="72e68-224">Asynchronous.</span></span>         |



 

## <a name="answering-incoming-calls"></a><span data-ttu-id="72e68-225">Ответ на входящие вызовы</span><span class="sxs-lookup"><span data-stu-id="72e68-225">Answering Incoming Calls</span></span>



|  <span data-ttu-id="72e68-226">Функция</span><span class="sxs-lookup"><span data-stu-id="72e68-226">Function</span></span>                                                         |   <span data-ttu-id="72e68-227">Описание</span><span class="sxs-lookup"><span data-stu-id="72e68-227">Description</span></span>                                                        |
|---------------------------------------------|-----------------------------------------|
| [<span data-ttu-id="72e68-228">**ТСПИ \_ линеансвер**</span><span class="sxs-lookup"><span data-stu-id="72e68-228">**TSPI\_lineAnswer**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineanswer) | <span data-ttu-id="72e68-229">Отвечает на входящий вызов.</span><span class="sxs-lookup"><span data-stu-id="72e68-229">Answers an incoming call.</span></span> <span data-ttu-id="72e68-230">Асинхронная.</span><span class="sxs-lookup"><span data-stu-id="72e68-230">Asynchronous.</span></span> |



 

## <a name="call-drop-functions"></a><span data-ttu-id="72e68-231">Вызов функций Drop</span><span class="sxs-lookup"><span data-stu-id="72e68-231">Call Drop Functions</span></span>



|  <span data-ttu-id="72e68-232">Функция</span><span class="sxs-lookup"><span data-stu-id="72e68-232">Function</span></span>                                                         |   <span data-ttu-id="72e68-233">Описание</span><span class="sxs-lookup"><span data-stu-id="72e68-233">Description</span></span>                                                        |
|-----------------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="72e68-234">**ТСПИ \_ линедроп**</span><span class="sxs-lookup"><span data-stu-id="72e68-234">**TSPI\_lineDrop**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linedrop) | <span data-ttu-id="72e68-235">Отключает вызов или прерывает выполнение попытки вызова.</span><span class="sxs-lookup"><span data-stu-id="72e68-235">Disconnects a call, or abandons a call attempt in progress.</span></span> <span data-ttu-id="72e68-236">Асинхронная.</span><span class="sxs-lookup"><span data-stu-id="72e68-236">Asynchronous.</span></span> |



 

 

 
