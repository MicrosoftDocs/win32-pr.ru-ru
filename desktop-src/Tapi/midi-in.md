---
description: Класс MIDI/in Device состоит из последовательностей MIDI, используемых для ввода. Доступ к этим устройствам осуществляется с помощью функций MIDI, которые описаны в пакете SDK для платформы.
ms.assetid: 8997a391-bf61-4ec9-8ffc-fe3e6b92d63a
title: MIDI/in
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1d8119990af37cb030211b7dcc3a75d5261411f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808303"
---
# <a name="midiin"></a><span data-ttu-id="67b61-104">MIDI/in</span><span class="sxs-lookup"><span data-stu-id="67b61-104">midi/in</span></span>

<span data-ttu-id="67b61-105">Класс MIDI/in Device состоит из последовательностей MIDI, используемых для ввода.</span><span class="sxs-lookup"><span data-stu-id="67b61-105">The midi/in device class consists of MIDI sequencers that are used for input.</span></span> <span data-ttu-id="67b61-106">Доступ к этим устройствам осуществляется с помощью функций MIDI, которые описаны в пакете SDK для платформы.</span><span class="sxs-lookup"><span data-stu-id="67b61-106">You access these devices by using the MIDI functions, which are described in the Platform Software Development Kit (SDK).</span></span>

<span data-ttu-id="67b61-107">Функции [**линежетид**](/windows/desktop/api/Tapi/nf-tapi-linegetid) и [**фонежетид**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) заполняют структуру [**Варстринг**](/windows/desktop/api/Tapi/ns-tapi-varstring) , устанавливая элемент **двстрингформат** в \_ двоичное значение STRINGFORMAT и добавляя этот дополнительный элемент:</span><span class="sxs-lookup"><span data-stu-id="67b61-107">The [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) and [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) functions fill a [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) structure, setting the **dwStringFormat** member to the STRINGFORMAT\_BINARY value and appending this additional member:</span></span>

``` syntax
DWORD DeviceId;  // identifier of MIDI device
```

<span data-ttu-id="67b61-108">Элемент **DeviceID** — это идентификатор закрытого устройства MIDI.</span><span class="sxs-lookup"><span data-stu-id="67b61-108">The **DeviceId** member is the identifier of a closed MIDI device.</span></span> <span data-ttu-id="67b61-109">Этот идентификатор используется в вызове функции [**мидиинопен**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) для открытия устройства для ввода.</span><span class="sxs-lookup"><span data-stu-id="67b61-109">You use this identifier in a call to the [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) function to open the device for input.</span></span> <span data-ttu-id="67b61-110">С помощью результирующего маркера устройства можно записывать данные MIDI с устройства линии или телефона.</span><span class="sxs-lookup"><span data-stu-id="67b61-110">You can use the resulting device handle to record MIDI data from the line or phone device.</span></span>

<span data-ttu-id="67b61-111">Дополнительные сведения о функциях MIDI см. в разделе [**функции мультимедиа**](../multimedia/multimedia-functions.md).</span><span class="sxs-lookup"><span data-stu-id="67b61-111">For more information about the MIDI functions, see [**Multimedia Functions**](../multimedia/multimedia-functions.md).</span></span>

 

 
