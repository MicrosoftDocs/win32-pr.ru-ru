---
title: Имена устройств
description: Имена устройств
ms.assetid: 0ba06439-cc33-43e1-a094-09bcc5e2f6b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e516f7f8eed338067dc373f8509f46598e198c71
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104487045"
---
# <a name="device-names"></a><span data-ttu-id="260fb-103">Имена устройств</span><span class="sxs-lookup"><span data-stu-id="260fb-103">Device Names</span></span>

<span data-ttu-id="260fb-104">Для каждого типа устройства может существовать несколько драйверов MCI, которые совместно используют набор команд, но работают с различными форматами данных.</span><span class="sxs-lookup"><span data-stu-id="260fb-104">For each device type, there might be several MCI drivers that share the command set but operate on different data formats.</span></span> <span data-ttu-id="260fb-105">Для уникальной идентификации драйвера MCI MCI использует *имена устройств*.</span><span class="sxs-lookup"><span data-stu-id="260fb-105">To uniquely identify an MCI driver, MCI uses *device names*.</span></span>

<span data-ttu-id="260fb-106">Имена устройств идентифицируются либо в \[ разделе MCI \] файла SYSTEM.INI, либо в соответствующей части реестра.</span><span class="sxs-lookup"><span data-stu-id="260fb-106">Device names are identified either in the \[mci\] section of the SYSTEM.INI file or in the appropriate part of the registry.</span></span> <span data-ttu-id="260fb-107">Эта информация определяет все драйверы MCI для Windows.</span><span class="sxs-lookup"><span data-stu-id="260fb-107">This information identifies all MCI drivers to Windows.</span></span> <span data-ttu-id="260fb-108">Записи в \[ \] разделе MCI используют следующую форму:</span><span class="sxs-lookup"><span data-stu-id="260fb-108">The entries in the \[mci\] section use the following form:</span></span>

<span data-ttu-id="260fb-109">*\_ имя файла драйвера имени устройства*  =  *\_ . расширение*</span><span class="sxs-lookup"><span data-stu-id="260fb-109">*device\_name* = *driver\_filename.extension*</span></span>

<span data-ttu-id="260fb-110">В следующем примере показан типичный \[ \] раздел mci из SYSTEM.INI.</span><span class="sxs-lookup"><span data-stu-id="260fb-110">The following example shows a typical \[mci\] section from SYSTEM.INI:</span></span>


```C++
[mci]
cdaudio=mcicda.drv 
sequencer=mciseq.drv 
waveaudio=mciwave.drv 
avivideo=mciavi.drv
```



<span data-ttu-id="260fb-111">Если драйвер MCI установлен с использованием имени устройства, которое уже существует в SYSTEM.INI или в реестре, система добавляет целое число в имя устройства нового драйвера, создавая уникальное имя устройства.</span><span class="sxs-lookup"><span data-stu-id="260fb-111">If an MCI driver is installed using a device name that already exists in SYSTEM.INI or the registry, the system appends an integer to the device name of the new driver, creating a unique device name.</span></span> <span data-ttu-id="260fb-112">В предыдущем примере дополнительному драйверу, установленному с помощью имени устройства "кдаудио", будет назначено имя устройства "cdaudio1".</span><span class="sxs-lookup"><span data-stu-id="260fb-112">In the preceding example, an additional driver installed using the "cdaudio" device name would be assigned the device name "cdaudio1".</span></span>

 

 




