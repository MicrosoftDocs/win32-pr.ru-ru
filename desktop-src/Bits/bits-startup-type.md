---
title: Тип запуска BITS
description: Тип запуска BITS — задержка автоматического запуска. До Windows Vista в качестве типа запуска для BITS используется ручной режим. При создании задания BITS тип запуска меняется на автоматический. Тип запуска возвращается в ручное состояние после завершения или отмены всех заданий.
ms.assetid: 0d9ec60f-3488-4eb2-a6a2-22932fd74caf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd1ce1dcd2f939237142a0afd44e49b4b63df419
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104410637"
---
# <a name="bits-startup-type"></a><span data-ttu-id="16405-106">Тип запуска BITS</span><span class="sxs-lookup"><span data-stu-id="16405-106">BITS Startup Type</span></span>

<span data-ttu-id="16405-107">**Тип запуска** BITS — это отложенный автоматический запуск (при наличии активных заданий BITS) или запуск по требованию (если активные задания отсутствуют).</span><span class="sxs-lookup"><span data-stu-id="16405-107">The **Startup Type** for BITS is delayed auto-start (if there are active BITS jobs) or demand start (if there are no active jobs).</span></span> <span data-ttu-id="16405-108">Версии Windows до обновления за ноябрь использовали только тип запуска отложенного автоматического запуска; в версиях, предшествовавших версии Vista, используется ручной тип запуска.</span><span class="sxs-lookup"><span data-stu-id="16405-108">Versions of Windows prior to the November Update used only the delayed auto-start startup type; versions prior to Vista used the manual startup type.</span></span>

<span data-ttu-id="16405-109">Не следует задавать для параметра **Тип запуска** значение отключено.</span><span class="sxs-lookup"><span data-stu-id="16405-109">You should not set the **Startup Type** to Disabled.</span></span> <span data-ttu-id="16405-110">Отключение BITS может привести к нарушению работы приложений, использующих BITS для передачи файлов.</span><span class="sxs-lookup"><span data-stu-id="16405-110">Disabling BITS may break applications that rely on BITS to transfer files.</span></span>

 

 




