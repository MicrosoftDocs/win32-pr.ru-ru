---
title: Имсрдпклиентадванцедсеттингс Битмапперсистенце, свойство
description: Указывает, следует ли использовать постоянное кэширование битовых карт. Постоянное кэширование может повысить производительность, но требует дополнительного места на диске.
ms.assetid: ffaa9277-9dd7-4b2a-9de5-009b7e8766bc
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Битмапперсистенце
- Службы удаленных рабочих столов свойства Битмапперсистенце, интерфейс Имсрдпклиентадванцедсеттингс
- Службы удаленных рабочих столов интерфейса Имсрдпклиентадванцедсеттингс, свойство Битмапперсистенце
- Службы удаленных рабочих столов свойства Битмапперсистенце, интерфейс IMsRdpClientAdvancedSettings2
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings2, свойство Битмапперсистенце
- Службы удаленных рабочих столов свойства Битмапперсистенце, интерфейс IMsRdpClientAdvancedSettings3
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings3, свойство Битмапперсистенце
- Службы удаленных рабочих столов свойства Битмапперсистенце, интерфейс IMsRdpClientAdvancedSettings4
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings4, свойство Битмапперсистенце
- Службы удаленных рабочих столов свойства Битмапперсистенце, интерфейс IMsRdpClientAdvancedSettings5
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings5, свойство Битмапперсистенце
- Службы удаленных рабочих столов свойства Битмапперсистенце, интерфейс IMsRdpClientAdvancedSettings6
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings6, свойство Битмапперсистенце
- Службы удаленных рабочих столов свойства Битмапперсистенце, интерфейс IMsRdpClientAdvancedSettings7
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings7, свойство Битмапперсистенце
- Службы удаленных рабочих столов свойства Битмапперсистенце, интерфейс IMsRdpClientAdvancedSettings8
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings8, свойство Битмапперсистенце
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.BitmapPersistence
- IMsRdpClientAdvancedSettings.get_BitmapPersistence
- IMsRdpClientAdvancedSettings.put_BitmapPersistence
- IMsRdpClientAdvancedSettings2.BitmapPersistence
- IMsRdpClientAdvancedSettings2.get_BitmapPersistence
- IMsRdpClientAdvancedSettings2.put_BitmapPersistence
- IMsRdpClientAdvancedSettings3.BitmapPersistence
- IMsRdpClientAdvancedSettings3.get_BitmapPersistence
- IMsRdpClientAdvancedSettings3.put_BitmapPersistence
- IMsRdpClientAdvancedSettings4.BitmapPersistence
- IMsRdpClientAdvancedSettings4.get_BitmapPersistence
- IMsRdpClientAdvancedSettings4.put_BitmapPersistence
- IMsRdpClientAdvancedSettings5.BitmapPersistence
- IMsRdpClientAdvancedSettings5.get_BitmapPersistence
- IMsRdpClientAdvancedSettings5.put_BitmapPersistence
- IMsRdpClientAdvancedSettings6.BitmapPersistence
- IMsRdpClientAdvancedSettings6.get_BitmapPersistence
- IMsRdpClientAdvancedSettings6.put_BitmapPersistence
- IMsRdpClientAdvancedSettings7.BitmapPersistence
- IMsRdpClientAdvancedSettings7.get_BitmapPersistence
- IMsRdpClientAdvancedSettings7.put_BitmapPersistence
- IMsRdpClientAdvancedSettings8.BitmapPersistence
- IMsRdpClientAdvancedSettings8.get_BitmapPersistence
- IMsRdpClientAdvancedSettings8.put_BitmapPersistence
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65795b5217c785befe0db6ac529d5760a6211d4d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415197"
---
# <a name="imsrdpclientadvancedsettingsbitmappersistence-property"></a><span data-ttu-id="a5ff3-121">Свойство Имсрдпклиентадванцедсеттингс:: Битмапперсистенце</span><span class="sxs-lookup"><span data-stu-id="a5ff3-121">IMsRdpClientAdvancedSettings::BitmapPersistence property</span></span>

