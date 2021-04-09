---
title: IMsRdpClientNonScriptable4 Лаунчедвиаклиентшеллинтерфаце, свойство
description: Указывает, запустил ли пользователь клиентский элемент управления с помощью интерфейса удаленный рабочий стол Веб-доступ (RD Веб-доступ).
ms.assetid: bf72c375-0eec-49c7-9f9a-c7545a95bdce
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Лаунчедвиаклиентшеллинтерфаце
- Службы удаленных рабочих столов свойства Лаунчедвиаклиентшеллинтерфаце, интерфейс IMsRdpClientNonScriptable4
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable4, свойство Лаунчедвиаклиентшеллинтерфаце
- Службы удаленных рабочих столов свойства Лаунчедвиаклиентшеллинтерфаце, интерфейс IMsRdpClientNonScriptable5
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable5, свойство Лаунчедвиаклиентшеллинтерфаце
- Службы удаленных рабочих столов свойства Лаунчедвиаклиентшеллинтерфаце, объект MsRdpClient5
- Службы удаленных рабочих столов объекта MsRdpClient5, свойство Лаунчедвиаклиентшеллинтерфаце
- Службы удаленных рабочих столов свойства Лаунчедвиаклиентшеллинтерфаце, объект MsRdpClient6
- Службы удаленных рабочих столов объекта MsRdpClient6, свойство Лаунчедвиаклиентшеллинтерфаце
- Службы удаленных рабочих столов свойства Лаунчедвиаклиентшеллинтерфаце, объект MsRdpClient7
- Службы удаленных рабочих столов объекта MsRdpClient7, свойство Лаунчедвиаклиентшеллинтерфаце
- Службы удаленных рабочих столов свойства Лаунчедвиаклиентшеллинтерфаце, объект MsRdpClient8
- Службы удаленных рабочих столов объекта MsRdpClient8, свойство Лаунчедвиаклиентшеллинтерфаце
- Службы удаленных рабочих столов свойства Лаунчедвиаклиентшеллинтерфаце, объект MsRdpClient9
- Службы удаленных рабочих столов объекта MsRdpClient9, свойство Лаунчедвиаклиентшеллинтерфаце
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable4.LaunchedViaClientShellInterface
- IMsRdpClientNonScriptable4.get_LaunchedViaClientShellInterface
- IMsRdpClientNonScriptable4.put_LaunchedViaClientShellInterface
- IMsRdpClientNonScriptable5.LaunchedViaClientShellInterface
- IMsRdpClientNonScriptable5.get_LaunchedViaClientShellInterface
- IMsRdpClientNonScriptable5.put_LaunchedViaClientShellInterface
- MsRdpClient5.LaunchedViaClientShellInterface
- MsRdpClient6.LaunchedViaClientShellInterface
- MsRdpClient7.LaunchedViaClientShellInterface
- MsRdpClient8.LaunchedViaClientShellInterface
- MsRdpClient9.LaunchedViaClientShellInterface
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d5854a4e75be455035fd9a123418bd486932379
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988859"
---
# <a name="imsrdpclientnonscriptable4launchedviaclientshellinterface-property"></a><span data-ttu-id="cf554-118">Свойство IMsRdpClientNonScriptable4:: Лаунчедвиаклиентшеллинтерфаце</span><span class="sxs-lookup"><span data-stu-id="cf554-118">IMsRdpClientNonScriptable4::LaunchedViaClientShellInterface property</span></span>

<span data-ttu-id="cf554-119">Указывает, запустил ли пользователь клиентский элемент управления с помощью интерфейса удаленный рабочий стол Веб-доступ (RD Веб-доступ).</span><span class="sxs-lookup"><span data-stu-id="cf554-119">Specifies whether the user launched the client control by using the Remote Desktop Web Access (RD Web Access) interface.</span></span>

<span data-ttu-id="cf554-120">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="cf554-120">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf554-121">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cf554-121">Syntax</span></span>


```C++
HRESULT put_LaunchedViaClientShellInterface(
  [in]  VARIANT_BOOL fLaunchedViaClientShellInterface
);

HRESULT get_LaunchedViaClientShellInterface(
  [out]  VARIANT_BOOL *pfLaunchedViaClientShellInterface
);
```



## <a name="property-value"></a><span data-ttu-id="cf554-122">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="cf554-122">Property value</span></span>

<span data-ttu-id="cf554-123">Задает свойство **лаунчедвиаклиентшеллинтерфаце** .</span><span class="sxs-lookup"><span data-stu-id="cf554-123">Sets the **LaunchedViaClientShellInterface** property.</span></span>

## <a name="error-codes"></a><span data-ttu-id="cf554-124">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="cf554-124">Error codes</span></span>

<span data-ttu-id="cf554-125">При успешном выполнении возвращает значение **\_ ОК** .</span><span class="sxs-lookup"><span data-stu-id="cf554-125">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf554-126">Требования</span><span class="sxs-lookup"><span data-stu-id="cf554-126">Requirements</span></span>



| <span data-ttu-id="cf554-127">Требование</span><span class="sxs-lookup"><span data-stu-id="cf554-127">Requirement</span></span> | <span data-ttu-id="cf554-128">Значение</span><span class="sxs-lookup"><span data-stu-id="cf554-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf554-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cf554-129">Minimum supported client</span></span><br/> | <span data-ttu-id="cf554-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cf554-130">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="cf554-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cf554-131">Minimum supported server</span></span><br/> | <span data-ttu-id="cf554-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cf554-132">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="cf554-133">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="cf554-133">Type library</span></span><br/>             | <dl> <span data-ttu-id="cf554-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cf554-134"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="cf554-135">DLL</span><span class="sxs-lookup"><span data-stu-id="cf554-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cf554-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cf554-136"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="cf554-137">IID</span><span class="sxs-lookup"><span data-stu-id="cf554-137">IID</span></span><br/>                      | <span data-ttu-id="cf554-138">IMsRdpClientNonScriptable4 определяется как f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb</span><span class="sxs-lookup"><span data-stu-id="cf554-138">IMsRdpClientNonScriptable4 is defined as f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="cf554-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cf554-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf554-140">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="cf554-140">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="cf554-141">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="cf554-141">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> </dl>

 

 





