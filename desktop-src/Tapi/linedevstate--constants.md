---
description: '\_Константы битового флага линедевстате описывают различные события состояния линии.'
ms.assetid: 41e8a777-a57a-4d6c-850f-e21b58081b0d
title: Константы LINEDEVSTATE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49717c1adb0f62a48a041f5920c0b82c7b817277
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689490"
---
# <a name="linedevstate_-constants"></a><span data-ttu-id="bad2e-103">\_Константы линедевстате</span><span class="sxs-lookup"><span data-stu-id="bad2e-103">LINEDEVSTATE\_ Constants</span></span>

<span data-ttu-id="bad2e-104">Константы битового флага **линедевстате \_** описывают различные события состояния линии.</span><span class="sxs-lookup"><span data-stu-id="bad2e-104">The **LINEDEVSTATE\_** bit-flag constants describe various line status events.</span></span>

<dl> <dt>

<span data-ttu-id="bad2e-105"><span id="LINEDEVSTATE_BATTERY"></span><span id="linedevstate_battery"></span>**\_батарея линедевстате**</span><span class="sxs-lookup"><span data-stu-id="bad2e-105"><span id="LINEDEVSTATE_BATTERY"></span><span id="linedevstate_battery"></span>**LINEDEVSTATE\_BATTERY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="bad2e-106">Уровень аккумулятора значительно изменился (сотовый).</span><span class="sxs-lookup"><span data-stu-id="bad2e-106">The battery level has changed significantly (cellular).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bad2e-107"><span id="LINEDEVSTATE_CAPSCHANGE"></span><span id="linedevstate_capschange"></span>**ЛИНЕДЕВСТАТЕ \_ капсчанже**</span><span class="sxs-lookup"><span data-stu-id="bad2e-107"><span id="LINEDEVSTATE_CAPSCHANGE"></span><span id="linedevstate_capschange"></span>**LINEDEVSTATE\_CAPSCHANGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="bad2e-108">Указывает, что из-за изменений, внесенных в конфигурацию пользователем или в других обстоятельствах, изменился один или несколько элементов структуры [**линедевкапс**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) для адреса.</span><span class="sxs-lookup"><span data-stu-id="bad2e-108">Indicates that, due to configuration changes made by the user or other circumstances, one or more of the members in the [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) structure for the address have changed.</span></span> <span data-ttu-id="bad2e-109">Приложение должно использовать [**линежетдевкапс**](/windows/desktop/api/Tapi/nf-tapi-linegetdevcaps) для чтения обновленной структуры.</span><span class="sxs-lookup"><span data-stu-id="bad2e-109">The application should use [**lineGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetdevcaps) to read the updated structure.</span></span> <span data-ttu-id="bad2e-110">Если поставщик услуг отправляет сообщение [**Line \_ линедевстате**](line-linedevstate.md) , содержащее это значение в TAPI, TAPI передает его приложениям, ИМЕЮЩИМ согласованный интерфейс TAPI версии 1,4 или более поздней; приложения, согласованные с предыдущей версией TAPI, получают **строки \_ ЛИНЕДЕВСТАТЕ** сообщения с указанием линедевстате \_ reinit, что требует от них завершения работы и повторной инициализации подключения к TAPI для получения обновленной информации.</span><span class="sxs-lookup"><span data-stu-id="bad2e-110">If a service provider sends a [**LINE\_LINEDEVSTATE**](line-linedevstate.md) message containing this value to TAPI, TAPI will pass it along to applications that have negotiated TAPI version 1.4 or later; applications negotiating a previous TAPI version will receive **LINE\_LINEDEVSTATE** messages specifying LINEDEVSTATE\_REINIT, requiring them to shut down and reinitialize their connection to TAPI to obtain the updated information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bad2e-111"><span id="LINEDEVSTATE_CLOSE"></span><span id="linedevstate_close"></span>**ЛИНЕДЕВСТАТЕ \_ Закрыть**</span><span class="sxs-lookup"><span data-stu-id="bad2e-111"><span id="LINEDEVSTATE_CLOSE"></span><span id="linedevstate_close"></span>**LINEDEVSTATE\_CLOSE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="bad2e-112">Строка была закрыта другим приложением.</span><span class="sxs-lookup"><span data-stu-id="bad2e-112">The line has been closed by another application.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bad2e-113"><span id="LINEDEVSTATE_CONFIGCHANGE"></span><span id="linedevstate_configchange"></span>**ЛИНЕДЕВСТАТЕ \_ CONFIGCHANGE**</span><span class="sxs-lookup"><span data-stu-id="bad2e-113"><span id="LINEDEVSTATE_CONFIGCHANGE"></span><span id="linedevstate_configchange"></span>**LINEDEVSTATE\_CONFIGCHANGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="bad2e-114">Указывает, что изменения конфигурации были внесены в одно или несколько устройств мультимедиа, связанных с устройством линии.</span><span class="sxs-lookup"><span data-stu-id="bad2e-114">Indicates that configuration changes have been made to one or more of the media devices associated with the line device.</span></span> <span data-ttu-id="bad2e-115">Приложение, если оно хочет, может использовать [**линежетдевконфиг**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig) для чтения обновленной информации.</span><span class="sxs-lookup"><span data-stu-id="bad2e-115">The application, if it desires, can use [**lineGetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig) to read the updated information.</span></span> <span data-ttu-id="bad2e-116">Если поставщик услуг отправляет сообщение [**Line \_ линедевстате**](line-linedevstate.md) , содержащее это значение в TAPI, TAPI передает его приложениям, имеющим согласованный интерфейс TAPI версии 1,4 или более поздней; приложения, согласованные с предыдущей версией API, не получат уведомлений.</span><span class="sxs-lookup"><span data-stu-id="bad2e-116">If a service provider sends a [**LINE\_LINEDEVSTATE**](line-linedevstate.md) message containing this value to TAPI, TAPI will pass it along to applications that have negotiated TAPI version 1.4 or later; applications negotiating a previous API version will not receive any notification.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bad2e-117"><span id="LINEDEVSTATE_COMPLCANCEL"></span><span id="linedevstate_complcancel"></span>**ЛИНЕДЕВСТАТЕ \_ комплканцел**</span><span class="sxs-lookup"><span data-stu-id="bad2e-117"><span id="LINEDEVSTATE_COMPLCANCEL"></span><span id="linedevstate_complcancel"></span>**LINEDEVSTATE\_COMPLCANCEL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="bad2e-118">Указывает, что завершение вызова, определяемое идентификатором завершения, которое содержится в параметре *dwParam2* сообщения [**Line \_ линедевстате**](line-linedevstate.md) , было внешне отменено и больше не считается допустимым (если это значение было передано при последующем вызове [**ЛИНЕУНКОМПЛЕТЕКАЛЛ**](/windows/desktop/api/Tapi/nf-tapi-lineuncompletecall), функция завершится с линирр \_ инвалкомплетионид).</span><span class="sxs-lookup"><span data-stu-id="bad2e-118">Indicates that the call completion identified by the completion identifier contained in the *dwParam2* parameter of the [**LINE\_LINEDEVSTATE**](line-linedevstate.md) message has been externally canceled and is no longer considered valid (if that value were to be passed in a subsequent call to [**lineUncompleteCall**](/windows/desktop/api/Tapi/nf-tapi-lineuncompletecall), the function would fail with LINEERR\_INVALCOMPLETIONID).</span></span> <span data-ttu-id="bad2e-119">Если поставщик услуг отправляет сообщение [**Line \_ линедевстате**](line-linedevstate.md) , содержащее это значение в TAPI, TAPI передает его приложениям, имеющим согласованный интерфейс TAPI версии 1,4 или более поздней; приложения, согласованные с предыдущей версией API, не получат уведомлений.</span><span class="sxs-lookup"><span data-stu-id="bad2e-119">If a service provider sends a [**LINE\_LINEDEVSTATE**](line-linedevstate.md) message containing this value to TAPI, TAPI will pass it along to applications that have negotiated TAPI version 1.4 or later; applications negotiating a previous API version will not receive any notification.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bad2e-120"><span id="LINEDEVSTATE_CONNECTED"></span><span id="linedevstate_connected"></span>**ЛИНЕДЕВСТАТЕ \_ подключен**</span><span class="sxs-lookup"><span data-stu-id="bad2e-120"><span id="LINEDEVSTATE_CONNECTED"></span><span id="linedevstate_connected"></span>**LINEDEVSTATE\_CONNECTED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="bad2e-121">Строка была ранее отключена и теперь подключена к TAPI.</span><span class="sxs-lookup"><span data-stu-id="bad2e-121">The line was previously disconnected and is now connected to TAPI.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bad2e-122"><span id="LINEDEVSTATE_DEVSPECIFIC"></span><span id="linedevstate_devspecific"></span>**ЛИНЕДЕВСТАТЕ \_ девспеЦифик**</span><span class="sxs-lookup"><span data-stu-id="bad2e-122"><span id="LINEDEVSTATE_DEVSPECIFIC"></span><span id="linedevstate_devspecific"></span>**LINEDEVSTATE\_DEVSPECIFIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="bad2e-123">Изменились сведения, относящиеся к устройству строки.</span><span class="sxs-lookup"><span data-stu-id="bad2e-123">The line's device-specific information has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bad2e-124"><span id="LINEDEVSTATE_DISCONNECTED"></span><span id="linedevstate_disconnected"></span>**ЛИНЕДЕВСТАТЕ \_ отключен**</span><span class="sxs-lookup"><span data-stu-id="bad2e-124"><span id="LINEDEVSTATE_DISCONNECTED"></span><span id="linedevstate_disconnected"></span>**LINEDEVSTATE\_DISCONNECTED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="bad2e-125">Эта строка была подключена ранее и теперь отключена от TAPI.</span><span class="sxs-lookup"><span data-stu-id="bad2e-125">This line was previously connected and is now disconnected from TAPI.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bad2e-126"><span id="LINEDEVSTATE_INSERVICE"></span><span id="linedevstate_inservice"></span>**ЛИНЕДЕВСТАТЕ \_**</span><span class="sxs-lookup"><span data-stu-id="bad2e-126"><span id="LINEDEVSTATE_INSERVICE"></span><span id="linedevstate_inservice"></span>**LINEDEVSTATE\_INSERVICE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="bad2e-127">Линия подключена к TAPI.</span><span class="sxs-lookup"><span data-stu-id="bad2e-127">The line is connected to TAPI.</span></span> <span data-ttu-id="bad2e-128">Это происходит при первой активации TAPI или при физическом соединении линии и в службе в коммутаторе, когда TAPI активен.</span><span class="sxs-lookup"><span data-stu-id="bad2e-128">This happens when TAPI is first activated or when the line wire is physically plugged in and in-service at the switch while TAPI is active.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bad2e-129"><span id="LINEDEVSTATE_LOCK"></span><span id="linedevstate_lock"></span>**\_Блокировка линедевстате**</span><span class="sxs-lookup"><span data-stu-id="bad2e-129"><span id="LINEDEVSTATE_LOCK"></span><span id="linedevstate_lock"></span>**LINEDEVSTATE\_LOCK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="bad2e-130">Состояние блокировки устройства изменилось.</span><span class="sxs-lookup"><span data-stu-id="bad2e-130">The locked status of the line device has changed.</span></span> <span data-ttu-id="bad2e-131">(Дополнительные сведения см. в разделе ЛИНЕДЕВСТАТУСФЛАГС \_ ЗАБЛОКИРОВАНо [**в \_ константах линедевстатусфлагс**](linedevstatusflags--constants.md).)</span><span class="sxs-lookup"><span data-stu-id="bad2e-131">(For more information, see LINEDEVSTATUSFLAGS\_LOCKED in [**LINEDEVSTATUSFLAGS\_ Constants**](linedevstatusflags--constants.md).)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bad2e-132"><span id="LINEDEVSTATE_MAINTENANCE"></span><span id="linedevstate_maintenance"></span>**\_обслуживание линедевстате**</span><span class="sxs-lookup"><span data-stu-id="bad2e-132"><span id="LINEDEVSTATE_MAINTENANCE"></span><span id="linedevstate_maintenance"></span>**LINEDEVSTATE\_MAINTENANCE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="bad2e-133">Обслуживание выполняется в строке на переключателе.</span><span class="sxs-lookup"><span data-stu-id="bad2e-133">Maintenance is being performed on the line at the switch.</span></span> <span data-ttu-id="bad2e-134">TAPI не может использоваться для обработки на устройстве линии.</span><span class="sxs-lookup"><span data-stu-id="bad2e-134">TAPI cannot be used to operate on the line device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bad2e-135"><span id="LINEDEVSTATE_MSGWAITOFF"></span><span id="linedevstate_msgwaitoff"></span>**ЛИНЕДЕВСТАТЕ \_ мсгваитофф**</span><span class="sxs-lookup"><span data-stu-id="bad2e-135"><span id="LINEDEVSTATE_MSGWAITOFF"></span><span id="linedevstate_msgwaitoff"></span>**LINEDEVSTATE\_MSGWAITOFF**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="bad2e-136">Индикатор ожидания сообщений отключен.</span><span class="sxs-lookup"><span data-stu-id="bad2e-136">The message waiting indicator is turned off.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bad2e-137"><span id="LINEDEVSTATE_MSGWAITON"></span><span id="linedevstate_msgwaiton"></span>**ЛИНЕДЕВСТАТЕ \_ мсгваитон**</span><span class="sxs-lookup"><span data-stu-id="bad2e-137"><span id="LINEDEVSTATE_MSGWAITON"></span><span id="linedevstate_msgwaiton"></span>**LINEDEVSTATE\_MSGWAITON**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="bad2e-138">Индикатор ожидания сообщений включен.</span><span class="sxs-lookup"><span data-stu-id="bad2e-138">The message waiting indicator is turned on.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bad2e-139"><span id="LINEDEVSTATE_NUMCALLS"></span><span id="linedevstate_numcalls"></span>**ЛИНЕДЕВСТАТЕ \_ нумкаллс**</span><span class="sxs-lookup"><span data-stu-id="bad2e-139"><span id="LINEDEVSTATE_NUMCALLS"></span><span id="linedevstate_numcalls"></span>**LINEDEVSTATE\_NUMCALLS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="bad2e-140">Число вызовов на устройстве линии изменилось.</span><span class="sxs-lookup"><span data-stu-id="bad2e-140">The number of calls on the line device has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bad2e-141"><span id="LINEDEVSTATE_NUMCOMPLETIONS"></span><span id="linedevstate_numcompletions"></span>**ЛИНЕДЕВСТАТЕ \_ нумкомплетионс**</span><span class="sxs-lookup"><span data-stu-id="bad2e-141"><span id="LINEDEVSTATE_NUMCOMPLETIONS"></span><span id="linedevstate_numcompletions"></span>**LINEDEVSTATE\_NUMCOMPLETIONS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="bad2e-142">Число незавершенных завершений вызова на устройстве линии изменилось.</span><span class="sxs-lookup"><span data-stu-id="bad2e-142">The number of outstanding call completions on the line device has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bad2e-143"><span id="LINEDEVSTATE_OPEN"></span><span id="linedevstate_open"></span>**ЛИНЕДЕВСТАТЕ \_ Открыть**</span><span class="sxs-lookup"><span data-stu-id="bad2e-143"><span id="LINEDEVSTATE_OPEN"></span><span id="linedevstate_open"></span>**LINEDEVSTATE\_OPEN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="bad2e-144">Строка была открыта другим приложением.</span><span class="sxs-lookup"><span data-stu-id="bad2e-144">The line has been opened by another application.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bad2e-145"><span id="LINEDEVSTATE_OTHER"></span><span id="linedevstate_other"></span>**ЛИНЕДЕВСТАТЕ \_**</span><span class="sxs-lookup"><span data-stu-id="bad2e-145"><span id="LINEDEVSTATE_OTHER"></span><span id="linedevstate_other"></span>**LINEDEVSTATE\_OTHER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="bad2e-146">Устройства — элементы состояния, отличные от перечисленных ниже, были изменены.</span><span class="sxs-lookup"><span data-stu-id="bad2e-146">Device-status items other than those listed below have changed.</span></span> <span data-ttu-id="bad2e-147">Приложение должно проверить текущее состояние устройства, чтобы определить, какие элементы были изменены.</span><span class="sxs-lookup"><span data-stu-id="bad2e-147">The application should check the current device status to determine which items have changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bad2e-148"><span id="LINEDEVSTATE_OUTOFSERVICE"></span><span id="linedevstate_outofservice"></span>**ЛИНЕДЕВСТАТЕ \_ аутофсервице**</span><span class="sxs-lookup"><span data-stu-id="bad2e-148"><span id="LINEDEVSTATE_OUTOFSERVICE"></span><span id="linedevstate_outofservice"></span>**LINEDEVSTATE\_OUTOFSERVICE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="bad2e-149">Линия находится вне службы на коммутаторе или физически отключена.</span><span class="sxs-lookup"><span data-stu-id="bad2e-149">The line is out of service at the switch or physically disconnected.</span></span> <span data-ttu-id="bad2e-150">TAPI не может использоваться для обработки на устройстве линии.</span><span class="sxs-lookup"><span data-stu-id="bad2e-150">TAPI cannot be used to operate on the line device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bad2e-151"><span id="LINEDEVSTATE_REINIT"></span><span id="linedevstate_reinit"></span>**ЛИНЕДЕВСТАТЕ \_ REinit**</span><span class="sxs-lookup"><span data-stu-id="bad2e-151"><span id="LINEDEVSTATE_REINIT"></span><span id="linedevstate_reinit"></span>**LINEDEVSTATE\_REINIT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="bad2e-152">Элементы изменились в конфигурации линейных устройств.</span><span class="sxs-lookup"><span data-stu-id="bad2e-152">Items have changed in the configuration of line devices.</span></span> <span data-ttu-id="bad2e-153">Чтобы получить сведения об этих изменениях (как для внешнего вида новых устройств), приложение должно повторно инициализировать использование TAPI.</span><span class="sxs-lookup"><span data-stu-id="bad2e-153">To become aware of these changes (as for the appearance of new line devices) the application should reinitialize its use of TAPI.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bad2e-154"><span id="LINEDEVSTATE_REMOVED"></span><span id="linedevstate_removed"></span>**ЛИНЕДЕВСТАТЕ \_ удален**</span><span class="sxs-lookup"><span data-stu-id="bad2e-154"><span id="LINEDEVSTATE_REMOVED"></span><span id="linedevstate_removed"></span>**LINEDEVSTATE\_REMOVED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="bad2e-155">Указывает, что устройство удаляется из системы поставщиком услуг (скорее всего, через действие пользователя, через панель управления или аналогичную служебную программу).</span><span class="sxs-lookup"><span data-stu-id="bad2e-155">Indicates that the device is being removed from the system by the service provider (most likely through user action, through a control panel or similar utility).</span></span> <span data-ttu-id="bad2e-156">Как правило, [**строка \_ линедевстате**](line-linedevstate.md) с этим значением будет немедленно сопровождаться сообщением [**о \_ закрытии строки**](line-close.md) на устройстве.</span><span class="sxs-lookup"><span data-stu-id="bad2e-156">A [**LINE\_LINEDEVSTATE**](line-linedevstate.md) message with this value will normally be immediately followed by a [**LINE\_CLOSE**](line-close.md) message on the device.</span></span> <span data-ttu-id="bad2e-157">Последующие попытки доступа к устройству до повторной инициализации TAPI приведут к тому, что в \_ приложение будет возвращено устройство линирр.</span><span class="sxs-lookup"><span data-stu-id="bad2e-157">Subsequent attempts to access the device prior to TAPI being reinitialized will result in LINEERR\_NODEVICE being returned to the application.</span></span> <span data-ttu-id="bad2e-158">Если поставщик услуг отправляет сообщение [**Line \_ линедевстате**](line-linedevstate.md) , содержащее это значение в TAPI, TAPI передает его приложениям, имеющим согласованный интерфейс TAPI версии 1,4 или более поздней; приложения, согласованные с предыдущей версией API, не получат уведомлений.</span><span class="sxs-lookup"><span data-stu-id="bad2e-158">If a service provider sends a [**LINE\_LINEDEVSTATE**](line-linedevstate.md) message containing this value to TAPI, TAPI will pass it along to applications that have negotiated TAPI version 1.4 or later; applications negotiating a previous API version will not receive any notification.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bad2e-159"><span id="LINEDEVSTATE_RINGING"></span><span id="linedevstate_ringing"></span>**ЛИНЕДЕВСТАТЕ \_ Звонок**</span><span class="sxs-lookup"><span data-stu-id="bad2e-159"><span id="LINEDEVSTATE_RINGING"></span><span id="linedevstate_ringing"></span>**LINEDEVSTATE\_RINGING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="bad2e-160">Параметр сообщает строке о необходимости оповещения пользователя.</span><span class="sxs-lookup"><span data-stu-id="bad2e-160">The switch tells the line to alert the user.</span></span>

