---
description: 'Дополнительные сведения о: Есентобжектдупликатиксцептион Class'
title: Класс Есентобжектдупликатиксцептион
TOCTitle: EsentObjectDuplicateException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentObjectDuplicateException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentobjectduplicateexception(v=EXCHG.10)
ms:contentKeyID: 55102411
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentObjectDuplicateException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentObjectDuplicateException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 25af4c5ca5654ed769a61afa19ad3afe8732ac54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702967"
---
# <a name="esentobjectduplicateexception-class"></a><span data-ttu-id="e1c7e-103">Класс Есентобжектдупликатиксцептион</span><span class="sxs-lookup"><span data-stu-id="e1c7e-103">EsentObjectDuplicateException class</span></span>

<span data-ttu-id="e1c7e-104">Базовый класс для JET_err. Исключения Обжектдупликате.</span><span class="sxs-lookup"><span data-stu-id="e1c7e-104">Base class for JET_err.ObjectDuplicate exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="e1c7e-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="e1c7e-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="e1c7e-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="e1c7e-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="e1c7e-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="e1c7e-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="e1c7e-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="e1c7e-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="e1c7e-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="e1c7e-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="e1c7e-110">Microsoft. ISAM. ESENT. Interop. Есентапиексцептион</span><span class="sxs-lookup"><span data-stu-id="e1c7e-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="e1c7e-111">Microsoft. ISAM. ESENT. Interop. Есентобсолетиксцептион</span><span class="sxs-lookup"><span data-stu-id="e1c7e-111">Microsoft.Isam.Esent.Interop.EsentObsoleteException</span></span>](./esentobsoleteexception-class.md)  
            <span data-ttu-id="e1c7e-112">Microsoft. ISAM. ESENT. Interop. Есентобжектдупликатиксцептион</span><span class="sxs-lookup"><span data-stu-id="e1c7e-112">Microsoft.Isam.Esent.Interop.EsentObjectDuplicateException</span></span>  

<span data-ttu-id="e1c7e-113">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e1c7e-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="e1c7e-114">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="e1c7e-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e1c7e-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e1c7e-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentObjectDuplicateException _
    Inherits EsentObsoleteException
'Usage
Dim instance As EsentObjectDuplicateException
```

``` csharp
[SerializableAttribute]
public sealed class EsentObjectDuplicateException : EsentObsoleteException
```

## <a name="thread-safety"></a><span data-ttu-id="e1c7e-116">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="e1c7e-116">Thread safety</span></span>

<span data-ttu-id="e1c7e-117">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="e1c7e-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="e1c7e-118">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="e1c7e-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="e1c7e-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e1c7e-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e1c7e-120">Справочник</span><span class="sxs-lookup"><span data-stu-id="e1c7e-120">Reference</span></span>

[<span data-ttu-id="e1c7e-121">Элементы Есентобжектдупликатиксцептион</span><span class="sxs-lookup"><span data-stu-id="e1c7e-121">EsentObjectDuplicateException members</span></span>](./esentobjectduplicateexception-members.md)

[<span data-ttu-id="e1c7e-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="e1c7e-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
