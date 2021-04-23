---
description: Метод размещения \_ инициатора задает инициатора Конференции.
ms.assetid: b70fc584-3536-4296-bc38-e20ff6630abc
title: 'Итсдп: метод ut_Originator:p (Сдпблб. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 506554668e697e9281dc5dc15784fa36f7429d63
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105674779"
---
# <a name="itsdpput_originator-method"></a><span data-ttu-id="541d5-103">Итсдп::p \_ метод UT инициатора</span><span class="sxs-lookup"><span data-stu-id="541d5-103">ITSdp::put\_Originator method</span></span>

<span data-ttu-id="541d5-104">\[ В Windows Vista, Windows Server 2008 и последующих версиях операционной системы нельзя использовать встречные средства и элементы управления Конференц-телефонией и интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="541d5-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="541d5-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="541d5-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="541d5-106">Метод **размещения \_ инициатора** задает инициатора Конференции.</span><span class="sxs-lookup"><span data-stu-id="541d5-106">The **put\_Originator** method sets the conference originator.</span></span>

## <a name="syntax"></a><span data-ttu-id="541d5-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="541d5-107">Syntax</span></span>


```C++
HRESULT put_Originator(
  [in] BSTR pOriginator
);
```



## <a name="parameters"></a><span data-ttu-id="541d5-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="541d5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="541d5-109">*поригинатор* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="541d5-109">*pOriginator* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="541d5-110">Указатель на представление в формате **BSTR** инициатора Конференции.</span><span class="sxs-lookup"><span data-stu-id="541d5-110">Pointer to a **BSTR** representation of the conference originator.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="541d5-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="541d5-111">Return value</span></span>

<span data-ttu-id="541d5-112">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="541d5-112">This method can return one of these values.</span></span>



| <span data-ttu-id="541d5-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="541d5-113">Return code</span></span>                                                                                   | <span data-ttu-id="541d5-114">Описание</span><span class="sxs-lookup"><span data-stu-id="541d5-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="541d5-115"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="541d5-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="541d5-116">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="541d5-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="541d5-117"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="541d5-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="541d5-118">Параметр *поригинатор* не является допустимым указателем.</span><span class="sxs-lookup"><span data-stu-id="541d5-118">The *pOriginator* parameter is not a valid pointer.</span></span><br/>  |
| <dl> <span data-ttu-id="541d5-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="541d5-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="541d5-120">Недостаточно памяти для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="541d5-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="541d5-121"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="541d5-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="541d5-122">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="541d5-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="541d5-123"><dt>**E \_ нотимпл**</dt></span><span class="sxs-lookup"><span data-stu-id="541d5-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="541d5-124">Этот метод еще не реализован.</span><span class="sxs-lookup"><span data-stu-id="541d5-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="541d5-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="541d5-125">Remarks</span></span>

<span data-ttu-id="541d5-126">Приложение должно использовать [**сисаллокстринг**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) для выделения памяти для параметра *Поригинатор* и использовать [**сисфристринг**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) для освобождения памяти, когда переменная больше не нужна.</span><span class="sxs-lookup"><span data-stu-id="541d5-126">The application must use [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) to allocate memory for the *pOriginator* parameter and use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory when the variable is no longer needed.</span></span>

<span data-ttu-id="541d5-127">Эта функция может передавать данные по сети в незашифрованном виде; Таким образом, кто-то, кто прослушивает сеть, может прочитать данные.</span><span class="sxs-lookup"><span data-stu-id="541d5-127">This function may send data over the wire in unencrypted form; therefore, someone eavesdropping on the network may be able to read the data.</span></span> <span data-ttu-id="541d5-128">Прежде чем использовать этот метод, следует учесть угрозу безопасности при отправке данных в виде открытого текста.</span><span class="sxs-lookup"><span data-stu-id="541d5-128">The security risk of sending the data in clear text should be considered before using this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="541d5-129">Требования</span><span class="sxs-lookup"><span data-stu-id="541d5-129">Requirements</span></span>



| <span data-ttu-id="541d5-130">Требование</span><span class="sxs-lookup"><span data-stu-id="541d5-130">Requirement</span></span> | <span data-ttu-id="541d5-131">Значение</span><span class="sxs-lookup"><span data-stu-id="541d5-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="541d5-132">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="541d5-132">TAPI version</span></span><br/> | <span data-ttu-id="541d5-133">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="541d5-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="541d5-134">Header</span><span class="sxs-lookup"><span data-stu-id="541d5-134">Header</span></span><br/>       | <dl> <span data-ttu-id="541d5-135"><dt>Сдпблб. h</dt></span><span class="sxs-lookup"><span data-stu-id="541d5-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="541d5-136">Библиотека</span><span class="sxs-lookup"><span data-stu-id="541d5-136">Library</span></span><br/>      | <dl> <span data-ttu-id="541d5-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="541d5-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="541d5-138">DLL</span><span class="sxs-lookup"><span data-stu-id="541d5-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="541d5-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="541d5-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="541d5-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="541d5-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="541d5-141">**итсдп**</span><span class="sxs-lookup"><span data-stu-id="541d5-141">**ITSdp**</span></span>](itsdp.md)
</dt> <dt>

[<span data-ttu-id="541d5-142">**Итсдп:: получение \_ инициатора**</span><span class="sxs-lookup"><span data-stu-id="541d5-142">**ITSdp::get\_Originator**</span></span>](itsdp-get-originator.md)
</dt> </dl>

 

