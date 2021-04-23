---
description: Метод Get \_ медиатитле извлекает текстовое название для носителя, который приложение может использовать для информационных и экранных целей. Это должна быть Преобразуемая строка в кодировке ASCII, если кодировка — ASCII. В противном случае это может быть любая строка BSTR.
ms.assetid: c5567672-54f0-45d6-81d2-5a501a33c25f
title: 'Метод Итмедиа:: get_MediaTitle (Сдпблб. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59f2ec4bf16fc27c23277113ee13c8fe02f89c6e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675487"
---
# <a name="itmediaget_mediatitle-method"></a><span data-ttu-id="4be31-105">Метод Итмедиа:: Get \_ медиатитле</span><span class="sxs-lookup"><span data-stu-id="4be31-105">ITMedia::get\_MediaTitle method</span></span>

<span data-ttu-id="4be31-106">\[ В Windows Vista, Windows Server 2008 и последующих версиях операционной системы нельзя использовать встречные средства и элементы управления Конференц-телефонией и интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="4be31-106">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="4be31-107">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="4be31-107">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="4be31-108">Метод **Get \_ медиатитле** извлекает текстовое название для носителя, который приложение может использовать для информационных и экранных целей.</span><span class="sxs-lookup"><span data-stu-id="4be31-108">The **get\_MediaTitle** method retrieves a textual title for the media that the application can use for informational or display purposes.</span></span> <span data-ttu-id="4be31-109">Это должна быть Преобразуемая строка в кодировке ASCII, если кодировка — ASCII.</span><span class="sxs-lookup"><span data-stu-id="4be31-109">This must be an ASCII convertible string if the character set is ASCII.</span></span> <span data-ttu-id="4be31-110">В противном случае это может быть любая строка **BSTR** .</span><span class="sxs-lookup"><span data-stu-id="4be31-110">Otherwise, it can be any **BSTR** string.</span></span>

## <a name="syntax"></a><span data-ttu-id="4be31-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4be31-111">Syntax</span></span>


```C++
HRESULT get_MediaTitle(
  [out] BSTR *ppMediaTitle
);
```



## <a name="parameters"></a><span data-ttu-id="4be31-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="4be31-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4be31-113">*ппмедиатитле* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="4be31-113">*ppMediaTitle* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4be31-114">Указатель на **строку BSTR** , содержащую заголовок носителя.</span><span class="sxs-lookup"><span data-stu-id="4be31-114">Pointer to a **BSTR** containing the title of the media.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4be31-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4be31-115">Return value</span></span>

<span data-ttu-id="4be31-116">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="4be31-116">This method can return one of these values.</span></span>



| <span data-ttu-id="4be31-117">Код возврата</span><span class="sxs-lookup"><span data-stu-id="4be31-117">Return code</span></span>                                                                                   | <span data-ttu-id="4be31-118">Описание</span><span class="sxs-lookup"><span data-stu-id="4be31-118">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="4be31-119"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="4be31-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="4be31-120">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="4be31-120">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="4be31-121"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="4be31-121"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="4be31-122">Параметр *ппмедиатитле* не является допустимым указателем.</span><span class="sxs-lookup"><span data-stu-id="4be31-122">The *ppMediaTitle* parameter is not a valid pointer.</span></span><br/> |
| <dl> <span data-ttu-id="4be31-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="4be31-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="4be31-124">Недостаточно памяти для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="4be31-124">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="4be31-125"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="4be31-125"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="4be31-126">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="4be31-126">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="4be31-127"><dt>**E \_ нотимпл**</dt></span><span class="sxs-lookup"><span data-stu-id="4be31-127"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="4be31-128">Этот метод еще не реализован.</span><span class="sxs-lookup"><span data-stu-id="4be31-128">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="4be31-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4be31-129">Remarks</span></span>

<span data-ttu-id="4be31-130">Приложение должно использовать [**сисфристринг**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) для освобождения памяти, выделенной для параметра *ппмедиатитле* .</span><span class="sxs-lookup"><span data-stu-id="4be31-130">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory allocated for the *ppMediaTitle* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="4be31-131">Требования</span><span class="sxs-lookup"><span data-stu-id="4be31-131">Requirements</span></span>



| <span data-ttu-id="4be31-132">Требование</span><span class="sxs-lookup"><span data-stu-id="4be31-132">Requirement</span></span> | <span data-ttu-id="4be31-133">Значение</span><span class="sxs-lookup"><span data-stu-id="4be31-133">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4be31-134">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="4be31-134">TAPI version</span></span><br/> | <span data-ttu-id="4be31-135">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="4be31-135">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="4be31-136">Header</span><span class="sxs-lookup"><span data-stu-id="4be31-136">Header</span></span><br/>       | <dl> <span data-ttu-id="4be31-137"><dt>Сдпблб. h</dt></span><span class="sxs-lookup"><span data-stu-id="4be31-137"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="4be31-138">Библиотека</span><span class="sxs-lookup"><span data-stu-id="4be31-138">Library</span></span><br/>      | <dl> <span data-ttu-id="4be31-139"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4be31-139"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="4be31-140">DLL</span><span class="sxs-lookup"><span data-stu-id="4be31-140">DLL</span></span><br/>          | <dl> <span data-ttu-id="4be31-141"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4be31-141"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4be31-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4be31-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4be31-143">**итмедиа**</span><span class="sxs-lookup"><span data-stu-id="4be31-143">**ITMedia**</span></span>](itmedia.md)
</dt> <dt>

[<span data-ttu-id="4be31-144">**Итмедиа::P UT \_ медиатитле**</span><span class="sxs-lookup"><span data-stu-id="4be31-144">**ITMedia::Put\_MediaTitle**</span></span>](itmedia-put-mediatitle.md)
</dt> </dl>

 

