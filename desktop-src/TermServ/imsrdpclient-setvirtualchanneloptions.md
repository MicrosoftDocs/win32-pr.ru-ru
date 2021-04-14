---
title: Имсрдпклиент Сетвиртуалчаннелоптионс, метод
description: Задает параметры виртуального канала для элемента управления ActiveX удаленный рабочий стол.
ms.assetid: c74c3917-5766-4d5b-8458-b051eb91cb28
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сетвиртуалчаннелоптионс
- Службы удаленных рабочих столов метода Сетвиртуалчаннелоптионс, интерфейс Имсрдпклиент
- Службы удаленных рабочих столов интерфейса Имсрдпклиент, метод Сетвиртуалчаннелоптионс
- Службы удаленных рабочих столов метода Сетвиртуалчаннелоптионс, интерфейс IMsRdpClient2
- Службы удаленных рабочих столов интерфейса IMsRdpClient2, метод Сетвиртуалчаннелоптионс
- Службы удаленных рабочих столов метода Сетвиртуалчаннелоптионс, интерфейс IMsRdpClient3
- Службы удаленных рабочих столов интерфейса IMsRdpClient3, метод Сетвиртуалчаннелоптионс
- Службы удаленных рабочих столов метода Сетвиртуалчаннелоптионс, интерфейс IMsRdpClient4
- Службы удаленных рабочих столов интерфейса IMsRdpClient4, метод Сетвиртуалчаннелоптионс
- Службы удаленных рабочих столов метода Сетвиртуалчаннелоптионс, интерфейс IMsRdpClient5
- Службы удаленных рабочих столов интерфейса IMsRdpClient5, метод Сетвиртуалчаннелоптионс
- Службы удаленных рабочих столов метода Сетвиртуалчаннелоптионс, интерфейс IMsRdpClient6
- Службы удаленных рабочих столов интерфейса IMsRdpClient6, метод Сетвиртуалчаннелоптионс
- Службы удаленных рабочих столов метода Сетвиртуалчаннелоптионс, интерфейс IMsRdpClient7
- Службы удаленных рабочих столов интерфейса IMsRdpClient7, метод Сетвиртуалчаннелоптионс
- Службы удаленных рабочих столов метода Сетвиртуалчаннелоптионс, интерфейс IMsRdpClient8
- Службы удаленных рабочих столов интерфейса IMsRdpClient8, метод Сетвиртуалчаннелоптионс
- Службы удаленных рабочих столов метода Сетвиртуалчаннелоптионс, интерфейс IMsRdpClient9
- Службы удаленных рабочих столов интерфейса IMsRdpClient9, метод Сетвиртуалчаннелоптионс
- Службы удаленных рабочих столов метода Сетвиртуалчаннелоптионс, интерфейс IMsRdpClient10
- Службы удаленных рабочих столов интерфейса IMsRdpClient10, метод Сетвиртуалчаннелоптионс
topic_type:
- apiref
api_name:
- IMsRdpClient.SetVirtualChannelOptions
- IMsRdpClient2.SetVirtualChannelOptions
- IMsRdpClient3.SetVirtualChannelOptions
- IMsRdpClient4.SetVirtualChannelOptions
- IMsRdpClient5.SetVirtualChannelOptions
- IMsRdpClient6.SetVirtualChannelOptions
- IMsRdpClient7.SetVirtualChannelOptions
- IMsRdpClient8.SetVirtualChannelOptions
- IMsRdpClient9.SetVirtualChannelOptions
- IMsRdpClient10.SetVirtualChannelOptions
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10e727fd3486b9d1b31fb3a421ea6ff268949790
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415077"
---
# <a name="imsrdpclientsetvirtualchanneloptions-method"></a><span data-ttu-id="ec7be-124">Метод Имсрдпклиент:: Сетвиртуалчаннелоптионс</span><span class="sxs-lookup"><span data-stu-id="ec7be-124">IMsRdpClient::SetVirtualChannelOptions method</span></span>

<span data-ttu-id="ec7be-125">Задает параметры виртуального канала для элемента управления ActiveX удаленный рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="ec7be-125">Sets the virtual channel options for the Remote Desktop ActiveX control.</span></span>

