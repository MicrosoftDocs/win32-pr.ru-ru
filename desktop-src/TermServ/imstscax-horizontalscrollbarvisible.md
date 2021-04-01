---
title: Имстскакс Хоризонталскроллбарвисибле, свойство
description: Указывает, отображает ли элемент управления горизонтальную полосу прокрутки.
ms.assetid: d3c22c5f-321f-476e-bcdb-224eb988a7bb
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Хоризонталскроллбарвисибле
- Службы удаленных рабочих столов свойства Хоризонталскроллбарвисибле, интерфейс Имстскакс
- Службы удаленных рабочих столов интерфейса Имстскакс, свойство Хоризонталскроллбарвисибле
- Службы удаленных рабочих столов свойства Хоризонталскроллбарвисибле, интерфейс Имсрдпклиент
- Службы удаленных рабочих столов интерфейса Имсрдпклиент, свойство Хоризонталскроллбарвисибле
- Службы удаленных рабочих столов свойства Хоризонталскроллбарвисибле, интерфейс IMsRdpClient2
- Службы удаленных рабочих столов интерфейса IMsRdpClient2, свойство Хоризонталскроллбарвисибле
- Службы удаленных рабочих столов свойства Хоризонталскроллбарвисибле, интерфейс IMsRdpClient3
- Службы удаленных рабочих столов интерфейса IMsRdpClient3, свойство Хоризонталскроллбарвисибле
- Службы удаленных рабочих столов свойства Хоризонталскроллбарвисибле, интерфейс IMsRdpClient4
- Службы удаленных рабочих столов интерфейса IMsRdpClient4, свойство Хоризонталскроллбарвисибле
- Службы удаленных рабочих столов свойства Хоризонталскроллбарвисибле, интерфейс IMsRdpClient5
- Службы удаленных рабочих столов интерфейса IMsRdpClient5, свойство Хоризонталскроллбарвисибле
- Службы удаленных рабочих столов свойства Хоризонталскроллбарвисибле, интерфейс IMsRdpClient6
- Службы удаленных рабочих столов интерфейса IMsRdpClient6, свойство Хоризонталскроллбарвисибле
- Службы удаленных рабочих столов свойства Хоризонталскроллбарвисибле, интерфейс IMsRdpClient7
- Службы удаленных рабочих столов интерфейса IMsRdpClient7, свойство Хоризонталскроллбарвисибле
- Службы удаленных рабочих столов свойства Хоризонталскроллбарвисибле, интерфейс IMsRdpClient8
- Службы удаленных рабочих столов интерфейса IMsRdpClient8, свойство Хоризонталскроллбарвисибле
- Службы удаленных рабочих столов свойства Хоризонталскроллбарвисибле, интерфейс IMsRdpClient9
- Службы удаленных рабочих столов интерфейса IMsRdpClient9, свойство Хоризонталскроллбарвисибле
topic_type:
- apiref
api_name:
- IMsTscAx.HorizontalScrollBarVisible
- IMsTscAx.get_HorizontalScrollBarVisible
- IMsRdpClient.HorizontalScrollBarVisible
- IMsRdpClient.get_HorizontalScrollBarVisible
- IMsRdpClient2.HorizontalScrollBarVisible
- IMsRdpClient2.get_HorizontalScrollBarVisible
- IMsRdpClient3.HorizontalScrollBarVisible
- IMsRdpClient3.get_HorizontalScrollBarVisible
- IMsRdpClient4.HorizontalScrollBarVisible
- IMsRdpClient4.get_HorizontalScrollBarVisible
- IMsRdpClient5.HorizontalScrollBarVisible
- IMsRdpClient5.get_HorizontalScrollBarVisible
- IMsRdpClient6.HorizontalScrollBarVisible
- IMsRdpClient6.get_HorizontalScrollBarVisible
- IMsRdpClient7.HorizontalScrollBarVisible
- IMsRdpClient7.get_HorizontalScrollBarVisible
- IMsRdpClient8.HorizontalScrollBarVisible
- IMsRdpClient8.get_HorizontalScrollBarVisible
- IMsRdpClient9.HorizontalScrollBarVisible
- IMsRdpClient9.get_HorizontalScrollBarVisible
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08fa2abb97a28af013e5791bcbd643f3f479d5c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071550"
---
# <a name="imstscaxhorizontalscrollbarvisible-property"></a><span data-ttu-id="ff1bf-124">Свойство Имстскакс:: Хоризонталскроллбарвисибле</span><span class="sxs-lookup"><span data-stu-id="ff1bf-124">IMsTscAx::HorizontalScrollBarVisible property</span></span>

