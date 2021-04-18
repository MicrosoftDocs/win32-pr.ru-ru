---
description: 'Дополнительные сведения о: Есентдатабасеинкомплетеупградиксцептион Class'
title: Класс Есентдатабасеинкомплетеупградиксцептион
TOCTitle: EsentDatabaseIncompleteUpgradeException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDatabaseIncompleteUpgradeException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdatabaseincompleteupgradeexception(v=EXCHG.10)
ms:contentKeyID: 55101371
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDatabaseIncompleteUpgradeException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDatabaseIncompleteUpgradeException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8ae6272559c537ae870794a9d5a7a76bb8672b26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711171"
---
# <a name="esentdatabaseincompleteupgradeexception-class"></a><span data-ttu-id="168bb-103">Класс Есентдатабасеинкомплетеупградиксцептион</span><span class="sxs-lookup"><span data-stu-id="168bb-103">EsentDatabaseIncompleteUpgradeException class</span></span>

<span data-ttu-id="168bb-104">Базовый класс для JET_err. Исключения Датабасеинкомплетеупграде.</span><span class="sxs-lookup"><span data-stu-id="168bb-104">Base class for JET_err.DatabaseIncompleteUpgrade exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="168bb-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="168bb-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="168bb-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="168bb-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="168bb-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="168bb-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="168bb-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="168bb-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="168bb-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="168bb-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="168bb-110">Microsoft. ISAM. ESENT. Interop. Есентапиексцептион</span><span class="sxs-lookup"><span data-stu-id="168bb-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="168bb-111">Microsoft. ISAM. ESENT. Interop. Есентстатиксцептион</span><span class="sxs-lookup"><span data-stu-id="168bb-111">Microsoft.Isam.Esent.Interop.EsentStateException</span></span>](./esentstateexception-class.md)  
            <span data-ttu-id="168bb-112">Microsoft. ISAM. ESENT. Interop. Есентдатабасеинкомплетеупградиксцептион</span><span class="sxs-lookup"><span data-stu-id="168bb-112">Microsoft.Isam.Esent.Interop.EsentDatabaseIncompleteUpgradeException</span></span>  

<span data-ttu-id="168bb-113">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="168bb-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="168bb-114">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="168bb-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="168bb-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="168bb-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentDatabaseIncompleteUpgradeException _
    Inherits EsentStateException
'Usage
Dim instance As EsentDatabaseIncompleteUpgradeException
```

``` csharp
[SerializableAttribute]
public sealed class EsentDatabaseIncompleteUpgradeException : EsentStateException
```

## <a name="thread-safety"></a><span data-ttu-id="168bb-116">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="168bb-116">Thread safety</span></span>

<span data-ttu-id="168bb-117">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="168bb-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="168bb-118">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="168bb-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="168bb-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="168bb-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="168bb-120">Справочник</span><span class="sxs-lookup"><span data-stu-id="168bb-120">Reference</span></span>

[<span data-ttu-id="168bb-121">Элементы Есентдатабасеинкомплетеупградиксцептион</span><span class="sxs-lookup"><span data-stu-id="168bb-121">EsentDatabaseIncompleteUpgradeException members</span></span>](./esentdatabaseincompleteupgradeexception-members.md)

[<span data-ttu-id="168bb-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="168bb-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
