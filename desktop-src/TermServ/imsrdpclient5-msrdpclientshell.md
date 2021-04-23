---
title: IMsRdpClient5 Мсрдпклиентшелл, свойство
description: Получает интерфейс параметра клиента с скриптом Имсрдпклиентшелл.
ms.assetid: cc56cec4-779d-4b51-8e94-ae0dd9bae997
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Мсрдпклиентшелл
- Службы удаленных рабочих столов свойства Мсрдпклиентшелл, интерфейс IMsRdpClient5
- Службы удаленных рабочих столов интерфейса IMsRdpClient5, свойство Мсрдпклиентшелл
- Службы удаленных рабочих столов свойства Мсрдпклиентшелл, интерфейс IMsRdpClient6
- Службы удаленных рабочих столов интерфейса IMsRdpClient6, свойство Мсрдпклиентшелл
- Службы удаленных рабочих столов свойства Мсрдпклиентшелл, интерфейс IMsRdpClient7
- Службы удаленных рабочих столов интерфейса IMsRdpClient7, свойство Мсрдпклиентшелл
- Службы удаленных рабочих столов свойства Мсрдпклиентшелл, интерфейс IMsRdpClient8
- Службы удаленных рабочих столов интерфейса IMsRdpClient8, свойство Мсрдпклиентшелл
- Службы удаленных рабочих столов свойства Мсрдпклиентшелл, интерфейс IMsRdpClient9
- Службы удаленных рабочих столов интерфейса IMsRdpClient9, свойство Мсрдпклиентшелл
- Службы удаленных рабочих столов свойства Мсрдпклиентшелл, интерфейс IMsRdpClient10
- Службы удаленных рабочих столов интерфейса IMsRdpClient10, свойство Мсрдпклиентшелл
topic_type:
- apiref
api_name:
- IMsRdpClient5.MsRdpClientShell
- IMsRdpClient5.get_MsRdpClientShell
- IMsRdpClient6.MsRdpClientShell
- IMsRdpClient6.get_MsRdpClientShell
- IMsRdpClient7.MsRdpClientShell
- IMsRdpClient7.get_MsRdpClientShell
- IMsRdpClient8.MsRdpClientShell
- IMsRdpClient8.get_MsRdpClientShell
- IMsRdpClient9.MsRdpClientShell
- IMsRdpClient9.get_MsRdpClientShell
- IMsRdpClient10.MsRdpClientShell
- IMsRdpClient10.get_MsRdpClientShell
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46129dc4736b50e8b6a650cc7a59f9b238da56e2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137563"
---
# <a name="imsrdpclient5msrdpclientshell-property"></a><span data-ttu-id="01d81-116">Свойство IMsRdpClient5:: Мсрдпклиентшелл</span><span class="sxs-lookup"><span data-stu-id="01d81-116">IMsRdpClient5::MsRdpClientShell property</span></span>

<span data-ttu-id="01d81-117">Получает интерфейс параметра клиента с скриптом [**имсрдпклиентшелл**](imsrdpclientshell.md).</span><span class="sxs-lookup"><span data-stu-id="01d81-117">Retrieves the scriptable client setting interface [**IMsRdpClientShell**](imsrdpclientshell.md).</span></span>

<span data-ttu-id="01d81-118">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="01d81-118">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="01d81-119">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="01d81-119">Syntax</span></span>


```C++
HRESULT get_MsRdpClientShell(
  [out] IMsRdpClientShell **ppLauncher
);
```



## <a name="property-value"></a><span data-ttu-id="01d81-120">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="01d81-120">Property value</span></span>

<span data-ttu-id="01d81-121">Указатель интерфейса [**имсрдпклиентшелл**](imsrdpclientshell.md) .</span><span class="sxs-lookup"><span data-stu-id="01d81-121">An [**IMsRdpClientShell**](imsrdpclientshell.md) interface pointer.</span></span>

## <a name="requirements"></a><span data-ttu-id="01d81-122">Требования</span><span class="sxs-lookup"><span data-stu-id="01d81-122">Requirements</span></span>



| <span data-ttu-id="01d81-123">Требование</span><span class="sxs-lookup"><span data-stu-id="01d81-123">Requirement</span></span> | <span data-ttu-id="01d81-124">Значение</span><span class="sxs-lookup"><span data-stu-id="01d81-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="01d81-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="01d81-125">Minimum supported client</span></span><br/> | <span data-ttu-id="01d81-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="01d81-126">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="01d81-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="01d81-127">Minimum supported server</span></span><br/> | <span data-ttu-id="01d81-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="01d81-128">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="01d81-129">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="01d81-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="01d81-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="01d81-130"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="01d81-131">DLL</span><span class="sxs-lookup"><span data-stu-id="01d81-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="01d81-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="01d81-132"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="01d81-133">IID</span><span class="sxs-lookup"><span data-stu-id="01d81-133">IID</span></span><br/>                      | <span data-ttu-id="01d81-134">IID \_ IMsRdpClient5 определен как 4eb5335b-6429-477d-B922-e06a28ecd8bf</span><span class="sxs-lookup"><span data-stu-id="01d81-134">IID\_IMsRdpClient5 is defined as 4eb5335b-6429-477d-b922-e06a28ecd8bf</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="01d81-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="01d81-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01d81-136">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="01d81-136">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="01d81-137">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="01d81-137">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="01d81-138">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="01d81-138">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="01d81-139">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="01d81-139">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="01d81-140">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="01d81-140">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="01d81-141">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="01d81-141">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





