---
title: Имстскакс Вертикалскроллбарвисибле, свойство
description: Указывает, отображает ли элемент управления вертикальную полосу прокрутки.
ms.assetid: b31e2db3-b367-4900-a2c6-51fd794341c2
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Вертикалскроллбарвисибле
- Службы удаленных рабочих столов свойства Вертикалскроллбарвисибле, интерфейс Имстскакс
- Службы удаленных рабочих столов интерфейса Имстскакс, свойство Вертикалскроллбарвисибле
- Службы удаленных рабочих столов свойства Вертикалскроллбарвисибле, интерфейс Имсрдпклиент
- Службы удаленных рабочих столов интерфейса Имсрдпклиент, свойство Вертикалскроллбарвисибле
- Службы удаленных рабочих столов свойства Вертикалскроллбарвисибле, интерфейс IMsRdpClient2
- Службы удаленных рабочих столов интерфейса IMsRdpClient2, свойство Вертикалскроллбарвисибле
- Службы удаленных рабочих столов свойства Вертикалскроллбарвисибле, интерфейс IMsRdpClient3
- Службы удаленных рабочих столов интерфейса IMsRdpClient3, свойство Вертикалскроллбарвисибле
- Службы удаленных рабочих столов свойства Вертикалскроллбарвисибле, интерфейс IMsRdpClient4
- Службы удаленных рабочих столов интерфейса IMsRdpClient4, свойство Вертикалскроллбарвисибле
- Службы удаленных рабочих столов свойства Вертикалскроллбарвисибле, интерфейс IMsRdpClient5
- Службы удаленных рабочих столов интерфейса IMsRdpClient5, свойство Вертикалскроллбарвисибле
- Службы удаленных рабочих столов свойства Вертикалскроллбарвисибле, интерфейс IMsRdpClient6
- Службы удаленных рабочих столов интерфейса IMsRdpClient6, свойство Вертикалскроллбарвисибле
- Службы удаленных рабочих столов свойства Вертикалскроллбарвисибле, интерфейс IMsRdpClient7
- Службы удаленных рабочих столов интерфейса IMsRdpClient7, свойство Вертикалскроллбарвисибле
- Службы удаленных рабочих столов свойства Вертикалскроллбарвисибле, интерфейс IMsRdpClient8
- Службы удаленных рабочих столов интерфейса IMsRdpClient8, свойство Вертикалскроллбарвисибле
- Службы удаленных рабочих столов свойства Вертикалскроллбарвисибле, интерфейс IMsRdpClient9
- Службы удаленных рабочих столов интерфейса IMsRdpClient9, свойство Вертикалскроллбарвисибле
topic_type:
- apiref
api_name:
- IMsTscAx.VerticalScrollBarVisible
- IMsTscAx.get_VerticalScrollBarVisible
- IMsRdpClient.VerticalScrollBarVisible
- IMsRdpClient.get_VerticalScrollBarVisible
- IMsRdpClient2.VerticalScrollBarVisible
- IMsRdpClient2.get_VerticalScrollBarVisible
- IMsRdpClient3.VerticalScrollBarVisible
- IMsRdpClient3.get_VerticalScrollBarVisible
- IMsRdpClient4.VerticalScrollBarVisible
- IMsRdpClient4.get_VerticalScrollBarVisible
- IMsRdpClient5.VerticalScrollBarVisible
- IMsRdpClient5.get_VerticalScrollBarVisible
- IMsRdpClient6.VerticalScrollBarVisible
- IMsRdpClient6.get_VerticalScrollBarVisible
- IMsRdpClient7.VerticalScrollBarVisible
- IMsRdpClient7.get_VerticalScrollBarVisible
- IMsRdpClient8.VerticalScrollBarVisible
- IMsRdpClient8.get_VerticalScrollBarVisible
- IMsRdpClient9.VerticalScrollBarVisible
- IMsRdpClient9.get_VerticalScrollBarVisible
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1365a0ab6d4a1411d78496cf157f3bc49fe5db15
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489669"
---
# <a name="imstscaxverticalscrollbarvisible-property"></a><span data-ttu-id="ef589-124">Свойство Имстскакс:: Вертикалскроллбарвисибле</span><span class="sxs-lookup"><span data-stu-id="ef589-124">IMsTscAx::VerticalScrollBarVisible property</span></span>

