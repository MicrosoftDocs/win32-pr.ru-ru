---
description: О фильтре записи звука
ms.assetid: ff345670-5a75-40d3-a228-8bc22aa76708
title: О фильтре записи звука
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf5e28bef37ca52f0a33fc95b6d2a387cbbe2fb3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104140506"
---
# <a name="about-the-audio-capture-filter"></a><span data-ttu-id="8f917-103">О фильтре записи звука</span><span class="sxs-lookup"><span data-stu-id="8f917-103">About the Audio Capture Filter</span></span>

<span data-ttu-id="8f917-104">DirectShow позволяет осуществлять захват аналоговых входных данных на звуковой карте с помощью [фильтра записи звука](audio-capture-filter.md).</span><span class="sxs-lookup"><span data-stu-id="8f917-104">DirectShow enables capture from the analog inputs on a sound card through the [Audio Capture Filter](audio-capture-filter.md).</span></span> <span data-ttu-id="8f917-105">Этот фильтр использует API-интерфейсы Wave *xxx* для управления любым устройством, драйвером которого поддерживаются эти API.</span><span class="sxs-lookup"><span data-stu-id="8f917-105">This filter uses the waveIn *XXX* APIs to control any device whose driver supports these APIs.</span></span> <span data-ttu-id="8f917-106">Каждая карта в системе представляется отдельным экземпляром фильтра.</span><span class="sxs-lookup"><span data-stu-id="8f917-106">Each card on the system is represented by a separate instance of the filter.</span></span>

<span data-ttu-id="8f917-107">Фильтр записи звука предоставляет все входные данные на карточке, например микрофон или вход MIDI, в качестве ПИН-кода входа.</span><span class="sxs-lookup"><span data-stu-id="8f917-107">The Audio Capture filter exposes each input on the card, such as the microphone or the MIDI input, as an input pin.</span></span> <span data-ttu-id="8f917-108">Входной ПИН-код представляет то, что драйвер предоставляет в виде линий источника звука.</span><span class="sxs-lookup"><span data-stu-id="8f917-108">The input pins represent what the driver exposes as audio source lines.</span></span> <span data-ttu-id="8f917-109">Однако данные не проходят через эти входные контакты и не подключаются к другим фильтрам DirectShow.</span><span class="sxs-lookup"><span data-stu-id="8f917-109">No data travels through these input pins, however, and they do not connect to other DirectShow filters.</span></span> <span data-ttu-id="8f917-110">Они просто предоставляют приложению способ управления входными данными.</span><span class="sxs-lookup"><span data-stu-id="8f917-110">They simply provide a way for an application to control the inputs.</span></span> <span data-ttu-id="8f917-111">Приложение может использовать входной ПИН-код для включения или отключения входных данных, а также для установки смешанных свойств, таких как наподобие басов, высоких частот, панорамы и т. д.</span><span class="sxs-lookup"><span data-stu-id="8f917-111">The application can use an input pin to enable or disable the input, or to set mixing properties such as bass equalization, treble equalization, pan, and so forth.</span></span> <span data-ttu-id="8f917-112">Доступное количество элементов управления зависит от драйвера.</span><span class="sxs-lookup"><span data-stu-id="8f917-112">The amount of control that is available depends on the driver.</span></span> <span data-ttu-id="8f917-113">Чтобы полностью понять и использовать возможности определенной звуковой платы, вам потребуется документация от производителя карты.</span><span class="sxs-lookup"><span data-stu-id="8f917-113">To fully understand and exploit the capabilities of a particular sound card, you will need the documentation from the card's manufacturer.</span></span>

> [!Note]  
> <span data-ttu-id="8f917-114">Вы можете записать CD-Audio входные данные, но этот поток звука уже пропустил преобразование "цифровой-аналоговый", поэтому качество звука будет утеряно с исходного компакт-диска.</span><span class="sxs-lookup"><span data-stu-id="8f917-114">You can capture from the CD-Audio input, but this audio stream has already gone through the digital-to-analog converter, so there will be a loss of sound quality from the original CD.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="8f917-115">См. также</span><span class="sxs-lookup"><span data-stu-id="8f917-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8f917-116">Запись звука</span><span class="sxs-lookup"><span data-stu-id="8f917-116">Audio Capture</span></span>](audio-capture.md)
</dt> </dl>

 

 



