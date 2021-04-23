---
title: Свойство сжатия Имстскадванцедсеттингс
description: Указывает, включено ли сжатие.
ms.assetid: 274774b3-0442-4a46-95f8-7857f885bfdb
ms.tgt_platform: multiple
keywords:
- Сжатие службы удаленных рабочих столов свойств
- Сжатие службы удаленных рабочих столов свойств, интерфейс Имстскадванцедсеттингс
- Службы удаленных рабочих столов интерфейса Имстскадванцедсеттингс, свойство сжатия
- Сжатие службы удаленных рабочих столов свойств, интерфейс Имсрдпклиентадванцедсеттингс
- Службы удаленных рабочих столов интерфейса Имсрдпклиентадванцедсеттингс, свойство сжатия
- Сжатие службы удаленных рабочих столов свойств, интерфейс IMsRdpClientAdvancedSettings2
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings2, свойство сжатия
- Сжатие службы удаленных рабочих столов свойств, интерфейс IMsRdpClientAdvancedSettings3
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings3, свойство сжатия
- Сжатие службы удаленных рабочих столов свойств, интерфейс IMsRdpClientAdvancedSettings4
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings4, свойство сжатия
- Сжатие службы удаленных рабочих столов свойств, интерфейс IMsRdpClientAdvancedSettings5
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings5, свойство сжатия
- Сжатие службы удаленных рабочих столов свойств, интерфейс IMsRdpClientAdvancedSettings6
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings6, свойство сжатия
- Сжатие службы удаленных рабочих столов свойств, интерфейс IMsRdpClientAdvancedSettings7
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings7, свойство сжатия
- Сжатие службы удаленных рабочих столов свойств, интерфейс IMsRdpClientAdvancedSettings8
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings8, свойство сжатия
topic_type:
- apiref
api_name:
- IMsTscAdvancedSettings.Compress
- IMsTscAdvancedSettings.get_Compress
- IMsTscAdvancedSettings.put_Compress
- IMsRdpClientAdvancedSettings.Compress
- IMsRdpClientAdvancedSettings.get_Compress
- IMsRdpClientAdvancedSettings.put_Compress
- IMsRdpClientAdvancedSettings2.Compress
- IMsRdpClientAdvancedSettings2.get_Compress
- IMsRdpClientAdvancedSettings2.put_Compress
- IMsRdpClientAdvancedSettings3.Compress
- IMsRdpClientAdvancedSettings3.get_Compress
- IMsRdpClientAdvancedSettings3.put_Compress
- IMsRdpClientAdvancedSettings4.Compress
- IMsRdpClientAdvancedSettings4.get_Compress
- IMsRdpClientAdvancedSettings4.put_Compress
- IMsRdpClientAdvancedSettings5.Compress
- IMsRdpClientAdvancedSettings5.get_Compress
- IMsRdpClientAdvancedSettings5.put_Compress
- IMsRdpClientAdvancedSettings6.Compress
- IMsRdpClientAdvancedSettings6.get_Compress
- IMsRdpClientAdvancedSettings6.put_Compress
- IMsRdpClientAdvancedSettings7.Compress
- IMsRdpClientAdvancedSettings7.get_Compress
- IMsRdpClientAdvancedSettings7.put_Compress
- IMsRdpClientAdvancedSettings8.Compress
- IMsRdpClientAdvancedSettings8.get_Compress
- IMsRdpClientAdvancedSettings8.put_Compress
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c588784d9b06bd2e8e1605a96c8aa9fd157c10eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988857"
---
# <a name="imstscadvancedsettingscompress-property"></a><span data-ttu-id="27569-122">Свойство Имстскадванцедсеттингс:: сжимать</span><span class="sxs-lookup"><span data-stu-id="27569-122">IMsTscAdvancedSettings::Compress property</span></span>

<span data-ttu-id="27569-123">Указывает, включено ли сжатие.</span><span class="sxs-lookup"><span data-stu-id="27569-123">Specifies whether compression is enabled.</span></span>

<span data-ttu-id="27569-124">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="27569-124">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="27569-125">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="27569-125">Syntax</span></span>


```C++
HRESULT put_Compress(
  [in]  LONG compress
);

HRESULT get_Compress(
  [out] LONG *pcompress
);
```



## <a name="property-value"></a><span data-ttu-id="27569-126">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="27569-126">Property value</span></span>

<span data-ttu-id="27569-127">Задайте для этого параметра значение 0, чтобы отключить сжатие, или ненулевое, чтобы включить сжатие.</span><span class="sxs-lookup"><span data-stu-id="27569-127">Set this parameter to 0 to disable compression or a nonzero value to enable compression.</span></span>

## <a name="error-codes"></a><span data-ttu-id="27569-128">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="27569-128">Error codes</span></span>

<span data-ttu-id="27569-129">При успешном выполнении возвращает значение **\_ ОК** .</span><span class="sxs-lookup"><span data-stu-id="27569-129">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="27569-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="27569-130">Remarks</span></span>

<span data-ttu-id="27569-131">Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="27569-131">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="27569-132">Требования</span><span class="sxs-lookup"><span data-stu-id="27569-132">Requirements</span></span>



| <span data-ttu-id="27569-133">Требование</span><span class="sxs-lookup"><span data-stu-id="27569-133">Requirement</span></span> | <span data-ttu-id="27569-134">Значение</span><span class="sxs-lookup"><span data-stu-id="27569-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="27569-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="27569-135">Minimum supported client</span></span><br/> | <span data-ttu-id="27569-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="27569-136">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="27569-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="27569-137">Minimum supported server</span></span><br/> | <span data-ttu-id="27569-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="27569-138">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="27569-139">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="27569-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="27569-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="27569-140"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="27569-141">DLL</span><span class="sxs-lookup"><span data-stu-id="27569-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="27569-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="27569-142"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="27569-143">IID</span><span class="sxs-lookup"><span data-stu-id="27569-143">IID</span></span><br/>                      | <span data-ttu-id="27569-144">IID \_ имстскадванцедсеттингс определен как 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d</span><span class="sxs-lookup"><span data-stu-id="27569-144">IID\_IMsTscAdvancedSettings is defined as 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="27569-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="27569-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27569-146">**имсрдпклиентадванцедсеттингс**</span><span class="sxs-lookup"><span data-stu-id="27569-146">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="27569-147">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="27569-147">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="27569-148">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="27569-148">**IMsRdpClientAdvancedSettings3**</span></span>](imsrdpclientadvancedsettings3.md)
</dt> <dt>

[<span data-ttu-id="27569-149">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="27569-149">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="27569-150">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="27569-150">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="27569-151">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="27569-151">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="27569-152">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="27569-152">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="27569-153">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="27569-153">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="27569-154">**имстскадванцедсеттингс**</span><span class="sxs-lookup"><span data-stu-id="27569-154">**IMsTscAdvancedSettings**</span></span>](imstscadvancedsettings-interface.md)
</dt> </dl>

 

 





