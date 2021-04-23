---
description: Метод Get \_ форматкодес получает список кодов формата полезных данных мультимедиа. Вариант возвращает SAFEARRAY для BSTR. Каждая BSTR в этом массиве является строкой кода форматирования.
ms.assetid: 8663d7e8-d46f-44d1-93db-9b5142bb28dd
title: 'Метод Итмедиа:: get_FormatCodes (Сдпблб. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce9e28a0323ac001c948a3b19b8dae2cfe9daf5d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675923"
---
# <a name="itmediaget_formatcodes-method"></a><span data-ttu-id="fc0c4-105">Метод Итмедиа:: Get \_ форматкодес</span><span class="sxs-lookup"><span data-stu-id="fc0c4-105">ITMedia::get\_FormatCodes method</span></span>

<span data-ttu-id="fc0c4-106">\[ В Windows Vista, Windows Server 2008 и последующих версиях операционной системы нельзя использовать встречные средства и элементы управления Конференц-телефонией и интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="fc0c4-106">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="fc0c4-107">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="fc0c4-107">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="fc0c4-108">Метод **Get \_ форматкодес** получает список кодов формата полезных данных мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="fc0c4-108">The **get\_FormatCodes** method gets the list of media payload format codes.</span></span> <span data-ttu-id="fc0c4-109">Вариант возвращает SAFEARRAY для **BSTR** s.</span><span class="sxs-lookup"><span data-stu-id="fc0c4-109">The variant returns a SAFEARRAY of **BSTR** s.</span></span> <span data-ttu-id="fc0c4-110">Каждая **BSTR** в этом массиве является строкой кода форматирования.</span><span class="sxs-lookup"><span data-stu-id="fc0c4-110">Each **BSTR** within that array is a format code string.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc0c4-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fc0c4-111">Syntax</span></span>


```C++
HRESULT get_FormatCodes(
  [out] VARIANT *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="fc0c4-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="fc0c4-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc0c4-113">*Pval* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="fc0c4-113">*pVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fc0c4-114">Массив кодов формата полезных данных мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="fc0c4-114">Array of media payload format codes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc0c4-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fc0c4-115">Return value</span></span>

<span data-ttu-id="fc0c4-116">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="fc0c4-116">This method can return one of these values.</span></span>



| <span data-ttu-id="fc0c4-117">Код возврата</span><span class="sxs-lookup"><span data-stu-id="fc0c4-117">Return code</span></span>                                                                                   | <span data-ttu-id="fc0c4-118">Описание</span><span class="sxs-lookup"><span data-stu-id="fc0c4-118">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="fc0c4-119"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="fc0c4-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="fc0c4-120">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="fc0c4-120">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="fc0c4-121"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="fc0c4-121"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="fc0c4-122">Параметр *Pval* не является допустимым указателем.</span><span class="sxs-lookup"><span data-stu-id="fc0c4-122">The *pVal* parameter is not a valid pointer.</span></span><br/>         |
| <dl> <span data-ttu-id="fc0c4-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="fc0c4-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="fc0c4-124">Недостаточно памяти для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="fc0c4-124">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="fc0c4-125"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="fc0c4-125"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="fc0c4-126">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="fc0c4-126">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="fc0c4-127"><dt>**E \_ нотимпл**</dt></span><span class="sxs-lookup"><span data-stu-id="fc0c4-127"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="fc0c4-128">Этот метод еще не реализован.</span><span class="sxs-lookup"><span data-stu-id="fc0c4-128">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="fc0c4-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fc0c4-129">Remarks</span></span>

<span data-ttu-id="fc0c4-130">При указании списка форматов полезных данных это означает, что все эти форматы могут использоваться в сеансе, но первый из этих форматов является форматом по умолчанию для сеанса.</span><span class="sxs-lookup"><span data-stu-id="fc0c4-130">When a list of payload formats is given, this implies that all of these formats may be used in the session, but the first of these formats is the default format for the session.</span></span> <span data-ttu-id="fc0c4-131">Если транспортным протоколом является RTP, то коды форматов являются типами полезных данных RTP.</span><span class="sxs-lookup"><span data-stu-id="fc0c4-131">When the transport protocol is RTP, the format codes are RTP payload types.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc0c4-132">Требования</span><span class="sxs-lookup"><span data-stu-id="fc0c4-132">Requirements</span></span>



| <span data-ttu-id="fc0c4-133">Требование</span><span class="sxs-lookup"><span data-stu-id="fc0c4-133">Requirement</span></span> | <span data-ttu-id="fc0c4-134">Значение</span><span class="sxs-lookup"><span data-stu-id="fc0c4-134">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fc0c4-135">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="fc0c4-135">TAPI version</span></span><br/> | <span data-ttu-id="fc0c4-136">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="fc0c4-136">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="fc0c4-137">Header</span><span class="sxs-lookup"><span data-stu-id="fc0c4-137">Header</span></span><br/>       | <dl> <span data-ttu-id="fc0c4-138"><dt>Сдпблб. h</dt></span><span class="sxs-lookup"><span data-stu-id="fc0c4-138"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="fc0c4-139">Библиотека</span><span class="sxs-lookup"><span data-stu-id="fc0c4-139">Library</span></span><br/>      | <dl> <span data-ttu-id="fc0c4-140"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fc0c4-140"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="fc0c4-141">DLL</span><span class="sxs-lookup"><span data-stu-id="fc0c4-141">DLL</span></span><br/>          | <dl> <span data-ttu-id="fc0c4-142"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fc0c4-142"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc0c4-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fc0c4-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc0c4-144">**итмедиа**</span><span class="sxs-lookup"><span data-stu-id="fc0c4-144">**ITMedia**</span></span>](itmedia.md)
</dt> <dt>

[<span data-ttu-id="fc0c4-145">**Итмедиа::p UT \_ форматкодес**</span><span class="sxs-lookup"><span data-stu-id="fc0c4-145">**ITMedia::put\_FormatCodes**</span></span>](itmedia-put-formatcodes.md)
</dt> </dl>

 

 




