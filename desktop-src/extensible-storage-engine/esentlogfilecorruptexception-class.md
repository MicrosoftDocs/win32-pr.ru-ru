---
description: 'Дополнительные сведения о: Есентлогфилекорруптексцептион Class'
title: Класс Есентлогфилекорруптексцептион
TOCTitle: EsentLogFileCorruptException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentLogFileCorruptException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentlogfilecorruptexception(v=EXCHG.10)
ms:contentKeyID: 55102161
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentLogFileCorruptException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentLogFileCorruptException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f2a3fa54d83cd1e88597b3689619e48a2372952e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712009"
---
# <a name="esentlogfilecorruptexception-class"></a><span data-ttu-id="4a43f-103">Класс Есентлогфилекорруптексцептион</span><span class="sxs-lookup"><span data-stu-id="4a43f-103">EsentLogFileCorruptException class</span></span>

<span data-ttu-id="4a43f-104">Базовый класс для JET_err. Исключения Логфилекоррупт.</span><span class="sxs-lookup"><span data-stu-id="4a43f-104">Base class for JET_err.LogFileCorrupt exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="4a43f-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="4a43f-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="4a43f-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="4a43f-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="4a43f-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="4a43f-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="4a43f-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="4a43f-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="4a43f-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="4a43f-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="4a43f-110">Microsoft. ISAM. ESENT. Interop. Есентдатаексцептион</span><span class="sxs-lookup"><span data-stu-id="4a43f-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="4a43f-111">Microsoft. ISAM. ESENT. Interop. Есенткорруптионексцептион</span><span class="sxs-lookup"><span data-stu-id="4a43f-111">Microsoft.Isam.Esent.Interop.EsentCorruptionException</span></span>](./esentcorruptionexception-class.md)  
            <span data-ttu-id="4a43f-112">Microsoft. ISAM. ESENT. Interop. Есентлогфилекорруптексцептион</span><span class="sxs-lookup"><span data-stu-id="4a43f-112">Microsoft.Isam.Esent.Interop.EsentLogFileCorruptException</span></span>  

<span data-ttu-id="4a43f-113">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="4a43f-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="4a43f-114">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="4a43f-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="4a43f-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4a43f-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentLogFileCorruptException _
    Inherits EsentCorruptionException
'Usage
Dim instance As EsentLogFileCorruptException
```

``` csharp
[SerializableAttribute]
public sealed class EsentLogFileCorruptException : EsentCorruptionException
```

## <a name="thread-safety"></a><span data-ttu-id="4a43f-116">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="4a43f-116">Thread safety</span></span>

<span data-ttu-id="4a43f-117">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="4a43f-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="4a43f-118">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="4a43f-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="4a43f-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4a43f-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="4a43f-120">Справочник</span><span class="sxs-lookup"><span data-stu-id="4a43f-120">Reference</span></span>

[<span data-ttu-id="4a43f-121">Элементы Есентлогфилекорруптексцептион</span><span class="sxs-lookup"><span data-stu-id="4a43f-121">EsentLogFileCorruptException members</span></span>](./esentlogfilecorruptexception-members.md)

[<span data-ttu-id="4a43f-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="4a43f-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
