---
description: Метод Get \_ мачинеаддресс возвращает адрес исходного узла.
ms.assetid: 8a67cc9f-f9fc-4ec3-86f9-ffe34d075830
title: 'Метод Итсдп:: get_MachineAddress (Сдпблб. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a34968efa16f04cba8f99dbc0dc42b0cf4995a43
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685312"
---
# <a name="itsdpget_machineaddress-method"></a><span data-ttu-id="087a6-103">Метод Итсдп:: Get \_ мачинеаддресс</span><span class="sxs-lookup"><span data-stu-id="087a6-103">ITSdp::get\_MachineAddress method</span></span>

<span data-ttu-id="087a6-104">\[ В Windows Vista, Windows Server 2008 и последующих версиях операционной системы нельзя использовать встречные средства и элементы управления Конференц-телефонией и интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="087a6-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="087a6-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="087a6-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="087a6-106">Метод **Get \_ мачинеаддресс** возвращает адрес исходного узла.</span><span class="sxs-lookup"><span data-stu-id="087a6-106">The **get\_MachineAddress** method gets the machine address of the originating host.</span></span>

## <a name="syntax"></a><span data-ttu-id="087a6-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="087a6-107">Syntax</span></span>


```C++
HRESULT get_MachineAddress(
  [out] BSTR *ppMachineAddress
);
```



## <a name="parameters"></a><span data-ttu-id="087a6-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="087a6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="087a6-109">*ппмачинеаддресс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="087a6-109">*ppMachineAddress* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="087a6-110">Указатель на **строку BSTR** , содержащую адрес компьютера узла Конференции.</span><span class="sxs-lookup"><span data-stu-id="087a6-110">Pointer to a **BSTR** containing the machine address of the conference host.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="087a6-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="087a6-111">Return value</span></span>

<span data-ttu-id="087a6-112">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="087a6-112">This method can return one of these values.</span></span>



| <span data-ttu-id="087a6-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="087a6-113">Return code</span></span>                                                                                   | <span data-ttu-id="087a6-114">Описание</span><span class="sxs-lookup"><span data-stu-id="087a6-114">Description</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <span data-ttu-id="087a6-115"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="087a6-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="087a6-116">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="087a6-116">Method succeeded.</span></span><br/>                                        |
| <dl> <span data-ttu-id="087a6-117"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="087a6-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="087a6-118">Параметр *ппмачинеаддрес* s не является допустимым указателем.</span><span class="sxs-lookup"><span data-stu-id="087a6-118">The *ppMachineAddres* s parameter is not a valid pointer.</span></span><br/> |
| <dl> <span data-ttu-id="087a6-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="087a6-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="087a6-120">Недостаточно памяти для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="087a6-120">Insufficient memory exists to perform the operation.</span></span><br/>     |
| <dl> <span data-ttu-id="087a6-121"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="087a6-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="087a6-122">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="087a6-122">Unspecified error.</span></span><br/>                                       |
| <dl> <span data-ttu-id="087a6-123"><dt>**E \_ нотимпл**</dt></span><span class="sxs-lookup"><span data-stu-id="087a6-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="087a6-124">Этот метод еще не реализован.</span><span class="sxs-lookup"><span data-stu-id="087a6-124">This method is not yet implemented.</span></span><br/>                      |



 

## <a name="remarks"></a><span data-ttu-id="087a6-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="087a6-125">Remarks</span></span>

<span data-ttu-id="087a6-126">Приложение должно использовать [**сисфристринг**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) для освобождения памяти, выделенной для параметра *ппмачинеаддресс* .</span><span class="sxs-lookup"><span data-stu-id="087a6-126">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory allocated for the *ppMachineAddress* parameter.</span></span>

<span data-ttu-id="087a6-127">Параметр *ппмачинеаддресс* может быть возвращен как DNS-имя ("JohnSmith.workinghard.Microsoft.com") или IP-адрес ("10.111.222.111").</span><span class="sxs-lookup"><span data-stu-id="087a6-127">The *ppMachineAddress* parameter can be returned as either a DNS name ("JohnSmith.workinghard.microsoft.com") or an IP address ("10.111.222.111").</span></span>

## <a name="requirements"></a><span data-ttu-id="087a6-128">Требования</span><span class="sxs-lookup"><span data-stu-id="087a6-128">Requirements</span></span>



| <span data-ttu-id="087a6-129">Требование</span><span class="sxs-lookup"><span data-stu-id="087a6-129">Requirement</span></span> | <span data-ttu-id="087a6-130">Значение</span><span class="sxs-lookup"><span data-stu-id="087a6-130">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="087a6-131">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="087a6-131">TAPI version</span></span><br/> | <span data-ttu-id="087a6-132">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="087a6-132">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="087a6-133">Header</span><span class="sxs-lookup"><span data-stu-id="087a6-133">Header</span></span><br/>       | <dl> <span data-ttu-id="087a6-134"><dt>Сдпблб. h</dt></span><span class="sxs-lookup"><span data-stu-id="087a6-134"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="087a6-135">Библиотека</span><span class="sxs-lookup"><span data-stu-id="087a6-135">Library</span></span><br/>      | <dl> <span data-ttu-id="087a6-136"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="087a6-136"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="087a6-137">DLL</span><span class="sxs-lookup"><span data-stu-id="087a6-137">DLL</span></span><br/>          | <dl> <span data-ttu-id="087a6-138"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="087a6-138"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="087a6-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="087a6-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="087a6-140">**итсдп**</span><span class="sxs-lookup"><span data-stu-id="087a6-140">**ITSdp**</span></span>](itsdp.md)
</dt> <dt>

[<span data-ttu-id="087a6-141">**Итсдп::p UT \_ мачинеаддресс**</span><span class="sxs-lookup"><span data-stu-id="087a6-141">**ITSdp::put\_MachineAddress**</span></span>](itsdp-put-machineaddress.md)
</dt> </dl>

 

