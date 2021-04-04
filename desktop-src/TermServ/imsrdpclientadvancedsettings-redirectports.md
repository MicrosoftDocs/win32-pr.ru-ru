---
title: Имсрдпклиентадванцедсеттингс Редиректпортс, свойство
description: Указывает, разрешено ли перенаправление локальных портов (например, COM и LPT).
ms.assetid: 85e1e40d-8da7-4333-ae96-2bfa44479267
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Редиректпортс
- Службы удаленных рабочих столов свойства Редиректпортс, интерфейс Имсрдпклиентадванцедсеттингс
- Службы удаленных рабочих столов интерфейса Имсрдпклиентадванцедсеттингс, свойство Редиректпортс
- Службы удаленных рабочих столов свойства Редиректпортс, интерфейс IMsRdpClientAdvancedSettings2
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings2, свойство Редиректпортс
- Службы удаленных рабочих столов свойства Редиректпортс, интерфейс IMsRdpClientAdvancedSettings3
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings3, свойство Редиректпортс
- Службы удаленных рабочих столов свойства Редиректпортс, интерфейс IMsRdpClientAdvancedSettings4
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings4, свойство Редиректпортс
- Службы удаленных рабочих столов свойства Редиректпортс, интерфейс IMsRdpClientAdvancedSettings5
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings5, свойство Редиректпортс
- Службы удаленных рабочих столов свойства Редиректпортс, интерфейс IMsRdpClientAdvancedSettings6
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings6, свойство Редиректпортс
- Службы удаленных рабочих столов свойства Редиректпортс, интерфейс IMsRdpClientAdvancedSettings7
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings7, свойство Редиректпортс
- Службы удаленных рабочих столов свойства Редиректпортс, интерфейс IMsRdpClientAdvancedSettings8
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings8, свойство Редиректпортс
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.RedirectPorts
- IMsRdpClientAdvancedSettings.get_RedirectPorts
- IMsRdpClientAdvancedSettings.put_RedirectPorts
- IMsRdpClientAdvancedSettings2.RedirectPorts
- IMsRdpClientAdvancedSettings2.get_RedirectPorts
- IMsRdpClientAdvancedSettings2.put_RedirectPorts
- IMsRdpClientAdvancedSettings3.RedirectPorts
- IMsRdpClientAdvancedSettings3.get_RedirectPorts
- IMsRdpClientAdvancedSettings3.put_RedirectPorts
- IMsRdpClientAdvancedSettings4.RedirectPorts
- IMsRdpClientAdvancedSettings4.get_RedirectPorts
- IMsRdpClientAdvancedSettings4.put_RedirectPorts
- IMsRdpClientAdvancedSettings5.RedirectPorts
- IMsRdpClientAdvancedSettings5.get_RedirectPorts
- IMsRdpClientAdvancedSettings5.put_RedirectPorts
- IMsRdpClientAdvancedSettings6.RedirectPorts
- IMsRdpClientAdvancedSettings6.get_RedirectPorts
- IMsRdpClientAdvancedSettings6.put_RedirectPorts
- IMsRdpClientAdvancedSettings7.RedirectPorts
- IMsRdpClientAdvancedSettings7.get_RedirectPorts
- IMsRdpClientAdvancedSettings7.put_RedirectPorts
- IMsRdpClientAdvancedSettings8.RedirectPorts
- IMsRdpClientAdvancedSettings8.get_RedirectPorts
- IMsRdpClientAdvancedSettings8.put_RedirectPorts
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 714b26081bb4caadface283553b1dd3ebd91192d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988210"
---
# <a name="imsrdpclientadvancedsettingsredirectports-property"></a><span data-ttu-id="d51a2-120">Свойство Имсрдпклиентадванцедсеттингс:: Редиректпортс</span><span class="sxs-lookup"><span data-stu-id="d51a2-120">IMsRdpClientAdvancedSettings::RedirectPorts property</span></span>

<span data-ttu-id="d51a2-121">Указывает, разрешено ли перенаправление локальных портов (например, COM и LPT).</span><span class="sxs-lookup"><span data-stu-id="d51a2-121">Specifies if redirection of local ports (for example, COM and LPT) is allowed.</span></span>

<span data-ttu-id="d51a2-122">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="d51a2-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="d51a2-123">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d51a2-123">Syntax</span></span>


```C++
HRESULT put_RedirectPorts(
  [in]  VARIANT_BOOL redirectPorts
);

HRESULT get_RedirectPorts(
  [out] VARIANT_BOOL *predirectPorts
);
```



## <a name="property-value"></a><span data-ttu-id="d51a2-124">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="d51a2-124">Property value</span></span>

<span data-ttu-id="d51a2-125">Присвойте этому параметру значение **Variant \_ true** , чтобы разрешить перенаправление или **вариант \_ false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="d51a2-125">Set this parameter to **VARIANT\_TRUE** to allow redirection or **VARIANT\_FALSE** otherwise.</span></span> <span data-ttu-id="d51a2-126">**Вариант \_ Значение TRUE** предложит пользователю подтвердить возможность перенаправления во время подключения в целях безопасности.</span><span class="sxs-lookup"><span data-stu-id="d51a2-126">**VARIANT\_TRUE** prompts the user to confirm allowing redirection at connection time, for security purposes.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d51a2-127">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="d51a2-127">Error codes</span></span>

<span data-ttu-id="d51a2-128">При успешном выполнении возвращает значение **\_ ОК** .</span><span class="sxs-lookup"><span data-stu-id="d51a2-128">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="d51a2-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d51a2-129">Remarks</span></span>

<span data-ttu-id="d51a2-130">Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="d51a2-130">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d51a2-131">Требования</span><span class="sxs-lookup"><span data-stu-id="d51a2-131">Requirements</span></span>



| <span data-ttu-id="d51a2-132">Требование</span><span class="sxs-lookup"><span data-stu-id="d51a2-132">Requirement</span></span> | <span data-ttu-id="d51a2-133">Значение</span><span class="sxs-lookup"><span data-stu-id="d51a2-133">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d51a2-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d51a2-134">Minimum supported client</span></span><br/> | <span data-ttu-id="d51a2-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d51a2-135">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="d51a2-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d51a2-136">Minimum supported server</span></span><br/> | <span data-ttu-id="d51a2-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d51a2-137">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="d51a2-138">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="d51a2-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="d51a2-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d51a2-139"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="d51a2-140">DLL</span><span class="sxs-lookup"><span data-stu-id="d51a2-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d51a2-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d51a2-141"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="d51a2-142">IID</span><span class="sxs-lookup"><span data-stu-id="d51a2-142">IID</span></span><br/>                      | <span data-ttu-id="d51a2-143">IID \_ имсрдпклиентадванцедсеттингс определен как 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="d51a2-143">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d51a2-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d51a2-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d51a2-145">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="d51a2-145">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="d51a2-146">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="d51a2-146">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="d51a2-147">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="d51a2-147">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="d51a2-148">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="d51a2-148">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="d51a2-149">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="d51a2-149">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="d51a2-150">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="d51a2-150">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="d51a2-151">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="d51a2-151">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="d51a2-152">**имсрдпклиентадванцедсеттингс**</span><span class="sxs-lookup"><span data-stu-id="d51a2-152">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





