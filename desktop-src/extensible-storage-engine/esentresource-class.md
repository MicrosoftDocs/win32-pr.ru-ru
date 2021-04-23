---
description: 'Дополнительные сведения о: Есентресаурце Class'
title: Класс Есентресаурце
TOCTitle: EsentResource class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentResource
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentresource(v=EXCHG.10)
ms:contentKeyID: 55102575
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentResource
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentResource
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 607fb59d6f9f89c33e685ed411ae9dc95eaa6818
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711233"
---
# <a name="esentresource-class"></a><span data-ttu-id="5adc7-103">Класс Есентресаурце</span><span class="sxs-lookup"><span data-stu-id="5adc7-103">EsentResource class</span></span>

<span data-ttu-id="5adc7-104">Это базовый класс для всех объектов ресурсов ESENT.</span><span class="sxs-lookup"><span data-stu-id="5adc7-104">This is the base class for all esent resource objects.</span></span> <span data-ttu-id="5adc7-105">Подклассы этого класса могут распределять и освобождать неуправляемые ресурсы.</span><span class="sxs-lookup"><span data-stu-id="5adc7-105">Subclasses of this class can allocate and release unmanaged resources.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="5adc7-106">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="5adc7-106">Inheritance hierarchy</span></span>

[<span data-ttu-id="5adc7-107">System.Object</span><span class="sxs-lookup"><span data-stu-id="5adc7-107">System.Object</span></span>](/dotnet/api/system.object)  
  <span data-ttu-id="5adc7-108">Microsoft. ISAM. ESENT. Interop. Есентресаурце</span><span class="sxs-lookup"><span data-stu-id="5adc7-108">Microsoft.Isam.Esent.Interop.EsentResource</span></span>  
    [<span data-ttu-id="5adc7-109">Microsoft. ISAM. ESENT. Interop. Session</span><span class="sxs-lookup"><span data-stu-id="5adc7-109">Microsoft.Isam.Esent.Interop.Session</span></span>](./session-class.md)  
    [<span data-ttu-id="5adc7-110">Microsoft. ISAM. ESENT. Interop. Table</span><span class="sxs-lookup"><span data-stu-id="5adc7-110">Microsoft.Isam.Esent.Interop.Table</span></span>](./table-class.md)  
    [<span data-ttu-id="5adc7-111">Microsoft. ISAM. ESENT. Interop. Transaction</span><span class="sxs-lookup"><span data-stu-id="5adc7-111">Microsoft.Isam.Esent.Interop.Transaction</span></span>](./transaction-class.md)  
    [<span data-ttu-id="5adc7-112">Microsoft. ISAM. ESENT. Interop. Update</span><span class="sxs-lookup"><span data-stu-id="5adc7-112">Microsoft.Isam.Esent.Interop.Update</span></span>](./update-class.md)  
    [<span data-ttu-id="5adc7-113">Microsoft. ISAM. ESENT. Interop. Windows8. Дураблекоммиткаллбакк</span><span class="sxs-lookup"><span data-stu-id="5adc7-113">Microsoft.Isam.Esent.Interop.Windows8.DurableCommitCallback</span></span>](./durablecommitcallback-class.md)  

<span data-ttu-id="5adc7-114">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="5adc7-114">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="5adc7-115">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="5adc7-115">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="5adc7-116">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5adc7-116">Syntax</span></span>

``` vb
'Declaration
Public MustInherit Class EsentResource _
    Implements IDisposable
'Usage
Dim instance As EsentResource
```

``` csharp
public abstract class EsentResource : IDisposable
```

## <a name="thread-safety"></a><span data-ttu-id="5adc7-117">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="5adc7-117">Thread safety</span></span>

<span data-ttu-id="5adc7-118">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="5adc7-118">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="5adc7-119">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="5adc7-119">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="5adc7-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5adc7-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="5adc7-121">Справочник</span><span class="sxs-lookup"><span data-stu-id="5adc7-121">Reference</span></span>

[<span data-ttu-id="5adc7-122">Элементы Есентресаурце</span><span class="sxs-lookup"><span data-stu-id="5adc7-122">EsentResource members</span></span>](./esentresource-members.md)

[<span data-ttu-id="5adc7-123">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="5adc7-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