<span data-ttu-id="ec7be-126">Вызовите этот метод после вызова метода [**креатевиртуалчаннелс**](imstscax-createvirtualchannels.md) , но перед установкой соединения с помощью метода [**Connect**](imstscax-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="ec7be-126">Call this method after calling the [**CreateVirtualChannels**](imstscax-createvirtualchannels.md) method, but before establishing a connection with the [**Connect**](imstscax-connect.md) method.</span></span> <span data-ttu-id="ec7be-127">Этот метод задает дополнительные параметры для виртуальных каналов, созданных с помощью **креатевиртуалчаннелс**.</span><span class="sxs-lookup"><span data-stu-id="ec7be-127">This method sets additional options on virtual channels that have been created with **CreateVirtualChannels**.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec7be-128">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ec7be-128">Syntax</span></span>


```C++
HRESULT SetVirtualChannelOptions(
  [in] BSTR ChanName,
  [in] LONG chanOptions
);
```



## <a name="parameters"></a><span data-ttu-id="ec7be-129">Параметры</span><span class="sxs-lookup"><span data-stu-id="ec7be-129">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec7be-130">*Чаннаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ec7be-130">*ChanName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec7be-131">Имя виртуального канала, указанного в вызове метода [**креатевиртуалчаннелс**](imstscax-createvirtualchannels.md) .</span><span class="sxs-lookup"><span data-stu-id="ec7be-131">The name of the virtual channel that was specified in the call to the [**CreateVirtualChannels**](imstscax-createvirtualchannels.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="ec7be-132">*чаноптионс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ec7be-132">*chanOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec7be-133">Параметры, устанавливаемые для виртуального канала, заданного параметром *чаннаме* .</span><span class="sxs-lookup"><span data-stu-id="ec7be-133">The options to set for the virtual channel specified by the *ChanName* parameter.</span></span> <span data-ttu-id="ec7be-134">Описание возможных вариантов см. в разделе [**Channel \_ DEF**](/windows/desktop/api/Pchannel/ns-pchannel-tagchannel_def).</span><span class="sxs-lookup"><span data-stu-id="ec7be-134">For a description of possible options, see [**CHANNEL\_DEF**](/windows/desktop/api/Pchannel/ns-pchannel-tagchannel_def).</span></span> <span data-ttu-id="ec7be-135">Дополнительные сведения см. в разделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="ec7be-135">For more information, see the following Remarks section.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec7be-136">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ec7be-136">Return value</span></span>

<span data-ttu-id="ec7be-137">В случае успеха возвратите значение **\_ ОК** .</span><span class="sxs-lookup"><span data-stu-id="ec7be-137">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="ec7be-138">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ec7be-138">Remarks</span></span>

<span data-ttu-id="ec7be-139">В качестве примера использования этого метода можно объявить канал как удаленное управление, задав **\_ \_ Постоянный флаг удаленного \_ управления \_ для параметра канала** .</span><span class="sxs-lookup"><span data-stu-id="ec7be-139">An example of using this method would be to declare the channel as remote control persistent by setting the **CHANNEL\_OPTION\_REMOTE\_CONTROL\_PERSISTENT** flag.</span></span> <span data-ttu-id="ec7be-140">Это означает, что канал не будет закрыт, когда удаленный элемент управления подключается к сеансу, подключенному к клиенту, или отключается от него.</span><span class="sxs-lookup"><span data-stu-id="ec7be-140">This means that the channel would not be closed when a remote control connects to or disconnects from the session connected to the client.</span></span> <span data-ttu-id="ec7be-141">Дополнительные сведения см. в разделе [постоянные виртуальные каналы удаленного управления](remote-control-persistent-virtual-channels.md).</span><span class="sxs-lookup"><span data-stu-id="ec7be-141">For more information, see [Remote Control Persistent Virtual Channels](remote-control-persistent-virtual-channels.md).</span></span>

<span data-ttu-id="ec7be-142">Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="ec7be-142">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ec7be-143">Требования</span><span class="sxs-lookup"><span data-stu-id="ec7be-143">Requirements</span></span>



| <span data-ttu-id="ec7be-144">Требование</span><span class="sxs-lookup"><span data-stu-id="ec7be-144">Requirement</span></span> | <span data-ttu-id="ec7be-145">Значение</span><span class="sxs-lookup"><span data-stu-id="ec7be-145">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ec7be-146">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ec7be-146">Minimum supported client</span></span><br/> | <span data-ttu-id="ec7be-147">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ec7be-147">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="ec7be-148">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ec7be-148">Minimum supported server</span></span><br/> | <span data-ttu-id="ec7be-149">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ec7be-149">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="ec7be-150">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="ec7be-150">Type library</span></span><br/>             | <dl> <span data-ttu-id="ec7be-151"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ec7be-151"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="ec7be-152">DLL</span><span class="sxs-lookup"><span data-stu-id="ec7be-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ec7be-153"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ec7be-153"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="ec7be-154">IID</span><span class="sxs-lookup"><span data-stu-id="ec7be-154">IID</span></span><br/>                      | <span data-ttu-id="ec7be-155">IID \_ имсрдпклиент определен как 92b4a539-7115-4b7c-a5a9-e5d9efc2780a</span><span class="sxs-lookup"><span data-stu-id="ec7be-155">IID\_IMsRdpClient is defined as 92b4a539-7115-4b7c-a5a9-e5d9efc2780a</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="ec7be-156">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ec7be-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec7be-157">**имсрдпклиент**</span><span class="sxs-lookup"><span data-stu-id="ec7be-157">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="ec7be-158">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="ec7be-158">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="ec7be-159">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="ec7be-159">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="ec7be-160">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="ec7be-160">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="ec7be-161">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="ec7be-161">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="ec7be-162">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="ec7be-162">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="ec7be-163">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="ec7be-163">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="ec7be-164">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="ec7be-164">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="ec7be-165">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="ec7be-165">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="ec7be-166">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="ec7be-166">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> <dt>

[<span data-ttu-id="ec7be-167">**DEF по КАНАЛу \_**</span><span class="sxs-lookup"><span data-stu-id="ec7be-167">**CHANNEL\_DEF**</span></span>](/windows/desktop/api/Pchannel/ns-pchannel-tagchannel_def)
</dt> <dt>

[<span data-ttu-id="ec7be-168">**креатевиртуалчаннелс**</span><span class="sxs-lookup"><span data-stu-id="ec7be-168">**CreateVirtualChannels**</span></span>](imstscax-createvirtualchannels.md)
</dt> <dt>

[<span data-ttu-id="ec7be-169">**жетвиртуалчаннелоптионс**</span><span class="sxs-lookup"><span data-stu-id="ec7be-169">**GetVirtualChannelOptions**</span></span>](imsrdpclient-getvirtualchanneloptions.md)
</dt> </dl>

 

 





