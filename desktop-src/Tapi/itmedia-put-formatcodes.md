---
description: Метод размещения \_ форматкодес задает список кодов формата полезных данных мультимедиа. Вариант содержит SAFEARRAY для BSTR. Каждая BSTR в этом массиве является строкой кода форматирования.
ms.assetid: b76a7fee-0fae-41fb-a8cd-6803458d9182
title: 'Итмедиа: метод ut_FormatCodes:p (Сдпблб. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9131f946635c2bb066e704f1d6245c1c30d1372
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685022"
---
# <a name="itmediaput_formatcodes-method"></a><span data-ttu-id="a6aac-105">Итмедиа::p UT \_ форматкодес метод</span><span class="sxs-lookup"><span data-stu-id="a6aac-105">ITMedia::put\_FormatCodes method</span></span>

<span data-ttu-id="a6aac-106">\[ В Windows Vista, Windows Server 2008 и последующих версиях операционной системы нельзя использовать встречные средства и элементы управления Конференц-телефонией и интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="a6aac-106">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="a6aac-107">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="a6aac-107">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="a6aac-108">Метод **размещения \_ форматкодес** задает список кодов формата полезных данных мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="a6aac-108">The **put\_FormatCodes** method sets the list of media payload format codes.</span></span> <span data-ttu-id="a6aac-109">Вариант содержит SAFEARRAY для **BSTR** s.</span><span class="sxs-lookup"><span data-stu-id="a6aac-109">The variant contains a SAFEARRAY of **BSTR** s.</span></span> <span data-ttu-id="a6aac-110">Каждая **BSTR** в этом массиве является строкой кода форматирования.</span><span class="sxs-lookup"><span data-stu-id="a6aac-110">Each **BSTR** within that array is a format code string.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6aac-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a6aac-111">Syntax</span></span>


```C++
HRESULT put_FormatCodes(
  [in] VARIANT NewVal
);
```



## <a name="parameters"></a><span data-ttu-id="a6aac-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="a6aac-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6aac-113">*Неввал* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a6aac-113">*NewVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a6aac-114">Список кодов формата полезных данных мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="a6aac-114">List of media payload format codes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6aac-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a6aac-115">Return value</span></span>

<span data-ttu-id="a6aac-116">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="a6aac-116">This method can return one of these values.</span></span>



| <span data-ttu-id="a6aac-117">Код возврата</span><span class="sxs-lookup"><span data-stu-id="a6aac-117">Return code</span></span>                                                                                   | <span data-ttu-id="a6aac-118">Описание</span><span class="sxs-lookup"><span data-stu-id="a6aac-118">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="a6aac-119"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="a6aac-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="a6aac-120">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="a6aac-120">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="a6aac-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="a6aac-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="a6aac-122">Недопустимый параметр *неввал* .</span><span class="sxs-lookup"><span data-stu-id="a6aac-122">The *NewVal* parameter is not valid.</span></span><br/>                 |
| <dl> <span data-ttu-id="a6aac-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="a6aac-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="a6aac-124">Недостаточно памяти для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="a6aac-124">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="a6aac-125"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="a6aac-125"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="a6aac-126">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="a6aac-126">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="a6aac-127"><dt>**E \_ нотимпл**</dt></span><span class="sxs-lookup"><span data-stu-id="a6aac-127"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="a6aac-128">Этот метод еще не реализован.</span><span class="sxs-lookup"><span data-stu-id="a6aac-128">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="a6aac-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a6aac-129">Remarks</span></span>

<span data-ttu-id="a6aac-130">При указании списка форматов полезных данных это означает, что все эти форматы могут использоваться в сеансе, но первый из этих форматов является форматом по умолчанию для сеанса.</span><span class="sxs-lookup"><span data-stu-id="a6aac-130">When a list of payload formats is given, this implies that all of these formats may be used in the session, but the first of these formats is the default format for the session.</span></span> <span data-ttu-id="a6aac-131">Если транспортным протоколом является RTP, то коды форматов являются типами полезных данных RTP.</span><span class="sxs-lookup"><span data-stu-id="a6aac-131">When the transport protocol is RTP, the format codes are RTP payload types.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6aac-132">Требования</span><span class="sxs-lookup"><span data-stu-id="a6aac-132">Requirements</span></span>



| <span data-ttu-id="a6aac-133">Требование</span><span class="sxs-lookup"><span data-stu-id="a6aac-133">Requirement</span></span> | <span data-ttu-id="a6aac-134">Значение</span><span class="sxs-lookup"><span data-stu-id="a6aac-134">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a6aac-135">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="a6aac-135">TAPI version</span></span><br/> | <span data-ttu-id="a6aac-136">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="a6aac-136">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="a6aac-137">Header</span><span class="sxs-lookup"><span data-stu-id="a6aac-137">Header</span></span><br/>       | <dl> <span data-ttu-id="a6aac-138"><dt>Сдпблб. h</dt></span><span class="sxs-lookup"><span data-stu-id="a6aac-138"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="a6aac-139">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a6aac-139">Library</span></span><br/>      | <dl> <span data-ttu-id="a6aac-140"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a6aac-140"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="a6aac-141">DLL</span><span class="sxs-lookup"><span data-stu-id="a6aac-141">DLL</span></span><br/>          | <dl> <span data-ttu-id="a6aac-142"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a6aac-142"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6aac-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a6aac-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6aac-144">**итмедиа**</span><span class="sxs-lookup"><span data-stu-id="a6aac-144">**ITMedia**</span></span>](itmedia.md)
</dt> <dt>

[<span data-ttu-id="a6aac-145">**Итмедиа:: Get \_ форматкодес**</span><span class="sxs-lookup"><span data-stu-id="a6aac-145">**ITMedia::get\_FormatCodes**</span></span>](itmedia-get-formatcodes.md)
</dt> </dl>

 

 




