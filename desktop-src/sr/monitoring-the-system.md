---
title: Мониторинг системы
description: Мониторинг системы
ms.assetid: e0318aca-4e3e-4272-ba31-c770d6b05272
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da7d18f42ac091b9c73c4d9a9ac3929bed235310
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104410569"
---
# <a name="monitoring-the-system"></a><span data-ttu-id="8caea-103">Мониторинг системы</span><span class="sxs-lookup"><span data-stu-id="8caea-103">Monitoring the System</span></span>

<span data-ttu-id="8caea-104">Восстановление системы в Windows Vista и более поздних версиях сохраняет копию тома при создании точки восстановления.</span><span class="sxs-lookup"><span data-stu-id="8caea-104">System Restore in Windows Vista and later saves a copy of the volume when generating a restore point.</span></span> <span data-ttu-id="8caea-105">Для восстановления системы требуется не менее 300 МБ свободного дискового пространства на системном диске при установке.</span><span class="sxs-lookup"><span data-stu-id="8caea-105">System Restore requires a minimum of 300 MB of free disk space on the system drive at installation.</span></span>

<span data-ttu-id="8caea-106">Восстановление системы в Windows XP отслеживает основной набор файлов системы и приложений, заархивирование состояний этих файлов до внесения изменений в систему.</span><span class="sxs-lookup"><span data-stu-id="8caea-106">System Restore in Windows XP monitors a core set of system and application files, archiving the states of these files before system changes are made.</span></span> <span data-ttu-id="8caea-107">Восстановление системы также сохраняет полный снимок реестра и некоторые динамические системные файлы.</span><span class="sxs-lookup"><span data-stu-id="8caea-107">System Restore also saves a full snapshot of the registry and some dynamic system files.</span></span> <span data-ttu-id="8caea-108">Для восстановления системы требуется не менее 200 МБ свободного дискового пространства на системном диске при установке.</span><span class="sxs-lookup"><span data-stu-id="8caea-108">System Restore requires a minimum of 200 MB of free disk space on the system drive at installation.</span></span> <span data-ttu-id="8caea-109">Когда объем свободного дискового пространства становится меньше 50 МБ на любом диске, восстановление системы переключается в режим ожидания и прекращает создание точек восстановления.</span><span class="sxs-lookup"><span data-stu-id="8caea-109">When the amount of free disk space falls below 50 MB on any drive, System Restore switches to standby mode and stops creating restore points.</span></span> <span data-ttu-id="8caea-110">Все точки восстановления удаляются в это время.</span><span class="sxs-lookup"><span data-stu-id="8caea-110">All restore points are deleted at that time.</span></span> <span data-ttu-id="8caea-111">Восстановление системы повторно активирует и возобновляет создание точек восстановления, как только на системном диске освободится 200 МБ свободного места.</span><span class="sxs-lookup"><span data-stu-id="8caea-111">System Restore reactivates and resumes creating restore points as soon as 200 MB of disk space is free on the system drive.</span></span> <span data-ttu-id="8caea-112">Файлы, которые отслеживаются или исключаются из наблюдения, указываются в файле% WINDIR% \\ system32 \\ restore \\Filelist.xml.</span><span class="sxs-lookup"><span data-stu-id="8caea-112">The files that are monitored or excluded from monitoring are specified in the file %windir%\\system32\\restore\\Filelist.xml.</span></span> <span data-ttu-id="8caea-113">Дополнительные сведения см. в разделе [отслеживаемые расширения имен файлов](monitored-file-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="8caea-113">For more information, see [Monitored File Name Extensions](monitored-file-extensions.md).</span></span>

 

 




