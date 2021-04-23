---
title: Имсрдпклиентадванцедсеттингс Редиректпринтерс, свойство
description: Указывает, разрешено ли перенаправление принтеров.
ms.assetid: 7d4f28a7-a99d-4d0b-ab51-832a78881900
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Редиректпринтерс
- Службы удаленных рабочих столов свойства Редиректпринтерс, интерфейс Имсрдпклиентадванцедсеттингс
- Службы удаленных рабочих столов интерфейса Имсрдпклиентадванцедсеттингс, свойство Редиректпринтерс
- Службы удаленных рабочих столов свойства Редиректпринтерс, интерфейс IMsRdpClientAdvancedSettings2
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings2, свойство Редиректпринтерс
- Службы удаленных рабочих столов свойства Редиректпринтерс, интерфейс IMsRdpClientAdvancedSettings3
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings3, свойство Редиректпринтерс
- Службы удаленных рабочих столов свойства Редиректпринтерс, интерфейс IMsRdpClientAdvancedSettings4
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings4, свойство Редиректпринтерс
- Службы удаленных рабочих столов свойства Редиректпринтерс, интерфейс IMsRdpClientAdvancedSettings5
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings5, свойство Редиректпринтерс
- Службы удаленных рабочих столов свойства Редиректпринтерс, интерфейс IMsRdpClientAdvancedSettings6
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings6, свойство Редиректпринтерс
- Службы удаленных рабочих столов свойства Редиректпринтерс, интерфейс IMsRdpClientAdvancedSettings7
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings7, свойство Редиректпринтерс
- Службы удаленных рабочих столов свойства Редиректпринтерс, интерфейс IMsRdpClientAdvancedSettings8
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings8, свойство Редиректпринтерс
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.RedirectPrinters
- IMsRdpClientAdvancedSettings.get_RedirectPrinters
- IMsRdpClientAdvancedSettings.put_RedirectPrinters
- IMsRdpClientAdvancedSettings2.RedirectPrinters
- IMsRdpClientAdvancedSettings2.get_RedirectPrinters
- IMsRdpClientAdvancedSettings2.put_RedirectPrinters
- IMsRdpClientAdvancedSettings3.RedirectPrinters
- IMsRdpClientAdvancedSettings3.get_RedirectPrinters
- IMsRdpClientAdvancedSettings3.put_RedirectPrinters
- IMsRdpClientAdvancedSettings4.RedirectPrinters
- IMsRdpClientAdvancedSettings4.get_RedirectPrinters
- IMsRdpClientAdvancedSettings4.put_RedirectPrinters
- IMsRdpClientAdvancedSettings5.RedirectPrinters
- IMsRdpClientAdvancedSettings5.get_RedirectPrinters
- IMsRdpClientAdvancedSettings5.put_RedirectPrinters
- IMsRdpClientAdvancedSettings6.RedirectPrinters
- IMsRdpClientAdvancedSettings6.get_RedirectPrinters
- IMsRdpClientAdvancedSettings6.put_RedirectPrinters
- IMsRdpClientAdvancedSettings7.RedirectPrinters
- IMsRdpClientAdvancedSettings7.get_RedirectPrinters
- IMsRdpClientAdvancedSettings7.put_RedirectPrinters
- IMsRdpClientAdvancedSettings8.RedirectPrinters
- IMsRdpClientAdvancedSettings8.get_RedirectPrinters
- IMsRdpClientAdvancedSettings8.put_RedirectPrinters
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94fecc3b6f72b8706168c75d220d78fc49340752
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801168"
---
# <a name="imsrdpclientadvancedsettingsredirectprinters-property"></a><span data-ttu-id="d0089-120">Свойство Имсрдпклиентадванцедсеттингс:: Редиректпринтерс</span><span class="sxs-lookup"><span data-stu-id="d0089-120">IMsRdpClientAdvancedSettings::RedirectPrinters property</span></span>

<span data-ttu-id="d0089-121">Указывает, разрешено ли перенаправление принтеров.</span><span class="sxs-lookup"><span data-stu-id="d0089-121">Specifies if redirection of printers is allowed.</span></span>

<span data-ttu-id="d0089-122">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="d0089-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0089-123">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d0089-123">Syntax</span></span>


```C++
HRESULT put_RedirectPrinters(
  [in]  VARIANT_BOOL redirectPrinters
);

HRESULT get_RedirectPrinters(
  [out] VARIANT_BOOL *predirectPrinters
);
```



## <a name="property-value"></a><span data-ttu-id="d0089-124">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="d0089-124">Property value</span></span>

<span data-ttu-id="d0089-125">Присвойте этому параметру значение **Variant \_ true** , чтобы разрешить перенаправление или **вариант \_ false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="d0089-125">Set this parameter to **VARIANT\_TRUE** to allow redirection or **VARIANT\_FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d0089-126">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="d0089-126">Error codes</span></span>

<span data-ttu-id="d0089-127">При успешном выполнении возвращает значение **\_ ОК** .</span><span class="sxs-lookup"><span data-stu-id="d0089-127">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="d0089-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d0089-128">Remarks</span></span>

<span data-ttu-id="d0089-129">Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="d0089-129">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d0089-130">Требования</span><span class="sxs-lookup"><span data-stu-id="d0089-130">Requirements</span></span>



| <span data-ttu-id="d0089-131">Требование</span><span class="sxs-lookup"><span data-stu-id="d0089-131">Requirement</span></span> | <span data-ttu-id="d0089-132">Значение</span><span class="sxs-lookup"><span data-stu-id="d0089-132">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0089-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d0089-133">Minimum supported client</span></span><br/> | <span data-ttu-id="d0089-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d0089-134">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="d0089-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d0089-135">Minimum supported server</span></span><br/> | <span data-ttu-id="d0089-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d0089-136">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="d0089-137">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="d0089-137">Type library</span></span><br/>             | <dl> <span data-ttu-id="d0089-138"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d0089-138"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="d0089-139">DLL</span><span class="sxs-lookup"><span data-stu-id="d0089-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d0089-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d0089-140"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="d0089-141">IID</span><span class="sxs-lookup"><span data-stu-id="d0089-141">IID</span></span><br/>                      | <span data-ttu-id="d0089-142">IID \_ имсрдпклиентадванцедсеттингс определен как 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="d0089-142">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d0089-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d0089-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0089-144">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="d0089-144">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="d0089-145">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="d0089-145">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="d0089-146">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="d0089-146">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="d0089-147">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="d0089-147">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="d0089-148">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="d0089-148">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="d0089-149">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="d0089-149">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="d0089-150">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="d0089-150">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="d0089-151">**имсрдпклиентадванцедсеттингс**</span><span class="sxs-lookup"><span data-stu-id="d0089-151">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





