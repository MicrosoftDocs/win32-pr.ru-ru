---
title: Имсрдпклиент Жетвиртуалчаннелоптионс, метод
description: Извлекает параметры, заданные для виртуального канала.
ms.assetid: d2ec9fb2-c0dc-49f1-a86b-d7abca13a322
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Жетвиртуалчаннелоптионс
- Службы удаленных рабочих столов метода Жетвиртуалчаннелоптионс, интерфейс Имсрдпклиент
- Службы удаленных рабочих столов интерфейса Имсрдпклиент, метод Жетвиртуалчаннелоптионс
- Службы удаленных рабочих столов метода Жетвиртуалчаннелоптионс, интерфейс IMsRdpClient2
- Службы удаленных рабочих столов интерфейса IMsRdpClient2, метод Жетвиртуалчаннелоптионс
- Службы удаленных рабочих столов метода Жетвиртуалчаннелоптионс, интерфейс IMsRdpClient3
- Службы удаленных рабочих столов интерфейса IMsRdpClient3, метод Жетвиртуалчаннелоптионс
- Службы удаленных рабочих столов метода Жетвиртуалчаннелоптионс, интерфейс IMsRdpClient4
- Службы удаленных рабочих столов интерфейса IMsRdpClient4, метод Жетвиртуалчаннелоптионс
- Службы удаленных рабочих столов метода Жетвиртуалчаннелоптионс, интерфейс IMsRdpClient5
- Службы удаленных рабочих столов интерфейса IMsRdpClient5, метод Жетвиртуалчаннелоптионс
- Службы удаленных рабочих столов метода Жетвиртуалчаннелоптионс, интерфейс IMsRdpClient6
- Службы удаленных рабочих столов интерфейса IMsRdpClient6, метод Жетвиртуалчаннелоптионс
- Службы удаленных рабочих столов метода Жетвиртуалчаннелоптионс, интерфейс IMsRdpClient7
- Службы удаленных рабочих столов интерфейса IMsRdpClient7, метод Жетвиртуалчаннелоптионс
- Службы удаленных рабочих столов метода Жетвиртуалчаннелоптионс, интерфейс IMsRdpClient8
- Службы удаленных рабочих столов интерфейса IMsRdpClient8, метод Жетвиртуалчаннелоптионс
- Службы удаленных рабочих столов метода Жетвиртуалчаннелоптионс, интерфейс IMsRdpClient9
- Службы удаленных рабочих столов интерфейса IMsRdpClient9, метод Жетвиртуалчаннелоптионс
- Службы удаленных рабочих столов метода Жетвиртуалчаннелоптионс, интерфейс IMsRdpClient10
- Службы удаленных рабочих столов интерфейса IMsRdpClient10, метод Жетвиртуалчаннелоптионс
topic_type:
- apiref
api_name:
- IMsRdpClient.GetVirtualChannelOptions
- IMsRdpClient2.GetVirtualChannelOptions
- IMsRdpClient3.GetVirtualChannelOptions
- IMsRdpClient4.GetVirtualChannelOptions
- IMsRdpClient5.GetVirtualChannelOptions
- IMsRdpClient6.GetVirtualChannelOptions
- IMsRdpClient7.GetVirtualChannelOptions
- IMsRdpClient8.GetVirtualChannelOptions
- IMsRdpClient9.GetVirtualChannelOptions
- IMsRdpClient10.GetVirtualChannelOptions
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71548002ebc67dae8dc1a49e8144da3de608afb2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672840"
---
# <a name="imsrdpclientgetvirtualchanneloptions-method"></a><span data-ttu-id="e681b-124">Метод Имсрдпклиент:: Жетвиртуалчаннелоптионс</span><span class="sxs-lookup"><span data-stu-id="e681b-124">IMsRdpClient::GetVirtualChannelOptions method</span></span>

<span data-ttu-id="e681b-125">Извлекает параметры, заданные для виртуального канала.</span><span class="sxs-lookup"><span data-stu-id="e681b-125">Retrieves the options set for a virtual channel.</span></span>

## <a name="syntax"></a><span data-ttu-id="e681b-126">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e681b-126">Syntax</span></span>


```C++
HRESULT GetVirtualChannelOptions(
  [in]  BSTR ChanName,
  [out] LONG *pChanOptions
);
```



