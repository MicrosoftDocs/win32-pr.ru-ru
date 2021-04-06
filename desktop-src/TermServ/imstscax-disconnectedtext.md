---
title: Имстскакс Дисконнектедтекст, свойство
description: Задает текст, отображаемый по центру элемента управления до завершения соединения.
ms.assetid: ec7efe7a-8fb9-4c45-8e16-78951365de13
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Дисконнектедтекст
- Службы удаленных рабочих столов свойства Дисконнектедтекст, интерфейс Имстскакс
- Службы удаленных рабочих столов интерфейса Имстскакс, свойство Дисконнектедтекст
- Службы удаленных рабочих столов свойства Дисконнектедтекст, интерфейс Имсрдпклиент
- Службы удаленных рабочих столов интерфейса Имсрдпклиент, свойство Дисконнектедтекст
- Службы удаленных рабочих столов свойства Дисконнектедтекст, интерфейс IMsRdpClient2
- Службы удаленных рабочих столов интерфейса IMsRdpClient2, свойство Дисконнектедтекст
- Службы удаленных рабочих столов свойства Дисконнектедтекст, интерфейс IMsRdpClient3
- Службы удаленных рабочих столов интерфейса IMsRdpClient3, свойство Дисконнектедтекст
- Службы удаленных рабочих столов свойства Дисконнектедтекст, интерфейс IMsRdpClient4
- Службы удаленных рабочих столов интерфейса IMsRdpClient4, свойство Дисконнектедтекст
- Службы удаленных рабочих столов свойства Дисконнектедтекст, интерфейс IMsRdpClient5
- Службы удаленных рабочих столов интерфейса IMsRdpClient5, свойство Дисконнектедтекст
- Службы удаленных рабочих столов свойства Дисконнектедтекст, интерфейс IMsRdpClient6
- Службы удаленных рабочих столов интерфейса IMsRdpClient6, свойство Дисконнектедтекст
- Службы удаленных рабочих столов свойства Дисконнектедтекст, интерфейс IMsRdpClient7
- Службы удаленных рабочих столов интерфейса IMsRdpClient7, свойство Дисконнектедтекст
- Службы удаленных рабочих столов свойства Дисконнектедтекст, интерфейс IMsRdpClient8
- Службы удаленных рабочих столов интерфейса IMsRdpClient8, свойство Дисконнектедтекст
- Службы удаленных рабочих столов свойства Дисконнектедтекст, интерфейс IMsRdpClient9
- Службы удаленных рабочих столов интерфейса IMsRdpClient9, свойство Дисконнектедтекст
topic_type:
- apiref
api_name:
- IMsTscAx.DisconnectedText
- IMsTscAx.get_DisconnectedText
- IMsTscAx.put_DisconnectedText
- IMsRdpClient.DisconnectedText
- IMsRdpClient.get_DisconnectedText
- IMsRdpClient.put_DisconnectedText
- IMsRdpClient2.DisconnectedText
- IMsRdpClient2.get_DisconnectedText
- IMsRdpClient2.put_DisconnectedText
- IMsRdpClient3.DisconnectedText
- IMsRdpClient3.get_DisconnectedText
- IMsRdpClient3.put_DisconnectedText
- IMsRdpClient4.DisconnectedText
- IMsRdpClient4.get_DisconnectedText
- IMsRdpClient4.put_DisconnectedText
- IMsRdpClient5.DisconnectedText
- IMsRdpClient5.get_DisconnectedText
- IMsRdpClient5.put_DisconnectedText
- IMsRdpClient6.DisconnectedText
- IMsRdpClient6.get_DisconnectedText
- IMsRdpClient6.put_DisconnectedText
- IMsRdpClient7.DisconnectedText
- IMsRdpClient7.get_DisconnectedText
- IMsRdpClient7.put_DisconnectedText
- IMsRdpClient8.DisconnectedText
- IMsRdpClient8.get_DisconnectedText
- IMsRdpClient8.put_DisconnectedText
- IMsRdpClient9.DisconnectedText
- IMsRdpClient9.get_DisconnectedText
- IMsRdpClient9.put_DisconnectedText
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4768e639cbfb1543e06c03f2d9e6566d0adb147e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802746"
---
# <a name="imstscaxdisconnectedtext-property"></a><span data-ttu-id="6010e-124">Имстскакс: свойство Исконнектедтекст:D</span><span class="sxs-lookup"><span data-stu-id="6010e-124">IMsTscAx::DisconnectedText property</span></span>

<span data-ttu-id="6010e-125">Задает текст, отображаемый по центру элемента управления до завершения соединения.</span><span class="sxs-lookup"><span data-stu-id="6010e-125">Specifies the text that appears centered in the control before a connection is terminated.</span></span>

<span data-ttu-id="6010e-126">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="6010e-126">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="6010e-127">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6010e-127">Syntax</span></span>


