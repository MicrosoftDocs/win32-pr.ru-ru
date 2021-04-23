---
title: Свойство сервера Имстскакс (Асптлб. h)
description: Указывает имя сервера, к которому подключен текущий элемент управления.
ms.assetid: 81118ddd-2662-47f5-8e9d-9c2a5056820b
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойств сервера
- Свойство сервера службы удаленных рабочих столов, интерфейс Имстскакс
- Службы удаленных рабочих столов интерфейса Имстскакс, свойство сервера
- Свойство сервера службы удаленных рабочих столов, интерфейс Имсрдпклиент
- Службы удаленных рабочих столов интерфейса Имсрдпклиент, свойство сервера
- Свойство сервера службы удаленных рабочих столов, интерфейс IMsRdpClient2
- Службы удаленных рабочих столов интерфейса IMsRdpClient2, свойство сервера
- Свойство сервера службы удаленных рабочих столов, интерфейс IMsRdpClient3
- Службы удаленных рабочих столов интерфейса IMsRdpClient3, свойство сервера
- Свойство сервера службы удаленных рабочих столов, интерфейс IMsRdpClient4
- Службы удаленных рабочих столов интерфейса IMsRdpClient4, свойство сервера
- Свойство сервера службы удаленных рабочих столов, интерфейс IMsRdpClient5
- Службы удаленных рабочих столов интерфейса IMsRdpClient5, свойство сервера
- Свойство сервера службы удаленных рабочих столов, интерфейс IMsRdpClient6
- Службы удаленных рабочих столов интерфейса IMsRdpClient6, свойство сервера
- Свойство сервера службы удаленных рабочих столов, интерфейс IMsRdpClient7
- Службы удаленных рабочих столов интерфейса IMsRdpClient7, свойство сервера
- Свойство сервера службы удаленных рабочих столов, интерфейс IMsRdpClient8
- Службы удаленных рабочих столов интерфейса IMsRdpClient8, свойство сервера
- Свойство сервера службы удаленных рабочих столов, интерфейс IMsRdpClient9
- Службы удаленных рабочих столов интерфейса IMsRdpClient9, свойство сервера
topic_type:
- apiref
api_name:
- IMsTscAx.Server
- IMsTscAx.get_Server
- IMsTscAx.put_Server
- IMsRdpClient.Server
- IMsRdpClient.get_Server
- IMsRdpClient.put_Server
- IMsRdpClient2.Server
- IMsRdpClient2.get_Server
- IMsRdpClient2.put_Server
- IMsRdpClient3.Server
- IMsRdpClient3.get_Server
- IMsRdpClient3.put_Server
- IMsRdpClient4.Server
- IMsRdpClient4.get_Server
- IMsRdpClient4.put_Server
- IMsRdpClient5.Server
- IMsRdpClient5.get_Server
- IMsRdpClient5.put_Server
- IMsRdpClient6.Server
- IMsRdpClient6.get_Server
- IMsRdpClient6.put_Server
- IMsRdpClient7.Server
- IMsRdpClient7.get_Server
- IMsRdpClient7.put_Server
- IMsRdpClient8.Server
- IMsRdpClient8.get_Server
- IMsRdpClient8.put_Server
- IMsRdpClient9.Server
- IMsRdpClient9.get_Server
- IMsRdpClient9.put_Server
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7b7be04c149e2ac10c1a3e905678bd2b5f663cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988276"
---
# <a name="imstscaxserver-property"></a><span data-ttu-id="4d16d-124">Свойство Имстскакс:: Server</span><span class="sxs-lookup"><span data-stu-id="4d16d-124">IMsTscAx::Server property</span></span>

<span data-ttu-id="4d16d-125">Указывает имя сервера, к которому подключен текущий элемент управления.</span><span class="sxs-lookup"><span data-stu-id="4d16d-125">Specifies the name of the server to which the current control is connected.</span></span>

<span data-ttu-id="4d16d-126">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="4d16d-126">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d16d-127">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4d16d-127">Syntax</span></span>


```C++
HRESULT put_Server(
  [in]  BSTR newVal
);

HRESULT get_Server(
  [out] BSTR *pServer
);
```



## <a name="property-value"></a><span data-ttu-id="4d16d-128">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="4d16d-128">Property value</span></span>

<span data-ttu-id="4d16d-129">Новое имя сервера.</span><span class="sxs-lookup"><span data-stu-id="4d16d-129">The new server name.</span></span> <span data-ttu-id="4d16d-130">Этот параметр может быть DNS-именем или IP-адресом.</span><span class="sxs-lookup"><span data-stu-id="4d16d-130">This parameter can be a DNS name or IP address.</span></span>

## <a name="error-codes"></a><span data-ttu-id="4d16d-131">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="4d16d-131">Error codes</span></span>

