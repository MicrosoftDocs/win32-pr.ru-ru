---
title: IMsRdpClient6 AdvancedSettings7, свойство
description: Извлекает интерфейс IMsRdpClientAdvancedSettings6.
ms.assetid: 64b05c66-ac6a-4190-9df8-4a88dbc46c3f
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства AdvancedSettings7
- Службы удаленных рабочих столов свойства AdvancedSettings7, интерфейс IMsRdpClient6
- Службы удаленных рабочих столов интерфейса IMsRdpClient6, свойство AdvancedSettings7
- Службы удаленных рабочих столов свойства AdvancedSettings7, интерфейс IMsRdpClient7
- Службы удаленных рабочих столов интерфейса IMsRdpClient7, свойство AdvancedSettings7
- Службы удаленных рабочих столов свойства AdvancedSettings7, интерфейс IMsRdpClient8
- Службы удаленных рабочих столов интерфейса IMsRdpClient8, свойство AdvancedSettings7
- Службы удаленных рабочих столов свойства AdvancedSettings7, интерфейс IMsRdpClient9
- Службы удаленных рабочих столов интерфейса IMsRdpClient9, свойство AdvancedSettings7
- Службы удаленных рабочих столов свойства AdvancedSettings7, интерфейс IMsRdpClient10
- Службы удаленных рабочих столов интерфейса IMsRdpClient10, свойство AdvancedSettings7
- Службы удаленных рабочих столов свойства AdvancedSettings7, объект MsRdpClient6
- Службы удаленных рабочих столов объекта MsRdpClient6, свойство AdvancedSettings7
topic_type:
- apiref
api_name:
- IMsRdpClient6.AdvancedSettings7
- IMsRdpClient6.get_AdvancedSettings7
- IMsRdpClient7.AdvancedSettings7
- IMsRdpClient7.get_AdvancedSettings7
- IMsRdpClient8.AdvancedSettings7
- IMsRdpClient8.get_AdvancedSettings7
- IMsRdpClient9.AdvancedSettings7
- IMsRdpClient9.get_AdvancedSettings7
- IMsRdpClient10.AdvancedSettings7
- IMsRdpClient10.get_AdvancedSettings7
- MsRdpClient6.AdvancedSettings7
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f51d364c14be3311272455e040d55f277f3fb136
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415068"
---
# <a name="imsrdpclient6advancedsettings7-property"></a><span data-ttu-id="21105-116">Свойство IMsRdpClient6:: AdvancedSettings7</span><span class="sxs-lookup"><span data-stu-id="21105-116">IMsRdpClient6::AdvancedSettings7 property</span></span>

<span data-ttu-id="21105-117">Извлекает интерфейс [**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings5.md) .</span><span class="sxs-lookup"><span data-stu-id="21105-117">Retrieves the [**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings5.md) interface.</span></span>

<span data-ttu-id="21105-118">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="21105-118">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="21105-119">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="21105-119">Syntax</span></span>


```C++
HRESULT get_AdvancedSettings7(
  [out] IMsRdpClientAdvancedSettings6 **ppAdvSettings
);
```



## <a name="property-value"></a><span data-ttu-id="21105-120">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="21105-120">Property value</span></span>

<span data-ttu-id="21105-121">Указатель интерфейса [**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md) .</span><span class="sxs-lookup"><span data-stu-id="21105-121">An [**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md) interface pointer.</span></span>

## <a name="requirements"></a><span data-ttu-id="21105-122">Требования</span><span class="sxs-lookup"><span data-stu-id="21105-122">Requirements</span></span>



| <span data-ttu-id="21105-123">Требование</span><span class="sxs-lookup"><span data-stu-id="21105-123">Requirement</span></span> | <span data-ttu-id="21105-124">Значение</span><span class="sxs-lookup"><span data-stu-id="21105-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="21105-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="21105-125">Minimum supported client</span></span><br/> | <span data-ttu-id="21105-126">Windows Vista с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="21105-126">Windows Vista with SP1</span></span><br/>                                                      |
| <span data-ttu-id="21105-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="21105-127">Minimum supported server</span></span><br/> | <span data-ttu-id="21105-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="21105-128">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="21105-129">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="21105-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="21105-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="21105-130"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="21105-131">DLL</span><span class="sxs-lookup"><span data-stu-id="21105-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="21105-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="21105-132"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="21105-133">IID</span><span class="sxs-lookup"><span data-stu-id="21105-133">IID</span></span><br/>                      | <span data-ttu-id="21105-134">IID \_ IMsRdpClient6 определен как d43b7d80-8517-4b6d-9eac-96ad6800d7f2</span><span class="sxs-lookup"><span data-stu-id="21105-134">IID\_IMsRdpClient6 is defined as d43b7d80-8517-4b6d-9eac-96ad6800d7f2</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="21105-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="21105-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21105-136">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="21105-136">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="21105-137">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="21105-137">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="21105-138">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="21105-138">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="21105-139">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="21105-139">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="21105-140">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="21105-140">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





