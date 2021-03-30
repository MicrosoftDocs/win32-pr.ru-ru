---
title: Получение сообщений Running-Status
description: Получение сообщений Running-Status
ms.assetid: 4f2e8e41-89f6-45e3-ae16-47b856f0e63e
keywords:
- Цифровой интерфейс музыкального инструмента (MIDI), состояние выполнения
- MIDI (цифровой интерфейс музыкального инструмента), состояние выполнения
- запись звука MIDI, состояние выполнения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0a4d12a19f525a6fa673747063774bf4507d65b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104410649"
---
# <a name="receiving-running-status-messages"></a><span data-ttu-id="ca3aa-106">Получение сообщений Running-Status</span><span class="sxs-lookup"><span data-stu-id="ca3aa-106">Receiving Running-Status Messages</span></span>

<span data-ttu-id="ca3aa-107">*Стандартная спецификация файлов MIDI 1,0* позволяет использовать *состояние выполнения* , если сообщение имеет тот же самый байт состояния, что и предыдущее сообщение.</span><span class="sxs-lookup"><span data-stu-id="ca3aa-107">The *Standard MIDI Files 1.0* specification allows the use of *running status* when a message has the same status byte as the previous message.</span></span> <span data-ttu-id="ca3aa-108">Если используется состояние выполнения, то байт состояния последующих сообщений можно опустить.</span><span class="sxs-lookup"><span data-stu-id="ca3aa-108">When running status is used, the status byte of subsequent messages can be omitted.</span></span> <span data-ttu-id="ca3aa-109">Все драйверы устройств ввода MIDI необходимы для расширения сообщений, использующих состояние выполнения, в полные сообщения, чтобы всегда отправлять сообщения MIDI от драйвера устройства ввода MIDI.</span><span class="sxs-lookup"><span data-stu-id="ca3aa-109">All MIDI input device drivers are required to expand messages using running status into complete messages, so that you always receive complete MIDI messages from a MIDI input device driver.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ca3aa-110">См. также</span><span class="sxs-lookup"><span data-stu-id="ca3aa-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ca3aa-111">Запись звука MIDI</span><span class="sxs-lookup"><span data-stu-id="ca3aa-111">Recording MIDI Audio</span></span>](recording-midi-audio.md)
</dt> </dl>

 

 




