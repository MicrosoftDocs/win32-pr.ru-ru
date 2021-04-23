---
description: '\_Константы побитового флага фонестате описывают различные элементы состояния для телефонного устройства.'
ms.assetid: 5db53dd4-606a-40b9-9159-b67a0ea1e400
title: Константы PHONESTATE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6346251f6947aebb2a5941389843e2abcec77c4a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675136"
---
# <a name="phonestate_-constants"></a><span data-ttu-id="6a823-103">\_Константы фонестате</span><span class="sxs-lookup"><span data-stu-id="6a823-103">PHONESTATE\_ Constants</span></span>

<span data-ttu-id="6a823-104">Константы побитового флага **фонестате \_** описывают различные элементы состояния для телефонного устройства.</span><span class="sxs-lookup"><span data-stu-id="6a823-104">The **PHONESTATE\_** bit-flag constants describe various status items for a phone device.</span></span>

<dl> <dt>

<span data-ttu-id="6a823-105"><span id="PHONESTATE_CAPSCHANGE"></span><span id="phonestate_capschange"></span>**ФОНЕСТАТЕ \_ капсчанже**</span><span class="sxs-lookup"><span data-stu-id="6a823-105"><span id="PHONESTATE_CAPSCHANGE"></span><span id="phonestate_capschange"></span>**PHONESTATE\_CAPSCHANGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6a823-106">Указывает, что из-за изменений в конфигурации, внесенных пользователем или в других обстоятельствах, изменился один или несколько элементов в структуре [**фонекапс**](/windows/desktop/api/Tapi/ns-tapi-phonecaps) .</span><span class="sxs-lookup"><span data-stu-id="6a823-106">Indicates that, due to configuration changes made by the user or other circumstances, one or more of the members in the [**PHONECAPS**](/windows/desktop/api/Tapi/ns-tapi-phonecaps) structure have changed.</span></span> <span data-ttu-id="6a823-107">Приложение должно использовать [**фонежетдевкапс**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps) для чтения обновленной структуры.</span><span class="sxs-lookup"><span data-stu-id="6a823-107">The application should use [**phoneGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps) to read the updated structure.</span></span> <span data-ttu-id="6a823-108">Если поставщик услуг отправляет сообщение о [**\_ состоянии телефона**](phone-state.md) , содержащее это значение, в TAPI, TAPI передает его в приложения с согласованным интерфейсом TAPI версии 1,4 или более поздней; приложения, согласованные с предыдущей версией API, будут получать сообщения о состоянии телефона с \_ указанием фонестате \_ reinit, что требует от них завершения работы и ПОВТОРНОй инициализации подключения к TAPI для получения обновленных сведений.</span><span class="sxs-lookup"><span data-stu-id="6a823-108">If a service provider sends a [**PHONE\_STATE**](phone-state.md) message containing this value to TAPI, TAPI will pass it along to applications that have negotiated TAPI version 1.4 or later; applications negotiating a previous API version will receive PHONE\_STATE messages specifying PHONESTATE\_REINIT, requiring them to shut down and reinitialize their connection to TAPI to obtain the updated information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6a823-109"><span id="PHONESTATE_CONNECTED"></span><span id="phonestate_connected"></span>**ФОНЕСТАТЕ \_ подключен**</span><span class="sxs-lookup"><span data-stu-id="6a823-109"><span id="PHONESTATE_CONNECTED"></span><span id="phonestate_connected"></span>**PHONESTATE\_CONNECTED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6a823-110">Подключение между телефонным устройством и TAPI было только что установлено.</span><span class="sxs-lookup"><span data-stu-id="6a823-110">The connection between the phone device and TAPI was just made.</span></span> <span data-ttu-id="6a823-111">Это происходит при первом вызове TAPI или при соединении телефонного подключения к компьютеру с помощью TAPI Active.</span><span class="sxs-lookup"><span data-stu-id="6a823-111">This happens when TAPI is first invoked or when the wire connecting the phone to the PC is plugged in with TAPI active.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6a823-112"><span id="PHONESTATE_DEVSPECIFIC"></span><span id="phonestate_devspecific"></span>**ФОНЕСТАТЕ \_ девспеЦифик**</span><span class="sxs-lookup"><span data-stu-id="6a823-112"><span id="PHONESTATE_DEVSPECIFIC"></span><span id="phonestate_devspecific"></span>**PHONESTATE\_DEVSPECIFIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6a823-113">Сведения об устройстве, относящиеся к устройству телефона, изменились.</span><span class="sxs-lookup"><span data-stu-id="6a823-113">The phone's device-specific information has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6a823-114"><span id="PHONESTATE_DISCONNECTED"></span><span id="phonestate_disconnected"></span>**ФОНЕСТАТЕ \_ отключен**</span><span class="sxs-lookup"><span data-stu-id="6a823-114"><span id="PHONESTATE_DISCONNECTED"></span><span id="phonestate_disconnected"></span>**PHONESTATE\_DISCONNECTED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6a823-115">Подключение между телефонным устройством и TAPI было только что разорвано.</span><span class="sxs-lookup"><span data-stu-id="6a823-115">The connection between the phone device and TAPI was just broken.</span></span> <span data-ttu-id="6a823-116">Это происходит, когда подключение, соединяющее набор телефонов с компьютером, не подключено, пока активен интерфейс TAPI.</span><span class="sxs-lookup"><span data-stu-id="6a823-116">This happens when the wire connecting the phone set to the PC is unplugged while TAPI is active.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6a823-117"><span id="PHONESTATE_DISPLAY"></span><span id="phonestate_display"></span>**ФОНЕСТАТЕ \_ дисплей**</span><span class="sxs-lookup"><span data-stu-id="6a823-117"><span id="PHONESTATE_DISPLAY"></span><span id="phonestate_display"></span>**PHONESTATE\_DISPLAY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6a823-118">Изменился вид телефона.</span><span class="sxs-lookup"><span data-stu-id="6a823-118">The display of the phone has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6a823-119"><span id="PHONESTATE_HANDSETGAIN"></span><span id="phonestate_handsetgain"></span>**ФОНЕСТАТЕ \_ хандсетгаин**</span><span class="sxs-lookup"><span data-stu-id="6a823-119"><span id="PHONESTATE_HANDSETGAIN"></span><span id="phonestate_handsetgain"></span>**PHONESTATE\_HANDSETGAIN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6a823-120">Настройка усиления микрофона телефонной трубки изменилась.</span><span class="sxs-lookup"><span data-stu-id="6a823-120">The handset's microphone gain setting has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6a823-121"><span id="PHONESTATE_HANDSETHOOKSWITCH"></span><span id="phonestate_handsethookswitch"></span>**ФОНЕСТАТЕ \_ хандсесуксвитч**</span><span class="sxs-lookup"><span data-stu-id="6a823-121"><span id="PHONESTATE_HANDSETHOOKSWITCH"></span><span id="phonestate_handsethookswitch"></span>**PHONESTATE\_HANDSETHOOKSWITCH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6a823-122">Изменилось состояние хуксвитча трубки.</span><span class="sxs-lookup"><span data-stu-id="6a823-122">The handset hookswitch state has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6a823-123"><span id="PHONESTATE_HANDSETVOLUME"></span><span id="phonestate_handsetvolume"></span>**ФОНЕСТАТЕ \_ хандсетволуме**</span><span class="sxs-lookup"><span data-stu-id="6a823-123"><span id="PHONESTATE_HANDSETVOLUME"></span><span id="phonestate_handsetvolume"></span>**PHONESTATE\_HANDSETVOLUME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6a823-124">Параметр громкости динамика телефонной трубки изменился.</span><span class="sxs-lookup"><span data-stu-id="6a823-124">The handset's speaker volume setting has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6a823-125"><span id="PHONESTATE_HEADSETHOOKSWITCH"></span><span id="phonestate_headsethookswitch"></span>**ФОНЕСТАТЕ \_ хеадсесуксвитч**</span><span class="sxs-lookup"><span data-stu-id="6a823-125"><span id="PHONESTATE_HEADSETHOOKSWITCH"></span><span id="phonestate_headsethookswitch"></span>**PHONESTATE\_HEADSETHOOKSWITCH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6a823-126">Изменилось состояние хуксвитч гарнитуры.</span><span class="sxs-lookup"><span data-stu-id="6a823-126">The headset's hookswitch state has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6a823-127"><span id="PHONESTATE_HEADSETGAIN"></span><span id="phonestate_headsetgain"></span>**ФОНЕСТАТЕ \_ хеадсетгаин**</span><span class="sxs-lookup"><span data-stu-id="6a823-127"><span id="PHONESTATE_HEADSETGAIN"></span><span id="phonestate_headsetgain"></span>**PHONESTATE\_HEADSETGAIN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6a823-128">Настройка усиления микрофона для гарнитуры изменена.</span><span class="sxs-lookup"><span data-stu-id="6a823-128">The headset's microphone gain setting has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6a823-129"><span id="PHONESTATE_HEADSETVOLUME"></span><span id="phonestate_headsetvolume"></span>**ФОНЕСТАТЕ \_ хеадсетволуме**</span><span class="sxs-lookup"><span data-stu-id="6a823-129"><span id="PHONESTATE_HEADSETVOLUME"></span><span id="phonestate_headsetvolume"></span>**PHONESTATE\_HEADSETVOLUME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6a823-130">Параметр громкости динамика гарнитуры изменился.</span><span class="sxs-lookup"><span data-stu-id="6a823-130">The headset's speaker volume setting has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6a823-131"><span id="PHONESTATE_LAMP"></span><span id="phonestate_lamp"></span>**\_лампа фонестате**</span><span class="sxs-lookup"><span data-stu-id="6a823-131"><span id="PHONESTATE_LAMP"></span><span id="phonestate_lamp"></span>**PHONESTATE\_LAMP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6a823-132">Изменилась лампа телефона.</span><span class="sxs-lookup"><span data-stu-id="6a823-132">A lamp of the phone has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6a823-133"><span id="PHONESTATE_MONITORS"></span><span id="phonestate_monitors"></span>**\_мониторы фонестате**</span><span class="sxs-lookup"><span data-stu-id="6a823-133"><span id="PHONESTATE_MONITORS"></span><span id="phonestate_monitors"></span>**PHONESTATE\_MONITORS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6a823-134">Число мониторов для телефонного устройства.</span><span class="sxs-lookup"><span data-stu-id="6a823-134">The number of monitors for the phone device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6a823-135"><span id="PHONESTATE_OTHER"></span><span id="phonestate_other"></span>**ФОНЕСТАТЕ \_**</span><span class="sxs-lookup"><span data-stu-id="6a823-135"><span id="PHONESTATE_OTHER"></span><span id="phonestate_other"></span>**PHONESTATE\_OTHER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6a823-136">Phone — изменились элементы состояния, отличные от перечисленных ниже.</span><span class="sxs-lookup"><span data-stu-id="6a823-136">Phone-status items other than those listed below have changed.</span></span> <span data-ttu-id="6a823-137">Приложение должно проверить текущее состояние телефона, чтобы определить, какие элементы были изменены.</span><span class="sxs-lookup"><span data-stu-id="6a823-137">The application should check the current phone status to determine which items have changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6a823-138"><span id="PHONESTATE_OWNER"></span><span id="phonestate_owner"></span>**\_владелец фонестате**</span><span class="sxs-lookup"><span data-stu-id="6a823-138"><span id="PHONESTATE_OWNER"></span><span id="phonestate_owner"></span>**PHONESTATE\_OWNER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6a823-139">Число владельцев для телефонного устройства.</span><span class="sxs-lookup"><span data-stu-id="6a823-139">The number of owners for the phone device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6a823-140"><span id="PHONESTATE_REINIT"></span><span id="phonestate_reinit"></span>**ФОНЕСТАТЕ \_ REinit**</span><span class="sxs-lookup"><span data-stu-id="6a823-140"><span id="PHONESTATE_REINIT"></span><span id="phonestate_reinit"></span>**PHONESTATE\_REINIT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6a823-141">Элементы изменились в конфигурации телефонных устройств.</span><span class="sxs-lookup"><span data-stu-id="6a823-141">Items have changed in the configuration of phone devices.</span></span> <span data-ttu-id="6a823-142">Чтобы получать сведения об этих изменениях (как для внешнего вида новых телефонных устройств), приложение должно повторно инициализировать использование TAPI.</span><span class="sxs-lookup"><span data-stu-id="6a823-142">To become aware of these changes (as for the appearance of new phone devices), the application should reinitialize its use of TAPI.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6a823-143"><span id="PHONESTATE_REMOVED"></span><span id="phonestate_removed"></span>**ФОНЕСТАТЕ \_ удален**</span><span class="sxs-lookup"><span data-stu-id="6a823-143"><span id="PHONESTATE_REMOVED"></span><span id="phonestate_removed"></span>**PHONESTATE\_REMOVED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6a823-144">Указывает, что устройство удаляется из системы поставщиком услуг (скорее всего, через действие пользователя, через панель управления или аналогичную служебную программу).</span><span class="sxs-lookup"><span data-stu-id="6a823-144">Indicates that the device is being removed from the system by the service provider (most likely through user action, through a control panel or similar utility).</span></span> <span data-ttu-id="6a823-145">Обычно за сообщением о [**\_ состоянии телефона**](phone-state.md) с этим значением будет немедленно следовать сообщение [**\_ закрытия телефона**](phone-close.md) на устройстве.</span><span class="sxs-lookup"><span data-stu-id="6a823-145">A [**PHONE\_STATE**](phone-state.md) message with this value will normally be immediately followed by a [**PHONE\_CLOSE**](phone-close.md) message on the device.</span></span> <span data-ttu-id="6a823-146">Последующие попытки доступа к устройству до повторной инициализации TAPI приведут к тому, что в \_ приложение будет возвращено устройство фонирр.</span><span class="sxs-lookup"><span data-stu-id="6a823-146">Subsequent attempts to access the device prior to TAPI being reinitialized will result in PHONEERR\_NODEVICE being returned to the application.</span></span> <span data-ttu-id="6a823-147">Если поставщик услуг отправляет \_ сообщение о состоянии телефона, содержащее это значение, в TAPI, TAPI передает его приложениям, имеющим согласованный интерфейс TAPI версии 1,4 или более поздней; приложения, согласованные с предыдущей версией API, не получат уведомлений.</span><span class="sxs-lookup"><span data-stu-id="6a823-147">If a service provider sends a PHONE\_STATE message containing this value to TAPI, TAPI will pass it along to applications that have negotiated TAPI version 1.4 or later; applications negotiating a previous API version will not receive any notification.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6a823-148"><span id="PHONESTATE_RESUME"></span><span id="phonestate_resume"></span>**возобновление ФОНЕСТАТЕ \_**</span><span class="sxs-lookup"><span data-stu-id="6a823-148"><span id="PHONESTATE_RESUME"></span><span id="phonestate_resume"></span>**PHONESTATE\_RESUME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6a823-149">Приложение, используемое для телефонного устройства, будет возобновлено после приостановки в течение некоторого времени.</span><span class="sxs-lookup"><span data-stu-id="6a823-149">The application's use of the phone device is resumed after having been suspended for some time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6a823-150"><span id="PHONESTATE_RINGMODE"></span><span id="phonestate_ringmode"></span>**ФОНЕСТАТЕ \_ рингмоде**</span><span class="sxs-lookup"><span data-stu-id="6a823-150"><span id="PHONESTATE_RINGMODE"></span><span id="phonestate_ringmode"></span>**PHONESTATE\_RINGMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6a823-151">Режим кольца телефона изменился.</span><span class="sxs-lookup"><span data-stu-id="6a823-151">The ring mode of the phone has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6a823-152"><span id="PHONESTATE_RINGVOLUME"></span><span id="phonestate_ringvolume"></span>**ФОНЕСТАТЕ \_ рингволуме**</span><span class="sxs-lookup"><span data-stu-id="6a823-152"><span id="PHONESTATE_RINGVOLUME"></span><span id="phonestate_ringvolume"></span>**PHONESTATE\_RINGVOLUME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6a823-153">Громкость звонка на телефоне изменилась.</span><span class="sxs-lookup"><span data-stu-id="6a823-153">The ring volume of the phone has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6a823-154"><span id="PHONESTATE_SPEAKERHOOKSWITCH"></span><span id="phonestate_speakerhookswitch"></span>**ФОНЕСТАТЕ \_ спеакерхуксвитч**</span><span class="sxs-lookup"><span data-stu-id="6a823-154"><span id="PHONESTATE_SPEAKERHOOKSWITCH"></span><span id="phonestate_speakerhookswitch"></span>**PHONESTATE\_SPEAKERHOOKSWITCH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6a823-155">Изменилось состояние хуксвитча динамика.</span><span class="sxs-lookup"><span data-stu-id="6a823-155">The speakerphone's hookswitch state has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6a823-156"><span id="PHONESTATE_SPEAKERGAIN"></span><span id="phonestate_speakergain"></span>**ФОНЕСТАТЕ \_ спеакергаин**</span><span class="sxs-lookup"><span data-stu-id="6a823-156"><span id="PHONESTATE_SPEAKERGAIN"></span><span id="phonestate_speakergain"></span>**PHONESTATE\_SPEAKERGAIN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6a823-157">Состояние настройки усиления микрофона динамика изменилось.</span><span class="sxs-lookup"><span data-stu-id="6a823-157">The speakerphone's microphone gain setting state has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6a823-158"><span id="PHONESTATE_SPEAKERVOLUME"></span><span id="phonestate_speakervolume"></span>**ФОНЕСТАТЕ \_ спеакерволуме**</span><span class="sxs-lookup"><span data-stu-id="6a823-158"><span id="PHONESTATE_SPEAKERVOLUME"></span><span id="phonestate_speakervolume"></span>**PHONESTATE\_SPEAKERVOLUME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6a823-159">Параметр громкости динамиков динамика изменился.</span><span class="sxs-lookup"><span data-stu-id="6a823-159">The speakerphone's speaker volume setting has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6a823-160"><span id="PHONESTATE_SUSPEND"></span><span id="phonestate_suspend"></span>**Приостановка ФОНЕСТАТЕ \_**</span><span class="sxs-lookup"><span data-stu-id="6a823-160"><span id="PHONESTATE_SUSPEND"></span><span id="phonestate_suspend"></span>**PHONESTATE\_SUSPEND**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6a823-161">Приложение использует телефон временно приостановлено.</span><span class="sxs-lookup"><span data-stu-id="6a823-161">The application's use of the phone is temporarily suspended.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6a823-162">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6a823-162">Remarks</span></span>

