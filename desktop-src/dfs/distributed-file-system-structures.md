---
description: Ниже приведены распределенная файловая система структуры DFS.
ms.assetid: f55ad3c0-0457-4d5a-a7d3-8eff744d573d
title: Структуры распределенная файловая система
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42fc3351402c4721952cbfc4dc3fe3c6ac6d3a76
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496581"
---
# <a name="distributed-file-system-structures"></a><span data-ttu-id="fb5ab-103">Структуры распределенная файловая система</span><span class="sxs-lookup"><span data-stu-id="fb5ab-103">Distributed File System Structures</span></span>

<span data-ttu-id="fb5ab-104">Ниже перечислены структуры распределенная файловая система (DFS).</span><span class="sxs-lookup"><span data-stu-id="fb5ab-104">The following are the Distributed File System (DFS) structures:</span></span>

## <a name="in-this-section"></a><span data-ttu-id="fb5ab-105">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="fb5ab-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="fb5ab-106">**DFS_GET_PKT_ENTRY_STATE_ARG**</span><span class="sxs-lookup"><span data-stu-id="fb5ab-106">**DFS_GET_PKT_ENTRY_STATE_ARG**</span></span>](/windows/win32/api/lmdfs/ns-lmdfs-dfs_get_pkt_entry_state_arg)
</dt> <dd>

<span data-ttu-id="fb5ab-107">Входной буфер, используемый с кодом элемента управления [**FSCTL_DFS_GET_PKT_ENTRY_STATE**](fsctl-dfs-get-pkt-entry-state.md)</span><span class="sxs-lookup"><span data-stu-id="fb5ab-107">Input buffer used with the [**FSCTL_DFS_GET_PKT_ENTRY_STATE**](fsctl-dfs-get-pkt-entry-state.md) control code</span></span>
</dd> <dt>

[<span data-ttu-id="fb5ab-108">Структура _DFS_INFO_1</span><span class="sxs-lookup"><span data-stu-id="fb5ab-108">_DFS_INFO_1 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_1)
</dt> <dd>
<span data-ttu-id="fb5ab-109">Содержит имя корня или ссылки распределенная файловая система (DFS).</span><span class="sxs-lookup"><span data-stu-id="fb5ab-109">Contains the name of a Distributed File System (DFS) root or link.</span></span>

</dd> <dt>

[<span data-ttu-id="fb5ab-110">Структура _DFS_INFO_2</span><span class="sxs-lookup"><span data-stu-id="fb5ab-110">_DFS_INFO_2 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_2)
</dt> <dd>
<span data-ttu-id="fb5ab-111">Содержит сведения о корне или ссылке распределенная файловая система (DFS).</span><span class="sxs-lookup"><span data-stu-id="fb5ab-111">Contains information about a Distributed File System (DFS) root or link.</span></span> <span data-ttu-id="fb5ab-112">Эта структура содержит имя, состояние и число целевых объектов DFS для корня или ссылки.</span><span class="sxs-lookup"><span data-stu-id="fb5ab-112">This structure contains the name, status, and number of DFS targets for the root or link.</span></span>

</dd> <dt>

[<span data-ttu-id="fb5ab-113">Структура _DFS_INFO_3</span><span class="sxs-lookup"><span data-stu-id="fb5ab-113">_DFS_INFO_3 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_3)
</dt> <dd>
<span data-ttu-id="fb5ab-114">Содержит сведения о корне или ссылке распределенная файловая система (DFS).</span><span class="sxs-lookup"><span data-stu-id="fb5ab-114">Contains information about a Distributed File System (DFS) root or link.</span></span> <span data-ttu-id="fb5ab-115">Эта структура содержит имя, состояние, количество целевых объектов DFS и сведения о каждом целевом объекте корня или ссылки.</span><span class="sxs-lookup"><span data-stu-id="fb5ab-115">This structure contains the name, status, number of DFS targets, and information about each target of the root or link.</span></span>

</dd> <dt>

[<span data-ttu-id="fb5ab-116">Структура _DFS_INFO_4</span><span class="sxs-lookup"><span data-stu-id="fb5ab-116">_DFS_INFO_4 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_4)
</dt> <dd>
<span data-ttu-id="fb5ab-117">Содержит сведения о корне или ссылке распределенная файловая система (DFS).</span><span class="sxs-lookup"><span data-stu-id="fb5ab-117">Contains information about a Distributed File System (DFS) root or link.</span></span> <span data-ttu-id="fb5ab-118">Эта структура содержит имя, состояние, **GUID**, время ожидания, количество целевых объектов и сведения о каждом целевом объекте корня или ссылки.</span><span class="sxs-lookup"><span data-stu-id="fb5ab-118">This structure contains the name, status, **GUID**, time-out, number of targets, and information about each target of the root or link.</span></span>

