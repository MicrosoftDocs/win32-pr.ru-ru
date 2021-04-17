---
description: Метод Get \_ медиаколлектион получает указатель на интерфейс итмедиаколлектион для Конференции.
ms.assetid: 8109582a-74f0-47e8-91d1-0d89c3d3c331
title: 'Метод Итсдп:: get_MediaCollection (Сдпблб. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f8812debf8c04fe022f24061660d6ea3bb5f162
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675221"
---
# <a name="itsdpget_mediacollection-method"></a><span data-ttu-id="94a18-103">Метод Итсдп:: Get \_ медиаколлектион</span><span class="sxs-lookup"><span data-stu-id="94a18-103">ITSdp::get\_MediaCollection method</span></span>

<span data-ttu-id="94a18-104">\[ В Windows Vista, Windows Server 2008 и последующих версиях операционной системы нельзя использовать встречные средства и элементы управления Конференц-телефонией и интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="94a18-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="94a18-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="94a18-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="94a18-106">Метод **Get \_ медиаколлектион** получает указатель на интерфейс [**итмедиаколлектион**](itmediacollection.md) для Конференции.</span><span class="sxs-lookup"><span data-stu-id="94a18-106">The **get\_MediaCollection** method gets a pointer to the [**ITMediaCollection**](itmediacollection.md) interface for the conference.</span></span>

## <a name="syntax"></a><span data-ttu-id="94a18-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="94a18-107">Syntax</span></span>


```C++
HRESULT get_MediaCollection(
  [out] ITMediaCollection **ppMediaCollection
);
```



## <a name="parameters"></a><span data-ttu-id="94a18-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="94a18-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94a18-109">*ппмедиаколлектион* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="94a18-109">*ppMediaCollection* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="94a18-110">Указатель на [**итмедиаколлектион**](itmediacollection.md).</span><span class="sxs-lookup"><span data-stu-id="94a18-110">Pointer to [**ITMediaCollection**](itmediacollection.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="94a18-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="94a18-111">Return value</span></span>

<span data-ttu-id="94a18-112">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="94a18-112">This method can return one of these values.</span></span>



| <span data-ttu-id="94a18-113">Значение</span><span class="sxs-lookup"><span data-stu-id="94a18-113">Value</span></span>                                                                                                                           | <span data-ttu-id="94a18-114">Значение</span><span class="sxs-lookup"><span data-stu-id="94a18-114">Meaning</span></span>                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="94a18-115"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="94a18-115"><dt>**S\_OK**</dt></span></span> </dl>                                            | <span data-ttu-id="94a18-116">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="94a18-116">Method succeeded.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="94a18-117"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="94a18-117"><dt>**E\_INVALIDARG**</dt></span></span> </dl>                                    | <span data-ttu-id="94a18-118">Параметр *ппмедиаколлектион* не является допустимым указателем.</span><span class="sxs-lookup"><span data-stu-id="94a18-118">The *ppMediaCollection* parameter is not a valid pointer.</span></span><br/>                        |
| <dl> <span data-ttu-id="94a18-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="94a18-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>                                   | <span data-ttu-id="94a18-120">Недостаточно памяти для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="94a18-120">Insufficient memory exists to perform the operation.</span></span><br/>                             |
| <dl> <span data-ttu-id="94a18-121"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="94a18-121"><dt>**E\_FAIL**</dt></span></span> </dl>                                          | <span data-ttu-id="94a18-122">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="94a18-122">Unspecified error.</span></span><br/>                                                               |
| <dl> <span data-ttu-id="94a18-123"><dt>**HRESULT \_ из \_ \_ кода ошибки (ошибка: \_ недопустимые \_ данные)**</dt></span><span class="sxs-lookup"><span data-stu-id="94a18-123"><dt>**HRESULT\_FROM\_ERROR\_CODE(ERROR\_INVALID\_DATA)**</dt></span></span> </dl> | <span data-ttu-id="94a18-124">Произошла внутренняя ошибка, обычно из-за сбоя предыдущего метода.</span><span class="sxs-lookup"><span data-stu-id="94a18-124">An internal error has occurred, usually due to the failure of a previous method.</span></span><br/> |
| <dl> <span data-ttu-id="94a18-125"><dt>**E \_ нотимпл**</dt></span><span class="sxs-lookup"><span data-stu-id="94a18-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>                                       | <span data-ttu-id="94a18-126">Этот метод еще не реализован.</span><span class="sxs-lookup"><span data-stu-id="94a18-126">This method is not yet implemented.</span></span><br/>                                              |



 

## <a name="remarks"></a><span data-ttu-id="94a18-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="94a18-127">Remarks</span></span>

<span data-ttu-id="94a18-128">[**Итмедиаколлектион**](itmediacollection.md) указатель можно также получить с помощью **QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="94a18-128">An [**ITMediaCollection**](itmediacollection.md) pointer could also be obtained using **QueryInterface**.</span></span>

<span data-ttu-id="94a18-129">TAPI вызывает метод **AddRef** в интерфейсе [**итмедиаколлектион**](itmediacollection.md) , возвращенном методом **итсдп:: Get \_ медиаколлектион**.</span><span class="sxs-lookup"><span data-stu-id="94a18-129">TAPI calls the **AddRef** method on the [**ITMediaCollection**](itmediacollection.md) interface returned by **ITSdp::get\_MediaCollection**.</span></span> <span data-ttu-id="94a18-130">Приложение должно вызвать **выпуск** в интерфейсе **итмедиаколлектион** , чтобы освободить ресурсы, связанные с ним.</span><span class="sxs-lookup"><span data-stu-id="94a18-130">The application must call **Release** on the **ITMediaCollection** interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="94a18-131">Требования</span><span class="sxs-lookup"><span data-stu-id="94a18-131">Requirements</span></span>



| <span data-ttu-id="94a18-132">Требование</span><span class="sxs-lookup"><span data-stu-id="94a18-132">Requirement</span></span> | <span data-ttu-id="94a18-133">Значение</span><span class="sxs-lookup"><span data-stu-id="94a18-133">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="94a18-134">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="94a18-134">TAPI version</span></span><br/> | <span data-ttu-id="94a18-135">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="94a18-135">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="94a18-136">Header</span><span class="sxs-lookup"><span data-stu-id="94a18-136">Header</span></span><br/>       | <dl> <span data-ttu-id="94a18-137"><dt>Сдпблб. h</dt></span><span class="sxs-lookup"><span data-stu-id="94a18-137"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="94a18-138">Библиотека</span><span class="sxs-lookup"><span data-stu-id="94a18-138">Library</span></span><br/>      | <dl> <span data-ttu-id="94a18-139"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="94a18-139"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="94a18-140">DLL</span><span class="sxs-lookup"><span data-stu-id="94a18-140">DLL</span></span><br/>          | <dl> <span data-ttu-id="94a18-141"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="94a18-141"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94a18-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="94a18-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94a18-143">**итсдп**</span><span class="sxs-lookup"><span data-stu-id="94a18-143">**ITSdp**</span></span>](itsdp.md)
</dt> <dt>

[<span data-ttu-id="94a18-144">**итмедиаколлектион**</span><span class="sxs-lookup"><span data-stu-id="94a18-144">**ITMediaCollection**</span></span>](itmediacollection.md)
</dt> </dl>

 

 




