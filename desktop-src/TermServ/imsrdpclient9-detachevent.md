---
title: IMsRdpClient9 Детачевент, метод
description: Отсоединяет событие.
ms.assetid: 6a3ca713-1d5c-4070-a527-ad4f532a4cbf
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Детачевент
- службы удаленных рабочих столов метода Детачевент, интерфейс IMsRdpClient9
- Службы удаленных рабочих столов интерфейса IMsRdpClient9, метод Детачевент
- службы удаленных рабочих столов метода Детачевент, интерфейс IMsRdpClient10
- Службы удаленных рабочих столов интерфейса IMsRdpClient10, метод Детачевент
topic_type:
- apiref
api_name:
- IMsRdpClient9.detachEvent
- IMsRdpClient10.detachEvent
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 399611ea526338f4cfe40ef3a4d6543bf27f134a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135174"
---
# <a name="imsrdpclient9detachevent-method"></a><span data-ttu-id="3a65e-108">IMsRdpClient9: метод:d Етачевент</span><span class="sxs-lookup"><span data-stu-id="3a65e-108">IMsRdpClient9::detachEvent method</span></span>

<span data-ttu-id="3a65e-109">Отсоединяет событие.</span><span class="sxs-lookup"><span data-stu-id="3a65e-109">Detaches an event.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a65e-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3a65e-110">Syntax</span></span>


```C++
HRESULT detachEvent(
  [in] BSTR      eventName,
  [in] IDispatch *callback
);
```



## <a name="parameters"></a><span data-ttu-id="3a65e-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="3a65e-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a65e-112">*EventName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3a65e-112">*eventName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a65e-113">Имя события.</span><span class="sxs-lookup"><span data-stu-id="3a65e-113">Name of the event.</span></span>

</dd> <dt>

<span data-ttu-id="3a65e-114">*обратный вызов* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3a65e-114">*callback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a65e-115">Обратный вызов, связанный с событием.</span><span class="sxs-lookup"><span data-stu-id="3a65e-115">The callback associated with the event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a65e-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3a65e-116">Return value</span></span>

<span data-ttu-id="3a65e-117">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="3a65e-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3a65e-118">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3a65e-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a65e-119">Требования</span><span class="sxs-lookup"><span data-stu-id="3a65e-119">Requirements</span></span>



| <span data-ttu-id="3a65e-120">Требование</span><span class="sxs-lookup"><span data-stu-id="3a65e-120">Requirement</span></span> | <span data-ttu-id="3a65e-121">Значение</span><span class="sxs-lookup"><span data-stu-id="3a65e-121">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a65e-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3a65e-122">Minimum supported client</span></span><br/> | <span data-ttu-id="3a65e-123">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="3a65e-123">Windows 8.1</span></span><br/>                                                                                                                                                                                                                                                  |
| <span data-ttu-id="3a65e-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3a65e-124">Minimum supported server</span></span><br/> | <span data-ttu-id="3a65e-125">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="3a65e-125">Windows Server 2012 R2</span></span><br/>                                                                                                                                                                                                                                       |
| <span data-ttu-id="3a65e-126">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="3a65e-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="3a65e-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3a65e-127"><dt>MsTscAx.dll</dt></span></span> </dl>                                                                                                                                                                                  |
| <span data-ttu-id="3a65e-128">DLL</span><span class="sxs-lookup"><span data-stu-id="3a65e-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3a65e-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3a65e-129"><dt>MsTscAx.dll</dt></span></span> </dl>                                                                                                                                                                                  |
| <span data-ttu-id="3a65e-130">IID</span><span class="sxs-lookup"><span data-stu-id="3a65e-130">IID</span></span><br/>                      | <span data-ttu-id="3a65e-131">\_MSRDPCLIENT9 CLSID определен как 301B94BA-5D25-4A12-BFFE-3B6E7A616585</span><span class="sxs-lookup"><span data-stu-id="3a65e-131">CLSID\_MsRdpClient9 is defined as 301B94BA-5D25-4A12-BFFE-3B6E7A616585</span></span><br/> <span data-ttu-id="3a65e-132">\_MSRDPCLIENT9NOTSAFEFORSCRIPTING CLSID определен как 8B918B82-7985-4C24-89DF-C33AD2BBFBCD</span><span class="sxs-lookup"><span data-stu-id="3a65e-132">CLSID\_MsRdpClient9NotSafeForScripting is defined as 8B918B82-7985-4C24-89DF-C33AD2BBFBCD</span></span><br/> <span data-ttu-id="3a65e-133">IID \_ IMsRdpClient9 определен как 28904001-04B6-436C-A55B-0AF1A0883DC9</span><span class="sxs-lookup"><span data-stu-id="3a65e-133">IID\_IMsRdpClient9 is defined as 28904001-04B6-436C-A55B-0AF1A0883DC9</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3a65e-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3a65e-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a65e-135">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="3a65e-135">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> <dt>

[<span data-ttu-id="3a65e-136">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="3a65e-136">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> </dl>

 

 





