---
description: Метод размещения \_ состояния задает состояние участника.
ms.assetid: 8478fcf4-00b3-4b77-9859-e5a80ce24be1
title: 'ИтпартиЦипант: метод ut_Status:p (Ипмсп. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82eadc9832105ecb0cf440b070dbff8b3fe658d1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105688810"
---
# <a name="itparticipantput_status-method"></a><span data-ttu-id="52722-103">ИтпартиЦипант: \_ метод состояния:p UT</span><span class="sxs-lookup"><span data-stu-id="52722-103">ITParticipant::put\_Status method</span></span>

<span data-ttu-id="52722-104">\[**Размещение \_ Состояние** недоступно для использования в Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="52722-104">\[**put\_Status** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="52722-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="52722-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="52722-106">Метод **размещения \_ состояния** задает состояние участника.</span><span class="sxs-lookup"><span data-stu-id="52722-106">The **put\_Status** method sets the status of a participant.</span></span>

## <a name="syntax"></a><span data-ttu-id="52722-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="52722-107">Syntax</span></span>


```C++
HRESULT put_Status(
  [in] ITStream     *pITStream,
  [in] VARIANT_BOOL fEnable
);
```



## <a name="parameters"></a><span data-ttu-id="52722-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="52722-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52722-109">*питстреам* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="52722-109">*pITStream* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52722-110">Указатель на интерфейс [**итстреам**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) .</span><span class="sxs-lookup"><span data-stu-id="52722-110">Pointer to [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) interface.</span></span>

</dd> <dt>

<span data-ttu-id="52722-111">*фенабле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="52722-111">*fEnable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52722-112">ВАРИАНТ \_ true, если участник включен в потоке, вариант \_ false, если он должен быть отключен.</span><span class="sxs-lookup"><span data-stu-id="52722-112">VARIANT\_TRUE if the participant is enabled on the stream, VARIANT\_FALSE if it is to be disabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52722-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="52722-113">Return value</span></span>

<span data-ttu-id="52722-114">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="52722-114">This method can return one of these values.</span></span>



| <span data-ttu-id="52722-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="52722-115">Return code</span></span>                                                                                   | <span data-ttu-id="52722-116">Описание</span><span class="sxs-lookup"><span data-stu-id="52722-116">Description</span></span>                                                               |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="52722-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="52722-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="52722-118">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="52722-118">Method succeeded.</span></span><br/>                                              |
| <dl> <span data-ttu-id="52722-119"><dt>**E \_ нотимпл**</dt></span><span class="sxs-lookup"><span data-stu-id="52722-119"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="52722-120">Метод не реализован.</span><span class="sxs-lookup"><span data-stu-id="52722-120">Method not implemented.</span></span><br/>                                        |
| <dl> <span data-ttu-id="52722-121"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="52722-121"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="52722-122">Параметр *питстреам* не является допустимым указателем.</span><span class="sxs-lookup"><span data-stu-id="52722-122">The *pITStream* parameter is not a valid pointer.</span></span><br/>              |
| <dl> <span data-ttu-id="52722-123"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="52722-123"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="52722-124">Параметр *питстреам* не указывает на допустимый интерфейс.</span><span class="sxs-lookup"><span data-stu-id="52722-124">The *pITStream* parameter does not point to a valid interface.</span></span><br/> |
| <dl> <span data-ttu-id="52722-125"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="52722-125"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="52722-126">Недостаточно памяти для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="52722-126">Insufficient memory exists to perform the operation.</span></span><br/>           |



 

## <a name="remarks"></a><span data-ttu-id="52722-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="52722-127">Remarks</span></span>

<span data-ttu-id="52722-128">Включение или отключение состояния участника в потоке позволяет приложению по сути отключать данного участника.</span><span class="sxs-lookup"><span data-stu-id="52722-128">Enabling or disabling a participant's status on a stream allows an application to essentially mute a given participant.</span></span>

## <a name="requirements"></a><span data-ttu-id="52722-129">Требования</span><span class="sxs-lookup"><span data-stu-id="52722-129">Requirements</span></span>



| <span data-ttu-id="52722-130">Требование</span><span class="sxs-lookup"><span data-stu-id="52722-130">Requirement</span></span> | <span data-ttu-id="52722-131">Значение</span><span class="sxs-lookup"><span data-stu-id="52722-131">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="52722-132">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="52722-132">TAPI version</span></span><br/> | <span data-ttu-id="52722-133">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="52722-133">Requires TAPI 3.0 or later</span></span><br/>                                                |
| <span data-ttu-id="52722-134">Header</span><span class="sxs-lookup"><span data-stu-id="52722-134">Header</span></span><br/>       | <dl> <span data-ttu-id="52722-135"><dt>Ипмсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="52722-135"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="52722-136">Библиотека</span><span class="sxs-lookup"><span data-stu-id="52722-136">Library</span></span><br/>      | <dl> <span data-ttu-id="52722-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="52722-137"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="52722-138">DLL</span><span class="sxs-lookup"><span data-stu-id="52722-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="52722-139"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="52722-139"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52722-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="52722-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52722-141">**итпартиЦипант**</span><span class="sxs-lookup"><span data-stu-id="52722-141">**ITParticipant**</span></span>](itparticipant.md)
</dt> <dt>

[<span data-ttu-id="52722-142">**итстреам**</span><span class="sxs-lookup"><span data-stu-id="52722-142">**ITStream**</span></span>](/windows/win32/api/tapi3if/nn-tapi3if-itstream)
</dt> <dt>

[<span data-ttu-id="52722-143">**получение \_ состояния**</span><span class="sxs-lookup"><span data-stu-id="52722-143">**get\_Status**</span></span>](itparticipant-get-status.md)
</dt> </dl>

 