<span data-ttu-id="ff1bf-125">Указывает, отображает ли элемент управления горизонтальную полосу прокрутки.</span><span class="sxs-lookup"><span data-stu-id="ff1bf-125">Indicates whether the control has displayed a horizontal scroll bar.</span></span>

<span data-ttu-id="ff1bf-126">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="ff1bf-126">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff1bf-127">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ff1bf-127">Syntax</span></span>


```C++
HRESULT get_HorizontalScrollBarVisible(
  [out] BOOL *pfHScrollVisible
);
```



## <a name="property-value"></a><span data-ttu-id="ff1bf-128">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="ff1bf-128">Property value</span></span>

<span data-ttu-id="ff1bf-129">Значение этого параметра равно **true** , если горизонтальная полоса прокрутки видима, и **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="ff1bf-129">The value of this parameter is **TRUE** if the horizontal scroll bar is visible, and **FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ff1bf-130">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="ff1bf-130">Error codes</span></span>

<span data-ttu-id="ff1bf-131">В случае успеха возвратите значение **\_ ОК** .</span><span class="sxs-lookup"><span data-stu-id="ff1bf-131">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="ff1bf-132">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ff1bf-132">Remarks</span></span>

<span data-ttu-id="ff1bf-133">Элемент управления автоматически отображает горизонтальную полосу прокрутки, если ширина элемента управления меньше ширины рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="ff1bf-133">The control automatically displays a horizontal scroll bar if the width of the control is less than the desktop width.</span></span>

<span data-ttu-id="ff1bf-134">Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="ff1bf-134">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ff1bf-135">Требования</span><span class="sxs-lookup"><span data-stu-id="ff1bf-135">Requirements</span></span>



| <span data-ttu-id="ff1bf-136">Требование</span><span class="sxs-lookup"><span data-stu-id="ff1bf-136">Requirement</span></span> | <span data-ttu-id="ff1bf-137">Значение</span><span class="sxs-lookup"><span data-stu-id="ff1bf-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ff1bf-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ff1bf-138">Minimum supported client</span></span><br/> | <span data-ttu-id="ff1bf-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ff1bf-139">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="ff1bf-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ff1bf-140">Minimum supported server</span></span><br/> | <span data-ttu-id="ff1bf-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ff1bf-141">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="ff1bf-142">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="ff1bf-142">Type library</span></span><br/>             | <dl> <span data-ttu-id="ff1bf-143"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ff1bf-143"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="ff1bf-144">DLL</span><span class="sxs-lookup"><span data-stu-id="ff1bf-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ff1bf-145"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ff1bf-145"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="ff1bf-146">IID</span><span class="sxs-lookup"><span data-stu-id="ff1bf-146">IID</span></span><br/>                      | <span data-ttu-id="ff1bf-147">IID \_ имстскакс определен как 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="ff1bf-147">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="ff1bf-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ff1bf-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff1bf-149">**имсрдпклиент**</span><span class="sxs-lookup"><span data-stu-id="ff1bf-149">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="ff1bf-150">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="ff1bf-150">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="ff1bf-151">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="ff1bf-151">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="ff1bf-152">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="ff1bf-152">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="ff1bf-153">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="ff1bf-153">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="ff1bf-154">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="ff1bf-154">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="ff1bf-155">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="ff1bf-155">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="ff1bf-156">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="ff1bf-156">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="ff1bf-157">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="ff1bf-157">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="ff1bf-158">**имстскакс**</span><span class="sxs-lookup"><span data-stu-id="ff1bf-158">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> <dt>

[<span data-ttu-id="ff1bf-159">**вертикалскроллбарвисибле**</span><span class="sxs-lookup"><span data-stu-id="ff1bf-159">**VerticalScrollBarVisible**</span></span>](imstscax-verticalscrollbarvisible.md)
</dt> </dl>

 

 





