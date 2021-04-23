---
description: Метод Get \_ Item получает указатель итмедиа, соответствующий указанному индексу.
ms.assetid: ad218357-82c8-4fcb-b71b-ba17564a5ca5
title: 'Метод Итмедиаколлектион:: get_Item (Сдпблб. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c68f3571dbd1f66e325dd7fa1bb30dfe6d6bc35
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689045"
---
# <a name="itmediacollectionget_item-method"></a><span data-ttu-id="a4c50-103">Метод Итмедиаколлектион:: Get \_ Item</span><span class="sxs-lookup"><span data-stu-id="a4c50-103">ITMediaCollection::get\_Item method</span></span>

<span data-ttu-id="a4c50-104">\[ В Windows Vista, Windows Server 2008 и последующих версиях операционной системы нельзя использовать встречные средства и элементы управления Конференц-телефонией и интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="a4c50-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="a4c50-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="a4c50-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="a4c50-106">Метод **Get \_ Item** получает указатель [**итмедиа**](itmedia.md) , соответствующий указанному индексу.</span><span class="sxs-lookup"><span data-stu-id="a4c50-106">The **get\_Item** method gets an [**ITMedia**](itmedia.md) pointer corresponding to the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4c50-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a4c50-107">Syntax</span></span>


```C++
HRESULT get_Item(
  [in]  LONG    Index,
  [out] ITMedia **pVal
);
```



## <a name="parameters"></a><span data-ttu-id="a4c50-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="a4c50-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4c50-109">*Индекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a4c50-109">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4c50-110">Индекс получаемого элемента мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="a4c50-110">Index of media item to get.</span></span>

</dd> <dt>

<span data-ttu-id="a4c50-111">*Pval* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="a4c50-111">*pVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a4c50-112">Указатель на интерфейс [**итмедиа**](itmedia.md) для требуемого элемента.</span><span class="sxs-lookup"><span data-stu-id="a4c50-112">Pointer to the [**ITMedia**](itmedia.md) interface for the desired item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4c50-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a4c50-113">Return value</span></span>

<span data-ttu-id="a4c50-114">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="a4c50-114">This method can return one of these values.</span></span>



| <span data-ttu-id="a4c50-115">Значение</span><span class="sxs-lookup"><span data-stu-id="a4c50-115">Value</span></span>                                                                                         | <span data-ttu-id="a4c50-116">Значение</span><span class="sxs-lookup"><span data-stu-id="a4c50-116">Meaning</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="a4c50-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="a4c50-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="a4c50-118">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="a4c50-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="a4c50-119"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="a4c50-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="a4c50-120">Параметр *Pval* не является допустимым указателем.</span><span class="sxs-lookup"><span data-stu-id="a4c50-120">The *pVal* parameter is not a valid pointer.</span></span><br/>         |
| <dl> <span data-ttu-id="a4c50-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="a4c50-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="a4c50-122">Недопустимый параметр *индекса* .</span><span class="sxs-lookup"><span data-stu-id="a4c50-122">The *Index* parameter is not valid.</span></span><br/>                  |
| <dl> <span data-ttu-id="a4c50-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="a4c50-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="a4c50-124">Недостаточно памяти для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="a4c50-124">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="a4c50-125"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="a4c50-125"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="a4c50-126">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="a4c50-126">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="a4c50-127"><dt>**E \_ нотимпл**</dt></span><span class="sxs-lookup"><span data-stu-id="a4c50-127"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="a4c50-128">Этот метод еще не реализован.</span><span class="sxs-lookup"><span data-stu-id="a4c50-128">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="a4c50-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a4c50-129">Remarks</span></span>

<span data-ttu-id="a4c50-130">Большинство списков C и C++ основаны на 0, но этот индекс основан на 1 для Visual Basic совместимости, то есть первый элемент имеет номер индекса 1.</span><span class="sxs-lookup"><span data-stu-id="a4c50-130">Most C and C++ lists are 0-based, but this index is 1-based for Visual Basic compatibility, meaning the first item has an index number of 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4c50-131">Требования</span><span class="sxs-lookup"><span data-stu-id="a4c50-131">Requirements</span></span>



| <span data-ttu-id="a4c50-132">Требование</span><span class="sxs-lookup"><span data-stu-id="a4c50-132">Requirement</span></span> | <span data-ttu-id="a4c50-133">Значение</span><span class="sxs-lookup"><span data-stu-id="a4c50-133">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a4c50-134">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="a4c50-134">TAPI version</span></span><br/> | <span data-ttu-id="a4c50-135">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="a4c50-135">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="a4c50-136">Header</span><span class="sxs-lookup"><span data-stu-id="a4c50-136">Header</span></span><br/>       | <dl> <span data-ttu-id="a4c50-137"><dt>Сдпблб. h</dt></span><span class="sxs-lookup"><span data-stu-id="a4c50-137"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="a4c50-138">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a4c50-138">Library</span></span><br/>      | <dl> <span data-ttu-id="a4c50-139"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a4c50-139"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="a4c50-140">DLL</span><span class="sxs-lookup"><span data-stu-id="a4c50-140">DLL</span></span><br/>          | <dl> <span data-ttu-id="a4c50-141"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a4c50-141"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4c50-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a4c50-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4c50-143">**итмедиа**</span><span class="sxs-lookup"><span data-stu-id="a4c50-143">**ITMedia**</span></span>](itmedia.md)
</dt> <dt>

[<span data-ttu-id="a4c50-144">**итмедиаколлектион**</span><span class="sxs-lookup"><span data-stu-id="a4c50-144">**ITMediaCollection**</span></span>](itmediacollection.md)
</dt> </dl>

 

 




