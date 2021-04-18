---
description: Метод Get \_ StopTime получает значение времени окончания NTP (сетевой протокол времени). Если время окончания равно нулю, сеанс не ограничен.
ms.assetid: f18042c0-e41d-43b3-a75d-6ab161afde6e
title: 'Метод Иттиме:: get_StopTime (Сдпблб. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b55ac03c4701884b5a4b7716cb2758887b6160bc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685360"
---
# <a name="ittimeget_stoptime-method"></a><span data-ttu-id="c67b0-104">Метод Иттиме:: Get \_ StopTime</span><span class="sxs-lookup"><span data-stu-id="c67b0-104">ITTime::get\_StopTime method</span></span>

<span data-ttu-id="c67b0-105">\[ В Windows Vista, Windows Server 2008 и последующих версиях операционной системы нельзя использовать встречные средства и элементы управления Конференц-телефонией и интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="c67b0-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="c67b0-106">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="c67b0-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="c67b0-107">Метод **Get \_ StopTime** получает значение времени окончания NTP (сетевой протокол времени).</span><span class="sxs-lookup"><span data-stu-id="c67b0-107">The **get\_StopTime** method gets the NTP (Network Time Protocol) ending time value.</span></span> <span data-ttu-id="c67b0-108">Если время окончания равно нулю, сеанс не ограничен.</span><span class="sxs-lookup"><span data-stu-id="c67b0-108">If the end time is zero, the session is not bounded.</span></span>

## <a name="syntax"></a><span data-ttu-id="c67b0-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c67b0-109">Syntax</span></span>


```C++
HRESULT get_StopTime(
  [out] DOUBLE *pTime
);
```



## <a name="parameters"></a><span data-ttu-id="c67b0-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="c67b0-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c67b0-111">*птиме* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="c67b0-111">*pTime* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c67b0-112">Указатель на время окончания сеанса.</span><span class="sxs-lookup"><span data-stu-id="c67b0-112">Pointer to the stop time for the session.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c67b0-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c67b0-113">Return value</span></span>

<span data-ttu-id="c67b0-114">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="c67b0-114">This method can return one of these values.</span></span>



| <span data-ttu-id="c67b0-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="c67b0-115">Return code</span></span>                                                                                   | <span data-ttu-id="c67b0-116">Описание</span><span class="sxs-lookup"><span data-stu-id="c67b0-116">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="c67b0-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="c67b0-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="c67b0-118">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="c67b0-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="c67b0-119"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="c67b0-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="c67b0-120">Параметр *птиме* не является допустимым указателем.</span><span class="sxs-lookup"><span data-stu-id="c67b0-120">The *pTime* parameter is not a valid pointer.</span></span><br/>        |
| <dl> <span data-ttu-id="c67b0-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="c67b0-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="c67b0-122">Недостаточно памяти для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="c67b0-122">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="c67b0-123"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="c67b0-123"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="c67b0-124">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="c67b0-124">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="c67b0-125"><dt>**E \_ нотимпл**</dt></span><span class="sxs-lookup"><span data-stu-id="c67b0-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="c67b0-126">Этот метод еще не реализован.</span><span class="sxs-lookup"><span data-stu-id="c67b0-126">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="c67b0-127">Требования</span><span class="sxs-lookup"><span data-stu-id="c67b0-127">Requirements</span></span>



| <span data-ttu-id="c67b0-128">Требование</span><span class="sxs-lookup"><span data-stu-id="c67b0-128">Requirement</span></span> | <span data-ttu-id="c67b0-129">Значение</span><span class="sxs-lookup"><span data-stu-id="c67b0-129">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c67b0-130">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="c67b0-130">TAPI version</span></span><br/> | <span data-ttu-id="c67b0-131">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="c67b0-131">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="c67b0-132">Header</span><span class="sxs-lookup"><span data-stu-id="c67b0-132">Header</span></span><br/>       | <dl> <span data-ttu-id="c67b0-133"><dt>Сдпблб. h</dt></span><span class="sxs-lookup"><span data-stu-id="c67b0-133"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="c67b0-134">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c67b0-134">Library</span></span><br/>      | <dl> <span data-ttu-id="c67b0-135"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c67b0-135"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="c67b0-136">DLL</span><span class="sxs-lookup"><span data-stu-id="c67b0-136">DLL</span></span><br/>          | <dl> <span data-ttu-id="c67b0-137"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c67b0-137"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c67b0-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c67b0-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c67b0-139">**иттиме**</span><span class="sxs-lookup"><span data-stu-id="c67b0-139">**ITTime**</span></span>](ittime.md)
</dt> <dt>

[<span data-ttu-id="c67b0-140">**Иттиме::p UT \_ StopTime**</span><span class="sxs-lookup"><span data-stu-id="c67b0-140">**ITTime::put\_StopTime**</span></span>](ittime-put-stoptime.md)
</dt> </dl>

 

 




