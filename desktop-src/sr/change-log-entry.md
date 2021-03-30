---
title: Структура CHANGE_LOG_ENTRY
description: Запись журнала изменений.
ms.assetid: adbdc6e6-895e-486d-a194-c74d2cbd0052
keywords:
- Восстановление системы структуры CHANGE_LOG_ENTRY
- Восстановление системы указателей на структуру PCHANGE_LOG_ENTRY
topic_type:
- apiref
api_name:
- CHANGE_LOG_ENTRY
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4a129b7c8368e6af1d259d6c19a9dde963d9deef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071266"
---
# <a name="change_log_entry-structure"></a><span data-ttu-id="99679-105">\_ \_ Структура записи журнала изменений</span><span class="sxs-lookup"><span data-stu-id="99679-105">CHANGE\_LOG\_ENTRY structure</span></span>

<span data-ttu-id="99679-106">\[Эти сведения относятся только к Windows XP с пакетом обновления 2 (SP2).\]</span><span class="sxs-lookup"><span data-stu-id="99679-106">\[This information applies only to Windows XP with Service Pack 2 (SP2).\]</span></span>

<span data-ttu-id="99679-107">Запись журнала изменений.</span><span class="sxs-lookup"><span data-stu-id="99679-107">A change log entry.</span></span>

## <a name="syntax"></a><span data-ttu-id="99679-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="99679-108">Syntax</span></span>


```C++
typedef struct _CHANGE_LOG_ENTRY {
  RECORD_HEADER RecordHeader;
  DWORD         dwMagicNum;
  DWORD         dwEntryType;
  DWORD         dwEntryFlags;
  DWORD         dwAttributes;
  INT64         i64SequenceNum;
  WCHAR         szProcName[16];
} CHANGE_LOG_ENTRY, *PCHANGE_LOG_ENTRY;
```



## <a name="members"></a><span data-ttu-id="99679-109">Члены</span><span class="sxs-lookup"><span data-stu-id="99679-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="99679-110">**рекордхеадер**</span><span class="sxs-lookup"><span data-stu-id="99679-110">**RecordHeader**</span></span>
</dt> <dd>

<span data-ttu-id="99679-111">Структура [**\_ заголовка записи**](record-header.md) .</span><span class="sxs-lookup"><span data-stu-id="99679-111">A [**RECORD\_HEADER**](record-header.md) structure.</span></span> <span data-ttu-id="99679-112">Элемент **дврекордтипе** должен иметь значение **рекордтипеложентри** (1).</span><span class="sxs-lookup"><span data-stu-id="99679-112">The **dwRecordType** member should be set to **RecordTypeLogEntry** (1).</span></span>

</dd> <dt>

<span data-ttu-id="99679-113">**двмагикнум**</span><span class="sxs-lookup"><span data-stu-id="99679-113">**dwMagicNum**</span></span>
</dt> <dd>

<span data-ttu-id="99679-114">Этот элемент должен иметь значение 0xabcdef12.</span><span class="sxs-lookup"><span data-stu-id="99679-114">This member should be set to 0xabcdef12.</span></span>

</dd> <dt>

<span data-ttu-id="99679-115">**двентритипе**</span><span class="sxs-lookup"><span data-stu-id="99679-115">**dwEntryType**</span></span>
</dt> <dd>

<span data-ttu-id="99679-116">Этот элемент может принимать одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="99679-116">This member can be one of the following values:</span></span>

<dl><span id="CHANGE_LOG_ENTRYTYPES_ACLCHANGE__0x2_"></span><span id="change_log_entrytypes_aclchange__0x2_"></span><span id="CHANGE_LOG_ENTRYTYPES_ACLCHANGE__0X2_"></span><dt>

<span data-ttu-id="99679-117">\_Журнал изменений \_ ентритипес \_ аклчанже \* \* (0x2) \* \*</span><span class="sxs-lookup"><span data-stu-id="99679-117">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_ACLCHANGE\*\* (0x2)\*\*</span></span>
</dt><span id="CHANGE_LOG_ENTRYTYPES_ATTRCHANGE__0x4_"></span><span id="change_log_entrytypes_attrchange__0x4_"></span><span id="CHANGE_LOG_ENTRYTYPES_ATTRCHANGE__0X4_"></span><dt>

