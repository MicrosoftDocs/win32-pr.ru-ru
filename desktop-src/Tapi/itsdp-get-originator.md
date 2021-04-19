---
description: Метод Get \_ инициатора получает инициатор Конференции.
ms.assetid: a324098d-ae22-42e9-901e-b277433af199
title: 'Метод Итсдп:: get_Originator (Сдпблб. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f751dd5a9dffe2d3bbc7883b8a0f8f18f8e6381
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675220"
---
# <a name="itsdpget_originator-method"></a><span data-ttu-id="c6d58-103">Метод Итсдп:: Get \_ инициатора</span><span class="sxs-lookup"><span data-stu-id="c6d58-103">ITSdp::get\_Originator method</span></span>

<span data-ttu-id="c6d58-104">\[ В Windows Vista, Windows Server 2008 и последующих версиях операционной системы нельзя использовать встречные средства и элементы управления Конференц-телефонией и интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="c6d58-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="c6d58-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="c6d58-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="c6d58-106">Метод **Get \_ инициатора** получает инициатор Конференции.</span><span class="sxs-lookup"><span data-stu-id="c6d58-106">The **get\_Originator** method gets the conference originator.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6d58-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c6d58-107">Syntax</span></span>


```C++
HRESULT get_Originator(
  [out] BSTR *ppOriginator
);
```



## <a name="parameters"></a><span data-ttu-id="c6d58-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="c6d58-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6d58-109">*ппоригинатор* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="c6d58-109">*ppOriginator* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c6d58-110">Указатель на представление в формате **BSTR** инициатора Конференции.</span><span class="sxs-lookup"><span data-stu-id="c6d58-110">Pointer to a **BSTR** representation of the conference originator.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c6d58-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c6d58-111">Return value</span></span>

<span data-ttu-id="c6d58-112">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="c6d58-112">This method can return one of these values.</span></span>



| <span data-ttu-id="c6d58-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="c6d58-113">Return code</span></span>                                                                                   | <span data-ttu-id="c6d58-114">Описание</span><span class="sxs-lookup"><span data-stu-id="c6d58-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="c6d58-115"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="c6d58-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="c6d58-116">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="c6d58-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="c6d58-117"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="c6d58-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="c6d58-118">Параметр *ппоригинатор* не является допустимым указателем.</span><span class="sxs-lookup"><span data-stu-id="c6d58-118">The *ppOriginator* parameter is not a valid pointer.</span></span><br/> |
| <dl> <span data-ttu-id="c6d58-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="c6d58-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="c6d58-120">Недостаточно памяти для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="c6d58-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="c6d58-121"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="c6d58-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="c6d58-122">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="c6d58-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="c6d58-123"><dt>**E \_ нотимпл**</dt></span><span class="sxs-lookup"><span data-stu-id="c6d58-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="c6d58-124">Этот метод еще не реализован.</span><span class="sxs-lookup"><span data-stu-id="c6d58-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="c6d58-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c6d58-125">Remarks</span></span>

<span data-ttu-id="c6d58-126">Приложение должно использовать [**сисфристринг**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) для освобождения памяти, выделенной для параметра *ппоригинатор* .</span><span class="sxs-lookup"><span data-stu-id="c6d58-126">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory allocated for the *ppOriginator* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6d58-127">Требования</span><span class="sxs-lookup"><span data-stu-id="c6d58-127">Requirements</span></span>



| <span data-ttu-id="c6d58-128">Требование</span><span class="sxs-lookup"><span data-stu-id="c6d58-128">Requirement</span></span> | <span data-ttu-id="c6d58-129">Значение</span><span class="sxs-lookup"><span data-stu-id="c6d58-129">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c6d58-130">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="c6d58-130">TAPI version</span></span><br/> | <span data-ttu-id="c6d58-131">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="c6d58-131">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="c6d58-132">Header</span><span class="sxs-lookup"><span data-stu-id="c6d58-132">Header</span></span><br/>       | <dl> <span data-ttu-id="c6d58-133"><dt>Сдпблб. h</dt></span><span class="sxs-lookup"><span data-stu-id="c6d58-133"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="c6d58-134">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c6d58-134">Library</span></span><br/>      | <dl> <span data-ttu-id="c6d58-135"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c6d58-135"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="c6d58-136">DLL</span><span class="sxs-lookup"><span data-stu-id="c6d58-136">DLL</span></span><br/>          | <dl> <span data-ttu-id="c6d58-137"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c6d58-137"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6d58-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c6d58-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6d58-139">**итсдп**</span><span class="sxs-lookup"><span data-stu-id="c6d58-139">**ITSdp**</span></span>](itsdp.md)
</dt> <dt>

[<span data-ttu-id="c6d58-140">**Итсдп::p UT \_ инициатор**</span><span class="sxs-lookup"><span data-stu-id="c6d58-140">**ITSdp::put\_Originator**</span></span>](itsdp-put-originator.md)
</dt> </dl>

 

