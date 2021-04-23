---
description: Метод Get \_ нумаддрессес возвращает количество адресов, используемых для сеанса.
ms.assetid: c3aef5df-02e9-4c7e-99aa-8e4043798bf4
title: 'Метод Итконнектион:: get_NumAddresses (Сдпблб. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24b121275c6af8f026e7321e4fd85327e970eb78
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675228"
---
# <a name="itconnectionget_numaddresses-method"></a><span data-ttu-id="18d7b-103">Метод Итконнектион:: Get \_ нумаддрессес</span><span class="sxs-lookup"><span data-stu-id="18d7b-103">ITConnection::get\_NumAddresses method</span></span>

<span data-ttu-id="18d7b-104">\[ В Windows Vista, Windows Server 2008 и последующих версиях операционной системы нельзя использовать встречные средства и элементы управления Конференц-телефонией и интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="18d7b-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="18d7b-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="18d7b-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="18d7b-106">Метод **Get \_ нумаддрессес** возвращает количество адресов, используемых для сеанса.</span><span class="sxs-lookup"><span data-stu-id="18d7b-106">The **get\_NumAddresses** method gets the number of addresses to be used for the session.</span></span>

## <a name="syntax"></a><span data-ttu-id="18d7b-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="18d7b-107">Syntax</span></span>


```C++
HRESULT get_NumAddresses(
  [out] LONG *pNumAddresses
);
```



## <a name="parameters"></a><span data-ttu-id="18d7b-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="18d7b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18d7b-109">*пнумаддрессес* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="18d7b-109">*pNumAddresses* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="18d7b-110">Число адресов для сеанса.</span><span class="sxs-lookup"><span data-stu-id="18d7b-110">Number of addresses for the session.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="18d7b-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="18d7b-111">Return value</span></span>

<span data-ttu-id="18d7b-112">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="18d7b-112">This method can return one of these values.</span></span>



| <span data-ttu-id="18d7b-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="18d7b-113">Return code</span></span>                                                                                   | <span data-ttu-id="18d7b-114">Описание</span><span class="sxs-lookup"><span data-stu-id="18d7b-114">Description</span></span>                                                      |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <span data-ttu-id="18d7b-115"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="18d7b-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="18d7b-116">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="18d7b-116">Method succeeded.</span></span><br/>                                     |
| <dl> <span data-ttu-id="18d7b-117"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="18d7b-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="18d7b-118">Параметр *пнумаддрессе* s не является допустимым указателем.</span><span class="sxs-lookup"><span data-stu-id="18d7b-118">The *pNumAddresse* s parameter is not a valid pointer.</span></span><br/> |
| <dl> <span data-ttu-id="18d7b-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="18d7b-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="18d7b-120">Недостаточно памяти для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="18d7b-120">Insufficient memory exists to perform the operation.</span></span><br/>  |
| <dl> <span data-ttu-id="18d7b-121"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="18d7b-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="18d7b-122">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="18d7b-122">Unspecified error.</span></span><br/>                                    |
| <dl> <span data-ttu-id="18d7b-123"><dt>**E \_ нотимпл**</dt></span><span class="sxs-lookup"><span data-stu-id="18d7b-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="18d7b-124">Этот метод еще не реализован.</span><span class="sxs-lookup"><span data-stu-id="18d7b-124">This method is not yet implemented.</span></span><br/>                   |



 

## <a name="requirements"></a><span data-ttu-id="18d7b-125">Требования</span><span class="sxs-lookup"><span data-stu-id="18d7b-125">Requirements</span></span>



| <span data-ttu-id="18d7b-126">Требование</span><span class="sxs-lookup"><span data-stu-id="18d7b-126">Requirement</span></span> | <span data-ttu-id="18d7b-127">Значение</span><span class="sxs-lookup"><span data-stu-id="18d7b-127">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="18d7b-128">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="18d7b-128">TAPI version</span></span><br/> | <span data-ttu-id="18d7b-129">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="18d7b-129">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="18d7b-130">Header</span><span class="sxs-lookup"><span data-stu-id="18d7b-130">Header</span></span><br/>       | <dl> <span data-ttu-id="18d7b-131"><dt>Сдпблб. h</dt></span><span class="sxs-lookup"><span data-stu-id="18d7b-131"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="18d7b-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="18d7b-132">Library</span></span><br/>      | <dl> <span data-ttu-id="18d7b-133"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="18d7b-133"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="18d7b-134">DLL</span><span class="sxs-lookup"><span data-stu-id="18d7b-134">DLL</span></span><br/>          | <dl> <span data-ttu-id="18d7b-135"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="18d7b-135"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18d7b-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="18d7b-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18d7b-137">**итконнектион**</span><span class="sxs-lookup"><span data-stu-id="18d7b-137">**ITConnection**</span></span>](itconnection.md)
</dt> </dl>

 

 