<span data-ttu-id="4d16d-132">Если методы выполнены успешно, возвращается значение **S \_ OK** .</span><span class="sxs-lookup"><span data-stu-id="4d16d-132">If the methods succeed, **S\_OK** is returned.</span></span> <span data-ttu-id="4d16d-133">Любое другое значение **HRESULT** указывает на сбой вызова.</span><span class="sxs-lookup"><span data-stu-id="4d16d-133">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="4d16d-134">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4d16d-134">Remarks</span></span>

<span data-ttu-id="4d16d-135">Это свойство должно быть установлено до вызова метода [**Connect**](imstscax-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="4d16d-135">This property must be set before calling the [**Connect**](imstscax-connect.md) method.</span></span> <span data-ttu-id="4d16d-136">Это единственное свойство, которое необходимо задать перед подключением.</span><span class="sxs-lookup"><span data-stu-id="4d16d-136">It is the only property that must be set before connecting.</span></span>

<span data-ttu-id="4d16d-137">Это свойство может быть задано только в том случае, если элемент управления не находится в состоянии Connected.</span><span class="sxs-lookup"><span data-stu-id="4d16d-137">This property can be set only if the control is not in the connected state.</span></span> <span data-ttu-id="4d16d-138">Это свойство возвращает значение **E \_ Fail** , если оно вызывается при соединении элемента управления.</span><span class="sxs-lookup"><span data-stu-id="4d16d-138">This property returns **E\_FAIL** if it is called when the control is connected.</span></span> <span data-ttu-id="4d16d-139">Проверить состояние подключения можно с помощью свойства [**подключено**](imstscax-connected.md) .</span><span class="sxs-lookup"><span data-stu-id="4d16d-139">You can check for the connected state by using the [**Connected**](imstscax-connected.md) property.</span></span>

<span data-ttu-id="4d16d-140">Этот метод выделяет память, необходимую для буфера, на который указывает параметр *псервер* .</span><span class="sxs-lookup"><span data-stu-id="4d16d-140">This method allocates the memory required for the buffer pointed to by the *pServer* parameter.</span></span> <span data-ttu-id="4d16d-141">Вызов приложений C/C++ должен освободить память с помощью вызова функции [**сисфристринг**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) .</span><span class="sxs-lookup"><span data-stu-id="4d16d-141">Calling C/C++ applications must free the memory with a call to the [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) function.</span></span> <span data-ttu-id="4d16d-142">Это не является обязательным для Visual Basic и скриптов клиентов.</span><span class="sxs-lookup"><span data-stu-id="4d16d-142">This is not required for Visual Basic and scripting clients.</span></span>

<span data-ttu-id="4d16d-143">Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="4d16d-143">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4d16d-144">Требования</span><span class="sxs-lookup"><span data-stu-id="4d16d-144">Requirements</span></span>



| <span data-ttu-id="4d16d-145">Требование</span><span class="sxs-lookup"><span data-stu-id="4d16d-145">Requirement</span></span> | <span data-ttu-id="4d16d-146">Значение</span><span class="sxs-lookup"><span data-stu-id="4d16d-146">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4d16d-147">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4d16d-147">Minimum supported client</span></span><br/> | <span data-ttu-id="4d16d-148">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4d16d-148">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="4d16d-149">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4d16d-149">Minimum supported server</span></span><br/> | <span data-ttu-id="4d16d-150">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4d16d-150">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="4d16d-151">Header</span><span class="sxs-lookup"><span data-stu-id="4d16d-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="4d16d-152"><dt>Асптлб. h</dt></span><span class="sxs-lookup"><span data-stu-id="4d16d-152"><dt>Asptlb.h</dt></span></span> </dl>    |
| <span data-ttu-id="4d16d-153">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="4d16d-153">Type library</span></span><br/>             | <dl> <span data-ttu-id="4d16d-154"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4d16d-154"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="4d16d-155">DLL</span><span class="sxs-lookup"><span data-stu-id="4d16d-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4d16d-156"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4d16d-156"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="4d16d-157">IID</span><span class="sxs-lookup"><span data-stu-id="4d16d-157">IID</span></span><br/>                      | <span data-ttu-id="4d16d-158">IID \_ имстскакс определен как 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="4d16d-158">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="4d16d-159">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4d16d-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d16d-160">**имсрдпклиент**</span><span class="sxs-lookup"><span data-stu-id="4d16d-160">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="4d16d-161">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="4d16d-161">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="4d16d-162">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="4d16d-162">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="4d16d-163">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="4d16d-163">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="4d16d-164">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="4d16d-164">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="4d16d-165">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="4d16d-165">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="4d16d-166">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="4d16d-166">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="4d16d-167">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="4d16d-167">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="4d16d-168">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="4d16d-168">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="4d16d-169">**имстскакс**</span><span class="sxs-lookup"><span data-stu-id="4d16d-169">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> </dl>

 

