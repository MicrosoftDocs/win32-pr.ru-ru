---
title: Имсрдпклиентадванцедсеттингс Рдппорт, свойство
description: Указывает порт подключения.
ms.assetid: 15be7ef8-8ed2-46e0-8cc5-d5cf1642b79e
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Рдппорт
- Службы удаленных рабочих столов свойства Рдппорт, интерфейс Имсрдпклиентадванцедсеттингс
- Службы удаленных рабочих столов интерфейса Имсрдпклиентадванцедсеттингс, свойство Рдппорт
- Службы удаленных рабочих столов свойства Рдппорт, интерфейс IMsRdpClientAdvancedSettings2
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings2, свойство Рдппорт
- Службы удаленных рабочих столов свойства Рдппорт, интерфейс IMsRdpClientAdvancedSettings3
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings3, свойство Рдппорт
- Службы удаленных рабочих столов свойства Рдппорт, интерфейс IMsRdpClientAdvancedSettings4
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings4, свойство Рдппорт
- Службы удаленных рабочих столов свойства Рдппорт, интерфейс IMsRdpClientAdvancedSettings5
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings5, свойство Рдппорт
- Службы удаленных рабочих столов свойства Рдппорт, интерфейс IMsRdpClientAdvancedSettings6
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings6, свойство Рдппорт
- Службы удаленных рабочих столов свойства Рдппорт, интерфейс IMsRdpClientAdvancedSettings7
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings7, свойство Рдппорт
- Службы удаленных рабочих столов свойства Рдппорт, интерфейс IMsRdpClientAdvancedSettings8
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings8, свойство Рдппорт
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.RDPPort
- IMsRdpClientAdvancedSettings.get_RDPPort
- IMsRdpClientAdvancedSettings.put_RDPPort
- IMsRdpClientAdvancedSettings2.RDPPort
- IMsRdpClientAdvancedSettings2.get_RDPPort
- IMsRdpClientAdvancedSettings2.put_RDPPort
- IMsRdpClientAdvancedSettings3.RDPPort
- IMsRdpClientAdvancedSettings3.get_RDPPort
- IMsRdpClientAdvancedSettings3.put_RDPPort
- IMsRdpClientAdvancedSettings4.RDPPort
- IMsRdpClientAdvancedSettings4.get_RDPPort
- IMsRdpClientAdvancedSettings4.put_RDPPort
- IMsRdpClientAdvancedSettings5.RDPPort
- IMsRdpClientAdvancedSettings5.get_RDPPort
- IMsRdpClientAdvancedSettings5.put_RDPPort
- IMsRdpClientAdvancedSettings6.RDPPort
- IMsRdpClientAdvancedSettings6.get_RDPPort
- IMsRdpClientAdvancedSettings6.put_RDPPort
- IMsRdpClientAdvancedSettings7.RDPPort
- IMsRdpClientAdvancedSettings7.get_RDPPort
- IMsRdpClientAdvancedSettings7.put_RDPPort
- IMsRdpClientAdvancedSettings8.RDPPort
- IMsRdpClientAdvancedSettings8.get_RDPPort
- IMsRdpClientAdvancedSettings8.put_RDPPort
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c8eafb3521d6338a0a2d469c813ff7ffa447a20
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137562"
---
# <a name="imsrdpclientadvancedsettingsrdpport-property"></a><span data-ttu-id="6e897-120">Свойство Имсрдпклиентадванцедсеттингс:: Рдппорт</span><span class="sxs-lookup"><span data-stu-id="6e897-120">IMsRdpClientAdvancedSettings::RDPPort property</span></span>

<span data-ttu-id="6e897-121">Указывает порт подключения.</span><span class="sxs-lookup"><span data-stu-id="6e897-121">Specifies the connection port.</span></span>

<span data-ttu-id="6e897-122">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="6e897-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e897-123">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6e897-123">Syntax</span></span>


```C++
HRESULT put_RDPPort(
  [in]  LONG rdpPort
);

HRESULT get_RDPPort(
  [out] LONG *prdpPort
);
```



## <a name="property-value"></a><span data-ttu-id="6e897-124">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="6e897-124">Property value</span></span>

<span data-ttu-id="6e897-125">Новый порт.</span><span class="sxs-lookup"><span data-stu-id="6e897-125">The new port.</span></span> <span data-ttu-id="6e897-126">Значение по умолчанию — 3389.</span><span class="sxs-lookup"><span data-stu-id="6e897-126">The default value is 3389.</span></span>

## <a name="error-codes"></a><span data-ttu-id="6e897-127">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="6e897-127">Error codes</span></span>

<span data-ttu-id="6e897-128">При успешном выполнении возвращает значение **\_ ОК** .</span><span class="sxs-lookup"><span data-stu-id="6e897-128">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="6e897-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6e897-129">Remarks</span></span>

<span data-ttu-id="6e897-130">Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="6e897-130">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6e897-131">Требования</span><span class="sxs-lookup"><span data-stu-id="6e897-131">Requirements</span></span>



| <span data-ttu-id="6e897-132">Требование</span><span class="sxs-lookup"><span data-stu-id="6e897-132">Requirement</span></span> | <span data-ttu-id="6e897-133">Значение</span><span class="sxs-lookup"><span data-stu-id="6e897-133">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e897-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6e897-134">Minimum supported client</span></span><br/> | <span data-ttu-id="6e897-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6e897-135">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="6e897-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6e897-136">Minimum supported server</span></span><br/> | <span data-ttu-id="6e897-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6e897-137">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="6e897-138">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="6e897-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="6e897-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6e897-139"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="6e897-140">DLL</span><span class="sxs-lookup"><span data-stu-id="6e897-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6e897-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6e897-141"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="6e897-142">IID</span><span class="sxs-lookup"><span data-stu-id="6e897-142">IID</span></span><br/>                      | <span data-ttu-id="6e897-143">IID \_ имсрдпклиентадванцедсеттингс определен как 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="6e897-143">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6e897-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6e897-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e897-145">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="6e897-145">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="6e897-146">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="6e897-146">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="6e897-147">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="6e897-147">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="6e897-148">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="6e897-148">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="6e897-149">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="6e897-149">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="6e897-150">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="6e897-150">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="6e897-151">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="6e897-151">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="6e897-152">**имсрдпклиентадванцедсеттингс**</span><span class="sxs-lookup"><span data-stu-id="6e897-152">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





