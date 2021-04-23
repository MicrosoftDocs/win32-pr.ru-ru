---
description: 'Дополнительные сведения о: Есентдатабасеунаваилабликсцептион Class'
title: Класс Есентдатабасеунаваилабликсцептион
TOCTitle: EsentDatabaseUnavailableException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDatabaseUnavailableException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdatabaseunavailableexception(v=EXCHG.10)
ms:contentKeyID: 55101562
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDatabaseUnavailableException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDatabaseUnavailableException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a3210a3d5a546d6c27294473137b0306f87f0888
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263762"
---
# <a name="esentdatabaseunavailableexception-class"></a><span data-ttu-id="7d450-103">Класс Есентдатабасеунаваилабликсцептион</span><span class="sxs-lookup"><span data-stu-id="7d450-103">EsentDatabaseUnavailableException class</span></span>

<span data-ttu-id="7d450-104">Базовый класс для JET_err. Исключения Датабасеунаваилабле.</span><span class="sxs-lookup"><span data-stu-id="7d450-104">Base class for JET_err.DatabaseUnavailable exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="7d450-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="7d450-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="7d450-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="7d450-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="7d450-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="7d450-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="7d450-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="7d450-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="7d450-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="7d450-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="7d450-110">Microsoft. ISAM. ESENT. Interop. Есентапиексцептион</span><span class="sxs-lookup"><span data-stu-id="7d450-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="7d450-111">Microsoft. ISAM. ESENT. Interop. Есентобсолетиксцептион</span><span class="sxs-lookup"><span data-stu-id="7d450-111">Microsoft.Isam.Esent.Interop.EsentObsoleteException</span></span>](./esentobsoleteexception-class.md)  
            <span data-ttu-id="7d450-112">Microsoft. ISAM. ESENT. Interop. Есентдатабасеунаваилабликсцептион</span><span class="sxs-lookup"><span data-stu-id="7d450-112">Microsoft.Isam.Esent.Interop.EsentDatabaseUnavailableException</span></span>  

<span data-ttu-id="7d450-113">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="7d450-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="7d450-114">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="7d450-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="7d450-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7d450-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentDatabaseUnavailableException _
    Inherits EsentObsoleteException
'Usage
Dim instance As EsentDatabaseUnavailableException
```

``` csharp
[SerializableAttribute]
public sealed class EsentDatabaseUnavailableException : EsentObsoleteException
```

## <a name="thread-safety"></a><span data-ttu-id="7d450-116">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="7d450-116">Thread safety</span></span>

<span data-ttu-id="7d450-117">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="7d450-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="7d450-118">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="7d450-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="7d450-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7d450-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="7d450-120">Справочник</span><span class="sxs-lookup"><span data-stu-id="7d450-120">Reference</span></span>

[<span data-ttu-id="7d450-121">Элементы Есентдатабасеунаваилабликсцептион</span><span class="sxs-lookup"><span data-stu-id="7d450-121">EsentDatabaseUnavailableException members</span></span>](./esentdatabaseunavailableexception-members.md)

[<span data-ttu-id="7d450-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="7d450-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
