---
title: IMsRdpClient9 attachEvent, метод
description: Присоединяет событие.
ms.assetid: 3a887aeb-a74f-4477-8cf3-8ac43a31fa26
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода attachEvent
- службы удаленных рабочих столов метода attachEvent, интерфейс IMsRdpClient9
- Службы удаленных рабочих столов интерфейса IMsRdpClient9, метод attachEvent
- службы удаленных рабочих столов метода attachEvent, интерфейс IMsRdpClient10
- Службы удаленных рабочих столов интерфейса IMsRdpClient10, метод attachEvent
topic_type:
- apiref
api_name:
- IMsRdpClient9.attachEvent
- IMsRdpClient10.attachEvent
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1bd3fd518fba825c209a4170e6b314a7b774a49
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489135"
---
# <a name="imsrdpclient9attachevent-method"></a><span data-ttu-id="c061b-108">Метод IMsRdpClient9:: attachEvent</span><span class="sxs-lookup"><span data-stu-id="c061b-108">IMsRdpClient9::attachEvent method</span></span>

<span data-ttu-id="c061b-109">Присоединяет событие.</span><span class="sxs-lookup"><span data-stu-id="c061b-109">Attaches an event.</span></span>

## <a name="syntax"></a><span data-ttu-id="c061b-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c061b-110">Syntax</span></span>


```C++
HRESULT attachEvent(
  [in] BSTR      eventName,
  [in] IDispatch *callback
);
```



## <a name="parameters"></a><span data-ttu-id="c061b-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="c061b-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c061b-112">*EventName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c061b-112">*eventName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c061b-113">Событие для присоединения.</span><span class="sxs-lookup"><span data-stu-id="c061b-113">The event to attach.</span></span>

</dd> <dt>

<span data-ttu-id="c061b-114">*обратный вызов* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c061b-114">*callback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c061b-115">Обратный вызов.</span><span class="sxs-lookup"><span data-stu-id="c061b-115">The callback.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c061b-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c061b-116">Return value</span></span>

<span data-ttu-id="c061b-117">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="c061b-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c061b-118">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c061b-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="c061b-119">Требования</span><span class="sxs-lookup"><span data-stu-id="c061b-119">Requirements</span></span>



| <span data-ttu-id="c061b-120">Требование</span><span class="sxs-lookup"><span data-stu-id="c061b-120">Requirement</span></span> | <span data-ttu-id="c061b-121">Значение</span><span class="sxs-lookup"><span data-stu-id="c061b-121">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c061b-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c061b-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c061b-123">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="c061b-123">Windows 8.1</span></span><br/>                                                                                                                                                                                                                                                  |
| <span data-ttu-id="c061b-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c061b-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c061b-125">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="c061b-125">Windows Server 2012 R2</span></span><br/>                                                                                                                                                                                                                                       |
| <span data-ttu-id="c061b-126">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="c061b-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="c061b-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c061b-127"><dt>MsTscAx.dll</dt></span></span> </dl>                                                                                                                                                                                  |
| <span data-ttu-id="c061b-128">DLL</span><span class="sxs-lookup"><span data-stu-id="c061b-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c061b-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c061b-129"><dt>MsTscAx.dll</dt></span></span> </dl>                                                                                                                                                                                  |
| <span data-ttu-id="c061b-130">IID</span><span class="sxs-lookup"><span data-stu-id="c061b-130">IID</span></span><br/>                      | <span data-ttu-id="c061b-131">\_MSRDPCLIENT9 CLSID определен как 301B94BA-5D25-4A12-BFFE-3B6E7A616585</span><span class="sxs-lookup"><span data-stu-id="c061b-131">CLSID\_MsRdpClient9 is defined as 301B94BA-5D25-4A12-BFFE-3B6E7A616585</span></span><br/> <span data-ttu-id="c061b-132">\_MSRDPCLIENT9NOTSAFEFORSCRIPTING CLSID определен как 8B918B82-7985-4C24-89DF-C33AD2BBFBCD</span><span class="sxs-lookup"><span data-stu-id="c061b-132">CLSID\_MsRdpClient9NotSafeForScripting is defined as 8B918B82-7985-4C24-89DF-C33AD2BBFBCD</span></span><br/> <span data-ttu-id="c061b-133">IID \_ IMsRdpClient9 определен как 28904001-04B6-436C-A55B-0AF1A0883DC9</span><span class="sxs-lookup"><span data-stu-id="c061b-133">IID\_IMsRdpClient9 is defined as 28904001-04B6-436C-A55B-0AF1A0883DC9</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c061b-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c061b-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c061b-135">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="c061b-135">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> <dt>

[<span data-ttu-id="c061b-136">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="c061b-136">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> </dl>

 

 





