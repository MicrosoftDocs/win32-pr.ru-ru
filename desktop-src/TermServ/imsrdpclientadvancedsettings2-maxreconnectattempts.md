---
title: IMsRdpClientAdvancedSettings2 Максреконнектаттемптс, свойство
description: Указывает количество повторных попыток подключения во время автоматического повторного подключения.
ms.assetid: 24bfd3b6-d2de-4e46-8b5f-a4702c18a93c
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Максреконнектаттемптс
- Службы удаленных рабочих столов свойства Максреконнектаттемптс, интерфейс IMsRdpClientAdvancedSettings2
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings2, свойство Максреконнектаттемптс
- Службы удаленных рабочих столов свойства Максреконнектаттемптс, интерфейс IMsRdpClientAdvancedSettings3
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings3, свойство Максреконнектаттемптс
- Службы удаленных рабочих столов свойства Максреконнектаттемптс, интерфейс IMsRdpClientAdvancedSettings4
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings4, свойство Максреконнектаттемптс
- Службы удаленных рабочих столов свойства Максреконнектаттемптс, интерфейс IMsRdpClientAdvancedSettings5
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings5, свойство Максреконнектаттемптс
- Службы удаленных рабочих столов свойства Максреконнектаттемптс, интерфейс IMsRdpClientAdvancedSettings6
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings6, свойство Максреконнектаттемптс
- Службы удаленных рабочих столов свойства Максреконнектаттемптс, интерфейс IMsRdpClientAdvancedSettings7
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings7, свойство Максреконнектаттемптс
- Службы удаленных рабочих столов свойства Максреконнектаттемптс, интерфейс IMsRdpClientAdvancedSettings8
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings8, свойство Максреконнектаттемптс
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings2.MaxReconnectAttempts
- IMsRdpClientAdvancedSettings2.get_MaxReconnectAttempts
- IMsRdpClientAdvancedSettings2.put_MaxReconnectAttempts
- IMsRdpClientAdvancedSettings3.MaxReconnectAttempts
- IMsRdpClientAdvancedSettings3.get_MaxReconnectAttempts
- IMsRdpClientAdvancedSettings3.put_MaxReconnectAttempts
- IMsRdpClientAdvancedSettings4.MaxReconnectAttempts
- IMsRdpClientAdvancedSettings4.get_MaxReconnectAttempts
- IMsRdpClientAdvancedSettings4.put_MaxReconnectAttempts
- IMsRdpClientAdvancedSettings5.MaxReconnectAttempts
- IMsRdpClientAdvancedSettings5.get_MaxReconnectAttempts
- IMsRdpClientAdvancedSettings5.put_MaxReconnectAttempts
- IMsRdpClientAdvancedSettings6.MaxReconnectAttempts
- IMsRdpClientAdvancedSettings6.get_MaxReconnectAttempts
- IMsRdpClientAdvancedSettings6.put_MaxReconnectAttempts
- IMsRdpClientAdvancedSettings7.MaxReconnectAttempts
- IMsRdpClientAdvancedSettings7.get_MaxReconnectAttempts
- IMsRdpClientAdvancedSettings7.put_MaxReconnectAttempts
- IMsRdpClientAdvancedSettings8.MaxReconnectAttempts
- IMsRdpClientAdvancedSettings8.get_MaxReconnectAttempts
- IMsRdpClientAdvancedSettings8.put_MaxReconnectAttempts
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 322796a2d6ca6a13476dad58af8c385b8bdfa1fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681976"
---
# <a name="imsrdpclientadvancedsettings2maxreconnectattempts-property"></a><span data-ttu-id="bfed8-118">Свойство IMsRdpClientAdvancedSettings2:: Максреконнектаттемптс</span><span class="sxs-lookup"><span data-stu-id="bfed8-118">IMsRdpClientAdvancedSettings2::MaxReconnectAttempts property</span></span>

<span data-ttu-id="bfed8-119">Указывает количество повторных попыток подключения во время автоматического повторного подключения.</span><span class="sxs-lookup"><span data-stu-id="bfed8-119">Specifies the number of times to try to reconnect during automatic reconnection.</span></span>

<span data-ttu-id="bfed8-120">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="bfed8-120">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="bfed8-121">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bfed8-121">Syntax</span></span>


```C++
HRESULT put_MaxReconnectAttempts(
  [in]  LONG MaxReconnectAttempts
);

HRESULT get_MaxReconnectAttempts(
  [out] LONG *pMaxReconnectAttempts
);
```



## <a name="property-value"></a><span data-ttu-id="bfed8-122">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="bfed8-122">Property value</span></span>

<span data-ttu-id="bfed8-123">Новое число повторных попыток.</span><span class="sxs-lookup"><span data-stu-id="bfed8-123">The new number of retries.</span></span> <span data-ttu-id="bfed8-124">Допустимые значения: от 0 до 200 включительно.</span><span class="sxs-lookup"><span data-stu-id="bfed8-124">The valid values are 0 to 200, inclusive.</span></span>

## <a name="error-codes"></a><span data-ttu-id="bfed8-125">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="bfed8-125">Error codes</span></span>

<span data-ttu-id="bfed8-126">В случае успеха возвратите значение **\_ ОК** .</span><span class="sxs-lookup"><span data-stu-id="bfed8-126">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="bfed8-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bfed8-127">Remarks</span></span>

<span data-ttu-id="bfed8-128">Это свойство не может быть задано, если элемент управления подключен.</span><span class="sxs-lookup"><span data-stu-id="bfed8-128">This property cannot be set when the control is connected.</span></span>

<span data-ttu-id="bfed8-129">Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="bfed8-129">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bfed8-130">Требования</span><span class="sxs-lookup"><span data-stu-id="bfed8-130">Requirements</span></span>



| <span data-ttu-id="bfed8-131">Требование</span><span class="sxs-lookup"><span data-stu-id="bfed8-131">Requirement</span></span> | <span data-ttu-id="bfed8-132">Значение</span><span class="sxs-lookup"><span data-stu-id="bfed8-132">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bfed8-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bfed8-133">Minimum supported client</span></span><br/> | <span data-ttu-id="bfed8-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bfed8-134">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="bfed8-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bfed8-135">Minimum supported server</span></span><br/> | <span data-ttu-id="bfed8-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bfed8-136">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="bfed8-137">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="bfed8-137">Type library</span></span><br/>             | <dl> <span data-ttu-id="bfed8-138"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bfed8-138"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="bfed8-139">DLL</span><span class="sxs-lookup"><span data-stu-id="bfed8-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bfed8-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bfed8-140"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="bfed8-141">IID</span><span class="sxs-lookup"><span data-stu-id="bfed8-141">IID</span></span><br/>                      | <span data-ttu-id="bfed8-142">IID \_ IMsRdpClientAdvancedSettings2 определен как 9ac42117-2b76-4320-aa44-0e616ab8437b</span><span class="sxs-lookup"><span data-stu-id="bfed8-142">IID\_IMsRdpClientAdvancedSettings2 is defined as 9ac42117-2b76-4320-aa44-0e616ab8437b</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bfed8-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bfed8-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bfed8-144">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="bfed8-144">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="bfed8-145">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="bfed8-145">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="bfed8-146">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="bfed8-146">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="bfed8-147">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="bfed8-147">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="bfed8-148">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="bfed8-148">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="bfed8-149">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="bfed8-149">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="bfed8-150">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="bfed8-150">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> </dl>

 

 