<span data-ttu-id="99679-118">\_Журнал изменений \_ ентритипес \_ аттрчанже \* \* (0x4) \* \*</span><span class="sxs-lookup"><span data-stu-id="99679-118">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_ATTRCHANGE\*\* (0x4)\*\*</span></span>
</dt><span id="CHANGE_LOG_ENTRYTYPES_DIRCREATE__0x80_"></span><span id="change_log_entrytypes_dircreate__0x80_"></span><span id="CHANGE_LOG_ENTRYTYPES_DIRCREATE__0X80_"></span><dt>

<span data-ttu-id="99679-119">\_Журнал изменений \_ ентритипес \_ диркреате \* \* (0x80) \* \*</span><span class="sxs-lookup"><span data-stu-id="99679-119">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_DIRCREATE\*\* (0x80)\*\*</span></span>
</dt><span id="CHANGE_LOG_ENTRYTYPES_DIRRENAME__0x100_"></span><span id="change_log_entrytypes_dirrename__0x100_"></span><span id="CHANGE_LOG_ENTRYTYPES_DIRRENAME__0X100_"></span><dt>

<span data-ttu-id="99679-120">\_Журнал изменений \_ ентритипес \_ дирренаме \* \* (0x100) \* \*</span><span class="sxs-lookup"><span data-stu-id="99679-120">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_DIRRENAME\*\* (0x100)\*\*</span></span>
</dt><span id="CHANGE_LOG_ENTRYTYPES_DIRDELETE__0x200_"></span><span id="change_log_entrytypes_dirdelete__0x200_"></span><span id="CHANGE_LOG_ENTRYTYPES_DIRDELETE__0X200_"></span><dt>

<span data-ttu-id="99679-121">\_Журнал изменений \_ ентритипес \_ дирделете \* \* (0x200) \* \*</span><span class="sxs-lookup"><span data-stu-id="99679-121">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_DIRDELETE\*\* (0x200)\*\*</span></span>
</dt><span id="CHANGE_LOG_ENTRYTYPES_FILECREATE__0x20_"></span><span id="change_log_entrytypes_filecreate__0x20_"></span><span id="CHANGE_LOG_ENTRYTYPES_FILECREATE__0X20_"></span><dt>

<span data-ttu-id="99679-122">\_Ентритипес журнал \_ изменений \_ филекреате \* \* (0x20) \* \*</span><span class="sxs-lookup"><span data-stu-id="99679-122">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_FILECREATE\*\* (0x20)\*\*</span></span>
</dt><span id="CHANGE_LOG_ENTRYTYPES_FILEDELETE__0x10_"></span><span id="change_log_entrytypes_filedelete__0x10_"></span><span id="CHANGE_LOG_ENTRYTYPES_FILEDELETE__0X10_"></span><dt>

<span data-ttu-id="99679-123">\_Ентритипес журнал \_ изменений \_ выполнить операцию filedelete \* \* (0x10) \* \*</span><span class="sxs-lookup"><span data-stu-id="99679-123">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_FILEDELETE\*\* (0x10)\*\*</span></span>
</dt><span id="CHANGE_LOG_ENTRYTYPES_FILERENAME__0x40_"></span><span id="change_log_entrytypes_filerename__0x40_"></span><span id="CHANGE_LOG_ENTRYTYPES_FILERENAME__0X40_"></span><dt>

<span data-ttu-id="99679-124">\_Журнал изменений \_ ентритипес \_ филеренаме \* \* (0x40) \* \*</span><span class="sxs-lookup"><span data-stu-id="99679-124">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_FILERENAME\*\* (0x40)\*\*</span></span>
</dt><span id="CHANGE_LOG_ENTRYTYPES_INPRECREATE__0x100000_"></span><span id="change_log_entrytypes_inprecreate__0x100000_"></span><span id="CHANGE_LOG_ENTRYTYPES_INPRECREATE__0X100000_"></span><dt>

<span data-ttu-id="99679-125">\_Журнал изменений \_ ентритипес \_ инпрекреате \* \* (0x100000) \* \*</span><span class="sxs-lookup"><span data-stu-id="99679-125">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_INPRECREATE\*\* (0x100000)\*\*</span></span>
</dt><span id="CHANGE_LOG_ENTRYTYPES_ISDIR__0x20000_"></span><span id="change_log_entrytypes_isdir__0x20000_"></span><span id="CHANGE_LOG_ENTRYTYPES_ISDIR__0X20000_"></span><dt>

