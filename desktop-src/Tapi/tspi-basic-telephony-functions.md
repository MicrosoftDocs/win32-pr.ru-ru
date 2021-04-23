---
description: Все поставщики служб должны реализовывать базовые функции телефонии.
ms.assetid: 4250f3a0-a66a-4a6e-8566-d71be7463179
title: Базовые функции телефонии ТСПИ
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6276be51482620af32650ad1625eea97bddb8e5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913216"
---
# <a name="tspi-basic-telephony-functions"></a><span data-ttu-id="a44d9-103">Базовые функции телефонии ТСПИ</span><span class="sxs-lookup"><span data-stu-id="a44d9-103">TSPI Basic Telephony Functions</span></span>

<span data-ttu-id="a44d9-104">Все поставщики служб должны реализовывать базовые функции телефонии.</span><span class="sxs-lookup"><span data-stu-id="a44d9-104">All service providers must implement Basic Telephony functions.</span></span> <span data-ttu-id="a44d9-105">Ниже приведен список таких функций по категориям.</span><span class="sxs-lookup"><span data-stu-id="a44d9-105">The following is a list of such functions by category.</span></span> <span data-ttu-id="a44d9-106">Функция определяется как *асинхронная* , если она указывает на завершение в ответном сообщении для приложения.</span><span class="sxs-lookup"><span data-stu-id="a44d9-106">A function is identified as *asynchronous* if it indicates completion in a REPLY message to the application.</span></span> <span data-ttu-id="a44d9-107">Если функция всегда возвращает результат немедленно, функция считается *синхронной*.</span><span class="sxs-lookup"><span data-stu-id="a44d9-107">If the function always returns its result immediately, the function is considered *synchronous*.</span></span>

