---
title: IMsRdpClientNonScriptable4 Варнабаутпринтерредиректион, свойство
description: Определяет, отображает ли диалоговое окно перенаправление сообщение о перенаправлении принтера перед запуском сеанса.
ms.assetid: 12c5bc8d-7bc1-4a94-a9b8-6b852772c936
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Варнабаутпринтерредиректион
- Службы удаленных рабочих столов свойства Варнабаутпринтерредиректион, интерфейс IMsRdpClientNonScriptable4
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable4, свойство Варнабаутпринтерредиректион
- Службы удаленных рабочих столов свойства Варнабаутпринтерредиректион, интерфейс IMsRdpClientNonScriptable5
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable5, свойство Варнабаутпринтерредиректион
- Службы удаленных рабочих столов свойства Варнабаутпринтерредиректион, объект MsRdpClient6
- Службы удаленных рабочих столов объекта MsRdpClient6, свойство Варнабаутпринтерредиректион
- Службы удаленных рабочих столов свойства Варнабаутпринтерредиректион, объект MsRdpClient7
- Службы удаленных рабочих столов объекта MsRdpClient7, свойство Варнабаутпринтерредиректион
- Службы удаленных рабочих столов свойства Варнабаутпринтерредиректион, объект MsRdpClient8
- Службы удаленных рабочих столов объекта MsRdpClient8, свойство Варнабаутпринтерредиректион
- Службы удаленных рабочих столов свойства Варнабаутпринтерредиректион, объект MsRdpClient9
- Службы удаленных рабочих столов объекта MsRdpClient9, свойство Варнабаутпринтерредиректион
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable4.WarnAboutPrinterRedirection
- IMsRdpClientNonScriptable4.get_WarnAboutPrinterRedirection
- IMsRdpClientNonScriptable4.put_WarnAboutPrinterRedirection
- IMsRdpClientNonScriptable5.WarnAboutPrinterRedirection
- IMsRdpClientNonScriptable5.get_WarnAboutPrinterRedirection
- IMsRdpClientNonScriptable5.put_WarnAboutPrinterRedirection
- MsRdpClient6.WarnAboutPrinterRedirection
- MsRdpClient7.WarnAboutPrinterRedirection
- MsRdpClient8.WarnAboutPrinterRedirection
- MsRdpClient9.WarnAboutPrinterRedirection
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24e2fa93995946e741caa76f1ee5b84be79d9c90
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340805"
---
# <a name="imsrdpclientnonscriptable4warnaboutprinterredirection-property"></a><span data-ttu-id="ea8e0-116">Свойство IMsRdpClientNonScriptable4:: Варнабаутпринтерредиректион</span><span class="sxs-lookup"><span data-stu-id="ea8e0-116">IMsRdpClientNonScriptable4::WarnAboutPrinterRedirection property</span></span>

<span data-ttu-id="ea8e0-117">Определяет, отображает ли диалоговое окно перенаправление сообщение о перенаправлении принтера перед запуском сеанса.</span><span class="sxs-lookup"><span data-stu-id="ea8e0-117">Controls whether the redirection dialog box displays a message about printer redirection before starting a session.</span></span>

<span data-ttu-id="ea8e0-118">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="ea8e0-118">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea8e0-119">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ea8e0-119">Syntax</span></span>


```C++
HRESULT put_WarnAboutPrinterRedirection(
  [in]  VARIANT_BOOL fWarn
);

HRESULT get_WarnAboutPrinterRedirection(
  [out] VARIANT_BOOL *pfWarn
);
```



## <a name="property-value"></a><span data-ttu-id="ea8e0-120">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="ea8e0-120">Property value</span></span>

<span data-ttu-id="ea8e0-121">Указывает, отображает ли диалоговое окно перенаправление сообщение о перенаправлении принтера.</span><span class="sxs-lookup"><span data-stu-id="ea8e0-121">Sets whether the redirection dialog box displays a message about printer redirection.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ea8e0-122">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="ea8e0-122">Error codes</span></span>

<span data-ttu-id="ea8e0-123">При успешном выполнении возвращает значение **\_ ОК** .</span><span class="sxs-lookup"><span data-stu-id="ea8e0-123">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea8e0-124">Требования</span><span class="sxs-lookup"><span data-stu-id="ea8e0-124">Requirements</span></span>



| <span data-ttu-id="ea8e0-125">Требование</span><span class="sxs-lookup"><span data-stu-id="ea8e0-125">Requirement</span></span> | <span data-ttu-id="ea8e0-126">Значение</span><span class="sxs-lookup"><span data-stu-id="ea8e0-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea8e0-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ea8e0-127">Minimum supported client</span></span><br/> | <span data-ttu-id="ea8e0-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ea8e0-128">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="ea8e0-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ea8e0-129">Minimum supported server</span></span><br/> | <span data-ttu-id="ea8e0-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ea8e0-130">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="ea8e0-131">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="ea8e0-131">Type library</span></span><br/>             | <dl> <span data-ttu-id="ea8e0-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ea8e0-132"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="ea8e0-133">DLL</span><span class="sxs-lookup"><span data-stu-id="ea8e0-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ea8e0-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ea8e0-134"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="ea8e0-135">IID</span><span class="sxs-lookup"><span data-stu-id="ea8e0-135">IID</span></span><br/>                      | <span data-ttu-id="ea8e0-136">IMsRdpClientNonScriptable4 определяется как f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb</span><span class="sxs-lookup"><span data-stu-id="ea8e0-136">IMsRdpClientNonScriptable4 is defined as f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ea8e0-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ea8e0-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea8e0-138">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="ea8e0-138">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="ea8e0-139">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="ea8e0-139">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> </dl>

 

 





