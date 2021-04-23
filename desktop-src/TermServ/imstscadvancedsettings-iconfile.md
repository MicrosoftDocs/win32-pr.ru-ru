---
title: Имстскадванцедсеттингс Иконфиле, свойство
description: Указывает имя файла, содержащего данные значков, которые будут доступны при отображении клиента в полноэкранном режиме.
ms.assetid: 2b6ac2ad-9745-4b80-a415-4840cd8aa8b3
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Иконфиле
- Службы удаленных рабочих столов свойства Иконфиле, интерфейс Имстскадванцедсеттингс
- Службы удаленных рабочих столов интерфейса Имстскадванцедсеттингс, свойство Иконфиле
- Службы удаленных рабочих столов свойства Иконфиле, интерфейс Имсрдпклиентадванцедсеттингс
- Службы удаленных рабочих столов интерфейса Имсрдпклиентадванцедсеттингс, свойство Иконфиле
- Службы удаленных рабочих столов свойства Иконфиле, интерфейс IMsRdpClientAdvancedSettings2
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings2, свойство Иконфиле
- Службы удаленных рабочих столов свойства Иконфиле, интерфейс IMsRdpClientAdvancedSettings3
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings3, свойство Иконфиле
- Службы удаленных рабочих столов свойства Иконфиле, интерфейс IMsRdpClientAdvancedSettings4
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings4, свойство Иконфиле
- Службы удаленных рабочих столов свойства Иконфиле, интерфейс IMsRdpClientAdvancedSettings5
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings5, свойство Иконфиле
- Службы удаленных рабочих столов свойства Иконфиле, интерфейс IMsRdpClientAdvancedSettings6
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings6, свойство Иконфиле
- Службы удаленных рабочих столов свойства Иконфиле, интерфейс IMsRdpClientAdvancedSettings7
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings7, свойство Иконфиле
- Службы удаленных рабочих столов свойства Иконфиле, интерфейс IMsRdpClientAdvancedSettings8
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings8, свойство Иконфиле
topic_type:
- apiref
api_name:
- IMsTscAdvancedSettings.IconFile
- IMsTscAdvancedSettings.put_IconFile
- IMsRdpClientAdvancedSettings.IconFile
- IMsRdpClientAdvancedSettings.put_IconFile
- IMsRdpClientAdvancedSettings2.IconFile
- IMsRdpClientAdvancedSettings2.put_IconFile
- IMsRdpClientAdvancedSettings3.IconFile
- IMsRdpClientAdvancedSettings3.put_IconFile
- IMsRdpClientAdvancedSettings4.IconFile
- IMsRdpClientAdvancedSettings4.put_IconFile
- IMsRdpClientAdvancedSettings5.IconFile
- IMsRdpClientAdvancedSettings5.put_IconFile
- IMsRdpClientAdvancedSettings6.IconFile
- IMsRdpClientAdvancedSettings6.put_IconFile
- IMsRdpClientAdvancedSettings7.IconFile
- IMsRdpClientAdvancedSettings7.put_IconFile
- IMsRdpClientAdvancedSettings8.IconFile
- IMsRdpClientAdvancedSettings8.put_IconFile
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d8f996e70873d5584bb80bbf4f40f71a7deae8f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802279"
---
# <a name="imstscadvancedsettingsiconfile-property"></a><span data-ttu-id="d1432-122">Свойство Имстскадванцедсеттингс:: Иконфиле</span><span class="sxs-lookup"><span data-stu-id="d1432-122">IMsTscAdvancedSettings::IconFile property</span></span>

<span data-ttu-id="d1432-123">Указывает имя файла, содержащего данные значков, которые будут доступны при отображении клиента в полноэкранном режиме.</span><span class="sxs-lookup"><span data-stu-id="d1432-123">Specifies the name of the file containing icon data that will be accessed when displaying the client in full-screen mode.</span></span>

