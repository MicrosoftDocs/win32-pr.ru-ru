---
description: 'Метод IWiaDevMgr2:: Регистеревенткаллбаккпрограм регистрирует приложение для получения событий устройства. В основном он предоставляется для обеспечения обратной совместимости с приложениями, которые не были написаны для получения образа Windows (WIA) 2,0.'
ms.assetid: 6b427f19-719b-44ce-8e2c-3c44672345c8
title: 'Метод IWiaDevMgr2:: Регистеревенткаллбаккпрограм (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2.RegisterEventCallbackProgram
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 9b18b5833b7616493c24f0128caa7c910b685e37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105719368"
---
# <a name="iwiadevmgr2registereventcallbackprogram-method"></a><span data-ttu-id="9859c-104">Метод IWiaDevMgr2:: Регистеревенткаллбаккпрограм</span><span class="sxs-lookup"><span data-stu-id="9859c-104">IWiaDevMgr2::RegisterEventCallbackProgram method</span></span>

<span data-ttu-id="9859c-105">Метод **IWiaDevMgr2:: регистеревенткаллбаккпрограм** регистрирует приложение для получения событий устройства.</span><span class="sxs-lookup"><span data-stu-id="9859c-105">The **IWiaDevMgr2::RegisterEventCallbackProgram** method registers an application to receive device events.</span></span> <span data-ttu-id="9859c-106">В основном он предоставляется для обеспечения обратной совместимости с приложениями, которые не были написаны для получения образа Windows (WIA) 2,0.</span><span class="sxs-lookup"><span data-stu-id="9859c-106">It is primarily provided for backward compatibility with applications that were not written for Windows Image Acquisition (WIA) 2.0.</span></span>

## <a name="syntax"></a><span data-ttu-id="9859c-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9859c-107">Syntax</span></span>


```C++
HRESULT RegisterEventCallbackProgram(
  [in]       LONG lFlags,
  [in]       BSTR bstrDeviceID,
  [in] const GUID *pEventGUID,
  [in]       BSTR bstrFullAppName,
  [in]       BSTR bstrCommandlineArg,
  [in]       BSTR bstrName,
  [in]       BSTR bstrDescription,
  [in]       BSTR bstrIcon
);
```



## <a name="parameters"></a><span data-ttu-id="9859c-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="9859c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9859c-109">*лфлагс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9859c-109">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9859c-110">Тип: **Long**</span><span class="sxs-lookup"><span data-stu-id="9859c-110">Type: **LONG**</span></span>

<span data-ttu-id="9859c-111">Флаги регистрации.</span><span class="sxs-lookup"><span data-stu-id="9859c-111">The registration flags.</span></span> <span data-ttu-id="9859c-112">Можно задать следующие значения.</span><span class="sxs-lookup"><span data-stu-id="9859c-112">Can be set to the following values.</span></span>



| <span data-ttu-id="9859c-113">Значение</span><span class="sxs-lookup"><span data-stu-id="9859c-113">Value</span></span>                                                                                                                                                                                                           | <span data-ttu-id="9859c-114">Значение</span><span class="sxs-lookup"><span data-stu-id="9859c-114">Meaning</span></span>                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <span id="WIA_REGISTER_EVENT_CALLBACK"></span><span id="wia_register_event_callback"></span><dl> <span data-ttu-id="9859c-115"><dt>**\_ \_ обратный вызов события регистрации WIA \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9859c-115"><dt>**WIA\_REGISTER\_EVENT\_CALLBACK**</dt></span></span> </dl>       | <span data-ttu-id="9859c-116">Зарегистрируйтесь для события.</span><span class="sxs-lookup"><span data-stu-id="9859c-116">Register for the event.</span></span><br/>                           |
| <span id="WIA_UNREGISTER_EVENT_CALLBACK"></span><span id="wia_unregister_event_callback"></span><dl> <span data-ttu-id="9859c-117"><dt>**\_обратный вызов для отмены регистрации \_ события WIA \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9859c-117"><dt>**WIA\_UNREGISTER\_EVENT\_CALLBACK**</dt></span></span> </dl> | <span data-ttu-id="9859c-118">Удалите регистрацию для события.</span><span class="sxs-lookup"><span data-stu-id="9859c-118">Delete the registration for the event.</span></span><br/>            |
| <span id="WIA_SET_DEFAULT_HANDLER"></span><span id="wia_set_default_handler"></span><dl> <span data-ttu-id="9859c-119"><dt>**\_ \_ обработчик по умолчанию для WIA Set \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9859c-119"><dt>**WIA\_SET\_DEFAULT\_HANDLER**</dt></span></span> </dl>                   | <span data-ttu-id="9859c-120">Задайте приложение в качестве обработчика событий по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="9859c-120">Set the application as the default event handler.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="9859c-121">*бстрдевицеид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9859c-121">*bstrDeviceID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9859c-122">Тип: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="9859c-122">Type: **BSTR**</span></span>

