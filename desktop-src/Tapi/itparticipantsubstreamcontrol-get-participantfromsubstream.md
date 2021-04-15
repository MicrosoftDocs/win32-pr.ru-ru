---
description: Метод Get \_ партиЦипантфромсубстреам позволяет приложению обнаруживать, какие участники связаны с данным подпотоком.
ms.assetid: 0e42b4f0-d5b6-4b33-b7e5-dc525524ece7
title: 'Метод ИтпартиЦипантсубстреамконтрол:: get_ParticipantFromSubStream (Конфприв. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a507665e7f81339ce10961d69e08e76f60bb2be
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675940"
---
# <a name="itparticipantsubstreamcontrolget_participantfromsubstream-method"></a><span data-ttu-id="dc7e8-103">Метод ИтпартиЦипантсубстреамконтрол:: Get \_ партиЦипантфромсубстреам</span><span class="sxs-lookup"><span data-stu-id="dc7e8-103">ITParticipantSubStreamControl::get\_ParticipantFromSubStream method</span></span>

<span data-ttu-id="dc7e8-104">\[**получить \_ ПартиЦипантфромсубстреам** недоступен для использования в Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="dc7e8-104">\[**get\_ParticipantFromSubStream** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="dc7e8-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="dc7e8-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="dc7e8-106">Метод **Get \_ партиЦипантфромсубстреам** позволяет приложению обнаруживать, какие участники связаны с данным подпотоком.</span><span class="sxs-lookup"><span data-stu-id="dc7e8-106">The **get\_ParticipantFromSubStream** method allows an application to discover which participants are associated with a given substream.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc7e8-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dc7e8-107">Syntax</span></span>


```C++
HRESULT get_ParticipantFromSubStream(
  [in]  ITSubStream   *pITSubStream,
  [out] ITParticipant **ppParticipant
);
```



## <a name="parameters"></a><span data-ttu-id="dc7e8-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="dc7e8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc7e8-109">*питсубстреам* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dc7e8-109">*pITSubStream* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc7e8-110">Указатель на интерфейс [**итсубстреам**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream) .</span><span class="sxs-lookup"><span data-stu-id="dc7e8-110">Pointer to [**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream) interface.</span></span>

</dd> <dt>

<span data-ttu-id="dc7e8-111">*пппартиЦипант* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="dc7e8-111">*ppParticipant* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dc7e8-112">Указатель на массив указателей интерфейса [**итпартиЦипант**](itparticipant.md) .</span><span class="sxs-lookup"><span data-stu-id="dc7e8-112">Pointer to array of [**ITParticipant**](itparticipant.md) interface pointers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc7e8-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dc7e8-113">Return value</span></span>

<span data-ttu-id="dc7e8-114">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="dc7e8-114">This method can return one of these values.</span></span>



| <span data-ttu-id="dc7e8-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="dc7e8-115">Return code</span></span>                                                                                     | <span data-ttu-id="dc7e8-116">Описание</span><span class="sxs-lookup"><span data-stu-id="dc7e8-116">Description</span></span>                                                                        |
|-------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="dc7e8-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="dc7e8-117"><dt>**S\_OK**</dt></span></span> </dl>            | <span data-ttu-id="dc7e8-118">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="dc7e8-118">Method succeeded.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="dc7e8-119"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="dc7e8-119"><dt>**E\_POINTER**</dt></span></span> </dl>       | <span data-ttu-id="dc7e8-120">Параметр *питсубстреам* или *пппартиЦипант* не является допустимым указателем.</span><span class="sxs-lookup"><span data-stu-id="dc7e8-120">The *pITSubStream* or *ppParticipant* parameter is not a valid pointer.</span></span><br/> |
| <dl> <span data-ttu-id="dc7e8-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="dc7e8-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>    | <span data-ttu-id="dc7e8-122">Параметр *питсубстреам* не указывает на допустимый интерфейс.</span><span class="sxs-lookup"><span data-stu-id="dc7e8-122">The *pITSubStream* parameter does not point to valid interface.</span></span><br/>         |
| <dl> <span data-ttu-id="dc7e8-123"><dt>**\_нежелательные \_ элементы TAPI**</dt></span><span class="sxs-lookup"><span data-stu-id="dc7e8-123"><dt>**TAPI\_E\_NOITEMS**</dt></span></span> </dl> | <span data-ttu-id="dc7e8-124">Нет участников, связанных с подпотоком.</span><span class="sxs-lookup"><span data-stu-id="dc7e8-124">There are no participants associated with the substream.</span></span><br/>                |
| <dl> <span data-ttu-id="dc7e8-125"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="dc7e8-125"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>   | <span data-ttu-id="dc7e8-126">Недостаточно памяти для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="dc7e8-126">Insufficient memory exists to perform the operation.</span></span><br/>                    |



 

## <a name="requirements"></a><span data-ttu-id="dc7e8-127">Требования</span><span class="sxs-lookup"><span data-stu-id="dc7e8-127">Requirements</span></span>



| <span data-ttu-id="dc7e8-128">Требование</span><span class="sxs-lookup"><span data-stu-id="dc7e8-128">Requirement</span></span> | <span data-ttu-id="dc7e8-129">Значение</span><span class="sxs-lookup"><span data-stu-id="dc7e8-129">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dc7e8-130">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="dc7e8-130">TAPI version</span></span><br/> | <span data-ttu-id="dc7e8-131">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="dc7e8-131">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="dc7e8-132">Header</span><span class="sxs-lookup"><span data-stu-id="dc7e8-132">Header</span></span><br/>       | <dl> <span data-ttu-id="dc7e8-133"><dt>Конфприв. h</dt></span><span class="sxs-lookup"><span data-stu-id="dc7e8-133"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="dc7e8-134">Библиотека</span><span class="sxs-lookup"><span data-stu-id="dc7e8-134">Library</span></span><br/>      | <dl> <span data-ttu-id="dc7e8-135"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dc7e8-135"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="dc7e8-136">DLL</span><span class="sxs-lookup"><span data-stu-id="dc7e8-136">DLL</span></span><br/>          | <dl> <span data-ttu-id="dc7e8-137"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dc7e8-137"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="dc7e8-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dc7e8-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc7e8-139">**итпартиЦипантсубстреамконтрол**</span><span class="sxs-lookup"><span data-stu-id="dc7e8-139">**ITParticipantSubStreamControl**</span></span>](itparticipantsubstreamcontrol.md)
</dt> <dt>

[<span data-ttu-id="dc7e8-140">**итпартиЦипант**</span><span class="sxs-lookup"><span data-stu-id="dc7e8-140">**ITParticipant**</span></span>](itparticipant.md)
</dt> <dt>

[<span data-ttu-id="dc7e8-141">**итсубстреам**</span><span class="sxs-lookup"><span data-stu-id="dc7e8-141">**ITSubStream**</span></span>](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream)
</dt> </dl>

 

