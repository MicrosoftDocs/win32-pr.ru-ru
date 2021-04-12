---
title: Имсрдпклиентадванцедсеттингс keepAliveInterval, свойство
description: Указывает интервал (в миллисекундах), в течение которого клиент отправляет сообщения проверки активности на сервер.
ms.assetid: 0d1b7d8f-f81c-4591-bb08-adab307e87fe
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства keepAliveInterval
- службы удаленных рабочих столов свойства keepAliveInterval, интерфейс Имсрдпклиентадванцедсеттингс
- Службы удаленных рабочих столов интерфейса Имсрдпклиентадванцедсеттингс, свойство keepAliveInterval
- службы удаленных рабочих столов свойства keepAliveInterval, интерфейс IMsRdpClientAdvancedSettings2
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings2, свойство keepAliveInterval
- службы удаленных рабочих столов свойства keepAliveInterval, интерфейс IMsRdpClientAdvancedSettings3
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings3, свойство keepAliveInterval
- службы удаленных рабочих столов свойства keepAliveInterval, интерфейс IMsRdpClientAdvancedSettings4
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings4, свойство keepAliveInterval
- службы удаленных рабочих столов свойства keepAliveInterval, интерфейс IMsRdpClientAdvancedSettings5
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings5, свойство keepAliveInterval
- службы удаленных рабочих столов свойства keepAliveInterval, интерфейс IMsRdpClientAdvancedSettings6
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings6, свойство keepAliveInterval
- службы удаленных рабочих столов свойства keepAliveInterval, интерфейс IMsRdpClientAdvancedSettings7
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings7, свойство keepAliveInterval
- службы удаленных рабочих столов свойства keepAliveInterval, интерфейс IMsRdpClientAdvancedSettings8
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings8, свойство keepAliveInterval
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.keepAliveInterval
- IMsRdpClientAdvancedSettings.get_keepAliveInterval
- IMsRdpClientAdvancedSettings.put_keepAliveInterval
- IMsRdpClientAdvancedSettings2.keepAliveInterval
- IMsRdpClientAdvancedSettings2.get_keepAliveInterval
- IMsRdpClientAdvancedSettings2.put_keepAliveInterval
- IMsRdpClientAdvancedSettings3.keepAliveInterval
- IMsRdpClientAdvancedSettings3.get_keepAliveInterval
- IMsRdpClientAdvancedSettings3.put_keepAliveInterval
- IMsRdpClientAdvancedSettings4.keepAliveInterval
- IMsRdpClientAdvancedSettings4.get_keepAliveInterval
- IMsRdpClientAdvancedSettings4.put_keepAliveInterval
- IMsRdpClientAdvancedSettings5.keepAliveInterval
- IMsRdpClientAdvancedSettings5.get_keepAliveInterval
- IMsRdpClientAdvancedSettings5.put_keepAliveInterval
- IMsRdpClientAdvancedSettings6.keepAliveInterval
- IMsRdpClientAdvancedSettings6.get_keepAliveInterval
- IMsRdpClientAdvancedSettings6.put_keepAliveInterval
- IMsRdpClientAdvancedSettings7.keepAliveInterval
- IMsRdpClientAdvancedSettings7.get_keepAliveInterval
- IMsRdpClientAdvancedSettings7.put_keepAliveInterval
- IMsRdpClientAdvancedSettings8.keepAliveInterval
- IMsRdpClientAdvancedSettings8.get_keepAliveInterval
- IMsRdpClientAdvancedSettings8.put_keepAliveInterval
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d15412b5b1803aadcffa08a8617742e0c90b1a0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415185"
---
# <a name="imsrdpclientadvancedsettingskeepaliveinterval-property"></a><span data-ttu-id="c75ab-120">Свойство Имсрдпклиентадванцедсеттингс:: keepAliveInterval</span><span class="sxs-lookup"><span data-stu-id="c75ab-120">IMsRdpClientAdvancedSettings::keepAliveInterval property</span></span>

