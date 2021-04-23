---
title: Имсрдпклиентадванцедсеттингс Акцелераторпасссраугх, свойство
description: Указывает, следует ли передавать сочетания клавиш на сервер.
ms.assetid: ad0053bc-e3a9-4cd5-a409-fab3e24ffffa
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Акцелераторпасссраугх
- Службы удаленных рабочих столов свойства Акцелераторпасссраугх, интерфейс Имсрдпклиентадванцедсеттингс
- Службы удаленных рабочих столов интерфейса Имсрдпклиентадванцедсеттингс, свойство Акцелераторпасссраугх
- Службы удаленных рабочих столов свойства Акцелераторпасссраугх, интерфейс IMsRdpClientAdvancedSettings2
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings2, свойство Акцелераторпасссраугх
- Службы удаленных рабочих столов свойства Акцелераторпасссраугх, интерфейс IMsRdpClientAdvancedSettings3
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings3, свойство Акцелераторпасссраугх
- Службы удаленных рабочих столов свойства Акцелераторпасссраугх, интерфейс IMsRdpClientAdvancedSettings4
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings4, свойство Акцелераторпасссраугх
- Службы удаленных рабочих столов свойства Акцелераторпасссраугх, интерфейс IMsRdpClientAdvancedSettings5
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings5, свойство Акцелераторпасссраугх
- Службы удаленных рабочих столов свойства Акцелераторпасссраугх, интерфейс IMsRdpClientAdvancedSettings6
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings6, свойство Акцелераторпасссраугх
- Службы удаленных рабочих столов свойства Акцелераторпасссраугх, интерфейс IMsRdpClientAdvancedSettings7
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings7, свойство Акцелераторпасссраугх
- Службы удаленных рабочих столов свойства Акцелераторпасссраугх, интерфейс IMsRdpClientAdvancedSettings8
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings8, свойство Акцелераторпасссраугх
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.AcceleratorPassthrough
- IMsRdpClientAdvancedSettings.get_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings.put_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings2.AcceleratorPassthrough
- IMsRdpClientAdvancedSettings2.get_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings2.put_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings3.AcceleratorPassthrough
- IMsRdpClientAdvancedSettings3.get_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings3.put_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings4.AcceleratorPassthrough
- IMsRdpClientAdvancedSettings4.get_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings4.put_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings5.AcceleratorPassthrough
- IMsRdpClientAdvancedSettings5.get_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings5.put_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings6.AcceleratorPassthrough
- IMsRdpClientAdvancedSettings6.get_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings6.put_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings7.AcceleratorPassthrough
- IMsRdpClientAdvancedSettings7.get_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings7.put_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings8.AcceleratorPassthrough
- IMsRdpClientAdvancedSettings8.get_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings8.put_AcceleratorPassthrough
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c252c5c0477f331b66cf65b93ed2cab844fb88e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672581"
---
# <a name="imsrdpclientadvancedsettingsacceleratorpassthrough-property"></a><span data-ttu-id="74683-120">Свойство Имсрдпклиентадванцедсеттингс:: Акцелераторпасссраугх</span><span class="sxs-lookup"><span data-stu-id="74683-120">IMsRdpClientAdvancedSettings::AcceleratorPassthrough property</span></span>

<span data-ttu-id="74683-121">Указывает, следует ли передавать сочетания клавиш на сервер.</span><span class="sxs-lookup"><span data-stu-id="74683-121">Specifies if keyboard accelerators should be passed to the server.</span></span>

<span data-ttu-id="74683-122">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="74683-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="74683-123">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="74683-123">Syntax</span></span>


```C++
HRESULT put_AcceleratorPassthrough(
  [in]  LONG acceleratorPassthrough
);

HRESULT get_AcceleratorPassthrough(
  [out] LONG *pacceleratorPassthrough
);
```



## <a name="property-value"></a><span data-ttu-id="74683-124">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="74683-124">Property value</span></span>

<span data-ttu-id="74683-125">Задайте для этого параметра значение 0, чтобы отключить функцию, или ненулевое, чтобы включить эту функцию.</span><span class="sxs-lookup"><span data-stu-id="74683-125">Set this parameter to 0 to disable the feature or a nonzero value to enable the feature.</span></span> <span data-ttu-id="74683-126">Значение по умолчанию равно ненулевому значению.</span><span class="sxs-lookup"><span data-stu-id="74683-126">The default is a nonzero value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="74683-127">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="74683-127">Error codes</span></span>

<span data-ttu-id="74683-128">При успешном выполнении возвращает значение **\_ ОК** .</span><span class="sxs-lookup"><span data-stu-id="74683-128">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="74683-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="74683-129">Remarks</span></span>

<span data-ttu-id="74683-130">Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="74683-130">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="74683-131">Требования</span><span class="sxs-lookup"><span data-stu-id="74683-131">Requirements</span></span>



| <span data-ttu-id="74683-132">Требование</span><span class="sxs-lookup"><span data-stu-id="74683-132">Requirement</span></span> | <span data-ttu-id="74683-133">Значение</span><span class="sxs-lookup"><span data-stu-id="74683-133">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74683-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="74683-134">Minimum supported client</span></span><br/> | <span data-ttu-id="74683-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="74683-135">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="74683-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="74683-136">Minimum supported server</span></span><br/> | <span data-ttu-id="74683-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="74683-137">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="74683-138">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="74683-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="74683-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="74683-139"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="74683-140">DLL</span><span class="sxs-lookup"><span data-stu-id="74683-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="74683-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="74683-141"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="74683-142">IID</span><span class="sxs-lookup"><span data-stu-id="74683-142">IID</span></span><br/>                      | <span data-ttu-id="74683-143">IID \_ имсрдпклиентадванцедсеттингс определен как 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="74683-143">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="74683-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="74683-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74683-145">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="74683-145">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="74683-146">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="74683-146">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="74683-147">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="74683-147">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="74683-148">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="74683-148">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="74683-149">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="74683-149">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="74683-150">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="74683-150">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="74683-151">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="74683-151">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="74683-152">**имсрдпклиентадванцедсеттингс**</span><span class="sxs-lookup"><span data-stu-id="74683-152">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





