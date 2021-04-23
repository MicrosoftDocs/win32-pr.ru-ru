---
title: Имсрдпклиентадванцедсеттингс Овераллконнектионтимеаут, свойство
description: Указывает общий период времени в секундах, в течение которого клиентский элемент управления ожидает завершения соединения.
ms.assetid: 02fb24e1-b5e4-4d8e-a1c2-a9bd62a69bed
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Овераллконнектионтимеаут
- службы удаленных рабочих столов свойства Овераллконнектионтимеаут, интерфейс Имсрдпклиентадванцедсеттингс
- Службы удаленных рабочих столов интерфейса Имсрдпклиентадванцедсеттингс, свойство Овераллконнектионтимеаут
- службы удаленных рабочих столов свойства Овераллконнектионтимеаут, интерфейс IMsRdpClientAdvancedSettings2
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings2, свойство Овераллконнектионтимеаут
- службы удаленных рабочих столов свойства Овераллконнектионтимеаут, интерфейс IMsRdpClientAdvancedSettings3
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings3, свойство Овераллконнектионтимеаут
- службы удаленных рабочих столов свойства Овераллконнектионтимеаут, интерфейс IMsRdpClientAdvancedSettings4
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings4, свойство Овераллконнектионтимеаут
- службы удаленных рабочих столов свойства Овераллконнектионтимеаут, интерфейс IMsRdpClientAdvancedSettings5
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings5, свойство Овераллконнектионтимеаут
- службы удаленных рабочих столов свойства Овераллконнектионтимеаут, интерфейс IMsRdpClientAdvancedSettings6
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings6, свойство Овераллконнектионтимеаут
- службы удаленных рабочих столов свойства Овераллконнектионтимеаут, интерфейс IMsRdpClientAdvancedSettings7
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings7, свойство Овераллконнектионтимеаут
- службы удаленных рабочих столов свойства Овераллконнектионтимеаут, интерфейс IMsRdpClientAdvancedSettings8
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings8, свойство Овераллконнектионтимеаут
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.overallConnectionTimeout
- IMsRdpClientAdvancedSettings.get_overallConnectionTimeout
- IMsRdpClientAdvancedSettings.put_overallConnectionTimeout
- IMsRdpClientAdvancedSettings2.overallConnectionTimeout
- IMsRdpClientAdvancedSettings2.get_overallConnectionTimeout
- IMsRdpClientAdvancedSettings2.put_overallConnectionTimeout
- IMsRdpClientAdvancedSettings3.overallConnectionTimeout
- IMsRdpClientAdvancedSettings3.get_overallConnectionTimeout
- IMsRdpClientAdvancedSettings3.put_overallConnectionTimeout
- IMsRdpClientAdvancedSettings4.overallConnectionTimeout
- IMsRdpClientAdvancedSettings4.get_overallConnectionTimeout
- IMsRdpClientAdvancedSettings4.put_overallConnectionTimeout
- IMsRdpClientAdvancedSettings5.overallConnectionTimeout
- IMsRdpClientAdvancedSettings5.get_overallConnectionTimeout
- IMsRdpClientAdvancedSettings5.put_overallConnectionTimeout
- IMsRdpClientAdvancedSettings6.overallConnectionTimeout
- IMsRdpClientAdvancedSettings6.get_overallConnectionTimeout
- IMsRdpClientAdvancedSettings6.put_overallConnectionTimeout
- IMsRdpClientAdvancedSettings7.overallConnectionTimeout
- IMsRdpClientAdvancedSettings7.get_overallConnectionTimeout
- IMsRdpClientAdvancedSettings7.put_overallConnectionTimeout
- IMsRdpClientAdvancedSettings8.overallConnectionTimeout
- IMsRdpClientAdvancedSettings8.get_overallConnectionTimeout
- IMsRdpClientAdvancedSettings8.put_overallConnectionTimeout
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50de6687d3d5cbccb3f7fdab94eca5ba4f2331c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672576"
---
# <a name="imsrdpclientadvancedsettingsoverallconnectiontimeout-property"></a><span data-ttu-id="0de5f-120">Свойство Имсрдпклиентадванцедсеттингс:: Овераллконнектионтимеаут</span><span class="sxs-lookup"><span data-stu-id="0de5f-120">IMsRdpClientAdvancedSettings::overallConnectionTimeout property</span></span>

