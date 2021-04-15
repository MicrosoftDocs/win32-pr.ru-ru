---
title: Имстскакс Креатевиртуалчаннелс, метод
description: Создает объект виртуального канала на стороне клиента для каждого указанного имени виртуального канала.
ms.assetid: 3afd2f1c-abd5-4f85-93fb-6d1173f09b07
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Креатевиртуалчаннелс
- Службы удаленных рабочих столов метода Креатевиртуалчаннелс, интерфейс Имстскакс
- Службы удаленных рабочих столов интерфейса Имстскакс, метод Креатевиртуалчаннелс
- Службы удаленных рабочих столов метода Креатевиртуалчаннелс, интерфейс Имсрдпклиент
- Службы удаленных рабочих столов интерфейса Имсрдпклиент, метод Креатевиртуалчаннелс
- Службы удаленных рабочих столов метода Креатевиртуалчаннелс, интерфейс IMsRdpClient2
- Службы удаленных рабочих столов интерфейса IMsRdpClient2, метод Креатевиртуалчаннелс
- Службы удаленных рабочих столов метода Креатевиртуалчаннелс, интерфейс IMsRdpClient3
- Службы удаленных рабочих столов интерфейса IMsRdpClient3, метод Креатевиртуалчаннелс
- Службы удаленных рабочих столов метода Креатевиртуалчаннелс, интерфейс IMsRdpClient4
- Службы удаленных рабочих столов интерфейса IMsRdpClient4, метод Креатевиртуалчаннелс
- Службы удаленных рабочих столов метода Креатевиртуалчаннелс, интерфейс IMsRdpClient5
- Службы удаленных рабочих столов интерфейса IMsRdpClient5, метод Креатевиртуалчаннелс
- Службы удаленных рабочих столов метода Креатевиртуалчаннелс, интерфейс IMsRdpClient6
- Службы удаленных рабочих столов интерфейса IMsRdpClient6, метод Креатевиртуалчаннелс
- Службы удаленных рабочих столов метода Креатевиртуалчаннелс, интерфейс IMsRdpClient7
- Службы удаленных рабочих столов интерфейса IMsRdpClient7, метод Креатевиртуалчаннелс
- Службы удаленных рабочих столов метода Креатевиртуалчаннелс, интерфейс IMsRdpClient8
- Службы удаленных рабочих столов интерфейса IMsRdpClient8, метод Креатевиртуалчаннелс
- Службы удаленных рабочих столов метода Креатевиртуалчаннелс, интерфейс IMsRdpClient9
- Службы удаленных рабочих столов интерфейса IMsRdpClient9, метод Креатевиртуалчаннелс
topic_type:
- apiref
api_name:
- IMsTscAx.CreateVirtualChannels
- IMsRdpClient.CreateVirtualChannels
- IMsRdpClient2.CreateVirtualChannels
- IMsRdpClient3.CreateVirtualChannels
- IMsRdpClient4.CreateVirtualChannels
- IMsRdpClient5.CreateVirtualChannels
- IMsRdpClient6.CreateVirtualChannels
- IMsRdpClient7.CreateVirtualChannels
- IMsRdpClient8.CreateVirtualChannels
- IMsRdpClient9.CreateVirtualChannels
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d59c185763ddd3685e5e566f88e26a6aa6211b4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491625"
---
# <a name="imstscaxcreatevirtualchannels-method"></a><span data-ttu-id="159cf-124">Метод Имстскакс:: Креатевиртуалчаннелс</span><span class="sxs-lookup"><span data-stu-id="159cf-124">IMsTscAx::CreateVirtualChannels method</span></span>

<span data-ttu-id="159cf-125">Создает объект виртуального канала на стороне клиента для каждого указанного имени виртуального канала.</span><span class="sxs-lookup"><span data-stu-id="159cf-125">Creates a client-side virtual channel object for each specified virtual channel name.</span></span>

## <a name="syntax"></a><span data-ttu-id="159cf-126">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="159cf-126">Syntax</span></span>


```C++
HRESULT CreateVirtualChannels(
  [in] BSTR newVal
);
```



