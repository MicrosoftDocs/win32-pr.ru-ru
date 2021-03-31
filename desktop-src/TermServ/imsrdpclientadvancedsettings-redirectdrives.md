---
title: Имсрдпклиентадванцедсеттингс Редиректдривес, свойство
description: Указывает, разрешено ли перенаправление дисков.
ms.assetid: 5ed4cd28-4a1f-4d3b-9f9d-bf44a8483209
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Редиректдривес
- Службы удаленных рабочих столов свойства Редиректдривес, интерфейс Имсрдпклиентадванцедсеттингс
- Службы удаленных рабочих столов интерфейса Имсрдпклиентадванцедсеттингс, свойство Редиректдривес
- Службы удаленных рабочих столов свойства Редиректдривес, интерфейс IMsRdpClientAdvancedSettings2
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings2, свойство Редиректдривес
- Службы удаленных рабочих столов свойства Редиректдривес, интерфейс IMsRdpClientAdvancedSettings3
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings3, свойство Редиректдривес
- Службы удаленных рабочих столов свойства Редиректдривес, интерфейс IMsRdpClientAdvancedSettings4
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings4, свойство Редиректдривес
- Службы удаленных рабочих столов свойства Редиректдривес, интерфейс IMsRdpClientAdvancedSettings5
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings5, свойство Редиректдривес
- Службы удаленных рабочих столов свойства Редиректдривес, интерфейс IMsRdpClientAdvancedSettings6
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings6, свойство Редиректдривес
- Службы удаленных рабочих столов свойства Редиректдривес, интерфейс IMsRdpClientAdvancedSettings7
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings7, свойство Редиректдривес
- Службы удаленных рабочих столов свойства Редиректдривес, интерфейс IMsRdpClientAdvancedSettings8
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings8, свойство Редиректдривес
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.RedirectDrives
- IMsRdpClientAdvancedSettings.get_RedirectDrives
- IMsRdpClientAdvancedSettings.put_RedirectDrives
- IMsRdpClientAdvancedSettings2.RedirectDrives
- IMsRdpClientAdvancedSettings2.get_RedirectDrives
- IMsRdpClientAdvancedSettings2.put_RedirectDrives
- IMsRdpClientAdvancedSettings3.RedirectDrives
- IMsRdpClientAdvancedSettings3.get_RedirectDrives
- IMsRdpClientAdvancedSettings3.put_RedirectDrives
- IMsRdpClientAdvancedSettings4.RedirectDrives
- IMsRdpClientAdvancedSettings4.get_RedirectDrives
- IMsRdpClientAdvancedSettings4.put_RedirectDrives
- IMsRdpClientAdvancedSettings5.RedirectDrives
- IMsRdpClientAdvancedSettings5.get_RedirectDrives
- IMsRdpClientAdvancedSettings5.put_RedirectDrives
- IMsRdpClientAdvancedSettings6.RedirectDrives
- IMsRdpClientAdvancedSettings6.get_RedirectDrives
- IMsRdpClientAdvancedSettings6.put_RedirectDrives
- IMsRdpClientAdvancedSettings7.RedirectDrives
- IMsRdpClientAdvancedSettings7.get_RedirectDrives
- IMsRdpClientAdvancedSettings7.put_RedirectDrives
- IMsRdpClientAdvancedSettings8.RedirectDrives
- IMsRdpClientAdvancedSettings8.get_RedirectDrives
- IMsRdpClientAdvancedSettings8.put_RedirectDrives
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c83d24ae4ea4dae2760c1e468f4fa8b326a94c38
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803892"
---
# <a name="imsrdpclientadvancedsettingsredirectdrives-property"></a><span data-ttu-id="eeabc-120">Свойство Имсрдпклиентадванцедсеттингс:: Редиректдривес</span><span class="sxs-lookup"><span data-stu-id="eeabc-120">IMsRdpClientAdvancedSettings::RedirectDrives property</span></span>

<span data-ttu-id="eeabc-121">Указывает, разрешено ли перенаправление дисков.</span><span class="sxs-lookup"><span data-stu-id="eeabc-121">Specifies if redirection of disk drives is allowed.</span></span>

<span data-ttu-id="eeabc-122">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="eeabc-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="eeabc-123">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="eeabc-123">Syntax</span></span>


```C++
HRESULT put_RedirectDrives(
  [in]  VARIANT_BOOL redirectDrives
);

HRESULT get_RedirectDrives(
  [out] VARIANT_BOOL *predirectDrives
);
```



## <a name="property-value"></a><span data-ttu-id="eeabc-124">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="eeabc-124">Property value</span></span>

<span data-ttu-id="eeabc-125">Присвойте этому параметру значение **Variant \_ true** , чтобы разрешить перенаправление или **вариант \_ false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="eeabc-125">Set this parameter to **VARIANT\_TRUE** to allow redirection or **VARIANT\_FALSE** otherwise.</span></span> <span data-ttu-id="eeabc-126">**Вариант \_ Значение TRUE** предложит пользователю подтвердить возможность перенаправления во время подключения в целях безопасности.</span><span class="sxs-lookup"><span data-stu-id="eeabc-126">**VARIANT\_TRUE** prompts the user to confirm allowing redirection at connection time, for security purposes.</span></span>

## <a name="error-codes"></a><span data-ttu-id="eeabc-127">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="eeabc-127">Error codes</span></span>

<span data-ttu-id="eeabc-128">При успешном выполнении возвращает значение **\_ ОК** .</span><span class="sxs-lookup"><span data-stu-id="eeabc-128">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="eeabc-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="eeabc-129">Remarks</span></span>

<span data-ttu-id="eeabc-130">Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="eeabc-130">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="eeabc-131">Требования</span><span class="sxs-lookup"><span data-stu-id="eeabc-131">Requirements</span></span>



| <span data-ttu-id="eeabc-132">Требование</span><span class="sxs-lookup"><span data-stu-id="eeabc-132">Requirement</span></span> | <span data-ttu-id="eeabc-133">Значение</span><span class="sxs-lookup"><span data-stu-id="eeabc-133">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eeabc-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="eeabc-134">Minimum supported client</span></span><br/> | <span data-ttu-id="eeabc-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="eeabc-135">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="eeabc-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="eeabc-136">Minimum supported server</span></span><br/> | <span data-ttu-id="eeabc-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="eeabc-137">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="eeabc-138">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="eeabc-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="eeabc-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eeabc-139"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="eeabc-140">DLL</span><span class="sxs-lookup"><span data-stu-id="eeabc-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eeabc-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eeabc-141"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="eeabc-142">IID</span><span class="sxs-lookup"><span data-stu-id="eeabc-142">IID</span></span><br/>                      | <span data-ttu-id="eeabc-143">IID \_ имсрдпклиентадванцедсеттингс определен как 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="eeabc-143">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="eeabc-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="eeabc-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eeabc-145">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="eeabc-145">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="eeabc-146">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="eeabc-146">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="eeabc-147">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="eeabc-147">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="eeabc-148">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="eeabc-148">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="eeabc-149">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="eeabc-149">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="eeabc-150">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="eeabc-150">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="eeabc-151">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="eeabc-151">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="eeabc-152">**имсрдпклиентадванцедсеттингс**</span><span class="sxs-lookup"><span data-stu-id="eeabc-152">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





