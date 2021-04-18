---
description: Метод "вставить \_ StartTime" задает значение времени начала 32-разрядного NTP (сетевой протокол времени). Сеанс считается активным с этого момента.
ms.assetid: c7c96265-4588-4f05-83b6-6ef54f02650b
title: 'Иттиме: метод ut_StartTime:p (Сдпблб. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a5b574f7c90d7cc2f92204e3a045b33e6fb8480
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675280"
---
# <a name="ittimeput_starttime-method"></a><span data-ttu-id="35462-104">Иттиме: метод:p UT \_ StartTime</span><span class="sxs-lookup"><span data-stu-id="35462-104">ITTime::put\_StartTime method</span></span>

<span data-ttu-id="35462-105">\[ В Windows Vista, Windows Server 2008 и последующих версиях операционной системы нельзя использовать встречные средства и элементы управления Конференц-телефонией и интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="35462-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="35462-106">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="35462-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="35462-107">Метод " **Вставить \_ StartTime** " задает значение времени начала 32-разрядного NTP (сетевой протокол времени).</span><span class="sxs-lookup"><span data-stu-id="35462-107">The **put\_StartTime** method sets the 32-bit NTP (Network Time Protocol) starting time value.</span></span> <span data-ttu-id="35462-108">Сеанс считается активным с этого момента.</span><span class="sxs-lookup"><span data-stu-id="35462-108">The session is considered active from this time.</span></span>

## <a name="syntax"></a><span data-ttu-id="35462-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="35462-109">Syntax</span></span>


```C++
HRESULT put_StartTime(
  [in] DOUBLE Time
);
```



## <a name="parameters"></a><span data-ttu-id="35462-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="35462-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35462-111">*Время* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="35462-111">*Time* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35462-112">Время начала сеанса.</span><span class="sxs-lookup"><span data-stu-id="35462-112">Start time for the session.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35462-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="35462-113">Return value</span></span>

<span data-ttu-id="35462-114">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="35462-114">This method can return one of these values.</span></span>



| <span data-ttu-id="35462-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="35462-115">Return code</span></span>                                                                                   | <span data-ttu-id="35462-116">Описание</span><span class="sxs-lookup"><span data-stu-id="35462-116">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="35462-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="35462-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="35462-118">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="35462-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="35462-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="35462-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="35462-120">Недопустимый параметр *Тим* e.</span><span class="sxs-lookup"><span data-stu-id="35462-120">The *Tim* e parameter is not valid.</span></span><br/>                   |
| <dl> <span data-ttu-id="35462-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="35462-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="35462-122">Недостаточно памяти для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="35462-122">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="35462-123"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="35462-123"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="35462-124">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="35462-124">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="35462-125"><dt>**E \_ нотимпл**</dt></span><span class="sxs-lookup"><span data-stu-id="35462-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="35462-126">Этот метод еще не реализован.</span><span class="sxs-lookup"><span data-stu-id="35462-126">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="35462-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="35462-127">Remarks</span></span>

<span data-ttu-id="35462-128">Эта функция может передавать данные по сети в незашифрованном виде; Таким образом, кто-то, кто прослушивает сеть, может прочитать данные.</span><span class="sxs-lookup"><span data-stu-id="35462-128">This function may send data over the wire in unencrypted form; therefore, someone eavesdropping on the network may be able to read the data.</span></span> <span data-ttu-id="35462-129">Прежде чем использовать этот метод, следует учесть угрозу безопасности при отправке данных в виде открытого текста.</span><span class="sxs-lookup"><span data-stu-id="35462-129">The security risk of sending the data in clear text should be considered before using this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="35462-130">Требования</span><span class="sxs-lookup"><span data-stu-id="35462-130">Requirements</span></span>



| <span data-ttu-id="35462-131">Требование</span><span class="sxs-lookup"><span data-stu-id="35462-131">Requirement</span></span> | <span data-ttu-id="35462-132">Значение</span><span class="sxs-lookup"><span data-stu-id="35462-132">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="35462-133">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="35462-133">TAPI version</span></span><br/> | <span data-ttu-id="35462-134">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="35462-134">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="35462-135">Header</span><span class="sxs-lookup"><span data-stu-id="35462-135">Header</span></span><br/>       | <dl> <span data-ttu-id="35462-136"><dt>Сдпблб. h</dt></span><span class="sxs-lookup"><span data-stu-id="35462-136"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="35462-137">Библиотека</span><span class="sxs-lookup"><span data-stu-id="35462-137">Library</span></span><br/>      | <dl> <span data-ttu-id="35462-138"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="35462-138"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="35462-139">DLL</span><span class="sxs-lookup"><span data-stu-id="35462-139">DLL</span></span><br/>          | <dl> <span data-ttu-id="35462-140"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="35462-140"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35462-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="35462-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35462-142">**иттиме**</span><span class="sxs-lookup"><span data-stu-id="35462-142">**ITTime**</span></span>](ittime.md)
</dt> <dt>

[<span data-ttu-id="35462-143">**Иттиме:: Get \_ StartTime**</span><span class="sxs-lookup"><span data-stu-id="35462-143">**ITTime::get\_StartTime**</span></span>](ittime-get-starttime.md)
</dt> </dl>

 

 




