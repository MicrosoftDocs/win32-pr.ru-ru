---
title: Имсрдпклиент AdvancedSettings2, свойство
description: Получает указатель на интерфейс Имсрдпклиентадванцедсеттингс. Интерфейс можно использовать для задания дополнительных параметров клиентского элемента управления.
ms.assetid: 207b625c-fc2b-41ad-9339-9f3c3b8eeab7
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства AdvancedSettings2
- Службы удаленных рабочих столов свойства AdvancedSettings2, интерфейс Имсрдпклиент
- Службы удаленных рабочих столов интерфейса Имсрдпклиент, свойство AdvancedSettings2
- Службы удаленных рабочих столов свойства AdvancedSettings2, интерфейс IMsRdpClient2
- Службы удаленных рабочих столов интерфейса IMsRdpClient2, свойство AdvancedSettings2
- Службы удаленных рабочих столов свойства AdvancedSettings2, интерфейс IMsRdpClient3
- Службы удаленных рабочих столов интерфейса IMsRdpClient3, свойство AdvancedSettings2
- Службы удаленных рабочих столов свойства AdvancedSettings2, интерфейс IMsRdpClient4
- Службы удаленных рабочих столов интерфейса IMsRdpClient4, свойство AdvancedSettings2
- Службы удаленных рабочих столов свойства AdvancedSettings2, интерфейс IMsRdpClient5
- Службы удаленных рабочих столов интерфейса IMsRdpClient5, свойство AdvancedSettings2
- Службы удаленных рабочих столов свойства AdvancedSettings2, интерфейс IMsRdpClient6
- Службы удаленных рабочих столов интерфейса IMsRdpClient6, свойство AdvancedSettings2
- Службы удаленных рабочих столов свойства AdvancedSettings2, интерфейс IMsRdpClient7
- Службы удаленных рабочих столов интерфейса IMsRdpClient7, свойство AdvancedSettings2
- Службы удаленных рабочих столов свойства AdvancedSettings2, интерфейс IMsRdpClient8
- Службы удаленных рабочих столов интерфейса IMsRdpClient8, свойство AdvancedSettings2
- Службы удаленных рабочих столов свойства AdvancedSettings2, интерфейс IMsRdpClient9
- Службы удаленных рабочих столов интерфейса IMsRdpClient9, свойство AdvancedSettings2
- Службы удаленных рабочих столов свойства AdvancedSettings2, интерфейс IMsRdpClient10
- Службы удаленных рабочих столов интерфейса IMsRdpClient10, свойство AdvancedSettings2
topic_type:
- apiref
api_name:
- IMsRdpClient.AdvancedSettings2
- IMsRdpClient.get_AdvancedSettings2
- IMsRdpClient2.AdvancedSettings2
- IMsRdpClient2.get_AdvancedSettings2
- IMsRdpClient3.AdvancedSettings2
- IMsRdpClient3.get_AdvancedSettings2
- IMsRdpClient4.AdvancedSettings2
- IMsRdpClient4.get_AdvancedSettings2
- IMsRdpClient5.AdvancedSettings2
- IMsRdpClient5.get_AdvancedSettings2
- IMsRdpClient6.AdvancedSettings2
- IMsRdpClient6.get_AdvancedSettings2
- IMsRdpClient7.AdvancedSettings2
- IMsRdpClient7.get_AdvancedSettings2
- IMsRdpClient8.AdvancedSettings2
- IMsRdpClient8.get_AdvancedSettings2
- IMsRdpClient9.AdvancedSettings2
- IMsRdpClient9.get_AdvancedSettings2
- IMsRdpClient10.AdvancedSettings2
- IMsRdpClient10.get_AdvancedSettings2
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 683d56d5e9501114b1e60635ca406b4509d2032b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105682082"
---
# <a name="imsrdpclientadvancedsettings2-property"></a><span data-ttu-id="25f22-125">Свойство Имсрдпклиент:: AdvancedSettings2</span><span class="sxs-lookup"><span data-stu-id="25f22-125">IMsRdpClient::AdvancedSettings2 property</span></span>

