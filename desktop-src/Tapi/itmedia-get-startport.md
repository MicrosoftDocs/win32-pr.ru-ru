---
description: Метод Get \_ стартпорт получает 16-битное значение порта для первого порта.
ms.assetid: 203b51ea-8e0c-47d2-b267-36a0bf3bff72
title: 'Метод Итмедиа:: get_StartPort (Сдпблб. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99c5cf50f4a8beb0a1694bd1ceaf000620c69b69
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105674899"
---
# <a name="itmediaget_startport-method"></a><span data-ttu-id="beafd-103">Метод Итмедиа:: Get \_ стартпорт</span><span class="sxs-lookup"><span data-stu-id="beafd-103">ITMedia::get\_StartPort method</span></span>

<span data-ttu-id="beafd-104">\[ В Windows Vista, Windows Server 2008 и последующих версиях операционной системы нельзя использовать встречные средства и элементы управления Конференц-телефонией и интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="beafd-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="beafd-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="beafd-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="beafd-106">Метод **Get \_ стартпорт** получает 16-битное значение порта для первого порта.</span><span class="sxs-lookup"><span data-stu-id="beafd-106">The **get\_StartPort** method gets the 16-bit port value for the first port.</span></span>

## <a name="syntax"></a><span data-ttu-id="beafd-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="beafd-107">Syntax</span></span>


```C++
HRESULT get_StartPort(
  [out] LONG *pStartPort
);
```



## <a name="parameters"></a><span data-ttu-id="beafd-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="beafd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="beafd-109">*пстартпорт* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="beafd-109">*pStartPort* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="beafd-110">Значение первого порта.</span><span class="sxs-lookup"><span data-stu-id="beafd-110">Value of the first port.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="beafd-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="beafd-111">Return value</span></span>

<span data-ttu-id="beafd-112">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="beafd-112">This method can return one of these values.</span></span>



| <span data-ttu-id="beafd-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="beafd-113">Return code</span></span>                                                                                   | <span data-ttu-id="beafd-114">Описание</span><span class="sxs-lookup"><span data-stu-id="beafd-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="beafd-115"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="beafd-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="beafd-116">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="beafd-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="beafd-117"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="beafd-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="beafd-118">Параметр *пстартпорт* не является допустимым указателем.</span><span class="sxs-lookup"><span data-stu-id="beafd-118">The *pStartPort* parameter is not a valid pointer.</span></span><br/>   |
| <dl> <span data-ttu-id="beafd-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="beafd-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="beafd-120">Недостаточно памяти для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="beafd-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="beafd-121"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="beafd-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="beafd-122">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="beafd-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="beafd-123"><dt>**E \_ нотимпл**</dt></span><span class="sxs-lookup"><span data-stu-id="beafd-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="beafd-124">Этот метод еще не реализован.</span><span class="sxs-lookup"><span data-stu-id="beafd-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="beafd-125">Требования</span><span class="sxs-lookup"><span data-stu-id="beafd-125">Requirements</span></span>



| <span data-ttu-id="beafd-126">Требование</span><span class="sxs-lookup"><span data-stu-id="beafd-126">Requirement</span></span> | <span data-ttu-id="beafd-127">Значение</span><span class="sxs-lookup"><span data-stu-id="beafd-127">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="beafd-128">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="beafd-128">TAPI version</span></span><br/> | <span data-ttu-id="beafd-129">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="beafd-129">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="beafd-130">Header</span><span class="sxs-lookup"><span data-stu-id="beafd-130">Header</span></span><br/>       | <dl> <span data-ttu-id="beafd-131"><dt>Сдпблб. h</dt></span><span class="sxs-lookup"><span data-stu-id="beafd-131"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="beafd-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="beafd-132">Library</span></span><br/>      | <dl> <span data-ttu-id="beafd-133"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="beafd-133"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="beafd-134">DLL</span><span class="sxs-lookup"><span data-stu-id="beafd-134">DLL</span></span><br/>          | <dl> <span data-ttu-id="beafd-135"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="beafd-135"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="beafd-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="beafd-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="beafd-137">**итмедиа**</span><span class="sxs-lookup"><span data-stu-id="beafd-137">**ITMedia**</span></span>](itmedia.md)
</dt> </dl>

 

 




