---
description: 'Дополнительные сведения о: Есентлогсекуенцеенддатабасесконсистентексцептион Class'
title: Класс Есентлогсекуенцеенддатабасесконсистентексцептион
TOCTitle: EsentLogSequenceEndDatabasesConsistentException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentLogSequenceEndDatabasesConsistentException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentlogsequenceenddatabasesconsistentexception(v=EXCHG.10)
ms:contentKeyID: 55102212
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentLogSequenceEndDatabasesConsistentException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentLogSequenceEndDatabasesConsistentException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bb1663f80d4b233670852f80b06c405a1bab0207
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703291"
---
# <a name="esentlogsequenceenddatabasesconsistentexception-class"></a><span data-ttu-id="61edc-103">Класс Есентлогсекуенцеенддатабасесконсистентексцептион</span><span class="sxs-lookup"><span data-stu-id="61edc-103">EsentLogSequenceEndDatabasesConsistentException class</span></span>

<span data-ttu-id="61edc-104">Базовый класс для JET_err. Исключения Логсекуенцеенддатабасесконсистент.</span><span class="sxs-lookup"><span data-stu-id="61edc-104">Base class for JET_err.LogSequenceEndDatabasesConsistent exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="61edc-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="61edc-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="61edc-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="61edc-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="61edc-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="61edc-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="61edc-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="61edc-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="61edc-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="61edc-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="61edc-110">Microsoft. ISAM. ESENT. Interop. Есентдатаексцептион</span><span class="sxs-lookup"><span data-stu-id="61edc-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="61edc-111">Microsoft. ISAM. ESENT. Interop. Есентфрагментатионексцептион</span><span class="sxs-lookup"><span data-stu-id="61edc-111">Microsoft.Isam.Esent.Interop.EsentFragmentationException</span></span>](./esentfragmentationexception-class.md)  
            <span data-ttu-id="61edc-112">Microsoft. ISAM. ESENT. Interop. Есентлогсекуенцеенддатабасесконсистентексцептион</span><span class="sxs-lookup"><span data-stu-id="61edc-112">Microsoft.Isam.Esent.Interop.EsentLogSequenceEndDatabasesConsistentException</span></span>  

<span data-ttu-id="61edc-113">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="61edc-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="61edc-114">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="61edc-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="61edc-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="61edc-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentLogSequenceEndDatabasesConsistentException _
    Inherits EsentFragmentationException
'Usage
Dim instance As EsentLogSequenceEndDatabasesConsistentException
```

``` csharp
[SerializableAttribute]
public sealed class EsentLogSequenceEndDatabasesConsistentException : EsentFragmentationException
```

## <a name="thread-safety"></a><span data-ttu-id="61edc-116">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="61edc-116">Thread safety</span></span>

<span data-ttu-id="61edc-117">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="61edc-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="61edc-118">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="61edc-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="61edc-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="61edc-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="61edc-120">Справочник</span><span class="sxs-lookup"><span data-stu-id="61edc-120">Reference</span></span>

[<span data-ttu-id="61edc-121">Элементы Есентлогсекуенцеенддатабасесконсистентексцептион</span><span class="sxs-lookup"><span data-stu-id="61edc-121">EsentLogSequenceEndDatabasesConsistentException members</span></span>](./esentlogsequenceenddatabasesconsistentexception-members.md)

[<span data-ttu-id="61edc-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="61edc-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
