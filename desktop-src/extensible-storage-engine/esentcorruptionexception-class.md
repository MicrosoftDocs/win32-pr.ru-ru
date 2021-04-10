---
description: 'Дополнительные сведения о: Есенткорруптионексцептион Class'
title: Класс EsentCorruptionException
TOCTitle: EsentCorruptionException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentCorruptionException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentcorruptionexception(v=EXCHG.10)
ms:contentKeyID: 55101411
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentCorruptionException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentCorruptionException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a6914c2bf133a1050e3e3800e5c113c6cac1a11f
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/10/2021
ms.locfileid: "104273203"
---
# <a name="esentcorruptionexception-class"></a><span data-ttu-id="b56ad-103">Класс EsentCorruptionException</span><span class="sxs-lookup"><span data-stu-id="b56ad-103">EsentCorruptionException class</span></span>

<span data-ttu-id="b56ad-104">Базовый класс для исключений повреждения.</span><span class="sxs-lookup"><span data-stu-id="b56ad-104">Base class for Corruption exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="b56ad-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="b56ad-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="b56ad-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="b56ad-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="b56ad-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="b56ad-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="b56ad-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="b56ad-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="b56ad-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="b56ad-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="b56ad-110">Microsoft. ISAM. ESENT. Interop. Есентдатаексцептион</span><span class="sxs-lookup"><span data-stu-id="b56ad-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          <span data-ttu-id="b56ad-111">Microsoft. ISAM. ESENT. Interop. Есенткорруптионексцептион</span><span class="sxs-lookup"><span data-stu-id="b56ad-111">Microsoft.Isam.Esent.Interop.EsentCorruptionException</span></span>  
            

<span data-ttu-id="b56ad-112">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b56ad-112">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b56ad-113">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="b56ad-113">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b56ad-114">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b56ad-114">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentCorruptionException _
    Inherits EsentDataException
