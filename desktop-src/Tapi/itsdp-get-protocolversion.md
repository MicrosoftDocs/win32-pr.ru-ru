---
description: Метод Get \_ протоколверсион получает версию протокола дескриптора сеанса (см. RFC 2327).
ms.assetid: 7c62357c-427f-40f9-a9d2-c4e1a8400e97
title: 'Метод Итсдп:: get_ProtocolVersion (Сдпблб. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 652c6c3d6723a10cfe474376cf8b9f1342321db8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675398"
---
# <a name="itsdpget_protocolversion-method"></a><span data-ttu-id="46f63-103">Метод Итсдп:: Get \_ протоколверсион</span><span class="sxs-lookup"><span data-stu-id="46f63-103">ITSdp::get\_ProtocolVersion method</span></span>

<span data-ttu-id="46f63-104">\[ В Windows Vista, Windows Server 2008 и последующих версиях операционной системы нельзя использовать встречные средства и элементы управления Конференц-телефонией и интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="46f63-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="46f63-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="46f63-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="46f63-106">Метод **Get \_ протоколверсион** получает версию протокола дескриптора сеанса (см. RFC 2327).</span><span class="sxs-lookup"><span data-stu-id="46f63-106">The **get\_ProtocolVersion** method gets the Session Descriptor Protocol (SDP; see RFC 2327) protocol version.</span></span>

## <a name="syntax"></a><span data-ttu-id="46f63-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="46f63-107">Syntax</span></span>


```C++
HRESULT get_ProtocolVersion(
  [out] unsigned char *pProtocolVersion
);
```



## <a name="parameters"></a><span data-ttu-id="46f63-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="46f63-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46f63-109">*ппротоколверсион* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="46f63-109">*pProtocolVersion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="46f63-110">Указатель на версию протокола.</span><span class="sxs-lookup"><span data-stu-id="46f63-110">Pointer to the protocol version.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46f63-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="46f63-111">Return value</span></span>

<span data-ttu-id="46f63-112">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="46f63-112">This method can return one of these values.</span></span>



| <span data-ttu-id="46f63-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="46f63-113">Return code</span></span>                                                                                   | <span data-ttu-id="46f63-114">Описание</span><span class="sxs-lookup"><span data-stu-id="46f63-114">Description</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <span data-ttu-id="46f63-115"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="46f63-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="46f63-116">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="46f63-116">Method succeeded.</span></span><br/>                                        |
| <dl> <span data-ttu-id="46f63-117"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="46f63-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="46f63-118">Параметр *ппротоколверсион* не является допустимым указателем.</span><span class="sxs-lookup"><span data-stu-id="46f63-118">The *pProtocolVersion* parameter is not a valid pointer.</span></span><br/> |
| <dl> <span data-ttu-id="46f63-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="46f63-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="46f63-120">Недостаточно памяти для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="46f63-120">Insufficient memory exists to perform the operation.</span></span><br/>     |
| <dl> <span data-ttu-id="46f63-121"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="46f63-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="46f63-122">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="46f63-122">Unspecified error.</span></span><br/>                                       |
| <dl> <span data-ttu-id="46f63-123"><dt>**E \_ нотимпл**</dt></span><span class="sxs-lookup"><span data-stu-id="46f63-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="46f63-124">Этот метод еще не реализован.</span><span class="sxs-lookup"><span data-stu-id="46f63-124">This method is not yet implemented.</span></span><br/>                      |



 

## <a name="requirements"></a><span data-ttu-id="46f63-125">Требования</span><span class="sxs-lookup"><span data-stu-id="46f63-125">Requirements</span></span>



| <span data-ttu-id="46f63-126">Требование</span><span class="sxs-lookup"><span data-stu-id="46f63-126">Requirement</span></span> | <span data-ttu-id="46f63-127">Значение</span><span class="sxs-lookup"><span data-stu-id="46f63-127">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="46f63-128">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="46f63-128">TAPI version</span></span><br/> | <span data-ttu-id="46f63-129">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="46f63-129">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="46f63-130">Header</span><span class="sxs-lookup"><span data-stu-id="46f63-130">Header</span></span><br/>       | <dl> <span data-ttu-id="46f63-131"><dt>Сдпблб. h</dt></span><span class="sxs-lookup"><span data-stu-id="46f63-131"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="46f63-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="46f63-132">Library</span></span><br/>      | <dl> <span data-ttu-id="46f63-133"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="46f63-133"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="46f63-134">DLL</span><span class="sxs-lookup"><span data-stu-id="46f63-134">DLL</span></span><br/>          | <dl> <span data-ttu-id="46f63-135"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="46f63-135"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46f63-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="46f63-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46f63-137">**итсдп**</span><span class="sxs-lookup"><span data-stu-id="46f63-137">**ITSdp**</span></span>](itsdp.md)
</dt> </dl>

 

 




