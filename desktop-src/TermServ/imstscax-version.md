---
title: Свойство версии Имстскакс
description: Указывает номер версии текущего элемента управления.
ms.assetid: 91ddeb4c-9d61-41e7-af96-95b0c4884682
ms.tgt_platform: multiple
keywords:
- Свойство Version службы удаленных рабочих столов
- Свойство Version службы удаленных рабочих столов, интерфейс Имстскакс
- Службы удаленных рабочих столов интерфейса Имстскакс, свойство Version
- Свойство Version службы удаленных рабочих столов, интерфейс Имсрдпклиент
- Службы удаленных рабочих столов интерфейса Имсрдпклиент, свойство Version
- Свойство Version службы удаленных рабочих столов, интерфейс IMsRdpClient2
- Службы удаленных рабочих столов интерфейса IMsRdpClient2, свойство Version
- Свойство Version службы удаленных рабочих столов, интерфейс IMsRdpClient3
- Службы удаленных рабочих столов интерфейса IMsRdpClient3, свойство Version
- Свойство Version службы удаленных рабочих столов, интерфейс IMsRdpClient4
- Службы удаленных рабочих столов интерфейса IMsRdpClient4, свойство Version
- Свойство Version службы удаленных рабочих столов, интерфейс IMsRdpClient5
- Службы удаленных рабочих столов интерфейса IMsRdpClient5, свойство Version
- Свойство Version службы удаленных рабочих столов, интерфейс IMsRdpClient6
- Службы удаленных рабочих столов интерфейса IMsRdpClient6, свойство Version
- Свойство Version службы удаленных рабочих столов, интерфейс IMsRdpClient7
- Службы удаленных рабочих столов интерфейса IMsRdpClient7, свойство Version
- Свойство Version службы удаленных рабочих столов, интерфейс IMsRdpClient8
- Службы удаленных рабочих столов интерфейса IMsRdpClient8, свойство Version
- Свойство Version службы удаленных рабочих столов, интерфейс IMsRdpClient9
- Службы удаленных рабочих столов интерфейса IMsRdpClient9, свойство Version
topic_type:
- apiref
api_name:
- IMsTscAx.Version
- IMsTscAx.get_Version
- IMsRdpClient.Version
- IMsRdpClient.get_Version
- IMsRdpClient2.Version
- IMsRdpClient2.get_Version
- IMsRdpClient3.Version
- IMsRdpClient3.get_Version
- IMsRdpClient4.Version
- IMsRdpClient4.get_Version
- IMsRdpClient5.Version
- IMsRdpClient5.get_Version
- IMsRdpClient6.Version
- IMsRdpClient6.get_Version
- IMsRdpClient7.Version
- IMsRdpClient7.get_Version
- IMsRdpClient8.Version
- IMsRdpClient8.get_Version
- IMsRdpClient9.Version
- IMsRdpClient9.get_Version
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff25f274d1f076c9c4119648ccb9cc6d82f43b33
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490629"
---
# <a name="imstscaxversion-property"></a><span data-ttu-id="edd19-124">Свойство Имстскакс:: Version</span><span class="sxs-lookup"><span data-stu-id="edd19-124">IMsTscAx::Version property</span></span>

<span data-ttu-id="edd19-125">Указывает номер версии текущего элемента управления.</span><span class="sxs-lookup"><span data-stu-id="edd19-125">Specifies the version number of the current control.</span></span>

<span data-ttu-id="edd19-126">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="edd19-126">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="edd19-127">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="edd19-127">Syntax</span></span>


```C++
HRESULT get_Version(
  [out] BSTR *pVersion
);
```



## <a name="property-value"></a><span data-ttu-id="edd19-128">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="edd19-128">Property value</span></span>

<span data-ttu-id="edd19-129">Номер версии.</span><span class="sxs-lookup"><span data-stu-id="edd19-129">The version number.</span></span>

## <a name="error-codes"></a><span data-ttu-id="edd19-130">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="edd19-130">Error codes</span></span>

<span data-ttu-id="edd19-131">В случае успеха возвратите значение **\_ ОК** .</span><span class="sxs-lookup"><span data-stu-id="edd19-131">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="edd19-132">Комментарии</span><span class="sxs-lookup"><span data-stu-id="edd19-132">Remarks</span></span>

<span data-ttu-id="edd19-133">Этот метод выделяет память, необходимую для буфера, на который указывает параметр *пверсион* .</span><span class="sxs-lookup"><span data-stu-id="edd19-133">This method allocates the memory required for the buffer pointed to by the *pVersion* parameter.</span></span> <span data-ttu-id="edd19-134">Вызов приложений C/C++ должен освободить память с помощью вызова функции [**сисфристринг**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) .</span><span class="sxs-lookup"><span data-stu-id="edd19-134">Calling C/C++ applications must free the memory with a call to the [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) function.</span></span> <span data-ttu-id="edd19-135">Это не является обязательным для Visual Basic и скриптов клиентов.</span><span class="sxs-lookup"><span data-stu-id="edd19-135">This is not required for Visual Basic and scripting clients.</span></span>

<span data-ttu-id="edd19-136">Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="edd19-136">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="edd19-137">Требования</span><span class="sxs-lookup"><span data-stu-id="edd19-137">Requirements</span></span>



| <span data-ttu-id="edd19-138">Требование</span><span class="sxs-lookup"><span data-stu-id="edd19-138">Requirement</span></span> | <span data-ttu-id="edd19-139">Значение</span><span class="sxs-lookup"><span data-stu-id="edd19-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="edd19-140">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="edd19-140">Minimum supported client</span></span><br/> | <span data-ttu-id="edd19-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="edd19-141">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="edd19-142">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="edd19-142">Minimum supported server</span></span><br/> | <span data-ttu-id="edd19-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="edd19-143">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="edd19-144">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="edd19-144">Type library</span></span><br/>             | <dl> <span data-ttu-id="edd19-145"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="edd19-145"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="edd19-146">DLL</span><span class="sxs-lookup"><span data-stu-id="edd19-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="edd19-147"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="edd19-147"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="edd19-148">IID</span><span class="sxs-lookup"><span data-stu-id="edd19-148">IID</span></span><br/>                      | <span data-ttu-id="edd19-149">IID \_ имстскакс определен как 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="edd19-149">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="edd19-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="edd19-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="edd19-151">**имсрдпклиент**</span><span class="sxs-lookup"><span data-stu-id="edd19-151">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="edd19-152">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="edd19-152">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="edd19-153">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="edd19-153">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="edd19-154">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="edd19-154">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="edd19-155">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="edd19-155">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="edd19-156">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="edd19-156">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="edd19-157">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="edd19-157">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="edd19-158">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="edd19-158">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="edd19-159">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="edd19-159">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="edd19-160">**имстскакс**</span><span class="sxs-lookup"><span data-stu-id="edd19-160">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> </dl>

 

