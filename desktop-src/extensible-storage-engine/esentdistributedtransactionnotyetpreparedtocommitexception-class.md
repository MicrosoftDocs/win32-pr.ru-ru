---
description: 'Дополнительные сведения о: Есентдистрибутедтрансактионнотетпрепаредтокоммитексцептион Class'
title: Класс Есентдистрибутедтрансактионнотетпрепаредтокоммитексцептион
TOCTitle: EsentDistributedTransactionNotYetPreparedToCommitException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDistributedTransactionNotYetPreparedToCommitException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdistributedtransactionnotyetpreparedtocommitexception(v=EXCHG.10)
ms:contentKeyID: 55101626
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDistributedTransactionNotYetPreparedToCommitException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDistributedTransactionNotYetPreparedToCommitException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bc118aa601559677c4b93025b9f39275b12bd89d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103909948"
---
# <a name="esentdistributedtransactionnotyetpreparedtocommitexception-class"></a><span data-ttu-id="f7432-103">Класс Есентдистрибутедтрансактионнотетпрепаредтокоммитексцептион</span><span class="sxs-lookup"><span data-stu-id="f7432-103">EsentDistributedTransactionNotYetPreparedToCommitException class</span></span>

<span data-ttu-id="f7432-104">Базовый класс для JET_err. Исключения Дистрибутедтрансактионнотетпрепаредтокоммит.</span><span class="sxs-lookup"><span data-stu-id="f7432-104">Base class for JET_err.DistributedTransactionNotYetPreparedToCommit exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="f7432-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="f7432-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="f7432-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="f7432-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="f7432-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="f7432-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="f7432-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="f7432-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="f7432-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="f7432-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="f7432-110">Microsoft. ISAM. ESENT. Interop. Есентапиексцептион</span><span class="sxs-lookup"><span data-stu-id="f7432-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="f7432-111">Microsoft. ISAM. ESENT. Interop. Есентобсолетиксцептион</span><span class="sxs-lookup"><span data-stu-id="f7432-111">Microsoft.Isam.Esent.Interop.EsentObsoleteException</span></span>](./esentobsoleteexception-class.md)  
            <span data-ttu-id="f7432-112">Microsoft. ISAM. ESENT. Interop. Есентдистрибутедтрансактионнотетпрепаредтокоммитексцептион</span><span class="sxs-lookup"><span data-stu-id="f7432-112">Microsoft.Isam.Esent.Interop.EsentDistributedTransactionNotYetPreparedToCommitException</span></span>  

<span data-ttu-id="f7432-113">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f7432-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f7432-114">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="f7432-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f7432-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f7432-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentDistributedTransactionNotYetPreparedToCommitException _
    Inherits EsentObsoleteException
'Usage
Dim instance As EsentDistributedTransactionNotYetPreparedToCommitException
```

``` csharp
[SerializableAttribute]
public sealed class EsentDistributedTransactionNotYetPreparedToCommitException : EsentObsoleteException
```

## <a name="thread-safety"></a><span data-ttu-id="f7432-116">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="f7432-116">Thread safety</span></span>

<span data-ttu-id="f7432-117">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="f7432-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="f7432-118">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="f7432-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="f7432-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f7432-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f7432-120">Справочник</span><span class="sxs-lookup"><span data-stu-id="f7432-120">Reference</span></span>

[<span data-ttu-id="f7432-121">Элементы Есентдистрибутедтрансактионнотетпрепаредтокоммитексцептион</span><span class="sxs-lookup"><span data-stu-id="f7432-121">EsentDistributedTransactionNotYetPreparedToCommitException members</span></span>](./esentdistributedtransactionnotyetpreparedtocommitexception-members.md)

[<span data-ttu-id="f7432-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="f7432-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
