---
title: IMsRdpClientNonScriptable3 Дривеколлектион, свойство
description: Извлекает коллекцию объектов Drive для перенаправления.
ms.assetid: 5aaac605-584b-442e-9d67-1cb8213a70b3
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Дривеколлектион
- Службы удаленных рабочих столов свойства Дривеколлектион, интерфейс IMsRdpClientNonScriptable3
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable3, свойство Дривеколлектион
- Службы удаленных рабочих столов свойства Дривеколлектион, интерфейс IMsRdpClientNonScriptable4
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable4, свойство Дривеколлектион
- Службы удаленных рабочих столов свойства Дривеколлектион, интерфейс IMsRdpClientNonScriptable5
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable5, свойство Дривеколлектион
- Службы удаленных рабочих столов свойства Дривеколлектион, объект MsRdpClient5
- Службы удаленных рабочих столов объекта MsRdpClient5, свойство Дривеколлектион
- Службы удаленных рабочих столов свойства Дривеколлектион, объект MsRdpClient6
- Службы удаленных рабочих столов объекта MsRdpClient6, свойство Дривеколлектион
- Службы удаленных рабочих столов свойства Дривеколлектион, объект MsRdpClient7
- Службы удаленных рабочих столов объекта MsRdpClient7, свойство Дривеколлектион
- Службы удаленных рабочих столов свойства Дривеколлектион, объект MsRdpClient8
- Службы удаленных рабочих столов объекта MsRdpClient8, свойство Дривеколлектион
- Службы удаленных рабочих столов свойства Дривеколлектион, объект MsRdpClient9
- Службы удаленных рабочих столов объекта MsRdpClient9, свойство Дривеколлектион
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.DriveCollection
- IMsRdpClientNonScriptable3.get_DriveCollection
- IMsRdpClientNonScriptable4.DriveCollection
- IMsRdpClientNonScriptable4.get_DriveCollection
- IMsRdpClientNonScriptable5.DriveCollection
- IMsRdpClientNonScriptable5.get_DriveCollection
- MsRdpClient5.DriveCollection
- MsRdpClient6.DriveCollection
- MsRdpClient7.DriveCollection
- MsRdpClient8.DriveCollection
- MsRdpClient9.DriveCollection
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37d4bfcaa52d483adc8b0d0885d8316f10ce01d1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489675"
---
# <a name="imsrdpclientnonscriptable3drivecollection-property"></a><span data-ttu-id="33753-120">IMsRdpClientNonScriptable3: свойство Ривеколлектион:D</span><span class="sxs-lookup"><span data-stu-id="33753-120">IMsRdpClientNonScriptable3::DriveCollection property</span></span>

<span data-ttu-id="33753-121">Извлекает коллекцию объектов Drive для перенаправления.</span><span class="sxs-lookup"><span data-stu-id="33753-121">Retrieves the collection of drive objects to be redirected.</span></span>

<span data-ttu-id="33753-122">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="33753-122">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="33753-123">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="33753-123">Syntax</span></span>


```C++
HRESULT get_DriveCollection(
  [out] IMsRdpDriveCollection **ppDriveCollection
);
```



## <a name="property-value"></a><span data-ttu-id="33753-124">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="33753-124">Property value</span></span>

<span data-ttu-id="33753-125">Извлекает коллекцию объектов Drive типа [**имсрдпдриве**](imsrdpdrive.md).</span><span class="sxs-lookup"><span data-stu-id="33753-125">Retrieves the collection of drive objects of type [**IMSRdpDrive**](imsrdpdrive.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="33753-126">Требования</span><span class="sxs-lookup"><span data-stu-id="33753-126">Requirements</span></span>



| <span data-ttu-id="33753-127">Требование</span><span class="sxs-lookup"><span data-stu-id="33753-127">Requirement</span></span> | <span data-ttu-id="33753-128">Значение</span><span class="sxs-lookup"><span data-stu-id="33753-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="33753-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="33753-129">Minimum supported client</span></span><br/> | <span data-ttu-id="33753-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="33753-130">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="33753-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="33753-131">Minimum supported server</span></span><br/> | <span data-ttu-id="33753-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="33753-132">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="33753-133">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="33753-133">Type library</span></span><br/>             | <dl> <span data-ttu-id="33753-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="33753-134"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="33753-135">DLL</span><span class="sxs-lookup"><span data-stu-id="33753-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="33753-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="33753-136"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="33753-137">IID</span><span class="sxs-lookup"><span data-stu-id="33753-137">IID</span></span><br/>                      | <span data-ttu-id="33753-138">IID \_ IMsRdpClientNonScriptable3 определен как b3378d90-0728-45c7-8ed7-b6159fb92219</span><span class="sxs-lookup"><span data-stu-id="33753-138">IID\_IMsRdpClientNonScriptable3 is defined as b3378d90-0728-45c7-8ed7-b6159fb92219</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="33753-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="33753-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33753-140">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="33753-140">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="33753-141">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="33753-141">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="33753-142">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="33753-142">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> </dl>

 

 





