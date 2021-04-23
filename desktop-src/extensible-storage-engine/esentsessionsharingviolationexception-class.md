---
description: 'Дополнительные сведения о: Есентсессионшарингвиолатионексцептион Class'
title: Класс Есентсессионшарингвиолатионексцептион
TOCTitle: EsentSessionSharingViolationException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentSessionSharingViolationException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentsessionsharingviolationexception(v=EXCHG.10)
ms:contentKeyID: 55102713
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentSessionSharingViolationException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentSessionSharingViolationException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1303792b8d45ec169211c1e176d913db682c850b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999737"
---
# <a name="esentsessionsharingviolationexception-class"></a><span data-ttu-id="0a677-103">Класс Есентсессионшарингвиолатионексцептион</span><span class="sxs-lookup"><span data-stu-id="0a677-103">EsentSessionSharingViolationException class</span></span>

<span data-ttu-id="0a677-104">Базовый класс для JET_err. Исключения Сессионшарингвиолатион.</span><span class="sxs-lookup"><span data-stu-id="0a677-104">Base class for JET_err.SessionSharingViolation exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="0a677-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="0a677-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="0a677-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="0a677-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="0a677-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="0a677-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="0a677-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="0a677-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="0a677-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="0a677-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="0a677-110">Microsoft. ISAM. ESENT. Interop. Есентапиексцептион</span><span class="sxs-lookup"><span data-stu-id="0a677-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="0a677-111">Microsoft. ISAM. ESENT. Interop. Есентусажеексцептион</span><span class="sxs-lookup"><span data-stu-id="0a677-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="0a677-112">Microsoft. ISAM. ESENT. Interop. Есентсессионшарингвиолатионексцептион</span><span class="sxs-lookup"><span data-stu-id="0a677-112">Microsoft.Isam.Esent.Interop.EsentSessionSharingViolationException</span></span>  

<span data-ttu-id="0a677-113">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="0a677-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="0a677-114">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="0a677-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="0a677-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0a677-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentSessionSharingViolationException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentSessionSharingViolationException
```

``` csharp
[SerializableAttribute]
public sealed class EsentSessionSharingViolationException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="0a677-116">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="0a677-116">Thread safety</span></span>

<span data-ttu-id="0a677-117">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="0a677-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="0a677-118">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="0a677-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="0a677-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0a677-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="0a677-120">Справочник</span><span class="sxs-lookup"><span data-stu-id="0a677-120">Reference</span></span>

[<span data-ttu-id="0a677-121">Элементы Есентсессионшарингвиолатионексцептион</span><span class="sxs-lookup"><span data-stu-id="0a677-121">EsentSessionSharingViolationException members</span></span>](./esentsessionsharingviolationexception-members.md)

[<span data-ttu-id="0a677-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="0a677-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
