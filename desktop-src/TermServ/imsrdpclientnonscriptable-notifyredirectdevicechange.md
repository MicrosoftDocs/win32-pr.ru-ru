---
title: Имсрдпклиентнонскриптабле Нотифиредиректдевицечанже, метод
description: Уведомляет модуль перенаправления устройств элемента управления ActiveX удаленный рабочий стол, что в системе произошло изменение устройства. Этот метод передает в \_ элемент управления уведомления WM девицечанже.
ms.assetid: 36323831-06e0-4e47-8a6c-06367119298f
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Нотифиредиректдевицечанже
- Службы удаленных рабочих столов метода Нотифиредиректдевицечанже, интерфейс Имсрдпклиентнонскриптабле
- Службы удаленных рабочих столов интерфейса Имсрдпклиентнонскриптабле, метод Нотифиредиректдевицечанже
- Службы удаленных рабочих столов метода Нотифиредиректдевицечанже, интерфейс IMsRdpClientNonScriptable2
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable2, метод Нотифиредиректдевицечанже
- Службы удаленных рабочих столов метода Нотифиредиректдевицечанже, интерфейс IMsRdpClientNonScriptable3
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable3, метод Нотифиредиректдевицечанже
- Службы удаленных рабочих столов метода Нотифиредиректдевицечанже, интерфейс IMsRdpClientNonScriptable4
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable4, метод Нотифиредиректдевицечанже
- Службы удаленных рабочих столов метода Нотифиредиректдевицечанже, интерфейс IMsRdpClientNonScriptable5
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable5, метод Нотифиредиректдевицечанже
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable.NotifyRedirectDeviceChange
- IMsRdpClientNonScriptable2.NotifyRedirectDeviceChange
- IMsRdpClientNonScriptable3.NotifyRedirectDeviceChange
- IMsRdpClientNonScriptable4.NotifyRedirectDeviceChange
- IMsRdpClientNonScriptable5.NotifyRedirectDeviceChange
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7357fcb5e31eeeb0de5791425b8d9fada4365ab8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989318"
---
# <a name="imsrdpclientnonscriptablenotifyredirectdevicechange-method"></a><span data-ttu-id="74b6f-115">Метод Имсрдпклиентнонскриптабле:: Нотифиредиректдевицечанже</span><span class="sxs-lookup"><span data-stu-id="74b6f-115">IMsRdpClientNonScriptable::NotifyRedirectDeviceChange method</span></span>

<span data-ttu-id="74b6f-116">Уведомляет модуль перенаправления устройств элемента управления ActiveX удаленный рабочий стол, что в системе произошло изменение устройства.</span><span class="sxs-lookup"><span data-stu-id="74b6f-116">Notifies the device redirection module of the Remote Desktop ActiveX control that a device change has occurred on the system.</span></span> <span data-ttu-id="74b6f-117">Этот метод передает в элемент управления уведомления [**WM \_ девицечанже**](/windows/desktop/DevIO/wm-devicechange) .</span><span class="sxs-lookup"><span data-stu-id="74b6f-117">This method passes [**WM\_DEVICECHANGE**](/windows/desktop/DevIO/wm-devicechange) notifications to the control.</span></span>

## <a name="syntax"></a><span data-ttu-id="74b6f-118">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="74b6f-118">Syntax</span></span>


```C++
HRESULT NotifyRedirectDeviceChange(
  [in] WPARAM wParam,
  [in] LPARAM lParam
);
```



## <a name="parameters"></a><span data-ttu-id="74b6f-119">Параметры</span><span class="sxs-lookup"><span data-stu-id="74b6f-119">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74b6f-120">*wParam* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="74b6f-120">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74b6f-121">Указывает событие устройства.</span><span class="sxs-lookup"><span data-stu-id="74b6f-121">Specifies the device event.</span></span> <span data-ttu-id="74b6f-122">Этот параметр может принимать одно из указанных ниже значений.</span><span class="sxs-lookup"><span data-stu-id="74b6f-122">This parameter can be one of the following values.</span></span>

<dt>

<span id="DBT_CONFIGCHANGECANCELED"></span><span id="dbt_configchangecanceled"></span>

<span data-ttu-id="74b6f-123"><span id="DBT_CONFIGCHANGECANCELED"></span><span id="dbt_configchangecanceled"></span>**ДБТ \_ конфигчанжеканцелед**</span><span class="sxs-lookup"><span data-stu-id="74b6f-123"><span id="DBT_CONFIGCHANGECANCELED"></span><span id="dbt_configchangecanceled"></span>**DBT\_CONFIGCHANGECANCELED**</span></span>


</dt> <dd>

<span data-ttu-id="74b6f-124">Запрос на изменение текущей конфигурации (закрепления или отстыковки) отменен.</span><span class="sxs-lookup"><span data-stu-id="74b6f-124">A request to change the current configuration (dock or undock) has been canceled.</span></span>

