---
description: Метод Енумератестреамс перечисляет потоки, в настоящее время с участниками. Этот метод предоставляется для приложений C и C++. Клиентские приложения автоматизации, например написанные на Visual Basic, должны использовать метод Get \_ Streams.
ms.assetid: 69db198d-fb4c-482b-bf49-5c636ac2f86b
title: 'Метод ИтпартиЦипант:: Енумератестреамс (Ипмсп. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbc92c617ed4baee3ecc33aec65cbdcf50986a27
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689044"
---
# <a name="itparticipantenumeratestreams-method"></a><span data-ttu-id="b55ba-105">Метод ИтпартиЦипант:: Енумератестреамс</span><span class="sxs-lookup"><span data-stu-id="b55ba-105">ITParticipant::EnumerateStreams method</span></span>

<span data-ttu-id="b55ba-106">\[**Енумератестреамс** недоступен для использования в Windows Vista, windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="b55ba-106">\[**EnumerateStreams** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="b55ba-107">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="b55ba-107">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="b55ba-108">Метод **енумератестреамс** перечисляет потоки, в настоящее время с участниками.</span><span class="sxs-lookup"><span data-stu-id="b55ba-108">The **EnumerateStreams** method enumerates streams currently with the participants.</span></span> <span data-ttu-id="b55ba-109">Этот метод предоставляется для приложений C и C++.</span><span class="sxs-lookup"><span data-stu-id="b55ba-109">This method is provided for C and C++ applications.</span></span> <span data-ttu-id="b55ba-110">Клиентские приложения автоматизации, например написанные на Visual Basic, должны использовать метод [**Get \_ Streams**](itparticipant-get-streams.md) .</span><span class="sxs-lookup"><span data-stu-id="b55ba-110">Automation client applications, such as those written in Visual Basic, must use the [**get\_Streams**](itparticipant-get-streams.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="b55ba-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b55ba-111">Syntax</span></span>


```C++
HRESULT EnumerateStreams(
  [out] IEnumStream **ppEnumStream
);
```



## <a name="parameters"></a><span data-ttu-id="b55ba-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="b55ba-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b55ba-113">*ппенумстреам* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="b55ba-113">*ppEnumStream* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b55ba-114">Указатель на указатель интерфейса [**иенумстреам**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumstream) .</span><span class="sxs-lookup"><span data-stu-id="b55ba-114">Pointer to [**IEnumStream**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumstream) interface pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b55ba-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b55ba-115">Return value</span></span>

<span data-ttu-id="b55ba-116">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="b55ba-116">This method can return one of these values.</span></span>



| <span data-ttu-id="b55ba-117">Значение</span><span class="sxs-lookup"><span data-stu-id="b55ba-117">Value</span></span>                                                                                     | <span data-ttu-id="b55ba-118">Значение</span><span class="sxs-lookup"><span data-stu-id="b55ba-118">Meaning</span></span>                                                         |
|-------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="b55ba-119"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="b55ba-119"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="b55ba-120">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="b55ba-120">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="b55ba-121"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="b55ba-121"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="b55ba-122">Параметр *ппенумстреам* не является допустимым указателем.</span><span class="sxs-lookup"><span data-stu-id="b55ba-122">The *ppEnumStream* parameter is not a valid pointer.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b55ba-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b55ba-123">Remarks</span></span>

<span data-ttu-id="b55ba-124">TAPI вызывает метод **AddRef** в интерфейсе [**иенумстреам**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumstream) , возвращенном **итпартиЦипант:: енумератестреамс**.</span><span class="sxs-lookup"><span data-stu-id="b55ba-124">TAPI calls the **AddRef** method on the [**IEnumStream**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumstream) interface returned by **ITParticipant::EnumerateStreams**.</span></span> <span data-ttu-id="b55ba-125">Приложение должно вызвать **выпуск** в интерфейсе **иенумстреам** , чтобы освободить ресурсы, связанные с ним.</span><span class="sxs-lookup"><span data-stu-id="b55ba-125">The application must call **Release** on the **IEnumStream** interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="b55ba-126">Требования</span><span class="sxs-lookup"><span data-stu-id="b55ba-126">Requirements</span></span>



| <span data-ttu-id="b55ba-127">Требование</span><span class="sxs-lookup"><span data-stu-id="b55ba-127">Requirement</span></span> | <span data-ttu-id="b55ba-128">Значение</span><span class="sxs-lookup"><span data-stu-id="b55ba-128">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b55ba-129">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="b55ba-129">TAPI version</span></span><br/> | <span data-ttu-id="b55ba-130">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="b55ba-130">Requires TAPI 3.0 or later</span></span><br/>                                                |
| <span data-ttu-id="b55ba-131">Header</span><span class="sxs-lookup"><span data-stu-id="b55ba-131">Header</span></span><br/>       | <dl> <span data-ttu-id="b55ba-132"><dt>Ипмсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="b55ba-132"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="b55ba-133">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b55ba-133">Library</span></span><br/>      | <dl> <span data-ttu-id="b55ba-134"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b55ba-134"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="b55ba-135">DLL</span><span class="sxs-lookup"><span data-stu-id="b55ba-135">DLL</span></span><br/>          | <dl> <span data-ttu-id="b55ba-136"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b55ba-136"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b55ba-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b55ba-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b55ba-138">**итпартиЦипант**</span><span class="sxs-lookup"><span data-stu-id="b55ba-138">**ITParticipant**</span></span>](itparticipant.md)
</dt> <dt>

[<span data-ttu-id="b55ba-139">**получение \_ потоков**</span><span class="sxs-lookup"><span data-stu-id="b55ba-139">**get\_Streams**</span></span>](itparticipant-get-streams.md)
</dt> <dt>

[<span data-ttu-id="b55ba-140">**иенумстреам**</span><span class="sxs-lookup"><span data-stu-id="b55ba-140">**IEnumStream**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-ienumstream)
</dt> </dl>

 

 




