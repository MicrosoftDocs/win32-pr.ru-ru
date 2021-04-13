---
title: Имстскакс Сендонвиртуалчаннел, метод
description: Отправляет данные на сервер узла сеансов удаленный рабочий стол (узел сеанса удаленных рабочих столов) по виртуальному каналу, созданному ранее с помощью метода Креатевиртуалчаннелс.
ms.assetid: 795ef508-bdf7-4897-84b1-931615262293
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сендонвиртуалчаннел
- Службы удаленных рабочих столов метода Сендонвиртуалчаннел, интерфейс Имстскакс
- Службы удаленных рабочих столов интерфейса Имстскакс, метод Сендонвиртуалчаннел
- Службы удаленных рабочих столов метода Сендонвиртуалчаннел, интерфейс Имсрдпклиент
- Службы удаленных рабочих столов интерфейса Имсрдпклиент, метод Сендонвиртуалчаннел
- Службы удаленных рабочих столов метода Сендонвиртуалчаннел, интерфейс IMsRdpClient2
- Службы удаленных рабочих столов интерфейса IMsRdpClient2, метод Сендонвиртуалчаннел
- Службы удаленных рабочих столов метода Сендонвиртуалчаннел, интерфейс IMsRdpClient3
- Службы удаленных рабочих столов интерфейса IMsRdpClient3, метод Сендонвиртуалчаннел
- Службы удаленных рабочих столов метода Сендонвиртуалчаннел, интерфейс IMsRdpClient4
- Службы удаленных рабочих столов интерфейса IMsRdpClient4, метод Сендонвиртуалчаннел
- Службы удаленных рабочих столов метода Сендонвиртуалчаннел, интерфейс IMsRdpClient5
- Службы удаленных рабочих столов интерфейса IMsRdpClient5, метод Сендонвиртуалчаннел
- Службы удаленных рабочих столов метода Сендонвиртуалчаннел, интерфейс IMsRdpClient6
- Службы удаленных рабочих столов интерфейса IMsRdpClient6, метод Сендонвиртуалчаннел
- Службы удаленных рабочих столов метода Сендонвиртуалчаннел, интерфейс IMsRdpClient7
- Службы удаленных рабочих столов интерфейса IMsRdpClient7, метод Сендонвиртуалчаннел
- Службы удаленных рабочих столов метода Сендонвиртуалчаннел, интерфейс IMsRdpClient8
- Службы удаленных рабочих столов интерфейса IMsRdpClient8, метод Сендонвиртуалчаннел
- Службы удаленных рабочих столов метода Сендонвиртуалчаннел, интерфейс IMsRdpClient9
- Службы удаленных рабочих столов интерфейса IMsRdpClient9, метод Сендонвиртуалчаннел
topic_type:
- apiref
api_name:
- IMsTscAx.SendOnVirtualChannel
- IMsRdpClient.SendOnVirtualChannel
- IMsRdpClient2.SendOnVirtualChannel
- IMsRdpClient3.SendOnVirtualChannel
- IMsRdpClient4.SendOnVirtualChannel
- IMsRdpClient5.SendOnVirtualChannel
- IMsRdpClient6.SendOnVirtualChannel
- IMsRdpClient7.SendOnVirtualChannel
- IMsRdpClient8.SendOnVirtualChannel
- IMsRdpClient9.SendOnVirtualChannel
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1371ae17978601a3194f755dd364d9227b8fc28
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489504"
---
# <a name="imstscaxsendonvirtualchannel-method"></a><span data-ttu-id="0d764-124">Метод Имстскакс:: Сендонвиртуалчаннел</span><span class="sxs-lookup"><span data-stu-id="0d764-124">IMsTscAx::SendOnVirtualChannel method</span></span>

