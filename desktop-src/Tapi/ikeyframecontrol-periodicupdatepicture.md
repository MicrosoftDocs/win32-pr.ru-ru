---
description: Метод Периодикупдатепиктуре вызывается приложением для настройки таймера в потоке, который будет периодически запрашивать обновления изображений. Обновления изображений приводят к использованию высокой пропускной способности, поэтому этот метод обычно используется вместо Упдатепиктуре.
ms.assetid: 6ae3b5e9-bc11-4f3f-972b-21c9ac299987
title: 'Икэйфрамеконтрол: метод:P Ериодикупдатепиктуре (H323priv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50bbfb18b0be96d611f0fe385cc825602dc316ad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685123"
---
# <a name="ikeyframecontrolperiodicupdatepicture-method"></a><span data-ttu-id="1589e-104">Икэйфрамеконтрол: метод:P Ериодикупдатепиктуре</span><span class="sxs-lookup"><span data-stu-id="1589e-104">IKeyFrameControl::PeriodicUpdatePicture method</span></span>

<span data-ttu-id="1589e-105">\[**Периодикупдатепиктуре** недоступен для использования в Windows Vista, windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="1589e-105">\[**PeriodicUpdatePicture** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="1589e-106">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="1589e-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="1589e-107">Метод **периодикупдатепиктуре** вызывается приложением для настройки таймера в потоке, который будет периодически запрашивать обновления изображений.</span><span class="sxs-lookup"><span data-stu-id="1589e-107">The **PeriodicUpdatePicture** method is called by an application to configure a timer in the stream that will ask for picture updates periodically.</span></span> <span data-ttu-id="1589e-108">Обновления изображений приводят к использованию высокой пропускной способности, поэтому этот метод обычно используется вместо [**упдатепиктуре**](ikeyframecontrol-updatepicture.md).</span><span class="sxs-lookup"><span data-stu-id="1589e-108">Picture updates cause high bandwidth usage, so this method will normally be used instead of [**UpdatePicture**](ikeyframecontrol-updatepicture.md).</span></span>

<span data-ttu-id="1589e-109">Если метод вызывается, когда поток активен, таймер запустится немедленно.</span><span class="sxs-lookup"><span data-stu-id="1589e-109">If the method is called when the stream is active, the timer will start immediately.</span></span> <span data-ttu-id="1589e-110">Если поток неактивен, таймер будет запущен, когда поток войдет в активное состояние.</span><span class="sxs-lookup"><span data-stu-id="1589e-110">If the stream is not active, the timer will be started when the stream enters the active state.</span></span>

## <a name="syntax"></a><span data-ttu-id="1589e-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1589e-111">Syntax</span></span>


```C++
HRESULT PeriodicUpdatePicture(
  [in] BOOL  fEnable,
  [in] DWORD dwInterval
);
```



## <a name="parameters"></a><span data-ttu-id="1589e-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="1589e-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1589e-113">*фенабле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1589e-113">*fEnable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1589e-114">**Значение true** включает таймер.</span><span class="sxs-lookup"><span data-stu-id="1589e-114">**TRUE** enables the timer.</span></span> <span data-ttu-id="1589e-115">**Значение false** отключает его.</span><span class="sxs-lookup"><span data-stu-id="1589e-115">**FALSE** disables it.</span></span>

</dd> <dt>

<span data-ttu-id="1589e-116">*двинтервал* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1589e-116">*dwInterval* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1589e-117">Интервал времени для таймера в секундах.</span><span class="sxs-lookup"><span data-stu-id="1589e-117">The interval for the timer, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1589e-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1589e-118">Return value</span></span>

<span data-ttu-id="1589e-119">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="1589e-119">This method can return one of these values.</span></span>



| <span data-ttu-id="1589e-120">Код возврата</span><span class="sxs-lookup"><span data-stu-id="1589e-120">Return code</span></span>                                                                            | <span data-ttu-id="1589e-121">Описание</span><span class="sxs-lookup"><span data-stu-id="1589e-121">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="1589e-122"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="1589e-122"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="1589e-123">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="1589e-123">Method succeeded.</span></span><br/>              |
| <dl> <span data-ttu-id="1589e-124"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="1589e-124"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="1589e-125">Сбой по непредвиденным причинам.</span><span class="sxs-lookup"><span data-stu-id="1589e-125">Failed for unexpected reasons.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="1589e-126">Требования</span><span class="sxs-lookup"><span data-stu-id="1589e-126">Requirements</span></span>



| <span data-ttu-id="1589e-127">Требование</span><span class="sxs-lookup"><span data-stu-id="1589e-127">Requirement</span></span> | <span data-ttu-id="1589e-128">Значение</span><span class="sxs-lookup"><span data-stu-id="1589e-128">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1589e-129">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="1589e-129">TAPI version</span></span><br/> | <span data-ttu-id="1589e-130">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="1589e-130">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="1589e-131">Header</span><span class="sxs-lookup"><span data-stu-id="1589e-131">Header</span></span><br/>       | <dl> <span data-ttu-id="1589e-132"><dt>H323priv. h</dt></span><span class="sxs-lookup"><span data-stu-id="1589e-132"><dt>H323priv.h</dt></span></span> </dl> |
| <span data-ttu-id="1589e-133">Библиотека</span><span class="sxs-lookup"><span data-stu-id="1589e-133">Library</span></span><br/>      | <dl> <span data-ttu-id="1589e-134"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1589e-134"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="1589e-135">DLL</span><span class="sxs-lookup"><span data-stu-id="1589e-135">DLL</span></span><br/>          | <dl> <span data-ttu-id="1589e-136"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1589e-136"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="1589e-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1589e-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1589e-138">H323 MSP</span><span class="sxs-lookup"><span data-stu-id="1589e-138">H323 MSP</span></span>](h323-msp.md)
</dt> </dl>

 

 




