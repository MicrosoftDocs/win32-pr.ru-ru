---
description: Метод Get \_ MediaName получает имя носителя. К определенным носителям относятся аудио, видео, доска, текст и данные.
ms.assetid: 4afb24f9-582e-420d-8bda-772a3dc4d96c
title: 'Метод Итмедиа:: get_MediaName (Сдпблб. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9152994eac98d5e846ac147072a51a3334930da9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689272"
---
# <a name="itmediaget_medianame-method"></a><span data-ttu-id="27386-104">Метод Итмедиа:: Get \_ MediaName</span><span class="sxs-lookup"><span data-stu-id="27386-104">ITMedia::get\_MediaName method</span></span>

<span data-ttu-id="27386-105">\[ В Windows Vista, Windows Server 2008 и последующих версиях операционной системы нельзя использовать встречные средства и элементы управления Конференц-телефонией и интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="27386-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="27386-106">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="27386-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="27386-107">Метод **Get \_ MediaName** получает имя носителя.</span><span class="sxs-lookup"><span data-stu-id="27386-107">The **get\_MediaName** method gets the media name.</span></span> <span data-ttu-id="27386-108">К определенным носителям относятся аудио, видео, доска, текст и данные.</span><span class="sxs-lookup"><span data-stu-id="27386-108">Defined media are audio, video, whiteboard, text, and data.</span></span>

## <a name="syntax"></a><span data-ttu-id="27386-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="27386-109">Syntax</span></span>


```C++
HRESULT get_MediaName(
  [out] BSTR *ppMediaName
);
```



## <a name="parameters"></a><span data-ttu-id="27386-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="27386-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27386-111">*ппмедианаме* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="27386-111">*ppMediaName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="27386-112">Указатель на **BSTR** , содержащий имя носителя, например Audio.</span><span class="sxs-lookup"><span data-stu-id="27386-112">Pointer to a **BSTR** containing the name of the media, such as audio.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27386-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="27386-113">Return value</span></span>

<span data-ttu-id="27386-114">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="27386-114">This method can return one of these values.</span></span>



| <span data-ttu-id="27386-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="27386-115">Return code</span></span>                                                                                   | <span data-ttu-id="27386-116">Описание</span><span class="sxs-lookup"><span data-stu-id="27386-116">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="27386-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="27386-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="27386-118">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="27386-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="27386-119"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="27386-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="27386-120">Параметр *ппмедианаме* не является допустимым указателем.</span><span class="sxs-lookup"><span data-stu-id="27386-120">The *ppMediaName* parameter is not a valid pointer.</span></span><br/>  |
| <dl> <span data-ttu-id="27386-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="27386-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="27386-122">Недостаточно памяти для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="27386-122">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="27386-123"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="27386-123"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="27386-124">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="27386-124">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="27386-125"><dt>**E \_ нотимпл**</dt></span><span class="sxs-lookup"><span data-stu-id="27386-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="27386-126">Этот метод еще не реализован.</span><span class="sxs-lookup"><span data-stu-id="27386-126">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="27386-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="27386-127">Remarks</span></span>

<span data-ttu-id="27386-128">Приложение должно использовать [**сисфристринг**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) для освобождения памяти, выделенной для параметра *ппмедианаме* .</span><span class="sxs-lookup"><span data-stu-id="27386-128">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory allocated for the *ppMediaName* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="27386-129">Требования</span><span class="sxs-lookup"><span data-stu-id="27386-129">Requirements</span></span>



| <span data-ttu-id="27386-130">Требование</span><span class="sxs-lookup"><span data-stu-id="27386-130">Requirement</span></span> | <span data-ttu-id="27386-131">Значение</span><span class="sxs-lookup"><span data-stu-id="27386-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="27386-132">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="27386-132">TAPI version</span></span><br/> | <span data-ttu-id="27386-133">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="27386-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="27386-134">Header</span><span class="sxs-lookup"><span data-stu-id="27386-134">Header</span></span><br/>       | <dl> <span data-ttu-id="27386-135"><dt>Сдпблб. h</dt></span><span class="sxs-lookup"><span data-stu-id="27386-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="27386-136">Библиотека</span><span class="sxs-lookup"><span data-stu-id="27386-136">Library</span></span><br/>      | <dl> <span data-ttu-id="27386-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="27386-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="27386-138">DLL</span><span class="sxs-lookup"><span data-stu-id="27386-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="27386-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="27386-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27386-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="27386-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27386-141">**итмедиа**</span><span class="sxs-lookup"><span data-stu-id="27386-141">**ITMedia**</span></span>](itmedia.md)
</dt> <dt>

[<span data-ttu-id="27386-142">**Итмедиа::p UT \_ MediaName**</span><span class="sxs-lookup"><span data-stu-id="27386-142">**ITMedia::put\_MediaName**</span></span>](itmedia-put-medianame.md)
</dt> </dl>

 

