---
title: Имсрдпклиент, свойство полноэкранного режима
description: Определяет, находится ли клиентский элемент управления в полноэкранном режиме.
ms.assetid: 64fe2835-c00e-4d21-812d-dcf160147d93
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства во весь экран
- Свойство "Полноэкранный" службы удаленных рабочих столов, интерфейс Имсрдпклиент
- Службы удаленных рабочих столов интерфейса Имсрдпклиент, свойство "во весь экран"
- Свойство "Полноэкранный" службы удаленных рабочих столов, интерфейс IMsRdpClient2
- Службы удаленных рабочих столов интерфейса IMsRdpClient2, свойство "во весь экран"
- Свойство "Полноэкранный" службы удаленных рабочих столов, интерфейс IMsRdpClient3
- Службы удаленных рабочих столов интерфейса IMsRdpClient3, свойство "во весь экран"
- Свойство "Полноэкранный" службы удаленных рабочих столов, интерфейс IMsRdpClient4
- Службы удаленных рабочих столов интерфейса IMsRdpClient4, свойство "во весь экран"
- Свойство "Полноэкранный" службы удаленных рабочих столов, интерфейс IMsRdpClient5
- Службы удаленных рабочих столов интерфейса IMsRdpClient5, свойство "во весь экран"
- Свойство "Полноэкранный" службы удаленных рабочих столов, интерфейс IMsRdpClient6
- Службы удаленных рабочих столов интерфейса IMsRdpClient6, свойство "во весь экран"
- Свойство "Полноэкранный" службы удаленных рабочих столов, интерфейс IMsRdpClient7
- Службы удаленных рабочих столов интерфейса IMsRdpClient7, свойство "во весь экран"
- Свойство "Полноэкранный" службы удаленных рабочих столов, интерфейс IMsRdpClient8
- Службы удаленных рабочих столов интерфейса IMsRdpClient8, свойство "во весь экран"
- Свойство "Полноэкранный" службы удаленных рабочих столов, интерфейс IMsRdpClient9
- Службы удаленных рабочих столов интерфейса IMsRdpClient9, свойство "во весь экран"
- Свойство "Полноэкранный" службы удаленных рабочих столов, интерфейс IMsRdpClient10
- Службы удаленных рабочих столов интерфейса IMsRdpClient10, свойство "во весь экран"
topic_type:
- apiref
api_name:
- IMsRdpClient.FullScreen
- IMsRdpClient.get_FullScreen
- IMsRdpClient.put_FullScreen
- IMsRdpClient2.FullScreen
- IMsRdpClient2.get_FullScreen
- IMsRdpClient2.put_FullScreen
- IMsRdpClient3.FullScreen
- IMsRdpClient3.get_FullScreen
- IMsRdpClient3.put_FullScreen
- IMsRdpClient4.FullScreen
- IMsRdpClient4.get_FullScreen
- IMsRdpClient4.put_FullScreen
- IMsRdpClient5.FullScreen
- IMsRdpClient5.get_FullScreen
- IMsRdpClient5.put_FullScreen
- IMsRdpClient6.FullScreen
- IMsRdpClient6.get_FullScreen
- IMsRdpClient6.put_FullScreen
- IMsRdpClient7.FullScreen
- IMsRdpClient7.get_FullScreen
- IMsRdpClient7.put_FullScreen
- IMsRdpClient8.FullScreen
- IMsRdpClient8.get_FullScreen
- IMsRdpClient8.put_FullScreen
- IMsRdpClient9.FullScreen
- IMsRdpClient9.get_FullScreen
- IMsRdpClient9.put_FullScreen
- IMsRdpClient10.FullScreen
- IMsRdpClient10.get_FullScreen
- IMsRdpClient10.put_FullScreen
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1adbc8e11d2cc4fb4a8071372777a01d81b5edad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137362"
---
# <a name="imsrdpclientfullscreen-property"></a><span data-ttu-id="2f2b5-124">Свойство Имсрдпклиент:: полноэкранного режима</span><span class="sxs-lookup"><span data-stu-id="2f2b5-124">IMsRdpClient::FullScreen property</span></span>

<span data-ttu-id="2f2b5-125">Определяет, находится ли клиентский элемент управления в полноэкранном режиме.</span><span class="sxs-lookup"><span data-stu-id="2f2b5-125">Determines whether the client control is in full-screen mode.</span></span>

<span data-ttu-id="2f2b5-126">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="2f2b5-126">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f2b5-127">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2f2b5-127">Syntax</span></span>


