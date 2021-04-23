---
description: Класс устройства MIDI состоит из последовательностей MIDI, которые используются для вывода. Доступ к этим устройствам осуществляется с помощью функций MIDI, которые описаны в пакете SDK для платформы.
ms.assetid: 398119ec-2d08-4c37-a993-a9b5ce52bcc8
title: MIDI/OUT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d6ae6a3daba8fa0520fca666e6c43a8b3db86c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262848"
---
# <a name="midiout"></a><span data-ttu-id="8653d-104">MIDI/OUT</span><span class="sxs-lookup"><span data-stu-id="8653d-104">midi/out</span></span>

<span data-ttu-id="8653d-105">Класс устройства MIDI состоит из последовательностей MIDI, которые используются для вывода.</span><span class="sxs-lookup"><span data-stu-id="8653d-105">The midi/out device class consists of MIDI sequencers that are used for output.</span></span> <span data-ttu-id="8653d-106">Доступ к этим устройствам осуществляется с помощью функций MIDI, которые описаны в пакете SDK для платформы.</span><span class="sxs-lookup"><span data-stu-id="8653d-106">You access these devices by using the MIDI functions, which are described in the Platform Software Development Kit (SDK).</span></span>

<span data-ttu-id="8653d-107">Функции [**линежетид**](/windows/desktop/api/Tapi/nf-tapi-linegetid) и [**фонежетид**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) заполняют структуру [**Варстринг**](/windows/desktop/api/Tapi/ns-tapi-varstring) , устанавливая элемент **двстрингформат** в \_ двоичное значение STRINGFORMAT и добавляя этот дополнительный элемент:</span><span class="sxs-lookup"><span data-stu-id="8653d-107">The [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) and [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) functions fill a [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) structure, setting the **dwStringFormat** member to the STRINGFORMAT\_BINARY value and appending this additional member:</span></span>

``` syntax
DWORD DeviceId;  // identifier of MIDI device
```

<span data-ttu-id="8653d-108">Элемент **DeviceID** — это идентификатор закрытого устройства MIDI.</span><span class="sxs-lookup"><span data-stu-id="8653d-108">The **DeviceId** member is the identifier of a closed MIDI device.</span></span> <span data-ttu-id="8653d-109">Этот идентификатор используется в вызове функции [**мидиаутопен**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) для открытия устройства для вывода.</span><span class="sxs-lookup"><span data-stu-id="8653d-109">You use this identifier in a call to the [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) function to open the device for output.</span></span> <span data-ttu-id="8653d-110">С помощью полученного маркера устройства можно воспроизводить данные MIDI на устройстве линии или телефоне.</span><span class="sxs-lookup"><span data-stu-id="8653d-110">You can use the resulting device handle to play MIDI data at the line or phone device.</span></span>

<span data-ttu-id="8653d-111">Дополнительные сведения о функциях MIDI см. в разделе [**функции мультимедиа**](../multimedia/multimedia-functions.md).</span><span class="sxs-lookup"><span data-stu-id="8653d-111">For more information about the MIDI functions, see [**Multimedia Functions**](../multimedia/multimedia-functions.md).</span></span>

 

 
