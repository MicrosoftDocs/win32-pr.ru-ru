---
title: Запрос Waveform-Audio устройств ввода
description: Запрос Waveform-Audio устройств ввода
ms.assetid: 573b33bc-f445-496e-a0e6-0194d30bb668
keywords:
- звуковая волна, запрос устройств ввода
- аудио-интерфейс, запрос устройств ввода
- запись аудио звукозаписи, запрос устройств ввода
- запросы к звуковым устройствам ввода
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91b915b3f39ad417a3d92396d887e5fb66092119
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103987448"
---
# <a name="querying-waveform-audio-input-devices"></a><span data-ttu-id="f2e33-107">Запрос Waveform-Audio устройств ввода</span><span class="sxs-lookup"><span data-stu-id="f2e33-107">Querying Waveform-Audio Input Devices</span></span>

<span data-ttu-id="f2e33-108">Перед записью звукового аудио-файла необходимо вызвать функцию [**вавеинжетдевкапс**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetdevcaps) , чтобы определить возможности ввода звука с помощью звукового сигнала системы.</span><span class="sxs-lookup"><span data-stu-id="f2e33-108">Before recording waveform audio, you should call the [**waveInGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetdevcaps) function to determine the waveform-audio input capabilities of the system.</span></span> <span data-ttu-id="f2e33-109">Эта функция заполняет структуру [**вавеинкапс**](/windows/win32/api/mmeapi/ns-mmeapi-waveincaps) данными о возможностях указанного устройства.</span><span class="sxs-lookup"><span data-stu-id="f2e33-109">This function fills a [**WAVEINCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-waveincaps) structure with information about the capabilities of a specified device.</span></span> <span data-ttu-id="f2e33-110">Эти сведения включают в себя изготовителя и идентификаторы продуктов, название продукта для устройства и номер версии драйвера устройства.</span><span class="sxs-lookup"><span data-stu-id="f2e33-110">This information includes the manufacturer and product identifiers, a product name for the device, and the version number of the device driver.</span></span> <span data-ttu-id="f2e33-111">Кроме того, структура **вавеинкапс** предоставляет сведения о стандартных форматах аудио, поддерживаемых устройством.</span><span class="sxs-lookup"><span data-stu-id="f2e33-111">In addition, the **WAVEINCAPS** structure provides information about the standard waveform-audio formats that the device supports.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f2e33-112">См. также</span><span class="sxs-lookup"><span data-stu-id="f2e33-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f2e33-113">Запись звука звукозаписи</span><span class="sxs-lookup"><span data-stu-id="f2e33-113">Recording Waveform Audio</span></span>](recording-waveform-audio.md)
</dt> </dl>

 

 