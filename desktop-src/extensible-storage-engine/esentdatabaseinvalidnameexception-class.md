---
description: 'Дополнительные сведения о: Есентдатабасеинвалиднамиксцептион Class'
title: Класс Есентдатабасеинвалиднамиксцептион
TOCTitle: EsentDatabaseInvalidNameException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDatabaseInvalidNameException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdatabaseinvalidnameexception(v=EXCHG.10)
ms:contentKeyID: 55101502
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDatabaseInvalidNameException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDatabaseInvalidNameException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1754ed199986a048d188a5cd6a5927f8e3307867
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541095"
---
# <a name="esentdatabaseinvalidnameexception-class"></a><span data-ttu-id="881fe-103">Класс Есентдатабасеинвалиднамиксцептион</span><span class="sxs-lookup"><span data-stu-id="881fe-103">EsentDatabaseInvalidNameException class</span></span>

<span data-ttu-id="881fe-104">Базовый класс для JET_err. Исключения Датабасеинвалиднаме.</span><span class="sxs-lookup"><span data-stu-id="881fe-104">Base class for JET_err.DatabaseInvalidName exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="881fe-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="881fe-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="881fe-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="881fe-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="881fe-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="881fe-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="881fe-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="881fe-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="881fe-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="881fe-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="881fe-110">Microsoft. ISAM. ESENT. Interop. Есентапиексцептион</span><span class="sxs-lookup"><span data-stu-id="881fe-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="881fe-111">Microsoft. ISAM. ESENT. Interop. Есентусажеексцептион</span><span class="sxs-lookup"><span data-stu-id="881fe-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="881fe-112">Microsoft. ISAM. ESENT. Interop. Есентдатабасеинвалиднамиксцептион</span><span class="sxs-lookup"><span data-stu-id="881fe-112">Microsoft.Isam.Esent.Interop.EsentDatabaseInvalidNameException</span></span>  

<span data-ttu-id="881fe-113">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="881fe-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="881fe-114">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="881fe-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="881fe-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="881fe-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentDatabaseInvalidNameException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentDatabaseInvalidNameException
```

``` csharp
[SerializableAttribute]
public sealed class EsentDatabaseInvalidNameException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="881fe-116">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="881fe-116">Thread safety</span></span>

<span data-ttu-id="881fe-117">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="881fe-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="881fe-118">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="881fe-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="881fe-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="881fe-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="881fe-120">Справочник</span><span class="sxs-lookup"><span data-stu-id="881fe-120">Reference</span></span>

[<span data-ttu-id="881fe-121">Элементы Есентдатабасеинвалиднамиксцептион</span><span class="sxs-lookup"><span data-stu-id="881fe-121">EsentDatabaseInvalidNameException members</span></span>](./esentdatabaseinvalidnameexception-members.md)

[<span data-ttu-id="881fe-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="881fe-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
