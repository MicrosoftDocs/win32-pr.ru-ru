---
title: Типы устройств
description: Типы устройств
ms.assetid: 6556fa6a-5906-4afb-ab7d-ef41a0e22d13
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e27ed77debb663a1d90e03512832ca83e6e276d3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103778503"
---
# <a name="device-types"></a><span data-ttu-id="ec1ed-103">Типы устройств</span><span class="sxs-lookup"><span data-stu-id="ec1ed-103">Device Types</span></span>

<span data-ttu-id="ec1ed-104">MCI распознает базовый набор *типов устройств*.</span><span class="sxs-lookup"><span data-stu-id="ec1ed-104">MCI recognizes a basic set of *device types*.</span></span> <span data-ttu-id="ec1ed-105">Тип устройства — это набор драйверов MCI, использующих общий набор команд и используемый для управления аналогичными устройствами мультимедиа или файлами данных.</span><span class="sxs-lookup"><span data-stu-id="ec1ed-105">A device type is a set of MCI drivers that share a common command set and are used to control similar multimedia devices or data files.</span></span> <span data-ttu-id="ec1ed-106">Многие команды MCI, например [**Open**](open.md) ([**MCI \_ Open**](mci-open.md)), потребовали указать тип устройства.</span><span class="sxs-lookup"><span data-stu-id="ec1ed-106">Many MCI commands, such as [**open**](open.md) ([**MCI\_OPEN**](mci-open.md)), require you to specify a device type.</span></span>

<span data-ttu-id="ec1ed-107">В следующей таблице перечислены определенные типы устройств.</span><span class="sxs-lookup"><span data-stu-id="ec1ed-107">The following table lists the defined device types.</span></span> <span data-ttu-id="ec1ed-108">Текущая реализация MCI включает наборы команд для подмножества этих устройств.</span><span class="sxs-lookup"><span data-stu-id="ec1ed-108">The current implementation of MCI includes command sets for a subset of these devices.</span></span>



