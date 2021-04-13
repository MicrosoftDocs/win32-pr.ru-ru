---
title: Закрытие устройства
description: Закрытие устройства
ms.assetid: eef40f23-2c58-4deb-a6f0-3563d9c30d10
keywords:
- Команда MCI_CLOSE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 824d156baa72ee404f29ae490d4d9816078f4d15
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104410650"
---
# <a name="closing-a-device"></a><span data-ttu-id="0886d-104">Закрытие устройства</span><span class="sxs-lookup"><span data-stu-id="0886d-104">Closing a Device</span></span>

<span data-ttu-id="0886d-105">Команда [**Close**](close.md) ([**MCI \_ Close**](mci-close.md)) освобождает доступ к устройству или файлу.</span><span class="sxs-lookup"><span data-stu-id="0886d-105">The [**close**](close.md) ([**MCI\_CLOSE**](mci-close.md)) command releases access to a device or file.</span></span> <span data-ttu-id="0886d-106">MCI освобождает устройство, когда все задачи, использующие устройство, закрыли его.</span><span class="sxs-lookup"><span data-stu-id="0886d-106">MCI frees a device when all tasks using a device have closed it.</span></span> <span data-ttu-id="0886d-107">Чтобы помочь MCI управлять устройствами, приложение должно закрыть каждое устройство или файл по завершении его использования.</span><span class="sxs-lookup"><span data-stu-id="0886d-107">To help MCI manage the devices, your application must close each device or file when it is finished using it.</span></span>

<span data-ttu-id="0886d-108">Когда вы закрываете внешнее устройство MCI, использующее собственный носитель, а не файлы (например, CD Audio), драйвер оставляет устройство в текущем режиме работы.</span><span class="sxs-lookup"><span data-stu-id="0886d-108">When you close an external MCI device that uses its own media instead of files (such as CD audio), the driver leaves the device in its current mode of operation.</span></span> <span data-ttu-id="0886d-109">Таким словами, если вы закроете устройство воспроизведения компакт-дисков, даже если драйвер устройства выпущен из памяти, устройство воспроизведения компакт-дисков будет продолжать воспроизводиться до конца его содержимого.</span><span class="sxs-lookup"><span data-stu-id="0886d-109">Thus, if you close a CD audio device that is playing, even though the device driver is released from memory, the CD audio device will continue to play until it reaches the end of its content.</span></span>

> [!Note]  
> <span data-ttu-id="0886d-110">Закрытие приложения с открытыми устройствами MCI может помешать другим приложениям использовать эти устройства до перезапуска Windows.</span><span class="sxs-lookup"><span data-stu-id="0886d-110">Closing an application with open MCI devices can prevent other applications from using those devices until Windows is restarted.</span></span>

 

 

 




