---
description: Класс устройства "звук/выход" состоит из звуковых устройств для звукового вывода нижнего уровня.
ms.assetid: 85894134-e8ad-43e2-8b97-09b80bfd36d5
title: звук и выход
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 975a3308b6f0b29e130ad07534494e1cb1d991a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913804"
---
# <a name="waveout"></a><span data-ttu-id="9bdea-103">звук и выход</span><span class="sxs-lookup"><span data-stu-id="9bdea-103">wave/out</span></span>

<span data-ttu-id="9bdea-104">Класс устройства "звук/выход" состоит из звуковых устройств для звукового вывода нижнего уровня.</span><span class="sxs-lookup"><span data-stu-id="9bdea-104">The wave/out device class consists of audio devices for low-level wave audio output.</span></span> <span data-ttu-id="9bdea-105">Доступ к этим устройствам осуществляется с помощью функций Wave, которые описаны в пакете SDK для платформы.</span><span class="sxs-lookup"><span data-stu-id="9bdea-105">You access these devices by using the wave functions, which are described in the Platform Software Development Kit (SDK).</span></span> <span data-ttu-id="9bdea-106">Устройства в этом классе связаны с линейными устройствами, поддерживающими \_ тип носителя линемедиамоде аутоматедвоице, который указан в **двмедиамодес** в структуре [**линедевкапс**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) для линейного устройства.</span><span class="sxs-lookup"><span data-stu-id="9bdea-106">Devices in this class are associated with line devices that support the LINEMEDIAMODE\_AUTOMATEDVOICE media type, which is specified in the **dwMediaModes** member of the [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) structure for the line device.</span></span>

<span data-ttu-id="9bdea-107">Функции [**линежетид**](/windows/desktop/api/Tapi/nf-tapi-linegetid) и [**фонежетид**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) заполняют структуру [**Варстринг**](/windows/desktop/api/Tapi/ns-tapi-varstring) , устанавливая элемент **двстрингформат** в \_ двоичное значение STRINGFORMAT и добавляя этот дополнительный элемент:</span><span class="sxs-lookup"><span data-stu-id="9bdea-107">The [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) and [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) functions fill a [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) structure, setting the **dwStringFormat** member to the STRINGFORMAT\_BINARY value and appending this additional member:</span></span>

``` syntax
DWORD DeviceId;  // identifier of audio device
```

<span data-ttu-id="9bdea-108">Элемент **DeviceID** — это идентификатор закрытого звукового устройства.</span><span class="sxs-lookup"><span data-stu-id="9bdea-108">The **DeviceId** member is the identifier of a closed audio device.</span></span> <span data-ttu-id="9bdea-109">Этот идентификатор используется в вызове функции [**вавеаутопен**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) для открытия устройства для вывода.</span><span class="sxs-lookup"><span data-stu-id="9bdea-109">You use this identifier in a call to the [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) function to open the device for output.</span></span> <span data-ttu-id="9bdea-110">Полученный в результате маркер устройства можно использовать для воспроизведения цифровых звуковых данных на устройстве Line или Phone.</span><span class="sxs-lookup"><span data-stu-id="9bdea-110">You can use the resulting device handle to play digitized audio data at the line or phone device.</span></span>

<span data-ttu-id="9bdea-111">Хотя для низкоуровневых звуковых устройств также существует класс устройств "Wave", для низкоуровневых выходных данных всегда следует использовать класс устройств волн/out.</span><span class="sxs-lookup"><span data-stu-id="9bdea-111">Although a "wave" device class also exists for low-level wave audio devices, you should always use the wave/out device class for low-level wave output.</span></span>

<span data-ttu-id="9bdea-112">Дополнительные сведения о функциях Wave см. в разделе [**функции мультимедиа**](../multimedia/multimedia-functions.md).</span><span class="sxs-lookup"><span data-stu-id="9bdea-112">For more information about the wave functions, see [**Multimedia Functions**](../multimedia/multimedia-functions.md).</span></span>

 

 
