---
description: 'Дополнительные сведения о: Есентоператионексцептион Class'
title: Класс EsentOperationException
TOCTitle: EsentOperationException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentOperationException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentoperationexception(v=EXCHG.10)
ms:contentKeyID: 55102414
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentOperationException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentOperationException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 314ae88a674f6bd59b0111d40ff3ca5a9eab8a2f
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/10/2021
ms.locfileid: "105713237"
---
# <a name="esentoperationexception-class"></a><span data-ttu-id="31e49-103">Класс EsentOperationException</span><span class="sxs-lookup"><span data-stu-id="31e49-103">EsentOperationException class</span></span>

<span data-ttu-id="31e49-104">Базовый класс для исключений операций.</span><span class="sxs-lookup"><span data-stu-id="31e49-104">Base class for Operation exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="31e49-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="31e49-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="31e49-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="31e49-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="31e49-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="31e49-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="31e49-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="31e49-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="31e49-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="31e49-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        <span data-ttu-id="31e49-110">Microsoft. ISAM. ESENT. Interop. Есентоператионексцептион</span><span class="sxs-lookup"><span data-stu-id="31e49-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>  
          

<span data-ttu-id="31e49-111">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="31e49-111">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="31e49-112">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="31e49-112">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="31e49-113">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="31e49-113">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentOperationException _
    Inherits EsentErrorException
'Usage
Dim instance As EsentOperationException
```

``` csharp
[SerializableAttribute]
public abstract class EsentOperationException : EsentErrorException
```

## <a name="thread-safety"></a><span data-ttu-id="31e49-114">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="31e49-114">Thread safety</span></span>

<span data-ttu-id="31e49-115">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="31e49-115">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="31e49-116">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="31e49-116">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="31e49-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="31e49-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="31e49-118">Справочник</span><span class="sxs-lookup"><span data-stu-id="31e49-118">Reference</span></span>

[<span data-ttu-id="31e49-119">Элементы Есентоператионексцептион</span><span class="sxs-lookup"><span data-stu-id="31e49-119">EsentOperationException members</span></span>](./esentoperationexception-members.md)

[<span data-ttu-id="31e49-120">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="31e49-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

## <a name="derived-types"></a><span data-ttu-id="31e49-121">Производные типы</span><span class="sxs-lookup"><span data-stu-id="31e49-121">Derived types</span></span>

[<span data-ttu-id="31e49-122">System.Object</span><span class="sxs-lookup"><span data-stu-id="31e49-122">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="31e49-123">System. Exception</span><span class="sxs-lookup"><span data-stu-id="31e49-123">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="31e49-124">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="31e49-124">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="31e49-125">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="31e49-125">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        <span data-ttu-id="31e49-126">Microsoft. ISAM. ESENT. Interop. Есентоператионексцептион</span><span class="sxs-lookup"><span data-stu-id="31e49-126">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>  
          [<span data-ttu-id="31e49-127">Microsoft. ISAM. ESENT. Interop. Есентбаккупабортбисерверексцептион</span><span class="sxs-lookup"><span data-stu-id="31e49-127">Microsoft.Isam.Esent.Interop.EsentBackupAbortByServerException</span></span>](./esentbackupabortbyserverexception-class.md)  
          [<span data-ttu-id="31e49-128">Microsoft. ISAM. ESENT. Interop. Есентчеккпоинтдепстудипексцептион</span><span class="sxs-lookup"><span data-stu-id="31e49-128">Microsoft.Isam.Esent.Interop.EsentCheckpointDepthTooDeepException</span></span>](./esentcheckpointdepthtoodeepexception-class.md)  
          [<span data-ttu-id="31e49-129">Microsoft. ISAM. ESENT. Interop. Есентклиентрекуесттостопжетсервицеексцептион</span><span class="sxs-lookup"><span data-stu-id="31e49-129">Microsoft.Isam.Esent.Interop.EsentClientRequestToStopJetServiceException</span></span>](./esentclientrequesttostopjetserviceexception-class.md)  
          [<span data-ttu-id="31e49-130">Microsoft. ISAM. ESENT. Interop. Есентфаталексцептион</span><span class="sxs-lookup"><span data-stu-id="31e49-130">Microsoft.Isam.Esent.Interop.EsentFatalException</span></span>](./esentfatalexception-class.md)  
          [<span data-ttu-id="31e49-131">Microsoft. ISAM. ESENT. Interop. Есентинитинпрогрессексцептион</span><span class="sxs-lookup"><span data-stu-id="31e49-131">Microsoft.Isam.Esent.Interop.EsentInitInProgressException</span></span>](./esentinitinprogressexception-class.md)  
          [<span data-ttu-id="31e49-132">Microsoft. ISAM. ESENT. Interop. Есентинтерналеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="31e49-132">Microsoft.Isam.Esent.Interop.EsentInternalErrorException</span></span>](./esentinternalerrorexception-class.md)  
          [<span data-ttu-id="31e49-133">Microsoft. ISAM. ESENT. Interop. Есентиоексцептион</span><span class="sxs-lookup"><span data-stu-id="31e49-133">Microsoft.Isam.Esent.Interop.EsentIOException</span></span>](./esentioexception-class.md)  
          [<span data-ttu-id="31e49-134">Microsoft. ISAM. ESENT. Interop. Есентнтсистемкаллфаиледексцептион</span><span class="sxs-lookup"><span data-stu-id="31e49-134">Microsoft.Isam.Esent.Interop.EsentNTSystemCallFailedException</span></span>](./esentntsystemcallfailedexception-class.md)  
          [<span data-ttu-id="31e49-135">Microsoft. ISAM. ESENT. Interop. Есентосснапшоттимеаутексцептион</span><span class="sxs-lookup"><span data-stu-id="31e49-135">Microsoft.Isam.Esent.Interop.EsentOSSnapshotTimeOutException</span></span>](./esentossnapshottimeoutexception-class.md)  
          [<span data-ttu-id="31e49-136">Microsoft. ISAM. ESENT. Interop. Есентрекорднотделетедексцептион</span><span class="sxs-lookup"><span data-stu-id="31e49-136">Microsoft.Isam.Esent.Interop.EsentRecordNotDeletedException</span></span>](./esentrecordnotdeletedexception-class.md)  
          [<span data-ttu-id="31e49-137">Microsoft. ISAM. ESENT. Interop. Есентресаурцеексцептион</span><span class="sxs-lookup"><span data-stu-id="31e49-137">Microsoft.Isam.Esent.Interop.EsentResourceException</span></span>](./esentresourceexception-class.md)  
          [<span data-ttu-id="31e49-138">Microsoft. ISAM. ESENT. Interop. Есенттерминпрогрессексцептион</span><span class="sxs-lookup"><span data-stu-id="31e49-138">Microsoft.Isam.Esent.Interop.EsentTermInProgressException</span></span>](./esentterminprogressexception-class.md)  
          [<span data-ttu-id="31e49-139">Microsoft. ISAM. ESENT. Interop. Есентуникоделангуажевалидатионфаилуриксцептион</span><span class="sxs-lookup"><span data-stu-id="31e49-139">Microsoft.Isam.Esent.Interop.EsentUnicodeLanguageValidationFailureException</span></span>](./esentunicodelanguagevalidationfailureexception-class.md)  
          [<span data-ttu-id="31e49-140">Microsoft. ISAM. ESENT. Interop. Есентуникодетранслатионфаилексцептион</span><span class="sxs-lookup"><span data-stu-id="31e49-140">Microsoft.Isam.Esent.Interop.EsentUnicodeTranslationFailException</span></span>](./esentunicodetranslationfailexception-class.md)