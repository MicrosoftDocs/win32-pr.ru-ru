---
title: Свойство UserName Имстскакс
description: Указывает учетные данные имени пользователя для входа.
ms.assetid: 9be25003-b9aa-41bb-a5a9-512546175114
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства имени пользователя
- Свойство UserName службы удаленных рабочих столов, интерфейс Имстскакс
- Службы удаленных рабочих столов интерфейса Имстскакс, свойство UserName
- Свойство UserName службы удаленных рабочих столов, интерфейс Имсрдпклиент
- Службы удаленных рабочих столов интерфейса Имсрдпклиент, свойство UserName
- Свойство UserName службы удаленных рабочих столов, интерфейс IMsRdpClient2
- Службы удаленных рабочих столов интерфейса IMsRdpClient2, свойство UserName
- Свойство UserName службы удаленных рабочих столов, интерфейс IMsRdpClient3
- Службы удаленных рабочих столов интерфейса IMsRdpClient3, свойство UserName
- Свойство UserName службы удаленных рабочих столов, интерфейс IMsRdpClient4
- Службы удаленных рабочих столов интерфейса IMsRdpClient4, свойство UserName
- Свойство UserName службы удаленных рабочих столов, интерфейс IMsRdpClient5
- Службы удаленных рабочих столов интерфейса IMsRdpClient5, свойство UserName
- Свойство UserName службы удаленных рабочих столов, интерфейс IMsRdpClient6
- Службы удаленных рабочих столов интерфейса IMsRdpClient6, свойство UserName
- Свойство UserName службы удаленных рабочих столов, интерфейс IMsRdpClient7
- Службы удаленных рабочих столов интерфейса IMsRdpClient7, свойство UserName
- Свойство UserName службы удаленных рабочих столов, интерфейс IMsRdpClient8
- Службы удаленных рабочих столов интерфейса IMsRdpClient8, свойство UserName
- Свойство UserName службы удаленных рабочих столов, интерфейс IMsRdpClient9
- Службы удаленных рабочих столов интерфейса IMsRdpClient9, свойство UserName
topic_type:
- apiref
api_name:
- IMsTscAx.UserName
- IMsTscAx.get_UserName
- IMsTscAx.put_UserName
- IMsRdpClient.UserName
- IMsRdpClient.get_UserName
- IMsRdpClient.put_UserName
- IMsRdpClient2.UserName
- IMsRdpClient2.get_UserName
- IMsRdpClient2.put_UserName
- IMsRdpClient3.UserName
- IMsRdpClient3.get_UserName
- IMsRdpClient3.put_UserName
- IMsRdpClient4.UserName
- IMsRdpClient4.get_UserName
- IMsRdpClient4.put_UserName
- IMsRdpClient5.UserName
- IMsRdpClient5.get_UserName
- IMsRdpClient5.put_UserName
- IMsRdpClient6.UserName
- IMsRdpClient6.get_UserName
- IMsRdpClient6.put_UserName
- IMsRdpClient7.UserName
- IMsRdpClient7.get_UserName
- IMsRdpClient7.put_UserName
- IMsRdpClient8.UserName
- IMsRdpClient8.get_UserName
- IMsRdpClient8.put_UserName
- IMsRdpClient9.UserName
- IMsRdpClient9.get_UserName
- IMsRdpClient9.put_UserName
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a94a7f7d9fe5d6532de55f36a50094205fe1d4ac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492921"
---
# <a name="imstscaxusername-property"></a><span data-ttu-id="d36a6-124">Свойство Имстскакс:: UserName</span><span class="sxs-lookup"><span data-stu-id="d36a6-124">IMsTscAx::UserName property</span></span>

<span data-ttu-id="d36a6-125">Указывает учетные данные имени пользователя для входа.</span><span class="sxs-lookup"><span data-stu-id="d36a6-125">Specifies the user name logon credential.</span></span>

<span data-ttu-id="d36a6-126">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="d36a6-126">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="d36a6-127">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d36a6-127">Syntax</span></span>


```C++
HRESULT put_UserName(
  [in]  BSTR newVal
);

HRESULT get_UserName(
  [out] BSTR *pUserName
);
```



## <a name="property-value"></a><span data-ttu-id="d36a6-128">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="d36a6-128">Property value</span></span>

<span data-ttu-id="d36a6-129">Новое имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="d36a6-129">The new user name.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d36a6-130">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="d36a6-130">Error codes</span></span>

