---
title: IMsRdpClientNonScriptable4 Трустедзонесите, свойство
description: Указывает, находится ли веб-сайт, с которого пользователь запустил подключение, в списке надежных сайтов клиентского компьютера пользователя.
ms.assetid: cb7efacc-b13b-494c-ab02-35c4f914744c
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Трустедзонесите
- Службы удаленных рабочих столов свойства Трустедзонесите, интерфейс IMsRdpClientNonScriptable4
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable4, свойство Трустедзонесите
- Службы удаленных рабочих столов свойства Трустедзонесите, интерфейс IMsRdpClientNonScriptable5
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable5, свойство Трустедзонесите
- Службы удаленных рабочих столов свойства Трустедзонесите, объект MsRdpClient6
- Службы удаленных рабочих столов объекта MsRdpClient6, свойство Трустедзонесите
- Службы удаленных рабочих столов свойства Трустедзонесите, объект MsRdpClient7
- Службы удаленных рабочих столов объекта MsRdpClient7, свойство Трустедзонесите
- Службы удаленных рабочих столов свойства Трустедзонесите, объект MsRdpClient8
- Службы удаленных рабочих столов объекта MsRdpClient8, свойство Трустедзонесите
- Службы удаленных рабочих столов свойства Трустедзонесите, объект MsRdpClient9
- Службы удаленных рабочих столов объекта MsRdpClient9, свойство Трустедзонесите
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable4.TrustedZoneSite
- IMsRdpClientNonScriptable4.get_TrustedZoneSite
- IMsRdpClientNonScriptable4.put_TrustedZoneSite
- IMsRdpClientNonScriptable5.TrustedZoneSite
- IMsRdpClientNonScriptable5.get_TrustedZoneSite
- IMsRdpClientNonScriptable5.put_TrustedZoneSite
- MsRdpClient6.TrustedZoneSite
- MsRdpClient7.TrustedZoneSite
- MsRdpClient8.TrustedZoneSite
- MsRdpClient9.TrustedZoneSite
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d791b5eff3346f61f999ea1f4f78bc41a5acea0e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415768"
---
# <a name="imsrdpclientnonscriptable4trustedzonesite-property"></a><span data-ttu-id="bc034-116">Свойство IMsRdpClientNonScriptable4:: Трустедзонесите</span><span class="sxs-lookup"><span data-stu-id="bc034-116">IMsRdpClientNonScriptable4::TrustedZoneSite property</span></span>

<span data-ttu-id="bc034-117">Указывает, находится ли веб-сайт, с которого пользователь запустил подключение, в списке надежных сайтов клиентского компьютера пользователя.</span><span class="sxs-lookup"><span data-stu-id="bc034-117">Specifies whether the website from which the user launched the connection is in the trusted sites list of the user's client computer.</span></span>

<span data-ttu-id="bc034-118">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="bc034-118">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc034-119">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bc034-119">Syntax</span></span>


```C++
HRESULT put_TrustedZoneSite(
  [in]  VARIANT_BOOL fIsTrustedZone
);

HRESULT get_TrustedZoneSite(
  [out] VARIANT_BOOL *pfIsTrustedZone
);
```



## <a name="property-value"></a><span data-ttu-id="bc034-120">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="bc034-120">Property value</span></span>

<span data-ttu-id="bc034-121">Задает свойство Трустедзонесите.</span><span class="sxs-lookup"><span data-stu-id="bc034-121">Sets the TrustedZoneSite property.</span></span> <span data-ttu-id="bc034-122">Этот метод не влияет на то, находится ли веб-сайт, с которого пользователь запустил подключение, в списке надежных сайтов клиентского компьютера.</span><span class="sxs-lookup"><span data-stu-id="bc034-122">This method has no effect on whether the website from which the user launched the connection is in the trusted sites list of the client computer.</span></span>

## <a name="error-codes"></a><span data-ttu-id="bc034-123">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="bc034-123">Error codes</span></span>

<span data-ttu-id="bc034-124">При успешном выполнении возвращает значение **\_ ОК** .</span><span class="sxs-lookup"><span data-stu-id="bc034-124">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc034-125">Требования</span><span class="sxs-lookup"><span data-stu-id="bc034-125">Requirements</span></span>



| <span data-ttu-id="bc034-126">Требование</span><span class="sxs-lookup"><span data-stu-id="bc034-126">Requirement</span></span> | <span data-ttu-id="bc034-127">Значение</span><span class="sxs-lookup"><span data-stu-id="bc034-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc034-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bc034-128">Minimum supported client</span></span><br/> | <span data-ttu-id="bc034-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bc034-129">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="bc034-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bc034-130">Minimum supported server</span></span><br/> | <span data-ttu-id="bc034-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bc034-131">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="bc034-132">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="bc034-132">Type library</span></span><br/>             | <dl> <span data-ttu-id="bc034-133"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bc034-133"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="bc034-134">DLL</span><span class="sxs-lookup"><span data-stu-id="bc034-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bc034-135"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bc034-135"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="bc034-136">IID</span><span class="sxs-lookup"><span data-stu-id="bc034-136">IID</span></span><br/>                      | <span data-ttu-id="bc034-137">IMsRdpClientNonScriptable4 определяется как f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb</span><span class="sxs-lookup"><span data-stu-id="bc034-137">IMsRdpClientNonScriptable4 is defined as f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bc034-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bc034-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc034-139">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="bc034-139">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="bc034-140">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="bc034-140">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> </dl>

 

 





