---
title: Имстскакс Секуредсеттингс, свойство
description: Извлекает указатель интерфейса Имстсксекуредсеттингс.
ms.assetid: 64d4059b-e617-449d-a733-c19c1d281132
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Секуредсеттингс
- Службы удаленных рабочих столов свойства Секуредсеттингс, интерфейс Имстскакс
- Службы удаленных рабочих столов интерфейса Имстскакс, свойство Секуредсеттингс
- Службы удаленных рабочих столов свойства Секуредсеттингс, интерфейс Имсрдпклиент
- Службы удаленных рабочих столов интерфейса Имсрдпклиент, свойство Секуредсеттингс
- Службы удаленных рабочих столов свойства Секуредсеттингс, интерфейс IMsRdpClient2
- Службы удаленных рабочих столов интерфейса IMsRdpClient2, свойство Секуредсеттингс
- Службы удаленных рабочих столов свойства Секуредсеттингс, интерфейс IMsRdpClient3
- Службы удаленных рабочих столов интерфейса IMsRdpClient3, свойство Секуредсеттингс
- Службы удаленных рабочих столов свойства Секуредсеттингс, интерфейс IMsRdpClient4
- Службы удаленных рабочих столов интерфейса IMsRdpClient4, свойство Секуредсеттингс
- Службы удаленных рабочих столов свойства Секуредсеттингс, интерфейс IMsRdpClient5
- Службы удаленных рабочих столов интерфейса IMsRdpClient5, свойство Секуредсеттингс
- Службы удаленных рабочих столов свойства Секуредсеттингс, интерфейс IMsRdpClient6
- Службы удаленных рабочих столов интерфейса IMsRdpClient6, свойство Секуредсеттингс
- Службы удаленных рабочих столов свойства Секуредсеттингс, интерфейс IMsRdpClient7
- Службы удаленных рабочих столов интерфейса IMsRdpClient7, свойство Секуредсеттингс
- Службы удаленных рабочих столов свойства Секуредсеттингс, интерфейс IMsRdpClient8
- Службы удаленных рабочих столов интерфейса IMsRdpClient8, свойство Секуредсеттингс
- Службы удаленных рабочих столов свойства Секуредсеттингс, интерфейс IMsRdpClient9
- Службы удаленных рабочих столов интерфейса IMsRdpClient9, свойство Секуредсеттингс
topic_type:
- apiref
api_name:
- IMsTscAx.SecuredSettings
- IMsTscAx.get_SecuredSettings
- IMsRdpClient.SecuredSettings
- IMsRdpClient.get_SecuredSettings
- IMsRdpClient2.SecuredSettings
- IMsRdpClient2.get_SecuredSettings
- IMsRdpClient3.SecuredSettings
- IMsRdpClient3.get_SecuredSettings
- IMsRdpClient4.SecuredSettings
- IMsRdpClient4.get_SecuredSettings
- IMsRdpClient5.SecuredSettings
- IMsRdpClient5.get_SecuredSettings
- IMsRdpClient6.SecuredSettings
- IMsRdpClient6.get_SecuredSettings
- IMsRdpClient7.SecuredSettings
- IMsRdpClient7.get_SecuredSettings
- IMsRdpClient8.SecuredSettings
- IMsRdpClient8.get_SecuredSettings
- IMsRdpClient9.SecuredSettings
- IMsRdpClient9.get_SecuredSettings
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6610448d822fe75082c225686dc6d809229a325f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135902"
---
# <a name="imstscaxsecuredsettings-property"></a><span data-ttu-id="a1867-124">Свойство Имстскакс:: Секуредсеттингс</span><span class="sxs-lookup"><span data-stu-id="a1867-124">IMsTscAx::SecuredSettings property</span></span>