<span data-ttu-id="99679-126">\_Журнал изменений \_ ентритипес \_ исдир \* \* (0x20000) \* \*</span><span class="sxs-lookup"><span data-stu-id="99679-126">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_ISDIR\*\* (0x20000)\*\*</span></span>
</dt><span id="CHANGE_LOG_ENTRYTYPES_ISNOTDIR__0x40000_"></span><span id="change_log_entrytypes_isnotdir__0x40000_"></span><span id="CHANGE_LOG_ENTRYTYPES_ISNOTDIR__0X40000_"></span><dt>

<span data-ttu-id="99679-127">\_Журнал изменений \_ ентритипес \_ иснотдир \* \* (0x40000) \* \*</span><span class="sxs-lookup"><span data-stu-id="99679-127">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_ISNOTDIR\*\* (0x40000)\*\*</span></span>
</dt><span id="CHANGE_LOG_ENTRYTYPES_MOUNTCREATE__0x400_"></span><span id="change_log_entrytypes_mountcreate__0x400_"></span><span id="CHANGE_LOG_ENTRYTYPES_MOUNTCREATE__0X400_"></span><dt>

<span data-ttu-id="99679-128">\_Журнал изменений \_ ентритипес \_ маунткреате \* \* (0x400) \* \*</span><span class="sxs-lookup"><span data-stu-id="99679-128">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_MOUNTCREATE\*\* (0x400)\*\*</span></span>
</dt><span id="CHANGE_LOG_ENTRYTYPES_MOUNTDELETE__0x800_"></span><span id="change_log_entrytypes_mountdelete__0x800_"></span><span id="CHANGE_LOG_ENTRYTYPES_MOUNTDELETE__0X800_"></span><dt>

<span data-ttu-id="99679-129">\_Журнал изменений \_ ентритипес \_ маунтделете \* \* (0x800) \* \*</span><span class="sxs-lookup"><span data-stu-id="99679-129">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_MOUNTDELETE\*\* (0x800)\*\*</span></span>
</dt><span id="CHANGE_LOG_ENTRYTYPES_NOOPTIMIZE__0x10000_"></span><span id="change_log_entrytypes_nooptimize__0x10000_"></span><span id="CHANGE_LOG_ENTRYTYPES_NOOPTIMIZE__0X10000_"></span><dt>

<span data-ttu-id="99679-130">CHANGE \_ журнала \_ ЕНТРИТИПЕС \_ unoptimize \* \* (0x10000) \* \*</span><span class="sxs-lookup"><span data-stu-id="99679-130">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_NOOPTIMIZE\*\* (0x10000)\*\*</span></span>
</dt><span id="CHANGE_LOG_ENTRYTYPES_OPENBYID__0x200000_"></span><span id="change_log_entrytypes_openbyid__0x200000_"></span><span id="CHANGE_LOG_ENTRYTYPES_OPENBYID__0X200000_"></span><dt>

<span data-ttu-id="99679-131">\_Журнал изменений \_ ентритипес \_ опенбид \* \* (0x200000) \* \*</span><span class="sxs-lookup"><span data-stu-id="99679-131">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_OPENBYID\*\* (0x200000)\*\*</span></span>
</dt><span id="CHANGE_LOG_ENTRYTYPES_SIMULATEDELETE__0x80000_"></span><span id="change_log_entrytypes_simulatedelete__0x80000_"></span><span id="CHANGE_LOG_ENTRYTYPES_SIMULATEDELETE__0X80000_"></span><dt>

<span data-ttu-id="99679-132">\_Журнал изменений \_ ентритипес \_ симулатеделете \* \* (0x80000) \* \*</span><span class="sxs-lookup"><span data-stu-id="99679-132">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_SIMULATEDELETE\*\* (0x80000)\*\*</span></span>
</dt><span id="CHANGE_LOG_ENTRYTYPES_STREAMCHANGE__0x1_"></span><span id="change_log_entrytypes_streamchange__0x1_"></span><span id="CHANGE_LOG_ENTRYTYPES_STREAMCHANGE__0X1_"></span><dt>

<span data-ttu-id="99679-133">\_Ентритипес журнал \_ изменений \_ стреамчанже \* \* (0x1) \* \*</span><span class="sxs-lookup"><span data-stu-id="99679-133">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_STREAMCHANGE\*\* (0x1)\*\*</span></span>
</dt><span id="CHANGE_LOG_ENTRYTYPES_STREAMCREATE__0x2000_"></span><span id="change_log_entrytypes_streamcreate__0x2000_"></span><span id="CHANGE_LOG_ENTRYTYPES_STREAMCREATE__0X2000_"></span><dt>

