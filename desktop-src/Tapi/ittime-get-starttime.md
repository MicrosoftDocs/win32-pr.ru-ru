---
description: Метод Get \_ StartTime получает значение времени начала 32-разрядного NTP (сетевой протокол времени). Сеанс считается активным с этого момента.
ms.assetid: 511e4486-4c73-4610-8e64-9c70acc98eab
title: 'Метод Иттиме:: get_StartTime (Сдпблб. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 051096c6cbdab1960c67ddb2cbcaf57eccab9556
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685361"
---
# <a name="ittimeget_starttime-method"></a><span data-ttu-id="4bdce-104">Метод Иттиме:: Get \_ StartTime</span><span class="sxs-lookup"><span data-stu-id="4bdce-104">ITTime::get\_StartTime method</span></span>

<span data-ttu-id="4bdce-105">\[ В Windows Vista, Windows Server 2008 и последующих версиях операционной системы нельзя использовать встречные средства и элементы управления Конференц-телефонией и интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="4bdce-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="4bdce-106">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="4bdce-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="4bdce-107">Метод **Get \_ StartTime** получает значение времени начала 32-разрядного NTP (сетевой протокол времени).</span><span class="sxs-lookup"><span data-stu-id="4bdce-107">The **get\_StartTime** method gets the 32-bit NTP (Network Time Protocol) starting time value.</span></span> <span data-ttu-id="4bdce-108">Сеанс считается активным с этого момента.</span><span class="sxs-lookup"><span data-stu-id="4bdce-108">The session is considered active from this time.</span></span>

## <a name="syntax"></a><span data-ttu-id="4bdce-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4bdce-109">Syntax</span></span>


```C++
HRESULT get_StartTime(
  [out] DOUBLE *pTime
);
```



## <a name="parameters"></a><span data-ttu-id="4bdce-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="4bdce-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4bdce-111">*птиме* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="4bdce-111">*pTime* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4bdce-112">Указатель на время начала сеанса.</span><span class="sxs-lookup"><span data-stu-id="4bdce-112">Pointer to the start time for the session.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4bdce-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4bdce-113">Return value</span></span>

<span data-ttu-id="4bdce-114">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="4bdce-114">This method can return one of these values.</span></span>



| <span data-ttu-id="4bdce-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="4bdce-115">Return code</span></span>                                                                                   | <span data-ttu-id="4bdce-116">Описание</span><span class="sxs-lookup"><span data-stu-id="4bdce-116">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="4bdce-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="4bdce-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="4bdce-118">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="4bdce-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="4bdce-119"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="4bdce-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="4bdce-120">Параметр *птиме* не является допустимым указателем.</span><span class="sxs-lookup"><span data-stu-id="4bdce-120">The *pTime* parameter is not a valid pointer.</span></span><br/>        |
| <dl> <span data-ttu-id="4bdce-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="4bdce-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="4bdce-122">Недостаточно памяти для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="4bdce-122">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="4bdce-123"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="4bdce-123"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="4bdce-124">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="4bdce-124">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="4bdce-125"><dt>**E \_ нотимпл**</dt></span><span class="sxs-lookup"><span data-stu-id="4bdce-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="4bdce-126">Этот метод еще не реализован.</span><span class="sxs-lookup"><span data-stu-id="4bdce-126">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="4bdce-127">Требования</span><span class="sxs-lookup"><span data-stu-id="4bdce-127">Requirements</span></span>



| <span data-ttu-id="4bdce-128">Требование</span><span class="sxs-lookup"><span data-stu-id="4bdce-128">Requirement</span></span> | <span data-ttu-id="4bdce-129">Значение</span><span class="sxs-lookup"><span data-stu-id="4bdce-129">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4bdce-130">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="4bdce-130">TAPI version</span></span><br/> | <span data-ttu-id="4bdce-131">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="4bdce-131">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="4bdce-132">Header</span><span class="sxs-lookup"><span data-stu-id="4bdce-132">Header</span></span><br/>       | <dl> <span data-ttu-id="4bdce-133"><dt>Сдпблб. h</dt></span><span class="sxs-lookup"><span data-stu-id="4bdce-133"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="4bdce-134">Библиотека</span><span class="sxs-lookup"><span data-stu-id="4bdce-134">Library</span></span><br/>      | <dl> <span data-ttu-id="4bdce-135"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4bdce-135"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="4bdce-136">DLL</span><span class="sxs-lookup"><span data-stu-id="4bdce-136">DLL</span></span><br/>          | <dl> <span data-ttu-id="4bdce-137"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4bdce-137"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4bdce-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4bdce-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4bdce-139">**иттиме**</span><span class="sxs-lookup"><span data-stu-id="4bdce-139">**ITTime**</span></span>](ittime.md)
</dt> <dt>

[<span data-ttu-id="4bdce-140">**Иттиме::p UT \_ StartTime**</span><span class="sxs-lookup"><span data-stu-id="4bdce-140">**ITTime::put\_StartTime**</span></span>](ittime-put-starttime.md)
</dt> </dl>

 

 