</dd> <dt>

[<span data-ttu-id="fb5ab-119">Структура _DFS_INFO_5</span><span class="sxs-lookup"><span data-stu-id="fb5ab-119">_DFS_INFO_5 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_5)
</dt> <dd>
<span data-ttu-id="fb5ab-120">Содержит сведения о корне или ссылке распределенная файловая система (DFS).</span><span class="sxs-lookup"><span data-stu-id="fb5ab-120">Contains information about a Distributed File System (DFS) root or link.</span></span> <span data-ttu-id="fb5ab-121">Эта структура содержит имя, состояние, **GUID**, время ожидания, пространство имен, свойства корня или ссылки, размер метаданных и число целевых объектов для корня или ссылки.</span><span class="sxs-lookup"><span data-stu-id="fb5ab-121">This structure contains the name, status, **GUID**, time-out, namespace/root/link properties, metadata size, and number of targets for the root or link.</span></span>

</dd> <dt>

[<span data-ttu-id="fb5ab-122">Структура _DFS_INFO_6</span><span class="sxs-lookup"><span data-stu-id="fb5ab-122">_DFS_INFO_6 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_6)
</dt> <dd>
<span data-ttu-id="fb5ab-123">Содержит сведения о корне или ссылке распределенная файловая система (DFS).</span><span class="sxs-lookup"><span data-stu-id="fb5ab-123">Contains information about a Distributed File System (DFS) root or link.</span></span> <span data-ttu-id="fb5ab-124">Эта структура содержит имя, состояние, **GUID**, время ожидания, пространство имен, свойства корня или ссылки, размер метаданных, число целевых объектов и сведения о каждом целевом объекте корня или ссылки.</span><span class="sxs-lookup"><span data-stu-id="fb5ab-124">This structure contains the name, status, **GUID**, time-out, namespace/root/link properties, metadata size, number of targets, and information about each target of the root or link.</span></span>

</dd> <dt>

[<span data-ttu-id="fb5ab-125">Структура _DFS_INFO_7</span><span class="sxs-lookup"><span data-stu-id="fb5ab-125">_DFS_INFO_7 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_7)
</dt> <dd>
<span data-ttu-id="fb5ab-126">Содержит сведения о пространстве имен DFS.</span><span class="sxs-lookup"><span data-stu-id="fb5ab-126">Contains information about a DFS namespace.</span></span> <span data-ttu-id="fb5ab-127">Эта структура содержит **идентификатор GUID** версии для метаданных пространства имен.</span><span class="sxs-lookup"><span data-stu-id="fb5ab-127">This structure contains the version **GUID** for the metadata for the namespace.</span></span>

</dd> <dt>

[<span data-ttu-id="fb5ab-128">Структура _DFS_INFO_8</span><span class="sxs-lookup"><span data-stu-id="fb5ab-128">_DFS_INFO_8 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_8)
</dt> <dd>
<span data-ttu-id="fb5ab-129">Содержит имя, состояние, **GUID**, время ожидания, флаги свойств, размер метаданных, сведения о целевом объекте DFS и дескриптор безопасности точки повторного анализа ссылок для корня или ссылки.</span><span class="sxs-lookup"><span data-stu-id="fb5ab-129">Contains the name, status, **GUID**, time-out, property flags, metadata size, DFS target information, and link reparse point security descriptor for a root or link.</span></span>

</dd> <dt>

[<span data-ttu-id="fb5ab-130">Структура _DFS_INFO_9</span><span class="sxs-lookup"><span data-stu-id="fb5ab-130">_DFS_INFO_9 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_9)
</dt> <dd>
<span data-ttu-id="fb5ab-131">Содержит имя, состояние, **GUID**, время ожидания, флаги свойств, размер метаданных, сведения о целевом объекте DFS, дескриптор безопасности точки повторного анализа канала и список целевых объектов DFS для корня или ссылки.</span><span class="sxs-lookup"><span data-stu-id="fb5ab-131">Contains the name, status, **GUID**, time-out, property flags, metadata size, DFS target information, link reparse point security descriptor, and a list of DFS targets for a root or link.</span></span>

</dd> <dt>

