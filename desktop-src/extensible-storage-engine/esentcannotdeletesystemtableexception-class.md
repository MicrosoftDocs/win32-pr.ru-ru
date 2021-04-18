---
description: 'Дополнительные сведения о: Есентканнотделетесистемтабликсцептион Class'
title: Класс Есентканнотделетесистемтабликсцептион
TOCTitle: EsentCannotDeleteSystemTableException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentCannotDeleteSystemTableException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentcannotdeletesystemtableexception(v=EXCHG.10)
ms:contentKeyID: 55101231
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentCannotDeleteSystemTableException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentCannotDeleteSystemTableException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9b6d05a6a4a24da1233993f7ca260fc609e73147
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702877"
---
# <a name="esentcannotdeletesystemtableexception-class"></a><span data-ttu-id="e2c10-103">Класс Есентканнотделетесистемтабликсцептион</span><span class="sxs-lookup"><span data-stu-id="e2c10-103">EsentCannotDeleteSystemTableException class</span></span>

<span data-ttu-id="e2c10-104">Базовый класс для JET_err. Исключения Каннотделетесистемтабле.</span><span class="sxs-lookup"><span data-stu-id="e2c10-104">Base class for JET_err.CannotDeleteSystemTable exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="e2c10-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="e2c10-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="e2c10-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="e2c10-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="e2c10-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="e2c10-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="e2c10-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="e2c10-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="e2c10-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="e2c10-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="e2c10-110">Microsoft. ISAM. ESENT. Interop. Есентапиексцептион</span><span class="sxs-lookup"><span data-stu-id="e2c10-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="e2c10-111">Microsoft. ISAM. ESENT. Interop. Есентусажеексцептион</span><span class="sxs-lookup"><span data-stu-id="e2c10-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="e2c10-112">Microsoft. ISAM. ESENT. Interop. Есентканнотделетесистемтабликсцептион</span><span class="sxs-lookup"><span data-stu-id="e2c10-112">Microsoft.Isam.Esent.Interop.EsentCannotDeleteSystemTableException</span></span>  

<span data-ttu-id="e2c10-113">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e2c10-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="e2c10-114">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="e2c10-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e2c10-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e2c10-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentCannotDeleteSystemTableException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentCannotDeleteSystemTableException
```

``` csharp
[SerializableAttribute]
public sealed class EsentCannotDeleteSystemTableException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="e2c10-116">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="e2c10-116">Thread safety</span></span>

<span data-ttu-id="e2c10-117">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="e2c10-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="e2c10-118">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="e2c10-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="e2c10-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e2c10-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e2c10-120">Справочник</span><span class="sxs-lookup"><span data-stu-id="e2c10-120">Reference</span></span>

[<span data-ttu-id="e2c10-121">Элементы Есентканнотделетесистемтабликсцептион</span><span class="sxs-lookup"><span data-stu-id="e2c10-121">EsentCannotDeleteSystemTableException members</span></span>](./esentcannotdeletesystemtableexception-members.md)

[<span data-ttu-id="e2c10-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="e2c10-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
