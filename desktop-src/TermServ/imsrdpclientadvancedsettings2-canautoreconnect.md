---
title: IMsRdpClientAdvancedSettings2 Канаутореконнект, свойство
description: Указывает, может ли клиентский элемент управления автоматически подключаться к текущему сеансу в случае отключения от сети.
ms.assetid: 0a7ecf90-832b-4ec1-990b-7fe26ff134b1
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Канаутореконнект
- Службы удаленных рабочих столов свойства Канаутореконнект, интерфейс IMsRdpClientAdvancedSettings2
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings2, свойство Канаутореконнект
- Службы удаленных рабочих столов свойства Канаутореконнект, интерфейс IMsRdpClientAdvancedSettings3
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings3, свойство Канаутореконнект
- Службы удаленных рабочих столов свойства Канаутореконнект, интерфейс IMsRdpClientAdvancedSettings4
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings4, свойство Канаутореконнект
- Службы удаленных рабочих столов свойства Канаутореконнект, интерфейс IMsRdpClientAdvancedSettings5
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings5, свойство Канаутореконнект
- Службы удаленных рабочих столов свойства Канаутореконнект, интерфейс IMsRdpClientAdvancedSettings6
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings6, свойство Канаутореконнект
- Службы удаленных рабочих столов свойства Канаутореконнект, интерфейс IMsRdpClientAdvancedSettings7
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings7, свойство Канаутореконнект
- Службы удаленных рабочих столов свойства Канаутореконнект, интерфейс IMsRdpClientAdvancedSettings8
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings8, свойство Канаутореконнект
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings2.CanAutoReconnect
- IMsRdpClientAdvancedSettings2.get_CanAutoReconnect
- IMsRdpClientAdvancedSettings3.CanAutoReconnect
- IMsRdpClientAdvancedSettings3.get_CanAutoReconnect
- IMsRdpClientAdvancedSettings4.CanAutoReconnect
- IMsRdpClientAdvancedSettings4.get_CanAutoReconnect
- IMsRdpClientAdvancedSettings5.CanAutoReconnect
- IMsRdpClientAdvancedSettings5.get_CanAutoReconnect
- IMsRdpClientAdvancedSettings6.CanAutoReconnect
- IMsRdpClientAdvancedSettings6.get_CanAutoReconnect
- IMsRdpClientAdvancedSettings7.CanAutoReconnect
- IMsRdpClientAdvancedSettings7.get_CanAutoReconnect
- IMsRdpClientAdvancedSettings8.CanAutoReconnect
- IMsRdpClientAdvancedSettings8.get_CanAutoReconnect
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d8c8f4113c39b79783978252136c50d2111ed0c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891461"
---
# <a name="imsrdpclientadvancedsettings2canautoreconnect-property"></a><span data-ttu-id="99369-118">Свойство IMsRdpClientAdvancedSettings2:: Канаутореконнект</span><span class="sxs-lookup"><span data-stu-id="99369-118">IMsRdpClientAdvancedSettings2::CanAutoReconnect property</span></span>

<span data-ttu-id="99369-119">Указывает, может ли клиентский элемент управления автоматически подключаться к текущему сеансу в случае отключения от сети.</span><span class="sxs-lookup"><span data-stu-id="99369-119">Specifies whether the client control is able to reconnect automatically to the current session in the event of a network disconnection.</span></span>

<span data-ttu-id="99369-120">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="99369-120">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="99369-121">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="99369-121">Syntax</span></span>


```C++
HRESULT get_CanAutoReconnect(
  [out] VARIANT_BOOL *pfCanAutoReconnect
);
```



## <a name="property-value"></a><span data-ttu-id="99369-122">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="99369-122">Property value</span></span>

<span data-ttu-id="99369-123">Получает **вариант \_ true** , если элемент управления может автоматически повторно подключиться, и **вариант \_ false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="99369-123">Receives **VARIANT\_TRUE** if the control is able to automatically reconnect, and **VARIANT\_FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="99369-124">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="99369-124">Error codes</span></span>

<span data-ttu-id="99369-125">В случае успеха возвратите значение **\_ ОК** .</span><span class="sxs-lookup"><span data-stu-id="99369-125">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="99369-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="99369-126">Remarks</span></span>

<span data-ttu-id="99369-127">Ситуации, в которых автоматическое повторное подключение может не быть включено, включают те, в которых администратор использует групповую политику для отключения аутореконнектион и устаревшие среды, не поддерживающие автоматическое повторное подключение.</span><span class="sxs-lookup"><span data-stu-id="99369-127">Situations in which automatic reconnection might not be enabled include those in which an administrator uses group policy to disable autoreconnection, and legacy environments that do not support automatic reconnection.</span></span>

<span data-ttu-id="99369-128">Это свойство не может быть задано, если элемент управления подключен.</span><span class="sxs-lookup"><span data-stu-id="99369-128">This property cannot be set when the control is connected.</span></span>

<span data-ttu-id="99369-129">Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="99369-129">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="99369-130">Требования</span><span class="sxs-lookup"><span data-stu-id="99369-130">Requirements</span></span>



| <span data-ttu-id="99369-131">Требование</span><span class="sxs-lookup"><span data-stu-id="99369-131">Requirement</span></span> | <span data-ttu-id="99369-132">Значение</span><span class="sxs-lookup"><span data-stu-id="99369-132">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="99369-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="99369-133">Minimum supported client</span></span><br/> | <span data-ttu-id="99369-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="99369-134">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="99369-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="99369-135">Minimum supported server</span></span><br/> | <span data-ttu-id="99369-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="99369-136">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="99369-137">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="99369-137">Type library</span></span><br/>             | <dl> <span data-ttu-id="99369-138"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="99369-138"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="99369-139">DLL</span><span class="sxs-lookup"><span data-stu-id="99369-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="99369-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="99369-140"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="99369-141">IID</span><span class="sxs-lookup"><span data-stu-id="99369-141">IID</span></span><br/>                      | <span data-ttu-id="99369-142">IID \_ IMsRdpClientAdvancedSettings2 определен как 9ac42117-2b76-4320-aa44-0e616ab8437b</span><span class="sxs-lookup"><span data-stu-id="99369-142">IID\_IMsRdpClientAdvancedSettings2 is defined as 9ac42117-2b76-4320-aa44-0e616ab8437b</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="99369-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="99369-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99369-144">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="99369-144">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="99369-145">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="99369-145">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="99369-146">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="99369-146">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="99369-147">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="99369-147">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="99369-148">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="99369-148">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="99369-149">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="99369-149">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="99369-150">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="99369-150">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> </dl>

 

 





