---
description: Объект Phone — это сущность, представляющая реальное телефонное устройство и все его элементы управления.
ms.assetid: 5bc2f595-8e2b-4938-b813-1574a9390084
title: Интерфейсы объекта Phone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f39b163e895a512e7adc7be5c2fb848c5849361
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683909"
---
# <a name="phone-object-interfaces"></a><span data-ttu-id="1555e-103">Интерфейсы объекта Phone</span><span class="sxs-lookup"><span data-stu-id="1555e-103">Phone Object Interfaces</span></span>

<span data-ttu-id="1555e-104">Объект Phone — это сущность, представляющая реальное телефонное устройство и все его элементы управления.</span><span class="sxs-lookup"><span data-stu-id="1555e-104">The Phone object is the entity that represents the actual phone device and all of its controls.</span></span>

<span data-ttu-id="1555e-105">Интерфейсы [**итфонивент**](/windows/desktop/api/tapi3if/nn-tapi3if-itphoneevent) и [**иенумфоне**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumphone) не предоставляются напрямую в объекте Phone, но тесно связаны с ним и перечислены здесь для удобства использования справки.</span><span class="sxs-lookup"><span data-stu-id="1555e-105">The [**ITPhoneEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itphoneevent) and [**IEnumPhone**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumphone) interfaces are not directly exposed on the Phone object, but are tightly related to it and are listed here for convenience of reference.</span></span>



| <span data-ttu-id="1555e-106">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="1555e-106">Interface</span></span>                                                  | <span data-ttu-id="1555e-107">Описание</span><span class="sxs-lookup"><span data-stu-id="1555e-107">Description</span></span>                                                                                                                               |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1555e-108">**ITPhone**</span><span class="sxs-lookup"><span data-stu-id="1555e-108">**ITPhone**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itphone)                                 | <span data-ttu-id="1555e-109">Разрешает доступ к телефонному устройству на уровне, сравнимом с интерфейсом TAPI 2. API *x* C.</span><span class="sxs-lookup"><span data-stu-id="1555e-109">Allows access to the phone device at a level comparable to that available with the TAPI 2.*x* C API.</span></span>                                      |
| [<span data-ttu-id="1555e-110">**итаутоматедфонеконтрол**</span><span class="sxs-lookup"><span data-stu-id="1555e-110">**ITAutomatedPhoneControl**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itautomatedphonecontrol) | <span data-ttu-id="1555e-111">Предоставляет методы для автоматического управления тонами и кольцами телефона, а также для автоматизированной обработки вызовов на основе состояния хуксвитч телефона.</span><span class="sxs-lookup"><span data-stu-id="1555e-111">Provides methods for automated control of a phone's tones and rings, and for automated call handling based on a phone's hookswitch state.</span></span> |
| [<span data-ttu-id="1555e-112">**итфонивент**</span><span class="sxs-lookup"><span data-stu-id="1555e-112">**ITPhoneEvent**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itphoneevent)                       | <span data-ttu-id="1555e-113">Извлекает описание событий телефона.</span><span class="sxs-lookup"><span data-stu-id="1555e-113">Retrieves the description of phone events.</span></span>                                                                                                |
| [<span data-ttu-id="1555e-114">**иенумфоне**</span><span class="sxs-lookup"><span data-stu-id="1555e-114">**IEnumPhone**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-ienumphone)                           | <span data-ttu-id="1555e-115">Перечисляет [**итфоне**](/windows/desktop/api/tapi3if/nn-tapi3if-itphone).</span><span class="sxs-lookup"><span data-stu-id="1555e-115">Enumerates [**ITPhone**](/windows/desktop/api/tapi3if/nn-tapi3if-itphone).</span></span>                                                                                                    |



 

 

 