<span data-ttu-id="99679-134">\_Журнал изменений \_ ентритипес \_ стреамкреате \* \* (0x2000) \* \*</span><span class="sxs-lookup"><span data-stu-id="99679-134">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_STREAMCREATE\*\* (0x2000)\*\*</span></span>
</dt><span id="CHANGE_LOG_ENTRYTYPES_STREAMOVERWRITE__0x8_"></span><span id="change_log_entrytypes_streamoverwrite__0x8_"></span><span id="CHANGE_LOG_ENTRYTYPES_STREAMOVERWRITE__0X8_"></span><dt>

<span data-ttu-id="99679-135">\_Журнал изменений \_ ентритипес \_ стреамоверврите \* \* (0x8) \* \*</span><span class="sxs-lookup"><span data-stu-id="99679-135">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_STREAMOVERWRITE\*\* (0x8)\*\*</span></span>
</dt><span id="CHANGE_LOG_ENTRYTYPES_VOLUMEERROR__0x1000_"></span><span id="change_log_entrytypes_volumeerror__0x1000_"></span><span id="CHANGE_LOG_ENTRYTYPES_VOLUMEERROR__0X1000_"></span><dt>

<span data-ttu-id="99679-136">\_Журнал изменений \_ ентритипес \_ волумиррор \* \* (0x1000) \* \*</span><span class="sxs-lookup"><span data-stu-id="99679-136">\*\*\*\*CHANGE\_LOG\_ENTRYTYPES\_VOLUMEERROR\*\* (0x1000)\*\*</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="99679-137">**двентрифлагс**</span><span class="sxs-lookup"><span data-stu-id="99679-137">**dwEntryFlags**</span></span>
</dt> <dd>

<span data-ttu-id="99679-138">Этот элемент может принимать одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="99679-138">This member can be one of the following values:</span></span>

<dl><span id="CHANGE_LOG_ENTRYFLAGS_ACLINFO__0x4_"></span><span id="change_log_entryflags_aclinfo__0x4_"></span><span id="CHANGE_LOG_ENTRYFLAGS_ACLINFO__0X4_"></span><dt>

<span data-ttu-id="99679-139">**\_Журнал изменений \_ ентрифлагс \_ аклинфо (0x4)**</span><span class="sxs-lookup"><span data-stu-id="99679-139">**CHANGE\_LOG\_ENTRYFLAGS\_ACLINFO (0x4)**</span></span>
</dt><span id="CHANGE_LOG_ENTRYFLAGS_DEBUGINFO__0x8_"></span><span id="change_log_entryflags_debuginfo__0x8_"></span><span id="CHANGE_LOG_ENTRYFLAGS_DEBUGINFO__0X8_"></span><dt>

<span data-ttu-id="99679-140">**\_Журнал изменений \_ ентрифлагс \_ дебугинфо (0x8)**</span><span class="sxs-lookup"><span data-stu-id="99679-140">**CHANGE\_LOG\_ENTRYFLAGS\_DEBUGINFO (0x8)**</span></span>
</dt><span id="CHANGE_LOG_ENTRYFLAGS_SECONDPATH__0x2_"></span><span id="change_log_entryflags_secondpath__0x2_"></span><span id="CHANGE_LOG_ENTRYFLAGS_SECONDPATH__0X2_"></span><dt>

<span data-ttu-id="99679-141">**\_Журнал изменений \_ ентрифлагс \_ секондпас (0x2)**</span><span class="sxs-lookup"><span data-stu-id="99679-141">**CHANGE\_LOG\_ENTRYFLAGS\_SECONDPATH (0x2)**</span></span>
</dt><span id="CHANGE_LOG_ENTRYFLAGS_SHORTNAME__0x10_"></span><span id="change_log_entryflags_shortname__0x10_"></span><span id="CHANGE_LOG_ENTRYFLAGS_SHORTNAME__0X10_"></span><dt>

