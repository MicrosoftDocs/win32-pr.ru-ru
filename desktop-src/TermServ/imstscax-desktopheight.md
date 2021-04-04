---
title: Имстскакс Десктофеигхт, свойство
description: Задает высоту текущего элемента управления в пикселях на начальном удаленном рабочем столе.
ms.assetid: 7071053b-bdd1-408b-ab69-965c504fafb0
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Десктофеигхт
- Службы удаленных рабочих столов свойства Десктофеигхт, интерфейс Имстскакс
- Службы удаленных рабочих столов интерфейса Имстскакс, свойство Десктофеигхт
- Службы удаленных рабочих столов свойства Десктофеигхт, интерфейс Имсрдпклиент
- Службы удаленных рабочих столов интерфейса Имсрдпклиент, свойство Десктофеигхт
- Службы удаленных рабочих столов свойства Десктофеигхт, интерфейс IMsRdpClient2
- Службы удаленных рабочих столов интерфейса IMsRdpClient2, свойство Десктофеигхт
- Службы удаленных рабочих столов свойства Десктофеигхт, интерфейс IMsRdpClient3
- Службы удаленных рабочих столов интерфейса IMsRdpClient3, свойство Десктофеигхт
- Службы удаленных рабочих столов свойства Десктофеигхт, интерфейс IMsRdpClient4
- Службы удаленных рабочих столов интерфейса IMsRdpClient4, свойство Десктофеигхт
- Службы удаленных рабочих столов свойства Десктофеигхт, интерфейс IMsRdpClient5
- Службы удаленных рабочих столов интерфейса IMsRdpClient5, свойство Десктофеигхт
- Службы удаленных рабочих столов свойства Десктофеигхт, интерфейс IMsRdpClient6
- Службы удаленных рабочих столов интерфейса IMsRdpClient6, свойство Десктофеигхт
- Службы удаленных рабочих столов свойства Десктофеигхт, интерфейс IMsRdpClient7
- Службы удаленных рабочих столов интерфейса IMsRdpClient7, свойство Десктофеигхт
- Службы удаленных рабочих столов свойства Десктофеигхт, интерфейс IMsRdpClient8
- Службы удаленных рабочих столов интерфейса IMsRdpClient8, свойство Десктофеигхт
- Службы удаленных рабочих столов свойства Десктофеигхт, интерфейс IMsRdpClient9
- Службы удаленных рабочих столов интерфейса IMsRdpClient9, свойство Десктофеигхт
topic_type:
- apiref
api_name:
- IMsTscAx.DesktopHeight
- IMsTscAx.get_DesktopHeight
- IMsTscAx.put_DesktopHeight
- IMsRdpClient.DesktopHeight
- IMsRdpClient.get_DesktopHeight
- IMsRdpClient.put_DesktopHeight
- IMsRdpClient2.DesktopHeight
- IMsRdpClient2.get_DesktopHeight
- IMsRdpClient2.put_DesktopHeight
- IMsRdpClient3.DesktopHeight
- IMsRdpClient3.get_DesktopHeight
- IMsRdpClient3.put_DesktopHeight
- IMsRdpClient4.DesktopHeight
- IMsRdpClient4.get_DesktopHeight
- IMsRdpClient4.put_DesktopHeight
- IMsRdpClient5.DesktopHeight
- IMsRdpClient5.get_DesktopHeight
- IMsRdpClient5.put_DesktopHeight
- IMsRdpClient6.DesktopHeight
- IMsRdpClient6.get_DesktopHeight
- IMsRdpClient6.put_DesktopHeight
- IMsRdpClient7.DesktopHeight
- IMsRdpClient7.get_DesktopHeight
- IMsRdpClient7.put_DesktopHeight
- IMsRdpClient8.DesktopHeight
- IMsRdpClient8.get_DesktopHeight
- IMsRdpClient8.put_DesktopHeight
- IMsRdpClient9.DesktopHeight
- IMsRdpClient9.get_DesktopHeight
- IMsRdpClient9.put_DesktopHeight
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb75467b35703420ce49fd99ea032b139d721505
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988940"
---
# <a name="imstscaxdesktopheight-property"></a><span data-ttu-id="7b73c-124">Имстскакс: свойство Есктофеигхт:D</span><span class="sxs-lookup"><span data-stu-id="7b73c-124">IMsTscAx::DesktopHeight property</span></span>

<span data-ttu-id="7b73c-125">Задает высоту текущего элемента управления в пикселях на начальном удаленном рабочем столе.</span><span class="sxs-lookup"><span data-stu-id="7b73c-125">Specifies the current control's height, in pixels, on the initial remote desktop.</span></span>

<span data-ttu-id="7b73c-126">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="7b73c-126">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b73c-127">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7b73c-127">Syntax</span></span>


```C++
HRESULT put_DesktopHeight(
  [in]  LONG newVal
);

HRESULT get_DesktopHeight(
  [out] LONG *pVal
);
```



## <a name="property-value"></a><span data-ttu-id="7b73c-128">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="7b73c-128">Property value</span></span>

<span data-ttu-id="7b73c-129">Новая высота (в пикселях).</span><span class="sxs-lookup"><span data-stu-id="7b73c-129">The new height, in pixels.</span></span>