<span data-ttu-id="0d764-125">Отправляет данные на сервер узла сеансов удаленный рабочий стол (узел сеанса удаленных рабочих столов) по виртуальному каналу, созданному ранее с помощью метода [**креатевиртуалчаннелс**](imstscax-createvirtualchannels.md) .</span><span class="sxs-lookup"><span data-stu-id="0d764-125">Sends data to the Remote Desktop Session Host (RD Session Host) server over a virtual channel that was created previously by using the [**CreateVirtualChannels**](imstscax-createvirtualchannels.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d764-126">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0d764-126">Syntax</span></span>


```C++
HRESULT SendOnVirtualChannel(
  [in] BSTR ChanName,
  [in] BSTR ChanData
);
```



## <a name="parameters"></a><span data-ttu-id="0d764-127">Параметры</span><span class="sxs-lookup"><span data-stu-id="0d764-127">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d764-128">*Чаннаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0d764-128">*ChanName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d764-129">Имя виртуального канала, указанное в вызове [**креатевиртуалчаннелс**](imstscax-createvirtualchannels.md).</span><span class="sxs-lookup"><span data-stu-id="0d764-129">The virtual channel name that was specified in the call to [**CreateVirtualChannels**](imstscax-createvirtualchannels.md).</span></span>

</dd> <dt>

<span data-ttu-id="0d764-130">*Чандата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0d764-130">*ChanData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d764-131">Данные для отправки по виртуальному каналу в форме **BSTR** .</span><span class="sxs-lookup"><span data-stu-id="0d764-131">The data to send over the virtual channel, in **BSTR** form.</span></span> <span data-ttu-id="0d764-132">Нет ограничений, что эти данные должны быть строками, заканчивающимися нулем.</span><span class="sxs-lookup"><span data-stu-id="0d764-132">There is no restriction that this data must be null-terminated strings.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d764-133">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0d764-133">Return value</span></span>

<span data-ttu-id="0d764-134">В случае успеха возвратите значение **\_ ОК** .</span><span class="sxs-lookup"><span data-stu-id="0d764-134">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="0d764-135">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0d764-135">Remarks</span></span>

<span data-ttu-id="0d764-136">Сведения об ограничениях именования виртуальных каналов см. в статье [Регистрация клиента виртуального канала](virtual-channel-client-registration.md) .</span><span class="sxs-lookup"><span data-stu-id="0d764-136">Refer to [Virtual Channel Client Registration](virtual-channel-client-registration.md) for information about virtual channel naming restrictions.</span></span>

<span data-ttu-id="0d764-137">Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="0d764-137">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0d764-138">Требования</span><span class="sxs-lookup"><span data-stu-id="0d764-138">Requirements</span></span>



| <span data-ttu-id="0d764-139">Требование</span><span class="sxs-lookup"><span data-stu-id="0d764-139">Requirement</span></span> | <span data-ttu-id="0d764-140">Значение</span><span class="sxs-lookup"><span data-stu-id="0d764-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0d764-141">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0d764-141">Minimum supported client</span></span><br/> | <span data-ttu-id="0d764-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0d764-142">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="0d764-143">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0d764-143">Minimum supported server</span></span><br/> | <span data-ttu-id="0d764-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0d764-144">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="0d764-145">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="0d764-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="0d764-146"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0d764-146"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="0d764-147">DLL</span><span class="sxs-lookup"><span data-stu-id="0d764-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0d764-148"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0d764-148"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="0d764-149">IID</span><span class="sxs-lookup"><span data-stu-id="0d764-149">IID</span></span><br/>                      | <span data-ttu-id="0d764-150">IID \_ имстскакс определен как 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="0d764-150">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="0d764-151">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0d764-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d764-152">**имсрдпклиент**</span><span class="sxs-lookup"><span data-stu-id="0d764-152">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="0d764-153">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="0d764-153">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="0d764-154">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="0d764-154">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="0d764-155">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="0d764-155">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="0d764-156">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="0d764-156">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="0d764-157">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="0d764-157">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="0d764-158">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="0d764-158">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="0d764-159">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="0d764-159">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="0d764-160">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="0d764-160">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="0d764-161">**креатевиртуалчаннелс**</span><span class="sxs-lookup"><span data-stu-id="0d764-161">**CreateVirtualChannels**</span></span>](imstscax-createvirtualchannels.md)
</dt> <dt>

[<span data-ttu-id="0d764-162">**имстскакс**</span><span class="sxs-lookup"><span data-stu-id="0d764-162">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> </dl>

 

 





