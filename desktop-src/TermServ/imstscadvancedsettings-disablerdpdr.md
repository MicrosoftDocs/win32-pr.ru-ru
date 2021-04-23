---
title: Имстскадванцедсеттингс Дисаблердпдр, свойство
description: Указывает, включено ли перенаправление принтеров и буферов обмена.
ms.assetid: 63e0e024-4792-4efe-a6c5-d122f8adcb0a
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Дисаблердпдр
- Службы удаленных рабочих столов свойства Дисаблердпдр, интерфейс Имстскадванцедсеттингс
- Службы удаленных рабочих столов интерфейса Имстскадванцедсеттингс, свойство Дисаблердпдр
- Службы удаленных рабочих столов свойства Дисаблердпдр, интерфейс Имсрдпклиентадванцедсеттингс
- Службы удаленных рабочих столов интерфейса Имсрдпклиентадванцедсеттингс, свойство Дисаблердпдр
- Службы удаленных рабочих столов свойства Дисаблердпдр, интерфейс IMsRdpClientAdvancedSettings2
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings2, свойство Дисаблердпдр
- Службы удаленных рабочих столов свойства Дисаблердпдр, интерфейс IMsRdpClientAdvancedSettings3
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings3, свойство Дисаблердпдр
- Службы удаленных рабочих столов свойства Дисаблердпдр, интерфейс IMsRdpClientAdvancedSettings4
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings4, свойство Дисаблердпдр
- Службы удаленных рабочих столов свойства Дисаблердпдр, интерфейс IMsRdpClientAdvancedSettings5
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings5, свойство Дисаблердпдр
- Службы удаленных рабочих столов свойства Дисаблердпдр, интерфейс IMsRdpClientAdvancedSettings6
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings6, свойство Дисаблердпдр
- Службы удаленных рабочих столов свойства Дисаблердпдр, интерфейс IMsRdpClientAdvancedSettings7
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings7, свойство Дисаблердпдр
- Службы удаленных рабочих столов свойства Дисаблердпдр, интерфейс IMsRdpClientAdvancedSettings8
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings8, свойство Дисаблердпдр
topic_type:
- apiref
api_name:
- IMsTscAdvancedSettings.DisableRdpdr
- IMsTscAdvancedSettings.get_DisableRdpdr
- IMsTscAdvancedSettings.put_DisableRdpdr
- IMsRdpClientAdvancedSettings.DisableRdpdr
- IMsRdpClientAdvancedSettings.get_DisableRdpdr
- IMsRdpClientAdvancedSettings.put_DisableRdpdr
- IMsRdpClientAdvancedSettings2.DisableRdpdr
- IMsRdpClientAdvancedSettings2.get_DisableRdpdr
- IMsRdpClientAdvancedSettings2.put_DisableRdpdr
- IMsRdpClientAdvancedSettings3.DisableRdpdr
- IMsRdpClientAdvancedSettings3.get_DisableRdpdr
- IMsRdpClientAdvancedSettings3.put_DisableRdpdr
- IMsRdpClientAdvancedSettings4.DisableRdpdr
- IMsRdpClientAdvancedSettings4.get_DisableRdpdr
- IMsRdpClientAdvancedSettings4.put_DisableRdpdr
- IMsRdpClientAdvancedSettings5.DisableRdpdr
- IMsRdpClientAdvancedSettings5.get_DisableRdpdr
- IMsRdpClientAdvancedSettings5.put_DisableRdpdr
- IMsRdpClientAdvancedSettings6.DisableRdpdr
- IMsRdpClientAdvancedSettings6.get_DisableRdpdr
- IMsRdpClientAdvancedSettings6.put_DisableRdpdr
- IMsRdpClientAdvancedSettings7.DisableRdpdr
- IMsRdpClientAdvancedSettings7.get_DisableRdpdr
- IMsRdpClientAdvancedSettings7.put_DisableRdpdr
- IMsRdpClientAdvancedSettings8.DisableRdpdr
- IMsRdpClientAdvancedSettings8.get_DisableRdpdr
- IMsRdpClientAdvancedSettings8.put_DisableRdpdr
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0747f37cd5e85c62946c9b8e3a1587f736dd8af9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681931"
---
# <a name="imstscadvancedsettingsdisablerdpdr-property"></a><span data-ttu-id="5da4d-122">Имстскадванцедсеттингс: свойство Исаблердпдр:D</span><span class="sxs-lookup"><span data-stu-id="5da4d-122">IMsTscAdvancedSettings::DisableRdpdr property</span></span>

