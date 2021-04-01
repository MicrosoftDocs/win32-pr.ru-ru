---
title: IMsRdpClientAdvancedSettings3 Коннектионбаршовминимизебуттон, свойство
description: Указывает, отображать ли кнопку сворачивания на панели подключения.
ms.assetid: 3ad89f25-f1ff-4bfc-ae86-09603058c9b5
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Коннектионбаршовминимизебуттон
- Службы удаленных рабочих столов свойства Коннектионбаршовминимизебуттон, интерфейс IMsRdpClientAdvancedSettings3
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings3, свойство Коннектионбаршовминимизебуттон
- Службы удаленных рабочих столов свойства Коннектионбаршовминимизебуттон, интерфейс IMsRdpClientAdvancedSettings4
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings4, свойство Коннектионбаршовминимизебуттон
- Службы удаленных рабочих столов свойства Коннектионбаршовминимизебуттон, интерфейс IMsRdpClientAdvancedSettings5
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings5, свойство Коннектионбаршовминимизебуттон
- Службы удаленных рабочих столов свойства Коннектионбаршовминимизебуттон, интерфейс IMsRdpClientAdvancedSettings6
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings6, свойство Коннектионбаршовминимизебуттон
- Службы удаленных рабочих столов свойства Коннектионбаршовминимизебуттон, интерфейс IMsRdpClientAdvancedSettings7
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings7, свойство Коннектионбаршовминимизебуттон
- Службы удаленных рабочих столов свойства Коннектионбаршовминимизебуттон, интерфейс IMsRdpClientAdvancedSettings8
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings8, свойство Коннектионбаршовминимизебуттон
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings3.ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings3.get_ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings3.put_ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings4.ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings4.get_ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings4.put_ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings5.ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings5.get_ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings5.put_ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings6.ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings6.get_ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings6.put_ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings7.ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings7.get_ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings7.put_ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings8.ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings8.get_ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings8.put_ConnectionBarShowMinimizeButton
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc3cb600a853e4bc2dea7c693e676f992db85f48
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801157"
---
# <a name="imsrdpclientadvancedsettings3connectionbarshowminimizebutton-property"></a><span data-ttu-id="ddefc-116">Свойство IMsRdpClientAdvancedSettings3:: Коннектионбаршовминимизебуттон</span><span class="sxs-lookup"><span data-stu-id="ddefc-116">IMsRdpClientAdvancedSettings3::ConnectionBarShowMinimizeButton property</span></span>

<span data-ttu-id="ddefc-117">Указывает, отображать ли кнопку **сворачивания** на панели подключения.</span><span class="sxs-lookup"><span data-stu-id="ddefc-117">Specifies whether to display the **Minimize** button on the connection bar.</span></span>

<span data-ttu-id="ddefc-118">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="ddefc-118">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="ddefc-119">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ddefc-119">Syntax</span></span>


```C++
HRESULT put_ConnectionBarShowMinimizeButton(
  [in]  VARIANT_BOOL fShowMinimize
);

HRESULT get_ConnectionBarShowMinimizeButton(
  [out] VARIANT_BOOL *pfShowMinimize
);
```



## <a name="property-value"></a><span data-ttu-id="ddefc-120">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="ddefc-120">Property value</span></span>

<span data-ttu-id="ddefc-121">Присвойте этому параметру значение **\_ true** , чтобы отобразить кнопку **сворачивания** , и значение **Variant \_ false** , чтобы отключить отображение кнопки **сворачивания** .</span><span class="sxs-lookup"><span data-stu-id="ddefc-121">Set this parameter to **VARIANT\_TRUE** to display the **Minimize** button, and to **VARIANT\_FALSE** to disable the display of the **Minimize** button.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ddefc-122">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="ddefc-122">Error codes</span></span>

<span data-ttu-id="ddefc-123">При успешном выполнении возвращает значение **\_ ОК** .</span><span class="sxs-lookup"><span data-stu-id="ddefc-123">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="ddefc-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ddefc-124">Remarks</span></span>

<span data-ttu-id="ddefc-125">Это свойство не может быть задано, пока элемент управления подключен.</span><span class="sxs-lookup"><span data-stu-id="ddefc-125">This property cannot be set while the control is connected.</span></span>

<span data-ttu-id="ddefc-126">Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="ddefc-126">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ddefc-127">Требования</span><span class="sxs-lookup"><span data-stu-id="ddefc-127">Requirements</span></span>



| <span data-ttu-id="ddefc-128">Требование</span><span class="sxs-lookup"><span data-stu-id="ddefc-128">Requirement</span></span> | <span data-ttu-id="ddefc-129">Значение</span><span class="sxs-lookup"><span data-stu-id="ddefc-129">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ddefc-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ddefc-130">Minimum supported client</span></span><br/> | <span data-ttu-id="ddefc-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ddefc-131">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="ddefc-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ddefc-132">Minimum supported server</span></span><br/> | <span data-ttu-id="ddefc-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ddefc-133">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="ddefc-134">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="ddefc-134">Type library</span></span><br/>             | <dl> <span data-ttu-id="ddefc-135"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ddefc-135"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="ddefc-136">DLL</span><span class="sxs-lookup"><span data-stu-id="ddefc-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ddefc-137"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ddefc-137"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="ddefc-138">IID</span><span class="sxs-lookup"><span data-stu-id="ddefc-138">IID</span></span><br/>                      | <span data-ttu-id="ddefc-139">IID \_ IMsRdpClientAdvancedSettings3 определен как 19cd856b-C542-4c53-ACee-f127e3be1a59</span><span class="sxs-lookup"><span data-stu-id="ddefc-139">IID\_IMsRdpClientAdvancedSettings3 is defined as 19cd856b-c542-4c53-acee-f127e3be1a59</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ddefc-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ddefc-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ddefc-141">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="ddefc-141">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="ddefc-142">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="ddefc-142">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="ddefc-143">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="ddefc-143">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="ddefc-144">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="ddefc-144">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="ddefc-145">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="ddefc-145">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="ddefc-146">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="ddefc-146">**IMsRdpClientAdvancedSettings3**</span></span>](imsrdpclientadvancedsettings3.md)
</dt> </dl>

 

 





