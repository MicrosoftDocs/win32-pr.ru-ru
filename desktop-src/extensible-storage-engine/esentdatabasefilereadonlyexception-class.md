---
description: 'Дополнительные сведения о: Есентдатабасефилереадонлексцептион Class'
title: Класс Есентдатабасефилереадонлексцептион
TOCTitle: EsentDatabaseFileReadOnlyException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDatabaseFileReadOnlyException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdatabasefilereadonlyexception(v=EXCHG.10)
ms:contentKeyID: 55101357
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDatabaseFileReadOnlyException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDatabaseFileReadOnlyException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d9a086aa4ba07125b437114fcf3b52ca705f1851
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497595"
---
# <a name="esentdatabasefilereadonlyexception-class"></a><span data-ttu-id="f5875-103">Класс Есентдатабасефилереадонлексцептион</span><span class="sxs-lookup"><span data-stu-id="f5875-103">EsentDatabaseFileReadOnlyException class</span></span>

<span data-ttu-id="f5875-104">Базовый класс для JET_err. Исключения Датабасефилереадонли.</span><span class="sxs-lookup"><span data-stu-id="f5875-104">Base class for JET_err.DatabaseFileReadOnly exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="f5875-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="f5875-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="f5875-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="f5875-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="f5875-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="f5875-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="f5875-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="f5875-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="f5875-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="f5875-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="f5875-110">Microsoft. ISAM. ESENT. Interop. Есентапиексцептион</span><span class="sxs-lookup"><span data-stu-id="f5875-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="f5875-111">Microsoft. ISAM. ESENT. Interop. Есентусажеексцептион</span><span class="sxs-lookup"><span data-stu-id="f5875-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="f5875-112">Microsoft. ISAM. ESENT. Interop. Есентдатабасефилереадонлексцептион</span><span class="sxs-lookup"><span data-stu-id="f5875-112">Microsoft.Isam.Esent.Interop.EsentDatabaseFileReadOnlyException</span></span>  

<span data-ttu-id="f5875-113">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f5875-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f5875-114">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="f5875-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f5875-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f5875-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentDatabaseFileReadOnlyException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentDatabaseFileReadOnlyException
```

``` csharp
[SerializableAttribute]
public sealed class EsentDatabaseFileReadOnlyException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="f5875-116">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="f5875-116">Thread safety</span></span>

<span data-ttu-id="f5875-117">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="f5875-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="f5875-118">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="f5875-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="f5875-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f5875-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f5875-120">Справочник</span><span class="sxs-lookup"><span data-stu-id="f5875-120">Reference</span></span>

[<span data-ttu-id="f5875-121">Элементы Есентдатабасефилереадонлексцептион</span><span class="sxs-lookup"><span data-stu-id="f5875-121">EsentDatabaseFileReadOnlyException members</span></span>](./esentdatabasefilereadonlyexception-members.md)

[<span data-ttu-id="f5875-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="f5875-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
