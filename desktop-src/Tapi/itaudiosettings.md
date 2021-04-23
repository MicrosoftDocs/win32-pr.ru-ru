---
description: Интерфейс Итаудиосеттингс предоставляет методы, позволяющие приложению получать и задавать параметры для управления звуковым устройством.
ms.assetid: 56607024-255d-4d1b-9ca0-6086eff7b7b2
title: Интерфейс Итаудиосеттингс (Ипмсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eaf2566c7438dbcd14cdacee46cc4d5ec4166731
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689206"
---
# <a name="itaudiosettings-interface"></a><span data-ttu-id="50443-103">Интерфейс Итаудиосеттингс</span><span class="sxs-lookup"><span data-stu-id="50443-103">ITAudioSettings interface</span></span>

<span data-ttu-id="50443-104">\[ Этот интерфейс недоступен для использования в Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="50443-104">\[ This interface is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="50443-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="50443-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="50443-106">Интерфейс **итаудиосеттингс** предоставляет методы, позволяющие приложению получать и задавать параметры для управления звуковым устройством.</span><span class="sxs-lookup"><span data-stu-id="50443-106">The **ITAudioSettings** interface exposes methods that allow an application to get and set parameters for control of an audio device.</span></span>

<span data-ttu-id="50443-107">Этот интерфейс реализуется с помощью [ИПКОНФ MSP](ipconf-msp.md) и [H323 MSP](h323-msp.md).</span><span class="sxs-lookup"><span data-stu-id="50443-107">This interface is implemented by the [IPConf MSP](ipconf-msp.md) and the [H323 MSP](h323-msp.md).</span></span> <span data-ttu-id="50443-108">Он предоставляется только в том случае, если вызов использует эти поставщики служб.</span><span class="sxs-lookup"><span data-stu-id="50443-108">It is exposed only when a call uses these service providers.</span></span>

## <a name="members"></a><span data-ttu-id="50443-109">Элементы</span><span class="sxs-lookup"><span data-stu-id="50443-109">Members</span></span>

<span data-ttu-id="50443-110">Интерфейс **итаудиосеттингс** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="50443-110">The **ITAudioSettings** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="50443-111">**Итаудиосеттингс** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="50443-111">**ITAudioSettings** also has these types of members:</span></span>

-   [<span data-ttu-id="50443-112">Методы</span><span class="sxs-lookup"><span data-stu-id="50443-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="50443-113">Методы</span><span class="sxs-lookup"><span data-stu-id="50443-113">Methods</span></span>

<span data-ttu-id="50443-114">Интерфейс **итаудиосеттингс** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="50443-114">The **ITAudioSettings** interface has these methods.</span></span>



| <span data-ttu-id="50443-115">Метод</span><span class="sxs-lookup"><span data-stu-id="50443-115">Method</span></span>                                              | <span data-ttu-id="50443-116">Описание</span><span class="sxs-lookup"><span data-stu-id="50443-116">Description</span></span>                                                                                                |
|:----------------------------------------------------|:-----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="50443-117">**Получить**</span><span class="sxs-lookup"><span data-stu-id="50443-117">**Get**</span></span>](/windows/desktop/api/tapi3if/nf-tapi3if-itasrterminalevent-get_call)          | <span data-ttu-id="50443-118">Возвращает значение заданного [Свойства звукового параметра](audiosettingsproperty.md).</span><span class="sxs-lookup"><span data-stu-id="50443-118">Gets the value of a given [audio setting property](audiosettingsproperty.md).</span></span><br/>                  |
| [<span data-ttu-id="50443-119">**GetRange**</span><span class="sxs-lookup"><span data-stu-id="50443-119">**GetRange**</span></span>](/windows/desktop/api/tapi3if/nf-tapi3if-itasrterminalevent-get_terminal) | <span data-ttu-id="50443-120">Возвращает диапазон допустимых значений для заданного [Свойства звукового параметра](audiosettingsproperty.md).</span><span class="sxs-lookup"><span data-stu-id="50443-120">Gets the range of valid values for a given [audio setting property](audiosettingsproperty.md).</span></span><br/> |
| [<span data-ttu-id="50443-121">**Параметр**</span><span class="sxs-lookup"><span data-stu-id="50443-121">**Set**</span></span>](/windows/desktop/api/tapi3if/nf-tapi3if-itasrterminalevent-get_error)         | <span data-ttu-id="50443-122">Задает значение заданного [Свойства звукового параметра](audiosettingsproperty.md).</span><span class="sxs-lookup"><span data-stu-id="50443-122">Sets the value of a given [audio setting property](audiosettingsproperty.md).</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="50443-123">Требования</span><span class="sxs-lookup"><span data-stu-id="50443-123">Requirements</span></span>



| <span data-ttu-id="50443-124">Требование</span><span class="sxs-lookup"><span data-stu-id="50443-124">Requirement</span></span> | <span data-ttu-id="50443-125">Значение</span><span class="sxs-lookup"><span data-stu-id="50443-125">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="50443-126">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="50443-126">TAPI version</span></span><br/> | <span data-ttu-id="50443-127">Требуется TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="50443-127">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="50443-128">Header</span><span class="sxs-lookup"><span data-stu-id="50443-128">Header</span></span><br/>       | <dl> <span data-ttu-id="50443-129"><dt>Ипмсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="50443-129"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="50443-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="50443-130">Library</span></span><br/>      | <dl> <span data-ttu-id="50443-131"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="50443-131"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="50443-132">DLL</span><span class="sxs-lookup"><span data-stu-id="50443-132">DLL</span></span><br/>          | <dl> <span data-ttu-id="50443-133"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="50443-133"><dt>Tapi3.dll</dt></span></span> </dl> |



 

