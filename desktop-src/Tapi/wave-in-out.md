---
description: Класс устройства "звук/вход/выход" состоит из полных звуковых устройств.
ms.assetid: 1b49c9ae-da64-4415-95ce-785ffedc65bc
title: звук/вход/выход
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0e814cf2e8de1c3c5700a7570d2ed2b4c428572
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105673961"
---
# <a name="waveinout"></a><span data-ttu-id="e2121-103">звук/вход/выход</span><span class="sxs-lookup"><span data-stu-id="e2121-103">wave/in/out</span></span>

<span data-ttu-id="e2121-104">Класс устройства "звук/вход/выход" состоит из полных звуковых устройств.</span><span class="sxs-lookup"><span data-stu-id="e2121-104">The wave/in/out device class consists of full duplex audio devices.</span></span> <span data-ttu-id="e2121-105">Доступ к этим устройствам осуществляется с помощью функций Wave, которые описаны в пакете SDK для платформы.</span><span class="sxs-lookup"><span data-stu-id="e2121-105">You access these devices by using the wave functions, which are described in the Platform Software Development Kit (SDK).</span></span> <span data-ttu-id="e2121-106">Устройства в этом классе связаны с линейными устройствами, поддерживающими \_ тип носителя линемедиамоде аутоматедвоице, который указан в **двмедиамодес** в структуре [**линедевкапс**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) для линейного устройства.</span><span class="sxs-lookup"><span data-stu-id="e2121-106">Devices in this class are associated with line devices that support the LINEMEDIAMODE\_AUTOMATEDVOICE media type, which is specified in the **dwMediaModes** member of the [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) structure for the line device.</span></span>

<span data-ttu-id="e2121-107">Функции [**линежетид**](/windows/desktop/api/Tapi/nf-tapi-linegetid) и [**фонежетид**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) заполняют структуру [**Варстринг**](/windows/desktop/api/Tapi/ns-tapi-varstring) , устанавливая элемент **двстрингформат** в \_ двоичное значение STRINGFORMAT и добавляя два дополнительных члена:</span><span class="sxs-lookup"><span data-stu-id="e2121-107">The [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) and [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) functions fill a [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) structure, setting the **dwStringFormat** member to the STRINGFORMAT\_BINARY value and appending two additional members:</span></span>

``` syntax
DWORD DeviceInId;  // identifier of wave in audio device
DWORD DeviceOutId;  // identifier of wave out audio device
```

<span data-ttu-id="e2121-108">Члены **девицеинид** и **девицеаутид** являются идентификаторами закрытого звукового устройства.</span><span class="sxs-lookup"><span data-stu-id="e2121-108">The **DeviceInId** and **DeviceOutId** members are identifiers of a closed audio device.</span></span> <span data-ttu-id="e2121-109">Эти идентификаторы используются в вызове функции [**вавеаутопен**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) для открытия устройства для вывода.</span><span class="sxs-lookup"><span data-stu-id="e2121-109">You use these identifiers in a call to the [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) function to open the device for output.</span></span> <span data-ttu-id="e2121-110">Полученный в результате маркер устройства можно использовать для воспроизведения цифровых звуковых данных на устройстве Line или Phone.</span><span class="sxs-lookup"><span data-stu-id="e2121-110">You can use the resulting device handle to play digitized audio data at the line or phone device.</span></span>

<span data-ttu-id="e2121-111">Дополнительные сведения о функциях Wave см. в разделе [**функции мультимедиа**](../multimedia/multimedia-functions.md).</span><span class="sxs-lookup"><span data-stu-id="e2121-111">For more information about the wave functions, see [**Multimedia Functions**](../multimedia/multimedia-functions.md).</span></span>

 

 
