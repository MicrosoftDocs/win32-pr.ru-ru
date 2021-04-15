---
description: Будет \_ Отправлено сообщение о кнопке телефона TAPI, чтобы уведомить приложение о том, что нажатие кнопки мониторинг включено, если обнаружено нажатие кнопки на локальном телефоне.
ms.assetid: fe47eed7-89d1-488b-b945-9e1aedc1f63c
title: Сообщение PHONE_BUTTON (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2da810630a937f8415e070373f359dca06a694e6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675740"
---
# <a name="phone_button-message"></a><span data-ttu-id="d476d-103">\_Сообщение кнопки телефона</span><span class="sxs-lookup"><span data-stu-id="d476d-103">PHONE\_BUTTON message</span></span>

<span data-ttu-id="d476d-104">Будет отправлено сообщение о **\_ кнопке телефона** TAPI, чтобы уведомить приложение о том, что нажатие кнопки мониторинг включено, если обнаружено нажатие кнопки на локальном телефоне.</span><span class="sxs-lookup"><span data-stu-id="d476d-104">The TAPI **PHONE\_BUTTON** message is sent to notify the application that button press monitoring is enabled if it has detected a button press on the local phone.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="d476d-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="d476d-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d476d-106">*хфоне*</span><span class="sxs-lookup"><span data-stu-id="d476d-106">*hPhone*</span></span> 
</dt> <dd>

<span data-ttu-id="d476d-107">Маркер телефонного устройства.</span><span class="sxs-lookup"><span data-stu-id="d476d-107">A handle to the phone device.</span></span>

</dd> <dt>

<span data-ttu-id="d476d-108">*двкаллбаккинстанце*</span><span class="sxs-lookup"><span data-stu-id="d476d-108">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="d476d-109">Экземпляр обратного вызова приложения, предоставленный при открытии телефонного устройства.</span><span class="sxs-lookup"><span data-stu-id="d476d-109">The application's callback instance provided when opening the phone device.</span></span>

</dd> <dt>

<span data-ttu-id="d476d-110">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="d476d-110">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="d476d-111">Идентификатор кнопки или лампы нажатой кнопки.</span><span class="sxs-lookup"><span data-stu-id="d476d-111">The button/lamp identifier of the button that was pressed.</span></span> <span data-ttu-id="d476d-112">Обратите внимание, что идентификаторы кнопок с нуля по 11 всегда являются кнопками с кнопками, где "0" — нулевой идентификатор кнопки, "1" — идентификатором кнопки 1 (и так далее через идентификатор Button 9), и с "" идентификатором кнопки, равным \* 10, и " \# " идентификатором кнопки 11.</span><span class="sxs-lookup"><span data-stu-id="d476d-112">Note that button identifiers zero through 11 are always the KEYPAD buttons, with '0' being button identifier zero, '1' being button identifier 1 (and so on through button identifier 9), and with '\*' being button identifier 10, and '\#' being button identifier 11.</span></span> <span data-ttu-id="d476d-113">Дополнительные сведения о идентификаторе кнопки доступны в [**фонежетдевкапс**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps) и [**фонежетбуттонинфо**](/windows/desktop/api/Tapi/nf-tapi-phonegetbuttoninfo).</span><span class="sxs-lookup"><span data-stu-id="d476d-113">Additional information about a button identifier is available with [**phoneGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps) and [**phoneGetButtonInfo**](/windows/desktop/api/Tapi/nf-tapi-phonegetbuttoninfo).</span></span>

</dd> <dt>

<span data-ttu-id="d476d-114">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="d476d-114">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="d476d-115">Режим кнопки кнопки.</span><span class="sxs-lookup"><span data-stu-id="d476d-115">The button mode of the button.</span></span> <span data-ttu-id="d476d-116">Этот параметр использует одну из [**\_ констант фонебуттонмоде**](phonebuttonmode--constants.md).</span><span class="sxs-lookup"><span data-stu-id="d476d-116">This parameter uses one of the [**PHONEBUTTONMODE\_ constants**](phonebuttonmode--constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="d476d-117">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="d476d-117">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="d476d-118">Указывает, является ли это событием кнопки или нажатием кнопки.</span><span class="sxs-lookup"><span data-stu-id="d476d-118">Specifies whether this is a button-down event or a button-up event.</span></span> <span data-ttu-id="d476d-119">Этот параметр использует одну из [**\_ констант фонебуттонстате**](phonebuttonstate--constants.md).</span><span class="sxs-lookup"><span data-stu-id="d476d-119">This parameter uses one of the [**PHONEBUTTONSTATE\_ constants**](phonebuttonstate--constants.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d476d-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d476d-120">Return value</span></span>

<span data-ttu-id="d476d-121">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="d476d-121">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d476d-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d476d-122">Remarks</span></span>

<span data-ttu-id="d476d-123">Сообщение **\_ кнопки телефона** отправляется при каждом изменении состояния кнопки.</span><span class="sxs-lookup"><span data-stu-id="d476d-123">A **PHONE\_BUTTON** message is sent whenever a button changes state.</span></span> <span data-ttu-id="d476d-124">Приложение гарантирует, что для каждого события нажатия кнопки в конечном итоге отправляется соответствующее событие кнопки up.</span><span class="sxs-lookup"><span data-stu-id="d476d-124">An application is guaranteed that for each button down event, it is eventually sent a corresponding button up event.</span></span> <span data-ttu-id="d476d-125">Поставщик услуг, который не способен обнаружить фактическую кнопку, должен создать сообщение кнопки вверх вскоре после сообщения нажатия кнопки.</span><span class="sxs-lookup"><span data-stu-id="d476d-125">A service provider that is incapable of detecting the actual button up is required to generate the button up message shortly after the button down message for each button press.</span></span>

## <a name="requirements"></a><span data-ttu-id="d476d-126">Требования</span><span class="sxs-lookup"><span data-stu-id="d476d-126">Requirements</span></span>



| <span data-ttu-id="d476d-127">Требование</span><span class="sxs-lookup"><span data-stu-id="d476d-127">Requirement</span></span> | <span data-ttu-id="d476d-128">Значение</span><span class="sxs-lookup"><span data-stu-id="d476d-128">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="d476d-129">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="d476d-129">TAPI version</span></span><br/> | <span data-ttu-id="d476d-130">Требуется TAPI 2,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="d476d-130">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="d476d-131">Header</span><span class="sxs-lookup"><span data-stu-id="d476d-131">Header</span></span><br/>       | <dl> <span data-ttu-id="d476d-132"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="d476d-132"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d476d-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d476d-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d476d-134">**фонежетбуттонинфо**</span><span class="sxs-lookup"><span data-stu-id="d476d-134">**phoneGetButtonInfo**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetbuttoninfo)
</dt> <dt>

[<span data-ttu-id="d476d-135">**фонежетдевкапс**</span><span class="sxs-lookup"><span data-stu-id="d476d-135">**phoneGetDevCaps**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps)
</dt> </dl>

 

 




