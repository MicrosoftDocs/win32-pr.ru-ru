---
title: Имсрдпклиентадванцедсеттингс Лоадбаланцеинфо, свойство
description: Указывает файл cookie балансировки нагрузки, который будет помещен в пакет запроса на подключение X. 224 в последовательности подключений протокола сервера узла сеансов удаленный рабочий стол (узел сеансов удаленных рабочих столов).
ms.assetid: 25f12a2e-00a2-42a8-afd3-81efcd94da94
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Лоадбаланцеинфо
- Службы удаленных рабочих столов свойства Лоадбаланцеинфо, интерфейс Имсрдпклиентадванцедсеттингс
- Службы удаленных рабочих столов интерфейса Имсрдпклиентадванцедсеттингс, свойство Лоадбаланцеинфо
- Службы удаленных рабочих столов свойства Лоадбаланцеинфо, интерфейс IMsRdpClientAdvancedSettings2
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings2, свойство Лоадбаланцеинфо
- Службы удаленных рабочих столов свойства Лоадбаланцеинфо, интерфейс IMsRdpClientAdvancedSettings3
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings3, свойство Лоадбаланцеинфо
- Службы удаленных рабочих столов свойства Лоадбаланцеинфо, интерфейс IMsRdpClientAdvancedSettings4
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings4, свойство Лоадбаланцеинфо
- Службы удаленных рабочих столов свойства Лоадбаланцеинфо, интерфейс IMsRdpClientAdvancedSettings5
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings5, свойство Лоадбаланцеинфо
- Службы удаленных рабочих столов свойства Лоадбаланцеинфо, интерфейс IMsRdpClientAdvancedSettings6
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings6, свойство Лоадбаланцеинфо
- Службы удаленных рабочих столов свойства Лоадбаланцеинфо, интерфейс IMsRdpClientAdvancedSettings7
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings7, свойство Лоадбаланцеинфо
- Службы удаленных рабочих столов свойства Лоадбаланцеинфо, интерфейс IMsRdpClientAdvancedSettings8
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings8, свойство Лоадбаланцеинфо
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.LoadBalanceInfo
- IMsRdpClientAdvancedSettings.get_LoadBalanceInfo
- IMsRdpClientAdvancedSettings.put_LoadBalanceInfo
- IMsRdpClientAdvancedSettings2.LoadBalanceInfo
- IMsRdpClientAdvancedSettings2.get_LoadBalanceInfo
- IMsRdpClientAdvancedSettings2.put_LoadBalanceInfo
- IMsRdpClientAdvancedSettings3.LoadBalanceInfo
- IMsRdpClientAdvancedSettings3.get_LoadBalanceInfo
- IMsRdpClientAdvancedSettings3.put_LoadBalanceInfo
- IMsRdpClientAdvancedSettings4.LoadBalanceInfo
- IMsRdpClientAdvancedSettings4.get_LoadBalanceInfo
- IMsRdpClientAdvancedSettings4.put_LoadBalanceInfo
- IMsRdpClientAdvancedSettings5.LoadBalanceInfo
- IMsRdpClientAdvancedSettings5.get_LoadBalanceInfo
- IMsRdpClientAdvancedSettings5.put_LoadBalanceInfo
- IMsRdpClientAdvancedSettings6.LoadBalanceInfo
- IMsRdpClientAdvancedSettings6.get_LoadBalanceInfo
- IMsRdpClientAdvancedSettings6.put_LoadBalanceInfo
- IMsRdpClientAdvancedSettings7.LoadBalanceInfo
- IMsRdpClientAdvancedSettings7.get_LoadBalanceInfo
- IMsRdpClientAdvancedSettings7.put_LoadBalanceInfo
- IMsRdpClientAdvancedSettings8.LoadBalanceInfo
- IMsRdpClientAdvancedSettings8.get_LoadBalanceInfo
- IMsRdpClientAdvancedSettings8.put_LoadBalanceInfo
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a12112eb2a18d38993e905f8d36175f1ab15f58a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415184"
---
# <a name="imsrdpclientadvancedsettingsloadbalanceinfo-property"></a><span data-ttu-id="65cd9-120">Свойство Имсрдпклиентадванцедсеттингс:: Лоадбаланцеинфо</span><span class="sxs-lookup"><span data-stu-id="65cd9-120">IMsRdpClientAdvancedSettings::LoadBalanceInfo property</span></span>

<span data-ttu-id="65cd9-121">Указывает файл cookie балансировки нагрузки, который будет помещен в пакет запроса на подключение X. 224 в последовательности подключений протокола сервера узла сеансов удаленный рабочий стол (узел сеансов удаленных рабочих столов).</span><span class="sxs-lookup"><span data-stu-id="65cd9-121">Specifies the load balancing cookie that will be placed in the X.224 Connection Request packet in the Remote Desktop Session Host (RD Session Host) server protocol connection sequence.</span></span>

<span data-ttu-id="65cd9-122">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="65cd9-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="65cd9-123">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="65cd9-123">Syntax</span></span>


```C++
HRESULT put_LoadBalanceInfo(
  [in]  BSTR newLBInfo
);

HRESULT get_LoadBalanceInfo(
  [out] BSTR *pLBInfo
);
```



## <a name="property-value"></a><span data-ttu-id="65cd9-124">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="65cd9-124">Property value</span></span>

<span data-ttu-id="65cd9-125">Указатель на новый файл cookie.</span><span class="sxs-lookup"><span data-stu-id="65cd9-125">Pointer to the new cookie.</span></span> <span data-ttu-id="65cd9-126">Дополнительные сведения см. в разделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="65cd9-126">For more information, see the remarks section.</span></span>

