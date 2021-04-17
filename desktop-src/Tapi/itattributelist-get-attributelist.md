---
description: Метод Get \_ аттрибутелист получает список атрибутов.
ms.assetid: 75518257-3339-441f-9965-b93e27f0e2bf
title: 'Метод Итаттрибутелист:: get_AttributeList (Сдпблб. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 499352cd5087f478e58653fd304e27101db9b433
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689349"
---
# <a name="itattributelistget_attributelist-method"></a><span data-ttu-id="714ff-103">Метод Итаттрибутелист:: Get \_ аттрибутелист</span><span class="sxs-lookup"><span data-stu-id="714ff-103">ITAttributeList::get\_AttributeList method</span></span>

<span data-ttu-id="714ff-104">\[ В Windows Vista, Windows Server 2008 и последующих версиях операционной системы нельзя использовать встречные средства и элементы управления Конференц-телефонией и интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="714ff-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="714ff-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="714ff-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="714ff-106">Метод **Get \_ аттрибутелист** получает список атрибутов.</span><span class="sxs-lookup"><span data-stu-id="714ff-106">The **get\_AttributeList** method gets the list of attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="714ff-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="714ff-107">Syntax</span></span>


```C++
HRESULT get_AttributeList(
  [out] VARIANT *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="714ff-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="714ff-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="714ff-109">*Pval* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="714ff-109">*pVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="714ff-110">Массив атрибутов.</span><span class="sxs-lookup"><span data-stu-id="714ff-110">Array of attributes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="714ff-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="714ff-111">Return value</span></span>

<span data-ttu-id="714ff-112">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="714ff-112">This method can return one of these values.</span></span>



| <span data-ttu-id="714ff-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="714ff-113">Return code</span></span>                                                                                   | <span data-ttu-id="714ff-114">Описание</span><span class="sxs-lookup"><span data-stu-id="714ff-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="714ff-115"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="714ff-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="714ff-116">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="714ff-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="714ff-117"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="714ff-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="714ff-118">Параметр *Pval* не является допустимым указателем.</span><span class="sxs-lookup"><span data-stu-id="714ff-118">The *pVal* parameter is not a valid pointer.</span></span><br/>         |
| <dl> <span data-ttu-id="714ff-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="714ff-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="714ff-120">Недостаточно памяти для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="714ff-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="714ff-121"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="714ff-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="714ff-122">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="714ff-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="714ff-123"><dt>**E \_ нотимпл**</dt></span><span class="sxs-lookup"><span data-stu-id="714ff-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="714ff-124">Этот метод еще не реализован.</span><span class="sxs-lookup"><span data-stu-id="714ff-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="714ff-125">Требования</span><span class="sxs-lookup"><span data-stu-id="714ff-125">Requirements</span></span>



| <span data-ttu-id="714ff-126">Требование</span><span class="sxs-lookup"><span data-stu-id="714ff-126">Requirement</span></span> | <span data-ttu-id="714ff-127">Значение</span><span class="sxs-lookup"><span data-stu-id="714ff-127">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="714ff-128">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="714ff-128">TAPI version</span></span><br/> | <span data-ttu-id="714ff-129">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="714ff-129">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="714ff-130">Header</span><span class="sxs-lookup"><span data-stu-id="714ff-130">Header</span></span><br/>       | <dl> <span data-ttu-id="714ff-131"><dt>Сдпблб. h</dt></span><span class="sxs-lookup"><span data-stu-id="714ff-131"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="714ff-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="714ff-132">Library</span></span><br/>      | <dl> <span data-ttu-id="714ff-133"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="714ff-133"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="714ff-134">DLL</span><span class="sxs-lookup"><span data-stu-id="714ff-134">DLL</span></span><br/>          | <dl> <span data-ttu-id="714ff-135"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="714ff-135"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="714ff-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="714ff-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="714ff-137">**итаттрибутелист**</span><span class="sxs-lookup"><span data-stu-id="714ff-137">**ITAttributeList**</span></span>](itattributelist.md)
</dt> <dt>

[<span data-ttu-id="714ff-138">**Итаттрибутелист::p UT \_ аттрибутелист**</span><span class="sxs-lookup"><span data-stu-id="714ff-138">**ITAttributeList::put\_AttributeList**</span></span>](itattributelist-put-attributelist.md)
</dt> </dl>

 

 




