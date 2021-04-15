---
description: Метод Skip пропускает следующее заданное число элементов в последовательности перечисления.
ms.assetid: e4d9c95d-1b68-4af6-beb2-2014074e5089
title: 'Метод Иенумтиме:: Skip (Сдпблб. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebd157afc51f52a8453c38f8a14702476c46eb9d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689124"
---
# <a name="ienumtimeskip-method"></a><span data-ttu-id="9ab75-103">Метод Иенумтиме:: Skip</span><span class="sxs-lookup"><span data-stu-id="9ab75-103">IEnumTime::Skip method</span></span>

<span data-ttu-id="9ab75-104">\[ В Windows Vista, Windows Server 2008 и последующих версиях операционной системы нельзя использовать встречные средства и элементы управления Конференц-телефонией и интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="9ab75-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="9ab75-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="9ab75-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="9ab75-106">Метод **Skip** пропускает следующее заданное число элементов в последовательности перечисления.</span><span class="sxs-lookup"><span data-stu-id="9ab75-106">The **Skip** method skips over the next specified number of elements in the enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ab75-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9ab75-107">Syntax</span></span>


```C++
HRESULT Skip(
  [in] ULONG celt
);
```



## <a name="parameters"></a><span data-ttu-id="9ab75-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="9ab75-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ab75-109">*celt* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9ab75-109">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ab75-110">Число пропускаемых элементов.</span><span class="sxs-lookup"><span data-stu-id="9ab75-110">Number of elements to skip.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ab75-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9ab75-111">Return value</span></span>

<span data-ttu-id="9ab75-112">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="9ab75-112">This method can return one of these values.</span></span>



| <span data-ttu-id="9ab75-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="9ab75-113">Return code</span></span>                                                                             | <span data-ttu-id="9ab75-114">Описание</span><span class="sxs-lookup"><span data-stu-id="9ab75-114">Description</span></span>                                           |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <span data-ttu-id="9ab75-115"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="9ab75-115"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="9ab75-116">Число пропущенных элементов: *celt*.</span><span class="sxs-lookup"><span data-stu-id="9ab75-116">Number of elements skipped was *celt*.</span></span><br/>     |
| <dl> <span data-ttu-id="9ab75-117"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="9ab75-117"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="9ab75-118">Число пропущенных элементов не является *celt*.</span><span class="sxs-lookup"><span data-stu-id="9ab75-118">Number of elements skipped was not *celt*.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="9ab75-119">Требования</span><span class="sxs-lookup"><span data-stu-id="9ab75-119">Requirements</span></span>



| <span data-ttu-id="9ab75-120">Требование</span><span class="sxs-lookup"><span data-stu-id="9ab75-120">Requirement</span></span> | <span data-ttu-id="9ab75-121">Значение</span><span class="sxs-lookup"><span data-stu-id="9ab75-121">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9ab75-122">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="9ab75-122">TAPI version</span></span><br/> | <span data-ttu-id="9ab75-123">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="9ab75-123">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="9ab75-124">Header</span><span class="sxs-lookup"><span data-stu-id="9ab75-124">Header</span></span><br/>       | <dl> <span data-ttu-id="9ab75-125"><dt>Сдпблб. h</dt></span><span class="sxs-lookup"><span data-stu-id="9ab75-125"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="9ab75-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="9ab75-126">Library</span></span><br/>      | <dl> <span data-ttu-id="9ab75-127"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9ab75-127"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="9ab75-128">DLL</span><span class="sxs-lookup"><span data-stu-id="9ab75-128">DLL</span></span><br/>          | <dl> <span data-ttu-id="9ab75-129"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9ab75-129"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ab75-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9ab75-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ab75-131">**иенумтиме**</span><span class="sxs-lookup"><span data-stu-id="9ab75-131">**IEnumTime**</span></span>](ienumtime.md)
</dt> </dl>

 

 




