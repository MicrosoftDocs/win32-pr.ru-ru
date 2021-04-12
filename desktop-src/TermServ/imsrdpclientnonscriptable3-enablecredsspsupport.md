---
title: IMsRdpClientNonScriptable3 Енаблекредсспсуппорт, свойство
description: Указывает или получает значение, указывающее, включен ли поставщик службы безопасности учетных данных (CredSSP) для этого подключения.
ms.assetid: 770da50b-2a93-4274-9b6f-c24c13f08549
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Енаблекредсспсуппорт
- Службы удаленных рабочих столов свойства Енаблекредсспсуппорт, интерфейс IMsRdpClientNonScriptable3
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable3, свойство Енаблекредсспсуппорт
- Службы удаленных рабочих столов свойства Енаблекредсспсуппорт, интерфейс IMsRdpClientNonScriptable4
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable4, свойство Енаблекредсспсуппорт
- Службы удаленных рабочих столов свойства Енаблекредсспсуппорт, интерфейс IMsRdpClientNonScriptable5
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable5, свойство Енаблекредсспсуппорт
- Службы удаленных рабочих столов свойства Енаблекредсспсуппорт, объект MsRdpClient5
- Службы удаленных рабочих столов объекта MsRdpClient5, свойство Енаблекредсспсуппорт
- Службы удаленных рабочих столов свойства Енаблекредсспсуппорт, объект MsRdpClient6
- Службы удаленных рабочих столов объекта MsRdpClient6, свойство Енаблекредсспсуппорт
- Службы удаленных рабочих столов свойства Енаблекредсспсуппорт, объект MsRdpClient7
- Службы удаленных рабочих столов объекта MsRdpClient7, свойство Енаблекредсспсуппорт
- Службы удаленных рабочих столов свойства Енаблекредсспсуппорт, объект MsRdpClient8
- Службы удаленных рабочих столов объекта MsRdpClient8, свойство Енаблекредсспсуппорт
- Службы удаленных рабочих столов свойства Енаблекредсспсуппорт, объект MsRdpClient9
- Службы удаленных рабочих столов объекта MsRdpClient9, свойство Енаблекредсспсуппорт
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.EnableCredSspSupport
- IMsRdpClientNonScriptable3.get_EnableCredSspSupport
- IMsRdpClientNonScriptable3.put_EnableCredSspSupport
- IMsRdpClientNonScriptable4.EnableCredSspSupport
- IMsRdpClientNonScriptable4.get_EnableCredSspSupport
- IMsRdpClientNonScriptable4.put_EnableCredSspSupport
- IMsRdpClientNonScriptable5.EnableCredSspSupport
- IMsRdpClientNonScriptable5.get_EnableCredSspSupport
- IMsRdpClientNonScriptable5.put_EnableCredSspSupport
- MsRdpClient5.EnableCredSspSupport
- MsRdpClient6.EnableCredSspSupport
- MsRdpClient7.EnableCredSspSupport
- MsRdpClient8.EnableCredSspSupport
- MsRdpClient9.EnableCredSspSupport
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2330b800d15f95a7b59a01735de971dd4b212d6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135767"
---
# <a name="imsrdpclientnonscriptable3enablecredsspsupport-property"></a><span data-ttu-id="80206-120">Свойство IMsRdpClientNonScriptable3:: Енаблекредсспсуппорт</span><span class="sxs-lookup"><span data-stu-id="80206-120">IMsRdpClientNonScriptable3::EnableCredSspSupport property</span></span>

<span data-ttu-id="80206-121">Указывает или получает значение, указывающее, включен ли поставщик службы безопасности учетных данных (CredSSP) для этого подключения.</span><span class="sxs-lookup"><span data-stu-id="80206-121">Specifies or retrieves whether the Credential Security Service Provider (CredSSP) is enabled for this connection.</span></span>

<span data-ttu-id="80206-122">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="80206-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="80206-123">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="80206-123">Syntax</span></span>


```C++
HRESULT put_EnableCredSspSupport(
  [in]  VARIANT_BOOL fEnableSupport
);

HRESULT get_EnableCredSspSupport(
  [out] VARIANT_BOOL *pfEnableSupport
);
```



## <a name="property-value"></a><span data-ttu-id="80206-124">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="80206-124">Property value</span></span>

<span data-ttu-id="80206-125">Указывает, включен ли CredSSP для этого соединения.</span><span class="sxs-lookup"><span data-stu-id="80206-125">Specifies whether CredSSP is enabled for this connection.</span></span>

## <a name="requirements"></a><span data-ttu-id="80206-126">Требования</span><span class="sxs-lookup"><span data-stu-id="80206-126">Requirements</span></span>



| <span data-ttu-id="80206-127">Требование</span><span class="sxs-lookup"><span data-stu-id="80206-127">Requirement</span></span> | <span data-ttu-id="80206-128">Значение</span><span class="sxs-lookup"><span data-stu-id="80206-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="80206-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="80206-129">Minimum supported client</span></span><br/> | <span data-ttu-id="80206-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="80206-130">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="80206-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="80206-131">Minimum supported server</span></span><br/> | <span data-ttu-id="80206-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="80206-132">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="80206-133">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="80206-133">Type library</span></span><br/>             | <dl> <span data-ttu-id="80206-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="80206-134"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="80206-135">DLL</span><span class="sxs-lookup"><span data-stu-id="80206-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="80206-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="80206-136"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="80206-137">IID</span><span class="sxs-lookup"><span data-stu-id="80206-137">IID</span></span><br/>                      | <span data-ttu-id="80206-138">IID \_ IMsRdpClientNonScriptable3 определен как b3378d90-0728-45c7-8ed7-b6159fb92219</span><span class="sxs-lookup"><span data-stu-id="80206-138">IID\_IMsRdpClientNonScriptable3 is defined as b3378d90-0728-45c7-8ed7-b6159fb92219</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="80206-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="80206-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80206-140">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="80206-140">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="80206-141">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="80206-141">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="80206-142">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="80206-142">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> </dl>

 

 





