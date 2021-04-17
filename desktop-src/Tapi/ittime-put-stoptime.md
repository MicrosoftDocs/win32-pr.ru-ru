---
description: Метод размещения \_ StopTime задает значение времени окончания NTP (сетевой протокол времени). Если время окончания равно нулю, сеанс не ограничен.
ms.assetid: 6f07054c-5fb2-4ee4-9025-3acf9b51ddbd
title: 'Иттиме: метод ut_StopTime:p (Сдпблб. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53446ea1d7ee93589987c42b005d7a84e7e728ae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675279"
---
# <a name="ittimeput_stoptime-method"></a><span data-ttu-id="2b71d-104">Иттиме::p UT \_ StopTime метод</span><span class="sxs-lookup"><span data-stu-id="2b71d-104">ITTime::put\_StopTime method</span></span>

<span data-ttu-id="2b71d-105">\[ В Windows Vista, Windows Server 2008 и последующих версиях операционной системы нельзя использовать встречные средства и элементы управления Конференц-телефонией и интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="2b71d-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="2b71d-106">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="2b71d-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="2b71d-107">Метод **размещения \_ StopTime** задает значение времени окончания NTP (сетевой протокол времени).</span><span class="sxs-lookup"><span data-stu-id="2b71d-107">The **put\_StopTime** method sets the NTP (Network Time Protocol) ending time value.</span></span> <span data-ttu-id="2b71d-108">Если время окончания равно нулю, сеанс не ограничен.</span><span class="sxs-lookup"><span data-stu-id="2b71d-108">If the end time is zero, the session is not bounded.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b71d-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2b71d-109">Syntax</span></span>


```C++
HRESULT put_StopTime(
  [in] DOUBLE Time
);
```



## <a name="parameters"></a><span data-ttu-id="2b71d-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="2b71d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b71d-111">*Время* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2b71d-111">*Time* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b71d-112">Время окончания сеанса.</span><span class="sxs-lookup"><span data-stu-id="2b71d-112">Stop time for the session.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b71d-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2b71d-113">Return value</span></span>

<span data-ttu-id="2b71d-114">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="2b71d-114">This method can return one of these values.</span></span>



| <span data-ttu-id="2b71d-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="2b71d-115">Return code</span></span>                                                                                   | <span data-ttu-id="2b71d-116">Описание</span><span class="sxs-lookup"><span data-stu-id="2b71d-116">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="2b71d-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="2b71d-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="2b71d-118">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="2b71d-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="2b71d-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="2b71d-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="2b71d-120">Недопустимый параметр *времени* .</span><span class="sxs-lookup"><span data-stu-id="2b71d-120">The *Time* parameter is not valid.</span></span><br/>                   |
| <dl> <span data-ttu-id="2b71d-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="2b71d-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="2b71d-122">Недостаточно памяти для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="2b71d-122">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="2b71d-123"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="2b71d-123"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="2b71d-124">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="2b71d-124">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="2b71d-125"><dt>**E \_ нотимпл**</dt></span><span class="sxs-lookup"><span data-stu-id="2b71d-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="2b71d-126">Этот метод еще не реализован.</span><span class="sxs-lookup"><span data-stu-id="2b71d-126">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="2b71d-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2b71d-127">Remarks</span></span>

<span data-ttu-id="2b71d-128">Эта функция может передавать данные по сети в незашифрованном виде; Таким образом, кто-то, кто прослушивает сеть, может прочитать данные.</span><span class="sxs-lookup"><span data-stu-id="2b71d-128">This function may send data over the wire in unencrypted form; therefore, someone eavesdropping on the network may be able to read the data.</span></span> <span data-ttu-id="2b71d-129">Прежде чем использовать этот метод, следует учесть угрозу безопасности при отправке данных в виде открытого текста.</span><span class="sxs-lookup"><span data-stu-id="2b71d-129">The security risk of sending the data in clear text should be considered before using this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b71d-130">Требования</span><span class="sxs-lookup"><span data-stu-id="2b71d-130">Requirements</span></span>



| <span data-ttu-id="2b71d-131">Требование</span><span class="sxs-lookup"><span data-stu-id="2b71d-131">Requirement</span></span> | <span data-ttu-id="2b71d-132">Значение</span><span class="sxs-lookup"><span data-stu-id="2b71d-132">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2b71d-133">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="2b71d-133">TAPI version</span></span><br/> | <span data-ttu-id="2b71d-134">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="2b71d-134">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="2b71d-135">Header</span><span class="sxs-lookup"><span data-stu-id="2b71d-135">Header</span></span><br/>       | <dl> <span data-ttu-id="2b71d-136"><dt>Сдпблб. h</dt></span><span class="sxs-lookup"><span data-stu-id="2b71d-136"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="2b71d-137">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2b71d-137">Library</span></span><br/>      | <dl> <span data-ttu-id="2b71d-138"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2b71d-138"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="2b71d-139">DLL</span><span class="sxs-lookup"><span data-stu-id="2b71d-139">DLL</span></span><br/>          | <dl> <span data-ttu-id="2b71d-140"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2b71d-140"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b71d-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2b71d-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b71d-142">**иттиме**</span><span class="sxs-lookup"><span data-stu-id="2b71d-142">**ITTime**</span></span>](ittime.md)
</dt> <dt>

[<span data-ttu-id="2b71d-143">**Иттиме:: Get \_ StopTime**</span><span class="sxs-lookup"><span data-stu-id="2b71d-143">**ITTime::get\_StopTime**</span></span>](ittime-get-stoptime.md)
</dt> </dl>

 

 




