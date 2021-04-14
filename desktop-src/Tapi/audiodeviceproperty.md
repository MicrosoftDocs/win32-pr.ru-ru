---
description: 'Перечисление Аудиодевицепроперти используется методами Итаудиодевицеконтрол::, Итаудиодевицеконтрол:: Get и Итаудиодевицеконтрол:: Set для указания свойства, для которого выполняется обращение.'
ms.assetid: 0ed9b75e-3c79-4e41-9883-63b85ebfae06
title: Перечисление Аудиодевицепроперти (Ипмсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab807759bfb316858be41ea9bb4b78d795ee1a1a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675637"
---
# <a name="audiodeviceproperty-enumeration"></a><span data-ttu-id="24a13-103">Перечисление Аудиодевицепроперти</span><span class="sxs-lookup"><span data-stu-id="24a13-103">AudioDeviceProperty enumeration</span></span>

<span data-ttu-id="24a13-104">\[ Это перечисление недоступно для использования в Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="24a13-104">\[ This enumeration is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="24a13-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="24a13-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="24a13-106">Перечисление **аудиодевицепроперти** используется методами [**итаудиодевицеконтрол::**](itaudiodevicecontrol-getrange.md), [**Итаудиодевицеконтрол:: Get**](itaudiodevicecontrol-get.md)и [**итаудиодевицеконтрол:: Set**](itaudiodevicecontrol-set.md) для указания свойства, для которого выполняется обращение.</span><span class="sxs-lookup"><span data-stu-id="24a13-106">The **AudioDeviceProperty** enum is used by the [**ITAudioDeviceControl::GetRange**](itaudiodevicecontrol-getrange.md), [**ITAudioDeviceControl::Get**](itaudiodevicecontrol-get.md), and [**ITAudioDeviceControl::Set**](itaudiodevicecontrol-set.md) methods to indicate the property being addressed.</span></span>

## <a name="syntax"></a><span data-ttu-id="24a13-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="24a13-107">Syntax</span></span>


```C++
} AudioDeviceProperty;
```



## <a name="constants"></a><span data-ttu-id="24a13-108">Константы</span><span class="sxs-lookup"><span data-stu-id="24a13-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="24a13-109"><span id="AudioDevice_DuplexMode"></span><span id="audiodevice_duplexmode"></span><span id="AUDIODEVICE_DUPLEXMODE"></span>**Аудиодевице \_ дуплексмоде**</span><span class="sxs-lookup"><span data-stu-id="24a13-109"><span id="AudioDevice_DuplexMode"></span><span id="audiodevice_duplexmode"></span><span id="AUDIODEVICE_DUPLEXMODE"></span>**AudioDevice\_DuplexMode**</span></span>
</dt> <dd>

<span data-ttu-id="24a13-110">Указывает, что режим дуплекса устройства устанавливается или извлекается.</span><span class="sxs-lookup"><span data-stu-id="24a13-110">Indicates that the duplex mode of the device is being set or retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="24a13-111"><span id="AudioDevice_AutomaticGainControl"></span><span id="audiodevice_automaticgaincontrol"></span><span id="AUDIODEVICE_AUTOMATICGAINCONTROL"></span>**Аудиодевице \_ аутоматикгаинконтрол**</span><span class="sxs-lookup"><span data-stu-id="24a13-111"><span id="AudioDevice_AutomaticGainControl"></span><span id="audiodevice_automaticgaincontrol"></span><span id="AUDIODEVICE_AUTOMATICGAINCONTROL"></span>**AudioDevice\_AutomaticGainControl**</span></span>
</dt> <dd>

<span data-ttu-id="24a13-112">Указывает, что устанавливается или извлекается автоматический контроль усиления устройства.</span><span class="sxs-lookup"><span data-stu-id="24a13-112">Indicates that the automatic gain control of the device is being set or retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="24a13-113"><span id="AudioDevice_AcousticEchoCancellation"></span><span id="audiodevice_acousticechocancellation"></span><span id="AUDIODEVICE_ACOUSTICECHOCANCELLATION"></span>**Аудиодевице \_ акаустицечоканцеллатион**</span><span class="sxs-lookup"><span data-stu-id="24a13-113"><span id="AudioDevice_AcousticEchoCancellation"></span><span id="audiodevice_acousticechocancellation"></span><span id="AUDIODEVICE_ACOUSTICECHOCANCELLATION"></span>**AudioDevice\_AcousticEchoCancellation**</span></span>
</dt> <dd>

<span data-ttu-id="24a13-114">Указывает, что задаются или извлекаются свойства отмены акустического эха устройства.</span><span class="sxs-lookup"><span data-stu-id="24a13-114">Indicates that the acoustic echo cancellation properties of the device are being set or retrieved.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="24a13-115">Требования</span><span class="sxs-lookup"><span data-stu-id="24a13-115">Requirements</span></span>



| <span data-ttu-id="24a13-116">Требование</span><span class="sxs-lookup"><span data-stu-id="24a13-116">Requirement</span></span> | <span data-ttu-id="24a13-117">Значение</span><span class="sxs-lookup"><span data-stu-id="24a13-117">Value</span></span> |
|-------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="24a13-118">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="24a13-118">TAPI version</span></span><br/> | <span data-ttu-id="24a13-119">Требуется TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="24a13-119">Requires TAPI 3.1</span></span><br/>                                                       |
| <span data-ttu-id="24a13-120">Header</span><span class="sxs-lookup"><span data-stu-id="24a13-120">Header</span></span><br/>       | <dl> <span data-ttu-id="24a13-121"><dt>Ипмсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="24a13-121"><dt>Ipmsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24a13-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="24a13-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24a13-123">**Итаудиодевицеконтрол:: Range**</span><span class="sxs-lookup"><span data-stu-id="24a13-123">**ITAudioDeviceControl::GetRange**</span></span>](itaudiodevicecontrol-getrange.md)
</dt> <dt>

[<span data-ttu-id="24a13-124">**Итаудиодевицеконтрол:: Get**</span><span class="sxs-lookup"><span data-stu-id="24a13-124">**ITAudioDeviceControl::Get**</span></span>](itaudiodevicecontrol-get.md)
</dt> <dt>

[<span data-ttu-id="24a13-125">**Итаудиодевицеконтрол:: Set**</span><span class="sxs-lookup"><span data-stu-id="24a13-125">**ITAudioDeviceControl::Set**</span></span>](itaudiodevicecontrol-set.md)
</dt> </dl>

 

 




