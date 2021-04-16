---
description: Метод Get \_ субстреамфромпартиЦипант позволяет приложению определить, какие подпотоки связаны с данным участником.
ms.assetid: d45cdd1d-13cf-433a-9b19-193d5c0cba11
title: 'Метод ИтпартиЦипантсубстреамконтрол:: get_SubStreamFromParticipant (Конфприв. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0eae68cd62c38348e1a576f114a9e93ac52f9cc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680059"
---
# <a name="itparticipantsubstreamcontrolget_substreamfromparticipant-method"></a><span data-ttu-id="72235-103">Метод ИтпартиЦипантсубстреамконтрол:: Get \_ субстреамфромпартиЦипант</span><span class="sxs-lookup"><span data-stu-id="72235-103">ITParticipantSubStreamControl::get\_SubStreamFromParticipant method</span></span>

<span data-ttu-id="72235-104">\[**получить \_ СубстреамфромпартиЦипант** недоступен для использования в Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="72235-104">\[**get\_SubStreamFromParticipant** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="72235-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="72235-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="72235-106">Метод **Get \_ субстреамфромпартиЦипант** позволяет приложению определить, какие подпотоки связаны с данным участником.</span><span class="sxs-lookup"><span data-stu-id="72235-106">The **get\_SubStreamFromParticipant** method allows an application to discover which substreams are associated with a given participant.</span></span>

## <a name="syntax"></a><span data-ttu-id="72235-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="72235-107">Syntax</span></span>


```C++
HRESULT get_SubStreamFromParticipant(
  [in]  ITParticipant *pParticipant,
  [out] ITSubStream   **ppITSubStream
);
```



## <a name="parameters"></a><span data-ttu-id="72235-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="72235-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="72235-109">*ппартиЦипант* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="72235-109">*pParticipant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72235-110">Указатель на интерфейс [**итпартиЦипант**](itparticipant.md) .</span><span class="sxs-lookup"><span data-stu-id="72235-110">Pointer to [**ITParticipant**](itparticipant.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="72235-111">*ппитсубстреам* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="72235-111">*ppITSubStream* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="72235-112">Указатель на массив указателей интерфейса [**итпартиЦипант**](itparticipant.md) .</span><span class="sxs-lookup"><span data-stu-id="72235-112">Pointer to array of [**ITParticipant**](itparticipant.md) interface pointers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="72235-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="72235-113">Return value</span></span>

<span data-ttu-id="72235-114">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="72235-114">This method can return one of these values.</span></span>



| <span data-ttu-id="72235-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="72235-115">Return code</span></span>                                                                                   | <span data-ttu-id="72235-116">Описание</span><span class="sxs-lookup"><span data-stu-id="72235-116">Description</span></span>                                                                  |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="72235-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="72235-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="72235-118">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="72235-118">Method succeeded.</span></span><br/>                                                 |
| <dl> <span data-ttu-id="72235-119"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="72235-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="72235-120">Параметр *ппитсубстреам* не является допустимым указателем.</span><span class="sxs-lookup"><span data-stu-id="72235-120">The *ppITSubStream* parameter is not a valid pointer.</span></span><br/>             |
| <dl> <span data-ttu-id="72235-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="72235-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="72235-122">Параметр *ппартиЦипант* не указывает на допустимый интерфейс.</span><span class="sxs-lookup"><span data-stu-id="72235-122">The *pParticipant* parameter does not point to a valid interface.</span></span><br/> |
| <dl> <span data-ttu-id="72235-123"><dt>**\_непредвиденная E**</dt></span><span class="sxs-lookup"><span data-stu-id="72235-123"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>  | <span data-ttu-id="72235-124">Не удалось получить доступ к сведениям о участнике потока.</span><span class="sxs-lookup"><span data-stu-id="72235-124">The stream's participant information could not be accessed.</span></span><br/>       |
| <dl> <span data-ttu-id="72235-125"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="72235-125"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="72235-126">Недостаточно памяти для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="72235-126">Insufficient memory exists to perform the operation.</span></span><br/>              |



 

## <a name="requirements"></a><span data-ttu-id="72235-127">Требования</span><span class="sxs-lookup"><span data-stu-id="72235-127">Requirements</span></span>



| <span data-ttu-id="72235-128">Требование</span><span class="sxs-lookup"><span data-stu-id="72235-128">Requirement</span></span> | <span data-ttu-id="72235-129">Значение</span><span class="sxs-lookup"><span data-stu-id="72235-129">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="72235-130">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="72235-130">TAPI version</span></span><br/> | <span data-ttu-id="72235-131">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="72235-131">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="72235-132">Header</span><span class="sxs-lookup"><span data-stu-id="72235-132">Header</span></span><br/>       | <dl> <span data-ttu-id="72235-133"><dt>Конфприв. h</dt></span><span class="sxs-lookup"><span data-stu-id="72235-133"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="72235-134">Библиотека</span><span class="sxs-lookup"><span data-stu-id="72235-134">Library</span></span><br/>      | <dl> <span data-ttu-id="72235-135"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="72235-135"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="72235-136">DLL</span><span class="sxs-lookup"><span data-stu-id="72235-136">DLL</span></span><br/>          | <dl> <span data-ttu-id="72235-137"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="72235-137"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="72235-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="72235-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72235-139">**итпартиЦипантсубстреамконтрол**</span><span class="sxs-lookup"><span data-stu-id="72235-139">**ITParticipantSubStreamControl**</span></span>](itparticipantsubstreamcontrol.md)
</dt> <dt>

[<span data-ttu-id="72235-140">**итпартиЦипант**</span><span class="sxs-lookup"><span data-stu-id="72235-140">**ITParticipant**</span></span>](itparticipant.md)
</dt> <dt>

[<span data-ttu-id="72235-141">**итсубстреам**</span><span class="sxs-lookup"><span data-stu-id="72235-141">**ITSubStream**</span></span>](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream)
</dt> </dl>

 

