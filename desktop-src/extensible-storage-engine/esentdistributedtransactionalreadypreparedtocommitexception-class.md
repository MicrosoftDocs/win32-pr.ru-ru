---
description: 'Дополнительные сведения о: Есентдистрибутедтрансактионалреадипрепаредтокоммитексцептион Class'
title: Класс Есентдистрибутедтрансактионалреадипрепаредтокоммитексцептион
TOCTitle: EsentDistributedTransactionAlreadyPreparedToCommitException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDistributedTransactionAlreadyPreparedToCommitException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdistributedtransactionalreadypreparedtocommitexception(v=EXCHG.10)
ms:contentKeyID: 55101543
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDistributedTransactionAlreadyPreparedToCommitException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDistributedTransactionAlreadyPreparedToCommitException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bbf4c9b6059cafa6a8cd2c35ce1a26e82fc8804d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104423978"
---
# <a name="esentdistributedtransactionalreadypreparedtocommitexception-class"></a><span data-ttu-id="e6df9-103">Класс Есентдистрибутедтрансактионалреадипрепаредтокоммитексцептион</span><span class="sxs-lookup"><span data-stu-id="e6df9-103">EsentDistributedTransactionAlreadyPreparedToCommitException class</span></span>

<span data-ttu-id="e6df9-104">Базовый класс для JET_err. Исключения Дистрибутедтрансактионалреадипрепаредтокоммит.</span><span class="sxs-lookup"><span data-stu-id="e6df9-104">Base class for JET_err.DistributedTransactionAlreadyPreparedToCommit exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="e6df9-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="e6df9-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="e6df9-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="e6df9-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="e6df9-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="e6df9-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="e6df9-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="e6df9-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="e6df9-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="e6df9-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="e6df9-110">Microsoft. ISAM. ESENT. Interop. Есентапиексцептион</span><span class="sxs-lookup"><span data-stu-id="e6df9-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="e6df9-111">Microsoft. ISAM. ESENT. Interop. Есентобсолетиксцептион</span><span class="sxs-lookup"><span data-stu-id="e6df9-111">Microsoft.Isam.Esent.Interop.EsentObsoleteException</span></span>](./esentobsoleteexception-class.md)  
            <span data-ttu-id="e6df9-112">Microsoft. ISAM. ESENT. Interop. Есентдистрибутедтрансактионалреадипрепаредтокоммитексцептион</span><span class="sxs-lookup"><span data-stu-id="e6df9-112">Microsoft.Isam.Esent.Interop.EsentDistributedTransactionAlreadyPreparedToCommitException</span></span>  

<span data-ttu-id="e6df9-113">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e6df9-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="e6df9-114">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="e6df9-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e6df9-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e6df9-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentDistributedTransactionAlreadyPreparedToCommitException _
    Inherits EsentObsoleteException
'Usage
Dim instance As EsentDistributedTransactionAlreadyPreparedToCommitException
```

``` csharp
[SerializableAttribute]
public sealed class EsentDistributedTransactionAlreadyPreparedToCommitException : EsentObsoleteException
```

## <a name="thread-safety"></a><span data-ttu-id="e6df9-116">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="e6df9-116">Thread safety</span></span>

<span data-ttu-id="e6df9-117">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="e6df9-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="e6df9-118">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="e6df9-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="e6df9-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e6df9-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e6df9-120">Справочник</span><span class="sxs-lookup"><span data-stu-id="e6df9-120">Reference</span></span>

[<span data-ttu-id="e6df9-121">Элементы Есентдистрибутедтрансактионалреадипрепаредтокоммитексцептион</span><span class="sxs-lookup"><span data-stu-id="e6df9-121">EsentDistributedTransactionAlreadyPreparedToCommitException members</span></span>](./esentdistributedtransactionalreadypreparedtocommitexception-members.md)

[<span data-ttu-id="e6df9-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="e6df9-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
