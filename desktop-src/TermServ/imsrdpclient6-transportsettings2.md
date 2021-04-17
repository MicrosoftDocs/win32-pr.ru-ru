---
title: IMsRdpClient6 TransportSettings2, свойство
description: Извлекает интерфейс IMsRdpClientTransportSettings2.
ms.assetid: 5cd3c745-b360-43fb-b780-c526ed539db0
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства TransportSettings2
- Службы удаленных рабочих столов свойства TransportSettings2, интерфейс IMsRdpClient6
- Службы удаленных рабочих столов интерфейса IMsRdpClient6, свойство TransportSettings2
- Службы удаленных рабочих столов свойства TransportSettings2, интерфейс IMsRdpClient7
- Службы удаленных рабочих столов интерфейса IMsRdpClient7, свойство TransportSettings2
- Службы удаленных рабочих столов свойства TransportSettings2, интерфейс IMsRdpClient8
- Службы удаленных рабочих столов интерфейса IMsRdpClient8, свойство TransportSettings2
- Службы удаленных рабочих столов свойства TransportSettings2, интерфейс IMsRdpClient9
- Службы удаленных рабочих столов интерфейса IMsRdpClient9, свойство TransportSettings2
- Службы удаленных рабочих столов свойства TransportSettings2, интерфейс IMsRdpClient10
- Службы удаленных рабочих столов интерфейса IMsRdpClient10, свойство TransportSettings2
topic_type:
- apiref
api_name:
- IMsRdpClient6.TransportSettings2
- IMsRdpClient6.get_TransportSettings2
- IMsRdpClient7.TransportSettings2
- IMsRdpClient7.get_TransportSettings2
- IMsRdpClient8.TransportSettings2
- IMsRdpClient8.get_TransportSettings2
- IMsRdpClient9.TransportSettings2
- IMsRdpClient9.get_TransportSettings2
- IMsRdpClient10.TransportSettings2
- IMsRdpClient10.get_TransportSettings2
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91ba11975e0e065e0cfcce91eb22402153acf236
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681808"
---
# <a name="imsrdpclient6transportsettings2-property"></a><span data-ttu-id="24bb4-114">Свойство IMsRdpClient6:: TransportSettings2</span><span class="sxs-lookup"><span data-stu-id="24bb4-114">IMsRdpClient6::TransportSettings2 property</span></span>

<span data-ttu-id="24bb4-115">Извлекает интерфейс [**IMsRdpClientTransportSettings2**](imsrdpclienttransportsettings2.md) .</span><span class="sxs-lookup"><span data-stu-id="24bb4-115">Retrieves the [**IMsRdpClientTransportSettings2**](imsrdpclienttransportsettings2.md) interface.</span></span>

<span data-ttu-id="24bb4-116">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="24bb4-116">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="24bb4-117">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="24bb4-117">Syntax</span></span>


```C++
HRESULT get_TransportSettings2(
  [out] IMsRdpClientTransportSettings2 **ppXportSet2
);
```



## <a name="property-value"></a><span data-ttu-id="24bb4-118">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="24bb4-118">Property value</span></span>

<span data-ttu-id="24bb4-119">Указатель интерфейса [**IMsRdpClientTransportSettings2**](imsrdpclienttransportsettings2.md) .</span><span class="sxs-lookup"><span data-stu-id="24bb4-119">An [**IMsRdpClientTransportSettings2**](imsrdpclienttransportsettings2.md) interface pointer.</span></span>

## <a name="requirements"></a><span data-ttu-id="24bb4-120">Требования</span><span class="sxs-lookup"><span data-stu-id="24bb4-120">Requirements</span></span>



| <span data-ttu-id="24bb4-121">Требование</span><span class="sxs-lookup"><span data-stu-id="24bb4-121">Requirement</span></span> | <span data-ttu-id="24bb4-122">Значение</span><span class="sxs-lookup"><span data-stu-id="24bb4-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="24bb4-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="24bb4-123">Minimum supported client</span></span><br/> | <span data-ttu-id="24bb4-124">Windows Vista с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="24bb4-124">Windows Vista with SP1</span></span><br/>                                                      |
| <span data-ttu-id="24bb4-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="24bb4-125">Minimum supported server</span></span><br/> | <span data-ttu-id="24bb4-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="24bb4-126">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="24bb4-127">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="24bb4-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="24bb4-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="24bb4-128"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="24bb4-129">DLL</span><span class="sxs-lookup"><span data-stu-id="24bb4-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="24bb4-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="24bb4-130"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="24bb4-131">IID</span><span class="sxs-lookup"><span data-stu-id="24bb4-131">IID</span></span><br/>                      | <span data-ttu-id="24bb4-132">IID \_ IMsRdpClient6 определен как d43b7d80-8517-4b6d-9eac-96ad6800d7f2</span><span class="sxs-lookup"><span data-stu-id="24bb4-132">IID\_IMsRdpClient6 is defined as d43b7d80-8517-4b6d-9eac-96ad6800d7f2</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="24bb4-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="24bb4-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24bb4-134">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="24bb4-134">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="24bb4-135">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="24bb4-135">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="24bb4-136">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="24bb4-136">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="24bb4-137">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="24bb4-137">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="24bb4-138">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="24bb4-138">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





