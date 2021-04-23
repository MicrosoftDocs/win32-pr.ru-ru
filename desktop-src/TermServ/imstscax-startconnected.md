---
title: Имстскакс Стартконнектед, свойство
description: Указывает, будет ли элемент управления устанавливать подключение к серверу узла сеансов удаленный рабочий стол (узел сеансов удаленных рабочих столов) сразу после запуска.
ms.assetid: cf2956c0-be4f-4f80-a14b-253ae8117824
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Стартконнектед
- Службы удаленных рабочих столов свойства Стартконнектед, интерфейс Имстскакс
- Службы удаленных рабочих столов интерфейса Имстскакс, свойство Стартконнектед
- Службы удаленных рабочих столов свойства Стартконнектед, интерфейс Имсрдпклиент
- Службы удаленных рабочих столов интерфейса Имсрдпклиент, свойство Стартконнектед
- Службы удаленных рабочих столов свойства Стартконнектед, интерфейс IMsRdpClient2
- Службы удаленных рабочих столов интерфейса IMsRdpClient2, свойство Стартконнектед
- Службы удаленных рабочих столов свойства Стартконнектед, интерфейс IMsRdpClient3
- Службы удаленных рабочих столов интерфейса IMsRdpClient3, свойство Стартконнектед
- Службы удаленных рабочих столов свойства Стартконнектед, интерфейс IMsRdpClient4
- Службы удаленных рабочих столов интерфейса IMsRdpClient4, свойство Стартконнектед
- Службы удаленных рабочих столов свойства Стартконнектед, интерфейс IMsRdpClient5
- Службы удаленных рабочих столов интерфейса IMsRdpClient5, свойство Стартконнектед
- Службы удаленных рабочих столов свойства Стартконнектед, интерфейс IMsRdpClient6
- Службы удаленных рабочих столов интерфейса IMsRdpClient6, свойство Стартконнектед
- Службы удаленных рабочих столов свойства Стартконнектед, интерфейс IMsRdpClient7
- Службы удаленных рабочих столов интерфейса IMsRdpClient7, свойство Стартконнектед
- Службы удаленных рабочих столов свойства Стартконнектед, интерфейс IMsRdpClient8
- Службы удаленных рабочих столов интерфейса IMsRdpClient8, свойство Стартконнектед
- Службы удаленных рабочих столов свойства Стартконнектед, интерфейс IMsRdpClient9
- Службы удаленных рабочих столов интерфейса IMsRdpClient9, свойство Стартконнектед
topic_type:
- apiref
api_name:
- IMsTscAx.StartConnected
- IMsTscAx.get_StartConnected
- IMsTscAx.put_StartConnected
- IMsRdpClient.StartConnected
- IMsRdpClient.get_StartConnected
- IMsRdpClient.put_StartConnected
- IMsRdpClient2.StartConnected
- IMsRdpClient2.get_StartConnected
- IMsRdpClient2.put_StartConnected
- IMsRdpClient3.StartConnected
- IMsRdpClient3.get_StartConnected
- IMsRdpClient3.put_StartConnected
- IMsRdpClient4.StartConnected
- IMsRdpClient4.get_StartConnected
- IMsRdpClient4.put_StartConnected
- IMsRdpClient5.StartConnected
- IMsRdpClient5.get_StartConnected
- IMsRdpClient5.put_StartConnected
- IMsRdpClient6.StartConnected
- IMsRdpClient6.get_StartConnected
- IMsRdpClient6.put_StartConnected
- IMsRdpClient7.StartConnected
- IMsRdpClient7.get_StartConnected
- IMsRdpClient7.put_StartConnected
- IMsRdpClient8.StartConnected
- IMsRdpClient8.get_StartConnected
- IMsRdpClient8.put_StartConnected
- IMsRdpClient9.StartConnected
- IMsRdpClient9.get_StartConnected
- IMsRdpClient9.put_StartConnected
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09bda77a06723a6df63055374a3fc96cb80f7654
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672501"
---
# <a name="imstscaxstartconnected-property"></a><span data-ttu-id="5da33-124">Свойство Имстскакс:: Стартконнектед</span><span class="sxs-lookup"><span data-stu-id="5da33-124">IMsTscAx::StartConnected property</span></span>