<span data-ttu-id="9859c-123">Идентификатор устройства.</span><span class="sxs-lookup"><span data-stu-id="9859c-123">A device identifier.</span></span> <span data-ttu-id="9859c-124">Передайте **значение NULL** , чтобы зарегистрировать событие на всех устройствах WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="9859c-124">Pass **NULL** to register for the event on all WIA 2.0 devices.</span></span>

</dd> <dt>

<span data-ttu-id="9859c-125">*певентгуид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9859c-125">*pEventGUID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9859c-126">Тип: \**константа \* GUID* _</span><span class="sxs-lookup"><span data-stu-id="9859c-126">Type: \**const GUID\** _</span></span>

<span data-ttu-id="9859c-127">Событие, для которого регистрируется приложение.</span><span class="sxs-lookup"><span data-stu-id="9859c-127">The event that the application is registering for.</span></span> <span data-ttu-id="9859c-128">Список допустимых идентификаторов GUID событий см. в разделе [идентификаторы событий WIA](-wia-wia-event-identifiers.md).</span><span class="sxs-lookup"><span data-stu-id="9859c-128">For a list of valid event GUIDs, see [WIA Event Identifiers](-wia-wia-event-identifiers.md).</span></span>

</dd> <dt>

<span data-ttu-id="9859c-129">_bstrFullAppName \* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="9859c-129">_bstrFullAppName\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9859c-130">Тип: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="9859c-130">Type: **BSTR**</span></span>

<span data-ttu-id="9859c-131">Полное имя пути приложения.</span><span class="sxs-lookup"><span data-stu-id="9859c-131">The full path name of the application.</span></span>

</dd> <dt>

<span data-ttu-id="9859c-132">*бстркоммандлинеарг* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9859c-132">*bstrCommandlineArg* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9859c-133">Тип: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="9859c-133">Type: **BSTR**</span></span>

<span data-ttu-id="9859c-134">Соответствующие аргументы командной строки для приложения.</span><span class="sxs-lookup"><span data-stu-id="9859c-134">The appropriate command-line arguments for the application.</span></span>

</dd> <dt>

<span data-ttu-id="9859c-135">*bstrName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9859c-135">*bstrName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9859c-136">Тип: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="9859c-136">Type: **BSTR**</span></span>

<span data-ttu-id="9859c-137">Имя приложения.</span><span class="sxs-lookup"><span data-stu-id="9859c-137">The name of the application.</span></span> <span data-ttu-id="9859c-138">Имя отображается пользователю, когда несколько приложений регистрируются для одного и того же события.</span><span class="sxs-lookup"><span data-stu-id="9859c-138">The name is displayed to the user when multiple applications register for the same event.</span></span>

</dd> <dt>

<span data-ttu-id="9859c-139">*bstrDescription* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9859c-139">*bstrDescription* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9859c-140">Тип: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="9859c-140">Type: **BSTR**</span></span>

<span data-ttu-id="9859c-141">Описание приложения.</span><span class="sxs-lookup"><span data-stu-id="9859c-141">The description of the application.</span></span> <span data-ttu-id="9859c-142">Описание отображается пользователю, когда несколько приложений регистрируются для одного и того же события.</span><span class="sxs-lookup"><span data-stu-id="9859c-142">The description is displayed to the user when multiple applications register for the same event.</span></span>

</dd> <dt>

<span data-ttu-id="9859c-143">*бстрикон* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9859c-143">*bstrIcon* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9859c-144">Тип: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="9859c-144">Type: **BSTR**</span></span>

<span data-ttu-id="9859c-145">Значок, представляющий приложение.</span><span class="sxs-lookup"><span data-stu-id="9859c-145">The icon that represents the application.</span></span> <span data-ttu-id="9859c-146">Этот значок отображается пользователю, когда несколько приложений регистрируются для одного и того же события.</span><span class="sxs-lookup"><span data-stu-id="9859c-146">The icon is displayed to the user when multiple applications register for the same event.</span></span> <span data-ttu-id="9859c-147">Строка содержит имя приложения и Отсчитываемый от нуля индекс значка, разделенный запятыми, например MyApp, 0.</span><span class="sxs-lookup"><span data-stu-id="9859c-147">The string contains the name of the application and the zero-based index of the icon separated by a comma, for example, "MyApp, 0".</span></span> <span data-ttu-id="9859c-148">Может быть несколько значков, представляющих приложение.</span><span class="sxs-lookup"><span data-stu-id="9859c-148">There might be more than one icon that represents an application.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9859c-149">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9859c-149">Return value</span></span>