<span data-ttu-id="bad2e-161">**TAPI:** Поставщики услуг уведомляют приложения в каждом цикле круга за счет многократной отправки [**строк \_ линедевстате**](line-linedevstate.md) сообщений, содержащих эту константу.</span><span class="sxs-lookup"><span data-stu-id="bad2e-161">**TAPI:** Service providers notify applications on each ring cycle by repeatedly sending [**LINE\_LINEDEVSTATE**](line-linedevstate.md) messages containing this constant.</span></span> <span data-ttu-id="bad2e-162">Например, в США поставщики услуг отправляют сообщение с этой константой каждые шесть секунд.</span><span class="sxs-lookup"><span data-stu-id="bad2e-162">For example, in the United States, service providers send a message with this constant every six seconds.</span></span>

<span data-ttu-id="bad2e-163">**Тспи:** На устройстве POTS поставщик услуг может отправлять сообщение каждый раз, когда Центральный офис отправляет напряжение кольца.</span><span class="sxs-lookup"><span data-stu-id="bad2e-163">**TSPI:** On a POTS device, the service provider can send the message whenever the central office sends ring voltage.</span></span> <span data-ttu-id="bad2e-164">На цифровых устройствах, таких как ISDN, поставщику услуг может потребоваться создать повторение сообщения, если параметр создает только один запрос кольца.</span><span class="sxs-lookup"><span data-stu-id="bad2e-164">On digital devices such as ISDN, the service provider may need to synthesize the repetition of the message if the switch generates only one ring request.</span></span> <span data-ttu-id="bad2e-165">Каждое повторение сообщения должно показывать увеличение числа звонков, чтобы функции бесплатного сохранения работали правильно.</span><span class="sxs-lookup"><span data-stu-id="bad2e-165">Each repetition of the message should show the ring count increasing, so that toll save functions work properly.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bad2e-166"><span id="LINEDEVSTATE_ROAMMODE"></span><span id="linedevstate_roammode"></span>**ЛИНЕДЕВСТАТЕ \_ роаммоде**</span><span class="sxs-lookup"><span data-stu-id="bad2e-166"><span id="LINEDEVSTATE_ROAMMODE"></span><span id="linedevstate_roammode"></span>**LINEDEVSTATE\_ROAMMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="bad2e-167">Режим перемещения линейного устройства изменился.</span><span class="sxs-lookup"><span data-stu-id="bad2e-167">The roam mode of the line device has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bad2e-168"><span id="LINEDEVSTATE_SIGNAL"></span><span id="linedevstate_signal"></span>**\_сигнал линедевстате**</span><span class="sxs-lookup"><span data-stu-id="bad2e-168"><span id="LINEDEVSTATE_SIGNAL"></span><span id="linedevstate_signal"></span>**LINEDEVSTATE\_SIGNAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="bad2e-169">Уровень сигнала значительно изменился (сотовый).</span><span class="sxs-lookup"><span data-stu-id="bad2e-169">The signal level has changed significantly (cellular).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bad2e-170"><span id="LINEDEVSTATE_TERMINALS"></span><span id="linedevstate_terminals"></span>**ЛИНЕДЕВСТАТЕ \_ терминалов**</span><span class="sxs-lookup"><span data-stu-id="bad2e-170"><span id="LINEDEVSTATE_TERMINALS"></span><span id="linedevstate_terminals"></span>**LINEDEVSTATE\_TERMINALS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="bad2e-171">Параметры терминала изменены.</span><span class="sxs-lookup"><span data-stu-id="bad2e-171">The terminal settings have changed.</span></span> <span data-ttu-id="bad2e-172">Это может произойти, например, если несколько линий используют терминалы между ними (например, две линии, совместно использующие телефонный терминал).</span><span class="sxs-lookup"><span data-stu-id="bad2e-172">This can happen, for example, if multiple line devices share terminals among them (for example, two lines sharing a phone terminal).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bad2e-173"><span id="LINEDEVSTATE_TRANSLATECHANGE"></span><span id="linedevstate_translatechange"></span>**ЛИНЕДЕВСТАТЕ \_ транслатечанже**</span><span class="sxs-lookup"><span data-stu-id="bad2e-173"><span id="LINEDEVSTATE_TRANSLATECHANGE"></span><span id="linedevstate_translatechange"></span>**LINEDEVSTATE\_TRANSLATECHANGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="bad2e-174">Указывает, что из-за изменений в конфигурации, внесенных пользователем или в других обстоятельствах, изменился один или несколько элементов в структуре [**линетранслатекапс**](/windows/desktop/api/Tapi/ns-tapi-linetranslatecaps) .</span><span class="sxs-lookup"><span data-stu-id="bad2e-174">Indicates that, due to configuration changes made by the user or other circumstances, one or more of the members in the [**LINETRANSLATECAPS**](/windows/desktop/api/Tapi/ns-tapi-linetranslatecaps) structure have changed.</span></span> <span data-ttu-id="bad2e-175">Приложение должно использовать [**линежеттранслатекапс**](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps) для чтения обновленной структуры.</span><span class="sxs-lookup"><span data-stu-id="bad2e-175">The application should use [**lineGetTranslateCaps**](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps) to read the updated structure.</span></span> <span data-ttu-id="bad2e-176">Если поставщик услуг отправляет сообщение [**Line \_ линедевстате**](line-linedevstate.md) , содержащее это значение в TAPI, TAPI передает его приложениям, ИМЕЮЩИМ согласованный интерфейс TAPI версии 1,4 или более поздней; приложения, согласованные с предыдущей версией TAPI, получают **строки \_ ЛИНЕДЕВСТАТЕ** сообщения с указанием линедевстате \_ reinit, что требует от них завершения работы и повторной инициализации подключения к TAPI для получения обновленной информации.</span><span class="sxs-lookup"><span data-stu-id="bad2e-176">If a service provider sends a [**LINE\_LINEDEVSTATE**](line-linedevstate.md) message containing this value to TAPI, TAPI will pass it along to applications that have negotiated TAPI version 1.4 or later; applications negotiating a previous TAPI version will receive **LINE\_LINEDEVSTATE** messages specifying LINEDEVSTATE\_REINIT, requiring them to shut down and reinitialize their connection to TAPI to obtain the updated information.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bad2e-177">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bad2e-177">Remarks</span></span>

