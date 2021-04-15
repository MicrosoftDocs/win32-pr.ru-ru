---
description: Метод Сетфоненумберс задает массив номеров телефонов, связанных с объектом Conference.
ms.assetid: 674c08df-7e91-4f19-9d65-4bc6e7af117b
title: 'Метод Итсдп:: Сетфоненумберс (Сдпблб. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30ec2820d8d033ac2eed9d9287c3ca52c9deb316
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675764"
---
# <a name="itsdpsetphonenumbers-method"></a><span data-ttu-id="1a3d7-103">Метод Итсдп:: Сетфоненумберс</span><span class="sxs-lookup"><span data-stu-id="1a3d7-103">ITSdp::SetPhoneNumbers method</span></span>

<span data-ttu-id="1a3d7-104">\[ В Windows Vista, Windows Server 2008 и последующих версиях операционной системы нельзя использовать встречные средства и элементы управления Конференц-телефонией и интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="1a3d7-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="1a3d7-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="1a3d7-106">Метод **сетфоненумберс** задает массив номеров телефонов, связанных с объектом Conference.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-106">The **SetPhoneNumbers** method sets an array of phone numbers associated with a conference blob.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a3d7-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1a3d7-107">Syntax</span></span>


```C++
HRESULT SetPhoneNumbers(
  [in] VARIANT Numbers,
  [in] VARIANT Names
);
```



## <a name="parameters"></a><span data-ttu-id="1a3d7-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="1a3d7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a3d7-109">*Число* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1a3d7-109">*Numbers* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a3d7-110">Список номеров телефонов в МАССИВе SAFEARRAY из **BSTR**.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-110">SAFEARRAY of **BSTR** s listing phone numbers.</span></span>

</dd> <dt>

<span data-ttu-id="1a3d7-111">*Имена* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1a3d7-111">*Names* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a3d7-112">**Массив SafeArray с именами**.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-112">SAFEARRAY of **BSTR** s listing names.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a3d7-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1a3d7-113">Return value</span></span>

<span data-ttu-id="1a3d7-114">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-114">This method can return one of these values.</span></span>



| <span data-ttu-id="1a3d7-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="1a3d7-115">Return code</span></span>                                                                                   | <span data-ttu-id="1a3d7-116">Описание</span><span class="sxs-lookup"><span data-stu-id="1a3d7-116">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="1a3d7-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="1a3d7-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="1a3d7-118">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="1a3d7-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="1a3d7-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="1a3d7-120">Недопустимый параметр *numbers* или *names* .</span><span class="sxs-lookup"><span data-stu-id="1a3d7-120">The *Numbers* or *Names* parameter is not valid.</span></span><br/>     |
| <dl> <span data-ttu-id="1a3d7-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="1a3d7-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="1a3d7-122">Недостаточно памяти для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-122">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="1a3d7-123"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="1a3d7-123"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="1a3d7-124">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-124">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="1a3d7-125"><dt>**E \_ нотимпл**</dt></span><span class="sxs-lookup"><span data-stu-id="1a3d7-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="1a3d7-126">Этот метод еще не реализован.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-126">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="1a3d7-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1a3d7-127">Remarks</span></span>

<span data-ttu-id="1a3d7-128">Списки, на которые указывают *числа* и *имена* , имеют одинаковую длину.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-128">The lists that *Numbers* and *Names* point to are the same length.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a3d7-129">Требования</span><span class="sxs-lookup"><span data-stu-id="1a3d7-129">Requirements</span></span>



| <span data-ttu-id="1a3d7-130">Требование</span><span class="sxs-lookup"><span data-stu-id="1a3d7-130">Requirement</span></span> | <span data-ttu-id="1a3d7-131">Значение</span><span class="sxs-lookup"><span data-stu-id="1a3d7-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1a3d7-132">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="1a3d7-132">TAPI version</span></span><br/> | <span data-ttu-id="1a3d7-133">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="1a3d7-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="1a3d7-134">Header</span><span class="sxs-lookup"><span data-stu-id="1a3d7-134">Header</span></span><br/>       | <dl> <span data-ttu-id="1a3d7-135"><dt>Сдпблб. h</dt></span><span class="sxs-lookup"><span data-stu-id="1a3d7-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="1a3d7-136">Библиотека</span><span class="sxs-lookup"><span data-stu-id="1a3d7-136">Library</span></span><br/>      | <dl> <span data-ttu-id="1a3d7-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1a3d7-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="1a3d7-138">DLL</span><span class="sxs-lookup"><span data-stu-id="1a3d7-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="1a3d7-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1a3d7-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a3d7-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1a3d7-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a3d7-141">**итсдп**</span><span class="sxs-lookup"><span data-stu-id="1a3d7-141">**ITSdp**</span></span>](itsdp.md)
</dt> </dl>

 

 




