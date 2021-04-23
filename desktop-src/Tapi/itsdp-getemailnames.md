---
description: Метод Жетемаилнамес возвращает массив имен электронной почты, связанных с объектом Conference.
ms.assetid: e51f25d7-41e5-408e-930b-396c7ac24437
title: 'Метод Итсдп:: Жетемаилнамес (Сдпблб. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31f0200b5cc6ea0422f47a323cd1c57d7e0f9a5d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685122"
---
# <a name="itsdpgetemailnames-method"></a><span data-ttu-id="42a9b-103">Метод Итсдп:: Жетемаилнамес</span><span class="sxs-lookup"><span data-stu-id="42a9b-103">ITSdp::GetEmailNames method</span></span>

<span data-ttu-id="42a9b-104">\[ В Windows Vista, Windows Server 2008 и последующих версиях операционной системы нельзя использовать встречные средства и элементы управления Конференц-телефонией и интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="42a9b-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="42a9b-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="42a9b-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="42a9b-106">Метод **жетемаилнамес** возвращает массив имен электронной почты, связанных с объектом Conference.</span><span class="sxs-lookup"><span data-stu-id="42a9b-106">The **GetEmailNames** method gets an array of e-mail names associated with the conference blob.</span></span>

## <a name="syntax"></a><span data-ttu-id="42a9b-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="42a9b-107">Syntax</span></span>


```C++
HRESULT GetEmailNames(
  [out] VARIANT *pAddresses,
  [out] VARIANT *pNames
);
```



## <a name="parameters"></a><span data-ttu-id="42a9b-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="42a9b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42a9b-109">*паддрессес* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="42a9b-109">*pAddresses* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="42a9b-110">Указатель на **вариант** для массива SAFEARRAY из массива типа данных ( **BSTR**) с перечнем адресов электронной почты.</span><span class="sxs-lookup"><span data-stu-id="42a9b-110">**VARIANT** pointer to a SAFEARRAY of **BSTR** s listing e-mail addresses.</span></span>

</dd> <dt>

<span data-ttu-id="42a9b-111">*пнамес* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="42a9b-111">*pNames* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="42a9b-112">Указатель **Variant** на массив **SAFEARRAY с именами**.</span><span class="sxs-lookup"><span data-stu-id="42a9b-112">**VARIANT** pointer to a SAFEARRAY of **BSTR** s listing names.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42a9b-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="42a9b-113">Return value</span></span>

<span data-ttu-id="42a9b-114">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="42a9b-114">This method can return one of these values.</span></span>



| <span data-ttu-id="42a9b-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="42a9b-115">Return code</span></span>                                                                                   | <span data-ttu-id="42a9b-116">Описание</span><span class="sxs-lookup"><span data-stu-id="42a9b-116">Description</span></span>                                                               |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="42a9b-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="42a9b-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="42a9b-118">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="42a9b-118">Method succeeded.</span></span><br/>                                              |
| <dl> <span data-ttu-id="42a9b-119"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="42a9b-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="42a9b-120">Параметр *паддрессес* или *пнамес* не является допустимым указателем.</span><span class="sxs-lookup"><span data-stu-id="42a9b-120">The *pAddresses* or *pNames* parameter is not a valid pointer.</span></span><br/> |
| <dl> <span data-ttu-id="42a9b-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="42a9b-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="42a9b-122">Недостаточно памяти для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="42a9b-122">Insufficient memory exists to perform the operation.</span></span><br/>           |
| <dl> <span data-ttu-id="42a9b-123"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="42a9b-123"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="42a9b-124">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="42a9b-124">Unspecified error.</span></span><br/>                                             |
| <dl> <span data-ttu-id="42a9b-125"><dt>**E \_ нотимпл**</dt></span><span class="sxs-lookup"><span data-stu-id="42a9b-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="42a9b-126">Этот метод еще не реализован.</span><span class="sxs-lookup"><span data-stu-id="42a9b-126">This method is not yet implemented.</span></span><br/>                            |



 

## <a name="remarks"></a><span data-ttu-id="42a9b-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="42a9b-127">Remarks</span></span>

<span data-ttu-id="42a9b-128">Списки, на которые указывает *паддрессес* и *пнамес* , имеют одинаковую длину.</span><span class="sxs-lookup"><span data-stu-id="42a9b-128">The lists that *pAddresses* and *pNames* point to are the same length.</span></span>

## <a name="requirements"></a><span data-ttu-id="42a9b-129">Требования</span><span class="sxs-lookup"><span data-stu-id="42a9b-129">Requirements</span></span>



| <span data-ttu-id="42a9b-130">Требование</span><span class="sxs-lookup"><span data-stu-id="42a9b-130">Requirement</span></span> | <span data-ttu-id="42a9b-131">Значение</span><span class="sxs-lookup"><span data-stu-id="42a9b-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="42a9b-132">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="42a9b-132">TAPI version</span></span><br/> | <span data-ttu-id="42a9b-133">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="42a9b-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="42a9b-134">Header</span><span class="sxs-lookup"><span data-stu-id="42a9b-134">Header</span></span><br/>       | <dl> <span data-ttu-id="42a9b-135"><dt>Сдпблб. h</dt></span><span class="sxs-lookup"><span data-stu-id="42a9b-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="42a9b-136">Библиотека</span><span class="sxs-lookup"><span data-stu-id="42a9b-136">Library</span></span><br/>      | <dl> <span data-ttu-id="42a9b-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="42a9b-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="42a9b-138">DLL</span><span class="sxs-lookup"><span data-stu-id="42a9b-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="42a9b-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="42a9b-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42a9b-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="42a9b-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42a9b-141">**итсдп**</span><span class="sxs-lookup"><span data-stu-id="42a9b-141">**ITSdp**</span></span>](itsdp.md)
</dt> </dl>

 

 




