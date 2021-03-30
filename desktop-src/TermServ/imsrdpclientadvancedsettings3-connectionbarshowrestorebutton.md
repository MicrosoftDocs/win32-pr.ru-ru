---
title: IMsRdpClientAdvancedSettings3 Коннектионбаршовресторебуттон, свойство
description: Указывает, следует ли отображать кнопку восстановить на панели подключения.
ms.assetid: a56c3c05-d253-404a-bf49-9c1d804802e0
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Коннектионбаршовресторебуттон
- Службы удаленных рабочих столов свойства Коннектионбаршовресторебуттон, интерфейс IMsRdpClientAdvancedSettings3
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings3, свойство Коннектионбаршовресторебуттон
- Службы удаленных рабочих столов свойства Коннектионбаршовресторебуттон, интерфейс IMsRdpClientAdvancedSettings4
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings4, свойство Коннектионбаршовресторебуттон
- Службы удаленных рабочих столов свойства Коннектионбаршовресторебуттон, интерфейс IMsRdpClientAdvancedSettings5
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings5, свойство Коннектионбаршовресторебуттон
- Службы удаленных рабочих столов свойства Коннектионбаршовресторебуттон, интерфейс IMsRdpClientAdvancedSettings6
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings6, свойство Коннектионбаршовресторебуттон
- Службы удаленных рабочих столов свойства Коннектионбаршовресторебуттон, интерфейс IMsRdpClientAdvancedSettings7
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings7, свойство Коннектионбаршовресторебуттон
- Службы удаленных рабочих столов свойства Коннектионбаршовресторебуттон, интерфейс IMsRdpClientAdvancedSettings8
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings8, свойство Коннектионбаршовресторебуттон
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings3.ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings3.get_ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings3.put_ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings4.ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings4.get_ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings4.put_ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings5.ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings5.get_ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings5.put_ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings6.ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings6.get_ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings6.put_ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings7.ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings7.get_ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings7.put_ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings8.ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings8.get_ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings8.put_ConnectionBarShowRestoreButton
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ae83ecde31461eff9c553782b8bfa3ae760fb54
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104414913"
---
# <a name="imsrdpclientadvancedsettings3connectionbarshowrestorebutton-property"></a><span data-ttu-id="9d6e4-116">Свойство IMsRdpClientAdvancedSettings3:: Коннектионбаршовресторебуттон</span><span class="sxs-lookup"><span data-stu-id="9d6e4-116">IMsRdpClientAdvancedSettings3::ConnectionBarShowRestoreButton property</span></span>

<span data-ttu-id="9d6e4-117">Указывает, следует ли отображать кнопку **восстановить** на панели подключения.</span><span class="sxs-lookup"><span data-stu-id="9d6e4-117">Specifies whether to display the **Restore** button on the connection bar.</span></span>

<span data-ttu-id="9d6e4-118">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="9d6e4-118">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d6e4-119">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9d6e4-119">Syntax</span></span>


```C++
HRESULT put_ConnectionBarShowRestoreButton(
  [in]  VARIANT_BOOL fShowRestore
);

HRESULT get_ConnectionBarShowRestoreButton(
  [out] VARIANT_BOOL *pfShowRestore
);
```



## <a name="property-value"></a><span data-ttu-id="9d6e4-120">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="9d6e4-120">Property value</span></span>

<span data-ttu-id="9d6e4-121">Задайте для параметра значение **\_ true** , чтобы отобразить кнопку **восстановить** , и значение **вариант \_ false** , чтобы отключить отображение кнопки **восстановить** .</span><span class="sxs-lookup"><span data-stu-id="9d6e4-121">Set to **VARIANT\_TRUE** to display the **Restore** button, and to **VARIANT\_FALSE** to disable the display of the **Restore** button.</span></span>

## <a name="error-codes"></a><span data-ttu-id="9d6e4-122">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="9d6e4-122">Error codes</span></span>

<span data-ttu-id="9d6e4-123">При успешном выполнении возвращает значение **\_ ОК** .</span><span class="sxs-lookup"><span data-stu-id="9d6e4-123">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="9d6e4-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9d6e4-124">Remarks</span></span>

<span data-ttu-id="9d6e4-125">Это свойство не может быть задано, пока элемент управления подключен.</span><span class="sxs-lookup"><span data-stu-id="9d6e4-125">This property cannot be set while the control is connected.</span></span>

<span data-ttu-id="9d6e4-126">Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="9d6e4-126">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9d6e4-127">Требования</span><span class="sxs-lookup"><span data-stu-id="9d6e4-127">Requirements</span></span>



| <span data-ttu-id="9d6e4-128">Требование</span><span class="sxs-lookup"><span data-stu-id="9d6e4-128">Requirement</span></span> | <span data-ttu-id="9d6e4-129">Значение</span><span class="sxs-lookup"><span data-stu-id="9d6e4-129">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d6e4-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9d6e4-130">Minimum supported client</span></span><br/> | <span data-ttu-id="9d6e4-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9d6e4-131">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="9d6e4-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9d6e4-132">Minimum supported server</span></span><br/> | <span data-ttu-id="9d6e4-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9d6e4-133">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="9d6e4-134">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="9d6e4-134">Type library</span></span><br/>             | <dl> <span data-ttu-id="9d6e4-135"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9d6e4-135"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="9d6e4-136">DLL</span><span class="sxs-lookup"><span data-stu-id="9d6e4-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9d6e4-137"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9d6e4-137"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="9d6e4-138">IID</span><span class="sxs-lookup"><span data-stu-id="9d6e4-138">IID</span></span><br/>                      | <span data-ttu-id="9d6e4-139">IID \_ IMsRdpClientAdvancedSettings3 определен как 19cd856b-C542-4c53-ACee-f127e3be1a59</span><span class="sxs-lookup"><span data-stu-id="9d6e4-139">IID\_IMsRdpClientAdvancedSettings3 is defined as 19cd856b-c542-4c53-acee-f127e3be1a59</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9d6e4-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9d6e4-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d6e4-141">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="9d6e4-141">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="9d6e4-142">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="9d6e4-142">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="9d6e4-143">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="9d6e4-143">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="9d6e4-144">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="9d6e4-144">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="9d6e4-145">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="9d6e4-145">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="9d6e4-146">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="9d6e4-146">**IMsRdpClientAdvancedSettings3**</span></span>](imsrdpclientadvancedsettings3.md)
</dt> </dl>

 

 





