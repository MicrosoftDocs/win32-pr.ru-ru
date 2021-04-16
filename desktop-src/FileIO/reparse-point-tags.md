---
description: Каждая точка повторного анализа имеет тег идентификатора, чтобы можно было эффективно различать различные типы точек повторного анализа без необходимости анализировать определяемые пользователем данные в точке повторного анализа.
ms.assetid: d02a2f50-d374-4149-bc04-49b7db052f62
title: Теги точек повторного анализа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a53b65034347e2a2c07afcd6c1f03e31f73cef7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664047"
---
# <a name="reparse-point-tags"></a><span data-ttu-id="79e8a-103">Теги точек повторного анализа</span><span class="sxs-lookup"><span data-stu-id="79e8a-103">Reparse Point Tags</span></span>

<span data-ttu-id="79e8a-104">Каждая точка повторного анализа имеет тег идентификатора, чтобы можно было эффективно различать различные типы точек повторного анализа без необходимости анализировать определяемые пользователем данные в точке повторного анализа.</span><span class="sxs-lookup"><span data-stu-id="79e8a-104">Each reparse point has an identifier tag so that you can efficiently differentiate between the different types of reparse points, without having to examine the user-defined data in the reparse point.</span></span> <span data-ttu-id="79e8a-105">Система использует набор предопределенных тегов и диапазон тегов, зарезервированных для Microsoft.</span><span class="sxs-lookup"><span data-stu-id="79e8a-105">The system uses a set of predefined tags and a range of tags reserved for Microsoft.</span></span> <span data-ttu-id="79e8a-106">При использовании любого из зарезервированных тегов при задании точки повторного анализа операция завершается ошибкой.</span><span class="sxs-lookup"><span data-stu-id="79e8a-106">If you use any of the reserved tags when setting a reparse point, the operation fails.</span></span> <span data-ttu-id="79e8a-107">Теги, не входящие в эти диапазоны, не зарезервированы и доступны для приложения.</span><span class="sxs-lookup"><span data-stu-id="79e8a-107">Tags not included in these ranges are not reserved and are available for your application.</span></span>

<span data-ttu-id="79e8a-108">При установке точки повторного анализа необходимо пометить данные, которые будут помещены в точку повторного анализа.</span><span class="sxs-lookup"><span data-stu-id="79e8a-108">When you set a reparse point, you must tag the data to be placed in the reparse point.</span></span> <span data-ttu-id="79e8a-109">После установки точки повторного анализа новая операция Set завершается ошибкой, если тег для новых данных не соответствует тегу для существующих данных.</span><span class="sxs-lookup"><span data-stu-id="79e8a-109">After the reparse point has been established, a new set operation fails if the tag for the new data does not match the tag for the existing data.</span></span> <span data-ttu-id="79e8a-110">Если теги совпадают, операция Set перезаписывает существующую точку повторного анализа.</span><span class="sxs-lookup"><span data-stu-id="79e8a-110">If the tags match, the set operation overwrites the existing reparse point.</span></span>

<span data-ttu-id="79e8a-111">Чтобы получить тег точки повторной обработки, используйте функцию [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea) .</span><span class="sxs-lookup"><span data-stu-id="79e8a-111">To retrieve the reparse point tag, use the [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea) function.</span></span> <span data-ttu-id="79e8a-112">Если элемент **двфилеаттрибутес** включает атрибут **\_ \_ \_ точки повторного анализа атрибута файла** , то элемент **dwReserved0** указывает точку повторного анализа.</span><span class="sxs-lookup"><span data-stu-id="79e8a-112">If the **dwFileAttributes** member includes the **FILE\_ATTRIBUTE\_REPARSE\_POINT** attribute, then the **dwReserved0** member specifies the reparse point.</span></span>

## <a name="tag-contents"></a><span data-ttu-id="79e8a-113">Содержимое тега</span><span class="sxs-lookup"><span data-stu-id="79e8a-113">Tag Contents</span></span>

