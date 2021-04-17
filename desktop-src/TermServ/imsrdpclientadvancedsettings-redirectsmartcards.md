---
title: Имсрдпклиентадванцедсеттингс Редиректсмарткардс, свойство
description: Указывает, разрешено ли перенаправление смарт-карт.
ms.assetid: 53b6b483-ccba-41eb-a417-241a4430958e
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Редиректсмарткардс
- Службы удаленных рабочих столов свойства Редиректсмарткардс, интерфейс Имсрдпклиентадванцедсеттингс
- Службы удаленных рабочих столов интерфейса Имсрдпклиентадванцедсеттингс, свойство Редиректсмарткардс
- Службы удаленных рабочих столов свойства Редиректсмарткардс, интерфейс IMsRdpClientAdvancedSettings2
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings2, свойство Редиректсмарткардс
- Службы удаленных рабочих столов свойства Редиректсмарткардс, интерфейс IMsRdpClientAdvancedSettings3
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings3, свойство Редиректсмарткардс
- Службы удаленных рабочих столов свойства Редиректсмарткардс, интерфейс IMsRdpClientAdvancedSettings4
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings4, свойство Редиректсмарткардс
- Службы удаленных рабочих столов свойства Редиректсмарткардс, интерфейс IMsRdpClientAdvancedSettings5
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings5, свойство Редиректсмарткардс
- Службы удаленных рабочих столов свойства Редиректсмарткардс, интерфейс IMsRdpClientAdvancedSettings6
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings6, свойство Редиректсмарткардс
- Службы удаленных рабочих столов свойства Редиректсмарткардс, интерфейс IMsRdpClientAdvancedSettings7
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings7, свойство Редиректсмарткардс
- Службы удаленных рабочих столов свойства Редиректсмарткардс, интерфейс IMsRdpClientAdvancedSettings8
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings8, свойство Редиректсмарткардс
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.RedirectSmartCards
- IMsRdpClientAdvancedSettings.get_RedirectSmartCards
- IMsRdpClientAdvancedSettings.put_RedirectSmartCards
- IMsRdpClientAdvancedSettings2.RedirectSmartCards
- IMsRdpClientAdvancedSettings2.get_RedirectSmartCards
- IMsRdpClientAdvancedSettings2.put_RedirectSmartCards
- IMsRdpClientAdvancedSettings3.RedirectSmartCards
- IMsRdpClientAdvancedSettings3.get_RedirectSmartCards
- IMsRdpClientAdvancedSettings3.put_RedirectSmartCards
- IMsRdpClientAdvancedSettings4.RedirectSmartCards
- IMsRdpClientAdvancedSettings4.get_RedirectSmartCards
- IMsRdpClientAdvancedSettings4.put_RedirectSmartCards
- IMsRdpClientAdvancedSettings5.RedirectSmartCards
- IMsRdpClientAdvancedSettings5.get_RedirectSmartCards
- IMsRdpClientAdvancedSettings5.put_RedirectSmartCards
- IMsRdpClientAdvancedSettings6.RedirectSmartCards
- IMsRdpClientAdvancedSettings6.get_RedirectSmartCards
- IMsRdpClientAdvancedSettings6.put_RedirectSmartCards
- IMsRdpClientAdvancedSettings7.RedirectSmartCards
- IMsRdpClientAdvancedSettings7.get_RedirectSmartCards
- IMsRdpClientAdvancedSettings7.put_RedirectSmartCards
- IMsRdpClientAdvancedSettings8.RedirectSmartCards
- IMsRdpClientAdvancedSettings8.get_RedirectSmartCards
- IMsRdpClientAdvancedSettings8.put_RedirectSmartCards
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ba58a492ede5371c0f43d996f46ed7a898df7f8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672467"
---
# <a name="imsrdpclientadvancedsettingsredirectsmartcards-property"></a><span data-ttu-id="6cf94-120">Свойство Имсрдпклиентадванцедсеттингс:: Редиректсмарткардс</span><span class="sxs-lookup"><span data-stu-id="6cf94-120">IMsRdpClientAdvancedSettings::RedirectSmartCards property</span></span>

<span data-ttu-id="6cf94-121">Указывает, разрешено ли перенаправление смарт-карт.</span><span class="sxs-lookup"><span data-stu-id="6cf94-121">Specifies if redirection of smart cards is allowed.</span></span>

<span data-ttu-id="6cf94-122">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="6cf94-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="6cf94-123">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6cf94-123">Syntax</span></span>


```C++
HRESULT put_RedirectSmartCards(
  [in]  VARIANT_BOOL redirectSmartCards
);

HRESULT get_RedirectSmartCards(
  [out] VARIANT_BOOL *predirectSmartCards
);
```



## <a name="property-value"></a><span data-ttu-id="6cf94-124">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="6cf94-124">Property value</span></span>

<span data-ttu-id="6cf94-125">Присвойте этому параметру значение **Variant \_ true** , чтобы разрешить перенаправление или **вариант \_ false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="6cf94-125">Set this parameter to **VARIANT\_TRUE** to allow redirection or **VARIANT\_FALSE** otherwise.</span></span> <span data-ttu-id="6cf94-126">**Вариант \_ Значение TRUE** предложит пользователю подтвердить возможность перенаправления во время подключения в целях безопасности.</span><span class="sxs-lookup"><span data-stu-id="6cf94-126">**VARIANT\_TRUE** prompts the user to confirm allowing redirection at connection time, for security purposes.</span></span>

## <a name="error-codes"></a><span data-ttu-id="6cf94-127">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="6cf94-127">Error codes</span></span>

<span data-ttu-id="6cf94-128">При успешном выполнении возвращает значение **\_ ОК** .</span><span class="sxs-lookup"><span data-stu-id="6cf94-128">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="6cf94-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6cf94-129">Remarks</span></span>

<span data-ttu-id="6cf94-130">Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="6cf94-130">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6cf94-131">Требования</span><span class="sxs-lookup"><span data-stu-id="6cf94-131">Requirements</span></span>



| <span data-ttu-id="6cf94-132">Требование</span><span class="sxs-lookup"><span data-stu-id="6cf94-132">Requirement</span></span> | <span data-ttu-id="6cf94-133">Значение</span><span class="sxs-lookup"><span data-stu-id="6cf94-133">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6cf94-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6cf94-134">Minimum supported client</span></span><br/> | <span data-ttu-id="6cf94-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6cf94-135">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="6cf94-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6cf94-136">Minimum supported server</span></span><br/> | <span data-ttu-id="6cf94-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6cf94-137">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="6cf94-138">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="6cf94-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="6cf94-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6cf94-139"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="6cf94-140">DLL</span><span class="sxs-lookup"><span data-stu-id="6cf94-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6cf94-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6cf94-141"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="6cf94-142">IID</span><span class="sxs-lookup"><span data-stu-id="6cf94-142">IID</span></span><br/>                      | <span data-ttu-id="6cf94-143">IID \_ имсрдпклиентадванцедсеттингс определен как 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="6cf94-143">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6cf94-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6cf94-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6cf94-145">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="6cf94-145">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="6cf94-146">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="6cf94-146">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="6cf94-147">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="6cf94-147">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="6cf94-148">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="6cf94-148">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="6cf94-149">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="6cf94-149">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="6cf94-150">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="6cf94-150">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="6cf94-151">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="6cf94-151">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="6cf94-152">**имсрдпклиентадванцедсеттингс**</span><span class="sxs-lookup"><span data-stu-id="6cf94-152">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





