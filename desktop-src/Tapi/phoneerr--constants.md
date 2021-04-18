---
description: Это список кодов ошибок, которые может возвращать реализация при вызове операций на телефонных устройствах. Ознакомьтесь с описаниями отдельных функций, чтобы определить, какие из этих кодов ошибок могут быть возвращены каждой функцией.
ms.assetid: 763a9dc2-3e70-4169-a66e-3aac78ef8d33
title: Константы PHONEERR_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b41ba5d14f4aa12318dd4bc9f2b20e4e9e2e6b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680107"
---
# <a name="phoneerr_-constants"></a><span data-ttu-id="ec403-104">\_Константы фонирр</span><span class="sxs-lookup"><span data-stu-id="ec403-104">PHONEERR\_ Constants</span></span>

<span data-ttu-id="ec403-105">Это список кодов ошибок, которые может возвращать реализация при вызове операций на телефонных устройствах.</span><span class="sxs-lookup"><span data-stu-id="ec403-105">This is the list of error codes that the implementation can return when invoking operations on phone devices.</span></span> <span data-ttu-id="ec403-106">Ознакомьтесь с описаниями отдельных функций, чтобы определить, какие из этих кодов ошибок могут быть возвращены каждой функцией.</span><span class="sxs-lookup"><span data-stu-id="ec403-106">Consult the individual function descriptions to determine which of these error codes each function can return.</span></span>

<dl> <dt>