<span data-ttu-id="a5ff3-122">Указывает, следует ли использовать постоянное кэширование битовых карт.</span><span class="sxs-lookup"><span data-stu-id="a5ff3-122">Specifies if persistent bitmap caching should be used.</span></span> <span data-ttu-id="a5ff3-123">Постоянное кэширование может повысить производительность, но требует дополнительного места на диске.</span><span class="sxs-lookup"><span data-stu-id="a5ff3-123">Persistent caching can improve performance but requires additional disk space.</span></span>

<span data-ttu-id="a5ff3-124">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="a5ff3-124">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5ff3-125">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a5ff3-125">Syntax</span></span>


```C++
HRESULT put_BitmapPersistence(
  [in]  LONG bitmapPeristence
);

HRESULT get_BitmapPersistence(
  [out] LONG *pbitmapPeristence
);
```



## <a name="property-value"></a><span data-ttu-id="a5ff3-126">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="a5ff3-126">Property value</span></span>

<span data-ttu-id="a5ff3-127">Задайте для этого параметра значение 0, чтобы отключить кэширование, или ненулевое, чтобы включить кэширование.</span><span class="sxs-lookup"><span data-stu-id="a5ff3-127">Set this parameter to 0 to disable caching or a nonzero value to enable caching.</span></span>

> [!Note]  
> <span data-ttu-id="a5ff3-128">Орфографическая ошибка в имени параметра находится в выпущенной версии элемента управления.</span><span class="sxs-lookup"><span data-stu-id="a5ff3-128">The spelling error in the name of the parameter is in the released version of the control.</span></span>

 

## <a name="error-codes"></a><span data-ttu-id="a5ff3-129">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="a5ff3-129">Error codes</span></span>

<span data-ttu-id="a5ff3-130">При успешном выполнении возвращает значение **\_ ОК** .</span><span class="sxs-lookup"><span data-stu-id="a5ff3-130">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="a5ff3-131">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a5ff3-131">Remarks</span></span>

<span data-ttu-id="a5ff3-132">Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="a5ff3-132">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a5ff3-133">Требования</span><span class="sxs-lookup"><span data-stu-id="a5ff3-133">Requirements</span></span>



| <span data-ttu-id="a5ff3-134">Требование</span><span class="sxs-lookup"><span data-stu-id="a5ff3-134">Requirement</span></span> | <span data-ttu-id="a5ff3-135">Значение</span><span class="sxs-lookup"><span data-stu-id="a5ff3-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5ff3-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a5ff3-136">Minimum supported client</span></span><br/> | <span data-ttu-id="a5ff3-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a5ff3-137">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="a5ff3-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a5ff3-138">Minimum supported server</span></span><br/> | <span data-ttu-id="a5ff3-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a5ff3-139">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="a5ff3-140">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="a5ff3-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="a5ff3-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a5ff3-141"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="a5ff3-142">DLL</span><span class="sxs-lookup"><span data-stu-id="a5ff3-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a5ff3-143"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a5ff3-143"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="a5ff3-144">IID</span><span class="sxs-lookup"><span data-stu-id="a5ff3-144">IID</span></span><br/>                      | <span data-ttu-id="a5ff3-145">IID \_ имсрдпклиентадванцедсеттингс определен как 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="a5ff3-145">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a5ff3-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a5ff3-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5ff3-147">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="a5ff3-147">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="a5ff3-148">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="a5ff3-148">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="a5ff3-149">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="a5ff3-149">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="a5ff3-150">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="a5ff3-150">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="a5ff3-151">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="a5ff3-151">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="a5ff3-152">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="a5ff3-152">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="a5ff3-153">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="a5ff3-153">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="a5ff3-154">**имсрдпклиентадванцедсеттингс**</span><span class="sxs-lookup"><span data-stu-id="a5ff3-154">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