</dd> <dt>

<span id="DBT_CONFIGCHANGED"></span><span id="dbt_configchanged"></span>

<span data-ttu-id="74b6f-125"><span id="DBT_CONFIGCHANGED"></span><span id="dbt_configchanged"></span>**ДБТ \_ конфигчанжед**</span><span class="sxs-lookup"><span data-stu-id="74b6f-125"><span id="DBT_CONFIGCHANGED"></span><span id="dbt_configchanged"></span>**DBT\_CONFIGCHANGED**</span></span>


</dt> <dd>

<span data-ttu-id="74b6f-126">Текущая конфигурация изменилась из-за закрепления или открепления.</span><span class="sxs-lookup"><span data-stu-id="74b6f-126">The current configuration has changed due to a dock or undock.</span></span>

</dd> <dt>

<span id="DBT_CUSTOMEVENT"></span><span id="dbt_customevent"></span>

<span data-ttu-id="74b6f-127"><span id="DBT_CUSTOMEVENT"></span><span id="dbt_customevent"></span>**ДБТ \_ CUSTOMEVENT**</span><span class="sxs-lookup"><span data-stu-id="74b6f-127"><span id="DBT_CUSTOMEVENT"></span><span id="dbt_customevent"></span>**DBT\_CUSTOMEVENT**</span></span>


</dt> <dd>

<span data-ttu-id="74b6f-128">Произошло пользовательское событие.</span><span class="sxs-lookup"><span data-stu-id="74b6f-128">A custom event has occurred.</span></span>

</dd> <dt>

<span id="DBT_DEVICEARRIVAL"></span><span id="dbt_devicearrival"></span>

<span data-ttu-id="74b6f-129"><span id="DBT_DEVICEARRIVAL"></span><span id="dbt_devicearrival"></span>**ДБТ \_ девицеарривал**</span><span class="sxs-lookup"><span data-stu-id="74b6f-129"><span id="DBT_DEVICEARRIVAL"></span><span id="dbt_devicearrival"></span>**DBT\_DEVICEARRIVAL**</span></span>


</dt> <dd>

<span data-ttu-id="74b6f-130">Устройство было вставлено и теперь доступно.</span><span class="sxs-lookup"><span data-stu-id="74b6f-130">A device has been inserted and is now available.</span></span>

</dd> <dt>

<span id="DBT_DEVICEQUERYREMOVE"></span><span id="dbt_devicequeryremove"></span>

<span data-ttu-id="74b6f-131"><span id="DBT_DEVICEQUERYREMOVE"></span><span id="dbt_devicequeryremove"></span>**ДБТ \_ девицекуериремове**</span><span class="sxs-lookup"><span data-stu-id="74b6f-131"><span id="DBT_DEVICEQUERYREMOVE"></span><span id="dbt_devicequeryremove"></span>**DBT\_DEVICEQUERYREMOVE**</span></span>


</dt> <dd>

<span data-ttu-id="74b6f-132">Запрошено разрешение на удаление устройства.</span><span class="sxs-lookup"><span data-stu-id="74b6f-132">Permission is requested to remove a device.</span></span> <span data-ttu-id="74b6f-133">Любое приложение может отклонить этот запрос и отменить удаление.</span><span class="sxs-lookup"><span data-stu-id="74b6f-133">Any application can deny this request and cancel the removal.</span></span>

</dd> <dt>

<span id="DBT_DEVICEQUERYREMOVEFAILED"></span><span id="dbt_devicequeryremovefailed"></span>

<span data-ttu-id="74b6f-134"><span id="DBT_DEVICEQUERYREMOVEFAILED"></span><span id="dbt_devicequeryremovefailed"></span>**ДБТ \_ девицекуериремовефаилед**</span><span class="sxs-lookup"><span data-stu-id="74b6f-134"><span id="DBT_DEVICEQUERYREMOVEFAILED"></span><span id="dbt_devicequeryremovefailed"></span>**DBT\_DEVICEQUERYREMOVEFAILED**</span></span>


</dt> <dd>

<span data-ttu-id="74b6f-135">Запрос на удаление устройства отменен.</span><span class="sxs-lookup"><span data-stu-id="74b6f-135">A request to remove a device has been canceled.</span></span>

</dd> <dt>

<span id="DBT_DEVICEREMOVECOMPLETE"></span><span id="dbt_deviceremovecomplete"></span>

<span data-ttu-id="74b6f-136"><span id="DBT_DEVICEREMOVECOMPLETE"></span><span id="dbt_deviceremovecomplete"></span>**ДБТ \_ девицеремовекомплете**</span><span class="sxs-lookup"><span data-stu-id="74b6f-136"><span id="DBT_DEVICEREMOVECOMPLETE"></span><span id="dbt_deviceremovecomplete"></span>**DBT\_DEVICEREMOVECOMPLETE**</span></span>


