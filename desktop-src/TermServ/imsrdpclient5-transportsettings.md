---
title: IMsRdpClient5 TransportSettings, свойство
description: Возвращает сведения о том, что было передано через скрипт в интерфейс Имсрдпклиенттранспортсеттингс.
ms.assetid: 38f5a735-55c7-425a-835b-22f6e0900d57
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства TransportSettings
- Службы удаленных рабочих столов свойства TransportSettings, интерфейс IMsRdpClient5
- Службы удаленных рабочих столов интерфейса IMsRdpClient5, свойство TransportSettings
- Службы удаленных рабочих столов свойства TransportSettings, интерфейс IMsRdpClient6
- Службы удаленных рабочих столов интерфейса IMsRdpClient6, свойство TransportSettings
- Службы удаленных рабочих столов свойства TransportSettings, интерфейс IMsRdpClient7
- Службы удаленных рабочих столов интерфейса IMsRdpClient7, свойство TransportSettings
- Службы удаленных рабочих столов свойства TransportSettings, интерфейс IMsRdpClient8
- Службы удаленных рабочих столов интерфейса IMsRdpClient8, свойство TransportSettings
- Службы удаленных рабочих столов свойства TransportSettings, интерфейс IMsRdpClient9
- Службы удаленных рабочих столов интерфейса IMsRdpClient9, свойство TransportSettings
- Службы удаленных рабочих столов свойства TransportSettings, интерфейс IMsRdpClient10
- Службы удаленных рабочих столов интерфейса IMsRdpClient10, свойство TransportSettings
topic_type:
- apiref
api_name:
- IMsRdpClient5.TransportSettings
- IMsRdpClient5.get_TransportSettings
- IMsRdpClient6.TransportSettings
- IMsRdpClient6.get_TransportSettings
- IMsRdpClient7.TransportSettings
- IMsRdpClient7.get_TransportSettings
- IMsRdpClient8.TransportSettings
- IMsRdpClient8.get_TransportSettings
- IMsRdpClient9.TransportSettings
- IMsRdpClient9.get_TransportSettings
- IMsRdpClient10.TransportSettings
- IMsRdpClient10.get_TransportSettings
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 077ed94253c0ebadeed775e54c4db2ae6cbacf13
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135398"
---
# <a name="imsrdpclient5transportsettings-property"></a><span data-ttu-id="67a42-116">Свойство IMsRdpClient5:: TransportSettings</span><span class="sxs-lookup"><span data-stu-id="67a42-116">IMsRdpClient5::TransportSettings property</span></span>

<span data-ttu-id="67a42-117">Возвращает сведения о том, что было передано через скрипт в интерфейс [**имсрдпклиенттранспортсеттингс**](imsrdpclienttransportsettings.md) .</span><span class="sxs-lookup"><span data-stu-id="67a42-117">Retrieves what was passed through a script to the [**IMsRdpClientTransportSettings**](imsrdpclienttransportsettings.md) interface.</span></span>

<span data-ttu-id="67a42-118">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="67a42-118">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="67a42-119">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="67a42-119">Syntax</span></span>


```C++
HRESULT get_TransportSettings(
  [out] IMsRdpClientTransportSettings **ppXportSet
);
```



## <a name="property-value"></a><span data-ttu-id="67a42-120">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="67a42-120">Property value</span></span>

<span data-ttu-id="67a42-121">Указатель интерфейса [**имсрдпклиенттранспортсеттингс**](imsrdpclienttransportsettings.md) .</span><span class="sxs-lookup"><span data-stu-id="67a42-121">An [**IMsRdpClientTransportSettings**](imsrdpclienttransportsettings.md) interface pointer.</span></span>

## <a name="requirements"></a><span data-ttu-id="67a42-122">Требования</span><span class="sxs-lookup"><span data-stu-id="67a42-122">Requirements</span></span>



| <span data-ttu-id="67a42-123">Требование</span><span class="sxs-lookup"><span data-stu-id="67a42-123">Requirement</span></span> | <span data-ttu-id="67a42-124">Значение</span><span class="sxs-lookup"><span data-stu-id="67a42-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="67a42-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="67a42-125">Minimum supported client</span></span><br/> | <span data-ttu-id="67a42-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="67a42-126">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="67a42-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="67a42-127">Minimum supported server</span></span><br/> | <span data-ttu-id="67a42-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="67a42-128">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="67a42-129">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="67a42-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="67a42-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="67a42-130"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="67a42-131">DLL</span><span class="sxs-lookup"><span data-stu-id="67a42-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="67a42-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="67a42-132"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="67a42-133">IID</span><span class="sxs-lookup"><span data-stu-id="67a42-133">IID</span></span><br/>                      | <span data-ttu-id="67a42-134">IID \_ IMsRdpClient5 определен как 4eb5335b-6429-477d-B922-e06a28ecd8bf</span><span class="sxs-lookup"><span data-stu-id="67a42-134">IID\_IMsRdpClient5 is defined as 4eb5335b-6429-477d-b922-e06a28ecd8bf</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="67a42-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="67a42-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67a42-136">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="67a42-136">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="67a42-137">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="67a42-137">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="67a42-138">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="67a42-138">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="67a42-139">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="67a42-139">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="67a42-140">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="67a42-140">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="67a42-141">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="67a42-141">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





