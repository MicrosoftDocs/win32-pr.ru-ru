---
title: Свойство Имстскакс Connected (Тсвиртуалчаннелс. h)
description: Возвращает состояние соединения текущего элемента управления.
ms.assetid: f6f65ef6-d321-4362-b192-1ea5ffd2b712
ms.tgt_platform: multiple
keywords:
- Подключенное свойство службы удаленных рабочих столов
- Подключенное свойство службы удаленных рабочих столов, интерфейс Имстскакс
- Службы удаленных рабочих столов интерфейса Имстскакс, подключенное свойство
- Подключенное свойство службы удаленных рабочих столов, интерфейс Имсрдпклиент
- Службы удаленных рабочих столов интерфейса Имсрдпклиент, подключенное свойство
- Подключенное свойство службы удаленных рабочих столов, интерфейс IMsRdpClient2
- Службы удаленных рабочих столов интерфейса IMsRdpClient2, подключенное свойство
- Подключенное свойство службы удаленных рабочих столов, интерфейс IMsRdpClient3
- Службы удаленных рабочих столов интерфейса IMsRdpClient3, подключенное свойство
- Подключенное свойство службы удаленных рабочих столов, интерфейс IMsRdpClient4
- Службы удаленных рабочих столов интерфейса IMsRdpClient4, подключенное свойство
- Подключенное свойство службы удаленных рабочих столов, интерфейс IMsRdpClient5
- Службы удаленных рабочих столов интерфейса IMsRdpClient5, подключенное свойство
- Подключенное свойство службы удаленных рабочих столов, интерфейс IMsRdpClient6
- Службы удаленных рабочих столов интерфейса IMsRdpClient6, подключенное свойство
- Подключенное свойство службы удаленных рабочих столов, интерфейс IMsRdpClient7
- Службы удаленных рабочих столов интерфейса IMsRdpClient7, подключенное свойство
- Подключенное свойство службы удаленных рабочих столов, интерфейс IMsRdpClient8
- Службы удаленных рабочих столов интерфейса IMsRdpClient8, подключенное свойство
- Подключенное свойство службы удаленных рабочих столов, интерфейс IMsRdpClient9
- Службы удаленных рабочих столов интерфейса IMsRdpClient9, подключенное свойство
topic_type:
- apiref
api_name:
- IMsTscAx.Connected
- IMsTscAx.get_Connected
- IMsRdpClient.Connected
- IMsRdpClient.get_Connected
- IMsRdpClient2.Connected
- IMsRdpClient2.get_Connected
- IMsRdpClient3.Connected
- IMsRdpClient3.get_Connected
- IMsRdpClient4.Connected
- IMsRdpClient4.get_Connected
- IMsRdpClient5.Connected
- IMsRdpClient5.get_Connected
- IMsRdpClient6.Connected
- IMsRdpClient6.get_Connected
- IMsRdpClient7.Connected
- IMsRdpClient7.get_Connected
- IMsRdpClient8.Connected
- IMsRdpClient8.get_Connected
- IMsRdpClient9.Connected
- IMsRdpClient9.get_Connected
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 883ba670ab9a6b5d4e4a065c35f263734929ba02
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105682144"
---
# <a name="imstscaxconnected-property"></a><span data-ttu-id="11951-124">Свойство Имстскакс:: Connected</span><span class="sxs-lookup"><span data-stu-id="11951-124">IMsTscAx::Connected property</span></span>

<span data-ttu-id="11951-125">Возвращает состояние соединения текущего элемента управления.</span><span class="sxs-lookup"><span data-stu-id="11951-125">Retrieves the connection state of the current control.</span></span>

<span data-ttu-id="11951-126">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="11951-126">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="11951-127">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="11951-127">Syntax</span></span>


```C++
HRESULT get_Connected(
  [out] short *pIsConnected
);
```



## <a name="property-value"></a><span data-ttu-id="11951-128">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="11951-128">Property value</span></span>

<span data-ttu-id="11951-129">Указывает состояние соединения элемента управления.</span><span class="sxs-lookup"><span data-stu-id="11951-129">Indicates the connection state of the control.</span></span> <span data-ttu-id="11951-130">Это может быть одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="11951-130">This can be one of the following values.</span></span>

