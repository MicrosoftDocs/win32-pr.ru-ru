---
description: 'Дополнительные сведения о: Есентобсолетиксцептион Class'
title: Класс EsentObsoleteException
TOCTitle: EsentObsoleteException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentObsoleteException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentobsoleteexception(v=EXCHG.10)
ms:contentKeyID: 55102357
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentObsoleteException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentObsoleteException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c9d9597c3022d18ba0c6d476710f1c43430babc2
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/10/2021
ms.locfileid: "104547274"
---
# <a name="esentobsoleteexception-class"></a><span data-ttu-id="bc4e2-103">Класс EsentObsoleteException</span><span class="sxs-lookup"><span data-stu-id="bc4e2-103">EsentObsoleteException class</span></span>

<span data-ttu-id="bc4e2-104">Базовый класс для устаревших исключений.</span><span class="sxs-lookup"><span data-stu-id="bc4e2-104">Base class for Obsolete exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="bc4e2-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="bc4e2-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="bc4e2-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="bc4e2-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="bc4e2-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="bc4e2-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="bc4e2-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="bc4e2-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="bc4e2-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="bc4e2-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="bc4e2-110">Microsoft. ISAM. ESENT. Interop. Есентапиексцептион</span><span class="sxs-lookup"><span data-stu-id="bc4e2-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          <span data-ttu-id="bc4e2-111">Microsoft. ISAM. ESENT. Interop. Есентобсолетиксцептион</span><span class="sxs-lookup"><span data-stu-id="bc4e2-111">Microsoft.Isam.Esent.Interop.EsentObsoleteException</span></span>  
            

<span data-ttu-id="bc4e2-112">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="bc4e2-112">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="bc4e2-113">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="bc4e2-113">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="bc4e2-114">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bc4e2-114">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentObsoleteException _
    Inherits EsentApiException