<span data-ttu-id="6a823-163">Без расширяемости.</span><span class="sxs-lookup"><span data-stu-id="6a823-163">No extensibility.</span></span> <span data-ttu-id="6a823-164">Все 32 бит зарезервированы.</span><span class="sxs-lookup"><span data-stu-id="6a823-164">All 32 bits are reserved.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a823-165">Требования</span><span class="sxs-lookup"><span data-stu-id="6a823-165">Requirements</span></span>



| <span data-ttu-id="6a823-166">Требование</span><span class="sxs-lookup"><span data-stu-id="6a823-166">Requirement</span></span> | <span data-ttu-id="6a823-167">Значение</span><span class="sxs-lookup"><span data-stu-id="6a823-167">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="6a823-168">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="6a823-168">TAPI version</span></span><br/> | <span data-ttu-id="6a823-169">Требуется TAPI 2,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="6a823-169">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="6a823-170">Header</span><span class="sxs-lookup"><span data-stu-id="6a823-170">Header</span></span><br/>       | <dl> <span data-ttu-id="6a823-171"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="6a823-171"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a823-172">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6a823-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a823-173">**\_закрытие телефона**</span><span class="sxs-lookup"><span data-stu-id="6a823-173">**PHONE\_CLOSE**</span></span>](phone-close.md)
</dt> <dt>

[<span data-ttu-id="6a823-174">**\_состояние телефона**</span><span class="sxs-lookup"><span data-stu-id="6a823-174">**PHONE\_STATE**</span></span>](phone-state.md)
</dt> <dt>

[<span data-ttu-id="6a823-175">**фонекапс**</span><span class="sxs-lookup"><span data-stu-id="6a823-175">**PHONECAPS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-phonecaps)
</dt> <dt>

[<span data-ttu-id="6a823-176">**фонежетдевкапс**</span><span class="sxs-lookup"><span data-stu-id="6a823-176">**phoneGetDevCaps**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps)
</dt> </dl>

 

 




