---
title: IMsRdpClientNonScriptable3 Варнабаутклипбоардредиректион, свойство
description: Указывает, следует ли отображать диалоговое окно "предупреждение системы безопасности", чтобы предупредить пользователей о перенаправлении буфера обмена.
ms.assetid: 2f3ca58b-3c89-4251-ae15-2c0aaf308893
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Варнабаутклипбоардредиректион
- Службы удаленных рабочих столов свойства Варнабаутклипбоардредиректион, интерфейс IMsRdpClientNonScriptable3
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable3, свойство Варнабаутклипбоардредиректион
- Службы удаленных рабочих столов свойства Варнабаутклипбоардредиректион, интерфейс IMsRdpClientNonScriptable4
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable4, свойство Варнабаутклипбоардредиректион
- Службы удаленных рабочих столов свойства Варнабаутклипбоардредиректион, интерфейс IMsRdpClientNonScriptable5
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable5, свойство Варнабаутклипбоардредиректион
- Службы удаленных рабочих столов свойства Варнабаутклипбоардредиректион, объект MsRdpClient5
- Службы удаленных рабочих столов объекта MsRdpClient5, свойство Варнабаутклипбоардредиректион
- Службы удаленных рабочих столов свойства Варнабаутклипбоардредиректион, объект MsRdpClient6
- Службы удаленных рабочих столов объекта MsRdpClient6, свойство Варнабаутклипбоардредиректион
- Службы удаленных рабочих столов свойства Варнабаутклипбоардредиректион, объект MsRdpClient7
- Службы удаленных рабочих столов объекта MsRdpClient7, свойство Варнабаутклипбоардредиректион
- Службы удаленных рабочих столов свойства Варнабаутклипбоардредиректион, объект MsRdpClient8
- Службы удаленных рабочих столов объекта MsRdpClient8, свойство Варнабаутклипбоардредиректион
- Службы удаленных рабочих столов свойства Варнабаутклипбоардредиректион, объект MsRdpClient9
- Службы удаленных рабочих столов объекта MsRdpClient9, свойство Варнабаутклипбоардредиректион
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.WarnAboutClipboardRedirection
- IMsRdpClientNonScriptable3.get_WarnAboutClipboardRedirection
- IMsRdpClientNonScriptable3.put_WarnAboutClipboardRedirection
- IMsRdpClientNonScriptable4.WarnAboutClipboardRedirection
- IMsRdpClientNonScriptable4.get_WarnAboutClipboardRedirection
- IMsRdpClientNonScriptable4.put_WarnAboutClipboardRedirection
- IMsRdpClientNonScriptable5.WarnAboutClipboardRedirection
- IMsRdpClientNonScriptable5.get_WarnAboutClipboardRedirection
- IMsRdpClientNonScriptable5.put_WarnAboutClipboardRedirection
- MsRdpClient5.WarnAboutClipboardRedirection
- MsRdpClient6.WarnAboutClipboardRedirection
- MsRdpClient7.WarnAboutClipboardRedirection
- MsRdpClient8.WarnAboutClipboardRedirection
- MsRdpClient9.WarnAboutClipboardRedirection
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8da6fa2f7fb36a110666c8b14a818264813d816
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104533932"
---
# <a name="imsrdpclientnonscriptable3warnaboutclipboardredirection-property"></a><span data-ttu-id="e9d69-120">Свойство IMsRdpClientNonScriptable3:: Варнабаутклипбоардредиректион</span><span class="sxs-lookup"><span data-stu-id="e9d69-120">IMsRdpClientNonScriptable3::WarnAboutClipboardRedirection property</span></span>

<span data-ttu-id="e9d69-121">Указывает, следует ли отображать диалоговое окно "предупреждение системы безопасности", чтобы предупредить пользователей о перенаправлении буфера обмена.</span><span class="sxs-lookup"><span data-stu-id="e9d69-121">Specifies or retrieves whether the security warning dialog box should be displayed to warn users about clipboard redirection.</span></span>

<span data-ttu-id="e9d69-122">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="e9d69-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9d69-123">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e9d69-123">Syntax</span></span>


```C++
HRESULT put_WarnAboutClipboardRedirection(
  [in]  VARIANT_BOOL fWarn
);

HRESULT get_WarnAboutClipboardRedirection(
  [out] VARIANT_BOOL *pfWarn
);
```



## <a name="property-value"></a><span data-ttu-id="e9d69-124">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="e9d69-124">Property value</span></span>

<span data-ttu-id="e9d69-125">Указывает, следует ли отображать диалоговое окно "предупреждение системы безопасности", чтобы предупредить пользователей о перенаправлении буфера обмена.</span><span class="sxs-lookup"><span data-stu-id="e9d69-125">Specifies whether the security warning dialog box should be displayed to warn users about clipboard redirection.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9d69-126">Требования</span><span class="sxs-lookup"><span data-stu-id="e9d69-126">Requirements</span></span>



| <span data-ttu-id="e9d69-127">Требование</span><span class="sxs-lookup"><span data-stu-id="e9d69-127">Requirement</span></span> | <span data-ttu-id="e9d69-128">Значение</span><span class="sxs-lookup"><span data-stu-id="e9d69-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9d69-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e9d69-129">Minimum supported client</span></span><br/> | <span data-ttu-id="e9d69-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e9d69-130">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="e9d69-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e9d69-131">Minimum supported server</span></span><br/> | <span data-ttu-id="e9d69-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e9d69-132">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="e9d69-133">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="e9d69-133">Type library</span></span><br/>             | <dl> <span data-ttu-id="e9d69-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e9d69-134"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="e9d69-135">DLL</span><span class="sxs-lookup"><span data-stu-id="e9d69-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e9d69-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e9d69-136"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="e9d69-137">IID</span><span class="sxs-lookup"><span data-stu-id="e9d69-137">IID</span></span><br/>                      | <span data-ttu-id="e9d69-138">IID \_ IMsRdpClientNonScriptable3 определен как b3378d90-0728-45c7-8ed7-b6159fb92219</span><span class="sxs-lookup"><span data-stu-id="e9d69-138">IID\_IMsRdpClientNonScriptable3 is defined as b3378d90-0728-45c7-8ed7-b6159fb92219</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e9d69-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e9d69-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9d69-140">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="e9d69-140">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="e9d69-141">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="e9d69-141">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="e9d69-142">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="e9d69-142">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> </dl>

 

 





