---
title: Имсрдпклиентадванцедсеттингс Хоткэйфуллскрин, свойство
description: Указывает код виртуального ключа, добавляемый в сочетание клавиш CTRL + ALT для определения замены с помощью сочетания клавиш для переключения в полноэкранный режим.
ms.assetid: 75fda212-ec68-4b68-b7db-2bfcdee7a7de
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Хоткэйфуллскрин
- Службы удаленных рабочих столов свойства Хоткэйфуллскрин, интерфейс Имсрдпклиентадванцедсеттингс
- Службы удаленных рабочих столов интерфейса Имсрдпклиентадванцедсеттингс, свойство Хоткэйфуллскрин
- Службы удаленных рабочих столов свойства Хоткэйфуллскрин, интерфейс IMsRdpClientAdvancedSettings2
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings2, свойство Хоткэйфуллскрин
- Службы удаленных рабочих столов свойства Хоткэйфуллскрин, интерфейс IMsRdpClientAdvancedSettings3
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings3, свойство Хоткэйфуллскрин
- Службы удаленных рабочих столов свойства Хоткэйфуллскрин, интерфейс IMsRdpClientAdvancedSettings4
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings4, свойство Хоткэйфуллскрин
- Службы удаленных рабочих столов свойства Хоткэйфуллскрин, интерфейс IMsRdpClientAdvancedSettings5
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings5, свойство Хоткэйфуллскрин
- Службы удаленных рабочих столов свойства Хоткэйфуллскрин, интерфейс IMsRdpClientAdvancedSettings6
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings6, свойство Хоткэйфуллскрин
- Службы удаленных рабочих столов свойства Хоткэйфуллскрин, интерфейс IMsRdpClientAdvancedSettings7
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings7, свойство Хоткэйфуллскрин
- Службы удаленных рабочих столов свойства Хоткэйфуллскрин, интерфейс IMsRdpClientAdvancedSettings8
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings8, свойство Хоткэйфуллскрин
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.HotKeyFullScreen
- IMsRdpClientAdvancedSettings.get_HotKeyFullScreen
- IMsRdpClientAdvancedSettings.put_HotKeyFullScreen
- IMsRdpClientAdvancedSettings2.HotKeyFullScreen
- IMsRdpClientAdvancedSettings2.get_HotKeyFullScreen
- IMsRdpClientAdvancedSettings2.put_HotKeyFullScreen
- IMsRdpClientAdvancedSettings3.HotKeyFullScreen
- IMsRdpClientAdvancedSettings3.get_HotKeyFullScreen
- IMsRdpClientAdvancedSettings3.put_HotKeyFullScreen
- IMsRdpClientAdvancedSettings4.HotKeyFullScreen
- IMsRdpClientAdvancedSettings4.get_HotKeyFullScreen
- IMsRdpClientAdvancedSettings4.put_HotKeyFullScreen
- IMsRdpClientAdvancedSettings5.HotKeyFullScreen
- IMsRdpClientAdvancedSettings5.get_HotKeyFullScreen
- IMsRdpClientAdvancedSettings5.put_HotKeyFullScreen
- IMsRdpClientAdvancedSettings6.HotKeyFullScreen
- IMsRdpClientAdvancedSettings6.get_HotKeyFullScreen
- IMsRdpClientAdvancedSettings6.put_HotKeyFullScreen
- IMsRdpClientAdvancedSettings7.HotKeyFullScreen
- IMsRdpClientAdvancedSettings7.get_HotKeyFullScreen
- IMsRdpClientAdvancedSettings7.put_HotKeyFullScreen
- IMsRdpClientAdvancedSettings8.HotKeyFullScreen
- IMsRdpClientAdvancedSettings8.get_HotKeyFullScreen
- IMsRdpClientAdvancedSettings8.put_HotKeyFullScreen
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed9c53dd0c6dff9e47b87ea8c8697c20b3613a14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988280"
---
# <a name="imsrdpclientadvancedsettingshotkeyfullscreen-property"></a><span data-ttu-id="1f950-120">Свойство Имсрдпклиентадванцедсеттингс:: Хоткэйфуллскрин</span><span class="sxs-lookup"><span data-stu-id="1f950-120">IMsRdpClientAdvancedSettings::HotKeyFullScreen property</span></span>

<span data-ttu-id="1f950-121">Указывает код виртуального ключа, добавляемый в сочетание клавиш CTRL + ALT для определения замены с помощью сочетания клавиш для переключения в полноэкранный режим.</span><span class="sxs-lookup"><span data-stu-id="1f950-121">Specifies the virtual-key code to add to CTRL+ALT to determine the hotkey replacement for switching to full-screen mode.</span></span>

<span data-ttu-id="1f950-122">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="1f950-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f950-123">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1f950-123">Syntax</span></span>


```C++
HRESULT put_HotKeyFullScreen(
  [in]  LONG hotKeyFullScreen
);

HRESULT get_HotKeyFullScreen(
  [out] LONG *photKeyFullScreen
);
```



## <a name="property-value"></a><span data-ttu-id="1f950-124">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="1f950-124">Property value</span></span>

<span data-ttu-id="1f950-125">Новый код виртуального ключа.</span><span class="sxs-lookup"><span data-stu-id="1f950-125">The new virtual-key code.</span></span> <span data-ttu-id="1f950-126">**VK \_ Значение CANCEL** является значением по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1f950-126">**VK\_CANCEL** is the default value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="1f950-127">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="1f950-127">Error codes</span></span>

<span data-ttu-id="1f950-128">При успешном выполнении возвращает значение **\_ ОК** .</span><span class="sxs-lookup"><span data-stu-id="1f950-128">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="1f950-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1f950-129">Remarks</span></span>

<span data-ttu-id="1f950-130">Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="1f950-130">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1f950-131">Требования</span><span class="sxs-lookup"><span data-stu-id="1f950-131">Requirements</span></span>



| <span data-ttu-id="1f950-132">Требование</span><span class="sxs-lookup"><span data-stu-id="1f950-132">Requirement</span></span> | <span data-ttu-id="1f950-133">Значение</span><span class="sxs-lookup"><span data-stu-id="1f950-133">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f950-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1f950-134">Minimum supported client</span></span><br/> | <span data-ttu-id="1f950-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1f950-135">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="1f950-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1f950-136">Minimum supported server</span></span><br/> | <span data-ttu-id="1f950-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1f950-137">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="1f950-138">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="1f950-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="1f950-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1f950-139"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="1f950-140">DLL</span><span class="sxs-lookup"><span data-stu-id="1f950-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1f950-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1f950-141"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="1f950-142">IID</span><span class="sxs-lookup"><span data-stu-id="1f950-142">IID</span></span><br/>                      | <span data-ttu-id="1f950-143">IID \_ имсрдпклиентадванцедсеттингс определен как 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="1f950-143">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1f950-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1f950-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f950-145">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="1f950-145">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="1f950-146">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="1f950-146">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="1f950-147">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="1f950-147">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="1f950-148">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="1f950-148">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="1f950-149">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="1f950-149">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="1f950-150">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="1f950-150">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="1f950-151">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="1f950-151">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="1f950-152">**имсрдпклиентадванцедсеттингс**</span><span class="sxs-lookup"><span data-stu-id="1f950-152">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