```C++
HRESULT put_DisconnectedText(
  [in]  BSTR newVal
);

HRESULT get_DisconnectedText(
  [out] BSTR *pDisconnectedText
);
```



## <a name="property-value"></a><span data-ttu-id="6010e-128">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="6010e-128">Property value</span></span>

<span data-ttu-id="6010e-129">Новый отображаемый текст.</span><span class="sxs-lookup"><span data-stu-id="6010e-129">The new display text.</span></span>

## <a name="error-codes"></a><span data-ttu-id="6010e-130">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="6010e-130">Error codes</span></span>

<span data-ttu-id="6010e-131">В случае успеха возвратите значение **\_ ОК** .</span><span class="sxs-lookup"><span data-stu-id="6010e-131">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="6010e-132">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6010e-132">Remarks</span></span>

<span data-ttu-id="6010e-133">Установка свойства **дисконнектедтекст** является необязательной.</span><span class="sxs-lookup"><span data-stu-id="6010e-133">Setting the **DisconnectedText** property is optional.</span></span> <span data-ttu-id="6010e-134">Если он не указан, элемент управления будет пустым до установления соединения.</span><span class="sxs-lookup"><span data-stu-id="6010e-134">If it is not specified the control appears blank before a connection is established.</span></span>

<span data-ttu-id="6010e-135">Это свойство может быть задано только в том случае, если элемент управления не находится в состоянии Connected.</span><span class="sxs-lookup"><span data-stu-id="6010e-135">This property can be set only if the control is not in the connected state.</span></span> <span data-ttu-id="6010e-136">Метод возвращает **E \_ Fail** , если он вызывается после подключения элемента управления.</span><span class="sxs-lookup"><span data-stu-id="6010e-136">The method returns **E\_FAIL** if it is called after the control is connected.</span></span> <span data-ttu-id="6010e-137">Проверить, подключен ли элемент управления, можно, отреагировать на события соединения в [**имстскаксевентс**](imstscaxevents-interface.md) или изучив свойство [**Connected**](imstscax-connected.md) .</span><span class="sxs-lookup"><span data-stu-id="6010e-137">You can check if the control is connected by responding to connection events in [**IMsTscAxEvents**](imstscaxevents-interface.md) or examining the [**Connected**](imstscax-connected.md) property.</span></span>

<span data-ttu-id="6010e-138">Этот метод выделяет память, необходимую для буфера, на который указывает параметр *пдисконнектедтекст* .</span><span class="sxs-lookup"><span data-stu-id="6010e-138">This method allocates the memory required for the buffer pointed to by the *pDisconnectedText* parameter.</span></span> <span data-ttu-id="6010e-139">Вызов приложений C/C++ должен освободить память с помощью вызова функции [**сисфристринг**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) .</span><span class="sxs-lookup"><span data-stu-id="6010e-139">Calling C/C++ applications must free the memory with a call to the [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) function.</span></span> <span data-ttu-id="6010e-140">Это не является обязательным для Visual Basic и скриптов клиентов.</span><span class="sxs-lookup"><span data-stu-id="6010e-140">This is not required for Visual Basic and scripting clients.</span></span>

<span data-ttu-id="6010e-141">Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="6010e-141">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6010e-142">Требования</span><span class="sxs-lookup"><span data-stu-id="6010e-142">Requirements</span></span>



| <span data-ttu-id="6010e-143">Требование</span><span class="sxs-lookup"><span data-stu-id="6010e-143">Requirement</span></span> | <span data-ttu-id="6010e-144">Значение</span><span class="sxs-lookup"><span data-stu-id="6010e-144">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6010e-145">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6010e-145">Minimum supported client</span></span><br/> | <span data-ttu-id="6010e-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6010e-146">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="6010e-147">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6010e-147">Minimum supported server</span></span><br/> | <span data-ttu-id="6010e-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6010e-148">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="6010e-149">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="6010e-149">Type library</span></span><br/>             | <dl> <span data-ttu-id="6010e-150"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6010e-150"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="6010e-151">DLL</span><span class="sxs-lookup"><span data-stu-id="6010e-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6010e-152"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6010e-152"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="6010e-153">IID</span><span class="sxs-lookup"><span data-stu-id="6010e-153">IID</span></span><br/>                      | <span data-ttu-id="6010e-154">IID \_ имстскакс определен как 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="6010e-154">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="6010e-155">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6010e-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6010e-156">**имсрдпклиент**</span><span class="sxs-lookup"><span data-stu-id="6010e-156">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="6010e-157">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="6010e-157">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="6010e-158">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="6010e-158">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="6010e-159">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="6010e-159">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="6010e-160">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="6010e-160">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="6010e-161">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="6010e-161">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="6010e-162">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="6010e-162">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="6010e-163">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="6010e-163">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="6010e-164">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="6010e-164">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="6010e-165">**имстскакс**</span><span class="sxs-lookup"><span data-stu-id="6010e-165">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> </dl>

 

