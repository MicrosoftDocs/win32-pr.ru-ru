---
description: 'Дополнительные сведения о: Есентрековередвисаутундодатабасесконсистентексцептион Class'
title: Класс Есентрековередвисаутундодатабасесконсистентексцептион
TOCTitle: EsentRecoveredWithoutUndoDatabasesConsistentException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentRecoveredWithoutUndoDatabasesConsistentException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentrecoveredwithoutundodatabasesconsistentexception(v=EXCHG.10)
ms:contentKeyID: 55102610
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentRecoveredWithoutUndoDatabasesConsistentException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentRecoveredWithoutUndoDatabasesConsistentException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6e874fb436ae30fe8e393b21d48c560a8ad6e92f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262966"
---
# <a name="esentrecoveredwithoutundodatabasesconsistentexception-class"></a><span data-ttu-id="f39a1-103">Класс Есентрековередвисаутундодатабасесконсистентексцептион</span><span class="sxs-lookup"><span data-stu-id="f39a1-103">EsentRecoveredWithoutUndoDatabasesConsistentException class</span></span>

<span data-ttu-id="f39a1-104">Базовый класс для JET_err. Исключения Рековередвисаутундодатабасесконсистент.</span><span class="sxs-lookup"><span data-stu-id="f39a1-104">Base class for JET_err.RecoveredWithoutUndoDatabasesConsistent exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="f39a1-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="f39a1-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="f39a1-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="f39a1-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="f39a1-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="f39a1-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="f39a1-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="f39a1-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="f39a1-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="f39a1-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="f39a1-110">Microsoft. ISAM. ESENT. Interop. Есентапиексцептион</span><span class="sxs-lookup"><span data-stu-id="f39a1-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="f39a1-111">Microsoft. ISAM. ESENT. Interop. Есентстатиксцептион</span><span class="sxs-lookup"><span data-stu-id="f39a1-111">Microsoft.Isam.Esent.Interop.EsentStateException</span></span>](./esentstateexception-class.md)  
            <span data-ttu-id="f39a1-112">Microsoft. ISAM. ESENT. Interop. Есентрековередвисаутундодатабасесконсистентексцептион</span><span class="sxs-lookup"><span data-stu-id="f39a1-112">Microsoft.Isam.Esent.Interop.EsentRecoveredWithoutUndoDatabasesConsistentException</span></span>  

<span data-ttu-id="f39a1-113">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f39a1-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f39a1-114">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="f39a1-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f39a1-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f39a1-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentRecoveredWithoutUndoDatabasesConsistentException _
    Inherits EsentStateException
'Usage
Dim instance As EsentRecoveredWithoutUndoDatabasesConsistentException
```

``` csharp
[SerializableAttribute]
public sealed class EsentRecoveredWithoutUndoDatabasesConsistentException : EsentStateException
```

## <a name="thread-safety"></a><span data-ttu-id="f39a1-116">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="f39a1-116">Thread safety</span></span>

<span data-ttu-id="f39a1-117">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="f39a1-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="f39a1-118">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="f39a1-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="f39a1-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f39a1-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f39a1-120">Справочник</span><span class="sxs-lookup"><span data-stu-id="f39a1-120">Reference</span></span>

[<span data-ttu-id="f39a1-121">Элементы Есентрековередвисаутундодатабасесконсистентексцептион</span><span class="sxs-lookup"><span data-stu-id="f39a1-121">EsentRecoveredWithoutUndoDatabasesConsistentException members</span></span>](./esentrecoveredwithoutundodatabasesconsistentexception-members.md)

[<span data-ttu-id="f39a1-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="f39a1-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
