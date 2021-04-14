---
title: IMsRdpClientNonScriptable3 описания, свойство
description: Извлекает коллекцию объектов устройств самонастраивающийся (PnP) для перенаправления.
ms.assetid: dd5fe4c7-58bf-4e7a-b066-59278419ea6f
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства описания
- Службы удаленных рабочих столов свойства описания, интерфейс IMsRdpClientNonScriptable3
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable3, свойство описания
- Службы удаленных рабочих столов свойства описания, интерфейс IMsRdpClientNonScriptable4
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable4, свойство описания
- Службы удаленных рабочих столов свойства описания, интерфейс IMsRdpClientNonScriptable5
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable5, свойство описания
- Службы удаленных рабочих столов свойства описания, объект MsRdpClient5
- Службы удаленных рабочих столов объекта MsRdpClient5, свойство описания
- Службы удаленных рабочих столов свойства описания, объект MsRdpClient6
- Службы удаленных рабочих столов объекта MsRdpClient6, свойство описания
- Службы удаленных рабочих столов свойства описания, объект MsRdpClient7
- Службы удаленных рабочих столов объекта MsRdpClient7, свойство описания
- Службы удаленных рабочих столов свойства описания, объект MsRdpClient8
- Службы удаленных рабочих столов объекта MsRdpClient8, свойство описания
- Службы удаленных рабочих столов свойства описания, объект MsRdpClient9
- Службы удаленных рабочих столов объекта MsRdpClient9, свойство описания
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.DeviceCollection
- IMsRdpClientNonScriptable3.get_DeviceCollection
- IMsRdpClientNonScriptable4.DeviceCollection
- IMsRdpClientNonScriptable4.get_DeviceCollection
- IMsRdpClientNonScriptable5.DeviceCollection
- IMsRdpClientNonScriptable5.get_DeviceCollection
- MsRdpClient5.DeviceCollection
- MsRdpClient6.DeviceCollection
- MsRdpClient7.DeviceCollection
- MsRdpClient8.DeviceCollection
- MsRdpClient9.DeviceCollection
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a545d2f4aaae2af68c14dd6531a2c57cf73711dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415053"
---
# <a name="imsrdpclientnonscriptable3devicecollection-property"></a><span data-ttu-id="c3be4-120">IMsRdpClientNonScriptable3: свойство Евицеколлектион:D</span><span class="sxs-lookup"><span data-stu-id="c3be4-120">IMsRdpClientNonScriptable3::DeviceCollection property</span></span>

<span data-ttu-id="c3be4-121">Извлекает коллекцию объектов устройств самонастраивающийся (PnP) для перенаправления.</span><span class="sxs-lookup"><span data-stu-id="c3be4-121">Retrieves the collection of Plug and Play (PnP) device objects to be redirected.</span></span>

<span data-ttu-id="c3be4-122">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="c3be4-122">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3be4-123">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c3be4-123">Syntax</span></span>


```C++
HRESULT get_DeviceCollection(
  [out] IMSRdpDeviceCollection **ppDeviceCollection
);
```



## <a name="property-value"></a><span data-ttu-id="c3be4-124">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="c3be4-124">Property value</span></span>

<span data-ttu-id="c3be4-125">Извлекает коллекцию объектов устройств PnP типа [**имсрдпдевице**](imsrdpdevice.md).</span><span class="sxs-lookup"><span data-stu-id="c3be4-125">Retrieves the collection of PnP device objects of type [**IMSRdpDevice**](imsrdpdevice.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c3be4-126">Требования</span><span class="sxs-lookup"><span data-stu-id="c3be4-126">Requirements</span></span>



| <span data-ttu-id="c3be4-127">Требование</span><span class="sxs-lookup"><span data-stu-id="c3be4-127">Requirement</span></span> | <span data-ttu-id="c3be4-128">Значение</span><span class="sxs-lookup"><span data-stu-id="c3be4-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3be4-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c3be4-129">Minimum supported client</span></span><br/> | <span data-ttu-id="c3be4-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c3be4-130">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="c3be4-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c3be4-131">Minimum supported server</span></span><br/> | <span data-ttu-id="c3be4-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c3be4-132">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="c3be4-133">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="c3be4-133">Type library</span></span><br/>             | <dl> <span data-ttu-id="c3be4-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c3be4-134"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="c3be4-135">DLL</span><span class="sxs-lookup"><span data-stu-id="c3be4-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c3be4-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c3be4-136"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="c3be4-137">IID</span><span class="sxs-lookup"><span data-stu-id="c3be4-137">IID</span></span><br/>                      | <span data-ttu-id="c3be4-138">IID \_ IMsRdpClientNonScriptable3 определен как b3378d90-0728-45c7-8ed7-b6159fb92219</span><span class="sxs-lookup"><span data-stu-id="c3be4-138">IID\_IMsRdpClientNonScriptable3 is defined as b3378d90-0728-45c7-8ed7-b6159fb92219</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c3be4-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c3be4-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3be4-140">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="c3be4-140">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="c3be4-141">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="c3be4-141">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="c3be4-142">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="c3be4-142">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> </dl>

 

 





