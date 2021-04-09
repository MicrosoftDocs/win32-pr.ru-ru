---
title: Имсрдпклиентадванцедсеттингс Пинконнектионбар, свойство
description: Указывает состояние панели подключения пользовательского интерфейса.
ms.assetid: b1f9cb02-3ee3-4574-a874-2584b0d5b47e
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Пинконнектионбар
- Службы удаленных рабочих столов свойства Пинконнектионбар, интерфейс Имсрдпклиентадванцедсеттингс
- Службы удаленных рабочих столов интерфейса Имсрдпклиентадванцедсеттингс, свойство Пинконнектионбар
- Службы удаленных рабочих столов свойства Пинконнектионбар, интерфейс IMsRdpClientAdvancedSettings2
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings2, свойство Пинконнектионбар
- Службы удаленных рабочих столов свойства Пинконнектионбар, интерфейс IMsRdpClientAdvancedSettings3
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings3, свойство Пинконнектионбар
- Службы удаленных рабочих столов свойства Пинконнектионбар, интерфейс IMsRdpClientAdvancedSettings4
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings4, свойство Пинконнектионбар
- Службы удаленных рабочих столов свойства Пинконнектионбар, интерфейс IMsRdpClientAdvancedSettings5
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings5, свойство Пинконнектионбар
- Службы удаленных рабочих столов свойства Пинконнектионбар, интерфейс IMsRdpClientAdvancedSettings6
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings6, свойство Пинконнектионбар
- Службы удаленных рабочих столов свойства Пинконнектионбар, интерфейс IMsRdpClientAdvancedSettings7
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings7, свойство Пинконнектионбар
- Службы удаленных рабочих столов свойства Пинконнектионбар, интерфейс IMsRdpClientAdvancedSettings8
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings8, свойство Пинконнектионбар
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.PinConnectionBar
- IMsRdpClientAdvancedSettings.get_PinConnectionBar
- IMsRdpClientAdvancedSettings.put_PinConnectionBar
- IMsRdpClientAdvancedSettings2.PinConnectionBar
- IMsRdpClientAdvancedSettings2.get_PinConnectionBar
- IMsRdpClientAdvancedSettings2.put_PinConnectionBar
- IMsRdpClientAdvancedSettings3.PinConnectionBar
- IMsRdpClientAdvancedSettings3.get_PinConnectionBar
- IMsRdpClientAdvancedSettings3.put_PinConnectionBar
- IMsRdpClientAdvancedSettings4.PinConnectionBar
- IMsRdpClientAdvancedSettings4.get_PinConnectionBar
- IMsRdpClientAdvancedSettings4.put_PinConnectionBar
- IMsRdpClientAdvancedSettings5.PinConnectionBar
- IMsRdpClientAdvancedSettings5.get_PinConnectionBar
- IMsRdpClientAdvancedSettings5.put_PinConnectionBar
- IMsRdpClientAdvancedSettings6.PinConnectionBar
- IMsRdpClientAdvancedSettings6.get_PinConnectionBar
- IMsRdpClientAdvancedSettings6.put_PinConnectionBar
- IMsRdpClientAdvancedSettings7.PinConnectionBar
- IMsRdpClientAdvancedSettings7.get_PinConnectionBar
- IMsRdpClientAdvancedSettings7.put_PinConnectionBar
- IMsRdpClientAdvancedSettings8.PinConnectionBar
- IMsRdpClientAdvancedSettings8.get_PinConnectionBar
- IMsRdpClientAdvancedSettings8.put_PinConnectionBar
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0da294d933026194d7307a7fa0a175575761809e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891465"
---
# <a name="imsrdpclientadvancedsettingspinconnectionbar-property"></a><span data-ttu-id="80113-120">Имсрдпклиентадванцедсеттингс: свойство Инконнектионбар:P</span><span class="sxs-lookup"><span data-stu-id="80113-120">IMsRdpClientAdvancedSettings::PinConnectionBar property</span></span>

<span data-ttu-id="80113-121">Указывает состояние панели подключения пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="80113-121">Specifies the state of the UI connection bar.</span></span>

<span data-ttu-id="80113-122">Это свойство возвращает **E \_ нотимпл** , если контейнер вызывает метод [**иобжектсафети:: сетинтерфацесафетйоптионс**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768225(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="80113-122">This property returns **E\_NOTIMPL** if the container calls the [**IObjectSafety::SetInterfaceSafetyOptions**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768225(v=vs.85)) method.</span></span>

<span data-ttu-id="80113-123">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="80113-123">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="80113-124">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="80113-124">Syntax</span></span>


```C++
HRESULT put_PinConnectionBar(
  [in]  VARIANT_BOOL fPinConnectionBar
);

HRESULT get_PinConnectionBar(
  [out] VARIANT_BOOL *pfPinConnectionBar
);
```



## <a name="property-value"></a><span data-ttu-id="80113-125">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="80113-125">Property value</span></span>

<span data-ttu-id="80113-126">Если задать для этого свойства значение **Variant \_ true** , состояние будет равно «lower», то есть невидимым для пользователя и недоступным для входных данных.</span><span class="sxs-lookup"><span data-stu-id="80113-126">Setting this property to **VARIANT\_TRUE** sets the state to "lowered", that is, invisible to the user and unavailable for input.</span></span> <span data-ttu-id="80113-127">**Вариант \_ Значение FALSE** задает состояние "вызвано" и доступно для входных данных пользователя.</span><span class="sxs-lookup"><span data-stu-id="80113-127">**VARIANT\_FALSE** sets the state to "raised" and available for user input.</span></span>

## <a name="error-codes"></a><span data-ttu-id="80113-128">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="80113-128">Error codes</span></span>

<span data-ttu-id="80113-129">При успешном выполнении возвращает значение **\_ ОК** .</span><span class="sxs-lookup"><span data-stu-id="80113-129">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="80113-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="80113-130">Remarks</span></span>

<span data-ttu-id="80113-131">Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="80113-131">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="80113-132">Требования</span><span class="sxs-lookup"><span data-stu-id="80113-132">Requirements</span></span>



| <span data-ttu-id="80113-133">Требование</span><span class="sxs-lookup"><span data-stu-id="80113-133">Requirement</span></span> | <span data-ttu-id="80113-134">Значение</span><span class="sxs-lookup"><span data-stu-id="80113-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80113-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="80113-135">Minimum supported client</span></span><br/> | <span data-ttu-id="80113-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="80113-136">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="80113-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="80113-137">Minimum supported server</span></span><br/> | <span data-ttu-id="80113-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="80113-138">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="80113-139">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="80113-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="80113-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="80113-140"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="80113-141">DLL</span><span class="sxs-lookup"><span data-stu-id="80113-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="80113-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="80113-142"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="80113-143">IID</span><span class="sxs-lookup"><span data-stu-id="80113-143">IID</span></span><br/>                      | <span data-ttu-id="80113-144">IID \_ имсрдпклиентадванцедсеттингс определен как 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="80113-144">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="80113-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="80113-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80113-146">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="80113-146">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="80113-147">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="80113-147">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="80113-148">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="80113-148">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="80113-149">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="80113-149">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="80113-150">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="80113-150">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="80113-151">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="80113-151">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="80113-152">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="80113-152">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="80113-153">**имсрдпклиентадванцедсеттингс**</span><span class="sxs-lookup"><span data-stu-id="80113-153">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

