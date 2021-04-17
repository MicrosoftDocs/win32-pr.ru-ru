---
description: Метод Get \_ Description Возвращает описание сеанса (BSTR).
ms.assetid: 09a372fe-0dcd-4daf-8f13-c4c89b1ecd16
title: 'Метод Итсдп:: get_Description (Сдпблб. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5f60f7aefcfac852a1665f54a59ff0541b1d82a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680052"
---
# <a name="itsdpget_description-method"></a><span data-ttu-id="f6f56-103">Метод Итсдп:: Get \_ Description</span><span class="sxs-lookup"><span data-stu-id="f6f56-103">ITSdp::get\_Description method</span></span>

<span data-ttu-id="f6f56-104">\[ В Windows Vista, Windows Server 2008 и последующих версиях операционной системы нельзя использовать встречные средства и элементы управления Конференц-телефонией и интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="f6f56-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="f6f56-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="f6f56-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="f6f56-106">Метод **Get \_ Description** Возвращает описание сеанса (**BSTR**).</span><span class="sxs-lookup"><span data-stu-id="f6f56-106">The **get\_Description** method gets the session description (**BSTR**).</span></span> <span data-ttu-id="f6f56-107">Это должна быть строка, преобразуемая в строку ASCII, если кодировка — ASCII.</span><span class="sxs-lookup"><span data-stu-id="f6f56-107">This has to be an ASCII convertible string if the character set is ASCII.</span></span> <span data-ttu-id="f6f56-108">(В противном случае это может быть любая строка **BSTR** .)</span><span class="sxs-lookup"><span data-stu-id="f6f56-108">(Otherwise, it can be any **BSTR** string.)</span></span>

## <a name="syntax"></a><span data-ttu-id="f6f56-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f6f56-109">Syntax</span></span>


```C++
HRESULT get_Description(
  [out] BSTR *ppDescription
);
```



## <a name="parameters"></a><span data-ttu-id="f6f56-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="f6f56-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6f56-111">*ппдескриптион* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="f6f56-111">*ppDescription* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f6f56-112">Указатель на **строку BSTR** , содержащую описание сеанса.</span><span class="sxs-lookup"><span data-stu-id="f6f56-112">Pointer to a **BSTR** containing the session description.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6f56-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f6f56-113">Return value</span></span>

<span data-ttu-id="f6f56-114">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="f6f56-114">This method can return one of these values.</span></span>



| <span data-ttu-id="f6f56-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="f6f56-115">Return code</span></span>                                                                                   | <span data-ttu-id="f6f56-116">Описание</span><span class="sxs-lookup"><span data-stu-id="f6f56-116">Description</span></span>                                                      |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <span data-ttu-id="f6f56-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="f6f56-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="f6f56-118">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="f6f56-118">Method succeeded.</span></span><br/>                                     |
| <dl> <span data-ttu-id="f6f56-119"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="f6f56-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="f6f56-120">Параметр *ппдескриптион* не является допустимым указателем.</span><span class="sxs-lookup"><span data-stu-id="f6f56-120">The *ppDescription* parameter is not a valid pointer.</span></span><br/> |
| <dl> <span data-ttu-id="f6f56-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="f6f56-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="f6f56-122">Недостаточно памяти для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="f6f56-122">Insufficient memory exists to perform the operation.</span></span><br/>  |
| <dl> <span data-ttu-id="f6f56-123"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="f6f56-123"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="f6f56-124">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="f6f56-124">Unspecified error.</span></span><br/>                                    |
| <dl> <span data-ttu-id="f6f56-125"><dt>**E \_ нотимпл**</dt></span><span class="sxs-lookup"><span data-stu-id="f6f56-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="f6f56-126">Этот метод еще не реализован.</span><span class="sxs-lookup"><span data-stu-id="f6f56-126">This method is not yet implemented.</span></span><br/>                   |



 

## <a name="remarks"></a><span data-ttu-id="f6f56-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f6f56-127">Remarks</span></span>

<span data-ttu-id="f6f56-128">Приложение должно использовать [**сисфристринг**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) для высвобождения параметра *ппдескриптион* .</span><span class="sxs-lookup"><span data-stu-id="f6f56-128">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the *ppDescription* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6f56-129">Требования</span><span class="sxs-lookup"><span data-stu-id="f6f56-129">Requirements</span></span>



| <span data-ttu-id="f6f56-130">Требование</span><span class="sxs-lookup"><span data-stu-id="f6f56-130">Requirement</span></span> | <span data-ttu-id="f6f56-131">Значение</span><span class="sxs-lookup"><span data-stu-id="f6f56-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f6f56-132">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="f6f56-132">TAPI version</span></span><br/> | <span data-ttu-id="f6f56-133">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="f6f56-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="f6f56-134">Header</span><span class="sxs-lookup"><span data-stu-id="f6f56-134">Header</span></span><br/>       | <dl> <span data-ttu-id="f6f56-135"><dt>Сдпблб. h</dt></span><span class="sxs-lookup"><span data-stu-id="f6f56-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="f6f56-136">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f6f56-136">Library</span></span><br/>      | <dl> <span data-ttu-id="f6f56-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f6f56-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="f6f56-138">DLL</span><span class="sxs-lookup"><span data-stu-id="f6f56-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="f6f56-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f6f56-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6f56-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f6f56-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6f56-141">**итсдп**</span><span class="sxs-lookup"><span data-stu-id="f6f56-141">**ITSdp**</span></span>](itsdp.md)
</dt> <dt>

[<span data-ttu-id="f6f56-142">**Итсдп: описание:p UT \_**</span><span class="sxs-lookup"><span data-stu-id="f6f56-142">**ITSdp::put\_Description**</span></span>](itsdp-put-description.md)
</dt> </dl>

 

