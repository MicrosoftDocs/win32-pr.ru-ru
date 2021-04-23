---
description: 'Дополнительные сведения о: Есентмиссингкуррентлогфилесексцептион Class'
title: Класс Есентмиссингкуррентлогфилесексцептион
TOCTitle: EsentMissingCurrentLogFilesException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentMissingCurrentLogFilesException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentmissingcurrentlogfilesexception(v=EXCHG.10)
ms:contentKeyID: 55102260
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentMissingCurrentLogFilesException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentMissingCurrentLogFilesException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c00bec8ba2dee02bf0240bda78f29b3b8f4eafa7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673507"
---
# <a name="esentmissingcurrentlogfilesexception-class"></a><span data-ttu-id="dc339-103">Класс Есентмиссингкуррентлогфилесексцептион</span><span class="sxs-lookup"><span data-stu-id="dc339-103">EsentMissingCurrentLogFilesException class</span></span>

<span data-ttu-id="dc339-104">Базовый класс для JET_err. Исключения Миссингкуррентлогфилес.</span><span class="sxs-lookup"><span data-stu-id="dc339-104">Base class for JET_err.MissingCurrentLogFiles exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="dc339-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="dc339-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="dc339-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="dc339-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="dc339-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="dc339-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="dc339-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="dc339-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="dc339-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="dc339-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="dc339-110">Microsoft. ISAM. ESENT. Interop. Есентдатаексцептион</span><span class="sxs-lookup"><span data-stu-id="dc339-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="dc339-111">Microsoft. ISAM. ESENT. Interop. Есентинконсистентексцептион</span><span class="sxs-lookup"><span data-stu-id="dc339-111">Microsoft.Isam.Esent.Interop.EsentInconsistentException</span></span>](./esentinconsistentexception-class.md)  
            <span data-ttu-id="dc339-112">Microsoft. ISAM. ESENT. Interop. Есентмиссингкуррентлогфилесексцептион</span><span class="sxs-lookup"><span data-stu-id="dc339-112">Microsoft.Isam.Esent.Interop.EsentMissingCurrentLogFilesException</span></span>  

<span data-ttu-id="dc339-113">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="dc339-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="dc339-114">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="dc339-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="dc339-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dc339-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentMissingCurrentLogFilesException _
    Inherits EsentInconsistentException
'Usage
Dim instance As EsentMissingCurrentLogFilesException
```

``` csharp
[SerializableAttribute]
public sealed class EsentMissingCurrentLogFilesException : EsentInconsistentException
```

## <a name="thread-safety"></a><span data-ttu-id="dc339-116">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="dc339-116">Thread safety</span></span>

<span data-ttu-id="dc339-117">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="dc339-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="dc339-118">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="dc339-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="dc339-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dc339-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="dc339-120">Справочник</span><span class="sxs-lookup"><span data-stu-id="dc339-120">Reference</span></span>

[<span data-ttu-id="dc339-121">Элементы Есентмиссингкуррентлогфилесексцептион</span><span class="sxs-lookup"><span data-stu-id="dc339-121">EsentMissingCurrentLogFilesException members</span></span>](./esentmissingcurrentlogfilesexception-members.md)

[<span data-ttu-id="dc339-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="dc339-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
