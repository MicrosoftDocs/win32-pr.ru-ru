---
description: Метод Get \_ тимеколлектион получает указатель на интерфейс иттимеколлектион для Конференции.
ms.assetid: 1cfe3f5a-dcf7-480b-9b23-e17259d8ee9c
title: 'Метод Итсдп:: get_TimeCollection (Сдпблб. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1bac0f38f8c96762d4e36d8d3dfdff2136bdb86
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689067"
---
# <a name="itsdpget_timecollection-method"></a><span data-ttu-id="ccf2b-103">Метод Итсдп:: Get \_ тимеколлектион</span><span class="sxs-lookup"><span data-stu-id="ccf2b-103">ITSdp::get\_TimeCollection method</span></span>

<span data-ttu-id="ccf2b-104">\[ В Windows Vista, Windows Server 2008 и последующих версиях операционной системы нельзя использовать встречные средства и элементы управления Конференц-телефонией и интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="ccf2b-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="ccf2b-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="ccf2b-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="ccf2b-106">Метод **Get \_ тимеколлектион** получает указатель на интерфейс [**иттимеколлектион**](ittimecollection.md) для Конференции.</span><span class="sxs-lookup"><span data-stu-id="ccf2b-106">The **get\_TimeCollection** method gets a pointer to an [**ITTimeCollection**](ittimecollection.md) interface for conference.</span></span>

## <a name="syntax"></a><span data-ttu-id="ccf2b-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ccf2b-107">Syntax</span></span>


```C++
HRESULT get_TimeCollection(
  [out] ITTimeCollection **ppTimeCollection
);
```



## <a name="parameters"></a><span data-ttu-id="ccf2b-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="ccf2b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ccf2b-109">*пптимеколлектион* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="ccf2b-109">*ppTimeCollection* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ccf2b-110">Указатель на [**иттимеколлектион**](ittimecollection.md).</span><span class="sxs-lookup"><span data-stu-id="ccf2b-110">Pointer to [**ITTimeCollection**](ittimecollection.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ccf2b-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ccf2b-111">Return value</span></span>

<span data-ttu-id="ccf2b-112">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="ccf2b-112">This method can return one of these values.</span></span>



| <span data-ttu-id="ccf2b-113">Значение</span><span class="sxs-lookup"><span data-stu-id="ccf2b-113">Value</span></span>                                                                                                                           | <span data-ttu-id="ccf2b-114">Значение</span><span class="sxs-lookup"><span data-stu-id="ccf2b-114">Meaning</span></span>                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ccf2b-115"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="ccf2b-115"><dt>**S\_OK**</dt></span></span> </dl>                                            | <span data-ttu-id="ccf2b-116">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="ccf2b-116">Method succeeded.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="ccf2b-117"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="ccf2b-117"><dt>**E\_INVALIDARG**</dt></span></span> </dl>                                    | <span data-ttu-id="ccf2b-118">Параметр *пптимеколлектион* не является допустимым указателем.</span><span class="sxs-lookup"><span data-stu-id="ccf2b-118">The *ppTimeCollection* parameter is not a valid pointer.</span></span><br/>                         |
| <dl> <span data-ttu-id="ccf2b-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="ccf2b-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>                                   | <span data-ttu-id="ccf2b-120">Недостаточно памяти для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="ccf2b-120">Insufficient memory exists to perform the operation.</span></span><br/>                             |
| <dl> <span data-ttu-id="ccf2b-121"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="ccf2b-121"><dt>**E\_FAIL**</dt></span></span> </dl>                                          | <span data-ttu-id="ccf2b-122">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="ccf2b-122">Unspecified error.</span></span><br/>                                                               |
| <dl> <span data-ttu-id="ccf2b-123"><dt>**HRESULT \_ из \_ \_ кода ошибки (ошибка: \_ недопустимые \_ данные)**</dt></span><span class="sxs-lookup"><span data-stu-id="ccf2b-123"><dt>**HRESULT\_FROM\_ERROR\_CODE(ERROR\_INVALID\_DATA)**</dt></span></span> </dl> | <span data-ttu-id="ccf2b-124">Произошла внутренняя ошибка, обычно из-за сбоя предыдущего метода.</span><span class="sxs-lookup"><span data-stu-id="ccf2b-124">An internal error has occurred, usually due to the failure of a previous method.</span></span><br/> |
| <dl> <span data-ttu-id="ccf2b-125"><dt>**E \_ нотимпл**</dt></span><span class="sxs-lookup"><span data-stu-id="ccf2b-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>                                       | <span data-ttu-id="ccf2b-126">Этот метод еще не реализован.</span><span class="sxs-lookup"><span data-stu-id="ccf2b-126">This method is not yet implemented.</span></span><br/>                                              |



 

## <a name="remarks"></a><span data-ttu-id="ccf2b-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ccf2b-127">Remarks</span></span>

<span data-ttu-id="ccf2b-128">[**Иттимеколлектион**](ittimecollection.md) указатель можно также получить с помощью **QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="ccf2b-128">An [**ITTimeCollection**](ittimecollection.md) pointer could also be obtained using **QueryInterface**.</span></span>

<span data-ttu-id="ccf2b-129">TAPI вызывает метод **AddRef** в интерфейсе [**иттимеколлектион**](ittimecollection.md) , возвращенном методом **итсдп:: Get \_ тимеколлектион**.</span><span class="sxs-lookup"><span data-stu-id="ccf2b-129">TAPI calls the **AddRef** method on the [**ITTimeCollection**](ittimecollection.md) interface returned by **ITSdp::get\_TimeCollection**.</span></span> <span data-ttu-id="ccf2b-130">Приложение должно вызвать **выпуск** в интерфейсе **иттимеколлектион** , чтобы освободить ресурсы, связанные с ним.</span><span class="sxs-lookup"><span data-stu-id="ccf2b-130">The application must call **Release** on the **ITTimeCollection** interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="ccf2b-131">Требования</span><span class="sxs-lookup"><span data-stu-id="ccf2b-131">Requirements</span></span>



| <span data-ttu-id="ccf2b-132">Требование</span><span class="sxs-lookup"><span data-stu-id="ccf2b-132">Requirement</span></span> | <span data-ttu-id="ccf2b-133">Значение</span><span class="sxs-lookup"><span data-stu-id="ccf2b-133">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ccf2b-134">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="ccf2b-134">TAPI version</span></span><br/> | <span data-ttu-id="ccf2b-135">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="ccf2b-135">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="ccf2b-136">Header</span><span class="sxs-lookup"><span data-stu-id="ccf2b-136">Header</span></span><br/>       | <dl> <span data-ttu-id="ccf2b-137"><dt>Сдпблб. h</dt></span><span class="sxs-lookup"><span data-stu-id="ccf2b-137"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="ccf2b-138">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ccf2b-138">Library</span></span><br/>      | <dl> <span data-ttu-id="ccf2b-139"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ccf2b-139"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="ccf2b-140">DLL</span><span class="sxs-lookup"><span data-stu-id="ccf2b-140">DLL</span></span><br/>          | <dl> <span data-ttu-id="ccf2b-141"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ccf2b-141"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ccf2b-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ccf2b-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ccf2b-143">**итсдп**</span><span class="sxs-lookup"><span data-stu-id="ccf2b-143">**ITSdp**</span></span>](itsdp.md)
</dt> <dt>

[<span data-ttu-id="ccf2b-144">**иттимеколлектион**</span><span class="sxs-lookup"><span data-stu-id="ccf2b-144">**ITTimeCollection**</span></span>](ittimecollection.md)
</dt> </dl>

 

 




