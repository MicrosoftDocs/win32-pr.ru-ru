---
description: Метод Get \_ пропускной способности возвращает значение пропускной способности.
ms.assetid: d9020443-d061-4a60-9d54-191144def110
title: 'Метод Итконнектион:: get_Bandwidth (Сдпблб. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 563ff4d5902a3434839167ffd28fad2b7552e5c2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689475"
---
# <a name="itconnectionget_bandwidth-method"></a><span data-ttu-id="fbe25-103">Итконнектион:: получение \_ метода пропускной способности</span><span class="sxs-lookup"><span data-stu-id="fbe25-103">ITConnection::get\_Bandwidth method</span></span>

<span data-ttu-id="fbe25-104">\[ В Windows Vista, Windows Server 2008 и последующих версиях операционной системы нельзя использовать встречные средства и элементы управления Конференц-телефонией и интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="fbe25-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="fbe25-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="fbe25-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="fbe25-106">Метод **Get \_ пропускной способности** возвращает значение пропускной способности.</span><span class="sxs-lookup"><span data-stu-id="fbe25-106">The **get\_Bandwidth** method gets the bandwidth value.</span></span>

## <a name="syntax"></a><span data-ttu-id="fbe25-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fbe25-107">Syntax</span></span>


```C++
HRESULT get_Bandwidth(
  [out] DOUBLE *pBandwidth
);
```



## <a name="parameters"></a><span data-ttu-id="fbe25-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="fbe25-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fbe25-109">*пбандвидс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="fbe25-109">*pBandwidth* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fbe25-110">Значение пропускной способности.</span><span class="sxs-lookup"><span data-stu-id="fbe25-110">Bandwidth value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fbe25-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fbe25-111">Return value</span></span>

<span data-ttu-id="fbe25-112">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="fbe25-112">This method can return one of these values.</span></span>



| <span data-ttu-id="fbe25-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="fbe25-113">Return code</span></span>                                                                                   | <span data-ttu-id="fbe25-114">Описание</span><span class="sxs-lookup"><span data-stu-id="fbe25-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="fbe25-115"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="fbe25-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="fbe25-116">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="fbe25-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="fbe25-117"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="fbe25-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="fbe25-118">Параметр *пбандвидс* не является допустимым указателем.</span><span class="sxs-lookup"><span data-stu-id="fbe25-118">The *pBandwidth* parameter is not a valid pointer.</span></span><br/>   |
| <dl> <span data-ttu-id="fbe25-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="fbe25-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="fbe25-120">Недостаточно памяти для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="fbe25-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="fbe25-121"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="fbe25-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="fbe25-122">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="fbe25-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="fbe25-123"><dt>**E \_ нотимпл**</dt></span><span class="sxs-lookup"><span data-stu-id="fbe25-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="fbe25-124">Этот метод еще не реализован.</span><span class="sxs-lookup"><span data-stu-id="fbe25-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="fbe25-125">Требования</span><span class="sxs-lookup"><span data-stu-id="fbe25-125">Requirements</span></span>



| <span data-ttu-id="fbe25-126">Требование</span><span class="sxs-lookup"><span data-stu-id="fbe25-126">Requirement</span></span> | <span data-ttu-id="fbe25-127">Значение</span><span class="sxs-lookup"><span data-stu-id="fbe25-127">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fbe25-128">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="fbe25-128">TAPI version</span></span><br/> | <span data-ttu-id="fbe25-129">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="fbe25-129">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="fbe25-130">Header</span><span class="sxs-lookup"><span data-stu-id="fbe25-130">Header</span></span><br/>       | <dl> <span data-ttu-id="fbe25-131"><dt>Сдпблб. h</dt></span><span class="sxs-lookup"><span data-stu-id="fbe25-131"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="fbe25-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="fbe25-132">Library</span></span><br/>      | <dl> <span data-ttu-id="fbe25-133"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fbe25-133"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="fbe25-134">DLL</span><span class="sxs-lookup"><span data-stu-id="fbe25-134">DLL</span></span><br/>          | <dl> <span data-ttu-id="fbe25-135"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fbe25-135"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fbe25-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fbe25-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbe25-137">**итконнектион**</span><span class="sxs-lookup"><span data-stu-id="fbe25-137">**ITConnection**</span></span>](itconnection.md)
</dt> </dl>

 

 




