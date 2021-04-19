---
description: Метод получения \_ подсчета возвращает количество носителей в сеансе.
ms.assetid: 9d085a34-9a49-4447-8d11-56d71a2a3592
title: 'Метод Итмедиаколлектион:: get_Count (Сдпблб. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1f5a4fb6d7f1b942f37aae1356c7b49e0e60f77
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675941"
---
# <a name="itmediacollectionget_count-method"></a><span data-ttu-id="5ba00-103">Метод Итмедиаколлектион:: Get \_ Count</span><span class="sxs-lookup"><span data-stu-id="5ba00-103">ITMediaCollection::get\_Count method</span></span>

<span data-ttu-id="5ba00-104">\[ В Windows Vista, Windows Server 2008 и последующих версиях операционной системы нельзя использовать встречные средства и элементы управления Конференц-телефонией и интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="5ba00-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="5ba00-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="5ba00-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="5ba00-106">Метод **получения \_ подсчета** возвращает количество носителей в сеансе.</span><span class="sxs-lookup"><span data-stu-id="5ba00-106">The **get\_Count** method gets the number of media in the session.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ba00-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5ba00-107">Syntax</span></span>


```C++
HRESULT get_Count(
  [out] LONG *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="5ba00-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="5ba00-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ba00-109">*Pval* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="5ba00-109">*pVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5ba00-110">Число носителей в сеансе.</span><span class="sxs-lookup"><span data-stu-id="5ba00-110">Count of media in the session.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ba00-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5ba00-111">Return value</span></span>

<span data-ttu-id="5ba00-112">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="5ba00-112">This method can return one of these values.</span></span>



| <span data-ttu-id="5ba00-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="5ba00-113">Return code</span></span>                                                                                   | <span data-ttu-id="5ba00-114">Описание</span><span class="sxs-lookup"><span data-stu-id="5ba00-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="5ba00-115"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="5ba00-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="5ba00-116">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="5ba00-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="5ba00-117"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="5ba00-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="5ba00-118">Параметр *Pval* не является допустимым указателем.</span><span class="sxs-lookup"><span data-stu-id="5ba00-118">The *pVal* parameter is not a valid pointer.</span></span><br/>         |
| <dl> <span data-ttu-id="5ba00-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="5ba00-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="5ba00-120">Недостаточно памяти для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="5ba00-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="5ba00-121"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="5ba00-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="5ba00-122">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="5ba00-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="5ba00-123"><dt>**E \_ нотимпл**</dt></span><span class="sxs-lookup"><span data-stu-id="5ba00-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="5ba00-124">Этот метод еще не реализован.</span><span class="sxs-lookup"><span data-stu-id="5ba00-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="5ba00-125">Требования</span><span class="sxs-lookup"><span data-stu-id="5ba00-125">Requirements</span></span>



| <span data-ttu-id="5ba00-126">Требование</span><span class="sxs-lookup"><span data-stu-id="5ba00-126">Requirement</span></span> | <span data-ttu-id="5ba00-127">Значение</span><span class="sxs-lookup"><span data-stu-id="5ba00-127">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5ba00-128">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="5ba00-128">TAPI version</span></span><br/> | <span data-ttu-id="5ba00-129">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="5ba00-129">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="5ba00-130">Header</span><span class="sxs-lookup"><span data-stu-id="5ba00-130">Header</span></span><br/>       | <dl> <span data-ttu-id="5ba00-131"><dt>Сдпблб. h</dt></span><span class="sxs-lookup"><span data-stu-id="5ba00-131"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="5ba00-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5ba00-132">Library</span></span><br/>      | <dl> <span data-ttu-id="5ba00-133"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5ba00-133"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="5ba00-134">DLL</span><span class="sxs-lookup"><span data-stu-id="5ba00-134">DLL</span></span><br/>          | <dl> <span data-ttu-id="5ba00-135"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5ba00-135"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ba00-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5ba00-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ba00-137">**итмедиаколлектион**</span><span class="sxs-lookup"><span data-stu-id="5ba00-137">**ITMediaCollection**</span></span>](itmediacollection.md)
</dt> </dl>

 

 




