---
title: Имсрдпклиентадванцедсеттингс Клеартекстпассворд, свойство
description: Указывает пароль для подключения. Дополнительные сведения см. в описании интерфейса Имстскнонскриптабле.
ms.assetid: 9bb12dd6-f74c-488d-b6e5-4f96346610a1
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Клеартекстпассворд
- Службы удаленных рабочих столов свойства Клеартекстпассворд, интерфейс Имсрдпклиентадванцедсеттингс
- Службы удаленных рабочих столов интерфейса Имсрдпклиентадванцедсеттингс, свойство Клеартекстпассворд
- Службы удаленных рабочих столов свойства Клеартекстпассворд, интерфейс IMsRdpClientAdvancedSettings2
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings2, свойство Клеартекстпассворд
- Службы удаленных рабочих столов свойства Клеартекстпассворд, интерфейс IMsRdpClientAdvancedSettings3
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings3, свойство Клеартекстпассворд
- Службы удаленных рабочих столов свойства Клеартекстпассворд, интерфейс IMsRdpClientAdvancedSettings4
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings4, свойство Клеартекстпассворд
- Службы удаленных рабочих столов свойства Клеартекстпассворд, интерфейс IMsRdpClientAdvancedSettings5
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings5, свойство Клеартекстпассворд
- Службы удаленных рабочих столов свойства Клеартекстпассворд, интерфейс IMsRdpClientAdvancedSettings6
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings6, свойство Клеартекстпассворд
- Службы удаленных рабочих столов свойства Клеартекстпассворд, интерфейс IMsRdpClientAdvancedSettings7
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings7, свойство Клеартекстпассворд
- Службы удаленных рабочих столов свойства Клеартекстпассворд, интерфейс IMsRdpClientAdvancedSettings8
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings8, свойство Клеартекстпассворд
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.ClearTextPassword
- IMsRdpClientAdvancedSettings.put_ClearTextPassword
- IMsRdpClientAdvancedSettings2.ClearTextPassword
- IMsRdpClientAdvancedSettings2.put_ClearTextPassword
- IMsRdpClientAdvancedSettings3.ClearTextPassword
- IMsRdpClientAdvancedSettings3.put_ClearTextPassword
- IMsRdpClientAdvancedSettings4.ClearTextPassword
- IMsRdpClientAdvancedSettings4.put_ClearTextPassword
- IMsRdpClientAdvancedSettings5.ClearTextPassword
- IMsRdpClientAdvancedSettings5.put_ClearTextPassword
- IMsRdpClientAdvancedSettings6.ClearTextPassword
- IMsRdpClientAdvancedSettings6.put_ClearTextPassword
- IMsRdpClientAdvancedSettings7.ClearTextPassword
- IMsRdpClientAdvancedSettings7.put_ClearTextPassword
- IMsRdpClientAdvancedSettings8.ClearTextPassword
- IMsRdpClientAdvancedSettings8.put_ClearTextPassword
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6943913193b2ecc9ed6ab31728d0274fb9ddd231
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490353"
---
# <a name="imsrdpclientadvancedsettingscleartextpassword-property"></a><span data-ttu-id="1be54-121">Свойство Имсрдпклиентадванцедсеттингс:: Клеартекстпассворд</span><span class="sxs-lookup"><span data-stu-id="1be54-121">IMsRdpClientAdvancedSettings::ClearTextPassword property</span></span>

<span data-ttu-id="1be54-122">Указывает пароль для подключения.</span><span class="sxs-lookup"><span data-stu-id="1be54-122">Specifies the password with which to connect.</span></span> <span data-ttu-id="1be54-123">Дополнительные сведения см. в описании интерфейса [**имстскнонскриптабле**](imstscnonscriptable-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="1be54-123">For more information, see the [**IMsTscNonScriptable**](imstscnonscriptable-interface.md) interface.</span></span>

> [!Caution]  
> <span data-ttu-id="1be54-124">Несмотря на то, что доступ к паролям с использованием обычного текста можно получить с помощью этого свойства, разработчик по-прежнему обязан соблюдать осторожность и обеспечивать безопасность при передаче паролей в свои приложения.</span><span class="sxs-lookup"><span data-stu-id="1be54-124">Even though scriptable access to plaintext passwords is available through this property, it is still the responsibility of the developer to exercise every caution and maintain security when passing passwords in their applications.</span></span>

 

<span data-ttu-id="1be54-125">Это свойство доступно только на запись.</span><span class="sxs-lookup"><span data-stu-id="1be54-125">This property is write-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="1be54-126">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1be54-126">Syntax</span></span>


```C++
HRESULT put_ClearTextPassword(
  [in] BSTR clearTextPassword
);
```



## <a name="property-value"></a><span data-ttu-id="1be54-127">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="1be54-127">Property value</span></span>

<span data-ttu-id="1be54-128">Новый пароль.</span><span class="sxs-lookup"><span data-stu-id="1be54-128">The new password.</span></span>

## <a name="error-codes"></a><span data-ttu-id="1be54-129">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="1be54-129">Error codes</span></span>

<span data-ttu-id="1be54-130">При успешном выполнении возвращает значение **\_ ОК** .</span><span class="sxs-lookup"><span data-stu-id="1be54-130">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="1be54-131">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1be54-131">Remarks</span></span>

<span data-ttu-id="1be54-132">Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="1be54-132">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1be54-133">Требования</span><span class="sxs-lookup"><span data-stu-id="1be54-133">Requirements</span></span>



| <span data-ttu-id="1be54-134">Требование</span><span class="sxs-lookup"><span data-stu-id="1be54-134">Requirement</span></span> | <span data-ttu-id="1be54-135">Значение</span><span class="sxs-lookup"><span data-stu-id="1be54-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1be54-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1be54-136">Minimum supported client</span></span><br/> | <span data-ttu-id="1be54-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1be54-137">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="1be54-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1be54-138">Minimum supported server</span></span><br/> | <span data-ttu-id="1be54-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1be54-139">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="1be54-140">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="1be54-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="1be54-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1be54-141"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="1be54-142">DLL</span><span class="sxs-lookup"><span data-stu-id="1be54-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1be54-143"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1be54-143"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="1be54-144">IID</span><span class="sxs-lookup"><span data-stu-id="1be54-144">IID</span></span><br/>                      | <span data-ttu-id="1be54-145">IID \_ имсрдпклиентадванцедсеттингс определен как 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="1be54-145">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1be54-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1be54-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1be54-147">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="1be54-147">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="1be54-148">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="1be54-148">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="1be54-149">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="1be54-149">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="1be54-150">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="1be54-150">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="1be54-151">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="1be54-151">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="1be54-152">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="1be54-152">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="1be54-153">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="1be54-153">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="1be54-154">**имсрдпклиентадванцедсеттингс**</span><span class="sxs-lookup"><span data-stu-id="1be54-154">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