-   [<span data-ttu-id="a44d9-108">Адреса</span><span class="sxs-lookup"><span data-stu-id="a44d9-108">Addresses</span></span>](#addresses)
-   [<span data-ttu-id="a44d9-109">Ответ на входящие вызовы</span><span class="sxs-lookup"><span data-stu-id="a44d9-109">Answering Incoming Calls</span></span>](#answering-incoming-calls)
-   [<span data-ttu-id="a44d9-110">Вызов функций Drop</span><span class="sxs-lookup"><span data-stu-id="a44d9-110">Call Drop Functions</span></span>](#call-drop-functions)
-   [<span data-ttu-id="a44d9-111">Состояния вызовов и события</span><span class="sxs-lookup"><span data-stu-id="a44d9-111">Call States and Events</span></span>](#call-states-and-events)
-   [<span data-ttu-id="a44d9-112">Состояние и возможности линий</span><span class="sxs-lookup"><span data-stu-id="a44d9-112">Line Status and Capabilities</span></span>](#line-status-and-capabilities)
-   [<span data-ttu-id="a44d9-113">Согласование версии строки</span><span class="sxs-lookup"><span data-stu-id="a44d9-113">Line Version Negotiation</span></span>](#line-version-negotiation)
-   [<span data-ttu-id="a44d9-114">Выполнение вызовов</span><span class="sxs-lookup"><span data-stu-id="a44d9-114">Making Calls</span></span>](#making-calls)
-   [<span data-ttu-id="a44d9-115">Открытие и закрытие линейных устройств</span><span class="sxs-lookup"><span data-stu-id="a44d9-115">Opening and Closing Line Devices</span></span>](#opening-and-closing-line-devices)
-   [<span data-ttu-id="a44d9-116">Согласование версии телефона</span><span class="sxs-lookup"><span data-stu-id="a44d9-116">Phone Version Negotiation</span></span>](#phone-version-negotiation)
-   [<span data-ttu-id="a44d9-117">Инициализация и завершение работы TSP</span><span class="sxs-lookup"><span data-stu-id="a44d9-117">TSP Initialization and Shutdown</span></span>](#tsp-initialization-and-shutdown)

## <a name="tsp-initialization-and-shutdown"></a><span data-ttu-id="a44d9-118">Инициализация и завершение работы TSP</span><span class="sxs-lookup"><span data-stu-id="a44d9-118">TSP Initialization and Shutdown</span></span>



|                                                           |                                                           |
|-----------------------------------------------------------|-----------------------------------------------------------|
| [<span data-ttu-id="a44d9-119">**ТУИСПИ \_ провидеринсталл**</span><span class="sxs-lookup"><span data-stu-id="a44d9-119">**TUISPI\_providerInstall**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_providerinstall) | <span data-ttu-id="a44d9-120">Устанавливает TSP.</span><span class="sxs-lookup"><span data-stu-id="a44d9-120">Installs a TSP.</span></span> <span data-ttu-id="a44d9-121">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="a44d9-121">Synchronous.</span></span>                              |
| [<span data-ttu-id="a44d9-122">**ТСПИ \_ провидеринсталл**</span><span class="sxs-lookup"><span data-stu-id="a44d9-122">**TSPI\_providerInstall**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_providerinstall)     | <span data-ttu-id="a44d9-123">Устанавливает TSP.</span><span class="sxs-lookup"><span data-stu-id="a44d9-123">Installs the TSP.</span></span> <span data-ttu-id="a44d9-124">Устарело с версией 2,0.</span><span class="sxs-lookup"><span data-stu-id="a44d9-124">Obsolete with Version 2.0.</span></span> <span data-ttu-id="a44d9-125">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="a44d9-125">Synchronous.</span></span> |
| [<span data-ttu-id="a44d9-126">**ТСПИ \_ провидеринит**</span><span class="sxs-lookup"><span data-stu-id="a44d9-126">**TSPI\_providerInit**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_providerinit)           | <span data-ttu-id="a44d9-127">Инициализирует TSP.</span><span class="sxs-lookup"><span data-stu-id="a44d9-127">Initializes the TSP.</span></span> <span data-ttu-id="a44d9-128">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="a44d9-128">Synchronous.</span></span>                         |
| [<span data-ttu-id="a44d9-129">**ТСПИ \_ провидершутдовн**</span><span class="sxs-lookup"><span data-stu-id="a44d9-129">**TSPI\_providerShutdown**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_providershutdown)   | <span data-ttu-id="a44d9-130">Завершает работу поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="a44d9-130">Shuts down the service provider.</span></span>                          |
| [<span data-ttu-id="a44d9-131">**ТУИСПИ \_ провидерремове**</span><span class="sxs-lookup"><span data-stu-id="a44d9-131">**TUISPI\_providerRemove**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_providerremove)   | <span data-ttu-id="a44d9-132">Удаляет TSP.</span><span class="sxs-lookup"><span data-stu-id="a44d9-132">Removes a TSP.</span></span> <span data-ttu-id="a44d9-133">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="a44d9-133">Synchronous.</span></span>                               |
| [<span data-ttu-id="a44d9-134">**ТСПИ \_ провидерремове**</span><span class="sxs-lookup"><span data-stu-id="a44d9-134">**TSPI\_providerRemove**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_providerremove)       | <span data-ttu-id="a44d9-135">Удаляет TSP.</span><span class="sxs-lookup"><span data-stu-id="a44d9-135">Removes a TSP.</span></span> <span data-ttu-id="a44d9-136">Устарело с версией 2,0.</span><span class="sxs-lookup"><span data-stu-id="a44d9-136">Obsolete with Version 2.0.</span></span> <span data-ttu-id="a44d9-137">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="a44d9-137">Synchronous.</span></span>    |



 

## <a name="phone-version-negotiation"></a><span data-ttu-id="a44d9-138">Согласование версии телефона</span><span class="sxs-lookup"><span data-stu-id="a44d9-138">Phone Version Negotiation</span></span>



|                                                                           |                                                                                         |
|---------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="a44d9-139">**ТСПИ \_ фоненеготиатетспиверсион**</span><span class="sxs-lookup"><span data-stu-id="a44d9-139">**TSPI\_phoneNegotiateTSPIVersion**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_phonenegotiatetspiversion) | <span data-ttu-id="a44d9-140">Возвращает максимальную версию SPI, для которой может действовать поставщик служб для этого устройства.</span><span class="sxs-lookup"><span data-stu-id="a44d9-140">Returns the highest SPI version the service provider can operate under for this device.</span></span> |



 

## <a name="line-version-negotiation"></a><span data-ttu-id="a44d9-141">Согласование версии строки</span><span class="sxs-lookup"><span data-stu-id="a44d9-141">Line Version Negotiation</span></span>



|                                                                         |                                                                                                 |
|-------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a44d9-142">**ТСПИ \_ линенеготиатетспиверсион**</span><span class="sxs-lookup"><span data-stu-id="a44d9-142">**TSPI\_lineNegotiateTSPIVersion**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linenegotiatetspiversion) | <span data-ttu-id="a44d9-143">Позволяет приложению согласовывать версию ТСПИ для использования с заданным устройством.</span><span class="sxs-lookup"><span data-stu-id="a44d9-143">Allows an application to negotiate a TSPI version to use with a given line device.</span></span> <span data-ttu-id="a44d9-144">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="a44d9-144">Synchronous.</span></span> |



 

## <a name="line-status-and-capabilities"></a><span data-ttu-id="a44d9-145">Состояние и возможности линий</span><span class="sxs-lookup"><span data-stu-id="a44d9-145">Line Status and Capabilities</span></span>



|                                                                     |                                                                                                                                                                |
|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a44d9-146">**ТСПИ \_ линежетдевкапс**</span><span class="sxs-lookup"><span data-stu-id="a44d9-146">**TSPI\_lineGetDevCaps**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetdevcaps)                 | <span data-ttu-id="a44d9-147">Возвращает возможности данного устройства линии.</span><span class="sxs-lookup"><span data-stu-id="a44d9-147">Returns the capabilities of a given line device.</span></span> <span data-ttu-id="a44d9-148">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="a44d9-148">Synchronous.</span></span>                                                                                                  |
| [<span data-ttu-id="a44d9-149">**ТСПИ \_ линежетдевконфиг**</span><span class="sxs-lookup"><span data-stu-id="a44d9-149">**TSPI\_lineGetDevConfig**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetdevconfig)             | <span data-ttu-id="a44d9-150">Возвращает конфигурацию устройства потоковой передачи мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="a44d9-150">Returns configuration of a media stream device.</span></span> <span data-ttu-id="a44d9-151">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="a44d9-151">Synchronous.</span></span>                                                                                                   |
| [<span data-ttu-id="a44d9-152">**ТСПИ \_ линежетлинедевстатус**</span><span class="sxs-lookup"><span data-stu-id="a44d9-152">**TSPI\_lineGetLineDevStatus**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetlinedevstatus)     | <span data-ttu-id="a44d9-153">Возвращает текущее состояние указанного устройства с открытым графиком.</span><span class="sxs-lookup"><span data-stu-id="a44d9-153">Returns current status of the specified open line device.</span></span> <span data-ttu-id="a44d9-154">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="a44d9-154">Synchronous.</span></span>                                                                                         |
| [<span data-ttu-id="a44d9-155">**ТСПИ \_ линесетдевконфиг**</span><span class="sxs-lookup"><span data-stu-id="a44d9-155">**TSPI\_lineSetDevConfig**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetdevconfig)             | <span data-ttu-id="a44d9-156">Задает конфигурацию указанного устройства потока мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="a44d9-156">Sets the configuration of the specified media stream device.</span></span> <span data-ttu-id="a44d9-157">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="a44d9-157">Synchronous.</span></span>                                                                                      |
| [<span data-ttu-id="a44d9-158">**ТСПИ \_ линесетстатусмессажес**</span><span class="sxs-lookup"><span data-stu-id="a44d9-158">**TSPI\_lineSetStatusMessages**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetstatusmessages)   | <span data-ttu-id="a44d9-159">Указывает изменения состояния, для которых приложение должно получать уведомления.</span><span class="sxs-lookup"><span data-stu-id="a44d9-159">Specifies the status changes for which the application needs to be notified.</span></span> <span data-ttu-id="a44d9-160">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="a44d9-160">Synchronous.</span></span>                                                                      |
| [<span data-ttu-id="a44d9-161">**ТСПИ \_ линежетид**</span><span class="sxs-lookup"><span data-stu-id="a44d9-161">**TSPI\_lineGetID**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetid)                           | <span data-ttu-id="a44d9-162">Извлекает идентификатор устройства, связанный с указанной открытой строкой, адресом или вызовом.</span><span class="sxs-lookup"><span data-stu-id="a44d9-162">Retrieves a device ID associated with the specified open line, address, or call.</span></span> <span data-ttu-id="a44d9-163">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="a44d9-163">Synchronous.</span></span>                                                                  |
| [<span data-ttu-id="a44d9-164">**ТСПИ \_ линежетикон**</span><span class="sxs-lookup"><span data-stu-id="a44d9-164">**TSPI\_lineGetIcon**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegeticon)                       | <span data-ttu-id="a44d9-165">Позволяет приложению получить значок для показа пользователю.</span><span class="sxs-lookup"><span data-stu-id="a44d9-165">Allows an application to retrieve an icon for display to the user.</span></span> <span data-ttu-id="a44d9-166">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="a44d9-166">Synchronous.</span></span>                                                                                |
| [<span data-ttu-id="a44d9-167">**ТУИСПИ \_ линеконфигдиалог**</span><span class="sxs-lookup"><span data-stu-id="a44d9-167">**TUISPI\_lineConfigDialog**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_lineconfigdialog)         | <span data-ttu-id="a44d9-168">Заставляет поставщик указанного устройства отображать диалоговое окно, позволяющее пользователю настраивать параметры, связанные с устройством линии.</span><span class="sxs-lookup"><span data-stu-id="a44d9-168">Causes the provider of the specified line device to display a dialog box that allows the user to configure parameters related to the line device.</span></span> <span data-ttu-id="a44d9-169">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="a44d9-169">Synchronous.</span></span> |
| [<span data-ttu-id="a44d9-170">**ТУИСПИ \_ линеконфигдиаложедит**</span><span class="sxs-lookup"><span data-stu-id="a44d9-170">**TUISPI\_lineConfigDialogEdit**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_lineconfigdialogedit) | <span data-ttu-id="a44d9-171">Отображает диалоговое окно, позволяющее пользователю изменить сведения о конфигурации для линейного устройства.</span><span class="sxs-lookup"><span data-stu-id="a44d9-171">Displays a dialog box allowing the user to change configuration information for a line device.</span></span> <span data-ttu-id="a44d9-172">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="a44d9-172">Synchronous.</span></span>                                                    |



 

## <a name="addresses"></a><span data-ttu-id="a44d9-173">Адреса</span><span class="sxs-lookup"><span data-stu-id="a44d9-173">Addresses</span></span>



|                                                                 |                                                                                          |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a44d9-174">**ТСПИ \_ линежетаддресскапс**</span><span class="sxs-lookup"><span data-stu-id="a44d9-174">**TSPI\_lineGetAddressCaps**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddresscaps)     | <span data-ttu-id="a44d9-175">Возвращает возможности телефонии адреса.</span><span class="sxs-lookup"><span data-stu-id="a44d9-175">Returns the telephony capabilities of an address.</span></span> <span data-ttu-id="a44d9-176">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="a44d9-176">Synchronous.</span></span>                           |
| [<span data-ttu-id="a44d9-177">**ТСПИ \_ линежетаддрессстатус**</span><span class="sxs-lookup"><span data-stu-id="a44d9-177">**TSPI\_lineGetAddressStatus**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddressstatus) | <span data-ttu-id="a44d9-178">Возвращает текущее состояние указанного адреса.</span><span class="sxs-lookup"><span data-stu-id="a44d9-178">Returns current status of a specified address.</span></span> <span data-ttu-id="a44d9-179">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="a44d9-179">Synchronous.</span></span>                              |
| [<span data-ttu-id="a44d9-180">**ТСПИ \_ линежетнумаддрессидс**</span><span class="sxs-lookup"><span data-stu-id="a44d9-180">**TSPI\_lineGetNumAddressIDs**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetnumaddressids) | <span data-ttu-id="a44d9-181">Извлекает количество идентификаторов адресов, поддерживаемое в указанной строке.</span><span class="sxs-lookup"><span data-stu-id="a44d9-181">Retrieves the number of address identifiers supported on the indicated line.</span></span>             |
| [<span data-ttu-id="a44d9-182">**ТСПИ \_ линежетаддрессид**</span><span class="sxs-lookup"><span data-stu-id="a44d9-182">**TSPI\_lineGetAddressID**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddressid)         | <span data-ttu-id="a44d9-183">Извлекает идентификатор адреса, указанного в альтернативном формате.</span><span class="sxs-lookup"><span data-stu-id="a44d9-183">Retrieves the address ID of an address specified using an alternate format.</span></span> <span data-ttu-id="a44d9-184">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="a44d9-184">Synchronous.</span></span> |



 

## <a name="opening-and-closing-line-devices"></a><span data-ttu-id="a44d9-185">Открытие и закрытие линейных устройств</span><span class="sxs-lookup"><span data-stu-id="a44d9-185">Opening and Closing Line Devices</span></span>



|                                           |                                                                                                            |
|-------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a44d9-186">**ТСПИ \_ линеопен**</span><span class="sxs-lookup"><span data-stu-id="a44d9-186">**TSPI\_lineOpen**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineopen)   | <span data-ttu-id="a44d9-187">Открывает указанное устройство линии для последующего мониторинга и (или) управления строкой.</span><span class="sxs-lookup"><span data-stu-id="a44d9-187">Opens a specified line device for providing subsequent monitoring and/or control of the line.</span></span> <span data-ttu-id="a44d9-188">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="a44d9-188">Synchronous.</span></span> |
| [<span data-ttu-id="a44d9-189">**ТСПИ \_ линеклосе**</span><span class="sxs-lookup"><span data-stu-id="a44d9-189">**TSPI\_lineClose**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineclose) | <span data-ttu-id="a44d9-190">Закрывает указанное устройство Open Line.</span><span class="sxs-lookup"><span data-stu-id="a44d9-190">Closes a specified opened line device.</span></span> <span data-ttu-id="a44d9-191">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="a44d9-191">Synchronous.</span></span>                                                        |



 

## <a name="call-states-and-events"></a><span data-ttu-id="a44d9-192">Состояния вызовов и события</span><span class="sxs-lookup"><span data-stu-id="a44d9-192">Call States and Events</span></span>



|                                                             |                                                                                     |
|-------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="a44d9-193">**ТСПИ \_ линежеткаллинфо**</span><span class="sxs-lookup"><span data-stu-id="a44d9-193">**TSPI\_lineGetCallInfo**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetcallinfo)       | <span data-ttu-id="a44d9-194">Возвращает фиксированные сведения о вызове.</span><span class="sxs-lookup"><span data-stu-id="a44d9-194">Returns fixed information about a call.</span></span> <span data-ttu-id="a44d9-195">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="a44d9-195">Synchronous.</span></span>                                |
| [<span data-ttu-id="a44d9-196">**ТСПИ \_ линежеткаллстатус**</span><span class="sxs-lookup"><span data-stu-id="a44d9-196">**TSPI\_lineGetCallStatus**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetcallstatus)   | <span data-ttu-id="a44d9-197">Возвращает сведения о состоянии завершения вызова для указанного вызова.</span><span class="sxs-lookup"><span data-stu-id="a44d9-197">Returns complete call status information for the specified call.</span></span> <span data-ttu-id="a44d9-198">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="a44d9-198">Synchronous.</span></span>       |
| [<span data-ttu-id="a44d9-199">**ТСПИ \_ линесетаппспеЦифик**</span><span class="sxs-lookup"><span data-stu-id="a44d9-199">**TSPI\_lineSetAppSpecific**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetappspecific) | <span data-ttu-id="a44d9-200">Задает зависящее от приложения поле структуры сведений о вызове.</span><span class="sxs-lookup"><span data-stu-id="a44d9-200">Sets the application-specific field of a call's information structure.</span></span> <span data-ttu-id="a44d9-201">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="a44d9-201">Synchronous.</span></span> |



 

## <a name="making-calls"></a><span data-ttu-id="a44d9-202">Выполнение вызовов</span><span class="sxs-lookup"><span data-stu-id="a44d9-202">Making Calls</span></span>



|                                                 |                                                                        |
|-------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="a44d9-203">**ТСПИ \_ линемакекалл**</span><span class="sxs-lookup"><span data-stu-id="a44d9-203">**TSPI\_lineMakeCall**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall) | <span data-ttu-id="a44d9-204">Выполняет исходящий вызов и возвращает для него маркер вызова.</span><span class="sxs-lookup"><span data-stu-id="a44d9-204">Makes an outbound call and returns a call handle for it.</span></span> <span data-ttu-id="a44d9-205">Асинхронная.</span><span class="sxs-lookup"><span data-stu-id="a44d9-205">Asynchronous.</span></span> |
| [<span data-ttu-id="a44d9-206">**ТСПИ \_ линедиал**</span><span class="sxs-lookup"><span data-stu-id="a44d9-206">**TSPI\_lineDial**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linedial)         | <span data-ttu-id="a44d9-207">Звонки (части одного или нескольких) коммутируемых адресов.</span><span class="sxs-lookup"><span data-stu-id="a44d9-207">Dials (parts of one or more) dialable addresses.</span></span> <span data-ttu-id="a44d9-208">Асинхронная.</span><span class="sxs-lookup"><span data-stu-id="a44d9-208">Asynchronous.</span></span>         |



 

## <a name="answering-incoming-calls"></a><span data-ttu-id="a44d9-209">Ответ на входящие вызовы</span><span class="sxs-lookup"><span data-stu-id="a44d9-209">Answering Incoming Calls</span></span>



|                                             |                                         |
|---------------------------------------------|-----------------------------------------|
| [<span data-ttu-id="a44d9-210">**ТСПИ \_ линеансвер**</span><span class="sxs-lookup"><span data-stu-id="a44d9-210">**TSPI\_lineAnswer**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineanswer) | <span data-ttu-id="a44d9-211">Отвечает на входящий вызов.</span><span class="sxs-lookup"><span data-stu-id="a44d9-211">Answers an incoming call.</span></span> <span data-ttu-id="a44d9-212">Асинхронная.</span><span class="sxs-lookup"><span data-stu-id="a44d9-212">Asynchronous.</span></span> |



 

## <a name="call-drop-functions"></a><span data-ttu-id="a44d9-213">Вызов функций Drop</span><span class="sxs-lookup"><span data-stu-id="a44d9-213">Call Drop Functions</span></span>



|                                         |                                                                           |
|-----------------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="a44d9-214">**ТСПИ \_ линедроп**</span><span class="sxs-lookup"><span data-stu-id="a44d9-214">**TSPI\_lineDrop**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linedrop) | <span data-ttu-id="a44d9-215">Отключает вызов или прерывает выполнение попытки вызова.</span><span class="sxs-lookup"><span data-stu-id="a44d9-215">Disconnects a call, or abandons a call attempt in progress.</span></span> <span data-ttu-id="a44d9-216">Асинхронная.</span><span class="sxs-lookup"><span data-stu-id="a44d9-216">Asynchronous.</span></span> |



 

 

 