<span data-ttu-id="5da4d-123">Указывает, включено ли перенаправление принтеров и буферов обмена.</span><span class="sxs-lookup"><span data-stu-id="5da4d-123">Specifies whether printer and clipboard redirection is enabled.</span></span>

<span data-ttu-id="5da4d-124">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="5da4d-124">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="5da4d-125">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5da4d-125">Syntax</span></span>


```C++
HRESULT put_DisableRdpdr(
  [in]  BOOL DisableRdpdr
);

HRESULT get_DisableRdpdr(
  [out] BOOL *pDisableRdpdr
);
```



## <a name="property-value"></a><span data-ttu-id="5da4d-126">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="5da4d-126">Property value</span></span>

<span data-ttu-id="5da4d-127">Установите для этого параметра **значение true** , чтобы отключить перенаправление, или **значение false** , чтобы включить перенаправление.</span><span class="sxs-lookup"><span data-stu-id="5da4d-127">Set this parameter to **TRUE** to disable redirection or **FALSE** to enable redirection.</span></span>

## <a name="error-codes"></a><span data-ttu-id="5da4d-128">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="5da4d-128">Error codes</span></span>

<span data-ttu-id="5da4d-129">При успешном выполнении возвращает значение **\_ ОК** .</span><span class="sxs-lookup"><span data-stu-id="5da4d-129">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="5da4d-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5da4d-130">Remarks</span></span>

<span data-ttu-id="5da4d-131">Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="5da4d-131">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5da4d-132">Требования</span><span class="sxs-lookup"><span data-stu-id="5da4d-132">Requirements</span></span>



| <span data-ttu-id="5da4d-133">Требование</span><span class="sxs-lookup"><span data-stu-id="5da4d-133">Requirement</span></span> | <span data-ttu-id="5da4d-134">Значение</span><span class="sxs-lookup"><span data-stu-id="5da4d-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="5da4d-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5da4d-135">Minimum supported client</span></span><br/> | <span data-ttu-id="5da4d-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5da4d-136">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="5da4d-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5da4d-137">Minimum supported server</span></span><br/> | <span data-ttu-id="5da4d-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5da4d-138">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="5da4d-139">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="5da4d-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="5da4d-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5da4d-140"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="5da4d-141">DLL</span><span class="sxs-lookup"><span data-stu-id="5da4d-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5da4d-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5da4d-142"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="5da4d-143">IID</span><span class="sxs-lookup"><span data-stu-id="5da4d-143">IID</span></span><br/>                      | <span data-ttu-id="5da4d-144">IID \_ имстскадванцедсеттингс определен как 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d</span><span class="sxs-lookup"><span data-stu-id="5da4d-144">IID\_IMsTscAdvancedSettings is defined as 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5da4d-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5da4d-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5da4d-146">**имсрдпклиентадванцедсеттингс**</span><span class="sxs-lookup"><span data-stu-id="5da4d-146">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="5da4d-147">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="5da4d-147">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="5da4d-148">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="5da4d-148">**IMsRdpClientAdvancedSettings3**</span></span>](imsrdpclientadvancedsettings3.md)
</dt> <dt>

[<span data-ttu-id="5da4d-149">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="5da4d-149">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="5da4d-150">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="5da4d-150">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="5da4d-151">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="5da4d-151">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="5da4d-152">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="5da4d-152">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="5da4d-153">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="5da4d-153">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="5da4d-154">**имстскадванцедсеттингс**</span><span class="sxs-lookup"><span data-stu-id="5da4d-154">**IMsTscAdvancedSettings**</span></span>](imstscadvancedsettings-interface.md)
</dt> </dl>

 

 





