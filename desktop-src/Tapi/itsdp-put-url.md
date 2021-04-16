---
description: Метод размещения \_ URL-адреса задает URL-адрес.
ms.assetid: 538bb1dd-c7ad-446d-9df7-23363b466263
title: 'Итсдп: метод ut_Url:p (Сдпблб. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b791d18b97851e6b0b27a4ba26d1dfdbce7dbb7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675765"
---
# <a name="itsdpput_url-method"></a><span data-ttu-id="9abcc-103">Итсдп: \_ метод URL-адреса:p UT</span><span class="sxs-lookup"><span data-stu-id="9abcc-103">ITSdp::put\_Url method</span></span>

<span data-ttu-id="9abcc-104">\[ В Windows Vista, Windows Server 2008 и последующих версиях операционной системы нельзя использовать встречные средства и элементы управления Конференц-телефонией и интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="9abcc-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="9abcc-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="9abcc-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="9abcc-106">Метод **размещения \_ URL** -адреса задает URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="9abcc-106">The **put\_Url** method sets the URL.</span></span>

## <a name="syntax"></a><span data-ttu-id="9abcc-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9abcc-107">Syntax</span></span>


```C++
HRESULT put_Url(
  [in] BSTR pUrl
);
```



## <a name="parameters"></a><span data-ttu-id="9abcc-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="9abcc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9abcc-109">*пурл* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9abcc-109">*pUrl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9abcc-110">Указатель на представление URL-адреса в формате **BSTR** .</span><span class="sxs-lookup"><span data-stu-id="9abcc-110">Pointer to a **BSTR** representation of the URL.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9abcc-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9abcc-111">Return value</span></span>

<span data-ttu-id="9abcc-112">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="9abcc-112">This method can return one of these values.</span></span>



| <span data-ttu-id="9abcc-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="9abcc-113">Return code</span></span>                                                                                   | <span data-ttu-id="9abcc-114">Описание</span><span class="sxs-lookup"><span data-stu-id="9abcc-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="9abcc-115"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="9abcc-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="9abcc-116">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="9abcc-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="9abcc-117"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="9abcc-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="9abcc-118">Параметр *пурл* не является допустимым указателем.</span><span class="sxs-lookup"><span data-stu-id="9abcc-118">The *pUrl* parameter is not a valid pointer.</span></span><br/>         |
| <dl> <span data-ttu-id="9abcc-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="9abcc-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="9abcc-120">Недостаточно памяти для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="9abcc-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="9abcc-121"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="9abcc-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="9abcc-122">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="9abcc-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="9abcc-123"><dt>**E \_ нотимпл**</dt></span><span class="sxs-lookup"><span data-stu-id="9abcc-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="9abcc-124">Этот метод еще не реализован.</span><span class="sxs-lookup"><span data-stu-id="9abcc-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="9abcc-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9abcc-125">Remarks</span></span>

<span data-ttu-id="9abcc-126">Приложение должно использовать [**сисаллокстринг**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) для выделения памяти для параметра *Пурл* и использовать [**сисфристринг**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) для освобождения памяти, когда переменная больше не нужна.</span><span class="sxs-lookup"><span data-stu-id="9abcc-126">The application must use [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) to allocate memory for the *pUrl* parameter and use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory when the variable is no longer needed.</span></span>

<span data-ttu-id="9abcc-127">URL-адрес обычно используется для ссылки на веб-страницу, содержащую дополнительные ресурсы или общие сведения о Конференции.</span><span class="sxs-lookup"><span data-stu-id="9abcc-127">An URL is typically used to reference a Web page containing additional resources or background information about a conference.</span></span>

<span data-ttu-id="9abcc-128">Эта функция может передавать данные по сети в незашифрованном виде; Таким образом, кто-то, кто прослушивает сеть, может прочитать данные.</span><span class="sxs-lookup"><span data-stu-id="9abcc-128">This function may send data over the wire in unencrypted form; therefore, someone eavesdropping on the network may be able to read the data.</span></span> <span data-ttu-id="9abcc-129">Прежде чем использовать этот метод, следует учесть угрозу безопасности при отправке данных в виде открытого текста.</span><span class="sxs-lookup"><span data-stu-id="9abcc-129">The security risk of sending the data in clear text should be considered before using this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="9abcc-130">Требования</span><span class="sxs-lookup"><span data-stu-id="9abcc-130">Requirements</span></span>



| <span data-ttu-id="9abcc-131">Требование</span><span class="sxs-lookup"><span data-stu-id="9abcc-131">Requirement</span></span> | <span data-ttu-id="9abcc-132">Значение</span><span class="sxs-lookup"><span data-stu-id="9abcc-132">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9abcc-133">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="9abcc-133">TAPI version</span></span><br/> | <span data-ttu-id="9abcc-134">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="9abcc-134">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="9abcc-135">Header</span><span class="sxs-lookup"><span data-stu-id="9abcc-135">Header</span></span><br/>       | <dl> <span data-ttu-id="9abcc-136"><dt>Сдпблб. h</dt></span><span class="sxs-lookup"><span data-stu-id="9abcc-136"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="9abcc-137">Библиотека</span><span class="sxs-lookup"><span data-stu-id="9abcc-137">Library</span></span><br/>      | <dl> <span data-ttu-id="9abcc-138"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9abcc-138"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="9abcc-139">DLL</span><span class="sxs-lookup"><span data-stu-id="9abcc-139">DLL</span></span><br/>          | <dl> <span data-ttu-id="9abcc-140"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9abcc-140"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9abcc-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9abcc-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9abcc-142">**итсдп**</span><span class="sxs-lookup"><span data-stu-id="9abcc-142">**ITSdp**</span></span>](itsdp.md)
</dt> <dt>

[<span data-ttu-id="9abcc-143">**Итсдп:: Get \_ URL-адрес**</span><span class="sxs-lookup"><span data-stu-id="9abcc-143">**ITSdp::get\_Url**</span></span>](itsdp-get-url.md)
</dt> </dl>

 

