---
description: Метод Get \_ нетворктипе получает тип сети.
ms.assetid: 5597284a-9cc6-422b-a064-cda25aa5964b
title: 'Метод Итконнектион:: get_NetworkType (Сдпблб. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31189ec0e3b42e3ed249cd0c62365b1f8c793908
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685325"
---
# <a name="itconnectionget_networktype-method"></a><span data-ttu-id="ad142-103">Метод Итконнектион:: Get \_ нетворктипе</span><span class="sxs-lookup"><span data-stu-id="ad142-103">ITConnection::get\_NetworkType method</span></span>

<span data-ttu-id="ad142-104">\[ В Windows Vista, Windows Server 2008 и последующих версиях операционной системы нельзя использовать встречные средства и элементы управления Конференц-телефонией и интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="ad142-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="ad142-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="ad142-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="ad142-106">Метод **Get \_ нетворктипе** получает тип сети.</span><span class="sxs-lookup"><span data-stu-id="ad142-106">The **get\_NetworkType** method gets the network type.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad142-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ad142-107">Syntax</span></span>


```C++
HRESULT get_NetworkType(
  [out] BSTR *ppNetworkType
);
```



## <a name="parameters"></a><span data-ttu-id="ad142-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="ad142-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad142-109">*ппнетворктипе* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="ad142-109">*ppNetworkType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ad142-110">Указатель на **строку BSTR** , содержащую тип сети.</span><span class="sxs-lookup"><span data-stu-id="ad142-110">Pointer to a **BSTR** containing the network type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad142-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ad142-111">Return value</span></span>

<span data-ttu-id="ad142-112">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="ad142-112">This method can return one of these values.</span></span>



| <span data-ttu-id="ad142-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="ad142-113">Return code</span></span>                                                                                   | <span data-ttu-id="ad142-114">Описание</span><span class="sxs-lookup"><span data-stu-id="ad142-114">Description</span></span>                                                      |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <span data-ttu-id="ad142-115"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="ad142-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="ad142-116">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="ad142-116">Method succeeded.</span></span><br/>                                     |
| <dl> <span data-ttu-id="ad142-117"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="ad142-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="ad142-118">Параметр *ппнетворктипе* не является допустимым указателем.</span><span class="sxs-lookup"><span data-stu-id="ad142-118">The *ppNetworkType* parameter is not a valid pointer.</span></span><br/> |
| <dl> <span data-ttu-id="ad142-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="ad142-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="ad142-120">Недостаточно памяти для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="ad142-120">Insufficient memory exists to perform the operation.</span></span><br/>  |
| <dl> <span data-ttu-id="ad142-121"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="ad142-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="ad142-122">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="ad142-122">Unspecified error.</span></span><br/>                                    |
| <dl> <span data-ttu-id="ad142-123"><dt>**E \_ нотимпл**</dt></span><span class="sxs-lookup"><span data-stu-id="ad142-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="ad142-124">Этот метод еще не реализован.</span><span class="sxs-lookup"><span data-stu-id="ad142-124">This method is not yet implemented.</span></span><br/>                   |



 

## <a name="remarks"></a><span data-ttu-id="ad142-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ad142-125">Remarks</span></span>

<span data-ttu-id="ad142-126">Приложение должно использовать [**сисфристринг**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) для освобождения памяти, выделенной для параметра *ппнетворктипе* .</span><span class="sxs-lookup"><span data-stu-id="ad142-126">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory allocated for the *ppNetworkType* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad142-127">Требования</span><span class="sxs-lookup"><span data-stu-id="ad142-127">Requirements</span></span>



| <span data-ttu-id="ad142-128">Требование</span><span class="sxs-lookup"><span data-stu-id="ad142-128">Requirement</span></span> | <span data-ttu-id="ad142-129">Значение</span><span class="sxs-lookup"><span data-stu-id="ad142-129">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ad142-130">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="ad142-130">TAPI version</span></span><br/> | <span data-ttu-id="ad142-131">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="ad142-131">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="ad142-132">Header</span><span class="sxs-lookup"><span data-stu-id="ad142-132">Header</span></span><br/>       | <dl> <span data-ttu-id="ad142-133"><dt>Сдпблб. h</dt></span><span class="sxs-lookup"><span data-stu-id="ad142-133"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="ad142-134">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ad142-134">Library</span></span><br/>      | <dl> <span data-ttu-id="ad142-135"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ad142-135"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="ad142-136">DLL</span><span class="sxs-lookup"><span data-stu-id="ad142-136">DLL</span></span><br/>          | <dl> <span data-ttu-id="ad142-137"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ad142-137"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad142-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ad142-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad142-139">**итконнектион**</span><span class="sxs-lookup"><span data-stu-id="ad142-139">**ITConnection**</span></span>](itconnection.md)
</dt> <dt>

[<span data-ttu-id="ad142-140">**Итконнектион::p UT \_ нетворктипе**</span><span class="sxs-lookup"><span data-stu-id="ad142-140">**ITConnection::put\_NetworkType**</span></span>](itconnection-put-networktype.md)
</dt> </dl>

 

