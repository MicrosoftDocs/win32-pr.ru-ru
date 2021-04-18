---
description: Метод Get \_ addressType получает тип адреса.
ms.assetid: b2ff6303-6beb-429c-ad1a-2f729749e5db
title: 'Метод Итконнектион:: get_AddressType (Сдпблб. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d015b0b395f0219fa9a7af2ca7002f242cfaa1b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675517"
---
# <a name="itconnectionget_addresstype-method"></a><span data-ttu-id="6c8d4-103">Метод Итконнектион:: Get \_ addressType</span><span class="sxs-lookup"><span data-stu-id="6c8d4-103">ITConnection::get\_AddressType method</span></span>

<span data-ttu-id="6c8d4-104">\[ В Windows Vista, Windows Server 2008 и последующих версиях операционной системы нельзя использовать встречные средства и элементы управления Конференц-телефонией и интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="6c8d4-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="6c8d4-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="6c8d4-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="6c8d4-106">Метод **Get \_ addressType** получает тип адреса.</span><span class="sxs-lookup"><span data-stu-id="6c8d4-106">The **get\_AddressType** method gets the address type.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c8d4-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6c8d4-107">Syntax</span></span>


```C++
HRESULT get_AddressType(
  [out] BSTR *ppAddressType
);
```



## <a name="parameters"></a><span data-ttu-id="6c8d4-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="6c8d4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c8d4-109">*ппаддресстипе* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="6c8d4-109">*ppAddressType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6c8d4-110">Указатель на **строку BSTR** , содержащую тип адреса.</span><span class="sxs-lookup"><span data-stu-id="6c8d4-110">Pointer to a **BSTR** containing the address type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c8d4-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6c8d4-111">Return value</span></span>

<span data-ttu-id="6c8d4-112">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="6c8d4-112">This method can return one of these values.</span></span>



| <span data-ttu-id="6c8d4-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="6c8d4-113">Return code</span></span>                                                                                   | <span data-ttu-id="6c8d4-114">Описание</span><span class="sxs-lookup"><span data-stu-id="6c8d4-114">Description</span></span>                                                      |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <span data-ttu-id="6c8d4-115"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="6c8d4-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="6c8d4-116">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="6c8d4-116">Method succeeded.</span></span><br/>                                     |
| <dl> <span data-ttu-id="6c8d4-117"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="6c8d4-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="6c8d4-118">Параметр *ппаддресстипе* не является допустимым указателем.</span><span class="sxs-lookup"><span data-stu-id="6c8d4-118">The *ppAddressType* parameter is not a valid pointer.</span></span><br/> |
| <dl> <span data-ttu-id="6c8d4-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="6c8d4-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="6c8d4-120">Недостаточно памяти для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="6c8d4-120">Insufficient memory exists to perform the operation.</span></span><br/>  |
| <dl> <span data-ttu-id="6c8d4-121"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="6c8d4-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="6c8d4-122">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="6c8d4-122">Unspecified error.</span></span><br/>                                    |
| <dl> <span data-ttu-id="6c8d4-123"><dt>**E \_ нотимпл**</dt></span><span class="sxs-lookup"><span data-stu-id="6c8d4-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="6c8d4-124">Этот метод еще не реализован.</span><span class="sxs-lookup"><span data-stu-id="6c8d4-124">This method is not yet implemented.</span></span><br/>                   |



 

## <a name="remarks"></a><span data-ttu-id="6c8d4-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6c8d4-125">Remarks</span></span>

<span data-ttu-id="6c8d4-126">Приложение должно использовать [**сисфристринг**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) для освобождения памяти, выделенной для параметра *ппаддресстипе* .</span><span class="sxs-lookup"><span data-stu-id="6c8d4-126">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory allocated for the *ppAddressType* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c8d4-127">Требования</span><span class="sxs-lookup"><span data-stu-id="6c8d4-127">Requirements</span></span>



| <span data-ttu-id="6c8d4-128">Требование</span><span class="sxs-lookup"><span data-stu-id="6c8d4-128">Requirement</span></span> | <span data-ttu-id="6c8d4-129">Значение</span><span class="sxs-lookup"><span data-stu-id="6c8d4-129">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6c8d4-130">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="6c8d4-130">TAPI version</span></span><br/> | <span data-ttu-id="6c8d4-131">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="6c8d4-131">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="6c8d4-132">Header</span><span class="sxs-lookup"><span data-stu-id="6c8d4-132">Header</span></span><br/>       | <dl> <span data-ttu-id="6c8d4-133"><dt>Сдпблб. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c8d4-133"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="6c8d4-134">Библиотека</span><span class="sxs-lookup"><span data-stu-id="6c8d4-134">Library</span></span><br/>      | <dl> <span data-ttu-id="6c8d4-135"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6c8d4-135"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="6c8d4-136">DLL</span><span class="sxs-lookup"><span data-stu-id="6c8d4-136">DLL</span></span><br/>          | <dl> <span data-ttu-id="6c8d4-137"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6c8d4-137"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c8d4-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6c8d4-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c8d4-139">**итконнектион**</span><span class="sxs-lookup"><span data-stu-id="6c8d4-139">**ITConnection**</span></span>](itconnection.md)
</dt> <dt>

[<span data-ttu-id="6c8d4-140">**Итконнектион::p \_ addressType**</span><span class="sxs-lookup"><span data-stu-id="6c8d4-140">**ITConnection::put\_AddressType**</span></span>](itconnection-put-addresstype.md)
</dt> </dl>

 