</dt> <dd>

<span data-ttu-id="74b6f-137">Устройство удалено.</span><span class="sxs-lookup"><span data-stu-id="74b6f-137">A device has been removed.</span></span>

</dd> <dt>

<span id="DBT_DEVICEREMOVEPENDING"></span><span id="dbt_deviceremovepending"></span>

<span data-ttu-id="74b6f-138"><span id="DBT_DEVICEREMOVEPENDING"></span><span id="dbt_deviceremovepending"></span>**ДБТ \_ девицеремовепендинг**</span><span class="sxs-lookup"><span data-stu-id="74b6f-138"><span id="DBT_DEVICEREMOVEPENDING"></span><span id="dbt_deviceremovepending"></span>**DBT\_DEVICEREMOVEPENDING**</span></span>


</dt> <dd>

<span data-ttu-id="74b6f-139">Устройство будет удалено.</span><span class="sxs-lookup"><span data-stu-id="74b6f-139">A device is about to be removed.</span></span> <span data-ttu-id="74b6f-140">Удаление не может быть запрещено.</span><span class="sxs-lookup"><span data-stu-id="74b6f-140">The removal cannot be denied.</span></span>

</dd> <dt>

<span id="DBT_DEVICETYPESPECIFIC"></span><span id="dbt_devicetypespecific"></span>

<span data-ttu-id="74b6f-141"><span id="DBT_DEVICETYPESPECIFIC"></span><span id="dbt_devicetypespecific"></span>**ДБТ \_ девицетипеспеЦифик**</span><span class="sxs-lookup"><span data-stu-id="74b6f-141"><span id="DBT_DEVICETYPESPECIFIC"></span><span id="dbt_devicetypespecific"></span>**DBT\_DEVICETYPESPECIFIC**</span></span>


</dt> <dd>

<span data-ttu-id="74b6f-142">Произошло событие для конкретного устройства.</span><span class="sxs-lookup"><span data-stu-id="74b6f-142">A device-specific event has occurred.</span></span>

</dd> <dt>

<span id="DBT_DEVNODES_CHANGED"></span><span id="dbt_devnodes_changed"></span>

<span data-ttu-id="74b6f-143"><span id="DBT_DEVNODES_CHANGED"></span><span id="dbt_devnodes_changed"></span>**ДБТ \_ девнодес \_ изменен**</span><span class="sxs-lookup"><span data-stu-id="74b6f-143"><span id="DBT_DEVNODES_CHANGED"></span><span id="dbt_devnodes_changed"></span>**DBT\_DEVNODES\_CHANGED**</span></span>


</dt> <dd>

<span data-ttu-id="74b6f-144">Устройство было добавлено в систему или удалено из нее.</span><span class="sxs-lookup"><span data-stu-id="74b6f-144">A device has been added to or removed from the system.</span></span>

</dd> <dt>

<span id="DBT_QUERYCHANGECONFIG"></span><span id="dbt_querychangeconfig"></span>

<span data-ttu-id="74b6f-145"><span id="DBT_QUERYCHANGECONFIG"></span><span id="dbt_querychangeconfig"></span>**ДБТ \_ куеричанжеконфиг**</span><span class="sxs-lookup"><span data-stu-id="74b6f-145"><span id="DBT_QUERYCHANGECONFIG"></span><span id="dbt_querychangeconfig"></span>**DBT\_QUERYCHANGECONFIG**</span></span>


</dt> <dd>

<span data-ttu-id="74b6f-146">Запрошено разрешение на изменение текущей конфигурации (закрепление или Отстыковка).</span><span class="sxs-lookup"><span data-stu-id="74b6f-146">Permission is requested to change the current configuration (dock or undock).</span></span>

</dd> <dt>

<span id="DBT_USERDEFINED"></span><span id="dbt_userdefined"></span>

<span data-ttu-id="74b6f-147"><span id="DBT_USERDEFINED"></span><span id="dbt_userdefined"></span>**ДБТ \_ пользователяопределенные**</span><span class="sxs-lookup"><span data-stu-id="74b6f-147"><span id="DBT_USERDEFINED"></span><span id="dbt_userdefined"></span>**DBT\_USERDEFINED**</span></span>


</dt> <dd>

