---
title: Имсрдпклиентадванцедсеттингс Смартсизинг, свойство
description: Указывает, следует ли масштабировать изображение, чтобы вместить клиентскую область элемента управления. Обратите внимание, что полосы прокрутки не отображаются, если свойство Смартсизинг включено.
ms.assetid: d0b93129-5f84-49c5-bf8c-048075ac1481
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Смартсизинг
- Службы удаленных рабочих столов свойства Смартсизинг, интерфейс Имсрдпклиентадванцедсеттингс
- Службы удаленных рабочих столов интерфейса Имсрдпклиентадванцедсеттингс, свойство Смартсизинг
- Службы удаленных рабочих столов свойства Смартсизинг, интерфейс IMsRdpClientAdvancedSettings2
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings2, свойство Смартсизинг
- Службы удаленных рабочих столов свойства Смартсизинг, интерфейс IMsRdpClientAdvancedSettings3
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings3, свойство Смартсизинг
- Службы удаленных рабочих столов свойства Смартсизинг, интерфейс IMsRdpClientAdvancedSettings4
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings4, свойство Смартсизинг
- Службы удаленных рабочих столов свойства Смартсизинг, интерфейс IMsRdpClientAdvancedSettings5
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings5, свойство Смартсизинг
- Службы удаленных рабочих столов свойства Смартсизинг, интерфейс IMsRdpClientAdvancedSettings6
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings6, свойство Смартсизинг
- Службы удаленных рабочих столов свойства Смартсизинг, интерфейс IMsRdpClientAdvancedSettings7
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings7, свойство Смартсизинг
- Службы удаленных рабочих столов свойства Смартсизинг, интерфейс IMsRdpClientAdvancedSettings8
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings8, свойство Смартсизинг
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.SmartSizing
- IMsRdpClientAdvancedSettings.get_SmartSizing
- IMsRdpClientAdvancedSettings.put_SmartSizing
- IMsRdpClientAdvancedSettings2.SmartSizing
- IMsRdpClientAdvancedSettings2.get_SmartSizing
- IMsRdpClientAdvancedSettings2.put_SmartSizing
- IMsRdpClientAdvancedSettings3.SmartSizing
- IMsRdpClientAdvancedSettings3.get_SmartSizing
- IMsRdpClientAdvancedSettings3.put_SmartSizing
- IMsRdpClientAdvancedSettings4.SmartSizing
- IMsRdpClientAdvancedSettings4.get_SmartSizing
- IMsRdpClientAdvancedSettings4.put_SmartSizing
- IMsRdpClientAdvancedSettings5.SmartSizing
- IMsRdpClientAdvancedSettings5.get_SmartSizing
- IMsRdpClientAdvancedSettings5.put_SmartSizing
- IMsRdpClientAdvancedSettings6.SmartSizing
- IMsRdpClientAdvancedSettings6.get_SmartSizing
- IMsRdpClientAdvancedSettings6.put_SmartSizing
- IMsRdpClientAdvancedSettings7.SmartSizing
- IMsRdpClientAdvancedSettings7.get_SmartSizing
- IMsRdpClientAdvancedSettings7.put_SmartSizing
- IMsRdpClientAdvancedSettings8.SmartSizing
- IMsRdpClientAdvancedSettings8.get_SmartSizing
- IMsRdpClientAdvancedSettings8.put_SmartSizing
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49ec2a825725e01d876b9e8658f215de6595f32f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104414765"
---
# <a name="imsrdpclientadvancedsettingssmartsizing-property"></a><span data-ttu-id="4fd29-121">Свойство Имсрдпклиентадванцедсеттингс:: Смартсизинг</span><span class="sxs-lookup"><span data-stu-id="4fd29-121">IMsRdpClientAdvancedSettings::SmartSizing property</span></span>

<span data-ttu-id="4fd29-122">Указывает, следует ли масштабировать изображение, чтобы вместить клиентскую область элемента управления.</span><span class="sxs-lookup"><span data-stu-id="4fd29-122">Specifies if the display should be scaled to fit the client area of the control.</span></span> <span data-ttu-id="4fd29-123">Обратите внимание, что полосы прокрутки не отображаются, если свойство **смартсизинг** включено.</span><span class="sxs-lookup"><span data-stu-id="4fd29-123">Note that scroll bars do not appear when the **SmartSizing** property is enabled.</span></span>

<span data-ttu-id="4fd29-124">В отличие от большинства других свойств, это свойство может быть задано при соединении элемента управления.</span><span class="sxs-lookup"><span data-stu-id="4fd29-124">Unlike most other properties, this property can be set when the control is connected.</span></span>

<span data-ttu-id="4fd29-125">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="4fd29-125">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="4fd29-126">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4fd29-126">Syntax</span></span>


```C++
HRESULT put_SmartSizing(
  [in]  VARIANT_BOOL fSmartSizing
);

HRESULT get_SmartSizing(
  [out] VARIANT_BOOL *pfSmartSizing
);
```



## <a name="property-value"></a><span data-ttu-id="4fd29-127">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="4fd29-127">Property value</span></span>

<span data-ttu-id="4fd29-128">Присвойте этому параметру значение **Variant \_ false** , чтобы отключить функцию или **вариант \_ true** , чтобы включить эту функцию.</span><span class="sxs-lookup"><span data-stu-id="4fd29-128">Set this parameter to **VARIANT\_FALSE** to disable the feature or **VARIANT\_TRUE** to enable the feature.</span></span>

## <a name="error-codes"></a><span data-ttu-id="4fd29-129">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="4fd29-129">Error codes</span></span>

<span data-ttu-id="4fd29-130">При успешном выполнении возвращает значение **\_ ОК** .</span><span class="sxs-lookup"><span data-stu-id="4fd29-130">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="4fd29-131">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4fd29-131">Remarks</span></span>

<span data-ttu-id="4fd29-132">Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="4fd29-132">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4fd29-133">Требования</span><span class="sxs-lookup"><span data-stu-id="4fd29-133">Requirements</span></span>



| <span data-ttu-id="4fd29-134">Требование</span><span class="sxs-lookup"><span data-stu-id="4fd29-134">Requirement</span></span> | <span data-ttu-id="4fd29-135">Значение</span><span class="sxs-lookup"><span data-stu-id="4fd29-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4fd29-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4fd29-136">Minimum supported client</span></span><br/> | <span data-ttu-id="4fd29-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4fd29-137">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="4fd29-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4fd29-138">Minimum supported server</span></span><br/> | <span data-ttu-id="4fd29-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4fd29-139">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="4fd29-140">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="4fd29-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="4fd29-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4fd29-141"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="4fd29-142">DLL</span><span class="sxs-lookup"><span data-stu-id="4fd29-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4fd29-143"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4fd29-143"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="4fd29-144">IID</span><span class="sxs-lookup"><span data-stu-id="4fd29-144">IID</span></span><br/>                      | <span data-ttu-id="4fd29-145">IID \_ имсрдпклиентадванцедсеттингс определен как 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="4fd29-145">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4fd29-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4fd29-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4fd29-147">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="4fd29-147">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="4fd29-148">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="4fd29-148">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="4fd29-149">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="4fd29-149">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="4fd29-150">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="4fd29-150">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="4fd29-151">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="4fd29-151">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="4fd29-152">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="4fd29-152">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="4fd29-153">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="4fd29-153">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="4fd29-154">**имсрдпклиентадванцедсеттингс**</span><span class="sxs-lookup"><span data-stu-id="4fd29-154">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





