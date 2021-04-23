---
description: 'Дополнительные сведения о: Есентдатабасенотфаундексцептион Class'
title: Класс Есентдатабасенотфаундексцептион
TOCTitle: EsentDatabaseNotFoundException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDatabaseNotFoundException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdatabasenotfoundexception(v=EXCHG.10)
ms:contentKeyID: 55101533
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDatabaseNotFoundException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDatabaseNotFoundException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2354fc510899aa75373ba2b32df54c949ae9efed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898509"
---
# <a name="esentdatabasenotfoundexception-class"></a><span data-ttu-id="041b8-103">Класс Есентдатабасенотфаундексцептион</span><span class="sxs-lookup"><span data-stu-id="041b8-103">EsentDatabaseNotFoundException class</span></span>

<span data-ttu-id="041b8-104">Базовый класс для JET_err. Исключения Датабасенотфаунд.</span><span class="sxs-lookup"><span data-stu-id="041b8-104">Base class for JET_err.DatabaseNotFound exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="041b8-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="041b8-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="041b8-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="041b8-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="041b8-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="041b8-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="041b8-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="041b8-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="041b8-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="041b8-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="041b8-110">Microsoft. ISAM. ESENT. Interop. Есентапиексцептион</span><span class="sxs-lookup"><span data-stu-id="041b8-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="041b8-111">Microsoft. ISAM. ESENT. Interop. Есентусажеексцептион</span><span class="sxs-lookup"><span data-stu-id="041b8-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="041b8-112">Microsoft. ISAM. ESENT. Interop. Есентдатабасенотфаундексцептион</span><span class="sxs-lookup"><span data-stu-id="041b8-112">Microsoft.Isam.Esent.Interop.EsentDatabaseNotFoundException</span></span>  

<span data-ttu-id="041b8-113">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="041b8-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="041b8-114">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="041b8-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="041b8-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="041b8-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentDatabaseNotFoundException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentDatabaseNotFoundException
```

``` csharp
[SerializableAttribute]
public sealed class EsentDatabaseNotFoundException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="041b8-116">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="041b8-116">Thread safety</span></span>

<span data-ttu-id="041b8-117">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="041b8-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="041b8-118">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="041b8-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="041b8-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="041b8-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="041b8-120">Справочник</span><span class="sxs-lookup"><span data-stu-id="041b8-120">Reference</span></span>

[<span data-ttu-id="041b8-121">Элементы Есентдатабасенотфаундексцептион</span><span class="sxs-lookup"><span data-stu-id="041b8-121">EsentDatabaseNotFoundException members</span></span>](./esentdatabasenotfoundexception-members.md)

[<span data-ttu-id="041b8-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="041b8-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
