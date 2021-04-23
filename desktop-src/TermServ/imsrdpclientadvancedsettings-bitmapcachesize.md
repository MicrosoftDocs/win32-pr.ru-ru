---
title: Имсрдпклиентадванцедсеттингс Битмапкачесизе, свойство
description: Размер файла кэша растрового изображения в килобайтах, используемый для точечных рисунков размером 8 бит на пиксель.
ms.assetid: a2a4b739-0fa3-4a76-87ae-3cba913b7703
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Битмапкачесизе
- Службы удаленных рабочих столов свойства Битмапкачесизе, интерфейс Имсрдпклиентадванцедсеттингс
- Службы удаленных рабочих столов интерфейса Имсрдпклиентадванцедсеттингс, свойство Битмапкачесизе
- Службы удаленных рабочих столов свойства Битмапкачесизе, интерфейс IMsRdpClientAdvancedSettings2
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings2, свойство Битмапкачесизе
- Службы удаленных рабочих столов свойства Битмапкачесизе, интерфейс IMsRdpClientAdvancedSettings3
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings3, свойство Битмапкачесизе
- Службы удаленных рабочих столов свойства Битмапкачесизе, интерфейс IMsRdpClientAdvancedSettings4
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings4, свойство Битмапкачесизе
- Службы удаленных рабочих столов свойства Битмапкачесизе, интерфейс IMsRdpClientAdvancedSettings5
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings5, свойство Битмапкачесизе
- Службы удаленных рабочих столов свойства Битмапкачесизе, интерфейс IMsRdpClientAdvancedSettings6
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings6, свойство Битмапкачесизе
- Службы удаленных рабочих столов свойства Битмапкачесизе, интерфейс IMsRdpClientAdvancedSettings7
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings7, свойство Битмапкачесизе
- Службы удаленных рабочих столов свойства Битмапкачесизе, интерфейс IMsRdpClientAdvancedSettings8
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings8, свойство Битмапкачесизе
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.BitmapCacheSize
- IMsRdpClientAdvancedSettings.get_BitmapCacheSize
- IMsRdpClientAdvancedSettings.put_BitmapCacheSize
- IMsRdpClientAdvancedSettings2.BitmapCacheSize
- IMsRdpClientAdvancedSettings2.get_BitmapCacheSize
- IMsRdpClientAdvancedSettings2.put_BitmapCacheSize
- IMsRdpClientAdvancedSettings3.BitmapCacheSize
- IMsRdpClientAdvancedSettings3.get_BitmapCacheSize
- IMsRdpClientAdvancedSettings3.put_BitmapCacheSize
- IMsRdpClientAdvancedSettings4.BitmapCacheSize
- IMsRdpClientAdvancedSettings4.get_BitmapCacheSize
- IMsRdpClientAdvancedSettings4.put_BitmapCacheSize
- IMsRdpClientAdvancedSettings5.BitmapCacheSize
- IMsRdpClientAdvancedSettings5.get_BitmapCacheSize
- IMsRdpClientAdvancedSettings5.put_BitmapCacheSize
- IMsRdpClientAdvancedSettings6.BitmapCacheSize
- IMsRdpClientAdvancedSettings6.get_BitmapCacheSize
- IMsRdpClientAdvancedSettings6.put_BitmapCacheSize
- IMsRdpClientAdvancedSettings7.BitmapCacheSize
- IMsRdpClientAdvancedSettings7.get_BitmapCacheSize
- IMsRdpClientAdvancedSettings7.put_BitmapCacheSize
- IMsRdpClientAdvancedSettings8.BitmapCacheSize
- IMsRdpClientAdvancedSettings8.get_BitmapCacheSize
- IMsRdpClientAdvancedSettings8.put_BitmapCacheSize
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a38376bb0b06bd4efea36d3c4cad4e4aec0f35b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415200"
---
# <a name="imsrdpclientadvancedsettingsbitmapcachesize-property"></a><span data-ttu-id="19524-120">Свойство Имсрдпклиентадванцедсеттингс:: Битмапкачесизе</span><span class="sxs-lookup"><span data-stu-id="19524-120">IMsRdpClientAdvancedSettings::BitmapCacheSize property</span></span>

<span data-ttu-id="19524-121">Размер файла кэша растрового изображения в килобайтах, используемый для точечных рисунков размером 8 бит на пиксель.</span><span class="sxs-lookup"><span data-stu-id="19524-121">The size, in kilobytes, of the bitmap cache file used for 8-bits-per-pixel bitmaps.</span></span>

<span data-ttu-id="19524-122">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="19524-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="19524-123">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="19524-123">Syntax</span></span>


```C++
HRESULT put_BitmapCacheSize(
  [in]  LONG bitmapCacheSize
);

HRESULT get_BitmapCacheSize(
  [out] LONG *pbitmapCacheSize
);
```



## <a name="property-value"></a><span data-ttu-id="19524-124">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="19524-124">Property value</span></span>

<span data-ttu-id="19524-125">Новый размер кэша в килобайтах.</span><span class="sxs-lookup"><span data-stu-id="19524-125">The new cache size, in kilobytes.</span></span> <span data-ttu-id="19524-126">Допустимые числовые значения: от 1 до 32 включительно.</span><span class="sxs-lookup"><span data-stu-id="19524-126">The valid numeric values are 1 to 32 inclusive.</span></span>

## <a name="error-codes"></a><span data-ttu-id="19524-127">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="19524-127">Error codes</span></span>

<span data-ttu-id="19524-128">При успешном выполнении возвращает значение **\_ ОК** .</span><span class="sxs-lookup"><span data-stu-id="19524-128">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="19524-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="19524-129">Remarks</span></span>

<span data-ttu-id="19524-130">Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="19524-130">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="19524-131">Требования</span><span class="sxs-lookup"><span data-stu-id="19524-131">Requirements</span></span>



| <span data-ttu-id="19524-132">Требование</span><span class="sxs-lookup"><span data-stu-id="19524-132">Requirement</span></span> | <span data-ttu-id="19524-133">Значение</span><span class="sxs-lookup"><span data-stu-id="19524-133">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19524-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="19524-134">Minimum supported client</span></span><br/> | <span data-ttu-id="19524-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="19524-135">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="19524-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="19524-136">Minimum supported server</span></span><br/> | <span data-ttu-id="19524-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="19524-137">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="19524-138">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="19524-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="19524-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="19524-139"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="19524-140">DLL</span><span class="sxs-lookup"><span data-stu-id="19524-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="19524-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="19524-141"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="19524-142">IID</span><span class="sxs-lookup"><span data-stu-id="19524-142">IID</span></span><br/>                      | <span data-ttu-id="19524-143">IID \_ имсрдпклиентадванцедсеттингс определен как 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="19524-143">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="19524-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="19524-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19524-145">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="19524-145">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="19524-146">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="19524-146">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="19524-147">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="19524-147">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="19524-148">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="19524-148">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="19524-149">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="19524-149">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="19524-150">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="19524-150">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="19524-151">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="19524-151">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="19524-152">**имсрдпклиентадванцедсеттингс**</span><span class="sxs-lookup"><span data-stu-id="19524-152">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





