---
description: Метод Get \_ стартаддресс получает первый адрес, который будет использоваться для сеанса.
ms.assetid: 3c4fec19-1b7d-4052-afd8-7aaf095907d0
title: 'Метод Итконнектион:: get_StartAddress (Сдпблб. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84266d1874e7d04acb594bcfb9d99b440b0390b2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685322"
---
# <a name="itconnectionget_startaddress-method"></a><span data-ttu-id="1c1ee-103">Метод Итконнектион:: Get \_ стартаддресс</span><span class="sxs-lookup"><span data-stu-id="1c1ee-103">ITConnection::get\_StartAddress method</span></span>

<span data-ttu-id="1c1ee-104">\[ В Windows Vista, Windows Server 2008 и последующих версиях операционной системы нельзя использовать встречные средства и элементы управления Конференц-телефонией и интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="1c1ee-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="1c1ee-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="1c1ee-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="1c1ee-106">Метод **Get \_ стартаддресс** получает первый адрес, который будет использоваться для сеанса.</span><span class="sxs-lookup"><span data-stu-id="1c1ee-106">The **get\_StartAddress** method gets the first address to be used for the session.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c1ee-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1c1ee-107">Syntax</span></span>


```C++
HRESULT get_StartAddress(
  [out] BSTR *ppStartAddress
);
```



## <a name="parameters"></a><span data-ttu-id="1c1ee-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="1c1ee-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c1ee-109">*ппстартаддресс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="1c1ee-109">*ppStartAddress* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1c1ee-110">Указатель на **строку BSTR** , содержащую начальный адрес сеанса.</span><span class="sxs-lookup"><span data-stu-id="1c1ee-110">Pointer to a **BSTR** containing the starting address for the session.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c1ee-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1c1ee-111">Return value</span></span>

<span data-ttu-id="1c1ee-112">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="1c1ee-112">This method can return one of these values.</span></span>



| <span data-ttu-id="1c1ee-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="1c1ee-113">Return code</span></span>                                                                                   | <span data-ttu-id="1c1ee-114">Описание</span><span class="sxs-lookup"><span data-stu-id="1c1ee-114">Description</span></span>                                                       |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <dl> <span data-ttu-id="1c1ee-115"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="1c1ee-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="1c1ee-116">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="1c1ee-116">Method succeeded.</span></span><br/>                                      |
| <dl> <span data-ttu-id="1c1ee-117"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="1c1ee-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="1c1ee-118">Параметр *ппстартаддресс* не является допустимым указателем.</span><span class="sxs-lookup"><span data-stu-id="1c1ee-118">The *ppStartAddress* parameter is not a valid pointer.</span></span><br/> |
| <dl> <span data-ttu-id="1c1ee-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="1c1ee-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="1c1ee-120">Недостаточно памяти для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="1c1ee-120">Insufficient memory exists to perform the operation.</span></span><br/>   |
| <dl> <span data-ttu-id="1c1ee-121"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="1c1ee-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="1c1ee-122">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="1c1ee-122">Unspecified error.</span></span><br/>                                     |
| <dl> <span data-ttu-id="1c1ee-123"><dt>**E \_ нотимпл**</dt></span><span class="sxs-lookup"><span data-stu-id="1c1ee-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="1c1ee-124">Этот метод еще не реализован.</span><span class="sxs-lookup"><span data-stu-id="1c1ee-124">This method is not yet implemented.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="1c1ee-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1c1ee-125">Remarks</span></span>

<span data-ttu-id="1c1ee-126">Приложение должно использовать [**сисфристринг**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) для освобождения памяти, выделенной для параметра *ппстартаддресс* .</span><span class="sxs-lookup"><span data-stu-id="1c1ee-126">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory allocated for the *ppStartAddress* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c1ee-127">Требования</span><span class="sxs-lookup"><span data-stu-id="1c1ee-127">Requirements</span></span>



| <span data-ttu-id="1c1ee-128">Требование</span><span class="sxs-lookup"><span data-stu-id="1c1ee-128">Requirement</span></span> | <span data-ttu-id="1c1ee-129">Значение</span><span class="sxs-lookup"><span data-stu-id="1c1ee-129">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1c1ee-130">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="1c1ee-130">TAPI version</span></span><br/> | <span data-ttu-id="1c1ee-131">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="1c1ee-131">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="1c1ee-132">Header</span><span class="sxs-lookup"><span data-stu-id="1c1ee-132">Header</span></span><br/>       | <dl> <span data-ttu-id="1c1ee-133"><dt>Сдпблб. h</dt></span><span class="sxs-lookup"><span data-stu-id="1c1ee-133"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="1c1ee-134">Библиотека</span><span class="sxs-lookup"><span data-stu-id="1c1ee-134">Library</span></span><br/>      | <dl> <span data-ttu-id="1c1ee-135"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1c1ee-135"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="1c1ee-136">DLL</span><span class="sxs-lookup"><span data-stu-id="1c1ee-136">DLL</span></span><br/>          | <dl> <span data-ttu-id="1c1ee-137"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1c1ee-137"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c1ee-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1c1ee-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c1ee-139">**итконнектион**</span><span class="sxs-lookup"><span data-stu-id="1c1ee-139">**ITConnection**</span></span>](itconnection.md)
</dt> </dl>

 