<span data-ttu-id="99679-142">**\_Журнал изменений \_ ентрифлагс \_ SHORTNAME (0x10)**</span><span class="sxs-lookup"><span data-stu-id="99679-142">**CHANGE\_LOG\_ENTRYFLAGS\_SHORTNAME (0x10)**</span></span>
</dt><span id="CHANGE_LOG_ENTRYFLAGS_TEMPPATH__0x1_"></span><span id="change_log_entryflags_temppath__0x1_"></span><span id="CHANGE_LOG_ENTRYFLAGS_TEMPPATH__0X1_"></span><dt>

<span data-ttu-id="99679-143">**\_Журнал изменений \_ ентрифлагс \_ темппас (0x1)**</span><span class="sxs-lookup"><span data-stu-id="99679-143">**CHANGE\_LOG\_ENTRYFLAGS\_TEMPPATH (0x1)**</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="99679-144">**дваттрибутес**</span><span class="sxs-lookup"><span data-stu-id="99679-144">**dwAttributes**</span></span>
</dt> <dd>

<span data-ttu-id="99679-145">Атрибуты файла журнала изменений.</span><span class="sxs-lookup"><span data-stu-id="99679-145">The file attributes of the change log file.</span></span> <span data-ttu-id="99679-146">Если атрибуты не указаны, это значение должно быть равно 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="99679-146">If no attributes are specified, this value should be set to 0xFFFFFFFF.</span></span>

</dd> <dt>

<span data-ttu-id="99679-147">**i64SequenceNum**</span><span class="sxs-lookup"><span data-stu-id="99679-147">**i64SequenceNum**</span></span>
</dt> <dd>

<span data-ttu-id="99679-148">Порядковый номер, назначенный записи журнала изменений.</span><span class="sxs-lookup"><span data-stu-id="99679-148">The sequence number assigned to the change log entry.</span></span>

</dd> <dt>

<span data-ttu-id="99679-149">**сзпрокнаме**</span><span class="sxs-lookup"><span data-stu-id="99679-149">**szProcName**</span></span>
</dt> <dd>

<span data-ttu-id="99679-150">Имя процесса, выполняющего изменение.</span><span class="sxs-lookup"><span data-stu-id="99679-150">The name of the process making the change.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="99679-151">Комментарии</span><span class="sxs-lookup"><span data-stu-id="99679-151">Remarks</span></span>

<span data-ttu-id="99679-152">За этой структурой следует переменное число записей данных переменной длины, а также значение **DWORD** , которое должно быть идентично значению элемента **дврекордсизе** в **рекордхеадер**.</span><span class="sxs-lookup"><span data-stu-id="99679-152">This structure is followed by a variable number of variable-length data records, plus a **DWORD** value that should be identical to the value of the **dwRecordSize** member of **RecordHeader**.</span></span>

<span data-ttu-id="99679-153">Записи данных переменной длины состоят из структуры [**\_ заголовка записи**](record-header.md) и данных, которые можно использовать для восстановления записи журнала изменений.</span><span class="sxs-lookup"><span data-stu-id="99679-153">The variable-length data records consist of a [**RECORD\_HEADER**](record-header.md) structure plus data that can be used to restore the change log entry.</span></span> <span data-ttu-id="99679-154">Формат данных зависит от значения элемента **дврекордтипе** структуры **\_ заголовка записи** .</span><span class="sxs-lookup"><span data-stu-id="99679-154">The format of the data depends on the value of the **dwRecordType** member of the **RECORD\_HEADER** structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="99679-155">Требования</span><span class="sxs-lookup"><span data-stu-id="99679-155">Requirements</span></span>



| <span data-ttu-id="99679-156">Требование</span><span class="sxs-lookup"><span data-stu-id="99679-156">Requirement</span></span> | <span data-ttu-id="99679-157">Значение</span><span class="sxs-lookup"><span data-stu-id="99679-157">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="99679-158">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="99679-158">Minimum supported client</span></span><br/> | <span data-ttu-id="99679-159">Только для настольных приложений Windows XP с пакетом обновления 2 \[\]</span><span class="sxs-lookup"><span data-stu-id="99679-159">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="99679-160">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="99679-160">Minimum supported server</span></span><br/> | <span data-ttu-id="99679-161">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="99679-161">None supported</span></span><br/>                            |
| <span data-ttu-id="99679-162">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="99679-162">End of client support</span></span><br/>    | <span data-ttu-id="99679-163">Windows XP с пакетом обновления 2 (SP2)</span><span class="sxs-lookup"><span data-stu-id="99679-163">Windows XP with SP2</span></span><br/>                       |



 

 