<span data-ttu-id="c75ab-121">Указывает интервал (в миллисекундах), в течение которого клиент отправляет сообщения проверки активности на сервер.</span><span class="sxs-lookup"><span data-stu-id="c75ab-121">Specifies an interval, in milliseconds, at which the client sends keep-alive messages to the server.</span></span>

<span data-ttu-id="c75ab-122">Параметр групповой политики, указывающий, разрешено ли постоянное подключение клиентов к серверу, может переопределить этот параметр свойства.</span><span class="sxs-lookup"><span data-stu-id="c75ab-122">A group policy setting that specifies whether persistent client connections to the server are allowed can override this property setting.</span></span>

<span data-ttu-id="c75ab-123">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="c75ab-123">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="c75ab-124">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c75ab-124">Syntax</span></span>


```C++
HRESULT put_keepAliveInterval(
  [in]  LONG keepAliveInterval
);

HRESULT get_keepAliveInterval(
  [out] LONG *pkeepAliveInterval
);
```



## <a name="property-value"></a><span data-ttu-id="c75ab-125">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="c75ab-125">Property value</span></span>

<span data-ttu-id="c75ab-126">Новый интервал в миллисекундах.</span><span class="sxs-lookup"><span data-stu-id="c75ab-126">The new interval, in milliseconds.</span></span> <span data-ttu-id="c75ab-127">Значение свойства по умолчанию равно нулю, что отключает сообщения о состоянии активности.</span><span class="sxs-lookup"><span data-stu-id="c75ab-127">The default value of the property is zero, which disables keep-alive messages.</span></span> <span data-ttu-id="c75ab-128">Минимальное допустимое значение этого свойства — 10 000, которое представляет 10 секунд.</span><span class="sxs-lookup"><span data-stu-id="c75ab-128">The minimum valid value of this property is 10,000, which represents 10 seconds.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c75ab-129">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="c75ab-129">Error codes</span></span>

<span data-ttu-id="c75ab-130">При успешном выполнении возвращает значение **\_ ОК** .</span><span class="sxs-lookup"><span data-stu-id="c75ab-130">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="c75ab-131">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c75ab-131">Remarks</span></span>

<span data-ttu-id="c75ab-132">Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="c75ab-132">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c75ab-133">Требования</span><span class="sxs-lookup"><span data-stu-id="c75ab-133">Requirements</span></span>



| <span data-ttu-id="c75ab-134">Требование</span><span class="sxs-lookup"><span data-stu-id="c75ab-134">Requirement</span></span> | <span data-ttu-id="c75ab-135">Значение</span><span class="sxs-lookup"><span data-stu-id="c75ab-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c75ab-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c75ab-136">Minimum supported client</span></span><br/> | <span data-ttu-id="c75ab-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c75ab-137">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="c75ab-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c75ab-138">Minimum supported server</span></span><br/> | <span data-ttu-id="c75ab-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c75ab-139">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="c75ab-140">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="c75ab-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="c75ab-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c75ab-141"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="c75ab-142">DLL</span><span class="sxs-lookup"><span data-stu-id="c75ab-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c75ab-143"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c75ab-143"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="c75ab-144">IID</span><span class="sxs-lookup"><span data-stu-id="c75ab-144">IID</span></span><br/>                      | <span data-ttu-id="c75ab-145">IID \_ имсрдпклиентадванцедсеттингс определен как 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="c75ab-145">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c75ab-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c75ab-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c75ab-147">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="c75ab-147">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="c75ab-148">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="c75ab-148">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="c75ab-149">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="c75ab-149">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="c75ab-150">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="c75ab-150">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="c75ab-151">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="c75ab-151">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="c75ab-152">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="c75ab-152">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="c75ab-153">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="c75ab-153">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="c75ab-154">**имсрдпклиентадванцедсеттингс**</span><span class="sxs-lookup"><span data-stu-id="c75ab-154">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





