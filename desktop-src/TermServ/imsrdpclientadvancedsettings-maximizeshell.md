---
title: Имсрдпклиентадванцедсеттингс Максимизешелл, свойство
description: Указывает, следует ли развернуть программы, запускаемые с помощью свойства Стартпрограм.
ms.assetid: d8c194b6-04ef-495f-a763-7e18064230e6
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Максимизешелл
- Службы удаленных рабочих столов свойства Максимизешелл, интерфейс Имсрдпклиентадванцедсеттингс
- Службы удаленных рабочих столов интерфейса Имсрдпклиентадванцедсеттингс, свойство Максимизешелл
- Службы удаленных рабочих столов свойства Максимизешелл, интерфейс IMsRdpClientAdvancedSettings2
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings2, свойство Максимизешелл
- Службы удаленных рабочих столов свойства Максимизешелл, интерфейс IMsRdpClientAdvancedSettings3
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings3, свойство Максимизешелл
- Службы удаленных рабочих столов свойства Максимизешелл, интерфейс IMsRdpClientAdvancedSettings4
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings4, свойство Максимизешелл
- Службы удаленных рабочих столов свойства Максимизешелл, интерфейс IMsRdpClientAdvancedSettings5
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings5, свойство Максимизешелл
- Службы удаленных рабочих столов свойства Максимизешелл, интерфейс IMsRdpClientAdvancedSettings6
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings6, свойство Максимизешелл
- Службы удаленных рабочих столов свойства Максимизешелл, интерфейс IMsRdpClientAdvancedSettings7
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings7, свойство Максимизешелл
- Службы удаленных рабочих столов свойства Максимизешелл, интерфейс IMsRdpClientAdvancedSettings8
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings8, свойство Максимизешелл
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.MaximizeShell
- IMsRdpClientAdvancedSettings.get_MaximizeShell
- IMsRdpClientAdvancedSettings.put_MaximizeShell
- IMsRdpClientAdvancedSettings2.MaximizeShell
- IMsRdpClientAdvancedSettings2.get_MaximizeShell
- IMsRdpClientAdvancedSettings2.put_MaximizeShell
- IMsRdpClientAdvancedSettings3.MaximizeShell
- IMsRdpClientAdvancedSettings3.get_MaximizeShell
- IMsRdpClientAdvancedSettings3.put_MaximizeShell
- IMsRdpClientAdvancedSettings4.MaximizeShell
- IMsRdpClientAdvancedSettings4.get_MaximizeShell
- IMsRdpClientAdvancedSettings4.put_MaximizeShell
- IMsRdpClientAdvancedSettings5.MaximizeShell
- IMsRdpClientAdvancedSettings5.get_MaximizeShell
- IMsRdpClientAdvancedSettings5.put_MaximizeShell
- IMsRdpClientAdvancedSettings6.MaximizeShell
- IMsRdpClientAdvancedSettings6.get_MaximizeShell
- IMsRdpClientAdvancedSettings6.put_MaximizeShell
- IMsRdpClientAdvancedSettings7.MaximizeShell
- IMsRdpClientAdvancedSettings7.get_MaximizeShell
- IMsRdpClientAdvancedSettings7.put_MaximizeShell
- IMsRdpClientAdvancedSettings8.MaximizeShell
- IMsRdpClientAdvancedSettings8.get_MaximizeShell
- IMsRdpClientAdvancedSettings8.put_MaximizeShell
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02c172dd71fcf57f2028f6ba64c93ceaeec2ffb2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988408"
---
# <a name="imsrdpclientadvancedsettingsmaximizeshell-property"></a><span data-ttu-id="a8eb5-120">Свойство Имсрдпклиентадванцедсеттингс:: Максимизешелл</span><span class="sxs-lookup"><span data-stu-id="a8eb5-120">IMsRdpClientAdvancedSettings::MaximizeShell property</span></span>

<span data-ttu-id="a8eb5-121">Указывает, следует ли развернуть программы, запускаемые с помощью свойства [**стартпрограм**](imstscsecuredsettings-startprogram.md) .</span><span class="sxs-lookup"><span data-stu-id="a8eb5-121">Specifies if programs launched with the [**StartProgram**](imstscsecuredsettings-startprogram.md) property should be maximized.</span></span>

<span data-ttu-id="a8eb5-122">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="a8eb5-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8eb5-123">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a8eb5-123">Syntax</span></span>


```C++
HRESULT put_MaximizeShell(
  [in]  LONG maximizeShell
);

HRESULT get_MaximizeShell(
  [out] LONG *pmaximizeShell
);
```



## <a name="property-value"></a><span data-ttu-id="a8eb5-124">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="a8eb5-124">Property value</span></span>

<span data-ttu-id="a8eb5-125">Задайте для этого параметра значение 0, чтобы отключить функцию, или ненулевое, чтобы включить эту функцию.</span><span class="sxs-lookup"><span data-stu-id="a8eb5-125">Set this parameter to 0 to disable the feature or a nonzero value to enable the feature.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a8eb5-126">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="a8eb5-126">Error codes</span></span>

<span data-ttu-id="a8eb5-127">При успешном выполнении возвращает значение **\_ ОК** .</span><span class="sxs-lookup"><span data-stu-id="a8eb5-127">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="a8eb5-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a8eb5-128">Remarks</span></span>

<span data-ttu-id="a8eb5-129">Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="a8eb5-129">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a8eb5-130">Требования</span><span class="sxs-lookup"><span data-stu-id="a8eb5-130">Requirements</span></span>



| <span data-ttu-id="a8eb5-131">Требование</span><span class="sxs-lookup"><span data-stu-id="a8eb5-131">Requirement</span></span> | <span data-ttu-id="a8eb5-132">Значение</span><span class="sxs-lookup"><span data-stu-id="a8eb5-132">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8eb5-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a8eb5-133">Minimum supported client</span></span><br/> | <span data-ttu-id="a8eb5-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a8eb5-134">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="a8eb5-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a8eb5-135">Minimum supported server</span></span><br/> | <span data-ttu-id="a8eb5-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a8eb5-136">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="a8eb5-137">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="a8eb5-137">Type library</span></span><br/>             | <dl> <span data-ttu-id="a8eb5-138"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a8eb5-138"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="a8eb5-139">DLL</span><span class="sxs-lookup"><span data-stu-id="a8eb5-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a8eb5-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a8eb5-140"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="a8eb5-141">IID</span><span class="sxs-lookup"><span data-stu-id="a8eb5-141">IID</span></span><br/>                      | <span data-ttu-id="a8eb5-142">IID \_ имсрдпклиентадванцедсеттингс определен как 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="a8eb5-142">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a8eb5-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a8eb5-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8eb5-144">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="a8eb5-144">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="a8eb5-145">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="a8eb5-145">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="a8eb5-146">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="a8eb5-146">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="a8eb5-147">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="a8eb5-147">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="a8eb5-148">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="a8eb5-148">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="a8eb5-149">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="a8eb5-149">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="a8eb5-150">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="a8eb5-150">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="a8eb5-151">**имсрдпклиентадванцедсеттингс**</span><span class="sxs-lookup"><span data-stu-id="a8eb5-151">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