<span data-ttu-id="d36a6-131">В случае успеха возвратите значение **\_ ОК** .</span><span class="sxs-lookup"><span data-stu-id="d36a6-131">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="d36a6-132">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d36a6-132">Remarks</span></span>

<span data-ttu-id="d36a6-133">Задавать свойство **username** необязательно.</span><span class="sxs-lookup"><span data-stu-id="d36a6-133">Setting the **UserName** property is optional.</span></span> <span data-ttu-id="d36a6-134">Если он не указан, пользователь может указать имя пользователя при появлении диалогового окна входа в систему Windows во время подключения.</span><span class="sxs-lookup"><span data-stu-id="d36a6-134">If it is not specified, the user can provide a user name when the Windows Logon dialog box appears during connection.</span></span>

<span data-ttu-id="d36a6-135">Это свойство может быть задано только в том случае, если элемент управления не находится в состоянии Connected.</span><span class="sxs-lookup"><span data-stu-id="d36a6-135">This property can be set only if the control is not in the connected state.</span></span> <span data-ttu-id="d36a6-136">Он возвращает **E \_ Fail** , если он вызывается при соединении элемента управления.</span><span class="sxs-lookup"><span data-stu-id="d36a6-136">It returns **E\_FAIL** if it is called when the control is connected.</span></span> <span data-ttu-id="d36a6-137">Проверить, подключен ли элемент управления, можно, отреагировать на события соединения в [**имстскаксевентс**](imstscaxevents-interface.md) или изучив свойство [**Connected**](imstscax-connected.md) .</span><span class="sxs-lookup"><span data-stu-id="d36a6-137">You can check if the control is connected by responding to connection events in [**IMsTscAxEvents**](imstscaxevents-interface.md) or examining the [**Connected**](imstscax-connected.md) property.</span></span>

<span data-ttu-id="d36a6-138">Метод **получения свойства \_ username** выделяет память, необходимую для буфера, на который указывает параметр *пверсион* .</span><span class="sxs-lookup"><span data-stu-id="d36a6-138">The **get\_UserName** property method allocates the memory required for the buffer pointed to by the *pVersion* parameter.</span></span> <span data-ttu-id="d36a6-139">Вызов приложений C/C++ должен освободить память с помощью вызова функции [**сисфристринг**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) .</span><span class="sxs-lookup"><span data-stu-id="d36a6-139">Calling C/C++ applications must free the memory with a call to the [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) function.</span></span> <span data-ttu-id="d36a6-140">Это не является обязательным для Visual Basic и скриптов клиентов.</span><span class="sxs-lookup"><span data-stu-id="d36a6-140">This is not required for Visual Basic and scripting clients.</span></span>

<span data-ttu-id="d36a6-141">Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="d36a6-141">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d36a6-142">Требования</span><span class="sxs-lookup"><span data-stu-id="d36a6-142">Requirements</span></span>



| <span data-ttu-id="d36a6-143">Требование</span><span class="sxs-lookup"><span data-stu-id="d36a6-143">Requirement</span></span> | <span data-ttu-id="d36a6-144">Значение</span><span class="sxs-lookup"><span data-stu-id="d36a6-144">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d36a6-145">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d36a6-145">Minimum supported client</span></span><br/> | <span data-ttu-id="d36a6-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d36a6-146">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="d36a6-147">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d36a6-147">Minimum supported server</span></span><br/> | <span data-ttu-id="d36a6-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d36a6-148">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="d36a6-149">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="d36a6-149">Type library</span></span><br/>             | <dl> <span data-ttu-id="d36a6-150"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d36a6-150"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="d36a6-151">DLL</span><span class="sxs-lookup"><span data-stu-id="d36a6-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d36a6-152"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d36a6-152"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="d36a6-153">IID</span><span class="sxs-lookup"><span data-stu-id="d36a6-153">IID</span></span><br/>                      | <span data-ttu-id="d36a6-154">IID \_ имстскакс определен как 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="d36a6-154">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="d36a6-155">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d36a6-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d36a6-156">**имсрдпклиент**</span><span class="sxs-lookup"><span data-stu-id="d36a6-156">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="d36a6-157">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="d36a6-157">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="d36a6-158">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="d36a6-158">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="d36a6-159">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="d36a6-159">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="d36a6-160">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="d36a6-160">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="d36a6-161">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="d36a6-161">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="d36a6-162">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="d36a6-162">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="d36a6-163">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="d36a6-163">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="d36a6-164">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="d36a6-164">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="d36a6-165">**имстскакс**</span><span class="sxs-lookup"><span data-stu-id="d36a6-165">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> </dl>

 