| <span data-ttu-id="ec1ed-109">Тип устройства</span><span class="sxs-lookup"><span data-stu-id="ec1ed-109">Device type</span></span>      | <span data-ttu-id="ec1ed-110">Константа</span><span class="sxs-lookup"><span data-stu-id="ec1ed-110">Constant</span></span>                      | <span data-ttu-id="ec1ed-111">Описание</span><span class="sxs-lookup"><span data-stu-id="ec1ed-111">Description</span></span>                                      |
|------------------|-------------------------------|--------------------------------------------------|
| <span data-ttu-id="ec1ed-112">**кдаудио**</span><span class="sxs-lookup"><span data-stu-id="ec1ed-112">**cdaudio**</span></span>      | <span data-ttu-id="ec1ed-113">\_ \_ аудио компакт-диск MCI девтипе \_</span><span class="sxs-lookup"><span data-stu-id="ec1ed-113">MCI\_DEVTYPE\_CD\_AUDIO</span></span>       | <span data-ttu-id="ec1ed-114">Проигрыватель CD Audio</span><span class="sxs-lookup"><span data-stu-id="ec1ed-114">CD audio player</span></span>                                  |
| <span data-ttu-id="ec1ed-115">**включая**</span><span class="sxs-lookup"><span data-stu-id="ec1ed-115">**dat**</span></span>          | <span data-ttu-id="ec1ed-116">MCI \_ девтипе \_ dat</span><span class="sxs-lookup"><span data-stu-id="ec1ed-116">MCI\_DEVTYPE\_DAT</span></span>             | <span data-ttu-id="ec1ed-117">Ленточный проигрыватель для цифрового аудио</span><span class="sxs-lookup"><span data-stu-id="ec1ed-117">Digital-audio tape player</span></span>                        |
| <span data-ttu-id="ec1ed-118">**дигиталвидео**</span><span class="sxs-lookup"><span data-stu-id="ec1ed-118">**digitalvideo**</span></span> | <span data-ttu-id="ec1ed-119">\_устройство MCI девтипе \_ Digital \_ Video</span><span class="sxs-lookup"><span data-stu-id="ec1ed-119">MCI\_DEVTYPE\_DIGITAL\_VIDEO</span></span>  | <span data-ttu-id="ec1ed-120">Цифровое видео в окне (не на основе GDI)</span><span class="sxs-lookup"><span data-stu-id="ec1ed-120">Digital video in a window (not GDI-based)</span></span>        |
| <span data-ttu-id="ec1ed-121">**иной**</span><span class="sxs-lookup"><span data-stu-id="ec1ed-121">**other**</span></span>        | <span data-ttu-id="ec1ed-122">\_ДЕВТИПЕ MCI \_</span><span class="sxs-lookup"><span data-stu-id="ec1ed-122">MCI\_DEVTYPE\_OTHER</span></span>           | <span data-ttu-id="ec1ed-123">Неопределенное устройство MCI</span><span class="sxs-lookup"><span data-stu-id="ec1ed-123">Undefined MCI device</span></span>                             |
| <span data-ttu-id="ec1ed-124">**объединения**</span><span class="sxs-lookup"><span data-stu-id="ec1ed-124">**overlay**</span></span>      | <span data-ttu-id="ec1ed-125">наложение MCI \_ девтипе \_</span><span class="sxs-lookup"><span data-stu-id="ec1ed-125">MCI\_DEVTYPE\_OVERLAY</span></span>         | <span data-ttu-id="ec1ed-126">Наложение устройства (аналоговый видеоролик в окне)</span><span class="sxs-lookup"><span data-stu-id="ec1ed-126">Overlay device (analog video in a window)</span></span>        |
| <span data-ttu-id="ec1ed-127">**вирусов**</span><span class="sxs-lookup"><span data-stu-id="ec1ed-127">**scanner**</span></span>      | <span data-ttu-id="ec1ed-128">\_сканер ДЕВТИПЕ \_ MCI</span><span class="sxs-lookup"><span data-stu-id="ec1ed-128">MCI\_DEVTYPE\_SCANNER</span></span>         | <span data-ttu-id="ec1ed-129">Сканер изображений</span><span class="sxs-lookup"><span data-stu-id="ec1ed-129">Image scanner</span></span>                                    |
| <span data-ttu-id="ec1ed-130">**sequencer**</span><span class="sxs-lookup"><span data-stu-id="ec1ed-130">**sequencer**</span></span>    | <span data-ttu-id="ec1ed-131">Программа MCI \_ девтипе \_ Sequencer</span><span class="sxs-lookup"><span data-stu-id="ec1ed-131">MCI\_DEVTYPE\_SEQUENCER</span></span>       | <span data-ttu-id="ec1ed-132">Секвенсор MIDI</span><span class="sxs-lookup"><span data-stu-id="ec1ed-132">MIDI sequencer</span></span>                                   |
| <span data-ttu-id="ec1ed-133">**видеомагнитофон**</span><span class="sxs-lookup"><span data-stu-id="ec1ed-133">**vcr**</span></span>          | <span data-ttu-id="ec1ed-134">\_видеомагнитофон ДЕВТИПЕ \_ MCI</span><span class="sxs-lookup"><span data-stu-id="ec1ed-134">MCI\_DEVTYPE\_VCR</span></span>             | <span data-ttu-id="ec1ed-135">Устройство записи видеокассет или проигрыватель</span><span class="sxs-lookup"><span data-stu-id="ec1ed-135">Video-cassette recorder or player</span></span>                |
| <span data-ttu-id="ec1ed-136">**видеодиск**</span><span class="sxs-lookup"><span data-stu-id="ec1ed-136">**videodisc**</span></span>    | <span data-ttu-id="ec1ed-137">\_ВИДЕОДИСК MCI девтипе \_</span><span class="sxs-lookup"><span data-stu-id="ec1ed-137">MCI\_DEVTYPE\_VIDEODISC</span></span>       | <span data-ttu-id="ec1ed-138">Проигрыватель видеодиск</span><span class="sxs-lookup"><span data-stu-id="ec1ed-138">Videodisc player</span></span>                                 |
| <span data-ttu-id="ec1ed-139">**вавеаудио**</span><span class="sxs-lookup"><span data-stu-id="ec1ed-139">**waveaudio**</span></span>    | <span data-ttu-id="ec1ed-140">\_ \_ звуковая волна MCI девтипе \_</span><span class="sxs-lookup"><span data-stu-id="ec1ed-140">MCI\_DEVTYPE\_WAVEFORM\_AUDIO</span></span> | <span data-ttu-id="ec1ed-141">Звуковое устройство, воспроизводящее оцифрованные файлы звукозаписи</span><span class="sxs-lookup"><span data-stu-id="ec1ed-141">Audio device that plays digitized waveform files</span></span> |



 

<span data-ttu-id="ec1ed-142">В этом документе имена типов устройств выделены полужирным шрифтом.</span><span class="sxs-lookup"><span data-stu-id="ec1ed-142">In this document, the names of device types are bold.</span></span> <span data-ttu-id="ec1ed-143">Имена типов устройств используются с интерфейсом командной строки.</span><span class="sxs-lookup"><span data-stu-id="ec1ed-143">Device-type names are used with the command-string interface.</span></span> <span data-ttu-id="ec1ed-144">Константы типа устройства используются с интерфейсом командной строки.</span><span class="sxs-lookup"><span data-stu-id="ec1ed-144">Device-type constants are used with the command-message interface.</span></span>

 

 