<dt>

<span data-ttu-id="11951-131">0</span><span class="sxs-lookup"><span data-stu-id="11951-131">0</span></span>
</dt> <dd>

<span data-ttu-id="11951-132">Элемент управления не подключен.</span><span class="sxs-lookup"><span data-stu-id="11951-132">The control is not connected.</span></span>

</dd> <dt>

<span data-ttu-id="11951-133">1</span><span class="sxs-lookup"><span data-stu-id="11951-133">1</span></span>
</dt> <dd>

<span data-ttu-id="11951-134">Элемент управления подключен.</span><span class="sxs-lookup"><span data-stu-id="11951-134">The control is connected.</span></span>

</dd> <dt>

<span data-ttu-id="11951-135">2</span><span class="sxs-lookup"><span data-stu-id="11951-135">2</span></span>
</dt> <dd>

<span data-ttu-id="11951-136">Элемент управления устанавливает соединение.</span><span class="sxs-lookup"><span data-stu-id="11951-136">The control is establishing a connection.</span></span>

</dd> </dl>

## <a name="error-codes"></a><span data-ttu-id="11951-137">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="11951-137">Error codes</span></span>

<span data-ttu-id="11951-138">В случае успеха возвратите значение **\_ ОК** .</span><span class="sxs-lookup"><span data-stu-id="11951-138">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="11951-139">Комментарии</span><span class="sxs-lookup"><span data-stu-id="11951-139">Remarks</span></span>

<span data-ttu-id="11951-140">Предпочтительным способом определения состояния соединения элемента управления является реагирование на события соединения в [**имстскаксевентс**](imstscaxevents-interface.md).</span><span class="sxs-lookup"><span data-stu-id="11951-140">The preferred way to determine the control's connection state is to respond to the connection events in [**IMsTscAxEvents**](imstscaxevents-interface.md).</span></span>

<span data-ttu-id="11951-141">Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="11951-141">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="11951-142">Требования</span><span class="sxs-lookup"><span data-stu-id="11951-142">Requirements</span></span>



| <span data-ttu-id="11951-143">Требование</span><span class="sxs-lookup"><span data-stu-id="11951-143">Requirement</span></span> | <span data-ttu-id="11951-144">Значение</span><span class="sxs-lookup"><span data-stu-id="11951-144">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11951-145">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="11951-145">Minimum supported client</span></span><br/> | <span data-ttu-id="11951-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="11951-146">Windows Vista</span></span><br/>                                                                       |
| <span data-ttu-id="11951-147">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="11951-147">Minimum supported server</span></span><br/> | <span data-ttu-id="11951-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="11951-148">Windows Server 2008</span></span><br/>                                                                 |
| <span data-ttu-id="11951-149">Header</span><span class="sxs-lookup"><span data-stu-id="11951-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="11951-150"><dt>Тсвиртуалчаннелс. h</dt></span><span class="sxs-lookup"><span data-stu-id="11951-150"><dt>Tsvirtualchannels.h</dt></span></span> </dl> |
| <span data-ttu-id="11951-151">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="11951-151">Type library</span></span><br/>             | <dl> <span data-ttu-id="11951-152"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="11951-152"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="11951-153">DLL</span><span class="sxs-lookup"><span data-stu-id="11951-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="11951-154"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="11951-154"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="11951-155">IID</span><span class="sxs-lookup"><span data-stu-id="11951-155">IID</span></span><br/>                      | <span data-ttu-id="11951-156">IID \_ имстскакс определен как 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="11951-156">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>                    |



## <a name="see-also"></a><span data-ttu-id="11951-157">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="11951-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11951-158">**имсрдпклиент**</span><span class="sxs-lookup"><span data-stu-id="11951-158">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="11951-159">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="11951-159">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="11951-160">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="11951-160">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="11951-161">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="11951-161">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="11951-162">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="11951-162">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="11951-163">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="11951-163">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="11951-164">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="11951-164">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="11951-165">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="11951-165">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="11951-166">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="11951-166">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="11951-167">**имстскакс**</span><span class="sxs-lookup"><span data-stu-id="11951-167">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> </dl>

 

 





