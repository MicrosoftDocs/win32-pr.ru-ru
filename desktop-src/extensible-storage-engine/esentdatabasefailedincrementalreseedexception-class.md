---
description: 'Дополнительные сведения о: Есентдатабасефаилединкременталресидексцептион Class'
title: Класс Есентдатабасефаилединкременталресидексцептион
TOCTitle: EsentDatabaseFailedIncrementalReseedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDatabaseFailedIncrementalReseedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdatabasefailedincrementalreseedexception(v=EXCHG.10)
ms:contentKeyID: 55101465
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDatabaseFailedIncrementalReseedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDatabaseFailedIncrementalReseedException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cfa0f4a82e3a8936ee3e7a262f8079396b95a54a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104145670"
---
# <a name="esentdatabasefailedincrementalreseedexception-class"></a><span data-ttu-id="fd9bf-103">Класс Есентдатабасефаилединкременталресидексцептион</span><span class="sxs-lookup"><span data-stu-id="fd9bf-103">EsentDatabaseFailedIncrementalReseedException class</span></span>

<span data-ttu-id="fd9bf-104">Базовый класс для JET_err. Исключения Датабасефаилединкременталресид.</span><span class="sxs-lookup"><span data-stu-id="fd9bf-104">Base class for JET_err.DatabaseFailedIncrementalReseed exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="fd9bf-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="fd9bf-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="fd9bf-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="fd9bf-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="fd9bf-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="fd9bf-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="fd9bf-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="fd9bf-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="fd9bf-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="fd9bf-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="fd9bf-110">Microsoft. ISAM. ESENT. Interop. Есентапиексцептион</span><span class="sxs-lookup"><span data-stu-id="fd9bf-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="fd9bf-111">Microsoft. ISAM. ESENT. Interop. Есентстатиксцептион</span><span class="sxs-lookup"><span data-stu-id="fd9bf-111">Microsoft.Isam.Esent.Interop.EsentStateException</span></span>](./esentstateexception-class.md)  
            <span data-ttu-id="fd9bf-112">Microsoft. ISAM. ESENT. Interop. Есентдатабасефаилединкременталресидексцептион</span><span class="sxs-lookup"><span data-stu-id="fd9bf-112">Microsoft.Isam.Esent.Interop.EsentDatabaseFailedIncrementalReseedException</span></span>  

<span data-ttu-id="fd9bf-113">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="fd9bf-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="fd9bf-114">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="fd9bf-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="fd9bf-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fd9bf-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentDatabaseFailedIncrementalReseedException _
    Inherits EsentStateException
'Usage
Dim instance As EsentDatabaseFailedIncrementalReseedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentDatabaseFailedIncrementalReseedException : EsentStateException
```

## <a name="thread-safety"></a><span data-ttu-id="fd9bf-116">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="fd9bf-116">Thread safety</span></span>

<span data-ttu-id="fd9bf-117">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="fd9bf-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="fd9bf-118">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="fd9bf-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="fd9bf-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fd9bf-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="fd9bf-120">Справочник</span><span class="sxs-lookup"><span data-stu-id="fd9bf-120">Reference</span></span>

[<span data-ttu-id="fd9bf-121">Элементы Есентдатабасефаилединкременталресидексцептион</span><span class="sxs-lookup"><span data-stu-id="fd9bf-121">EsentDatabaseFailedIncrementalReseedException members</span></span>](./esentdatabasefailedincrementalreseedexception-members.md)

[<span data-ttu-id="fd9bf-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="fd9bf-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