<span data-ttu-id="25f22-126">Получает указатель на интерфейс [**имсрдпклиентадванцедсеттингс**](imsrdpclientadvancedsettings-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="25f22-126">Retrieves a pointer to the [**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md) interface.</span></span> <span data-ttu-id="25f22-127">Интерфейс можно использовать для задания дополнительных параметров клиентского элемента управления.</span><span class="sxs-lookup"><span data-stu-id="25f22-127">The interface can be used to set advanced settings for the client control.</span></span>

<span data-ttu-id="25f22-128">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="25f22-128">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="25f22-129">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="25f22-129">Syntax</span></span>


```C++
HRESULT get_AdvancedSettings2(
  [out] IMsRdpClientAdvancedSettings **ppAdvSettings
);
```



## <a name="property-value"></a><span data-ttu-id="25f22-130">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="25f22-130">Property value</span></span>

<span data-ttu-id="25f22-131">Указатель на интерфейс [**имсрдпклиентадванцедсеттингс**](imsrdpclientadvancedsettings-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="25f22-131">Pointer to the [**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md) interface.</span></span> <span data-ttu-id="25f22-132">Интерфейс можно использовать для задания дополнительных параметров клиентского элемента управления.</span><span class="sxs-lookup"><span data-stu-id="25f22-132">The interface can be used to set advanced settings for the client control.</span></span>

## <a name="error-codes"></a><span data-ttu-id="25f22-133">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="25f22-133">Error codes</span></span>

<span data-ttu-id="25f22-134">Если метод выполнен успешно, возвращается значение **S \_ OK** .</span><span class="sxs-lookup"><span data-stu-id="25f22-134">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="25f22-135">Любое другое значение **HRESULT** указывает на сбой вызова.</span><span class="sxs-lookup"><span data-stu-id="25f22-135">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="25f22-136">Комментарии</span><span class="sxs-lookup"><span data-stu-id="25f22-136">Remarks</span></span>

<span data-ttu-id="25f22-137">Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="25f22-137">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="25f22-138">Требования</span><span class="sxs-lookup"><span data-stu-id="25f22-138">Requirements</span></span>



| <span data-ttu-id="25f22-139">Требование</span><span class="sxs-lookup"><span data-stu-id="25f22-139">Requirement</span></span> | <span data-ttu-id="25f22-140">Значение</span><span class="sxs-lookup"><span data-stu-id="25f22-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="25f22-141">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="25f22-141">Minimum supported client</span></span><br/> | <span data-ttu-id="25f22-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="25f22-142">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="25f22-143">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="25f22-143">Minimum supported server</span></span><br/> | <span data-ttu-id="25f22-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="25f22-144">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="25f22-145">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="25f22-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="25f22-146"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="25f22-146"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="25f22-147">DLL</span><span class="sxs-lookup"><span data-stu-id="25f22-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="25f22-148"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="25f22-148"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="25f22-149">IID</span><span class="sxs-lookup"><span data-stu-id="25f22-149">IID</span></span><br/>                      | <span data-ttu-id="25f22-150">IID \_ имсрдпклиент определен как 92b4a539-7115-4b7c-a5a9-e5d9efc2780a</span><span class="sxs-lookup"><span data-stu-id="25f22-150">IID\_IMsRdpClient is defined as 92b4a539-7115-4b7c-a5a9-e5d9efc2780a</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="25f22-151">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="25f22-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25f22-152">**имсрдпклиент**</span><span class="sxs-lookup"><span data-stu-id="25f22-152">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="25f22-153">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="25f22-153">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="25f22-154">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="25f22-154">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="25f22-155">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="25f22-155">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="25f22-156">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="25f22-156">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="25f22-157">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="25f22-157">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="25f22-158">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="25f22-158">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="25f22-159">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="25f22-159">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="25f22-160">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="25f22-160">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="25f22-161">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="25f22-161">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





