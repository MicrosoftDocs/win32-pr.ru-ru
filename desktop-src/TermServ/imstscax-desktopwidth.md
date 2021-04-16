---
title: Имстскакс Десктопвидс, свойство
description: Задает ширину текущего элемента управления в пикселях на начальном удаленном рабочем столе.
ms.assetid: 3b349f6c-d068-4047-b8b5-29d022894729
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Десктопвидс
- Службы удаленных рабочих столов свойства Десктопвидс, интерфейс Имстскакс
- Службы удаленных рабочих столов интерфейса Имстскакс, свойство Десктопвидс
- Службы удаленных рабочих столов свойства Десктопвидс, интерфейс Имсрдпклиент
- Службы удаленных рабочих столов интерфейса Имсрдпклиент, свойство Десктопвидс
- Службы удаленных рабочих столов свойства Десктопвидс, интерфейс IMsRdpClient2
- Службы удаленных рабочих столов интерфейса IMsRdpClient2, свойство Десктопвидс
- Службы удаленных рабочих столов свойства Десктопвидс, интерфейс IMsRdpClient3
- Службы удаленных рабочих столов интерфейса IMsRdpClient3, свойство Десктопвидс
- Службы удаленных рабочих столов свойства Десктопвидс, интерфейс IMsRdpClient4
- Службы удаленных рабочих столов интерфейса IMsRdpClient4, свойство Десктопвидс
- Службы удаленных рабочих столов свойства Десктопвидс, интерфейс IMsRdpClient5
- Службы удаленных рабочих столов интерфейса IMsRdpClient5, свойство Десктопвидс
- Службы удаленных рабочих столов свойства Десктопвидс, интерфейс IMsRdpClient6
- Службы удаленных рабочих столов интерфейса IMsRdpClient6, свойство Десктопвидс
- Службы удаленных рабочих столов свойства Десктопвидс, интерфейс IMsRdpClient7
- Службы удаленных рабочих столов интерфейса IMsRdpClient7, свойство Десктопвидс
- Службы удаленных рабочих столов свойства Десктопвидс, интерфейс IMsRdpClient8
- Службы удаленных рабочих столов интерфейса IMsRdpClient8, свойство Десктопвидс
- Службы удаленных рабочих столов свойства Десктопвидс, интерфейс IMsRdpClient9
- Службы удаленных рабочих столов интерфейса IMsRdpClient9, свойство Десктопвидс
topic_type:
- apiref
api_name:
- IMsTscAx.DesktopWidth
- IMsTscAx.get_DesktopWidth
- IMsTscAx.put_DesktopWidth
- IMsRdpClient.DesktopWidth
- IMsRdpClient.get_DesktopWidth
- IMsRdpClient.put_DesktopWidth
- IMsRdpClient2.DesktopWidth
- IMsRdpClient2.get_DesktopWidth
- IMsRdpClient2.put_DesktopWidth
- IMsRdpClient3.DesktopWidth
- IMsRdpClient3.get_DesktopWidth
- IMsRdpClient3.put_DesktopWidth
- IMsRdpClient4.DesktopWidth
- IMsRdpClient4.get_DesktopWidth
- IMsRdpClient4.put_DesktopWidth
- IMsRdpClient5.DesktopWidth
- IMsRdpClient5.get_DesktopWidth
- IMsRdpClient5.put_DesktopWidth
- IMsRdpClient6.DesktopWidth
- IMsRdpClient6.get_DesktopWidth
- IMsRdpClient6.put_DesktopWidth
- IMsRdpClient7.DesktopWidth
- IMsRdpClient7.get_DesktopWidth
- IMsRdpClient7.put_DesktopWidth
- IMsRdpClient8.DesktopWidth
- IMsRdpClient8.get_DesktopWidth
- IMsRdpClient8.put_DesktopWidth
- IMsRdpClient9.DesktopWidth
- IMsRdpClient9.get_DesktopWidth
- IMsRdpClient9.put_DesktopWidth
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16cd1391c6aeb27d9ec0f87317b06e9084337fbb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534133"
---
# <a name="imstscaxdesktopwidth-property"></a><span data-ttu-id="c13f3-124">Имстскакс: свойство Есктопвидс:D</span><span class="sxs-lookup"><span data-stu-id="c13f3-124">IMsTscAx::DesktopWidth property</span></span>

<span data-ttu-id="c13f3-125">Задает ширину текущего элемента управления в пикселях на начальном удаленном рабочем столе.</span><span class="sxs-lookup"><span data-stu-id="c13f3-125">Specifies the current control's width, in pixels, on the initial remote desktop.</span></span>

<span data-ttu-id="c13f3-126">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="c13f3-126">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="c13f3-127">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c13f3-127">Syntax</span></span>


```C++
HRESULT put_DesktopWidth(
  [in]  LONG newVal
);

HRESULT get_DesktopWidth(
  [out] LONG *pVal
);
```



## <a name="property-value"></a><span data-ttu-id="c13f3-128">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="c13f3-128">Property value</span></span>

<span data-ttu-id="c13f3-129">Новая ширина (в пикселях).</span><span class="sxs-lookup"><span data-stu-id="c13f3-129">The new width, in pixels.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c13f3-130">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="c13f3-130">Error codes</span></span>