> [!Note]  
> <span data-ttu-id="d1432-124">Это свойство не поддерживается в элементе управления ActiveX (MsRdp. ocx).</span><span class="sxs-lookup"><span data-stu-id="d1432-124">This property is not supported in the ActiveX control (MsRdp.ocx).</span></span> <span data-ttu-id="d1432-125">Она поддерживается в библиотеке MsTscAx.dll, включенной в стандартный клиент (MsTsc.exe).</span><span class="sxs-lookup"><span data-stu-id="d1432-125">It is supported in the MsTscAx.dll library included in the standard client (MsTsc.exe).</span></span>

 

<span data-ttu-id="d1432-126">Это свойство доступно только на запись.</span><span class="sxs-lookup"><span data-stu-id="d1432-126">This property is write-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1432-127">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d1432-127">Syntax</span></span>


```C++
HRESULT put_IconFile(
  [in] BSTR IconFile
);
```



## <a name="property-value"></a><span data-ttu-id="d1432-128">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="d1432-128">Property value</span></span>

<span data-ttu-id="d1432-129">Полный путь к файлу значка или файлу, содержащему данные значков, например DLL.</span><span class="sxs-lookup"><span data-stu-id="d1432-129">The fully qualified path of icon file or a file containing icon data, such as a DLL.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d1432-130">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="d1432-130">Error codes</span></span>

<span data-ttu-id="d1432-131">Возвращает **\_ значение false**.</span><span class="sxs-lookup"><span data-stu-id="d1432-131">Returns **S\_FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="d1432-132">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d1432-132">Remarks</span></span>

<span data-ttu-id="d1432-133">Расширение имени файла значка — ICO.</span><span class="sxs-lookup"><span data-stu-id="d1432-133">The file name extension of an icon file is ".ico".</span></span>

<span data-ttu-id="d1432-134">Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="d1432-134">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d1432-135">Требования</span><span class="sxs-lookup"><span data-stu-id="d1432-135">Requirements</span></span>



| <span data-ttu-id="d1432-136">Требование</span><span class="sxs-lookup"><span data-stu-id="d1432-136">Requirement</span></span> | <span data-ttu-id="d1432-137">Значение</span><span class="sxs-lookup"><span data-stu-id="d1432-137">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1432-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d1432-138">Minimum supported client</span></span><br/> | <span data-ttu-id="d1432-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d1432-139">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="d1432-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d1432-140">Minimum supported server</span></span><br/> | <span data-ttu-id="d1432-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d1432-141">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="d1432-142">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="d1432-142">Type library</span></span><br/>             | <dl> <span data-ttu-id="d1432-143"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d1432-143"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="d1432-144">DLL</span><span class="sxs-lookup"><span data-stu-id="d1432-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d1432-145"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d1432-145"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="d1432-146">IID</span><span class="sxs-lookup"><span data-stu-id="d1432-146">IID</span></span><br/>                      | <span data-ttu-id="d1432-147">IID \_ имстскадванцедсеттингс определен как 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d</span><span class="sxs-lookup"><span data-stu-id="d1432-147">IID\_IMsTscAdvancedSettings is defined as 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d1432-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d1432-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1432-149">**имсрдпклиентадванцедсеттингс**</span><span class="sxs-lookup"><span data-stu-id="d1432-149">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="d1432-150">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="d1432-150">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="d1432-151">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="d1432-151">**IMsRdpClientAdvancedSettings3**</span></span>](imsrdpclientadvancedsettings3.md)
</dt> <dt>

[<span data-ttu-id="d1432-152">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="d1432-152">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="d1432-153">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="d1432-153">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="d1432-154">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="d1432-154">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="d1432-155">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="d1432-155">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="d1432-156">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="d1432-156">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="d1432-157">**имстскадванцедсеттингс**</span><span class="sxs-lookup"><span data-stu-id="d1432-157">**IMsTscAdvancedSettings**</span></span>](imstscadvancedsettings-interface.md)
</dt> </dl>

 

 





