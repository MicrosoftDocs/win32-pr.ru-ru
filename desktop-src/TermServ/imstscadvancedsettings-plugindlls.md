---
title: Имстскадванцедсеттингс Плугиндллс, свойство
description: Указывает имена клиентских DLL-библиотек виртуальных каналов для загрузки.
ms.assetid: 4b248fb8-200a-4ce0-8c8e-ce1692a80d88
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Плугиндллс
- Службы удаленных рабочих столов свойства Плугиндллс, интерфейс Имстскадванцедсеттингс
- Службы удаленных рабочих столов интерфейса Имстскадванцедсеттингс, свойство Плугиндллс
- Службы удаленных рабочих столов свойства Плугиндллс, интерфейс Имсрдпклиентадванцедсеттингс
- Службы удаленных рабочих столов интерфейса Имсрдпклиентадванцедсеттингс, свойство Плугиндллс
- Службы удаленных рабочих столов свойства Плугиндллс, интерфейс IMsRdpClientAdvancedSettings2
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings2, свойство Плугиндллс
- Службы удаленных рабочих столов свойства Плугиндллс, интерфейс IMsRdpClientAdvancedSettings3
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings3, свойство Плугиндллс
- Службы удаленных рабочих столов свойства Плугиндллс, интерфейс IMsRdpClientAdvancedSettings4
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings4, свойство Плугиндллс
- Службы удаленных рабочих столов свойства Плугиндллс, интерфейс IMsRdpClientAdvancedSettings5
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings5, свойство Плугиндллс
- Службы удаленных рабочих столов свойства Плугиндллс, интерфейс IMsRdpClientAdvancedSettings6
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings6, свойство Плугиндллс
- Службы удаленных рабочих столов свойства Плугиндллс, интерфейс IMsRdpClientAdvancedSettings7
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings7, свойство Плугиндллс
- Службы удаленных рабочих столов свойства Плугиндллс, интерфейс IMsRdpClientAdvancedSettings8
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings8, свойство Плугиндллс
topic_type:
- apiref
api_name:
- IMsTscAdvancedSettings.PluginDlls
- IMsTscAdvancedSettings.put_PluginDlls
- IMsRdpClientAdvancedSettings.PluginDlls
- IMsRdpClientAdvancedSettings.put_PluginDlls
- IMsRdpClientAdvancedSettings2.PluginDlls
- IMsRdpClientAdvancedSettings2.put_PluginDlls
- IMsRdpClientAdvancedSettings3.PluginDlls
- IMsRdpClientAdvancedSettings3.put_PluginDlls
- IMsRdpClientAdvancedSettings4.PluginDlls
- IMsRdpClientAdvancedSettings4.put_PluginDlls
- IMsRdpClientAdvancedSettings5.PluginDlls
- IMsRdpClientAdvancedSettings5.put_PluginDlls
- IMsRdpClientAdvancedSettings6.PluginDlls
- IMsRdpClientAdvancedSettings6.put_PluginDlls
- IMsRdpClientAdvancedSettings7.PluginDlls
- IMsRdpClientAdvancedSettings7.put_PluginDlls
- IMsRdpClientAdvancedSettings8.PluginDlls
- IMsRdpClientAdvancedSettings8.put_PluginDlls
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3ef2e518145ae34533477bcbefb92e15d9c8d94
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490635"
---
# <a name="imstscadvancedsettingsplugindlls-property"></a><span data-ttu-id="9fc3b-122">Имстскадванцедсеттингс: свойство Лугиндллс:P</span><span class="sxs-lookup"><span data-stu-id="9fc3b-122">IMsTscAdvancedSettings::PluginDlls property</span></span>

<span data-ttu-id="9fc3b-123">Указывает имена клиентских DLL-библиотек виртуальных каналов для загрузки.</span><span class="sxs-lookup"><span data-stu-id="9fc3b-123">Specifies the names of virtual channel client DLLs to be loaded.</span></span> <span data-ttu-id="9fc3b-124">Клиентские библиотеки DLL виртуальных каналов также называются подключаемыми библиотеками DLL.</span><span class="sxs-lookup"><span data-stu-id="9fc3b-124">Virtual channel client DLLs are also referred to as Plug-in DLLs.</span></span>

<span data-ttu-id="9fc3b-125">Это свойство доступно только на запись.</span><span class="sxs-lookup"><span data-stu-id="9fc3b-125">This property is write-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="9fc3b-126">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9fc3b-126">Syntax</span></span>


```C++
HRESULT put_PluginDlls(
  [in] BSTR PluginDlls
);
```



## <a name="property-value"></a><span data-ttu-id="9fc3b-127">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="9fc3b-127">Property value</span></span>

