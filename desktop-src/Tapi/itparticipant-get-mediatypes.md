---
description: Метод Get \_ медиатипес получает типы мультимедиа, связанные с участником.
ms.assetid: a2323d16-8eec-4c17-b5f2-b6fbd910ba60
title: 'Метод ИтпартиЦипант:: get_MediaTypes (Ипмсп. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e464295f58d72e0b905387f188dc2cf6da9ad609
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105674841"
---
# <a name="itparticipantget_mediatypes-method"></a><span data-ttu-id="81c07-103">Метод ИтпартиЦипант:: Get \_ медиатипес</span><span class="sxs-lookup"><span data-stu-id="81c07-103">ITParticipant::get\_MediaTypes method</span></span>

<span data-ttu-id="81c07-104">\[**получить \_ Медиатипес** недоступен для использования в Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="81c07-104">\[**get\_MediaTypes** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="81c07-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="81c07-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="81c07-106">Метод **Get \_ медиатипес** получает [**типы мультимедиа**](tapimediatype--constants.md) , связанные с участником.</span><span class="sxs-lookup"><span data-stu-id="81c07-106">The **get\_MediaTypes** method gets the [**media types**](tapimediatype--constants.md) associated with a participant.</span></span>

## <a name="syntax"></a><span data-ttu-id="81c07-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="81c07-107">Syntax</span></span>


```C++
HRESULT get_MediaTypes(
  [out] long *plMediaType
);
```



## <a name="parameters"></a><span data-ttu-id="81c07-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="81c07-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81c07-109">*плмедиатипе* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="81c07-109">*plMediaType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="81c07-110">Указатель на флаги типа мультимедиа, например \_ видео тапимедиатипе.</span><span class="sxs-lookup"><span data-stu-id="81c07-110">Pointer to media type flags, such as TAPIMEDIATYPE\_VIDEO.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81c07-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="81c07-111">Return value</span></span>

<span data-ttu-id="81c07-112">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="81c07-112">This method can return one of these values.</span></span>



| <span data-ttu-id="81c07-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="81c07-113">Return code</span></span>                                                                                   | <span data-ttu-id="81c07-114">Описание</span><span class="sxs-lookup"><span data-stu-id="81c07-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="81c07-115"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="81c07-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="81c07-116">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="81c07-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="81c07-117"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="81c07-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="81c07-118">Недостаточно памяти для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="81c07-118">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="81c07-119"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="81c07-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="81c07-120">Параметр *плмедиатипе* не является допустимым указателем.</span><span class="sxs-lookup"><span data-stu-id="81c07-120">The *plMediaType* parameter is not a valid pointer.</span></span><br/>  |



 

## <a name="requirements"></a><span data-ttu-id="81c07-121">Требования</span><span class="sxs-lookup"><span data-stu-id="81c07-121">Requirements</span></span>



| <span data-ttu-id="81c07-122">Требование</span><span class="sxs-lookup"><span data-stu-id="81c07-122">Requirement</span></span> | <span data-ttu-id="81c07-123">Значение</span><span class="sxs-lookup"><span data-stu-id="81c07-123">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="81c07-124">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="81c07-124">TAPI version</span></span><br/> | <span data-ttu-id="81c07-125">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="81c07-125">Requires TAPI 3.0 or later</span></span><br/>                                                |
| <span data-ttu-id="81c07-126">Header</span><span class="sxs-lookup"><span data-stu-id="81c07-126">Header</span></span><br/>       | <dl> <span data-ttu-id="81c07-127"><dt>Ипмсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="81c07-127"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="81c07-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="81c07-128">Library</span></span><br/>      | <dl> <span data-ttu-id="81c07-129"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="81c07-129"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="81c07-130">DLL</span><span class="sxs-lookup"><span data-stu-id="81c07-130">DLL</span></span><br/>          | <dl> <span data-ttu-id="81c07-131"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="81c07-131"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81c07-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="81c07-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81c07-133">**итпартиЦипант**</span><span class="sxs-lookup"><span data-stu-id="81c07-133">**ITParticipant**</span></span>](itparticipant.md)
</dt> <dt>

[<span data-ttu-id="81c07-134">**типы носителей**</span><span class="sxs-lookup"><span data-stu-id="81c07-134">**media types**</span></span>](tapimediatype--constants.md)
</dt> </dl>

 

 