<span data-ttu-id="ef589-125">Указывает, отображает ли элемент управления вертикальную полосу прокрутки.</span><span class="sxs-lookup"><span data-stu-id="ef589-125">Indicates whether the control displays a vertical scroll bar.</span></span>

<span data-ttu-id="ef589-126">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="ef589-126">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef589-127">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ef589-127">Syntax</span></span>


```C++
HRESULT get_VerticalScrollBarVisible(
  [out] BOOL *pfVScrollVisible
);
```



## <a name="property-value"></a><span data-ttu-id="ef589-128">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="ef589-128">Property value</span></span>

<span data-ttu-id="ef589-129">Значение этого параметра равно **true** , если вертикальная полоса прокрутки видима, и **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="ef589-129">The value of this parameter is **TRUE** if the vertical scroll bar is visible, and **FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ef589-130">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="ef589-130">Error codes</span></span>

<span data-ttu-id="ef589-131">В случае успеха возвратите значение **\_ ОК** .</span><span class="sxs-lookup"><span data-stu-id="ef589-131">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="ef589-132">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ef589-132">Remarks</span></span>

<span data-ttu-id="ef589-133">Элемент управления автоматически отображает вертикальную полосу прокрутки, если высота текущего элемента управления меньше, чем высота рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="ef589-133">The control automatically displays a vertical scroll bar if the height of the current control is less than the height of the desktop.</span></span>

<span data-ttu-id="ef589-134">Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="ef589-134">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ef589-135">Требования</span><span class="sxs-lookup"><span data-stu-id="ef589-135">Requirements</span></span>



| <span data-ttu-id="ef589-136">Требование</span><span class="sxs-lookup"><span data-stu-id="ef589-136">Requirement</span></span> | <span data-ttu-id="ef589-137">Значение</span><span class="sxs-lookup"><span data-stu-id="ef589-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ef589-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ef589-138">Minimum supported client</span></span><br/> | <span data-ttu-id="ef589-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ef589-139">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="ef589-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ef589-140">Minimum supported server</span></span><br/> | <span data-ttu-id="ef589-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ef589-141">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="ef589-142">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="ef589-142">Type library</span></span><br/>             | <dl> <span data-ttu-id="ef589-143"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ef589-143"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="ef589-144">DLL</span><span class="sxs-lookup"><span data-stu-id="ef589-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ef589-145"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ef589-145"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="ef589-146">IID</span><span class="sxs-lookup"><span data-stu-id="ef589-146">IID</span></span><br/>                      | <span data-ttu-id="ef589-147">IID \_ имстскакс определен как 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="ef589-147">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="ef589-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ef589-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef589-149">**имсрдпклиент**</span><span class="sxs-lookup"><span data-stu-id="ef589-149">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="ef589-150">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="ef589-150">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="ef589-151">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="ef589-151">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="ef589-152">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="ef589-152">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="ef589-153">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="ef589-153">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="ef589-154">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="ef589-154">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="ef589-155">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="ef589-155">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="ef589-156">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="ef589-156">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="ef589-157">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="ef589-157">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="ef589-158">**хоризонталскроллбарвисибле**</span><span class="sxs-lookup"><span data-stu-id="ef589-158">**HorizontalScrollBarVisible**</span></span>](imstscax-horizontalscrollbarvisible.md)
</dt> <dt>

[<span data-ttu-id="ef589-159">**имстскакс**</span><span class="sxs-lookup"><span data-stu-id="ef589-159">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> </dl>

 

 





