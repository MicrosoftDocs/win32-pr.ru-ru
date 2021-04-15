---
description: '\_Метод события Get получает \_ дескриптор события участника типа произошедшего события.'
ms.assetid: 6b5e6358-2ba6-48b5-8d55-bc896fbb9962
title: 'Метод ИтпартиЦипантевент:: get_Event (Конфприв. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b6cbfcf709b1f9f3f49047504bf5d9e8c02b159
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689252"
---
# <a name="itparticipanteventget_event-method"></a><span data-ttu-id="f3b99-103">Метод события ИтпартиЦипантевент:: Get \_</span><span class="sxs-lookup"><span data-stu-id="f3b99-103">ITParticipantEvent::get\_Event method</span></span>

<span data-ttu-id="f3b99-104">\[**получить \_ Событие** недоступно для использования в Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="f3b99-104">\[**get\_Event** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="f3b99-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="f3b99-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="f3b99-106">Метод **\_ события Get** получает дескриптор [**\_ события участника**](participant-event.md) типа произошедшего события.</span><span class="sxs-lookup"><span data-stu-id="f3b99-106">The **get\_Event** method gets a [**PARTICIPANT\_EVENT**](participant-event.md) descriptor of the type of event that has occurred.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3b99-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f3b99-107">Syntax</span></span>


```C++
HRESULT get_Event(
  [out] PARTICIPANT_EVENT *pParticipantEvent
);
```



## <a name="parameters"></a><span data-ttu-id="f3b99-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="f3b99-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3b99-109">*ппартиЦипантевент* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="f3b99-109">*pParticipantEvent* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f3b99-110">Указатель на дескриптор [**события \_ участника**](participant-event.md) события.</span><span class="sxs-lookup"><span data-stu-id="f3b99-110">Pointer to a [**PARTICIPANT\_EVENT**](participant-event.md) descriptor of the event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3b99-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f3b99-111">Return value</span></span>

<span data-ttu-id="f3b99-112">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="f3b99-112">This method can return one of these values.</span></span>



| <span data-ttu-id="f3b99-113">Значение</span><span class="sxs-lookup"><span data-stu-id="f3b99-113">Value</span></span>                                                                                         | <span data-ttu-id="f3b99-114">Значение</span><span class="sxs-lookup"><span data-stu-id="f3b99-114">Meaning</span></span>                                                              |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <span data-ttu-id="f3b99-115"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="f3b99-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="f3b99-116">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="f3b99-116">Method succeeded.</span></span><br/>                                         |
| <dl> <span data-ttu-id="f3b99-117"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="f3b99-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="f3b99-118">Недостаточно памяти для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="f3b99-118">Insufficient memory exists to perform the operation.</span></span><br/>      |
| <dl> <span data-ttu-id="f3b99-119"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="f3b99-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="f3b99-120">Параметр *ппартиЦипантевент* не является допустимым указателем.</span><span class="sxs-lookup"><span data-stu-id="f3b99-120">The *pParticipantEvent* parameter is not a valid pointer.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="f3b99-121">Требования</span><span class="sxs-lookup"><span data-stu-id="f3b99-121">Requirements</span></span>



| <span data-ttu-id="f3b99-122">Требование</span><span class="sxs-lookup"><span data-stu-id="f3b99-122">Requirement</span></span> | <span data-ttu-id="f3b99-123">Значение</span><span class="sxs-lookup"><span data-stu-id="f3b99-123">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f3b99-124">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="f3b99-124">TAPI version</span></span><br/> | <span data-ttu-id="f3b99-125">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="f3b99-125">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="f3b99-126">Header</span><span class="sxs-lookup"><span data-stu-id="f3b99-126">Header</span></span><br/>       | <dl> <span data-ttu-id="f3b99-127"><dt>Конфприв. h</dt></span><span class="sxs-lookup"><span data-stu-id="f3b99-127"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="f3b99-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f3b99-128">Library</span></span><br/>      | <dl> <span data-ttu-id="f3b99-129"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f3b99-129"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="f3b99-130">DLL</span><span class="sxs-lookup"><span data-stu-id="f3b99-130">DLL</span></span><br/>          | <dl> <span data-ttu-id="f3b99-131"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f3b99-131"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="f3b99-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f3b99-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3b99-133">**итпартиЦипантевент**</span><span class="sxs-lookup"><span data-stu-id="f3b99-133">**ITParticipantEvent**</span></span>](itparticipantevent.md)
</dt> <dt>

[<span data-ttu-id="f3b99-134">**\_событие участника**</span><span class="sxs-lookup"><span data-stu-id="f3b99-134">**PARTICIPANT\_EVENT**</span></span>](participant-event.md)
</dt> </dl>

 

 




