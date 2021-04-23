---
title: Метод отключения Имстскакс
description: Отключает активное подключение.
ms.assetid: 9fcffd45-b293-4650-be8f-1b0d01d592a2
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода отключения
- Метод Disconnect службы удаленных рабочих столов, интерфейс Имстскакс
- Службы удаленных рабочих столов интерфейса Имстскакс, метод Disconnect
- Метод Disconnect службы удаленных рабочих столов, интерфейс Имсрдпклиент
- Службы удаленных рабочих столов интерфейса Имсрдпклиент, метод Disconnect
- Метод Disconnect службы удаленных рабочих столов, интерфейс IMsRdpClient2
- Службы удаленных рабочих столов интерфейса IMsRdpClient2, метод Disconnect
- Метод Disconnect службы удаленных рабочих столов, интерфейс IMsRdpClient3
- Службы удаленных рабочих столов интерфейса IMsRdpClient3, метод Disconnect
- Метод Disconnect службы удаленных рабочих столов, интерфейс IMsRdpClient4
- Службы удаленных рабочих столов интерфейса IMsRdpClient4, метод Disconnect
- Метод Disconnect службы удаленных рабочих столов, интерфейс IMsRdpClient5
- Службы удаленных рабочих столов интерфейса IMsRdpClient5, метод Disconnect
- Метод Disconnect службы удаленных рабочих столов, интерфейс IMsRdpClient6
- Службы удаленных рабочих столов интерфейса IMsRdpClient6, метод Disconnect
- Метод Disconnect службы удаленных рабочих столов, интерфейс IMsRdpClient7
- Службы удаленных рабочих столов интерфейса IMsRdpClient7, метод Disconnect
- Метод Disconnect службы удаленных рабочих столов, интерфейс IMsRdpClient8
- Службы удаленных рабочих столов интерфейса IMsRdpClient8, метод Disconnect
- Метод Disconnect службы удаленных рабочих столов, интерфейс IMsRdpClient9
- Службы удаленных рабочих столов интерфейса IMsRdpClient9, метод Disconnect
topic_type:
- apiref
api_name:
- IMsTscAx.Disconnect
- IMsRdpClient.Disconnect
- IMsRdpClient2.Disconnect
- IMsRdpClient3.Disconnect
- IMsRdpClient4.Disconnect
- IMsRdpClient5.Disconnect
- IMsRdpClient6.Disconnect
- IMsRdpClient7.Disconnect
- IMsRdpClient8.Disconnect
- IMsRdpClient9.Disconnect
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d4f1545a8244209c0b4fa8267fcc8ce2a41e090
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534565"
---
# <a name="imstscaxdisconnect-method"></a><span data-ttu-id="e056b-124">Имстскакс::D метода соединения</span><span class="sxs-lookup"><span data-stu-id="e056b-124">IMsTscAx::Disconnect method</span></span>

<span data-ttu-id="e056b-125">Отключает активное подключение.</span><span class="sxs-lookup"><span data-stu-id="e056b-125">Disconnects the active connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="e056b-126">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e056b-126">Syntax</span></span>


```C++
HRESULT Disconnect();
```



## <a name="parameters"></a><span data-ttu-id="e056b-127">Параметры</span><span class="sxs-lookup"><span data-stu-id="e056b-127">Parameters</span></span>

<span data-ttu-id="e056b-128">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="e056b-128">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e056b-129">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e056b-129">Return value</span></span>

<span data-ttu-id="e056b-130">В случае успеха возвратите значение **\_ ОК** .</span><span class="sxs-lookup"><span data-stu-id="e056b-130">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="e056b-131">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e056b-131">Remarks</span></span>

<span data-ttu-id="e056b-132">Этот метод возвращает значение ошибки сбоя, если оно вызывается, когда элемент управления не подключен.</span><span class="sxs-lookup"><span data-stu-id="e056b-132">This method returns a failure error value if it is called when the control is not connected.</span></span>

<span data-ttu-id="e056b-133">Можно также отключить элемент управления, закрыв его главное окно.</span><span class="sxs-lookup"><span data-stu-id="e056b-133">It is also possible to disconnect the control by closing its main window.</span></span> <span data-ttu-id="e056b-134">Например, если элемент управления размещается на веб-странице, не обязательно вызывать этот метод перед тем, как покинуть страницу. Закрытие элемента управления активирует отключение.</span><span class="sxs-lookup"><span data-stu-id="e056b-134">For example, if the control is hosted in a webpage, it is not necessary to call this method before leaving the page; the closing of the control triggers a disconnection.</span></span>

<span data-ttu-id="e056b-135">Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="e056b-135">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e056b-136">Требования</span><span class="sxs-lookup"><span data-stu-id="e056b-136">Requirements</span></span>



| <span data-ttu-id="e056b-137">Требование</span><span class="sxs-lookup"><span data-stu-id="e056b-137">Requirement</span></span> | <span data-ttu-id="e056b-138">Значение</span><span class="sxs-lookup"><span data-stu-id="e056b-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e056b-139">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e056b-139">Minimum supported client</span></span><br/> | <span data-ttu-id="e056b-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e056b-140">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="e056b-141">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e056b-141">Minimum supported server</span></span><br/> | <span data-ttu-id="e056b-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e056b-142">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="e056b-143">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="e056b-143">Type library</span></span><br/>             | <dl> <span data-ttu-id="e056b-144"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e056b-144"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="e056b-145">DLL</span><span class="sxs-lookup"><span data-stu-id="e056b-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e056b-146"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e056b-146"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="e056b-147">IID</span><span class="sxs-lookup"><span data-stu-id="e056b-147">IID</span></span><br/>                      | <span data-ttu-id="e056b-148">IID \_ имстскакс определен как 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="e056b-148">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="e056b-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e056b-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e056b-150">**имсрдпклиент**</span><span class="sxs-lookup"><span data-stu-id="e056b-150">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="e056b-151">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="e056b-151">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="e056b-152">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="e056b-152">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="e056b-153">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="e056b-153">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="e056b-154">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="e056b-154">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="e056b-155">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="e056b-155">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="e056b-156">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="e056b-156">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="e056b-157">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="e056b-157">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="e056b-158">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="e056b-158">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="e056b-159">**Подключение**</span><span class="sxs-lookup"><span data-stu-id="e056b-159">**Connect**</span></span>](imstscax-connect.md)
</dt> <dt>

[<span data-ttu-id="e056b-160">**имстскакс**</span><span class="sxs-lookup"><span data-stu-id="e056b-160">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> </dl>

 

 





