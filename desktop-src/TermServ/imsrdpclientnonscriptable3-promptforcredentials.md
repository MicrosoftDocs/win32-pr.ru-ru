---
title: Свойство Промптфоркредентиалс IMsRdpClientNonScriptable3 (Вуапи. h)
description: Указывает или получает значение, указывающее, включено ли диалоговое окно Запрос учетных данных для подключения.
ms.assetid: 252ec5bd-bd52-40d4-ae48-b2c00c0720c0
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Промптфоркредентиалс
- Службы удаленных рабочих столов свойства Промптфоркредентиалс, интерфейс IMsRdpClientNonScriptable3
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable3, свойство Промптфоркредентиалс
- Службы удаленных рабочих столов свойства Промптфоркредентиалс, интерфейс IMsRdpClientNonScriptable4
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable4, свойство Промптфоркредентиалс
- Службы удаленных рабочих столов свойства Промптфоркредентиалс, интерфейс IMsRdpClientNonScriptable5
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable5, свойство Промптфоркредентиалс
- Службы удаленных рабочих столов свойства Промптфоркредентиалс, объект MsRdpClient5
- Службы удаленных рабочих столов объекта MsRdpClient5, свойство Промптфоркредентиалс
- Службы удаленных рабочих столов свойства Промптфоркредентиалс, объект MsRdpClient6
- Службы удаленных рабочих столов объекта MsRdpClient6, свойство Промптфоркредентиалс
- Службы удаленных рабочих столов свойства Промптфоркредентиалс, объект MsRdpClient7
- Службы удаленных рабочих столов объекта MsRdpClient7, свойство Промптфоркредентиалс
- Службы удаленных рабочих столов свойства Промптфоркредентиалс, объект MsRdpClient8
- Службы удаленных рабочих столов объекта MsRdpClient8, свойство Промптфоркредентиалс
- Службы удаленных рабочих столов свойства Промптфоркредентиалс, объект MsRdpClient9
- Службы удаленных рабочих столов объекта MsRdpClient9, свойство Промптфоркредентиалс
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.PromptForCredentials
- IMsRdpClientNonScriptable3.get_PromptForCredentials
- IMsRdpClientNonScriptable3.put_PromptForCredentials
- IMsRdpClientNonScriptable4.PromptForCredentials
- IMsRdpClientNonScriptable4.get_PromptForCredentials
- IMsRdpClientNonScriptable4.put_PromptForCredentials
- IMsRdpClientNonScriptable5.PromptForCredentials
- IMsRdpClientNonScriptable5.get_PromptForCredentials
- IMsRdpClientNonScriptable5.put_PromptForCredentials
- MsRdpClient5.PromptForCredentials
- MsRdpClient6.PromptForCredentials
- MsRdpClient7.PromptForCredentials
- MsRdpClient8.PromptForCredentials
- MsRdpClient9.PromptForCredentials
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62f913937c9a2ff01d4aabeaba48dcbdc8ddb21d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340370"
---
# <a name="imsrdpclientnonscriptable3promptforcredentials-property"></a><span data-ttu-id="fdd1e-120">IMsRdpClientNonScriptable3: свойство Ромптфоркредентиалс:P</span><span class="sxs-lookup"><span data-stu-id="fdd1e-120">IMsRdpClientNonScriptable3::PromptForCredentials property</span></span>

<span data-ttu-id="fdd1e-121">Указывает или получает значение, указывающее, включено ли диалоговое окно Запрос учетных данных для подключения.</span><span class="sxs-lookup"><span data-stu-id="fdd1e-121">Specifies or retrieves whether the prompt for credentials dialog is enabled for the connection.</span></span>

<span data-ttu-id="fdd1e-122">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="fdd1e-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="fdd1e-123">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fdd1e-123">Syntax</span></span>


```C++
HRESULT put_PromptForCredentials(
  [in]  VARIANT_BOOL fPrompt
);

HRESULT get_PromptForCredentials(
  [out] VARIANT_BOOL *pfPrompt
);
```



## <a name="property-value"></a><span data-ttu-id="fdd1e-124">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="fdd1e-124">Property value</span></span>

<span data-ttu-id="fdd1e-125">Указывает, включено ли диалоговое окно Запрос учетных данных для подключения.</span><span class="sxs-lookup"><span data-stu-id="fdd1e-125">Specifies whether the prompt for credentials dialog is enabled for the connection.</span></span>

## <a name="error-codes"></a><span data-ttu-id="fdd1e-126">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="fdd1e-126">Error codes</span></span>

## <a name="requirements"></a><span data-ttu-id="fdd1e-127">Требования</span><span class="sxs-lookup"><span data-stu-id="fdd1e-127">Requirements</span></span>



| <span data-ttu-id="fdd1e-128">Требование</span><span class="sxs-lookup"><span data-stu-id="fdd1e-128">Requirement</span></span> | <span data-ttu-id="fdd1e-129">Значение</span><span class="sxs-lookup"><span data-stu-id="fdd1e-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="fdd1e-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fdd1e-130">Minimum supported client</span></span><br/> | <span data-ttu-id="fdd1e-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fdd1e-131">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="fdd1e-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fdd1e-132">Minimum supported server</span></span><br/> | <span data-ttu-id="fdd1e-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fdd1e-133">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="fdd1e-134">Header</span><span class="sxs-lookup"><span data-stu-id="fdd1e-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="fdd1e-135"><dt>Вуапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="fdd1e-135"><dt>Wuapi.h</dt></span></span> </dl>            |
| <span data-ttu-id="fdd1e-136">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="fdd1e-136">Type library</span></span><br/>             | <dl> <span data-ttu-id="fdd1e-137"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fdd1e-137"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="fdd1e-138">DLL</span><span class="sxs-lookup"><span data-stu-id="fdd1e-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fdd1e-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fdd1e-139"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="fdd1e-140">IID</span><span class="sxs-lookup"><span data-stu-id="fdd1e-140">IID</span></span><br/>                      | <span data-ttu-id="fdd1e-141">IID \_ IMsRdpClientNonScriptable3 определен как b3378d90-0728-45c7-8ed7-b6159fb92219</span><span class="sxs-lookup"><span data-stu-id="fdd1e-141">IID\_IMsRdpClientNonScriptable3 is defined as b3378d90-0728-45c7-8ed7-b6159fb92219</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fdd1e-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fdd1e-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fdd1e-143">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="fdd1e-143">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="fdd1e-144">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="fdd1e-144">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="fdd1e-145">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="fdd1e-145">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> </dl>

 

 





