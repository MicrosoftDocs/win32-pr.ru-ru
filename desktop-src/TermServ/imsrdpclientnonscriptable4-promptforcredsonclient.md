---
title: IMsRdpClientNonScriptable4 Промптфоркредсонклиент, свойство
description: Указывает, отображает ли клиентский элемент управления диалоговое окно с запросом учетных данных.
ms.assetid: 426676be-0150-4a33-acd0-26423966f32a
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Промптфоркредсонклиент
- Службы удаленных рабочих столов свойства Промптфоркредсонклиент, интерфейс IMsRdpClientNonScriptable4
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable4, свойство Промптфоркредсонклиент
- Службы удаленных рабочих столов свойства Промптфоркредсонклиент, интерфейс IMsRdpClientNonScriptable5
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable5, свойство Промптфоркредсонклиент
- Службы удаленных рабочих столов свойства Промптфоркредсонклиент, объект MsRdpClient6
- Службы удаленных рабочих столов объекта MsRdpClient6, свойство Промптфоркредсонклиент
- Службы удаленных рабочих столов свойства Промптфоркредсонклиент, объект MsRdpClient7
- Службы удаленных рабочих столов объекта MsRdpClient7, свойство Промптфоркредсонклиент
- Службы удаленных рабочих столов свойства Промптфоркредсонклиент, объект MsRdpClient8
- Службы удаленных рабочих столов объекта MsRdpClient8, свойство Промптфоркредсонклиент
- Службы удаленных рабочих столов свойства Промптфоркредсонклиент, объект MsRdpClient9
- Службы удаленных рабочих столов объекта MsRdpClient9, свойство Промптфоркредсонклиент
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable4.PromptForCredsOnClient
- IMsRdpClientNonScriptable4.get_PromptForCredsOnClient
- IMsRdpClientNonScriptable4.put_PromptForCredsOnClient
- IMsRdpClientNonScriptable5.PromptForCredsOnClient
- IMsRdpClientNonScriptable5.get_PromptForCredsOnClient
- IMsRdpClientNonScriptable5.put_PromptForCredsOnClient
- MsRdpClient6.PromptForCredsOnClient
- MsRdpClient7.PromptForCredsOnClient
- MsRdpClient8.PromptForCredsOnClient
- MsRdpClient9.PromptForCredsOnClient
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6443c503e107bb2edb164a17beedddb1bbbc88a5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415769"
---
# <a name="imsrdpclientnonscriptable4promptforcredsonclient-property"></a><span data-ttu-id="b7f05-116">IMsRdpClientNonScriptable4: свойство Ромптфоркредсонклиент:P</span><span class="sxs-lookup"><span data-stu-id="b7f05-116">IMsRdpClientNonScriptable4::PromptForCredsOnClient property</span></span>

<span data-ttu-id="b7f05-117">Указывает, отображает ли клиентский элемент управления диалоговое окно с запросом учетных данных.</span><span class="sxs-lookup"><span data-stu-id="b7f05-117">Specifies whether the client control displays a dialog box that prompts for credentials.</span></span>

<span data-ttu-id="b7f05-118">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="b7f05-118">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7f05-119">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b7f05-119">Syntax</span></span>


```C++
HRESULT put_PromptForCredsOnClient(
  [in]  VARIANT_BOOL fPromptForCredsOnClient
);

HRESULT get_PromptForCredsOnClient(
  [out] VARIANT_BOOL *pfPromptForCredsOnClient
);
```



## <a name="property-value"></a><span data-ttu-id="b7f05-120">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="b7f05-120">Property value</span></span>

<span data-ttu-id="b7f05-121">Определяет, отображает ли клиентский элемент управления диалоговое окно с запросом учетных данных.</span><span class="sxs-lookup"><span data-stu-id="b7f05-121">Sets whether the client control displays a dialog box that prompts for credentials.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b7f05-122">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="b7f05-122">Error codes</span></span>

<span data-ttu-id="b7f05-123">При успешном выполнении возвращает значение **\_ ОК** .</span><span class="sxs-lookup"><span data-stu-id="b7f05-123">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7f05-124">Требования</span><span class="sxs-lookup"><span data-stu-id="b7f05-124">Requirements</span></span>



| <span data-ttu-id="b7f05-125">Требование</span><span class="sxs-lookup"><span data-stu-id="b7f05-125">Requirement</span></span> | <span data-ttu-id="b7f05-126">Значение</span><span class="sxs-lookup"><span data-stu-id="b7f05-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7f05-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b7f05-127">Minimum supported client</span></span><br/> | <span data-ttu-id="b7f05-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b7f05-128">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="b7f05-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b7f05-129">Minimum supported server</span></span><br/> | <span data-ttu-id="b7f05-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b7f05-130">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="b7f05-131">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="b7f05-131">Type library</span></span><br/>             | <dl> <span data-ttu-id="b7f05-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b7f05-132"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="b7f05-133">DLL</span><span class="sxs-lookup"><span data-stu-id="b7f05-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b7f05-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b7f05-134"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="b7f05-135">IID</span><span class="sxs-lookup"><span data-stu-id="b7f05-135">IID</span></span><br/>                      | <span data-ttu-id="b7f05-136">IMsRdpClientNonScriptable4 определяется как f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb</span><span class="sxs-lookup"><span data-stu-id="b7f05-136">IMsRdpClientNonScriptable4 is defined as f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b7f05-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b7f05-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7f05-138">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="b7f05-138">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="b7f05-139">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="b7f05-139">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> </dl>

 

 