<span data-ttu-id="0de5f-121">Указывает общий период времени в секундах, в течение которого клиентский элемент управления ожидает завершения соединения.</span><span class="sxs-lookup"><span data-stu-id="0de5f-121">Specifies the total length of time, in seconds, that the client control waits for a connection to complete.</span></span>

<span data-ttu-id="0de5f-122">Если указанное время истекает до завершения соединения, элемент управления отключится и вызовет метод [**имстскаксевентс:: OnDisconnection**](imstscaxevents-ondisconnected.md) .</span><span class="sxs-lookup"><span data-stu-id="0de5f-122">If the specified time elapses before connection completes, the control disconnects and calls the [**IMsTscAxEvents::OnDisconnected**](imstscaxevents-ondisconnected.md) method.</span></span>

<span data-ttu-id="0de5f-123">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="0de5f-123">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="0de5f-124">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0de5f-124">Syntax</span></span>


```C++
HRESULT put_overallConnectionTimeout(
  [in]  LONG overallConnectionTimeout
);

HRESULT get_overallConnectionTimeout(
  [out] LONG *poverallConnectionTimeout
);
```



## <a name="property-value"></a><span data-ttu-id="0de5f-125">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="0de5f-125">Property value</span></span>

<span data-ttu-id="0de5f-126">Новое время в секундах.</span><span class="sxs-lookup"><span data-stu-id="0de5f-126">The new time, in seconds.</span></span> <span data-ttu-id="0de5f-127">Максимальное значение — 600, которое представляет 10 минут.</span><span class="sxs-lookup"><span data-stu-id="0de5f-127">The maximum value is 600, which represents 10 minutes.</span></span>

## <a name="error-codes"></a><span data-ttu-id="0de5f-128">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="0de5f-128">Error codes</span></span>

<span data-ttu-id="0de5f-129">При успешном выполнении возвращает значение **\_ ОК** .</span><span class="sxs-lookup"><span data-stu-id="0de5f-129">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="0de5f-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0de5f-130">Remarks</span></span>

<span data-ttu-id="0de5f-131">Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="0de5f-131">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0de5f-132">Требования</span><span class="sxs-lookup"><span data-stu-id="0de5f-132">Requirements</span></span>



| <span data-ttu-id="0de5f-133">Требование</span><span class="sxs-lookup"><span data-stu-id="0de5f-133">Requirement</span></span> | <span data-ttu-id="0de5f-134">Значение</span><span class="sxs-lookup"><span data-stu-id="0de5f-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0de5f-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0de5f-135">Minimum supported client</span></span><br/> | <span data-ttu-id="0de5f-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0de5f-136">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="0de5f-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0de5f-137">Minimum supported server</span></span><br/> | <span data-ttu-id="0de5f-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0de5f-138">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="0de5f-139">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="0de5f-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="0de5f-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0de5f-140"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="0de5f-141">DLL</span><span class="sxs-lookup"><span data-stu-id="0de5f-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0de5f-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0de5f-142"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="0de5f-143">IID</span><span class="sxs-lookup"><span data-stu-id="0de5f-143">IID</span></span><br/>                      | <span data-ttu-id="0de5f-144">IID \_ имсрдпклиентадванцедсеттингс определен как 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="0de5f-144">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0de5f-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0de5f-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0de5f-146">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="0de5f-146">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="0de5f-147">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="0de5f-147">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="0de5f-148">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="0de5f-148">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="0de5f-149">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="0de5f-149">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="0de5f-150">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="0de5f-150">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="0de5f-151">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="0de5f-151">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="0de5f-152">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="0de5f-152">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="0de5f-153">**имсрдпклиентадванцедсеттингс**</span><span class="sxs-lookup"><span data-stu-id="0de5f-153">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="0de5f-154">**синглеконнектионтимеаут**</span><span class="sxs-lookup"><span data-stu-id="0de5f-154">**singleConnectionTimeout**</span></span>](imsrdpclientadvancedsettings-singleconnectiontimeout.md)
</dt> </dl>

 

 





