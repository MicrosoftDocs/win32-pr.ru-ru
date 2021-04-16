---
title: Имстскакс Секуредсеттингсенаблед, свойство
description: Указывает, доступен ли интерфейс Имстсксекуредсеттингс. То есть, находится ли веб-страница, содержащая данный элемент управления, в одной из разрешенных зон безопасности URL-адресов Internet Explorer.
ms.assetid: 0747eab0-9d62-4c10-b02d-fc65ca2f752e
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Секуредсеттингсенаблед
- Службы удаленных рабочих столов свойства Секуредсеттингсенаблед, интерфейс Имстскакс
- Службы удаленных рабочих столов интерфейса Имстскакс, свойство Секуредсеттингсенаблед
- Службы удаленных рабочих столов свойства Секуредсеттингсенаблед, интерфейс Имсрдпклиент
- Службы удаленных рабочих столов интерфейса Имсрдпклиент, свойство Секуредсеттингсенаблед
- Службы удаленных рабочих столов свойства Секуредсеттингсенаблед, интерфейс IMsRdpClient2
- Службы удаленных рабочих столов интерфейса IMsRdpClient2, свойство Секуредсеттингсенаблед
- Службы удаленных рабочих столов свойства Секуредсеттингсенаблед, интерфейс IMsRdpClient3
- Службы удаленных рабочих столов интерфейса IMsRdpClient3, свойство Секуредсеттингсенаблед
- Службы удаленных рабочих столов свойства Секуредсеттингсенаблед, интерфейс IMsRdpClient4
- Службы удаленных рабочих столов интерфейса IMsRdpClient4, свойство Секуредсеттингсенаблед
- Службы удаленных рабочих столов свойства Секуредсеттингсенаблед, интерфейс IMsRdpClient5
- Службы удаленных рабочих столов интерфейса IMsRdpClient5, свойство Секуредсеттингсенаблед
- Службы удаленных рабочих столов свойства Секуредсеттингсенаблед, интерфейс IMsRdpClient6
- Службы удаленных рабочих столов интерфейса IMsRdpClient6, свойство Секуредсеттингсенаблед
- Службы удаленных рабочих столов свойства Секуредсеттингсенаблед, интерфейс IMsRdpClient7
- Службы удаленных рабочих столов интерфейса IMsRdpClient7, свойство Секуредсеттингсенаблед
- Службы удаленных рабочих столов свойства Секуредсеттингсенаблед, интерфейс IMsRdpClient8
- Службы удаленных рабочих столов интерфейса IMsRdpClient8, свойство Секуредсеттингсенаблед
- Службы удаленных рабочих столов свойства Секуредсеттингсенаблед, интерфейс IMsRdpClient9
- Службы удаленных рабочих столов интерфейса IMsRdpClient9, свойство Секуредсеттингсенаблед
topic_type:
- apiref
api_name:
- IMsTscAx.SecuredSettingsEnabled
- IMsTscAx.get_SecuredSettingsEnabled
- IMsRdpClient.SecuredSettingsEnabled
- IMsRdpClient.get_SecuredSettingsEnabled
- IMsRdpClient2.SecuredSettingsEnabled
- IMsRdpClient2.get_SecuredSettingsEnabled
- IMsRdpClient3.SecuredSettingsEnabled
- IMsRdpClient3.get_SecuredSettingsEnabled
- IMsRdpClient4.SecuredSettingsEnabled
- IMsRdpClient4.get_SecuredSettingsEnabled
- IMsRdpClient5.SecuredSettingsEnabled
- IMsRdpClient5.get_SecuredSettingsEnabled
- IMsRdpClient6.SecuredSettingsEnabled
- IMsRdpClient6.get_SecuredSettingsEnabled
- IMsRdpClient7.SecuredSettingsEnabled
- IMsRdpClient7.get_SecuredSettingsEnabled
- IMsRdpClient8.SecuredSettingsEnabled
- IMsRdpClient8.get_SecuredSettingsEnabled
- IMsRdpClient9.SecuredSettingsEnabled
- IMsRdpClient9.get_SecuredSettingsEnabled
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de0601ac64ab0ca55f3d92ec460861a4347f70b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672834"
---
# <a name="imstscaxsecuredsettingsenabled-property"></a><span data-ttu-id="d5367-125">Свойство Имстскакс:: Секуредсеттингсенаблед</span><span class="sxs-lookup"><span data-stu-id="d5367-125">IMsTscAx::SecuredSettingsEnabled property</span></span>

