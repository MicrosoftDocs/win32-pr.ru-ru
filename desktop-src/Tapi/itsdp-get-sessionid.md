---
description: Метод Get \_ SessionID получает значение 32-битного протокола NTP (сетевого времени), которое служит идентификатором сеанса. Создается автоматически при создании сеанса.
ms.assetid: 5177f120-4b93-40bc-9481-aedf65a8dee9
title: 'Метод Итсдп:: get_SessionId (Сдпблб. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ad593b61f4c935a220e59383ae170569f04af54
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105688754"
---
# <a name="itsdpget_sessionid-method"></a><span data-ttu-id="f0d13-104">Метод Итсдп:: Get \_ SessionID</span><span class="sxs-lookup"><span data-stu-id="f0d13-104">ITSdp::get\_SessionId method</span></span>

<span data-ttu-id="f0d13-105">\[ В Windows Vista, Windows Server 2008 и последующих версиях операционной системы нельзя использовать встречные средства и элементы управления Конференц-телефонией и интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="f0d13-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="f0d13-106">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="f0d13-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="f0d13-107">Метод **Get \_ SessionID** получает значение 32-битного протокола NTP (сетевого времени), которое служит идентификатором сеанса.</span><span class="sxs-lookup"><span data-stu-id="f0d13-107">The **get\_SessionId** method gets the 32-bit NTP (Network Time Protocol) value that serves as the session identifier.</span></span> <span data-ttu-id="f0d13-108">Создается автоматически при создании сеанса.</span><span class="sxs-lookup"><span data-stu-id="f0d13-108">This is generated automatically when the session is created.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0d13-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f0d13-109">Syntax</span></span>


```C++
HRESULT get_SessionId(
  [out] DOUBLE *pSessionId
);
```



## <a name="parameters"></a><span data-ttu-id="f0d13-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="f0d13-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0d13-111">*псессионид* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="f0d13-111">*pSessionId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f0d13-112">Указатель на идентификатор сеанса.</span><span class="sxs-lookup"><span data-stu-id="f0d13-112">Pointer to the session identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0d13-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f0d13-113">Return value</span></span>

<span data-ttu-id="f0d13-114">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="f0d13-114">This method can return one of these values.</span></span>



| <span data-ttu-id="f0d13-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="f0d13-115">Return code</span></span>                                                                                   | <span data-ttu-id="f0d13-116">Описание</span><span class="sxs-lookup"><span data-stu-id="f0d13-116">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="f0d13-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="f0d13-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="f0d13-118">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="f0d13-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="f0d13-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="f0d13-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="f0d13-120">Недопустимый параметр *псессионид* .</span><span class="sxs-lookup"><span data-stu-id="f0d13-120">The *pSessionId* parameter is not valid.</span></span><br/>             |
| <dl> <span data-ttu-id="f0d13-121"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="f0d13-121"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="f0d13-122">Параметр *псессионид* не является допустимым указателем.</span><span class="sxs-lookup"><span data-stu-id="f0d13-122">The *pSessionId* parameter is not a valid pointer.</span></span><br/>   |
| <dl> <span data-ttu-id="f0d13-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="f0d13-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="f0d13-124">Недостаточно памяти для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="f0d13-124">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="f0d13-125"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="f0d13-125"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="f0d13-126">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="f0d13-126">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="f0d13-127"><dt>**E \_ нотимпл**</dt></span><span class="sxs-lookup"><span data-stu-id="f0d13-127"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="f0d13-128">Этот метод еще не реализован.</span><span class="sxs-lookup"><span data-stu-id="f0d13-128">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="f0d13-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f0d13-129">Remarks</span></span>

<span data-ttu-id="f0d13-130">Возвращаемое значение этого метода может быть **ulong**, но Visual Basic не поддерживает тип **ulong** .</span><span class="sxs-lookup"><span data-stu-id="f0d13-130">The return value of this method could be **ULONG**, but Visual Basic doesn't support the **ULONG** type.</span></span> <span data-ttu-id="f0d13-131">**Double** — это следующий наименьший тип, охватывающий весь диапазон требуемых значений.</span><span class="sxs-lookup"><span data-stu-id="f0d13-131">A **DOUBLE** is the next smallest type that encompasses the entire range of values required.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0d13-132">Требования</span><span class="sxs-lookup"><span data-stu-id="f0d13-132">Requirements</span></span>



| <span data-ttu-id="f0d13-133">Требование</span><span class="sxs-lookup"><span data-stu-id="f0d13-133">Requirement</span></span> | <span data-ttu-id="f0d13-134">Значение</span><span class="sxs-lookup"><span data-stu-id="f0d13-134">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f0d13-135">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="f0d13-135">TAPI version</span></span><br/> | <span data-ttu-id="f0d13-136">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="f0d13-136">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="f0d13-137">Header</span><span class="sxs-lookup"><span data-stu-id="f0d13-137">Header</span></span><br/>       | <dl> <span data-ttu-id="f0d13-138"><dt>Сдпблб. h</dt></span><span class="sxs-lookup"><span data-stu-id="f0d13-138"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="f0d13-139">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f0d13-139">Library</span></span><br/>      | <dl> <span data-ttu-id="f0d13-140"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f0d13-140"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="f0d13-141">DLL</span><span class="sxs-lookup"><span data-stu-id="f0d13-141">DLL</span></span><br/>          | <dl> <span data-ttu-id="f0d13-142"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f0d13-142"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0d13-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f0d13-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0d13-144">**итсдп**</span><span class="sxs-lookup"><span data-stu-id="f0d13-144">**ITSdp**</span></span>](itsdp.md)
</dt> </dl>

 

 




