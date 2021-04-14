---
title: Имсрдпклиент SecuredSettings2, свойство
description: Получает указатель на интерфейс Имсрдпклиентсекуредсеттингс. Этот интерфейс можно использовать для задания защищенных параметров клиентского элемента управления.
ms.assetid: f570a3f6-70ae-45fd-ba20-75c9f4d2f5ca
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства SecuredSettings2
- Службы удаленных рабочих столов свойства SecuredSettings2, интерфейс Имсрдпклиент
- Службы удаленных рабочих столов интерфейса Имсрдпклиент, свойство SecuredSettings2
- Службы удаленных рабочих столов свойства SecuredSettings2, интерфейс IMsRdpClient2
- Службы удаленных рабочих столов интерфейса IMsRdpClient2, свойство SecuredSettings2
- Службы удаленных рабочих столов свойства SecuredSettings2, интерфейс IMsRdpClient3
- Службы удаленных рабочих столов интерфейса IMsRdpClient3, свойство SecuredSettings2
- Службы удаленных рабочих столов свойства SecuredSettings2, интерфейс IMsRdpClient4
- Службы удаленных рабочих столов интерфейса IMsRdpClient4, свойство SecuredSettings2
- Службы удаленных рабочих столов свойства SecuredSettings2, интерфейс IMsRdpClient5
- Службы удаленных рабочих столов интерфейса IMsRdpClient5, свойство SecuredSettings2
- Службы удаленных рабочих столов свойства SecuredSettings2, интерфейс IMsRdpClient6
- Службы удаленных рабочих столов интерфейса IMsRdpClient6, свойство SecuredSettings2
- Службы удаленных рабочих столов свойства SecuredSettings2, интерфейс IMsRdpClient7
- Службы удаленных рабочих столов интерфейса IMsRdpClient7, свойство SecuredSettings2
- Службы удаленных рабочих столов свойства SecuredSettings2, интерфейс IMsRdpClient8
- Службы удаленных рабочих столов интерфейса IMsRdpClient8, свойство SecuredSettings2
- Службы удаленных рабочих столов свойства SecuredSettings2, интерфейс IMsRdpClient9
- Службы удаленных рабочих столов интерфейса IMsRdpClient9, свойство SecuredSettings2
- Службы удаленных рабочих столов свойства SecuredSettings2, интерфейс IMsRdpClient10
- Службы удаленных рабочих столов интерфейса IMsRdpClient10, свойство SecuredSettings2
topic_type:
- apiref
api_name:
- IMsRdpClient.SecuredSettings2
- IMsRdpClient.get_SecuredSettings2
- IMsRdpClient2.SecuredSettings2
- IMsRdpClient2.get_SecuredSettings2
- IMsRdpClient3.SecuredSettings2
- IMsRdpClient3.get_SecuredSettings2
- IMsRdpClient4.SecuredSettings2
- IMsRdpClient4.get_SecuredSettings2
- IMsRdpClient5.SecuredSettings2
- IMsRdpClient5.get_SecuredSettings2
- IMsRdpClient6.SecuredSettings2
- IMsRdpClient6.get_SecuredSettings2
- IMsRdpClient7.SecuredSettings2
- IMsRdpClient7.get_SecuredSettings2
- IMsRdpClient8.SecuredSettings2
- IMsRdpClient8.get_SecuredSettings2
- IMsRdpClient9.SecuredSettings2
- IMsRdpClient9.get_SecuredSettings2
- IMsRdpClient10.SecuredSettings2
- IMsRdpClient10.get_SecuredSettings2
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39e26d9d7a7b2ac776166c251e5a2ab9923297f0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104533752"
---
# <a name="imsrdpclientsecuredsettings2-property"></a><span data-ttu-id="89d73-125">Свойство Имсрдпклиент:: SecuredSettings2</span><span class="sxs-lookup"><span data-stu-id="89d73-125">IMsRdpClient::SecuredSettings2 property</span></span>

