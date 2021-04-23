---
title: Запросы устройства микшера
description: Запросы устройства микшера
ms.assetid: 3b453802-954b-4356-9ad5-0f8376b6199d
keywords:
- мультимедиа аудио, запросы устройств микшера
- звуковые запросы устройства микшера
- аудио миксерс, запросы устройств
- миксерс, запросы устройств
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02acc3d5c7e418d14412c60a2e28e32849497c1a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104069943"
---
# <a name="mixer-device-queries"></a><span data-ttu-id="02d43-107">Запросы устройства микшера</span><span class="sxs-lookup"><span data-stu-id="02d43-107">Mixer Device Queries</span></span>

<span data-ttu-id="02d43-108">Службы микшера предоставляют функции для определения количества устройств микшера, имеющихся в системе, и возможностей устройств.</span><span class="sxs-lookup"><span data-stu-id="02d43-108">The mixer services provide functions for determining the number of mixer devices present in the system and the capabilities of the devices.</span></span> <span data-ttu-id="02d43-109">Для определения идентификатора устройства микшера можно также использовать функцию служб микшера.</span><span class="sxs-lookup"><span data-stu-id="02d43-109">You can also use a mixer services function to determine the device identifier for a mixer device.</span></span>

<span data-ttu-id="02d43-110">Функцию [**миксержетнумдевс**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetnumdevs) можно использовать для определения количества устройств микшера, имеющихся в системе.</span><span class="sxs-lookup"><span data-stu-id="02d43-110">You can use the [**mixerGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetnumdevs) function to determine how many mixer devices are present in the system.</span></span> <span data-ttu-id="02d43-111">Устройства микшера идентифицируются по идентификатору устройства.</span><span class="sxs-lookup"><span data-stu-id="02d43-111">Mixer devices are identified by a device identifier.</span></span> <span data-ttu-id="02d43-112">Идентификаторы устройств определяются неявно на количестве устройств, имеющихся в данной системе.</span><span class="sxs-lookup"><span data-stu-id="02d43-112">Device identifiers are determined implicitly from the number of devices present in a given system.</span></span> <span data-ttu-id="02d43-113">Они находятся в диапазоне от нуля до числа имеющихся устройств.</span><span class="sxs-lookup"><span data-stu-id="02d43-113">They range from zero through one less than the number of devices present.</span></span>

<span data-ttu-id="02d43-114">Перед использованием микшера устройства необходимо определить его возможности.</span><span class="sxs-lookup"><span data-stu-id="02d43-114">Before using a mixer device, you must determine its capabilities.</span></span> <span data-ttu-id="02d43-115">Звуковые возможности могут меняться от одного компьютера мультимедиа к другому, поэтому приложения должны работать с различными звуковыми устройствами.</span><span class="sxs-lookup"><span data-stu-id="02d43-115">Audio capabilities can vary from one multimedia computer to another, so applications need to work with a variety of audio hardware.</span></span>

<span data-ttu-id="02d43-116">Для определения возможностей микшерных устройств можно использовать функцию [**миксержетдевкапс**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetdevcaps) .</span><span class="sxs-lookup"><span data-stu-id="02d43-116">You can use the [**mixerGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetdevcaps) function to determine the capabilities of mixer devices.</span></span> <span data-ttu-id="02d43-117">Эта функция заполняет структуру [**миксеркапс**](/windows/win32/api/mmeapi/ns-mmeapi-mixercaps) данными о возможностях указанного устройства.</span><span class="sxs-lookup"><span data-stu-id="02d43-117">This function fills a [**MIXERCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-mixercaps) structure with information about the capabilities of a specified device.</span></span>

<span data-ttu-id="02d43-118">Функция [**миксержетид**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetid) извлекает идентификатор устройства микшера звука, связанный с указанным маркером устройства.</span><span class="sxs-lookup"><span data-stu-id="02d43-118">The [**mixerGetID**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetid) function retrieves the audio mixer device identifier associated with a specified device handle.</span></span> <span data-ttu-id="02d43-119">Например, эту функцию можно использовать для получения идентификатора устройства для звукового микшера, а затем использовать идентификатор устройства для настройки тома или для показа другого элемента управления.</span><span class="sxs-lookup"><span data-stu-id="02d43-119">For example, you could use this function to retrieve the device identifier for an audio mixer and then use the device identifier to adjust the volume or to display another control.</span></span>

 

 