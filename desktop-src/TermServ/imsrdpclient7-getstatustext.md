---
title: Метод IMsRdpClient7 Жетстатустекст (OpenService. h)
description: Получает текст состояния для указанного кода состояния.
ms.assetid: 1da2280a-c26d-4caa-b227-c289055f3aa9
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Жетстатустекст
- Службы удаленных рабочих столов метода Жетстатустекст, интерфейс IMsRdpClient7
- Службы удаленных рабочих столов интерфейса IMsRdpClient7, метод Жетстатустекст
- Службы удаленных рабочих столов метода Жетстатустекст, интерфейс IMsRdpClient8
- Службы удаленных рабочих столов интерфейса IMsRdpClient8, метод Жетстатустекст
- Службы удаленных рабочих столов метода Жетстатустекст, интерфейс IMsRdpClient9
- Службы удаленных рабочих столов интерфейса IMsRdpClient9, метод Жетстатустекст
- Службы удаленных рабочих столов метода Жетстатустекст, интерфейс IMsRdpClient10
- Службы удаленных рабочих столов интерфейса IMsRdpClient10, метод Жетстатустекст
topic_type:
- apiref
api_name:
- IMsRdpClient7.GetStatusText
- IMsRdpClient8.GetStatusText
- IMsRdpClient9.GetStatusText
- IMsRdpClient10.GetStatusText
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 820628bfba59ec980e5128b9d9df3ee21b49a064
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802758"
---
# <a name="imsrdpclient7getstatustext-method"></a><span data-ttu-id="04176-112">Метод IMsRdpClient7:: Жетстатустекст</span><span class="sxs-lookup"><span data-stu-id="04176-112">IMsRdpClient7::GetStatusText method</span></span>

<span data-ttu-id="04176-113">Получает текст состояния для указанного кода состояния.</span><span class="sxs-lookup"><span data-stu-id="04176-113">Retrieves the status text for the specified status code.</span></span>

## <a name="syntax"></a><span data-ttu-id="04176-114">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="04176-114">Syntax</span></span>


```C++
HRESULT GetStatusText(
  [in]          UINT statusCode,
  [out, retval] BSTR *pBstrStatusText
);
```



## <a name="parameters"></a><span data-ttu-id="04176-115">Параметры</span><span class="sxs-lookup"><span data-stu-id="04176-115">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04176-116">*StatusCode* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="04176-116">*statusCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04176-117">Значение **uint** , указывающее код состояния, для которого извлекается текст.</span><span class="sxs-lookup"><span data-stu-id="04176-117">A **UINT** that specifies the status code to retrieve the text for.</span></span>

</dd> <dt>

<span data-ttu-id="04176-118">*пбстрстатустекст* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="04176-118">*pBstrStatusText* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="04176-119">Адрес объекта **BSTR** , который получает текст состояния.</span><span class="sxs-lookup"><span data-stu-id="04176-119">The address of a **BSTR** that receives the status text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04176-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="04176-120">Return value</span></span>

<span data-ttu-id="04176-121">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="04176-121">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="04176-122">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="04176-122">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="04176-123">Требования</span><span class="sxs-lookup"><span data-stu-id="04176-123">Requirements</span></span>



| <span data-ttu-id="04176-124">Требование</span><span class="sxs-lookup"><span data-stu-id="04176-124">Requirement</span></span> | <span data-ttu-id="04176-125">Значение</span><span class="sxs-lookup"><span data-stu-id="04176-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="04176-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="04176-126">Minimum supported client</span></span><br/> | <span data-ttu-id="04176-127">Windows 7</span><span class="sxs-lookup"><span data-stu-id="04176-127">Windows 7</span></span><br/>                                                                     |
| <span data-ttu-id="04176-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="04176-128">Minimum supported server</span></span><br/> | <span data-ttu-id="04176-129">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="04176-129">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="04176-130">Header</span><span class="sxs-lookup"><span data-stu-id="04176-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="04176-131"><dt>OpenService. h</dt></span><span class="sxs-lookup"><span data-stu-id="04176-131"><dt>Openservice.h</dt></span></span> </dl> |
| <span data-ttu-id="04176-132">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="04176-132">Type library</span></span><br/>             | <dl> <span data-ttu-id="04176-133"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="04176-133"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="04176-134">DLL</span><span class="sxs-lookup"><span data-stu-id="04176-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="04176-135"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="04176-135"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="04176-136">IID</span><span class="sxs-lookup"><span data-stu-id="04176-136">IID</span></span><br/>                      | <span data-ttu-id="04176-137">IID \_ IMsRdpClient7 определен как b2a5b5ce-3461-444a-91d4-add26d070638</span><span class="sxs-lookup"><span data-stu-id="04176-137">IID\_IMsRdpClient7 is defined as b2a5b5ce-3461-444a-91d4-add26d070638</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="04176-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="04176-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04176-139">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="04176-139">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="04176-140">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="04176-140">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="04176-141">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="04176-141">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="04176-142">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="04176-142">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





