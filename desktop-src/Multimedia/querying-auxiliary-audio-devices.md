---
title: Запрос вспомогательных звуковых устройств
description: Запрос вспомогательных звуковых устройств
ms.assetid: 9fc0b17f-cc93-4eab-bcb3-09f2332b352f
keywords:
- звуковая волна, запрос дополнительных звуковых устройств
- добавочный звук, запросы устройств
- вспомогательный звуковой интерфейс
- вспомогательные звуковые устройства, запросы
- запрос вспомогательных звуковых устройств
- Вспомогательное аудио, интерфейс
- Вспомогательные аудио, устройства
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d7de949c304cdd6941be87277f2eef1711ada24
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104069885"
---
# <a name="querying-auxiliary-audio-devices"></a><span data-ttu-id="8b423-110">Запрос вспомогательных звуковых устройств</span><span class="sxs-lookup"><span data-stu-id="8b423-110">Querying Auxiliary Audio Devices</span></span>

<span data-ttu-id="8b423-111">Не все мультимедийные системы имеют вспомогательную поддержку аудио.</span><span class="sxs-lookup"><span data-stu-id="8b423-111">Not all multimedia systems have auxiliary audio support.</span></span> <span data-ttu-id="8b423-112">Функцию [**ауксжетнумдевс**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetnumdevs) можно использовать для определения числа управляемых устройств, которые могут находиться в системе.</span><span class="sxs-lookup"><span data-stu-id="8b423-112">You can use the [**auxGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetnumdevs) function to determine the number of controllable auxiliary devices present in a system.</span></span>

<span data-ttu-id="8b423-113">Чтобы получить сведения о конкретном дополнительном звуковом устройстве, используйте функцию [**ауксжетдевкапс**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetdevcaps) .</span><span class="sxs-lookup"><span data-stu-id="8b423-113">To get information about a particular auxiliary audio device, use the [**auxGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetdevcaps) function.</span></span> <span data-ttu-id="8b423-114">Эта функция заполняет структуру [**аукскапс**](/windows/win32/api/mmeapi/ns-mmeapi-auxcaps) данными о возможностях указанного устройства.</span><span class="sxs-lookup"><span data-stu-id="8b423-114">This function fills an [**AUXCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-auxcaps) structure with information about the capabilities of a specified device.</span></span> <span data-ttu-id="8b423-115">Эти сведения включают в себя производителя и идентификаторы продуктов, название продукта для устройства и номер версии драйвера устройства.</span><span class="sxs-lookup"><span data-stu-id="8b423-115">This information includes the manufacturer and product identifiers, a product name for the device, and the device-driver version number.</span></span>

 

 