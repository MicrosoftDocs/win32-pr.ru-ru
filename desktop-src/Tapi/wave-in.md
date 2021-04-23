---
description: Класс "волна/in Device" состоит из звуковых устройств для звукового ввода низкого уровня.
ms.assetid: b2f32019-088f-4805-af7e-559a8179b1e6
title: звук/в
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3465a575937538c6a4113ec544b1d246fec3a598
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104266229"
---
# <a name="wavein"></a><span data-ttu-id="191e8-103">звук/в</span><span class="sxs-lookup"><span data-stu-id="191e8-103">wave/in</span></span>

<span data-ttu-id="191e8-104">Класс "волна/in Device" состоит из звуковых устройств для звукового ввода низкого уровня.</span><span class="sxs-lookup"><span data-stu-id="191e8-104">The wave/in device class consists of audio devices for low-level wave audio input.</span></span> <span data-ttu-id="191e8-105">Доступ к этим устройствам осуществляется с помощью функций Wave, которые описаны в пакете SDK для платформы.</span><span class="sxs-lookup"><span data-stu-id="191e8-105">You access these devices by using the wave functions, which are described in the Platform Software Development Kit (SDK).</span></span> <span data-ttu-id="191e8-106">Устройства в этом классе связаны с линейными устройствами, поддерживающими \_ тип носителя линемедиамоде аутоматедвоице, который указан в **двмедиамодес** в структуре [**линедевкапс**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) для линейного устройства.</span><span class="sxs-lookup"><span data-stu-id="191e8-106">Devices in this class are associated with line devices that support the LINEMEDIAMODE\_AUTOMATEDVOICE media type, which is specified in the **dwMediaModes** member of the [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) structure for the line device.</span></span>

<span data-ttu-id="191e8-107">Функции [**линежетид**](/windows/desktop/api/Tapi/nf-tapi-linegetid) и [**фонежетид**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) заполняют структуру [**Варстринг**](/windows/desktop/api/Tapi/ns-tapi-varstring) , устанавливая элемент **двстрингформат** в \_ двоичное значение STRINGFORMAT и добавляя этот дополнительный элемент:</span><span class="sxs-lookup"><span data-stu-id="191e8-107">The [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) and [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) functions fill a [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) structure, setting the **dwStringFormat** member to the STRINGFORMAT\_BINARY value and appending this additional member:</span></span>

``` syntax
DWORD DeviceId;  // identifier of audio device
```

<span data-ttu-id="191e8-108">Элемент **DeviceID** — это идентификатор закрытого звукового устройства.</span><span class="sxs-lookup"><span data-stu-id="191e8-108">The **DeviceId** member is the identifier of a closed audio device.</span></span> <span data-ttu-id="191e8-109">Этот идентификатор используется в вызове функции [**вавеинопен**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) для открытия устройства для ввода.</span><span class="sxs-lookup"><span data-stu-id="191e8-109">You use this identifier in a call to the [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) function to open the device for input.</span></span> <span data-ttu-id="191e8-110">Полученный в результате маркер устройства можно использовать для записи цифровых звуковых данных с устройства Line или Phone.</span><span class="sxs-lookup"><span data-stu-id="191e8-110">You can use the resulting device handle to record digitized audio data from the line or phone device.</span></span>

<span data-ttu-id="191e8-111">Хотя класс устройств "Wave" также существует для низкоуровневых звуковых устройств, для низкоуровневых входных данных всегда следует использовать класс "волна/in Device".</span><span class="sxs-lookup"><span data-stu-id="191e8-111">Although a "wave" device class also exists for low-level wave audio devices, you should always use the wave/in device class for low-level wave input.</span></span>

<span data-ttu-id="191e8-112">Дополнительные сведения о функциях Wave см. в разделе [**функции мультимедиа**](../multimedia/multimedia-functions.md).</span><span class="sxs-lookup"><span data-stu-id="191e8-112">For more information about the wave functions, see [**Multimedia Functions**](../multimedia/multimedia-functions.md).</span></span>

 

 