<span data-ttu-id="c13f3-131">В случае успеха возвратите значение **\_ ОК** .</span><span class="sxs-lookup"><span data-stu-id="c13f3-131">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="c13f3-132">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c13f3-132">Remarks</span></span>

<span data-ttu-id="c13f3-133">Задание свойства **десктопвидс** является необязательным, но оно должно быть задано перед вызовом метода [**Connect**](imstscax-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="c13f3-133">Setting the **DesktopWidth** property is optional, but it must be set before calling the [**Connect**](imstscax-connect.md) method.</span></span> <span data-ttu-id="c13f3-134">Если ширина рабочего стола не указана или имеет значение 0, ширина рабочего стола будет равна ширине элемента управления.</span><span class="sxs-lookup"><span data-stu-id="c13f3-134">If a desktop width is not specified, or is set to zero, the desktop width is set to the width of the control.</span></span> <span data-ttu-id="c13f3-135">Минимальное и максимальное значения зависят от версии операционной системы клиента удаленный рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="c13f3-135">The minimum and maximum values are dependent upon the operating system version of the Remote Desktop client.</span></span>

<dl> <dt>

<span data-ttu-id="c13f3-136"><span id="_"></span>Windows 8 или Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c13f3-136"><span id="_"></span>Windows 8/Windows Server 2012</span></span>
</dt> <dd>

<span data-ttu-id="c13f3-137">200 минимум, максимум 8192</span><span class="sxs-lookup"><span data-stu-id="c13f3-137">200 minimum, 8192 maximum</span></span>

</dd> <dt>

<span data-ttu-id="c13f3-138"><span id="_"></span>Windows 7 или Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c13f3-138"><span id="_"></span>Windows 7/Windows Server 2008</span></span>
</dt> <dd>

<span data-ttu-id="c13f3-139">200 минимум, максимум 2048</span><span class="sxs-lookup"><span data-stu-id="c13f3-139">200 minimum, 2048 maximum</span></span>

</dd> <dt>

<span data-ttu-id="c13f3-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c13f3-140">Windows Vista</span></span>
</dt> <dd>

<span data-ttu-id="c13f3-141">200 минимум, максимум 1200</span><span class="sxs-lookup"><span data-stu-id="c13f3-141">200 minimum, 1200 maximum</span></span>

</dd> </dl>

<span data-ttu-id="c13f3-142">После установки соединения любые изменения ширины элемента управления не изменяют ширину удаленного рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="c13f3-142">After a connection is established, any changes to the control's width do not change the width of the remote desktop.</span></span> <span data-ttu-id="c13f3-143">Вместо этого элемент управления выводит полосу прокрутки или центрирует удаленный рабочий стол по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="c13f3-143">Instead, the control brings up scroll bars or centers the remote desktop, as appropriate.</span></span> <span data-ttu-id="c13f3-144">Чтобы изменить размер рабочего стола активного подключения, используйте метод [**IMsRdpClient8:: Reconnect**](imsrdpclient8-reconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="c13f3-144">To change the desktop size of an active connection, use the [**IMsRdpClient8::Reconnect**](imsrdpclient8-reconnect.md) method.</span></span>

<span data-ttu-id="c13f3-145">Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="c13f3-145">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c13f3-146">Требования</span><span class="sxs-lookup"><span data-stu-id="c13f3-146">Requirements</span></span>



| <span data-ttu-id="c13f3-147">Требование</span><span class="sxs-lookup"><span data-stu-id="c13f3-147">Requirement</span></span> | <span data-ttu-id="c13f3-148">Значение</span><span class="sxs-lookup"><span data-stu-id="c13f3-148">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c13f3-149">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c13f3-149">Minimum supported client</span></span><br/> | <span data-ttu-id="c13f3-150">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c13f3-150">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="c13f3-151">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c13f3-151">Minimum supported server</span></span><br/> | <span data-ttu-id="c13f3-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c13f3-152">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="c13f3-153">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="c13f3-153">Type library</span></span><br/>             | <dl> <span data-ttu-id="c13f3-154"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c13f3-154"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="c13f3-155">DLL</span><span class="sxs-lookup"><span data-stu-id="c13f3-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c13f3-156"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c13f3-156"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="c13f3-157">IID</span><span class="sxs-lookup"><span data-stu-id="c13f3-157">IID</span></span><br/>                      | <span data-ttu-id="c13f3-158">IID \_ имстскакс определен как 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="c13f3-158">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="c13f3-159">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c13f3-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c13f3-160">**имсрдпклиент**</span><span class="sxs-lookup"><span data-stu-id="c13f3-160">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="c13f3-161">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="c13f3-161">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="c13f3-162">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="c13f3-162">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="c13f3-163">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="c13f3-163">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="c13f3-164">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="c13f3-164">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="c13f3-165">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="c13f3-165">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="c13f3-166">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="c13f3-166">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="c13f3-167">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="c13f3-167">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="c13f3-168">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="c13f3-168">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="c13f3-169">**имстскакс**</span><span class="sxs-lookup"><span data-stu-id="c13f3-169">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> </dl>

 

 