<span data-ttu-id="5da33-125">Указывает, будет ли элемент управления устанавливать подключение к серверу узла сеансов удаленный рабочий стол (узел сеансов удаленных рабочих столов) сразу после запуска.</span><span class="sxs-lookup"><span data-stu-id="5da33-125">Indicates whether the control will establish the Remote Desktop Session Host (RD Session Host) server connection immediately upon startup.</span></span>

<span data-ttu-id="5da33-126">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="5da33-126">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="5da33-127">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5da33-127">Syntax</span></span>


```C++
HRESULT put_StartConnected(
  [in]  BOOL fStartConnected
);

HRESULT get_StartConnected(
  [out] BOOL *pfStartConnected
);
```



## <a name="property-value"></a><span data-ttu-id="5da33-128">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="5da33-128">Property value</span></span>

<span data-ttu-id="5da33-129">Задайте для этого параметра **значение true** , если элемент управления должен сразу же подключаться при запуске, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="5da33-129">Set this parameter to **TRUE** if the control should connect immediately on startup, or **FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="5da33-130">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="5da33-130">Error codes</span></span>

<span data-ttu-id="5da33-131">В случае успеха возвратите значение **\_ ОК** .</span><span class="sxs-lookup"><span data-stu-id="5da33-131">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="5da33-132">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5da33-132">Remarks</span></span>

<span data-ttu-id="5da33-133">Это свойство наиболее полезно, если свойства элемента управления заданы в списке параметров <OBJECT> тега, а не через вызовы скриптов.</span><span class="sxs-lookup"><span data-stu-id="5da33-133">This property is most useful when the control properties are set in the parameter list of an <OBJECT> tag, rather than through script calls.</span></span>

<span data-ttu-id="5da33-134">Это свойство может использоваться, только если имя сервера указано также с помощью свойства сервера.</span><span class="sxs-lookup"><span data-stu-id="5da33-134">This property can be used only if the server name is also specified using the server property.</span></span> <span data-ttu-id="5da33-135">Этот параметр должен быть задан перед запуском элемента управления, например путем включения его в список параметров <OBJECT> тега при использовании элемента управления на веб-странице.</span><span class="sxs-lookup"><span data-stu-id="5da33-135">This parameter has to be set before the control starts up for example, by including it in the parameter list of an <OBJECT> tag when using the control from a webpage.</span></span>

<span data-ttu-id="5da33-136">Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="5da33-136">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5da33-137">Требования</span><span class="sxs-lookup"><span data-stu-id="5da33-137">Requirements</span></span>



| <span data-ttu-id="5da33-138">Требование</span><span class="sxs-lookup"><span data-stu-id="5da33-138">Requirement</span></span> | <span data-ttu-id="5da33-139">Значение</span><span class="sxs-lookup"><span data-stu-id="5da33-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5da33-140">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5da33-140">Minimum supported client</span></span><br/> | <span data-ttu-id="5da33-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5da33-141">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="5da33-142">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5da33-142">Minimum supported server</span></span><br/> | <span data-ttu-id="5da33-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5da33-143">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="5da33-144">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="5da33-144">Type library</span></span><br/>             | <dl> <span data-ttu-id="5da33-145"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5da33-145"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="5da33-146">DLL</span><span class="sxs-lookup"><span data-stu-id="5da33-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5da33-147"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5da33-147"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="5da33-148">IID</span><span class="sxs-lookup"><span data-stu-id="5da33-148">IID</span></span><br/>                      | <span data-ttu-id="5da33-149">IID \_ имстскакс определен как 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="5da33-149">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="5da33-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5da33-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5da33-151">**имсрдпклиент**</span><span class="sxs-lookup"><span data-stu-id="5da33-151">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="5da33-152">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="5da33-152">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="5da33-153">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="5da33-153">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="5da33-154">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="5da33-154">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="5da33-155">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="5da33-155">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="5da33-156">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="5da33-156">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="5da33-157">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="5da33-157">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="5da33-158">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="5da33-158">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="5da33-159">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="5da33-159">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="5da33-160">Внедрение удаленный рабочий стол элемента управления ActiveX на веб-страницу</span><span class="sxs-lookup"><span data-stu-id="5da33-160">Embedding the Remote Desktop ActiveX Control in a Webpage</span></span>](embedding-the-remote-desktop-activex-control-in-a-web-page.md)
</dt> <dt>

[<span data-ttu-id="5da33-161">**имстскакс**</span><span class="sxs-lookup"><span data-stu-id="5da33-161">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> </dl>

 

 





