---
title: Имстскакс, свойство домена
description: Указывает домен, в который входит текущий пользователь.
ms.assetid: 5d9a2048-5f5d-43ca-a8b8-400dac7d7472
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойств домена
- Службы удаленных рабочих столов свойств домена, интерфейс Имстскакс
- Службы удаленных рабочих столов интерфейса Имстскакс, свойство Domain
- Службы удаленных рабочих столов свойств домена, интерфейс Имсрдпклиент
- Службы удаленных рабочих столов интерфейса Имсрдпклиент, свойство Domain
- Службы удаленных рабочих столов свойств домена, интерфейс IMsRdpClient2
- Службы удаленных рабочих столов интерфейса IMsRdpClient2, свойство Domain
- Службы удаленных рабочих столов свойств домена, интерфейс IMsRdpClient3
- Службы удаленных рабочих столов интерфейса IMsRdpClient3, свойство Domain
- Службы удаленных рабочих столов свойств домена, интерфейс IMsRdpClient4
- Службы удаленных рабочих столов интерфейса IMsRdpClient4, свойство Domain
- Службы удаленных рабочих столов свойств домена, интерфейс IMsRdpClient5
- Службы удаленных рабочих столов интерфейса IMsRdpClient5, свойство Domain
- Службы удаленных рабочих столов свойств домена, интерфейс IMsRdpClient6
- Службы удаленных рабочих столов интерфейса IMsRdpClient6, свойство Domain
- Службы удаленных рабочих столов свойств домена, интерфейс IMsRdpClient7
- Службы удаленных рабочих столов интерфейса IMsRdpClient7, свойство Domain
- Службы удаленных рабочих столов свойств домена, интерфейс IMsRdpClient8
- Службы удаленных рабочих столов интерфейса IMsRdpClient8, свойство Domain
- Службы удаленных рабочих столов свойств домена, интерфейс IMsRdpClient9
- Службы удаленных рабочих столов интерфейса IMsRdpClient9, свойство Domain
topic_type:
- apiref
api_name:
- IMsTscAx.Domain
- IMsTscAx.get_Domain
- IMsTscAx.put_Domain
- IMsRdpClient.Domain
- IMsRdpClient.get_Domain
- IMsRdpClient.put_Domain
- IMsRdpClient2.Domain
- IMsRdpClient2.get_Domain
- IMsRdpClient2.put_Domain
- IMsRdpClient3.Domain
- IMsRdpClient3.get_Domain
- IMsRdpClient3.put_Domain
- IMsRdpClient4.Domain
- IMsRdpClient4.get_Domain
- IMsRdpClient4.put_Domain
- IMsRdpClient5.Domain
- IMsRdpClient5.get_Domain
- IMsRdpClient5.put_Domain
- IMsRdpClient6.Domain
- IMsRdpClient6.get_Domain
- IMsRdpClient6.put_Domain
- IMsRdpClient7.Domain
- IMsRdpClient7.get_Domain
- IMsRdpClient7.put_Domain
- IMsRdpClient8.Domain
- IMsRdpClient8.get_Domain
- IMsRdpClient8.put_Domain
- IMsRdpClient9.Domain
- IMsRdpClient9.get_Domain
- IMsRdpClient9.put_Domain
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: faf95c02de10fe8db38a53b75d4d20cf796020f8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989250"
---
# <a name="imstscaxdomain-property"></a><span data-ttu-id="b9a35-124">Имстскакс: свойство омаин:D</span><span class="sxs-lookup"><span data-stu-id="b9a35-124">IMsTscAx::Domain property</span></span>

<span data-ttu-id="b9a35-125">Указывает домен, в который входит текущий пользователь.</span><span class="sxs-lookup"><span data-stu-id="b9a35-125">Specifies the domain to which the current user logs on.</span></span>

<span data-ttu-id="b9a35-126">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="b9a35-126">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9a35-127">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b9a35-127">Syntax</span></span>


```C++
HRESULT put_Domain(
  [in]  BSTR newVal
);

HRESULT get_Domain(
  [out] BSTR *pDomain
);
```



## <a name="property-value"></a><span data-ttu-id="b9a35-128">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="b9a35-128">Property value</span></span>

<span data-ttu-id="b9a35-129">Новое доменное имя.</span><span class="sxs-lookup"><span data-stu-id="b9a35-129">The new domain name.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b9a35-130">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="b9a35-130">Error codes</span></span>

<span data-ttu-id="b9a35-131">В случае успеха возвратите значение **\_ ОК** .</span><span class="sxs-lookup"><span data-stu-id="b9a35-131">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="b9a35-132">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b9a35-132">Remarks</span></span>

