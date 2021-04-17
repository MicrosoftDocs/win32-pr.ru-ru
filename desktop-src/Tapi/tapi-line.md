---
description: Класс устройств TAPI/Line состоит из всех устройств линии. Доступ к этим устройствам осуществляется с помощью функций линии TAPI.
ms.assetid: 2215b10b-e410-462c-8cf9-42f3e688e82e
title: TAPI/Line
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 928cfa6144e9a701d6462519d2aa9d590a54a511
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674140"
---
# <a name="tapiline"></a><span data-ttu-id="f14b4-104">TAPI/Line</span><span class="sxs-lookup"><span data-stu-id="f14b4-104">tapi/line</span></span>

<span data-ttu-id="f14b4-105">Класс устройств TAPI/Line состоит из всех устройств линии.</span><span class="sxs-lookup"><span data-stu-id="f14b4-105">The tapi/line device class consists of all line devices.</span></span> <span data-ttu-id="f14b4-106">Доступ к этим устройствам осуществляется с помощью функций линии TAPI.</span><span class="sxs-lookup"><span data-stu-id="f14b4-106">You access these devices using the TAPI line functions.</span></span>

<span data-ttu-id="f14b4-107">Функция [**линежетид**](/windows/desktop/api/Tapi/nf-tapi-linegetid) заполняет структуру [**варстринг**](/windows/desktop/api/Tapi/ns-tapi-varstring) , устанавливая элемент **ДВСТРИНГФОРМАТ** в \_ двоичное значение STRINGFORMAT и добавляя этот дополнительный элемент.</span><span class="sxs-lookup"><span data-stu-id="f14b4-107">The [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) function fills a [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) structure, setting the **dwStringFormat** member to the STRINGFORMAT\_BINARY value and appending this additional member.</span></span>

``` syntax
DWORD dwDeviceI;  // line device identifier
```

<span data-ttu-id="f14b4-108">Элемент **двдевицеид** — это идентификатор устройства линии, связанного с маркером линии, заданным параметром [**линежетид**](/windows/desktop/api/Tapi/nf-tapi-linegetid).</span><span class="sxs-lookup"><span data-stu-id="f14b4-108">The **dwDeviceId** member is the identifier of the line device associated with the line handle given by [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid).</span></span>

<span data-ttu-id="f14b4-109">Функция [**фонежетид**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) также заполняет структуру [**варстринг**](/windows/desktop/api/Tapi/ns-tapi-varstring) , настроив **двстрингформат** на STRINGFORMAT \_ binary и добавляя этот дополнительный элемент:</span><span class="sxs-lookup"><span data-stu-id="f14b4-109">The [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) function also fills a [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) structure, setting **dwStringFormat** to STRINGFORMAT\_BINARY and appending this additional member:</span></span>

``` syntax
DWORD adwDeviceIds[];  // array of line device identifiers
```

<span data-ttu-id="f14b4-110">Элемент **адвдевицеидс** — это массив, содержащий идентификаторы устройств всех устройств линий, связанных с телефонным устройством.</span><span class="sxs-lookup"><span data-stu-id="f14b4-110">The **adwDeviceIds** member is an array containing the device identifiers of all line devices that are associated with the phone device.</span></span> <span data-ttu-id="f14b4-111">Если связанных устройств нет, [**фонежетид**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) ВОЗВРАЩАЕТ \_ значение фонирр инвалдевицекласс.</span><span class="sxs-lookup"><span data-stu-id="f14b4-111">If there are no associated line devices, [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) returns the PHONEERR\_INVALDEVICECLASS value.</span></span>

 

 



