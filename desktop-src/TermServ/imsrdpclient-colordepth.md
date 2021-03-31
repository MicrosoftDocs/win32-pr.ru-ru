---
title: Имсрдпклиент Clientareawidth, свойство
description: Глубина цвета (в битах на пиксель) для соединения элемента управления.
ms.assetid: 9ba4d8fe-20cd-40e9-a71a-0dce0ddd29fc
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Clientareawidth
- Службы удаленных рабочих столов свойства Clientareawidth, интерфейс Имсрдпклиент
- Службы удаленных рабочих столов интерфейса Имсрдпклиент, свойство Clientareawidth
- Службы удаленных рабочих столов свойства Clientareawidth, интерфейс IMsRdpClient2
- Службы удаленных рабочих столов интерфейса IMsRdpClient2, свойство Clientareawidth
- Службы удаленных рабочих столов свойства Clientareawidth, интерфейс IMsRdpClient3
- Службы удаленных рабочих столов интерфейса IMsRdpClient3, свойство Clientareawidth
- Службы удаленных рабочих столов свойства Clientareawidth, интерфейс IMsRdpClient4
- Службы удаленных рабочих столов интерфейса IMsRdpClient4, свойство Clientareawidth
- Службы удаленных рабочих столов свойства Clientareawidth, интерфейс IMsRdpClient5
- Службы удаленных рабочих столов интерфейса IMsRdpClient5, свойство Clientareawidth
- Службы удаленных рабочих столов свойства Clientareawidth, интерфейс IMsRdpClient6
- Службы удаленных рабочих столов интерфейса IMsRdpClient6, свойство Clientareawidth
- Службы удаленных рабочих столов свойства Clientareawidth, интерфейс IMsRdpClient7
- Службы удаленных рабочих столов интерфейса IMsRdpClient7, свойство Clientareawidth
- Службы удаленных рабочих столов свойства Clientareawidth, интерфейс IMsRdpClient8
- Службы удаленных рабочих столов интерфейса IMsRdpClient8, свойство Clientareawidth
- Службы удаленных рабочих столов свойства Clientareawidth, интерфейс IMsRdpClient9
- Службы удаленных рабочих столов интерфейса IMsRdpClient9, свойство Clientareawidth
- Службы удаленных рабочих столов свойства Clientareawidth, интерфейс IMsRdpClient10
- Службы удаленных рабочих столов интерфейса IMsRdpClient10, свойство Clientareawidth
topic_type:
- apiref
api_name:
- IMsRdpClient.ColorDepth
- IMsRdpClient.get_ColorDepth
- IMsRdpClient.put_ColorDepth
- IMsRdpClient2.ColorDepth
- IMsRdpClient2.get_ColorDepth
- IMsRdpClient2.put_ColorDepth
- IMsRdpClient3.ColorDepth
- IMsRdpClient3.get_ColorDepth
- IMsRdpClient3.put_ColorDepth
- IMsRdpClient4.ColorDepth
- IMsRdpClient4.get_ColorDepth
- IMsRdpClient4.put_ColorDepth
- IMsRdpClient5.ColorDepth
- IMsRdpClient5.get_ColorDepth
- IMsRdpClient5.put_ColorDepth
- IMsRdpClient6.ColorDepth
- IMsRdpClient6.get_ColorDepth
- IMsRdpClient6.put_ColorDepth
- IMsRdpClient7.ColorDepth
- IMsRdpClient7.get_ColorDepth
- IMsRdpClient7.put_ColorDepth
- IMsRdpClient8.ColorDepth
- IMsRdpClient8.get_ColorDepth
- IMsRdpClient8.put_ColorDepth
- IMsRdpClient9.ColorDepth
- IMsRdpClient9.get_ColorDepth
- IMsRdpClient9.put_ColorDepth
- IMsRdpClient10.ColorDepth
- IMsRdpClient10.get_ColorDepth
- IMsRdpClient10.put_ColorDepth
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5099deff3913d23173a466245cbf08fd5b95a6a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137363"
---
# <a name="imsrdpclientcolordepth-property"></a><span data-ttu-id="e29fc-124">Свойство Имсрдпклиент:: Clientareawidth</span><span class="sxs-lookup"><span data-stu-id="e29fc-124">IMsRdpClient::ColorDepth property</span></span>

