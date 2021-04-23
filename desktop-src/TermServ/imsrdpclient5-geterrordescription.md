---
title: IMsRdpClient5 Жетеррордескриптион, метод
description: Возвращает описание ошибки для событий отключения сеанса.
ms.assetid: 8c8f7b10-7f79-4586-845e-e99f5ca81905
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Жетеррордескриптион
- Службы удаленных рабочих столов метода Жетеррордескриптион, интерфейс IMsRdpClient5
- Службы удаленных рабочих столов интерфейса IMsRdpClient5, метод Жетеррордескриптион
- Службы удаленных рабочих столов метода Жетеррордескриптион, интерфейс IMsRdpClient6
- Службы удаленных рабочих столов интерфейса IMsRdpClient6, метод Жетеррордескриптион
- Службы удаленных рабочих столов метода Жетеррордескриптион, интерфейс IMsRdpClient7
- Службы удаленных рабочих столов интерфейса IMsRdpClient7, метод Жетеррордескриптион
- Службы удаленных рабочих столов метода Жетеррордескриптион, интерфейс IMsRdpClient8
- Службы удаленных рабочих столов интерфейса IMsRdpClient8, метод Жетеррордескриптион
- Службы удаленных рабочих столов метода Жетеррордескриптион, интерфейс IMsRdpClient9
- Службы удаленных рабочих столов интерфейса IMsRdpClient9, метод Жетеррордескриптион
- Службы удаленных рабочих столов метода Жетеррордескриптион, интерфейс IMsRdpClient10
- Службы удаленных рабочих столов интерфейса IMsRdpClient10, метод Жетеррордескриптион
topic_type:
- apiref
api_name:
- IMsRdpClient5.GetErrorDescription
- IMsRdpClient6.GetErrorDescription
- IMsRdpClient7.GetErrorDescription
- IMsRdpClient8.GetErrorDescription
- IMsRdpClient9.GetErrorDescription
- IMsRdpClient10.GetErrorDescription
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c402a0128286964ddeb1c53cd805e4ef6414bfb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104416049"
---
# <a name="imsrdpclient5geterrordescription-method"></a><span data-ttu-id="53c3e-116">Метод IMsRdpClient5:: Жетеррордескриптион</span><span class="sxs-lookup"><span data-stu-id="53c3e-116">IMsRdpClient5::GetErrorDescription method</span></span>

<span data-ttu-id="53c3e-117">Возвращает описание ошибки для событий отключения сеанса.</span><span class="sxs-lookup"><span data-stu-id="53c3e-117">Retrieves the error description for the session disconnect events.</span></span>

## <a name="syntax"></a><span data-ttu-id="53c3e-118">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="53c3e-118">Syntax</span></span>


```C++
HRESULT GetErrorDescription(
  [in]  UINT disconnectReason,
  [in]  UINT extendedDisconnectReason,
  [out] BSTR *pBstrErrorMsg
);
```



## <a name="parameters"></a><span data-ttu-id="53c3e-119">Параметры</span><span class="sxs-lookup"><span data-stu-id="53c3e-119">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53c3e-120">*дисконнектреасон* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="53c3e-120">*disconnectReason* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53c3e-121">Причина отключения.</span><span class="sxs-lookup"><span data-stu-id="53c3e-121">The disconnect reason.</span></span>

</dd> <dt>

<span data-ttu-id="53c3e-122">*екстендеддисконнектреасон* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="53c3e-122">*extendedDisconnectReason* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53c3e-123">Содержит подробные сведения о том, почему было инициировано отключение.</span><span class="sxs-lookup"><span data-stu-id="53c3e-123">Provides detailed information about why a disconnect was initiated.</span></span>

</dd> <dt>

<span data-ttu-id="53c3e-124">*пбстреррормсг* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="53c3e-124">*pBstrErrorMsg* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="53c3e-125">Указатель на переменную **BSTR** , которая получает текст сообщения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="53c3e-125">A pointer to a **BSTR** variable that receives the error message text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53c3e-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="53c3e-126">Return value</span></span>

<span data-ttu-id="53c3e-127">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="53c3e-127">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="53c3e-128">Требования</span><span class="sxs-lookup"><span data-stu-id="53c3e-128">Requirements</span></span>



| <span data-ttu-id="53c3e-129">Требование</span><span class="sxs-lookup"><span data-stu-id="53c3e-129">Requirement</span></span> | <span data-ttu-id="53c3e-130">Значение</span><span class="sxs-lookup"><span data-stu-id="53c3e-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="53c3e-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="53c3e-131">Minimum supported client</span></span><br/> | <span data-ttu-id="53c3e-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="53c3e-132">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="53c3e-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="53c3e-133">Minimum supported server</span></span><br/> | <span data-ttu-id="53c3e-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="53c3e-134">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="53c3e-135">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="53c3e-135">Type library</span></span><br/>             | <dl> <span data-ttu-id="53c3e-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="53c3e-136"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="53c3e-137">DLL</span><span class="sxs-lookup"><span data-stu-id="53c3e-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="53c3e-138"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="53c3e-138"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="53c3e-139">IID</span><span class="sxs-lookup"><span data-stu-id="53c3e-139">IID</span></span><br/>                      | <span data-ttu-id="53c3e-140">IID \_ IMsRdpClient5 определен как 4eb5335b-6429-477d-B922-e06a28ecd8bf</span><span class="sxs-lookup"><span data-stu-id="53c3e-140">IID\_IMsRdpClient5 is defined as 4eb5335b-6429-477d-b922-e06a28ecd8bf</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="53c3e-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="53c3e-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53c3e-142">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="53c3e-142">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="53c3e-143">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="53c3e-143">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="53c3e-144">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="53c3e-144">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="53c3e-145">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="53c3e-145">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="53c3e-146">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="53c3e-146">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="53c3e-147">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="53c3e-147">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





