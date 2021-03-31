---
title: Устаревшая ссылка на восстановление системы
description: В этой документации описываются сведения о реализации репозитория, используемого устаревшей версией восстановления системы. Он не применяется к реализации восстановления системы в Windows Vista.
ms.assetid: d221e83d-beb0-405c-b332-a3ab8aaef688
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be8703cbf88b97458f07c616d48405708e25acec
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103887695"
---
# <a name="legacy-system-restore-reference"></a><span data-ttu-id="fd92f-104">Устаревшая ссылка на восстановление системы</span><span class="sxs-lookup"><span data-stu-id="fd92f-104">Legacy System Restore Reference</span></span>

<span data-ttu-id="fd92f-105">\[Эти сведения относятся только к Windows XP с пакетом обновления 2 (SP2).\]</span><span class="sxs-lookup"><span data-stu-id="fd92f-105">\[This information applies only to Windows XP with Service Pack 2 (SP2).\]</span></span>

<span data-ttu-id="fd92f-106">В этой документации описываются сведения о реализации репозитория, используемого устаревшей версией восстановления системы.</span><span class="sxs-lookup"><span data-stu-id="fd92f-106">This documentation describes implementation details of the repository used by a legacy version of System Restore.</span></span> <span data-ttu-id="fd92f-107">Он не применяется к реализации восстановления системы в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="fd92f-107">It does not apply to the implementation of System Restore on Windows Vista.</span></span>

## <a name="system-restore-repository-structure"></a><span data-ttu-id="fd92f-108">Структура репозитория восстановления системы</span><span class="sxs-lookup"><span data-stu-id="fd92f-108">System Restore Repository Structure</span></span>

<span data-ttu-id="fd92f-109">Windows XP с пакетом обновления 2 (SP2) содержит репозиторий для восстановления системы в следующей папке:% SYSTEMDRIVE% \\ сведения о системном томе.</span><span class="sxs-lookup"><span data-stu-id="fd92f-109">Windows XP with SP2 contains a repository for System Restore in the following folder: %SYSTEMDRIVE%\\System Volume Information.</span></span> <span data-ttu-id="fd92f-110">Этот репозиторий содержит сведения для точек восстановления, которые по сути являются моментальным снимком системы в данный момент времени.</span><span class="sxs-lookup"><span data-stu-id="fd92f-110">This repository contains information for restore points, which are essentially a snapshot of the system at a moment in time.</span></span>

<span data-ttu-id="fd92f-111">Репозиторий структурирован следующим образом:</span><span class="sxs-lookup"><span data-stu-id="fd92f-111">The repository is structured as follows:</span></span>

<span data-ttu-id="fd92f-112">Восстановление **сведений о системных томах**    \*\* \_ {*GUID*}\*\*       **Rp1**       **RP2**       **RP *n*-1**       **RP \* n** \*     \*\* \_ RESTORE {*GUID*}\*\*       **Rp1**       **RP2**       **RP *n*-1**       **RP \* n**\*</span><span class="sxs-lookup"><span data-stu-id="fd92f-112">**System Volume Information**    **\_restore{*GUID*}**       **RP1**       **RP2**       **RP *n*-1**       **RP\*n**\*    **\_restore{*GUID*}**       **RP1**       **RP2**       **RP *n*-1**       **RP\*n**\*</span></span>

<span data-ttu-id="fd92f-113">Чтобы определить \_ , какую папку Restore {*GUID*} использовать, прочитайте **идентификатор GUID** , указанный в следующем файле: SYSTEMROOT% \\ system32 \\ RESTORE \\MachineGUID.txt.</span><span class="sxs-lookup"><span data-stu-id="fd92f-113">To determine which \_restore{*GUID*} folder to use, read the **GUID** specified in the following file: SYSTEMROOT%\\System32\\Restore\\MachineGUID.txt.</span></span>

<span data-ttu-id="fd92f-114">В каждой \_ папке Restore {*GUID*} \_ файл driver. cfg содержит сведения из структуры **\_ постоянной \_ конфигурации SR** , определенные следующим образом.</span><span class="sxs-lookup"><span data-stu-id="fd92f-114">Within each \_restore{*GUID*} folder, the \_driver.cfg file contains information from a **SR\_PERSISTENT\_CONFIG** structure defined as follows:</span></span>

``` syntax
typedef struct _SR_PERSISTENT_CONFIG
 {      
  ULONG Signature;            // Set to CPrs
  ULONG FileNameNumber;       // Number for next temp file 
                              // For example, A0000001 would be 1  
  INT64 FileSeqNumber;        // Next sequence number
  ULONG CurrentRestoreNumber; // For example, RP5 would be 5
 } SR_PERSISTENT_CONFIG, * PSR_PERSISTENT_CONFIG;
```