## <a name="parameters"></a><span data-ttu-id="e681b-127">Параметры</span><span class="sxs-lookup"><span data-stu-id="e681b-127">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e681b-128">*Чаннаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e681b-128">*ChanName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e681b-129">Имя виртуального канала, указанного в вызове метода [**креатевиртуалчаннелс**](imstscax-createvirtualchannels.md) .</span><span class="sxs-lookup"><span data-stu-id="e681b-129">The name of a virtual channel that was specified in the call to [**CreateVirtualChannels**](imstscax-createvirtualchannels.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="e681b-130">*пчаноптионс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e681b-130">*pChanOptions* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e681b-131">Параметры, заданные для виртуального канала, заданного параметром *чаннаме* .</span><span class="sxs-lookup"><span data-stu-id="e681b-131">The options set for the virtual channel specified by the *ChanName* parameter.</span></span> <span data-ttu-id="e681b-132">Описание возможных вариантов см. в разделе [**Channel \_ DEF**](/windows/desktop/api/Pchannel/ns-pchannel-tagchannel_def).</span><span class="sxs-lookup"><span data-stu-id="e681b-132">For a description of possible options, see [**CHANNEL\_DEF**](/windows/desktop/api/Pchannel/ns-pchannel-tagchannel_def).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e681b-133">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e681b-133">Return value</span></span>

<span data-ttu-id="e681b-134">В случае успеха возвратите значение **\_ ОК** .</span><span class="sxs-lookup"><span data-stu-id="e681b-134">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="e681b-135">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e681b-135">Remarks</span></span>

<span data-ttu-id="e681b-136">Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="e681b-136">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e681b-137">Требования</span><span class="sxs-lookup"><span data-stu-id="e681b-137">Requirements</span></span>



| <span data-ttu-id="e681b-138">Требование</span><span class="sxs-lookup"><span data-stu-id="e681b-138">Requirement</span></span> | <span data-ttu-id="e681b-139">Значение</span><span class="sxs-lookup"><span data-stu-id="e681b-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e681b-140">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e681b-140">Minimum supported client</span></span><br/> | <span data-ttu-id="e681b-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e681b-141">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="e681b-142">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e681b-142">Minimum supported server</span></span><br/> | <span data-ttu-id="e681b-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e681b-143">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="e681b-144">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="e681b-144">Type library</span></span><br/>             | <dl> <span data-ttu-id="e681b-145"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e681b-145"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="e681b-146">DLL</span><span class="sxs-lookup"><span data-stu-id="e681b-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e681b-147"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e681b-147"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="e681b-148">IID</span><span class="sxs-lookup"><span data-stu-id="e681b-148">IID</span></span><br/>                      | <span data-ttu-id="e681b-149">IID \_ имсрдпклиент определен как 92b4a539-7115-4b7c-a5a9-e5d9efc2780a</span><span class="sxs-lookup"><span data-stu-id="e681b-149">IID\_IMsRdpClient is defined as 92b4a539-7115-4b7c-a5a9-e5d9efc2780a</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="e681b-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e681b-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e681b-151">**имсрдпклиент**</span><span class="sxs-lookup"><span data-stu-id="e681b-151">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="e681b-152">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="e681b-152">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="e681b-153">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="e681b-153">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="e681b-154">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="e681b-154">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="e681b-155">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="e681b-155">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="e681b-156">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="e681b-156">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="e681b-157">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="e681b-157">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="e681b-158">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="e681b-158">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="e681b-159">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="e681b-159">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="e681b-160">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="e681b-160">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> <dt>

[<span data-ttu-id="e681b-161">**DEF по КАНАЛу \_**</span><span class="sxs-lookup"><span data-stu-id="e681b-161">**CHANNEL\_DEF**</span></span>](/windows/desktop/api/Pchannel/ns-pchannel-tagchannel_def)
</dt> <dt>

[<span data-ttu-id="e681b-162">**креатевиртуалчаннелс**</span><span class="sxs-lookup"><span data-stu-id="e681b-162">**CreateVirtualChannels**</span></span>](imstscax-createvirtualchannels.md)
</dt> <dt>

[<span data-ttu-id="e681b-163">**сетвиртуалчаннелоптионс**</span><span class="sxs-lookup"><span data-stu-id="e681b-163">**SetVirtualChannelOptions**</span></span>](imsrdpclient-setvirtualchanneloptions.md)
</dt> </dl>

 

 





