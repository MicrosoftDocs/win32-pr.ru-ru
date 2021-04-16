---
title: О классе окна МЦивнд
description: О классе окна МЦивнд
ms.assetid: 7dde7346-5853-4c8f-8788-bf74d01ece83
keywords:
- Класс окна МЦивнд, сведения
- Функция МЦивндкреате
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e459a0e7d93543af126287a776b64130595ad11
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104410993"
---
# <a name="about-the-mciwnd-window-class"></a><span data-ttu-id="ee8b0-105">О классе окна МЦивнд</span><span class="sxs-lookup"><span data-stu-id="ee8b0-105">About the MCIWnd Window Class</span></span>

<span data-ttu-id="ee8b0-106">Класс окна МЦивнд прост в использовании.</span><span class="sxs-lookup"><span data-stu-id="ee8b0-106">The MCIWnd Window class is easy to use.</span></span> <span data-ttu-id="ee8b0-107">С помощью одной функции [**мЦивндкреате**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) приложение может создать элемент управления, который воспроизводит любое устройство, использующее интерфейс управления мультимедиа (MCI).</span><span class="sxs-lookup"><span data-stu-id="ee8b0-107">By using a single function, [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) your application can create a control that plays any device that uses the media control interface (MCI).</span></span> <span data-ttu-id="ee8b0-108">К таким устройствам относятся аудио CD, аудио-и видеоустройства, MIDI и видео.</span><span class="sxs-lookup"><span data-stu-id="ee8b0-108">These devices include CD audio, waveform-audio, MIDI, and video devices.</span></span>

<span data-ttu-id="ee8b0-109">Автоматизировать воспроизведение также можно быстро и легко.</span><span class="sxs-lookup"><span data-stu-id="ee8b0-109">Automating playback is also quick and easy.</span></span> <span data-ttu-id="ee8b0-110">Используя только одну функцию и два макроса, приложение может создать окно МЦивнд с соответствующим устройством мультимедиа, воспроизвести устройство и закрыть как устройство, так и окно после завершения воспроизведения содержимого.</span><span class="sxs-lookup"><span data-stu-id="ee8b0-110">Using only one function and two macros, an application can create an MCIWnd window with the appropriate media device, play the device, and close both the device and the window when the content has finished playing.</span></span>

> [!Note]  
> <span data-ttu-id="ee8b0-111">На некоторых устройствах воспроизводится содержимое, хранящееся в файлах.</span><span class="sxs-lookup"><span data-stu-id="ee8b0-111">Some devices play content that is stored in files.</span></span> <span data-ttu-id="ee8b0-112">Другие устройства, например устройства с компакт-дисков, воспроизводят содержимое, которое хранится на другом носителе.</span><span class="sxs-lookup"><span data-stu-id="ee8b0-112">Other devices, such as CD audio devices, play content that is stored in another medium.</span></span> <span data-ttu-id="ee8b0-113">В целях ясности в этом обзоре используются оба обстоятельства: "воспроизведение устройства".</span><span class="sxs-lookup"><span data-stu-id="ee8b0-113">For purposes of clarity, this overview refers to both circumstances as "playing the device."</span></span>

 

 

 