## <a name="parameters"></a><span data-ttu-id="159cf-127">Параметры</span><span class="sxs-lookup"><span data-stu-id="159cf-127">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="159cf-128">*неввал* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="159cf-128">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="159cf-129">Список допустимых имен виртуальных каналов с разделителями-запятыми.</span><span class="sxs-lookup"><span data-stu-id="159cf-129">A comma-separated list of valid virtual channel names.</span></span> <span data-ttu-id="159cf-130">Длина каждого имени в списке может быть не меньше одного, а не более семи алфавитных символов.</span><span class="sxs-lookup"><span data-stu-id="159cf-130">The length of each name in this list can be a minimum of one and a maximum of seven alphabetical characters.</span></span> <span data-ttu-id="159cf-131">Длина всей строки может быть как минимум одной длиной не более 300 алфавитных символов.</span><span class="sxs-lookup"><span data-stu-id="159cf-131">The length of the entire string can be a minimum of one and a maximum of 300 alphabetical characters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="159cf-132">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="159cf-132">Return value</span></span>

<span data-ttu-id="159cf-133">При успешном выполнении возвращает значение **\_ ОК** .</span><span class="sxs-lookup"><span data-stu-id="159cf-133">Returns **S\_OK** if successful.</span></span> <span data-ttu-id="159cf-134">Возвращает значение **E \_ INVALIDARG** , если переданный параметр не соответствует заданным критериям.</span><span class="sxs-lookup"><span data-stu-id="159cf-134">Returns **E\_INVALIDARG** if the parameter that is passed does not meet the criteria that is specified.</span></span>

## <a name="remarks"></a><span data-ttu-id="159cf-135">Комментарии</span><span class="sxs-lookup"><span data-stu-id="159cf-135">Remarks</span></span>

<span data-ttu-id="159cf-136">Вызовите этот метод перед вызовом метода [**Connect**](imstscax-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="159cf-136">Call this method before calling the [**Connect**](imstscax-connect.md) method.</span></span>

<span data-ttu-id="159cf-137">Сведения об ограничениях именования виртуальных каналов см. в статье [Регистрация клиента виртуального канала](virtual-channel-client-registration.md) .</span><span class="sxs-lookup"><span data-stu-id="159cf-137">Refer to [Virtual Channel Client Registration](virtual-channel-client-registration.md) for information about virtual channel naming restrictions.</span></span>

<span data-ttu-id="159cf-138">Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="159cf-138">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="159cf-139">Требования</span><span class="sxs-lookup"><span data-stu-id="159cf-139">Requirements</span></span>



| <span data-ttu-id="159cf-140">Требование</span><span class="sxs-lookup"><span data-stu-id="159cf-140">Requirement</span></span> | <span data-ttu-id="159cf-141">Значение</span><span class="sxs-lookup"><span data-stu-id="159cf-141">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="159cf-142">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="159cf-142">Minimum supported client</span></span><br/> | <span data-ttu-id="159cf-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="159cf-143">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="159cf-144">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="159cf-144">Minimum supported server</span></span><br/> | <span data-ttu-id="159cf-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="159cf-145">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="159cf-146">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="159cf-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="159cf-147"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="159cf-147"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="159cf-148">DLL</span><span class="sxs-lookup"><span data-stu-id="159cf-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="159cf-149"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="159cf-149"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="159cf-150">IID</span><span class="sxs-lookup"><span data-stu-id="159cf-150">IID</span></span><br/>                      | <span data-ttu-id="159cf-151">IID \_ имстскакс определен как 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="159cf-151">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="159cf-152">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="159cf-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="159cf-153">**имсрдпклиент**</span><span class="sxs-lookup"><span data-stu-id="159cf-153">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="159cf-154">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="159cf-154">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="159cf-155">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="159cf-155">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="159cf-156">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="159cf-156">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="159cf-157">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="159cf-157">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="159cf-158">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="159cf-158">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="159cf-159">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="159cf-159">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="159cf-160">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="159cf-160">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="159cf-161">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="159cf-161">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="159cf-162">**имстскакс**</span><span class="sxs-lookup"><span data-stu-id="159cf-162">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> </dl>

 

 





