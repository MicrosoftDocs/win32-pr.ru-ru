---
description: В каждой операции резервного копирования и восстановления VSS используется протокол для взаимодействия систем, использующих запоминающие устройства (модули записи) и резервное копирование (запрашивающих).
ms.assetid: c4dae5ce-0dfa-46ec-909f-8ae79d50a9cb
title: Использование служба теневого копирования томов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06a1c81d79de30085f783feb02b7a7d47d5dc765
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541762"
---
# <a name="using-the-volume-shadow-copy-service"></a><span data-ttu-id="3233c-103">Использование служба теневого копирования томов</span><span class="sxs-lookup"><span data-stu-id="3233c-103">Using the Volume Shadow Copy Service</span></span>

<span data-ttu-id="3233c-104">В каждой операции резервного копирования и восстановления VSS используется протокол для взаимодействия систем, использующих запоминающие устройства (модули записи) и резервное копирование (запрашивающих).</span><span class="sxs-lookup"><span data-stu-id="3233c-104">VSS backup and restore operations each use a protocol for the interaction of the systems that use mass storage (writers) and those that back it up (requesters).</span></span>

<span data-ttu-id="3233c-105">Операции резервного копирования и восстановления в основном управляются инициатором запроса, который управляет поведением модуля записи и поставщика путем создания событий COM на уровне системы для обработки процессом записи.</span><span class="sxs-lookup"><span data-stu-id="3233c-105">Both backup and restore operations are primarily driven by the requester, which controls writer and provider behavior by generating systemwide COM events for the writer to process.</span></span> <span data-ttu-id="3233c-106">Поскольку методы генерации событий являются асинхронными, модули записи имеют ограниченный контроль над состоянием инициатора запроса через асинхронные обработчики, доступные для VSS (см. [**ивссасинк**](/windows/desktop/api/Vss/nn-vss-ivssasync)).</span><span class="sxs-lookup"><span data-stu-id="3233c-106">Because event-generating methods are asynchronous, writers do have limited control into the requester's state through the asynchronous handlers available to VSS (see [**IVssAsync**](/windows/desktop/api/Vss/nn-vss-ivssasync)).</span></span>

<span data-ttu-id="3233c-107">Для этого взаимодействия требуются основные структуры данных, описывающие файлы и группы файлов ([*компоненты*](vssgloss-c.md)), а также модель метаданных, которая позволяет хранить данные резервного копирования и разрешать обмен данными с модулем записи или запрашивающей стороны.</span><span class="sxs-lookup"><span data-stu-id="3233c-107">This interaction requires basic data structures describing files and groups of files ([*components*](vssgloss-c.md)), as well as a metadata model to allow the storage of backup information and to permit writer/requester communication.</span></span>

-   [<span data-ttu-id="3233c-108">Совместимость приложений VSS</span><span class="sxs-lookup"><span data-stu-id="3233c-108">VSS Application Compatibility</span></span>](usage-conventions.md)
-   [<span data-ttu-id="3233c-109">Настройка VSS</span><span class="sxs-lookup"><span data-stu-id="3233c-109">Configuring VSS</span></span>](configuring-vss.md)
-   [<span data-ttu-id="3233c-110">Метаданные VSS</span><span class="sxs-lookup"><span data-stu-id="3233c-110">VSS Metadata</span></span>](vss-metadata.md)
-   [<span data-ttu-id="3233c-111">Работа с выборкой и логическими путями</span><span class="sxs-lookup"><span data-stu-id="3233c-111">Working with Selectability and Logical Paths</span></span>](working-with-selectability-and-logical-paths.md)
-   [<span data-ttu-id="3233c-112">Общие сведения об обработке резервной копии в VSS</span><span class="sxs-lookup"><span data-stu-id="3233c-112">Overview of Processing a Backup Under VSS</span></span>](overview-of-processing-a-backup-under-vss.md)
-   [<span data-ttu-id="3233c-113">Общие сведения об обработке восстановления в VSS</span><span class="sxs-lookup"><span data-stu-id="3233c-113">Overview of Processing a Restore Under VSS</span></span>](overview-of-processing-a-restore-under-vss.md)

 

 



