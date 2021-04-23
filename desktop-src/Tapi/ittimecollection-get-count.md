---
description: Метод получения \_ подсчета возвращает количество элементов в коллекции.
ms.assetid: 9fe96af3-bb7b-4f6c-8df2-85bf7850c527
title: 'Метод Иттимеколлектион:: get_Count (Сдпблб. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a385c8fa3120cbeaa4b876a8af4f60e0df5cb48
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685352"
---
# <a name="ittimecollectionget_count-method"></a><span data-ttu-id="90b5e-103">Метод Иттимеколлектион:: Get \_ Count</span><span class="sxs-lookup"><span data-stu-id="90b5e-103">ITTimeCollection::get\_Count method</span></span>

<span data-ttu-id="90b5e-104">\[ В Windows Vista, Windows Server 2008 и последующих версиях операционной системы нельзя использовать встречные средства и элементы управления Конференц-телефонией и интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="90b5e-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="90b5e-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="90b5e-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="90b5e-106">Метод **получения \_ подсчета** возвращает количество элементов в коллекции.</span><span class="sxs-lookup"><span data-stu-id="90b5e-106">The **get\_Count** method gets the number of items in the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="90b5e-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="90b5e-107">Syntax</span></span>


```C++
HRESULT get_Count(
  [out] LONG *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="90b5e-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="90b5e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90b5e-109">*Pval* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="90b5e-109">*pVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="90b5e-110">Указатель на число элементов в коллекции.</span><span class="sxs-lookup"><span data-stu-id="90b5e-110">Pointer to the number of items in the collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90b5e-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="90b5e-111">Return value</span></span>

<span data-ttu-id="90b5e-112">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="90b5e-112">This method can return one of these values.</span></span>



| <span data-ttu-id="90b5e-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="90b5e-113">Return code</span></span>                                                                                   | <span data-ttu-id="90b5e-114">Описание</span><span class="sxs-lookup"><span data-stu-id="90b5e-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="90b5e-115"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="90b5e-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="90b5e-116">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="90b5e-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="90b5e-117"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="90b5e-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="90b5e-118">Параметр *Pval* не является допустимым указателем.</span><span class="sxs-lookup"><span data-stu-id="90b5e-118">The *pVal* parameter is not a valid pointer.</span></span><br/>         |
| <dl> <span data-ttu-id="90b5e-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="90b5e-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="90b5e-120">Недостаточно памяти для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="90b5e-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="90b5e-121"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="90b5e-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="90b5e-122">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="90b5e-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="90b5e-123"><dt>**E \_ нотимпл**</dt></span><span class="sxs-lookup"><span data-stu-id="90b5e-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="90b5e-124">Этот метод еще не реализован.</span><span class="sxs-lookup"><span data-stu-id="90b5e-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="90b5e-125">Требования</span><span class="sxs-lookup"><span data-stu-id="90b5e-125">Requirements</span></span>



| <span data-ttu-id="90b5e-126">Требование</span><span class="sxs-lookup"><span data-stu-id="90b5e-126">Requirement</span></span> | <span data-ttu-id="90b5e-127">Значение</span><span class="sxs-lookup"><span data-stu-id="90b5e-127">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="90b5e-128">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="90b5e-128">TAPI version</span></span><br/> | <span data-ttu-id="90b5e-129">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="90b5e-129">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="90b5e-130">Header</span><span class="sxs-lookup"><span data-stu-id="90b5e-130">Header</span></span><br/>       | <dl> <span data-ttu-id="90b5e-131"><dt>Сдпблб. h</dt></span><span class="sxs-lookup"><span data-stu-id="90b5e-131"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="90b5e-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="90b5e-132">Library</span></span><br/>      | <dl> <span data-ttu-id="90b5e-133"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="90b5e-133"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="90b5e-134">DLL</span><span class="sxs-lookup"><span data-stu-id="90b5e-134">DLL</span></span><br/>          | <dl> <span data-ttu-id="90b5e-135"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="90b5e-135"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="90b5e-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="90b5e-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90b5e-137">**иттимеколлектион**</span><span class="sxs-lookup"><span data-stu-id="90b5e-137">**ITTimeCollection**</span></span>](ittimecollection.md)
</dt> <dt>

[<span data-ttu-id="90b5e-138">**иттиме**</span><span class="sxs-lookup"><span data-stu-id="90b5e-138">**ITTime**</span></span>](ittime.md)
</dt> </dl>

 

 




