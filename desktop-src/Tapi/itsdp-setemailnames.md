---
description: Метод Сетемаилнамес задает массив адресов электронной почты, связанных с объектом Conference.
ms.assetid: 1d6d5b01-bc0f-455f-8b23-bc0f409afde4
title: 'Метод Итсдп:: Сетемаилнамес (Сдпблб. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9ff31e66f5f69fe7fad43da5ec436c3f567cd49
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105688948"
---
# <a name="itsdpsetemailnames-method"></a><span data-ttu-id="43a17-103">Метод Итсдп:: Сетемаилнамес</span><span class="sxs-lookup"><span data-stu-id="43a17-103">ITSdp::SetEmailNames method</span></span>

<span data-ttu-id="43a17-104">\[ В Windows Vista, Windows Server 2008 и последующих версиях операционной системы нельзя использовать встречные средства и элементы управления Конференц-телефонией и интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="43a17-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="43a17-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="43a17-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="43a17-106">Метод **сетемаилнамес** задает массив адресов электронной почты, связанных с объектом Conference.</span><span class="sxs-lookup"><span data-stu-id="43a17-106">The **SetEmailNames** method sets an array of e-mail addresses associated with the conference blob.</span></span>

## <a name="syntax"></a><span data-ttu-id="43a17-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="43a17-107">Syntax</span></span>


```C++
HRESULT SetEmailNames(
  [in] VARIANT Addresses,
  [in] VARIANT Names
);
```



## <a name="parameters"></a><span data-ttu-id="43a17-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="43a17-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43a17-109">*Адреса* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="43a17-109">*Addresses* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43a17-110">Список адресов электронной почты в МАССИВе SAFEARRAY из **BSTR**.</span><span class="sxs-lookup"><span data-stu-id="43a17-110">SAFEARRAY of **BSTR** s listing e-mail addresses.</span></span>

</dd> <dt>

<span data-ttu-id="43a17-111">*Имена* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="43a17-111">*Names* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43a17-112">**Массив SafeArray с именами**.</span><span class="sxs-lookup"><span data-stu-id="43a17-112">SAFEARRAY of **BSTR** s listing names.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43a17-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="43a17-113">Return value</span></span>

<span data-ttu-id="43a17-114">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="43a17-114">This method can return one of these values.</span></span>



| <span data-ttu-id="43a17-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="43a17-115">Return code</span></span>                                                                                   | <span data-ttu-id="43a17-116">Описание</span><span class="sxs-lookup"><span data-stu-id="43a17-116">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="43a17-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="43a17-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="43a17-118">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="43a17-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="43a17-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="43a17-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="43a17-120">Недопустимый параметр *addresses* или *names* .</span><span class="sxs-lookup"><span data-stu-id="43a17-120">The *Addresses* or *Names* parameter is not valid.</span></span><br/>   |
| <dl> <span data-ttu-id="43a17-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="43a17-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="43a17-122">Недостаточно памяти для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="43a17-122">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="43a17-123"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="43a17-123"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="43a17-124">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="43a17-124">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="43a17-125"><dt>**E \_ нотимпл**</dt></span><span class="sxs-lookup"><span data-stu-id="43a17-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="43a17-126">Этот метод еще не реализован.</span><span class="sxs-lookup"><span data-stu-id="43a17-126">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="43a17-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="43a17-127">Remarks</span></span>

<span data-ttu-id="43a17-128">Списки, на которые указывают *адреса* и *имена* , имеют одинаковую длину.</span><span class="sxs-lookup"><span data-stu-id="43a17-128">The lists that *Addresses* and *Names* point to are the same length.</span></span>

## <a name="requirements"></a><span data-ttu-id="43a17-129">Требования</span><span class="sxs-lookup"><span data-stu-id="43a17-129">Requirements</span></span>



| <span data-ttu-id="43a17-130">Требование</span><span class="sxs-lookup"><span data-stu-id="43a17-130">Requirement</span></span> | <span data-ttu-id="43a17-131">Значение</span><span class="sxs-lookup"><span data-stu-id="43a17-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="43a17-132">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="43a17-132">TAPI version</span></span><br/> | <span data-ttu-id="43a17-133">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="43a17-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="43a17-134">Header</span><span class="sxs-lookup"><span data-stu-id="43a17-134">Header</span></span><br/>       | <dl> <span data-ttu-id="43a17-135"><dt>Сдпблб. h</dt></span><span class="sxs-lookup"><span data-stu-id="43a17-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="43a17-136">Библиотека</span><span class="sxs-lookup"><span data-stu-id="43a17-136">Library</span></span><br/>      | <dl> <span data-ttu-id="43a17-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="43a17-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="43a17-138">DLL</span><span class="sxs-lookup"><span data-stu-id="43a17-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="43a17-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="43a17-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43a17-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="43a17-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43a17-141">**итсдп**</span><span class="sxs-lookup"><span data-stu-id="43a17-141">**ITSdp**</span></span>](itsdp.md)
</dt> </dl>

 

 




