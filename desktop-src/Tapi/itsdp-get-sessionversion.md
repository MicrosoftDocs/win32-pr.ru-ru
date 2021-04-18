---
description: Метод Get \_ сессионверсион получает значение 32-bit (идеальное сетевое время или NTP), которое служит версией сеанса.
ms.assetid: 39c2aef4-24e3-4ea0-8b23-dff842f9ab84
title: 'Метод Итсдп:: get_SessionVersion (Сдпблб. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3466844f3f21f54ec0ec76a3569e7af25e4b0143
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680113"
---
# <a name="itsdpget_sessionversion-method"></a><span data-ttu-id="101a2-103">Метод Итсдп:: Get \_ сессионверсион</span><span class="sxs-lookup"><span data-stu-id="101a2-103">ITSdp::get\_SessionVersion method</span></span>

<span data-ttu-id="101a2-104">\[ В Windows Vista, Windows Server 2008 и последующих версиях операционной системы нельзя использовать встречные средства и элементы управления Конференц-телефонией и интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="101a2-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="101a2-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="101a2-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="101a2-106">Метод **Get \_ сессионверсион** получает значение 32-bit (идеальное сетевое время или NTP), которое служит версией сеанса.</span><span class="sxs-lookup"><span data-stu-id="101a2-106">The **get\_SessionVersion** method gets the 32-bit (ideally Network Time Protocol, or NTP) value that serves as the session version.</span></span> <span data-ttu-id="101a2-107">Хотя это автоматически создается при создании сеанса, пользователь несет ответственность за его изменение при изменении SDP.</span><span class="sxs-lookup"><span data-stu-id="101a2-107">Although this is generated automatically when the session is created, the user is responsible for changing it when the SDP is modified.</span></span>

## <a name="syntax"></a><span data-ttu-id="101a2-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="101a2-108">Syntax</span></span>


```C++
HRESULT get_SessionVersion(
  [out] DOUBLE *pSessionVersion
);
```



## <a name="parameters"></a><span data-ttu-id="101a2-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="101a2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="101a2-110">*псессионверсион* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="101a2-110">*pSessionVersion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="101a2-111">Указатель на идентификатор версии сеанса.</span><span class="sxs-lookup"><span data-stu-id="101a2-111">Pointer to the session version identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="101a2-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="101a2-112">Return value</span></span>

<span data-ttu-id="101a2-113">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="101a2-113">This method can return one of these values.</span></span>



| <span data-ttu-id="101a2-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="101a2-114">Return code</span></span>                                                                                   | <span data-ttu-id="101a2-115">Описание</span><span class="sxs-lookup"><span data-stu-id="101a2-115">Description</span></span>                                                        |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="101a2-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="101a2-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="101a2-117">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="101a2-117">Method succeeded.</span></span><br/>                                       |
| <dl> <span data-ttu-id="101a2-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="101a2-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="101a2-119">Недопустимый параметр *псессионверсион* .</span><span class="sxs-lookup"><span data-stu-id="101a2-119">The *pSessionVersion* parameter is not valid.</span></span><br/>           |
| <dl> <span data-ttu-id="101a2-120"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="101a2-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="101a2-121">Параметр *псессионверсион* не является допустимым указателем.</span><span class="sxs-lookup"><span data-stu-id="101a2-121">The *pSessionVersion* parameter is not a valid pointer.</span></span><br/> |
| <dl> <span data-ttu-id="101a2-122"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="101a2-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="101a2-123">Недостаточно памяти для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="101a2-123">Insufficient memory exists to perform the operation.</span></span><br/>    |
| <dl> <span data-ttu-id="101a2-124"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="101a2-124"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="101a2-125">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="101a2-125">Unspecified error.</span></span><br/>                                      |
| <dl> <span data-ttu-id="101a2-126"><dt>**E \_ нотимпл**</dt></span><span class="sxs-lookup"><span data-stu-id="101a2-126"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="101a2-127">Этот метод еще не реализован.</span><span class="sxs-lookup"><span data-stu-id="101a2-127">This method is not yet implemented.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="101a2-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="101a2-128">Remarks</span></span>

<span data-ttu-id="101a2-129">Возвращаемое значение этого метода может быть **ulong**, но Visual Basic не поддерживает тип **ulong** .</span><span class="sxs-lookup"><span data-stu-id="101a2-129">The return value of this method could be **ULONG**, but Visual Basic doesn't support the **ULONG** type.</span></span> <span data-ttu-id="101a2-130">**Double** — это следующий наименьший тип, охватывающий весь диапазон требуемых значений.</span><span class="sxs-lookup"><span data-stu-id="101a2-130">A **DOUBLE** is the next smallest type that encompasses the entire range of values required.</span></span>

## <a name="requirements"></a><span data-ttu-id="101a2-131">Требования</span><span class="sxs-lookup"><span data-stu-id="101a2-131">Requirements</span></span>



| <span data-ttu-id="101a2-132">Требование</span><span class="sxs-lookup"><span data-stu-id="101a2-132">Requirement</span></span> | <span data-ttu-id="101a2-133">Значение</span><span class="sxs-lookup"><span data-stu-id="101a2-133">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="101a2-134">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="101a2-134">TAPI version</span></span><br/> | <span data-ttu-id="101a2-135">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="101a2-135">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="101a2-136">Header</span><span class="sxs-lookup"><span data-stu-id="101a2-136">Header</span></span><br/>       | <dl> <span data-ttu-id="101a2-137"><dt>Сдпблб. h</dt></span><span class="sxs-lookup"><span data-stu-id="101a2-137"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="101a2-138">Библиотека</span><span class="sxs-lookup"><span data-stu-id="101a2-138">Library</span></span><br/>      | <dl> <span data-ttu-id="101a2-139"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="101a2-139"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="101a2-140">DLL</span><span class="sxs-lookup"><span data-stu-id="101a2-140">DLL</span></span><br/>          | <dl> <span data-ttu-id="101a2-141"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="101a2-141"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="101a2-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="101a2-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="101a2-143">**итсдп**</span><span class="sxs-lookup"><span data-stu-id="101a2-143">**ITSdp**</span></span>](itsdp.md)
</dt> <dt>

[<span data-ttu-id="101a2-144">**Итсдп::p UT \_ сессионверсион**</span><span class="sxs-lookup"><span data-stu-id="101a2-144">**ITSdp::put\_SessionVersion**</span></span>](itsdp-put-sessionversion.md)
</dt> </dl>

 

 




