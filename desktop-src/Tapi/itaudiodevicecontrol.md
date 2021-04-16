---
description: Интерфейс Итаудиодевицеконтрол предоставляет методы, позволяющие приложению получать и задавать параметры для управления звуковым устройством.
ms.assetid: 9a557cb2-acad-406c-9a87-18cbe96e8a9f
title: Интерфейс Итаудиодевицеконтрол (Ипмсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 589bf50ee219f200a81aed7057b7755f203b2275
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679756"
---
# <a name="itaudiodevicecontrol-interface"></a><span data-ttu-id="441a4-103">Интерфейс Итаудиодевицеконтрол</span><span class="sxs-lookup"><span data-stu-id="441a4-103">ITAudioDeviceControl interface</span></span>

<span data-ttu-id="441a4-104">\[ Этот интерфейс недоступен для использования в Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="441a4-104">\[ This interface is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="441a4-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="441a4-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="441a4-106">Интерфейс **итаудиодевицеконтрол** предоставляет методы, позволяющие приложению получать и задавать параметры для управления звуковым устройством.</span><span class="sxs-lookup"><span data-stu-id="441a4-106">The **ITAudioDeviceControl** interface exposes methods that enable an application to get and set parameters for control of an audio device.</span></span>

<span data-ttu-id="441a4-107">Этот интерфейс реализуется с помощью [ИПКОНФ MSP](ipconf-msp.md) и [H323 MSP](h323-msp.md).</span><span class="sxs-lookup"><span data-stu-id="441a4-107">This interface is implemented by the [IPConf MSP](ipconf-msp.md) and the [H323 MSP](h323-msp.md).</span></span> <span data-ttu-id="441a4-108">Он предоставляется, когда в вызове используются поставщики услуг или поставщик услуг стороннего поставщика, реализующий этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="441a4-108">It is exposed when a call uses these service providers or a third party service provider that implements this interface.</span></span> <span data-ttu-id="441a4-109">Чтобы получить указатель на интерфейс **итаудиодевицеконтрол** , вызовите метод **QueryInterface** в интерфейсе [**итстреам**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) , который управляет звуковым устройством, соответствующим потоку.</span><span class="sxs-lookup"><span data-stu-id="441a4-109">To obtain a pointer to the **ITAudioDeviceControl** interface, call **QueryInterface** on the [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) interface that controls the audio device corresponding to the stream.</span></span> <span data-ttu-id="441a4-110">Для предоставления интерфейса **итаудиодевицеконтрол** тип мультимедиа интерфейса **итстреам** должен быть аудио.</span><span class="sxs-lookup"><span data-stu-id="441a4-110">The media type of the **ITStream** interface must be audio for the **ITAudioDeviceControl** interface to be exposed.</span></span>

## <a name="members"></a><span data-ttu-id="441a4-111">Элементы</span><span class="sxs-lookup"><span data-stu-id="441a4-111">Members</span></span>

<span data-ttu-id="441a4-112">Интерфейс **итаудиодевицеконтрол** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="441a4-112">The **ITAudioDeviceControl** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="441a4-113">**Итаудиодевицеконтрол** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="441a4-113">**ITAudioDeviceControl** also has these types of members:</span></span>

-   [<span data-ttu-id="441a4-114">Методы</span><span class="sxs-lookup"><span data-stu-id="441a4-114">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="441a4-115">Методы</span><span class="sxs-lookup"><span data-stu-id="441a4-115">Methods</span></span>

<span data-ttu-id="441a4-116">Интерфейс **итаудиодевицеконтрол** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="441a4-116">The **ITAudioDeviceControl** interface has these methods.</span></span>



| <span data-ttu-id="441a4-117">Метод</span><span class="sxs-lookup"><span data-stu-id="441a4-117">Method</span></span>                                              | <span data-ttu-id="441a4-118">Описание</span><span class="sxs-lookup"><span data-stu-id="441a4-118">Description</span></span>                                                                                             |
|:----------------------------------------------------|:--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="441a4-119">**Получить**</span><span class="sxs-lookup"><span data-stu-id="441a4-119">**Get**</span></span>](/windows/desktop/api/tapi3if/nf-tapi3if-itasrterminalevent-get_call)          | <span data-ttu-id="441a4-120">Возвращает значение заданного [Свойства звукового устройства](audiodeviceproperty.md).</span><span class="sxs-lookup"><span data-stu-id="441a4-120">Gets the value of a given [audio device property](audiodeviceproperty.md).</span></span><br/>                  |
| [<span data-ttu-id="441a4-121">**GetRange**</span><span class="sxs-lookup"><span data-stu-id="441a4-121">**GetRange**</span></span>](/windows/desktop/api/tapi3if/nf-tapi3if-itasrterminalevent-get_terminal) | <span data-ttu-id="441a4-122">Возвращает диапазон допустимых значений для заданного [Свойства звукового устройства](audiodeviceproperty.md).</span><span class="sxs-lookup"><span data-stu-id="441a4-122">Gets the range of valid values for a given [audio device property](audiodeviceproperty.md).</span></span><br/> |
| [<span data-ttu-id="441a4-123">**Параметр**</span><span class="sxs-lookup"><span data-stu-id="441a4-123">**Set**</span></span>](/windows/desktop/api/tapi3if/nf-tapi3if-itasrterminalevent-get_error)         | <span data-ttu-id="441a4-124">Задает значение заданного [Свойства звукового устройства](audiodeviceproperty.md).</span><span class="sxs-lookup"><span data-stu-id="441a4-124">Sets the value of a given [audio device property](audiodeviceproperty.md).</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="441a4-125">Требования</span><span class="sxs-lookup"><span data-stu-id="441a4-125">Requirements</span></span>



| <span data-ttu-id="441a4-126">Требование</span><span class="sxs-lookup"><span data-stu-id="441a4-126">Requirement</span></span> | <span data-ttu-id="441a4-127">Значение</span><span class="sxs-lookup"><span data-stu-id="441a4-127">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="441a4-128">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="441a4-128">TAPI version</span></span><br/> | <span data-ttu-id="441a4-129">Требуется TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="441a4-129">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="441a4-130">Header</span><span class="sxs-lookup"><span data-stu-id="441a4-130">Header</span></span><br/>       | <dl> <span data-ttu-id="441a4-131"><dt>Ипмсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="441a4-131"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="441a4-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="441a4-132">Library</span></span><br/>      | <dl> <span data-ttu-id="441a4-133"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="441a4-133"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="441a4-134">DLL</span><span class="sxs-lookup"><span data-stu-id="441a4-134">DLL</span></span><br/>          | <dl> <span data-ttu-id="441a4-135"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="441a4-135"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="441a4-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="441a4-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="441a4-137">Ипконф MSP</span><span class="sxs-lookup"><span data-stu-id="441a4-137">IPConf MSP</span></span>](ipconf-msp.md)
</dt> </dl>

 