<span data-ttu-id="ec403-107"><span id="PHONEERR_ALLOCATED"></span><span id="phoneerr_allocated"></span>**ФОНИРР \_ выделен**</span><span class="sxs-lookup"><span data-stu-id="ec403-107"><span id="PHONEERR_ALLOCATED"></span><span id="phoneerr_allocated"></span>**PHONEERR\_ALLOCATED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ec403-108">Указанный ресурс уже выделен.</span><span class="sxs-lookup"><span data-stu-id="ec403-108">The specified resource is already allocated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ec403-109"><span id="PHONEERR_BADDEVICEID"></span><span id="phoneerr_baddeviceid"></span>**ФОНИРР \_ баддевицеид**</span><span class="sxs-lookup"><span data-stu-id="ec403-109"><span id="PHONEERR_BADDEVICEID"></span><span id="phoneerr_baddeviceid"></span>**PHONEERR\_BADDEVICEID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ec403-110">Указанный идентификатор устройства недопустим или находится вне допустимого диапазона.</span><span class="sxs-lookup"><span data-stu-id="ec403-110">The specified device identifier is invalid or out of range.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ec403-111"><span id="PHONEERR_DISCONNECTED"></span><span id="phoneerr_disconnected"></span>**ФОНИРР \_ отключен**</span><span class="sxs-lookup"><span data-stu-id="ec403-111"><span id="PHONEERR_DISCONNECTED"></span><span id="phoneerr_disconnected"></span>**PHONEERR\_DISCONNECTED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ec403-112">Вызов был отключен.</span><span class="sxs-lookup"><span data-stu-id="ec403-112">The call was disconnected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ec403-113"><span id="PHONEERR_INCOMPATIBLEAPIVERSION"></span><span id="phoneerr_incompatibleapiversion"></span>**ФОНИРР \_ инкомпатиблеапиверсион**</span><span class="sxs-lookup"><span data-stu-id="ec403-113"><span id="PHONEERR_INCOMPATIBLEAPIVERSION"></span><span id="phoneerr_incompatibleapiversion"></span>**PHONEERR\_INCOMPATIBLEAPIVERSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ec403-114">Приложение запросило версию API или диапазон версий, которые не поддерживаются реализацией API телефонии или соответствующим поставщиком услуг.</span><span class="sxs-lookup"><span data-stu-id="ec403-114">The application requested an API version or version range that cannot be supported by the Telephony API implementation or the corresponding service provider.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ec403-115"><span id="PHONEERR_INCOMPATIBLEEXTVERSION"></span><span id="phoneerr_incompatibleextversion"></span>**ФОНИРР \_ инкомпатибликстверсион**</span><span class="sxs-lookup"><span data-stu-id="ec403-115"><span id="PHONEERR_INCOMPATIBLEEXTVERSION"></span><span id="phoneerr_incompatibleextversion"></span>**PHONEERR\_INCOMPATIBLEEXTVERSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ec403-116">Приложение запросило версию или диапазон версий расширения, которые не поддерживаются поставщиком услуг.</span><span class="sxs-lookup"><span data-stu-id="ec403-116">The application requested an extension version or version range that cannot be supported by the service provider.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ec403-117"><span id="PHONEERR_INIFILECORRUPT"></span><span id="phoneerr_inifilecorrupt"></span>**ФОНИРР \_ инифилекоррупт**</span><span class="sxs-lookup"><span data-stu-id="ec403-117"><span id="PHONEERR_INIFILECORRUPT"></span><span id="phoneerr_inifilecorrupt"></span>**PHONEERR\_INIFILECORRUPT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ec403-118">Из-за внутренних несоответствий или ошибок форматирования в файле Telephon.ini он не может быть правильно прочитан и понятен интерфейсом TAPI.</span><span class="sxs-lookup"><span data-stu-id="ec403-118">Because of internal inconsistencies or formatting problems in the Telephon.ini file, it cannot be read and understood properly by TAPI.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ec403-119"><span id="PHONEERR_INUSE"></span><span id="phoneerr_inuse"></span>**ФОНИРР \_ INUSE**</span><span class="sxs-lookup"><span data-stu-id="ec403-119"><span id="PHONEERR_INUSE"></span><span id="phoneerr_inuse"></span>**PHONEERR\_INUSE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ec403-120">Устройство сейчас используется.</span><span class="sxs-lookup"><span data-stu-id="ec403-120">The device is currently in use.</span></span> <span data-ttu-id="ec403-121">Не удается настроить устройство.</span><span class="sxs-lookup"><span data-stu-id="ec403-121">The device cannot be configured.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ec403-122"><span id="PHONEERR_INVALAPPHANDLE"></span><span id="phoneerr_invalapphandle"></span>**ФОНИРР \_ инвалапфандле**</span><span class="sxs-lookup"><span data-stu-id="ec403-122"><span id="PHONEERR_INVALAPPHANDLE"></span><span id="phoneerr_invalapphandle"></span>**PHONEERR\_INVALAPPHANDLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ec403-123">Указан недопустимый маркер использования или маркер регистрации приложения.</span><span class="sxs-lookup"><span data-stu-id="ec403-123">The application's specified usage handle or registration handle is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ec403-124"><span id="PHONEERR_INVALAPPNAME"></span><span id="phoneerr_invalappname"></span>**ФОНИРР \_ инвалаппнаме**</span><span class="sxs-lookup"><span data-stu-id="ec403-124"><span id="PHONEERR_INVALAPPNAME"></span><span id="phoneerr_invalappname"></span>**PHONEERR\_INVALAPPNAME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ec403-125">Указано недопустимое имя приложения.</span><span class="sxs-lookup"><span data-stu-id="ec403-125">The specified application name is invalid.</span></span> <span data-ttu-id="ec403-126">Если имя приложения задано приложением, предполагается, что строка не содержит **какие-либо** неотображаемые символы и завершается нулем.</span><span class="sxs-lookup"><span data-stu-id="ec403-126">If an application name is specified by the application, it is assumed that the string does not contain any nondisplayable characters and is **NULL**-terminated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ec403-127"><span id="PHONEERR_INVALBUTTONLAMPID"></span><span id="phoneerr_invalbuttonlampid"></span>**ФОНИРР \_ инвалбуттонлампид**</span><span class="sxs-lookup"><span data-stu-id="ec403-127"><span id="PHONEERR_INVALBUTTONLAMPID"></span><span id="phoneerr_invalbuttonlampid"></span>**PHONEERR\_INVALBUTTONLAMPID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ec403-128">Указанный идентификатор кнопки или лампы выходит за пределы допустимого диапазона или недопустим.</span><span class="sxs-lookup"><span data-stu-id="ec403-128">The specified button/lamp identifier is out of range or invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ec403-129"><span id="PHONEERR_INVALBUTTONMODE"></span><span id="phoneerr_invalbuttonmode"></span>**ФОНИРР \_ инвалбуттонмоде**</span><span class="sxs-lookup"><span data-stu-id="ec403-129"><span id="PHONEERR_INVALBUTTONMODE"></span><span id="phoneerr_invalbuttonmode"></span>**PHONEERR\_INVALBUTTONMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ec403-130">Недопустимый параметр режима кнопки.</span><span class="sxs-lookup"><span data-stu-id="ec403-130">The button mode parameter is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ec403-131"><span id="PHONEERR_INVALBUTTONSTATE"></span><span id="phoneerr_invalbuttonstate"></span>**ФОНИРР \_ инвалбуттонстате**</span><span class="sxs-lookup"><span data-stu-id="ec403-131"><span id="PHONEERR_INVALBUTTONSTATE"></span><span id="phoneerr_invalbuttonstate"></span>**PHONEERR\_INVALBUTTONSTATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ec403-132">Недопустимый параметр состояния кнопки.</span><span class="sxs-lookup"><span data-stu-id="ec403-132">The button states parameter is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ec403-133"><span id="PHONEERR_INVALDATAID"></span><span id="phoneerr_invaldataid"></span>**ФОНИРР \_ инвалдатаид**</span><span class="sxs-lookup"><span data-stu-id="ec403-133"><span id="PHONEERR_INVALDATAID"></span><span id="phoneerr_invaldataid"></span>**PHONEERR\_INVALDATAID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ec403-134">Указан недопустимый идентификатор данных.</span><span class="sxs-lookup"><span data-stu-id="ec403-134">The specified data identifier is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ec403-135"><span id="PHONEERR_INVALDEVICECLASS"></span><span id="phoneerr_invaldeviceclass"></span>**ФОНИРР \_ инвалдевицекласс**</span><span class="sxs-lookup"><span data-stu-id="ec403-135"><span id="PHONEERR_INVALDEVICECLASS"></span><span id="phoneerr_invaldeviceclass"></span>**PHONEERR\_INVALDEVICECLASS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ec403-136">Указанный телефон не поддерживает указанный класс устройств.</span><span class="sxs-lookup"><span data-stu-id="ec403-136">The specified phone does not support the indicated device class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ec403-137"><span id="PHONEERR_INVALEXTVERSION"></span><span id="phoneerr_invalextversion"></span>**ФОНИРР \_ инвалекстверсион**</span><span class="sxs-lookup"><span data-stu-id="ec403-137"><span id="PHONEERR_INVALEXTVERSION"></span><span id="phoneerr_invalextversion"></span>**PHONEERR\_INVALEXTVERSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ec403-138">Недопустимый номер версии расширения поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="ec403-138">The service provider extension version number is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ec403-139"><span id="PHONEERR_INVALHOOKSWITCHDEV"></span><span id="phoneerr_invalhookswitchdev"></span>**ФОНИРР \_ инвалхуксвитчдев**</span><span class="sxs-lookup"><span data-stu-id="ec403-139"><span id="PHONEERR_INVALHOOKSWITCHDEV"></span><span id="phoneerr_invalhookswitchdev"></span>**PHONEERR\_INVALHOOKSWITCHDEV**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ec403-140">Недопустимый параметр устройства хуксвитч.</span><span class="sxs-lookup"><span data-stu-id="ec403-140">The hookswitch device parameter is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ec403-141"><span id="PHONEERR_INVALHOOKSWITCHMODE"></span><span id="phoneerr_invalhookswitchmode"></span>**ФОНИРР \_ инвалхуксвитчмоде**</span><span class="sxs-lookup"><span data-stu-id="ec403-141"><span id="PHONEERR_INVALHOOKSWITCHMODE"></span><span id="phoneerr_invalhookswitchmode"></span>**PHONEERR\_INVALHOOKSWITCHMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ec403-142">Недопустимый параметр режима хуксвитч.</span><span class="sxs-lookup"><span data-stu-id="ec403-142">The hookswitch mode parameter is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ec403-143"><span id="PHONEERR_INVALLAMPMODE"></span><span id="phoneerr_invallampmode"></span>**ФОНИРР \_ инваллампмоде**</span><span class="sxs-lookup"><span data-stu-id="ec403-143"><span id="PHONEERR_INVALLAMPMODE"></span><span id="phoneerr_invallampmode"></span>**PHONEERR\_INVALLAMPMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ec403-144">Указан недопустимый параметр режима лампы.</span><span class="sxs-lookup"><span data-stu-id="ec403-144">The specified lamp mode parameter is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ec403-145"><span id="PHONEERR_INVALPARAM"></span><span id="phoneerr_invalparam"></span>**ФОНИРР \_ инвалпарам**</span><span class="sxs-lookup"><span data-stu-id="ec403-145"><span id="PHONEERR_INVALPARAM"></span><span id="phoneerr_invalparam"></span>**PHONEERR\_INVALPARAM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ec403-146">Параметр, например значение строки или столбца или маркер окна, является недопустимым или выходит за пределы допустимого диапазона.</span><span class="sxs-lookup"><span data-stu-id="ec403-146">A parameter, such as a row or column value or a window handle, is invalid or out of range.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ec403-147"><span id="PHONEERR_INVALPHONEHANDLE"></span><span id="phoneerr_invalphonehandle"></span>**ФОНИРР \_ инвалфонехандле**</span><span class="sxs-lookup"><span data-stu-id="ec403-147"><span id="PHONEERR_INVALPHONEHANDLE"></span><span id="phoneerr_invalphonehandle"></span>**PHONEERR\_INVALPHONEHANDLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ec403-148">Указан недопустимый маркер устройства.</span><span class="sxs-lookup"><span data-stu-id="ec403-148">The specified device handle is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ec403-149"><span id="PHONEERR_INVALPHONESTATE"></span><span id="phoneerr_invalphonestate"></span>**ФОНИРР \_ инвалфонестате**</span><span class="sxs-lookup"><span data-stu-id="ec403-149"><span id="PHONEERR_INVALPHONESTATE"></span><span id="phoneerr_invalphonestate"></span>**PHONEERR\_INVALPHONESTATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ec403-150">Телефонное устройство находится в недопустимом состоянии для запрошенной операции.</span><span class="sxs-lookup"><span data-stu-id="ec403-150">The phone device is not in a valid state for the requested operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ec403-151"><span id="PHONEERR_INVALPOINTER"></span><span id="phoneerr_invalpointer"></span>**ФОНИРР \_ инвалпоинтер**</span><span class="sxs-lookup"><span data-stu-id="ec403-151"><span id="PHONEERR_INVALPOINTER"></span><span id="phoneerr_invalpointer"></span>**PHONEERR\_INVALPOINTER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ec403-152">Один или несколько указанных параметров указателя недопустимы.</span><span class="sxs-lookup"><span data-stu-id="ec403-152">One or more of the specified pointer parameters are invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ec403-153"><span id="PHONEERR_INVALPRIVILEGE"></span><span id="phoneerr_invalprivilege"></span>**ФОНИРР \_ инвалпривилеже**</span><span class="sxs-lookup"><span data-stu-id="ec403-153"><span id="PHONEERR_INVALPRIVILEGE"></span><span id="phoneerr_invalprivilege"></span>**PHONEERR\_INVALPRIVILEGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ec403-154">Недопустимый параметр *двпривилеже* .</span><span class="sxs-lookup"><span data-stu-id="ec403-154">The *dwPrivilege* parameter is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ec403-155"><span id="PHONEERR_INVALRINGMODE"></span><span id="phoneerr_invalringmode"></span>**ФОНИРР \_ инвалрингмоде**</span><span class="sxs-lookup"><span data-stu-id="ec403-155"><span id="PHONEERR_INVALRINGMODE"></span><span id="phoneerr_invalringmode"></span>**PHONEERR\_INVALRINGMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ec403-156">Недопустимый параметр режима звонка.</span><span class="sxs-lookup"><span data-stu-id="ec403-156">The ring mode parameter is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ec403-157"><span id="PHONEERR_NODEVICE"></span><span id="phoneerr_nodevice"></span>**\_устройство фонирр**</span><span class="sxs-lookup"><span data-stu-id="ec403-157"><span id="PHONEERR_NODEVICE"></span><span id="phoneerr_nodevice"></span>**PHONEERR\_NODEVICE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ec403-158">Указанный идентификатор устройства, который ранее был действителен, больше не принимается, так как связанное устройство было удалено из системы с момента последней инициализации TAPI или повреждено способом, который не был обнаружен при инициализации.</span><span class="sxs-lookup"><span data-stu-id="ec403-158">The specified device identifier, which was previously valid, is no longer accepted because the associated device has been removed from the system since TAPI was last initialized or is corrupt in a way that was not detected at initialization.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ec403-159"><span id="PHONEERR_NODRIVER"></span><span id="phoneerr_nodriver"></span>**ФОНИРР \_ Drive**</span><span class="sxs-lookup"><span data-stu-id="ec403-159"><span id="PHONEERR_NODRIVER"></span><span id="phoneerr_nodriver"></span>**PHONEERR\_NODRIVER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ec403-160">Поставщик телефонной службы для указанного устройства обнаружил, что один из его компонентов отсутствует или поврежден таким образом, который не был обнаружен во время инициализации.</span><span class="sxs-lookup"><span data-stu-id="ec403-160">The telephone service provider for the specified device found that one of its components is missing or corrupt in a way that was not detected at initialization time.</span></span> <span data-ttu-id="ec403-161">Чтобы устранить проблему, пользователю рекомендуется использовать панель управления телефонии.</span><span class="sxs-lookup"><span data-stu-id="ec403-161">The user should be advised to use the Telephony Control Panel to correct the problem.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ec403-162"><span id="PHONEERR_NOMEM"></span><span id="phoneerr_nomem"></span>**ФОНИРР \_ номем**</span><span class="sxs-lookup"><span data-stu-id="ec403-162"><span id="PHONEERR_NOMEM"></span><span id="phoneerr_nomem"></span>**PHONEERR\_NOMEM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ec403-163">Недостаточно памяти для завершения запрошенной операции или не удается выделить или заблокировать память.</span><span class="sxs-lookup"><span data-stu-id="ec403-163">Insufficient memory to complete the requested operation, or unable to allocate or lock memory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ec403-164"><span id="PHONEERR_NOTOWNER"></span><span id="phoneerr_notowner"></span>**ФОНИРР \_**</span><span class="sxs-lookup"><span data-stu-id="ec403-164"><span id="PHONEERR_NOTOWNER"></span><span id="phoneerr_notowner"></span>**PHONEERR\_NOTOWNER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ec403-165">Приложение не имеет прав владельца для указанного телефонного устройства.</span><span class="sxs-lookup"><span data-stu-id="ec403-165">The application does not have owner privilege to the specified phone device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ec403-166"><span id="PHONEERR_OPERATIONFAILED"></span><span id="phoneerr_operationfailed"></span>**ФОНИРР \_ оператионфаилед**</span><span class="sxs-lookup"><span data-stu-id="ec403-166"><span id="PHONEERR_OPERATIONFAILED"></span><span id="phoneerr_operationfailed"></span>**PHONEERR\_OPERATIONFAILED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ec403-167">Не удалось выполнить операцию по неизвестной причине.</span><span class="sxs-lookup"><span data-stu-id="ec403-167">The operation failed for an unspecified reason.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ec403-168"><span id="PHONEERR_OPERATIONUNAVAIL"></span><span id="phoneerr_operationunavail"></span>**ФОНИРР \_ оператионунаваил**</span><span class="sxs-lookup"><span data-stu-id="ec403-168"><span id="PHONEERR_OPERATIONUNAVAIL"></span><span id="phoneerr_operationunavail"></span>**PHONEERR\_OPERATIONUNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ec403-169">Операция недоступна.</span><span class="sxs-lookup"><span data-stu-id="ec403-169">The operation is not available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ec403-170"><span id="PHONEERR_REINIT"></span><span id="phoneerr_reinit"></span>**ФОНИРР \_ REinit**</span><span class="sxs-lookup"><span data-stu-id="ec403-170"><span id="PHONEERR_REINIT"></span><span id="phoneerr_reinit"></span>**PHONEERR\_REINIT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ec403-171">Если была запрошена повторная инициализация TAPI, например в результате добавления или удаления поставщика услуг телефонии, то запросы [**фонеинитиализе**](/windows/desktop/api/Tapi/nf-tapi-phoneinitialize), [**фонеинитиализикс**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa) или [**фонеопен**](/windows/desktop/api/Tapi/nf-tapi-phoneopen) отклоняются с этой ошибкой до тех пор, пока Последнее приложение не завершит использование API (с помощью [**фонешутдовн**](/windows/desktop/api/Tapi/nf-tapi-phoneshutdown)), когда новая конфигурация вступит в силу и приложения снова смогут вызвать **фонеинитиализе** или **фонеинитиализикс**.</span><span class="sxs-lookup"><span data-stu-id="ec403-171">If TAPI reinitialization has been requested, for example as a result of adding or removing a telephony service provider, then [**phoneInitialize**](/windows/desktop/api/Tapi/nf-tapi-phoneinitialize), [**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa) or [**phoneOpen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen) requests are rejected with this error until the last application shuts down its usage of the API (using [**phoneShutdown**](/windows/desktop/api/Tapi/nf-tapi-phoneshutdown)), at which time the new configuration becomes effective and applications are once again permitted to call **phoneInitialize** or **phoneInitializeEx**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ec403-172"><span id="PHONEERR_REQUESTOVERRUN"></span><span id="phoneerr_requestoverrun"></span>**ФОНИРР \_ рекуестоверрун**</span><span class="sxs-lookup"><span data-stu-id="ec403-172"><span id="PHONEERR_REQUESTOVERRUN"></span><span id="phoneerr_requestoverrun"></span>**PHONEERR\_REQUESTOVERRUN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ec403-173">Превышено максимальное число невыполненных телефонных запросов.</span><span class="sxs-lookup"><span data-stu-id="ec403-173">The maximum number of outstanding phone requests has been exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ec403-174"><span id="PHONEERR_RESOURCEUNAVAIL"></span><span id="phoneerr_resourceunavail"></span>**ФОНИРР \_ ресаурцеунаваил**</span><span class="sxs-lookup"><span data-stu-id="ec403-174"><span id="PHONEERR_RESOURCEUNAVAIL"></span><span id="phoneerr_resourceunavail"></span>**PHONEERR\_RESOURCEUNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ec403-175">Невозможно завершить операцию из-за перерасхода ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ec403-175">The operation cannot be completed because of resource overcommitment.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ec403-176"><span id="PHONEERR_STRUCTURETOOSMALL"></span><span id="phoneerr_structuretoosmall"></span>**ФОНИРР \_ структуретусмалл**</span><span class="sxs-lookup"><span data-stu-id="ec403-176"><span id="PHONEERR_STRUCTURETOOSMALL"></span><span id="phoneerr_structuretoosmall"></span>**PHONEERR\_STRUCTURETOOSMALL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ec403-177">Указана слишком маленькая структура телефонных заглавных букв.</span><span class="sxs-lookup"><span data-stu-id="ec403-177">The specified phone caps structure is too small.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ec403-178"><span id="PHONEERR_UNINITIALIZED"></span><span id="phoneerr_uninitialized"></span>**ФОНИРР не \_ инициализирован**</span><span class="sxs-lookup"><span data-stu-id="ec403-178"><span id="PHONEERR_UNINITIALIZED"></span><span id="phoneerr_uninitialized"></span>**PHONEERR\_UNINITIALIZED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ec403-179">Операция была вызвана до любого приложения с именем [**фонеинитиализе**](/windows/desktop/api/Tapi/nf-tapi-phoneinitialize), [**фонеинитиализикс**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa).</span><span class="sxs-lookup"><span data-stu-id="ec403-179">The operation was invoked before any application called [**phoneInitialize**](/windows/desktop/api/Tapi/nf-tapi-phoneinitialize), [**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa).</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ec403-180">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ec403-180">Remarks</span></span>

