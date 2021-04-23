---
title: Имстскакс Фуллскринтитле, свойство
description: Указывает заголовок окна, отображаемый, когда элемент управления находится в полноэкранном режиме.
ms.assetid: 441aea43-2d1c-44b7-a74f-e375e711fb4f
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Фуллскринтитле
- Службы удаленных рабочих столов свойства Фуллскринтитле, интерфейс Имстскакс
- Службы удаленных рабочих столов интерфейса Имстскакс, свойство Фуллскринтитле
- Службы удаленных рабочих столов свойства Фуллскринтитле, интерфейс Имсрдпклиент
- Службы удаленных рабочих столов интерфейса Имсрдпклиент, свойство Фуллскринтитле
- Службы удаленных рабочих столов свойства Фуллскринтитле, интерфейс IMsRdpClient2
- Службы удаленных рабочих столов интерфейса IMsRdpClient2, свойство Фуллскринтитле
- Службы удаленных рабочих столов свойства Фуллскринтитле, интерфейс IMsRdpClient3
- Службы удаленных рабочих столов интерфейса IMsRdpClient3, свойство Фуллскринтитле
- Службы удаленных рабочих столов свойства Фуллскринтитле, интерфейс IMsRdpClient4
- Службы удаленных рабочих столов интерфейса IMsRdpClient4, свойство Фуллскринтитле
- Службы удаленных рабочих столов свойства Фуллскринтитле, интерфейс IMsRdpClient5
- Службы удаленных рабочих столов интерфейса IMsRdpClient5, свойство Фуллскринтитле
- Службы удаленных рабочих столов свойства Фуллскринтитле, интерфейс IMsRdpClient6
- Службы удаленных рабочих столов интерфейса IMsRdpClient6, свойство Фуллскринтитле
- Службы удаленных рабочих столов свойства Фуллскринтитле, интерфейс IMsRdpClient7
- Службы удаленных рабочих столов интерфейса IMsRdpClient7, свойство Фуллскринтитле
- Службы удаленных рабочих столов свойства Фуллскринтитле, интерфейс IMsRdpClient8
- Службы удаленных рабочих столов интерфейса IMsRdpClient8, свойство Фуллскринтитле
- Службы удаленных рабочих столов свойства Фуллскринтитле, интерфейс IMsRdpClient9
- Службы удаленных рабочих столов интерфейса IMsRdpClient9, свойство Фуллскринтитле
topic_type:
- apiref
api_name:
- IMsTscAx.FullScreenTitle
- IMsTscAx.put_FullScreenTitle
- IMsRdpClient.FullScreenTitle
- IMsRdpClient.put_FullScreenTitle
- IMsRdpClient2.FullScreenTitle
- IMsRdpClient2.put_FullScreenTitle
- IMsRdpClient3.FullScreenTitle
- IMsRdpClient3.put_FullScreenTitle
- IMsRdpClient4.FullScreenTitle
- IMsRdpClient4.put_FullScreenTitle
- IMsRdpClient5.FullScreenTitle
- IMsRdpClient5.put_FullScreenTitle
- IMsRdpClient6.FullScreenTitle
- IMsRdpClient6.put_FullScreenTitle
- IMsRdpClient7.FullScreenTitle
- IMsRdpClient7.put_FullScreenTitle
- IMsRdpClient8.FullScreenTitle
- IMsRdpClient8.put_FullScreenTitle
- IMsRdpClient9.FullScreenTitle
- IMsRdpClient9.put_FullScreenTitle
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1384d1582f4f0089df55030c22471438575bd072
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136330"
---
# <a name="imstscaxfullscreentitle-property"></a><span data-ttu-id="da9d6-124">Свойство Имстскакс:: Фуллскринтитле</span><span class="sxs-lookup"><span data-stu-id="da9d6-124">IMsTscAx::FullScreenTitle property</span></span>

<span data-ttu-id="da9d6-125">Указывает заголовок окна, отображаемый, когда элемент управления находится в полноэкранном режиме.</span><span class="sxs-lookup"><span data-stu-id="da9d6-125">Specifies the window title displayed when the control is in full-screen mode.</span></span>