'Usage
Dim instance As EsentCorruptionException
```

``` csharp
[SerializableAttribute]
public abstract class EsentCorruptionException : EsentDataException
```

## <a name="thread-safety"></a><span data-ttu-id="b56ad-115">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="b56ad-115">Thread safety</span></span>

<span data-ttu-id="b56ad-116">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="b56ad-116">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="b56ad-117">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="b56ad-117">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="b56ad-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b56ad-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b56ad-119">Справочник</span><span class="sxs-lookup"><span data-stu-id="b56ad-119">Reference</span></span>

[<span data-ttu-id="b56ad-120">Элементы Есенткорруптионексцептион</span><span class="sxs-lookup"><span data-stu-id="b56ad-120">EsentCorruptionException members</span></span>](./esentcorruptionexception-members.md)

[<span data-ttu-id="b56ad-121">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="b56ad-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

## <a name="derived-types"></a><span data-ttu-id="b56ad-122">Производные типы</span><span class="sxs-lookup"><span data-stu-id="b56ad-122">Derived types</span></span>

[<span data-ttu-id="b56ad-123">System.Object</span><span class="sxs-lookup"><span data-stu-id="b56ad-123">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="b56ad-124">System. Exception</span><span class="sxs-lookup"><span data-stu-id="b56ad-124">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="b56ad-125">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="b56ad-125">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="b56ad-126">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="b56ad-126">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="b56ad-127">Microsoft. ISAM. ESENT. Interop. Есентдатаексцептион</span><span class="sxs-lookup"><span data-stu-id="b56ad-127">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          <span data-ttu-id="b56ad-128">Microsoft. ISAM. ESENT. Interop. Есенткорруптионексцептион</span><span class="sxs-lookup"><span data-stu-id="b56ad-128">Microsoft.Isam.Esent.Interop.EsentCorruptionException</span></span>  
            [<span data-ttu-id="b56ad-129">Microsoft. ISAM. ESENT. Interop. Есентбадемптипажеексцептион</span><span class="sxs-lookup"><span data-stu-id="b56ad-129">Microsoft.Isam.Esent.Interop.EsentBadEmptyPageException</span></span>](./esentbademptypageexception-class.md)  
            [<span data-ttu-id="b56ad-130">Microsoft. ISAM. ESENT. Interop. Есентбадпажелинкексцептион</span><span class="sxs-lookup"><span data-stu-id="b56ad-130">Microsoft.Isam.Esent.Interop.EsentBadPageLinkException</span></span>](./esentbadpagelinkexception-class.md)  
            [<span data-ttu-id="b56ad-131">Microsoft. ISAM. ESENT. Interop. Есентбадпарентпажелинкексцептион</span><span class="sxs-lookup"><span data-stu-id="b56ad-131">Microsoft.Isam.Esent.Interop.EsentBadParentPageLinkException</span></span>](./esentbadparentpagelinkexception-class.md)  
            [<span data-ttu-id="b56ad-132">Microsoft. ISAM. ESENT. Interop. Есенткаталогкорруптедексцептион</span><span class="sxs-lookup"><span data-stu-id="b56ad-132">Microsoft.Isam.Esent.Interop.EsentCatalogCorruptedException</span></span>](./esentcatalogcorruptedexception-class.md)  
            [<span data-ttu-id="b56ad-133">Microsoft. ISAM. ESENT. Interop. Есентчеккпоинткорруптексцептион</span><span class="sxs-lookup"><span data-stu-id="b56ad-133">Microsoft.Isam.Esent.Interop.EsentCheckpointCorruptException</span></span>](./esentcheckpointcorruptexception-class.md)  
            [<span data-ttu-id="b56ad-134">Microsoft. ISAM. ESENT. Interop. Есенткоммиттедлогфилекорруптексцептион</span><span class="sxs-lookup"><span data-stu-id="b56ad-134">Microsoft.Isam.Esent.Interop.EsentCommittedLogFileCorruptException</span></span>](./esentcommittedlogfilecorruptexception-class.md)  
            [<span data-ttu-id="b56ad-135">Microsoft. ISAM. ESENT. Interop. Есенткоммиттедлогфилесмиссинжексцептион</span><span class="sxs-lookup"><span data-stu-id="b56ad-135">Microsoft.Isam.Esent.Interop.EsentCommittedLogFilesMissingException</span></span>](./esentcommittedlogfilesmissingexception-class.md)  
            [<span data-ttu-id="b56ad-136">Microsoft. ISAM. ESENT. Interop. ЕсентдатабасебуффердепенденЦиескорруптедексцептион</span><span class="sxs-lookup"><span data-stu-id="b56ad-136">Microsoft.Isam.Esent.Interop.EsentDatabaseBufferDependenciesCorruptedException</span></span>](./esentdatabasebufferdependenciescorruptedexception-class.md)  
            [<span data-ttu-id="b56ad-137">Microsoft. ISAM. ESENT. Interop. Есентдатабасекорруптедексцептион</span><span class="sxs-lookup"><span data-stu-id="b56ad-137">Microsoft.Isam.Esent.Interop.EsentDatabaseCorruptedException</span></span>](./esentdatabasecorruptedexception-class.md)  
            [<span data-ttu-id="b56ad-138">Microsoft. ISAM. ESENT. Interop. Есентдбтимекорруптедексцептион</span><span class="sxs-lookup"><span data-stu-id="b56ad-138">Microsoft.Isam.Esent.Interop.EsentDbTimeCorruptedException</span></span>](./esentdbtimecorruptedexception-class.md)  
            [<span data-ttu-id="b56ad-139">Microsoft. ISAM. ESENT. Interop. Есентдекомпрессионфаиледексцептион</span><span class="sxs-lookup"><span data-stu-id="b56ad-139">Microsoft.Isam.Esent.Interop.EsentDecompressionFailedException</span></span>](./esentdecompressionfailedexception-class.md)  
            [<span data-ttu-id="b56ad-140">Microsoft. ISAM. ESENT. Interop. Есентдериведколумнкорруптионексцептион</span><span class="sxs-lookup"><span data-stu-id="b56ad-140">Microsoft.Isam.Esent.Interop.EsentDerivedColumnCorruptionException</span></span>](./esentderivedcolumncorruptionexception-class.md)  
            [<span data-ttu-id="b56ad-141">Microsoft. ISAM. ESENT. Interop. Есентдискреадверификатионфаилуриксцептион</span><span class="sxs-lookup"><span data-stu-id="b56ad-141">Microsoft.Isam.Esent.Interop.EsentDiskReadVerificationFailureException</span></span>](./esentdiskreadverificationfailureexception-class.md)  
            [<span data-ttu-id="b56ad-142">Microsoft. ISAM. ESENT. Interop. Есентфилеиобэйондеофексцептион</span><span class="sxs-lookup"><span data-stu-id="b56ad-142">Microsoft.Isam.Esent.Interop.EsentFileIOBeyondEOFException</span></span>](./esentfileiobeyondeofexception-class.md)  
            [<span data-ttu-id="b56ad-143">Microsoft. ISAM. ESENT. Interop. Есентфилесистемкорруптионексцептион</span><span class="sxs-lookup"><span data-stu-id="b56ad-143">Microsoft.Isam.Esent.Interop.EsentFileSystemCorruptionException</span></span>](./esentfilesystemcorruptionexception-class.md)  
            [<span data-ttu-id="b56ad-144">Microsoft. ISAM. ESENT. Interop. Есентиндексбуилдкорруптедексцептион</span><span class="sxs-lookup"><span data-stu-id="b56ad-144">Microsoft.Isam.Esent.Interop.EsentIndexBuildCorruptedException</span></span>](./esentindexbuildcorruptedexception-class.md)  
            [<span data-ttu-id="b56ad-145">Microsoft. ISAM. ESENT. Interop. Есентинвалидлогсекуенцеексцептион</span><span class="sxs-lookup"><span data-stu-id="b56ad-145">Microsoft.Isam.Esent.Interop.EsentInvalidLogSequenceException</span></span>](./esentinvalidlogsequenceexception-class.md)  
            [<span data-ttu-id="b56ad-146">Microsoft. ISAM. ESENT. Interop. Есентлогкорруптдурингхардрековерексцептион</span><span class="sxs-lookup"><span data-stu-id="b56ad-146">Microsoft.Isam.Esent.Interop.EsentLogCorruptDuringHardRecoveryException</span></span>](./esentlogcorruptduringhardrecoveryexception-class.md)  
            [<span data-ttu-id="b56ad-147">Microsoft. ISAM. ESENT. Interop. Есентлогкорруптдурингхардресториксцептион</span><span class="sxs-lookup"><span data-stu-id="b56ad-147">Microsoft.Isam.Esent.Interop.EsentLogCorruptDuringHardRestoreException</span></span>](./esentlogcorruptduringhardrestoreexception-class.md)  
            [<span data-ttu-id="b56ad-148">Microsoft. ISAM. ESENT. Interop. Есентлогкорруптедексцептион</span><span class="sxs-lookup"><span data-stu-id="b56ad-148">Microsoft.Isam.Esent.Interop.EsentLogCorruptedException</span></span>](./esentlogcorruptedexception-class.md)  
            [<span data-ttu-id="b56ad-149">Microsoft. ISAM. ESENT. Interop. Есентлогфилекорруптексцептион</span><span class="sxs-lookup"><span data-stu-id="b56ad-149">Microsoft.Isam.Esent.Interop.EsentLogFileCorruptException</span></span>](./esentlogfilecorruptexception-class.md)  
            [<span data-ttu-id="b56ad-150">Microsoft. ISAM. ESENT. Interop. Есентлогреадверифифаилуриксцептион</span><span class="sxs-lookup"><span data-stu-id="b56ad-150">Microsoft.Isam.Esent.Interop.EsentLogReadVerifyFailureException</span></span>](./esentlogreadverifyfailureexception-class.md)  
            [<span data-ttu-id="b56ad-151">Microsoft. ISAM. ESENT. Interop. Есентлогторнвритедурингхардрековерексцептион</span><span class="sxs-lookup"><span data-stu-id="b56ad-151">Microsoft.Isam.Esent.Interop.EsentLogTornWriteDuringHardRecoveryException</span></span>](./esentlogtornwriteduringhardrecoveryexception-class.md)  
            [<span data-ttu-id="b56ad-152">Microsoft. ISAM. ESENT. Interop. Есентлогторнвритедурингхардресториксцептион</span><span class="sxs-lookup"><span data-stu-id="b56ad-152">Microsoft.Isam.Esent.Interop.EsentLogTornWriteDuringHardRestoreException</span></span>](./esentlogtornwriteduringhardrestoreexception-class.md)  
            [<span data-ttu-id="b56ad-153">Microsoft. ISAM. ESENT. Interop. Есентлвкорруптедексцептион</span><span class="sxs-lookup"><span data-stu-id="b56ad-153">Microsoft.Isam.Esent.Interop.EsentLVCorruptedException</span></span>](./esentlvcorruptedexception-class.md)  
            [<span data-ttu-id="b56ad-154">Microsoft. ISAM. ESENT. Interop. Есентмиссинглогфиликсцептион</span><span class="sxs-lookup"><span data-stu-id="b56ad-154">Microsoft.Isam.Esent.Interop.EsentMissingLogFileException</span></span>](./esentmissinglogfileexception-class.md)  
            [<span data-ttu-id="b56ad-155">Microsoft. ISAM. ESENT. Interop. Есентмиссингпревиауслогфиликсцептион</span><span class="sxs-lookup"><span data-stu-id="b56ad-155">Microsoft.Isam.Esent.Interop.EsentMissingPreviousLogFileException</span></span>](./esentmissingpreviouslogfileexception-class.md)  
            [<span data-ttu-id="b56ad-156">Microsoft. ISAM. ESENT. Interop. Есентпаженотинитиализедексцептион</span><span class="sxs-lookup"><span data-stu-id="b56ad-156">Microsoft.Isam.Esent.Interop.EsentPageNotInitializedException</span></span>](./esentpagenotinitializedexception-class.md)  
            [<span data-ttu-id="b56ad-157">Microsoft. ISAM. ESENT. Interop. Есентпримариндекскорруптедексцептион</span><span class="sxs-lookup"><span data-stu-id="b56ad-157">Microsoft.Isam.Esent.Interop.EsentPrimaryIndexCorruptedException</span></span>](./esentprimaryindexcorruptedexception-class.md)  
            [<span data-ttu-id="b56ad-158">Microsoft. ISAM. ESENT. Interop. Есентреадлостфлушверифифаилуриксцептион</span><span class="sxs-lookup"><span data-stu-id="b56ad-158">Microsoft.Isam.Esent.Interop.EsentReadLostFlushVerifyFailureException</span></span>](./esentreadlostflushverifyfailureexception-class.md)  
            [<span data-ttu-id="b56ad-159">Microsoft. ISAM. ESENT. Interop. Есентреадпгноверифифаилуриксцептион</span><span class="sxs-lookup"><span data-stu-id="b56ad-159">Microsoft.Isam.Esent.Interop.EsentReadPgnoVerifyFailureException</span></span>](./esentreadpgnoverifyfailureexception-class.md)  
            [<span data-ttu-id="b56ad-160">Microsoft. ISAM. ESENT. Interop. Есентреадверифифаилуриксцептион</span><span class="sxs-lookup"><span data-stu-id="b56ad-160">Microsoft.Isam.Esent.Interop.EsentReadVerifyFailureException</span></span>](./esentreadverifyfailureexception-class.md)  
            [<span data-ttu-id="b56ad-161">Microsoft. ISAM. ESENT. Interop. Есентрекордформатконверсионфаиледексцептион</span><span class="sxs-lookup"><span data-stu-id="b56ad-161">Microsoft.Isam.Esent.Interop.EsentRecordFormatConversionFailedException</span></span>](./esentrecordformatconversionfailedexception-class.md)  
            [<span data-ttu-id="b56ad-162">Microsoft. ISAM. ESENT. Interop. Есентрековериверифифаилуриксцептион</span><span class="sxs-lookup"><span data-stu-id="b56ad-162">Microsoft.Isam.Esent.Interop.EsentRecoveryVerifyFailureException</span></span>](./esentrecoveryverifyfailureexception-class.md)  
            [<span data-ttu-id="b56ad-163">Microsoft. ISAM. ESENT. Interop. Есентредоабруптендедексцептион</span><span class="sxs-lookup"><span data-stu-id="b56ad-163">Microsoft.Isam.Esent.Interop.EsentRedoAbruptEndedException</span></span>](./esentredoabruptendedexception-class.md)  
            [<span data-ttu-id="b56ad-164">Microsoft. ISAM. ESENT. Interop. Есентсекондариндекскорруптедексцептион</span><span class="sxs-lookup"><span data-stu-id="b56ad-164">Microsoft.Isam.Esent.Interop.EsentSecondaryIndexCorruptedException</span></span>](./esentsecondaryindexcorruptedexception-class.md)  
            [<span data-ttu-id="b56ad-165">Microsoft. ISAM. ESENT. Interop. Есентспаваилексткорруптедексцептион</span><span class="sxs-lookup"><span data-stu-id="b56ad-165">Microsoft.Isam.Esent.Interop.EsentSPAvailExtCorruptedException</span></span>](./esentspavailextcorruptedexception-class.md)  
            [<span data-ttu-id="b56ad-166">Microsoft. ISAM. ESENT. Interop. Есентсповнексткорруптедексцептион</span><span class="sxs-lookup"><span data-stu-id="b56ad-166">Microsoft.Isam.Esent.Interop.EsentSPOwnExtCorruptedException</span></span>](./esentspownextcorruptedexception-class.md)