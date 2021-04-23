---
description: 'Дополнительные сведения о: Есентдатабасеидинусиксцептион Class'
title: Класс Есентдатабасеидинусиксцептион
TOCTitle: EsentDatabaseIdInUseException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDatabaseIdInUseException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdatabaseidinuseexception(v=EXCHG.10)
ms:contentKeyID: 55101458
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDatabaseIdInUseException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDatabaseIdInUseException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 26788132dc36cbddbd2d891746c86045182a1e80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711173"
---
# <a name="esentdatabaseidinuseexception-class"></a><span data-ttu-id="08dff-103">Класс Есентдатабасеидинусиксцептион</span><span class="sxs-lookup"><span data-stu-id="08dff-103">EsentDatabaseIdInUseException class</span></span>

<span data-ttu-id="08dff-104">Базовый класс для JET_err. Исключения Датабасеидинусе.</span><span class="sxs-lookup"><span data-stu-id="08dff-104">Base class for JET_err.DatabaseIdInUse exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="08dff-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="08dff-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="08dff-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="08dff-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="08dff-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="08dff-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="08dff-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="08dff-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="08dff-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="08dff-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="08dff-110">Microsoft. ISAM. ESENT. Interop. Есентапиексцептион</span><span class="sxs-lookup"><span data-stu-id="08dff-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="08dff-111">Microsoft. ISAM. ESENT. Interop. Есентобсолетиксцептион</span><span class="sxs-lookup"><span data-stu-id="08dff-111">Microsoft.Isam.Esent.Interop.EsentObsoleteException</span></span>](./esentobsoleteexception-class.md)  
            <span data-ttu-id="08dff-112">Microsoft. ISAM. ESENT. Interop. Есентдатабасеидинусиксцептион</span><span class="sxs-lookup"><span data-stu-id="08dff-112">Microsoft.Isam.Esent.Interop.EsentDatabaseIdInUseException</span></span>  

<span data-ttu-id="08dff-113">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="08dff-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="08dff-114">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="08dff-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="08dff-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="08dff-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentDatabaseIdInUseException _
    Inherits EsentObsoleteException
'Usage
Dim instance As EsentDatabaseIdInUseException
```

``` csharp
[SerializableAttribute]
public sealed class EsentDatabaseIdInUseException : EsentObsoleteException
```

## <a name="thread-safety"></a><span data-ttu-id="08dff-116">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="08dff-116">Thread safety</span></span>

<span data-ttu-id="08dff-117">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="08dff-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="08dff-118">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="08dff-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="08dff-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="08dff-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="08dff-120">Справочник</span><span class="sxs-lookup"><span data-stu-id="08dff-120">Reference</span></span>

[<span data-ttu-id="08dff-121">Элементы Есентдатабасеидинусиксцептион</span><span class="sxs-lookup"><span data-stu-id="08dff-121">EsentDatabaseIdInUseException members</span></span>](./esentdatabaseidinuseexception-members.md)

[<span data-ttu-id="08dff-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="08dff-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
