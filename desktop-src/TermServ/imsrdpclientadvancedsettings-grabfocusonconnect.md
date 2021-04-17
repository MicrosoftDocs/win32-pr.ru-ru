---
title: Имсрдпклиентадванцедсеттингс Грабфокусонконнект, свойство
description: Указывает, должен ли клиентский элемент управления иметь фокус при подключении.
ms.assetid: c67fc284-6e07-4749-84bf-70c0ae4d1b2b
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Грабфокусонконнект
- Службы удаленных рабочих столов свойства Грабфокусонконнект, интерфейс Имсрдпклиентадванцедсеттингс
- Службы удаленных рабочих столов интерфейса Имсрдпклиентадванцедсеттингс, свойство Грабфокусонконнект
- Службы удаленных рабочих столов свойства Грабфокусонконнект, интерфейс IMsRdpClientAdvancedSettings2
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings2, свойство Грабфокусонконнект
- Службы удаленных рабочих столов свойства Грабфокусонконнект, интерфейс IMsRdpClientAdvancedSettings3
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings3, свойство Грабфокусонконнект
- Службы удаленных рабочих столов свойства Грабфокусонконнект, интерфейс IMsRdpClientAdvancedSettings4
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings4, свойство Грабфокусонконнект
- Службы удаленных рабочих столов свойства Грабфокусонконнект, интерфейс IMsRdpClientAdvancedSettings5
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings5, свойство Грабфокусонконнект
- Службы удаленных рабочих столов свойства Грабфокусонконнект, интерфейс IMsRdpClientAdvancedSettings6
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings6, свойство Грабфокусонконнект
- Службы удаленных рабочих столов свойства Грабфокусонконнект, интерфейс IMsRdpClientAdvancedSettings7
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings7, свойство Грабфокусонконнект
- Службы удаленных рабочих столов свойства Грабфокусонконнект, интерфейс IMsRdpClientAdvancedSettings8
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings8, свойство Грабфокусонконнект
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.GrabFocusOnConnect
- IMsRdpClientAdvancedSettings.get_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings.put_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings2.GrabFocusOnConnect
- IMsRdpClientAdvancedSettings2.get_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings2.put_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings3.GrabFocusOnConnect
- IMsRdpClientAdvancedSettings3.get_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings3.put_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings4.GrabFocusOnConnect
- IMsRdpClientAdvancedSettings4.get_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings4.put_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings5.GrabFocusOnConnect
- IMsRdpClientAdvancedSettings5.get_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings5.put_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings6.GrabFocusOnConnect
- IMsRdpClientAdvancedSettings6.get_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings6.put_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings7.GrabFocusOnConnect
- IMsRdpClientAdvancedSettings7.get_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings7.put_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings8.GrabFocusOnConnect
- IMsRdpClientAdvancedSettings8.get_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings8.put_GrabFocusOnConnect
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e7fb04c00bd7aaaf4de1252d961206ffee0e6b9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672837"
---
# <a name="imsrdpclientadvancedsettingsgrabfocusonconnect-property"></a><span data-ttu-id="86d63-120">Свойство Имсрдпклиентадванцедсеттингс:: Грабфокусонконнект</span><span class="sxs-lookup"><span data-stu-id="86d63-120">IMsRdpClientAdvancedSettings::GrabFocusOnConnect property</span></span>

<span data-ttu-id="86d63-121">Указывает, должен ли клиентский элемент управления иметь фокус при подключении.</span><span class="sxs-lookup"><span data-stu-id="86d63-121">Specifies if the client control should have the focus while connecting.</span></span> <span data-ttu-id="86d63-122">Элемент управления не будет пытаться захватить фокус из окна, выполняющегося в другом процессе.</span><span class="sxs-lookup"><span data-stu-id="86d63-122">The control will not attempt to grab focus from a window running in a different process.</span></span>

<span data-ttu-id="86d63-123">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="86d63-123">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="86d63-124">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="86d63-124">Syntax</span></span>


```C++
HRESULT put_GrabFocusOnConnect(
  [in]  VARIANT_BOOL fGrabFocusOnConnect
);

HRESULT get_GrabFocusOnConnect(
  [out] VARIANT_BOOL pfGrabFocusOnConnect
);
```



## <a name="property-value"></a><span data-ttu-id="86d63-125">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="86d63-125">Property value</span></span>

<span data-ttu-id="86d63-126">Присвойте этому параметру значение **Variant \_ false** , чтобы отключить функцию или **вариант \_ true** , чтобы включить эту функцию.</span><span class="sxs-lookup"><span data-stu-id="86d63-126">Set this parameter to **VARIANT\_FALSE** to disable the feature or **VARIANT\_TRUE** to enable the feature.</span></span> <span data-ttu-id="86d63-127">Установка этого свойства в значение **Variant \_ false** не позволяет элементу управления переустанавливать фокус при соединении.</span><span class="sxs-lookup"><span data-stu-id="86d63-127">Setting this property to **VARIANT\_FALSE** prevents the control from grabbing focus when connecting.</span></span>

## <a name="error-codes"></a><span data-ttu-id="86d63-128">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="86d63-128">Error codes</span></span>

<span data-ttu-id="86d63-129">При успешном выполнении возвращает значение **\_ ОК** .</span><span class="sxs-lookup"><span data-stu-id="86d63-129">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="86d63-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="86d63-130">Remarks</span></span>

<span data-ttu-id="86d63-131">Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="86d63-131">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="86d63-132">Требования</span><span class="sxs-lookup"><span data-stu-id="86d63-132">Requirements</span></span>



| <span data-ttu-id="86d63-133">Требование</span><span class="sxs-lookup"><span data-stu-id="86d63-133">Requirement</span></span> | <span data-ttu-id="86d63-134">Значение</span><span class="sxs-lookup"><span data-stu-id="86d63-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="86d63-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="86d63-135">Minimum supported client</span></span><br/> | <span data-ttu-id="86d63-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="86d63-136">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="86d63-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="86d63-137">Minimum supported server</span></span><br/> | <span data-ttu-id="86d63-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="86d63-138">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="86d63-139">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="86d63-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="86d63-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="86d63-140"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="86d63-141">DLL</span><span class="sxs-lookup"><span data-stu-id="86d63-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="86d63-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="86d63-142"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="86d63-143">IID</span><span class="sxs-lookup"><span data-stu-id="86d63-143">IID</span></span><br/>                      | <span data-ttu-id="86d63-144">IID \_ имсрдпклиентадванцедсеттингс определен как 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="86d63-144">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="86d63-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="86d63-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86d63-146">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="86d63-146">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="86d63-147">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="86d63-147">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="86d63-148">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="86d63-148">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="86d63-149">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="86d63-149">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="86d63-150">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="86d63-150">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="86d63-151">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="86d63-151">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="86d63-152">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="86d63-152">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="86d63-153">**имсрдпклиентадванцедсеттингс**</span><span class="sxs-lookup"><span data-stu-id="86d63-153">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