## <a name="error-codes"></a><span data-ttu-id="7b73c-130">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="7b73c-130">Error codes</span></span>

<span data-ttu-id="7b73c-131">В случае успеха возвратите значение **\_ ОК** .</span><span class="sxs-lookup"><span data-stu-id="7b73c-131">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="7b73c-132">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7b73c-132">Remarks</span></span>

<span data-ttu-id="7b73c-133">Задание свойства **десктофеигхт** является необязательным, но оно должно быть задано перед вызовом метода [**Connect**](imstscax-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="7b73c-133">Setting the **DesktopHeight** property is optional, but it must be set before calling the [**Connect**](imstscax-connect.md) method.</span></span> <span data-ttu-id="7b73c-134">Если высота рабочего стола не указана или имеет значение 0, высота рабочего стола устанавливается равным высоте элемента управления.</span><span class="sxs-lookup"><span data-stu-id="7b73c-134">If a desktop height is not specified, or is set to zero, the desktop height is set to the height of the control.</span></span> <span data-ttu-id="7b73c-135">Минимальное и максимальное значения зависят от версии операционной системы клиента удаленный рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="7b73c-135">The minimum and maximum values are dependent upon the operating system version of the Remote Desktop client.</span></span>

<dl> <dt>

<span data-ttu-id="7b73c-136"><span id="_"></span>Windows 8 или Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7b73c-136"><span id="_"></span>Windows 8/Windows Server 2012</span></span>
</dt> <dd>

<span data-ttu-id="7b73c-137">200 минимум, максимум 8192</span><span class="sxs-lookup"><span data-stu-id="7b73c-137">200 minimum, 8192 maximum</span></span>

</dd> <dt>

<span data-ttu-id="7b73c-138"><span id="_"></span>Windows 7 или Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7b73c-138"><span id="_"></span>Windows 7/Windows Server 2008</span></span>
</dt> <dd>

<span data-ttu-id="7b73c-139">200 минимум, максимум 2048</span><span class="sxs-lookup"><span data-stu-id="7b73c-139">200 minimum, 2048 maximum</span></span>

</dd> <dt>

<span data-ttu-id="7b73c-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7b73c-140">Windows Vista</span></span>
</dt> <dd>

<span data-ttu-id="7b73c-141">200 минимум, максимум 1200</span><span class="sxs-lookup"><span data-stu-id="7b73c-141">200 minimum, 1200 maximum</span></span>

</dd> </dl>

<span data-ttu-id="7b73c-142">После установки соединения любые изменения высоты элемента управления не изменяют высоту удаленного рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="7b73c-142">After a connection is established, any changes to the control's height do not change the height of the remote desktop.</span></span> <span data-ttu-id="7b73c-143">Вместо этого элемент управления выводит полосу прокрутки или центрирует удаленный рабочий стол по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="7b73c-143">Instead, the control brings up scroll bars or centers the remote desktop, as appropriate.</span></span> <span data-ttu-id="7b73c-144">Чтобы изменить размер рабочего стола активного подключения, используйте метод [**IMsRdpClient8:: Reconnect**](imsrdpclient8-reconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="7b73c-144">To change the desktop size of an active connection, use the [**IMsRdpClient8::Reconnect**](imsrdpclient8-reconnect.md) method.</span></span>

<span data-ttu-id="7b73c-145">Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="7b73c-145">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7b73c-146">Требования</span><span class="sxs-lookup"><span data-stu-id="7b73c-146">Requirements</span></span>



| <span data-ttu-id="7b73c-147">Требование</span><span class="sxs-lookup"><span data-stu-id="7b73c-147">Requirement</span></span> | <span data-ttu-id="7b73c-148">Значение</span><span class="sxs-lookup"><span data-stu-id="7b73c-148">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7b73c-149">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7b73c-149">Minimum supported client</span></span><br/> | <span data-ttu-id="7b73c-150">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7b73c-150">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="7b73c-151">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7b73c-151">Minimum supported server</span></span><br/> | <span data-ttu-id="7b73c-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7b73c-152">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="7b73c-153">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="7b73c-153">Type library</span></span><br/>             | <dl> <span data-ttu-id="7b73c-154"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7b73c-154"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="7b73c-155">DLL</span><span class="sxs-lookup"><span data-stu-id="7b73c-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7b73c-156"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7b73c-156"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="7b73c-157">IID</span><span class="sxs-lookup"><span data-stu-id="7b73c-157">IID</span></span><br/>                      | <span data-ttu-id="7b73c-158">IID \_ имстскакс определен как 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="7b73c-158">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="7b73c-159">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7b73c-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b73c-160">**имсрдпклиент**</span><span class="sxs-lookup"><span data-stu-id="7b73c-160">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="7b73c-161">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="7b73c-161">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="7b73c-162">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="7b73c-162">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="7b73c-163">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="7b73c-163">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="7b73c-164">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="7b73c-164">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="7b73c-165">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="7b73c-165">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="7b73c-166">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="7b73c-166">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="7b73c-167">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="7b73c-167">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="7b73c-168">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="7b73c-168">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="7b73c-169">**имстскакс**</span><span class="sxs-lookup"><span data-stu-id="7b73c-169">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> </dl>

 

 





