---
description: Метод Get \_ участник получает указатель на массив интерфейсов итпартиЦипант, представляющих участников, вовлеченных в событие.
ms.assetid: 3c650715-b1c3-4f84-976a-2cb0f7f19f52
title: 'Метод ИтпартиЦипантевент:: get_Participant (Конфприв. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc5e9ee84bac69bd77237f1a50b9a008b2830258
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675715"
---
# <a name="itparticipanteventget_participant-method"></a><span data-ttu-id="7f175-103">Метод ИтпартиЦипантевент:: Get \_ участника</span><span class="sxs-lookup"><span data-stu-id="7f175-103">ITParticipantEvent::get\_Participant method</span></span>

<span data-ttu-id="7f175-104">\[**получить \_ Участник** недоступен для использования в Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="7f175-104">\[**get\_Participant** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="7f175-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="7f175-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="7f175-106">Метод **Get \_ участник** получает указатель на массив интерфейсов [**итпартиЦипант**](itparticipant.md) , представляющих участников, вовлеченных в событие.</span><span class="sxs-lookup"><span data-stu-id="7f175-106">The **get\_Participant** method gets a pointer to an array of [**ITParticipant**](itparticipant.md) interfaces representing the participants involved in the event.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f175-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7f175-107">Syntax</span></span>


```C++
HRESULT get_Participant(
  [out] ITParticipant **ppParticipant
);
```



## <a name="parameters"></a><span data-ttu-id="7f175-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="7f175-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f175-109">*пппартиЦипант* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="7f175-109">*ppParticipant* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7f175-110">Указатель на массив интерфейсов [**итпартиЦипант**](itparticipant.md) .</span><span class="sxs-lookup"><span data-stu-id="7f175-110">Pointer to array of [**ITParticipant**](itparticipant.md) interfaces.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f175-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7f175-111">Return value</span></span>

<span data-ttu-id="7f175-112">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="7f175-112">This method can return one of these values.</span></span>



| <span data-ttu-id="7f175-113">Значение</span><span class="sxs-lookup"><span data-stu-id="7f175-113">Value</span></span>                                                                                           | <span data-ttu-id="7f175-114">Значение</span><span class="sxs-lookup"><span data-stu-id="7f175-114">Meaning</span></span>                                                          |
|-------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <span data-ttu-id="7f175-115"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="7f175-115"><dt>**S\_OK**</dt></span></span> </dl>            | <span data-ttu-id="7f175-116">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="7f175-116">Method succeeded.</span></span><br/>                                     |
| <dl> <span data-ttu-id="7f175-117"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="7f175-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>   | <span data-ttu-id="7f175-118">Недостаточно памяти для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="7f175-118">Insufficient memory exists to perform the operation.</span></span><br/>  |
| <dl> <span data-ttu-id="7f175-119"><dt>**\_нежелательные \_ элементы TAPI**</dt></span><span class="sxs-lookup"><span data-stu-id="7f175-119"><dt>**TAPI\_E\_NOITEMS**</dt></span></span> </dl> | <span data-ttu-id="7f175-120">Нет участников, связанных с событием.</span><span class="sxs-lookup"><span data-stu-id="7f175-120">There are no participants associated with the event.</span></span><br/>  |
| <dl> <span data-ttu-id="7f175-121"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="7f175-121"><dt>**E\_POINTER**</dt></span></span> </dl>       | <span data-ttu-id="7f175-122">Параметр *пппартиЦипант* не является допустимым указателем.</span><span class="sxs-lookup"><span data-stu-id="7f175-122">The *ppParticipant* parameter is not a valid pointer.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="7f175-123">Требования</span><span class="sxs-lookup"><span data-stu-id="7f175-123">Requirements</span></span>



| <span data-ttu-id="7f175-124">Требование</span><span class="sxs-lookup"><span data-stu-id="7f175-124">Requirement</span></span> | <span data-ttu-id="7f175-125">Значение</span><span class="sxs-lookup"><span data-stu-id="7f175-125">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7f175-126">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="7f175-126">TAPI version</span></span><br/> | <span data-ttu-id="7f175-127">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="7f175-127">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="7f175-128">Header</span><span class="sxs-lookup"><span data-stu-id="7f175-128">Header</span></span><br/>       | <dl> <span data-ttu-id="7f175-129"><dt>Конфприв. h</dt></span><span class="sxs-lookup"><span data-stu-id="7f175-129"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="7f175-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="7f175-130">Library</span></span><br/>      | <dl> <span data-ttu-id="7f175-131"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7f175-131"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="7f175-132">DLL</span><span class="sxs-lookup"><span data-stu-id="7f175-132">DLL</span></span><br/>          | <dl> <span data-ttu-id="7f175-133"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7f175-133"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="7f175-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7f175-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f175-135">**итпартиЦипантевент**</span><span class="sxs-lookup"><span data-stu-id="7f175-135">**ITParticipantEvent**</span></span>](itparticipantevent.md)
</dt> <dt>

[<span data-ttu-id="7f175-136">**итпартиЦипант**</span><span class="sxs-lookup"><span data-stu-id="7f175-136">**ITParticipant**</span></span>](itparticipant.md)
</dt> </dl>

 

 




