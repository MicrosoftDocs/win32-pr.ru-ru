---
title: IMsRdpClient4 AdvancedSettings5, свойство
description: Получает указатель на интерфейс IMsRdpClientAdvancedSettings4.
ms.assetid: 2dd0cc5f-7822-485f-8b3f-12407af1e091
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства AdvancedSettings5
- Службы удаленных рабочих столов свойства AdvancedSettings5, интерфейс IMsRdpClient4
- Службы удаленных рабочих столов интерфейса IMsRdpClient4, свойство AdvancedSettings5
- Службы удаленных рабочих столов свойства AdvancedSettings5, интерфейс IMsRdpClient5
- Службы удаленных рабочих столов интерфейса IMsRdpClient5, свойство AdvancedSettings5
- Службы удаленных рабочих столов свойства AdvancedSettings5, интерфейс IMsRdpClient6
- Службы удаленных рабочих столов интерфейса IMsRdpClient6, свойство AdvancedSettings5
- Службы удаленных рабочих столов свойства AdvancedSettings5, интерфейс IMsRdpClient7
- Службы удаленных рабочих столов интерфейса IMsRdpClient7, свойство AdvancedSettings5
- Службы удаленных рабочих столов свойства AdvancedSettings5, интерфейс IMsRdpClient8
- Службы удаленных рабочих столов интерфейса IMsRdpClient8, свойство AdvancedSettings5
- Службы удаленных рабочих столов свойства AdvancedSettings5, интерфейс IMsRdpClient9
- Службы удаленных рабочих столов интерфейса IMsRdpClient9, свойство AdvancedSettings5
- Службы удаленных рабочих столов свойства AdvancedSettings5, интерфейс IMsRdpClient10
- Службы удаленных рабочих столов интерфейса IMsRdpClient10, свойство AdvancedSettings5
topic_type:
- apiref
api_name:
- IMsRdpClient4.AdvancedSettings5
- IMsRdpClient4.get_AdvancedSettings5
- IMsRdpClient5.AdvancedSettings5
- IMsRdpClient5.get_AdvancedSettings5
- IMsRdpClient6.AdvancedSettings5
- IMsRdpClient6.get_AdvancedSettings5
- IMsRdpClient7.AdvancedSettings5
- IMsRdpClient7.get_AdvancedSettings5
- IMsRdpClient8.AdvancedSettings5
- IMsRdpClient8.get_AdvancedSettings5
- IMsRdpClient9.AdvancedSettings5
- IMsRdpClient9.get_AdvancedSettings5
- IMsRdpClient10.AdvancedSettings5
- IMsRdpClient10.get_AdvancedSettings5
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ad96588b2109375aed23c1024ef925936cb3368
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535405"
---
# <a name="imsrdpclient4advancedsettings5-property"></a><span data-ttu-id="30ef5-118">Свойство IMsRdpClient4:: AdvancedSettings5</span><span class="sxs-lookup"><span data-stu-id="30ef5-118">IMsRdpClient4::AdvancedSettings5 property</span></span>

<span data-ttu-id="30ef5-119">Получает указатель на интерфейс [**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md) .</span><span class="sxs-lookup"><span data-stu-id="30ef5-119">Retrieves a pointer to an [**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md) interface.</span></span>

<span data-ttu-id="30ef5-120">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="30ef5-120">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="30ef5-121">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="30ef5-121">Syntax</span></span>


```C++
HRESULT get_AdvancedSettings5(
  [out] IMsRdpClientAdvancedSettings4 **ppAdvSettings
);
```



## <a name="property-value"></a><span data-ttu-id="30ef5-122">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="30ef5-122">Property value</span></span>

<span data-ttu-id="30ef5-123">Указатель на интерфейс [**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md) .</span><span class="sxs-lookup"><span data-stu-id="30ef5-123">A pointer to the [**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md) interface.</span></span> <span data-ttu-id="30ef5-124">Интерфейс можно использовать для задания дополнительных параметров клиентского элемента управления.</span><span class="sxs-lookup"><span data-stu-id="30ef5-124">The interface can be used to set advanced settings for the client control.</span></span>

## <a name="error-codes"></a><span data-ttu-id="30ef5-125">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="30ef5-125">Error codes</span></span>

<span data-ttu-id="30ef5-126">Если метод выполнен успешно, возвращается значение **S \_ OK** .</span><span class="sxs-lookup"><span data-stu-id="30ef5-126">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="30ef5-127">Любое другое значение **HRESULT** указывает на сбой вызова.</span><span class="sxs-lookup"><span data-stu-id="30ef5-127">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="30ef5-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="30ef5-128">Remarks</span></span>

<span data-ttu-id="30ef5-129">Это свойство не может быть задано, если элемент управления подключен.</span><span class="sxs-lookup"><span data-stu-id="30ef5-129">This property cannot be set when the control is connected.</span></span>

<span data-ttu-id="30ef5-130">Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="30ef5-130">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="30ef5-131">Требования</span><span class="sxs-lookup"><span data-stu-id="30ef5-131">Requirements</span></span>



| <span data-ttu-id="30ef5-132">Требование</span><span class="sxs-lookup"><span data-stu-id="30ef5-132">Requirement</span></span> | <span data-ttu-id="30ef5-133">Значение</span><span class="sxs-lookup"><span data-stu-id="30ef5-133">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="30ef5-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="30ef5-134">Minimum supported client</span></span><br/> | <span data-ttu-id="30ef5-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="30ef5-135">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="30ef5-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="30ef5-136">Minimum supported server</span></span><br/> | <span data-ttu-id="30ef5-137">Windows Server 2008, Windows Server 2008 с пакетом обновления 1</span><span class="sxs-lookup"><span data-stu-id="30ef5-137">Windows Server 2008, Windows Server 2008 with SP1</span></span><br/>                           |
| <span data-ttu-id="30ef5-138">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="30ef5-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="30ef5-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="30ef5-139"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="30ef5-140">DLL</span><span class="sxs-lookup"><span data-stu-id="30ef5-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="30ef5-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="30ef5-141"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="30ef5-142">IID</span><span class="sxs-lookup"><span data-stu-id="30ef5-142">IID</span></span><br/>                      | <span data-ttu-id="30ef5-143">IMsRdpClient4 определяется как 095E0738-D97D-488b-B9F6-DD0E8D66C0DE</span><span class="sxs-lookup"><span data-stu-id="30ef5-143">IMsRdpClient4 is defined as 095E0738-D97D-488b-B9F6-DD0E8D66C0DE</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="30ef5-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="30ef5-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30ef5-145">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="30ef5-145">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="30ef5-146">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="30ef5-146">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="30ef5-147">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="30ef5-147">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="30ef5-148">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="30ef5-148">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="30ef5-149">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="30ef5-149">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="30ef5-150">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="30ef5-150">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="30ef5-151">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="30ef5-151">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





