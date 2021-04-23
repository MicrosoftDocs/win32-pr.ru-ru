---
title: IMsRdpClientNonScriptable3 Редиректдинамикдривес, свойство
description: Указывает или получает значение, указывающее, доступны ли для перенаправления динамически подключаемые диски самонастраивающийся (PnP), перечисленные в сеансе.
ms.assetid: 11eb19fc-9711-4293-8054-f7975dadb492
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Редиректдинамикдривес
- Службы удаленных рабочих столов свойства Редиректдинамикдривес, интерфейс IMsRdpClientNonScriptable3
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable3, свойство Редиректдинамикдривес
- Службы удаленных рабочих столов свойства Редиректдинамикдривес, интерфейс IMsRdpClientNonScriptable4
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable4, свойство Редиректдинамикдривес
- Службы удаленных рабочих столов свойства Редиректдинамикдривес, интерфейс IMsRdpClientNonScriptable5
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable5, свойство Редиректдинамикдривес
- Службы удаленных рабочих столов свойства Редиректдинамикдривес, объект MsRdpClient5
- Службы удаленных рабочих столов объекта MsRdpClient5, свойство Редиректдинамикдривес
- Службы удаленных рабочих столов свойства Редиректдинамикдривес, объект MsRdpClient6
- Службы удаленных рабочих столов объекта MsRdpClient6, свойство Редиректдинамикдривес
- Службы удаленных рабочих столов свойства Редиректдинамикдривес, объект MsRdpClient7
- Службы удаленных рабочих столов объекта MsRdpClient7, свойство Редиректдинамикдривес
- Службы удаленных рабочих столов свойства Редиректдинамикдривес, объект MsRdpClient8
- Службы удаленных рабочих столов объекта MsRdpClient8, свойство Редиректдинамикдривес
- Службы удаленных рабочих столов свойства Редиректдинамикдривес, объект MsRdpClient9
- Службы удаленных рабочих столов объекта MsRdpClient9, свойство Редиректдинамикдривес
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.RedirectDynamicDrives
- IMsRdpClientNonScriptable3.get_RedirectDynamicDrives
- IMsRdpClientNonScriptable3.put_RedirectDynamicDrives
- IMsRdpClientNonScriptable4.RedirectDynamicDrives
- IMsRdpClientNonScriptable4.get_RedirectDynamicDrives
- IMsRdpClientNonScriptable4.put_RedirectDynamicDrives
- IMsRdpClientNonScriptable5.RedirectDynamicDrives
- IMsRdpClientNonScriptable5.get_RedirectDynamicDrives
- IMsRdpClientNonScriptable5.put_RedirectDynamicDrives
- MsRdpClient5.RedirectDynamicDrives
- MsRdpClient6.RedirectDynamicDrives
- MsRdpClient7.RedirectDynamicDrives
- MsRdpClient8.RedirectDynamicDrives
- MsRdpClient9.RedirectDynamicDrives
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b19c0e6e20f7f73481f6f2ecbc50ab0eda512ded
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803886"
---
# <a name="imsrdpclientnonscriptable3redirectdynamicdrives-property"></a><span data-ttu-id="4fc10-120">Свойство IMsRdpClientNonScriptable3:: Редиректдинамикдривес</span><span class="sxs-lookup"><span data-stu-id="4fc10-120">IMsRdpClientNonScriptable3::RedirectDynamicDrives property</span></span>

<span data-ttu-id="4fc10-121">Указывает или получает значение, указывающее, доступны ли для перенаправления динамически подключаемые диски самонастраивающийся (PnP), перечисленные в сеансе.</span><span class="sxs-lookup"><span data-stu-id="4fc10-121">Specifies or retrieves whether dynamically attached Plug and Play (PnP) drives that are enumerated while in a session are available for redirection.</span></span>

<span data-ttu-id="4fc10-122">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="4fc10-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="4fc10-123">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4fc10-123">Syntax</span></span>


```C++
HRESULT put_RedirectDynamicDrives(
  [in]  VARIANT_BOOL fRedirectDynamicDrives
);

HRESULT get_RedirectDynamicDrives(
  [out] VARIANT_BOOL *pfRedirectDynamicDrives
);
```



## <a name="property-value"></a><span data-ttu-id="4fc10-124">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="4fc10-124">Property value</span></span>

<span data-ttu-id="4fc10-125">Указывает, доступны ли для перенаправления динамически подключаемые диски PnP, перечисленные в сеансе.</span><span class="sxs-lookup"><span data-stu-id="4fc10-125">Specifies whether dynamically attached PnP drives that are enumerated while in a session are available for redirection.</span></span>

## <a name="requirements"></a><span data-ttu-id="4fc10-126">Требования</span><span class="sxs-lookup"><span data-stu-id="4fc10-126">Requirements</span></span>



| <span data-ttu-id="4fc10-127">Требование</span><span class="sxs-lookup"><span data-stu-id="4fc10-127">Requirement</span></span> | <span data-ttu-id="4fc10-128">Значение</span><span class="sxs-lookup"><span data-stu-id="4fc10-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="4fc10-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4fc10-129">Minimum supported client</span></span><br/> | <span data-ttu-id="4fc10-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4fc10-130">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="4fc10-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4fc10-131">Minimum supported server</span></span><br/> | <span data-ttu-id="4fc10-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4fc10-132">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="4fc10-133">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="4fc10-133">Type library</span></span><br/>             | <dl> <span data-ttu-id="4fc10-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4fc10-134"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="4fc10-135">DLL</span><span class="sxs-lookup"><span data-stu-id="4fc10-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4fc10-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4fc10-136"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="4fc10-137">IID</span><span class="sxs-lookup"><span data-stu-id="4fc10-137">IID</span></span><br/>                      | <span data-ttu-id="4fc10-138">IID \_ IMsRdpClientNonScriptable3 определен как b3378d90-0728-45c7-8ed7-b6159fb92219</span><span class="sxs-lookup"><span data-stu-id="4fc10-138">IID\_IMsRdpClientNonScriptable3 is defined as b3378d90-0728-45c7-8ed7-b6159fb92219</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4fc10-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4fc10-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4fc10-140">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="4fc10-140">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="4fc10-141">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="4fc10-141">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="4fc10-142">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="4fc10-142">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> </dl>

 

 





