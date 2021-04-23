---
title: IMsRdpClientAdvancedSettings2 Енаблеаутореконнект, свойство
description: Указывает, следует ли включить клиентский элемент управления для автоматического подключения к сеансу в случае отключения от сети.
ms.assetid: 9d820f78-bf7f-479a-ae6f-be0f0abe549c
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Енаблеаутореконнект
- Службы удаленных рабочих столов свойства Енаблеаутореконнект, интерфейс IMsRdpClientAdvancedSettings2
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings2, свойство Енаблеаутореконнект
- Службы удаленных рабочих столов свойства Енаблеаутореконнект, интерфейс IMsRdpClientAdvancedSettings3
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings3, свойство Енаблеаутореконнект
- Службы удаленных рабочих столов свойства Енаблеаутореконнект, интерфейс IMsRdpClientAdvancedSettings4
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings4, свойство Енаблеаутореконнект
- Службы удаленных рабочих столов свойства Енаблеаутореконнект, интерфейс IMsRdpClientAdvancedSettings5
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings5, свойство Енаблеаутореконнект
- Службы удаленных рабочих столов свойства Енаблеаутореконнект, интерфейс IMsRdpClientAdvancedSettings6
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings6, свойство Енаблеаутореконнект
- Службы удаленных рабочих столов свойства Енаблеаутореконнект, интерфейс IMsRdpClientAdvancedSettings7
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings7, свойство Енаблеаутореконнект
- Службы удаленных рабочих столов свойства Енаблеаутореконнект, интерфейс IMsRdpClientAdvancedSettings8
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings8, свойство Енаблеаутореконнект
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings2.EnableAutoReconnect
- IMsRdpClientAdvancedSettings2.get_EnableAutoReconnect
- IMsRdpClientAdvancedSettings2.put_EnableAutoReconnect
- IMsRdpClientAdvancedSettings3.EnableAutoReconnect
- IMsRdpClientAdvancedSettings3.get_EnableAutoReconnect
- IMsRdpClientAdvancedSettings3.put_EnableAutoReconnect
- IMsRdpClientAdvancedSettings4.EnableAutoReconnect
- IMsRdpClientAdvancedSettings4.get_EnableAutoReconnect
- IMsRdpClientAdvancedSettings4.put_EnableAutoReconnect
- IMsRdpClientAdvancedSettings5.EnableAutoReconnect
- IMsRdpClientAdvancedSettings5.get_EnableAutoReconnect
- IMsRdpClientAdvancedSettings5.put_EnableAutoReconnect
- IMsRdpClientAdvancedSettings6.EnableAutoReconnect
- IMsRdpClientAdvancedSettings6.get_EnableAutoReconnect
- IMsRdpClientAdvancedSettings6.put_EnableAutoReconnect
- IMsRdpClientAdvancedSettings7.EnableAutoReconnect
- IMsRdpClientAdvancedSettings7.get_EnableAutoReconnect
- IMsRdpClientAdvancedSettings7.put_EnableAutoReconnect
- IMsRdpClientAdvancedSettings8.EnableAutoReconnect
- IMsRdpClientAdvancedSettings8.get_EnableAutoReconnect
- IMsRdpClientAdvancedSettings8.put_EnableAutoReconnect
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f8d4a1345395b5b5843872df256fe7a113094e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681977"
---
# <a name="imsrdpclientadvancedsettings2enableautoreconnect-property"></a><span data-ttu-id="e9db0-118">Свойство IMsRdpClientAdvancedSettings2:: Енаблеаутореконнект</span><span class="sxs-lookup"><span data-stu-id="e9db0-118">IMsRdpClientAdvancedSettings2::EnableAutoReconnect property</span></span>

<span data-ttu-id="e9db0-119">Указывает, следует ли включить клиентский элемент управления для автоматического подключения к сеансу в случае отключения от сети.</span><span class="sxs-lookup"><span data-stu-id="e9db0-119">Specifies whether to enable the client control to reconnect automatically to a session in the event of a network disconnection.</span></span>

<span data-ttu-id="e9db0-120">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="e9db0-120">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9db0-121">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e9db0-121">Syntax</span></span>


```C++
HRESULT put_EnableAutoReconnect(
  [in]  VARIANT_BOOL fEnableAutoReconnect
);

HRESULT get_EnableAutoReconnect(
  [out] VARIANT_BOOL *pfEnableAutoReconnect
);
```



## <a name="property-value"></a><span data-ttu-id="e9db0-122">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="e9db0-122">Property value</span></span>

<span data-ttu-id="e9db0-123">Задайте значение **\_ true** , чтобы включить автоматическое повторное подключение, и выберите **вариант \_ false** , чтобы отключить его.</span><span class="sxs-lookup"><span data-stu-id="e9db0-123">Set to **VARIANT\_TRUE** to enable automatic reconnection, and to **VARIANT\_FALSE** to disable it.</span></span> <span data-ttu-id="e9db0-124">Значение по умолчанию — **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="e9db0-124">The default is **VARIANT\_TRUE**.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e9db0-125">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="e9db0-125">Error codes</span></span>

<span data-ttu-id="e9db0-126">В случае успеха возвратите значение **\_ ОК** .</span><span class="sxs-lookup"><span data-stu-id="e9db0-126">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="e9db0-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e9db0-127">Remarks</span></span>

<span data-ttu-id="e9db0-128">Это свойство не может быть задано, если элемент управления подключен.</span><span class="sxs-lookup"><span data-stu-id="e9db0-128">This property cannot be set when the control is connected.</span></span>

<span data-ttu-id="e9db0-129">Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="e9db0-129">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e9db0-130">Требования</span><span class="sxs-lookup"><span data-stu-id="e9db0-130">Requirements</span></span>



| <span data-ttu-id="e9db0-131">Требование</span><span class="sxs-lookup"><span data-stu-id="e9db0-131">Requirement</span></span> | <span data-ttu-id="e9db0-132">Значение</span><span class="sxs-lookup"><span data-stu-id="e9db0-132">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9db0-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e9db0-133">Minimum supported client</span></span><br/> | <span data-ttu-id="e9db0-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e9db0-134">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="e9db0-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e9db0-135">Minimum supported server</span></span><br/> | <span data-ttu-id="e9db0-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e9db0-136">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="e9db0-137">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="e9db0-137">Type library</span></span><br/>             | <dl> <span data-ttu-id="e9db0-138"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e9db0-138"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="e9db0-139">DLL</span><span class="sxs-lookup"><span data-stu-id="e9db0-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e9db0-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e9db0-140"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="e9db0-141">IID</span><span class="sxs-lookup"><span data-stu-id="e9db0-141">IID</span></span><br/>                      | <span data-ttu-id="e9db0-142">IID \_ IMsRdpClientAdvancedSettings2 определен как 9ac42117-2b76-4320-aa44-0e616ab8437b</span><span class="sxs-lookup"><span data-stu-id="e9db0-142">IID\_IMsRdpClientAdvancedSettings2 is defined as 9ac42117-2b76-4320-aa44-0e616ab8437b</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e9db0-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e9db0-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9db0-144">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="e9db0-144">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="e9db0-145">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="e9db0-145">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="e9db0-146">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="e9db0-146">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="e9db0-147">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="e9db0-147">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="e9db0-148">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="e9db0-148">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="e9db0-149">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="e9db0-149">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="e9db0-150">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="e9db0-150">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> </dl>

 

 





