---
title: Имсрдпклиент RequestClose, метод
description: Запрашивает корректное завершение работы элемента управления ActiveX удаленный рабочий стол.
ms.assetid: 0b930a00-f134-4da2-a752-8fd131a22043
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода RequestClose
- Службы удаленных рабочих столов метода RequestClose, интерфейс Имсрдпклиент
- Службы удаленных рабочих столов интерфейса Имсрдпклиент, метод RequestClose
- Службы удаленных рабочих столов метода RequestClose, интерфейс IMsRdpClient2
- Службы удаленных рабочих столов интерфейса IMsRdpClient2, метод RequestClose
- Службы удаленных рабочих столов метода RequestClose, интерфейс IMsRdpClient3
- Службы удаленных рабочих столов интерфейса IMsRdpClient3, метод RequestClose
- Службы удаленных рабочих столов метода RequestClose, интерфейс IMsRdpClient4
- Службы удаленных рабочих столов интерфейса IMsRdpClient4, метод RequestClose
- Службы удаленных рабочих столов метода RequestClose, интерфейс IMsRdpClient5
- Службы удаленных рабочих столов интерфейса IMsRdpClient5, метод RequestClose
- Службы удаленных рабочих столов метода RequestClose, интерфейс IMsRdpClient6
- Службы удаленных рабочих столов интерфейса IMsRdpClient6, метод RequestClose
- Службы удаленных рабочих столов метода RequestClose, интерфейс IMsRdpClient7
- Службы удаленных рабочих столов интерфейса IMsRdpClient7, метод RequestClose
- Службы удаленных рабочих столов метода RequestClose, интерфейс IMsRdpClient8
- Службы удаленных рабочих столов интерфейса IMsRdpClient8, метод RequestClose
- Службы удаленных рабочих столов метода RequestClose, интерфейс IMsRdpClient9
- Службы удаленных рабочих столов интерфейса IMsRdpClient9, метод RequestClose
- Службы удаленных рабочих столов метода RequestClose, интерфейс IMsRdpClient10
- Службы удаленных рабочих столов интерфейса IMsRdpClient10, метод RequestClose
topic_type:
- apiref
api_name:
- IMsRdpClient.RequestClose
- IMsRdpClient2.RequestClose
- IMsRdpClient3.RequestClose
- IMsRdpClient4.RequestClose
- IMsRdpClient5.RequestClose
- IMsRdpClient6.RequestClose
- IMsRdpClient7.RequestClose
- IMsRdpClient8.RequestClose
- IMsRdpClient9.RequestClose
- IMsRdpClient10.RequestClose
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1679b08680b962cdbff57e9bbbd1c392607d8709
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801582"
---
# <a name="imsrdpclientrequestclose-method"></a><span data-ttu-id="2cbaf-124">Метод Имсрдпклиент:: RequestClose</span><span class="sxs-lookup"><span data-stu-id="2cbaf-124">IMsRdpClient::RequestClose method</span></span>

<span data-ttu-id="2cbaf-125">Запрашивает корректное завершение работы элемента управления ActiveX удаленный рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="2cbaf-125">Requests a graceful shutdown of the Remote Desktop ActiveX control.</span></span> <span data-ttu-id="2cbaf-126">Корректное завершение работы может включать в себя завершение сеанса службы удаленных рабочих столов пользователя, но не завершает работу сервера узла сеансов удаленный рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="2cbaf-126">A graceful shutdown can include ending the user's Remote Desktop Services session but it does not shut down the Remote Desktop Session Host (RD Session Host) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="2cbaf-127">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2cbaf-127">Syntax</span></span>


```C++
HRESULT RequestClose(
  [out] ControlCloseStatus *pCloseStatus
);
```



## <a name="parameters"></a><span data-ttu-id="2cbaf-128">Параметры</span><span class="sxs-lookup"><span data-stu-id="2cbaf-128">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2cbaf-129">*пклосестатус* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="2cbaf-129">*pCloseStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2cbaf-130">Значение из перечисления [**контролклосестатус**](controlclosestatus.md) , указывающее, может ли приложение немедленно закрыть элемент управления.</span><span class="sxs-lookup"><span data-stu-id="2cbaf-130">Value from the [**ControlCloseStatus**](controlclosestatus.md) enumeration that indicates whether the application can close the control immediately.</span></span> <span data-ttu-id="2cbaf-131">Ниже приведен список возможных значений.</span><span class="sxs-lookup"><span data-stu-id="2cbaf-131">Following is a list of possible values.</span></span>