<span data-ttu-id="bad2e-178">Без расширяемости.</span><span class="sxs-lookup"><span data-stu-id="bad2e-178">No extensibility.</span></span> <span data-ttu-id="bad2e-179">Все 32 бит зарезервированы.</span><span class="sxs-lookup"><span data-stu-id="bad2e-179">All 32 bits are reserved.</span></span>

## <a name="requirements"></a><span data-ttu-id="bad2e-180">Требования</span><span class="sxs-lookup"><span data-stu-id="bad2e-180">Requirements</span></span>



| <span data-ttu-id="bad2e-181">Требование</span><span class="sxs-lookup"><span data-stu-id="bad2e-181">Requirement</span></span> | <span data-ttu-id="bad2e-182">Значение</span><span class="sxs-lookup"><span data-stu-id="bad2e-182">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="bad2e-183">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="bad2e-183">TAPI version</span></span><br/> | <span data-ttu-id="bad2e-184">Требуется TAPI 2,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="bad2e-184">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="bad2e-185">Header</span><span class="sxs-lookup"><span data-stu-id="bad2e-185">Header</span></span><br/>       | <dl> <span data-ttu-id="bad2e-186"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="bad2e-186"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bad2e-187">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bad2e-187">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bad2e-188">**\_закрыть строку**</span><span class="sxs-lookup"><span data-stu-id="bad2e-188">**LINE\_CLOSE**</span></span>](line-close.md)
</dt> <dt>

