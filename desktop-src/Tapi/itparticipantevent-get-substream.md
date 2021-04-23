---
description: Подпоток Get \_ получает указатель на массив интерфейсов итсубстреам, представляющих подпотоки, участвующие в событии.
ms.assetid: 0af9097a-2481-4543-bb3d-35ccd352e992
title: 'Метод ИтпартиЦипантевент:: get_SubStream (Конфприв. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b8c2944004af31adfb7256376992506eef59b40
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105688912"
---
# <a name="itparticipanteventget_substream-method"></a><span data-ttu-id="65ab3-103">Метод ИтпартиЦипантевент:: Get для \_ подпотока</span><span class="sxs-lookup"><span data-stu-id="65ab3-103">ITParticipantEvent::get\_SubStream method</span></span>

<span data-ttu-id="65ab3-104">\[**получить \_ Подпоток** недоступен для использования в Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="65ab3-104">\[**get\_SubStream** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="65ab3-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="65ab3-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="65ab3-106">**Подпоток \_ Get** получает указатель на массив интерфейсов [**итсубстреам**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream) , представляющих подпотоки, участвующие в событии.</span><span class="sxs-lookup"><span data-stu-id="65ab3-106">The **get\_SubStream** gets a pointer to an array of [**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream) interfaces representing the substreams involved in the event.</span></span>

## <a name="syntax"></a><span data-ttu-id="65ab3-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="65ab3-107">Syntax</span></span>


```C++
HRESULT get_SubStream(
  [out] ITSubStream **ppSubStream
);
```



## <a name="parameters"></a><span data-ttu-id="65ab3-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="65ab3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65ab3-109">*ппсубстреам* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="65ab3-109">*ppSubStream* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="65ab3-110">Указатель на массив указателей [**итсубстреам**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream) .</span><span class="sxs-lookup"><span data-stu-id="65ab3-110">Pointer to array of [**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream) pointers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65ab3-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="65ab3-111">Return value</span></span>

<span data-ttu-id="65ab3-112">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="65ab3-112">This method can return one of these values.</span></span>



| <span data-ttu-id="65ab3-113">Значение</span><span class="sxs-lookup"><span data-stu-id="65ab3-113">Value</span></span>                                                                                           | <span data-ttu-id="65ab3-114">Значение</span><span class="sxs-lookup"><span data-stu-id="65ab3-114">Meaning</span></span>                                                         |
|-------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="65ab3-115"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="65ab3-115"><dt>**S\_OK**</dt></span></span> </dl>            | <span data-ttu-id="65ab3-116">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="65ab3-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="65ab3-117"><dt>**\_нежелательные \_ элементы TAPI**</dt></span><span class="sxs-lookup"><span data-stu-id="65ab3-117"><dt>**TAPI\_E\_NOITEMS**</dt></span></span> </dl> | <span data-ttu-id="65ab3-118">Нет ни одного подпотока, связанного с событием.</span><span class="sxs-lookup"><span data-stu-id="65ab3-118">There are no substreams associated with the event.</span></span><br/>   |
| <dl> <span data-ttu-id="65ab3-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="65ab3-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>   | <span data-ttu-id="65ab3-120">Недостаточно памяти для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="65ab3-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="65ab3-121"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="65ab3-121"><dt>**E\_POINTER**</dt></span></span> </dl>       | <span data-ttu-id="65ab3-122">Параметр *ппсубстреам* не является допустимым указателем.</span><span class="sxs-lookup"><span data-stu-id="65ab3-122">The *ppSubStream* parameter is not a valid pointer.</span></span><br/>  |



 

## <a name="requirements"></a><span data-ttu-id="65ab3-123">Требования</span><span class="sxs-lookup"><span data-stu-id="65ab3-123">Requirements</span></span>



| <span data-ttu-id="65ab3-124">Требование</span><span class="sxs-lookup"><span data-stu-id="65ab3-124">Requirement</span></span> | <span data-ttu-id="65ab3-125">Значение</span><span class="sxs-lookup"><span data-stu-id="65ab3-125">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="65ab3-126">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="65ab3-126">TAPI version</span></span><br/> | <span data-ttu-id="65ab3-127">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="65ab3-127">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="65ab3-128">Header</span><span class="sxs-lookup"><span data-stu-id="65ab3-128">Header</span></span><br/>       | <dl> <span data-ttu-id="65ab3-129"><dt>Конфприв. h</dt></span><span class="sxs-lookup"><span data-stu-id="65ab3-129"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="65ab3-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="65ab3-130">Library</span></span><br/>      | <dl> <span data-ttu-id="65ab3-131"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="65ab3-131"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="65ab3-132">DLL</span><span class="sxs-lookup"><span data-stu-id="65ab3-132">DLL</span></span><br/>          | <dl> <span data-ttu-id="65ab3-133"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="65ab3-133"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="65ab3-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="65ab3-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65ab3-135">**итпартиЦипантевент**</span><span class="sxs-lookup"><span data-stu-id="65ab3-135">**ITParticipantEvent**</span></span>](itparticipantevent.md)
</dt> <dt>

[<span data-ttu-id="65ab3-136">**итсубстреам**</span><span class="sxs-lookup"><span data-stu-id="65ab3-136">**ITSubStream**</span></span>](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream)
</dt> </dl>

 

