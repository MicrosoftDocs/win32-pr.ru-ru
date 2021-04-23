---
description: Дополнительные сведения о параметрах расширенной подсистемы хранилища.
title: Параметры расширяемой системы подсистемы хранилища
TOCTitle: Extensible Storage Engine System Parameters
ms:assetid: f95c2e87-b25e-4be5-8c17-8486ba37dad4
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294139(v=EXCHG.10)
ms:contentKeyID: 32765753
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 43473f1bf5f599ba8efd06bd31345485acc07061
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544010"
---
# <a name="extensible-storage-engine-system-parameters"></a><span data-ttu-id="cf73e-103">Параметры расширяемой системы подсистемы хранилища</span><span class="sxs-lookup"><span data-stu-id="cf73e-103">Extensible Storage Engine System Parameters</span></span>


<span data-ttu-id="cf73e-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="cf73e-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="extensible-storage-engine-system-parameters"></a><span data-ttu-id="cf73e-105">Параметры расширяемой системы подсистемы хранилища</span><span class="sxs-lookup"><span data-stu-id="cf73e-105">Extensible Storage Engine System Parameters</span></span>

<span data-ttu-id="cf73e-106">Следующие константы используются в качестве значений для параметра *парамид* функций [жетжетсистемпараметер](./jetgetsystemparameter-function.md) и [жетсетсистемпараметер](./jetsetsystemparameter-function.md) .</span><span class="sxs-lookup"><span data-stu-id="cf73e-106">The following constants are used as values for the *paramid* parameter of the [JetGetSystemParameter](./jetgetsystemparameter-function.md) and [JetSetSystemParameter](./jetsetsystemparameter-function.md) functions.</span></span>

  - [<span data-ttu-id="cf73e-107">Параметры резервного копирования и восстановления</span><span class="sxs-lookup"><span data-stu-id="cf73e-107">Backup and Restore Parameters</span></span>](./backup-and-restore-parameters.md)

  - [<span data-ttu-id="cf73e-108">Параметры обратного вызова</span><span class="sxs-lookup"><span data-stu-id="cf73e-108">Callback Parameters</span></span>](./callback-parameters.md)

  - [<span data-ttu-id="cf73e-109">Параметры базы данных</span><span class="sxs-lookup"><span data-stu-id="cf73e-109">Database Parameters</span></span>](./database-parameters.md)

  - [<span data-ttu-id="cf73e-110">Параметры кэша базы данных</span><span class="sxs-lookup"><span data-stu-id="cf73e-110">Database Cache Parameters</span></span>](./database-cache-parameters.md)

  - [<span data-ttu-id="cf73e-111">Параметры обработки ошибок</span><span class="sxs-lookup"><span data-stu-id="cf73e-111">Error Handling Parameters</span></span>](./error-handling-parameters.md)

  - [<span data-ttu-id="cf73e-112">Параметры журнала событий</span><span class="sxs-lookup"><span data-stu-id="cf73e-112">Event Log Parameters</span></span>](./event-log-parameters.md)

  - [<span data-ttu-id="cf73e-113">Параметры ввода-вывода</span><span class="sxs-lookup"><span data-stu-id="cf73e-113">I/O Parameters</span></span>](./i-o-parameters.md)

  - [<span data-ttu-id="cf73e-114">Параметры индекса</span><span class="sxs-lookup"><span data-stu-id="cf73e-114">Index Parameters</span></span>](./index-parameters.md)

  - [<span data-ttu-id="cf73e-115">Информационные параметры</span><span class="sxs-lookup"><span data-stu-id="cf73e-115">Informational Parameters</span></span>](./informational-parameters.md)

  - [<span data-ttu-id="cf73e-116">Параметры Meta</span><span class="sxs-lookup"><span data-stu-id="cf73e-116">Meta Parameters</span></span>](./meta-parameters.md)

  - [<span data-ttu-id="cf73e-117">Параметры ресурсов</span><span class="sxs-lookup"><span data-stu-id="cf73e-117">Resource Parameters</span></span>](./resource-parameters.md)

  - [<span data-ttu-id="cf73e-118">Параметры временной базы данных</span><span class="sxs-lookup"><span data-stu-id="cf73e-118">Temporary Database Parameters</span></span>](./temporary-database-parameters.md)

  - [<span data-ttu-id="cf73e-119">Параметры журнала транзакций</span><span class="sxs-lookup"><span data-stu-id="cf73e-119">Transaction Log Parameters</span></span>](./transaction-log-parameters.md)