<span data-ttu-id="da9d6-126">Это свойство доступно только на запись.</span><span class="sxs-lookup"><span data-stu-id="da9d6-126">This property is write-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="da9d6-127">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="da9d6-127">Syntax</span></span>


```C++
HRESULT put_FullScreenTitle(
  [in] BSTR fullScreenTitle
);
```



## <a name="property-value"></a><span data-ttu-id="da9d6-128">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="da9d6-128">Property value</span></span>

<span data-ttu-id="da9d6-129">Заголовок окна.</span><span class="sxs-lookup"><span data-stu-id="da9d6-129">The window title.</span></span> <span data-ttu-id="da9d6-130">Максимальная длина этой строки равна максимальному \_ пути-1 символам.</span><span class="sxs-lookup"><span data-stu-id="da9d6-130">The maximum length of this string is MAX\_PATH-1 characters.</span></span>

## <a name="error-codes"></a><span data-ttu-id="da9d6-131">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="da9d6-131">Error codes</span></span>

<span data-ttu-id="da9d6-132">В случае успеха возвратите значение **\_ ОК** .</span><span class="sxs-lookup"><span data-stu-id="da9d6-132">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="da9d6-133">Комментарии</span><span class="sxs-lookup"><span data-stu-id="da9d6-133">Remarks</span></span>

<span data-ttu-id="da9d6-134">Это свойство используется для задания заголовка окна элемента управления при открытии соединения в полноэкранном режиме.</span><span class="sxs-lookup"><span data-stu-id="da9d6-134">This property is used to set the title of the control's window when the connection is opened in full-screen mode.</span></span> <span data-ttu-id="da9d6-135">Не используйте это свойство для полноэкранного режима, который обрабатывает контейнеры.</span><span class="sxs-lookup"><span data-stu-id="da9d6-135">Do not use this property for container-handled full-screen mode.</span></span> <span data-ttu-id="da9d6-136">Когда вызывается метод [**имстскадванцедсеттингс::p UT \_ контаинерхандледфуллскрин**](imstscadvancedsettings-containerhandledfullscreen.md) , в окне контейнера отображается заголовок окна.</span><span class="sxs-lookup"><span data-stu-id="da9d6-136">When the [**IMsTscAdvancedSettings::put\_ContainerHandledFullScreen**](imstscadvancedsettings-containerhandledfullscreen.md) method is called, the container window displays the window title.</span></span>

<span data-ttu-id="da9d6-137">Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="da9d6-137">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="da9d6-138">Требования</span><span class="sxs-lookup"><span data-stu-id="da9d6-138">Requirements</span></span>



| <span data-ttu-id="da9d6-139">Требование</span><span class="sxs-lookup"><span data-stu-id="da9d6-139">Requirement</span></span> | <span data-ttu-id="da9d6-140">Значение</span><span class="sxs-lookup"><span data-stu-id="da9d6-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="da9d6-141">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="da9d6-141">Minimum supported client</span></span><br/> | <span data-ttu-id="da9d6-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="da9d6-142">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="da9d6-143">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="da9d6-143">Minimum supported server</span></span><br/> | <span data-ttu-id="da9d6-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="da9d6-144">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="da9d6-145">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="da9d6-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="da9d6-146"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="da9d6-146"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="da9d6-147">DLL</span><span class="sxs-lookup"><span data-stu-id="da9d6-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="da9d6-148"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="da9d6-148"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="da9d6-149">IID</span><span class="sxs-lookup"><span data-stu-id="da9d6-149">IID</span></span><br/>                      | <span data-ttu-id="da9d6-150">IID \_ имстскакс определен как 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="da9d6-150">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="da9d6-151">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="da9d6-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da9d6-152">**имсрдпклиент**</span><span class="sxs-lookup"><span data-stu-id="da9d6-152">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="da9d6-153">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="da9d6-153">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="da9d6-154">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="da9d6-154">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="da9d6-155">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="da9d6-155">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="da9d6-156">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="da9d6-156">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="da9d6-157">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="da9d6-157">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="da9d6-158">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="da9d6-158">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="da9d6-159">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="da9d6-159">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="da9d6-160">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="da9d6-160">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="da9d6-161">**имстскакс**</span><span class="sxs-lookup"><span data-stu-id="da9d6-161">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> </dl>

 

 





