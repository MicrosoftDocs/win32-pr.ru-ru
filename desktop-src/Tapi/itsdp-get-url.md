---
description: Метод Get \_ URL получает URL-адрес.
ms.assetid: 9ea2ddf6-b8c7-4bfa-aab3-ff2d2056837f
title: 'Метод Итсдп:: get_Url (Сдпблб. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a207c158d405ac0931e42aa19995d1d4b3078fd0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680112"
---
# <a name="itsdpget_url-method"></a><span data-ttu-id="18c96-103">Метод Итсдп:: Get \_ URL</span><span class="sxs-lookup"><span data-stu-id="18c96-103">ITSdp::get\_Url method</span></span>

<span data-ttu-id="18c96-104">\[ В Windows Vista, Windows Server 2008 и последующих версиях операционной системы нельзя использовать встречные средства и элементы управления Конференц-телефонией и интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="18c96-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="18c96-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="18c96-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="18c96-106">Метод **Get \_ URL** получает URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="18c96-106">The **get\_Url** method gets the URL.</span></span>

## <a name="syntax"></a><span data-ttu-id="18c96-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="18c96-107">Syntax</span></span>


```C++
HRESULT get_Url(
  [out] BSTR *ppUrl
);
```



## <a name="parameters"></a><span data-ttu-id="18c96-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="18c96-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18c96-109">*ппурл* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="18c96-109">*ppUrl* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="18c96-110">Указатель на представление URL-адреса в формате **BSTR** .</span><span class="sxs-lookup"><span data-stu-id="18c96-110">Pointer to a **BSTR** representation of the URL.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="18c96-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="18c96-111">Return value</span></span>

<span data-ttu-id="18c96-112">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="18c96-112">This method can return one of these values.</span></span>



| <span data-ttu-id="18c96-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="18c96-113">Return code</span></span>                                                                                   | <span data-ttu-id="18c96-114">Описание</span><span class="sxs-lookup"><span data-stu-id="18c96-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="18c96-115"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="18c96-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="18c96-116">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="18c96-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="18c96-117"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="18c96-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="18c96-118">Параметр *ппурл* не является допустимым указателем.</span><span class="sxs-lookup"><span data-stu-id="18c96-118">The *ppUrl* parameter is not a valid pointer.</span></span><br/>        |
| <dl> <span data-ttu-id="18c96-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="18c96-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="18c96-120">Недостаточно памяти для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="18c96-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="18c96-121"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="18c96-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="18c96-122">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="18c96-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="18c96-123"><dt>**E \_ нотимпл**</dt></span><span class="sxs-lookup"><span data-stu-id="18c96-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="18c96-124">Этот метод еще не реализован.</span><span class="sxs-lookup"><span data-stu-id="18c96-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="18c96-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="18c96-125">Remarks</span></span>

<span data-ttu-id="18c96-126">Приложение должно использовать [**сисфристринг**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) для освобождения памяти, выделенной для параметра *ппурл* .</span><span class="sxs-lookup"><span data-stu-id="18c96-126">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory allocated for the *ppUrl* parameter.</span></span>

<span data-ttu-id="18c96-127">URL-адрес обычно используется для ссылки на веб-страницу, содержащую дополнительные ресурсы или общие сведения о Конференции.</span><span class="sxs-lookup"><span data-stu-id="18c96-127">An URL is typically used to reference a Web page containing additional resources or background information about a conference.</span></span>

## <a name="requirements"></a><span data-ttu-id="18c96-128">Требования</span><span class="sxs-lookup"><span data-stu-id="18c96-128">Requirements</span></span>



| <span data-ttu-id="18c96-129">Требование</span><span class="sxs-lookup"><span data-stu-id="18c96-129">Requirement</span></span> | <span data-ttu-id="18c96-130">Значение</span><span class="sxs-lookup"><span data-stu-id="18c96-130">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="18c96-131">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="18c96-131">TAPI version</span></span><br/> | <span data-ttu-id="18c96-132">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="18c96-132">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="18c96-133">Header</span><span class="sxs-lookup"><span data-stu-id="18c96-133">Header</span></span><br/>       | <dl> <span data-ttu-id="18c96-134"><dt>Сдпблб. h</dt></span><span class="sxs-lookup"><span data-stu-id="18c96-134"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="18c96-135">Библиотека</span><span class="sxs-lookup"><span data-stu-id="18c96-135">Library</span></span><br/>      | <dl> <span data-ttu-id="18c96-136"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="18c96-136"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="18c96-137">DLL</span><span class="sxs-lookup"><span data-stu-id="18c96-137">DLL</span></span><br/>          | <dl> <span data-ttu-id="18c96-138"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="18c96-138"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18c96-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="18c96-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18c96-140">**итсдп**</span><span class="sxs-lookup"><span data-stu-id="18c96-140">**ITSdp**</span></span>](itsdp.md)
</dt> <dt>

[<span data-ttu-id="18c96-141">**Итсдп::p \_ URL-адрес UT**</span><span class="sxs-lookup"><span data-stu-id="18c96-141">**ITSdp::put\_Url**</span></span>](itsdp-put-url.md)
</dt> </dl>

 

