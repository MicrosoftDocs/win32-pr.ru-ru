---
description: Метод Get \_ IsValid проверяет наличие протокола дескриптора сеанса (см. RFC 2327) большого двоичного объекта для значений структуры и поля.
ms.assetid: a3f849ac-bda9-4937-bf3b-bce8df20cbf0
title: 'Метод Итсдп:: get_IsValid (Сдпблб. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88ca3cfdc1061e0a2830010ec39b2e6667c9341c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680050"
---
# <a name="itsdpget_isvalid-method"></a><span data-ttu-id="14db7-103">Метод Итсдп:: Get \_ IsValid</span><span class="sxs-lookup"><span data-stu-id="14db7-103">ITSdp::get\_IsValid method</span></span>

<span data-ttu-id="14db7-104">\[ В Windows Vista, Windows Server 2008 и последующих версиях операционной системы нельзя использовать встречные средства и элементы управления Конференц-телефонией и интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="14db7-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="14db7-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="14db7-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="14db7-106">Метод **Get \_ IsValid** проверяет наличие протокола дескриптора сеанса (см. RFC 2327) большого двоичного объекта для значений структуры и поля.</span><span class="sxs-lookup"><span data-stu-id="14db7-106">The **get\_IsValid** method validates the Session Descriptor Protocol (SDP; see RFC 2327) blob for structure and field values.</span></span>

## <a name="syntax"></a><span data-ttu-id="14db7-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="14db7-107">Syntax</span></span>


```C++
HRESULT get_IsValid(
  [out] VARIANT_BOOL *pfIsValid
);
```



## <a name="parameters"></a><span data-ttu-id="14db7-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="14db7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14db7-109">*пфисвалид* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="14db7-109">*pfIsValid* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="14db7-110">Указывает, допустима ли структура большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="14db7-110">Indicates whether the blob structure is valid.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14db7-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="14db7-111">Return value</span></span>

<span data-ttu-id="14db7-112">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="14db7-112">This method can return one of these values.</span></span>



| <span data-ttu-id="14db7-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="14db7-113">Return code</span></span>                                                                                   | <span data-ttu-id="14db7-114">Описание</span><span class="sxs-lookup"><span data-stu-id="14db7-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="14db7-115"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="14db7-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="14db7-116">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="14db7-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="14db7-117"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="14db7-117"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="14db7-118">Недопустимый параметр *пфисвалид* .</span><span class="sxs-lookup"><span data-stu-id="14db7-118">The *pfIsValid* parameter is not valid.</span></span><br/>              |
| <dl> <span data-ttu-id="14db7-119"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="14db7-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="14db7-120">Параметр *пфисвалид* не является допустимым указателем.</span><span class="sxs-lookup"><span data-stu-id="14db7-120">The *pfIsValid* parameter is not a valid pointer.</span></span><br/>    |
| <dl> <span data-ttu-id="14db7-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="14db7-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="14db7-122">Недостаточно памяти для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="14db7-122">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="14db7-123"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="14db7-123"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="14db7-124">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="14db7-124">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="14db7-125"><dt>**E \_ нотимпл**</dt></span><span class="sxs-lookup"><span data-stu-id="14db7-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="14db7-126">Этот метод еще не реализован.</span><span class="sxs-lookup"><span data-stu-id="14db7-126">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="14db7-127">Требования</span><span class="sxs-lookup"><span data-stu-id="14db7-127">Requirements</span></span>



| <span data-ttu-id="14db7-128">Требование</span><span class="sxs-lookup"><span data-stu-id="14db7-128">Requirement</span></span> | <span data-ttu-id="14db7-129">Значение</span><span class="sxs-lookup"><span data-stu-id="14db7-129">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="14db7-130">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="14db7-130">TAPI version</span></span><br/> | <span data-ttu-id="14db7-131">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="14db7-131">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="14db7-132">Header</span><span class="sxs-lookup"><span data-stu-id="14db7-132">Header</span></span><br/>       | <dl> <span data-ttu-id="14db7-133"><dt>Сдпблб. h</dt></span><span class="sxs-lookup"><span data-stu-id="14db7-133"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="14db7-134">Библиотека</span><span class="sxs-lookup"><span data-stu-id="14db7-134">Library</span></span><br/>      | <dl> <span data-ttu-id="14db7-135"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="14db7-135"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="14db7-136">DLL</span><span class="sxs-lookup"><span data-stu-id="14db7-136">DLL</span></span><br/>          | <dl> <span data-ttu-id="14db7-137"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="14db7-137"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14db7-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="14db7-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14db7-139">**итсдп**</span><span class="sxs-lookup"><span data-stu-id="14db7-139">**ITSdp**</span></span>](itsdp.md)
</dt> </dl>

 

 




