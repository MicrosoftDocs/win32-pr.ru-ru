---
title: Воспроизведение и позиционирование
description: Воспроизведение и позиционирование
ms.assetid: fbf9294e-c644-45c7-ab60-dd903409a44f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1efbd6256fbd0d258f5d5c9d3da9b01c72a203dd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105650274"
---
# <a name="playback-and-positioning"></a><span data-ttu-id="54aa9-103">Воспроизведение и позиционирование</span><span class="sxs-lookup"><span data-stu-id="54aa9-103">Playback and Positioning</span></span>

<span data-ttu-id="54aa9-104">Ряд команд MCI, таких как [**Play**](play.md) ([**MCI \_ Play**](mci-play.md)), [**Остановка**](stop.md) ([**\_ Остановка MCI**](mci-stop.md)), [**Пауза**](pause.md) ([**\_ Пауза MCI**](mci-pause.md)), [**возобновление**](resume.md) ([**MCI \_ Resume**](mci-resume.md)) и [**Seek**](seek.md) ([**\_ Поиск MCI**](mci-seek.md)), влияют на воспроизведение или размещение файла мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="54aa9-104">A number of MCI commands, such as [**play**](play.md) ([**MCI\_PLAY**](mci-play.md)), [**stop**](stop.md) ([**MCI\_STOP**](mci-stop.md)), [**pause**](pause.md) ([**MCI\_PAUSE**](mci-pause.md)), [**resume**](resume.md) ([**MCI\_RESUME**](mci-resume.md)), and [**seek**](seek.md) ([**MCI\_SEEK**](mci-seek.md)), affect the playback or positioning of a multimedia file.</span></span> <span data-ttu-id="54aa9-105">Если устройство MCI получает команду воспроизведения во время выполнения другой команды воспроизведения, оно принимает команду и либо останавливает, либо заменяет предыдущую команду.</span><span class="sxs-lookup"><span data-stu-id="54aa9-105">If an MCI device receives a playback command while another playback command is in progress, it accepts the command and either stops or supersedes the previous command.</span></span>

<span data-ttu-id="54aa9-106">Многие команды MCI, такие как [**Set**](set.md) ([**\_ набор MCI**](mci-set.md)), не влияют на воспроизведение.</span><span class="sxs-lookup"><span data-stu-id="54aa9-106">Many MCI commands, such as [**set**](set.md) ([**MCI\_SET**](mci-set.md)), do not affect playback.</span></span> <span data-ttu-id="54aa9-107">Уведомление одной из этих команд не мешает откладывать команды воспроизведения или позиционирования, пока уведомления не будут выполняться из одного и того же экземпляра драйвера.</span><span class="sxs-lookup"><span data-stu-id="54aa9-107">A notification from one of these commands does not interfere with pending playback or position commands as long as the notifications are not performed from the same instance of the driver.</span></span> <span data-ttu-id="54aa9-108">Например, можно выдать команду **Set** или [**Status**](status.md) ([**\_ состояние MCI**](mci-status.md)), пока устройство выполняет команду **Seek** без остановки или замены команды **Seek** .</span><span class="sxs-lookup"><span data-stu-id="54aa9-108">For example, you can issue a **set** or [**status**](status.md) ([**MCI\_STATUS**](mci-status.md)) command while a device is performing a **seek** command without stopping or superseding the **seek** command.</span></span>

<span data-ttu-id="54aa9-109">Однако может существовать только одно ожидающее уведомление.</span><span class="sxs-lookup"><span data-stu-id="54aa9-109">However, there can be only one pending notification.</span></span> <span data-ttu-id="54aa9-110">Например, если приложение запрашивает уведомление для **воспроизведения** и соответствует этому запросу с **состоянием** "уведомление об начальной должности", уведомление о **воспроизведении** будет возвращать "заменено", а уведомление для команды Status будет возвращено по завершении.</span><span class="sxs-lookup"><span data-stu-id="54aa9-110">For example, if an application requests a notification for **play** and follows that request with **status** "start position notify," the **play** notification will return "superseded" and the notification for the status command will return when it is finished.</span></span> <span data-ttu-id="54aa9-111">Однако в этом случае команда **Play** по-прежнему будет выполнена успешно, даже если приложение не получило уведомление.</span><span class="sxs-lookup"><span data-stu-id="54aa9-111">In this case, however, the **play** command will still succeed, even though the application did not receive the notification.</span></span>

 

 




