---
description: Другие функции телефона TAPI используют маркер для открытого телефонного устройства для распознавания открытого телефонного устройства.
ms.assetid: 3e8e18fc-d577-4406-8225-048813c4cb9e
title: идентификаторы устройств;
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc8eb9d43b22ab6cd39a90ab8ed0776c4e043ef3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673291"
---
# <a name="device-ids"></a><span data-ttu-id="01af6-103">идентификаторы устройств;</span><span class="sxs-lookup"><span data-stu-id="01af6-103">Device IDs</span></span>

<span data-ttu-id="01af6-104">Другие функции телефона TAPI используют маркер для открытого телефонного устройства для распознавания открытого телефонного устройства.</span><span class="sxs-lookup"><span data-stu-id="01af6-104">Other TAPI phone functions use a handle to an open phone device to identify the open phone device.</span></span> <span data-ttu-id="01af6-105">Единственными функциями для телефонных устройств, принимающих параметр идентификатора телефонного устройства (в отличие от телефонного маркера), являются функции [**фонежетдевкапс**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps) и [**фонеопен**](/windows/desktop/api/Tapi/nf-tapi-phoneopen) .</span><span class="sxs-lookup"><span data-stu-id="01af6-105">The only functions for phone devices that take a phone device identifier parameter (as opposed to a phone handle) are the [**phoneGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps) and [**phoneOpen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen) functions.</span></span> <span data-ttu-id="01af6-106">Приложение может получить идентификатор устройства телефона с помощью функции [**фонежетид**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) с телефонным маркером в качестве параметра.</span><span class="sxs-lookup"><span data-stu-id="01af6-106">An application can retrieve the phone's device identifier by using the [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) function with the phone handle as a parameter.</span></span>

<span data-ttu-id="01af6-107">Приложение также может получать идентификаторы устройств для различных классов устройств, связанных с открытым телефоном, вызывая [**фонежетид**](/windows/desktop/api/Tapi/nf-tapi-phonegetid).</span><span class="sxs-lookup"><span data-stu-id="01af6-107">An application can also obtain device identifiers for various device classes associated with an opened phone by invoking [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid).</span></span> <span data-ttu-id="01af6-108">См. раздел [классы устройств TAPI](tapi-device-classes.md) для имен классов устройств.</span><span class="sxs-lookup"><span data-stu-id="01af6-108">See [TAPI Device Classes](tapi-device-classes.md) for device class names.</span></span>

<span data-ttu-id="01af6-109">Эта функция принимает маркер телефона и описание класса устройства.</span><span class="sxs-lookup"><span data-stu-id="01af6-109">This function takes a phone handle and a device class description.</span></span> <span data-ttu-id="01af6-110">Он возвращает идентификатор устройства для данного класса устройств, связанного с устройством Open Phone.</span><span class="sxs-lookup"><span data-stu-id="01af6-110">It returns the device identifier for the device of the given device class that is associated with the open phone device.</span></span> <span data-ttu-id="01af6-111">Если класс устройств имеет значение TAPI/Phone, возвращается идентификатор устройства телефонного устройства.</span><span class="sxs-lookup"><span data-stu-id="01af6-111">If the device class is "tapi/phone", the device identifier of the phone device is returned.</span></span>

<span data-ttu-id="01af6-112">В отличие от линейных устройств, для которых основные службы являются эквивалентом POTS, для телефонных устройств не определен минимальный гарантированный набор функций.</span><span class="sxs-lookup"><span data-stu-id="01af6-112">In contrast with line devices, for which the basic line services provide the equivalent of POTS, no minimum guaranteed set of functions is defined for phone devices.</span></span> <span data-ttu-id="01af6-113">Хотя каждое телефонное устройство предоставляет по крайней мере функции и сообщения, описанные в этом разделе, они не предлагают никаких фактических операций на устройстве физического телефона.</span><span class="sxs-lookup"><span data-stu-id="01af6-113">While each phone device provides at least the functions and messages described in this section, they do not offer any actual operations on the physical phone device.</span></span>

 

 



