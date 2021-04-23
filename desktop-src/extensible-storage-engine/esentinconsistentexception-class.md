---
description: 'Дополнительные сведения о: Есентинконсистентексцептион Class'
title: Класс EsentInconsistentException
TOCTitle: EsentInconsistentException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentInconsistentException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentinconsistentexception(v=EXCHG.10)
ms:contentKeyID: 55101798
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentInconsistentException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentInconsistentException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e62b963e5b0d3f400a860f7742bb76a183b67bd7
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/10/2021
ms.locfileid: "105674525"
---
# <a name="esentinconsistentexception-class"></a><span data-ttu-id="1ef5d-103">Класс EsentInconsistentException</span><span class="sxs-lookup"><span data-stu-id="1ef5d-103">EsentInconsistentException class</span></span>

<span data-ttu-id="1ef5d-104">Базовый класс для непоследовательных исключений.</span><span class="sxs-lookup"><span data-stu-id="1ef5d-104">Base class for Inconsistent exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="1ef5d-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="1ef5d-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="1ef5d-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="1ef5d-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="1ef5d-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="1ef5d-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="1ef5d-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="1ef5d-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="1ef5d-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="1ef5d-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="1ef5d-110">Microsoft. ISAM. ESENT. Interop. Есентдатаексцептион</span><span class="sxs-lookup"><span data-stu-id="1ef5d-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          <span data-ttu-id="1ef5d-111">Microsoft. ISAM. ESENT. Interop. Есентинконсистентексцептион</span><span class="sxs-lookup"><span data-stu-id="1ef5d-111">Microsoft.Isam.Esent.Interop.EsentInconsistentException</span></span>  
            

<span data-ttu-id="1ef5d-112">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="1ef5d-112">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="1ef5d-113">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="1ef5d-113">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="1ef5d-114">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1ef5d-114">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentInconsistentException _
    Inherits EsentDataException
