---
title: Имсрдпклиентадванцедсеттингс Синглеконнектионтимеаут, свойство
description: Указывает максимальный интервал времени в секундах, в течение которого клиентский элемент управления ожидает подключения к IP-адресу.
ms.assetid: 57fb2397-8229-4446-88fd-e75cb96c7ac5
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Синглеконнектионтимеаут
- службы удаленных рабочих столов свойства Синглеконнектионтимеаут, интерфейс Имсрдпклиентадванцедсеттингс
- Службы удаленных рабочих столов интерфейса Имсрдпклиентадванцедсеттингс, свойство Синглеконнектионтимеаут
- службы удаленных рабочих столов свойства Синглеконнектионтимеаут, интерфейс IMsRdpClientAdvancedSettings2
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings2, свойство Синглеконнектионтимеаут
- службы удаленных рабочих столов свойства Синглеконнектионтимеаут, интерфейс IMsRdpClientAdvancedSettings3
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings3, свойство Синглеконнектионтимеаут
- службы удаленных рабочих столов свойства Синглеконнектионтимеаут, интерфейс IMsRdpClientAdvancedSettings4
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings4, свойство Синглеконнектионтимеаут
- службы удаленных рабочих столов свойства Синглеконнектионтимеаут, интерфейс IMsRdpClientAdvancedSettings5
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings5, свойство Синглеконнектионтимеаут
- службы удаленных рабочих столов свойства Синглеконнектионтимеаут, интерфейс IMsRdpClientAdvancedSettings6
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings6, свойство Синглеконнектионтимеаут
- службы удаленных рабочих столов свойства Синглеконнектионтимеаут, интерфейс IMsRdpClientAdvancedSettings7
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings7, свойство Синглеконнектионтимеаут
- службы удаленных рабочих столов свойства Синглеконнектионтимеаут, интерфейс IMsRdpClientAdvancedSettings8
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings8, свойство Синглеконнектионтимеаут
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.singleConnectionTimeout
- IMsRdpClientAdvancedSettings.get_singleConnectionTimeout
- IMsRdpClientAdvancedSettings.put_singleConnectionTimeout
- IMsRdpClientAdvancedSettings2.singleConnectionTimeout
- IMsRdpClientAdvancedSettings2.get_singleConnectionTimeout
- IMsRdpClientAdvancedSettings2.put_singleConnectionTimeout
- IMsRdpClientAdvancedSettings3.singleConnectionTimeout
- IMsRdpClientAdvancedSettings3.get_singleConnectionTimeout
- IMsRdpClientAdvancedSettings3.put_singleConnectionTimeout
- IMsRdpClientAdvancedSettings4.singleConnectionTimeout
- IMsRdpClientAdvancedSettings4.get_singleConnectionTimeout
- IMsRdpClientAdvancedSettings4.put_singleConnectionTimeout
- IMsRdpClientAdvancedSettings5.singleConnectionTimeout
- IMsRdpClientAdvancedSettings5.get_singleConnectionTimeout
- IMsRdpClientAdvancedSettings5.put_singleConnectionTimeout
- IMsRdpClientAdvancedSettings6.singleConnectionTimeout
- IMsRdpClientAdvancedSettings6.get_singleConnectionTimeout
- IMsRdpClientAdvancedSettings6.put_singleConnectionTimeout
- IMsRdpClientAdvancedSettings7.singleConnectionTimeout
- IMsRdpClientAdvancedSettings7.get_singleConnectionTimeout
- IMsRdpClientAdvancedSettings7.put_singleConnectionTimeout
- IMsRdpClientAdvancedSettings8.singleConnectionTimeout
- IMsRdpClientAdvancedSettings8.get_singleConnectionTimeout
- IMsRdpClientAdvancedSettings8.put_singleConnectionTimeout
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55a0d2eb34235c874b4408e5e4c6f0a349a1ab93
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104414768"
---
# <a name="imsrdpclientadvancedsettingssingleconnectiontimeout-property"></a><span data-ttu-id="4d8bd-120">Свойство Имсрдпклиентадванцедсеттингс:: Синглеконнектионтимеаут</span><span class="sxs-lookup"><span data-stu-id="4d8bd-120">IMsRdpClientAdvancedSettings::singleConnectionTimeout property</span></span>

