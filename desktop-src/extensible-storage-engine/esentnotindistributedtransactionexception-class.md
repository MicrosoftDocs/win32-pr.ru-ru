---
description: 'Дополнительные сведения о: Есентнотиндистрибутедтрансактионексцептион Class'
title: Класс Есентнотиндистрибутедтрансактионексцептион
TOCTitle: EsentNotInDistributedTransactionException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentNotInDistributedTransactionException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentnotindistributedtransactionexception(v=EXCHG.10)
ms:contentKeyID: 55102293
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentNotInDistributedTransactionException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentNotInDistributedTransactionException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 983aa045b83a0382a3ec7676080f3cdada5e1517
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999645"
---
# <a name="esentnotindistributedtransactionexception-class"></a><span data-ttu-id="ed84f-103">Класс Есентнотиндистрибутедтрансактионексцептион</span><span class="sxs-lookup"><span data-stu-id="ed84f-103">EsentNotInDistributedTransactionException class</span></span>

<span data-ttu-id="ed84f-104">Базовый класс для JET_err. Исключения Нотиндистрибутедтрансактион.</span><span class="sxs-lookup"><span data-stu-id="ed84f-104">Base class for JET_err.NotInDistributedTransaction exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="ed84f-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="ed84f-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="ed84f-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="ed84f-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="ed84f-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="ed84f-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="ed84f-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="ed84f-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="ed84f-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="ed84f-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="ed84f-110">Microsoft. ISAM. ESENT. Interop. Есентапиексцептион</span><span class="sxs-lookup"><span data-stu-id="ed84f-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="ed84f-111">Microsoft. ISAM. ESENT. Interop. Есентобсолетиксцептион</span><span class="sxs-lookup"><span data-stu-id="ed84f-111">Microsoft.Isam.Esent.Interop.EsentObsoleteException</span></span>](./esentobsoleteexception-class.md)  
            <span data-ttu-id="ed84f-112">Microsoft. ISAM. ESENT. Interop. Есентнотиндистрибутедтрансактионексцептион</span><span class="sxs-lookup"><span data-stu-id="ed84f-112">Microsoft.Isam.Esent.Interop.EsentNotInDistributedTransactionException</span></span>  

<span data-ttu-id="ed84f-113">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ed84f-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="ed84f-114">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="ed84f-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ed84f-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ed84f-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentNotInDistributedTransactionException _
    Inherits EsentObsoleteException
'Usage
Dim instance As EsentNotInDistributedTransactionException
```

``` csharp
[SerializableAttribute]
public sealed class EsentNotInDistributedTransactionException : EsentObsoleteException
```

## <a name="thread-safety"></a><span data-ttu-id="ed84f-116">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="ed84f-116">Thread safety</span></span>

<span data-ttu-id="ed84f-117">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="ed84f-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="ed84f-118">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="ed84f-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="ed84f-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ed84f-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ed84f-120">Справочник</span><span class="sxs-lookup"><span data-stu-id="ed84f-120">Reference</span></span>

[<span data-ttu-id="ed84f-121">Элементы Есентнотиндистрибутедтрансактионексцептион</span><span class="sxs-lookup"><span data-stu-id="ed84f-121">EsentNotInDistributedTransactionException members</span></span>](./esentnotindistributedtransactionexception-members.md)

[<span data-ttu-id="ed84f-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="ed84f-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