[<span data-ttu-id="fb5ab-132">Структура _DFS_INFO_50</span><span class="sxs-lookup"><span data-stu-id="fb5ab-132">_DFS_INFO_50 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_50)
</dt> <dd>
<span data-ttu-id="fb5ab-133">Содержит версию метаданных DFS и возможности существующего пространства имен DFS.</span><span class="sxs-lookup"><span data-stu-id="fb5ab-133">Contains the DFS metadata version and capabilities of an existing DFS namespace.</span></span>

</dd> <dt>

[<span data-ttu-id="fb5ab-134">Структура _DFS_INFO_100</span><span class="sxs-lookup"><span data-stu-id="fb5ab-134">_DFS_INFO_100 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_100)
</dt> <dd>
<span data-ttu-id="fb5ab-135">Содержит комментарий, связанный с корнем или ссылкой распределенная файловая система (DFS).</span><span class="sxs-lookup"><span data-stu-id="fb5ab-135">Contains a comment associated with a Distributed File System (DFS) root or link.</span></span>

</dd> <dt>

[<span data-ttu-id="fb5ab-136">Структура _DFS_INFO_101</span><span class="sxs-lookup"><span data-stu-id="fb5ab-136">_DFS_INFO_101 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_101)
</dt> <dd>
<span data-ttu-id="fb5ab-137">Описывает состояние хранилища в корне DFS, ссылке, корневом целевом объекте или целевом объекте ссылки.</span><span class="sxs-lookup"><span data-stu-id="fb5ab-137">Describes the state of storage on a DFS root, link, root target, or link target.</span></span>

</dd> <dt>

[<span data-ttu-id="fb5ab-138">Структура _DFS_INFO_102</span><span class="sxs-lookup"><span data-stu-id="fb5ab-138">_DFS_INFO_102 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_102)
</dt> <dd>
<span data-ttu-id="fb5ab-139">Содержит значение времени ожидания для связи с корнем распределенная файловая система (DFS) или ссылкой в именованном корне DFS.</span><span class="sxs-lookup"><span data-stu-id="fb5ab-139">Contains a time-out value to associate with a Distributed File System (DFS) root or a link in a named DFS root.</span></span>

</dd> <dt>

[<span data-ttu-id="fb5ab-140">Структура _DFS_INFO_103</span><span class="sxs-lookup"><span data-stu-id="fb5ab-140">_DFS_INFO_103 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_103)
</dt> <dd>
<span data-ttu-id="fb5ab-141">Содержит свойства, задают определенные поведения для корня или ссылки DFS.</span><span class="sxs-lookup"><span data-stu-id="fb5ab-141">Contains properties that set specific behaviors for a DFS root or link.</span></span>

</dd> <dt>

[<span data-ttu-id="fb5ab-142">Структура _DFS_INFO_104</span><span class="sxs-lookup"><span data-stu-id="fb5ab-142">_DFS_INFO_104 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_104)
</dt> <dd>
<span data-ttu-id="fb5ab-143">Содержит приоритет корневого целевого объекта DFS или ссылки.</span><span class="sxs-lookup"><span data-stu-id="fb5ab-143">Contains the priority of a DFS root target or link target.</span></span>

</dd> <dt>

[<span data-ttu-id="fb5ab-144">Структура _DFS_INFO_105</span><span class="sxs-lookup"><span data-stu-id="fb5ab-144">_DFS_INFO_105 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_105)
</dt> <dd>
<span data-ttu-id="fb5ab-145">Содержит сведения об корне или ссылке DFS, включая комментарии, состояние, время ожидания и поведение DFS, заданные флагами свойств.</span><span class="sxs-lookup"><span data-stu-id="fb5ab-145">Contains information about a DFS root or link, including comment, state, time-out, and DFS behaviors specified by property flags.</span></span>

</dd> <dt>

