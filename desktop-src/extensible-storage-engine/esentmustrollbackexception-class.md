---
description: 'Дополнительные сведения о: Есентмустроллбаккексцептион Class'
title: Класс Есентмустроллбаккексцептион
TOCTitle: EsentMustRollbackException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentMustRollbackException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentmustrollbackexception(v=EXCHG.10)
ms:contentKeyID: 55102335
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentMustRollbackException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentMustRollbackException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f7b5399db919b497579e25fae86de14003852fb8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544570"
---
# <a name="esentmustrollbackexception-class"></a><span data-ttu-id="85214-103">Класс Есентмустроллбаккексцептион</span><span class="sxs-lookup"><span data-stu-id="85214-103">EsentMustRollbackException class</span></span>

<span data-ttu-id="85214-104">Базовый класс для JET_err. Исключения Мустроллбакк.</span><span class="sxs-lookup"><span data-stu-id="85214-104">Base class for JET_err.MustRollback exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="85214-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="85214-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="85214-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="85214-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="85214-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="85214-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="85214-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="85214-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="85214-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="85214-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="85214-110">Microsoft. ISAM. ESENT. Interop. Есентапиексцептион</span><span class="sxs-lookup"><span data-stu-id="85214-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="85214-111">Microsoft. ISAM. ESENT. Interop. Есентусажеексцептион</span><span class="sxs-lookup"><span data-stu-id="85214-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="85214-112">Microsoft. ISAM. ESENT. Interop. Есентмустроллбаккексцептион</span><span class="sxs-lookup"><span data-stu-id="85214-112">Microsoft.Isam.Esent.Interop.EsentMustRollbackException</span></span>  

<span data-ttu-id="85214-113">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="85214-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="85214-114">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="85214-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="85214-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="85214-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentMustRollbackException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentMustRollbackException
```

``` csharp
[SerializableAttribute]
public sealed class EsentMustRollbackException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="85214-116">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="85214-116">Thread safety</span></span>

<span data-ttu-id="85214-117">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="85214-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="85214-118">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="85214-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="85214-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="85214-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="85214-120">Справочник</span><span class="sxs-lookup"><span data-stu-id="85214-120">Reference</span></span>

[<span data-ttu-id="85214-121">Элементы Есентмустроллбаккексцептион</span><span class="sxs-lookup"><span data-stu-id="85214-121">EsentMustRollbackException members</span></span>](./esentmustrollbackexception-members.md)

[<span data-ttu-id="85214-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="85214-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
