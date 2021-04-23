---
description: Метод Create создает новый носитель со свойствами по умолчанию, добавляет его в коллекцию по указанному индексу и возвращает указатель на интерфейс Итмедиа.
ms.assetid: f0036556-d2e7-4589-8bb4-e2c5559902fe
title: 'Метод Итмедиаколлектион:: Create (Сдпблб. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8033fb2f541f5451f918845858df756b32361f54
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689400"
---
# <a name="itmediacollectioncreate-method"></a><span data-ttu-id="fe3eb-103">Метод Итмедиаколлектион:: Create</span><span class="sxs-lookup"><span data-stu-id="fe3eb-103">ITMediaCollection::Create method</span></span>

<span data-ttu-id="fe3eb-104">\[ В Windows Vista, Windows Server 2008 и последующих версиях операционной системы нельзя использовать встречные средства и элементы управления Конференц-телефонией и интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="fe3eb-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="fe3eb-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="fe3eb-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="fe3eb-106">Метод **CREATE** создает новый носитель со свойствами по умолчанию, добавляет его в коллекцию по указанному индексу и возвращает указатель на интерфейс [**итмедиа**](itmedia.md) .</span><span class="sxs-lookup"><span data-stu-id="fe3eb-106">The **Create** method creates a new media with default properties, adds it to the collection at the specified index, and returns a pointer to the [**ITMedia**](itmedia.md) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe3eb-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fe3eb-107">Syntax</span></span>


```C++
HRESULT Create(
  [in]  LONG    Index,
  [out] ITMedia **ppMedia
);
```



## <a name="parameters"></a><span data-ttu-id="fe3eb-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="fe3eb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe3eb-109">*Индекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fe3eb-109">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe3eb-110">Индекс для нового элемента.</span><span class="sxs-lookup"><span data-stu-id="fe3eb-110">Index for the new item.</span></span> <span data-ttu-id="fe3eb-111">Минимальное значение индекса равно 1, а максимальное значение индекса — текущее число элементов + 1.</span><span class="sxs-lookup"><span data-stu-id="fe3eb-111">The minimum value for the index is 1, and the maximum value for the index is the current number of items + 1.</span></span>

</dd> <dt>

<span data-ttu-id="fe3eb-112">*ппмедиа* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="fe3eb-112">*ppMedia* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fe3eb-113">Создан указатель на интерфейс [**итмедиа**](itmedia.md) .</span><span class="sxs-lookup"><span data-stu-id="fe3eb-113">Pointer to [**ITMedia**](itmedia.md) interface created.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe3eb-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fe3eb-114">Return value</span></span>

<span data-ttu-id="fe3eb-115">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="fe3eb-115">This method can return one of these values.</span></span>



| <span data-ttu-id="fe3eb-116">Значение</span><span class="sxs-lookup"><span data-stu-id="fe3eb-116">Value</span></span>                                                                                         | <span data-ttu-id="fe3eb-117">Значение</span><span class="sxs-lookup"><span data-stu-id="fe3eb-117">Meaning</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="fe3eb-118"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="fe3eb-118"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="fe3eb-119">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="fe3eb-119">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="fe3eb-120"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="fe3eb-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="fe3eb-121">Параметр *ппмедиа* не является допустимым указателем.</span><span class="sxs-lookup"><span data-stu-id="fe3eb-121">The *ppMedia* parameter is not a valid pointer.</span></span><br/>      |
| <dl> <span data-ttu-id="fe3eb-122"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="fe3eb-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="fe3eb-123">Недопустимый параметр *индекса* .</span><span class="sxs-lookup"><span data-stu-id="fe3eb-123">The *Index* parameter is not valid.</span></span><br/>                  |
| <dl> <span data-ttu-id="fe3eb-124"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="fe3eb-124"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="fe3eb-125">Недостаточно памяти для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="fe3eb-125">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="fe3eb-126"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="fe3eb-126"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="fe3eb-127">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="fe3eb-127">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="fe3eb-128"><dt>**E \_ нотимпл**</dt></span><span class="sxs-lookup"><span data-stu-id="fe3eb-128"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="fe3eb-129">Этот метод еще не реализован.</span><span class="sxs-lookup"><span data-stu-id="fe3eb-129">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="fe3eb-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fe3eb-130">Remarks</span></span>

<span data-ttu-id="fe3eb-131">Большинство списков C и C++ основаны на 0, но этот индекс основан на 1 для Visual Basic совместимости, то есть первый элемент имеет номер индекса 1.</span><span class="sxs-lookup"><span data-stu-id="fe3eb-131">Most C and C++ lists are 0-based, but this index is 1-based for Visual Basic compatibility, meaning the first item has an index number of 1.</span></span>

<span data-ttu-id="fe3eb-132">TAPI вызывает метод **AddRef** в интерфейсе [**итмедиа**](itmedia.md) , возвращенном методом **итмедиаколлектион:: Create**.</span><span class="sxs-lookup"><span data-stu-id="fe3eb-132">TAPI calls the **AddRef** method on the [**ITMedia**](itmedia.md) interface returned by **ITMediaCollection::Create**.</span></span> <span data-ttu-id="fe3eb-133">Приложение должно вызвать **выпуск** в интерфейсе [**итмедиа**](itmedia.md) , чтобы освободить ресурсы, связанные с ним.</span><span class="sxs-lookup"><span data-stu-id="fe3eb-133">The application must call **Release** on the [**ITMedia**](itmedia.md) interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe3eb-134">Требования</span><span class="sxs-lookup"><span data-stu-id="fe3eb-134">Requirements</span></span>



| <span data-ttu-id="fe3eb-135">Требование</span><span class="sxs-lookup"><span data-stu-id="fe3eb-135">Requirement</span></span> | <span data-ttu-id="fe3eb-136">Значение</span><span class="sxs-lookup"><span data-stu-id="fe3eb-136">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fe3eb-137">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="fe3eb-137">TAPI version</span></span><br/> | <span data-ttu-id="fe3eb-138">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="fe3eb-138">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="fe3eb-139">Header</span><span class="sxs-lookup"><span data-stu-id="fe3eb-139">Header</span></span><br/>       | <dl> <span data-ttu-id="fe3eb-140"><dt>Сдпблб. h</dt></span><span class="sxs-lookup"><span data-stu-id="fe3eb-140"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="fe3eb-141">Библиотека</span><span class="sxs-lookup"><span data-stu-id="fe3eb-141">Library</span></span><br/>      | <dl> <span data-ttu-id="fe3eb-142"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fe3eb-142"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="fe3eb-143">DLL</span><span class="sxs-lookup"><span data-stu-id="fe3eb-143">DLL</span></span><br/>          | <dl> <span data-ttu-id="fe3eb-144"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fe3eb-144"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe3eb-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fe3eb-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe3eb-146">**итмедиа**</span><span class="sxs-lookup"><span data-stu-id="fe3eb-146">**ITMedia**</span></span>](itmedia.md)
</dt> <dt>

[<span data-ttu-id="fe3eb-147">**итмедиаколлектион**</span><span class="sxs-lookup"><span data-stu-id="fe3eb-147">**ITMediaCollection**</span></span>](itmediacollection.md)
</dt> </dl>

 

 




