---
title: Имсрдпклиентадванцедсеттингс Шутдовнтимеаут, свойство
description: Указывает период времени в секундах, в течение которого сервер должен ожидать ответа сервера на запрос на отключение.
ms.assetid: 3fa935dc-d4b0-433b-ab67-a644fcf09006
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Шутдовнтимеаут
- службы удаленных рабочих столов свойства Шутдовнтимеаут, интерфейс Имсрдпклиентадванцедсеттингс
- Службы удаленных рабочих столов интерфейса Имсрдпклиентадванцедсеттингс, свойство Шутдовнтимеаут
- службы удаленных рабочих столов свойства Шутдовнтимеаут, интерфейс IMsRdpClientAdvancedSettings2
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings2, свойство Шутдовнтимеаут
- службы удаленных рабочих столов свойства Шутдовнтимеаут, интерфейс IMsRdpClientAdvancedSettings3
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings3, свойство Шутдовнтимеаут
- службы удаленных рабочих столов свойства Шутдовнтимеаут, интерфейс IMsRdpClientAdvancedSettings4
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings4, свойство Шутдовнтимеаут
- службы удаленных рабочих столов свойства Шутдовнтимеаут, интерфейс IMsRdpClientAdvancedSettings5
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings5, свойство Шутдовнтимеаут
- службы удаленных рабочих столов свойства Шутдовнтимеаут, интерфейс IMsRdpClientAdvancedSettings6
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings6, свойство Шутдовнтимеаут
- службы удаленных рабочих столов свойства Шутдовнтимеаут, интерфейс IMsRdpClientAdvancedSettings7
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings7, свойство Шутдовнтимеаут
- службы удаленных рабочих столов свойства Шутдовнтимеаут, интерфейс IMsRdpClientAdvancedSettings8
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings8, свойство Шутдовнтимеаут
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.shutdownTimeout
- IMsRdpClientAdvancedSettings.get_shutdownTimeout
- IMsRdpClientAdvancedSettings.put_shutdownTimeout
- IMsRdpClientAdvancedSettings2.shutdownTimeout
- IMsRdpClientAdvancedSettings2.get_shutdownTimeout
- IMsRdpClientAdvancedSettings2.put_shutdownTimeout
- IMsRdpClientAdvancedSettings3.shutdownTimeout
- IMsRdpClientAdvancedSettings3.get_shutdownTimeout
- IMsRdpClientAdvancedSettings3.put_shutdownTimeout
- IMsRdpClientAdvancedSettings4.shutdownTimeout
- IMsRdpClientAdvancedSettings4.get_shutdownTimeout
- IMsRdpClientAdvancedSettings4.put_shutdownTimeout
- IMsRdpClientAdvancedSettings5.shutdownTimeout
- IMsRdpClientAdvancedSettings5.get_shutdownTimeout
- IMsRdpClientAdvancedSettings5.put_shutdownTimeout
- IMsRdpClientAdvancedSettings6.shutdownTimeout
- IMsRdpClientAdvancedSettings6.get_shutdownTimeout
- IMsRdpClientAdvancedSettings6.put_shutdownTimeout
- IMsRdpClientAdvancedSettings7.shutdownTimeout
- IMsRdpClientAdvancedSettings7.get_shutdownTimeout
- IMsRdpClientAdvancedSettings7.put_shutdownTimeout
- IMsRdpClientAdvancedSettings8.shutdownTimeout
- IMsRdpClientAdvancedSettings8.get_shutdownTimeout
- IMsRdpClientAdvancedSettings8.put_shutdownTimeout
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 868a011a0ce484f5bb2dd7d1ec610f4e3a436898
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104414769"
---
# <a name="imsrdpclientadvancedsettingsshutdowntimeout-property"></a><span data-ttu-id="f75d6-120">Свойство Имсрдпклиентадванцедсеттингс:: Шутдовнтимеаут</span><span class="sxs-lookup"><span data-stu-id="f75d6-120">IMsRdpClientAdvancedSettings::shutdownTimeout property</span></span>

<span data-ttu-id="f75d6-121">Указывает период времени в секундах, в течение которого сервер должен ожидать ответа сервера на запрос на отключение.</span><span class="sxs-lookup"><span data-stu-id="f75d6-121">Specifies the length of time, in seconds, to wait for the server to respond to a disconnection request.</span></span>

<span data-ttu-id="f75d6-122">Если сервер не отвечает в течение указанного времени, клиентский элемент управления отключается.</span><span class="sxs-lookup"><span data-stu-id="f75d6-122">If the server does not reply within the specified time, the client control disconnects.</span></span>

<span data-ttu-id="f75d6-123">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="f75d6-123">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="f75d6-124">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f75d6-124">Syntax</span></span>


```C++
HRESULT put_shutdownTimeout(
  [in]  LONG shutdownTimeout
);

HRESULT get_shutdownTimeout(
  [out] LONG *pshutdownTimeout
);
```



## <a name="property-value"></a><span data-ttu-id="f75d6-125">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="f75d6-125">Property value</span></span>

<span data-ttu-id="f75d6-126">Новое время в секундах.</span><span class="sxs-lookup"><span data-stu-id="f75d6-126">The new time, in seconds.</span></span> <span data-ttu-id="f75d6-127">Значение свойства по умолчанию равно 10.</span><span class="sxs-lookup"><span data-stu-id="f75d6-127">The default value of the property is 10.</span></span> <span data-ttu-id="f75d6-128">Максимальное значение — 600, которое представляет 10 минут.</span><span class="sxs-lookup"><span data-stu-id="f75d6-128">The maximum value is 600, which represents 10 minutes.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f75d6-129">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="f75d6-129">Error codes</span></span>

<span data-ttu-id="f75d6-130">При успешном выполнении возвращает значение **\_ ОК** .</span><span class="sxs-lookup"><span data-stu-id="f75d6-130">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="f75d6-131">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f75d6-131">Remarks</span></span>

<span data-ttu-id="f75d6-132">Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="f75d6-132">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f75d6-133">Требования</span><span class="sxs-lookup"><span data-stu-id="f75d6-133">Requirements</span></span>



| <span data-ttu-id="f75d6-134">Требование</span><span class="sxs-lookup"><span data-stu-id="f75d6-134">Requirement</span></span> | <span data-ttu-id="f75d6-135">Значение</span><span class="sxs-lookup"><span data-stu-id="f75d6-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f75d6-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f75d6-136">Minimum supported client</span></span><br/> | <span data-ttu-id="f75d6-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f75d6-137">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="f75d6-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f75d6-138">Minimum supported server</span></span><br/> | <span data-ttu-id="f75d6-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f75d6-139">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="f75d6-140">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="f75d6-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="f75d6-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f75d6-141"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="f75d6-142">DLL</span><span class="sxs-lookup"><span data-stu-id="f75d6-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f75d6-143"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f75d6-143"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="f75d6-144">IID</span><span class="sxs-lookup"><span data-stu-id="f75d6-144">IID</span></span><br/>                      | <span data-ttu-id="f75d6-145">IID \_ имсрдпклиентадванцедсеттингс определен как 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="f75d6-145">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f75d6-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f75d6-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f75d6-147">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="f75d6-147">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="f75d6-148">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="f75d6-148">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="f75d6-149">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="f75d6-149">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="f75d6-150">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="f75d6-150">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="f75d6-151">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="f75d6-151">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="f75d6-152">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="f75d6-152">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="f75d6-153">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="f75d6-153">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="f75d6-154">**имсрдпклиентадванцедсеттингс**</span><span class="sxs-lookup"><span data-stu-id="f75d6-154">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





