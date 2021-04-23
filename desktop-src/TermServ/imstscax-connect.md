---
title: Имстскакс Connect, метод
description: Инициирует соединение с использованием свойств, заданных в данный момент в элементе управления.
ms.assetid: 9bcbdc13-6c66-4737-82a4-98329f173743
ms.tgt_platform: multiple
keywords:
- Метод Connect службы удаленных рабочих столов
- Метод Connect службы удаленных рабочих столов, интерфейс Имстскакс
- Интерфейс Имстскакс службы удаленных рабочих столов, метод Connect
- Метод Connect службы удаленных рабочих столов, интерфейс Имсрдпклиент
- Интерфейс Имсрдпклиент службы удаленных рабочих столов, метод Connect
- Метод Connect службы удаленных рабочих столов, интерфейс IMsRdpClient2
- Интерфейс IMsRdpClient2 службы удаленных рабочих столов, метод Connect
- Метод Connect службы удаленных рабочих столов, интерфейс IMsRdpClient3
- Интерфейс IMsRdpClient3 службы удаленных рабочих столов, метод Connect
- Метод Connect службы удаленных рабочих столов, интерфейс IMsRdpClient4
- Интерфейс IMsRdpClient4 службы удаленных рабочих столов, метод Connect
- Метод Connect службы удаленных рабочих столов, интерфейс IMsRdpClient5
- Интерфейс IMsRdpClient5 службы удаленных рабочих столов, метод Connect
- Метод Connect службы удаленных рабочих столов, интерфейс IMsRdpClient6
- Интерфейс IMsRdpClient6 службы удаленных рабочих столов, метод Connect
- Метод Connect службы удаленных рабочих столов, интерфейс IMsRdpClient7
- Интерфейс IMsRdpClient7 службы удаленных рабочих столов, метод Connect
- Метод Connect службы удаленных рабочих столов, интерфейс IMsRdpClient8
- Интерфейс IMsRdpClient8 службы удаленных рабочих столов, метод Connect
- Метод Connect службы удаленных рабочих столов, интерфейс IMsRdpClient9
- Интерфейс IMsRdpClient9 службы удаленных рабочих столов, метод Connect
topic_type:
- apiref
api_name:
- IMsTscAx.Connect
- IMsRdpClient.Connect
- IMsRdpClient2.Connect
- IMsRdpClient3.Connect
- IMsRdpClient4.Connect
- IMsRdpClient5.Connect
- IMsRdpClient6.Connect
- IMsRdpClient7.Connect
- IMsRdpClient8.Connect
- IMsRdpClient9.Connect
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c267b24c3dd27dd875d895674d98e1350f757c82
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988400"
---
# <a name="imstscaxconnect-method"></a><span data-ttu-id="a68e0-124">Метод Имстскакс:: Connect</span><span class="sxs-lookup"><span data-stu-id="a68e0-124">IMsTscAx::Connect method</span></span>

<span data-ttu-id="a68e0-125">Инициирует соединение с использованием свойств, заданных в данный момент в элементе управления.</span><span class="sxs-lookup"><span data-stu-id="a68e0-125">Initiates a connection using the properties currently set on the control.</span></span>

## <a name="syntax"></a><span data-ttu-id="a68e0-126">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a68e0-126">Syntax</span></span>


```C++
HRESULT Connect();
```



## <a name="parameters"></a><span data-ttu-id="a68e0-127">Параметры</span><span class="sxs-lookup"><span data-stu-id="a68e0-127">Parameters</span></span>

<span data-ttu-id="a68e0-128">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="a68e0-128">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a68e0-129">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a68e0-129">Return value</span></span>

<span data-ttu-id="a68e0-130">В случае успеха возвратите значение **\_ ОК** .</span><span class="sxs-lookup"><span data-stu-id="a68e0-130">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="a68e0-131">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a68e0-131">Remarks</span></span>

