---
description: Прежде чем можно будет использовать журнал файлов, необходимо вызвать Сетупинитиализефилелог, чтобы открыть или создать его. При вызове этой функции можно указать флаги для создания или перезаписи журнала файлов, открытия системного журнала или открытия журнала файлов с правами только для чтения.
ms.assetid: 7ab133f6-2088-4bca-bf24-d3dcb29376a1
title: Использование журнала файлов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf7f1e3d27ba7d42d448a1eac48d60246c2b40db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999758"
---
# <a name="using-the-file-log"></a><span data-ttu-id="e8fc2-104">Использование журнала файлов</span><span class="sxs-lookup"><span data-stu-id="e8fc2-104">Using the File Log</span></span>

<span data-ttu-id="e8fc2-105">Прежде чем можно будет использовать журнал файлов, необходимо вызвать [**сетупинитиализефилелог**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitializefileloga) , чтобы открыть или создать его.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-105">Before you can use a file log, you must call [**SetupInitializeFileLog**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitializefileloga) to open or create it.</span></span> <span data-ttu-id="e8fc2-106">При вызове этой функции можно указать флаги для создания или перезаписи журнала файлов, открытия системного журнала или открытия журнала файлов с правами только для чтения.</span><span class="sxs-lookup"><span data-stu-id="e8fc2-106">When you call this function, you can specify flags to create or overwrite a file log, open the system log, or open a file log as read-only.</span></span>

<span data-ttu-id="e8fc2-107">После того как [**сетупинитиализефилелог**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitializefileloga) возвращает маркер в файл журнала, можно добавить запись, вызвав [**SetupLogFile**](/windows/desktop/api/Setupapi/nf-setupapi-setuplogfilea), удалить запись путем вызова [**сетупремовефилеложентри**](/windows/desktop/api/Setupapi/nf-setupapi-setupremovefilelogentrya)или получить сведения о конкретном файле в журнале файлов, вызвав [**сетупкуерифилелог**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryfileloga).</span><span class="sxs-lookup"><span data-stu-id="e8fc2-107">After [**SetupInitializeFileLog**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitializefileloga) returns a handle to a file log, you can add an entry by calling [**SetupLogFile**](/windows/desktop/api/Setupapi/nf-setupapi-setuplogfilea), delete an entry by calling [**SetupRemoveFileLogEntry**](/windows/desktop/api/Setupapi/nf-setupapi-setupremovefilelogentrya), or retrieve information about a particular file in a file log by calling [**SetupQueryFileLog**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryfileloga).</span></span>

<span data-ttu-id="e8fc2-108">Если файловый журнал больше не нужен, [**сетуптерминатефилелог**](/windows/desktop/api/Setupapi/nf-setupapi-setupterminatefilelog) должен быть вызван для освобождения ресурсов, выделенных во время вызова [**сетупинитиализефилелог**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitializefileloga).</span><span class="sxs-lookup"><span data-stu-id="e8fc2-108">When the file log is no longer needed, [**SetupTerminateFileLog**](/windows/desktop/api/Setupapi/nf-setupapi-setupterminatefilelog) should be called to release the resources allocated during the call to [**SetupInitializeFileLog**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitializefileloga).</span></span>

 

 



