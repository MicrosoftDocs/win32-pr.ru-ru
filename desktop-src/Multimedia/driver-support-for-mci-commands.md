---
title: Поддержка драйверов для команд MCI
description: Поддержка драйверов для команд MCI
ms.assetid: 1adea076-c04e-4613-a793-60de41b2e9db
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64b57e28feaa3fd1e0b4d7f3edc7c95df3f00e83
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103775122"
---
# <a name="driver-support-for-mci-commands"></a><span data-ttu-id="a6295-103">Поддержка драйверов для команд MCI</span><span class="sxs-lookup"><span data-stu-id="a6295-103">Driver Support for MCI Commands</span></span>

<span data-ttu-id="a6295-104">Драйверы MCI предоставляют функциональные возможности команд MCI.</span><span class="sxs-lookup"><span data-stu-id="a6295-104">MCI drivers provide the functionality for MCI commands.</span></span> <span data-ttu-id="a6295-105">Системное программное обеспечение выполняет некоторые основные задачи управления данными, но все воспроизведение, презентация и запись мультимедиа обрабатываются отдельными драйверами MCI.</span><span class="sxs-lookup"><span data-stu-id="a6295-105">The system software performs some basic data-management tasks, but all the multimedia playback, presentation, and recording is handled by the individual MCI drivers.</span></span>

<span data-ttu-id="a6295-106">Драйверы различаются в поддержке команд MCI и флагов команд.</span><span class="sxs-lookup"><span data-stu-id="a6295-106">Drivers vary in their support for MCI commands and command flags.</span></span> <span data-ttu-id="a6295-107">Так как мультимедийные устройства могут иметь широко разные возможности, MCI разрабатывает, чтобы отдельные драйверы могли расширять или уменьшать наборы команд в соответствии с возможностями устройства.</span><span class="sxs-lookup"><span data-stu-id="a6295-107">Because multimedia devices can have widely different capabilities, MCI is designed to let individual drivers extend or reduce the command sets to match the capabilities of the device.</span></span> <span data-ttu-id="a6295-108">Например, команда [**Record**](record.md) ([**\_ запись MCI**](mci-record.md)) является частью набора команд для средств нумерации MIDI, но драйвер МЦисек, входящий в состав Windows, не поддерживает эту команду.</span><span class="sxs-lookup"><span data-stu-id="a6295-108">For example, the [**record**](record.md) ([**MCI\_RECORD**](mci-record.md)) command is part of the command set for MIDI sequencers, but the MCISEQ driver included with Windows does not support this command.</span></span> <span data-ttu-id="a6295-109">В справочном разделе, посвященном команде Record, объясняется, что устройства типа устройства **Sequencer** распознают команду. Это не означает, что все устройства этого типа поддерживают команду.</span><span class="sxs-lookup"><span data-stu-id="a6295-109">The reference topic for the record command explains that devices of the **sequencer** device type recognize the command; this does not mean that all devices of this type support the command.</span></span> <span data-ttu-id="a6295-110">Для определения возможностей конкретного устройства в приложениях следует использовать команду [**capability**](capability.md) ([**MCI \_ жетдевкапс**](mci-getdevcaps.md)).</span><span class="sxs-lookup"><span data-stu-id="a6295-110">Applications should use the [**capability**](capability.md) ([**MCI\_GETDEVCAPS**](mci-getdevcaps.md)) command to determine the capabilities of a particular device.</span></span>

 

 




