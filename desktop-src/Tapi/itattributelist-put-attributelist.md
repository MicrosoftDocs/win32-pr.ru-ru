---
description: Метод размещения \_ аттрибутелист задает список атрибутов.
ms.assetid: f7d57c0c-9114-42a4-b2bc-c812334d8136
title: 'Итаттрибутелист: метод ut_AttributeList:p (Сдпблб. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3876b2cd8ecdef46a933ff3f3c91be96dd028892
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689346"
---
# <a name="itattributelistput_attributelist-method"></a><span data-ttu-id="50b7a-103">Итаттрибутелист::p UT \_ аттрибутелист метод</span><span class="sxs-lookup"><span data-stu-id="50b7a-103">ITAttributeList::put\_AttributeList method</span></span>

<span data-ttu-id="50b7a-104">\[ В Windows Vista, Windows Server 2008 и последующих версиях операционной системы нельзя использовать встречные средства и элементы управления Конференц-телефонией и интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="50b7a-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="50b7a-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="50b7a-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="50b7a-106">Метод **размещения \_ аттрибутелист** задает список атрибутов.</span><span class="sxs-lookup"><span data-stu-id="50b7a-106">The **put\_AttributeList** method sets the list of attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="50b7a-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="50b7a-107">Syntax</span></span>


```C++
HRESULT put_AttributeList(
  [in] VARIANT newVal
);
```



## <a name="parameters"></a><span data-ttu-id="50b7a-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="50b7a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50b7a-109">*неввал* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="50b7a-109">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50b7a-110">Массив заданных атрибутов.</span><span class="sxs-lookup"><span data-stu-id="50b7a-110">Array of attributes to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50b7a-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="50b7a-111">Return value</span></span>

<span data-ttu-id="50b7a-112">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="50b7a-112">This method can return one of these values.</span></span>



| <span data-ttu-id="50b7a-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="50b7a-113">Return code</span></span>                                                                                   | <span data-ttu-id="50b7a-114">Описание</span><span class="sxs-lookup"><span data-stu-id="50b7a-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="50b7a-115"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="50b7a-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="50b7a-116">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="50b7a-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="50b7a-117"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="50b7a-117"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="50b7a-118">Недопустимый параметр *неввал* .</span><span class="sxs-lookup"><span data-stu-id="50b7a-118">The *newVal* parameter is not valid.</span></span><br/>                 |
| <dl> <span data-ttu-id="50b7a-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="50b7a-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="50b7a-120">Недостаточно памяти для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="50b7a-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="50b7a-121"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="50b7a-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="50b7a-122">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="50b7a-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="50b7a-123"><dt>**E \_ нотимпл**</dt></span><span class="sxs-lookup"><span data-stu-id="50b7a-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="50b7a-124">Этот метод еще не реализован.</span><span class="sxs-lookup"><span data-stu-id="50b7a-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="50b7a-125">Требования</span><span class="sxs-lookup"><span data-stu-id="50b7a-125">Requirements</span></span>



| <span data-ttu-id="50b7a-126">Требование</span><span class="sxs-lookup"><span data-stu-id="50b7a-126">Requirement</span></span> | <span data-ttu-id="50b7a-127">Значение</span><span class="sxs-lookup"><span data-stu-id="50b7a-127">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="50b7a-128">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="50b7a-128">TAPI version</span></span><br/> | <span data-ttu-id="50b7a-129">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="50b7a-129">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="50b7a-130">Header</span><span class="sxs-lookup"><span data-stu-id="50b7a-130">Header</span></span><br/>       | <dl> <span data-ttu-id="50b7a-131"><dt>Сдпблб. h</dt></span><span class="sxs-lookup"><span data-stu-id="50b7a-131"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="50b7a-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="50b7a-132">Library</span></span><br/>      | <dl> <span data-ttu-id="50b7a-133"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="50b7a-133"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="50b7a-134">DLL</span><span class="sxs-lookup"><span data-stu-id="50b7a-134">DLL</span></span><br/>          | <dl> <span data-ttu-id="50b7a-135"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="50b7a-135"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50b7a-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="50b7a-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50b7a-137">**итаттрибутелист**</span><span class="sxs-lookup"><span data-stu-id="50b7a-137">**ITAttributeList**</span></span>](itattributelist.md)
</dt> <dt>

[<span data-ttu-id="50b7a-138">**Итаттрибутелист:: Get \_ аттрибутелист**</span><span class="sxs-lookup"><span data-stu-id="50b7a-138">**ITAttributeList::get\_AttributeList**</span></span>](itattributelist-get-attributelist.md)
</dt> </dl>

 

 




