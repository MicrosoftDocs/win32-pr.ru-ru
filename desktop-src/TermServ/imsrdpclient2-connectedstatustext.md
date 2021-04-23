---
title: IMsRdpClient2 Коннектедстатустекст, свойство
description: Содержит текст, отображаемый в клиентской области элемента управления, когда элемент управления находится в подключенном состоянии.
ms.assetid: c3d8433b-2fb0-413d-88a3-667149f858ba
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Коннектедстатустекст
- Службы удаленных рабочих столов свойства Коннектедстатустекст, интерфейс IMsRdpClient2
- Службы удаленных рабочих столов интерфейса IMsRdpClient2, свойство Коннектедстатустекст
- Службы удаленных рабочих столов свойства Коннектедстатустекст, интерфейс IMsRdpClient3
- Службы удаленных рабочих столов интерфейса IMsRdpClient3, свойство Коннектедстатустекст
- Службы удаленных рабочих столов свойства Коннектедстатустекст, интерфейс IMsRdpClient4
- Службы удаленных рабочих столов интерфейса IMsRdpClient4, свойство Коннектедстатустекст
- Службы удаленных рабочих столов свойства Коннектедстатустекст, интерфейс IMsRdpClient5
- Службы удаленных рабочих столов интерфейса IMsRdpClient5, свойство Коннектедстатустекст
- Службы удаленных рабочих столов свойства Коннектедстатустекст, интерфейс IMsRdpClient6
- Службы удаленных рабочих столов интерфейса IMsRdpClient6, свойство Коннектедстатустекст
- Службы удаленных рабочих столов свойства Коннектедстатустекст, интерфейс IMsRdpClient7
- Службы удаленных рабочих столов интерфейса IMsRdpClient7, свойство Коннектедстатустекст
- Службы удаленных рабочих столов свойства Коннектедстатустекст, интерфейс IMsRdpClient8
- Службы удаленных рабочих столов интерфейса IMsRdpClient8, свойство Коннектедстатустекст
- Службы удаленных рабочих столов свойства Коннектедстатустекст, интерфейс IMsRdpClient9
- Службы удаленных рабочих столов интерфейса IMsRdpClient9, свойство Коннектедстатустекст
- Службы удаленных рабочих столов свойства Коннектедстатустекст, интерфейс IMsRdpClient10
- Службы удаленных рабочих столов интерфейса IMsRdpClient10, свойство Коннектедстатустекст
topic_type:
- apiref
api_name:
- IMsRdpClient2.ConnectedStatusText
- IMsRdpClient2.get_ConnectedStatusText
- IMsRdpClient2.put_ConnectedStatusText
- IMsRdpClient3.ConnectedStatusText
- IMsRdpClient3.get_ConnectedStatusText
- IMsRdpClient3.put_ConnectedStatusText
- IMsRdpClient4.ConnectedStatusText
- IMsRdpClient4.get_ConnectedStatusText
- IMsRdpClient4.put_ConnectedStatusText
- IMsRdpClient5.ConnectedStatusText
- IMsRdpClient5.get_ConnectedStatusText
- IMsRdpClient5.put_ConnectedStatusText
- IMsRdpClient6.ConnectedStatusText
- IMsRdpClient6.get_ConnectedStatusText
- IMsRdpClient6.put_ConnectedStatusText
- IMsRdpClient7.ConnectedStatusText
- IMsRdpClient7.get_ConnectedStatusText
- IMsRdpClient7.put_ConnectedStatusText
- IMsRdpClient8.ConnectedStatusText
- IMsRdpClient8.get_ConnectedStatusText
- IMsRdpClient8.put_ConnectedStatusText
- IMsRdpClient9.ConnectedStatusText
- IMsRdpClient9.get_ConnectedStatusText
- IMsRdpClient9.put_ConnectedStatusText
- IMsRdpClient10.ConnectedStatusText
- IMsRdpClient10.get_ConnectedStatusText
- IMsRdpClient10.put_ConnectedStatusText
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fd6ee2ac155aa3fc4873ee1a5eb890774b50978
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681809"
---
# <a name="imsrdpclient2connectedstatustext-property"></a><span data-ttu-id="01b34-122">Свойство IMsRdpClient2:: Коннектедстатустекст</span><span class="sxs-lookup"><span data-stu-id="01b34-122">IMsRdpClient2::ConnectedStatusText property</span></span>

<span data-ttu-id="01b34-123">Содержит текст, отображаемый в клиентской области элемента управления, когда элемент управления находится в подключенном состоянии.</span><span class="sxs-lookup"><span data-stu-id="01b34-123">Contains the text that is displayed in the client area of the control while the control is in the connected state.</span></span>

<span data-ttu-id="01b34-124">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="01b34-124">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="01b34-125">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="01b34-125">Syntax</span></span>


```C++
HRESULT put_ConnectedStatusText(
  [in]  BSTR newVal
);

HRESULT get_ConnectedStatusText(
  [out] BSTR *pConnectedStatusText
);
```



