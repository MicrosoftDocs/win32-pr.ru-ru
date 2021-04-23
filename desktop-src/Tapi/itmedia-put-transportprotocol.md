---
description: Метод размещения \_ транспортпротокол задает транспортный протокол.
ms.assetid: d2f74d4a-a65d-4829-ad17-7548ef06cfeb
title: 'Итмедиа: метод ut_TransportProtocol:p (Сдпблб. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c6b4228a5d2a6ea49ae3f87b9306ea80e94fc36
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675634"
---
# <a name="itmediaput_transportprotocol-method"></a><span data-ttu-id="468ce-103">Итмедиа::p UT \_ транспортпротокол метод</span><span class="sxs-lookup"><span data-stu-id="468ce-103">ITMedia::put\_TransportProtocol method</span></span>

<span data-ttu-id="468ce-104">\[ В Windows Vista, Windows Server 2008 и последующих версиях операционной системы нельзя использовать встречные средства и элементы управления Конференц-телефонией и интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="468ce-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="468ce-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="468ce-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="468ce-106">Метод **размещения \_ транспортпротокол** задает транспортный протокол.</span><span class="sxs-lookup"><span data-stu-id="468ce-106">The **put\_TransportProtocol** method sets the transport protocol.</span></span> <span data-ttu-id="468ce-107">Это указывается в дополнение к формату мультимедиа, чтобы один и тот же стандартный формат мультимедиа можно было переносить по разным транспортным протоколам, даже если сетевой протокол аналогичен, например, с помощью звука PCM и звука PCM в формате "сеть — налог".</span><span class="sxs-lookup"><span data-stu-id="468ce-107">This is specified in addition to the media format so that the same standard media format may be carried over different transport protocols even when the network protocol is the same, such as with Vat PCM audio and RTP PCM audio.</span></span>

## <a name="syntax"></a><span data-ttu-id="468ce-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="468ce-108">Syntax</span></span>


```C++
HRESULT put_TransportProtocol(
  [in] BSTR pProtocol
);
```



## <a name="parameters"></a><span data-ttu-id="468ce-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="468ce-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="468ce-110">*ппротокол* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="468ce-110">*pProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="468ce-111">Указатель на **строку BSTR** , содержащую транспортный протокол.</span><span class="sxs-lookup"><span data-stu-id="468ce-111">Pointer to a **BSTR** containing the transport protocol.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="468ce-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="468ce-112">Return value</span></span>

<span data-ttu-id="468ce-113">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="468ce-113">This method can return one of these values.</span></span>



| <span data-ttu-id="468ce-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="468ce-114">Return code</span></span>                                                                                   | <span data-ttu-id="468ce-115">Описание</span><span class="sxs-lookup"><span data-stu-id="468ce-115">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="468ce-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="468ce-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="468ce-117">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="468ce-117">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="468ce-118"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="468ce-118"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="468ce-119">Параметр *ппротокол* не является допустимым указателем.</span><span class="sxs-lookup"><span data-stu-id="468ce-119">The *pProtocol* parameter is not a valid pointer.</span></span><br/>    |
| <dl> <span data-ttu-id="468ce-120"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="468ce-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="468ce-121">Недостаточно памяти для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="468ce-121">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="468ce-122"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="468ce-122"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="468ce-123">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="468ce-123">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="468ce-124"><dt>**E \_ нотимпл**</dt></span><span class="sxs-lookup"><span data-stu-id="468ce-124"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="468ce-125">Этот метод еще не реализован.</span><span class="sxs-lookup"><span data-stu-id="468ce-125">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="468ce-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="468ce-126">Remarks</span></span>

<span data-ttu-id="468ce-127">Приложение должно использовать [**сисаллокстринг**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) для выделения памяти для параметра *Ппротокол* и использовать [**сисфристринг**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) для освобождения памяти, когда переменная больше не нужна.</span><span class="sxs-lookup"><span data-stu-id="468ce-127">The application must use [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) to allocate memory for the *pProtocol* parameter and use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory when the variable is no longer needed.</span></span>

<span data-ttu-id="468ce-128">Эта функция может передавать данные по сети в незашифрованном виде; Таким образом, кто-то, кто прослушивает сеть, может прочитать данные.</span><span class="sxs-lookup"><span data-stu-id="468ce-128">This function may send data over the wire in unencrypted form; therefore, someone eavesdropping on the network may be able to read the data.</span></span> <span data-ttu-id="468ce-129">Прежде чем использовать этот метод, следует учесть угрозу безопасности при отправке данных в виде открытого текста.</span><span class="sxs-lookup"><span data-stu-id="468ce-129">The security risk of sending the data in clear text should be considered before using this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="468ce-130">Требования</span><span class="sxs-lookup"><span data-stu-id="468ce-130">Requirements</span></span>



| <span data-ttu-id="468ce-131">Требование</span><span class="sxs-lookup"><span data-stu-id="468ce-131">Requirement</span></span> | <span data-ttu-id="468ce-132">Значение</span><span class="sxs-lookup"><span data-stu-id="468ce-132">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="468ce-133">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="468ce-133">TAPI version</span></span><br/> | <span data-ttu-id="468ce-134">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="468ce-134">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="468ce-135">Header</span><span class="sxs-lookup"><span data-stu-id="468ce-135">Header</span></span><br/>       | <dl> <span data-ttu-id="468ce-136"><dt>Сдпблб. h</dt></span><span class="sxs-lookup"><span data-stu-id="468ce-136"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="468ce-137">Библиотека</span><span class="sxs-lookup"><span data-stu-id="468ce-137">Library</span></span><br/>      | <dl> <span data-ttu-id="468ce-138"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="468ce-138"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="468ce-139">DLL</span><span class="sxs-lookup"><span data-stu-id="468ce-139">DLL</span></span><br/>          | <dl> <span data-ttu-id="468ce-140"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="468ce-140"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="468ce-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="468ce-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="468ce-142">**итмедиа**</span><span class="sxs-lookup"><span data-stu-id="468ce-142">**ITMedia**</span></span>](itmedia.md)
</dt> <dt>

[<span data-ttu-id="468ce-143">**Итмедиа:: Get \_ транспортпротокол**</span><span class="sxs-lookup"><span data-stu-id="468ce-143">**ITMedia::get\_TransportProtocol**</span></span>](itmedia-get-transportprotocol.md)
</dt> </dl>

 

