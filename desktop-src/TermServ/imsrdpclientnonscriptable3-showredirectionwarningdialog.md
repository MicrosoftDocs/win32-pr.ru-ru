---
title: IMsRdpClientNonScriptable3 Шовредиректионварнингдиалог, свойство
description: Указывает или получает, должно ли отображаться диалоговое окно предупреждения перенаправления.
ms.assetid: 7ed37288-77c3-4551-a553-1ca679e1047a
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Шовредиректионварнингдиалог
- Службы удаленных рабочих столов свойства Шовредиректионварнингдиалог, интерфейс IMsRdpClientNonScriptable3
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable3, свойство Шовредиректионварнингдиалог
- Службы удаленных рабочих столов свойства Шовредиректионварнингдиалог, интерфейс IMsRdpClientNonScriptable4
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable4, свойство Шовредиректионварнингдиалог
- Службы удаленных рабочих столов свойства Шовредиректионварнингдиалог, интерфейс IMsRdpClientNonScriptable5
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable5, свойство Шовредиректионварнингдиалог
- Службы удаленных рабочих столов свойства Шовредиректионварнингдиалог, объект MsRdpClient5
- Службы удаленных рабочих столов объекта MsRdpClient5, свойство Шовредиректионварнингдиалог
- Службы удаленных рабочих столов свойства Шовредиректионварнингдиалог, объект MsRdpClient6
- Службы удаленных рабочих столов объекта MsRdpClient6, свойство Шовредиректионварнингдиалог
- Службы удаленных рабочих столов свойства Шовредиректионварнингдиалог, объект MsRdpClient7
- Службы удаленных рабочих столов объекта MsRdpClient7, свойство Шовредиректионварнингдиалог
- Службы удаленных рабочих столов свойства Шовредиректионварнингдиалог, объект MsRdpClient8
- Службы удаленных рабочих столов объекта MsRdpClient8, свойство Шовредиректионварнингдиалог
- Службы удаленных рабочих столов свойства Шовредиректионварнингдиалог, объект MsRdpClient9
- Службы удаленных рабочих столов объекта MsRdpClient9, свойство Шовредиректионварнингдиалог
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.ShowRedirectionWarningDialog
- IMsRdpClientNonScriptable3.get_ShowRedirectionWarningDialog
- IMsRdpClientNonScriptable3.put_ShowRedirectionWarningDialog
- IMsRdpClientNonScriptable4.ShowRedirectionWarningDialog
- IMsRdpClientNonScriptable4.get_ShowRedirectionWarningDialog
- IMsRdpClientNonScriptable4.put_ShowRedirectionWarningDialog
- IMsRdpClientNonScriptable5.ShowRedirectionWarningDialog
- IMsRdpClientNonScriptable5.get_ShowRedirectionWarningDialog
- IMsRdpClientNonScriptable5.put_ShowRedirectionWarningDialog
- MsRdpClient5.ShowRedirectionWarningDialog
- MsRdpClient6.ShowRedirectionWarningDialog
- MsRdpClient7.ShowRedirectionWarningDialog
- MsRdpClient8.ShowRedirectionWarningDialog
- MsRdpClient9.ShowRedirectionWarningDialog
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 468e1721de3395067ca570c2051f3906df626071
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071346"
---
# <a name="imsrdpclientnonscriptable3showredirectionwarningdialog-property"></a><span data-ttu-id="1fe25-120">Свойство IMsRdpClientNonScriptable3:: Шовредиректионварнингдиалог</span><span class="sxs-lookup"><span data-stu-id="1fe25-120">IMsRdpClientNonScriptable3::ShowRedirectionWarningDialog property</span></span>

<span data-ttu-id="1fe25-121">Указывает или получает, должно ли отображаться диалоговое окно предупреждения перенаправления.</span><span class="sxs-lookup"><span data-stu-id="1fe25-121">Specifies or retrieves whether the redirection warning dialog box should be shown.</span></span>

<span data-ttu-id="1fe25-122">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="1fe25-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="1fe25-123">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1fe25-123">Syntax</span></span>


```C++
HRESULT put_ShowRedirectionWarningDialog(
  [in]  VARIANT_BOOL fShowRdrDlg
);

HRESULT get_ShowRedirectionWarningDialog(
  [out] VARIANT_BOOL *pfShowRdrDlg
);
```



## <a name="property-value"></a><span data-ttu-id="1fe25-124">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="1fe25-124">Property value</span></span>

<span data-ttu-id="1fe25-125">Указывает, следует ли отображать диалоговое окно "предупреждение перенаправления".</span><span class="sxs-lookup"><span data-stu-id="1fe25-125">Specifies whether the redirection warning dialog box should be shown.</span></span>

## <a name="requirements"></a><span data-ttu-id="1fe25-126">Требования</span><span class="sxs-lookup"><span data-stu-id="1fe25-126">Requirements</span></span>



| <span data-ttu-id="1fe25-127">Требование</span><span class="sxs-lookup"><span data-stu-id="1fe25-127">Requirement</span></span> | <span data-ttu-id="1fe25-128">Значение</span><span class="sxs-lookup"><span data-stu-id="1fe25-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="1fe25-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1fe25-129">Minimum supported client</span></span><br/> | <span data-ttu-id="1fe25-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1fe25-130">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="1fe25-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1fe25-131">Minimum supported server</span></span><br/> | <span data-ttu-id="1fe25-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1fe25-132">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="1fe25-133">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="1fe25-133">Type library</span></span><br/>             | <dl> <span data-ttu-id="1fe25-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1fe25-134"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="1fe25-135">DLL</span><span class="sxs-lookup"><span data-stu-id="1fe25-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1fe25-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1fe25-136"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="1fe25-137">IID</span><span class="sxs-lookup"><span data-stu-id="1fe25-137">IID</span></span><br/>                      | <span data-ttu-id="1fe25-138">IID \_ IMsRdpClientNonScriptable3 определен как b3378d90-0728-45c7-8ed7-b6159fb92219</span><span class="sxs-lookup"><span data-stu-id="1fe25-138">IID\_IMsRdpClientNonScriptable3 is defined as b3378d90-0728-45c7-8ed7-b6159fb92219</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1fe25-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1fe25-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1fe25-140">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="1fe25-140">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="1fe25-141">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="1fe25-141">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="1fe25-142">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="1fe25-142">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> </dl>

 

 





