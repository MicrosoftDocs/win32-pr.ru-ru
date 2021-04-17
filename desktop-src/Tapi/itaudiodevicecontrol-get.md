---
description: Метод Get получает значение заданного свойства звукового устройства.
ms.assetid: 34cb3f3e-be4a-49e0-bf7d-6915906e2368
title: 'Метод Итаудиодевицеконтрол:: Get (Ипмсп. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4311dc18291fcfbbe533dbe17042e6ba19c1122
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689345"
---
# <a name="itaudiodevicecontrolget-method"></a><span data-ttu-id="7542a-103">Метод Итаудиодевицеконтрол:: Get</span><span class="sxs-lookup"><span data-stu-id="7542a-103">ITAudioDeviceControl::Get method</span></span>

<span data-ttu-id="7542a-104">\[ Этот метод недоступен для использования в Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="7542a-104">\[ This method is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="7542a-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="7542a-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="7542a-106">Метод **Get** получает значение заданного [**Свойства звукового устройства**](audiodeviceproperty.md).</span><span class="sxs-lookup"><span data-stu-id="7542a-106">The **Get** method retrieves the value of a given [**audio device property**](audiodeviceproperty.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="7542a-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7542a-107">Syntax</span></span>


```C++
HRESULT get_Call(
  [out] ITCallInfo **ppCall
);
```



## <a name="parameters"></a><span data-ttu-id="7542a-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="7542a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7542a-109">*Свойство* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7542a-109">*Property* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7542a-110">Член перечисления [**аудиодевицепроперти**](audiodeviceproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="7542a-110">Member of the [**AudioDeviceProperty**](audiodeviceproperty.md) enum.</span></span>

</dd> <dt>

<span data-ttu-id="7542a-111">*плвалуе* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="7542a-111">*plValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7542a-112">Значение входного *Свойства*.</span><span class="sxs-lookup"><span data-stu-id="7542a-112">Value of the input *Property*.</span></span>

</dd> <dt>

<span data-ttu-id="7542a-113">*плфлагс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="7542a-113">*plFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7542a-114">Значение перечисления [**тапиконтролфлагс**](tapicontrolflags.md) , указывающее, как управляется значение *свойства* .</span><span class="sxs-lookup"><span data-stu-id="7542a-114">Value of the [**TAPIControlFlags**](tapicontrolflags.md) enum indicating how the *Property* value is controlled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7542a-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7542a-115">Return value</span></span>

<span data-ttu-id="7542a-116">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="7542a-116">This method can return one of these values.</span></span>



| <span data-ttu-id="7542a-117">Код возврата</span><span class="sxs-lookup"><span data-stu-id="7542a-117">Return code</span></span>                                                                                   | <span data-ttu-id="7542a-118">Описание</span><span class="sxs-lookup"><span data-stu-id="7542a-118">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="7542a-119"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="7542a-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="7542a-120">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="7542a-120">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="7542a-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="7542a-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="7542a-122">Недостаточно памяти для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="7542a-122">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="7542a-123">Требования</span><span class="sxs-lookup"><span data-stu-id="7542a-123">Requirements</span></span>



| <span data-ttu-id="7542a-124">Требование</span><span class="sxs-lookup"><span data-stu-id="7542a-124">Requirement</span></span> | <span data-ttu-id="7542a-125">Значение</span><span class="sxs-lookup"><span data-stu-id="7542a-125">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="7542a-126">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="7542a-126">TAPI version</span></span><br/> | <span data-ttu-id="7542a-127">Требуется TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="7542a-127">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="7542a-128">Header</span><span class="sxs-lookup"><span data-stu-id="7542a-128">Header</span></span><br/>       | <dl> <span data-ttu-id="7542a-129"><dt>Ипмсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="7542a-129"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="7542a-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="7542a-130">Library</span></span><br/>      | <dl> <span data-ttu-id="7542a-131"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7542a-131"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="7542a-132">DLL</span><span class="sxs-lookup"><span data-stu-id="7542a-132">DLL</span></span><br/>          | <dl> <span data-ttu-id="7542a-133"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7542a-133"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7542a-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7542a-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7542a-135">**итаудиодевицеконтрол**</span><span class="sxs-lookup"><span data-stu-id="7542a-135">**ITAudioDeviceControl**</span></span>](itaudiodevicecontrol.md)
</dt> <dt>

[<span data-ttu-id="7542a-136">**тапиконтролфлагс**</span><span class="sxs-lookup"><span data-stu-id="7542a-136">**TAPIControlFlags**</span></span>](tapicontrolflags.md)
</dt> <dt>

[<span data-ttu-id="7542a-137">**аудиодевицепроперти**</span><span class="sxs-lookup"><span data-stu-id="7542a-137">**AudioDeviceProperty**</span></span>](audiodeviceproperty.md)
</dt> </dl>

 

 




