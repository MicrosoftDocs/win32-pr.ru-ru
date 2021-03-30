---
title: Остановка, приостановка и возобновление работы устройства
description: Остановка, приостановка и возобновление работы устройства
ms.assetid: df9ca4ab-4711-44dd-a058-909f291a1652
keywords:
- Команда MCI_STOP
- Команда MCI_PAUSE
- Команда MCI_RESUME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ddcd9618608226dec108d62754964fe6401d429
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103776238"
---
# <a name="stopping-pausing-and-resuming-a-device"></a><span data-ttu-id="a45f6-106">Остановка, приостановка и возобновление работы устройства</span><span class="sxs-lookup"><span data-stu-id="a45f6-106">Stopping, Pausing, and Resuming a Device</span></span>

<span data-ttu-id="a45f6-107">Команда [**остановить**](stop.md) ([**MCI \_ остановить**](mci-stop.md)) приостанавливает воспроизведение или запись устройства.</span><span class="sxs-lookup"><span data-stu-id="a45f6-107">The [**stop**](stop.md) ([**MCI\_STOP**](mci-stop.md)) command suspends the playing or recording of a device.</span></span> <span data-ttu-id="a45f6-108">Многие устройства также поддерживают команду [**Pause**](pause.md) ([**\_ Пауза MCI**](mci-pause.md)).</span><span class="sxs-lookup"><span data-stu-id="a45f6-108">Many devices also support the [**pause**](pause.md) ([**MCI\_PAUSE**](mci-pause.md)) command.</span></span> <span data-ttu-id="a45f6-109">Разница между **остановкой** и **приостановкой** зависит от устройства.</span><span class="sxs-lookup"><span data-stu-id="a45f6-109">The difference between **stop** and **pause** depends on the device.</span></span> <span data-ttu-id="a45f6-110">Обычно **приостанавливает** выполнение операции приостановки, но оставляет устройство готовым к возобновлению воспроизведения или записи немедленно.</span><span class="sxs-lookup"><span data-stu-id="a45f6-110">Usually **pause** suspends operation but leaves the device ready to resume playing or recording immediately.</span></span>

<span data-ttu-id="a45f6-111">При использовании команды [**воспроизвести**](play.md) ([**MCI \_ Play**](mci-play.md)) или [**записи**](record.md) ([**\_ запись MCI**](mci-record.md)) для перезапуска устройства сбрасываются значения, указанные с помощью флагов "Кому" (MCI \_ ) и "от" (MCI \_ из) перед приостановкой или остановкой устройства.</span><span class="sxs-lookup"><span data-stu-id="a45f6-111">Using the [**play**](play.md) ([**MCI\_PLAY**](mci-play.md)) or [**record**](record.md) ([**MCI\_RECORD**](mci-record.md)) command to restart a device resets the locations specified with the "to" (MCI\_TO) and "from" (MCI\_FROM) flags before the device was paused or stopped.</span></span> <span data-ttu-id="a45f6-112">Без флага "от" эти команды сбрасывают начальное расположение до текущей позиции.</span><span class="sxs-lookup"><span data-stu-id="a45f6-112">Without the "from" flag, these commands reset the starting location to the current position.</span></span> <span data-ttu-id="a45f6-113">Без флага "Кому" они сбрасывают конечное расположение до конца носителя.</span><span class="sxs-lookup"><span data-stu-id="a45f6-113">Without the "to" flag, they reset the ending location to the end of the media.</span></span> <span data-ttu-id="a45f6-114">Чтобы продолжить воспроизведение или запись без сброса ранее указанной позиции окончания, используйте флаг "to" для команды **воспроизведения** или **записи** , чтобы указать конечную точку.</span><span class="sxs-lookup"><span data-stu-id="a45f6-114">To continue playing or recording without resetting a previously specified stop position, use the **play** or **record** command's "to" flag to specify an ending position.</span></span>

<span data-ttu-id="a45f6-115">Некоторые устройства поддерживают команду [**Resume**](resume.md) ([**\_ возобновление MCI**](mci-resume.md)) для перезапуска приостановленного устройства.</span><span class="sxs-lookup"><span data-stu-id="a45f6-115">Some devices support the [**resume**](resume.md) ([**MCI\_RESUME**](mci-resume.md)) command to restart a paused device.</span></span> <span data-ttu-id="a45f6-116">Эта команда не изменяет расположения "to" и "from", указанные с помощью команды **Play** или **Record** , предшествующей команде [**Pause**](pause.md) .</span><span class="sxs-lookup"><span data-stu-id="a45f6-116">This command does not change the "to" and "from" locations specified with the **play** or **record** command that preceded the [**pause**](pause.md) command.</span></span>

 

 




