---
description: Метод Свитчтерминалтосубстреам задает терминал для подпотока участника.
ms.assetid: 39e1d4b9-2e39-4b36-9a6a-89e41cd59153
title: 'Метод ИтпартиЦипантсубстреамконтрол:: Свитчтерминалтосубстреам (Конфприв. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00f10401b2cf1598c76537ebd3a7049d67bf0657
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680057"
---
# <a name="itparticipantsubstreamcontrolswitchterminaltosubstream-method"></a><span data-ttu-id="7da61-103">Метод ИтпартиЦипантсубстреамконтрол:: Свитчтерминалтосубстреам</span><span class="sxs-lookup"><span data-stu-id="7da61-103">ITParticipantSubStreamControl::SwitchTerminalToSubStream method</span></span>

<span data-ttu-id="7da61-104">\[**Свитчтерминалтосубстреам** недоступен для использования в Windows Vista, windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="7da61-104">\[**SwitchTerminalToSubStream** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="7da61-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="7da61-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="7da61-106">Метод **свитчтерминалтосубстреам** задает терминал для подпотока участника.</span><span class="sxs-lookup"><span data-stu-id="7da61-106">The **SwitchTerminalToSubStream** method sets a terminal to the participant substream.</span></span>

## <a name="syntax"></a><span data-ttu-id="7da61-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7da61-107">Syntax</span></span>


```C++
HRESULT SwitchTerminalToSubStream(
  [in] ITTerminal  *pITTerminal,
  [in] ITSubStream *pITSubStream
);
```



## <a name="parameters"></a><span data-ttu-id="7da61-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="7da61-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7da61-109">*питтерминал* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7da61-109">*pITTerminal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7da61-110">Указатель на интерфейс [**иттерминал**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) .</span><span class="sxs-lookup"><span data-stu-id="7da61-110">Pointer to [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) interface.</span></span>

</dd> <dt>

<span data-ttu-id="7da61-111">*питсубстреам* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7da61-111">*pITSubStream* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7da61-112">Указатель на интерфейс [**итсубстреам**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream) .</span><span class="sxs-lookup"><span data-stu-id="7da61-112">Pointer to [**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7da61-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7da61-113">Return value</span></span>

<span data-ttu-id="7da61-114">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="7da61-114">This method can return one of these values.</span></span>



| <span data-ttu-id="7da61-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="7da61-115">Return code</span></span>                                                                                     | <span data-ttu-id="7da61-116">Описание</span><span class="sxs-lookup"><span data-stu-id="7da61-116">Description</span></span>                                                                                        |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7da61-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="7da61-117"><dt>**S\_OK**</dt></span></span> </dl>            | <span data-ttu-id="7da61-118">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="7da61-118">Method succeeded.</span></span><br/>                                                                       |
| <dl> <span data-ttu-id="7da61-119"><dt>**\_непредвиденная E**</dt></span><span class="sxs-lookup"><span data-stu-id="7da61-119"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>    | <span data-ttu-id="7da61-120">Не удалось получить доступ к сведениям о участнике для потока.</span><span class="sxs-lookup"><span data-stu-id="7da61-120">Participant information for the stream could not be accessed.</span></span><br/>                           |
| <dl> <span data-ttu-id="7da61-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="7da61-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>    | <span data-ttu-id="7da61-122">Параметр *ппартиЦипант* или *питсубстреам* не указывает на допустимый интерфейс.</span><span class="sxs-lookup"><span data-stu-id="7da61-122">The *pParticipant* or the *pITSubStream* parameter does not point to a valid interface.</span></span><br/> |
| <dl> <span data-ttu-id="7da61-123"><dt>**\_нежелательные \_ элементы TAPI**</dt></span><span class="sxs-lookup"><span data-stu-id="7da61-123"><dt>**TAPI\_E\_NOITEMS**</dt></span></span> </dl> | <span data-ttu-id="7da61-124">Подпоток не готов.</span><span class="sxs-lookup"><span data-stu-id="7da61-124">The substream is not ready.</span></span><br/>                                                             |
| <dl> <span data-ttu-id="7da61-125"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="7da61-125"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>   | <span data-ttu-id="7da61-126">Недостаточно памяти для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="7da61-126">Insufficient memory exists to perform the operation.</span></span><br/>                                    |



 

## <a name="requirements"></a><span data-ttu-id="7da61-127">Требования</span><span class="sxs-lookup"><span data-stu-id="7da61-127">Requirements</span></span>



| <span data-ttu-id="7da61-128">Требование</span><span class="sxs-lookup"><span data-stu-id="7da61-128">Requirement</span></span> | <span data-ttu-id="7da61-129">Значение</span><span class="sxs-lookup"><span data-stu-id="7da61-129">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7da61-130">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="7da61-130">TAPI version</span></span><br/> | <span data-ttu-id="7da61-131">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="7da61-131">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="7da61-132">Header</span><span class="sxs-lookup"><span data-stu-id="7da61-132">Header</span></span><br/>       | <dl> <span data-ttu-id="7da61-133"><dt>Конфприв. h</dt></span><span class="sxs-lookup"><span data-stu-id="7da61-133"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="7da61-134">Библиотека</span><span class="sxs-lookup"><span data-stu-id="7da61-134">Library</span></span><br/>      | <dl> <span data-ttu-id="7da61-135"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7da61-135"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="7da61-136">DLL</span><span class="sxs-lookup"><span data-stu-id="7da61-136">DLL</span></span><br/>          | <dl> <span data-ttu-id="7da61-137"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7da61-137"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="7da61-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7da61-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7da61-139">**итпартиЦипантсубстреамконтрол**</span><span class="sxs-lookup"><span data-stu-id="7da61-139">**ITParticipantSubStreamControl**</span></span>](itparticipantsubstreamcontrol.md)
</dt> <dt>

[<span data-ttu-id="7da61-140">**итпартиЦипант**</span><span class="sxs-lookup"><span data-stu-id="7da61-140">**ITParticipant**</span></span>](itparticipant.md)
</dt> <dt>

[<span data-ttu-id="7da61-141">**итсубстреам**</span><span class="sxs-lookup"><span data-stu-id="7da61-141">**ITSubStream**</span></span>](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream)
</dt> <dt>

[<span data-ttu-id="7da61-142">**иттерминал**</span><span class="sxs-lookup"><span data-stu-id="7da61-142">**ITTerminal**</span></span>](/windows/win32/api/tapi3if/nn-tapi3if-itterminal)
</dt> </dl>

 