<span data-ttu-id="b9a35-133">Задание свойства **домена** является необязательным.</span><span class="sxs-lookup"><span data-stu-id="b9a35-133">Setting the **Domain** property is optional.</span></span> <span data-ttu-id="b9a35-134">Если оно не задано, пользователь может выбрать домен при появлении диалогового окна входа в систему Windows во время подключения.</span><span class="sxs-lookup"><span data-stu-id="b9a35-134">If it is not set, the user can choose a domain when the Windows Logon dialog box appears during the connection.</span></span>

<span data-ttu-id="b9a35-135">Метод **Get \_ domain** выделяет память, необходимую для буфера, на который указывает параметр *пдомаин* .</span><span class="sxs-lookup"><span data-stu-id="b9a35-135">The **get\_Domain** method allocates the memory required for the buffer pointed to by the *pDomain* parameter.</span></span> <span data-ttu-id="b9a35-136">Вызов приложений C/C++ должен освободить память с помощью вызова функции [**сисфристринг**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) .</span><span class="sxs-lookup"><span data-stu-id="b9a35-136">Calling C/C++ applications must free the memory with a call to the [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) function.</span></span> <span data-ttu-id="b9a35-137">Это не является обязательным для Visual Basic и скриптов клиентов.</span><span class="sxs-lookup"><span data-stu-id="b9a35-137">This is not required for Visual Basic and scripting clients.</span></span>

<span data-ttu-id="b9a35-138">Это свойство может быть задано только в том случае, если элемент управления не находится в состоянии Connected.</span><span class="sxs-lookup"><span data-stu-id="b9a35-138">This property can be set only if the control is not in the connected state.</span></span> <span data-ttu-id="b9a35-139">Он возвращает **E \_ Fail** , если он вызывается при соединении элемента управления.</span><span class="sxs-lookup"><span data-stu-id="b9a35-139">It returns **E\_FAIL** if it is called when the control is connected.</span></span> <span data-ttu-id="b9a35-140">Проверить, подключен ли элемент управления, можно, отреагировать на события соединения в [**имстскаксевентс**](imstscaxevents-interface.md) или изучив свойство [**Connected**](imstscax-connected.md) .</span><span class="sxs-lookup"><span data-stu-id="b9a35-140">You can check if the control is connected by responding to connection events in [**IMsTscAxEvents**](imstscaxevents-interface.md) or examining the [**Connected**](imstscax-connected.md) property.</span></span>

<span data-ttu-id="b9a35-141">Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="b9a35-141">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b9a35-142">Требования</span><span class="sxs-lookup"><span data-stu-id="b9a35-142">Requirements</span></span>



| <span data-ttu-id="b9a35-143">Требование</span><span class="sxs-lookup"><span data-stu-id="b9a35-143">Requirement</span></span> | <span data-ttu-id="b9a35-144">Значение</span><span class="sxs-lookup"><span data-stu-id="b9a35-144">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b9a35-145">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b9a35-145">Minimum supported client</span></span><br/> | <span data-ttu-id="b9a35-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b9a35-146">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="b9a35-147">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b9a35-147">Minimum supported server</span></span><br/> | <span data-ttu-id="b9a35-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b9a35-148">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="b9a35-149">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="b9a35-149">Type library</span></span><br/>             | <dl> <span data-ttu-id="b9a35-150"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b9a35-150"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="b9a35-151">DLL</span><span class="sxs-lookup"><span data-stu-id="b9a35-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b9a35-152"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b9a35-152"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="b9a35-153">IID</span><span class="sxs-lookup"><span data-stu-id="b9a35-153">IID</span></span><br/>                      | <span data-ttu-id="b9a35-154">IID \_ имстскакс определен как 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="b9a35-154">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="b9a35-155">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b9a35-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9a35-156">**имсрдпклиент**</span><span class="sxs-lookup"><span data-stu-id="b9a35-156">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="b9a35-157">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="b9a35-157">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="b9a35-158">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="b9a35-158">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="b9a35-159">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="b9a35-159">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="b9a35-160">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="b9a35-160">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="b9a35-161">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="b9a35-161">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="b9a35-162">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="b9a35-162">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="b9a35-163">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="b9a35-163">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="b9a35-164">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="b9a35-164">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="b9a35-165">**Подключен**</span><span class="sxs-lookup"><span data-stu-id="b9a35-165">**Connected**</span></span>](imstscax-connected.md)
</dt> <dt>

[<span data-ttu-id="b9a35-166">**имстскакс**</span><span class="sxs-lookup"><span data-stu-id="b9a35-166">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> <dt>

[<span data-ttu-id="b9a35-167">**имстскаксевентс**</span><span class="sxs-lookup"><span data-stu-id="b9a35-167">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