[<span data-ttu-id="fb5ab-146">Структура _DFS_INFO_106</span><span class="sxs-lookup"><span data-stu-id="fb5ab-146">_DFS_INFO_106 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_106)
</dt> <dd>
<span data-ttu-id="fb5ab-147">Содержит состояние хранилища и приоритет для корня DFS или целевого объекта ссылки.</span><span class="sxs-lookup"><span data-stu-id="fb5ab-147">Contains the storage state and priority for a DFS root target or link target.</span></span> <span data-ttu-id="fb5ab-148">Эта структура предназначена только для использования с функцией [**нетдфссетинфо**](netdfssetinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="fb5ab-148">This structure is only for use with the [**NetDfsSetInfo**](netdfssetinfo.md) function.</span></span>

</dd> <dt>

[<span data-ttu-id="fb5ab-149">Структура _DFS_INFO_107</span><span class="sxs-lookup"><span data-stu-id="fb5ab-149">_DFS_INFO_107 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_107)
</dt> <dd>
<span data-ttu-id="fb5ab-150">Содержит сведения об корне или ссылке DFS, включая комментарий, состояние, время ожидания, флаги свойств и дескриптор безопасности точки повторного анализа ссылок.</span><span class="sxs-lookup"><span data-stu-id="fb5ab-150">Contains information about a DFS root or link, including the comment, state, time-out, property flags, and link reparse point security descriptor.</span></span>

</dd> <dt>

[<span data-ttu-id="fb5ab-151">Структура _DFS_INFO_150</span><span class="sxs-lookup"><span data-stu-id="fb5ab-151">_DFS_INFO_150 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_150)
</dt> <dd>
<span data-ttu-id="fb5ab-152">Содержит дескриптор безопасности для точки повторного анализа ссылки DFS.</span><span class="sxs-lookup"><span data-stu-id="fb5ab-152">Contains the security descriptor for a DFS link's reparse point.</span></span>

</dd> <dt>

[<span data-ttu-id="fb5ab-153">Структура _DFS_INFO_200</span><span class="sxs-lookup"><span data-stu-id="fb5ab-153">_DFS_INFO_200 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_200)
</dt> <dd>
<span data-ttu-id="fb5ab-154">Содержит имя пространства имен распределенная файловая система на основе домена (DFS).</span><span class="sxs-lookup"><span data-stu-id="fb5ab-154">Contains the name of a domain-based Distributed File System (DFS) namespace.</span></span>

</dd> <dt>

[<span data-ttu-id="fb5ab-155">Структура _DFS_INFO_300</span><span class="sxs-lookup"><span data-stu-id="fb5ab-155">_DFS_INFO_300 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_300)
</dt> <dd>
<span data-ttu-id="fb5ab-156">Содержит имя и тип (на основе домена или автономной версии) пространства имен DFS.</span><span class="sxs-lookup"><span data-stu-id="fb5ab-156">Contains the name and type (domain-based or stand-alone) of a DFS namespace.</span></span>

</dd> <dt>

[<span data-ttu-id="fb5ab-157">Структура _DFS_STORAGE_INFO</span><span class="sxs-lookup"><span data-stu-id="fb5ab-157">_DFS_STORAGE_INFO structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_storage_info)
</dt> <dd>
<span data-ttu-id="fb5ab-158">Содержит сведения о корне или ссылке DFS в пространстве имен DFS или в кэше, поддерживаемом клиентом DFS.</span><span class="sxs-lookup"><span data-stu-id="fb5ab-158">Contains information about a DFS root or link target in a DFS namespace or from the cache maintained by the DFS client.</span></span>

</dd> <dt>

[<span data-ttu-id="fb5ab-159">Структура _DFS_STORAGE_INFO_1</span><span class="sxs-lookup"><span data-stu-id="fb5ab-159">_DFS_STORAGE_INFO_1 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_storage_info_1)
</dt> <dd>
<span data-ttu-id="fb5ab-160">Содержит сведения о целевом объекте DFS, включая имя целевого сервера DFS и имя общего ресурса, а также состояние и приоритет целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="fb5ab-160">Contains information about a DFS target, including the DFS target server name and share name as well as the target's state and priority.</span></span>

</dd> <dt>

[<span data-ttu-id="fb5ab-161">Структура _DFS_SUPPORTED_NAMESPACE_VERSION_INFO</span><span class="sxs-lookup"><span data-stu-id="fb5ab-161">_DFS_SUPPORTED_NAMESPACE_VERSION_INFO structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_supported_namespace_version_info)
</dt> <dd>
<span data-ttu-id="fb5ab-162">Содержит сведения о версии для пространства имен DFS.</span><span class="sxs-lookup"><span data-stu-id="fb5ab-162">Contains version information for a DFS namespace.</span></span>

</dd> <dt>

[<span data-ttu-id="fb5ab-163">Структура _DFS_TARGET_PRIORITY</span><span class="sxs-lookup"><span data-stu-id="fb5ab-163">_DFS_TARGET_PRIORITY structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_target_priority)
</dt> <dd>
<span data-ttu-id="fb5ab-164">Содержит класс приоритета и ранг определенного целевого объекта DFS.</span><span class="sxs-lookup"><span data-stu-id="fb5ab-164">Contains the priority class and rank of a specific DFS target.</span></span>

</dd> </dl>
