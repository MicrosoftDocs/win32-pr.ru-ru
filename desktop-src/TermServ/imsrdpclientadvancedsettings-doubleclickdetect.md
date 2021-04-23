---
title: Имсрдпклиентадванцедсеттингс Даублекликкдетект, свойство
description: Указывает, определяет ли клиент двойные щелчки для сервера.
ms.assetid: 39e76bef-3d12-406d-a074-8c084fbe9ccc
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Даублекликкдетект
- Службы удаленных рабочих столов свойства Даублекликкдетект, интерфейс Имсрдпклиентадванцедсеттингс
- Службы удаленных рабочих столов интерфейса Имсрдпклиентадванцедсеттингс, свойство Даублекликкдетект
- Службы удаленных рабочих столов свойства Даублекликкдетект, интерфейс IMsRdpClientAdvancedSettings2
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings2, свойство Даублекликкдетект
- Службы удаленных рабочих столов свойства Даублекликкдетект, интерфейс IMsRdpClientAdvancedSettings3
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings3, свойство Даублекликкдетект
- Службы удаленных рабочих столов свойства Даублекликкдетект, интерфейс IMsRdpClientAdvancedSettings4
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings4, свойство Даублекликкдетект
- Службы удаленных рабочих столов свойства Даублекликкдетект, интерфейс IMsRdpClientAdvancedSettings5
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings5, свойство Даублекликкдетект
- Службы удаленных рабочих столов свойства Даублекликкдетект, интерфейс IMsRdpClientAdvancedSettings6
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings6, свойство Даублекликкдетект
- Службы удаленных рабочих столов свойства Даублекликкдетект, интерфейс IMsRdpClientAdvancedSettings7
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings7, свойство Даублекликкдетект
- Службы удаленных рабочих столов свойства Даублекликкдетект, интерфейс IMsRdpClientAdvancedSettings8
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings8, свойство Даублекликкдетект
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.DoubleClickDetect
- IMsRdpClientAdvancedSettings.get_DoubleClickDetect
- IMsRdpClientAdvancedSettings.put_DoubleClickDetect
- IMsRdpClientAdvancedSettings2.DoubleClickDetect
- IMsRdpClientAdvancedSettings2.get_DoubleClickDetect
- IMsRdpClientAdvancedSettings2.put_DoubleClickDetect
- IMsRdpClientAdvancedSettings3.DoubleClickDetect
- IMsRdpClientAdvancedSettings3.get_DoubleClickDetect
- IMsRdpClientAdvancedSettings3.put_DoubleClickDetect
- IMsRdpClientAdvancedSettings4.DoubleClickDetect
- IMsRdpClientAdvancedSettings4.get_DoubleClickDetect
- IMsRdpClientAdvancedSettings4.put_DoubleClickDetect
- IMsRdpClientAdvancedSettings5.DoubleClickDetect
- IMsRdpClientAdvancedSettings5.get_DoubleClickDetect
- IMsRdpClientAdvancedSettings5.put_DoubleClickDetect
- IMsRdpClientAdvancedSettings6.DoubleClickDetect
- IMsRdpClientAdvancedSettings6.get_DoubleClickDetect
- IMsRdpClientAdvancedSettings6.put_DoubleClickDetect
- IMsRdpClientAdvancedSettings7.DoubleClickDetect
- IMsRdpClientAdvancedSettings7.get_DoubleClickDetect
- IMsRdpClientAdvancedSettings7.put_DoubleClickDetect
- IMsRdpClientAdvancedSettings8.DoubleClickDetect
- IMsRdpClientAdvancedSettings8.get_DoubleClickDetect
- IMsRdpClientAdvancedSettings8.put_DoubleClickDetect
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd771614a80d909e0e7a748ab7256a5310084deb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137358"
---
# <a name="imsrdpclientadvancedsettingsdoubleclickdetect-property"></a><span data-ttu-id="49196-120">Имсрдпклиентадванцедсеттингс: свойство Аублекликкдетект:D</span><span class="sxs-lookup"><span data-stu-id="49196-120">IMsRdpClientAdvancedSettings::DoubleClickDetect property</span></span>

<span data-ttu-id="49196-121">Указывает, определяет ли клиент двойные щелчки для сервера.</span><span class="sxs-lookup"><span data-stu-id="49196-121">Specifies if the client identifies double-clicks for the server.</span></span>

<span data-ttu-id="49196-122">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="49196-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="49196-123">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="49196-123">Syntax</span></span>


```C++
HRESULT put_DoubleClickDetect(
  [in]  LONG doubleClickDetect
);

HRESULT get_DoubleClickDetect(
  [out] LONG *pdoubleClickDetect
);
```



## <a name="property-value"></a><span data-ttu-id="49196-124">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="49196-124">Property value</span></span>

<span data-ttu-id="49196-125">Задайте для этого параметра значение 0, чтобы отключить функцию, или ненулевое, чтобы включить эту функцию.</span><span class="sxs-lookup"><span data-stu-id="49196-125">Set this parameter to 0 to disable the feature or a nonzero value to enable the feature.</span></span>

## <a name="error-codes"></a><span data-ttu-id="49196-126">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="49196-126">Error codes</span></span>

<span data-ttu-id="49196-127">При успешном выполнении возвращает значение **\_ ОК** .</span><span class="sxs-lookup"><span data-stu-id="49196-127">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="49196-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="49196-128">Remarks</span></span>

<span data-ttu-id="49196-129">Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="49196-129">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="49196-130">Требования</span><span class="sxs-lookup"><span data-stu-id="49196-130">Requirements</span></span>



| <span data-ttu-id="49196-131">Требование</span><span class="sxs-lookup"><span data-stu-id="49196-131">Requirement</span></span> | <span data-ttu-id="49196-132">Значение</span><span class="sxs-lookup"><span data-stu-id="49196-132">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49196-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="49196-133">Minimum supported client</span></span><br/> | <span data-ttu-id="49196-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="49196-134">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="49196-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="49196-135">Minimum supported server</span></span><br/> | <span data-ttu-id="49196-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="49196-136">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="49196-137">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="49196-137">Type library</span></span><br/>             | <dl> <span data-ttu-id="49196-138"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="49196-138"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="49196-139">DLL</span><span class="sxs-lookup"><span data-stu-id="49196-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="49196-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="49196-140"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="49196-141">IID</span><span class="sxs-lookup"><span data-stu-id="49196-141">IID</span></span><br/>                      | <span data-ttu-id="49196-142">IID \_ имсрдпклиентадванцедсеттингс определен как 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="49196-142">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="49196-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="49196-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49196-144">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="49196-144">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="49196-145">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="49196-145">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="49196-146">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="49196-146">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="49196-147">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="49196-147">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="49196-148">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="49196-148">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="49196-149">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="49196-149">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="49196-150">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="49196-150">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="49196-151">**имсрдпклиентадванцедсеттингс**</span><span class="sxs-lookup"><span data-stu-id="49196-151">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





