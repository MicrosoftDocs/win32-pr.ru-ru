---
description: Модули записи могут точно настраивать производительность различных типов резервных копий на уровне набора файлов, указывая тип резервной копии спецификация файла, который определяется битовой маской или побитовой или членом \_ \_ \_ перечисления типа резервной копии спецификации файла VSS \_ .
ms.assetid: a3ac69b4-894a-4536-8fab-f45ad7e5118a
title: Поддержка схемы на уровне файлов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 460d256a3eaa016933e697687d05e26838c14ae2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999495"
---
# <a name="file-level-schema-support"></a><span data-ttu-id="95f39-103">Поддержка схемы на уровне файлов</span><span class="sxs-lookup"><span data-stu-id="95f39-103">File Level Schema Support</span></span>

<span data-ttu-id="95f39-104">Модули записи могут точно настраивать производительность различных типов резервных копий на уровне [*набора файлов*](vssgloss-f.md) , указывая тип резервной копии спецификация файла, который определяется битовой маской или побитовой или членом перечисления [**\_ \_ \_ \_ типа резервной копии спецификации файла VSS**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type) .</span><span class="sxs-lookup"><span data-stu-id="95f39-104">Writers can fine-tune the performance of various types of backup at the [*file set*](vssgloss-f.md) level by indicating through a file specification backup type, indicated by a bit mask or bitwise OR of the members of the [**VSS\_FILE\_SPEC\_BACKUP\_TYPE**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type) enumeration.</span></span>

<span data-ttu-id="95f39-105">Для указанных типов резервного копирования модуль записи сообщает следующее:</span><span class="sxs-lookup"><span data-stu-id="95f39-105">For specified types of backup, the writer indicates the following:</span></span>

-   <span data-ttu-id="95f39-106">Требуется ли теневая копия тома для правильной резервного копирования набора файлов.</span><span class="sxs-lookup"><span data-stu-id="95f39-106">Whether it will be necessary to shadow copy the volume to properly back up a file set.</span></span> <span data-ttu-id="95f39-107">Например, если файлы в наборе файлов не открыты средством записи в монопольном режиме и они могут обеспечить стабильность, теневая копия не требуется.</span><span class="sxs-lookup"><span data-stu-id="95f39-107">For instance, if the files in a file set are not exclusively opened by the writer and it can ensure that it is stable, a shadow copy is not needed.</span></span>
-   <span data-ttu-id="95f39-108">Должна ли запрашивающая сторона выполнять резервное копирование таким образом, что, независимо от времени последнего изменения или других проблем, версия файлов набора файлов, текущая при резервном копировании, будет восстановлена.</span><span class="sxs-lookup"><span data-stu-id="95f39-108">Whether the requester has to perform the backup in such a way that, regardless of last modification time or other issues, the version of the file set's files current at backup will be restored.</span></span> <span data-ttu-id="95f39-109">Как правило, это означает, что набор файлов копируется в составе резервной копии.</span><span class="sxs-lookup"><span data-stu-id="95f39-109">Typically, this means that the file set is copied as part of the backup.</span></span>

<span data-ttu-id="95f39-110">Значения параметра [**\_ \_ Backup File Spec \_ \_ Type**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type) , указывающие на требование теневого копирования:</span><span class="sxs-lookup"><span data-stu-id="95f39-110">The values of [**VSS\_FILE\_SPEC\_BACKUP\_TYPE**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type) that indicate shadow copy requirement are:</span></span>

-   <span data-ttu-id="95f39-111">\_ \_ \_ требуется моментальный снимок фсбт для VSS \_</span><span class="sxs-lookup"><span data-stu-id="95f39-111">VSS\_FSBT\_ALL\_SNAPSHOT\_REQUIRED</span></span>
-   <span data-ttu-id="95f39-112">\_ \_ \_ требуется полный моментальный снимок VSS фсбт \_</span><span class="sxs-lookup"><span data-stu-id="95f39-112">VSS\_FSBT\_FULL\_SNAPSHOT\_REQUIRED</span></span>
-   <span data-ttu-id="95f39-113">\_ \_ требуется разностный \_ моментальный снимок VSS фсбт \_</span><span class="sxs-lookup"><span data-stu-id="95f39-113">VSS\_FSBT\_DIFFERENTIAL\_SNAPSHOT\_REQUIRED</span></span>
-   <span data-ttu-id="95f39-114">\_ \_ требуется добавочный \_ моментальный снимок VSS фсбт \_</span><span class="sxs-lookup"><span data-stu-id="95f39-114">VSS\_FSBT\_INCREMENTAL\_SNAPSHOT\_REQUIRED</span></span>
-   <span data-ttu-id="95f39-115">\_ \_ \_ требуется моментальный снимок журнала фсбт для VSS \_</span><span class="sxs-lookup"><span data-stu-id="95f39-115">VSS\_FSBT\_LOG\_SNAPSHOT\_REQUIRED</span></span>

<span data-ttu-id="95f39-116">Значения [**\_ \_ \_ \_ типа резервного копирования спецификации файла VSS**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type) , указывающие на необходимость резервного копирования файла:</span><span class="sxs-lookup"><span data-stu-id="95f39-116">The values of [**VSS\_FILE\_SPEC\_BACKUP\_TYPE**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type) that indicate the requirement to back up a file are:</span></span>

-   <span data-ttu-id="95f39-117">\_ФСБТ VSS \_ \_ требуется вся резервная копия \_</span><span class="sxs-lookup"><span data-stu-id="95f39-117">VSS\_FSBT\_ALL\_BACKUP\_REQUIRED</span></span>
-   <span data-ttu-id="95f39-118">\_ \_ \_ требуется полная резервная копия VSS фсбт \_</span><span class="sxs-lookup"><span data-stu-id="95f39-118">VSS\_FSBT\_FULL\_BACKUP\_REQUIRED</span></span>
-   <span data-ttu-id="95f39-119">\_ \_ требуется разностное \_ резервное копирование VSS фсбт \_</span><span class="sxs-lookup"><span data-stu-id="95f39-119">VSS\_FSBT\_DIFFERENTIAL\_BACKUP\_REQUIRED</span></span>
-   <span data-ttu-id="95f39-120">\_ \_ требуется добавочное \_ резервное копирование VSS фсбт \_</span><span class="sxs-lookup"><span data-stu-id="95f39-120">VSS\_FSBT\_INCREMENTAL\_BACKUP\_REQUIRED</span></span>
-   <span data-ttu-id="95f39-121">\_ \_ \_ требуется резервная копия журнала фсбт для VSS \_</span><span class="sxs-lookup"><span data-stu-id="95f39-121">VSS\_FSBT\_LOG\_BACKUP\_REQUIRED</span></span>

<span data-ttu-id="95f39-122">По умолчанию наборы файлов помечаются как тип резервной копии фсбт для \_ \_ всех \_ резервных копий \_ , необходимых для \| VSS \_ \_ , фсбт все необходимые \_ моментальные снимки \_ , что означает, что теневая копия всегда необходима для обработки файлов набора файлов, а файлы должны быть скопированы во все типы резервных копий.</span><span class="sxs-lookup"><span data-stu-id="95f39-122">By default, file sets are tagged with a file specification backup type of VSS\_FSBT\_ALL\_BACKUP\_REQUIRED \| VSS\_FSBT\_ALL\_SNAPSHOT\_REQUIRED, meaning that a shadow copy is always required in handling the file set's files, and that the files should be copied in all types of backup.</span></span>

 

 



