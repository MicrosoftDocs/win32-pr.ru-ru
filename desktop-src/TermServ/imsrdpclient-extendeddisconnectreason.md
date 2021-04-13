---
title: Имсрдпклиент Екстендеддисконнектреасон, свойство
description: Содержит расширенные сведения о причине отключения элемента управления.
ms.assetid: 5729992f-6695-44c0-8cf0-0d6b4cbddb62
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Екстендеддисконнектреасон
- Службы удаленных рабочих столов свойства Екстендеддисконнектреасон, интерфейс Имсрдпклиент
- Службы удаленных рабочих столов интерфейса Имсрдпклиент, свойство Екстендеддисконнектреасон
- Службы удаленных рабочих столов свойства Екстендеддисконнектреасон, интерфейс IMsRdpClient2
- Службы удаленных рабочих столов интерфейса IMsRdpClient2, свойство Екстендеддисконнектреасон
- Службы удаленных рабочих столов свойства Екстендеддисконнектреасон, интерфейс IMsRdpClient3
- Службы удаленных рабочих столов интерфейса IMsRdpClient3, свойство Екстендеддисконнектреасон
- Службы удаленных рабочих столов свойства Екстендеддисконнектреасон, интерфейс IMsRdpClient4
- Службы удаленных рабочих столов интерфейса IMsRdpClient4, свойство Екстендеддисконнектреасон
- Службы удаленных рабочих столов свойства Екстендеддисконнектреасон, интерфейс IMsRdpClient5
- Службы удаленных рабочих столов интерфейса IMsRdpClient5, свойство Екстендеддисконнектреасон
- Службы удаленных рабочих столов свойства Екстендеддисконнектреасон, интерфейс IMsRdpClient6
- Службы удаленных рабочих столов интерфейса IMsRdpClient6, свойство Екстендеддисконнектреасон
- Службы удаленных рабочих столов свойства Екстендеддисконнектреасон, интерфейс IMsRdpClient7
- Службы удаленных рабочих столов интерфейса IMsRdpClient7, свойство Екстендеддисконнектреасон
- Службы удаленных рабочих столов свойства Екстендеддисконнектреасон, интерфейс IMsRdpClient8
- Службы удаленных рабочих столов интерфейса IMsRdpClient8, свойство Екстендеддисконнектреасон
- Службы удаленных рабочих столов свойства Екстендеддисконнектреасон, интерфейс IMsRdpClient9
- Службы удаленных рабочих столов интерфейса IMsRdpClient9, свойство Екстендеддисконнектреасон
- Службы удаленных рабочих столов свойства Екстендеддисконнектреасон, интерфейс IMsRdpClient10
- Службы удаленных рабочих столов интерфейса IMsRdpClient10, свойство Екстендеддисконнектреасон
topic_type:
- apiref
api_name:
- IMsRdpClient.ExtendedDisconnectReason
- IMsRdpClient.get_ExtendedDisconnectReason
- IMsRdpClient2.ExtendedDisconnectReason
- IMsRdpClient2.get_ExtendedDisconnectReason
- IMsRdpClient3.ExtendedDisconnectReason
- IMsRdpClient3.get_ExtendedDisconnectReason
- IMsRdpClient4.ExtendedDisconnectReason
- IMsRdpClient4.get_ExtendedDisconnectReason
- IMsRdpClient5.ExtendedDisconnectReason
- IMsRdpClient5.get_ExtendedDisconnectReason
- IMsRdpClient6.ExtendedDisconnectReason
- IMsRdpClient6.get_ExtendedDisconnectReason
- IMsRdpClient7.ExtendedDisconnectReason
- IMsRdpClient7.get_ExtendedDisconnectReason
- IMsRdpClient8.ExtendedDisconnectReason
- IMsRdpClient8.get_ExtendedDisconnectReason
- IMsRdpClient9.ExtendedDisconnectReason
- IMsRdpClient9.get_ExtendedDisconnectReason
- IMsRdpClient10.ExtendedDisconnectReason
- IMsRdpClient10.get_ExtendedDisconnectReason
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b94c2612b231e24aaec855b6ebd1f9a0498b63c3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535225"
---
# <a name="imsrdpclientextendeddisconnectreason-property"></a><span data-ttu-id="0dccc-124">Свойство Имсрдпклиент:: Екстендеддисконнектреасон</span><span class="sxs-lookup"><span data-stu-id="0dccc-124">IMsRdpClient::ExtendedDisconnectReason property</span></span>

