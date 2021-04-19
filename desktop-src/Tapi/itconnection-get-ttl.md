---
description: Метод Get \_ TTL получает область срока жизни (TTL) для передачи данных по адресам.
ms.assetid: ea3c22d8-476e-4b4b-98c6-f1075e704f3d
title: 'Метод Итконнектион:: get_Ttl (Сдпблб. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88f4810eeefc19647e6ed5601b3a6b88870f1e9c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675226"
---
# <a name="itconnectionget_ttl-method"></a><span data-ttu-id="789b2-103">Метод Итконнектион:: Get \_ TTL</span><span class="sxs-lookup"><span data-stu-id="789b2-103">ITConnection::get\_Ttl method</span></span>

<span data-ttu-id="789b2-104">\[ В Windows Vista, Windows Server 2008 и последующих версиях операционной системы нельзя использовать встречные средства и элементы управления Конференц-телефонией и интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="789b2-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="789b2-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="789b2-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="789b2-106">Метод **Get \_ TTL** получает [*область срока жизни (TTL*](t-tapgloss.md) ) для передачи данных по адресам.</span><span class="sxs-lookup"><span data-stu-id="789b2-106">The **get\_Ttl** method gets the [*time to live*](t-tapgloss.md) (TTL) scope for transmissions on the addresses.</span></span>

## <a name="syntax"></a><span data-ttu-id="789b2-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="789b2-107">Syntax</span></span>


```C++
HRESULT get_Ttl(
  [out] unsigned char *pTtl
);
```



## <a name="parameters"></a><span data-ttu-id="789b2-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="789b2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="789b2-109">*пттл* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="789b2-109">*pTtl* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="789b2-110">Область TTL.</span><span class="sxs-lookup"><span data-stu-id="789b2-110">TTL scope.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="789b2-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="789b2-111">Return value</span></span>

<span data-ttu-id="789b2-112">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="789b2-112">This method can return one of these values.</span></span>



| <span data-ttu-id="789b2-113">Значение</span><span class="sxs-lookup"><span data-stu-id="789b2-113">Value</span></span>                                                                                         | <span data-ttu-id="789b2-114">Значение</span><span class="sxs-lookup"><span data-stu-id="789b2-114">Meaning</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="789b2-115"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="789b2-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="789b2-116">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="789b2-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="789b2-117"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="789b2-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="789b2-118">Параметр *пттл* не является допустимым указателем.</span><span class="sxs-lookup"><span data-stu-id="789b2-118">The *pTtl* parameter is not a valid pointer.</span></span><br/>         |
| <dl> <span data-ttu-id="789b2-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="789b2-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="789b2-120">Недостаточно памяти для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="789b2-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="789b2-121"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="789b2-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="789b2-122">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="789b2-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="789b2-123"><dt>**E \_ нотимпл**</dt></span><span class="sxs-lookup"><span data-stu-id="789b2-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="789b2-124">Этот метод еще не реализован.</span><span class="sxs-lookup"><span data-stu-id="789b2-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="789b2-125">Требования</span><span class="sxs-lookup"><span data-stu-id="789b2-125">Requirements</span></span>



| <span data-ttu-id="789b2-126">Требование</span><span class="sxs-lookup"><span data-stu-id="789b2-126">Requirement</span></span> | <span data-ttu-id="789b2-127">Значение</span><span class="sxs-lookup"><span data-stu-id="789b2-127">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="789b2-128">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="789b2-128">TAPI version</span></span><br/> | <span data-ttu-id="789b2-129">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="789b2-129">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="789b2-130">Header</span><span class="sxs-lookup"><span data-stu-id="789b2-130">Header</span></span><br/>       | <dl> <span data-ttu-id="789b2-131"><dt>Сдпблб. h</dt></span><span class="sxs-lookup"><span data-stu-id="789b2-131"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="789b2-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="789b2-132">Library</span></span><br/>      | <dl> <span data-ttu-id="789b2-133"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="789b2-133"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="789b2-134">DLL</span><span class="sxs-lookup"><span data-stu-id="789b2-134">DLL</span></span><br/>          | <dl> <span data-ttu-id="789b2-135"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="789b2-135"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="789b2-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="789b2-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="789b2-137">**итконнектион**</span><span class="sxs-lookup"><span data-stu-id="789b2-137">**ITConnection**</span></span>](itconnection.md)
</dt> </dl>

 

 