<span data-ttu-id="ec403-181">Значения 0xC0000000 до 0xFFFFFFFF доступны для расширений устройств. значения от 0x80000000 до 0xBFFFFFFF зарезервированы; и 0x00000000 – 0x7FFFFFFF используются в качестве идентификаторов запросов.</span><span class="sxs-lookup"><span data-stu-id="ec403-181">The values 0xC0000000 through 0xFFFFFFFF are available for device-specific extensions; the values 0x80000000 through 0xBFFFFFFF are reserved; and 0x00000000 through 0x7FFFFFFF are used as request identifiers.</span></span>

<span data-ttu-id="ec403-182">Если приложение получает сообщение об ошибке, возвращающее, что оно не обрабатывается специально (например, сообщение об ошибке, определенное расширением конкретного устройства), оно должно рассматривать ошибку как ФОНИРР \_ оператионфаилед (по неизвестной причине).</span><span class="sxs-lookup"><span data-stu-id="ec403-182">If an application gets an error return that it does not specifically handle (such as an error defined by a device-specific extension), it should treat the error as a PHONEERR\_OPERATIONFAILED (for an unspecified reason).</span></span>

## <a name="requirements"></a><span data-ttu-id="ec403-183">Требования</span><span class="sxs-lookup"><span data-stu-id="ec403-183">Requirements</span></span>



