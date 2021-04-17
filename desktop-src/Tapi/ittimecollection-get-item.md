---
description: Метод Get \_ Item получает элемент из коллекции с помощью индекса.
ms.assetid: 7401ae21-190d-479c-aebc-51bf8a953b94
title: 'Метод Иттимеколлектион:: get_Item (Сдпблб. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68b9dec40070ff3abddce0e425300f6d805c1cc9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675274"
---
# <a name="ittimecollectionget_item-method"></a><span data-ttu-id="1e714-103">Метод Иттимеколлектион:: Get \_ Item</span><span class="sxs-lookup"><span data-stu-id="1e714-103">ITTimeCollection::get\_Item method</span></span>

<span data-ttu-id="1e714-104">\[ В Windows Vista, Windows Server 2008 и последующих версиях операционной системы нельзя использовать встречные средства и элементы управления Конференц-телефонией и интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="1e714-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="1e714-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="1e714-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="1e714-106">Метод **Get \_ Item** получает элемент из коллекции с помощью индекса.</span><span class="sxs-lookup"><span data-stu-id="1e714-106">The **get\_Item** method gets an item from the collection using an index.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e714-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1e714-107">Syntax</span></span>


```C++
HRESULT get_Item(
  [in]  LONG   Index,
  [out] ITTime **pVal
);
```



## <a name="parameters"></a><span data-ttu-id="1e714-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="1e714-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e714-109">*Индекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1e714-109">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e714-110">Индекс получаемого элемента.</span><span class="sxs-lookup"><span data-stu-id="1e714-110">Index of the item to get.</span></span>

</dd> <dt>

<span data-ttu-id="1e714-111">*Pval* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="1e714-111">*pVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1e714-112">Указатель на требуемый интерфейс [**иттиме**](ittime.md) .</span><span class="sxs-lookup"><span data-stu-id="1e714-112">Pointer to [**ITTime**](ittime.md) desired interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e714-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1e714-113">Return value</span></span>

<span data-ttu-id="1e714-114">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="1e714-114">This method can return one of these values.</span></span>



| <span data-ttu-id="1e714-115">Значение</span><span class="sxs-lookup"><span data-stu-id="1e714-115">Value</span></span>                                                                                         | <span data-ttu-id="1e714-116">Значение</span><span class="sxs-lookup"><span data-stu-id="1e714-116">Meaning</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="1e714-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="1e714-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="1e714-118">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="1e714-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="1e714-119"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="1e714-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="1e714-120">Параметр *Pval* не является допустимым указателем.</span><span class="sxs-lookup"><span data-stu-id="1e714-120">The *pVal* parameter is not a valid pointer.</span></span><br/>         |
| <dl> <span data-ttu-id="1e714-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="1e714-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="1e714-122">Недопустимый параметр *индекса* .</span><span class="sxs-lookup"><span data-stu-id="1e714-122">The *Index* parameter is not valid.</span></span><br/>                  |
| <dl> <span data-ttu-id="1e714-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="1e714-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="1e714-124">Недостаточно памяти для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="1e714-124">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="1e714-125"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="1e714-125"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="1e714-126">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="1e714-126">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="1e714-127"><dt>**E \_ нотимпл**</dt></span><span class="sxs-lookup"><span data-stu-id="1e714-127"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="1e714-128">Этот метод еще не реализован.</span><span class="sxs-lookup"><span data-stu-id="1e714-128">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="1e714-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1e714-129">Remarks</span></span>

<span data-ttu-id="1e714-130">TAPI вызывает метод **AddRef** для интерфейса [**иттиме**](ittime.md) , возвращенного I **ттимеколлектион:: Get \_ Item**.</span><span class="sxs-lookup"><span data-stu-id="1e714-130">TAPI calls the **AddRef** method on the [**ITTime**](ittime.md) interface returned by I **TTimeCollection::get\_Item**.</span></span> <span data-ttu-id="1e714-131">Приложение должно вызвать **выпуск** в интерфейсе **иттиме** , чтобы освободить ресурсы, связанные с ним.</span><span class="sxs-lookup"><span data-stu-id="1e714-131">The application must call **Release** on the **ITTime** interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e714-132">Требования</span><span class="sxs-lookup"><span data-stu-id="1e714-132">Requirements</span></span>



| <span data-ttu-id="1e714-133">Требование</span><span class="sxs-lookup"><span data-stu-id="1e714-133">Requirement</span></span> | <span data-ttu-id="1e714-134">Значение</span><span class="sxs-lookup"><span data-stu-id="1e714-134">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1e714-135">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="1e714-135">TAPI version</span></span><br/> | <span data-ttu-id="1e714-136">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="1e714-136">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="1e714-137">Header</span><span class="sxs-lookup"><span data-stu-id="1e714-137">Header</span></span><br/>       | <dl> <span data-ttu-id="1e714-138"><dt>Сдпблб. h</dt></span><span class="sxs-lookup"><span data-stu-id="1e714-138"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="1e714-139">Библиотека</span><span class="sxs-lookup"><span data-stu-id="1e714-139">Library</span></span><br/>      | <dl> <span data-ttu-id="1e714-140"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1e714-140"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="1e714-141">DLL</span><span class="sxs-lookup"><span data-stu-id="1e714-141">DLL</span></span><br/>          | <dl> <span data-ttu-id="1e714-142"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1e714-142"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e714-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1e714-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e714-144">**иттимеколлектион**</span><span class="sxs-lookup"><span data-stu-id="1e714-144">**ITTimeCollection**</span></span>](ittimecollection.md)
</dt> <dt>

[<span data-ttu-id="1e714-145">**иттиме**</span><span class="sxs-lookup"><span data-stu-id="1e714-145">**ITTime**</span></span>](ittime.md)
</dt> </dl>

 

 




