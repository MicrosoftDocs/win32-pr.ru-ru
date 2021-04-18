---
description: Метод Delete удаляет носитель, соответствующий указанному индексу.
ms.assetid: 5fcbd026-75a8-4db2-a701-e080dc222537
title: Итмедиаколлектион::D удалить метод (Сдпблб. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0ffabee84bd7d04f517ef26ad5259f642cfed48
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675819"
---
# <a name="itmediacollectiondelete-method"></a><span data-ttu-id="add16-103">Итмедиаколлектион::D удалить метод</span><span class="sxs-lookup"><span data-stu-id="add16-103">ITMediaCollection::Delete method</span></span>

<span data-ttu-id="add16-104">\[ В Windows Vista, Windows Server 2008 и последующих версиях операционной системы нельзя использовать встречные средства и элементы управления Конференц-телефонией и интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="add16-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="add16-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="add16-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="add16-106">Метод **Delete** удаляет носитель, соответствующий указанному индексу.</span><span class="sxs-lookup"><span data-stu-id="add16-106">The **Delete** method deletes the media corresponding to the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="add16-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="add16-107">Syntax</span></span>


```C++
HRESULT Delete(
  [in] LONG Index
);
```



## <a name="parameters"></a><span data-ttu-id="add16-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="add16-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="add16-109">*Индекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="add16-109">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="add16-110">Индекс удаляемого носителя.</span><span class="sxs-lookup"><span data-stu-id="add16-110">Index of media to be deleted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="add16-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="add16-111">Return value</span></span>

<span data-ttu-id="add16-112">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="add16-112">This method can return one of these values.</span></span>



| <span data-ttu-id="add16-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="add16-113">Return code</span></span>                                                                                                                              | <span data-ttu-id="add16-114">Описание</span><span class="sxs-lookup"><span data-stu-id="add16-114">Description</span></span>                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="add16-115"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="add16-115"><dt>**S\_OK**</dt></span></span> </dl>                                                     | <span data-ttu-id="add16-116">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="add16-116">Method succeeded.</span></span><br/>                                                                             |
| <dl> <span data-ttu-id="add16-117"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="add16-117"><dt>**E\_INVALIDARG**</dt></span></span> </dl>                                             | <span data-ttu-id="add16-118">Значение параметра *индекса* меньше 1 или больше текущего числа элементов.</span><span class="sxs-lookup"><span data-stu-id="add16-118">The *Index* parameter has a value less than 1 or greater than the current number of elements.</span></span><br/> |
| <dl> <span data-ttu-id="add16-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="add16-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>                                            | <span data-ttu-id="add16-120">Недостаточно памяти для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="add16-120">Insufficient memory exists to perform the operation.</span></span><br/>                                          |
| <dl> <span data-ttu-id="add16-121"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="add16-121"><dt>**E\_FAIL**</dt></span></span> </dl>                                                   | <span data-ttu-id="add16-122">Внутренняя ошибка (возникает, только если предыдущий вызов вернул ошибку).</span><span class="sxs-lookup"><span data-stu-id="add16-122">Internal error (should only occur if a previous call returned an error).</span></span><br/>                      |
| <dl> <span data-ttu-id="add16-123"><dt>**E \_ нотимпл**</dt></span><span class="sxs-lookup"><span data-stu-id="add16-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>                                                | <span data-ttu-id="add16-124">Этот метод еще не реализован.</span><span class="sxs-lookup"><span data-stu-id="add16-124">This method is not yet implemented.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="add16-125"><dt>**ЗНАЧЕНИЕ \_ HRESULT \_ из \_ кода ошибки ( \_ \_ уничтоженный BLOB-объект сдпблб CONF \_ )**</dt></span><span class="sxs-lookup"><span data-stu-id="add16-125"><dt>**HRESULT\_FROM\_ERROR\_CODE(SDPBLB\_CONF\_BLOB\_DESTROYED)**</dt></span></span> </dl> | <span data-ttu-id="add16-126">BLOB-объект SDP не существует.</span><span class="sxs-lookup"><span data-stu-id="add16-126">The SDP blob doesn't exist.</span></span><br/>                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="add16-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="add16-127">Remarks</span></span>

<span data-ttu-id="add16-128">Большинство списков C и C++ основаны на 0, но этот индекс основан на 1 для Visual Basic совместимости, то есть первый элемент имеет номер индекса 1.</span><span class="sxs-lookup"><span data-stu-id="add16-128">Most C and C++ lists are 0-based, but this index is 1-based for Visual Basic compatibility, meaning the first item has an index number of 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="add16-129">Требования</span><span class="sxs-lookup"><span data-stu-id="add16-129">Requirements</span></span>



| <span data-ttu-id="add16-130">Требование</span><span class="sxs-lookup"><span data-stu-id="add16-130">Requirement</span></span> | <span data-ttu-id="add16-131">Значение</span><span class="sxs-lookup"><span data-stu-id="add16-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="add16-132">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="add16-132">TAPI version</span></span><br/> | <span data-ttu-id="add16-133">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="add16-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="add16-134">Header</span><span class="sxs-lookup"><span data-stu-id="add16-134">Header</span></span><br/>       | <dl> <span data-ttu-id="add16-135"><dt>Сдпблб. h</dt></span><span class="sxs-lookup"><span data-stu-id="add16-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="add16-136">Библиотека</span><span class="sxs-lookup"><span data-stu-id="add16-136">Library</span></span><br/>      | <dl> <span data-ttu-id="add16-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="add16-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="add16-138">DLL</span><span class="sxs-lookup"><span data-stu-id="add16-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="add16-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="add16-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="add16-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="add16-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="add16-141">**итмедиаколлектион**</span><span class="sxs-lookup"><span data-stu-id="add16-141">**ITMediaCollection**</span></span>](itmediacollection.md)
</dt> </dl>

 

 




