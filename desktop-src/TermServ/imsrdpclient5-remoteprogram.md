---
title: IMsRdpClient5 Ремотепрограм, свойство
description: Извлекает объект, который поддерживает интерфейс Итсремотепрограм.
ms.assetid: 013f613b-af7b-4cc5-be1f-d45833806e3b
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Ремотепрограм
- Службы удаленных рабочих столов свойства Ремотепрограм, интерфейс IMsRdpClient5
- Службы удаленных рабочих столов интерфейса IMsRdpClient5, свойство Ремотепрограм
- Службы удаленных рабочих столов свойства Ремотепрограм, интерфейс IMsRdpClient6
- Службы удаленных рабочих столов интерфейса IMsRdpClient6, свойство Ремотепрограм
- Службы удаленных рабочих столов свойства Ремотепрограм, интерфейс IMsRdpClient7
- Службы удаленных рабочих столов интерфейса IMsRdpClient7, свойство Ремотепрограм
- Службы удаленных рабочих столов свойства Ремотепрограм, интерфейс IMsRdpClient8
- Службы удаленных рабочих столов интерфейса IMsRdpClient8, свойство Ремотепрограм
- Службы удаленных рабочих столов свойства Ремотепрограм, интерфейс IMsRdpClient9
- Службы удаленных рабочих столов интерфейса IMsRdpClient9, свойство Ремотепрограм
- Службы удаленных рабочих столов свойства Ремотепрограм, интерфейс IMsRdpClient10
- Службы удаленных рабочих столов интерфейса IMsRdpClient10, свойство Ремотепрограм
topic_type:
- apiref
api_name:
- IMsRdpClient5.RemoteProgram
- IMsRdpClient5.get_RemoteProgram
- IMsRdpClient6.RemoteProgram
- IMsRdpClient6.get_RemoteProgram
- IMsRdpClient7.RemoteProgram
- IMsRdpClient7.get_RemoteProgram
- IMsRdpClient8.RemoteProgram
- IMsRdpClient8.get_RemoteProgram
- IMsRdpClient9.RemoteProgram
- IMsRdpClient9.get_RemoteProgram
- IMsRdpClient10.RemoteProgram
- IMsRdpClient10.get_RemoteProgram
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 267e367af090a7fd70e9482406104fd0403d63f0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489681"
---
# <a name="imsrdpclient5remoteprogram-property"></a><span data-ttu-id="dfee9-116">Свойство IMsRdpClient5:: Ремотепрограм</span><span class="sxs-lookup"><span data-stu-id="dfee9-116">IMsRdpClient5::RemoteProgram property</span></span>

<span data-ttu-id="dfee9-117">Извлекает объект, который поддерживает интерфейс [**итсремотепрограм**](itsremoteprogram.md) .</span><span class="sxs-lookup"><span data-stu-id="dfee9-117">Retrieves an object that supports the [**ITSRemoteProgram**](itsremoteprogram.md) interface.</span></span>

<span data-ttu-id="dfee9-118">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="dfee9-118">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="dfee9-119">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dfee9-119">Syntax</span></span>


```C++
HRESULT get_RemoteProgram(
  [out] ITSRemoteProgram **ppRemoteProgram
);
```



## <a name="property-value"></a><span data-ttu-id="dfee9-120">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="dfee9-120">Property value</span></span>

<span data-ttu-id="dfee9-121">Указатель интерфейса [**итсремотепрограм**](itsremoteprogram.md) .</span><span class="sxs-lookup"><span data-stu-id="dfee9-121">An [**ITSRemoteProgram**](itsremoteprogram.md) interface pointer.</span></span>

## <a name="requirements"></a><span data-ttu-id="dfee9-122">Требования</span><span class="sxs-lookup"><span data-stu-id="dfee9-122">Requirements</span></span>



| <span data-ttu-id="dfee9-123">Требование</span><span class="sxs-lookup"><span data-stu-id="dfee9-123">Requirement</span></span> | <span data-ttu-id="dfee9-124">Значение</span><span class="sxs-lookup"><span data-stu-id="dfee9-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dfee9-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dfee9-125">Minimum supported client</span></span><br/> | <span data-ttu-id="dfee9-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dfee9-126">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="dfee9-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dfee9-127">Minimum supported server</span></span><br/> | <span data-ttu-id="dfee9-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dfee9-128">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="dfee9-129">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="dfee9-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="dfee9-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dfee9-130"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="dfee9-131">DLL</span><span class="sxs-lookup"><span data-stu-id="dfee9-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dfee9-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dfee9-132"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="dfee9-133">IID</span><span class="sxs-lookup"><span data-stu-id="dfee9-133">IID</span></span><br/>                      | <span data-ttu-id="dfee9-134">IID \_ IMsRdpClient5 определен как 4eb5335b-6429-477d-B922-e06a28ecd8bf</span><span class="sxs-lookup"><span data-stu-id="dfee9-134">IID\_IMsRdpClient5 is defined as 4eb5335b-6429-477d-b922-e06a28ecd8bf</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="dfee9-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dfee9-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dfee9-136">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="dfee9-136">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="dfee9-137">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="dfee9-137">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="dfee9-138">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="dfee9-138">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="dfee9-139">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="dfee9-139">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="dfee9-140">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="dfee9-140">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="dfee9-141">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="dfee9-141">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





