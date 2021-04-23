---
description: 'Дополнительные сведения о: Есентлогкорруптдурингхардрековерексцептион Class'
title: Класс Есентлогкорруптдурингхардрековерексцептион
TOCTitle: EsentLogCorruptDuringHardRecoveryException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentLogCorruptDuringHardRecoveryException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentlogcorruptduringhardrecoveryexception(v=EXCHG.10)
ms:contentKeyID: 55102063
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentLogCorruptDuringHardRecoveryException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentLogCorruptDuringHardRecoveryException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: da137553a791b92a929d60dc9cc9cd764695c784
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105719722"
---
# <a name="esentlogcorruptduringhardrecoveryexception-class"></a><span data-ttu-id="1c4a5-103">Класс Есентлогкорруптдурингхардрековерексцептион</span><span class="sxs-lookup"><span data-stu-id="1c4a5-103">EsentLogCorruptDuringHardRecoveryException class</span></span>

<span data-ttu-id="1c4a5-104">Базовый класс для JET_err. Исключения Логкорруптдурингхардрековери.</span><span class="sxs-lookup"><span data-stu-id="1c4a5-104">Base class for JET_err.LogCorruptDuringHardRecovery exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="1c4a5-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="1c4a5-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="1c4a5-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="1c4a5-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="1c4a5-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="1c4a5-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="1c4a5-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="1c4a5-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="1c4a5-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="1c4a5-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="1c4a5-110">Microsoft. ISAM. ESENT. Interop. Есентдатаексцептион</span><span class="sxs-lookup"><span data-stu-id="1c4a5-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="1c4a5-111">Microsoft. ISAM. ESENT. Interop. Есенткорруптионексцептион</span><span class="sxs-lookup"><span data-stu-id="1c4a5-111">Microsoft.Isam.Esent.Interop.EsentCorruptionException</span></span>](./esentcorruptionexception-class.md)  
            <span data-ttu-id="1c4a5-112">Microsoft. ISAM. ESENT. Interop. Есентлогкорруптдурингхардрековерексцептион</span><span class="sxs-lookup"><span data-stu-id="1c4a5-112">Microsoft.Isam.Esent.Interop.EsentLogCorruptDuringHardRecoveryException</span></span>  

<span data-ttu-id="1c4a5-113">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="1c4a5-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="1c4a5-114">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="1c4a5-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="1c4a5-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1c4a5-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentLogCorruptDuringHardRecoveryException _
    Inherits EsentCorruptionException
'Usage
Dim instance As EsentLogCorruptDuringHardRecoveryException
```

``` csharp
[SerializableAttribute]
public sealed class EsentLogCorruptDuringHardRecoveryException : EsentCorruptionException
```

## <a name="thread-safety"></a><span data-ttu-id="1c4a5-116">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="1c4a5-116">Thread safety</span></span>

<span data-ttu-id="1c4a5-117">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="1c4a5-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="1c4a5-118">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="1c4a5-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="1c4a5-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1c4a5-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="1c4a5-120">Справочник</span><span class="sxs-lookup"><span data-stu-id="1c4a5-120">Reference</span></span>

[<span data-ttu-id="1c4a5-121">Элементы Есентлогкорруптдурингхардрековерексцептион</span><span class="sxs-lookup"><span data-stu-id="1c4a5-121">EsentLogCorruptDuringHardRecoveryException members</span></span>](./esentlogcorruptduringhardrecoveryexception-members.md)

[<span data-ttu-id="1c4a5-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="1c4a5-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
