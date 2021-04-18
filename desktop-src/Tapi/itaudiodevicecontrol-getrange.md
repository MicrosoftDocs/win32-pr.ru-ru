---
description: Метод дальнего действия извлекает диапазон допустимых значений для заданного свойства звукового устройства.
ms.assetid: df8985f4-8153-4f32-a90c-a5eb7c76b3c7
title: Метод Итаудиодевицеконтрол::-Range (Ипмсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cbf5bf36d4ec754440e1612f2e228c495d165c0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675019"
---
# <a name="itaudiodevicecontrolgetrange-method"></a><span data-ttu-id="a511d-103">Метод Итаудиодевицеконтрол:: Range</span><span class="sxs-lookup"><span data-stu-id="a511d-103">ITAudioDeviceControl::GetRange method</span></span>

<span data-ttu-id="a511d-104">\[ Этот метод недоступен для использования в Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="a511d-104">\[ This method is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="a511d-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="a511d-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="a511d-106">Метод **дальнего действия** извлекает диапазон допустимых значений для заданного [**Свойства звукового устройства**](audiodeviceproperty.md).</span><span class="sxs-lookup"><span data-stu-id="a511d-106">The **GetRange** method retrieves the range of valid values for a given [**audio device property**](audiodeviceproperty.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="a511d-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a511d-107">Syntax</span></span>


```C++
HRESULT get_Terminal(
  [out] ITTerminal **ppTerminal
);
```



## <a name="parameters"></a><span data-ttu-id="a511d-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="a511d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a511d-109">*Свойство* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a511d-109">*Property* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a511d-110">Член перечисления [**аудиодевицепроперти**](audiodeviceproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="a511d-110">Member of the [**AudioDeviceProperty**](audiodeviceproperty.md) enum.</span></span>

</dd> <dt>

<span data-ttu-id="a511d-111">*плмин* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="a511d-111">*plMin* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a511d-112">Минимальное допустимое значение для входного свойства.</span><span class="sxs-lookup"><span data-stu-id="a511d-112">Minimum valid value for the input property.</span></span>

</dd> <dt>

<span data-ttu-id="a511d-113">*плмакс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="a511d-113">*plMax* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a511d-114">Максимальное допустимое значение для входного свойства.</span><span class="sxs-lookup"><span data-stu-id="a511d-114">Maximum valid value for the input property.</span></span>

</dd> <dt>

<span data-ttu-id="a511d-115">*плстеппингделта* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="a511d-115">*plSteppingDelta* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a511d-116">Шаг приращения, на который может увеличиться или уменьшиться значение свойства.</span><span class="sxs-lookup"><span data-stu-id="a511d-116">Increment by which the property value can be increased or decreased.</span></span>

</dd> <dt>

<span data-ttu-id="a511d-117">*плдефаулт* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="a511d-117">*plDefault* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a511d-118">Значение по умолчанию для параметра *Property* .</span><span class="sxs-lookup"><span data-stu-id="a511d-118">Default value for the *Property* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="a511d-119">*плфлагс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="a511d-119">*plFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a511d-120">Значение перечисления [**тапиконтролфлагс**](tapicontrolflags.md) , указывающее, как управляется значение *свойства* .</span><span class="sxs-lookup"><span data-stu-id="a511d-120">Value of the [**TAPIControlFlags**](tapicontrolflags.md) enum indicating how the *Property* value is controlled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a511d-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a511d-121">Return value</span></span>

<span data-ttu-id="a511d-122">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="a511d-122">This method can return one of these values.</span></span>



| <span data-ttu-id="a511d-123">Код возврата</span><span class="sxs-lookup"><span data-stu-id="a511d-123">Return code</span></span>                                                                                   | <span data-ttu-id="a511d-124">Описание</span><span class="sxs-lookup"><span data-stu-id="a511d-124">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="a511d-125"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="a511d-125"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="a511d-126">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="a511d-126">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="a511d-127"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="a511d-127"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="a511d-128">Недостаточно памяти для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="a511d-128">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="a511d-129">Требования</span><span class="sxs-lookup"><span data-stu-id="a511d-129">Requirements</span></span>



| <span data-ttu-id="a511d-130">Требование</span><span class="sxs-lookup"><span data-stu-id="a511d-130">Requirement</span></span> | <span data-ttu-id="a511d-131">Значение</span><span class="sxs-lookup"><span data-stu-id="a511d-131">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="a511d-132">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="a511d-132">TAPI version</span></span><br/> | <span data-ttu-id="a511d-133">Требуется TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="a511d-133">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="a511d-134">Header</span><span class="sxs-lookup"><span data-stu-id="a511d-134">Header</span></span><br/>       | <dl> <span data-ttu-id="a511d-135"><dt>Ипмсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="a511d-135"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="a511d-136">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a511d-136">Library</span></span><br/>      | <dl> <span data-ttu-id="a511d-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a511d-137"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="a511d-138">DLL</span><span class="sxs-lookup"><span data-stu-id="a511d-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="a511d-139"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a511d-139"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a511d-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a511d-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a511d-141">**итаудиодевицеконтрол**</span><span class="sxs-lookup"><span data-stu-id="a511d-141">**ITAudioDeviceControl**</span></span>](itaudiodevicecontrol.md)
</dt> <dt>

[<span data-ttu-id="a511d-142">**тапиконтролфлагс**</span><span class="sxs-lookup"><span data-stu-id="a511d-142">**TAPIControlFlags**</span></span>](tapicontrolflags.md)
</dt> <dt>

[<span data-ttu-id="a511d-143">**аудиодевицепроперти**</span><span class="sxs-lookup"><span data-stu-id="a511d-143">**AudioDeviceProperty**</span></span>](audiodeviceproperty.md)
</dt> </dl>

 

 




