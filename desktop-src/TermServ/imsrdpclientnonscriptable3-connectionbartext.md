---
title: IMsRdpClientNonScriptable3 Коннектионбартекст, свойство
description: Задает или получает текст для обновления панели подключения.
ms.assetid: 9671118d-ee7c-4077-be81-57655aff5e35
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Коннектионбартекст
- Службы удаленных рабочих столов свойства Коннектионбартекст, интерфейс IMsRdpClientNonScriptable3
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable3, свойство Коннектионбартекст
- Службы удаленных рабочих столов свойства Коннектионбартекст, интерфейс IMsRdpClientNonScriptable4
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable4, свойство Коннектионбартекст
- Службы удаленных рабочих столов свойства Коннектионбартекст, интерфейс IMsRdpClientNonScriptable5
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable5, свойство Коннектионбартекст
- Службы удаленных рабочих столов свойства Коннектионбартекст, объект MsRdpClient5
- Службы удаленных рабочих столов объекта MsRdpClient5, свойство Коннектионбартекст
- Службы удаленных рабочих столов свойства Коннектионбартекст, объект MsRdpClient6
- Службы удаленных рабочих столов объекта MsRdpClient6, свойство Коннектионбартекст
- Службы удаленных рабочих столов свойства Коннектионбартекст, объект MsRdpClient7
- Службы удаленных рабочих столов объекта MsRdpClient7, свойство Коннектионбартекст
- Службы удаленных рабочих столов свойства Коннектионбартекст, объект MsRdpClient8
- Службы удаленных рабочих столов объекта MsRdpClient8, свойство Коннектионбартекст
- Службы удаленных рабочих столов свойства Коннектионбартекст, объект MsRdpClient9
- Службы удаленных рабочих столов объекта MsRdpClient9, свойство Коннектионбартекст
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.ConnectionBarText
- IMsRdpClientNonScriptable3.get_ConnectionBarText
- IMsRdpClientNonScriptable3.put_ConnectionBarText
- IMsRdpClientNonScriptable4.ConnectionBarText
- IMsRdpClientNonScriptable4.get_ConnectionBarText
- IMsRdpClientNonScriptable4.put_ConnectionBarText
- IMsRdpClientNonScriptable5.ConnectionBarText
- IMsRdpClientNonScriptable5.get_ConnectionBarText
- IMsRdpClientNonScriptable5.put_ConnectionBarText
- MsRdpClient5.ConnectionBarText
- MsRdpClient6.ConnectionBarText
- MsRdpClient7.ConnectionBarText
- MsRdpClient8.ConnectionBarText
- MsRdpClient9.ConnectionBarText
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76819dd28ffd8b2ee5e2dfb30017e341dd49db5b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803622"
---
# <a name="imsrdpclientnonscriptable3connectionbartext-property"></a><span data-ttu-id="fd2c4-120">Свойство IMsRdpClientNonScriptable3:: Коннектионбартекст</span><span class="sxs-lookup"><span data-stu-id="fd2c4-120">IMsRdpClientNonScriptable3::ConnectionBarText property</span></span>

<span data-ttu-id="fd2c4-121">Задает или получает текст для обновления панели подключения.</span><span class="sxs-lookup"><span data-stu-id="fd2c4-121">Sets or retrieves the text to update the connection bar.</span></span>

<span data-ttu-id="fd2c4-122">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="fd2c4-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd2c4-123">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fd2c4-123">Syntax</span></span>


```C++
HRESULT put_ConnectionBarText(
  [in]  BSTR newVal
);

HRESULT get_ConnectionBarText(
  [out] BSTR *pConnectionBarText
);
```



## <a name="property-value"></a><span data-ttu-id="fd2c4-124">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="fd2c4-124">Property value</span></span>

<span data-ttu-id="fd2c4-125">Задает текстовую строку, отображаемую на панели подключения.</span><span class="sxs-lookup"><span data-stu-id="fd2c4-125">Sets the text string to display on the connection bar.</span></span>

## <a name="remarks"></a><span data-ttu-id="fd2c4-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fd2c4-126">Remarks</span></span>

<span data-ttu-id="fd2c4-127">Необходимо вызвать метод **IMsRdpClientNonScriptable3::p UT \_ коннектионбартекст** перед вызовом метода [**имстсксекуредсеттингс::p UT \_**](imstscsecuredsettings-fullscreen.md) , а также метода [**имсрдпклиент::p UT \_**](imsrdpclient-fullscreen.md) .</span><span class="sxs-lookup"><span data-stu-id="fd2c4-127">You must call the **IMsRdpClientNonScriptable3::put\_ConnectionBarText** method before you call the [**IMsTscSecuredSettings::put\_Fullscreen**](imstscsecuredsettings-fullscreen.md) method or the [**IMsRdpClient::put\_Fullscreen**](imsrdpclient-fullscreen.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd2c4-128">Требования</span><span class="sxs-lookup"><span data-stu-id="fd2c4-128">Requirements</span></span>



| <span data-ttu-id="fd2c4-129">Требование</span><span class="sxs-lookup"><span data-stu-id="fd2c4-129">Requirement</span></span> | <span data-ttu-id="fd2c4-130">Значение</span><span class="sxs-lookup"><span data-stu-id="fd2c4-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd2c4-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fd2c4-131">Minimum supported client</span></span><br/> | <span data-ttu-id="fd2c4-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fd2c4-132">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="fd2c4-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fd2c4-133">Minimum supported server</span></span><br/> | <span data-ttu-id="fd2c4-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fd2c4-134">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="fd2c4-135">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="fd2c4-135">Type library</span></span><br/>             | <dl> <span data-ttu-id="fd2c4-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fd2c4-136"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="fd2c4-137">DLL</span><span class="sxs-lookup"><span data-stu-id="fd2c4-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fd2c4-138"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fd2c4-138"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="fd2c4-139">IID</span><span class="sxs-lookup"><span data-stu-id="fd2c4-139">IID</span></span><br/>                      | <span data-ttu-id="fd2c4-140">IID \_ IMsRdpClientNonScriptable3 определен как b3378d90-0728-45c7-8ed7-b6159fb92219</span><span class="sxs-lookup"><span data-stu-id="fd2c4-140">IID\_IMsRdpClientNonScriptable3 is defined as b3378d90-0728-45c7-8ed7-b6159fb92219</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fd2c4-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fd2c4-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd2c4-142">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="fd2c4-142">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="fd2c4-143">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="fd2c4-143">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="fd2c4-144">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="fd2c4-144">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> </dl>

 

 





