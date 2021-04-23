---
description: Метод получения \_ подсчета возвращает количество атрибутов.
ms.assetid: dc607f09-4cca-4ef0-8b86-dbc5e6edcfdd
title: 'Метод Итаттрибутелист:: get_Count (Сдпблб. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 634996e8d920005f5da4c40b6cfca3f5cb632363
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679882"
---
# <a name="itattributelistget_count-method"></a><span data-ttu-id="5d13a-103">Метод Итаттрибутелист:: Get \_ Count</span><span class="sxs-lookup"><span data-stu-id="5d13a-103">ITAttributeList::get\_Count method</span></span>

<span data-ttu-id="5d13a-104">\[ В Windows Vista, Windows Server 2008 и последующих версиях операционной системы нельзя использовать встречные средства и элементы управления Конференц-телефонией и интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="5d13a-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="5d13a-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="5d13a-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="5d13a-106">Метод **получения \_ подсчета** возвращает количество атрибутов.</span><span class="sxs-lookup"><span data-stu-id="5d13a-106">The **get\_Count** method gets the number of attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d13a-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5d13a-107">Syntax</span></span>


```C++
HRESULT get_Count(
  [out] LONG *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="5d13a-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="5d13a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d13a-109">*Pval* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="5d13a-109">*pVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5d13a-110">Количество атрибутов в списке.</span><span class="sxs-lookup"><span data-stu-id="5d13a-110">Count of the attributes in the list.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d13a-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5d13a-111">Return value</span></span>

<span data-ttu-id="5d13a-112">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="5d13a-112">This method can return one of these values.</span></span>



| <span data-ttu-id="5d13a-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="5d13a-113">Return code</span></span>                                                                                   | <span data-ttu-id="5d13a-114">Описание</span><span class="sxs-lookup"><span data-stu-id="5d13a-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="5d13a-115"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="5d13a-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="5d13a-116">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="5d13a-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="5d13a-117"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="5d13a-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="5d13a-118">Параметр *Pval* не является допустимым указателем.</span><span class="sxs-lookup"><span data-stu-id="5d13a-118">The *pVal* parameter is not a valid pointer.</span></span><br/>         |
| <dl> <span data-ttu-id="5d13a-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="5d13a-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="5d13a-120">Недостаточно памяти для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="5d13a-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="5d13a-121"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="5d13a-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="5d13a-122">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="5d13a-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="5d13a-123"><dt>**E \_ нотимпл**</dt></span><span class="sxs-lookup"><span data-stu-id="5d13a-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="5d13a-124">Этот метод еще не реализован.</span><span class="sxs-lookup"><span data-stu-id="5d13a-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="5d13a-125">Требования</span><span class="sxs-lookup"><span data-stu-id="5d13a-125">Requirements</span></span>



| <span data-ttu-id="5d13a-126">Требование</span><span class="sxs-lookup"><span data-stu-id="5d13a-126">Requirement</span></span> | <span data-ttu-id="5d13a-127">Значение</span><span class="sxs-lookup"><span data-stu-id="5d13a-127">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5d13a-128">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="5d13a-128">TAPI version</span></span><br/> | <span data-ttu-id="5d13a-129">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="5d13a-129">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="5d13a-130">Header</span><span class="sxs-lookup"><span data-stu-id="5d13a-130">Header</span></span><br/>       | <dl> <span data-ttu-id="5d13a-131"><dt>Сдпблб. h</dt></span><span class="sxs-lookup"><span data-stu-id="5d13a-131"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="5d13a-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5d13a-132">Library</span></span><br/>      | <dl> <span data-ttu-id="5d13a-133"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5d13a-133"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="5d13a-134">DLL</span><span class="sxs-lookup"><span data-stu-id="5d13a-134">DLL</span></span><br/>          | <dl> <span data-ttu-id="5d13a-135"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5d13a-135"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d13a-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5d13a-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d13a-137">**итаттрибутелист**</span><span class="sxs-lookup"><span data-stu-id="5d13a-137">**ITAttributeList**</span></span>](itattributelist.md)
</dt> </dl>

 

 




