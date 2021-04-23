---
description: Ведение журнала и отчеты об ошибках
ms.assetid: 162ce34b-cc82-40bb-8422-a639152aee25
title: Ведение журнала и отчеты об ошибках
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cdc29d32ae26429f2fe23fe88762fabf82185c7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673143"
---
# <a name="logging-and-error-reporting"></a><span data-ttu-id="0b0f4-103">Ведение журнала и отчеты об ошибках</span><span class="sxs-lookup"><span data-stu-id="0b0f4-103">Logging and Error Reporting</span></span>

## <a name="log-file"></a><span data-ttu-id="0b0f4-104">Файл журнала</span><span class="sxs-lookup"><span data-stu-id="0b0f4-104">Log file</span></span>

<span data-ttu-id="0b0f4-105">COMREPL создает файл журнала, содержащий состояние и сообщения об ошибках.</span><span class="sxs-lookup"><span data-stu-id="0b0f4-105">COMREPL generates a log file containing status and error messages.</span></span> <span data-ttu-id="0b0f4-106">Этот файл хранится на компьютере, где COMREPL был запущен в% системдир% \\ COM- \\ репликации \\ Comrepl. log.</span><span class="sxs-lookup"><span data-stu-id="0b0f4-106">This file is stored on the computer where COMREPL was launched in %systemdir%\\com\\replication\\ComRepl.log.</span></span>

<span data-ttu-id="0b0f4-107">Этот файл журнала удаляется при запуске фазы копирования.</span><span class="sxs-lookup"><span data-stu-id="0b0f4-107">This log file is cleared when a copy phase is started.</span></span> <span data-ttu-id="0b0f4-108">При последующей установке в целевые объекты будут добавлены к файлу.</span><span class="sxs-lookup"><span data-stu-id="0b0f4-108">Subsequent installation on targets will append to the file.</span></span>

## <a name="error-handling"></a><span data-ttu-id="0b0f4-109">Обработка ошибок</span><span class="sxs-lookup"><span data-stu-id="0b0f4-109">Error handling</span></span>

<span data-ttu-id="0b0f4-110">Ошибки указаны в файле журнала, описанном выше.</span><span class="sxs-lookup"><span data-stu-id="0b0f4-110">Errors are noted in the log file described above.</span></span> <span data-ttu-id="0b0f4-111">Подробные сведения об ошибках также можно найти в журнале событий на исходном или целевом компьютере.</span><span class="sxs-lookup"><span data-stu-id="0b0f4-111">Detailed error information may also be found in the event log on source or target computers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0b0f4-112">См. также</span><span class="sxs-lookup"><span data-stu-id="0b0f4-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0b0f4-113">Управление файлами</span><span class="sxs-lookup"><span data-stu-id="0b0f4-113">File Management</span></span>](file-management.md)
</dt> <dt>

[<span data-ttu-id="0b0f4-114">Этапы репликации</span><span class="sxs-lookup"><span data-stu-id="0b0f4-114">Replication Phases</span></span>](replication-phases.md)
</dt> <dt>

[<span data-ttu-id="0b0f4-115">Использование COMREPL</span><span class="sxs-lookup"><span data-stu-id="0b0f4-115">Using COMREPL</span></span>](using-comrepl.md)
</dt> <dt>

[<span data-ttu-id="0b0f4-116">Что реплицируется</span><span class="sxs-lookup"><span data-stu-id="0b0f4-116">What Gets Replicated</span></span>](what-gets-replicated.md)
</dt> </dl>

 

 