<span data-ttu-id="79e8a-114">Теги повторного анализа хранятся в виде значений **типа DWORD** .</span><span class="sxs-lookup"><span data-stu-id="79e8a-114">Reparse tags are stored as **DWORD** values.</span></span> <span data-ttu-id="79e8a-115">Биты определяют определенные атрибуты, как показано на следующей схеме.</span><span class="sxs-lookup"><span data-stu-id="79e8a-115">The bits define certain attributes, as shown in the following diagram.</span></span>

``` syntax
   3 3 2 2 2 2 2 2 2 2 2 2 1 1 1 1 1 1 1 1 1 1
   1 0 9 8 7 6 5 4 3 2 1 0 9 8 7 6 5 4 3 2 1 0 9 8 7 6 5 4 3 2 1 0
  +-+-+-+-+-----------------------+-------------------------------+
  |M|R|N|R|     Reserved bits     |      Reparse tag value        |
  +-+-+-+-+-----------------------+-------------------------------+
```

<span data-ttu-id="79e8a-116">Младшие 16 бит определяют тип точки повторного анализа.</span><span class="sxs-lookup"><span data-stu-id="79e8a-116">The low 16 bits determine the kind of reparse point.</span></span> <span data-ttu-id="79e8a-117">Старшие 16 бит зарезервированы 12 бит для будущего использования и 4 бита, которые обозначают определенные атрибуты тегов и данные, представленные точкой повторного анализа.</span><span class="sxs-lookup"><span data-stu-id="79e8a-117">The high 16 bits have 12 bits reserved for future use and 4 bits that denote specific attributes of the tags and the data represented by the reparse point.</span></span> <span data-ttu-id="79e8a-118">Эти биты описаны в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="79e8a-118">The following table describes these bits.</span></span>



| <span data-ttu-id="79e8a-119">bit</span><span class="sxs-lookup"><span data-stu-id="79e8a-119">Bit</span></span> | <span data-ttu-id="79e8a-120">Описание</span><span class="sxs-lookup"><span data-stu-id="79e8a-120">Description</span></span>                                                                                                  |
|-----|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79e8a-121">M</span><span class="sxs-lookup"><span data-stu-id="79e8a-121">M</span></span>   | <span data-ttu-id="79e8a-122">Microsoft bit.</span><span class="sxs-lookup"><span data-stu-id="79e8a-122">Microsoft bit.</span></span> <span data-ttu-id="79e8a-123">Если этот бит задан, владельцем тега будет тег Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="79e8a-123">If this bit is set, the tag is owned by Microsoft.</span></span> <span data-ttu-id="79e8a-124">Все остальные теги должны использовать ноль для этого бита.</span><span class="sxs-lookup"><span data-stu-id="79e8a-124">All other tags must use zero for this bit.</span></span> |
| <span data-ttu-id="79e8a-125">R</span><span class="sxs-lookup"><span data-stu-id="79e8a-125">R</span></span>   | <span data-ttu-id="79e8a-126">Процессу для всех тегов, отличных от Microsoft, значение должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="79e8a-126">Reserved; must be zero for all non-Microsoft tags.</span></span>                                                           |
| <span data-ttu-id="79e8a-127">Нет</span><span class="sxs-lookup"><span data-stu-id="79e8a-127">N</span></span>   | <span data-ttu-id="79e8a-128">Имя суррогатного бита.</span><span class="sxs-lookup"><span data-stu-id="79e8a-128">Name surrogate bit.</span></span> <span data-ttu-id="79e8a-129">Если этот бит задан, файл или каталог представляет другую именованную сущность в системе.</span><span class="sxs-lookup"><span data-stu-id="79e8a-129">If this bit is set, the file or directory represents another named entity in the system.</span></span> |



 

<span data-ttu-id="79e8a-130">Существуют следующие макросы, помогающие в тестировании тегов:</span><span class="sxs-lookup"><span data-stu-id="79e8a-130">The following macros exist to assist in testing tags:</span></span>

