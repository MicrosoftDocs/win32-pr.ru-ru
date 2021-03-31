---
title: Имсрдпклиентадванцедсеттингс Дисаблектрлалтдел, свойство
description: Указывает, должен ли отображаться начальный экран пояснения в Winlogon.
ms.assetid: 79212472-105f-4e92-8065-f97819637d02
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Дисаблектрлалтдел
- Службы удаленных рабочих столов свойства Дисаблектрлалтдел, интерфейс Имсрдпклиентадванцедсеттингс
- Службы удаленных рабочих столов интерфейса Имсрдпклиентадванцедсеттингс, свойство Дисаблектрлалтдел
- Службы удаленных рабочих столов свойства Дисаблектрлалтдел, интерфейс IMsRdpClientAdvancedSettings2
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings2, свойство Дисаблектрлалтдел
- Службы удаленных рабочих столов свойства Дисаблектрлалтдел, интерфейс IMsRdpClientAdvancedSettings3
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings3, свойство Дисаблектрлалтдел
- Службы удаленных рабочих столов свойства Дисаблектрлалтдел, интерфейс IMsRdpClientAdvancedSettings4
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings4, свойство Дисаблектрлалтдел
- Службы удаленных рабочих столов свойства Дисаблектрлалтдел, интерфейс IMsRdpClientAdvancedSettings5
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings5, свойство Дисаблектрлалтдел
- Службы удаленных рабочих столов свойства Дисаблектрлалтдел, интерфейс IMsRdpClientAdvancedSettings6
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings6, свойство Дисаблектрлалтдел
- Службы удаленных рабочих столов свойства Дисаблектрлалтдел, интерфейс IMsRdpClientAdvancedSettings7
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings7, свойство Дисаблектрлалтдел
- Службы удаленных рабочих столов свойства Дисаблектрлалтдел, интерфейс IMsRdpClientAdvancedSettings8
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings8, свойство Дисаблектрлалтдел
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.DisableCtrlAltDel
- IMsRdpClientAdvancedSettings.get_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings.put_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings2.DisableCtrlAltDel
- IMsRdpClientAdvancedSettings2.get_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings2.put_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings3.DisableCtrlAltDel
- IMsRdpClientAdvancedSettings3.get_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings3.put_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings4.DisableCtrlAltDel
- IMsRdpClientAdvancedSettings4.get_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings4.put_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings5.DisableCtrlAltDel
- IMsRdpClientAdvancedSettings5.get_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings5.put_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings6.DisableCtrlAltDel
- IMsRdpClientAdvancedSettings6.get_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings6.put_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings7.DisableCtrlAltDel
- IMsRdpClientAdvancedSettings7.get_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings7.put_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings8.DisableCtrlAltDel
- IMsRdpClientAdvancedSettings8.get_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings8.put_DisableCtrlAltDel
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3380aa78c16c7e937637cc727fe81f054649f929
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801570"
---
# <a name="imsrdpclientadvancedsettingsdisablectrlaltdel-property"></a><span data-ttu-id="5e4eb-120">Имсрдпклиентадванцедсеттингс: свойство Исаблектрлалтдел:D</span><span class="sxs-lookup"><span data-stu-id="5e4eb-120">IMsRdpClientAdvancedSettings::DisableCtrlAltDel property</span></span>

<span data-ttu-id="5e4eb-121">Указывает, должен ли отображаться начальный экран пояснения в Winlogon.</span><span class="sxs-lookup"><span data-stu-id="5e4eb-121">Specifies if the initial explanatory screen in Winlogon should display.</span></span>

<span data-ttu-id="5e4eb-122">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="5e4eb-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e4eb-123">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5e4eb-123">Syntax</span></span>


```C++
HRESULT put_DisableCtrlAltDel(
  [in]  LONG disableCtrlAltDel
);

HRESULT get_DisableCtrlAltDel(
  [out] LONG *pdisableCtrlAltDel
);
```



## <a name="property-value"></a><span data-ttu-id="5e4eb-124">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="5e4eb-124">Property value</span></span>

<span data-ttu-id="5e4eb-125">Задайте для этого параметра значение 0, чтобы отключить функцию, или ненулевое, чтобы включить эту функцию.</span><span class="sxs-lookup"><span data-stu-id="5e4eb-125">Set this parameter to 0 to disable the feature or a nonzero value to enable the feature.</span></span>

## <a name="error-codes"></a><span data-ttu-id="5e4eb-126">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="5e4eb-126">Error codes</span></span>

<span data-ttu-id="5e4eb-127">При успешном выполнении возвращает значение **\_ ОК** .</span><span class="sxs-lookup"><span data-stu-id="5e4eb-127">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="5e4eb-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5e4eb-128">Remarks</span></span>

<span data-ttu-id="5e4eb-129">Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="5e4eb-129">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5e4eb-130">Требования</span><span class="sxs-lookup"><span data-stu-id="5e4eb-130">Requirements</span></span>



| <span data-ttu-id="5e4eb-131">Требование</span><span class="sxs-lookup"><span data-stu-id="5e4eb-131">Requirement</span></span> | <span data-ttu-id="5e4eb-132">Значение</span><span class="sxs-lookup"><span data-stu-id="5e4eb-132">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e4eb-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5e4eb-133">Minimum supported client</span></span><br/> | <span data-ttu-id="5e4eb-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5e4eb-134">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="5e4eb-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5e4eb-135">Minimum supported server</span></span><br/> | <span data-ttu-id="5e4eb-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5e4eb-136">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="5e4eb-137">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="5e4eb-137">Type library</span></span><br/>             | <dl> <span data-ttu-id="5e4eb-138"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5e4eb-138"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="5e4eb-139">DLL</span><span class="sxs-lookup"><span data-stu-id="5e4eb-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5e4eb-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5e4eb-140"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="5e4eb-141">IID</span><span class="sxs-lookup"><span data-stu-id="5e4eb-141">IID</span></span><br/>                      | <span data-ttu-id="5e4eb-142">IID \_ имсрдпклиентадванцедсеттингс определен как 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="5e4eb-142">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5e4eb-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5e4eb-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e4eb-144">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="5e4eb-144">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="5e4eb-145">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="5e4eb-145">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="5e4eb-146">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="5e4eb-146">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="5e4eb-147">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="5e4eb-147">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="5e4eb-148">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="5e4eb-148">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="5e4eb-149">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="5e4eb-149">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="5e4eb-150">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="5e4eb-150">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="5e4eb-151">**имсрдпклиентадванцедсеттингс**</span><span class="sxs-lookup"><span data-stu-id="5e4eb-151">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





