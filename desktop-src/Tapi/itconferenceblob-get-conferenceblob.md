---
description: Метод Get \_ конференцеблоб получает указатель на текстовый большой двоичный объект для конференций, который в настоящее время хранится в объекте Conference BLOB.
ms.assetid: eb378f84-11bc-4f6e-9133-bc303e07eb53
title: 'Метод Итконференцеблоб:: get_ConferenceBlob (Сдпблб. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e5642f60f7abc1cb10734de1897d35bd5222dd2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675520"
---
# <a name="itconferenceblobget_conferenceblob-method"></a><span data-ttu-id="4c595-103">Метод Итконференцеблоб:: Get \_ конференцеблоб</span><span class="sxs-lookup"><span data-stu-id="4c595-103">ITConferenceBlob::get\_ConferenceBlob method</span></span>

<span data-ttu-id="4c595-104">\[ В Windows Vista, Windows Server 2008 и последующих версиях операционной системы нельзя использовать встречные средства и элементы управления Конференц-телефонией и интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="4c595-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="4c595-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="4c595-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="4c595-106">Метод **Get \_ конференцеблоб** получает указатель на текстовый большой двоичный объект для конференций, который в настоящее время хранится в объекте Conference BLOB.</span><span class="sxs-lookup"><span data-stu-id="4c595-106">The **get\_ConferenceBlob** method gets a pointer to the textual conference blob currently stored in the conference blob object.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c595-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4c595-107">Syntax</span></span>


```C++
HRESULT get_ConferenceBlob(
  [out] BSTR *ppBlob
);
```



## <a name="parameters"></a><span data-ttu-id="4c595-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="4c595-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c595-109">*ппблоб* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="4c595-109">*ppBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4c595-110">Указатель на **строку BSTR** , содержащую большой двоичный объект конференции.</span><span class="sxs-lookup"><span data-stu-id="4c595-110">Pointer to a **BSTR** containing the conference blob.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c595-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4c595-111">Return value</span></span>

<span data-ttu-id="4c595-112">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="4c595-112">This method can return one of these values.</span></span>



| <span data-ttu-id="4c595-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="4c595-113">Return code</span></span>                                                                                   | <span data-ttu-id="4c595-114">Описание</span><span class="sxs-lookup"><span data-stu-id="4c595-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="4c595-115"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="4c595-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="4c595-116">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="4c595-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="4c595-117"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="4c595-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="4c595-118">Параметр *ппблоб* не является допустимым указателем.</span><span class="sxs-lookup"><span data-stu-id="4c595-118">The *ppBlob* parameter is not a valid pointer.</span></span><br/>       |
| <dl> <span data-ttu-id="4c595-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="4c595-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="4c595-120">Недостаточно памяти для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="4c595-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="4c595-121"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="4c595-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="4c595-122">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="4c595-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="4c595-123"><dt>**E \_ нотимпл**</dt></span><span class="sxs-lookup"><span data-stu-id="4c595-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="4c595-124">Этот метод еще не реализован.</span><span class="sxs-lookup"><span data-stu-id="4c595-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="4c595-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4c595-125">Remarks</span></span>

<span data-ttu-id="4c595-126">Приложение должно использовать [**сисфристринг**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) для освобождения памяти, выделенной для параметра *ппблоб* .</span><span class="sxs-lookup"><span data-stu-id="4c595-126">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory allocated for the *ppBlob* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c595-127">Требования</span><span class="sxs-lookup"><span data-stu-id="4c595-127">Requirements</span></span>



| <span data-ttu-id="4c595-128">Требование</span><span class="sxs-lookup"><span data-stu-id="4c595-128">Requirement</span></span> | <span data-ttu-id="4c595-129">Значение</span><span class="sxs-lookup"><span data-stu-id="4c595-129">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4c595-130">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="4c595-130">TAPI version</span></span><br/> | <span data-ttu-id="4c595-131">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="4c595-131">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="4c595-132">Header</span><span class="sxs-lookup"><span data-stu-id="4c595-132">Header</span></span><br/>       | <dl> <span data-ttu-id="4c595-133"><dt>Сдпблб. h</dt></span><span class="sxs-lookup"><span data-stu-id="4c595-133"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="4c595-134">Библиотека</span><span class="sxs-lookup"><span data-stu-id="4c595-134">Library</span></span><br/>      | <dl> <span data-ttu-id="4c595-135"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4c595-135"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="4c595-136">DLL</span><span class="sxs-lookup"><span data-stu-id="4c595-136">DLL</span></span><br/>          | <dl> <span data-ttu-id="4c595-137"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4c595-137"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c595-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4c595-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c595-139">**итконференцеблоб**</span><span class="sxs-lookup"><span data-stu-id="4c595-139">**ITConferenceBlob**</span></span>](itconferenceblob.md)
</dt> <dt>

[<span data-ttu-id="4c595-140">**\_набор символов BLOB-объектов \_**</span><span class="sxs-lookup"><span data-stu-id="4c595-140">**BLOB\_CHARACTER\_SET**</span></span>](blob-character-set.md)
</dt> </dl>

 