[<span data-ttu-id="bad2e-189">**Строка \_ линедевстате**</span><span class="sxs-lookup"><span data-stu-id="bad2e-189">**LINE\_LINEDEVSTATE**</span></span>](line-linedevstate.md)
</dt> <dt>

[<span data-ttu-id="bad2e-190">**линедевкапс**</span><span class="sxs-lookup"><span data-stu-id="bad2e-190">**LINEDEVCAPS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linedevcaps)
</dt> <dt>

[<span data-ttu-id="bad2e-191">**линежетдевкапс**</span><span class="sxs-lookup"><span data-stu-id="bad2e-191">**lineGetDevCaps**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetdevcaps)
</dt> <dt>

[<span data-ttu-id="bad2e-192">**линежетдевконфиг**</span><span class="sxs-lookup"><span data-stu-id="bad2e-192">**lineGetDevConfig**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig)
</dt> <dt>

[<span data-ttu-id="bad2e-193">**линежеттранслатекапс**</span><span class="sxs-lookup"><span data-stu-id="bad2e-193">**lineGetTranslateCaps**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps)
</dt> <dt>

[<span data-ttu-id="bad2e-194">**линетранслатекапс**</span><span class="sxs-lookup"><span data-stu-id="bad2e-194">**LINETRANSLATECAPS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linetranslatecaps)
</dt> <dt>

[<span data-ttu-id="bad2e-195">**линеункомплетекалл**</span><span class="sxs-lookup"><span data-stu-id="bad2e-195">**lineUncompleteCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineuncompletecall)
</dt> </dl>

 

 