<span data-ttu-id="e29fc-125">Глубина цвета (в битах на пиксель) для соединения элемента управления.</span><span class="sxs-lookup"><span data-stu-id="e29fc-125">The color depth (in bits per pixel) for the control's connection.</span></span>

<span data-ttu-id="e29fc-126">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="e29fc-126">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="e29fc-127">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e29fc-127">Syntax</span></span>


```C++
HRESULT put_ColorDepth(
  [in]  LONG colorDepth
);

HRESULT get_ColorDepth(
  [out] LONG pcolorDepth
);
```



## <a name="property-value"></a><span data-ttu-id="e29fc-128">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="e29fc-128">Property value</span></span>

<span data-ttu-id="e29fc-129">Глубина цвета.</span><span class="sxs-lookup"><span data-stu-id="e29fc-129">The color depth.</span></span> <span data-ttu-id="e29fc-130">Значения включают 8, 15, 16, 24 и 32 бит на пиксель.</span><span class="sxs-lookup"><span data-stu-id="e29fc-130">Values include 8, 15, 16, 24, and 32 bits per pixel.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e29fc-131">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="e29fc-131">Error codes</span></span>

<span data-ttu-id="e29fc-132">Если методы выполнены успешно, возвращается значение **S \_ OK** .</span><span class="sxs-lookup"><span data-stu-id="e29fc-132">If the methods succeed, **S\_OK** is returned.</span></span> <span data-ttu-id="e29fc-133">Любое другое значение **HRESULT** указывает на сбой вызова.</span><span class="sxs-lookup"><span data-stu-id="e29fc-133">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="e29fc-134">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e29fc-134">Remarks</span></span>

<span data-ttu-id="e29fc-135">Это свойство не может быть задано, если элемент управления подключен.</span><span class="sxs-lookup"><span data-stu-id="e29fc-135">This property cannot be set when the control is connected.</span></span>

<span data-ttu-id="e29fc-136">Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="e29fc-136">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e29fc-137">Требования</span><span class="sxs-lookup"><span data-stu-id="e29fc-137">Requirements</span></span>



| <span data-ttu-id="e29fc-138">Требование</span><span class="sxs-lookup"><span data-stu-id="e29fc-138">Requirement</span></span> | <span data-ttu-id="e29fc-139">Значение</span><span class="sxs-lookup"><span data-stu-id="e29fc-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e29fc-140">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e29fc-140">Minimum supported client</span></span><br/> | <span data-ttu-id="e29fc-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e29fc-141">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="e29fc-142">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e29fc-142">Minimum supported server</span></span><br/> | <span data-ttu-id="e29fc-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e29fc-143">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="e29fc-144">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="e29fc-144">Type library</span></span><br/>             | <dl> <span data-ttu-id="e29fc-145"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e29fc-145"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="e29fc-146">DLL</span><span class="sxs-lookup"><span data-stu-id="e29fc-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e29fc-147"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e29fc-147"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="e29fc-148">IID</span><span class="sxs-lookup"><span data-stu-id="e29fc-148">IID</span></span><br/>                      | <span data-ttu-id="e29fc-149">IID \_ имсрдпклиент определен как 92b4a539-7115-4b7c-a5a9-e5d9efc2780a</span><span class="sxs-lookup"><span data-stu-id="e29fc-149">IID\_IMsRdpClient is defined as 92b4a539-7115-4b7c-a5a9-e5d9efc2780a</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="e29fc-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e29fc-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e29fc-151">**имсрдпклиент**</span><span class="sxs-lookup"><span data-stu-id="e29fc-151">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="e29fc-152">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="e29fc-152">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="e29fc-153">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="e29fc-153">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="e29fc-154">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="e29fc-154">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="e29fc-155">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="e29fc-155">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="e29fc-156">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="e29fc-156">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="e29fc-157">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="e29fc-157">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="e29fc-158">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="e29fc-158">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="e29fc-159">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="e29fc-159">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="e29fc-160">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="e29fc-160">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