'Usage
Dim instance As EsentInconsistentException
```

``` csharp
[SerializableAttribute]
public abstract class EsentInconsistentException : EsentDataException
```

## <a name="thread-safety"></a><span data-ttu-id="1ef5d-115">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="1ef5d-115">Thread safety</span></span>

<span data-ttu-id="1ef5d-116">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="1ef5d-116">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="1ef5d-117">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="1ef5d-117">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="1ef5d-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1ef5d-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="1ef5d-119">Справочник</span><span class="sxs-lookup"><span data-stu-id="1ef5d-119">Reference</span></span>

[<span data-ttu-id="1ef5d-120">Элементы Есентинконсистентексцептион</span><span class="sxs-lookup"><span data-stu-id="1ef5d-120">EsentInconsistentException members</span></span>](./esentinconsistentexception-members.md)

[<span data-ttu-id="1ef5d-121">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="1ef5d-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

## <a name="derived-types"></a><span data-ttu-id="1ef5d-122">Производные типы</span><span class="sxs-lookup"><span data-stu-id="1ef5d-122">Derived types</span></span>

[<span data-ttu-id="1ef5d-123">System.Object</span><span class="sxs-lookup"><span data-stu-id="1ef5d-123">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="1ef5d-124">System. Exception</span><span class="sxs-lookup"><span data-stu-id="1ef5d-124">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="1ef5d-125">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="1ef5d-125">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="1ef5d-126">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="1ef5d-126">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="1ef5d-127">Microsoft. ISAM. ESENT. Interop. Есентдатаексцептион</span><span class="sxs-lookup"><span data-stu-id="1ef5d-127">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          <span data-ttu-id="1ef5d-128">Microsoft. ISAM. ESENT. Interop. Есентинконсистентексцептион</span><span class="sxs-lookup"><span data-stu-id="1ef5d-128">Microsoft.Isam.Esent.Interop.EsentInconsistentException</span></span>  
            [<span data-ttu-id="1ef5d-129">Microsoft. ISAM. ESENT. Interop. Есентаттачеддатабасемисматчексцептион</span><span class="sxs-lookup"><span data-stu-id="1ef5d-129">Microsoft.Isam.Esent.Interop.EsentAttachedDatabaseMismatchException</span></span>](./esentattacheddatabasemismatchexception-class.md)  
            [<span data-ttu-id="1ef5d-130">Microsoft. ISAM. ESENT. Interop. Есентбадчеккпоинтсигнатуриксцептион</span><span class="sxs-lookup"><span data-stu-id="1ef5d-130">Microsoft.Isam.Esent.Interop.EsentBadCheckpointSignatureException</span></span>](./esentbadcheckpointsignatureexception-class.md)  
            [<span data-ttu-id="1ef5d-131">Microsoft. ISAM. ESENT. Interop. Есентбадлогсигнатуриксцептион</span><span class="sxs-lookup"><span data-stu-id="1ef5d-131">Microsoft.Isam.Esent.Interop.EsentBadLogSignatureException</span></span>](./esentbadlogsignatureexception-class.md)  
            [<span data-ttu-id="1ef5d-132">Microsoft. ISAM. ESENT. Interop. Есентбадлогверсионексцептион</span><span class="sxs-lookup"><span data-stu-id="1ef5d-132">Microsoft.Isam.Esent.Interop.EsentBadLogVersionException</span></span>](./esentbadlogversionexception-class.md)  
            [<span data-ttu-id="1ef5d-133">Microsoft. ISAM. ESENT. Interop. Есентчеккпоинтфиленотфаундексцептион</span><span class="sxs-lookup"><span data-stu-id="1ef5d-133">Microsoft.Isam.Esent.Interop.EsentCheckpointFileNotFoundException</span></span>](./esentcheckpointfilenotfoundexception-class.md)  
            [<span data-ttu-id="1ef5d-134">Microsoft. ISAM. ESENT. Interop. Есентконсистенттимемисматчексцептион</span><span class="sxs-lookup"><span data-stu-id="1ef5d-134">Microsoft.Isam.Esent.Interop.EsentConsistentTimeMismatchException</span></span>](./esentconsistenttimemismatchexception-class.md)  
            [<span data-ttu-id="1ef5d-135">Microsoft. ISAM. ESENT. Interop. Есентдатабаседиртишутдовнексцептион</span><span class="sxs-lookup"><span data-stu-id="1ef5d-135">Microsoft.Isam.Esent.Interop.EsentDatabaseDirtyShutdownException</span></span>](./esentdatabasedirtyshutdownexception-class.md)  
            [<span data-ttu-id="1ef5d-136">Microsoft. ISAM. ESENT. Interop. Есентдатабасеинкомплетеинкременталресидексцептион</span><span class="sxs-lookup"><span data-stu-id="1ef5d-136">Microsoft.Isam.Esent.Interop.EsentDatabaseIncompleteIncrementalReseedException</span></span>](./esentdatabaseincompleteincrementalreseedexception-class.md)  
            [<span data-ttu-id="1ef5d-137">Microsoft. ISAM. ESENT. Interop. Есентдатабаселогсетмисматчексцептион</span><span class="sxs-lookup"><span data-stu-id="1ef5d-137">Microsoft.Isam.Esent.Interop.EsentDatabaseLogSetMismatchException</span></span>](./esentdatabaselogsetmismatchexception-class.md)  
            [<span data-ttu-id="1ef5d-138">Microsoft. ISAM. ESENT. Interop. Есентдбтиметуневексцептион</span><span class="sxs-lookup"><span data-stu-id="1ef5d-138">Microsoft.Isam.Esent.Interop.EsentDbTimeTooNewException</span></span>](./esentdbtimetoonewexception-class.md)  
            [<span data-ttu-id="1ef5d-139">Microsoft. ISAM. ESENT. Interop. Есентдбтиметуолдексцептион</span><span class="sxs-lookup"><span data-stu-id="1ef5d-139">Microsoft.Isam.Esent.Interop.EsentDbTimeTooOldException</span></span>](./esentdbtimetoooldexception-class.md)  
            [<span data-ttu-id="1ef5d-140">Microsoft. ISAM. ESENT. Interop. Есентендингресторелогтуловексцептион</span><span class="sxs-lookup"><span data-stu-id="1ef5d-140">Microsoft.Isam.Esent.Interop.EsentEndingRestoreLogTooLowException</span></span>](./esentendingrestorelogtoolowexception-class.md)  
            [<span data-ttu-id="1ef5d-141">Microsoft. ISAM. ESENT. Interop. Есентексистинглогфилехасбадсигнатуриксцептион</span><span class="sxs-lookup"><span data-stu-id="1ef5d-141">Microsoft.Isam.Esent.Interop.EsentExistingLogFileHasBadSignatureException</span></span>](./esentexistinglogfilehasbadsignatureexception-class.md)  
            [<span data-ttu-id="1ef5d-142">Microsoft. ISAM. ESENT. Interop. Есентексистинглогфилеиснотконтигуаусексцептион</span><span class="sxs-lookup"><span data-stu-id="1ef5d-142">Microsoft.Isam.Esent.Interop.EsentExistingLogFileIsNotContiguousException</span></span>](./esentexistinglogfileisnotcontiguousexception-class.md)  
            [<span data-ttu-id="1ef5d-143">Microsoft. ISAM. ESENT. Interop. Есентфилеинвалидтипиксцептион</span><span class="sxs-lookup"><span data-stu-id="1ef5d-143">Microsoft.Isam.Esent.Interop.EsentFileInvalidTypeException</span></span>](./esentfileinvalidtypeexception-class.md)  
            [<span data-ttu-id="1ef5d-144">Microsoft. ISAM. ESENT. Interop. Есентгивенлогфилехасбадсигнатуриксцептион</span><span class="sxs-lookup"><span data-stu-id="1ef5d-144">Microsoft.Isam.Esent.Interop.EsentGivenLogFileHasBadSignatureException</span></span>](./esentgivenlogfilehasbadsignatureexception-class.md)  
            [<span data-ttu-id="1ef5d-145">Microsoft. ISAM. ESENT. Interop. Есентгивенлогфилеиснотконтигуаусексцептион</span><span class="sxs-lookup"><span data-stu-id="1ef5d-145">Microsoft.Isam.Esent.Interop.EsentGivenLogFileIsNotContiguousException</span></span>](./esentgivenlogfileisnotcontiguousexception-class.md)  
            [<span data-ttu-id="1ef5d-146">Microsoft. ISAM. ESENT. Interop. Есентинвалидкреатедбверсионексцептион</span><span class="sxs-lookup"><span data-stu-id="1ef5d-146">Microsoft.Isam.Esent.Interop.EsentInvalidCreateDbVersionException</span></span>](./esentinvalidcreatedbversionexception-class.md)  
            [<span data-ttu-id="1ef5d-147">Microsoft. ISAM. ESENT. Interop. Есентинвалиддатабасеверсионексцептион</span><span class="sxs-lookup"><span data-stu-id="1ef5d-147">Microsoft.Isam.Esent.Interop.EsentInvalidDatabaseVersionException</span></span>](./esentinvaliddatabaseversionexception-class.md)  
            [<span data-ttu-id="1ef5d-148">Microsoft. ISAM. ESENT. Interop. Есентлогженератионмисматчексцептион</span><span class="sxs-lookup"><span data-stu-id="1ef5d-148">Microsoft.Isam.Esent.Interop.EsentLogGenerationMismatchException</span></span>](./esentloggenerationmismatchexception-class.md)  
            [<span data-ttu-id="1ef5d-149">Microsoft. ISAM. ESENT. Interop. Есентмиссингкуррентлогфилесексцептион</span><span class="sxs-lookup"><span data-stu-id="1ef5d-149">Microsoft.Isam.Esent.Interop.EsentMissingCurrentLogFilesException</span></span>](./esentmissingcurrentlogfilesexception-class.md)  
            [<span data-ttu-id="1ef5d-150">Microsoft. ISAM. ESENT. Interop. Есентмиссингфилетобаккупексцептион</span><span class="sxs-lookup"><span data-stu-id="1ef5d-150">Microsoft.Isam.Esent.Interop.EsentMissingFileToBackupException</span></span>](./esentmissingfiletobackupexception-class.md)  
            [<span data-ttu-id="1ef5d-151">Microsoft. ISAM. ESENT. Interop. Есентмиссингресторелогфилесексцептион</span><span class="sxs-lookup"><span data-stu-id="1ef5d-151">Microsoft.Isam.Esent.Interop.EsentMissingRestoreLogFilesException</span></span>](./esentmissingrestorelogfilesexception-class.md)  
            [<span data-ttu-id="1ef5d-152">Microsoft. ISAM. ESENT. Interop. Есентпажесиземисматчексцептион</span><span class="sxs-lookup"><span data-stu-id="1ef5d-152">Microsoft.Isam.Esent.Interop.EsentPageSizeMismatchException</span></span>](./esentpagesizemismatchexception-class.md)  
            [<span data-ttu-id="1ef5d-153">Microsoft. ISAM. ESENT. Interop. Есентрекуиредлогфилесмиссинжексцептион</span><span class="sxs-lookup"><span data-stu-id="1ef5d-153">Microsoft.Isam.Esent.Interop.EsentRequiredLogFilesMissingException</span></span>](./esentrequiredlogfilesmissingexception-class.md)  
            [<span data-ttu-id="1ef5d-154">Microsoft. ISAM. ESENT. Interop. Есентстартингресторелогтухигхексцептион</span><span class="sxs-lookup"><span data-stu-id="1ef5d-154">Microsoft.Isam.Esent.Interop.EsentStartingRestoreLogTooHighException</span></span>](./esentstartingrestorelogtoohighexception-class.md)