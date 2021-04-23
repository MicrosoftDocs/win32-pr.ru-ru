---
title: IMsRdpClientNonScriptable3 Редиректдинамикдевицес, свойство
description: Указывает или получает значение, указывающее, доступны ли для перенаправления динамически подключаемые устройства самонастраивающийся (PnP), перечисленные в сеансе.
ms.assetid: 8cc5d6a4-108b-4505-8937-f6e790a5c2ba
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Редиректдинамикдевицес
- Службы удаленных рабочих столов свойства Редиректдинамикдевицес, интерфейс IMsRdpClientNonScriptable3
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable3, свойство Редиректдинамикдевицес
- Службы удаленных рабочих столов свойства Редиректдинамикдевицес, интерфейс IMsRdpClientNonScriptable4
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable4, свойство Редиректдинамикдевицес
- Службы удаленных рабочих столов свойства Редиректдинамикдевицес, интерфейс IMsRdpClientNonScriptable5
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable5, свойство Редиректдинамикдевицес
- Службы удаленных рабочих столов свойства Редиректдинамикдевицес, объект MsRdpClient5
- Службы удаленных рабочих столов объекта MsRdpClient5, свойство Редиректдинамикдевицес
- Службы удаленных рабочих столов свойства Редиректдинамикдевицес, объект MsRdpClient6
- Службы удаленных рабочих столов объекта MsRdpClient6, свойство Редиректдинамикдевицес
- Службы удаленных рабочих столов свойства Редиректдинамикдевицес, объект MsRdpClient7
- Службы удаленных рабочих столов объекта MsRdpClient7, свойство Редиректдинамикдевицес
- Службы удаленных рабочих столов свойства Редиректдинамикдевицес, объект MsRdpClient8
- Службы удаленных рабочих столов объекта MsRdpClient8, свойство Редиректдинамикдевицес
- Службы удаленных рабочих столов свойства Редиректдинамикдевицес, объект MsRdpClient9
- Службы удаленных рабочих столов объекта MsRdpClient9, свойство Редиректдинамикдевицес
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.RedirectDynamicDevices
- IMsRdpClientNonScriptable3.get_RedirectDynamicDevices
- IMsRdpClientNonScriptable3.put_RedirectDynamicDevices
- IMsRdpClientNonScriptable4.RedirectDynamicDevices
- IMsRdpClientNonScriptable4.get_RedirectDynamicDevices
- IMsRdpClientNonScriptable4.put_RedirectDynamicDevices
- IMsRdpClientNonScriptable5.RedirectDynamicDevices
- IMsRdpClientNonScriptable5.get_RedirectDynamicDevices
- IMsRdpClientNonScriptable5.put_RedirectDynamicDevices
- MsRdpClient5.RedirectDynamicDevices
- MsRdpClient6.RedirectDynamicDevices
- MsRdpClient7.RedirectDynamicDevices
- MsRdpClient8.RedirectDynamicDevices
- MsRdpClient9.RedirectDynamicDevices
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75224d26034e606a7a46943a02845280a092c3b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801450"
---
# <a name="imsrdpclientnonscriptable3redirectdynamicdevices-property"></a><span data-ttu-id="6a009-120">Свойство IMsRdpClientNonScriptable3:: Редиректдинамикдевицес</span><span class="sxs-lookup"><span data-stu-id="6a009-120">IMsRdpClientNonScriptable3::RedirectDynamicDevices property</span></span>

<span data-ttu-id="6a009-121">Указывает или получает значение, указывающее, доступны ли для перенаправления динамически подключаемые устройства самонастраивающийся (PnP), перечисленные в сеансе.</span><span class="sxs-lookup"><span data-stu-id="6a009-121">Specifies or retrieves whether dynamically attached Plug and Play (PnP) devices that are enumerated while in a session are available for redirection.</span></span>

<span data-ttu-id="6a009-122">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="6a009-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a009-123">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6a009-123">Syntax</span></span>


```C++
HRESULT put_RedirectDynamicDevices(
  [in]  VARIANT_BOOL fRedirectDynamicDevices
);

HRESULT get_RedirectDynamicDevices(
  [out] VARIANT_BOOL *pfRedirectDynamicDevices
);
```



## <a name="property-value"></a><span data-ttu-id="6a009-124">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="6a009-124">Property value</span></span>

<span data-ttu-id="6a009-125">Указывает, доступны ли для перенаправления динамически подключаемые устройства PnP, перечисленные в сеансе.</span><span class="sxs-lookup"><span data-stu-id="6a009-125">Specifies whether dynamically attached PnP devices that are enumerated while in a session are available for redirection.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a009-126">Требования</span><span class="sxs-lookup"><span data-stu-id="6a009-126">Requirements</span></span>



| <span data-ttu-id="6a009-127">Требование</span><span class="sxs-lookup"><span data-stu-id="6a009-127">Requirement</span></span> | <span data-ttu-id="6a009-128">Значение</span><span class="sxs-lookup"><span data-stu-id="6a009-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a009-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6a009-129">Minimum supported client</span></span><br/> | <span data-ttu-id="6a009-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6a009-130">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="6a009-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6a009-131">Minimum supported server</span></span><br/> | <span data-ttu-id="6a009-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6a009-132">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="6a009-133">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="6a009-133">Type library</span></span><br/>             | <dl> <span data-ttu-id="6a009-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6a009-134"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="6a009-135">DLL</span><span class="sxs-lookup"><span data-stu-id="6a009-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6a009-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6a009-136"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="6a009-137">IID</span><span class="sxs-lookup"><span data-stu-id="6a009-137">IID</span></span><br/>                      | <span data-ttu-id="6a009-138">IID \_ IMsRdpClientNonScriptable3 определен как b3378d90-0728-45c7-8ed7-b6159fb92219</span><span class="sxs-lookup"><span data-stu-id="6a009-138">IID\_IMsRdpClientNonScriptable3 is defined as b3378d90-0728-45c7-8ed7-b6159fb92219</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6a009-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6a009-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a009-140">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="6a009-140">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="6a009-141">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="6a009-141">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="6a009-142">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="6a009-142">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> </dl>

 

 





