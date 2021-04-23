---
description: При обработке резервной копии в VSS, инициаторы и модули записи работают вместе для создания стабильного образа системы, из которого осуществляется резервное копирование данных, что требует координации и создания теневой копии текущей системы.
ms.assetid: 1cefb6ac-f2bb-464b-a62f-05be91ae56f7
title: Общие сведения об обработке восстановления в VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c0279888b28af82eb1b4b51093b421b9db5e15d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692892"
---
# <a name="overview-of-processing-a-restore-under-vss"></a><span data-ttu-id="d2fd6-103">Общие сведения об обработке восстановления в VSS</span><span class="sxs-lookup"><span data-stu-id="d2fd6-103">Overview of Processing a Restore Under VSS</span></span>

<span data-ttu-id="d2fd6-104">При обработке резервной копии в VSS, инициаторы и модули записи работают вместе для создания стабильного образа системы, из которого осуществляется резервное копирование данных, что требует координации и создания теневой копии текущей системы.</span><span class="sxs-lookup"><span data-stu-id="d2fd6-104">In processing a backup under VSS, requesters and writers worked together to produce a stable system image from which to back up data, which required coordination and the creation of a shadow copy of the current system.</span></span>

<span data-ttu-id="d2fd6-105">В отличие от резервной копии VSS, где целью координации запросов и модулей записи является создание стабильного образа системы, из которого копируются данные, цель восстановления на основе VSS заключается в возврате файлов на диск наиболее удобным для приложений (модулей записи), выполняющихся в системе.</span><span class="sxs-lookup"><span data-stu-id="d2fd6-105">In contrast to a VSS backup, where the purpose of requester and writers coordination is to produce a stable system image from which to copy data, the objective of a VSS-based restore is to return files to disk in a manner most useful to applications (writers) currently running on the system.</span></span> <span data-ttu-id="d2fd6-106">Это не требует стабильного образа системы, поэтому теневая копия не требуется.</span><span class="sxs-lookup"><span data-stu-id="d2fd6-106">This does not require a stable system image, so no shadow copy is necessary.</span></span>

<span data-ttu-id="d2fd6-107">Вместо этого Обратите внимание на предотвращение сбоев операций записи, предотвращение создания непоследовательных наборов данных на диске и предоставление средствам записи необходимой области для вычисления и слияния данных при необходимости.</span><span class="sxs-lookup"><span data-stu-id="d2fd6-107">Instead, attention is focused on avoiding disruption of writer activity, preventing the creation of inconsistent data sets on disk, and allowing writers the necessary scope to evaluate and merge data when necessary.</span></span>

<span data-ttu-id="d2fd6-108">Как и в случае с операцией резервного копирования, для восстановления VSS требуется доступ к документу с резервным копированием и документации по метаданным.</span><span class="sxs-lookup"><span data-stu-id="d2fd6-108">Like a backup operation, a VSS restore requires access to both a Backup Components Document and to Writer Metadata Documents.</span></span> <span data-ttu-id="d2fd6-109">Эти документы обычно не получаются с помощью запросов к выполняемым приложениям, а извлекаются из версий, хранящихся в виде XML-документов на носителе резервных копий.</span><span class="sxs-lookup"><span data-stu-id="d2fd6-109">These documents are not generally obtained by querying running applications, but instead are retrieved from versions stored as XML documents on backup media.</span></span>

<span data-ttu-id="d2fd6-110">Как и во время операций резервного копирования, документы метаданных модуля записи остаются объектами только для чтения и (после извлечения) документ компонентов резервного копирования все еще можно изменить.</span><span class="sxs-lookup"><span data-stu-id="d2fd6-110">As is the case during backup operations, the Writer Metadata Documents remain read-only objects, and (once retrieved) the Backup Components Document can still be modified.</span></span> <span data-ttu-id="d2fd6-111">Изменения в документе позволяют модулям записи и инициатору запроса обмениваться информацией о следующих компонентах:</span><span class="sxs-lookup"><span data-stu-id="d2fd6-111">Modifications of the Backup Components Document allow writers and requester to communicate about the following:</span></span>

-   <span data-ttu-id="d2fd6-112">Переопределение [*методов Restore*](vssgloss-r.md) с помощью [*целевых объектов восстановления*](vssgloss-r.md)</span><span class="sxs-lookup"><span data-stu-id="d2fd6-112">Overriding [*restore methods*](vssgloss-r.md) with [*restore targets*](vssgloss-r.md)</span></span>
-   <span data-ttu-id="d2fd6-113">Использование [ *сопоставлений альтернативного расположения*](vssgloss-a.md)</span><span class="sxs-lookup"><span data-stu-id="d2fd6-113">Using [*alternate location mappings*](vssgloss-a.md)</span></span>
-   <span data-ttu-id="d2fd6-114">Восстановление файлов в новые расположения на диске</span><span class="sxs-lookup"><span data-stu-id="d2fd6-114">Restoring files to new locations on disk</span></span>
-   <span data-ttu-id="d2fd6-115">Использование различных правил выбора из тех, которые использовались во время резервного копирования</span><span class="sxs-lookup"><span data-stu-id="d2fd6-115">Using different selection rules from those used during backup</span></span>

<span data-ttu-id="d2fd6-116">Чтобы лучше понять основные задачи, связанные с восстановлением, полезно разбить этот обзор на следующие разделы:</span><span class="sxs-lookup"><span data-stu-id="d2fd6-116">To more fully understand the basic tasks involved in performing a restore, it is useful to break down this overview into the following topics:</span></span>

-   [<span data-ttu-id="d2fd6-117">Общие сведения об инициализации восстановления</span><span class="sxs-lookup"><span data-stu-id="d2fd6-117">Overview of Restore Initialization</span></span>](overview-of-restore-initialization.md)
-   [<span data-ttu-id="d2fd6-118">Общие сведения о подготовке к восстановлению</span><span class="sxs-lookup"><span data-stu-id="d2fd6-118">Overview of Preparing for Restore</span></span>](overview-of-preparing-for-restore.md)
-   [<span data-ttu-id="d2fd6-119">Общие сведения о фактическом восстановлении файлов</span><span class="sxs-lookup"><span data-stu-id="d2fd6-119">Overview of Actual File Restoration</span></span>](overview-of-actual-file-restoration.md)
-   [<span data-ttu-id="d2fd6-120">Общие сведения о сбросе и завершении восстановления</span><span class="sxs-lookup"><span data-stu-id="d2fd6-120">Overview of Restore Clean up and Termination</span></span>](overview-of-restore-clean-up-and-termination.md)

 

 



