---
description: Метод Get \_ Status ВОЗВРАЩАЕТ тип Variant \_ bool, указывающий состояние участника.
ms.assetid: 03ad763b-5223-41b5-b0cf-1f13c761f5c2
title: 'Метод ИтпартиЦипант:: get_Status (Ипмсп. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2de39ac0833f856e35cc120b4f4e5b00bcd617de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675486"
---
# <a name="itparticipantget_status-method"></a><span data-ttu-id="2c4a8-103">Метод ИтпартиЦипант:: Get \_ status</span><span class="sxs-lookup"><span data-stu-id="2c4a8-103">ITParticipant::get\_Status method</span></span>

<span data-ttu-id="2c4a8-104">\[**получить \_ Состояние** недоступно для использования в Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="2c4a8-104">\[**get\_Status** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="2c4a8-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="2c4a8-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="2c4a8-106">Метод **Get \_ Status** Возвращает тип Variant \_ bool, указывающий состояние участника.</span><span class="sxs-lookup"><span data-stu-id="2c4a8-106">The **get\_Status** method returns a VARIANT\_BOOL indicating participant status.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c4a8-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2c4a8-107">Syntax</span></span>


```C++
HRESULT get_Status(
  [in]  ITStream     *pITStream,
  [out] VARIANT_BOOL *pStatus
);
```



## <a name="parameters"></a><span data-ttu-id="2c4a8-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="2c4a8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c4a8-109">*питстреам* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2c4a8-109">*pITStream* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c4a8-110">Указатель на интерфейс [**итстреам**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) .</span><span class="sxs-lookup"><span data-stu-id="2c4a8-110">Pointer to [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) interface.</span></span>

</dd> <dt>

<span data-ttu-id="2c4a8-111">*пстатус* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="2c4a8-111">*pStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2c4a8-112">ВАРИАНТ \_ true, если участник включен в потоке, вариант \_ false, если он отключен.</span><span class="sxs-lookup"><span data-stu-id="2c4a8-112">VARIANT\_TRUE if the participant is enabled on the stream, VARIANT\_FALSE if it is disabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c4a8-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2c4a8-113">Return value</span></span>

<span data-ttu-id="2c4a8-114">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="2c4a8-114">This method can return one of these values.</span></span>



| <span data-ttu-id="2c4a8-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="2c4a8-115">Return code</span></span>                                                                                   | <span data-ttu-id="2c4a8-116">Описание</span><span class="sxs-lookup"><span data-stu-id="2c4a8-116">Description</span></span>                                                               |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2c4a8-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="2c4a8-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="2c4a8-118">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="2c4a8-118">Method succeeded.</span></span><br/>                                              |
| <dl> <span data-ttu-id="2c4a8-119"><dt>**E \_ нотимпл**</dt></span><span class="sxs-lookup"><span data-stu-id="2c4a8-119"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="2c4a8-120">Метод не реализован.</span><span class="sxs-lookup"><span data-stu-id="2c4a8-120">Method not implemented.</span></span><br/>                                        |
| <dl> <span data-ttu-id="2c4a8-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="2c4a8-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="2c4a8-122">Недостаточно памяти для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="2c4a8-122">Insufficient memory exists to perform the operation.</span></span><br/>           |
| <dl> <span data-ttu-id="2c4a8-123"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="2c4a8-123"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="2c4a8-124">Параметр *питстреам* не является допустимым указателем.</span><span class="sxs-lookup"><span data-stu-id="2c4a8-124">The *pITStream* parameter is not a valid pointer.</span></span><br/>              |
| <dl> <span data-ttu-id="2c4a8-125"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="2c4a8-125"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="2c4a8-126">Параметр *питстреам* не указывает на допустимый интерфейс.</span><span class="sxs-lookup"><span data-stu-id="2c4a8-126">The *pITStream* parameter does not point to a valid interface.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2c4a8-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2c4a8-127">Remarks</span></span>

<span data-ttu-id="2c4a8-128">Включение или отключение состояния участника в потоке позволяет приложению по сути отключать данного участника.</span><span class="sxs-lookup"><span data-stu-id="2c4a8-128">Enabling or disabling a participant's status on a stream allows an application to essentially mute a given participant.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c4a8-129">Требования</span><span class="sxs-lookup"><span data-stu-id="2c4a8-129">Requirements</span></span>



| <span data-ttu-id="2c4a8-130">Требование</span><span class="sxs-lookup"><span data-stu-id="2c4a8-130">Requirement</span></span> | <span data-ttu-id="2c4a8-131">Значение</span><span class="sxs-lookup"><span data-stu-id="2c4a8-131">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="2c4a8-132">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="2c4a8-132">TAPI version</span></span><br/> | <span data-ttu-id="2c4a8-133">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="2c4a8-133">Requires TAPI 3.0 or later</span></span><br/>                                                |
| <span data-ttu-id="2c4a8-134">Header</span><span class="sxs-lookup"><span data-stu-id="2c4a8-134">Header</span></span><br/>       | <dl> <span data-ttu-id="2c4a8-135"><dt>Ипмсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="2c4a8-135"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="2c4a8-136">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2c4a8-136">Library</span></span><br/>      | <dl> <span data-ttu-id="2c4a8-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2c4a8-137"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="2c4a8-138">DLL</span><span class="sxs-lookup"><span data-stu-id="2c4a8-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="2c4a8-139"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2c4a8-139"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c4a8-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2c4a8-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c4a8-141">**итпартиЦипант**</span><span class="sxs-lookup"><span data-stu-id="2c4a8-141">**ITParticipant**</span></span>](itparticipant.md)
</dt> <dt>

[<span data-ttu-id="2c4a8-142">**итстреам**</span><span class="sxs-lookup"><span data-stu-id="2c4a8-142">**ITStream**</span></span>](/windows/win32/api/tapi3if/nn-tapi3if-itstream)
</dt> <dt>

[<span data-ttu-id="2c4a8-143">**\_состояние размещения**</span><span class="sxs-lookup"><span data-stu-id="2c4a8-143">**put\_Status**</span></span>](itparticipant-put-status.md)
</dt> </dl>

 

