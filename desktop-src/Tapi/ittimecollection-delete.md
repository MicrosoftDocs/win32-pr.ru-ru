---
description: Метод Delete удаляет компонент Иттиме.
ms.assetid: 0445d659-7b83-4462-b199-511fd8270f32
title: Иттимеколлектион::D удалить метод (Сдпблб. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9aad562660a2d563193e5074b52f4d1a513bb39
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685354"
---
# <a name="ittimecollectiondelete-method"></a><span data-ttu-id="ae6a8-103">Иттимеколлектион::D удалить метод</span><span class="sxs-lookup"><span data-stu-id="ae6a8-103">ITTimeCollection::Delete method</span></span>

<span data-ttu-id="ae6a8-104">\[ В Windows Vista, Windows Server 2008 и последующих версиях операционной системы нельзя использовать встречные средства и элементы управления Конференц-телефонией и интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="ae6a8-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="ae6a8-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="ae6a8-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="ae6a8-106">Метод **Delete** удаляет компонент [**иттиме**](ittime.md) .</span><span class="sxs-lookup"><span data-stu-id="ae6a8-106">The **Delete** method deletes an [**ITTime**](ittime.md) component.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae6a8-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ae6a8-107">Syntax</span></span>


```C++
HRESULT Delete(
  [in] LONG Index
);
```



## <a name="parameters"></a><span data-ttu-id="ae6a8-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="ae6a8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae6a8-109">*Индекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ae6a8-109">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae6a8-110">Индекс удаляемого компонента [**иттиме**](ittime.md) .</span><span class="sxs-lookup"><span data-stu-id="ae6a8-110">Index of the [**ITTime**](ittime.md) component to be deleted.</span></span> <span data-ttu-id="ae6a8-111">(Индексный массив основан на единицах.)</span><span class="sxs-lookup"><span data-stu-id="ae6a8-111">(The index array is one-based.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae6a8-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ae6a8-112">Return value</span></span>

<span data-ttu-id="ae6a8-113">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="ae6a8-113">This method can return one of these values.</span></span>



| <span data-ttu-id="ae6a8-114">Значение</span><span class="sxs-lookup"><span data-stu-id="ae6a8-114">Value</span></span>                                                                                         | <span data-ttu-id="ae6a8-115">Значение</span><span class="sxs-lookup"><span data-stu-id="ae6a8-115">Meaning</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="ae6a8-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="ae6a8-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="ae6a8-117">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="ae6a8-117">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="ae6a8-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="ae6a8-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="ae6a8-119">Недопустимый параметр *индекса* .</span><span class="sxs-lookup"><span data-stu-id="ae6a8-119">The *Index* parameter is not valid.</span></span><br/>                  |
| <dl> <span data-ttu-id="ae6a8-120"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="ae6a8-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="ae6a8-121">Недостаточно памяти для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="ae6a8-121">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="ae6a8-122"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="ae6a8-122"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="ae6a8-123">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="ae6a8-123">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="ae6a8-124"><dt>**E \_ нотимпл**</dt></span><span class="sxs-lookup"><span data-stu-id="ae6a8-124"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="ae6a8-125">Этот метод еще не реализован.</span><span class="sxs-lookup"><span data-stu-id="ae6a8-125">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="ae6a8-126">Требования</span><span class="sxs-lookup"><span data-stu-id="ae6a8-126">Requirements</span></span>



| <span data-ttu-id="ae6a8-127">Требование</span><span class="sxs-lookup"><span data-stu-id="ae6a8-127">Requirement</span></span> | <span data-ttu-id="ae6a8-128">Значение</span><span class="sxs-lookup"><span data-stu-id="ae6a8-128">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ae6a8-129">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="ae6a8-129">TAPI version</span></span><br/> | <span data-ttu-id="ae6a8-130">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="ae6a8-130">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="ae6a8-131">Header</span><span class="sxs-lookup"><span data-stu-id="ae6a8-131">Header</span></span><br/>       | <dl> <span data-ttu-id="ae6a8-132"><dt>Сдпблб. h</dt></span><span class="sxs-lookup"><span data-stu-id="ae6a8-132"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="ae6a8-133">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ae6a8-133">Library</span></span><br/>      | <dl> <span data-ttu-id="ae6a8-134"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ae6a8-134"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="ae6a8-135">DLL</span><span class="sxs-lookup"><span data-stu-id="ae6a8-135">DLL</span></span><br/>          | <dl> <span data-ttu-id="ae6a8-136"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ae6a8-136"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ae6a8-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ae6a8-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae6a8-138">**иттимеколлектион**</span><span class="sxs-lookup"><span data-stu-id="ae6a8-138">**ITTimeCollection**</span></span>](ittimecollection.md)
</dt> <dt>

[<span data-ttu-id="ae6a8-139">**иттиме**</span><span class="sxs-lookup"><span data-stu-id="ae6a8-139">**ITTime**</span></span>](ittime.md)
</dt> </dl>

 

 




