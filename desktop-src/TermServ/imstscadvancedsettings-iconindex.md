---
title: Имстскадванцедсеттингс Икониндекс, свойство
description: Задает индекс значка в текущем файле значка.
ms.assetid: c29ae1a7-9c54-4e56-bb69-4e929e8a4e5c
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Икониндекс
- Службы удаленных рабочих столов свойства Икониндекс, интерфейс Имстскадванцедсеттингс
- Службы удаленных рабочих столов интерфейса Имстскадванцедсеттингс, свойство Икониндекс
- Службы удаленных рабочих столов свойства Икониндекс, интерфейс Имсрдпклиентадванцедсеттингс
- Службы удаленных рабочих столов интерфейса Имсрдпклиентадванцедсеттингс, свойство Икониндекс
- Службы удаленных рабочих столов свойства Икониндекс, интерфейс IMsRdpClientAdvancedSettings2
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings2, свойство Икониндекс
- Службы удаленных рабочих столов свойства Икониндекс, интерфейс IMsRdpClientAdvancedSettings3
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings3, свойство Икониндекс
- Службы удаленных рабочих столов свойства Икониндекс, интерфейс IMsRdpClientAdvancedSettings4
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings4, свойство Икониндекс
- Службы удаленных рабочих столов свойства Икониндекс, интерфейс IMsRdpClientAdvancedSettings5
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings5, свойство Икониндекс
- Службы удаленных рабочих столов свойства Икониндекс, интерфейс IMsRdpClientAdvancedSettings6
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings6, свойство Икониндекс
- Службы удаленных рабочих столов свойства Икониндекс, интерфейс IMsRdpClientAdvancedSettings7
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings7, свойство Икониндекс
- Службы удаленных рабочих столов свойства Икониндекс, интерфейс IMsRdpClientAdvancedSettings8
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings8, свойство Икониндекс
topic_type:
- apiref
api_name:
- IMsTscAdvancedSettings.IconIndex
- IMsTscAdvancedSettings.put_IconIndex
- IMsRdpClientAdvancedSettings.IconIndex
- IMsRdpClientAdvancedSettings.put_IconIndex
- IMsRdpClientAdvancedSettings2.IconIndex
- IMsRdpClientAdvancedSettings2.put_IconIndex
- IMsRdpClientAdvancedSettings3.IconIndex
- IMsRdpClientAdvancedSettings3.put_IconIndex
- IMsRdpClientAdvancedSettings4.IconIndex
- IMsRdpClientAdvancedSettings4.put_IconIndex
- IMsRdpClientAdvancedSettings5.IconIndex
- IMsRdpClientAdvancedSettings5.put_IconIndex
- IMsRdpClientAdvancedSettings6.IconIndex
- IMsRdpClientAdvancedSettings6.put_IconIndex
- IMsRdpClientAdvancedSettings7.IconIndex
- IMsRdpClientAdvancedSettings7.put_IconIndex
- IMsRdpClientAdvancedSettings8.IconIndex
- IMsRdpClientAdvancedSettings8.put_IconIndex
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3be56eab5dbe7f03155c6082e4e70fc4bd439253
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534136"
---
# <a name="imstscadvancedsettingsiconindex-property"></a><span data-ttu-id="bd674-122">Свойство Имстскадванцедсеттингс:: Икониндекс</span><span class="sxs-lookup"><span data-stu-id="bd674-122">IMsTscAdvancedSettings::IconIndex property</span></span>

<span data-ttu-id="bd674-123">Задает индекс значка в текущем файле значка.</span><span class="sxs-lookup"><span data-stu-id="bd674-123">Specifies the index of the icon within the current icon file.</span></span>

> [!Note]  
> <span data-ttu-id="bd674-124">Это свойство не поддерживается в элементе управления ActiveX (MsRdp. ocx).</span><span class="sxs-lookup"><span data-stu-id="bd674-124">This property is not supported in the ActiveX control (MsRdp.ocx).</span></span> <span data-ttu-id="bd674-125">Она поддерживается в библиотеке MsTscAx.dll, включенной в стандартный клиент (MsTsc.exe).</span><span class="sxs-lookup"><span data-stu-id="bd674-125">It is supported in the MsTscAx.dll library included in the standard client (MsTsc.exe).</span></span>

 

<span data-ttu-id="bd674-126">Это свойство доступно только на запись.</span><span class="sxs-lookup"><span data-stu-id="bd674-126">This property is write-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd674-127">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bd674-127">Syntax</span></span>


```C++
HRESULT put_IconIndex(
  [in] LONG IconIndex
);
```



## <a name="property-value"></a><span data-ttu-id="bd674-128">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="bd674-128">Property value</span></span>

<span data-ttu-id="bd674-129">Индекс значка.</span><span class="sxs-lookup"><span data-stu-id="bd674-129">The index of the icon.</span></span>

## <a name="error-codes"></a><span data-ttu-id="bd674-130">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="bd674-130">Error codes</span></span>

<span data-ttu-id="bd674-131">Возвращает **\_ значение false**.</span><span class="sxs-lookup"><span data-stu-id="bd674-131">Returns **S\_FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="bd674-132">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bd674-132">Remarks</span></span>

<span data-ttu-id="bd674-133">Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="bd674-133">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bd674-134">Требования</span><span class="sxs-lookup"><span data-stu-id="bd674-134">Requirements</span></span>



| <span data-ttu-id="bd674-135">Требование</span><span class="sxs-lookup"><span data-stu-id="bd674-135">Requirement</span></span> | <span data-ttu-id="bd674-136">Значение</span><span class="sxs-lookup"><span data-stu-id="bd674-136">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd674-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bd674-137">Minimum supported client</span></span><br/> | <span data-ttu-id="bd674-138">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bd674-138">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="bd674-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bd674-139">Minimum supported server</span></span><br/> | <span data-ttu-id="bd674-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bd674-140">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="bd674-141">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="bd674-141">Type library</span></span><br/>             | <dl> <span data-ttu-id="bd674-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bd674-142"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="bd674-143">DLL</span><span class="sxs-lookup"><span data-stu-id="bd674-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bd674-144"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bd674-144"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="bd674-145">IID</span><span class="sxs-lookup"><span data-stu-id="bd674-145">IID</span></span><br/>                      | <span data-ttu-id="bd674-146">IID \_ имстскадванцедсеттингс определен как 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d</span><span class="sxs-lookup"><span data-stu-id="bd674-146">IID\_IMsTscAdvancedSettings is defined as 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bd674-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bd674-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd674-148">**имсрдпклиентадванцедсеттингс**</span><span class="sxs-lookup"><span data-stu-id="bd674-148">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="bd674-149">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="bd674-149">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="bd674-150">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="bd674-150">**IMsRdpClientAdvancedSettings3**</span></span>](imsrdpclientadvancedsettings3.md)
</dt> <dt>

[<span data-ttu-id="bd674-151">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="bd674-151">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="bd674-152">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="bd674-152">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="bd674-153">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="bd674-153">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="bd674-154">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="bd674-154">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="bd674-155">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="bd674-155">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="bd674-156">**имстскадванцедсеттингс**</span><span class="sxs-lookup"><span data-stu-id="bd674-156">**IMsTscAdvancedSettings**</span></span>](imstscadvancedsettings-interface.md)
</dt> </dl>

 

 





