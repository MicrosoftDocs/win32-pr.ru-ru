---
description: Класс устройств TAPI/Phone состоит из всех телефонных устройств. Доступ к этим устройствам осуществляется с помощью телефонных функций TAPI.
ms.assetid: c2e52fdf-e07a-4897-8af5-0a101d6c237a
title: TAPI и телефон
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c704a6999982fb0c23a8b02439a3d0e61b3af8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998990"
---
# <a name="tapiphone"></a><span data-ttu-id="17372-104">TAPI и телефон</span><span class="sxs-lookup"><span data-stu-id="17372-104">tapi/phone</span></span>

<span data-ttu-id="17372-105">Класс устройств TAPI/Phone состоит из всех телефонных устройств.</span><span class="sxs-lookup"><span data-stu-id="17372-105">The tapi/phone device class consists of all phone devices.</span></span> <span data-ttu-id="17372-106">Доступ к этим устройствам осуществляется с помощью телефонных функций TAPI.</span><span class="sxs-lookup"><span data-stu-id="17372-106">You access these devices by using the TAPI phone functions.</span></span>

<span data-ttu-id="17372-107">Функция [**фонежетид**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) заполняет структуру [**варстринг**](/windows/desktop/api/Tapi/ns-tapi-varstring) , устанавливая элемент **ДВСТРИНГФОРМАТ** в \_ двоичное значение STRINGFORMAT и добавляя этот дополнительный элемент:</span><span class="sxs-lookup"><span data-stu-id="17372-107">The [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) function fills a [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) structure, setting the **dwStringFormat** member to the STRINGFORMAT\_BINARY value and appending this additional member:</span></span>

``` syntax
DWORD dwDeviceI;  // phone device identifier
```

<span data-ttu-id="17372-108">Член **двдевицеид** — это идентификатор телефонного устройства, связанного с телефонным маркером, заданным параметром [**фонежетид**](/windows/desktop/api/Tapi/nf-tapi-phonegetid).</span><span class="sxs-lookup"><span data-stu-id="17372-108">The **dwDeviceId** member is the identifier of the phone device associated with the phone handle given by [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid).</span></span>

<span data-ttu-id="17372-109">Функция [**линежетид**](/windows/desktop/api/Tapi/nf-tapi-linegetid) также заполняет структуру [**варстринг**](/windows/desktop/api/Tapi/ns-tapi-varstring) , настроив **двстрингформат** на STRINGFORMAT \_ binary и добавляя этот дополнительный элемент:</span><span class="sxs-lookup"><span data-stu-id="17372-109">The [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) function also fills a [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) structure, setting **dwStringFormat** to STRINGFORMAT\_BINARY and appending this additional member:</span></span>

``` syntax
DWORD adwDeviceIds[];  // array of phone device identifiers
```

<span data-ttu-id="17372-110">Элемент **адвдевицеидс** — это массив, содержащий идентификаторы устройств всех телефонных устройств, связанных с данным устройством.</span><span class="sxs-lookup"><span data-stu-id="17372-110">The **adwDeviceIds** member is an array containing the device identifiers of all phone devices that are associated with the given line device.</span></span> <span data-ttu-id="17372-111">Если нет связанных телефонных устройств, [**линежетид**](/windows/desktop/api/Tapi/nf-tapi-linegetid) ВОЗВРАЩАЕТ \_ значение линирр инвалдевицекласс.</span><span class="sxs-lookup"><span data-stu-id="17372-111">If there are no associated phone devices, [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) returns the LINEERR\_INVALDEVICECLASS value.</span></span>

 

 



