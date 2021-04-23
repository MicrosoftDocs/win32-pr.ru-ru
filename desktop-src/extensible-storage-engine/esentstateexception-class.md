---
description: 'Дополнительные сведения о: Есентстатиксцептион Class'
title: Класс EsentStateException
TOCTitle: EsentStateException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentStateException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentstateexception(v=EXCHG.10)
ms:contentKeyID: 55102986
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentStateException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentStateException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d5815c3b308874f69eab9dcc7b3803ee24f6831b
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/10/2021
ms.locfileid: "104273201"
---
# <a name="esentstateexception-class"></a><span data-ttu-id="ba10c-103">Класс EsentStateException</span><span class="sxs-lookup"><span data-stu-id="ba10c-103">EsentStateException class</span></span>

<span data-ttu-id="ba10c-104">Базовый класс для исключений состояния.</span><span class="sxs-lookup"><span data-stu-id="ba10c-104">Base class for State exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="ba10c-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="ba10c-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="ba10c-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="ba10c-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="ba10c-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="ba10c-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="ba10c-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="ba10c-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="ba10c-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="ba10c-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="ba10c-110">Microsoft. ISAM. ESENT. Interop. Есентапиексцептион</span><span class="sxs-lookup"><span data-stu-id="ba10c-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          <span data-ttu-id="ba10c-111">Microsoft. ISAM. ESENT. Interop. Есентстатиксцептион</span><span class="sxs-lookup"><span data-stu-id="ba10c-111">Microsoft.Isam.Esent.Interop.EsentStateException</span></span>  
            

<span data-ttu-id="ba10c-112">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ba10c-112">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="ba10c-113">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="ba10c-113">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ba10c-114">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ba10c-114">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentStateException _
    Inherits EsentApiException