<span data-ttu-id="d5367-126">Указывает, доступен ли интерфейс [**имстсксекуредсеттингс**](imstscsecuredsettings-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="d5367-126">Indicates whether the [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md) interface is available.</span></span> <span data-ttu-id="d5367-127">То есть, находится ли веб-страница, содержащая данный элемент управления, в одной из разрешенных зон безопасности URL-адресов Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="d5367-127">That is, whether the webpage containing the control is currently in one of the allowed Internet Explorer URL security zones.</span></span>

<span data-ttu-id="d5367-128">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="d5367-128">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5367-129">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d5367-129">Syntax</span></span>


```C++
HRESULT get_SecuredSettingsEnabled(
  [out] BOOL *pSecuredSettingsEnabled
);
```



## <a name="property-value"></a><span data-ttu-id="d5367-130">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="d5367-130">Property value</span></span>

<span data-ttu-id="d5367-131">Значение этого параметра равно **true** , если интерфейс доступен, и **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="d5367-131">The value of this parameter is **TRUE** if the interface is available, and **FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d5367-132">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="d5367-132">Error codes</span></span>

<span data-ttu-id="d5367-133">При успешном выполнении возвращает значение **\_ ОК** .</span><span class="sxs-lookup"><span data-stu-id="d5367-133">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="d5367-134">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d5367-134">Remarks</span></span>

<span data-ttu-id="d5367-135">Используйте этот метод, чтобы запросить доступ к интерфейсу [**имстсксекуредсеттингс**](imstscsecuredsettings-interface.md) перед получением свойства [**секуредсеттингс**](imstscax-securedsettings.md) .</span><span class="sxs-lookup"><span data-stu-id="d5367-135">Use this method to query whether the [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md) interface is available before retrieving the [**SecuredSettings**](imstscax-securedsettings.md) property.</span></span>

<span data-ttu-id="d5367-136">Список зон безопасности с ограниченным URL-адресом см. в руководстве по обеспечению [безопасности клиента RDP](providing-for-rdp-client-security.md) .</span><span class="sxs-lookup"><span data-stu-id="d5367-136">Refer to [Providing for RDP Client Security](providing-for-rdp-client-security.md) for a list of restricted URL security zones.</span></span>

<span data-ttu-id="d5367-137">Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="d5367-137">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d5367-138">Требования</span><span class="sxs-lookup"><span data-stu-id="d5367-138">Requirements</span></span>



| <span data-ttu-id="d5367-139">Требование</span><span class="sxs-lookup"><span data-stu-id="d5367-139">Requirement</span></span> | <span data-ttu-id="d5367-140">Значение</span><span class="sxs-lookup"><span data-stu-id="d5367-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d5367-141">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d5367-141">Minimum supported client</span></span><br/> | <span data-ttu-id="d5367-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d5367-142">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="d5367-143">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d5367-143">Minimum supported server</span></span><br/> | <span data-ttu-id="d5367-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d5367-144">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="d5367-145">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="d5367-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="d5367-146"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d5367-146"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="d5367-147">DLL</span><span class="sxs-lookup"><span data-stu-id="d5367-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d5367-148"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d5367-148"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="d5367-149">IID</span><span class="sxs-lookup"><span data-stu-id="d5367-149">IID</span></span><br/>                      | <span data-ttu-id="d5367-150">IID \_ имстскакс определен как 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="d5367-150">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="d5367-151">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d5367-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5367-152">**имсрдпклиент**</span><span class="sxs-lookup"><span data-stu-id="d5367-152">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="d5367-153">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="d5367-153">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="d5367-154">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="d5367-154">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="d5367-155">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="d5367-155">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="d5367-156">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="d5367-156">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="d5367-157">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="d5367-157">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="d5367-158">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="d5367-158">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="d5367-159">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="d5367-159">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="d5367-160">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="d5367-160">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="d5367-161">**имстскакс**</span><span class="sxs-lookup"><span data-stu-id="d5367-161">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> <dt>

[<span data-ttu-id="d5367-162">**имстсксекуредсеттингс**</span><span class="sxs-lookup"><span data-stu-id="d5367-162">**IMsTscSecuredSettings**</span></span>](imstscsecuredsettings-interface.md)
</dt> </dl>

 

 





