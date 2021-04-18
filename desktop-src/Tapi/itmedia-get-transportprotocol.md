---
description: Метод Get \_ транспортпротокол получает транспортный протокол.
ms.assetid: d270d6f4-bdcf-4cf4-970b-65f0be706171
title: 'Метод Итмедиа:: get_TransportProtocol (Сдпблб. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cf2bc66a98e181674bbf6f7956579bbaa0b5a72
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105674898"
---
# <a name="itmediaget_transportprotocol-method"></a><span data-ttu-id="3a4ff-103">Метод Итмедиа:: Get \_ транспортпротокол</span><span class="sxs-lookup"><span data-stu-id="3a4ff-103">ITMedia::get\_TransportProtocol method</span></span>

<span data-ttu-id="3a4ff-104">\[ В Windows Vista, Windows Server 2008 и последующих версиях операционной системы нельзя использовать встречные средства и элементы управления Конференц-телефонией и интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="3a4ff-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="3a4ff-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="3a4ff-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="3a4ff-106">Метод **Get \_ транспортпротокол** получает транспортный протокол.</span><span class="sxs-lookup"><span data-stu-id="3a4ff-106">The **get\_TransportProtocol** method gets the transport protocol.</span></span> <span data-ttu-id="3a4ff-107">Это указывается в дополнение к формату мультимедиа, чтобы один и тот же стандартный формат мультимедиа можно было переносить по разным транспортным протоколам, даже если сетевой протокол аналогичен, например, с помощью звука PCM и звука PCM в формате "сеть — налог".</span><span class="sxs-lookup"><span data-stu-id="3a4ff-107">This is specified in addition to the media format so that the same standard media format may be carried over different transport protocols even when the network protocol is the same, such as with Vat PCM audio and RTP PCM audio.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a4ff-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3a4ff-108">Syntax</span></span>


```C++
HRESULT get_TransportProtocol(
  [out] BSTR *ppProtocol
);
```



## <a name="parameters"></a><span data-ttu-id="3a4ff-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="3a4ff-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a4ff-110">*пппротокол* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="3a4ff-110">*ppProtocol* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3a4ff-111">Указатель на представление **BSTR** транспортного протокола.</span><span class="sxs-lookup"><span data-stu-id="3a4ff-111">Pointer to the **BSTR** representation of the transport protocol.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a4ff-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3a4ff-112">Return value</span></span>

<span data-ttu-id="3a4ff-113">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="3a4ff-113">This method can return one of these values.</span></span>



| <span data-ttu-id="3a4ff-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="3a4ff-114">Return code</span></span>                                                                                   | <span data-ttu-id="3a4ff-115">Описание</span><span class="sxs-lookup"><span data-stu-id="3a4ff-115">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="3a4ff-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="3a4ff-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="3a4ff-117">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="3a4ff-117">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="3a4ff-118"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="3a4ff-118"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="3a4ff-119">Параметр *пппротокол* не является допустимым указателем.</span><span class="sxs-lookup"><span data-stu-id="3a4ff-119">The *ppProtocol* parameter is not a valid pointer.</span></span><br/>   |
| <dl> <span data-ttu-id="3a4ff-120"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="3a4ff-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="3a4ff-121">Недостаточно памяти для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="3a4ff-121">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="3a4ff-122"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="3a4ff-122"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="3a4ff-123">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="3a4ff-123">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="3a4ff-124"><dt>**E \_ нотимпл**</dt></span><span class="sxs-lookup"><span data-stu-id="3a4ff-124"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="3a4ff-125">Этот метод еще не реализован.</span><span class="sxs-lookup"><span data-stu-id="3a4ff-125">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="3a4ff-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3a4ff-126">Remarks</span></span>

<span data-ttu-id="3a4ff-127">Приложение должно использовать [**сисфристринг**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) для освобождения памяти, выделенной для параметра *пппротокол* .</span><span class="sxs-lookup"><span data-stu-id="3a4ff-127">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory allocated for the *ppProtocol* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a4ff-128">Требования</span><span class="sxs-lookup"><span data-stu-id="3a4ff-128">Requirements</span></span>



| <span data-ttu-id="3a4ff-129">Требование</span><span class="sxs-lookup"><span data-stu-id="3a4ff-129">Requirement</span></span> | <span data-ttu-id="3a4ff-130">Значение</span><span class="sxs-lookup"><span data-stu-id="3a4ff-130">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3a4ff-131">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="3a4ff-131">TAPI version</span></span><br/> | <span data-ttu-id="3a4ff-132">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="3a4ff-132">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="3a4ff-133">Header</span><span class="sxs-lookup"><span data-stu-id="3a4ff-133">Header</span></span><br/>       | <dl> <span data-ttu-id="3a4ff-134"><dt>Сдпблб. h</dt></span><span class="sxs-lookup"><span data-stu-id="3a4ff-134"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="3a4ff-135">Библиотека</span><span class="sxs-lookup"><span data-stu-id="3a4ff-135">Library</span></span><br/>      | <dl> <span data-ttu-id="3a4ff-136"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3a4ff-136"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="3a4ff-137">DLL</span><span class="sxs-lookup"><span data-stu-id="3a4ff-137">DLL</span></span><br/>          | <dl> <span data-ttu-id="3a4ff-138"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3a4ff-138"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a4ff-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3a4ff-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a4ff-140">**итмедиа**</span><span class="sxs-lookup"><span data-stu-id="3a4ff-140">**ITMedia**</span></span>](itmedia.md)
</dt> <dt>

[<span data-ttu-id="3a4ff-141">**Итмедиа::p UT \_ транспортпротокол**</span><span class="sxs-lookup"><span data-stu-id="3a4ff-141">**ITMedia::put\_TransportProtocol**</span></span>](itmedia-put-transportprotocol.md)
</dt> </dl>

 

