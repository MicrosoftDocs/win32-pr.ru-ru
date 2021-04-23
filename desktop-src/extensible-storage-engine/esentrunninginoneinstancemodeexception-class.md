---
description: 'Дополнительные сведения о: Есентруннингинонеинстанцемодиксцептион Class'
title: Класс Есентруннингинонеинстанцемодиксцептион
TOCTitle: EsentRunningInOneInstanceModeException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentRunningInOneInstanceModeException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentrunninginoneinstancemodeexception(v=EXCHG.10)
ms:contentKeyID: 55102675
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentRunningInOneInstanceModeException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentRunningInOneInstanceModeException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b764bd604076ee4dae1d3ee21d52c1d3b923407e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702963"
---
# <a name="esentrunninginoneinstancemodeexception-class"></a><span data-ttu-id="5574d-103">Класс Есентруннингинонеинстанцемодиксцептион</span><span class="sxs-lookup"><span data-stu-id="5574d-103">EsentRunningInOneInstanceModeException class</span></span>

<span data-ttu-id="5574d-104">Базовый класс для JET_err. Исключения Руннингинонеинстанцемоде.</span><span class="sxs-lookup"><span data-stu-id="5574d-104">Base class for JET_err.RunningInOneInstanceMode exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="5574d-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="5574d-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="5574d-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="5574d-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="5574d-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="5574d-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="5574d-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="5574d-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="5574d-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="5574d-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="5574d-110">Microsoft. ISAM. ESENT. Interop. Есентапиексцептион</span><span class="sxs-lookup"><span data-stu-id="5574d-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="5574d-111">Microsoft. ISAM. ESENT. Interop. Есентусажеексцептион</span><span class="sxs-lookup"><span data-stu-id="5574d-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="5574d-112">Microsoft. ISAM. ESENT. Interop. Есентруннингинонеинстанцемодиксцептион</span><span class="sxs-lookup"><span data-stu-id="5574d-112">Microsoft.Isam.Esent.Interop.EsentRunningInOneInstanceModeException</span></span>  

<span data-ttu-id="5574d-113">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="5574d-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="5574d-114">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="5574d-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="5574d-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5574d-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentRunningInOneInstanceModeException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentRunningInOneInstanceModeException
```

``` csharp
[SerializableAttribute]
public sealed class EsentRunningInOneInstanceModeException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="5574d-116">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="5574d-116">Thread safety</span></span>

<span data-ttu-id="5574d-117">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="5574d-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="5574d-118">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="5574d-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="5574d-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5574d-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="5574d-120">Справочник</span><span class="sxs-lookup"><span data-stu-id="5574d-120">Reference</span></span>

[<span data-ttu-id="5574d-121">Элементы Есентруннингинонеинстанцемодиксцептион</span><span class="sxs-lookup"><span data-stu-id="5574d-121">EsentRunningInOneInstanceModeException members</span></span>](./esentrunninginoneinstancemodeexception-members.md)

[<span data-ttu-id="5574d-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="5574d-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
