---
description: Метод Get \_ Streams создает коллекцию потоков, связанных с текущим участником.
ms.assetid: 9ab05b14-8ef8-4e7f-b598-05795011e35d
title: 'Метод ИтпартиЦипант:: get_Streams (Ипмсп. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a920929c71e01632edcd8c4c78029b479d8b250
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675485"
---
# <a name="itparticipantget_streams-method"></a><span data-ttu-id="82bac-103">Метод ИтпартиЦипант:: Get \_ Streams</span><span class="sxs-lookup"><span data-stu-id="82bac-103">ITParticipant::get\_Streams method</span></span>

<span data-ttu-id="82bac-104">\[**получить \_ Потоки** недоступны для использования в Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="82bac-104">\[**get\_Streams** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="82bac-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="82bac-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="82bac-106">Метод **Get \_ Streams** создает коллекцию потоков, связанных с текущим участником.</span><span class="sxs-lookup"><span data-stu-id="82bac-106">The **get\_Streams** method creates a collection of streams associated with the current participant.</span></span> <span data-ttu-id="82bac-107">Этот метод предоставляется для клиентских приложений автоматизации, например, написанных на Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="82bac-107">This method is provided for Automation client applications, such as those written in Visual Basic.</span></span> <span data-ttu-id="82bac-108">Приложения C и C++ должны использовать метод [**енумератестреамс**](itparticipant-enumeratestreams.md) .</span><span class="sxs-lookup"><span data-stu-id="82bac-108">C and C++ applications must use the [**EnumerateStreams**](itparticipant-enumeratestreams.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="82bac-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="82bac-109">Syntax</span></span>


```C++
HRESULT get_Streams(
  [out] VARIANT *pVariant
);
```



## <a name="parameters"></a><span data-ttu-id="82bac-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="82bac-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82bac-111">*пвариант* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="82bac-111">*pVariant* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="82bac-112">Указатель на **вариант** , содержащий [**итколлектион**](/windows/desktop/api/tapi3if/nn-tapi3if-itcollection) указателей интерфейса [**итстреам**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) .</span><span class="sxs-lookup"><span data-stu-id="82bac-112">Pointer to **VARIANT** containing an [**ITCollection**](/windows/desktop/api/tapi3if/nn-tapi3if-itcollection) of [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) interface pointers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82bac-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="82bac-113">Return value</span></span>

<span data-ttu-id="82bac-114">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="82bac-114">This method can return one of these values.</span></span>



| <span data-ttu-id="82bac-115">Значение</span><span class="sxs-lookup"><span data-stu-id="82bac-115">Value</span></span>                                                                                         | <span data-ttu-id="82bac-116">Значение</span><span class="sxs-lookup"><span data-stu-id="82bac-116">Meaning</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="82bac-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="82bac-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="82bac-118">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="82bac-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="82bac-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="82bac-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="82bac-120">Недостаточно памяти для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="82bac-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="82bac-121"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="82bac-121"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="82bac-122">Параметр *пвариант* не является допустимым указателем.</span><span class="sxs-lookup"><span data-stu-id="82bac-122">The *pVariant* parameter is not a valid pointer.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="82bac-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="82bac-123">Remarks</span></span>

<span data-ttu-id="82bac-124">TAPI вызывает метод **AddRef** в интерфейсе [**итстреам**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) , возвращенном **итпартиЦипант:: Get \_ Streams**.</span><span class="sxs-lookup"><span data-stu-id="82bac-124">TAPI calls the **AddRef** method on the [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) interface returned by **ITParticipant::get\_Streams**.</span></span> <span data-ttu-id="82bac-125">Приложение должно вызвать **выпуск** в интерфейсе **итстреам** , чтобы освободить ресурсы, связанные с ним.</span><span class="sxs-lookup"><span data-stu-id="82bac-125">The application must call **Release** on the **ITStream** interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="82bac-126">Требования</span><span class="sxs-lookup"><span data-stu-id="82bac-126">Requirements</span></span>



| <span data-ttu-id="82bac-127">Требование</span><span class="sxs-lookup"><span data-stu-id="82bac-127">Requirement</span></span> | <span data-ttu-id="82bac-128">Значение</span><span class="sxs-lookup"><span data-stu-id="82bac-128">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="82bac-129">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="82bac-129">TAPI version</span></span><br/> | <span data-ttu-id="82bac-130">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="82bac-130">Requires TAPI 3.0 or later</span></span><br/>                                                |
| <span data-ttu-id="82bac-131">Header</span><span class="sxs-lookup"><span data-stu-id="82bac-131">Header</span></span><br/>       | <dl> <span data-ttu-id="82bac-132"><dt>Ипмсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="82bac-132"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="82bac-133">Библиотека</span><span class="sxs-lookup"><span data-stu-id="82bac-133">Library</span></span><br/>      | <dl> <span data-ttu-id="82bac-134"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="82bac-134"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="82bac-135">DLL</span><span class="sxs-lookup"><span data-stu-id="82bac-135">DLL</span></span><br/>          | <dl> <span data-ttu-id="82bac-136"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="82bac-136"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82bac-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="82bac-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82bac-138">**итпартиЦипант**</span><span class="sxs-lookup"><span data-stu-id="82bac-138">**ITParticipant**</span></span>](itparticipant.md)
</dt> <dt>

[<span data-ttu-id="82bac-139">**енумератестреамс**</span><span class="sxs-lookup"><span data-stu-id="82bac-139">**EnumerateStreams**</span></span>](itparticipant-enumeratestreams.md)
</dt> <dt>

[<span data-ttu-id="82bac-140">**иенумстреам**</span><span class="sxs-lookup"><span data-stu-id="82bac-140">**IEnumStream**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-ienumstream)
</dt> <dt>

[<span data-ttu-id="82bac-141">**итколлектион**</span><span class="sxs-lookup"><span data-stu-id="82bac-141">**ITCollection**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itcollection)
</dt> <dt>

[<span data-ttu-id="82bac-142">**итстреам**</span><span class="sxs-lookup"><span data-stu-id="82bac-142">**ITStream**</span></span>](/windows/win32/api/tapi3if/nn-tapi3if-itstream)
</dt> </dl>

 