<span data-ttu-id="9859c-150">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="9859c-150">Type: **HRESULT**</span></span>

<span data-ttu-id="9859c-151">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="9859c-151">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9859c-152">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9859c-152">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="9859c-153">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9859c-153">Remarks</span></span>

<span data-ttu-id="9859c-154">Используйте **IWiaDevMgr2:: регистеревенткаллбаккпрограм** для регистрации событий аппаратного устройства.</span><span class="sxs-lookup"><span data-stu-id="9859c-154">Use **IWiaDevMgr2::RegisterEventCallbackProgram** to register for hardware device events.</span></span> <span data-ttu-id="9859c-155">При возникновении события, для которого зарегистрировано приложение, запускается приложение, а сведения о событии передаются в приложение.</span><span class="sxs-lookup"><span data-stu-id="9859c-155">When an event occurs that an application is registered for, the application is launched, and the event information is transmitted to the application.</span></span>

<span data-ttu-id="9859c-156">Используйте метод [**енумрегистеревентинфо**](-wia-iwiaitem2-enumregistereventinfo.md) для получения указателя на объект перечислителя для свойств регистрации событий.</span><span class="sxs-lookup"><span data-stu-id="9859c-156">Use the [**EnumRegisterEventInfo**](-wia-iwiaitem2-enumregistereventinfo.md) method to retrieve a pointer to an enumerator object for event registration properties.</span></span>

<span data-ttu-id="9859c-157">Используйте метод **IWiaDevMgr2:: регистеревенткаллбаккпрограм** для обеспечения обратной совместимости с приложениями, не написанными для архитектуры WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="9859c-157">Only use the **IWiaDevMgr2::RegisterEventCallbackProgram** method for backward compatibility with applications not written for the WIA 2.0 architecture.</span></span> <span data-ttu-id="9859c-158">Используйте интерфейсы модели COM, предоставляемые архитектурой WIA 2,0 для новых приложений.</span><span class="sxs-lookup"><span data-stu-id="9859c-158">Use the Component Object Model (COM) interfaces provided by the WIA 2.0 architecture for new applications.</span></span> <span data-ttu-id="9859c-159">В частности, вызовите [**IWiaDevMgr2:: регистеревенткаллбаккинтерфаце**](-wia-iwiadevmgr2-registereventcallbackinterface.md) или [**IWiaDevMgr2:: регистеревенткаллбаккклсид**](-wia-iwiadevmgr2-registereventcallbackclsid.md) , чтобы зарегистрировать новое приложение для событий устройства.</span><span class="sxs-lookup"><span data-stu-id="9859c-159">Specifically, call [**IWiaDevMgr2::RegisterEventCallbackInterface**](-wia-iwiadevmgr2-registereventcallbackinterface.md) or [**IWiaDevMgr2::RegisterEventCallbackCLSID**](-wia-iwiadevmgr2-registereventcallbackclsid.md) to register a new application for device events.</span></span>

<span data-ttu-id="9859c-160">Как правило, этот метод вызывается программой установки или сценарием.</span><span class="sxs-lookup"><span data-stu-id="9859c-160">Typically, this method is called by an install program or a script.</span></span> <span data-ttu-id="9859c-161">Программа установки или сценарий регистрирует приложение для получения событий устройства WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="9859c-161">The install program or script registers the application to receive WIA 2.0 device events.</span></span> <span data-ttu-id="9859c-162">Когда происходит это событие, приложение запускается с помощью системы времени выполнения WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="9859c-162">When the event occurs, the application is started by the WIA 2.0 run-time system.</span></span>

## <a name="requirements"></a><span data-ttu-id="9859c-163">Требования</span><span class="sxs-lookup"><span data-stu-id="9859c-163">Requirements</span></span>



| <span data-ttu-id="9859c-164">Требование</span><span class="sxs-lookup"><span data-stu-id="9859c-164">Requirement</span></span> | <span data-ttu-id="9859c-165">Значение</span><span class="sxs-lookup"><span data-stu-id="9859c-165">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="9859c-166">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9859c-166">Minimum supported client</span></span><br/> | <span data-ttu-id="9859c-167">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9859c-167">Windows Vista \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="9859c-168">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9859c-168">Minimum supported server</span></span><br/> | <span data-ttu-id="9859c-169">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9859c-169">Windows Server 2008 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="9859c-170">Header</span><span class="sxs-lookup"><span data-stu-id="9859c-170">Header</span></span><br/>                   | <dl> <span data-ttu-id="9859c-171"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="9859c-171"><dt>Wia.h</dt></span></span> </dl> |



 

 