<span data-ttu-id="4d8bd-121">Указывает максимальный интервал времени в секундах, в течение которого клиентский элемент управления ожидает подключения к IP-адресу.</span><span class="sxs-lookup"><span data-stu-id="4d8bd-121">Specifies the maximum length of time, in seconds, that the client control waits for a connection to an IP address.</span></span>

<span data-ttu-id="4d8bd-122">Во время подключения элемент управления может попытаться подключиться к нескольким IP-адресам.</span><span class="sxs-lookup"><span data-stu-id="4d8bd-122">During connection, the control may attempt to connect to multiple IP addresses.</span></span>

<span data-ttu-id="4d8bd-123">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="4d8bd-123">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d8bd-124">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4d8bd-124">Syntax</span></span>


```C++
HRESULT put_singleConnectionTimeout(
  [in]  LONG singleConnectionTimeout
);

HRESULT get_singleConnectionTimeout(
  [out] LONG *psingleConnectionTimeout
);
```



## <a name="property-value"></a><span data-ttu-id="4d8bd-125">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="4d8bd-125">Property value</span></span>

<span data-ttu-id="4d8bd-126">Новое время в секундах.</span><span class="sxs-lookup"><span data-stu-id="4d8bd-126">The new time, in seconds.</span></span> <span data-ttu-id="4d8bd-127">Максимальное значение — 600.</span><span class="sxs-lookup"><span data-stu-id="4d8bd-127">The maximum value is 600.</span></span>

## <a name="error-codes"></a><span data-ttu-id="4d8bd-128">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="4d8bd-128">Error codes</span></span>

<span data-ttu-id="4d8bd-129">При успешном выполнении возвращает значение **\_ ОК** .</span><span class="sxs-lookup"><span data-stu-id="4d8bd-129">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="4d8bd-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4d8bd-130">Remarks</span></span>

<span data-ttu-id="4d8bd-131">Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="4d8bd-131">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4d8bd-132">Требования</span><span class="sxs-lookup"><span data-stu-id="4d8bd-132">Requirements</span></span>



| <span data-ttu-id="4d8bd-133">Требование</span><span class="sxs-lookup"><span data-stu-id="4d8bd-133">Requirement</span></span> | <span data-ttu-id="4d8bd-134">Значение</span><span class="sxs-lookup"><span data-stu-id="4d8bd-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d8bd-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4d8bd-135">Minimum supported client</span></span><br/> | <span data-ttu-id="4d8bd-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4d8bd-136">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="4d8bd-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4d8bd-137">Minimum supported server</span></span><br/> | <span data-ttu-id="4d8bd-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4d8bd-138">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="4d8bd-139">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="4d8bd-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="4d8bd-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4d8bd-140"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="4d8bd-141">DLL</span><span class="sxs-lookup"><span data-stu-id="4d8bd-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4d8bd-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4d8bd-142"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="4d8bd-143">IID</span><span class="sxs-lookup"><span data-stu-id="4d8bd-143">IID</span></span><br/>                      | <span data-ttu-id="4d8bd-144">IID \_ имсрдпклиентадванцедсеттингс определен как 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="4d8bd-144">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4d8bd-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4d8bd-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d8bd-146">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="4d8bd-146">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="4d8bd-147">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="4d8bd-147">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="4d8bd-148">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="4d8bd-148">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="4d8bd-149">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="4d8bd-149">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="4d8bd-150">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="4d8bd-150">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="4d8bd-151">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="4d8bd-151">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="4d8bd-152">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="4d8bd-152">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="4d8bd-153">**имсрдпклиентадванцедсеттингс**</span><span class="sxs-lookup"><span data-stu-id="4d8bd-153">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="4d8bd-154">**овераллконнектионтимеаут**</span><span class="sxs-lookup"><span data-stu-id="4d8bd-154">**overallConnectionTimeout**</span></span>](imsrdpclientadvancedsettings-overallconnectiontimeout.md)
</dt> </dl>

 

 