### <a name="system-parameter-description-format"></a><span data-ttu-id="cf73e-120">Формат описания параметров системы</span><span class="sxs-lookup"><span data-stu-id="cf73e-120">System Parameter Description Format</span></span>

<span data-ttu-id="cf73e-121">Каждый системный параметр будет описан в следующем формате:</span><span class="sxs-lookup"><span data-stu-id="cf73e-121">Each system parameter will be described using the following format:</span></span>

<span data-ttu-id="cf73e-122">JET_paramX</span><span class="sxs-lookup"><span data-stu-id="cf73e-122">JET_paramX</span></span>

<span data-ttu-id="cf73e-123">Описание системного параметра JET_paramX.</span><span class="sxs-lookup"><span data-stu-id="cf73e-123">Description of the JET_paramX system parameter.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cf73e-124">Значение по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="cf73e-124">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="cf73e-125">Значение параметра по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="cf73e-125">The default value of the parameter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf73e-126">Тип:</span><span class="sxs-lookup"><span data-stu-id="cf73e-126">Type:</span></span></p></td>
<td><p><span data-ttu-id="cf73e-127">Тип данных параметра.</span><span class="sxs-lookup"><span data-stu-id="cf73e-127">The data type of the parameter.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf73e-128">Допустимый диапазон:</span><span class="sxs-lookup"><span data-stu-id="cf73e-128">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="cf73e-129">Допустимые значения для параметра.</span><span class="sxs-lookup"><span data-stu-id="cf73e-129">The legal values for the parameter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf73e-130">Область.</span><span class="sxs-lookup"><span data-stu-id="cf73e-130">Scope:</span></span></p></td>
<td><p><span data-ttu-id="cf73e-131">Является ли параметр глобальным или для каждого экземпляра?</span><span class="sxs-lookup"><span data-stu-id="cf73e-131">Is the parameter Global or per Instance?</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf73e-132">Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</span><span class="sxs-lookup"><span data-stu-id="cf73e-132">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="cf73e-133">Можно ли задать параметр, если существуют какие бы то ни было экземпляры?</span><span class="sxs-lookup"><span data-stu-id="cf73e-133">Can the parameter be set if any instances exist?</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf73e-134">Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</span><span class="sxs-lookup"><span data-stu-id="cf73e-134">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="cf73e-135">Можно ли задать параметр при инициализации?</span><span class="sxs-lookup"><span data-stu-id="cf73e-135">Can the parameter be set when initialized?</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf73e-136">Влияет на физический макет:</span><span class="sxs-lookup"><span data-stu-id="cf73e-136">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="cf73e-137">Влияет ли параметр на файлы на диске?</span><span class="sxs-lookup"><span data-stu-id="cf73e-137">Does the parameter affect the files on disk?</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf73e-138">Влияет на надежность:</span><span class="sxs-lookup"><span data-stu-id="cf73e-138">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="cf73e-139">Влияет ли параметр на надежность ядра?</span><span class="sxs-lookup"><span data-stu-id="cf73e-139">Does the parameter affect engine reliability?</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf73e-140">Влияет на производительность:</span><span class="sxs-lookup"><span data-stu-id="cf73e-140">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="cf73e-141">Влияет ли параметр на производительность ядра?</span><span class="sxs-lookup"><span data-stu-id="cf73e-141">Does the parameter affect engine performance?</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf73e-142">Влияет на ресурсы:</span><span class="sxs-lookup"><span data-stu-id="cf73e-142">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="cf73e-143">Влияет ли параметр на ресурсы ядра?</span><span class="sxs-lookup"><span data-stu-id="cf73e-143">Does the parameter affect engine resources?</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf73e-144">"Доступность":</span><span class="sxs-lookup"><span data-stu-id="cf73e-144">Availability:</span></span></p></td>
<td><p><span data-ttu-id="cf73e-145">Выпуски Windows, которые поддерживают параметр.</span><span class="sxs-lookup"><span data-stu-id="cf73e-145">Releases of Windows that support the parameter.</span></span></p></td>
</tr>
</tbody>
</table>