<span data-ttu-id="a68e0-132">Единственным обязательным свойством является имя сервера.</span><span class="sxs-lookup"><span data-stu-id="a68e0-132">The only required property is the server name.</span></span> <span data-ttu-id="a68e0-133">См. свойство [**Server**](imstscax-server.md) .</span><span class="sxs-lookup"><span data-stu-id="a68e0-133">Refer to the [**Server**](imstscax-server.md) property.</span></span>

<span data-ttu-id="a68e0-134">Элемент управления подключается асинхронно, поэтому возврат из вызова соединения указывает только на то, что соединение было инициировано успешно, но не завершено.</span><span class="sxs-lookup"><span data-stu-id="a68e0-134">The control connects asynchronously, so a return from a Connect call indicates only that the connection has been initiated successfully, not that it has been completed.</span></span> <span data-ttu-id="a68e0-135">Необходимо ответить на события в интерфейсе [**имстскаксевентс**](imstscaxevents-interface.md) , чтобы определить, когда элемент управления успешно подключен (или был отключен).</span><span class="sxs-lookup"><span data-stu-id="a68e0-135">You should respond to events on the [**IMsTscAxEvents**](imstscaxevents-interface.md) interface to determine when the control has successfully connected (or has been disconnected.)</span></span>

<span data-ttu-id="a68e0-136">Этот метод возвращает **E \_ Fail** , если он вызывается, когда элемент управления уже подключен или находится в состоянии подключения.</span><span class="sxs-lookup"><span data-stu-id="a68e0-136">This method returns **E\_FAIL** if it is called while the control is already connected or in the connecting state.</span></span>

<span data-ttu-id="a68e0-137">После вызова метода **Connect** большая часть свойств элемента управления больше не может быть задана до тех пор, пока элемент управления не вернется в состояние DISCONNECTED.</span><span class="sxs-lookup"><span data-stu-id="a68e0-137">After **Connect** has been called, most of the control properties can no longer be set until the control returns to the disconnected state.</span></span>

<span data-ttu-id="a68e0-138">Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="a68e0-138">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a68e0-139">Требования</span><span class="sxs-lookup"><span data-stu-id="a68e0-139">Requirements</span></span>



| <span data-ttu-id="a68e0-140">Требование</span><span class="sxs-lookup"><span data-stu-id="a68e0-140">Requirement</span></span> | <span data-ttu-id="a68e0-141">Значение</span><span class="sxs-lookup"><span data-stu-id="a68e0-141">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a68e0-142">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a68e0-142">Minimum supported client</span></span><br/> | <span data-ttu-id="a68e0-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a68e0-143">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="a68e0-144">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a68e0-144">Minimum supported server</span></span><br/> | <span data-ttu-id="a68e0-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a68e0-145">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="a68e0-146">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="a68e0-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="a68e0-147"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a68e0-147"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="a68e0-148">DLL</span><span class="sxs-lookup"><span data-stu-id="a68e0-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a68e0-149"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a68e0-149"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="a68e0-150">IID</span><span class="sxs-lookup"><span data-stu-id="a68e0-150">IID</span></span><br/>                      | <span data-ttu-id="a68e0-151">IID \_ имстскакс определен как 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="a68e0-151">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="a68e0-152">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a68e0-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a68e0-153">**имсрдпклиент**</span><span class="sxs-lookup"><span data-stu-id="a68e0-153">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="a68e0-154">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="a68e0-154">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="a68e0-155">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="a68e0-155">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="a68e0-156">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="a68e0-156">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="a68e0-157">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="a68e0-157">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="a68e0-158">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="a68e0-158">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="a68e0-159">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="a68e0-159">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="a68e0-160">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="a68e0-160">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="a68e0-161">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="a68e0-161">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="a68e0-162">**Отключение**</span><span class="sxs-lookup"><span data-stu-id="a68e0-162">**Disconnect**</span></span>](imstscax-disconnect.md)
</dt> <dt>

[<span data-ttu-id="a68e0-163">**имстскакс**</span><span class="sxs-lookup"><span data-stu-id="a68e0-163">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> </dl>

 

 