## <a name="files-contained-in-each-rpnfolder"></a><span data-ttu-id="fd92f-115">Файлы, содержащиеся в каждой папке RP *n*</span><span class="sxs-lookup"><span data-stu-id="fd92f-115">Files Contained in Each RP *n* Folder</span></span>

<span data-ttu-id="fd92f-116">Каждая папка RP *n* содержит папку моментальных снимков, которая содержит следующее:</span><span class="sxs-lookup"><span data-stu-id="fd92f-116">Each RP *n* folder contains a Snapshot folder that contains the following:</span></span>

-   <span data-ttu-id="fd92f-117">Моментальный снимок кустов реестра</span><span class="sxs-lookup"><span data-stu-id="fd92f-117">A snapshot of the registry hives</span></span>
-   <span data-ttu-id="fd92f-118">Папка репозитория, содержащая моментальный снимок репозитория WMI.</span><span class="sxs-lookup"><span data-stu-id="fd92f-118">A Repository folder that contains a snapshot of the WMI repository</span></span>
-   <span data-ttu-id="fd92f-119">Моментальный снимок базы данных COM+</span><span class="sxs-lookup"><span data-stu-id="fd92f-119">A snapshot of the COM+ database</span></span>
-   <span data-ttu-id="fd92f-120">Моментальный снимок базы данных IIS</span><span class="sxs-lookup"><span data-stu-id="fd92f-120">A snapshot of the IIS database</span></span>

<span data-ttu-id="fd92f-121">Каждая папка RP *n* содержит файл RP. log, содержащий общие сведения о точке восстановления из структуры [**ресторепоинтинфов**](/windows/win32/api/srrestoreptapi/ns-srrestoreptapi-restorepointinfoa) .</span><span class="sxs-lookup"><span data-stu-id="fd92f-121">Each RP *n* folder contains an RP.log file that contains general information about the restore point from the [**RESTOREPOINTINFOW**](/windows/win32/api/srrestoreptapi/ns-srrestoreptapi-restorepointinfoa) structure.</span></span>

<span data-ttu-id="fd92f-122">Каждая папка RP *n* может содержать файлы, используемые для наблюдения за изменениями точки восстановления.</span><span class="sxs-lookup"><span data-stu-id="fd92f-122">Each RP *n* folder may contain files used to track changes for a restore point.</span></span> <span data-ttu-id="fd92f-123">Первый файл называется Change. log, следующий файл называется Changed. log. 1 и т. д.</span><span class="sxs-lookup"><span data-stu-id="fd92f-123">The first file is named change.log, the next file is named change.log.1, and so on.</span></span> <span data-ttu-id="fd92f-124">Каждый файл журнала изменений содержит следующие структуры:</span><span class="sxs-lookup"><span data-stu-id="fd92f-124">Each change log file contains the following structures:</span></span>

-   [<span data-ttu-id="fd92f-125">**\_заголовок журнала \_ изменений**</span><span class="sxs-lookup"><span data-stu-id="fd92f-125">**CHANGE\_LOG\_HEADER**</span></span>](change-log-header.md)
-   <span data-ttu-id="fd92f-126">[**Изменить \_ \_Запись журнала**](change-log-entry.md)1</span><span class="sxs-lookup"><span data-stu-id="fd92f-126">[**CHANGE\_LOG\_ENTRY**](change-log-entry.md)1</span></span>
-   <span data-ttu-id="fd92f-127">[**Изменить \_ \_Запись журнала**](change-log-entry.md)2</span><span class="sxs-lookup"><span data-stu-id="fd92f-127">[**CHANGE\_LOG\_ENTRY**](change-log-entry.md)2</span></span>
-   <span data-ttu-id="fd92f-128">...</span><span class="sxs-lookup"><span data-stu-id="fd92f-128">...</span></span>
-   <span data-ttu-id="fd92f-129">[**Изменить \_ \_Запись журнала**](change-log-entry.md)*n*</span><span class="sxs-lookup"><span data-stu-id="fd92f-129">[**CHANGE\_LOG\_ENTRY**](change-log-entry.md)*n*</span></span>

## <a name="related-topics"></a><span data-ttu-id="fd92f-130">См. также</span><span class="sxs-lookup"><span data-stu-id="fd92f-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fd92f-131">Устаревшие структуры восстановления системы</span><span class="sxs-lookup"><span data-stu-id="fd92f-131">Legacy System Restore Structures</span></span>](legacy-system-restore-structures.md)
</dt> </dl>

 

 




