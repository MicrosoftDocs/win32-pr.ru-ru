---
description: Существует ряд соглашений о поддерживаемых типах резервных копий&\# 8212, добавочных, разностных и полных&\# 8212; это служба VSS, а также Конфигурация резервного копирования довольно необычная в VSS.
ms.assetid: eddf29bc-221b-4b10-9842-a893b62fa846
title: Конфигурации резервного копирования VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4e4c4f383a208781722053b47ba9ae5bcbf1db7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692377"
---
# <a name="vss-backup-configurations"></a><span data-ttu-id="765e4-103">Конфигурации резервного копирования VSS</span><span class="sxs-lookup"><span data-stu-id="765e4-103">VSS Backup Configurations</span></span>

<span data-ttu-id="765e4-104">Существует ряд соглашений о поддержке типов резервных копий (добавочный, разностный и полный), о которых имеет значение Служба VSS, а также о настройке резервного копирования довольно необычная в VSS.</span><span class="sxs-lookup"><span data-stu-id="765e4-104">There are a number of conventionally supported backup types—incremental, differential, and full—that VSS is aware of, as well as a backup configuration peculiar to VSS.</span></span>

<span data-ttu-id="765e4-105">При определении конфигурации резервного копирования инициатор запроса и модули записи в системе указывают, как данные будут записываться на устройство хранения, как будет развернут механизм теневого копирования и какие сведения необходимо сохранить.</span><span class="sxs-lookup"><span data-stu-id="765e4-105">In defining a backup configuration, a requester and the writers on a system indicate how data will be written to a storage device, how the shadow copy mechanism will be deployed, and what information needs to be saved.</span></span> <span data-ttu-id="765e4-106">Взаимодействие между модулями записи и запрашивающими элементами определяется типом резервной копии, которую должен выполнить запрашивающий, и типами (или схемами), которые может поддерживать каждый модуль записи:</span><span class="sxs-lookup"><span data-stu-id="765e4-106">Interaction between writers and requesters is determined by the type of backup a requester wants to perform and the kinds (or schemas) that each writer can support:</span></span>

-   [<span data-ttu-id="765e4-107">Состояние резервного копирования VSS</span><span class="sxs-lookup"><span data-stu-id="765e4-107">VSS Backup State</span></span>](vss-backup-state.md)
-   [<span data-ttu-id="765e4-108">Поддержка схемы резервного копирования модуля записи</span><span class="sxs-lookup"><span data-stu-id="765e4-108">Writer Backup Schema Support</span></span>](writer-backup-schema-support.md)
-   [<span data-ttu-id="765e4-109">Поддержка схемы на уровне файлов</span><span class="sxs-lookup"><span data-stu-id="765e4-109">File Level Schema Support</span></span>](file-level-schema-support.md)

 

 



