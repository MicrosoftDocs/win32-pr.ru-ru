---
description: Метод Get \_ Name получает имя сеанса.
ms.assetid: 97b44a01-585b-434c-ad59-51c35e8a1ceb
title: 'Метод Итсдп:: get_Name (Сдпблб. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b41d431a76f3d0bb2122847e8ee5c3a4dde3c1b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675059"
---
# <a name="itsdpget_name-method"></a><span data-ttu-id="8d0f4-103">Метод Итсдп:: Get \_ Name</span><span class="sxs-lookup"><span data-stu-id="8d0f4-103">ITSdp::get\_Name method</span></span>

<span data-ttu-id="8d0f4-104">\[ В Windows Vista, Windows Server 2008 и последующих версиях операционной системы нельзя использовать встречные средства и элементы управления Конференц-телефонией и интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="8d0f4-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="8d0f4-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="8d0f4-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="8d0f4-106">Метод **Get \_ Name** получает имя сеанса.</span><span class="sxs-lookup"><span data-stu-id="8d0f4-106">The **get\_Name** method gets the session name.</span></span> <span data-ttu-id="8d0f4-107">Это должна быть строка, преобразуемая в строку ASCII, если кодировка — ASCII.</span><span class="sxs-lookup"><span data-stu-id="8d0f4-107">This has to be an ASCII convertible string if the character set is ASCII.</span></span> <span data-ttu-id="8d0f4-108">(В противном случае это может быть любая строка **BSTR** .)</span><span class="sxs-lookup"><span data-stu-id="8d0f4-108">(Otherwise, it can be any **BSTR** string.)</span></span>

## <a name="syntax"></a><span data-ttu-id="8d0f4-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8d0f4-109">Syntax</span></span>


```C++
HRESULT get_Name(
  [out] BSTR *ppName
);
```



## <a name="parameters"></a><span data-ttu-id="8d0f4-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="8d0f4-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d0f4-111">*ппнаме* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="8d0f4-111">*ppName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8d0f4-112">Указатель на **строку BSTR** , содержащую имя сеанса.</span><span class="sxs-lookup"><span data-stu-id="8d0f4-112">Pointer to a **BSTR** containing the session name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d0f4-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8d0f4-113">Return value</span></span>

<span data-ttu-id="8d0f4-114">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="8d0f4-114">This method can return one of these values.</span></span>



| <span data-ttu-id="8d0f4-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="8d0f4-115">Return code</span></span>                                                                                   | <span data-ttu-id="8d0f4-116">Описание</span><span class="sxs-lookup"><span data-stu-id="8d0f4-116">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="8d0f4-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="8d0f4-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="8d0f4-118">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="8d0f4-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="8d0f4-119"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="8d0f4-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="8d0f4-120">Параметр *ппнаме* не является допустимым указателем.</span><span class="sxs-lookup"><span data-stu-id="8d0f4-120">The *ppName* parameter is not a valid pointer.</span></span><br/>       |
| <dl> <span data-ttu-id="8d0f4-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="8d0f4-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="8d0f4-122">Недостаточно памяти для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="8d0f4-122">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="8d0f4-123"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="8d0f4-123"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="8d0f4-124">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="8d0f4-124">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="8d0f4-125"><dt>**E \_ нотимпл**</dt></span><span class="sxs-lookup"><span data-stu-id="8d0f4-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="8d0f4-126">Этот метод еще не реализован.</span><span class="sxs-lookup"><span data-stu-id="8d0f4-126">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="8d0f4-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8d0f4-127">Remarks</span></span>

<span data-ttu-id="8d0f4-128">Приложение должно использовать [**сисфристринг**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) для освобождения памяти, выделенной для параметра *ппнаме* .</span><span class="sxs-lookup"><span data-stu-id="8d0f4-128">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory allocated for the *ppName* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d0f4-129">Требования</span><span class="sxs-lookup"><span data-stu-id="8d0f4-129">Requirements</span></span>



| <span data-ttu-id="8d0f4-130">Требование</span><span class="sxs-lookup"><span data-stu-id="8d0f4-130">Requirement</span></span> | <span data-ttu-id="8d0f4-131">Значение</span><span class="sxs-lookup"><span data-stu-id="8d0f4-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8d0f4-132">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="8d0f4-132">TAPI version</span></span><br/> | <span data-ttu-id="8d0f4-133">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="8d0f4-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="8d0f4-134">Header</span><span class="sxs-lookup"><span data-stu-id="8d0f4-134">Header</span></span><br/>       | <dl> <span data-ttu-id="8d0f4-135"><dt>Сдпблб. h</dt></span><span class="sxs-lookup"><span data-stu-id="8d0f4-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="8d0f4-136">Библиотека</span><span class="sxs-lookup"><span data-stu-id="8d0f4-136">Library</span></span><br/>      | <dl> <span data-ttu-id="8d0f4-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8d0f4-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="8d0f4-138">DLL</span><span class="sxs-lookup"><span data-stu-id="8d0f4-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="8d0f4-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8d0f4-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d0f4-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8d0f4-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d0f4-141">**итсдп**</span><span class="sxs-lookup"><span data-stu-id="8d0f4-141">**ITSdp**</span></span>](itsdp.md)
</dt> <dt>

[<span data-ttu-id="8d0f4-142">**Итсдп::p \_ имя UT**</span><span class="sxs-lookup"><span data-stu-id="8d0f4-142">**ITSdp::put\_Name**</span></span>](itsdp-put-name.md)
</dt> </dl>

 