-   [<span data-ttu-id="79e8a-131">**исрепарсетагмикрософт**</span><span class="sxs-lookup"><span data-stu-id="79e8a-131">**IsReparseTagMicrosoft**</span></span>](/windows/desktop/api/Winnt/nf-winnt-isreparsetagmicrosoft)
-   [<span data-ttu-id="79e8a-132">**исрепарсетагнамесуррогате**</span><span class="sxs-lookup"><span data-stu-id="79e8a-132">**IsReparseTagNameSurrogate**</span></span>](/windows/desktop/api/Winnt/nf-winnt-isreparsetagnamesurrogate)

<span data-ttu-id="79e8a-133">Каждый макрос возвращает ненулевое значение, если установлен соответствующий бит.</span><span class="sxs-lookup"><span data-stu-id="79e8a-133">Each macro returns a nonzero value if the associated bit is set.</span></span>

<span data-ttu-id="79e8a-134">Ниже приведены предварительно определенные значения тегов повторного анализа Microsoft. они определены в WinNT. h:</span><span class="sxs-lookup"><span data-stu-id="79e8a-134">The following are Microsoft's predefined reparse tag values; they are defined in WinNT.h:</span></span>

-   <span data-ttu-id="79e8a-135">**IO_REPARSE_TAG_AF_UNIX**</span><span class="sxs-lookup"><span data-stu-id="79e8a-135">**IO_REPARSE_TAG_AF_UNIX**</span></span>
-   <span data-ttu-id="79e8a-136">**IO_REPARSE_TAG_APPEXECLINK**</span><span class="sxs-lookup"><span data-stu-id="79e8a-136">**IO_REPARSE_TAG_APPEXECLINK**</span></span>
-   <span data-ttu-id="79e8a-137">**IO_REPARSE_TAG_CLOUD**</span><span class="sxs-lookup"><span data-stu-id="79e8a-137">**IO_REPARSE_TAG_CLOUD**</span></span>
-   <span data-ttu-id="79e8a-138">**IO_REPARSE_TAG_CLOUD_1**</span><span class="sxs-lookup"><span data-stu-id="79e8a-138">**IO_REPARSE_TAG_CLOUD_1**</span></span>
-   <span data-ttu-id="79e8a-139">**IO_REPARSE_TAG_CLOUD_2**</span><span class="sxs-lookup"><span data-stu-id="79e8a-139">**IO_REPARSE_TAG_CLOUD_2**</span></span>
-   <span data-ttu-id="79e8a-140">**IO_REPARSE_TAG_CLOUD_3**</span><span class="sxs-lookup"><span data-stu-id="79e8a-140">**IO_REPARSE_TAG_CLOUD_3**</span></span>
-   <span data-ttu-id="79e8a-141">**IO_REPARSE_TAG_CLOUD_4**</span><span class="sxs-lookup"><span data-stu-id="79e8a-141">**IO_REPARSE_TAG_CLOUD_4**</span></span>
-   <span data-ttu-id="79e8a-142">**IO_REPARSE_TAG_CLOUD_5**</span><span class="sxs-lookup"><span data-stu-id="79e8a-142">**IO_REPARSE_TAG_CLOUD_5**</span></span>
-   <span data-ttu-id="79e8a-143">**IO_REPARSE_TAG_CLOUD_6**</span><span class="sxs-lookup"><span data-stu-id="79e8a-143">**IO_REPARSE_TAG_CLOUD_6**</span></span>
-   <span data-ttu-id="79e8a-144">**IO_REPARSE_TAG_CLOUD_7**</span><span class="sxs-lookup"><span data-stu-id="79e8a-144">**IO_REPARSE_TAG_CLOUD_7**</span></span>
-   <span data-ttu-id="79e8a-145">**IO_REPARSE_TAG_CLOUD_8**</span><span class="sxs-lookup"><span data-stu-id="79e8a-145">**IO_REPARSE_TAG_CLOUD_8**</span></span>
-   <span data-ttu-id="79e8a-146">**IO_REPARSE_TAG_CLOUD_9**</span><span class="sxs-lookup"><span data-stu-id="79e8a-146">**IO_REPARSE_TAG_CLOUD_9**</span></span>
-   <span data-ttu-id="79e8a-147">**IO_REPARSE_TAG_CLOUD_A**</span><span class="sxs-lookup"><span data-stu-id="79e8a-147">**IO_REPARSE_TAG_CLOUD_A**</span></span>
-   <span data-ttu-id="79e8a-148">**IO_REPARSE_TAG_CLOUD_B**</span><span class="sxs-lookup"><span data-stu-id="79e8a-148">**IO_REPARSE_TAG_CLOUD_B**</span></span>
-   <span data-ttu-id="79e8a-149">**IO_REPARSE_TAG_CLOUD_C**</span><span class="sxs-lookup"><span data-stu-id="79e8a-149">**IO_REPARSE_TAG_CLOUD_C**</span></span>
-   <span data-ttu-id="79e8a-150">**IO_REPARSE_TAG_CLOUD_D**</span><span class="sxs-lookup"><span data-stu-id="79e8a-150">**IO_REPARSE_TAG_CLOUD_D**</span></span>
-   <span data-ttu-id="79e8a-151">**IO_REPARSE_TAG_CLOUD_E**</span><span class="sxs-lookup"><span data-stu-id="79e8a-151">**IO_REPARSE_TAG_CLOUD_E**</span></span>
-   <span data-ttu-id="79e8a-152">**IO_REPARSE_TAG_CLOUD_F**</span><span class="sxs-lookup"><span data-stu-id="79e8a-152">**IO_REPARSE_TAG_CLOUD_F**</span></span>
-   <span data-ttu-id="79e8a-153">**IO_REPARSE_TAG_CLOUD_MASK**</span><span class="sxs-lookup"><span data-stu-id="79e8a-153">**IO_REPARSE_TAG_CLOUD_MASK**</span></span>
-   <span data-ttu-id="79e8a-154">**IO_REPARSE_TAG_CSV**</span><span class="sxs-lookup"><span data-stu-id="79e8a-154">**IO_REPARSE_TAG_CSV**</span></span>
-   <span data-ttu-id="79e8a-155">**IO_REPARSE_TAG_DEDUP**</span><span class="sxs-lookup"><span data-stu-id="79e8a-155">**IO_REPARSE_TAG_DEDUP**</span></span>
-   <span data-ttu-id="79e8a-156">**IO_REPARSE_TAG_DFS**</span><span class="sxs-lookup"><span data-stu-id="79e8a-156">**IO_REPARSE_TAG_DFS**</span></span>
-   <span data-ttu-id="79e8a-157">**IO_REPARSE_TAG_DFSR**</span><span class="sxs-lookup"><span data-stu-id="79e8a-157">**IO_REPARSE_TAG_DFSR**</span></span>
-   <span data-ttu-id="79e8a-158">**IO_REPARSE_TAG_FILE_PLACEHOLDER**</span><span class="sxs-lookup"><span data-stu-id="79e8a-158">**IO_REPARSE_TAG_FILE_PLACEHOLDER**</span></span>
-   <span data-ttu-id="79e8a-159">**IO_REPARSE_TAG_GLOBAL_REPARSE**</span><span class="sxs-lookup"><span data-stu-id="79e8a-159">**IO_REPARSE_TAG_GLOBAL_REPARSE**</span></span>
-   <span data-ttu-id="79e8a-160">**IO_REPARSE_TAG_HSM**</span><span class="sxs-lookup"><span data-stu-id="79e8a-160">**IO_REPARSE_TAG_HSM**</span></span>
-   <span data-ttu-id="79e8a-161">**IO_REPARSE_TAG_HSM2**</span><span class="sxs-lookup"><span data-stu-id="79e8a-161">**IO_REPARSE_TAG_HSM2**</span></span>
-   <span data-ttu-id="79e8a-162">**IO_REPARSE_TAG_MOUNT_POINT**</span><span class="sxs-lookup"><span data-stu-id="79e8a-162">**IO_REPARSE_TAG_MOUNT_POINT**</span></span>
-   <span data-ttu-id="79e8a-163">**IO_REPARSE_TAG_NFS**</span><span class="sxs-lookup"><span data-stu-id="79e8a-163">**IO_REPARSE_TAG_NFS**</span></span>
-   <span data-ttu-id="79e8a-164">**IO_REPARSE_TAG_ONEDRIVE**</span><span class="sxs-lookup"><span data-stu-id="79e8a-164">**IO_REPARSE_TAG_ONEDRIVE**</span></span>
-   <span data-ttu-id="79e8a-165">**IO_REPARSE_TAG_PROJFS**</span><span class="sxs-lookup"><span data-stu-id="79e8a-165">**IO_REPARSE_TAG_PROJFS**</span></span>
-   <span data-ttu-id="79e8a-166">**IO_REPARSE_TAG_PROJFS_TOMBSTONE**</span><span class="sxs-lookup"><span data-stu-id="79e8a-166">**IO_REPARSE_TAG_PROJFS_TOMBSTONE**</span></span>
-   <span data-ttu-id="79e8a-167">**IO_REPARSE_TAG_SIS**</span><span class="sxs-lookup"><span data-stu-id="79e8a-167">**IO_REPARSE_TAG_SIS**</span></span>
-   <span data-ttu-id="79e8a-168">**IO_REPARSE_TAG_STORAGE_SYNC**</span><span class="sxs-lookup"><span data-stu-id="79e8a-168">**IO_REPARSE_TAG_STORAGE_SYNC**</span></span>
-   <span data-ttu-id="79e8a-169">**IO_REPARSE_TAG_SYMLINK**</span><span class="sxs-lookup"><span data-stu-id="79e8a-169">**IO_REPARSE_TAG_SYMLINK**</span></span>
-   <span data-ttu-id="79e8a-170">**IO_REPARSE_TAG_UNHANDLED**</span><span class="sxs-lookup"><span data-stu-id="79e8a-170">**IO_REPARSE_TAG_UNHANDLED**</span></span>
-   <span data-ttu-id="79e8a-171">**IO_REPARSE_TAG_WCI**</span><span class="sxs-lookup"><span data-stu-id="79e8a-171">**IO_REPARSE_TAG_WCI**</span></span>
-   <span data-ttu-id="79e8a-172">**IO_REPARSE_TAG_WCI_1**</span><span class="sxs-lookup"><span data-stu-id="79e8a-172">**IO_REPARSE_TAG_WCI_1**</span></span>
-   <span data-ttu-id="79e8a-173">**IO_REPARSE_TAG_WCI_LINK**</span><span class="sxs-lookup"><span data-stu-id="79e8a-173">**IO_REPARSE_TAG_WCI_LINK**</span></span>
-   <span data-ttu-id="79e8a-174">**IO_REPARSE_TAG_WCI_LINK_1**</span><span class="sxs-lookup"><span data-stu-id="79e8a-174">**IO_REPARSE_TAG_WCI_LINK_1**</span></span>
-   <span data-ttu-id="79e8a-175">**IO_REPARSE_TAG_WCI_TOMBSTONE**</span><span class="sxs-lookup"><span data-stu-id="79e8a-175">**IO_REPARSE_TAG_WCI_TOMBSTONE**</span></span>
-   <span data-ttu-id="79e8a-176">**IO_REPARSE_TAG_WIM**</span><span class="sxs-lookup"><span data-stu-id="79e8a-176">**IO_REPARSE_TAG_WIM**</span></span>
-   <span data-ttu-id="79e8a-177">**IO_REPARSE_TAG_WOF**</span><span class="sxs-lookup"><span data-stu-id="79e8a-177">**IO_REPARSE_TAG_WOF**</span></span>

<span data-ttu-id="79e8a-178">Чтобы обеспечить уникальность тегов, корпорация Майкрософт предоставляет механизм распространения новых тегов.</span><span class="sxs-lookup"><span data-stu-id="79e8a-178">To ensure uniqueness of tags, Microsoft provides a mechanism to distribute new tags.</span></span> <span data-ttu-id="79e8a-179">Дополнительные сведения см. в разделе [устанавливаемая файловая система (IFS)](https://www.microsoft.com/whdc/devtools/ifskit/reparse.mspx).</span><span class="sxs-lookup"><span data-stu-id="79e8a-179">For more information, see the [Installable File System (IFS) Kit](https://www.microsoft.com/whdc/devtools/ifskit/reparse.mspx).</span></span>

 

 



