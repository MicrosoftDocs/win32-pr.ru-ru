---
title: IMsRdpClientNonScriptable3 Варнабаутсендингкредентиалс, свойство
description: Указывает или получает значение, указывающее, должно ли диалоговое окно "предупреждение системы безопасности" включать предупреждение об отправке учетных данных на удаленный сервер перед запуском сеанса.
ms.assetid: b97baef5-4a51-4e5c-bd53-10cff175533c
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Варнабаутсендингкредентиалс
- Службы удаленных рабочих столов свойства Варнабаутсендингкредентиалс, интерфейс IMsRdpClientNonScriptable3
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable3, свойство Варнабаутсендингкредентиалс
- Службы удаленных рабочих столов свойства Варнабаутсендингкредентиалс, интерфейс IMsRdpClientNonScriptable4
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable4, свойство Варнабаутсендингкредентиалс
- Службы удаленных рабочих столов свойства Варнабаутсендингкредентиалс, интерфейс IMsRdpClientNonScriptable5
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable5, свойство Варнабаутсендингкредентиалс
- Службы удаленных рабочих столов свойства Варнабаутсендингкредентиалс, объект MsRdpClient5
- Службы удаленных рабочих столов объекта MsRdpClient5, свойство Варнабаутсендингкредентиалс
- Службы удаленных рабочих столов свойства Варнабаутсендингкредентиалс, объект MsRdpClient6
- Службы удаленных рабочих столов объекта MsRdpClient6, свойство Варнабаутсендингкредентиалс
- Службы удаленных рабочих столов свойства Варнабаутсендингкредентиалс, объект MsRdpClient7
- Службы удаленных рабочих столов объекта MsRdpClient7, свойство Варнабаутсендингкредентиалс
- Службы удаленных рабочих столов свойства Варнабаутсендингкредентиалс, объект MsRdpClient8
- Службы удаленных рабочих столов объекта MsRdpClient8, свойство Варнабаутсендингкредентиалс
- Службы удаленных рабочих столов свойства Варнабаутсендингкредентиалс, объект MsRdpClient9
- Службы удаленных рабочих столов объекта MsRdpClient9, свойство Варнабаутсендингкредентиалс
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.WarnAboutSendingCredentials
- IMsRdpClientNonScriptable3.get_WarnAboutSendingCredentials
- IMsRdpClientNonScriptable3.put_WarnAboutSendingCredentials
- IMsRdpClientNonScriptable4.WarnAboutSendingCredentials
- IMsRdpClientNonScriptable4.get_WarnAboutSendingCredentials
- IMsRdpClientNonScriptable4.put_WarnAboutSendingCredentials
- IMsRdpClientNonScriptable5.WarnAboutSendingCredentials
- IMsRdpClientNonScriptable5.get_WarnAboutSendingCredentials
- IMsRdpClientNonScriptable5.put_WarnAboutSendingCredentials
- MsRdpClient5.WarnAboutSendingCredentials
- MsRdpClient6.WarnAboutSendingCredentials
- MsRdpClient7.WarnAboutSendingCredentials
- MsRdpClient8.WarnAboutSendingCredentials
- MsRdpClient9.WarnAboutSendingCredentials
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29d9d2fcfe158f5a0bb6812002bfcc160f1c9009
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681832"
---
# <a name="imsrdpclientnonscriptable3warnaboutsendingcredentials-property"></a><span data-ttu-id="10852-120">Свойство IMsRdpClientNonScriptable3:: Варнабаутсендингкредентиалс</span><span class="sxs-lookup"><span data-stu-id="10852-120">IMsRdpClientNonScriptable3::WarnAboutSendingCredentials property</span></span>

<span data-ttu-id="10852-121">Указывает или получает значение, указывающее, должно ли диалоговое окно "предупреждение системы безопасности" включать предупреждение об отправке учетных данных на удаленный сервер перед запуском сеанса.</span><span class="sxs-lookup"><span data-stu-id="10852-121">Specifies or retrieves whether the security warning dialog box should include a warning about sending credentials to the remote server before starting a session.</span></span>

<span data-ttu-id="10852-122">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="10852-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="10852-123">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="10852-123">Syntax</span></span>


```C++
HRESULT put_WarnAboutSendingCredentials(
  [in]  VARIANT_BOOL fWarn
);

HRESULT get_WarnAboutSendingCredentials(
  [out] VARIANT_BOOL *pfWarn
);
```



## <a name="property-value"></a><span data-ttu-id="10852-124">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="10852-124">Property value</span></span>

<span data-ttu-id="10852-125">Указывает, должно ли диалоговое окно предупреждения системы безопасности включать предупреждение об отправке учетных данных на удаленный сервер перед запуском сеанса.</span><span class="sxs-lookup"><span data-stu-id="10852-125">Specifies whether the security warning dialog box should include a warning about sending credentials to the remote server before starting a session.</span></span>

## <a name="requirements"></a><span data-ttu-id="10852-126">Требования</span><span class="sxs-lookup"><span data-stu-id="10852-126">Requirements</span></span>



| <span data-ttu-id="10852-127">Требование</span><span class="sxs-lookup"><span data-stu-id="10852-127">Requirement</span></span> | <span data-ttu-id="10852-128">Значение</span><span class="sxs-lookup"><span data-stu-id="10852-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="10852-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="10852-129">Minimum supported client</span></span><br/> | <span data-ttu-id="10852-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="10852-130">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="10852-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="10852-131">Minimum supported server</span></span><br/> | <span data-ttu-id="10852-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="10852-132">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="10852-133">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="10852-133">Type library</span></span><br/>             | <dl> <span data-ttu-id="10852-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="10852-134"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="10852-135">DLL</span><span class="sxs-lookup"><span data-stu-id="10852-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="10852-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="10852-136"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="10852-137">IID</span><span class="sxs-lookup"><span data-stu-id="10852-137">IID</span></span><br/>                      | <span data-ttu-id="10852-138">IID \_ IMsRdpClientNonScriptable3 определен как b3378d90-0728-45c7-8ed7-b6159fb92219</span><span class="sxs-lookup"><span data-stu-id="10852-138">IID\_IMsRdpClientNonScriptable3 is defined as b3378d90-0728-45c7-8ed7-b6159fb92219</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="10852-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="10852-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10852-140">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="10852-140">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="10852-141">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="10852-141">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="10852-142">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="10852-142">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> </dl>

 

 





