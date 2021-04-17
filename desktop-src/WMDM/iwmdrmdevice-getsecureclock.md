---
title: Ивмдрмдевице Жетсекуреклокк, метод
description: Метод Жетсекуреклокк извлекает безопасное время, поэтому лицензии на основе времени можно применить.
ms.assetid: 6de9b7ce-9c2a-44e5-9de7-40cfbaf4d92c
keywords:
- Метод Жетсекуреклокк Windows Media диспетчер устройств
- Метод Жетсекуреклокк Windows Media диспетчер устройств, интерфейс Ивмдрмдевице
- Интерфейс Ивмдрмдевице Windows Media диспетчер устройств, метод Жетсекуреклокк
topic_type:
- apiref
api_name:
- IWMDRMDevice.GetSecureClock
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aaa92c3bc2ee82facf2f2e1043e71467a0c55bd8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694418"
---
# <a name="iwmdrmdevicegetsecureclock-method"></a><span data-ttu-id="d46fc-106">Метод Ивмдрмдевице:: Жетсекуреклокк</span><span class="sxs-lookup"><span data-stu-id="d46fc-106">IWMDRMDevice::GetSecureClock method</span></span>

<span data-ttu-id="d46fc-107">Метод **жетсекуреклокк** извлекает безопасное время, поэтому лицензии на основе времени можно применить.</span><span class="sxs-lookup"><span data-stu-id="d46fc-107">The **GetSecureClock** method retrieves the secure clock, so time-based licenses can be enforced.</span></span>

## <a name="syntax"></a><span data-ttu-id="d46fc-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d46fc-108">Syntax</span></span>


```C++
HRESULT GetSecureClock(
  [out] BYTE  **ppbSecureClock,
  [out] DWORD *pcbSecureClock,
  [out] DWORD *pdwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="d46fc-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="d46fc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d46fc-110">*ппбсекуреклокк* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="d46fc-110">*ppbSecureClock* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d46fc-111">Получены безопасные часы.</span><span class="sxs-lookup"><span data-stu-id="d46fc-111">Retrieved secure clock.</span></span>

</dd> <dt>

<span data-ttu-id="d46fc-112">*пкбсекуреклокк* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="d46fc-112">*pcbSecureClock* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d46fc-113">Размер безопасного времени в байтах.</span><span class="sxs-lookup"><span data-stu-id="d46fc-113">Size of the secure clock, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="d46fc-114">*пдвфлагс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="d46fc-114">*pdwFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d46fc-115">Флаги состояния устройства.</span><span class="sxs-lookup"><span data-stu-id="d46fc-115">Device status flags.</span></span> <span data-ttu-id="d46fc-116">Это значение должно быть одним из следующих флагов.</span><span class="sxs-lookup"><span data-stu-id="d46fc-116">This value must be one of the following flags.</span></span>



| <span data-ttu-id="d46fc-117">Flag</span><span class="sxs-lookup"><span data-stu-id="d46fc-117">Flag</span></span>                     | <span data-ttu-id="d46fc-118">Описание</span><span class="sxs-lookup"><span data-stu-id="d46fc-118">Description</span></span>                            |
|--------------------------|----------------------------------------|
| <span data-ttu-id="d46fc-119">\_исвмдрм устройства \_ WMDRM</span><span class="sxs-lookup"><span data-stu-id="d46fc-119">WMDRM\_DEVICE\_ISWMDRM</span></span>   | <span data-ttu-id="d46fc-120">Устройство поддерживает Windows Media DRM.</span><span class="sxs-lookup"><span data-stu-id="d46fc-120">The device supports Windows Media DRM.</span></span> |
| <span data-ttu-id="d46fc-121">\_нидклокк устройства \_ WMDRM</span><span class="sxs-lookup"><span data-stu-id="d46fc-121">WMDRM\_DEVICE\_NEEDCLOCK</span></span> | <span data-ttu-id="d46fc-122">Устройству требуется таймер.</span><span class="sxs-lookup"><span data-stu-id="d46fc-122">The device needs clock.</span></span>                |
| <span data-ttu-id="d46fc-123">\_устройство WMDRM \_ отозвано</span><span class="sxs-lookup"><span data-stu-id="d46fc-123">WMDRM\_DEVICE\_REVOKED</span></span>   | <span data-ttu-id="d46fc-124">Устройство было отозвано.</span><span class="sxs-lookup"><span data-stu-id="d46fc-124">The device has been revoked.</span></span>           |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d46fc-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d46fc-125">Return value</span></span>

<span data-ttu-id="d46fc-126">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="d46fc-126">The method returns an **HRESULT**.</span></span> <span data-ttu-id="d46fc-127">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="d46fc-127">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="d46fc-128">Код возврата</span><span class="sxs-lookup"><span data-stu-id="d46fc-128">Return code</span></span>                                                                          | <span data-ttu-id="d46fc-129">Описание</span><span class="sxs-lookup"><span data-stu-id="d46fc-129">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="d46fc-130"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="d46fc-130"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="d46fc-131">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="d46fc-131">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="d46fc-132">Требования</span><span class="sxs-lookup"><span data-stu-id="d46fc-132">Requirements</span></span>



| <span data-ttu-id="d46fc-133">Требование</span><span class="sxs-lookup"><span data-stu-id="d46fc-133">Requirement</span></span> | <span data-ttu-id="d46fc-134">Значение</span><span class="sxs-lookup"><span data-stu-id="d46fc-134">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d46fc-135">Header</span><span class="sxs-lookup"><span data-stu-id="d46fc-135">Header</span></span><br/>  | <dl> <span data-ttu-id="d46fc-136"><dt>ВМДДРМСП. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d46fc-136"><dt>WMDDRMSP.idl</dt></span></span> </dl> |
| <span data-ttu-id="d46fc-137">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d46fc-137">Library</span></span><br/> | <dl> <span data-ttu-id="d46fc-138"><dt>Мссачлп. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d46fc-138"><dt>Mssachlp.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d46fc-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d46fc-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d46fc-140">**жетсекуреклоккчалленже**</span><span class="sxs-lookup"><span data-stu-id="d46fc-140">**GetSecureClockChallenge**</span></span>](iwmdrmdevice-getsecureclockchallenge.md)
</dt> <dt>

[<span data-ttu-id="d46fc-141">**Интерфейс Ивмдрмдевице**</span><span class="sxs-lookup"><span data-stu-id="d46fc-141">**IWMDRMDevice Interface**</span></span>](iwmdrmdevice.md)
</dt> <dt>

[<span data-ttu-id="d46fc-142">**сетсекуреклоккреспонсе**</span><span class="sxs-lookup"><span data-stu-id="d46fc-142">**SetSecureClockResponse**</span></span>](iwmdrmdevice-setsecureclockresponse.md)
</dt> </dl>

 

 





