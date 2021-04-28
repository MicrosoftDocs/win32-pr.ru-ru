---
description: 'Метод Иенуммедиа:: Skip — метод Skip пропускает следующее заданное число элементов в последовательности перечисления.'
ms.assetid: 825972c9-5303-4c5a-9475-dc67c185af91
title: 'Метод Иенуммедиа:: Skip (Сдпблб. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d8c600a201d6800fcb04dba5f208fd5cb810078
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084192"
---
# <a name="ienummediaskip-method"></a><span data-ttu-id="1c416-103">Метод Иенуммедиа:: Skip</span><span class="sxs-lookup"><span data-stu-id="1c416-103">IEnumMedia::Skip method</span></span>

<span data-ttu-id="1c416-104">\[ В Windows Vista, Windows Server 2008 и последующих версиях операционной системы нельзя использовать встречные средства и элементы управления Конференц-телефонией и интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="1c416-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="1c416-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="1c416-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="1c416-106">Метод **Skip** пропускает следующее заданное число элементов в последовательности перечисления.</span><span class="sxs-lookup"><span data-stu-id="1c416-106">The **Skip** method skips over the next specified number of elements in the enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c416-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1c416-107">Syntax</span></span>


```C++
HRESULT Skip(
  [in] ULONG celt
);
```



## <a name="parameters"></a><span data-ttu-id="1c416-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="1c416-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c416-109">*celt* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1c416-109">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c416-110">Число пропускаемых элементов.</span><span class="sxs-lookup"><span data-stu-id="1c416-110">Number of elements to skip.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c416-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1c416-111">Return value</span></span>

<span data-ttu-id="1c416-112">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="1c416-112">This method can return one of these values.</span></span>



| <span data-ttu-id="1c416-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="1c416-113">Return code</span></span>                                                                             | <span data-ttu-id="1c416-114">Описание</span><span class="sxs-lookup"><span data-stu-id="1c416-114">Description</span></span>                                           |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <span data-ttu-id="1c416-115"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="1c416-115"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="1c416-116">Число пропущенных элементов: *celt*.</span><span class="sxs-lookup"><span data-stu-id="1c416-116">Number of elements skipped was *celt*.</span></span><br/>     |
| <dl> <span data-ttu-id="1c416-117"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="1c416-117"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="1c416-118">Число пропущенных элементов не является *celt*.</span><span class="sxs-lookup"><span data-stu-id="1c416-118">Number of elements skipped was not *celt*.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="1c416-119">Требования</span><span class="sxs-lookup"><span data-stu-id="1c416-119">Requirements</span></span>



| <span data-ttu-id="1c416-120">Требование</span><span class="sxs-lookup"><span data-stu-id="1c416-120">Requirement</span></span> | <span data-ttu-id="1c416-121">Значение</span><span class="sxs-lookup"><span data-stu-id="1c416-121">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1c416-122">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="1c416-122">TAPI version</span></span><br/> | <span data-ttu-id="1c416-123">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="1c416-123">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="1c416-124">Header</span><span class="sxs-lookup"><span data-stu-id="1c416-124">Header</span></span><br/>       | <dl> <span data-ttu-id="1c416-125"><dt>Сдпблб. h</dt></span><span class="sxs-lookup"><span data-stu-id="1c416-125"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="1c416-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="1c416-126">Library</span></span><br/>      | <dl> <span data-ttu-id="1c416-127"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1c416-127"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="1c416-128">DLL</span><span class="sxs-lookup"><span data-stu-id="1c416-128">DLL</span></span><br/>          | <dl> <span data-ttu-id="1c416-129"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1c416-129"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c416-130">См. также</span><span class="sxs-lookup"><span data-stu-id="1c416-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c416-131">**иенуммедиа**</span><span class="sxs-lookup"><span data-stu-id="1c416-131">**IEnumMedia**</span></span>](ienummedia.md)
</dt> </dl>

 

 