```C++
HRESULT put_FullScreen(
  [in]  VARIANT_BOOL fFullScreen
);

HRESULT get_FullScreen(
  [out] VARIANT_BOOL *pfFullScreen
);
```



## <a name="property-value"></a><span data-ttu-id="2f2b5-128">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="2f2b5-128">Property value</span></span>

<span data-ttu-id="2f2b5-129">**Значение true** , чтобы перейти в полноэкранный режим, **значение false** , чтобы выйти из полноэкранного режима и вернуться в режим окна.</span><span class="sxs-lookup"><span data-stu-id="2f2b5-129">**True** to enter full-screen mode, **False** to leave full-screen mode and return to window mode.</span></span>

## <a name="error-codes"></a><span data-ttu-id="2f2b5-130">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="2f2b5-130">Error codes</span></span>

<span data-ttu-id="2f2b5-131">Если методы выполнены успешно, возвращается значение **S \_ OK** .</span><span class="sxs-lookup"><span data-stu-id="2f2b5-131">If the methods succeed, **S\_OK** is returned.</span></span> <span data-ttu-id="2f2b5-132">Любое другое значение **HRESULT** указывает на сбой вызова.</span><span class="sxs-lookup"><span data-stu-id="2f2b5-132">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="2f2b5-133">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2f2b5-133">Remarks</span></span>

<span data-ttu-id="2f2b5-134">Это свойство можно задать, если элемент управления подключен.</span><span class="sxs-lookup"><span data-stu-id="2f2b5-134">You can set this property when the control is connected.</span></span>

<span data-ttu-id="2f2b5-135">Необходимо вызвать метод [**IMsRdpClientNonScriptable3::p UT \_ коннектионбартекст**](imsrdpclientnonscriptable3-connectionbartext.md) перед вызовом метода [**имстсксекуредсеттингс::p UT \_**](imstscsecuredsettings-fullscreen.md) , а также метода **имсрдпклиент::p UT \_** .</span><span class="sxs-lookup"><span data-stu-id="2f2b5-135">You must call the [**IMsRdpClientNonScriptable3::put\_ConnectionBarText**](imsrdpclientnonscriptable3-connectionbartext.md) method before you call the [**IMsTscSecuredSettings::put\_Fullscreen**](imstscsecuredsettings-fullscreen.md) method or the **IMsRdpClient::put\_Fullscreen** method.</span></span>

<span data-ttu-id="2f2b5-136">Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="2f2b5-136">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2f2b5-137">Требования</span><span class="sxs-lookup"><span data-stu-id="2f2b5-137">Requirements</span></span>



| <span data-ttu-id="2f2b5-138">Требование</span><span class="sxs-lookup"><span data-stu-id="2f2b5-138">Requirement</span></span> | <span data-ttu-id="2f2b5-139">Значение</span><span class="sxs-lookup"><span data-stu-id="2f2b5-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2f2b5-140">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2f2b5-140">Minimum supported client</span></span><br/> | <span data-ttu-id="2f2b5-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2f2b5-141">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="2f2b5-142">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2f2b5-142">Minimum supported server</span></span><br/> | <span data-ttu-id="2f2b5-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2f2b5-143">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="2f2b5-144">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="2f2b5-144">Type library</span></span><br/>             | <dl> <span data-ttu-id="2f2b5-145"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2f2b5-145"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="2f2b5-146">DLL</span><span class="sxs-lookup"><span data-stu-id="2f2b5-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2f2b5-147"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2f2b5-147"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="2f2b5-148">IID</span><span class="sxs-lookup"><span data-stu-id="2f2b5-148">IID</span></span><br/>                      | <span data-ttu-id="2f2b5-149">IID \_ имсрдпклиент определен как 92b4a539-7115-4b7c-a5a9-e5d9efc2780a</span><span class="sxs-lookup"><span data-stu-id="2f2b5-149">IID\_IMsRdpClient is defined as 92b4a539-7115-4b7c-a5a9-e5d9efc2780a</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="2f2b5-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2f2b5-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f2b5-151">**имсрдпклиент**</span><span class="sxs-lookup"><span data-stu-id="2f2b5-151">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="2f2b5-152">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="2f2b5-152">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="2f2b5-153">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="2f2b5-153">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="2f2b5-154">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="2f2b5-154">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="2f2b5-155">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="2f2b5-155">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="2f2b5-156">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="2f2b5-156">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="2f2b5-157">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="2f2b5-157">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="2f2b5-158">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="2f2b5-158">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="2f2b5-159">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="2f2b5-159">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="2f2b5-160">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="2f2b5-160">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