<dt>

<span id="controlCloseCanProceed"></span><span id="controlclosecanproceed"></span><span id="CONTROLCLOSECANPROCEED"></span>

<span data-ttu-id="2cbaf-132"><span id="controlCloseCanProceed"></span><span id="controlclosecanproceed"></span><span id="CONTROLCLOSECANPROCEED"></span>**контролклосеканпроцеед** (символ 0x0000)</span><span class="sxs-lookup"><span data-stu-id="2cbaf-132"><span id="controlCloseCanProceed"></span><span id="controlclosecanproceed"></span><span id="CONTROLCLOSECANPROCEED"></span>**controlCloseCanProceed** (0x0000)</span></span>


</dt> <dd>

<span data-ttu-id="2cbaf-133">Приложение контейнера может перейти к немедленному закрытию элемента управления.</span><span class="sxs-lookup"><span data-stu-id="2cbaf-133">The container application can proceed to close the control immediately.</span></span> <span data-ttu-id="2cbaf-134">Это значение может также означать, что соединение уже завершено.</span><span class="sxs-lookup"><span data-stu-id="2cbaf-134">This value can also indicate that the connection has already terminated.</span></span>

</dd> <dt>

<span id="controlCloseWaitForEvents"></span><span id="controlclosewaitforevents"></span><span id="CONTROLCLOSEWAITFOREVENTS"></span>

<span data-ttu-id="2cbaf-135"><span id="controlCloseWaitForEvents"></span><span id="controlclosewaitforevents"></span><span id="CONTROLCLOSEWAITFOREVENTS"></span>**контролклосеваитфоревентс** (0x0001)</span><span class="sxs-lookup"><span data-stu-id="2cbaf-135"><span id="controlCloseWaitForEvents"></span><span id="controlclosewaitforevents"></span><span id="CONTROLCLOSEWAITFOREVENTS"></span>**controlCloseWaitForEvents** (0x0001)</span></span>


</dt> <dd>

<span data-ttu-id="2cbaf-136">Приложение контейнера не должно немедленно закрыть элемент управления; приложение должно ожидать одно из событий, описанных в следующем разделе "Примечания", перед закрытием.</span><span class="sxs-lookup"><span data-stu-id="2cbaf-136">The container application should not close the control immediately; the application should wait for one of the events described in the following Remarks section to occur before closing.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2cbaf-137">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2cbaf-137">Return value</span></span>

<span data-ttu-id="2cbaf-138">В случае успеха возвратите значение **\_ ОК** .</span><span class="sxs-lookup"><span data-stu-id="2cbaf-138">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="2cbaf-139">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2cbaf-139">Remarks</span></span>

<span data-ttu-id="2cbaf-140">Если параметр *пклосестатус* равен **контролклосеваитфоревентс**, то приложение должно подождать одно из следующих событий, прежде чем приложение закроет элемент управления:</span><span class="sxs-lookup"><span data-stu-id="2cbaf-140">If the *pCloseStatus* parameter is equal to **controlCloseWaitForEvents**, the application should wait for one of the following events to occur before the application closes the control:</span></span>

-   <span data-ttu-id="2cbaf-141">[**Имстскаксевентс:: Ondisconnectо**](imstscaxevents-ondisconnected.md).</span><span class="sxs-lookup"><span data-stu-id="2cbaf-141">[**IMsTscAxEvents::OnDisconnected**](imstscaxevents-ondisconnected.md).</span></span> <span data-ttu-id="2cbaf-142">Если пользователь не вошел в сеанс службы удаленных рабочих столов, приложение может вызвать функцию [**дестройвиндов**](/windows/desktop/api/winuser/nf-winuser-destroywindow) , чтобы уничтожить все окна и закрыть элемент управления.</span><span class="sxs-lookup"><span data-stu-id="2cbaf-142">If the user is not logged on to the Remote Desktop Services session, the application can call the [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) function to destroy all windows and then close the control.</span></span>
-   <span data-ttu-id="2cbaf-143">[**Имстскаксевентс:: онконфирмклосе**](imstscaxevents-onconfirmclose.md).</span><span class="sxs-lookup"><span data-stu-id="2cbaf-143">[**IMsTscAxEvents::OnConfirmClose**](imstscaxevents-onconfirmclose.md).</span></span> <span data-ttu-id="2cbaf-144">Если пользователь вошел в сеанс службы удаленных рабочих столов, элемент управления запускает событие **онконфирмклосе** .</span><span class="sxs-lookup"><span data-stu-id="2cbaf-144">If the user is logged on to the Remote Desktop Services session, the control fires an **OnConfirmClose** event.</span></span> <span data-ttu-id="2cbaf-145">Это событие позволяет приложению запрашивать пользователя о том, следует ли закрыть подключение.</span><span class="sxs-lookup"><span data-stu-id="2cbaf-145">This event allows the application to prompt the user about whether to close the connection.</span></span> <span data-ttu-id="2cbaf-146">Если пользователь ответит на запрос, приложение контейнера может вызвать [**дестройвиндов**](/windows/desktop/api/winuser/nf-winuser-destroywindow) для уничтожения всех окон и закрыть элемент управления.</span><span class="sxs-lookup"><span data-stu-id="2cbaf-146">If the user replies yes to the prompt, the container application can call [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) to destroy all windows, and close the control.</span></span>

