---
title: IMsRdpClient5 AdvancedSettings6, свойство
description: Извлекает интерфейс IMsRdpClientAdvancedSettings5.
ms.assetid: b6a4efcf-87c3-438c-b6de-8a497ee5939d
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства AdvancedSettings6
- Службы удаленных рабочих столов свойства AdvancedSettings6, интерфейс IMsRdpClient5
- Службы удаленных рабочих столов интерфейса IMsRdpClient5, свойство AdvancedSettings6
- Службы удаленных рабочих столов свойства AdvancedSettings6, интерфейс IMsRdpClient6
- Службы удаленных рабочих столов интерфейса IMsRdpClient6, свойство AdvancedSettings6
- Службы удаленных рабочих столов свойства AdvancedSettings6, интерфейс IMsRdpClient7
- Службы удаленных рабочих столов интерфейса IMsRdpClient7, свойство AdvancedSettings6
- Службы удаленных рабочих столов свойства AdvancedSettings6, интерфейс IMsRdpClient8
- Службы удаленных рабочих столов интерфейса IMsRdpClient8, свойство AdvancedSettings6
- Службы удаленных рабочих столов свойства AdvancedSettings6, интерфейс IMsRdpClient9
- Службы удаленных рабочих столов интерфейса IMsRdpClient9, свойство AdvancedSettings6
- Службы удаленных рабочих столов свойства AdvancedSettings6, интерфейс IMsRdpClient10
- Службы удаленных рабочих столов интерфейса IMsRdpClient10, свойство AdvancedSettings6
topic_type:
- apiref
api_name:
- IMsRdpClient5.AdvancedSettings6
- IMsRdpClient5.get_AdvancedSettings6
- IMsRdpClient6.AdvancedSettings6
- IMsRdpClient6.get_AdvancedSettings6
- IMsRdpClient7.AdvancedSettings6
- IMsRdpClient7.get_AdvancedSettings6
- IMsRdpClient8.AdvancedSettings6
- IMsRdpClient8.get_AdvancedSettings6
- IMsRdpClient9.AdvancedSettings6
- IMsRdpClient9.get_AdvancedSettings6
- IMsRdpClient10.AdvancedSettings6
- IMsRdpClient10.get_AdvancedSettings6
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b93d2395ec7e673e50023867f4602eea5c2d9fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892662"
---
# <a name="imsrdpclient5advancedsettings6-property"></a><span data-ttu-id="dae2b-116">Свойство IMsRdpClient5:: AdvancedSettings6</span><span class="sxs-lookup"><span data-stu-id="dae2b-116">IMsRdpClient5::AdvancedSettings6 property</span></span>

<span data-ttu-id="dae2b-117">Извлекает интерфейс [**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md) .</span><span class="sxs-lookup"><span data-stu-id="dae2b-117">Retrieves the [**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md) interface.</span></span>

<span data-ttu-id="dae2b-118">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="dae2b-118">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="dae2b-119">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dae2b-119">Syntax</span></span>


```C++
HRESULT get_AdvancedSettings6(
  [out] IMsRdpClientAdvancedSettings5 **ppAdvSettings
);
```



## <a name="property-value"></a><span data-ttu-id="dae2b-120">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="dae2b-120">Property value</span></span>

<span data-ttu-id="dae2b-121">Указатель интерфейса [**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="dae2b-121">An [**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings-interface.md) interface pointer.</span></span>

## <a name="requirements"></a><span data-ttu-id="dae2b-122">Требования</span><span class="sxs-lookup"><span data-stu-id="dae2b-122">Requirements</span></span>



| <span data-ttu-id="dae2b-123">Требование</span><span class="sxs-lookup"><span data-stu-id="dae2b-123">Requirement</span></span> | <span data-ttu-id="dae2b-124">Значение</span><span class="sxs-lookup"><span data-stu-id="dae2b-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dae2b-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dae2b-125">Minimum supported client</span></span><br/> | <span data-ttu-id="dae2b-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dae2b-126">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="dae2b-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dae2b-127">Minimum supported server</span></span><br/> | <span data-ttu-id="dae2b-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dae2b-128">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="dae2b-129">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="dae2b-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="dae2b-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dae2b-130"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="dae2b-131">DLL</span><span class="sxs-lookup"><span data-stu-id="dae2b-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dae2b-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dae2b-132"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="dae2b-133">IID</span><span class="sxs-lookup"><span data-stu-id="dae2b-133">IID</span></span><br/>                      | <span data-ttu-id="dae2b-134">IID \_ IMsRdpClient5 определен как 4eb5335b-6429-477d-B922-e06a28ecd8bf</span><span class="sxs-lookup"><span data-stu-id="dae2b-134">IID\_IMsRdpClient5 is defined as 4eb5335b-6429-477d-b922-e06a28ecd8bf</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="dae2b-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dae2b-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dae2b-136">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="dae2b-136">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="dae2b-137">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="dae2b-137">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="dae2b-138">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="dae2b-138">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="dae2b-139">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="dae2b-139">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="dae2b-140">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="dae2b-140">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="dae2b-141">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="dae2b-141">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