<span data-ttu-id="9fc3b-128">Разделенный запятыми список имен загружаемых клиентских библиотек DLL для виртуальных каналов.</span><span class="sxs-lookup"><span data-stu-id="9fc3b-128">Comma-separated list of the names of the virtual channel client DLLs to be loaded.</span></span> <span data-ttu-id="9fc3b-129">Имена библиотек DLL должны содержать только буквенно-цифровые символы.</span><span class="sxs-lookup"><span data-stu-id="9fc3b-129">The DLL names must contain only alphanumeric characters.</span></span> <span data-ttu-id="9fc3b-130">Дополнительные сведения о формате этих имен см. [в разделе Регистрация подключаемого модуля DVC](dvc-plug-in-registration.md).</span><span class="sxs-lookup"><span data-stu-id="9fc3b-130">For more information about the format of these names, see [DVC plug-in registration](dvc-plug-in-registration.md).</span></span>

## <a name="error-codes"></a><span data-ttu-id="9fc3b-131">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="9fc3b-131">Error codes</span></span>

<span data-ttu-id="9fc3b-132">В случае успеха возвратите значение **\_ ОК** .</span><span class="sxs-lookup"><span data-stu-id="9fc3b-132">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="9fc3b-133">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9fc3b-133">Remarks</span></span>

<span data-ttu-id="9fc3b-134">По соображениям безопасности, если элемент управления размещен на веб-странице, свойство **плугиндллс** принимает только именованный список клиентских библиотек DLL для виртуальных каналов.</span><span class="sxs-lookup"><span data-stu-id="9fc3b-134">For security reasons, if the control is hosted in a webpage the **PluginDlls** property only accepts a named list of virtual channel client DLLs.</span></span> <span data-ttu-id="9fc3b-135">Элемент управления возвращает ошибку, если указана файловая система или путь UNC.</span><span class="sxs-lookup"><span data-stu-id="9fc3b-135">The control returns an error if a file system or UNC path is specified.</span></span>

<span data-ttu-id="9fc3b-136">Клиентские библиотеки DLL виртуальных каналов, которые будут доступны с веб-страницы, должны быть установлены в каталог "% WinDir% \\ System32", поскольку удаленный рабочий стол элемент управления ActiveX обращается только к ФАЙЛАМ DLL в этом расположении.</span><span class="sxs-lookup"><span data-stu-id="9fc3b-136">Virtual channel client DLLs that will be accessed from a webpage must be installed in the "%WinDir%\\system32" directory because the Remote Desktop ActiveX control only accesses DLL files in that location.</span></span> <span data-ttu-id="9fc3b-137">Если элемент управления не размещается на веб-странице, это ограничение безопасности не существует, а полные пути могут использоваться для доступа и загрузки клиентских библиотек DLL для виртуальных каналов, расположенных в любом месте файловой системы.</span><span class="sxs-lookup"><span data-stu-id="9fc3b-137">If the control is not hosted in a webpage, this security restriction does not exist and full paths may be used to access and load virtual channel client DLLs located anywhere on the file system.</span></span>

<span data-ttu-id="9fc3b-138">Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="9fc3b-138">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9fc3b-139">Требования</span><span class="sxs-lookup"><span data-stu-id="9fc3b-139">Requirements</span></span>



| <span data-ttu-id="9fc3b-140">Требование</span><span class="sxs-lookup"><span data-stu-id="9fc3b-140">Requirement</span></span> | <span data-ttu-id="9fc3b-141">Значение</span><span class="sxs-lookup"><span data-stu-id="9fc3b-141">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="9fc3b-142">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9fc3b-142">Minimum supported client</span></span><br/> | <span data-ttu-id="9fc3b-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9fc3b-143">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="9fc3b-144">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9fc3b-144">Minimum supported server</span></span><br/> | <span data-ttu-id="9fc3b-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9fc3b-145">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="9fc3b-146">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="9fc3b-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="9fc3b-147"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9fc3b-147"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="9fc3b-148">DLL</span><span class="sxs-lookup"><span data-stu-id="9fc3b-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9fc3b-149"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9fc3b-149"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="9fc3b-150">IID</span><span class="sxs-lookup"><span data-stu-id="9fc3b-150">IID</span></span><br/>                      | <span data-ttu-id="9fc3b-151">IID \_ имстскадванцедсеттингс определен как 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d</span><span class="sxs-lookup"><span data-stu-id="9fc3b-151">IID\_IMsTscAdvancedSettings is defined as 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9fc3b-152">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9fc3b-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9fc3b-153">**имсрдпклиентадванцедсеттингс**</span><span class="sxs-lookup"><span data-stu-id="9fc3b-153">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="9fc3b-154">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="9fc3b-154">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="9fc3b-155">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="9fc3b-155">**IMsRdpClientAdvancedSettings3**</span></span>](imsrdpclientadvancedsettings3.md)
</dt> <dt>

[<span data-ttu-id="9fc3b-156">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="9fc3b-156">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="9fc3b-157">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="9fc3b-157">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="9fc3b-158">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="9fc3b-158">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="9fc3b-159">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="9fc3b-159">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="9fc3b-160">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="9fc3b-160">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="9fc3b-161">**имстскадванцедсеттингс**</span><span class="sxs-lookup"><span data-stu-id="9fc3b-161">**IMsTscAdvancedSettings**</span></span>](imstscadvancedsettings-interface.md)
</dt> </dl>

 

 





