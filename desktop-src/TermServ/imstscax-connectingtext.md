---
title: Имстскакс Коннектингтекст, свойство
description: Задает текст, отображаемый в центре элемента управления во время подключения элемента управления.
ms.assetid: 9bc82074-988f-491b-80e3-00c3f7ba437a
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Коннектингтекст
- Службы удаленных рабочих столов свойства Коннектингтекст, интерфейс Имстскакс
- Службы удаленных рабочих столов интерфейса Имстскакс, свойство Коннектингтекст
- Службы удаленных рабочих столов свойства Коннектингтекст, интерфейс Имсрдпклиент
- Службы удаленных рабочих столов интерфейса Имсрдпклиент, свойство Коннектингтекст
- Службы удаленных рабочих столов свойства Коннектингтекст, интерфейс IMsRdpClient2
- Службы удаленных рабочих столов интерфейса IMsRdpClient2, свойство Коннектингтекст
- Службы удаленных рабочих столов свойства Коннектингтекст, интерфейс IMsRdpClient3
- Службы удаленных рабочих столов интерфейса IMsRdpClient3, свойство Коннектингтекст
- Службы удаленных рабочих столов свойства Коннектингтекст, интерфейс IMsRdpClient4
- Службы удаленных рабочих столов интерфейса IMsRdpClient4, свойство Коннектингтекст
- Службы удаленных рабочих столов свойства Коннектингтекст, интерфейс IMsRdpClient5
- Службы удаленных рабочих столов интерфейса IMsRdpClient5, свойство Коннектингтекст
- Службы удаленных рабочих столов свойства Коннектингтекст, интерфейс IMsRdpClient6
- Службы удаленных рабочих столов интерфейса IMsRdpClient6, свойство Коннектингтекст
- Службы удаленных рабочих столов свойства Коннектингтекст, интерфейс IMsRdpClient7
- Службы удаленных рабочих столов интерфейса IMsRdpClient7, свойство Коннектингтекст
- Службы удаленных рабочих столов свойства Коннектингтекст, интерфейс IMsRdpClient8
- Службы удаленных рабочих столов интерфейса IMsRdpClient8, свойство Коннектингтекст
- Службы удаленных рабочих столов свойства Коннектингтекст, интерфейс IMsRdpClient9
- Службы удаленных рабочих столов интерфейса IMsRdpClient9, свойство Коннектингтекст
topic_type:
- apiref
api_name:
- IMsTscAx.ConnectingText
- IMsTscAx.get_ConnectingText
- IMsTscAx.put_ConnectingText
- IMsRdpClient.ConnectingText
- IMsRdpClient.get_ConnectingText
- IMsRdpClient.put_ConnectingText
- IMsRdpClient2.ConnectingText
- IMsRdpClient2.get_ConnectingText
- IMsRdpClient2.put_ConnectingText
- IMsRdpClient3.ConnectingText
- IMsRdpClient3.get_ConnectingText
- IMsRdpClient3.put_ConnectingText
- IMsRdpClient4.ConnectingText
- IMsRdpClient4.get_ConnectingText
- IMsRdpClient4.put_ConnectingText
- IMsRdpClient5.ConnectingText
- IMsRdpClient5.get_ConnectingText
- IMsRdpClient5.put_ConnectingText
- IMsRdpClient6.ConnectingText
- IMsRdpClient6.get_ConnectingText
- IMsRdpClient6.put_ConnectingText
- IMsRdpClient7.ConnectingText
- IMsRdpClient7.get_ConnectingText
- IMsRdpClient7.put_ConnectingText
- IMsRdpClient8.ConnectingText
- IMsRdpClient8.get_ConnectingText
- IMsRdpClient8.put_ConnectingText
- IMsRdpClient9.ConnectingText
- IMsRdpClient9.get_ConnectingText
- IMsRdpClient9.put_ConnectingText
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 433da7d159f1fe5bf44114a0b76ed9b4d807046f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415856"
---
# <a name="imstscaxconnectingtext-property"></a><span data-ttu-id="122ba-124">Свойство Имстскакс:: Коннектингтекст</span><span class="sxs-lookup"><span data-stu-id="122ba-124">IMsTscAx::ConnectingText property</span></span>

<span data-ttu-id="122ba-125">Задает текст, отображаемый в центре элемента управления во время подключения элемента управления.</span><span class="sxs-lookup"><span data-stu-id="122ba-125">Specifies the text that appears centered in the control while the control is connecting.</span></span>

<span data-ttu-id="122ba-126">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="122ba-126">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="122ba-127">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="122ba-127">Syntax</span></span>


```C++
HRESULT put_ConnectingText(
  [in]  BSTR newVal
);

HRESULT get_ConnectingText(
  [out] BSTR *pConnectingText
);
```



## <a name="property-value"></a><span data-ttu-id="122ba-128">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="122ba-128">Property value</span></span>

<span data-ttu-id="122ba-129">Новый отображаемый текст.</span><span class="sxs-lookup"><span data-stu-id="122ba-129">The new display text.</span></span>