<span data-ttu-id="a1867-125">Извлекает указатель интерфейса [**имстсксекуредсеттингс**](imstscsecuredsettings-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="a1867-125">Retrieves an [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md) interface pointer.</span></span>

<span data-ttu-id="a1867-126">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="a1867-126">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1867-127">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a1867-127">Syntax</span></span>


```C++
HRESULT get_SecuredSettings(
  [out] IMsTscSecuredSettings **ppSecuredSettings
);
```



## <a name="property-value"></a><span data-ttu-id="a1867-128">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="a1867-128">Property value</span></span>

<span data-ttu-id="a1867-129">Указатель интерфейса [**имстсксекуредсеттингс**](imstscsecuredsettings-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="a1867-129">An [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md) interface pointer.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a1867-130">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="a1867-130">Error codes</span></span>

<span data-ttu-id="a1867-131">В случае успеха возвратите значение **\_ ОК** .</span><span class="sxs-lookup"><span data-stu-id="a1867-131">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="a1867-132">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a1867-132">Remarks</span></span>

<span data-ttu-id="a1867-133">Если элемент управления размещается на веб-странице, а текущая зона безопасности URL-адресов Internet Explorer не позволяет получить адрес интерфейса, этот метод возвращает значение **E \_ Fail**.</span><span class="sxs-lookup"><span data-stu-id="a1867-133">If the control is hosted in a webpage and the current Internet Explorer URL security zone does not permit the retrieval of the interface address, this method returns **E\_FAIL**.</span></span>

<span data-ttu-id="a1867-134">Ограничения на доступность интерфейса [**имстсксекуредсеттингс**](imstscsecuredsettings-interface.md) см. в [**секуредсеттингсенаблед**](imstscax-securedsettingsenabled.md) .</span><span class="sxs-lookup"><span data-stu-id="a1867-134">Refer to [**SecuredSettingsEnabled**](imstscax-securedsettingsenabled.md) for restrictions on the availability of the [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md) interface.</span></span>

<span data-ttu-id="a1867-135">Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="a1867-135">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a1867-136">Требования</span><span class="sxs-lookup"><span data-stu-id="a1867-136">Requirements</span></span>



| <span data-ttu-id="a1867-137">Требование</span><span class="sxs-lookup"><span data-stu-id="a1867-137">Requirement</span></span> | <span data-ttu-id="a1867-138">Значение</span><span class="sxs-lookup"><span data-stu-id="a1867-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a1867-139">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a1867-139">Minimum supported client</span></span><br/> | <span data-ttu-id="a1867-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a1867-140">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="a1867-141">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a1867-141">Minimum supported server</span></span><br/> | <span data-ttu-id="a1867-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a1867-142">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="a1867-143">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="a1867-143">Type library</span></span><br/>             | <dl> <span data-ttu-id="a1867-144"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a1867-144"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="a1867-145">DLL</span><span class="sxs-lookup"><span data-stu-id="a1867-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a1867-146"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a1867-146"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="a1867-147">IID</span><span class="sxs-lookup"><span data-stu-id="a1867-147">IID</span></span><br/>                      | <span data-ttu-id="a1867-148">IID \_ имстскакс определен как 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="a1867-148">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="a1867-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a1867-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1867-150">**имсрдпклиент**</span><span class="sxs-lookup"><span data-stu-id="a1867-150">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="a1867-151">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="a1867-151">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="a1867-152">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="a1867-152">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="a1867-153">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="a1867-153">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="a1867-154">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="a1867-154">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="a1867-155">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="a1867-155">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="a1867-156">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="a1867-156">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="a1867-157">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="a1867-157">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="a1867-158">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="a1867-158">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="a1867-159">**имстскакс**</span><span class="sxs-lookup"><span data-stu-id="a1867-159">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> <dt>

[<span data-ttu-id="a1867-160">**имстсксекуредсеттингс**</span><span class="sxs-lookup"><span data-stu-id="a1867-160">**IMsTscSecuredSettings**</span></span>](imstscsecuredsettings-interface.md)
</dt> </dl>

 

 