<span data-ttu-id="2cbaf-147">**RequestClose** позволяет приложению-контейнеру запрашивать пользователя о необходимости закрыть подключение.</span><span class="sxs-lookup"><span data-stu-id="2cbaf-147">**RequestClose** allows a container application to prompt the user about whether to close a connection.</span></span> <span data-ttu-id="2cbaf-148">Дополнительные сведения см. в разделе [**имстскаксевентс:: онконфирмклосе**](imstscaxevents-onconfirmclose.md).</span><span class="sxs-lookup"><span data-stu-id="2cbaf-148">For more information, see [**IMsTscAxEvents::OnConfirmClose**](imstscaxevents-onconfirmclose.md).</span></span>

<span data-ttu-id="2cbaf-149">Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="2cbaf-149">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2cbaf-150">Требования</span><span class="sxs-lookup"><span data-stu-id="2cbaf-150">Requirements</span></span>



| <span data-ttu-id="2cbaf-151">Требование</span><span class="sxs-lookup"><span data-stu-id="2cbaf-151">Requirement</span></span> | <span data-ttu-id="2cbaf-152">Значение</span><span class="sxs-lookup"><span data-stu-id="2cbaf-152">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2cbaf-153">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2cbaf-153">Minimum supported client</span></span><br/> | <span data-ttu-id="2cbaf-154">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2cbaf-154">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="2cbaf-155">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2cbaf-155">Minimum supported server</span></span><br/> | <span data-ttu-id="2cbaf-156">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2cbaf-156">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="2cbaf-157">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="2cbaf-157">Type library</span></span><br/>             | <dl> <span data-ttu-id="2cbaf-158"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2cbaf-158"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="2cbaf-159">DLL</span><span class="sxs-lookup"><span data-stu-id="2cbaf-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2cbaf-160"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2cbaf-160"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="2cbaf-161">IID</span><span class="sxs-lookup"><span data-stu-id="2cbaf-161">IID</span></span><br/>                      | <span data-ttu-id="2cbaf-162">IID \_ имсрдпклиент определен как 92b4a539-7115-4b7c-a5a9-e5d9efc2780a</span><span class="sxs-lookup"><span data-stu-id="2cbaf-162">IID\_IMsRdpClient is defined as 92b4a539-7115-4b7c-a5a9-e5d9efc2780a</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="2cbaf-163">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2cbaf-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2cbaf-164">**имсрдпклиент**</span><span class="sxs-lookup"><span data-stu-id="2cbaf-164">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="2cbaf-165">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="2cbaf-165">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="2cbaf-166">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="2cbaf-166">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="2cbaf-167">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="2cbaf-167">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="2cbaf-168">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="2cbaf-168">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="2cbaf-169">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="2cbaf-169">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="2cbaf-170">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="2cbaf-170">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="2cbaf-171">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="2cbaf-171">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="2cbaf-172">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="2cbaf-172">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="2cbaf-173">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="2cbaf-173">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> <dt>

[<span data-ttu-id="2cbaf-174">**Имстскаксевентс:: Онконфирмклосе**</span><span class="sxs-lookup"><span data-stu-id="2cbaf-174">**IMsTscAxEvents::OnConfirmClose**</span></span>](imstscaxevents-onconfirmclose.md)
</dt> <dt>

[<span data-ttu-id="2cbaf-175">**Имстскаксевентс:: ondisconnectо**</span><span class="sxs-lookup"><span data-stu-id="2cbaf-175">**IMsTscAxEvents::OnDisconnected**</span></span>](imstscaxevents-ondisconnected.md)
</dt> </dl>

 

