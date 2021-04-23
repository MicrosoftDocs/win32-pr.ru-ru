---
title: IMsRdpClientNonScriptable4 Алловкредентиалсавинг, свойство
description: Указывает, отображает ли диалоговое окно учетные данные флажок, позволяющий сохранить учетные данные.
ms.assetid: c5148ff0-0d7f-413d-b2a8-ff942668bee6
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Алловкредентиалсавинг
- Службы удаленных рабочих столов свойства Алловкредентиалсавинг, интерфейс IMsRdpClientNonScriptable4
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable4, свойство Алловкредентиалсавинг
- Службы удаленных рабочих столов свойства Алловкредентиалсавинг, интерфейс IMsRdpClientNonScriptable5
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable5, свойство Алловкредентиалсавинг
- Службы удаленных рабочих столов свойства Алловкредентиалсавинг, объект MsRdpClient6
- Службы удаленных рабочих столов объекта MsRdpClient6, свойство Алловкредентиалсавинг
- Службы удаленных рабочих столов свойства Алловкредентиалсавинг, объект MsRdpClient7
- Службы удаленных рабочих столов объекта MsRdpClient7, свойство Алловкредентиалсавинг
- Службы удаленных рабочих столов свойства Алловкредентиалсавинг, объект MsRdpClient8
- Службы удаленных рабочих столов объекта MsRdpClient8, свойство Алловкредентиалсавинг
- Службы удаленных рабочих столов свойства Алловкредентиалсавинг, объект MsRdpClient9
- Службы удаленных рабочих столов объекта MsRdpClient9, свойство Алловкредентиалсавинг
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable4.AllowCredentialSaving
- IMsRdpClientNonScriptable4.get_AllowCredentialSaving
- IMsRdpClientNonScriptable4.put_AllowCredentialSaving
- IMsRdpClientNonScriptable5.AllowCredentialSaving
- IMsRdpClientNonScriptable5.get_AllowCredentialSaving
- IMsRdpClientNonScriptable5.put_AllowCredentialSaving
- MsRdpClient6.AllowCredentialSaving
- MsRdpClient7.AllowCredentialSaving
- MsRdpClient8.AllowCredentialSaving
- MsRdpClient9.AllowCredentialSaving
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 240e2eb8e80209ee5c90d63f2996231cf84bb2dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681936"
---
# <a name="imsrdpclientnonscriptable4allowcredentialsaving-property"></a><span data-ttu-id="f86da-116">Свойство IMsRdpClientNonScriptable4:: Алловкредентиалсавинг</span><span class="sxs-lookup"><span data-stu-id="f86da-116">IMsRdpClientNonScriptable4::AllowCredentialSaving property</span></span>

<span data-ttu-id="f86da-117">Указывает, отображает ли диалоговое окно учетные данные флажок, позволяющий сохранить учетные данные.</span><span class="sxs-lookup"><span data-stu-id="f86da-117">Specifies whether the credentials dialog box displays a check box that enables the saving of credentials.</span></span>

<span data-ttu-id="f86da-118">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="f86da-118">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="f86da-119">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f86da-119">Syntax</span></span>


```C++
HRESULT put_AllowCredentialSaving(
  [in]  VARIANT_BOOL fAllowSave
);

HRESULT get_AllowCredentialSaving(
  [out] VARIANT_BOOL *pfAllowSave
);
```



## <a name="property-value"></a><span data-ttu-id="f86da-120">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="f86da-120">Property value</span></span>

<span data-ttu-id="f86da-121">Указывает, отображает ли диалоговое окно учетные данные флажок, позволяющий сохранить учетные данные.</span><span class="sxs-lookup"><span data-stu-id="f86da-121">Sets whether the credentials dialog box displays a check box that enables the saving of credentials.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f86da-122">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="f86da-122">Error codes</span></span>

<span data-ttu-id="f86da-123">При успешном выполнении возвращает значение **\_ ОК** .</span><span class="sxs-lookup"><span data-stu-id="f86da-123">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="f86da-124">Требования</span><span class="sxs-lookup"><span data-stu-id="f86da-124">Requirements</span></span>



| <span data-ttu-id="f86da-125">Требование</span><span class="sxs-lookup"><span data-stu-id="f86da-125">Requirement</span></span> | <span data-ttu-id="f86da-126">Значение</span><span class="sxs-lookup"><span data-stu-id="f86da-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f86da-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f86da-127">Minimum supported client</span></span><br/> | <span data-ttu-id="f86da-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f86da-128">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="f86da-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f86da-129">Minimum supported server</span></span><br/> | <span data-ttu-id="f86da-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f86da-130">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="f86da-131">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="f86da-131">Type library</span></span><br/>             | <dl> <span data-ttu-id="f86da-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f86da-132"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="f86da-133">DLL</span><span class="sxs-lookup"><span data-stu-id="f86da-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f86da-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f86da-134"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="f86da-135">IID</span><span class="sxs-lookup"><span data-stu-id="f86da-135">IID</span></span><br/>                      | <span data-ttu-id="f86da-136">IMsRdpClientNonScriptable4 определяется как f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb</span><span class="sxs-lookup"><span data-stu-id="f86da-136">IMsRdpClientNonScriptable4 is defined as f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f86da-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f86da-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f86da-138">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="f86da-138">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="f86da-139">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="f86da-139">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> </dl>

 

 