| <span data-ttu-id="ec403-184">Требование</span><span class="sxs-lookup"><span data-stu-id="ec403-184">Requirement</span></span> | <span data-ttu-id="ec403-185">Значение</span><span class="sxs-lookup"><span data-stu-id="ec403-185">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="ec403-186">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="ec403-186">TAPI version</span></span><br/> | <span data-ttu-id="ec403-187">Требуется TAPI 2,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="ec403-187">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="ec403-188">Header</span><span class="sxs-lookup"><span data-stu-id="ec403-188">Header</span></span><br/>       | <dl> <span data-ttu-id="ec403-189"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="ec403-189"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec403-190">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ec403-190">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec403-191">**фонеинитиализе**</span><span class="sxs-lookup"><span data-stu-id="ec403-191">**phoneInitialize**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneinitialize)
</dt> <dt>

[<span data-ttu-id="ec403-192">**фонеинитиализикс**</span><span class="sxs-lookup"><span data-stu-id="ec403-192">**phoneInitializeEx**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa)
</dt> <dt>

[<span data-ttu-id="ec403-193">**фонеопен**</span><span class="sxs-lookup"><span data-stu-id="ec403-193">**phoneOpen**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneopen)
</dt> <dt>

[<span data-ttu-id="ec403-194">**фонешутдовн**</span><span class="sxs-lookup"><span data-stu-id="ec403-194">**phoneShutdown**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneshutdown)
</dt> </dl>

 

 




