---
description: 'Дополнительные сведения о: Есентлогторнвритедурингхардресториксцептион Class'
title: Класс Есентлогторнвритедурингхардресториксцептион
TOCTitle: EsentLogTornWriteDuringHardRestoreException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentLogTornWriteDuringHardRestoreException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentlogtornwriteduringhardrestoreexception(v=EXCHG.10)
ms:contentKeyID: 55102166
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentLogTornWriteDuringHardRestoreException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentLogTornWriteDuringHardRestoreException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e0ce33334dfc45bcdc2e643a78b8cca9197f3855
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263729"
---
# <a name="esentlogtornwriteduringhardrestoreexception-class"></a><span data-ttu-id="abda2-103">Класс Есентлогторнвритедурингхардресториксцептион</span><span class="sxs-lookup"><span data-stu-id="abda2-103">EsentLogTornWriteDuringHardRestoreException class</span></span>

<span data-ttu-id="abda2-104">Базовый класс для JET_err. Исключения Логторнвритедурингхардресторе.</span><span class="sxs-lookup"><span data-stu-id="abda2-104">Base class for JET_err.LogTornWriteDuringHardRestore exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="abda2-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="abda2-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="abda2-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="abda2-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="abda2-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="abda2-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="abda2-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="abda2-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="abda2-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="abda2-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="abda2-110">Microsoft. ISAM. ESENT. Interop. Есентдатаексцептион</span><span class="sxs-lookup"><span data-stu-id="abda2-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="abda2-111">Microsoft. ISAM. ESENT. Interop. Есенткорруптионексцептион</span><span class="sxs-lookup"><span data-stu-id="abda2-111">Microsoft.Isam.Esent.Interop.EsentCorruptionException</span></span>](./esentcorruptionexception-class.md)  
            <span data-ttu-id="abda2-112">Microsoft. ISAM. ESENT. Interop. Есентлогторнвритедурингхардресториксцептион</span><span class="sxs-lookup"><span data-stu-id="abda2-112">Microsoft.Isam.Esent.Interop.EsentLogTornWriteDuringHardRestoreException</span></span>  

<span data-ttu-id="abda2-113">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="abda2-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="abda2-114">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="abda2-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="abda2-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="abda2-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentLogTornWriteDuringHardRestoreException _
    Inherits EsentCorruptionException
'Usage
Dim instance As EsentLogTornWriteDuringHardRestoreException
```

``` csharp
[SerializableAttribute]
public sealed class EsentLogTornWriteDuringHardRestoreException : EsentCorruptionException
```

## <a name="thread-safety"></a><span data-ttu-id="abda2-116">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="abda2-116">Thread safety</span></span>

<span data-ttu-id="abda2-117">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="abda2-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="abda2-118">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="abda2-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="abda2-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="abda2-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="abda2-120">Справочник</span><span class="sxs-lookup"><span data-stu-id="abda2-120">Reference</span></span>

[<span data-ttu-id="abda2-121">Элементы Есентлогторнвритедурингхардресториксцептион</span><span class="sxs-lookup"><span data-stu-id="abda2-121">EsentLogTornWriteDuringHardRestoreException members</span></span>](./esentlogtornwriteduringhardrestoreexception-members.md)

[<span data-ttu-id="abda2-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="abda2-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
