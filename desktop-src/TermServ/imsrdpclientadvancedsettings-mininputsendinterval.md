---
title: Имсрдпклиентадванцедсеттингс Мининпутсендинтервал, свойство
description: Указывает минимальный интервал (в миллисекундах) между отправкой событий мыши.
ms.assetid: d186c05f-0b45-47bd-8a8e-e1f9baf2bd75
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Мининпутсендинтервал
- службы удаленных рабочих столов свойства Мининпутсендинтервал, интерфейс Имсрдпклиентадванцедсеттингс
- Службы удаленных рабочих столов интерфейса Имсрдпклиентадванцедсеттингс, свойство Мининпутсендинтервал
- службы удаленных рабочих столов свойства Мининпутсендинтервал, интерфейс IMsRdpClientAdvancedSettings2
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings2, свойство Мининпутсендинтервал
- службы удаленных рабочих столов свойства Мининпутсендинтервал, интерфейс IMsRdpClientAdvancedSettings3
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings3, свойство Мининпутсендинтервал
- службы удаленных рабочих столов свойства Мининпутсендинтервал, интерфейс IMsRdpClientAdvancedSettings4
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings4, свойство Мининпутсендинтервал
- службы удаленных рабочих столов свойства Мининпутсендинтервал, интерфейс IMsRdpClientAdvancedSettings5
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings5, свойство Мининпутсендинтервал
- службы удаленных рабочих столов свойства Мининпутсендинтервал, интерфейс IMsRdpClientAdvancedSettings6
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings6, свойство Мининпутсендинтервал
- службы удаленных рабочих столов свойства Мининпутсендинтервал, интерфейс IMsRdpClientAdvancedSettings7
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings7, свойство Мининпутсендинтервал
- службы удаленных рабочих столов свойства Мининпутсендинтервал, интерфейс IMsRdpClientAdvancedSettings8
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings8, свойство Мининпутсендинтервал
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.minInputSendInterval
- IMsRdpClientAdvancedSettings.get_minInputSendInterval
- IMsRdpClientAdvancedSettings.put_minInputSendInterval
- IMsRdpClientAdvancedSettings2.minInputSendInterval
- IMsRdpClientAdvancedSettings2.get_minInputSendInterval
- IMsRdpClientAdvancedSettings2.put_minInputSendInterval
- IMsRdpClientAdvancedSettings3.minInputSendInterval
- IMsRdpClientAdvancedSettings3.get_minInputSendInterval
- IMsRdpClientAdvancedSettings3.put_minInputSendInterval
- IMsRdpClientAdvancedSettings4.minInputSendInterval
- IMsRdpClientAdvancedSettings4.get_minInputSendInterval
- IMsRdpClientAdvancedSettings4.put_minInputSendInterval
- IMsRdpClientAdvancedSettings5.minInputSendInterval
- IMsRdpClientAdvancedSettings5.get_minInputSendInterval
- IMsRdpClientAdvancedSettings5.put_minInputSendInterval
- IMsRdpClientAdvancedSettings6.minInputSendInterval
- IMsRdpClientAdvancedSettings6.get_minInputSendInterval
- IMsRdpClientAdvancedSettings6.put_minInputSendInterval
- IMsRdpClientAdvancedSettings7.minInputSendInterval
- IMsRdpClientAdvancedSettings7.get_minInputSendInterval
- IMsRdpClientAdvancedSettings7.put_minInputSendInterval
- IMsRdpClientAdvancedSettings8.minInputSendInterval
- IMsRdpClientAdvancedSettings8.get_minInputSendInterval
- IMsRdpClientAdvancedSettings8.put_minInputSendInterval
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56070e2ba395c4b89dc9caa9e6e5181bb03d81ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415181"
---
# <a name="imsrdpclientadvancedsettingsmininputsendinterval-property"></a><span data-ttu-id="868bd-120">Свойство Имсрдпклиентадванцедсеттингс:: Мининпутсендинтервал</span><span class="sxs-lookup"><span data-stu-id="868bd-120">IMsRdpClientAdvancedSettings::minInputSendInterval property</span></span>

<span data-ttu-id="868bd-121">Указывает минимальный интервал (в миллисекундах) между отправкой событий мыши.</span><span class="sxs-lookup"><span data-stu-id="868bd-121">Specifies the minimum interval, in milliseconds, between the sending of mouse events.</span></span>

<span data-ttu-id="868bd-122">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="868bd-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="868bd-123">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="868bd-123">Syntax</span></span>


```C++
HRESULT put_minInputSendInterval(
  [in]  LONG minInputSendInterval
);

HRESULT get_minInputSendInterval(
  [out] LONG *pminInputSendInterval
);
```



## <a name="property-value"></a><span data-ttu-id="868bd-124">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="868bd-124">Property value</span></span>

<span data-ttu-id="868bd-125">Новый интервал в миллисекундах.</span><span class="sxs-lookup"><span data-stu-id="868bd-125">The new interval, in milliseconds.</span></span> <span data-ttu-id="868bd-126">Значение по умолчанию — 100.</span><span class="sxs-lookup"><span data-stu-id="868bd-126">The default value is 100.</span></span>

## <a name="error-codes"></a><span data-ttu-id="868bd-127">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="868bd-127">Error codes</span></span>

<span data-ttu-id="868bd-128">При успешном выполнении возвращает значение **\_ ОК** .</span><span class="sxs-lookup"><span data-stu-id="868bd-128">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="868bd-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="868bd-129">Remarks</span></span>

<span data-ttu-id="868bd-130">Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="868bd-130">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="868bd-131">Требования</span><span class="sxs-lookup"><span data-stu-id="868bd-131">Requirements</span></span>



| <span data-ttu-id="868bd-132">Требование</span><span class="sxs-lookup"><span data-stu-id="868bd-132">Requirement</span></span> | <span data-ttu-id="868bd-133">Значение</span><span class="sxs-lookup"><span data-stu-id="868bd-133">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="868bd-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="868bd-134">Minimum supported client</span></span><br/> | <span data-ttu-id="868bd-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="868bd-135">Windows 7</span></span><br/>                                                                            |
| <span data-ttu-id="868bd-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="868bd-136">Minimum supported server</span></span><br/> | <span data-ttu-id="868bd-137">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="868bd-137">Windows Server 2008 R2</span></span><br/>                                                               |
| <span data-ttu-id="868bd-138">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="868bd-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="868bd-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="868bd-139"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="868bd-140">DLL</span><span class="sxs-lookup"><span data-stu-id="868bd-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="868bd-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="868bd-141"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="868bd-142">IID</span><span class="sxs-lookup"><span data-stu-id="868bd-142">IID</span></span><br/>                      | <span data-ttu-id="868bd-143">IID \_ имсрдпклиентадванцедсеттингс определен как 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="868bd-143">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="868bd-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="868bd-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="868bd-145">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="868bd-145">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="868bd-146">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="868bd-146">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="868bd-147">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="868bd-147">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="868bd-148">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="868bd-148">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="868bd-149">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="868bd-149">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="868bd-150">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="868bd-150">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="868bd-151">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="868bd-151">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="868bd-152">**имсрдпклиентадванцедсеттингс**</span><span class="sxs-lookup"><span data-stu-id="868bd-152">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





