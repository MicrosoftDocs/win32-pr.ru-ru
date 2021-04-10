---
title: IMsRdpClient3 AdvancedSettings4, свойство
description: Получает указатель на интерфейс IMsRdpClientAdvancedSettings3.
ms.assetid: 30935099-7f33-4745-8a31-f9a28ab78b63
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства AdvancedSettings4
- Службы удаленных рабочих столов свойства AdvancedSettings4, интерфейс IMsRdpClient3
- Службы удаленных рабочих столов интерфейса IMsRdpClient3, свойство AdvancedSettings4
- Службы удаленных рабочих столов свойства AdvancedSettings4, интерфейс IMsRdpClient4
- Службы удаленных рабочих столов интерфейса IMsRdpClient4, свойство AdvancedSettings4
- Службы удаленных рабочих столов свойства AdvancedSettings4, интерфейс IMsRdpClient5
- Службы удаленных рабочих столов интерфейса IMsRdpClient5, свойство AdvancedSettings4
- Службы удаленных рабочих столов свойства AdvancedSettings4, интерфейс IMsRdpClient6
- Службы удаленных рабочих столов интерфейса IMsRdpClient6, свойство AdvancedSettings4
- Службы удаленных рабочих столов свойства AdvancedSettings4, интерфейс IMsRdpClient7
- Службы удаленных рабочих столов интерфейса IMsRdpClient7, свойство AdvancedSettings4
- Службы удаленных рабочих столов свойства AdvancedSettings4, интерфейс IMsRdpClient8
- Службы удаленных рабочих столов интерфейса IMsRdpClient8, свойство AdvancedSettings4
- Службы удаленных рабочих столов свойства AdvancedSettings4, интерфейс IMsRdpClient9
- Службы удаленных рабочих столов интерфейса IMsRdpClient9, свойство AdvancedSettings4
- Службы удаленных рабочих столов свойства AdvancedSettings4, интерфейс IMsRdpClient10
- Службы удаленных рабочих столов интерфейса IMsRdpClient10, свойство AdvancedSettings4
topic_type:
- apiref
api_name:
- IMsRdpClient3.AdvancedSettings4
- IMsRdpClient3.get_AdvancedSettings4
- IMsRdpClient4.AdvancedSettings4
- IMsRdpClient4.get_AdvancedSettings4
- IMsRdpClient5.AdvancedSettings4
- IMsRdpClient5.get_AdvancedSettings4
- IMsRdpClient6.AdvancedSettings4
- IMsRdpClient6.get_AdvancedSettings4
- IMsRdpClient7.AdvancedSettings4
- IMsRdpClient7.get_AdvancedSettings4
- IMsRdpClient8.AdvancedSettings4
- IMsRdpClient8.get_AdvancedSettings4
- IMsRdpClient9.AdvancedSettings4
- IMsRdpClient9.get_AdvancedSettings4
- IMsRdpClient10.AdvancedSettings4
- IMsRdpClient10.get_AdvancedSettings4
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7a229c28b645e7920212a04cc44ca5a9ce42be3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891573"
---
# <a name="imsrdpclient3advancedsettings4-property"></a><span data-ttu-id="cda2c-120">Свойство IMsRdpClient3:: AdvancedSettings4</span><span class="sxs-lookup"><span data-stu-id="cda2c-120">IMsRdpClient3::AdvancedSettings4 property</span></span>

<span data-ttu-id="cda2c-121">Получает указатель на интерфейс [**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md) .</span><span class="sxs-lookup"><span data-stu-id="cda2c-121">Retrieves a pointer to the [**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md) interface.</span></span>

<span data-ttu-id="cda2c-122">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="cda2c-122">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="cda2c-123">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cda2c-123">Syntax</span></span>


```C++
HRESULT get_AdvancedSettings4(
  [out] IMsRdpClientAdvancedSettings3 **ppAdvSettings
);
```



## <a name="property-value"></a><span data-ttu-id="cda2c-124">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="cda2c-124">Property value</span></span>

<span data-ttu-id="cda2c-125">Указатель на интерфейс [**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md) .</span><span class="sxs-lookup"><span data-stu-id="cda2c-125">Pointer to the [**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md) interface.</span></span> <span data-ttu-id="cda2c-126">Интерфейс можно использовать для задания дополнительных параметров клиентского элемента управления.</span><span class="sxs-lookup"><span data-stu-id="cda2c-126">The interface can be used to set advanced settings for the client control.</span></span>

## <a name="error-codes"></a><span data-ttu-id="cda2c-127">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="cda2c-127">Error codes</span></span>

<span data-ttu-id="cda2c-128">Если метод выполнен успешно, возвращается значение **S \_ OK** .</span><span class="sxs-lookup"><span data-stu-id="cda2c-128">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="cda2c-129">Любое другое значение **HRESULT** указывает на сбой вызова.</span><span class="sxs-lookup"><span data-stu-id="cda2c-129">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="cda2c-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cda2c-130">Remarks</span></span>

<span data-ttu-id="cda2c-131">Это свойство не может быть задано, если элемент управления подключен.</span><span class="sxs-lookup"><span data-stu-id="cda2c-131">This property cannot be set when the control is connected.</span></span>

<span data-ttu-id="cda2c-132">Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="cda2c-132">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cda2c-133">Требования</span><span class="sxs-lookup"><span data-stu-id="cda2c-133">Requirements</span></span>



| <span data-ttu-id="cda2c-134">Требование</span><span class="sxs-lookup"><span data-stu-id="cda2c-134">Requirement</span></span> | <span data-ttu-id="cda2c-135">Значение</span><span class="sxs-lookup"><span data-stu-id="cda2c-135">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cda2c-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cda2c-136">Minimum supported client</span></span><br/> | <span data-ttu-id="cda2c-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cda2c-137">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="cda2c-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cda2c-138">Minimum supported server</span></span><br/> | <span data-ttu-id="cda2c-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cda2c-139">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="cda2c-140">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="cda2c-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="cda2c-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cda2c-141"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="cda2c-142">DLL</span><span class="sxs-lookup"><span data-stu-id="cda2c-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cda2c-143"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cda2c-143"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="cda2c-144">IID</span><span class="sxs-lookup"><span data-stu-id="cda2c-144">IID</span></span><br/>                      | <span data-ttu-id="cda2c-145">IID \_ IMsRdpClient3 определен как 91b7cbc5-a72e-4fa0-9300-d647d7e897ff</span><span class="sxs-lookup"><span data-stu-id="cda2c-145">IID\_IMsRdpClient3 is defined as 91b7cbc5-a72e-4fa0-9300-d647d7e897ff</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="cda2c-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cda2c-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cda2c-147">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="cda2c-147">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="cda2c-148">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="cda2c-148">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="cda2c-149">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="cda2c-149">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="cda2c-150">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="cda2c-150">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="cda2c-151">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="cda2c-151">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="cda2c-152">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="cda2c-152">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="cda2c-153">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="cda2c-153">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="cda2c-154">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="cda2c-154">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