'Usage
Dim instance As EsentStateException
```

``` csharp
[SerializableAttribute]
public abstract class EsentStateException : EsentApiException
```

## <a name="thread-safety"></a><span data-ttu-id="ba10c-115">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="ba10c-115">Thread safety</span></span>

<span data-ttu-id="ba10c-116">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="ba10c-116">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="ba10c-117">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="ba10c-117">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="ba10c-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ba10c-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ba10c-119">Справочник</span><span class="sxs-lookup"><span data-stu-id="ba10c-119">Reference</span></span>

[<span data-ttu-id="ba10c-120">Элементы Есентстатиксцептион</span><span class="sxs-lookup"><span data-stu-id="ba10c-120">EsentStateException members</span></span>](./esentstateexception-members.md)

[<span data-ttu-id="ba10c-121">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="ba10c-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

## <a name="derived-types"></a><span data-ttu-id="ba10c-122">Производные типы</span><span class="sxs-lookup"><span data-stu-id="ba10c-122">Derived types</span></span>

[<span data-ttu-id="ba10c-123">System.Object</span><span class="sxs-lookup"><span data-stu-id="ba10c-123">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="ba10c-124">System. Exception</span><span class="sxs-lookup"><span data-stu-id="ba10c-124">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="ba10c-125">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="ba10c-125">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="ba10c-126">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="ba10c-126">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="ba10c-127">Microsoft. ISAM. ESENT. Interop. Есентапиексцептион</span><span class="sxs-lookup"><span data-stu-id="ba10c-127">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          <span data-ttu-id="ba10c-128">Microsoft. ISAM. ESENT. Interop. Есентстатиксцептион</span><span class="sxs-lookup"><span data-stu-id="ba10c-128">Microsoft.Isam.Esent.Interop.EsentStateException</span></span>  
            [<span data-ttu-id="ba10c-129">Microsoft. ISAM. ESENT. Interop. Есентбаккупинпрогрессексцептион</span><span class="sxs-lookup"><span data-stu-id="ba10c-129">Microsoft.Isam.Esent.Interop.EsentBackupInProgressException</span></span>](./esentbackupinprogressexception-class.md)  
            [<span data-ttu-id="ba10c-130">Microsoft. ISAM. ESENT. Interop. Есентбаккупноталловедетексцептион</span><span class="sxs-lookup"><span data-stu-id="ba10c-130">Microsoft.Isam.Esent.Interop.EsentBackupNotAllowedYetException</span></span>](./esentbackupnotallowedyetexception-class.md)  
            [<span data-ttu-id="ba10c-131">Microsoft. ISAM. ESENT. Interop. Есентбадитагсекуенцеексцептион</span><span class="sxs-lookup"><span data-stu-id="ba10c-131">Microsoft.Isam.Esent.Interop.EsentBadItagSequenceException</span></span>](./esentbaditagsequenceexception-class.md)  
            [<span data-ttu-id="ba10c-132">Microsoft. ISAM. ESENT. Interop. Есентбуффертусмаллексцептион</span><span class="sxs-lookup"><span data-stu-id="ba10c-132">Microsoft.Isam.Esent.Interop.EsentBufferTooSmallException</span></span>](./esentbuffertoosmallexception-class.md)  
            [<span data-ttu-id="ba10c-133">Microsoft. ISAM. ESENT. Interop. Есенткаллбаккфаиледексцептион</span><span class="sxs-lookup"><span data-stu-id="ba10c-133">Microsoft.Isam.Esent.Interop.EsentCallbackFailedException</span></span>](./esentcallbackfailedexception-class.md)  
            [<span data-ttu-id="ba10c-134">Microsoft. ISAM. ESENT. Interop. Есентдатабасеалреадюпградедексцептион</span><span class="sxs-lookup"><span data-stu-id="ba10c-134">Microsoft.Isam.Esent.Interop.EsentDatabaseAlreadyUpgradedException</span></span>](./esentdatabasealreadyupgradedexception-class.md)  
            [<span data-ttu-id="ba10c-135">Microsoft. ISAM. ESENT. Interop. Есентдатабасефаилединкременталресидексцептион</span><span class="sxs-lookup"><span data-stu-id="ba10c-135">Microsoft.Isam.Esent.Interop.EsentDatabaseFailedIncrementalReseedException</span></span>](./esentdatabasefailedincrementalreseedexception-class.md)  
            [<span data-ttu-id="ba10c-136">Microsoft. ISAM. ESENT. Interop. Есентдатабасеинкомплетеупградиксцептион</span><span class="sxs-lookup"><span data-stu-id="ba10c-136">Microsoft.Isam.Esent.Interop.EsentDatabaseIncompleteUpgradeException</span></span>](./esentdatabaseincompleteupgradeexception-class.md)  
            [<span data-ttu-id="ba10c-137">Microsoft. ISAM. ESENT. Interop. Есентдатабаселеакинспацеексцептион</span><span class="sxs-lookup"><span data-stu-id="ba10c-137">Microsoft.Isam.Esent.Interop.EsentDatabaseLeakInSpaceException</span></span>](./esentdatabaseleakinspaceexception-class.md)  
            [<span data-ttu-id="ba10c-138">Microsoft. ISAM. ESENT. Interop. Есентдиртишутдовнексцептион</span><span class="sxs-lookup"><span data-stu-id="ba10c-138">Microsoft.Isam.Esent.Interop.EsentDirtyShutdownException</span></span>](./esentdirtyshutdownexception-class.md)  
            [<span data-ttu-id="ba10c-139">Microsoft. ISAM. ESENT. Interop. Есентфиленотфаундексцептион</span><span class="sxs-lookup"><span data-stu-id="ba10c-139">Microsoft.Isam.Esent.Interop.EsentFileNotFoundException</span></span>](./esentfilenotfoundexception-class.md)  
            [<span data-ttu-id="ba10c-140">Microsoft. ISAM. ESENT. Interop. Есентиндексинусиксцептион</span><span class="sxs-lookup"><span data-stu-id="ba10c-140">Microsoft.Isam.Esent.Interop.EsentIndexInUseException</span></span>](./esentindexinuseexception-class.md)  
            [<span data-ttu-id="ba10c-141">Microsoft. ISAM. ESENT. Interop. Есентиндекснотфаундексцептион</span><span class="sxs-lookup"><span data-stu-id="ba10c-141">Microsoft.Isam.Esent.Interop.EsentIndexNotFoundException</span></span>](./esentindexnotfoundexception-class.md)  
            [<span data-ttu-id="ba10c-142">Microsoft. ISAM. ESENT. Interop. Есентинвалидбуфферсизиксцептион</span><span class="sxs-lookup"><span data-stu-id="ba10c-142">Microsoft.Isam.Esent.Interop.EsentInvalidBufferSizeException</span></span>](./esentinvalidbuffersizeexception-class.md)  
            [<span data-ttu-id="ba10c-143">Microsoft. ISAM. ESENT. Interop. Есентинвалидлогдатасекуенцеексцептион</span><span class="sxs-lookup"><span data-stu-id="ba10c-143">Microsoft.Isam.Esent.Interop.EsentInvalidLogDataSequenceException</span></span>](./esentinvalidlogdatasequenceexception-class.md)  
            [<span data-ttu-id="ba10c-144">Microsoft. ISAM. ESENT. Interop. Есенткэйдупликатиксцептион</span><span class="sxs-lookup"><span data-stu-id="ba10c-144">Microsoft.Isam.Esent.Interop.EsentKeyDuplicateException</span></span>](./esentkeyduplicateexception-class.md)  
            [<span data-ttu-id="ba10c-145">Microsoft. ISAM. ESENT. Interop. Есенткэйтрункатедексцептион</span><span class="sxs-lookup"><span data-stu-id="ba10c-145">Microsoft.Isam.Esent.Interop.EsentKeyTruncatedException</span></span>](./esentkeytruncatedexception-class.md)  
            [<span data-ttu-id="ba10c-146">Microsoft. ISAM. ESENT. Interop. Есентлогфилесиземисматчдатабасесконсистентексцептион</span><span class="sxs-lookup"><span data-stu-id="ba10c-146">Microsoft.Isam.Esent.Interop.EsentLogFileSizeMismatchDatabasesConsistentException</span></span>](./esentlogfilesizemismatchdatabasesconsistentexception-class.md)  
            [<span data-ttu-id="ba10c-147">Microsoft. ISAM. ESENT. Interop. Есентлогсекторсиземисматчдатабасесконсистентексцептион</span><span class="sxs-lookup"><span data-stu-id="ba10c-147">Microsoft.Isam.Esent.Interop.EsentLogSectorSizeMismatchDatabasesConsistentException</span></span>](./esentlogsectorsizemismatchdatabasesconsistentexception-class.md)  
            [<span data-ttu-id="ba10c-148">Microsoft. ISAM. ESENT. Interop. Есентлснотсетексцептион</span><span class="sxs-lookup"><span data-stu-id="ba10c-148">Microsoft.Isam.Esent.Interop.EsentLSNotSetException</span></span>](./esentlsnotsetexception-class.md)  
            [<span data-ttu-id="ba10c-149">Microsoft. ISAM. ESENT. Interop. Есентмиссингфуллбаккупексцептион</span><span class="sxs-lookup"><span data-stu-id="ba10c-149">Microsoft.Isam.Esent.Interop.EsentMissingFullBackupException</span></span>](./esentmissingfullbackupexception-class.md)  
            [<span data-ttu-id="ba10c-150">Microsoft. ISAM. ESENT. Interop. Есентмултивалуеддупликатеафтертрункатионексцептион</span><span class="sxs-lookup"><span data-stu-id="ba10c-150">Microsoft.Isam.Esent.Interop.EsentMultiValuedDuplicateAfterTruncationException</span></span>](./esentmultivaluedduplicateaftertruncationexception-class.md)  
            [<span data-ttu-id="ba10c-151">Microsoft. ISAM. ESENT. Interop. Есентмултивалуеддупликатиксцептион</span><span class="sxs-lookup"><span data-stu-id="ba10c-151">Microsoft.Isam.Esent.Interop.EsentMultiValuedDuplicateException</span></span>](./esentmultivaluedduplicateexception-class.md)  
            [<span data-ttu-id="ba10c-152">Microsoft. ISAM. ESENT. Interop. Есентноаттачментсфаилединкременталресидексцептион</span><span class="sxs-lookup"><span data-stu-id="ba10c-152">Microsoft.Isam.Esent.Interop.EsentNoAttachmentsFailedIncrementalReseedException</span></span>](./esentnoattachmentsfailedincrementalreseedexception-class.md)  
            [<span data-ttu-id="ba10c-153">Microsoft. ISAM. ESENT. Interop. Есентнобаккупексцептион</span><span class="sxs-lookup"><span data-stu-id="ba10c-153">Microsoft.Isam.Esent.Interop.EsentNoBackupException</span></span>](./esentnobackupexception-class.md)  
            [<span data-ttu-id="ba10c-154">Microsoft. ISAM. ESENT. Interop. Есентнокуррентрекордексцептион</span><span class="sxs-lookup"><span data-stu-id="ba10c-154">Microsoft.Isam.Esent.Interop.EsentNoCurrentRecordException</span></span>](./esentnocurrentrecordexception-class.md)  
            [<span data-ttu-id="ba10c-155">Microsoft. ISAM. ESENT. Interop. Есентобжектнотфаундексцептион</span><span class="sxs-lookup"><span data-stu-id="ba10c-155">Microsoft.Isam.Esent.Interop.EsentObjectNotFoundException</span></span>](./esentobjectnotfoundexception-class.md)  
            [<span data-ttu-id="ba10c-156">Microsoft. ISAM. ESENT. Interop. Есентосснапшотноталловедексцептион</span><span class="sxs-lookup"><span data-stu-id="ba10c-156">Microsoft.Isam.Esent.Interop.EsentOSSnapshotNotAllowedException</span></span>](./esentossnapshotnotallowedexception-class.md)  
            [<span data-ttu-id="ba10c-157">Microsoft. ISAM. ESENT. Interop. Есентрекордделетедексцептион</span><span class="sxs-lookup"><span data-stu-id="ba10c-157">Microsoft.Isam.Esent.Interop.EsentRecordDeletedException</span></span>](./esentrecorddeletedexception-class.md)  
            [<span data-ttu-id="ba10c-158">Microsoft. ISAM. ESENT. Interop. Есентрекорднотфаундексцептион</span><span class="sxs-lookup"><span data-stu-id="ba10c-158">Microsoft.Isam.Esent.Interop.EsentRecordNotFoundException</span></span>](./esentrecordnotfoundexception-class.md)  
            [<span data-ttu-id="ba10c-159">Microsoft. ISAM. ESENT. Interop. Есентрекордтубижексцептион</span><span class="sxs-lookup"><span data-stu-id="ba10c-159">Microsoft.Isam.Esent.Interop.EsentRecordTooBigException</span></span>](./esentrecordtoobigexception-class.md)  
            [<span data-ttu-id="ba10c-160">Microsoft. ISAM. ESENT. Interop. Есентрекордтубигфорбакквардкомпатибилитексцептион</span><span class="sxs-lookup"><span data-stu-id="ba10c-160">Microsoft.Isam.Esent.Interop.EsentRecordTooBigForBackwardCompatibilityException</span></span>](./esentrecordtoobigforbackwardcompatibilityexception-class.md)  
            [<span data-ttu-id="ba10c-161">Microsoft. ISAM. ESENT. Interop. Есентрековередвисеррорсексцептион</span><span class="sxs-lookup"><span data-stu-id="ba10c-161">Microsoft.Isam.Esent.Interop.EsentRecoveredWithErrorsException</span></span>](./esentrecoveredwitherrorsexception-class.md)  
            [<span data-ttu-id="ba10c-162">Microsoft. ISAM. ESENT. Interop. Есентрековередвисаутундодатабасесконсистентексцептион</span><span class="sxs-lookup"><span data-stu-id="ba10c-162">Microsoft.Isam.Esent.Interop.EsentRecoveredWithoutUndoDatabasesConsistentException</span></span>](./esentrecoveredwithoutundodatabasesconsistentexception-class.md)  
            [<span data-ttu-id="ba10c-163">Microsoft. ISAM. ESENT. Interop. Есентрековередвисаутундоексцептион</span><span class="sxs-lookup"><span data-stu-id="ba10c-163">Microsoft.Isam.Esent.Interop.EsentRecoveredWithoutUndoException</span></span>](./esentrecoveredwithoutundoexception-class.md)  
            [<span data-ttu-id="ba10c-164">Microsoft. ISAM. ESENT. Interop. Есентрестореинпрогрессексцептион</span><span class="sxs-lookup"><span data-stu-id="ba10c-164">Microsoft.Isam.Esent.Interop.EsentRestoreInProgressException</span></span>](./esentrestoreinprogressexception-class.md)  
            [<span data-ttu-id="ba10c-165">Microsoft. ISAM. ESENT. Interop. Есентсепаратедлонгвалуиксцептион</span><span class="sxs-lookup"><span data-stu-id="ba10c-165">Microsoft.Isam.Esent.Interop.EsentSeparatedLongValueException</span></span>](./esentseparatedlongvalueexception-class.md)  
            [<span data-ttu-id="ba10c-166">Microsoft. ISAM. ESENT. Interop. Есентсуррогатебаккупинпрогрессексцептион</span><span class="sxs-lookup"><span data-stu-id="ba10c-166">Microsoft.Isam.Esent.Interop.EsentSurrogateBackupInProgressException</span></span>](./esentsurrogatebackupinprogressexception-class.md)  
            [<span data-ttu-id="ba10c-167">Microsoft. ISAM. ESENT. Interop. Есенттабледупликатиксцептион</span><span class="sxs-lookup"><span data-stu-id="ba10c-167">Microsoft.Isam.Esent.Interop.EsentTableDuplicateException</span></span>](./esenttableduplicateexception-class.md)  
            [<span data-ttu-id="ba10c-168">Microsoft. ISAM. ESENT. Interop. Есенттаблеинусиксцептион</span><span class="sxs-lookup"><span data-stu-id="ba10c-168">Microsoft.Isam.Esent.Interop.EsentTableInUseException</span></span>](./esenttableinuseexception-class.md)  
            [<span data-ttu-id="ba10c-169">Microsoft. ISAM. ESENT. Interop. Есенттестинжектионнотсуппортедексцептион</span><span class="sxs-lookup"><span data-stu-id="ba10c-169">Microsoft.Isam.Esent.Interop.EsentTestInjectionNotSupportedException</span></span>](./esenttestinjectionnotsupportedexception-class.md)  
            [<span data-ttu-id="ba10c-170">Microsoft. ISAM. ESENT. Interop. Есентвритеконфликтексцептион</span><span class="sxs-lookup"><span data-stu-id="ba10c-170">Microsoft.Isam.Esent.Interop.EsentWriteConflictException</span></span>](./esentwriteconflictexception-class.md)  
            [<span data-ttu-id="ba10c-171">Microsoft. ISAM. ESENT. Interop. Есентвритеконфликтпримариндексексцептион</span><span class="sxs-lookup"><span data-stu-id="ba10c-171">Microsoft.Isam.Esent.Interop.EsentWriteConflictPrimaryIndexException</span></span>](./esentwriteconflictprimaryindexexception-class.md)