## <a name="property-value"></a><span data-ttu-id="01b34-126">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="01b34-126">Property value</span></span>

<span data-ttu-id="01b34-127">Свойство **коннектедстатустекст** содержит текст, отображаемый в клиентской области элемента управления, когда элемент управления находится в состоянии Connected.</span><span class="sxs-lookup"><span data-stu-id="01b34-127">The **ConnectedStatusText** property contains the text that is displayed in the client area of the control while the control is in the connected state.</span></span>

## <a name="error-codes"></a><span data-ttu-id="01b34-128">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="01b34-128">Error codes</span></span>

<span data-ttu-id="01b34-129">В случае успеха возвратите значение **\_ ОК** .</span><span class="sxs-lookup"><span data-stu-id="01b34-129">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="01b34-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="01b34-130">Remarks</span></span>

<span data-ttu-id="01b34-131">Текст, отображаемый в клиентской области элемента управления, когда элемент управления находится в состоянии Connected.</span><span class="sxs-lookup"><span data-stu-id="01b34-131">Text to display in the client area of the control while the control is in the connected state.</span></span> <span data-ttu-id="01b34-132">Это текст, видимый, например, когда пользователь переключает элемент управления в полноэкранный режим в веб-браузере, сценарий, который оставляет часть элемента управления, размещенного в браузере.</span><span class="sxs-lookup"><span data-stu-id="01b34-132">This is the text that is visible, for example, when the user switches the control to the full-screen mode in a web browser, a scenario that leaves a portion of the control hosted in the browser.</span></span>

<span data-ttu-id="01b34-133">Метод **Get \_ коннектедстатустекст** выделяет память, необходимую для буфера, на который указывает параметр *пконнектедстатустекст* .</span><span class="sxs-lookup"><span data-stu-id="01b34-133">The **get\_ConnectedStatusText** method allocates the memory required for the buffer pointed to by the *pConnectedStatusText* parameter.</span></span> <span data-ttu-id="01b34-134">Вызов приложений C/C++ должен освободить память с помощью вызова функции [**сисфристринг**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) .</span><span class="sxs-lookup"><span data-stu-id="01b34-134">Calling C/C++ applications must free the memory with a call to the [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) function.</span></span> <span data-ttu-id="01b34-135">Это не является обязательным для Visual Basic и скриптов клиентов.</span><span class="sxs-lookup"><span data-stu-id="01b34-135">This is not required for Visual Basic and scripting clients.</span></span>

<span data-ttu-id="01b34-136">Это свойство не может быть задано, если элемент управления подключен.</span><span class="sxs-lookup"><span data-stu-id="01b34-136">This property cannot be set when the control is connected.</span></span> <span data-ttu-id="01b34-137">Проверить, подключен ли элемент управления, можно с помощью метода [**имстскакс:: Get \_ Connected**](imstscax-connected.md) .</span><span class="sxs-lookup"><span data-stu-id="01b34-137">You can check if the control is connected by calling the [**IMsTscAx::get\_Connected**](imstscax-connected.md) method.</span></span>

<span data-ttu-id="01b34-138">Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="01b34-138">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="01b34-139">Требования</span><span class="sxs-lookup"><span data-stu-id="01b34-139">Requirements</span></span>



| <span data-ttu-id="01b34-140">Требование</span><span class="sxs-lookup"><span data-stu-id="01b34-140">Requirement</span></span> | <span data-ttu-id="01b34-141">Значение</span><span class="sxs-lookup"><span data-stu-id="01b34-141">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="01b34-142">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="01b34-142">Minimum supported client</span></span><br/> | <span data-ttu-id="01b34-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="01b34-143">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="01b34-144">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="01b34-144">Minimum supported server</span></span><br/> | <span data-ttu-id="01b34-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="01b34-145">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="01b34-146">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="01b34-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="01b34-147"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="01b34-147"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="01b34-148">DLL</span><span class="sxs-lookup"><span data-stu-id="01b34-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="01b34-149"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="01b34-149"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="01b34-150">IID</span><span class="sxs-lookup"><span data-stu-id="01b34-150">IID</span></span><br/>                      | <span data-ttu-id="01b34-151">IID \_ IMsRdpClient2 определен как e7e17dc4-3b71-4ba7-a8e6-281ffadca28f</span><span class="sxs-lookup"><span data-stu-id="01b34-151">IID\_IMsRdpClient2 is defined as e7e17dc4-3b71-4ba7-a8e6-281ffadca28f</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="01b34-152">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="01b34-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01b34-153">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="01b34-153">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="01b34-154">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="01b34-154">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="01b34-155">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="01b34-155">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="01b34-156">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="01b34-156">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="01b34-157">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="01b34-157">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="01b34-158">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="01b34-158">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="01b34-159">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="01b34-159">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="01b34-160">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="01b34-160">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="01b34-161">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="01b34-161">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