## <a name="error-codes"></a><span data-ttu-id="122ba-130">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="122ba-130">Error codes</span></span>

<span data-ttu-id="122ba-131">В случае успеха возвратите значение **\_ ОК** .</span><span class="sxs-lookup"><span data-stu-id="122ba-131">Return **S\_OK** if successful.</span></span>

<span data-ttu-id="122ba-132">При возникновении ошибки возвращайте ненулевое **значение HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="122ba-132">Return a nonzero **HRESULT** if an error occurs.</span></span>

## <a name="remarks"></a><span data-ttu-id="122ba-133">Комментарии</span><span class="sxs-lookup"><span data-stu-id="122ba-133">Remarks</span></span>

<span data-ttu-id="122ba-134">Пример текста соединения — «подключение к серверу...».</span><span class="sxs-lookup"><span data-stu-id="122ba-134">An example of connection text is "Connecting to server ...".</span></span>

<span data-ttu-id="122ba-135">Установка свойства **коннектингтекст** является необязательной.</span><span class="sxs-lookup"><span data-stu-id="122ba-135">Setting the **ConnectingText** property is optional.</span></span> <span data-ttu-id="122ba-136">Если оно не задано, элемент управления отображается пустым до установления соединения.</span><span class="sxs-lookup"><span data-stu-id="122ba-136">If it is not set, the control appears blank before a connection is established.</span></span>

<span data-ttu-id="122ba-137">Это свойство может быть задано только в том случае, если элемент управления не находится в состоянии Connected.</span><span class="sxs-lookup"><span data-stu-id="122ba-137">This property can be set only if the control is not in the connected state.</span></span> <span data-ttu-id="122ba-138">Он возвращает **E \_ Fail** , если он вызывается при соединении элемента управления.</span><span class="sxs-lookup"><span data-stu-id="122ba-138">It returns **E\_FAIL** if it is called when the control is connected.</span></span> <span data-ttu-id="122ba-139">Проверить, подключен ли элемент управления, можно, отреагировать на события соединения в [**имстскаксевентс**](imstscaxevents-interface.md) или изучив свойство [**Connected**](imstscax-connected.md) .</span><span class="sxs-lookup"><span data-stu-id="122ba-139">You can check if the control is connected by responding to connection events in [**IMsTscAxEvents**](imstscaxevents-interface.md) or examining the [**Connected**](imstscax-connected.md) property.</span></span>

<span data-ttu-id="122ba-140">Метод свойства **Get \_ коннектингтекст** выделяет память, необходимую для буфера, на который указывает параметр *пконнектингтекст* .</span><span class="sxs-lookup"><span data-stu-id="122ba-140">The **get\_ConnectingText** property method allocates the memory required for the buffer pointed to by the *pConnectingText* parameter.</span></span> <span data-ttu-id="122ba-141">Вызов приложений C/C++ должен освободить память с помощью вызова функции [**сисфристринг**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) .</span><span class="sxs-lookup"><span data-stu-id="122ba-141">Calling C/C++ applications must free the memory with a call to the [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) function.</span></span> <span data-ttu-id="122ba-142">Это не является обязательным для Visual Basic и скриптов клиентов.</span><span class="sxs-lookup"><span data-stu-id="122ba-142">This is not required for Visual Basic and scripting clients.</span></span>

<span data-ttu-id="122ba-143">Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="122ba-143">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="122ba-144">Требования</span><span class="sxs-lookup"><span data-stu-id="122ba-144">Requirements</span></span>



| <span data-ttu-id="122ba-145">Требование</span><span class="sxs-lookup"><span data-stu-id="122ba-145">Requirement</span></span> | <span data-ttu-id="122ba-146">Значение</span><span class="sxs-lookup"><span data-stu-id="122ba-146">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="122ba-147">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="122ba-147">Minimum supported client</span></span><br/> | <span data-ttu-id="122ba-148">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="122ba-148">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="122ba-149">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="122ba-149">Minimum supported server</span></span><br/> | <span data-ttu-id="122ba-150">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="122ba-150">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="122ba-151">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="122ba-151">Type library</span></span><br/>             | <dl> <span data-ttu-id="122ba-152"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="122ba-152"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="122ba-153">DLL</span><span class="sxs-lookup"><span data-stu-id="122ba-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="122ba-154"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="122ba-154"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="122ba-155">IID</span><span class="sxs-lookup"><span data-stu-id="122ba-155">IID</span></span><br/>                      | <span data-ttu-id="122ba-156">IID \_ имстскакс определен как 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="122ba-156">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="122ba-157">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="122ba-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="122ba-158">**имсрдпклиент**</span><span class="sxs-lookup"><span data-stu-id="122ba-158">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="122ba-159">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="122ba-159">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="122ba-160">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="122ba-160">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="122ba-161">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="122ba-161">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="122ba-162">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="122ba-162">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="122ba-163">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="122ba-163">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="122ba-164">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="122ba-164">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="122ba-165">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="122ba-165">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="122ba-166">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="122ba-166">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="122ba-167">**имстскакс**</span><span class="sxs-lookup"><span data-stu-id="122ba-167">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> </dl>

 