<span data-ttu-id="89d73-126">Получает указатель на интерфейс [**имсрдпклиентсекуредсеттингс**](imsrdpclientsecuredsettings-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="89d73-126">Retrieves a pointer to the [**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md) interface.</span></span> <span data-ttu-id="89d73-127">Этот интерфейс можно использовать для задания защищенных параметров клиентского элемента управления.</span><span class="sxs-lookup"><span data-stu-id="89d73-127">This interface can be used to set secured settings for the client control.</span></span>

<span data-ttu-id="89d73-128">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="89d73-128">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="89d73-129">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="89d73-129">Syntax</span></span>


```C++
HRESULT get_SecuredSettings2(
  [out] IMsRdpClientSecuredSettings **ppSecuredSettings
);
```



## <a name="property-value"></a><span data-ttu-id="89d73-130">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="89d73-130">Property value</span></span>

<span data-ttu-id="89d73-131">Указатель интерфейса [**имсрдпклиентсекуредсеттингс**](imsrdpclientsecuredsettings-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="89d73-131">An [**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md) interface pointer.</span></span>

## <a name="error-codes"></a><span data-ttu-id="89d73-132">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="89d73-132">Error codes</span></span>

<span data-ttu-id="89d73-133">Если метод выполнен успешно, возвращается значение **S \_ OK** .</span><span class="sxs-lookup"><span data-stu-id="89d73-133">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="89d73-134">Любое другое значение **HRESULT** указывает на сбой вызова.</span><span class="sxs-lookup"><span data-stu-id="89d73-134">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="89d73-135">Комментарии</span><span class="sxs-lookup"><span data-stu-id="89d73-135">Remarks</span></span>

<span data-ttu-id="89d73-136">Дополнительные сведения см. в описании интерфейса [**имсрдпклиентсекуредсеттингс**](imsrdpclientsecuredsettings-interface.md) и [обеспечении безопасности клиента RDP](providing-for-rdp-client-security.md).</span><span class="sxs-lookup"><span data-stu-id="89d73-136">For more information, see the [**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md) interface, and [Providing for RDP Client Security](providing-for-rdp-client-security.md).</span></span>

<span data-ttu-id="89d73-137">Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="89d73-137">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="89d73-138">Требования</span><span class="sxs-lookup"><span data-stu-id="89d73-138">Requirements</span></span>



| <span data-ttu-id="89d73-139">Требование</span><span class="sxs-lookup"><span data-stu-id="89d73-139">Requirement</span></span> | <span data-ttu-id="89d73-140">Значение</span><span class="sxs-lookup"><span data-stu-id="89d73-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="89d73-141">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="89d73-141">Minimum supported client</span></span><br/> | <span data-ttu-id="89d73-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="89d73-142">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="89d73-143">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="89d73-143">Minimum supported server</span></span><br/> | <span data-ttu-id="89d73-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="89d73-144">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="89d73-145">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="89d73-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="89d73-146"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="89d73-146"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="89d73-147">DLL</span><span class="sxs-lookup"><span data-stu-id="89d73-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="89d73-148"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="89d73-148"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="89d73-149">IID</span><span class="sxs-lookup"><span data-stu-id="89d73-149">IID</span></span><br/>                      | <span data-ttu-id="89d73-150">IID \_ имсрдпклиент определен как 92b4a539-7115-4b7c-a5a9-e5d9efc2780a</span><span class="sxs-lookup"><span data-stu-id="89d73-150">IID\_IMsRdpClient is defined as 92b4a539-7115-4b7c-a5a9-e5d9efc2780a</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="89d73-151">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="89d73-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89d73-152">**имсрдпклиент**</span><span class="sxs-lookup"><span data-stu-id="89d73-152">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="89d73-153">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="89d73-153">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="89d73-154">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="89d73-154">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="89d73-155">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="89d73-155">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="89d73-156">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="89d73-156">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="89d73-157">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="89d73-157">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="89d73-158">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="89d73-158">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="89d73-159">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="89d73-159">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="89d73-160">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="89d73-160">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="89d73-161">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="89d73-161">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