<span data-ttu-id="0dccc-125">Содержит расширенные сведения о причине отключения элемента управления.</span><span class="sxs-lookup"><span data-stu-id="0dccc-125">Contains extended information about the control's reason for disconnection.</span></span>

<span data-ttu-id="0dccc-126">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="0dccc-126">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="0dccc-127">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0dccc-127">Syntax</span></span>


```C++
HRESULT get_ExtendedDisconnectReason(
  [out] ExtendedDisconnectReasonCode *pExtendedDisconnectReason
);
```



## <a name="property-value"></a><span data-ttu-id="0dccc-128">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="0dccc-128">Property value</span></span>

<span data-ttu-id="0dccc-129">Указатель на значение [**екстендеддисконнектреасонкоде**](extendeddisconnectreasoncode.md) , указывающее причину отключения клиента.</span><span class="sxs-lookup"><span data-stu-id="0dccc-129">Pointer to the [**ExtendedDisconnectReasonCode**](extendeddisconnectreasoncode.md) value indicating the reason for disconnection of the client.</span></span>

## <a name="error-codes"></a><span data-ttu-id="0dccc-130">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="0dccc-130">Error codes</span></span>

<span data-ttu-id="0dccc-131">Если метод выполнен успешно, возвращается значение **S \_ OK** .</span><span class="sxs-lookup"><span data-stu-id="0dccc-131">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="0dccc-132">Любое другое значение **HRESULT** указывает на сбой вызова.</span><span class="sxs-lookup"><span data-stu-id="0dccc-132">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="0dccc-133">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0dccc-133">Remarks</span></span>

<span data-ttu-id="0dccc-134">Обычно этот метод вызывается в обработчике событий [**имстскаксевентс:: Ondisconnectных**](imstscaxevents-ondisconnected.md) для получения дополнительных сведений о событии отключения.</span><span class="sxs-lookup"><span data-stu-id="0dccc-134">Typically this method is called in the [**IMsTscAxEvents::OnDisconnected**](imstscaxevents-ondisconnected.md) event handler to retrieve additional information about the disconnection event.</span></span>

<span data-ttu-id="0dccc-135">Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="0dccc-135">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0dccc-136">Требования</span><span class="sxs-lookup"><span data-stu-id="0dccc-136">Requirements</span></span>



| <span data-ttu-id="0dccc-137">Требование</span><span class="sxs-lookup"><span data-stu-id="0dccc-137">Requirement</span></span> | <span data-ttu-id="0dccc-138">Значение</span><span class="sxs-lookup"><span data-stu-id="0dccc-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0dccc-139">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0dccc-139">Minimum supported client</span></span><br/> | <span data-ttu-id="0dccc-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0dccc-140">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="0dccc-141">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0dccc-141">Minimum supported server</span></span><br/> | <span data-ttu-id="0dccc-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0dccc-142">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="0dccc-143">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="0dccc-143">Type library</span></span><br/>             | <dl> <span data-ttu-id="0dccc-144"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0dccc-144"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="0dccc-145">DLL</span><span class="sxs-lookup"><span data-stu-id="0dccc-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0dccc-146"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0dccc-146"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="0dccc-147">IID</span><span class="sxs-lookup"><span data-stu-id="0dccc-147">IID</span></span><br/>                      | <span data-ttu-id="0dccc-148">IID \_ имсрдпклиент определен как 92b4a539-7115-4b7c-a5a9-e5d9efc2780a</span><span class="sxs-lookup"><span data-stu-id="0dccc-148">IID\_IMsRdpClient is defined as 92b4a539-7115-4b7c-a5a9-e5d9efc2780a</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="0dccc-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0dccc-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0dccc-150">**имсрдпклиент**</span><span class="sxs-lookup"><span data-stu-id="0dccc-150">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="0dccc-151">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="0dccc-151">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="0dccc-152">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="0dccc-152">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="0dccc-153">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="0dccc-153">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="0dccc-154">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="0dccc-154">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="0dccc-155">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="0dccc-155">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="0dccc-156">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="0dccc-156">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="0dccc-157">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="0dccc-157">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="0dccc-158">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="0dccc-158">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="0dccc-159">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="0dccc-159">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> <dt>

[<span data-ttu-id="0dccc-160">**Имстскаксевентс:: ondisconnectо**</span><span class="sxs-lookup"><span data-stu-id="0dccc-160">**IMsTscAxEvents::OnDisconnected**</span></span>](imstscaxevents-ondisconnected.md)
</dt> </dl>

 

 