'Usage
Dim instance As EsentObsoleteException
```

``` csharp
[SerializableAttribute]
public abstract class EsentObsoleteException : EsentApiException
```

## <a name="thread-safety"></a><span data-ttu-id="bc4e2-115">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="bc4e2-115">Thread safety</span></span>

<span data-ttu-id="bc4e2-116">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="bc4e2-116">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="bc4e2-117">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="bc4e2-117">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="bc4e2-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bc4e2-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="bc4e2-119">Справочник</span><span class="sxs-lookup"><span data-stu-id="bc4e2-119">Reference</span></span>

[<span data-ttu-id="bc4e2-120">Элементы Есентобсолетиксцептион</span><span class="sxs-lookup"><span data-stu-id="bc4e2-120">EsentObsoleteException members</span></span>](./esentobsoleteexception-members.md)

[<span data-ttu-id="bc4e2-121">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="bc4e2-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

## <a name="derived-types"></a><span data-ttu-id="bc4e2-122">Производные типы</span><span class="sxs-lookup"><span data-stu-id="bc4e2-122">Derived types</span></span>

[<span data-ttu-id="bc4e2-123">System.Object</span><span class="sxs-lookup"><span data-stu-id="bc4e2-123">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="bc4e2-124">System. Exception</span><span class="sxs-lookup"><span data-stu-id="bc4e2-124">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="bc4e2-125">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="bc4e2-125">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="bc4e2-126">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="bc4e2-126">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="bc4e2-127">Microsoft. ISAM. ESENT. Interop. Есентапиексцептион</span><span class="sxs-lookup"><span data-stu-id="bc4e2-127">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          <span data-ttu-id="bc4e2-128">Microsoft. ISAM. ESENT. Interop. Есентобсолетиксцептион</span><span class="sxs-lookup"><span data-stu-id="bc4e2-128">Microsoft.Isam.Esent.Interop.EsentObsoleteException</span></span>  
            [<span data-ttu-id="bc4e2-129">Microsoft. ISAM. ESENT. Interop. Есентакцессдениедексцептион</span><span class="sxs-lookup"><span data-stu-id="bc4e2-129">Microsoft.Isam.Esent.Interop.EsentAccessDeniedException</span></span>](./esentaccessdeniedexception-class.md)  
            [<span data-ttu-id="bc4e2-130">Microsoft. ISAM. ESENT. Interop. Есентбадбаккупдатабасесизиксцептион</span><span class="sxs-lookup"><span data-stu-id="bc4e2-130">Microsoft.Isam.Esent.Interop.EsentBadBackupDatabaseSizeException</span></span>](./esentbadbackupdatabasesizeexception-class.md)  
            [<span data-ttu-id="bc4e2-131">Microsoft. ISAM. ESENT. Interop. Есентбадбукмаркексцептион</span><span class="sxs-lookup"><span data-stu-id="bc4e2-131">Microsoft.Isam.Esent.Interop.EsentBadBookmarkException</span></span>](./esentbadbookmarkexception-class.md)  
            [<span data-ttu-id="bc4e2-132">Microsoft. ISAM. ESENT. Interop. Есентбаддбсигнатуриксцептион</span><span class="sxs-lookup"><span data-stu-id="bc4e2-132">Microsoft.Isam.Esent.Interop.EsentBadDbSignatureException</span></span>](./esentbaddbsignatureexception-class.md)  
            [<span data-ttu-id="bc4e2-133">Microsoft. ISAM. ESENT. Interop. Есентбадпатчпажеексцептион</span><span class="sxs-lookup"><span data-stu-id="bc4e2-133">Microsoft.Isam.Esent.Interop.EsentBadPatchPageException</span></span>](./esentbadpatchpageexception-class.md)  
            [<span data-ttu-id="bc4e2-134">Microsoft. ISAM. ESENT. Interop. Есентбадслвсигнатуриксцептион</span><span class="sxs-lookup"><span data-stu-id="bc4e2-134">Microsoft.Isam.Esent.Interop.EsentBadSLVSignatureException</span></span>](./esentbadslvsignatureexception-class.md)  
            [<span data-ttu-id="bc4e2-135">Microsoft. ISAM. ESENT. Interop. Есентканнотаддфикседварколумнтодериведтабликсцептион</span><span class="sxs-lookup"><span data-stu-id="bc4e2-135">Microsoft.Isam.Esent.Interop.EsentCannotAddFixedVarColumnToDerivedTableException</span></span>](./esentcannotaddfixedvarcolumntoderivedtableexception-class.md)  
            [<span data-ttu-id="bc4e2-136">Microsoft. ISAM. ESENT. Interop. Есентканнотнестдистрибутедтрансактионсексцептион</span><span class="sxs-lookup"><span data-stu-id="bc4e2-136">Microsoft.Isam.Esent.Interop.EsentCannotNestDistributedTransactionsException</span></span>](./esentcannotnestdistributedtransactionsexception-class.md)  
            [<span data-ttu-id="bc4e2-137">Microsoft. ISAM. ESENT. Interop. Есентколумниндекседексцептион</span><span class="sxs-lookup"><span data-stu-id="bc4e2-137">Microsoft.Isam.Esent.Interop.EsentColumnIndexedException</span></span>](./esentcolumnindexedexception-class.md)  
            [<span data-ttu-id="bc4e2-138">Microsoft. ISAM. ESENT. Interop. Есентколумнинрелатионшипексцептион</span><span class="sxs-lookup"><span data-stu-id="bc4e2-138">Microsoft.Isam.Esent.Interop.EsentColumnInRelationshipException</span></span>](./esentcolumninrelationshipexception-class.md)  
            [<span data-ttu-id="bc4e2-139">Microsoft. ISAM. ESENT. Interop. Есентколумнлонжексцептион</span><span class="sxs-lookup"><span data-stu-id="bc4e2-139">Microsoft.Isam.Esent.Interop.EsentColumnLongException</span></span>](./esentcolumnlongexception-class.md)  
            [<span data-ttu-id="bc4e2-140">Microsoft. ISAM. ESENT. Interop. Есентконтаинернотемптексцептион</span><span class="sxs-lookup"><span data-stu-id="bc4e2-140">Microsoft.Isam.Esent.Interop.EsentContainerNotEmptyException</span></span>](./esentcontainernotemptyexception-class.md)  
            [<span data-ttu-id="bc4e2-141">Microsoft. ISAM. ESENT. Interop. Есенткурренцистаккаутофмеморексцептион</span><span class="sxs-lookup"><span data-stu-id="bc4e2-141">Microsoft.Isam.Esent.Interop.EsentCurrencyStackOutOfMemoryException</span></span>](./esentcurrencystackoutofmemoryexception-class.md)  
            [<span data-ttu-id="bc4e2-142">Microsoft. ISAM. ESENT. Interop. EsentDatabase200FormatException</span><span class="sxs-lookup"><span data-stu-id="bc4e2-142">Microsoft.Isam.Esent.Interop.EsentDatabase200FormatException</span></span>](./esentdatabase200formatexception-class.md)  
            [<span data-ttu-id="bc4e2-143">Microsoft. ISAM. ESENT. Interop. EsentDatabase400FormatException</span><span class="sxs-lookup"><span data-stu-id="bc4e2-143">Microsoft.Isam.Esent.Interop.EsentDatabase400FormatException</span></span>](./esentdatabase400formatexception-class.md)  
            [<span data-ttu-id="bc4e2-144">Microsoft. ISAM. ESENT. Interop. EsentDatabase500FormatException</span><span class="sxs-lookup"><span data-stu-id="bc4e2-144">Microsoft.Isam.Esent.Interop.EsentDatabase500FormatException</span></span>](./esentdatabase500formatexception-class.md)  
            [<span data-ttu-id="bc4e2-145">Microsoft. ISAM. ESENT. Interop. Есентдатабасеидинусиксцептион</span><span class="sxs-lookup"><span data-stu-id="bc4e2-145">Microsoft.Isam.Esent.Interop.EsentDatabaseIdInUseException</span></span>](./esentdatabaseidinuseexception-class.md)  
            [<span data-ttu-id="bc4e2-146">Microsoft. ISAM. ESENT. Interop. Есентдатабасепатчфилемисматчексцептион</span><span class="sxs-lookup"><span data-stu-id="bc4e2-146">Microsoft.Isam.Esent.Interop.EsentDatabasePatchFileMismatchException</span></span>](./esentdatabasepatchfilemismatchexception-class.md)  
            [<span data-ttu-id="bc4e2-147">Microsoft. ISAM. ESENT. Interop. Есентдатабасеснотфромсамеснапшотексцептион</span><span class="sxs-lookup"><span data-stu-id="bc4e2-147">Microsoft.Isam.Esent.Interop.EsentDatabasesNotFromSameSnapshotException</span></span>](./esentdatabasesnotfromsamesnapshotexception-class.md)  
            [<span data-ttu-id="bc4e2-148">Microsoft. ISAM. ESENT. Interop. Есентдатабасестреамингфилемисматчексцептион</span><span class="sxs-lookup"><span data-stu-id="bc4e2-148">Microsoft.Isam.Esent.Interop.EsentDatabaseStreamingFileMismatchException</span></span>](./esentdatabasestreamingfilemismatchexception-class.md)  
            [<span data-ttu-id="bc4e2-149">Microsoft. ISAM. ESENT. Interop. Есентдатабасеунаваилабликсцептион</span><span class="sxs-lookup"><span data-stu-id="bc4e2-149">Microsoft.Isam.Esent.Interop.EsentDatabaseUnavailableException</span></span>](./esentdatabaseunavailableexception-class.md)  
            [<span data-ttu-id="bc4e2-150">Microsoft. ISAM. ESENT. Interop. Есентдатахасчанжедексцептион</span><span class="sxs-lookup"><span data-stu-id="bc4e2-150">Microsoft.Isam.Esent.Interop.EsentDataHasChangedException</span></span>](./esentdatahaschangedexception-class.md)  
            [<span data-ttu-id="bc4e2-151">Microsoft. ISAM. ESENT. Interop. Есентдистрибутедтрансактионалреадипрепаредтокоммитексцептион</span><span class="sxs-lookup"><span data-stu-id="bc4e2-151">Microsoft.Isam.Esent.Interop.EsentDistributedTransactionAlreadyPreparedToCommitException</span></span>](./esentdistributedtransactionalreadypreparedtocommitexception-class.md)  
            [<span data-ttu-id="bc4e2-152">Microsoft. ISAM. ESENT. Interop. Есентдистрибутедтрансактионнотетпрепаредтокоммитексцептион</span><span class="sxs-lookup"><span data-stu-id="bc4e2-152">Microsoft.Isam.Esent.Interop.EsentDistributedTransactionNotYetPreparedToCommitException</span></span>](./esentdistributedtransactionnotyetpreparedtocommitexception-class.md)  
            [<span data-ttu-id="bc4e2-153">Microsoft. ISAM. ESENT. Interop. Есентдтккаллбаккунекспектедеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="bc4e2-153">Microsoft.Isam.Esent.Interop.EsentDTCCallbackUnexpectedErrorException</span></span>](./esentdtccallbackunexpectederrorexception-class.md)  
            [<span data-ttu-id="bc4e2-154">Microsoft. ISAM. ESENT. Interop. Есентдткмиссингкаллбаккексцептион</span><span class="sxs-lookup"><span data-stu-id="bc4e2-154">Microsoft.Isam.Esent.Interop.EsentDTCMissingCallbackException</span></span>](./esentdtcmissingcallbackexception-class.md)  
            [<span data-ttu-id="bc4e2-155">Microsoft. ISAM. ESENT. Interop. Есентдткмиссингкаллбакконрековерексцептион</span><span class="sxs-lookup"><span data-stu-id="bc4e2-155">Microsoft.Isam.Esent.Interop.EsentDTCMissingCallbackOnRecoveryException</span></span>](./esentdtcmissingcallbackonrecoveryexception-class.md)  
            [<span data-ttu-id="bc4e2-156">Microsoft. ISAM. ESENT. Interop. Есентфилеклосиксцептион</span><span class="sxs-lookup"><span data-stu-id="bc4e2-156">Microsoft.Isam.Esent.Interop.EsentFileCloseException</span></span>](./esentfilecloseexception-class.md)  
            [<span data-ttu-id="bc4e2-157">Microsoft. ISAM. ESENT. Interop. Есентфилеиоабортексцептион</span><span class="sxs-lookup"><span data-stu-id="bc4e2-157">Microsoft.Isam.Esent.Interop.EsentFileIOAbortException</span></span>](./esentfileioabortexception-class.md)  
            [<span data-ttu-id="bc4e2-158">Microsoft. ISAM. ESENT. Interop. Есентфилеиофаилексцептион</span><span class="sxs-lookup"><span data-stu-id="bc4e2-158">Microsoft.Isam.Esent.Interop.EsentFileIOFailException</span></span>](./esentfileiofailexception-class.md)  
            [<span data-ttu-id="bc4e2-159">Microsoft. ISAM. ESENT. Interop. Есентфилеиоретрексцептион</span><span class="sxs-lookup"><span data-stu-id="bc4e2-159">Microsoft.Isam.Esent.Interop.EsentFileIORetryException</span></span>](./esentfileioretryexception-class.md)  
            [<span data-ttu-id="bc4e2-160">Microsoft. ISAM. ESENT. Interop. Есентфилеиоспарсиксцептион</span><span class="sxs-lookup"><span data-stu-id="bc4e2-160">Microsoft.Isam.Esent.Interop.EsentFileIOSparseException</span></span>](./esentfileiosparseexception-class.md)  
            [<span data-ttu-id="bc4e2-161">Microsoft. ISAM. ESENT. Interop. Есентиндекскантбуилдексцептион</span><span class="sxs-lookup"><span data-stu-id="bc4e2-161">Microsoft.Isam.Esent.Interop.EsentIndexCantBuildException</span></span>](./esentindexcantbuildexception-class.md)  
            [<span data-ttu-id="bc4e2-162">Microsoft. ISAM. ESENT. Interop. Есентиндекступлестуманиколумнсексцептион</span><span class="sxs-lookup"><span data-stu-id="bc4e2-162">Microsoft.Isam.Esent.Interop.EsentIndexTuplesTooManyColumnsException</span></span>](./esentindextuplestoomanycolumnsexception-class.md)  
            [<span data-ttu-id="bc4e2-163">Microsoft. ISAM. ESENT. Interop. Есентинвалидкаунтрексцептион</span><span class="sxs-lookup"><span data-stu-id="bc4e2-163">Microsoft.Isam.Esent.Interop.EsentInvalidCountryException</span></span>](./esentinvalidcountryexception-class.md)  
            [<span data-ttu-id="bc4e2-164">Microsoft. ISAM. ESENT. Interop. Есентинвалидфиленамиксцептион</span><span class="sxs-lookup"><span data-stu-id="bc4e2-164">Microsoft.Isam.Esent.Interop.EsentInvalidFilenameException</span></span>](./esentinvalidfilenameexception-class.md)  
            [<span data-ttu-id="bc4e2-165">Microsoft. ISAM. ESENT. Interop. Есентинвалидлогдиректорексцептион</span><span class="sxs-lookup"><span data-stu-id="bc4e2-165">Microsoft.Isam.Esent.Interop.EsentInvalidLogDirectoryException</span></span>](./esentinvalidlogdirectoryexception-class.md)  
            [<span data-ttu-id="bc4e2-166">Microsoft. ISAM. ESENT. Interop. Есентинвалидлогжедоператионексцептион</span><span class="sxs-lookup"><span data-stu-id="bc4e2-166">Microsoft.Isam.Esent.Interop.EsentInvalidLoggedOperationException</span></span>](./esentinvalidloggedoperationexception-class.md)  
            [<span data-ttu-id="bc4e2-167">Microsoft. ISAM. ESENT. Interop. Есентинвалидобжектексцептион</span><span class="sxs-lookup"><span data-stu-id="bc4e2-167">Microsoft.Isam.Esent.Interop.EsentInvalidObjectException</span></span>](./esentinvalidobjectexception-class.md)  
            [<span data-ttu-id="bc4e2-168">Microsoft. ISAM. ESENT. Interop. Есентинвалидонсортексцептион</span><span class="sxs-lookup"><span data-stu-id="bc4e2-168">Microsoft.Isam.Esent.Interop.EsentInvalidOnSortException</span></span>](./esentinvalidonsortexception-class.md)  
            [<span data-ttu-id="bc4e2-169">Microsoft. ISAM. ESENT. Interop. Есентинвалидсистемпасексцептион</span><span class="sxs-lookup"><span data-stu-id="bc4e2-169">Microsoft.Isam.Esent.Interop.EsentInvalidSystemPathException</span></span>](./esentinvalidsystempathexception-class.md)  
            [<span data-ttu-id="bc4e2-170">Microsoft. ISAM. ESENT. Interop. Есенткэйбаундарексцептион</span><span class="sxs-lookup"><span data-stu-id="bc4e2-170">Microsoft.Isam.Esent.Interop.EsentKeyBoundaryException</span></span>](./esentkeyboundaryexception-class.md)  
            [<span data-ttu-id="bc4e2-171">Microsoft. ISAM. ESENT. Interop. Есенткэйтубижексцептион</span><span class="sxs-lookup"><span data-stu-id="bc4e2-171">Microsoft.Isam.Esent.Interop.EsentKeyTooBigException</span></span>](./esentkeytoobigexception-class.md)  
            [<span data-ttu-id="bc4e2-172">Microsoft. ISAM. ESENT. Interop. Есентлангуаженотсуппортедексцептион</span><span class="sxs-lookup"><span data-stu-id="bc4e2-172">Microsoft.Isam.Esent.Interop.EsentLanguageNotSupportedException</span></span>](./esentlanguagenotsupportedexception-class.md)  
            [<span data-ttu-id="bc4e2-173">Microsoft. ISAM. ESENT. Interop. Есентлинкнотсуппортедексцептион</span><span class="sxs-lookup"><span data-stu-id="bc4e2-173">Microsoft.Isam.Esent.Interop.EsentLinkNotSupportedException</span></span>](./esentlinknotsupportedexception-class.md)  
            [<span data-ttu-id="bc4e2-174">Microsoft. ISAM. ESENT. Interop. Есентлогбуффертусмаллексцептион</span><span class="sxs-lookup"><span data-stu-id="bc4e2-174">Microsoft.Isam.Esent.Interop.EsentLogBufferTooSmallException</span></span>](./esentlogbuffertoosmallexception-class.md)  
            [<span data-ttu-id="bc4e2-175">Microsoft. ISAM. ESENT. Interop. Есентмиссингпатчпажеексцептион</span><span class="sxs-lookup"><span data-stu-id="bc4e2-175">Microsoft.Isam.Esent.Interop.EsentMissingPatchPageException</span></span>](./esentmissingpatchpageexception-class.md)  
            [<span data-ttu-id="bc4e2-176">Microsoft. ISAM. ESENT. Interop. EsentMustCommitDistributedTransactionToLevel0Exception</span><span class="sxs-lookup"><span data-stu-id="bc4e2-176">Microsoft.Isam.Esent.Interop.EsentMustCommitDistributedTransactionToLevel0Exception</span></span>](./esentmustcommitdistributedtransactiontolevel0exception-class.md)  
            [<span data-ttu-id="bc4e2-177">Microsoft. ISAM. ESENT. Interop. Есентмустдисаблелоггингфордбупградиксцептион</span><span class="sxs-lookup"><span data-stu-id="bc4e2-177">Microsoft.Isam.Esent.Interop.EsentMustDisableLoggingForDbUpgradeException</span></span>](./esentmustdisableloggingfordbupgradeexception-class.md)  
            [<span data-ttu-id="bc4e2-178">Microsoft. ISAM. ESENT. Interop. Есентнотиндистрибутедтрансактионексцептион</span><span class="sxs-lookup"><span data-stu-id="bc4e2-178">Microsoft.Isam.Esent.Interop.EsentNotInDistributedTransactionException</span></span>](./esentnotindistributedtransactionexception-class.md)  
            [<span data-ttu-id="bc4e2-179">Microsoft. ISAM. ESENT. Interop. Есентобжектдупликатиксцептион</span><span class="sxs-lookup"><span data-stu-id="bc4e2-179">Microsoft.Isam.Esent.Interop.EsentObjectDuplicateException</span></span>](./esentobjectduplicateexception-class.md)  
            [<span data-ttu-id="bc4e2-180">Microsoft. ISAM. ESENT. Interop. Есентпажебаундарексцептион</span><span class="sxs-lookup"><span data-stu-id="bc4e2-180">Microsoft.Isam.Esent.Interop.EsentPageBoundaryException</span></span>](./esentpageboundaryexception-class.md)  
            [<span data-ttu-id="bc4e2-181">Microsoft. ISAM. ESENT. Interop. Есентпатчфилемиссинжексцептион</span><span class="sxs-lookup"><span data-stu-id="bc4e2-181">Microsoft.Isam.Esent.Interop.EsentPatchFileMissingException</span></span>](./esentpatchfilemissingexception-class.md)  
            [<span data-ttu-id="bc4e2-182">Microsoft. ISAM. ESENT. Interop. Есентрфсфаилуриксцептион</span><span class="sxs-lookup"><span data-stu-id="bc4e2-182">Microsoft.Isam.Esent.Interop.EsentRfsFailureException</span></span>](./esentrfsfailureexception-class.md)  
            [<span data-ttu-id="bc4e2-183">Microsoft. ISAM. ESENT. Interop. Есентрфснотармедексцептион</span><span class="sxs-lookup"><span data-stu-id="bc4e2-183">Microsoft.Isam.Esent.Interop.EsentRfsNotArmedException</span></span>](./esentrfsnotarmedexception-class.md)  
            [<span data-ttu-id="bc4e2-184">Microsoft. ISAM. ESENT. Interop. Есентроллбаккрекуиредексцептион</span><span class="sxs-lookup"><span data-stu-id="bc4e2-184">Microsoft.Isam.Esent.Interop.EsentRollbackRequiredException</span></span>](./esentrollbackrequiredexception-class.md)  
            [<span data-ttu-id="bc4e2-185">Microsoft. ISAM. ESENT. Interop. Есентслвбуффертусмаллексцептион</span><span class="sxs-lookup"><span data-stu-id="bc4e2-185">Microsoft.Isam.Esent.Interop.EsentSLVBufferTooSmallException</span></span>](./esentslvbuffertoosmallexception-class.md)  
            [<span data-ttu-id="bc4e2-186">Microsoft. ISAM. ESENT. Interop. Есентслвколумнканнотделетиксцептион</span><span class="sxs-lookup"><span data-stu-id="bc4e2-186">Microsoft.Isam.Esent.Interop.EsentSLVColumnCannotDeleteException</span></span>](./esentslvcolumncannotdeleteexception-class.md)  
            [<span data-ttu-id="bc4e2-187">Microsoft. ISAM. ESENT. Interop. Есентслвколумндефаултвалуеноталловедексцептион</span><span class="sxs-lookup"><span data-stu-id="bc4e2-187">Microsoft.Isam.Esent.Interop.EsentSLVColumnDefaultValueNotAllowedException</span></span>](./esentslvcolumndefaultvaluenotallowedexception-class.md)  
            [<span data-ttu-id="bc4e2-188">Microsoft. ISAM. ESENT. Interop. Есентслвкорруптедексцептион</span><span class="sxs-lookup"><span data-stu-id="bc4e2-188">Microsoft.Isam.Esent.Interop.EsentSLVCorruptedException</span></span>](./esentslvcorruptedexception-class.md)  
            [<span data-ttu-id="bc4e2-189">Microsoft. ISAM. ESENT. Interop. Есентслвдатабасемиссинжексцептион</span><span class="sxs-lookup"><span data-stu-id="bc4e2-189">Microsoft.Isam.Esent.Interop.EsentSLVDatabaseMissingException</span></span>](./esentslvdatabasemissingexception-class.md)  
            [<span data-ttu-id="bc4e2-190">Microsoft. ISAM. ESENT. Interop. Есентслвеалисткорруптексцептион</span><span class="sxs-lookup"><span data-stu-id="bc4e2-190">Microsoft.Isam.Esent.Interop.EsentSLVEAListCorruptException</span></span>](./esentslvealistcorruptexception-class.md)  
            [<span data-ttu-id="bc4e2-191">Microsoft. ISAM. ESENT. Interop. Есентслвеалисттубижексцептион</span><span class="sxs-lookup"><span data-stu-id="bc4e2-191">Microsoft.Isam.Esent.Interop.EsentSLVEAListTooBigException</span></span>](./esentslvealisttoobigexception-class.md)  
            [<span data-ttu-id="bc4e2-192">Microsoft. ISAM. ESENT. Interop. Есентслвеалистзероаллокатионексцептион</span><span class="sxs-lookup"><span data-stu-id="bc4e2-192">Microsoft.Isam.Esent.Interop.EsentSLVEAListZeroAllocationException</span></span>](./esentslvealistzeroallocationexception-class.md)  
            [<span data-ttu-id="bc4e2-193">Microsoft. ISAM. ESENT. Interop. Есентслвфилеакцессдениедексцептион</span><span class="sxs-lookup"><span data-stu-id="bc4e2-193">Microsoft.Isam.Esent.Interop.EsentSLVFileAccessDeniedException</span></span>](./esentslvfileaccessdeniedexception-class.md)  
            [<span data-ttu-id="bc4e2-194">Microsoft. ISAM. ESENT. Interop. Есентслвфилеинусиксцептион</span><span class="sxs-lookup"><span data-stu-id="bc4e2-194">Microsoft.Isam.Esent.Interop.EsentSLVFileInUseException</span></span>](./esentslvfileinuseexception-class.md)  
            [<span data-ttu-id="bc4e2-195">Microsoft. ISAM. ESENT. Interop. Есентслвфилеинвалидпасексцептион</span><span class="sxs-lookup"><span data-stu-id="bc4e2-195">Microsoft.Isam.Esent.Interop.EsentSLVFileInvalidPathException</span></span>](./esentslvfileinvalidpathexception-class.md)  
            [<span data-ttu-id="bc4e2-196">Microsoft. ISAM. ESENT. Interop. Есентслвфилеиоексцептион</span><span class="sxs-lookup"><span data-stu-id="bc4e2-196">Microsoft.Isam.Esent.Interop.EsentSLVFileIOException</span></span>](./esentslvfileioexception-class.md)  
            [<span data-ttu-id="bc4e2-197">Microsoft. ISAM. ESENT. Interop. Есентслвфиленотфаундексцептион</span><span class="sxs-lookup"><span data-stu-id="bc4e2-197">Microsoft.Isam.Esent.Interop.EsentSLVFileNotFoundException</span></span>](./esentslvfilenotfoundexception-class.md)  
            [<span data-ttu-id="bc4e2-198">Microsoft. ISAM. ESENT. Interop. Есентслвфилесталиксцептион</span><span class="sxs-lookup"><span data-stu-id="bc4e2-198">Microsoft.Isam.Esent.Interop.EsentSLVFileStaleException</span></span>](./esentslvfilestaleexception-class.md)  
            [<span data-ttu-id="bc4e2-199">Microsoft. ISAM. ESENT. Interop. Есентслвфилеункновнексцептион</span><span class="sxs-lookup"><span data-stu-id="bc4e2-199">Microsoft.Isam.Esent.Interop.EsentSLVFileUnknownException</span></span>](./esentslvfileunknownexception-class.md)  
            [<span data-ttu-id="bc4e2-200">Microsoft. ISAM. ESENT. Interop. Есентслвхеадербадчекксумексцептион</span><span class="sxs-lookup"><span data-stu-id="bc4e2-200">Microsoft.Isam.Esent.Interop.EsentSLVHeaderBadChecksumException</span></span>](./esentslvheaderbadchecksumexception-class.md)  
            [<span data-ttu-id="bc4e2-201">Microsoft. ISAM. ESENT. Interop. Есентслвхеадеркорруптедексцептион</span><span class="sxs-lookup"><span data-stu-id="bc4e2-201">Microsoft.Isam.Esent.Interop.EsentSLVHeaderCorruptedException</span></span>](./esentslvheadercorruptedexception-class.md)  
            [<span data-ttu-id="bc4e2-202">Microsoft. ISAM. ESENT. Interop. Есентслвинвалидпасексцептион</span><span class="sxs-lookup"><span data-stu-id="bc4e2-202">Microsoft.Isam.Esent.Interop.EsentSLVInvalidPathException</span></span>](./esentslvinvalidpathexception-class.md)  
            [<span data-ttu-id="bc4e2-203">Microsoft. ISAM. ESENT. Interop. Есентслвовнермапалреадексистсексцептион</span><span class="sxs-lookup"><span data-stu-id="bc4e2-203">Microsoft.Isam.Esent.Interop.EsentSLVOwnerMapAlreadyExistsException</span></span>](./esentslvownermapalreadyexistsexception-class.md)  
            [<span data-ttu-id="bc4e2-204">Microsoft. ISAM. ESENT. Interop. Есентслвовнермапкорруптедексцептион</span><span class="sxs-lookup"><span data-stu-id="bc4e2-204">Microsoft.Isam.Esent.Interop.EsentSLVOwnerMapCorruptedException</span></span>](./esentslvownermapcorruptedexception-class.md)  
            [<span data-ttu-id="bc4e2-205">Microsoft. ISAM. ESENT. Interop. Есентслвовнермаппаженотфаундексцептион</span><span class="sxs-lookup"><span data-stu-id="bc4e2-205">Microsoft.Isam.Esent.Interop.EsentSLVOwnerMapPageNotFoundException</span></span>](./esentslvownermappagenotfoundexception-class.md)  
            [<span data-ttu-id="bc4e2-206">Microsoft. ISAM. ESENT. Interop. Есентслвпажесноткоммиттедексцептион</span><span class="sxs-lookup"><span data-stu-id="bc4e2-206">Microsoft.Isam.Esent.Interop.EsentSLVPagesNotCommittedException</span></span>](./esentslvpagesnotcommittedexception-class.md)  
            [<span data-ttu-id="bc4e2-207">Microsoft. ISAM. ESENT. Interop. Есентслвпажеснотделетедексцептион</span><span class="sxs-lookup"><span data-stu-id="bc4e2-207">Microsoft.Isam.Esent.Interop.EsentSLVPagesNotDeletedException</span></span>](./esentslvpagesnotdeletedexception-class.md)  
            [<span data-ttu-id="bc4e2-208">Microsoft. ISAM. ESENT. Interop. Есентслвпажеснотфриексцептион</span><span class="sxs-lookup"><span data-stu-id="bc4e2-208">Microsoft.Isam.Esent.Interop.EsentSLVPagesNotFreeException</span></span>](./esentslvpagesnotfreeexception-class.md)  
            [<span data-ttu-id="bc4e2-209">Microsoft. ISAM. ESENT. Interop. Есентслвпажеснотресерведексцептион</span><span class="sxs-lookup"><span data-stu-id="bc4e2-209">Microsoft.Isam.Esent.Interop.EsentSLVPagesNotReservedException</span></span>](./esentslvpagesnotreservedexception-class.md)  
            [<span data-ttu-id="bc4e2-210">Microsoft. ISAM. ESENT. Interop. Есентслвпровидернотлоадедексцептион</span><span class="sxs-lookup"><span data-stu-id="bc4e2-210">Microsoft.Isam.Esent.Interop.EsentSLVProviderNotLoadedException</span></span>](./esentslvprovidernotloadedexception-class.md)  
            [<span data-ttu-id="bc4e2-211">Microsoft. ISAM. ESENT. Interop. Есентслвпровидерверсионмисматчексцептион</span><span class="sxs-lookup"><span data-stu-id="bc4e2-211">Microsoft.Isam.Esent.Interop.EsentSLVProviderVersionMismatchException</span></span>](./esentslvproviderversionmismatchexception-class.md)  
            [<span data-ttu-id="bc4e2-212">Microsoft. ISAM. ESENT. Interop. Есентслвреадверифифаилуриксцептион</span><span class="sxs-lookup"><span data-stu-id="bc4e2-212">Microsoft.Isam.Esent.Interop.EsentSLVReadVerifyFailureException</span></span>](./esentslvreadverifyfailureexception-class.md)  
            [<span data-ttu-id="bc4e2-213">Microsoft. ISAM. ESENT. Interop. ЕсентслврутнотспеЦифиедексцептион</span><span class="sxs-lookup"><span data-stu-id="bc4e2-213">Microsoft.Isam.Esent.Interop.EsentSLVRootNotSpecifiedException</span></span>](./esentslvrootnotspecifiedexception-class.md)  
            [<span data-ttu-id="bc4e2-214">Microsoft. ISAM. ESENT. Interop. Есентслврутпасинвалидексцептион</span><span class="sxs-lookup"><span data-stu-id="bc4e2-214">Microsoft.Isam.Esent.Interop.EsentSLVRootPathInvalidException</span></span>](./esentslvrootpathinvalidexception-class.md)  
            [<span data-ttu-id="bc4e2-215">Microsoft. ISAM. ESENT. Interop. Есентслврутстиллопенексцептион</span><span class="sxs-lookup"><span data-stu-id="bc4e2-215">Microsoft.Isam.Esent.Interop.EsentSLVRootStillOpenException</span></span>](./esentslvrootstillopenexception-class.md)  
            [<span data-ttu-id="bc4e2-216">Microsoft. ISAM. ESENT. Interop. Есентслвспацекорруптедексцептион</span><span class="sxs-lookup"><span data-stu-id="bc4e2-216">Microsoft.Isam.Esent.Interop.EsentSLVSpaceCorruptedException</span></span>](./esentslvspacecorruptedexception-class.md)  
            [<span data-ttu-id="bc4e2-217">Microsoft. ISAM. ESENT. Interop. Есентслвспацевритеконфликтексцептион</span><span class="sxs-lookup"><span data-stu-id="bc4e2-217">Microsoft.Isam.Esent.Interop.EsentSLVSpaceWriteConflictException</span></span>](./esentslvspacewriteconflictexception-class.md)  
            [<span data-ttu-id="bc4e2-218">Microsoft. ISAM. ESENT. Interop. Есентслвстреамингфилеалреадексистсексцептион</span><span class="sxs-lookup"><span data-stu-id="bc4e2-218">Microsoft.Isam.Esent.Interop.EsentSLVStreamingFileAlreadyExistsException</span></span>](./esentslvstreamingfilealreadyexistsexception-class.md)  
            [<span data-ttu-id="bc4e2-219">Microsoft. ISAM. ESENT. Interop. Есентслвстреамингфилефуллексцептион</span><span class="sxs-lookup"><span data-stu-id="bc4e2-219">Microsoft.Isam.Esent.Interop.EsentSLVStreamingFileFullException</span></span>](./esentslvstreamingfilefullexception-class.md)  
            [<span data-ttu-id="bc4e2-220">Microsoft. ISAM. ESENT. Interop. Есентслвстреамингфилеинусиксцептион</span><span class="sxs-lookup"><span data-stu-id="bc4e2-220">Microsoft.Isam.Esent.Interop.EsentSLVStreamingFileInUseException</span></span>](./esentslvstreamingfileinuseexception-class.md)  
            [<span data-ttu-id="bc4e2-221">Microsoft. ISAM. ESENT. Interop. Есентслвстреамингфилемиссинжексцептион</span><span class="sxs-lookup"><span data-stu-id="bc4e2-221">Microsoft.Isam.Esent.Interop.EsentSLVStreamingFileMissingException</span></span>](./esentslvstreamingfilemissingexception-class.md)  
            [<span data-ttu-id="bc4e2-222">Microsoft. ISAM. ESENT. Interop. Есентслвстреамингфиленоткреатедексцептион</span><span class="sxs-lookup"><span data-stu-id="bc4e2-222">Microsoft.Isam.Esent.Interop.EsentSLVStreamingFileNotCreatedException</span></span>](./esentslvstreamingfilenotcreatedexception-class.md)  
            [<span data-ttu-id="bc4e2-223">Microsoft. ISAM. ESENT. Interop. Есентслвстреамингфилереадонлексцептион</span><span class="sxs-lookup"><span data-stu-id="bc4e2-223">Microsoft.Isam.Esent.Interop.EsentSLVStreamingFileReadOnlyException</span></span>](./esentslvstreamingfilereadonlyexception-class.md)  
            [<span data-ttu-id="bc4e2-224">Microsoft. ISAM. ESENT. Interop. Есентсофтрековерйонснапшотексцептион</span><span class="sxs-lookup"><span data-stu-id="bc4e2-224">Microsoft.Isam.Esent.Interop.EsentSoftRecoveryOnSnapshotException</span></span>](./esentsoftrecoveryonsnapshotexception-class.md)  
            [<span data-ttu-id="bc4e2-225">Microsoft. ISAM. ESENT. Interop. Есентспаваилексткачеаутофмеморексцептион</span><span class="sxs-lookup"><span data-stu-id="bc4e2-225">Microsoft.Isam.Esent.Interop.EsentSPAvailExtCacheOutOfMemoryException</span></span>](./esentspavailextcacheoutofmemoryexception-class.md)  
            [<span data-ttu-id="bc4e2-226">Microsoft. ISAM. ESENT. Interop. Есентспаваилексткачеаутофсинцексцептион</span><span class="sxs-lookup"><span data-stu-id="bc4e2-226">Microsoft.Isam.Esent.Interop.EsentSPAvailExtCacheOutOfSyncException</span></span>](./esentspavailextcacheoutofsyncexception-class.md)  
            [<span data-ttu-id="bc4e2-227">Microsoft. ISAM. ESENT. Interop. Есентскллинкнотсуппортедексцептион</span><span class="sxs-lookup"><span data-stu-id="bc4e2-227">Microsoft.Isam.Esent.Interop.EsentSQLLinkNotSupportedException</span></span>](./esentsqllinknotsupportedexception-class.md)  
            [<span data-ttu-id="bc4e2-228">Microsoft. ISAM. ESENT. Interop. Есентстреамингдатанотлогжедексцептион</span><span class="sxs-lookup"><span data-stu-id="bc4e2-228">Microsoft.Isam.Esent.Interop.EsentStreamingDataNotLoggedException</span></span>](./esentstreamingdatanotloggedexception-class.md)  
            [<span data-ttu-id="bc4e2-229">Microsoft. ISAM. ESENT. Interop. Есенттагжеднотнуллексцептион</span><span class="sxs-lookup"><span data-stu-id="bc4e2-229">Microsoft.Isam.Esent.Interop.EsentTaggedNotNULLException</span></span>](./esenttaggednotnullexception-class.md)  
            [<span data-ttu-id="bc4e2-230">Microsoft. ISAM. ESENT. Interop. Есенттемпфилеопенеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="bc4e2-230">Microsoft.Isam.Esent.Interop.EsentTempFileOpenErrorException</span></span>](./esenttempfileopenerrorexception-class.md)  
            [<span data-ttu-id="bc4e2-231">Microsoft. ISAM. ESENT. Interop. Есенттуманйопендатабасесексцептион</span><span class="sxs-lookup"><span data-stu-id="bc4e2-231">Microsoft.Isam.Esent.Interop.EsentTooManyOpenDatabasesException</span></span>](./esenttoomanyopendatabasesexception-class.md)  
            [<span data-ttu-id="bc4e2-232">Microsoft. ISAM. ESENT. Interop. Есенттуманисплитсексцептион</span><span class="sxs-lookup"><span data-stu-id="bc4e2-232">Microsoft.Isam.Esent.Interop.EsentTooManySplitsException</span></span>](./esenttoomanysplitsexception-class.md)  
            [<span data-ttu-id="bc4e2-233">Microsoft. ISAM. ESENT. Interop. Есентуникодетранслатионбуффертусмаллексцептион</span><span class="sxs-lookup"><span data-stu-id="bc4e2-233">Microsoft.Isam.Esent.Interop.EsentUnicodeTranslationBufferTooSmallException</span></span>](./esentunicodetranslationbuffertoosmallexception-class.md)