## <a name="error-codes"></a><span data-ttu-id="65cd9-127">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="65cd9-127">Error codes</span></span>

<span data-ttu-id="65cd9-128">При успешном выполнении возвращает значение **\_ ОК** .</span><span class="sxs-lookup"><span data-stu-id="65cd9-128">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="65cd9-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="65cd9-129">Remarks</span></span>

<span data-ttu-id="65cd9-130">Сведения о балансировке нагрузки используются маршрутизаторами балансировки нагрузки для выбора наиболее подходящего сервера для клиента при использовании ферм серверов узлов сеансов удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="65cd9-130">The load balancing information is used by load balancing routers to choose the best server for the client when using farms of RD Session Host servers.</span></span> <span data-ttu-id="65cd9-131">Сам сервер узла сеансов удаленных рабочих столов не использует эти сведения и будет удален.</span><span class="sxs-lookup"><span data-stu-id="65cd9-131">The RD Session Host server itself does not use this information and will discard it.</span></span>

<span data-ttu-id="65cd9-132">Файл cookie использует следующий синтаксис с учетом регистра:</span><span class="sxs-lookup"><span data-stu-id="65cd9-132">The cookie uses the following, case-sensitive, syntax:</span></span>

<span data-ttu-id="65cd9-133">**Файл cookie: МСТС =**_ипаддрессандпортнумбер_*_\\ r \\ n_*</span><span class="sxs-lookup"><span data-stu-id="65cd9-133">**Cookie: msts=**_IpAddressAndPortNumber_*_\\r\\n_*</span></span>

<span data-ttu-id="65cd9-134">Где *ипаддрессандпортнумбер* — это IP-адрес и номер порта в сетевом порядке байтов.</span><span class="sxs-lookup"><span data-stu-id="65cd9-134">Where *IpAddressAndPortNumber* is the IP address and port number, in network byte order.</span></span>

<span data-ttu-id="65cd9-135">Например, файл cookie, используемый для доступа к IP-адресу 172.31.249.216, номер порта 3389 выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="65cd9-135">For example, the cookie used to access the IP address of 172.31.249.216, port number 3389 is as follows:</span></span>

<span data-ttu-id="65cd9-136">**Файл cookie: МСТС = 3640205228.15629.0000 \\ r \\ n**</span><span class="sxs-lookup"><span data-stu-id="65cd9-136">**Cookie: msts=3640205228.15629.0000\\r\\n**</span></span>

<span data-ttu-id="65cd9-137">Последние четыре нуля являются необязательными и зарезервированы.</span><span class="sxs-lookup"><span data-stu-id="65cd9-137">The final four zeros are optional and are reserved.</span></span> <span data-ttu-id="65cd9-138">Последняя десятичная запятая является обязательной, как и завершающий возврат каретки и перевод строки.</span><span class="sxs-lookup"><span data-stu-id="65cd9-138">The final decimal point is required, as are the trailing carriage return and linefeed.</span></span> <span data-ttu-id="65cd9-139">Длина строки в символах должна быть кратной 2, поэтому при необходимости добавьте пробел.</span><span class="sxs-lookup"><span data-stu-id="65cd9-139">The length of the string, in characters, must be an even multiple of 2, so add a space if necessary.</span></span>

<span data-ttu-id="65cd9-140">Если файл cookie не указан, по умолчанию используется **файл cookie: мстшаш =**_username_*_\\ r \\ n_*.</span><span class="sxs-lookup"><span data-stu-id="65cd9-140">If no cookie is supplied, the default is **Cookie: mstshash=**_UserName_*_\\r\\n_*.</span></span>

<span data-ttu-id="65cd9-141">Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="65cd9-141">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="65cd9-142">Требования</span><span class="sxs-lookup"><span data-stu-id="65cd9-142">Requirements</span></span>



| <span data-ttu-id="65cd9-143">Требование</span><span class="sxs-lookup"><span data-stu-id="65cd9-143">Requirement</span></span> | <span data-ttu-id="65cd9-144">Значение</span><span class="sxs-lookup"><span data-stu-id="65cd9-144">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="65cd9-145">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="65cd9-145">Minimum supported client</span></span><br/> | <span data-ttu-id="65cd9-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="65cd9-146">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="65cd9-147">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="65cd9-147">Minimum supported server</span></span><br/> | <span data-ttu-id="65cd9-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="65cd9-148">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="65cd9-149">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="65cd9-149">Type library</span></span><br/>             | <dl> <span data-ttu-id="65cd9-150"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="65cd9-150"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="65cd9-151">DLL</span><span class="sxs-lookup"><span data-stu-id="65cd9-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="65cd9-152"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="65cd9-152"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="65cd9-153">IID</span><span class="sxs-lookup"><span data-stu-id="65cd9-153">IID</span></span><br/>                      | <span data-ttu-id="65cd9-154">IID \_ имсрдпклиентадванцедсеттингс определен как 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="65cd9-154">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="65cd9-155">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="65cd9-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65cd9-156">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="65cd9-156">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="65cd9-157">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="65cd9-157">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="65cd9-158">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="65cd9-158">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="65cd9-159">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="65cd9-159">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="65cd9-160">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="65cd9-160">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="65cd9-161">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="65cd9-161">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="65cd9-162">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="65cd9-162">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="65cd9-163">**имсрдпклиентадванцедсеттингс**</span><span class="sxs-lookup"><span data-stu-id="65cd9-163">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