<span data-ttu-id="74b6f-148">Значение этого сообщения определяется пользователем.</span><span class="sxs-lookup"><span data-stu-id="74b6f-148">The meaning of this message is user-defined.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="74b6f-149">*lParam* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="74b6f-149">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74b6f-150">Указатель на структуру, содержащую данные, относящиеся к конкретному событию.</span><span class="sxs-lookup"><span data-stu-id="74b6f-150">Pointer to a structure that contains event-specific data.</span></span> <span data-ttu-id="74b6f-151">Его формат зависит от значения параметра *wParam* .</span><span class="sxs-lookup"><span data-stu-id="74b6f-151">Its format depends on the value of the *wParam* parameter.</span></span> <span data-ttu-id="74b6f-152">Дополнительные сведения см. в документации по каждому событию.</span><span class="sxs-lookup"><span data-stu-id="74b6f-152">For more information, refer to the documentation for each event.</span></span> <span data-ttu-id="74b6f-153">Дополнительные сведения см. в разделе [типы событий устройства](/windows/desktop/DevIO/device-event-types).</span><span class="sxs-lookup"><span data-stu-id="74b6f-153">For more information, see [Device Event Types](/windows/desktop/DevIO/device-event-types).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74b6f-154">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="74b6f-154">Return value</span></span>

<span data-ttu-id="74b6f-155">В случае успеха возвратите значение **\_ ОК** .</span><span class="sxs-lookup"><span data-stu-id="74b6f-155">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="74b6f-156">Комментарии</span><span class="sxs-lookup"><span data-stu-id="74b6f-156">Remarks</span></span>

<span data-ttu-id="74b6f-157">Приложение-контейнер, которое разрешает динамическое добавление или удаление устройств, должно обрабатывать сообщение [**WM \_ девицечанже**](/windows/desktop/DevIO/wm-devicechange) в своем окне верхнего уровня и пересылать сообщение в элемент управления с помощью метода **нотифиредиректдевицечанже** .</span><span class="sxs-lookup"><span data-stu-id="74b6f-157">A container application that allows dynamic addition or removal of devices should process the [**WM\_DEVICECHANGE**](/windows/desktop/DevIO/wm-devicechange) message in its top level window and forward the message to the control using the **NotifyRedirectDeviceChange** method.</span></span> <span data-ttu-id="74b6f-158">Примером динамического изменения устройства является то, что во время работы системы добавляется или удаляется перенаправленный диск.</span><span class="sxs-lookup"><span data-stu-id="74b6f-158">An example of a dynamic device change is when a redirected disk drive is added or removed while the system is running.</span></span>

<span data-ttu-id="74b6f-159">Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="74b6f-159">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="74b6f-160">Требования</span><span class="sxs-lookup"><span data-stu-id="74b6f-160">Requirements</span></span>



| <span data-ttu-id="74b6f-161">Требование</span><span class="sxs-lookup"><span data-stu-id="74b6f-161">Requirement</span></span> | <span data-ttu-id="74b6f-162">Значение</span><span class="sxs-lookup"><span data-stu-id="74b6f-162">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="74b6f-163">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="74b6f-163">Minimum supported client</span></span><br/> | <span data-ttu-id="74b6f-164">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="74b6f-164">Windows Vista</span></span><br/>                                                                     |
| <span data-ttu-id="74b6f-165">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="74b6f-165">Minimum supported server</span></span><br/> | <span data-ttu-id="74b6f-166">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="74b6f-166">Windows Server 2008</span></span><br/>                                                               |
| <span data-ttu-id="74b6f-167">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="74b6f-167">Type library</span></span><br/>             | <dl> <span data-ttu-id="74b6f-168"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="74b6f-168"><dt>MsTscAx.dll</dt></span></span> </dl>       |
| <span data-ttu-id="74b6f-169">DLL</span><span class="sxs-lookup"><span data-stu-id="74b6f-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="74b6f-170"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="74b6f-170"><dt>MsTscAx.dll</dt></span></span> </dl>       |
| <span data-ttu-id="74b6f-171">IID</span><span class="sxs-lookup"><span data-stu-id="74b6f-171">IID</span></span><br/>                      | <span data-ttu-id="74b6f-172">IID \_ имсрдпклиентнонскриптабле определен как 2f079c4c-87B2-4afd-97ab-20cdb43038ae</span><span class="sxs-lookup"><span data-stu-id="74b6f-172">IID\_IMsRdpClientNonScriptable is defined as 2f079c4c-87b2-4afd-97ab-20cdb43038ae</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="74b6f-173">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="74b6f-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74b6f-174">**IMsRdpClientNonScriptable2**</span><span class="sxs-lookup"><span data-stu-id="74b6f-174">**IMsRdpClientNonScriptable2**</span></span>](imsrdpclientnonscriptable2.md)
</dt> <dt>

[<span data-ttu-id="74b6f-175">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="74b6f-175">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> <dt>

[<span data-ttu-id="74b6f-176">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="74b6f-176">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="74b6f-177">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="74b6f-177">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="74b6f-178">**имсрдпклиентнонскриптабле**</span><span class="sxs-lookup"><span data-stu-id="74b6f-178">**IMsRdpClientNonScriptable**</span></span>](imsrdpclientnonscriptable-interface.md)
</dt> </dl>

 

